# HANDOVER — Projet ORAA, transfert vers Claude Code

**Statut du package : DÉFINITIF, prêt pour transfert.**
**Date** : 2026-08-07
**Origine** : Conversation Claude (app mobile/web), aucune modification effectuée sur Shopify durant tout l'échange — audit et conception uniquement.
**Objectif de ce document** : permettre à Claude Code de reprendre le projet sans perte de contexte, sans re-découvrir ce qui a déjà été établi, et sans re-décider ce qui a déjà été tranché.

---

## 1. État exact du projet

### 1.1 Ce qui existe réellement

- **Une boutique Shopify réelle et active** : `Oraa`, domaine `oraa-6632.myshopify.com`, plan Basic, devise EUR, fuseau CEST, France. **0 commande à date — la boutique n'est pas encore lancée commercialement.**
- **Un dépôt de gouvernance** construit dans un environnement d'exécution temporaire (sandbox) au fil de la conversation, **jamais poussé dans un dépôt Git réel**. Il a été transmis à l'utilisateur sous forme de fichiers `.zip` à plusieurs reprises, au fur et à mesure des ajouts. **Rien ne garantit que ces fichiers ont été importés dans le dépôt Git réel avant que Claude Code ne démarre** — c'est le premier point à vérifier (voir §6).
- **Aucun code applicatif, aucun thème, aucune infrastructure** n'existe à ce stade. Tout le travail réalisé jusqu'ici est de la gouvernance, de l'audit et de la conception d'architecture commerciale — rien n'a été implémenté techniquement.

### 1.2 Ce qui N'A PAS été fait

- Aucune modification sur Shopify (aucune écriture — produits, collections, prix, tout est en l'état constaté à l'audit).
- Aucune Phase B commencée (application de la taxonomie aux produits pilotes) — explicitement suspendue par l'utilisateur avant ce handover.
- Aucun accès au thème Shopify (Liquid, sections, templates) n'a été obtenu ni audité — le connecteur utilisé jusqu'ici couvre uniquement l'API Admin (produits, collections, commandes), pas le thème.

---

## 2. Audit Shopify réalisé et validé

**L'audit complet est désormais sauvegardé dans `05_COMMERCE/AUDIT_SHOPIFY_EXISTANT.md`** — ce fichier fait foi, résumé ci-dessous.

### 2.1 Catalogue (21 produits)

**8 produits actifs**, cohérents avec la mission ORAA (univers spirituel/Islam, maison) :
1. Enceinte Coranique Lune 3D — 44,90 €
2. Horloge Azan Bluetooth — 28,68–47,90 € ⚠️ **anomalie de prix entre variantes non résolue**
3. Brûleur d'Encens Coranique SQ-600 — 34,90 €
4. Lampe de Nuit Coranique Portable — 24,90 € ⚠️ **stock critique : 2 unités**
5. Horloge Adhan Lumineuse Blanche — 44,90 €
6. Horloge Coranique Adhan (multicolore) — 39,90 € ⚠️ **stock faible : 8 unités**
7. Bague Connectée Zikr et Qibla — 12,86–79,90 € (24 variantes) ⚠️ **anomalie de prix majeure, probable import fournisseur corrompu**
8. Haut-parleur Coranique Magnétique — 10,12–27,90 € (16 variantes) ⚠️ **même type d'anomalie**

**4 produits en brouillon**, mieux structurés que les actifs (tags et productType déjà présents), mais sans image, stock à 0 :
9. Horloge Adhan Al-Fatiha — 69,90 €
10. Veilleuse 3D Kaaba — 19,90 €
11. Enceinte Coranique Enfant — 34,90 € (segment éducatif enfant, prioritaire)
12. Pack Maison — 89,90 € (bundle, actuellement sans lien structurel vers ses composants)

**9 produits archivés**, hors mission (dropshipping générique : robot aspirateur, télé, parasols, ventilateur, etc.) — **conservés archivés sur décision explicite de l'utilisateur, suppression définitive non validée**. Ne pas y toucher sans nouvelle validation.

### 2.2 Collections (18 au total)

10 vides sur 18. Deux taxonomies superposées et jamais fusionnées (une ancienne générique : Maison/Hygiène/High-Tech, une plus récente alignée mission : Foi & Transmission/Enfants & Bébés/Cadeaux & Box). Anomalies notables : handle `maison` sur la collection titrée "High-Tech" ; handles `hygiene-1` et `maison-1` (reliquats de duplication) ; trois collections différentes pour le concept de "pack/promo".

### 2.3 Vocabulaire

Incohérence orthographique dans les titres/handles entre variantes françaises et translittérées (coran/quran, adhan/azan), fragmentant la recherche interne.

---

## 3. Les 6 ADR et leur statut réel

| ADR | Sujet | Statut |
|---|---|---|
| ADR-0001 | Gel de la structure du dépôt en 20 couches | Accepté |
| ADR-0002 | Modèle de taxonomie à 3 couches (Category/Product Type/Tags) | Accepté (2026-08-07) |
| ADR-0003 | Convention de nommage des SKU | Accepté (2026-08-07) |
| ADR-0004 | Convention de handles produits | Accepté (2026-08-07) |
| ADR-0005 | Navigation à deux niveaux | Accepté (2026-08-07) |
| ADR-0006 | Bundles et relations produits | Accepté (2026-08-07) |

Les 6 ADR sont désormais cohérents entre leur statut écrit et la validation réelle de l'utilisateur. Aucune action de correction requise sur ce point.

---

## 4. Taxonomie cible (architecture commerciale)

Détail complet dans `05_COMMERCE/TAXONOMY.md`. Résumé :

- **Modèle à 3 couches** : Category (standard Shopify) / Product Type (interne) / Tags (par espace de noms : `occasion:`, `public:`, `fonction:`, `connectivite:`, `couleur:`, `materiau:`).
- **Navigation à 2 niveaux** : primaire stable par famille produit (Enceintes & Horloges, Veilleuses, Encens, Bijoux & Dhikr, Décoration, Enfants, Coffrets) ; secondaire thématique/saisonnière (Ramadan, Aïd, cadeaux) pilotée par tags. Une seule collection manuelle assumée : **"Foi & Transmission"**.
- **Convention de handles** : courts, sans répétition de mot-clé, sous 60 caractères. Fenêtre de correction gratuite tant que la boutique n'est pas indexée publiquement (voir ADR-0004).
- **Convention de SKU** : `ORAA-[CODE_FAMILLE]-[CODE_PRODUIT]-[CODE_VARIANTE]`.
- **Bundles** : via fonctionnalité native Shopify ou app dédiée, avec relation structurée par metafield vers les composants — jamais un coffret sans lien structurel.

"Mode" et "Voyage & Aventure" sont tranchées comme catégories roadmap (vision long terme), non exposées avant d'avoir une offre cohérente — `TAXONOMY.md` §11 reflète déjà cette décision, aucune action requise.

---

## 5. Phase B — détail (suspendue, ne pas lancer avant vérification du contexte)

**Portée** : les 12 produits pilotes (8 actifs + 4 brouillons listés en §2.1).

**Actions prévues par produit** :
- Renseigner Category (taxonomie standard Shopify)
- Renseigner Product Type (vocabulaire interne, voir `TAXONOMY.md` §2)
- Ajouter les tags pertinents (espaces de noms définis en §4)
- Corriger le handle selon la nouvelle convention
- Renommer le SKU selon la nouvelle convention

**Explicitement exclu de la Phase B, décision arbitrée** :

Ces quatre points ne sont **pas des ambiguïtés de documentation** — ce sont des décisions qui touchent à l'argent réel et à l'image de la boutique, sans que les données nécessaires pour trancher correctement soient disponibles depuis cette conversation. Deviner serait plus risqué que reporter. Décision : Claude Code les traite selon le protocole ci-dessous, pas selon une valeur inventée ici.

- **Les 3 anomalies de prix** (Horloge Azan Bluetooth, Bague Connectée Zikr et Qibla, Haut-parleur Coranique Magnétique) — la cause et le prix correct ne sont pas connus (absence de données de coût/marge fournisseur). **Protocole** : Claude Code doit consulter l'historique de coût fournisseur si l'accès Shopify le permet ; à défaut, soumettre les 3 anomalies à l'utilisateur avec les options observées (prix bas / prix haut / moyenne) avant toute correction. Ne jamais choisir seul une valeur.
- **Le stock critique** (2 et 8 unités) — **Protocole** : signaler dans le rapport de fin de Phase B, ne pas déclencher de réassort ni de dépublication automatique.
- **Les images manquantes** (4 produits brouillon, toutes les collections) — **Protocole** : signaler le besoin de photographie produit réelle dans le rapport ; ne jamais générer d'image IA comme substitut, car un produit physique vendu avec un visuel non représentatif est trompeur pour le client.
- **Les 9 produits archivés hors mission** — **Protocole** : rester archivés. Suppression non validée. Ne redemander l'arbitrage à l'utilisateur qu'une seule fois, en fin de Phase B, pas avant.

---

## 6. Fichiers attendus dans le dépôt réel

Structure complète des 20 couches, avec ces fichiers déjà rédigés à ce stade (à vérifier réellement présents avant de continuer — voir §8) :

```
README.md (racine)
CONTRIBUTING.md (racine)
00_FOUNDATION/
  README.md
  FOUNDATIONAL_LAWS.md
  NEVER.md
  CERTIFICATION_CHECKLIST.md
  AGENT_PROTOCOL.md
01_GOVERNANCE/README.md
02_ARCHITECTURE/README.md  (référence l'architecture commerciale comme première brique)
03_DESIGN_SYSTEM/
  README.md
  DESIGN_PHILOSOPHY.md
04_PRODUCT_SYSTEM/
  README.md
  PRODUCT_PRINCIPLES.md
05_COMMERCE/
  README.md
  AUDIT_SHOPIFY_EXISTANT.md
  TAXONOMY.md
  MIGRATION_PLAN.md
06_CONTENT/README.md
07_EXPERIENCE/README.md
08_ENGINEERING/
  README.md
  ENGINEERING_PRINCIPLES.md
  PERFORMANCE_GUIDE.md
09_OPERATIONS/
  README.md
  RESILIENCE.md
  OBSERVABILITY.md
10_SECURITY/
  README.md
  SECURITY_PLAYBOOK.md
11_DATA/README.md
12_AI/
  README.md
  AI_GOVERNANCE.md
13_QUALITY/
  README.md
  QUALITY_GATE.md
14_GROWTH/README.md
15_ASSETS/README.md
16_REGISTRIES/README.md
17_DECISIONS/
  README.md
  ADR_TEMPLATE.md
  ADR-0001-structure-du-depot.md
  ADR-0002-modele-taxonomie-trois-couches.md
  ADR-0003-convention-sku.md
  ADR-0004-convention-handles.md
  ADR-0005-navigation-deux-niveaux.md
  ADR-0006-bundles-relations-produits.md
18_RELEASES/README.md
19_ARCHIVE/README.md
20_AI_PACKAGE/README.md
```

---

## 7. Accès et outils Shopify nécessaires

- **Pour la Phase B (écriture réelle sur la boutique)** : Claude Code a besoin d'un accès Shopify Admin en écriture. Deux options évoquées avec l'utilisateur : le Shopify Admin MCP officiel (fonctionne, mais **aucune confirmation ni rollback intégré** — un risque réel sur une boutique en préparation de lancement), ou **ShopMCP** (app tierce avec permissions granulaires, journal d'audit, sauvegarde automatique) — recommandé à l'utilisateur pour cette raison.
- **Pour la validation de code/schema Shopify** : Shopify Dev MCP (`@shopify/dev-mcp`), local, lecture seule, sans risque.
- **Accès au thème** : non couvert par les outils utilisés jusqu'ici. Si le prochain travail touche au thème (Liquid, sections), un accès supplémentaire sera nécessaire — ne pas supposer qu'il existe déjà.

---

## 8. Risques et points de vigilance

1. **Le dépôt Git réel n'a peut-être pas encore reçu tous les fichiers.** Avant toute action, vérifier leur présence effective plutôt que de supposer qu'ils y sont — ne pas réécrire par-dessus sans vérifier, ne pas non plus assumer l'absence.
2. **Boutique réelle, pré-lancement (0 commande)** — c'est une fenêtre de risque faible mais pas nulle : toute erreur reste visible en interne et corrompt les données avant même le premier client.
3. **Pas de rollback natif sur les mutations Shopify Admin API** — chaque écriture doit être pensée comme irréversible en pratique, conformément à `NEVER.md` sur les changements destructifs.
4. **Les 3 anomalies de prix restent non résolues** — ne jamais les corriger sans clarification de l'utilisateur sur l'origine et le prix correct.
5. **Mémoire non activée sur le compte utilisateur** — ce document est le seul pont de contexte entre les conversations ; ne pas supposer qu'un futur échange se souviendra de quoi que ce soit qui n'y figure pas.
6. **Statuts d'ADR à corriger avant toute autre action** (§3) — sinon le dépôt contient une contradiction entre ce qui a été décidé et ce qui est écrit.

---

## 9. Ordre d'exécution précis pour Claude Code

1. Lire `00_FOUNDATION/AGENT_PROTOCOL.md`, `FOUNDATIONAL_LAWS.md`, `NEVER.md`, `CERTIFICATION_CHECKLIST.md`.
2. Vérifier la présence effective de tous les fichiers listés en §6 dans le dépôt réel. Signaler tout écart avant de continuer.
3. Confirmer l'accès Shopify disponible (lequel des deux MCP, quelles permissions) avant toute écriture.
4. Exécuter la Phase B sur les 12 produits pilotes, **à l'exclusion explicite** des 3 anomalies de prix, du stock, et des images manquantes (signaler ces points, ne pas agir).
5. Rapport de fin de phase au format demandé par l'utilisateur : réalisé / restant / difficultés / recommandations.

---

## FIRST PROMPT FOR CLAUDE CODE

```
Tu reprends le projet ORAA. Ce dépôt suit une gouvernance stricte définie dans
00_FOUNDATION/ — lis dans l'ordre AGENT_PROTOCOL.md, FOUNDATIONAL_LAWS.md,
NEVER.md, CERTIFICATION_CHECKLIST.md avant toute action.

Contexte : ORAA est une marque e-commerce (boutique Shopify "Oraa",
oraa-6632.myshopify.com, plan Basic, 0 commande à ce jour — pré-lancement)
positionnée sur l'univers spirituel/Islam et la maison (enceintes coraniques,
horloges adhan, veilleuses, encens, bijoux connectés de dhikr, produits
éducatifs enfants).

Un audit complet du catalogue a déjà été réalisé et sauvegardé
(05_COMMERCE/AUDIT_SHOPIFY_EXISTANT.md : 21 produits, 18 collections) et une
architecture commerciale cible a été conçue et validée avec l'utilisateur
(05_COMMERCE/TAXONOMY.md, MIGRATION_PLAN.md, ADR-0002 à ADR-0006, tous
Acceptés). Ne refais pas cet audit, ne re-conçois pas cette architecture —
reprends-les tels quels.

Avant toute autre chose, exécute ces 2 actions de mise en cohérence :
1. Vérifie que tous les fichiers listés en §6 du présent handover existent
   réellement dans ce dépôt. Signale tout écart avant de continuer.
2. Confirme quel accès Shopify tu as effectivement à disposition (Admin MCP
   officiel ou ShopMCP) et ses permissions, avant toute écriture sur la
   boutique.

Une fois ces 2 points faits, tu peux lancer la Phase B du plan de migration
(05_COMMERCE/MIGRATION_PLAN.md) : appliquer Category, Product Type, tags,
handle et SKU aux 12 produits pilotes (8 actifs + 4 brouillons).

Exclusions strictes de la Phase B — protocole à suivre, ne rien deviner :
- 3 anomalies de prix (Horloge Azan Bluetooth, Bague Connectée Zikr et
  Qibla, Haut-parleur Coranique Magnétique) : cherche les données de coût
  fournisseur si l'accès Shopify le permet ; sinon, soumets les options
  observées à l'utilisateur avant toute correction ;
- stock critique de 2 produits (2 et 8 unités) : signale dans le rapport,
  n'agis pas ;
- images manquantes (4 produits brouillon, toutes les collections) :
  signale le besoin de vraie photographie produit, ne génère jamais une
  image IA en remplacement ;
- 9 produits archivés hors mission : restent archivés, suppression non
  validée — ne redemande l'arbitrage qu'une fois, en fin de Phase B.

Aucune modification destructive sans validation explicite (voir NEVER.md).
À la fin de la Phase B, fournis un rapport : ce qui a été réalisé, ce qui
reste à faire, les difficultés rencontrées, tes recommandations — c'est le
format que l'utilisateur attend à chaque fin de phase.
```
