# QUALITY_GATE.md

**Portée** : Toute évolution du produit ORAA, du développement à la mise en production.
**Relation avec les lois fondamentales** : Opérationnalise la Loi 6 (exigences natives) et sert de base concrète à `00_FOUNDATION/CERTIFICATION_CHECKLIST.md`, sans la dupliquer — ce document définit *quand* et *comment* la checklist s'applique dans le cycle de vie d'un changement.

---

## Principe général

Une porte de qualité (quality gate) est un point de passage obligatoire. Un changement qui ne la franchit pas ne progresse pas à l'étape suivante — il n'y a pas d'exception "juste pour cette fois".

## Les portes

### Porte 1 — Conception
**Avant le développement.** Le changement a-t-il été vérifié contre les principes pertinents (`PRODUCT_PRINCIPLES.md`, `DESIGN_PHILOSOPHY.md`, `ENGINEERING_PRINCIPLES.md`) et contre les critères bloquants de la checklist de certification ?
**Bloquant** : cohérence avec l'architecture et les lois fondamentales.

### Porte 2 — Revue de code
**Avant fusion.** Le code respecte-t-il `ENGINEERING_PRINCIPLES.md` ? Les tests couvrent-ils le comportement, pas seulement la ligne de code ? Une deuxième paire d'yeux (humaine ou agent distinct) a-t-elle vérifié le changement ?
**Bloquant** : au moins une revue effectuée, tests présents et pertinents.

### Porte 3 — Pré-production / staging
**Avant déploiement en production.** Le changement a-t-il été vérifié en conditions proches du réel ? Les critères de `PERFORMANCE_GUIDE.md`, `SECURITY_PLAYBOOK.md` et d'accessibilité sont-ils respectés ?
**Bloquant** : sécurité, performance sous le budget défini, accessibilité AA minimum.

### Porte 4 — Mise en production
**Avant et immédiatement après le déploiement.** Le plan de retour arrière est-il prêt (voir `RESILIENCE.md`) ? L'observabilité du changement est-elle en place (voir `OBSERVABILITY.md`) avant l'exposition aux utilisateurs ?
**Bloquant** : stratégie de rollback documentée et testable, observabilité active.

### Porte 5 — Post-déploiement
**Après mise en production.** Le comportement observé correspond-il à l'attendu sur une fenêtre de surveillance définie ? Un incident déclenche-t-il un rollback selon le seuil prévu dans `RESILIENCE.md` ?

---

## Ce qui bloque vs ce qui se documente

Reprend la distinction de `00_FOUNDATION/CERTIFICATION_CHECKLIST.md` : un point non respecté à une porte bloquante arrête la progression. Un point mineur peut être documenté et suivi (`16_REGISTRIES`), à condition d'être explicite — jamais silencieux.

## Régression

Toute régression détectée sur un critère bloquant (sécurité, accessibilité, performance sous le seuil critique) après mise en production déclenche un retour arrière immédiat, pas une correction "au prochain cycle".
