# ORAA SHOPIFY EXPERIENCE SYSTEM

## Maison pilote --- Tech & Accessoires / « L'Atelier Tech »

**Statut :** Spécification de conception --- pré-implémentation\
**Projet :** ORAA Shopify exclusivement --- ne pas confondre avec un
ancien projet WordPress\
**Rôle :** Maison pilote servant à définir le système réutilisable des
mini-univers de collection ORAA

------------------------------------------------------------------------

## 0. Intention

ORAA ne doit pas se comporter comme un catalogue Shopify décoré. Le
visiteur entre dans un monde, choisit une maison, découvre un univers
éditorial, comprend les produits, puis achète dans une interface
progressivement plus calme et plus claire.

**Principe directeur :**\
\> Les collections ORAA ne sont pas seulement des rayons. Ce sont des
endroits dans lesquels on entre.

**Rythme de l'expérience :**\
**WAOUH → respiration → découverte → respiration → désir → confiance →
transaction → souvenir.**

Le « waouh » est concentré là où il apporte de la valeur. L'identité
ORAA reste reconnaissable partout, mais n'occupe pas tout l'espace.

------------------------------------------------------------------------

# 1. Position de Tech & Accessoires dans le Monde ORAA

## 1.1 Nom extérieur

Sur la maison visible depuis le Monde ORAA :

**TECH & ACCESSOIRES**

Le nom commercial doit être immédiatement compréhensible. Il prime sur
tout intitulé narratif.

## 1.2 Nom intérieur

Après l'entrée dans la collection :

**L'ATELIER TECH**\
Sous-titre / repère : **Tech & Accessoires**

Le nom narratif enrichit l'expérience une fois que le visiteur sait
clairement où il se trouve.

## 1.3 Fonction de la maison pilote

Tech & Accessoires sert de prototype pour définir : - l'entrée depuis le
Monde ORAA ; - les interactions d'une maison ; - le template éditorial
d'une collection ; - le système vidéo ; - le merchandising ; - les blocs
Shopify administrables ; - le comportement mobile ; - les règles
d'animation ; - les règles de performance et d'accessibilité ; - le
passage de l'immersion au commerce.

Le système devra ensuite être réutilisable pour les autres maisons sans
les rendre identiques.

------------------------------------------------------------------------

# 2. Le Monde ORAA --- comportement commun

## 2.1 Direction artistique

Le Monde ORAA est : - lumineux ; - aérien ; - réaliste avec une part de
merveilleux ; - chaleureux ; - européen dans son architecture et son
atmosphère ; - riche mais jamais encombré ; - cinématographique sans
filtre jaune excessif.

Éléments caractéristiques : - ciel bleu et profondeur ; - eau et
végétation ; - architecture/village ; - rosiers rouges discrets ; -
espaces de respiration ; - montgolfière ORAA ; - avion dans le ciel ; -
maisons correspondant aux collections.

## 2.2 Mouvement ambiant

Le monde vit même lorsque le visiteur ne fait rien, mais très
subtilement.

**Montgolfière :** dérive lente, naturelle, sans boucle visuellement
mécanique.\
**Avion :** traversée occasionnelle du ciel, non permanente.\
**Eau :** micro-mouvement discret si techniquement pertinent.\
**Végétation :** mouvement presque imperceptible.\
**Nuages / atmosphère :** mouvement lent éventuel.

Règle : le mouvement ne doit jamais détourner l'attention de la
navigation ou dégrader la performance.

## 2.3 Réaction des maisons

Au repos, les maisons sont calmes.

Au survol d'une maison sur desktop : 1. son enseigne s'illumine
progressivement ; 2. le nom de collection devient plus présent ; 3. la
vitrine / certaines lumières peuvent gagner légèrement en intensité ; 4.
une invitation discrète telle que « Entrer » peut apparaître ; 5. aucun
zoom brutal, clignotement ou animation agressive.

Quand le curseur quitte la maison, l'état revient doucement à la
normale.

**Principe :** l'intérêt du visiteur « réveille » la maison.

## 2.4 Mobile / tactile

Aucune information indispensable ne doit dépendre du hover.

Le comportement tactile doit permettre : - de comprendre immédiatement
que la maison est interactive ; - d'identifier son nom ; - de recevoir
un feedback visuel au toucher ; - d'entrer facilement sans ambiguïté.

Le détail exact « premier toucher = sélection / second toucher = entrée
» devra être testé en UX ; ne pas l'imposer si une entrée directe avec
feedback est plus naturelle.

------------------------------------------------------------------------

# 3. L'anneau ORAA

## 3.1 Référence

L'anneau de référence est : - ouvert ; - métallique doré ; - avec
profondeur intérieure bleu nuit ; - avec une lumière bleue intense,
notamment vers sa partie basse ; - évocateur d'un portail, d'un passage,
d'une ouverture.

Il ne doit pas être remplacé par un cercle doré générique.

## 3.2 Fonction

L'anneau est une **signature**, pas un motif décoratif omniprésent.

Usages possibles : - transition entre Monde ORAA et maison ; - moment de
passage ; - signature de marque ; - certains moments post-achat ; -
favicon / petit format via une déclinaison spécifiquement conçue.

## 3.3 Animation

Préférer l'idée d'**activation du passage** : - lumière bleue qui
s'éveille ; - profondeur qui devient perceptible ; - transition courte
; - puis disparition / passage vers la destination.

Éviter : - spinner informatique ; - rotation permanente ; - apparition
répétitive sans fonction ; - multiplication de l'anneau sur toutes les
sections.

------------------------------------------------------------------------

# 4. Entrée dans Tech & Accessoires

## 4.1 Séquence cible

**Monde ORAA → survol/toucher de Tech & Accessoires → enseigne éclairée
→ clic → réaction courte de la maison → passage / transition ORAA →
L'Atelier Tech.**

## 4.2 Durée

La transition doit être courte et ne jamais devenir un obstacle.

Elle doit : - donner la sensation d'entrer ; - conserver le contexte ; -
ne pas ressembler à un écran de chargement artificiel ; - pouvoir être
raccourcie ou supprimée selon performance, accessibilité ou préférence
de réduction des mouvements.

## 4.3 Retour

Le visiteur doit toujours pouvoir revenir facilement au Monde ORAA.

Le retour ne doit pas dépendre du bouton « précédent » du navigateur
uniquement.

------------------------------------------------------------------------

# 5. Architecture éditoriale de L'Atelier Tech

La page ne commence pas par une grille de 40 produits.

## Section A --- Arrivée / respiration

Objectif : faire sentir l'univers Tech ORAA immédiatement.

Contenu : - titre « L'Atelier Tech » ; - repère « Tech & Accessoires »
; - phrase éditoriale courte ; - image ou vidéo héro forte ; - CTA
secondaire éventuel vers la sélection principale.

La scène doit laisser beaucoup d'air.

## Section B --- À découvrir

Une petite sélection éditorialisée : - produit phare ; - nouveauté ; -
sélection ORAA ; - éventuellement une innovation ou produit inattendu.

Pas de catalogue exhaustif ici.

## Section C --- Voir en action

Vidéos de démonstration : - produit utilisé réellement ; - bénéfice
visible ; - format court ; - contrôles accessibles ; - pas d'autoplay
sonore.

Une publicité raconte.\
Une démonstration prouve.

## Section D --- Histoires / campagnes

Vidéos ou visuels publicitaires plus émotionnels.

Objectif : - donner envie ; - construire la marque ; - présenter des
usages ou scénarios.

Ces contenus doivent rester distincts des démonstrations factuelles.

## Section E --- Choisir le bon produit

Selon la gamme : - guide de choix ; - comparatif ; - critères importants
; - réponses aux questions fréquentes ; - liens vers les produits
concernés.

Ne créer un comparatif que s'il aide réellement à décider.

## Section F --- Nouveautés

Bloc administrable Shopify permettant de sélectionner ou alimenter
automatiquement les nouveautés selon la stratégie retenue.

## Section G --- Conseils & journal

Articles liés à Tech & Accessoires : - comment choisir ; - comment
utiliser ; - entretien ; - idées d'usage ; - guides ; - contenus
éditoriaux pertinents.

Le blog ne doit pas être ajouté pour « faire du SEO » sans valeur pour
le lecteur.

## Section H --- Catalogue

Après la découverte, le visiteur peut accéder à la collection complète
: - filtres utiles ; - tri ; - cartes produit cohérentes ; - chargement
performant ; - navigation claire.

## Section I --- Réassurance

Selon les engagements réellement disponibles : - livraison ; - retours
; - paiement ; - assistance ; - garanties.

Ne jamais inventer un engagement commercial.

------------------------------------------------------------------------

# 6. Merchandising vivant depuis le Monde ORAA

La maison Tech peut refléter la campagne du moment.

Exemples : - produit vedette visible dans une vitrine ; - écran discret
présentant une campagne ; - changement de visuel saisonnier ; -
nouveauté mise en avant.

**Exigence clé :** ces changements doivent être administrables depuis
Shopify autant que possible, sans modification du code à chaque
campagne.

Le Monde ORAA devient ainsi un espace de merchandising, mais ne doit
jamais devenir un panneau publicitaire surchargé.

------------------------------------------------------------------------

# 7. Fiches produit --- règle de calme

Lorsqu'on arrive sur une fiche produit, le produit devient le héros.

Priorités : 1. comprendre immédiatement le produit ; 2. voir des images
réalistes et détaillées ; 3. comprendre variantes / options ; 4.
connaître le prix sans ambiguïté ; 5. comprendre les principaux
bénéfices ; 6. disposer de preuves / démonstrations pertinentes ; 7.
connaître livraison, retours et garanties réelles ; 8. ajouter au panier
sans friction.

L'identité ORAA reste présente par : - typographie ; - proportions ; -
espacements ; - boutons ; - iconographie ; - micro-interactions ; -
traitement photo/vidéo ; - signatures mesurées.

Elle ne doit pas concurrencer le produit.

------------------------------------------------------------------------

# 8. Brand System --- intensité

Guide d'intensité, non règle mathématique :

-   **Monde ORAA : 100 %** --- spectacle et découverte.
-   **Maison / collection : \~60 %** --- forte personnalité +
    respiration.
-   **Produit : \~30 %** --- ORAA accompagne, produit domine.
-   **Checkout : \~10 %** --- ORAA signe, la transaction domine.
-   **Post-achat : remontée émotionnelle mesurée** --- créer le
    souvenir.

**Harmoniser ne signifie pas uniformiser.**

Une maison peut avoir une ambiance propre tout en appartenant clairement
au même monde.

------------------------------------------------------------------------

# 9. Système de marque programmable

Claude Code doit implémenter une source de vérité unique plutôt que
répéter des valeurs arbitraires.

À prévoir : - couleurs / design tokens ; - typographies ; - tailles et
hiérarchies ; - espacements ; - rayons / formes ; - ombres si utilisées
; - composants bouton ; - cartes produit ; - navigation ; - formulaires
; - états hover/focus/active/disabled ; - vitesses et courbes
d'animation ; - règles de motion ; - styles vidéo ; - styles éditoriaux.

Objectif : une évolution à la source doit pouvoir se propager proprement
dans la boutique.

------------------------------------------------------------------------

# 10. Photographie et vidéo

## Monde

Peut être : - cinématographique ; - narratif ; - merveilleux ; -
immersif.

## Produit

Doit rester : - crédible ; - lisible ; - précis ; - utile ; - fidèle à
ce que le client recevra.

Prévoir : - vues générales ; - gros plans ; - échelle ; - détails de
matière ; - utilisation ; - démonstration.

Ne jamais sacrifier la compréhension du produit au spectaculaire.

------------------------------------------------------------------------

# 11. Motion System

Trois mots : **lent --- naturel --- intentionnel.**

Chaque mouvement doit avoir une fonction.

### Mouvement ambiant

Montgolfière, avion, eau, végétation : donne vie au monde.

### Mouvement réactif

Maison / enseigne : répond à l'intérêt du visiteur.

### Mouvement de passage

Anneau / transition : matérialise l'entrée.

### Mouvement commercial

Très réduit : feedback bouton, ajout panier, états UI.

### Produit

Calme.

Respect obligatoire de `prefers-reduced-motion` et d'une expérience
pleinement fonctionnelle sans animation.

------------------------------------------------------------------------

# 12. Mobile-first et responsive

Le Monde ORAA ne doit pas être une grande image desktop simplement
rétréccie.

À tester spécifiquement : - lisibilité des enseignes ; - taille des
zones tactiles ; - ordre des maisons ; - recadrage de la scène ; - poids
des assets ; - suppression / simplification d'animations ; - navigation
à une main ; - vitesse sur réseau mobile ; - stabilité de mise en page.

Si une animation nuit à la performance mobile, la performance gagne.

------------------------------------------------------------------------

# 13. Accessibilité

Minimum attendu : - navigation clavier ; - focus visible ; - contraste
suffisant ; - textes lisibles ; - alternatives textuelles pertinentes
; - contrôles vidéo accessibles ; - aucun contenu essentiel uniquement
au hover ; - réduction des mouvements ; - structure sémantique ; -
labels corrects ; - tailles tactiles adaptées.

Le merveilleux ORAA ne doit exclure personne.

------------------------------------------------------------------------

# 14. Performance

Le Monde ORAA peut être spectaculaire, mais doit respecter un budget
technique.

Claude Code devra : - privilégier CSS/SVG/assets optimisés quand
pertinent ; - charger les médias lourds intelligemment ; - lazy-loader
ce qui n'est pas immédiatement nécessaire ; - éviter les bibliothèques
lourdes sans justification ; - proposer une stratégie desktop/mobile ; -
mesurer les Core Web Vitals ; - éviter que les animations provoquent des
déplacements de layout ; - prévoir des fallbacks statiques élégants.

Aucune technologie (WebGL, vidéo lourde, etc.) ne doit être utilisée
uniquement parce qu'elle est possible.

------------------------------------------------------------------------

# 15. Administration Shopify

Le système doit être pensé pour que l'équipe puisse, autant que
raisonnablement possible, modifier sans coder : - produit vedette ; -
nouveautés ; - collections ; - image/vidéo hero ; - campagnes ; -
vitrine de maison ; - articles ; - guides ; - textes ; - CTA ; - ordre
des sections ; - activation/désactivation de blocs.

Préférer : - sections Shopify configurables ; - blocks ; -
metafields/metaobjects lorsque pertinents ; - sources dynamiques ; -
templates réutilisables.

Éviter le contenu stratégique hardcodé dans le thème lorsqu'il doit
changer régulièrement.

------------------------------------------------------------------------

# 16. Architecture réutilisable

Claude Code ne doit pas créer « une page Tech spéciale » impossible à
maintenir.

Il doit identifier : - ce qui appartient au système commun ; - ce qui
appartient à Tech ; - ce qui doit devenir configurable ; - ce qui doit
être un composant ; - ce qui peut être un template ; - ce qui nécessite
un asset spécifique.

Les autres maisons devront pouvoir partager le moteur tout en changeant
: - ambiance ; - accent ; - contenus ; - ordre éditorial ; - médias ; -
types de guides ; - merchandising.

**Même ville. Différentes maisons.**

------------------------------------------------------------------------

# 17. Ce que Claude Code ne doit pas décider seul

Sans validation humaine explicite, Claude Code ne doit pas : - redéfinir
l'identité ORAA ; - remplacer l'anneau de référence ; - inventer une
nouvelle palette maîtresse ; - changer la taxonomie ; - renommer une
collection ; - modifier prix ou promotions ; - corriger une anomalie
commerciale de sa propre initiative ; - supprimer du contenu stratégique
; - inventer des garanties, délais ou promesses ; - ajouter des effets
visuels majeurs non prévus ; - installer une dépendance lourde sans
justification ; - transformer l'expérience en thème Shopify générique
; - modifier Shopify en production avant autorisation explicite.

En cas de contradiction entre sources : documenter et demander
validation.

------------------------------------------------------------------------

# 18. Parcours cible

**MONDE ORAA**\
↓\
Maison **TECH & ACCESSOIRES**\
↓\
Enseigne qui s'éveille\
↓\
Entrée / passage ORAA\
↓\
**L'ATELIER TECH**\
↓\
Hero éditorial\
↓\
À découvrir\
↓\
Voir en action\
↓\
Campagnes / histoires\
↓\
Guides / comparatifs / conseils\
↓\
Nouveautés\
↓\
Catalogue\
↓\
Fiche produit\
↓\
Panier\
↓\
Checkout\
↓\
Confirmation\
↓\
Suivi / après-vente\
↓\
Souvenir ORAA

------------------------------------------------------------------------

# 19. Critères de validation --- Definition of Done

La maison pilote n'est validée que si :

### Identité

-   elle est immédiatement reconnaissable comme ORAA ;
-   elle respecte l'anneau et les codes de marque ;
-   elle possède une personnalité Tech sans devenir une marque séparée.

### Expérience

-   l'entrée depuis le Monde ORAA est compréhensible ;
-   la maison paraît vivante mais jamais agitée ;
-   la transition a une fonction ;
-   la page respire ;
-   l'utilisateur peut revenir au Monde ORAA.

### Commerce

-   le produit reste prioritaire au moment de l'achat ;
-   prix, variantes, CTA et réassurance sont clairs ;
-   aucun effet ne gêne la conversion.

### Contenu

-   vidéo publicitaire et démonstration sont distinguées ;
-   articles et guides ont une fonction réelle ;
-   le catalogue reste facilement accessible.

### Administration

-   les contenus récurrents peuvent être mis à jour depuis Shopify ;
-   les campagnes ne nécessitent pas systématiquement un développeur.

### Technique

-   responsive ;
-   performant ;
-   accessible ;
-   compatible réduction des mouvements ;
-   composants réutilisables ;
-   pas de dépendance inutile.

### Cohérence

-   aucun passage ne donne l'impression de quitter ORAA pour « tomber
    dans Shopify ».

------------------------------------------------------------------------

# 20. Principe final

ORAA ne remplit pas l'espace pour prouver son identité.

**ORAA crée suffisamment d'identité pour pouvoir laisser de l'espace.**

La technologie doit servir cette expérience, jamais devenir la direction
artistique.

Le visiteur doit pouvoir : **voir le Monde → avoir envie d'entrer →
découvrir → comprendre → désirer → faire confiance → acheter → se
souvenir.**

------------------------------------------------------------------------

## Note d'implémentation

Ce document constitue une **spécification de conception**. Il ne donne
pas, à lui seul, autorisation de modifier une boutique Shopify en
production. Avant implémentation, Claude Code doit le confronter au
handover, aux ADR, au design system, à la taxonomie et aux autres
sources de vérité du repository, signaler toute contradiction et
présenter son plan d'exécution pour validation.
