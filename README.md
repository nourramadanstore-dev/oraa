# ORAA

Dépôt source d'ORAA, organisé en 20 couches numérotées. Cette structure est figée depuis `ADR-0001` (voir `17_DECISIONS/ADR-0001-structure-du-depot.md`) et ne peut être modifiée sans un nouvel ADR.

## Point d'entrée pour tout agent (humain ou IA)

Avant toute intervention sur ce dépôt, lire dans l'ordre :

1. `00_FOUNDATION/AGENT_PROTOCOL.md` — l'ordre d'intervention obligatoire et la posture attendue
2. `00_FOUNDATION/FOUNDATIONAL_LAWS.md` — les lois qui priment sur tout le reste
3. `00_FOUNDATION/NEVER.md` — les interdictions absolues
4. `00_FOUNDATION/CERTIFICATION_CHECKLIST.md` — la checklist à valider avant toute livraison

## Point d'entrée spécifique pour les agents d'ingénierie IA

`20_AI_PACKAGE/` contient l'AI Engineering Specification : le package conçu pour être lu et suivi par tout agent de développement IA, quel que soit l'outil (Claude Code aujourd'hui, tout autre agent demain).

## Structure

| Couche | Rôle | Documents de gouvernance complémentaires |
|---|---|---|
| `00_FOUNDATION` | Lois, interdictions, protocole agent, checklist de certification | — |
| `01_GOVERNANCE` | Rôles, processus de décision | — |
| `02_ARCHITECTURE` | Architecture technique et fonctionnelle | — |
| `03_DESIGN_SYSTEM` | Tokens, composants, patterns visuels | `DESIGN_PHILOSOPHY.md` |
| `04_PRODUCT_SYSTEM` | Logique produit | `PRODUCT_PRINCIPLES.md` |
| `05_COMMERCE` | Logique commerciale | — |
| `06_CONTENT` | Modèles de contenu, traduction | — |
| `07_EXPERIENCE` | Parcours et ergonomie | — |
| `08_ENGINEERING` | Standards de code et d'outillage | `ENGINEERING_PRINCIPLES.md`, `PERFORMANCE_GUIDE.md` |
| `09_OPERATIONS` | Exploitation et déploiement | `RESILIENCE.md`, `OBSERVABILITY.md` |
| `10_SECURITY` | Sécurité | `SECURITY_PLAYBOOK.md` |
| `11_DATA` | Modèles et gouvernance de données | — |
| `12_AI` | IA intégrée au produit | `AI_GOVERNANCE.md` |
| `13_QUALITY` | Tests et critères qualité | `QUALITY_GATE.md` |
| `14_GROWTH` | Acquisition, rétention, expérimentation | — |
| `15_ASSETS` | Actifs bruts | — |
| `16_REGISTRIES` | Référentiels centraux | — |
| `17_DECISIONS` | ADR | — |
| `18_RELEASES` | Historique et planification des livraisons | — |
| `19_ARCHIVE` | Éléments obsolètes conservés pour mémoire | — |
| `20_AI_PACKAGE` | AI Engineering Specification | — |

Voir aussi `CONTRIBUTING.md` à la racine, pour toute contribution humaine ou IA.

### Principe de non-duplication de ces documents

Chaque document ci-dessus complète les lois fondamentales (`00_FOUNDATION/FOUNDATIONAL_LAWS.md`) sans les répéter. En cas de silence d'un document de couche sur un point déjà tranché par les lois fondamentales, ce sont les lois fondamentales qui font foi.

## Règle de gouvernance de la structure

Aucune modification de cette structure (ajout, suppression, renommage, réordonnancement de couche) sans un ADR explicite dans `17_DECISIONS`. Voir `ADR-0001`.
