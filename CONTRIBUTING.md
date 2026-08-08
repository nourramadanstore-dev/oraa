# CONTRIBUTING.md

**Portée** : Toute contribution au dépôt ORAA, par une personne ou un agent IA.

Ce document ne redéfinit rien de `00_FOUNDATION`. Il explique comment contribuer *dans le respect* de ce qui y est défini.

---

## Avant de contribuer

Lire, dans l'ordre :

1. `00_FOUNDATION/AGENT_PROTOCOL.md`
2. `00_FOUNDATION/FOUNDATIONAL_LAWS.md`
3. `00_FOUNDATION/NEVER.md`
4. Les principes de la couche concernée par votre contribution (ex. `08_ENGINEERING/ENGINEERING_PRINCIPLES.md` pour du code, `04_PRODUCT_SYSTEM/PRODUCT_PRINCIPLES.md` pour une fonctionnalité)

Cette exigence s'applique de façon identique à une personne et à un agent IA. Aucun des deux n'est dispensé de cette lecture parce que la contribution semble petite.

## Structure d'une contribution

- **Une branche par changement**, nommée de façon à refléter son objet (ex. `feature/`, `fix/`, `docs/`).
- **Des commits clairs**, décrivant *pourquoi* le changement est fait, pas seulement *quoi*.
- **Une taille de changement raisonnable** : si une revue ne peut pas être faite en une seule lecture attentive, le changement doit être découpé (voir `ENGINEERING_PRINCIPLES.md`).

## Revue

Toute contribution passe par une revue avant fusion, humaine ou par un agent distinct de celui qui a produit le changement. La revue vérifie :

- La cohérence avec les lois fondamentales et les principes de la couche concernée.
- Les critères bloquants de `00_FOUNDATION/CERTIFICATION_CHECKLIST.md`.
- L'absence de duplication d'une abstraction existante (`NEVER.md`).

## Proposer une décision structurante

Si votre contribution touche à l'architecture, à une dépendance nouvelle, ou à un standard existant, elle doit s'accompagner d'un ADR avant d'être fusionnée. Utiliser `17_DECISIONS/ADR_TEMPLATE.md`.

## Désaccord

Si une contribution entre en tension avec les lois fondamentales, les principes établis, ou l'architecture, cette tension doit être signalée explicitement — jamais résolue silencieusement dans un sens ou dans l'autre. Voir la posture attendue dans `00_FOUNDATION/AGENT_PROTOCOL.md`.

## Pour les agents IA

Un agent IA contribuant à ce dépôt suit ce document au même titre qu'une personne, sans exception liée à sa nature. Le protocole d'intervention en 10 étapes (`00_FOUNDATION/AGENT_PROTOCOL.md`) reste la référence pour l'ordre des opérations.
