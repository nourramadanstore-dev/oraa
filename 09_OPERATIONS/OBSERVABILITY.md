# OBSERVABILITY.md

**Portée** : Tout système d'ORAA en production.
**Relation avec les lois fondamentales** : Rend concrète la capacité à détecter une violation des exigences natives (Loi 6) avant qu'elle n'affecte durablement les utilisateurs.

---

## Principes

### Si ce n'est pas observable, ce n'est pas prêt pour la production
Un système ne doit pas être déployé sans que son état (santé, performance, erreurs) soit mesurable. L'observabilité n'est pas une amélioration post-lancement, elle fait partie de la définition de "terminé".

### Logs, métriques et traces ont chacun un rôle distinct
Les logs expliquent *ce qui s'est passé* sur un événement précis. Les métriques montrent *une tendance* dans le temps. Les traces relient *un parcours* à travers plusieurs composants. Un système bien observé combine les trois sans les confondre.

### On alerte sur les symptômes visibles par l'utilisateur, pas seulement sur les causes internes
Une alerte doit refléter un impact réel ou imminent (latence perçue, taux d'erreur utilisateur), pas uniquement une métrique interne qui n'a pas encore d'effet visible. Cela évite la fatigue d'alerte sur du bruit sans conséquence.

### Chaque alerte a un propriétaire et une action attendue
Une alerte qui ne déclenche aucune action claire ne devrait pas exister. Si personne ne sait quoi faire en la recevant, elle doit être reformulée ou supprimée.

### Aucune donnée personnelle dans les logs par défaut
Conformément à la gouvernance des données (`11_DATA`), les logs ne contiennent pas d'information personnelle identifiable sauf besoin explicite, justifié et protégé en conséquence.

### La rétention des données d'observabilité est définie, pas illimitée par défaut
Chaque type de donnée d'observabilité (log, métrique, trace) a une durée de rétention documentée, cohérente avec son usage réel (diagnostic court terme vs analyse de tendance long terme).

### Les tableaux de bord ont un propriétaire clair
Un tableau de bord sans propriétaire identifié devient obsolète silencieusement. Chaque dashboard critique est rattaché à une équipe ou un domaine responsable de sa pertinence.

---

## Application

L'observabilité d'un changement est vérifiée à la Porte 4 de `QUALITY_GATE.md` (`13_QUALITY`) : elle doit être active *avant* l'exposition aux utilisateurs, pas ajoutée après un premier incident.
