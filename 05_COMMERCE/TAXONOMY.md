# TAXONOMY.md — Architecture commerciale cible d'ORAA

**Statut** : Proposé — en attente de validation avant toute migration du catalogue existant.
**Portée** : Modèle de classification, navigation, recherche, bundles et relations produits, conçu pour supporter une croissance du catalogue de la dizaine à plusieurs milliers de produits.
**Relation avec les lois fondamentales** : Aucun contenu métier de cette taxonomie ne doit être codé en dur dans le thème (Loi 4) — elle vit entièrement dans les objets Shopify (Category, Product Type, Tags, Collections, Metafields) pour rester pilotable sans redéploiement de code.

---

## Principes directeurs

Cette architecture est jugée sur cinq critères, dans cet ordre en cas d'arbitrage :

1. **Fidélité à la mission** — la structure doit rendre visible l'identité spirituelle et familiale d'ORAA, pas seulement classer des objets.
2. **Expérience utilisateur** — un visiteur doit trouver ce qu'il cherche en 2 clics maximum depuis la page d'accueil.
3. **Référencement naturel** — chaque niveau de la taxonomie doit pouvoir devenir une page indexable pertinente (pas de duplication de contenu, pas de sur-optimisation de mots-clés).
4. **Maintenabilité** — l'ajout d'un produit ne doit jamais nécessiter une décision de structure ; la structure doit déjà prévoir sa place.
5. **Évolutivité** — passer de 21 à 2 000 produits ne doit pas nécessiter de refonte, seulement un remplissage progressif.

---

## 1. Modèle à trois couches

Shopify expose trois mécanismes de classification distincts. ORAA doit utiliser les trois, chacun pour un rôle précis — les confondre est la cause principale de la dérive observée dans l'audit de l'existant.

| Couche | Rôle | Cardinalité | Usage |
|---|---|---|---|
| **Category** (taxonomie standard Shopify) | Classification normalisée, hiérarchique, reconnue par Shopify, Google Shopping et les canaux de vente externes | Une par produit | Référencement, flux marchands, comparateurs |
| **Product Type** (champ interne) | Vocabulaire métier d'ORAA, lisible par l'équipe | Un par produit | Filtrage, reporting interne, règles de collections intelligentes |
| **Tags** (attributs multiples) | Facettes transversales (occasion, public, fonction, matière...) | Plusieurs par produit | Filtres boutique, recherche, collections intelligentes secondaires |

**Pourquoi ce modèle plutôt qu'un seul champ** : un champ unique atteint ses limites autour de quelques centaines de produits, car il doit porter à la fois la hiérarchie (arbre de navigation) et les attributs (facettes). Séparer les deux permet à la navigation de rester stable pendant que les facettes se multiplient librement.

---

## 2. Familles de produits (Product Type)

Vocabulaire interne, aligné sur l'usage réel plutôt que sur la fiche technique fournisseur.

| Product Type | Description | Exemples actuels |
|---|---|---|
| Enceintes & Diffusion Coranique | Haut-parleurs et enceintes dédiés à la récitation | Enceinte Lune 3D, Haut-parleur Magnétique |
| Horloges & Réveils Adhan | Objets qui rythment les temps de prière | Horloge Azan Bluetooth, Horloge Adhan Al-Fatiha |
| Veilleuses & Lampes Islamiques | Éclairage à fonction symbolique ou apaisante | Lampe de Nuit Coranique, Veilleuse 3D Kaaba |
| Encens & Ambiance | Diffusion olfactive et rituelle | Brûleur d'Encens SQ-600 |
| Bijoux & Dhikr Connecté | Objets portés, comptage et rappel | Bague Connectée Zikr et Qibla |
| Décoration & Symboles | Objets muraux ou d'exposition sans fonction électronique | *(catégorie à peupler)* |
| Éducatif Enfant | Apprentissage religieux adapté aux enfants | Enceinte Coranique Enfant |
| Coffrets & Packs | Assemblages multi-produits | Pack Maison |
| Accessoires de Prière | Objets d'usage rituel quotidien (à date, absent du catalogue) | *(catégorie future)* |

Cette liste est volontairement un point de départ, pas une limite : chaque nouvelle famille suit le même principe (un usage identifiable, pas une caractéristique technique) et s'ajoute par un simple enrichissement de ce document — pas par ADR, sauf si elle touche à la structure de navigation elle-même (voir §3).

---

## 3. Collections et navigation

### Navigation primaire (menu principal) — par famille produit

Stable dans le temps, reflète directement les `Product Type` ci-dessus. Une collection intelligente (`smart collection`) par famille, alimentée automatiquement par le champ Product Type — aucune maintenance manuelle nécessaire à l'ajout d'un produit.

```
Accueil
├── Enceintes & Horloges Coraniques
├── Veilleuses & Lampes
├── Encens & Ambiance
├── Bijoux & Dhikr Connecté
├── Décoration Islamique
├── Enfants
├── Coffrets & Packs
└── Nouveautés (tri automatique par date de création)
```

### Navigation secondaire — pages thématiques (marketing, SEO, saisonnier)

Collections intelligentes basées sur les tags d'occasion, activables/désactivables sans toucher au catalogue :

- **Foi & Transmission** — collection de marque, seule collection **manuelle et curatée**, incarne l'identité ORAA au-delà du classement produit
- **Ramadan**, **Aïd** — saisonnières, pilotées par tag `occasion:*`, publiées/dépubliées selon la période
- **Idées cadeaux** — pilotée par tag `occasion:cadeau`
- **Meilleures ventes** — automatique, triée sur les ventes une fois les données disponibles

**Règle de gouvernance** : toute collection reste smart (automatique) par défaut. Une collection manuelle n'est créée que si elle porte une intention éditoriale qu'aucune règle ne peut capturer — c'est le cas de "Foi & Transmission" uniquement à ce stade. C'est ce principe qui a manqué à l'existant et produit 10 collections vides.

---

## 4. Système de tags (facettes)

Tags organisés par espace de noms (`namespace:valeur`) pour rester lisibles et filtrables à grande échelle.

| Namespace | Exemples de valeurs | Usage |
|---|---|---|
| `occasion` | ramadan, aid, naissance, mariage, cadeau | Collections saisonnières et marketing |
| `public` | enfant, adulte, famille | Filtrage boutique |
| `fonction` | eveil, adhan, dhikr, decoration, parfum | Filtrage boutique, recommandations |
| `connectivite` | bluetooth, app, sans-fil | Filtrage boutique |
| `couleur` | blanc, noir, multicolore | Filtrage boutique (en complément des options de variante) |
| `materiau` | bois, acrylique, metal | Filtrage boutique |

Un tag qui ne rentre dans aucun namespace ne doit pas être créé sans mise à jour de ce document — c'est ce qui évite la dérive observée dans l'audit (tags absents ou incohérents).

---

## 5. Filtres Shopify

Configurer les filtres de recherche/navigation (app Search & Discovery native Shopify) sur :
- `Product Type` (filtre principal)
- Tags des namespaces `occasion`, `public`, `fonction`, `couleur`
- Prix (natif)
- Disponibilité (natif)

Ne pas créer de filtre sur un tag hors namespace ou sur un attribut qui concerne moins de 5 % du catalogue — un filtre qui ne réduit jamais la liste affichée nuit à l'UX plus qu'il n'aide.

---

## 6. Recherche

**Problème identifié dans l'existant** : vocabulaire incohérent entre variantes du français et de l'arabe translittéré (coran/quran, adhan/azan) dans les titres et handles, ce qui fragmente la pertinence de la recherche interne.

**Recommandation** : fixer un vocabulaire de référence unique par concept (ex. toujours "Coran" et "Adhan" en façade française) et déclarer les variantes orthographiques comme synonymes dans la configuration de recherche Shopify, plutôt que de les laisser se disperser dans les titres produits.

---

## 7. Bundles & coffrets

La famille "Coffrets & Packs" regroupe les assemblages multi-produits. Recommandation technique :
- Utiliser la fonctionnalité native de bundles Shopify (ou une app dédiée si un besoin dépasse ses capacités) plutôt qu'un produit "coffret" fabriqué manuellement sans lien structurel avec ses composants.
- Chaque bundle référence ses produits composants via une relation structurée (metafield de référence produit), pas seulement par description textuelle — ce qui permet l'affichage automatique du contenu du coffret et la mise à jour de stock cohérente.

---

## 8. Relations entre produits

Utiliser des metafields de référence produit pour deux relations distinctes, à ne pas confondre :

- **"Produits complémentaires"** — suggestion de vente croisée (ex. horloge + veilleuse de la même gamme visuelle)
- **"Fait partie du coffret"** — lien bundle → composants (voir §7)

Les collections par famille assurent déjà la découverte "produits similaires" — inutile de dupliquer cette relation en metafield.

---

## 9. Convention de handles (URL)

**Problème identifié** : handles actuels de plus de 150 caractères, mots-clés répétés, illisibles et contre-productifs pour le SEO moderne.

**Nouvelle convention** : `[famille-courte]-[nom-produit]`, en minuscules, sans répétition de mot-clé, sous 60 caractères.
Exemple : `enceinte-coranique-lune-3d` au lieu du handle actuel de 150+ caractères.

**Point de vigilance** : le catalogue actuel n'étant pas encore indexé publiquement (boutique non lancée, 0 commande), ce changement peut être fait maintenant **sans coût de redirection SEO**. Une fois la boutique lancée et indexée, tout changement de handle devra passer par une redirection 301 documentée — voir `ADR-0004`.

---

## 10. Convention de SKU interne

**Problème identifié** : SKUs actuels hérités bruts du fournisseur (`14:193#Style A;200007763:201336100`), illisibles et non exploitables en interne.

**Nouvelle convention** : `ORAA-[CODE_FAMILLE]-[CODE_PRODUIT]-[CODE_VARIANTE]`
Exemple : `ORAA-HOR-AZAN-BLC` (Horloges, Azan, Blanc).
Voir `ADR-0003` pour le détail des codes famille.

---

## 11. Catégories futures (roadmap de croissance)

Familles identifiées mais non actives, à réévaluer au fur et à mesure de la croissance du catalogue — leur ajout suit le même principe que §2, sans nécessiter de refonte :

- Accessoires de prière (tapis, boussole qibla physique)
- Papeterie & calligraphie
- Bien-être & aromathérapie halal
- Cadeaux collectivités (mosquées, écoles, associations)
- Abonnement / box mensuelle

**Familles roadmap, décision tranchée** — Mode et Voyage & Aventure font partie de la vision long terme d'ORAA mais ne sont pas prioritaires pour le lancement. Elles sont conservées dans l'architecture comme catégories prévues, **sans être exposées** (pas de collection publiée, pas d'entrée de navigation) tant qu'elles ne disposent pas d'une offre cohérente. L'architecture (modèle à 3 couches, §1) est conçue pour les intégrer nativement le moment venu, sans refonte.

---

## Ce que cette architecture ne couvre pas encore

Le thème (structure Liquid, sections, templates) n'est pas dans la portée de ce document — il vient dans une étape suivante, une fois l'architecture commerciale validée et migrée. Voir `MIGRATION_PLAN.md` pour l'enchaînement.
