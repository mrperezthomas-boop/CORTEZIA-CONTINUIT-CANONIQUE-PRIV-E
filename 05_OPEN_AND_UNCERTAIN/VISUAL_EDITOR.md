# CORTEZIA — ÉDITEUR VISUEL ADMIN

Statut : `SELECTED / À IMPLÉMENTER ET VALIDER DANS LE VRAI WORKTREE`  
Date : 2026-09-03

## Besoin utilisateur

Pouvoir, depuis le vrai compte admin Cortezia :
- déplacer/recomposer visuellement les blocs ;
- régler leurs tailles, ordre, espacements et présentation ;
- prévisualiser desktop/mobile ;
- conserver un site réellement fonctionnel ;
- ne pas devoir appeler Codex pour chaque ajustement de placement ;
- ne jamais rendre éditables les règles sensibles du backend.

## Verdict

### 1 — Puck — RECOMMANDÉ

Puck est le meilleur ajustement au besoin actuel.

Arguments vérifiés auprès de la documentation officielle :
- éditeur visuel modulaire open-source pour React ;
- fonctionne avec Next.js ;
- cœur MIT ;
- embarquable dans notre propre application ;
- composants React Cortezia enregistrables dans l'éditeur ;
- données de page sous forme JSON, stockables chez nous ;
- pas de vendor lock-in ;
- permissions `delete`, `drag`, `duplicate`, `edit`, `insert`, y compris dynamiques par instance ;
- viewports configurables.

Architecture cible :

`/admin/<route-à-choisir>` → vrai contrôle admin serveur → Puck editor → JSON draft → validation allowlist/schéma → publication → runtime Puck `<Render>` / renderer contrôlé avec vrais composants Cortezia.

### Ce que l'utilisateur pourrait modifier
- ordre des sections ;
- colonnes/layout ;
- largeur/hauteur autorisées ;
- espacements ;
- alignement ;
- variantes artistiques autorisées ;
- assets approuvés ;
- contenu textuel sûr si exposé ;
- visibilité de sections non critiques si autorisée.

### Ce qui doit rester verrouillé
- logique d'auth ;
- logique d'âge ;
- entitlement ;
- paiement ;
- délivrance média ;
- permissions admin ;
- destinations/actions sensibles ;
- code arbitraire ;
- JavaScript/HTML/CSS brut non contrôlé.

### Blocs Cortezia à enregistrer
- `GlobalHeader`
- `PageHero`
- `SectionHeading`
- `FeaturedMedia`
- `VideoRail`
- `VideoGrid`
- `SeriesRail`
- `AccountSummary`
- `Footer`
- `DecorativeShell`
- `Spacer/Columns` contrôlés

Blocs sensibles :
- `AgeGate`
- `AuthPanel`
- `Paywall`
- `Player`
- `PurchaseCTA`
- `AdminAction`

Ces blocs sensibles peuvent être repositionnés/skinés dans des limites prédéfinies mais leurs actions ne doivent jamais être remplacées par une URL ou un script libre.

## Persistance recommandée

Modèle conceptuel (noms DB à choisir seulement après audit du schéma existant) :
- page key / route key ;
- `draft_json`;
- `published_json`;
- revision;
- updated_by;
- updated_at.

Ajouter :
- historique des révisions ;
- bouton Restaurer ;
- Preview ;
- Publier ;
- retour à la composition canonique.

## Validation
Avant publication :
1. parse JSON ;
2. allowlist des composants ;
3. validation des props ;
4. interdiction de code arbitraire ;
5. vérification des composants obligatoires ;
6. contrôle du rôle admin côté serveur ;
7. sauvegarde revision ;
8. invalidation/revalidation de cache si nécessaire.

## Responsive
Configurer au minimum des viewports correspondant aux cibles du projet, par exemple :
- desktop 1440 ;
- desktop 1920 ;
- mobile 390 ;
- mobile 430.

Le layout sauvegardé doit privilégier contraintes responsive/grilles plutôt qu'une position absolue fragile pour chaque pixel.

## Pourquoi pas Plasmic comme premier choix
Le plan Free est réel, mais la page de tarification officielle place actuellement **Whitelabeling & embedding** dans l'offre Enterprise. Ce n'est donc pas le meilleur pari pour un éditeur gratuit directement embarqué dans l'admin.

## Pourquoi pas Builder.io comme premier choix
Builder possède un plan Free et un Visual Editor puissant, mais reste un service SaaS avec plans/crédits et workflows externes. Il ne correspond pas aussi bien au besoin « éditeur dans mon admin + données chez moi + zéro lock-in ».

## Pourquoi GrapesJS arrive derrière Puck
GrapesJS est puissant et historiquement open-source, mais son approche est plus orientée éditeur web/HTML-CSS. Son Studio SDK et le renderer React sont intéressants, mais l'intégration des vrais composants React métier de Cortezia est moins directe que le modèle Puck pour notre cas.

## Sources officielles — vérifiées le 2026-09-03

- Puck docs — https://puckeditor.com/docs
- Puck permissions — https://puckeditor.com/docs/api-reference/permissions
- Puck component config — https://puckeditor.com/docs/api-reference/configuration/component-config
- Puck component API / viewports / onPublish — https://puckeditor.com/docs/api-reference/components/puck
- Puck website — https://puckeditor.com/
- Plasmic pricing — https://www.plasmic.app/pricing
- Builder pricing — https://www.builder.io/pricing
- Builder Visual Editor — https://www.builder.io/c/docs/visual-editor
- GrapesJS React renderer — https://app.grapesjs.com/docs-sdk/plugins/custom-renderer/react

## Décision actuelle

`ADMIN_VISUAL_EDITOR_REQUIRED = ACTIVE_USER_REQUIREMENT`

`PUCK = SELECTED_NOT_IMPLEMENTED`

La sélection Puck est validée par le propriétaire. Ne pas annoncer Puck comme installé tant qu'il n'a pas été intégré et testé dans le vrai worktree.
