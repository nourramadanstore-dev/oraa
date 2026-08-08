# ADR-0006 — Stratégie de bundles et relations entre produits

**Statut** : Accepté
**Date** : 2026-08-07
**Décideur(s)** : Product Owner ORAA — validé le 2026-08-07

---

## Contexte

Le catalogue contient déjà un produit de type coffret ("Pack Maison") sans lien structurel documenté vers ses composants. À l'échelle de plusieurs milliers de produits, des coffrets construits sans relation structurée deviennent impossibles à maintenir de façon cohérente (stock, contenu affiché, mises à jour).

## Décision

Utiliser la fonctionnalité native de bundles Shopify (ou une application dédiée si les besoins la dépassent) pour tout produit de type coffret, avec une relation structurée vers ses composants via metafields de référence produit. Distinguer explicitement deux types de relations : "produits complémentaires" (vente croisée) et "fait partie du coffret" (composition du bundle) — jamais fusionnées dans un seul mécanisme.

## Alternatives considérées

| Option | Avantages | Inconvénients | Raison du rejet |
|---|---|---|---|
| Coffret comme produit indépendant sans lien structurel | Rapide à créer | Aucune cohérence de stock, contenu à mettre à jour manuellement | Rejetée : c'est déjà l'état actuel du "Pack Maison" |
| Fusionner vente croisée et composition de bundle dans un seul champ | Plus simple à configurer | Ambiguïté entre "on vous suggère" et "ce produit contient" | Rejetée : les deux relations n'ont pas la même conséquence pour le client ni pour la gestion de stock |

## Conséquences

Le "Pack Maison" existant doit être reconstruit avec cette relation structurée lors de sa migration (Phase B du plan de migration), pas simplement conservé tel quel.

## Conformité avec les lois fondamentales

Conforme à la Loi 4 (le contenu du coffret doit être piloté par la donnée, pas décrit en dur dans un texte non structuré).

## Références

`05_COMMERCE/TAXONOMY.md`, §7 et §8
