# 00_FOUNDATION

Cette couche est la source de vérité première du dépôt ORAA. Elle prime sur toutes les autres couches (`01_GOVERNANCE` à `20_AI_PACKAGE`).

## Contenu

| Fichier | Rôle |
|---|---|
| `FOUNDATIONAL_LAWS.md` | Les 7 lois qui priment sur toute décision, tout ADR, toute demande |
| `NEVER.md` | Les interdictions absolues, sans exception |
| `CERTIFICATION_CHECKLIST.md` | La checklist à valider avant toute proposition de code ou de livraison |
| `AGENT_PROTOCOL.md` | L'ordre d'intervention obligatoire et la posture attendue de tout agent |

## Règle de modification

La structure des 20 couches du dépôt (`00_FOUNDATION` → `20_AI_PACKAGE`) ne peut être modifiée que par un ADR, référencé dans `17_DECISIONS`.

Les fichiers de cette couche suivent la même règle : toute modification passe par un ADR et une validation humaine explicite (voir la section "Modification de ces lois" dans `FOUNDATIONAL_LAWS.md`).

## Pour tout agent démarrant une tâche

Commencez toujours par `AGENT_PROTOCOL.md` — il définit l'ordre de lecture et d'action pour toute intervention sur ce dépôt.
