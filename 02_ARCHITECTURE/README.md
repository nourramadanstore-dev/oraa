# 02_ARCHITECTURE

Architecture technique et fonctionnelle d'ORAA : structure des systèmes, flux de données, choix structurants. Toute modification de la structure des 20 couches du dépôt doit être actée ici via un ADR (voir 17_DECISIONS).

## Première brique : architecture commerciale

Conformément à `AGENT_PROTOCOL.md`, cette architecture est construite à partir d'un audit réel de la boutique Shopify existante, pas d'une conception théorique isolée du produit. Voir `05_COMMERCE/TAXONOMY.md` pour le modèle cible et `05_COMMERCE/MIGRATION_PLAN.md` pour le plan d'exécution. Décisions associées : `17_DECISIONS/ADR-0002` à `ADR-0006`.

L'architecture technique (stack, hébergement, découpage des services) reste à construire, une fois l'architecture commerciale validée et la migration engagée.

---

Cette couche est subordonnée à `00_FOUNDATION`. En cas de conflit entre le contenu de cette couche et les lois fondamentales, les lois fondamentales priment (voir `00_FOUNDATION/FOUNDATIONAL_LAWS.md`).
