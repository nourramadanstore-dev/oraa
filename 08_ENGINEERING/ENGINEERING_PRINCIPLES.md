# ENGINEERING_PRINCIPLES.md

**Portée** : Tout code écrit pour ORAA, par un humain ou un agent IA.
**Relation avec les lois fondamentales** : Ce document complète la Loi 5 (dépendances justifiées et remplaçables) et la Loi 4 (aucun contenu métier codé en dur). Il définit comment écrire du code qui les respecte concrètement.

---

## Principes

### La simplicité prime sur l'intelligence apparente
Un code qui impressionne mais que la prochaine personne doit déchiffrer coûte plus cher qu'il ne rapporte. Préférer la solution la plus simple qui résout le problème réel, pas le problème imaginé.

### L'explicite prime sur l'implicite
La magie (comportements implicites, conventions non documentées, effets de bord cachés) doit être évitée. Un lecteur du code doit pouvoir comprendre le comportement sans connaître un contexte non écrit.

### Petits changements, revus intégralement
Un changement doit rester assez petit pour être compris et vérifié en une seule lecture par un tiers. Un gros changement se découpe, il ne s'excuse pas.

### Les tests documentent le comportement, pas seulement la couverture
Un test doit exprimer une intention métier ou technique claire. Un taux de couverture élevé avec des tests qui ne vérifient rien de significatif n'est pas un objectif.

### Échouer bruyamment, jamais silencieusement
Une erreur non gérée doit être visible (log, alerte, exception explicite), jamais avalée silencieusement. Un système qui échoue en silence est un système qui trompe son exploitant.

### Pas d'abstraction avant un deuxième cas d'usage réel
Une abstraction créée pour un seul cas d'usage est une prédiction, pas une nécessité. On abstrait quand la duplication devient un fait constaté, pas anticipé.

### Toute dépendance a un propriétaire et une sortie possible
Conformément à la Loi 5, chaque dépendance ajoutée doit avoir sa justification documentée (voir `16_REGISTRIES`) et un chemin de remplacement identifié, même s'il n'est jamais activé.

### La compatibilité ascendante est un choix, pas un oubli
Casser une interface publique (API, contrat de composant, schéma de données) est une décision à documenter, jamais un effet de bord d'un refactor.

### Le code reflète le métier, jamais l'inverse
Conformément à la Loi 4, aucune règle métier ne doit être devinée en lisant le code — elle doit être lisible depuis la couche de configuration ou de données prévue à cet effet.

---

## Application

Ces principes s'appliquent à chaque étape 6 à 9 du protocole agent (`00_FOUNDATION/AGENT_PROTOCOL.md`) : concevoir, développer, tester, documenter.
