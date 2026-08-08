# PRODUCT_PRINCIPLES.md

**Portée** : Toute décision produit sur ORAA — fonctionnalité, parcours, priorisation.
**Relation avec les lois fondamentales** : Ce document complète la Loi 1 (la mission prévaut sur la fonctionnalité). Il définit comment reconnaître, au quotidien, ce qui sert la mission de ce qui sert seulement une demande ponctuelle.

---

## Principes

### Le problème utilisateur avant la solution demandée
Une demande formulée comme une solution ("ajoutez un bouton qui fait X") doit d'abord être ramenée au problème qu'elle prétend résoudre. On construit pour le problème, pas pour la formulation.

### Minimum viable, jamais minimum de qualité
Réduire le périmètre d'une fonctionnalité est légitime. Réduire sa qualité (fiabilité, accessibilité, cohérence) pour aller vite ne l'est pas — voir `NEVER.md`.

### Savoir dire non est aussi important que savoir dire oui
Une fonctionnalité qui n'est pas refusée par défaut doit justifier sa place. La simplicité du produit est un actif qui s'érode fonctionnalité après fonctionnalité si personne ne dit non.

### Informé par la donnée, jamais esclave de la donnée
Les métriques éclairent la décision, elles ne la remplacent pas. Une métrique qui pousse vers un choix contraire à la mission ou aux lois fondamentales ne doit pas l'emporter.

### Un cas d'usage principal par fonctionnalité
Une fonctionnalité qui tente de servir trop de cas d'usage à la fois finit par n'en bien servir aucun. Clarifier le cas principal avant de concevoir.

### La latence perçue est une fonctionnalité
Le temps de réponse et la fluidité perçue font partie de l'expérience produit au même titre qu'une fonctionnalité visible. Voir `PERFORMANCE_GUIDE.md` (`08_ENGINEERING`).

### Les valeurs par défaut comptent plus que les options
Un mauvais défaut avec une option pour le corriger reste un mauvais défaut pour la majorité des utilisateurs qui ne changent jamais les réglages. Optimiser le défaut avant d'ajouter une option.

### La dette produit se documente comme la dette technique
Un compromis produit pris pour une échéance (fonctionnalité incomplète, cas limite non traité) doit être noté explicitement et suivi, pas oublié dans le succès du lancement.

---

## Application

Ces principes s'appliquent dès l'étape 6 (concevoir) du protocole agent, et doivent être vérifiés avant de proposer une implémentation — voir `00_FOUNDATION/CERTIFICATION_CHECKLIST.md`.
