# AI_GOVERNANCE.md

**Portée** : Toute intelligence artificielle intégrée *au produit* ORAA (recommandation, génération, personnalisation, automatisation visible ou invisible pour l'utilisateur final).
**Ne pas confondre avec** : `00_FOUNDATION/AGENT_PROTOCOL.md`, qui gouverne les agents IA qui *construisent* ORAA. Ce document gouverne l'IA qui *fait partie* d'ORAA.
**Relation avec les lois fondamentales** : Complète la Loi 6 (sécurité, accessibilité, performance, multilingue natifs) appliquée aux composants IA, et la Loi 7 (toute décision importante documentée) appliquée aux choix de modèles.

---

## Principes

### Transparence envers l'utilisateur
Lorsqu'une IA génère, recommande ou décide quelque chose de visible par l'utilisateur, celui-ci doit pouvoir le savoir. Aucune fonctionnalité IA ne doit se faire passer pour un comportement purement humain ou déterministe sans le signaler.

### Supervision humaine proportionnelle à l'enjeu
Plus une décision assistée par IA a de conséquences pour l'utilisateur (financières, légales, irréversibles), plus le niveau de supervision ou de validation humaine avant application doit être élevé. Une IA ne doit jamais avoir une autorité finale sur une action irréversible et à fort enjeu sans point de contrôle humain.

### Traçabilité des modèles utilisés
Tout composant produit qui repose sur un modèle IA doit documenter : le modèle et sa version, le fournisseur, la date d'intégration, et le comportement de repli en cas d'indisponibilité. Cette traçabilité vit dans `16_REGISTRIES`.

### Comportement de repli obligatoire
Aucune fonctionnalité ne doit dépendre d'une IA sans un comportement de repli défini (dégradation gracieuse, message clair, alternative manuelle) en cas d'échec, de latence excessive, ou d'indisponibilité du modèle.

### Les données utilisées pour l'IA suivent la gouvernance des données
L'usage de données utilisateur pour l'entraînement, le fine-tuning ou l'inférence est soumis aux règles de `11_DATA`, sans exception liée au caractère "IA" du traitement.

### Évaluation avant mise en production
Tout composant IA orienté utilisateur doit être évalué avant lancement sur : la qualité des résultats sur des cas représentatifs, les biais potentiels identifiables, et les cas d'échec connus. Cette évaluation est documentée, pas seulement testée informellement.

### Pas de manipulation par la personnalisation
Une IA de personnalisation ne doit jamais être utilisée pour orienter un utilisateur vers un choix qui sert l'intérêt d'ORAA au détriment explicite du sien (dark pattern algorithmique). Ceci est un point de vérification, pas une option.

### Explicabilité minimale
Même sans exposer le fonctionnement interne d'un modèle, l'utilisateur doit pouvoir comprendre, au moins en substance, *pourquoi* un résultat ou une recommandation lui est présenté quand cela affecte sa décision.

---

## Application

Tout ajout ou modification d'un composant IA produit passe par la checklist de certification (`00_FOUNDATION/CERTIFICATION_CHECKLIST.md`) et, si le choix de modèle ou d'architecture IA est structurant, par un ADR (`17_DECISIONS`).
