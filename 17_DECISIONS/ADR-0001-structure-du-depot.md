# ADR-0001 — Gel de la structure du dépôt en 20 couches

**Statut** : Accepté
**Date** : 2026-08-07
**Décideur(s)** : Product Owner ORAA

---

## Contexte

Le projet ORAA nécessite une organisation stable de son dépôt pour permettre à tout agent de développement — humain ou IA — de s'y repérer de façon prévisible, aujourd'hui avec Claude Code, demain avec tout autre agent d'ingénierie.

## Décision

La structure du dépôt est figée en 20 couches numérotées :

```
00_FOUNDATION
01_GOVERNANCE
02_ARCHITECTURE
03_DESIGN_SYSTEM
04_PRODUCT_SYSTEM
05_COMMERCE
06_CONTENT
07_EXPERIENCE
08_ENGINEERING
09_OPERATIONS
10_SECURITY
11_DATA
12_AI
13_QUALITY
14_GROWTH
15_ASSETS
16_REGISTRIES
17_DECISIONS
18_RELEASES
19_ARCHIVE
20_AI_PACKAGE
```

Cette structure ne sera plus modifiée (ajout, suppression, renommage ou réordonnancement de couche) sans un nouvel ADR explicite.

## Alternatives considérées

| Option | Avantages | Inconvénients | Raison du rejet |
|---|---|---|---|
| Structure libre, sans numérotation figée | Flexibilité maximale | Dérive progressive, incohérence entre agents et sessions | Rejetée : l'objectif est la stabilité, pas la flexibilité |
| Structure dépendante de l'outil (dossier `.claude/` spécifique) | Intégration rapide avec Claude Code | Ne survit pas à un changement d'agent ou d'outil | Rejetée au profit d'une spécification neutre : "AI Engineering Specification" |

## Conséquences

- Tout agent peut se repérer de façon stable dans le dépôt, session après session.
- Toute évolution de la structure devient un événement tracé, pas une dérive silencieuse.
- Le coût : une rigidité assumée. Un besoin de réorganisation devra passer par un ADR, ce qui ralentit volontairement ce type de changement.

## Conformité avec les lois fondamentales

Conforme à la Loi 7 (toute décision importante doit être documentée) et à la Loi 2 (une décision ne peut jamais affaiblir les fondations) : figer la structure protège justement les fondations contre une dérive non tracée.

## Références

`00_FOUNDATION/FOUNDATIONAL_LAWS.md`, `00_FOUNDATION/README.md`
