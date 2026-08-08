# ADR-0002 — Modèle de taxonomie commerciale à trois couches

**Statut** : Accepté
**Date** : 2026-08-07
**Décideur(s)** : Product Owner ORAA — validé le 2026-08-07

---

## Contexte

L'audit du catalogue existant révèle une architecture de collections dupliquée et incohérente (deux taxonomies superposées, 56 % de collections vides), ainsi qu'une absence totale de `Product Type` et de tags sur les produits actifs. ORAA vise une croissance vers plusieurs milliers de produits ; le modèle actuel ne passerait pas cette échelle.

## Décision

Adopter un modèle à trois couches distinctes et non redondantes : Category (taxonomie standard Shopify, hiérarchique) pour le référencement et les canaux externes, Product Type (vocabulaire métier interne, un par produit) pour le filtrage et les règles de collections intelligentes, Tags (multiples, organisés par espace de noms) pour les facettes transversales. Détail complet dans `05_COMMERCE/TAXONOMY.md`.

## Alternatives considérées

| Option | Avantages | Inconvénients | Raison du rejet |
|---|---|---|---|
| Un seul champ (Product Type uniquement) | Simple à comprendre | Ne supporte pas le filtrage multi-critères à grande échelle | Rejetée : c'est le modèle qui a produit la dérive actuelle |
| Collections manuelles uniquement | Contrôle éditorial total | Charge de maintenance qui croît linéairement avec le catalogue | Rejetée sauf exception (voir "Foi & Transmission") |

## Conséquences

Chaque produit ajouté doit renseigner Category, Product Type et au minimum les tags pertinents — un coût de saisie légèrement supérieur à l'existant, compensé par une navigation et un référencement qui restent cohérents sans intervention manuelle même à grande échelle.

## Conformité avec les lois fondamentales

Conforme à la Loi 4 : aucune classification n'est codée en dur dans un futur thème, tout vit dans les objets Shopify pilotables sans redéploiement.

## Références

`05_COMMERCE/TAXONOMY.md`, §1
