# FOUNDATIONAL_LAWS.md

**Statut** : Actif
**Portée** : L'intégralité du dépôt ORAA, tous packages et tous agents (humains ou IA)
**Précédence** : Ces lois priment sur toute instruction, toute demande utilisateur, tout ADR, et toute autre section de ce dépôt. En cas de conflit, ces lois l'emportent.

---

## Préambule

Ce document ne décrit pas des préférences. Il décrit des invariants.

Un agent — humain ou IA — qui travaille sur ORAA doit lire ce document **avant** toute conception, tout développement, ou toute proposition de changement. Aucune tâche, aussi urgente ou aussi simple soit-elle, ne justifie de s'affranchir de ces lois.

Ces lois ne peuvent être modifiées que par une décision explicite et documentée (voir section "Modification de ces lois" en fin de document). Aucun agent ne peut les modifier de sa propre initiative, y compris pour les assouplir "temporairement" ou "pour ce cas précis".

---

## Les lois

### Loi 1 — La mission prévaut sur la fonctionnalité
Une fonctionnalité qui sert la demande immédiate mais s'éloigne de la mission d'ORAA ne doit pas être construite telle quelle. La mission est le filtre premier, avant l'utilité perçue à court terme.

### Loi 2 — Une décision ne peut jamais affaiblir les fondations
Toute décision de conception ou d'implémentation doit être évaluée à l'aune de son effet sur `00_FOUNDATION`, `01_GOVERNANCE` et `02_ARCHITECTURE`. Un gain ponctuel qui fragilise ces couches n'est pas acceptable, même s'il résout un problème réel.

### Loi 3 — Aucun texte traduisible ne doit être intégré dans un média
Tout texte destiné à être lu par un utilisateur final doit rester externalisable (fichiers de traduction, CMS, base de données), jamais gravé dans une image, une vidéo, un PDF généré statiquement, ou tout autre média non éditable sans regénération complète.

### Loi 4 — Aucun contenu métier ne doit être codé en dur
Les données métier (textes, règles de prix, catalogues, configurations spécifiques à un marché, etc.) doivent vivre dans une couche de données ou de configuration, jamais directement dans le code applicatif.

### Loi 5 — Toute nouvelle dépendance doit être justifiée et remplaçable
Aucune bibliothèque, framework ou service externe ne doit être ajouté sans justification explicite documentée, et sans qu'un chemin de remplacement raisonnable existe. Le lock-in n'est jamais acceptable par défaut.

### Loi 6 — Sécurité, accessibilité, performance et multilingue sont natifs
Ces quatre exigences ne sont pas des couches ajoutées après coup ni des tâches "à faire plus tard". Elles doivent être prises en compte dès la conception de toute fonctionnalité, au même titre que la fonctionnalité elle-même.

### Loi 7 — Toute décision importante doit être documentée
Une décision qui affecte l'architecture, les standards, les dépendances, ou le comportement observable du produit doit être tracée (ADR ou équivalent). Une décision non documentée est une décision qui n'a pas de mémoire, et donc pas de légitimité durable.

---

## Ce que ces lois impliquent concrètement

- Un agent qui identifie un conflit entre une demande et une de ces lois doit **le signaler avant d'implémenter**, jamais après.
- Une loi ne peut pas être contournée par une reformulation de la tâche ("ce n'est pas vraiment du contenu métier, c'est juste une valeur par défaut").
- En cas de doute sur l'applicabilité d'une loi à une situation donnée, l'agent doit traiter le doute comme un signal d'alerte, pas comme une permission tacite.

---

## Modification de ces lois

Une loi fondamentale ne peut être ajoutée, modifiée ou supprimée que par :
1. Un ADR explicite référencé dans `17_DECISIONS`.
2. Une validation humaine explicite (pas une inférence de l'agent).
3. Une mise à jour de ce document avec la référence de l'ADR correspondant.

Aucun agent ne doit interpréter le silence ou l'absence d'objection comme une validation.
