# PERFORMANCE_GUIDE.md

**Portée** : Tout composant d'ORAA ayant un impact sur le temps de chargement, de réponse, ou la fluidité perçue.
**Relation avec les lois fondamentales** : Opérationnalise la Loi 6 (la performance est une exigence native), en complément de `PRODUCT_PRINCIPLES.md` qui traite de la latence perçue comme fonctionnalité.

---

## Principes

### Un budget, pas une aspiration
Chaque parcours critique a un budget de performance chiffré (temps de chargement, taille de page, temps de réponse serveur), pas un simple objectif de "faire au mieux". Un budget dépassé est un défaut, pas un détail.

### Mesurer avant d'optimiser
Une optimisation sans mesure préalable est une supposition. On identifie le goulot d'étranglement réel avant d'investir du temps à le corriger.

### La performance perçue compte autant que la performance réelle
Un chargement progressif avec un retour visuel immédiat peut être perçu comme plus rapide qu'un chargement plus court mais silencieux. Les deux dimensions sont prises en compte, pas seulement le temps brut.

### Le budget est pensé pour le réseau et l'appareil les plus contraints, pas les plus favorables
Un budget validé uniquement sur une connexion rapide et un appareil récent ne reflète pas l'expérience réelle d'une partie significative des utilisateurs.

### Le multilingue a un coût de performance qui doit être anticipé
Une mise en page conçue pour une langue courte peut casser ou ralentir avec une langue plus longue. Les budgets de performance et de mise en page tiennent compte de cette variabilité dès la conception (voir Loi 3 et Loi 6).

### La mise en cache est une décision documentée, pas un réflexe
Chaque couche de cache ajoutée (CDN, application, base de données) est justifiée par un besoin mesuré et documentée avec sa stratégie d'invalidation. Un cache mal invalidé est une source de bugs plus coûteuse que le problème qu'il résout.

### La régression de performance sur un parcours critique est bloquante
Une baisse de performance mesurable sur un parcours identifié comme critique bloque la livraison au même titre qu'un bug fonctionnel, conformément à `QUALITY_GATE.md`.

---

## Application

Les budgets de performance sont vérifiés à la Porte 3 de `QUALITY_GATE.md` (`13_QUALITY`), avant la mise en production.
