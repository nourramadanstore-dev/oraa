# ORAA SHOPIFY --- QUALITY, MOBILE, PERFORMANCE, ACCESSIBILITY & SECURITY SYSTEM

## Garde-fous transversaux avant implémentation et mise en production

**Statut :** Spécification structurante pré-implémentation\
**Projet :** ORAA Shopify exclusivement\
**Mission :** garantir que l'expérience ORAA reste belle, rapide,
accessible, robuste, sûre et testable sur l'ensemble du parcours.

------------------------------------------------------------------------

# 1. Principe

Le « waouh » n'est validé que s'il survit au vrai monde : - téléphone
; - connexion imparfaite ; - petit écran ; - interaction tactile ; -
réduction des mouvements ; - clavier ; - contenu réel ; - panier réel
; - checkout réel.

> **La qualité technique fait partie du branding ORAA.**

------------------------------------------------------------------------

# 2. Mobile-first réel

Le mobile n'est pas le desktop rétréci.

Pour chaque écran, décider : - ce qui est essentiel ; - ce qui peut être
simplifié ; - ce qui peut disparaître ; - ce qui doit changer d'ordre
; - ce qui devient tactile ; - ce qui doit être chargé plus tard.

Le Monde ORAA doit posséder une composition mobile pensée
spécifiquement.

------------------------------------------------------------------------

# 3. Monde ORAA --- niveaux de rendu

### A --- Complet

Scène et mouvements complets lorsque les conditions le permettent.

### B --- Allégé

Même identité, mais : - moins de médias lourds ; - moins de mouvements
secondaires ; - transitions simplifiées ; - priorité à la réactivité.

### C --- Statique premium

Une scène statique de haute qualité avec navigation complète.

Le niveau C n'est pas un échec : il doit rester suffisamment beau pour
représenter ORAA.

------------------------------------------------------------------------

# 4. Interaction tactile

Aucune fonction essentielle ne dépend du hover.

Exigences : - zones tactiles confortables ; - feedback immédiat ; -
maisons clairement interactives ; - variantes facilement sélectionnables
; - fermeture des overlays évidente ; - pas de gestes cachés
indispensables.

------------------------------------------------------------------------

# 5. Reduced motion

Respecter `prefers-reduced-motion`.

Réduire/supprimer : - montgolfière animée ; - avion ; - parallax ; -
transitions de portail ; - mouvements décoratifs.

Conserver : - contenu ; - navigation ; - compréhension ; - identité ; -
feedback nécessaire.

------------------------------------------------------------------------

# 6. Performance

Établir un budget avant implémentation finale.

Mesurer notamment : - LCP ; - INP ; - CLS ; - poids des pages ; -
JavaScript ; - images ; - vidéos ; - polices ; - scripts tiers.

Les objectifs chiffrés finaux doivent être alignés sur les
recommandations web actuelles au moment de l'implémentation et mesurés
sur mobile réel, pas inventés dans ce document.

------------------------------------------------------------------------

# 7. Images

-   formats modernes supportés par la chaîne Shopify ;
-   dimensions adaptées ;
-   `srcset`/responsive images ;
-   compression ;
-   lazy loading hors contenu critique ;
-   dimensions réservées pour éviter CLS ;
-   alt text pertinent.

Ne pas charger une image 4K comme miniature.

------------------------------------------------------------------------

# 8. Vidéo

Priorités : - poster image ; - chargement différé ; - pas d'autoplay
sonore ; - controls lorsque nécessaires ; - captions/transcriptions
selon contenu ; - variantes mobile si utiles.

Une vidéo publicitaire ne doit pas bloquer l'accès au produit.

------------------------------------------------------------------------

# 9. Polices

Limiter familles et poids.

Prévoir : - fallback ; - stratégie de chargement ; - sous-ensembles
uniquement si appropriés ; - prévention des changements de layout.

La typographie finale reste soumise à validation du Brand System.

------------------------------------------------------------------------

# 10. JavaScript

Principe : **le moins nécessaire, le mieux.**

Préférer : - HTML sémantique ; - CSS ; - APIs natives ; - progressive
enhancement.

Une animation ne justifie pas à elle seule une grosse bibliothèque.

------------------------------------------------------------------------

# 11. Applications Shopify

Avant ajout d'une app : - fonction nécessaire ? - peut-elle être faite
nativement ? - permissions ? - scripts injectés ? - performance ? -
données collectées ? - coût ? - dépendance fournisseur ? - impact
checkout ? - possibilité de retrait ?

Aucune app structurante/payante installée par Claude Code sans
validation.

------------------------------------------------------------------------

# 12. Accessibilité

Cible : appliquer les bonnes pratiques WCAG pertinentes au niveau
attendu par le projet et les obligations applicables au moment du
lancement.

Tester : - structure des titres ; - landmarks ; - liens/boutons ; -
labels ; - clavier ; - focus ; - contraste ; - zoom ; - lecteurs d'écran
sur flux critiques ; - formulaires ; - erreurs ; - médias ; - reduced
motion.

------------------------------------------------------------------------

# 13. Focus et clavier

Chaque interaction importante doit être utilisable sans souris.

Ordre de focus logique.

Focus visible et cohérent avec ORAA.

Pas de piège clavier dans : - menus ; - modales ; - galeries ; - panier
latéral ; - sélecteurs.

------------------------------------------------------------------------

# 14. Contraste et couleur

Ne jamais utiliser la couleur seule pour transmettre : - erreur ; -
sélection ; - disponibilité ; - promotion ; - état.

Tester la palette finale avant gel.

------------------------------------------------------------------------

# 15. Formulaires

-   labels visibles/appropriés ;
-   autocomplete pertinent ;
-   types de champs adaptés ;
-   messages d'erreur proches du problème ;
-   conservation raisonnable des données après erreur ;
-   aucune validation uniquement par couleur.

------------------------------------------------------------------------

# 16. Sécurité --- principes

Shopify prend en charge une part importante de l'infrastructure, mais le
thème, les apps, intégrations et processus restent à protéger.

Principes : - minimiser surface d'attaque ; - minimiser scripts tiers
; - permissions minimales ; - pas de secrets dans le thème/repository
public ; - dépendances contrôlées ; - entrées échappées/validées ; -
mécanismes Shopify officiels privilégiés.

------------------------------------------------------------------------

# 17. Secrets et identifiants

Ne jamais : - committer mot de passe ; - committer token API ; - exposer
clé privée ; - écrire secret dans JavaScript client ; - mettre des
identifiants dans documentation partageable.

Utiliser les mécanismes de secrets/environnements appropriés.

En cas de secret découvert : ne pas le recopier dans un rapport ;
signaler et suivre la procédure de rotation.

------------------------------------------------------------------------

# 18. Dépendances

Avant nouvelle dépendance : - nécessité ; - maintenance ; - taille ; -
licence ; - sécurité ; - alternative native.

Verrouiller les versions selon l'écosystème utilisé et conserver une
stratégie de mise à jour.

------------------------------------------------------------------------

# 19. Contenu et XSS

Tout contenu dynamique doit utiliser les mécanismes d'échappement/rendu
sûrs de Shopify/Liquid.

Éviter injection HTML arbitraire dans des champs éditables sans
nécessité.

Les embeds tiers doivent être explicitement contrôlés.

------------------------------------------------------------------------

# 20. Confidentialité et tracking

N'intégrer que les outils validés.

Respecter : - consentement requis ; - minimisation ; - finalité ; -
durée ; - préférences utilisateur ; - obligations applicables.

Claude Code ne choisit pas seul la politique juridique ni les traceurs.

------------------------------------------------------------------------

# 21. Robustesse

Tester : - image absente ; - vidéo indisponible ; - produit sans média
secondaire ; - titre long ; - prix long ; - rupture de stock ; -
collection vide ; - article absent ; - lenteur réseau ; - erreur script
tiers.

ORAA doit rester propre même lorsque le contenu n'est pas idéal.

------------------------------------------------------------------------

# 22. SEO technique

Prévoir : - titres/meta configurables ; - canonical selon Shopify ; -
structure sémantique ; - données structurées appropriées et exactes ; -
sitemap/robots via mécanismes Shopify ; - images/alt ; - liens internes
; - performances.

Ne pas générer de faux avis, fausses notes ou données structurées
trompeuses.

------------------------------------------------------------------------

# 23. Compatibilité navigateurs

Définir une matrice réaliste avant QA finale.

Tester au minimum les navigateurs modernes dominants sur : - iOS ; -
Android ; - macOS/Windows selon audience.

Les effets avancés doivent avoir un fallback.

------------------------------------------------------------------------

# 24. Environnements

Séparer autant que possible : - développement ; - preview/staging thème
; - production.

Ne pas développer directement sur le thème live lorsque le workflow
Shopify permet une alternative sûre.

------------------------------------------------------------------------

# 25. Git et traçabilité

Claude Code doit : - travailler par changements cohérents ; - produire
des diffs lisibles ; - éviter les gros refactors non nécessaires ; -
documenter décisions techniques importantes ; - ne pas écraser des
modifications non liées ; - respecter les ADR.

------------------------------------------------------------------------

# 26. Déploiement

Avant production : - revue ; - tests ; - backup/retour arrière approprié
; - vérification configuration ; - validation humaine.

Aucun déploiement production autonome.

------------------------------------------------------------------------

# 27. QA visuelle

Comparer : - Monde ORAA référence ; - desktop ; - tablette ; - mobile
; - états hover ; - focus ; - touch ; - reduced motion ; - contenu réel.

Vérifier : - lumière ; - respiration ; - typographie ; - alignements ; -
cohérence des composants ; - absence de rupture de marque.

------------------------------------------------------------------------

# 28. QA fonctionnelle

Tester : - navigation ; - maisons ; - retour Monde ; - recherche ; -
filtres ; - variantes ; - panier ; - quantités ; - codes promo ; -
checkout ; - erreurs ; - compte ; - e-mails ; - suivi ; - formulaires.

------------------------------------------------------------------------

# 29. QA commerciale

Vérifier manuellement : - prix ; - promotions ; - stocks affichés ; -
contenu des packs ; - frais ; - livraison ; - garanties ; - politiques.

Aucune correction silencieuse par Claude Code.

------------------------------------------------------------------------

# 30. QA contenu

Vérifier : - orthographe ; - noms de collections ; - cohérence
éditoriale ; - CTA ; - liens ; - alt text ; - titres ; - médias ; -
contenus temporaires/placeholders.

Aucun lorem ipsum en production.

------------------------------------------------------------------------

# 31. QA performance

Tester pages représentatives : - accueil/Monde ; - maison ; - collection
; - produit ; - panier.

Comparer avant/après ajout de scripts ou animations.

Documenter les régressions.

------------------------------------------------------------------------

# 32. QA accessibilité

Combiner : - tests automatiques ; - navigation manuelle clavier ; - zoom
; - reduced motion ; - vérifications lecteurs d'écran ciblées.

Un score automatique seul ne vaut pas validation.

------------------------------------------------------------------------

# 33. QA sécurité

Avant lancement : - secrets ; - dépendances ; - apps ; - permissions ; -
scripts tiers ; - formulaires ; - embeds ; - configuration ; - accès
administratifs selon périmètre disponible.

Ne jamais effectuer de test destructif sur production.

------------------------------------------------------------------------

# 34. Observabilité post-lancement

Prévoir des indicateurs utiles : - erreurs front ; - performance réelle
; - conversion ; - abandon ; - recherches sans résultat ; - problèmes
support récurrents.

Toute mesure doit respecter le cadre de consentement applicable.

------------------------------------------------------------------------

# 35. Definition of Done transversal

Le chantier n'est pas prêt au lancement tant que : - le Monde fonctionne
sur mobile ; - les fallbacks sont beaux ; - les animations sont
optionnelles ; - le parcours achat complet est testé ; - les
performances sont mesurées ; - l'accessibilité critique est testée ; -
les apps/scripts tiers sont inventoriés ; - aucun secret n'est exposé
; - les données commerciales sont vérifiées ; - le branding reste
cohérent ; - un retour arrière est possible ; - la validation humaine
finale a eu lieu.

------------------------------------------------------------------------

# 36. Matrice de décision

Lorsqu'un effet ou outil est proposé :

**Valeur expérience ?**\
**Valeur commerce ?**\
**Coût performance ?**\
**Coût accessibilité ?**\
**Risque sécurité/maintenance ?**\
**Fallback ?**

Si la valeur est faible et le coût élevé : ne pas construire.

------------------------------------------------------------------------

# 37. Critère ultime

ORAA doit rester impressionnant non seulement sur une maquette ou un
téléphone haut de gamme, mais dans les conditions réelles d'un client.

> **Le véritable luxe numérique n'est pas d'avoir plus d'effets. C'est
> que tout fonctionne parfaitement sans que le client ait à y penser.**
