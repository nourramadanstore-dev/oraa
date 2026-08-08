# ADR-0004 — Convention de handles produits et gestion des redirections

**Statut** : Accepté
**Date** : 2026-08-07
**Décideur(s)** : Product Owner ORAA — validé le 2026-08-07

---

## Contexte

Les handles produits actuels dépassent 150 caractères, répètent les mêmes mots-clés plusieurs fois, et nuisent à la fois au référencement moderne et à la lisibilité des URL. La boutique n'ayant à ce jour aucune commande ni indexation publique significative, une correction immédiate n'entraîne pas de coût de redirection.

## Décision

Adopter une convention de handle courte (`[famille-courte]-[nom-produit]`, sous 60 caractères, sans répétition de mot-clé) pour tout produit migré ou créé. Tant que la boutique n'est pas indexée publiquement de façon significative, les handles peuvent être corrigés directement. Une fois la boutique lancée et indexée, tout changement de handle sur un produit déjà public devra être accompagné d'une redirection 301 documentée.

## Alternatives considérées

| Option | Avantages | Inconvénients | Raison du rejet |
|---|---|---|---|
| Conserver les handles actuels | Aucun effort | Handles illisibles et contre-productifs pour le SEO durablement | Rejetée : le coût de correction est minimal aujourd'hui, maximal plus tard |
| Corriger uniquement à la demande, produit par produit | Effort minimal immédiat | Incohérence persistante, dérive identique à l'existant | Rejetée : ne résout pas la cause structurelle |

## Conséquences

Fenêtre d'opportunité limitée : cette correction doit être faite avant le lancement commercial, pas après, pour éviter tout coût de redirection ultérieur.

## Conformité avec les lois fondamentales

Conforme à la Loi 6 (le référencement naturel — via la performance et la structure — est une exigence native, pas un correctif après coup).

## Références

`05_COMMERCE/TAXONOMY.md`, §9
