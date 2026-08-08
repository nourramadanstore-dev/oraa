# SECURITY_PLAYBOOK.md

**Portée** : Toute surface d'ORAA exposant des données, des accès, ou des interactions avec des tiers.
**Relation avec les lois fondamentales** : Opérationnalise la Loi 6 (la sécurité est une exigence native) et rappelle l'interdiction de `NEVER.md` de la sacrifier pour gagner du temps.

---

## Principes permanents

### Le moindre privilège par défaut
Tout accès (humain, service, agent IA) est accordé au strict nécessaire pour la tâche, jamais par commodité. L'élargissement d'un accès est une décision explicite, pas un défaut.

### Les secrets ne vivent jamais dans le code
Clés, tokens, identifiants ne sont jamais codés en dur ni versionnés, même temporairement, même dans une branche de travail. Ils vivent dans un gestionnaire de secrets dédié.

### Toute dépendance est une surface d'attaque potentielle
Conformément à la Loi 5, chaque dépendance ajoutée est aussi évaluée sous l'angle de son historique de vulnérabilités et de sa maintenance active.

### Le scan de vulnérabilités est continu, pas ponctuel
Les dépendances et l'infrastructure sont vérifiées automatiquement à une cadence régulière, pas seulement lors d'un audit ponctuel.

### La classification des données précède leur traitement
Avant de stocker ou transmettre une donnée, sa sensibilité (publique, interne, personnelle, sensible) doit être connue, car elle détermine son niveau de protection. Voir `11_DATA` pour la gouvernance associée.

### L'authentification et les sessions suivent les standards établis
Pas d'implémentation maison d'un mécanisme d'authentification ou de gestion de session sans justification documentée — voir `ENGINEERING_PRINCIPLES.md` sur les abstractions et dépendances.

---

## Réponse à incident

Un incident de sécurité suit ces étapes, dans l'ordre :

1. **Détecter** — confirmer l'incident via l'observabilité en place (`OBSERVABILITY.md`).
2. **Contenir** — limiter la propagation ou l'exposition avant de chercher la cause racine complète.
3. **Éradiquer** — supprimer la cause identifiée (accès compromis, faille, donnée exposée).
4. **Rétablir** — restaurer le service normal, en vérifiant l'absence de persistance de la compromission.
5. **Documenter** — post-mortem écrit, sans blâme individuel, avec actions correctives suivies dans `16_REGISTRIES`.

Aucune étape n'est sautée pour aller plus vite, y compris sous pression de disponibilité du service.

## Points de déclenchement d'une revue de sécurité obligatoire

- Introduction d'une nouvelle dépendance touchant à l'authentification, au paiement, ou au traitement de données personnelles.
- Ouverture d'une nouvelle surface d'API exposée publiquement.
- Changement de fournisseur d'infrastructure ou de service tiers ayant accès à des données sensibles.
