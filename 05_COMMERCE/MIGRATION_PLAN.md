# MIGRATION_PLAN.md — Migration du catalogue vers l'architecture cible

**Statut** : Proposé — exécution suspendue jusqu'à validation des ADR associés (`17_DECISIONS`).
**Principe directeur** : construire la cible d'abord, migrer une fois — pas de nettoyage intermédiaire qui serait ensuite réorganisé.

---

## Phase A — Fondations (documentation, aucune écriture Shopify)

**Objectif** : figer la référence avant d'y toucher.
**Actions** : validation de `TAXONOMY.md` et des ADR-0002 à 0006.
**Point de contrôle** : votre validation explicite de chaque ADR.
**Risque si sautée** : toute migration ultérieure devra être refaite.

## Phase B — Pilote (12 produits)

**Objectif** : valider le modèle sur un périmètre réduit avant généralisation.
**Actions** : appliquer Category / Product Type / Tags / SKU / handle aux 8 produits actifs et 4 brouillons.
**Point de contrôle** : revue conjointe du résultat sur ces 12 produits avant d'étendre.
**Risque si sautée** : erreurs de modèle découvertes seulement après application à tout le catalogue.

## Phase C — Construction des collections cibles

**Objectif** : créer la structure de navigation cible en parallèle de l'existante, sans la remplacer encore.
**Actions** : créer les collections intelligentes par famille (§3 de `TAXONOMY.md`), créer les collections thématiques, laisser les anciennes collections actives en parallèle.
**Point de contrôle** : vérifier que chaque produit migré en Phase B apparaît correctement dans sa nouvelle collection.

## Phase D — Migration du catalogue restant

**Objectif** : étendre la Phase B au reste du catalogue actif.
**Actions** : renseigner Category / Product Type / Tags / SKU / handles sur les produits restants ; laisser les 9 produits archivés hors sujet inchangés (statut archivé conservé, conformément à votre décision).
**Point de contrôle** : audit de cohérence — aucun produit actif sans Product Type ni tag.

## Phase E — Décommissionnement de l'ancienne structure

**Objectif** : retirer la confusion de l'ancienne architecture (Maison / Hygiène-1 / Maison-1 / High-Tech mal nommée / doublons de packs).
**Actions** : dépublier puis supprimer les anciennes collections une fois vérifié qu'aucun produit n'en dépend plus.
**Point de contrôle** : **validation explicite avant toute suppression**, conformément à `NEVER.md` sur les changements destructifs.

## Phase F — Prêt pour la croissance

**Objectif** : que l'ajout d'un nouveau produit suive naturellement l'architecture, sans décision au cas par cas.
**Actions** : rédiger un guide court "ajouter un produit à ORAA" (checklist Category/Product Type/Tags/SKU/handle) à ranger dans `05_COMMERCE`, référencé depuis `CONTRIBUTING.md`.
**Point de contrôle** : un produit test créé en suivant uniquement le guide, sans intervention supplémentaire.

---

## Ce qui reste en attente, quel que soit l'avancement des phases

La suppression définitive des 9 produits archivés hors sujet reste **non validée** et n'est déclenchée dans aucune des phases ci-dessus. Elle nécessite une décision séparée de votre part.
