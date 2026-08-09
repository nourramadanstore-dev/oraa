# ORAA SHOPIFY --- COMMERCE & TRANSACTION SYSTEM

## De la découverte au paiement, puis au souvenir

**Statut :** Spécification structurante pré-implémentation\
**Projet :** ORAA Shopify exclusivement\
**Mission :** transformer l'émerveillement et la découverte en achat
clair, confiant et fluide, sans rupture de marque.

------------------------------------------------------------------------

# 1. Principe

Le commerce ORAA ne doit jamais ressembler à une couche Shopify
générique greffée sous le Monde ORAA.

Mais plus le client se rapproche du paiement, plus l'interface devient
calme.

**Monde → désir. Produit → compréhension. Panier → décision. Checkout →
confiance. Post-achat → souvenir.**

Aucun effet de marque ne doit diminuer la compréhension ou augmenter la
friction.

------------------------------------------------------------------------

# 2. Parcours commercial cible

Monde ORAA\
→ Maison\
→ contenu / démonstration / sélection\
→ carte produit\
→ fiche produit\
→ ajout au panier\
→ panier\
→ checkout Shopify\
→ paiement\
→ confirmation\
→ suivi\
→ réception\
→ SAV / avis / fidélisation pertinente

Le client doit aussi pouvoir court-circuiter l'immersion : recherche →
produit → achat.

------------------------------------------------------------------------

# 3. Cartes produit

Une carte produit ORAA doit permettre de comprendre rapidement : - ce
que c'est ; - son nom ; - son prix ; - sa principale variation si
pertinente ; - son état de disponibilité ; - une promotion réelle si
applicable ; - les avis réels si disponibles.

## Visuel

-   photographie propre ;
-   ratio cohérent ;
-   pas de surcharge de badges ;
-   deuxième image/aperçu au hover uniquement si performant et utile.

## CTA

Selon contexte : - Voir le produit ; - Choisir les options ; - Ajouter
au panier uniquement si aucune décision de variante n'est nécessaire.

Ne jamais masquer une étape nécessaire pour accélérer artificiellement
l'achat.

------------------------------------------------------------------------

# 4. Prix

Le prix est une information prioritaire.

Exigences : - immédiatement lisible ; - format monétaire cohérent ; -
prix comparé uniquement lorsqu'il est juridiquement/commercialement
justifié ; - aucun prix fictif ; - aucun calcul d'économie inventé ; -
règles TVA/livraison présentées selon configuration réelle.

Claude Code ne modifie aucune donnée de prix sans autorisation.

Les anomalies de prix signalées dans le handover restent hors correction
autonome.

------------------------------------------------------------------------

# 5. Promotions

Une promotion ORAA doit être vraie, compréhensible et sobre.

Interdits : - fausse urgence ; - faux compte à rebours ; - fausse rareté
; - prix barré artificiel ; - économie inventée ; - badges promotionnels
excessifs.

Le branding ne doit jamais servir à masquer la réalité commerciale.

------------------------------------------------------------------------

# 6. Avis et preuve sociale

N'afficher que des avis réels issus du système retenu.

Prévoir : - note ; - volume d'avis ; - distribution si utile ; -
commentaires ; - médias clients si réellement disponibles ; - réponses
ORAA lorsque pertinent.

Ne jamais générer de faux avis ou faux volumes.

------------------------------------------------------------------------

# 7. Fiche produit

## Zone initiale

Doit répondre rapidement : - Qu'est-ce que c'est ? - Combien ? - Quelles
variantes ? - Est-ce disponible ? - Pourquoi ce produit ? - Comment
l'ajouter ?

Contenu cible : - galerie ; - titre ; - prix ; - avis ; - bénéfice
principal ; - variantes ; - quantité si utile ; - CTA principal ; -
paiement express seulement si cohérent avec la stratégie ; -
informations livraison/retours réelles.

## Plus bas

-   démonstration ;
-   détails ;
-   dimensions/matières ;
-   utilisation ;
-   entretien ;
-   FAQ ;
-   contenu éditorial ;
-   produits associés pertinents.

Le produit reste le héros.

------------------------------------------------------------------------

# 8. Galerie produit

Prévoir : - image principale nette ; - zoom/détail ; - vues
complémentaires ; - vidéo si utile ; - produit en situation ; - échelle
compréhensible.

Mobile : - navigation tactile évidente ; - pas de média lourd chargé
inutilement ; - indicateur de galerie clair.

------------------------------------------------------------------------

# 9. Variantes

Les variantes doivent être impossibles à confondre.

Prévoir selon produit : - taille ; - couleur ; - modèle ; - quantité ; -
autre option réelle.

États : - disponible ; - sélectionné ; - indisponible.

Ne jamais pré-sélectionner trompeusement une option plus chère sans
clarté.

------------------------------------------------------------------------

# 10. Ajouter au panier

Le clic doit produire un feedback immédiat et calme.

Possibilités : - mini-panier ; - confirmation inline ; - panier latéral
si retenu.

Le client doit savoir : - que l'ajout a réussi ; - ce qui a été ajouté
; - quantité ; - total intermédiaire ; - comment continuer ; - comment
passer au panier/checkout.

Animation courte. Pas de célébration qui bloque l'action.

------------------------------------------------------------------------

# 11. Cross-sell / recommandations

Uniquement si utiles.

Bon : - accessoire réellement compatible ; - produit complémentaire ; -
recharge/consommable ; - ensemble cohérent.

Mauvais : - recommandations aléatoires ; - multiplication de carrousels
; - interruption du checkout ; - pression artificielle.

------------------------------------------------------------------------

# 12. Packs & Offres

Toujours distinguer : - produit individuel ; - pack ; - cadeau/box ; -
promotion.

Pour un pack : - contenu exact ; - valeur/prix réel ; - options ; -
économies seulement si mathématiquement et commercialement exactes.

------------------------------------------------------------------------

# 13. Panier

Le panier est une zone de décision.

Il doit afficher clairement : - produits ; - variantes ; - quantité ; -
prix ; - suppression ; - sous-total ; - réductions réelles ; -
informations utiles sur livraison/taxes selon configuration ; - CTA
checkout.

Le panier ne doit pas devenir un second Monde ORAA.

Identité présente, distraction minimale.

------------------------------------------------------------------------

# 14. Seuils et livraison

N'afficher un seuil de livraison gratuite que s'il existe réellement.

Si barre de progression : - calcul exact ; - devise correcte ; -
conditions accessibles ; - aucun seuil inventé.

Délais de livraison : uniquement données/configurations validées.

------------------------------------------------------------------------

# 15. Codes promotionnels

Ne pas pousser agressivement le client à chercher un code qu'il n'a pas.

L'emplacement doit rester clair sans suggérer qu'il « paie trop cher »
s'il n'a pas de code.

------------------------------------------------------------------------

# 16. Checkout

Le checkout est le niveau d'intensité de marque le plus faible.

Objectifs : 1. confiance ; 2. vitesse ; 3. clarté ; 4. cohérence.

Appliquer le branding ORAA dans les possibilités réelles du plan Shopify
et du checkout utilisé.

Ne pas promettre une personnalisation techniquement indisponible.

------------------------------------------------------------------------

# 17. Paiement

Afficher uniquement les moyens réellement disponibles.

Respecter les interfaces et exigences des prestataires.

Aucun effet créatif ne doit interférer avec : - saisie ; -
authentification ; - 3-D Secure ; - validation ; - messages d'erreur.

------------------------------------------------------------------------

# 18. Erreurs

Les erreurs doivent être : - visibles ; - précises ; - humaines ; -
actionnables.

Éviter : « Une erreur est survenue ».

Préférer lorsque techniquement possible : indiquer ce qui doit être
corrigé sans culpabiliser le client.

------------------------------------------------------------------------

# 19. Confirmation de commande

Après paiement réussi, l'émotion ORAA peut remonter légèrement.

La page doit d'abord confirmer : - commande réussie ; - numéro/référence
; - résumé ; - prochaine étape ; - moyen de suivre ; - contact.

Puis une signature ORAA mesurée peut créer le moment de souvenir.

L'anneau peut éventuellement être utilisé comme signature/achèvement,
sans ralentir l'affichage des informations essentielles.

------------------------------------------------------------------------

# 20. E-mail de confirmation

Doit être immédiatement identifiable comme ORAA.

Priorités : - confirmation ; - produits ; - montant ; - adresse ; -
suivi attendu ; - assistance.

Design : - logo/signature ; - hiérarchie ORAA ; - CTA clair ; -
responsive ; - compatible clients e-mail.

Pas de décor lourd.

------------------------------------------------------------------------

# 21. Suivi

Le client doit toujours comprendre : - état de commande ; - prochaine
étape ; - lien de suivi si disponible ; - quoi faire en cas de problème.

Le suivi fait partie de l'expérience de marque.

------------------------------------------------------------------------

# 22. SAV

Le ton ORAA en SAV : - humain ; - respectueux ; - concret ; -
responsable ; - non défensif.

Rendre faciles : - contact ; - référence commande ; - demande ; -
retour/échange selon politique réelle.

Ne jamais cacher une procédure derrière l'esthétique.

------------------------------------------------------------------------

# 23. Retours / remboursements

Les règles doivent refléter les politiques réelles et obligations
applicables.

Claude Code n'invente : - aucun délai ; - aucune exception ; - aucun
coût ; - aucune garantie.

Les informations doivent être accessibles avant achat lorsqu'elles
influencent la décision.

------------------------------------------------------------------------

# 24. Packaging et réception

Le branding peut continuer physiquement : - signature ORAA ; - cohérence
couleur/matière ; - message court ; - QR utile si retenu ; - protection
adaptée du produit.

Le packaging ne doit pas créer de promesses écologiques non démontrées.

------------------------------------------------------------------------

# 25. QR / prolongement

Un QR peut mener vers : - guide d'utilisation ; - vidéo ; - univers de
la maison ; - entretien ; - assistance ; - expérience éditoriale.

Il doit apporter une vraie valeur, pas seulement renvoyer à la homepage.

------------------------------------------------------------------------

# 26. Avis post-achat

Demander un avis au moment pertinent, sans pression.

Permettre un retour honnête.

Ne pas conditionner une récompense à un avis positif.

------------------------------------------------------------------------

# 27. Compte client

Doit rester simple : - commandes ; - adresses ; - suivi ; - informations
utiles ; - accès assistance.

Pas de gamification ajoutée sans objectif réel.

------------------------------------------------------------------------

# 28. Recherche

La recherche est un chemin commercial majeur.

Prévoir : - résultats pertinents ; - tolérance raisonnable ; -
produits + éventuellement contenus ; - zéro résultat utile ; - filtres
si nécessaire.

Un client qui connaît son besoin ne doit jamais être obligé de passer
par le village.

------------------------------------------------------------------------

# 29. Filtres et tri

N'utiliser que des filtres utiles à la catégorie.

Exemples selon produits : - prix ; - taille ; - type ; - disponibilité
; - caractéristique pertinente.

Éviter les filtres vides ou artificiels.

------------------------------------------------------------------------

# 30. Confiance

La confiance se construit par : - prix clairs ; - informations exactes
; - livraison claire ; - retours accessibles ; - coordonnées/support ; -
paiement reconnu ; - avis réels ; - photographie crédible ; - cohérence
de marque ; - absence de dark patterns.

Pas par une accumulation de badges « sécurisé ».

------------------------------------------------------------------------

# 31. Mobile commerce

Priorités : - CTA facilement atteignable ; - variantes simples ; -
galerie fluide ; - panier clair ; - formulaires adaptés ; - clavier
mobile approprié ; - chargement rapide ; - aucun overlay envahissant.

Tester l'achat complet sur vrai téléphone.

------------------------------------------------------------------------

# 32. Accessibilité commerce

Tester : - clavier ; - focus ; - annonces d'ajout panier ; - erreurs de
formulaire ; - labels ; - prix ; - variantes ; - quantités ; - contraste
; - zoom ; - lecteurs d'écran sur flux critique selon moyens.

------------------------------------------------------------------------

# 33. Performance commerce

Priorité absolue sur : - fiche produit ; - panier ; - checkout.

Éviter scripts marketing/applications qui dégradent fortement le
parcours sans valeur démontrée.

Auditer les apps Shopify avant ajout.

------------------------------------------------------------------------

# 34. Analytics et mesure

Prévoir une instrumentation respectueuse des choix de consentement et
obligations applicables.

Événements utiles : - vue collection ; - vue produit ; - recherche ; -
sélection variante ; - ajout panier ; - début checkout ; - achat ; -
interactions éditoriales majeures.

Ne pas collecter « parce qu'on peut ».

------------------------------------------------------------------------

# 35. Sécurité

Principes : - minimisation des scripts tiers ; - dépendances contrôlées
; - pas de secrets dans le thème ; - permissions minimales ; - apps
vérifiées ; - validation des entrées ; - respect des mécanismes Shopify
; - pas de contournement du checkout.

------------------------------------------------------------------------

# 36. Administration Shopify

Les équipes doivent pouvoir gérer sans code, selon droits : - contenus
produit ; - médias ; - collections ; - recommandations ; - blocs de
réassurance validés ; - contenus éditoriaux ; - campagnes ; - FAQ.

Les règles centrales de marque restent protégées dans le système.

------------------------------------------------------------------------

# 37. Tests critiques

Scénarios : 1. Monde → maison → produit → achat. 2. Recherche → produit
→ achat. 3. Mobile → variante → panier → checkout. 4. Produit
indisponible. 5. Code promo valide/invalide. 6. Erreur formulaire. 7.
Retour panier. 8. Reduced motion. 9. Navigation clavier. 10. Connexion
lente. 11. E-mail confirmation. 12. Suivi/SAV.

------------------------------------------------------------------------

# 38. Ce que Claude Code ne décide pas seul

-   prix ;
-   promotions ;
-   garanties ;
-   politiques ;
-   délais ;
-   frais ;
-   moyens de paiement ;
-   faux avis ;
-   faux stocks ;
-   fausse urgence ;
-   apps payantes/structurantes ;
-   tracking non validé ;
-   changement checkout ;
-   déploiement production.

En cas de donnée manquante : afficher un placeholder de développement
clairement identifié ou demander validation, jamais inventer une donnée
client.

------------------------------------------------------------------------

# 39. Definition of Done --- Commerce

Le système commercial est validé lorsque : - parcours complet fonctionne
; - identité ORAA reste cohérente ; - produit domine au bon moment ; -
prix/variantes sont clairs ; - panier est simple ; - checkout ne
comporte aucune distraction inutile ; - confirmation rassure ; -
post-achat prolonge la marque ; - mobile est testé ; - accessibilité
critique est testée ; - performances sont mesurées ; - aucune promesse
commerciale n'a été inventée ; - aucune rupture « ORAA → Shopify
générique » majeure n'est ressentie.

------------------------------------------------------------------------

# 40. Critère ultime

Le client doit pouvoir être émerveillé par ORAA puis acheter sans avoir
à « apprendre » comment fonctionne ORAA.

> **La magie attire. La clarté convertit. La qualité de l'après-achat
> transforme la transaction en souvenir.**
