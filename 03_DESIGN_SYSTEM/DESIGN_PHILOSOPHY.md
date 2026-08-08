# DESIGN_PHILOSOPHY.md

**Portée** : Toute décision de design sur ORAA — interface, interaction, contenu visuel.
**Relation avec les lois fondamentales** : Ce document complète la Loi 6 (accessibilité native) et la Loi 3 (aucun texte traduisible dans un média). Il ne les répète pas, il les traduit en principes de décision quotidiens.

---

## Ce que ce document n'est pas

Il ne contient ni tokens, ni composants, ni spécifications visuelles précises — cela vit dans le reste de `03_DESIGN_SYSTEM`. Ici, ce sont les principes qui guident *pourquoi* on choisit une direction plutôt qu'une autre quand le système ne tranche pas déjà.

## Principes

### La clarté prime sur la décoration
Un élément visuel qui n'aide pas la compréhension ou l'action de l'utilisateur est un candidat à la suppression, pas à la justification.

### La cohérence prime sur la nouveauté
Une solution originale qui casse un pattern existant doit apporter une valeur supérieure au coût de l'incohérence introduite. Le doute profite à la cohérence.

### L'accessibilité est un point de départ, pas une correction
Une interface se conçoit accessible dès le premier jet (contraste, navigation clavier, structure sémantique), pas "accessibilisée" après coup.

### Le contenu précède la mise en forme
On conçoit avec du contenu réel ou réaliste, jamais avec du texte de remplissage définitif. Un design qui ne survit pas à un texte deux fois plus long (traduction, contenu réel) est un design incomplet.

### Le système avant le sur-mesure
Toute nouvelle interface commence par une composition d'éléments existants. Le sur-mesure est une exception justifiée, pas un point de départ.

### Le mouvement a une fonction
Une animation doit clarifier une transition d'état ou guider l'attention. Le mouvement décoratif sans fonction est un coût de performance et de charge cognitive non justifié.

### La sobriété est une valeur, pas une contrainte budgétaire
Retirer un élément est aussi légitime que d'en ajouter un. La densité d'une interface se justifie par l'usage, pas par l'envie de remplir l'espace.

### La dette de design se documente
Un compromis visuel pris pour tenir un délai doit être noté comme tel (voir `16_REGISTRIES` pour le suivi), pas silencieusement absorbé comme un standard.

---

## Quand ce document ne suffit pas

En cas de conflit entre un principe ici et une contrainte produit ou technique, le désaccord doit être signalé et documenté — jamais résolu silencieusement en faveur de l'un ou de l'autre. Voir `00_FOUNDATION/AGENT_PROTOCOL.md` sur la posture attendue.
