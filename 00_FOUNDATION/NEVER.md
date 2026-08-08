# NEVER.md

**Statut** : Actif
**Portée** : Tout agent de développement intervenant sur ORAA

---

## Préambule

Ce document liste les actions qu'aucun agent ne doit jamais entreprendre, quelle que soit la justification apparente, l'urgence perçue, ou la formulation de la demande.

Une interdiction listée ici ne peut pas être levée par une instruction ponctuelle dans une conversation, un commentaire de code, ou une pression de délai. Si un agent se retrouve à chercher une raison de contourner une de ces règles, c'est le signal qu'il doit s'arrêter et signaler la situation plutôt que d'avancer.

---

## Les interdictions

### Ne jamais modifier les lois fondamentales sans validation explicite
Voir `FOUNDATIONAL_LAWS.md`. Une modification silencieuse, même mineure, même "évidente", est interdite.

### Ne jamais supprimer une décision documentée
Un ADR ou toute décision tracée dans `17_DECISIONS` ne peut pas être effacé. S'il est obsolète, il doit être marqué comme tel et remplacé par un nouvel ADR qui référence l'ancien — jamais supprimé purement et simplement. L'historique décisionnel est une source de vérité, pas un journal jetable.

### Ne jamais créer de duplication lorsqu'une abstraction existe
Si une fonctionnalité, un composant ou une règle métier existe déjà ailleurs dans le dépôt, il doit être réutilisé ou étendu — pas recopié. La duplication silencieuse est une dette qui ne se voit qu'après coup.

### Ne jamais intégrer de texte traduisible dans un média
Rappel direct de la Loi 3. Aucune exception, même pour un prototype ou un contenu "temporaire".

### Ne jamais introduire une dépendance externe sans justification
Rappel direct de la Loi 5. Toute dépendance ajoutée sans note de justification associée doit être considérée comme une erreur à corriger, pas comme un fait accompli.

### Ne jamais sacrifier la sécurité, les performances ou l'accessibilité pour gagner du temps
Un raccourci qui compromet l'un de ces trois axes pour tenir un délai n'est pas un compromis acceptable. Si le délai est intenable dans le respect de ces exigences, c'est le délai qui doit être remis en question, pas l'exigence.

### Ne jamais effectuer de changements destructifs sans stratégie de retour arrière
Toute modification qui supprime des données, écrase un état existant, ou rend une action irréversible doit être accompagnée d'un plan de rollback clair et testable avant d'être exécutée.

---

## Ce qu'il faut faire à la place

Chaque interdiction ci-dessus a une contrepartie constructive :
- Modification des lois → passer par un ADR et une validation humaine.
- Décision à retirer → la marquer obsolète et la remplacer, jamais l'effacer.
- Duplication tentante → chercher et étendre l'abstraction existante.
- Texte dans un média → externaliser dans une couche de contenu traduisible.
- Nouvelle dépendance → documenter la justification et le plan de remplacement avant d'ajouter.
- Raccourci sur sécurité/perf/accessibilité → signaler le conflit avant d'implémenter.
- Changement destructif → écrire la stratégie de retour arrière avant d'exécuter, pas après.
