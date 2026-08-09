# ORAA SHOPIFY --- HOUSES SYSTEM

## Système des maisons / collections --- Spécification de conception

**Statut :** Pré-implémentation\
**Périmètre :** ORAA Shopify exclusivement\
**But :** définir la personnalité et l'expérience des maisons tout en
conservant un moteur ORAA commun.

> Les collections ORAA ne sont pas seulement des rayons. Ce sont des
> endroits dans lesquels on entre.

------------------------------------------------------------------------

# 1. Taxonomie de référence

Menu principal actuellement retenu dans le travail ORAA : 1. Maison &
Hygiène 2. Mode 3. Enfants & Bébés 4. Foi & Transmission 5. Cadeaux &
Box 6. Voyage & Aventure 7. Tech & Accessoires 8. Packs & Offres

**Important :** avant implémentation, confronter cette liste au
`TAXONOMY.md` et au handover du repository. Toute divergence de statut,
notamment exposition/roadmap, doit être signalée et non résolue
silencieusement par Claude Code.

**Distinction à préserver :** - Cadeaux & Box = offrir, célébrer,
attention portée à quelqu'un. - Packs & Offres = s'équiper, regrouper,
avantage commercial/prix lorsqu'il est réel.

------------------------------------------------------------------------

# 2. Moteur commun

Toutes les maisons partagent : - navigation ORAA ; - système de marque
; - composants UI ; - logique d'entrée ; - règles de motion ; -
accessibilité ; - performance ; - administration Shopify ; - système
produit/panier/checkout ; - possibilité de revenir au Monde ORAA.

Chaque maison peut adapter : - ambiance ; - vitrine ; - accent visuel
; - hero ; - ordre éditorial ; - type de vidéos ; - guides ; -
merchandising.

**Même ville. Différentes maisons.**

------------------------------------------------------------------------

# 3. Maison & Hygiène

## Rôle

Faire ressentir l'amélioration concrète du quotidien : maison, soin,
hygiène, routines et objets utiles.

## Expérience dominante

**Voir → comprendre l'usage → imaginer chez soi → adopter.**

## Vitrine

Une scène de vie élégante plutôt qu'un empilement de produits.

## Contenus

-   routines ;
-   démonstrations ;
-   avant/après uniquement lorsqu'ils sont honnêtes et pertinents ;
-   conseils d'usage et d'entretien ;
-   sélections par besoin ;
-   nouveautés ;
-   produits.

## Ton

Clair, propre, chaleureux, pratique.

## Mouvement

Très calme : lumière, eau ou détail domestique subtil selon le média.
Pas d'animation gadget.

------------------------------------------------------------------------

# 4. Mode

## Rôle

Permettre de voir les pièces portées, les matières et les associations.

## Expérience dominante

**Voir → se projeter → associer → choisir.**

## Vitrine

Silhouette, textile ou composition éditoriale.

## Contenus

-   looks ;
-   pièces vedettes ;
-   matières/détails ;
-   vidéos portées ;
-   associations ;
-   guide tailles si données fiables ;
-   sélections ;
-   catalogue.

## Ton

Élégant, vivant, simple.

## Règle

L'éditorial ne doit jamais rendre les tailles, variantes, matières ou
conditions de retour difficiles à comprendre.

------------------------------------------------------------------------

# 5. Enfants & Bébés

## Rôle

Créer un univers vivant et chaleureux tout en donnant aux adultes les
informations nécessaires pour acheter sereinement.

## Expérience dominante

**Découvrir → comprendre → rassurer → choisir.**

## Vitrine

Plus vivante et joyeuse, mais toujours cohérente avec le Monde ORAA.

## Contenus

-   produits en situation ;
-   âge/usage lorsque réellement applicable ;
-   démonstrations ;
-   idées ;
-   sélections ;
-   contenus utiles aux parents ;
-   informations de sécurité produit lorsque nécessaires.

## Règle

Ne pas transformer l'univers en interface surstimulante. La sécurité et
la compréhension priment.

------------------------------------------------------------------------

# 6. Foi & Transmission

## Rôle

Créer un espace plus calme autour des objets, livres, apprentissages et
produits appartenant réellement à cette collection.

## Expérience dominante

**Entrer → ralentir → découvrir → comprendre → choisir.**

## Vitrine

Composition sobre, lumineuse et respectueuse.

## Contenus

-   livres/objets ;
-   présentation approfondie ;
-   extraits ou aperçus lorsque les droits le permettent ;
-   guides ;
-   transmission/apprentissage ;
-   sélections ;
-   produits.

## Ton

Respectueux, clair, jamais caricatural.

## Règle

Éviter l'ornementation gratuite et toute affirmation religieuse ou
éducative inventée. Les informations doivent être sourcées/validées
selon leur nature.

------------------------------------------------------------------------

# 7. Cadeaux & Box

## Rôle

Aider le client à trouver quelque chose pour quelqu'un ou pour un moment
particulier.

## Expérience dominante

**Pour qui ? → pour quelle occasion ? → quelle attention ? → choisir.**

## Vitrine

Mise en scène d'un cadeau ou d'une box, avec sensation d'attention et de
découverte.

## Contenus

-   sélections par destinataire/occasion lorsque pertinentes ;
-   box ;
-   idées cadeaux ;
-   contenu de la box clairement détaillé ;
-   emballage si réellement disponible ;
-   nouveautés ;
-   produits.

## Ton

Généreux, chaleureux, jamais pressant.

## Règle

Ne pas confondre avec Packs & Offres.

------------------------------------------------------------------------

# 8. Voyage & Aventure

## Statut

La maison existe dans la taxonomie de travail historique, mais **son
statut d'exposition doit impérativement être vérifié dans le repository
avant implémentation**. Si la décision la plus récente indique
roadmap/non exposé, elle ne doit pas apparaître au lancement.

## Si/Quand activée

Expérience dominante : **Préparer → partir → utiliser → revenir.**

Contenus potentiels : - usages en déplacement ; - organisation ; -
démonstrations ; - sélections par contexte ; - guides pratiques ; -
produits.

Aucun contenu ne doit être construit en production tant que son statut
n'est pas confirmé.

------------------------------------------------------------------------

# 9. Tech & Accessoires

Maison pilote déjà documentée dans :
`ORAA_SHOPIFY_EXPERIENCE_SYSTEM_MAISON_PILOTE_TECH.md`

Expérience dominante : **Découvrir → voir fonctionner → comparer si
utile → comprendre → choisir.**

Elle sert de référence d'architecture, pas de modèle éditorial à copier
mot pour mot.

------------------------------------------------------------------------

# 10. Packs & Offres

## Rôle

Permettre de s'équiper intelligemment et de comprendre la valeur d'un
regroupement.

## Expérience dominante

**Besoin → composition → valeur → choix.**

## Vitrine

Composition claire de plusieurs produits formant un ensemble.

## Contenus

-   ce qui est inclus ;
-   pourquoi les produits sont regroupés ;
-   comparaison achat séparé / pack uniquement si les prix réels
    permettent de l'affirmer ;
-   usages ;
-   packs populaires ;
-   offres réellement actives.

## Règles commerciales

-   aucun faux prix barré ;
-   aucune économie inventée ;
-   aucune urgence artificielle ;
-   aucune promotion créée par Claude Code.

------------------------------------------------------------------------

# 11. Vitrines dynamiques

Chaque maison peut disposer d'une vitrine administrable : - média
vedette ; - produit ; - campagne ; - nouveauté ; - message court.

Le Monde ORAA peut ainsi évoluer sans recodage.

La vitrine ne doit pas devenir un panneau promotionnel permanent.

------------------------------------------------------------------------

# 12. Interaction commune des façades

Au repos : - enseigne lisible ; - maison calme.

Au survol : - enseigne qui s'allume progressivement ; - lumière/vitrine
légèrement réveillée ; - feedback élégant.

Au toucher : - feedback tactile/visuel ; - aucune dépendance au hover.

À l'entrée : - transition courte ; - anneau possible comme passage ; -
mini-univers.

------------------------------------------------------------------------

# 13. Variation sans fragmentation

Une maison n'a pas le droit de créer : - sa propre navigation
incompatible ; - son propre système de boutons ; - ses propres règles de
prix ; - son propre panier ; - une typographie arbitraire ; - une
identité qui ferait oublier ORAA.

La personnalité vient principalement : - du contenu ; - des médias ; -
du rythme ; - de la vitrine ; - de l'accent ; - de l'éditorial.

------------------------------------------------------------------------

# 14. Administration Shopify

Architecture cible : - template de maison réutilisable ; - sections
configurables ; - blocks ; - metaobjects/metafields si pertinents ; -
sélections de produits/collections ; - vidéos/images administrables ; -
ordre des sections modifiable dans des limites de marque.

Prévoir des garde-fous pour éviter qu'une édition courante casse
l'identité.

------------------------------------------------------------------------

# 15. Mobile

Chaque maison doit conserver son caractère avec moins d'effets.

Priorités : 1. nom ; 2. orientation ; 3. contenu vedette ; 4. produits ;
5. CTA ; 6. performance.

Pas de mini-version illisible de la scène desktop.

------------------------------------------------------------------------

# 16. Definition of Done --- système des maisons

Le système est prêt lorsque : - la taxonomie exposée est confirmée avec
le repository ; - chaque maison a une fonction distincte ; - le moteur
commun est identifié ; - les variations sont configurables ; - les
vitrines sont administrables ; - les interactions sont cohérentes ; -
mobile et accessibilité sont prévus ; - aucune maison ne ressemble à une
boutique séparée ; - les règles commerciales sont communes ; - Tech peut
être implémentée comme pilote sans empêcher les autres univers.

------------------------------------------------------------------------

# 17. Principe final

Le visiteur doit pouvoir parcourir plusieurs maisons et sentir :

**« Je change d'endroit, mais je suis toujours dans ORAA. »**
