# ADR-0005 — Modèle de navigation à deux niveaux (famille + thème)

**Statut** : Accepté
**Date** : 2026-08-07
**Décideur(s)** : Product Owner ORAA — validé le 2026-08-07

---

## Contexte

L'existant mélange collections par type de produit et collections thématiques sans distinction de rôle, produisant des doublons (trois collections pour le concept "pack") et de nombreuses collections vides jamais reliées à une logique claire.

## Décision

Séparer explicitement deux niveaux de navigation : une navigation primaire stable, organisée par famille de produit (`Product Type`), pilotée par des collections intelligentes sans maintenance manuelle ; une navigation secondaire thématique et saisonnière (occasions, mise en avant de marque), pilotée par tags, avec une seule exception manuelle assumée : la collection de marque "Foi & Transmission".

## Alternatives considérées

| Option | Avantages | Inconvénients | Raison du rejet |
|---|---|---|---|
| Navigation unique par famille seulement | Très simple à maintenir | Aucun espace pour les temps forts commerciaux (Ramadan, Aïd, cadeaux) | Rejetée : la mission d'ORAA a une forte dimension calendaire et symbolique qui mérite une mise en avant dédiée |
| Toutes les collections manuelles | Contrôle éditorial maximal | Charge de maintenance qui a produit la dérive actuelle | Rejetée |

## Conséquences

La quasi-totalité des collections deviennent intelligentes et se peuplent automatiquement ; seule "Foi & Transmission" demande une curation éditoriale continue, ce qui limite explicitement la charge de maintenance humaine.

## Conformité avec les lois fondamentales

Conforme à la Loi 4 (aucun contenu métier codé en dur — la navigation reste pilotée depuis les données produit, pas depuis le thème).

## Références

`05_COMMERCE/TAXONOMY.md`, §3
