# RESILIENCE.md

**Portée** : Tout système d'ORAA en production — services, intégrations, infrastructure.
**Relation avec les lois fondamentales** : Complète la Loi 6 (performance et sécurité natives) et donne le cadre concret exigé par `NEVER.md` pour tout changement destructif ("jamais sans stratégie de retour arrière").

---

## Principes

### La panne est une hypothèse de travail, pas une exception
Tout composant est conçu en supposant qu'une de ses dépendances échouera à un moment donné. La question n'est pas "si", mais "quand", et "que se passe-t-il alors".

### Dégradation gracieuse plutôt que panne totale
Quand un composant non critique échoue, le système doit continuer à fonctionner pour l'essentiel, même avec une fonctionnalité en moins, plutôt que de tomber entièrement.

### Isolation du rayon d'impact
Une panne dans un domaine (ex. `05_COMMERCE`) ne doit pas pouvoir se propager silencieusement à un domaine indépendant (ex. `07_EXPERIENCE`). Les dépendances critiques entre domaines sont explicites et documentées.

### Toute action destructive a un plan de retour arrière testé, pas supposé
Rappel opérationnel de `NEVER.md` : "testé" signifie que le rollback a été exécuté au moins une fois dans un environnement représentatif, pas seulement écrit en théorie.

### Les seuils de reprise sont définis avant l'incident, pas pendant
Chaque système critique a des objectifs définis en amont : temps de reprise acceptable (RTO) et perte de données acceptable (RPO). Ces seuils déterminent la stratégie de sauvegarde et de redondance, pas l'inverse.

### La redondance se justifie par la criticité, pas par principe
Dupliquer un composant a un coût (complexité, maintenance). La redondance est appliquée là où l'impact d'une panne le justifie, documentée comme un choix, pas appliquée uniformément par réflexe.

### La résilience se teste activement
Un plan de reprise non testé est une hypothèse, pas une garantie. Les scénarios de panne critiques doivent être exercés périodiquement (tests de bascule, simulations d'incident), pas seulement documentés.

---

## Application

Le plan de retour arrière et les seuils de reprise pour un système critique sont vérifiés à la Porte 4 de `QUALITY_GATE.md` (`13_QUALITY`), avant toute mise en production.
