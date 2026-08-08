# ADR-0003 — Convention de nommage des SKU

**Statut** : Accepté
**Date** : 2026-08-07
**Décideur(s)** : Product Owner ORAA — validé le 2026-08-07

---

## Contexte

Les SKU actuels sont des identifiants bruts hérités des fournisseurs (ex. `14:193#Style A;200007763:201336100`), illisibles pour l'équipe et inexploitables pour toute automatisation future (rapprochement fournisseur, gestion de stock, reporting).

## Décision

Adopter la convention `ORAA-[CODE_FAMILLE]-[CODE_PRODUIT]-[CODE_VARIANTE]` pour tout nouveau SKU, en trois lettres majuscules par segment quand possible (ex. `ORAA-HOR-AZAN-BLC` pour Horloges / Azan / Blanc).

## Alternatives considérées

| Option | Avantages | Inconvénients | Raison du rejet |
|---|---|---|---|
| Conserver les SKU fournisseur tels quels | Aucun effort de migration | Illisible, bloque toute automatisation interne | Rejetée : coût différé plus élevé que le coût immédiat |
| SKU purement numérique séquentiel | Simple à générer | Aucune information métier lisible dans l'identifiant | Rejetée : perd l'avantage principal d'un SKU structuré |

## Conséquences

Chaque produit migré doit se voir attribuer un nouveau SKU selon cette convention ; l'ancien SKU fournisseur peut être conservé en note interne (metafield) pour traçabilité, sans être l'identifiant de référence.

## Conformité avec les lois fondamentales

Conforme à la Loi 7 (documentation des décisions) et à `ENGINEERING_PRINCIPLES.md` sur l'explicite plutôt que l'implicite.

## Références

`05_COMMERCE/TAXONOMY.md`, §10
