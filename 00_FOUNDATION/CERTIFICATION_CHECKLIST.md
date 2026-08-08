# CERTIFICATION_CHECKLIST.md

**Statut** : Actif
**Objectif** : Vérification obligatoire avant toute proposition de code ou de conception, et avant toute livraison.

---

## Comment utiliser cette checklist

Deux catégories de critères, à ne pas traiter de la même façon :

- **Bloquants** — si un de ces points n'est pas respecté, l'agent doit s'arrêter, signaler le problème, et proposer une alternative avant d'implémenter quoi que ce soit. Il ne doit pas avancer "en attendant une réponse".
- **À signaler** — si un de ces points n'est pas pleinement respecté, l'agent peut avancer mais doit le documenter explicitement dans sa réponse, avec la raison et l'impact.

Ne jamais traiter un point "à signaler" comme s'il était optionnel : il doit apparaître dans la réponse, même brièvement.

---

## Critères bloquants

| # | Critère | Question à se poser |
|---|---|---|
| 1 | Cohérence avec les lois fondamentales | Est-ce que ce changement viole une des 7 lois de `FOUNDATIONAL_LAWS.md` ? |
| 2 | Respect des interdictions | Est-ce que ce changement enfreint un point de `NEVER.md` ? |
| 3 | Sécurité | Ce changement introduit-il une faille, une exposition de données, ou une surface d'attaque non maîtrisée ? |
| 4 | Réversibilité | Si ce changement est destructif, existe-t-il une stratégie de retour arrière documentée ? |
| 5 | Cohérence avec l'architecture | Ce changement respecte-t-il la structure définie dans `02_ARCHITECTURE`, ou nécessite-t-il un ADR ? |

## Critères à signaler

| # | Critère | Question à se poser |
|---|---|---|
| 6 | Cohérence avec le Design System | Le changement réutilise-t-il les tokens, composants et patterns de `03_DESIGN_SYSTEM` ? |
| 7 | Cohérence avec les standards | Le code respecte-t-il les conventions définies dans `08_ENGINEERING` ? |
| 8 | Compatibilité multilingue | Le contenu est-il externalisable et la mise en page tolère-t-elle des langues plus longues (ex. allemand) ou RTL si applicable ? |
| 9 | Performance | Y a-t-il un impact mesurable sur le temps de chargement, la taille du bundle, ou les requêtes ? |
| 10 | Accessibilité | Le changement respecte-t-il au minimum WCAG AA (navigation clavier, contraste, ARIA) ? |
| 11 | SEO | Le changement affecte-t-il le rendu côté serveur, les métadonnées, ou la structure sémantique ? |
| 12 | Maintenabilité | Le code est-il compréhensible sans contexte supplémentaire, et évite-t-il la duplication ? |
| 13 | Documentation | Le changement est-il documenté à l'endroit approprié (ADR, README, commentaire de justification) ? |

---

## Format de restitution attendu

Avant toute implémentation, l'agent doit présenter un résumé court sous cette forme :

```
Certification — [nom de la tâche]

Bloquants : OK / Point(s) soulevé(s)
[si point soulevé : description + alternative proposée]

À signaler :
- [critère] : [statut] — [note si pertinent]
```

Si tous les critères bloquants sont OK, l'agent peut procéder. S'il en manque un, il doit s'arrêter et proposer une alternative avant toute implémentation.
