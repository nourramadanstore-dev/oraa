# AUDIT_SHOPIFY_EXISTANT.md — État de l'existant à l'ouverture du projet

**Date de l'audit** : 2026-08-07
**Portée** : catalogue produits + collections. Thème non couvert (accès non disponible via le connecteur utilisé).
**Mode** : lecture seule, aucune modification effectuée.
**Contexte** : boutique `oraa-6632.myshopify.com`, plan Basic, **0 commande à date** — pré-lancement.

Ce document est la mémoire de référence de l'état du catalogue *avant* toute migration vers l'architecture cible (`TAXONOMY.md`). Il ne doit pas être modifié rétroactivement — c'est un instantané, pas un document vivant. Le suivi de l'avancement de la migration se fait dans `MIGRATION_PLAN.md`.

---

## 1. Produits (21 au total)

### Actifs — cœur de gamme (8)

| Produit | Prix | Cohérence mission | Constat |
|---|---|---|---|
| Enceinte Coranique Lune 3D | 44,90 € | ✅ | RAS |
| Horloge Azan Bluetooth | 28,68–47,90 € | ✅ | Anomalie de prix entre variantes non expliquée |
| Brûleur d'Encens Coranique SQ-600 | 34,90 € | ✅ | RAS |
| Lampe de Nuit Coranique Portable | 24,90 € | ✅ | Stock critique : 2 unités |
| Horloge Adhan Lumineuse Blanche | 44,90 € | ✅ | RAS |
| Horloge Coranique Adhan (multicolore) | 39,90 € | ✅ | Stock faible : 8 unités |
| Bague Connectée Zikr et Qibla | 12,86–79,90 € (24 variantes) | ✅ | Anomalie de prix majeure, probable import fournisseur corrompu |
| Haut-parleur Coranique Magnétique | 10,12–27,90 € (16 variantes) | ✅ | Même type d'anomalie |

**Constat commun aux 8** : aucun `Product Type`, aucun tag renseigné.

### Brouillons — nouvelle génération (4)

| Produit | Prix | Constat |
|---|---|---|
| Horloge Adhan Al-Fatiha | 69,90 € | Structure exemplaire (tags, Product Type) mais aucune image, stock 0 |
| Veilleuse 3D Kaaba | 19,90 € | Idem |
| Enceinte Coranique Enfant | 34,90 € | Idem — comble un segment absent du catalogue actif |
| Pack Maison (bundle) | 89,90 € | Idem — aucun lien structurel vers ses composants |

### Archivés — hors mission (9)

Robot aspirateur, cape de coiffure, téléviseur, parasols/éventails, ventilateur climatiseur, machine de rajeunissement facial, ensemble de nettoyage de voyage.

**Statut** : reliquat d'un dropshipping générique antérieur au pivot vers le positionnement spirituel d'ORAA. **Conservés archivés, suppression définitive non validée par l'utilisateur.**

---

## 2. Collections (18 au total)

| Collection | Handle | Produits | Constat |
|---|---|---|---|
| Page d'accueil | `frontpage` | 0 | Vide |
| Packs Promo | `pack-et-promotion` | 1 | Doublon avec "Les Packs ORAA" et "Packs & Offres" |
| High-Tech | `maison` | 2 | Titre et handle décorrélés |
| Foyer | `foyer` | 12 | — |
| Hygiène | `hygiene-1` | 3 | Reliquat de duplication |
| Maison | `maison-1` | 5 | Reliquat de duplication, chevauche "Foyer" |
| Les Nouveautés | — | 0 | Vide |
| Les Coups de cœur ORAA | — | 0 | Vide |
| Les Packs ORAA | — | 1 | Doublon |
| Les Box ORAA | — | 0 | Vide |
| Maison & Hygiène | — | 0 | Vide, chevauche Maison + Hygiène |
| Mode | — | 0 | Vide — cohérence mission tranchée : catégorie roadmap (voir TAXONOMY.md §11) |
| Enfants & Bébés | — | 0 | Vide — segment prometteur, produit brouillon déjà existant |
| Foi & Transmission | — | 11 | Nom aligné mission, bien peuplée |
| Cadeaux & Box | — | 0 | Vide |
| Voyage & Aventure | — | 0 | Vide — cohérence mission tranchée : catégorie roadmap (voir TAXONOMY.md §11) |
| Tech & Accessoires | — | 8 | Bien peuplée |
| Packs & Offres | — | 1 | Troisième doublon du concept "packs" |

**Constat central** : 10 collections sur 18 vides. Deux architectures d'information superposées et jamais fusionnées (ancienne générique vs nouvelle alignée mission).

---

## 3. Problèmes identifiés, classés par priorité

| Priorité | Sujet |
|---|---|
| P0 | Anomalies de prix sur variantes (Bague Zikr, Haut-parleur Magnétique, Horloge Azan) |
| P0 | Confusion titre/handle "High-Tech"/`maison` |
| P0 | Sort des 9 produits archivés (en attente de validation) |
| P1 | Fusion des deux taxonomies de collections |
| P1 | `Product Type` et tags manquants sur les 8 produits actifs |
| P1 | Handles produits trop longs / sur-optimisés |
| P1 | Stock critique (2 produits) |
| P2 | Finalisation des 4 produits brouillon (images) |
| P2 | Fusion des 3 collections "packs" |
| P2 | Images manquantes sur toutes les collections |
| P3 | Construction réelle de la collection Enfants & Bébés |
| P3 | Mode et Voyage & Aventure — tranché : roadmap, non exposé (voir TAXONOMY.md §11) |

---

## 4. Ce que cet audit ne couvre pas

Le thème (Liquid, sections, templates, assets visuels) n'a pas été audité — accès non disponible via le connecteur Admin API utilisé. À couvrir dans une étape ultérieure, avec un accès dédié.
