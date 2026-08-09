# ORAA SHOPIFY --- MONDE ORAA

## Master Experience Specification

**Statut :** Spécification maîtresse de conception ---
pré-implémentation\
**Projet :** ORAA Shopify exclusivement\
**Rôle :** Document parent définissant l'expérience du Monde ORAA et les
règles communes à toutes les maisons/collections.

------------------------------------------------------------------------

# 0. Hiérarchie et rôle du document

Hiérarchie cible :

**Codex / lois ORAA → Brand System ORAA → Monde ORAA → Système des
maisons → Spécifications de chaque maison → Composants Shopify →
Implémentation**

Ce document ne remplace ni le Codex, ni les ADR, ni la taxonomie, ni les
décisions commerciales. En cas de contradiction, Claude Code doit la
signaler avant modification.

Le Monde ORAA est la porte d'entrée de la boutique. Il ne doit pas être
traité comme une simple hero banner décorative.

> **Le Monde ORAA doit être beau lorsqu'il ne se passe absolument rien.
> L'animation ne doit jamais être nécessaire pour rendre la scène
> intéressante.**

------------------------------------------------------------------------

# 1. Mission de l'expérience

Le Monde ORAA doit simultanément : - provoquer un effet de découverte et
d'émerveillement ; - faire reconnaître immédiatement ORAA ; - permettre
de comprendre qu'il s'agit d'une boutique ; - rendre les grandes
collections immédiatement identifiables ; - inviter naturellement à
entrer dans une maison ; - préserver la confiance et la lisibilité
commerciale ; - rester performant, accessible et fonctionnel sur mobile.

Principe : \> **Les collections ORAA ne sont pas seulement des rayons.
Ce sont des endroits dans lesquels on entre.**

Rythme global : **WAOUH → respiration → découverte → respiration → désir
→ confiance → transaction → souvenir.**

------------------------------------------------------------------------

# 2. Direction artistique maîtresse

La référence validée est un Monde ORAA : - lumineux ; - aérien ; -
réaliste ; - magique sans devenir enfantin ou artificiel ; - chaleureux
; - inspiré d'un village/lieu européen contemporain et élégant ; - avec
ciel, eau, architecture, végétation et profondeur ; - riche en détails
mais visuellement respirant.

Le spectaculaire vient de la qualité de la scène, de la lumière, de la
profondeur et de quelques événements choisis --- pas de l'accumulation
d'effets.

## 2.1 Lumière

La lumière fait partie de l'identité ORAA.

Rechercher : - lumière naturelle/cinématographique ; - volumes lisibles
; - profondeur ; - reflets maîtrisés ; - équilibre chaud/frais ; - scène
claire et accueillante.

Éviter : - filtre jaune généralisé ; - surexposition ; - saturation
artificielle ; - ambiance nocturne imposée à tout le Monde ORAA.

## 2.2 Végétation

-   naturelle ;
-   élégante ;
-   jamais envahissante ;
-   rosiers rouges utilisés avec mesure comme détail récurrent possible.

## 2.3 Eau

Lorsqu'elle est présente : - participe à la respiration ; - apporte
profondeur et lumière ; - ne doit pas devenir l'élément principal au
détriment des maisons.

------------------------------------------------------------------------

# 3. Signature ORAA et anneau

L'anneau ORAA de référence : - grand anneau ouvert ; - structure
métallique dorée ; - profondeur intérieure bleu nuit ; - lumière bleue
intense, notamment dans la partie basse ; - sensation de portail /
passage / ouverture.

L'anneau n'est pas un cercle doré générique.

## 3.1 Usage

Il peut servir : - de signature ; - de passage entre Monde et maison ; -
de micro-moment cérémoniel ; - à certains moments post-achat.

Il ne doit pas : - être imprimé partout ; - devenir un motif de fond
systématique ; - tourner en permanence ; - être utilisé comme loader
générique.

## 3.2 Mouvement

L'animation privilégiée est une **activation** : lumière bleue →
perception de profondeur → passage.

Courte, fluide, évitable en reduced motion.

------------------------------------------------------------------------

# 4. Architecture des maisons

Chaque grande collection correspond à une maison/bâtiment ou lieu
clairement identifiable.

## 4.1 Nommage extérieur

Depuis le Monde ORAA, utiliser en priorité le **nom commercial clair de
la collection**.

Exemple : **TECH & ACCESSOIRES**

et non uniquement : « L'Atelier Tech ».

## 4.2 Nommage intérieur

Une fois à l'intérieur, un nom narratif peut enrichir l'univers.

Exemple : **L'ATELIER TECH**\
*Tech & Accessoires*

## 4.3 Taxonomie

Les noms définitifs des maisons doivent être dérivés de la taxonomie
ORAA validée dans le repository.

Claude Code ne doit : - ni inventer une collection ; - ni en renommer
une ; - ni exposer une catégorie roadmap/non validée ; sans décision
humaine explicite.

------------------------------------------------------------------------

# 5. États des maisons

## 5.1 État repos

La maison est belle et identifiable sans interaction.

Son enseigne reste lisible.

## 5.2 État intérêt --- desktop

Au passage du curseur : - l'enseigne s'illumine progressivement ; - le
texte gagne en présence ; - certaines lumières/vitrines peuvent
légèrement s'éveiller ; - une invitation discrète « Entrer » peut
apparaître si utile ; - la réaction doit rester raffinée.

Pas de : - flash ; - zoom agressif ; - tremblement ; - animation arcade
; - son automatique.

## 5.3 État tactile

Sur mobile, aucune fonction essentielle ne dépend du hover.

Le toucher doit fournir un feedback immédiat et l'entrée doit rester
évidente.

## 5.4 État entrée

Clic/toucher : - réaction courte ; - transition ORAA éventuelle ; -
entrée dans le mini-univers de la collection.

------------------------------------------------------------------------

# 6. Vie du Monde ORAA

Le monde possède deux familles de mouvements.

## 6.1 Vie autonome

Elle existe sans interaction.

### Montgolfière ORAA

-   dérive lente ;
-   trajectoire douce ;
-   mouvement naturel ;
-   pas de boucle courte évidente ;
-   ne doit pas masquer les enseignes.

### Avion

-   vole réellement à travers le ciel ;
-   passage occasionnel plutôt que présence permanente ;
-   trajectoire cohérente ;
-   discret ;
-   ne concurrence pas la montgolfière.

### Nuages / atmosphère

Mouvement extrêmement lent si utilisé.

### Eau

Micro-mouvement éventuel.

### Végétation

Mouvement très léger, presque imperceptible.

## 6.2 Vie réactive

Elle répond au visiteur : - illumination des enseignes ; - lumière de
vitrine ; - feedback de sélection ; - transition d'entrée.

**Grammaire :** - montgolfière = dérive du monde ; - avion = événement
du ciel ; - maison = réponse au visiteur ; - anneau = passage ; -
produit = calme.

------------------------------------------------------------------------

# 7. Règles anti-surcharge

Tout ce qui peut bouger ne doit pas bouger.

Avant d'ajouter une animation, répondre : 1. Quelle fonction
remplit-elle ? 2. Améliore-t-elle la compréhension, la présence ou le
plaisir ? 3. Reste-t-elle agréable après plusieurs visites ? 4. Est-elle
compatible mobile et reduced motion ? 5. Son absence laisse-t-elle une
scène toujours belle ?

Si la réponse est non : ne pas l'ajouter.

Principe : \> **ORAA crée suffisamment d'identité pour pouvoir laisser
de l'espace.**

------------------------------------------------------------------------

# 8. Orientation et navigation

Un nouveau visiteur doit comprendre rapidement : - où il est ; - ce
qu'est ORAA ; - quelles maisons sont disponibles ; - qu'elles sont
cliquables ; - comment chercher directement un produit ; - comment
accéder au panier/compte ; - comment revenir au Monde ORAA depuis une
maison.

Le Monde ne doit jamais sacrifier les conventions essentielles du
commerce à l'immersion.

Prévoir une navigation ORAA claire en complément de la scène.

------------------------------------------------------------------------

# 9. Recherche et accès direct

L'expérience immersive ne doit pas forcer tous les visiteurs à explorer.

Un client qui sait déjà ce qu'il veut doit pouvoir : - rechercher ; -
accéder à une collection ; - retrouver son panier ; - ouvrir son compte
; - atteindre un produit rapidement.

**Exploration et efficacité doivent coexister.**

------------------------------------------------------------------------

# 10. Merchandising du Monde

Le Monde ORAA peut refléter l'activité commerciale sans devenir une
homepage promotionnelle saturée.

Possibilités : - produit vedette en vitrine ; - campagne visible dans
une fenêtre/écran ; - changement éditorial saisonnier ; - nouveauté mise
en avant ; - décoration légère liée à un moment pertinent.

Les contenus variables doivent être administrables depuis Shopify autant
que raisonnablement possible.

Interdit : - accumulation de badges ; - panneaux promotionnels partout
; - multiplication des pop-ups ; - prix clignotants dans le village ; -
transformation du Monde en catalogue.

------------------------------------------------------------------------

# 11. Passage vers les mini-univers

Parcours : **Monde ORAA → maison → mini-univers éditorial → contenu +
produits → fiche produit → panier → checkout**

Une maison ne doit pas simplement ouvrir une grille Shopify standard.

Chaque mini-univers peut contenir : - hero éditorial ; - produit phare
; - nouveautés ; - vidéos publicitaires ; - démonstrations ; - guides
; - articles ; - sélections ; - catalogue.

La Maison pilote Tech & Accessoires est spécifiée séparément dans :
`ORAA_SHOPIFY_EXPERIENCE_SYSTEM_MAISON_PILOTE_TECH.md`

------------------------------------------------------------------------

# 12. Cohérence de marque

Chaque maison peut avoir : - ambiance ; - accent ; - matières ; - rythme
éditorial ; - contenu ; - type de médias ; différents.

Mais restent communs : - identité ORAA ; - logo/anneau ; - principes
typographiques ; - navigation ; - composants UI ; - règles commerciales
; - motion language ; - accessibilité ; - qualité photographique ; -
système transactionnel.

**Même ville. Différentes maisons.**

------------------------------------------------------------------------

# 13. Trois niveaux techniques du Monde

## Niveau A --- Expérience complète

Pour appareils/conditions adaptés : - scène complète ; - animations
ambiantes ; - interactions ; - transitions ; - merchandising vivant.

## Niveau B --- Expérience allégée

Pour mobile ou contraintes : - moins d'animations ; - assets optimisés
; - mouvements secondaires supprimés ; - même composition et identité.

## Niveau C --- Statique premium

Fallback : - scène statique magnifiquement composée ; - enseignes et
navigation totalement fonctionnelles ; - aucun besoin d'animation pour
comprendre ou apprécier ORAA.

Le choix du niveau doit dépendre de critères techniques mesurables, pas
d'un user-agent fragile uniquement.

------------------------------------------------------------------------

# 14. Mobile

Le mobile doit être conçu, pas seulement redimensionné.

À définir/tester : - cadrage du Monde ; - visibilité des maisons ; -
taille des textes ; - zones tactiles ; - priorité des bâtiments ; -
navigation ; - performance ; - ordre de découverte ; - animations
conservées/supprimées ; - comportement portrait/paysage pertinent.

Aucun texte critique ne doit être intégré uniquement dans une image
raster si cela nuit à la lisibilité, à l'accessibilité ou à
l'administration.

------------------------------------------------------------------------

# 15. Performance

Le « waouh » ne justifie pas un site lent.

Exigences : - optimisation des images ; - formats modernes ; -
responsive images ; - lazy loading hors viewport ; - vidéo chargée
intelligemment ; - animation privilégiant transform/opacity ; - pas de
dépendance lourde sans justification ; - contrôle des Core Web Vitals
; - prévention CLS ; - fallbacks ; - budget de poids documenté avant
production.

Claude Code doit mesurer avant/après chaque ajout visuel significatif.

------------------------------------------------------------------------

# 16. Accessibilité

Le Monde doit rester exploitable : - au clavier ; - au toucher ; - avec
réduction des mouvements ; - avec technologies d'assistance pertinentes
; - avec zoom texte ; - avec contraste suffisant.

Les maisons doivent être de vrais éléments interactifs sémantiques.

Les enseignes ne doivent pas être le seul moyen d'identifier une
destination si leur rendu visuel peut devenir inaccessible.

------------------------------------------------------------------------

# 17. Shopify --- administration

Prévoir autant que possible des réglages pour : - maison active/inactive
selon décisions validées ; - nom affiché ; - destination ; -
produit/campagne de vitrine ; - média ; - texte éditorial ; - CTA ; -
ordre ; - accent autorisé ; - contenus des mini-univers.

Utiliser selon pertinence : - sections ; - blocks ; - metafields ; -
metaobjects ; - sources dynamiques ; - templates JSON.

Ne pas hardcoder ce qui est destiné à évoluer régulièrement.

------------------------------------------------------------------------

# 18. Brand tokens et composants

Le Monde doit utiliser le même système programmable que le reste d'ORAA
: - couleurs ; - typo ; - espacements ; - états interactifs ; - focus
; - boutons ; - vitesses ; - easing ; - couches/z-index documentées ; -
styles d'enseigne ; - règles de lumière ; - composants de navigation.

Pas de valeurs arbitraires répétées dans plusieurs fichiers si un token
ou composant commun est approprié.

------------------------------------------------------------------------

# 19. Sécurité et robustesse

Les effets visuels ne doivent pas : - introduire des scripts tiers
inutiles ; - nécessiter des permissions inhabituelles ; - casser la
navigation sans JavaScript ; - empêcher les fonctions Shopify
essentielles ; - exposer des données sensibles ; - compromettre CSP ou
bonnes pratiques du thème.

Progressive enhancement privilégié.

------------------------------------------------------------------------

# 20. Ce que Claude Code ne décide pas seul

Sans validation humaine : - identité maîtresse ; - nouvel anneau ; -
nouvelle palette maîtresse ; - taxonomie ; - noms de collections ; -
exposition d'une catégorie roadmap ; - prix ; - promotions ; - promesses
commerciales ; - garanties ; - nouveaux effets majeurs ; - changement
radical du Monde ; - suppression d'un élément fondateur ; - technologie
lourde structurante ; - déploiement production.

Claude doit signaler les contradictions plutôt que les résoudre
silencieusement.

------------------------------------------------------------------------

# 21. Méthode d'implémentation

Avant de coder : 1. lire le handover ; 2. lire les lois/Codex
applicables ; 3. lire ADR ; 4. lire taxonomie ; 5. lire design/brand
system ; 6. lire ce document ; 7. lire la spécification Maison pilote
Tech ; 8. inspecter le thème Shopify réel ; 9. présenter les écarts ;
10. proposer architecture et plan ; 11. attendre validation pour les
décisions structurantes.

Puis construire par lots testables.

------------------------------------------------------------------------

# 22. Tests du Monde

Tester au minimum : - desktop large ; - laptop ; - tablette ; - mobile
courant ; - petit mobile ; - tactile ; - clavier ; - reduced motion ; -
connexion lente simulée ; - JavaScript dégradé si pertinent ; -
navigation maison → retour Monde ; - recherche directe ; - panier ; -
lisibilité des enseignes.

------------------------------------------------------------------------

# 23. Definition of Done --- Monde ORAA

Le Monde est validé uniquement si :

### Identité

-   reconnaissable comme ORAA ;
-   anneau fidèle ;
-   direction lumineuse/aérienne respectée ;
-   aucune impression de thème générique.

### Compréhension

-   les collections sont clairement identifiables ;
-   les maisons paraissent interactives ;
-   recherche/navigation restent accessibles.

### Magie

-   scène belle statiquement ;
-   montgolfière crédible ;
-   avion crédible et occasionnel ;
-   enseignes qui s'illuminent élégamment ;
-   mouvement subtil.

### Respiration

-   pas de surcharge ;
-   zones calmes ;
-   hiérarchie visuelle évidente.

### Commerce

-   accès produit simple ;
-   merchandising maîtrisé ;
-   aucune friction créée par l'immersion.

### Mobile

-   expérience pensée spécifiquement ;
-   aucune dépendance au hover ;
-   performances acceptables.

### Accessibilité

-   clavier/focus ;
-   reduced motion ;
-   contrastes ;
-   sémantique ;
-   alternatives.

### Administration

-   campagnes et contenus récurrents modifiables sans recoder autant que
    raisonnablement possible.

### Technique

-   architecture maintenable ;
-   progressive enhancement ;
-   assets optimisés ;
-   mesures de performance disponibles.

------------------------------------------------------------------------

# 24. Critère ultime

Le visiteur ne doit pas penser :

« Ils ont mis une jolie animation sur une boutique Shopify. »

Il doit ressentir :

**« Je suis entré dans ORAA. »**

Puis, au moment d'acheter, tout doit devenir si simple qu'il n'a plus
besoin de penser à l'interface.

------------------------------------------------------------------------

## Références liées

-   Codex / lois ORAA du repository
-   ADR applicables
-   Taxonomie ORAA
-   Brand System ORAA
-   `ORAA_SHOPIFY_EXPERIENCE_SYSTEM_MAISON_PILOTE_TECH.md`
-   Handover Claude Code dans `20_AI_PACKAGE/HANDOVER_CLAUDE_CODE.md`

**Ce document est une spécification de conception. Il ne constitue pas
une autorisation de déploiement ou de modification autonome de la
boutique Shopify en production.**
