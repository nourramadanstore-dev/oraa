# ORAA SHOPIFY --- MASTER INDEX & CROSS-AUDIT

## Package de conception pour Claude Code

**Date de consolidation :** 8 août 2026\
**Statut :** Audit de cohérence pré-implémentation\
**Projet :** ORAA Shopify exclusivement

------------------------------------------------------------------------

# 1. Conclusion exécutive

Les six nouvelles spécifications ORAA Shopify sont globalement
cohérentes entre elles et avec les lois fondamentales retrouvées dans le
repository.

Elles ne doivent cependant **pas encore être interprétées comme une
autorisation de construction ou de déploiement**.

Avant tout travail lourd, Claude Code doit confronter le package au
repository réel et résoudre par validation humaine les quelques points
encore ouverts identifiés dans ce document.

------------------------------------------------------------------------

# 2. Ordre d'autorité --- correction importante

Le repository indique que `00_FOUNDATION` est la source de vérité
première et prime sur les couches suivantes.

L'ordre d'autorité à appliquer est donc :

1.  `00_FOUNDATION`
    -   `AGENT_PROTOCOL.md`
    -   `FOUNDATIONAL_LAWS.md`
    -   `NEVER.md`
    -   `CERTIFICATION_CHECKLIST.md`
2.  Gouvernance / architecture et autres couches du repository selon
    leur ordre officiel
3.  ADR validés dans `17_DECISIONS`
4.  Taxonomie et sources métier applicables
5.  Handover Claude Code
6.  Brand System ORAA Shopify
7.  Monde ORAA
8.  Houses System
9.  Spécifications particulières des maisons
10. Commerce & Transaction System
11. Quality / Mobile / Performance / Accessibility / Security
12. Implémentation

**Correction :** toute formulation antérieure laissant penser que le
Brand System pouvait primer directement sur la gouvernance ou
l'architecture doit être lue à la lumière de cette hiérarchie
officielle.

------------------------------------------------------------------------

# 3. Documents du nouveau package

## 01 --- Brand System

`ORAA_SHOPIFY_BRAND_SYSTEM.md`

Rôle : - identité mère ; - anneau ; - lumière ; - couleur ; -
typographie ; - photo/vidéo ; - motion ; - UI ; - cohérence jusqu'au
post-achat.

## 02 --- Monde ORAA

`ORAA_SHOPIFY_MONDE_ORAA_MASTER_EXPERIENCE_SPEC.md`

Rôle : - scène d'accueil ; - maisons ; - enseignes lumineuses ; -
montgolfière ; - avion ; - interactions ; - transitions ; - niveaux
Complet / Allégé / Statique premium.

## 03 --- Houses System

`ORAA_SHOPIFY_HOUSES_SYSTEM.md`

Rôle : - moteur commun des maisons ; - personnalité éditoriale ; -
vitrines ; - variation sans fragmentation.

## 04 --- Maison pilote Tech

`ORAA_SHOPIFY_EXPERIENCE_SYSTEM_MAISON_PILOTE_TECH.md`

Rôle : - première application détaillée ; - L'Atelier Tech ; -
démonstrations ; - campagnes ; - guides ; - merchandising ; -
architecture administrable.

## 05 --- Commerce & Transaction

`ORAA_SHOPIFY_COMMERCE_TRANSACTION_SYSTEM.md`

Rôle : - carte produit ; - fiche produit ; - prix ; - promotions ; -
avis ; - panier ; - checkout ; - confirmation ; - suivi ; - SAV ; -
post-achat.

## 06 --- Quality System

`ORAA_SHOPIFY_QUALITY_MOBILE_PERFORMANCE_ACCESSIBILITY_SECURITY.md`

Rôle : - mobile ; - performance ; - accessibilité ; - sécurité ; -
confidentialité ; - QA ; - déploiement.

------------------------------------------------------------------------

# 4. Compatibilité avec les lois fondamentales retrouvées

## Loi --- aucune décision ne doit affaiblir les fondations

**Compatible.**

Le nouveau package impose de signaler les contradictions et interdit à
Claude Code de modifier seul les décisions structurantes.

## Loi --- aucun texte traduisible dans un média

**Compatible, avec vigilance particulière sur le Monde ORAA.**

Les enseignes des maisons ne doivent pas être définitivement peintes
dans une image raster.

Implémentation recommandée : - texte HTML/CSS/SVG accessible et
externalisable ; - ou autre mécanisme CMS/traduction ; - jamais texte
utilisateur final uniquement gravé dans la bannière.

## Loi --- aucun contenu métier codé en dur

**Compatible.**

Les documents demandent explicitement : - sections Shopify ; - blocks
; - metafields ; - metaobjects ; - sources dynamiques.

Les prix, textes, campagnes, collections et données métier ne doivent
pas être inscrits directement dans le code du thème.

## Loi --- toute dépendance doit être justifiée et remplaçable

**Compatible.**

Le Quality System prévoit une revue de nécessité, taille, maintenance,
licence, sécurité et alternative native.

## Loi --- sécurité, accessibilité, performance et multilingue sont natifs

**Compatible.**

Le package les traite dès la conception et non en finition.

**Point à renforcer à l'implémentation :** le multilingue devra être
explicitement testé dans les enseignes, navigation, mini-univers,
contenus éditoriaux et composants commerce.

## Loi --- toute décision importante doit être documentée

**Compatible.**

Les choix structurants nouveaux qui affecteront réellement
l'architecture devront produire ou mettre à jour un ADR lorsque requis.

------------------------------------------------------------------------

# 5. Cohérences fortes constatées

Les six documents répètent de manière cohérente les mêmes principes :

-   le Monde ORAA doit rester beau sans animation ;
-   l'animation est intentionnelle, jamais gratuite ;
-   les maisons s'éveillent au visiteur ;
-   l'anneau est un passage/signature, pas un décor omniprésent ;
-   le mobile est conçu séparément ;
-   aucune fonction essentielle ne dépend du hover ;
-   les contenus récurrents sont administrables ;
-   le produit domine au moment commercial ;
-   le checkout est calme ;
-   Claude Code ne décide pas seul des prix, promotions ou politiques ;
-   aucun déploiement production autonome ;
-   performance, sécurité et accessibilité sont intégrées dès la
    conception.

Ces répétitions sont utiles comme garde-fous, mais la future
implémentation devra éviter de dupliquer les mêmes règles dans plusieurs
sources de vérité techniques.

------------------------------------------------------------------------

# 6. Points à vérifier AVANT implémentation

## A --- Statut exact des ADR

Des éléments antérieurs indiquaient que plusieurs ADR avaient été
validés en conversation alors que leurs fichiers pouvaient encore
afficher « Proposé ».

**Action Claude :** lire les fichiers réels dans `17_DECISIONS`,
rapporter leur statut exact et ne pas réécrire l'histoire.

## B --- Taxonomie Mode / Voyage & Aventure

Les traces disponibles montrent qu'une décision spécifique a existé
autour de l'exposition de **Mode** et **Voyage & Aventure**.

Le package actuel protège déjà Voyage & Aventure, mais **le statut exact
des deux familles doit être relu dans la version la plus récente de
`TAXONOMY.md` et des ADR** avant génération des maisons visibles.

**Aucune supposition.**

## C --- Packs & Offres / bundles

Une trace ADR indique une architecture de bundles fondée sur des
relations via metafields et l'absence de coffret sans lien structurel.

**Action :** vérifier ADR-0006 et aligner Packs & Offres avant
implémentation.

## D --- Navigation

Une trace ADR indique une navigation à deux niveaux et une règle
particulière concernant « Foi & Transmission ».

**Action :** vérifier ADR-0005 avant de construire header, navigation et
collections.

## E --- Phase B / données Shopify

La roadmap antérieure comprend un pilote de 12 produits avant migration
plus large.

**Action :** ne pas confondre le chantier design avec une autorisation
de modifier le catalogue. Respecter la phase réelle du handover.

## F --- Anomalies de prix

Les anomalies déjà signalées restent explicitement hors correction
autonome.

**Action :** aucune modification sans validation humaine.

------------------------------------------------------------------------

# 7. Points encore ouverts de direction artistique

Ils ne bloquent pas l'audit, mais bloquent le **gel visuel V1** :

-   typographie exacte ;
-   codes couleur maîtres exacts ;
-   proportions finales de certains composants ;
-   assets définitifs de l'anneau ;
-   assets définitifs du Monde ORAA ;
-   composition mobile finale ;
-   comportement précis de certaines transitions.

Claude Code peut préparer une architecture compatible, mais ne doit pas
inventer les choix définitifs.

------------------------------------------------------------------------

# 8. Architecture d'implémentation recommandée

Le code devrait distinguer :

### Données / contenu

Shopify CMS, products, collections, metafields/metaobjects, locales.

### Design tokens

Couleurs, typo, espacements, motion, focus, dimensions.

### Composants

Navigation, maison, enseigne, carte produit, média, CTA, prix,
variantes, panier.

### Templates

Monde, maison, collection, produit, éditorial.

### Motion

Couche progressive, désactivable et compatible reduced motion.

### Commerce

S'appuyer sur les mécanismes Shopify plutôt que réinventer les flux
critiques.

------------------------------------------------------------------------

# 9. Ordre d'exécution proposé à Claude Code

## Gate 0 --- Lecture uniquement

-   AGENT_PROTOCOL ;
-   Foundation ;
-   architecture/gouvernance ;
-   ADR ;
-   taxonomy ;
-   handover ;
-   six nouveaux documents.

**Sortie attendue :** rapport de contradictions et état réel. Aucun
changement Shopify.

## Gate 1 --- Réconciliation documentaire

-   statuts ADR ;
-   taxonomie ;
-   décisions roadmap ;
-   liens entre nouvelles specs et repository.

**Validation humaine requise.**

## Gate 2 --- Architecture front-end

Proposer : - structure thème ; - tokens ; - composants ; - données ; -
sections ; - metaobjects/metafields ; - stratégie animation ; -
stratégie mobile.

Pas encore de construction massive.

## Gate 3 --- Prototype Monde ORAA statique

Construire d'abord une version belle **sans dépendre des animations**.

Valider : - composition ; - navigation ; - enseignes ; - responsive ; -
identité.

## Gate 4 --- Interactions du Monde

Ajouter progressivement : - illumination enseignes ; - montgolfière ; -
avion ; - micro-vie ; - passage anneau.

Mesurer performance à chaque étape.

## Gate 5 --- Maison pilote Tech

Construire L'Atelier Tech à partir du système commun.

## Gate 6 --- Commerce pilote

Valider le chemin : Tech → produit → panier → checkout/preview
compatible.

## Gate 7 --- Déclinaison des autres maisons

Seulement après validation du pilote.

## Gate 8 --- QA complète

Mobile, performance, accessibilité, sécurité, contenu, commerce.

## Gate 9 --- Production

Uniquement après validation humaine explicite et plan de retour arrière.

------------------------------------------------------------------------

# 10. Règle anti-dérive pour Claude Code

Claude Code doit classer toute nouvelle idée dans une des catégories
suivantes :

**A. Implémentation directe d'une décision déjà validée**\
→ peut être proposée/exécutée dans le lot autorisé.

**B. Détail technique réversible**\
→ peut proposer le meilleur choix avec justification.

**C. Décision d'architecture importante**\
→ ADR/validation selon gouvernance.

**D. Décision créative, commerciale, juridique ou de marque**\
→ validation humaine obligatoire.

Cette classification empêche l'outil de transformer une liberté
technique en liberté stratégique.

------------------------------------------------------------------------

# 11. Définition du package prêt à transmettre

Le package est prêt pour Claude Code lorsque :

-   les six spécifications sont présentes ;
-   ce Master Index est présent ;
-   handover présent ;
-   Foundation présente ;
-   ADR présents ;
-   taxonomie présente ;
-   statuts et divergences sont visibles ;
-   aucun secret n'est inclus ;
-   les références visuelles nécessaires sont disponibles ;
-   les décisions ouvertes sont clairement marquées OPEN ;
-   l'ordre de lecture est explicite.

------------------------------------------------------------------------

# 12. Ce qui n'est PAS encore autorisé

Ce package ne signifie pas : - « refais la boutique » ; - « déploie »
; - « modifie les prix » ; - « expose toutes les collections » ; - «
choisis la typographie » ; - « installe ce qu'il faut » sans contrôle.

Il signifie :

> **Comprends d'abord l'ORAA existante, confronte les nouvelles
> spécifications aux lois du repository, signale les écarts, propose le
> plan, puis construis par gates validés.**

------------------------------------------------------------------------

# 13. Verdict de l'audit

**État : VERT avec points de réconciliation obligatoires avant code
lourd.**

Aucune contradiction fondamentale majeure n'a été identifiée entre les
nouvelles spécifications et les lois retrouvées.

Les principaux risques restants sont : 1. statut documentaire réel des
ADR ; 2. taxonomie Mode / Voyage & Aventure ; 3. règles exactes ADR-0005
/ ADR-0006 ; 4. séparation chantier design / migration catalogue ; 5.
choix graphiques encore ouverts.

Ces points doivent être résolus à partir du repository réel, pas de
mémoire ni d'inférence.

------------------------------------------------------------------------

# 14. Phrase de contrôle finale

**ORAA doit pouvoir devenir plus sophistiquée techniquement sans devenir
plus compliquée pour le client.**
