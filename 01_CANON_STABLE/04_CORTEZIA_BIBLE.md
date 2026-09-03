# CORTEZIA — BIBLE CANONIQUE

Statut : `ACTIVE / CANON_UI_PRODUCT_WORKFLOW`  
Date de consolidation : `2026-09-03`  
But : donner à un humain, ChatGPT, Claude, Codex ou tout autre agent une compréhension commune de Cortezia sans relire l'historique complet.

> Cette Bible fige les décisions produit, UI, navigation, droits visibles, direction artistique, admin et workflow d'agents. Elle ne remplace pas l'état réel du code pour les faits techniques volatils et ne contient aucun secret. Les détails internes serveur restent dans les sources techniques dédiées.

---

## 0 — AUTORITÉ ET RÈGLE DE CONFLIT

Ordre de vérité :

1. consigne utilisateur actuelle explicite ;
2. état local/runtime réellement vérifié pour ce qui existe techniquement ;
3. présente Bible pour le canon produit/UI/workflow ;
4. documents de continuité actifs ;
5. discussions historiques ;
6. anciennes maquettes et suggestions IA.

Règles :
- une décision utilisateur plus récente remplace une décision plus ancienne incompatible ;
- une proposition IA ne devient jamais canon sans validation utilisateur ;
- une route ou fonction observée dans un ancien runtime ne devient pas canonique par sa seule présence ;
- une maquette transmet d'abord la composition et la DA, jamais automatiquement les textes, prix, données ou droits visibles ;
- `INFERRED / PROPOSAL / OPEN / HISTORICAL` ne sont pas des décisions actives.

---

# 1 — IDENTITÉ DU PRODUIT

Cortezia est un **service premium réel de diffusion de contenus adultes**, destiné à être exploitable au quotidien.

Invariants :
- ce n'est pas une simple vitrine ;
- le produit final n'est pas centré sur Ariana, une créatrice ou un personnage central ;
- les médias, données, droits et états sont dynamiques ;
- desktop et mobile sont deux compositions de production réelles ;
- la sécurité et les droits ne reposent jamais uniquement sur le frontend.

---

# 2 — PARCOURS D'ENTRÉE ET VÉRIFICATION D'ÂGE

## 2.1 Basic Age Gate — première arrivée

Le premier écran est une **déclaration/avertissement +18**.

Fonction :
- informer ;
- recueillir la déclaration d'âge ;
- permettre de quitter ;
- rester dans un environnement SAFE avant preuve officielle.

Décision récente prioritaire :

`PREMIÈRE ARRIVÉE → DÉCLARATION +18 → ACCUEIL SAFE`

Le Basic Gate **ne constitue jamais une preuve officielle d'âge**.

## 2.2 Vérification officielle d'âge

La vérification officielle est un mécanisme **distinct**.

Elle **n'est pas automatiquement l'écran suivant le Basic Gate**.

Elle doit se déclencher aux endroits où une preuve officielle est réellement requise par le produit, le droit applicable et le runtime. Les points d'activation exacts doivent être reliés au mécanisme réel du projet ; ne jamais les inventer à partir d'une ancienne maquette.

Avant preuve valide :
- aucun contenu pornographique ne doit être rendu, préchargé ou livré ;
- une interface SAFE peut être parcourue ;
- le backend reste fail-closed pour les médias sensibles.

Le provider final de preuve d'âge reste un sujet à valider contre les obligations officielles actuelles ; les anciennes mentions Yoti ne sont pas une obligation canonique définitive.

---

# 3 — ÉTATS UTILISATEURS

Les concepts suivants doivent rester distincts.

| État | Sens | Accès média |
|---|---|---|
| `VISITOR_SAFE` | visiteur ayant éventuellement accepté le Basic Gate mais sans preuve d'âge officielle | aucun accès pornographique |
| `REGISTERED_UNVERIFIED` | compte créé, preuve d'âge non valide/non établie | aucun accès pornographique |
| `AGE_VERIFIED_NO_ENTITLEMENT` | âge vérifié, mais sans abonnement ni achat PPV pour le contenu | catalogue selon règles SAFE/locked, pas de lecture réservée |
| `ACTIVE_SUBSCRIBER` | âge valide + abonnement actif | accès aux vidéos publiées couvertes par l'abonnement |
| `PPV_ENTITLED` | âge valide + achat individuel valide | accès à la vidéo achetée |
| `ADMIN_REAL` | administrateur réel, authentifié et autorisé côté serveur | capacités admin selon permissions |
| `DEV_SIMULATOR` | simulation locale DEV | jamais assimilée à l'admin réel ni à une preuve de sécurité |

Invariants :
- inscription ≠ vérification d'âge ;
- inscription ≠ abonnement ;
- vérification d'âge ≠ entitlement ;
- abonnement et PPV sont deux voies indépendantes d'accès ;
- un changement d'UI ne crée jamais un droit.

---

# 4 — MODÈLE COMMERCIAL ACTIF

## Abonnement
- **un seul abonnement : 14,99 €** ;
- aucun deuxième plan ;
- aucune offre Standard/Premium/VIP ;
- un utilisateur déjà abonné ne doit plus voir de CTA lui demandant de s'abonner ;
- l'expérience abonné doit valoriser son statut avec du contenu/UX réservé, pas un upsell inutile.

## PPV
- **3,99 € par vidéo publiée** ;
- toute vidéo publiée est réservée ;
- chaque vidéo publiée doit pouvoir être couverte par abonnement actif ou par achat individuel PPV.

## Favoris
- réservés aux **abonnés actifs**.

Toute ancienne offre à 13,99 €, 16,99 €, 19,99 € ou architecture multi-plans est `SUPERSEDED`.

---

# 5 — NAVIGATION PUBLIQUE CANONIQUE

Header public :
1. `Accueil`
2. `Nouveautés`
3. `Toutes les vidéos`
4. `Séries`

Règles :
- ne pas réintroduire une ancienne route parce qu'elle apparaît dans une référence ;
- `/videos` ne possède pas de filtre public `Catégorie` ;
- recherche et compte/connexion restent des actions globales appropriées au contexte ;
- les vrais labels, liens et destinations sont du runtime, jamais des pixels baked servant de vérité.

---

# 6 — CARTOGRAPHIE DE PAGES / ROUTES

La table ci-dessous sépare **canon produit** et **routes observées/historiques**. Les chemins dynamiques exacts doivent être confirmés dans le runtime lorsqu'une implémentation les touche.

## 6.1 Canon produit — public / compte / contenu

| Surface | Route connue/canonique | Fonction |
|---|---|---|
| Accueil | `/` | page principale, adaptée à l'état utilisateur |
| Nouveautés | `/nouveautes` | nouveautés réelles |
| Toutes les vidéos | `/videos` | catalogue vidéo, sans filtre public Catégorie |
| Recherche | `/recherche` | recherche et résultats |
| Séries | `/series` | index séries |
| Série détail | `/series/[slug]` | fiche série + épisodes |
| Watch | `/watch/[slug]` | lecture protégée d'une vidéo |
| Connexion | `/connexion` | authentification existante |
| Inscription | `/inscription` | création de compte existante |
| Abonnement | `/abonnement` | offre unique 14,99 € / état abonnement |
| Favoris | `/favoris` | favoris abonnés actifs |
| Historique | `/historique` | historique utilisateur |
| Notifications | `/notifications` | notifications utilisateur |
| Compte | `/compte` | dashboard compte consolidé |
| Achats | `/compte/achats` | achats/PPV de l'utilisateur |
| Support | `/support` ou route runtime équivalente | aide/support |
| Légal/CGV | `/legal/cgv` et routes légales runtime | obligations/légal |

## 6.2 Admin

| Surface | Statut |
|---|---|
| `/admin` | back-office réel attendu ; doit agir sur vraies données avec contrôles serveur |
| `/admin/dev` | simulateur DEV seulement, ne prouve jamais le vrai admin |
| routes dynamiques admin | runtime à auditer au besoin ; ne jamais inventer ID/slug |

Routes dynamiques historiquement bloquées faute de fixture lors du dernier audit visuel :
- `/admin/commandes/[id]`
- `/admin/conformite/performers/[id]`
- `/admin/recompenses/[slug]`
- `/admin/series/[slug]`
- `/admin/support/[id]`
- `/admin/videos/[slug]`
- `/boutique/commandes/[id]`
- `/series/[slug]`

Cette liste décrit un **état observé historique**, pas une validation canonique de toutes ces fonctions.

## 6.3 Legacy / non canonique par défaut

Les routes ou concepts suivants ont été observés dans des états historiques mais ne doivent pas redevenir produit canonique sans décision récente :
- `/points`
- `/boutique`
- `/admin/recompenses`
- anciennes catégories/créatrices
- programmes de points/crédits/récompenses/VIP.

---

# 7 — COMPORTEMENT DES VIDÉOS ET DROITS

## Toutes les vidéos publiées
- sont réservées ;
- sont accessibles par abonnement actif **ou** achat PPV individuel ;
- n'accordent jamais d'accès du seul fait d'être inscrit.

## Preview / hover / zoom
Une preview ne peut jamais augmenter le niveau de révélation :
- source verrouillée/safe → preview verrouillée/safe ;
- aucun média sensible plus clair ne doit apparaître dans hover/sheet/zoom sans entitlement réel.

Desktop :
- PreviewCardLayer indépendant ;
- l'effet de zoom/agrandissement doit conserver la carte dans son contexte et gérer les bords sans rendre les voisines inaccessibles ;
- ne pas implémenter un simple `scale(3)` aveugle si cela casse la rangée.

Mobile :
- `PreviewSheet` / interaction tactile ;
- pas de hover desktop compressé ;
- pas de curseur custom.

## Cartes
- carte entière cliquable lorsque le produit le prévoit ;
- métadonnées dans une zone dédiée, pas posées sur le média si cela le masque ;
- pas de bande blanche générique ;
- vrais médias et vraies données runtime.

---

# 8 — WATCH / PAYWALL / AUDIO

## Watch
- lecture réelle protégée par entitlement ;
- médias privés / URL de lecture contrôlés côté serveur ;
- aucune URL sensible délivrée à un utilisateur non autorisé.

## Paywall
- reflète exactement les deux voies d'accès actives : abonnement ou PPV ;
- aucun plan supplémentaire inventé ;
- textes contenus dans les zones, sans traverser les cadres artistiques.

## Audio ambiant
- continue sur watch/paywall/locked/pre-play tant que la vidéo n'a pas réellement démarré ;
- se coupe uniquement sur le véritable événement `play` ;
- reprend lorsque la lecture s'arrête.

---

# 9 — COMPTE MEMBRE

Le compte doit être un dashboard consolidé, pas un panneau générique.

Familles attendues :
- profil ;
- e-mail ;
- statut âge ;
- abonnement ;
- achats PPV ;
- favoris ;
- historique ;
- notifications ;
- sécurité ;
- support ;
- données/gestion du compte ;
- suppression selon règles produit.

Un abonné actif ne voit pas d'appel générique « S'abonner » là où son accès est déjà acquis.

---

# 10 — ADMIN OPÉRATIONNEL

Le vrai admin doit permettre, selon le modèle réel :
- créer ;
- consulter ;
- modifier ;
- supprimer ;
- publier/dépublier si le modèle le prévoit ;
- classer/ordonner ;
- gérer vidéos ;
- gérer photos/stills ;
- gérer séries et métadonnées pertinentes ;
- gérer les autres contenus administrables réels.

Exigences :
- desktop + mobile ;
- rapide et exploitable quotidiennement ;
- états loading/success/error ;
- confirmations destructives ;
- contrôles sensibles côté serveur ;
- `/admin/dev` reste séparé.

---

# 11 — ÉDITEUR VISUEL DANS L'ADMIN — EXIGENCE ACTIVE

Décision utilisateur du 2026-09-03 :
l'administrateur doit pouvoir **modifier visuellement la composition du site** depuis l'admin au lieu de dépendre d'un agent de code pour chaque déplacement/espacement.

Objectif :
- drag-and-drop de blocs Cortezia ;
- réglage position/ordre/largeur/espacement ;
- preview desktop/mobile ;
- choix contrôlé d'assets ;
- modification de contenu sûr si autorisée ;
- publication d'une composition sans modifier la logique métier.

Séparation absolue :
- **éditeur visuel** = composition et propriétés visuelles autorisées ;
- **code/backend** = auth, âge, entitlement, paiement, médias privés, admin permissions, destinations sensibles.

Un bouton visuellement déplacé doit continuer d'appeler **la vraie action codée** ; l'éditeur ne doit pas permettre de réécrire arbitrairement sa logique.

## Recommandation actuelle : PUCK

Statut : `RECOMMENDED / NOT_YET_IMPLEMENTED`.

Pourquoi :
- open-source MIT ;
- s'embarque directement dans React/Next.js ;
- utilise les vrais composants React de Cortezia ;
- données JSON stockables dans notre propre backend ;
- pas de vendor lock-in ;
- permissions globales/composant/instance pour interdire `delete`, `drag`, `duplicate`, `edit`, `insert` sur les blocs sensibles ;
- viewports configurables pour desktop/mobile.

Architecture recommandée :
- éditeur protégé dans le vrai admin (route exacte à choisir lors de l'implémentation) ;
- bibliothèque de blocs Cortezia autorisés ;
- fond marbre global fixé/indestructible ;
- composants sensibles verrouillés ou exposant uniquement des props sûres ;
- `draft` + `published` + historique/révision/rollback ;
- validation serveur d'un schéma/allowlist avant sauvegarde ;
- aucun champ arbitraire JS/HTML/CSS exécutable ;
- rendu public à partir du JSON sauvegardé avec les vrais composants.

---

# 12 — DIRECTION ARTISTIQUE CANONIQUE

## Matières
- fond global : marbre blanc / ivoire **animé existant** ;
- onyx/noir : matière locale ;
- or : champagne/poli, lumineux mais contrôlé.

## Langage
- premium ;
- joaillier ;
- sculpté ;
- courbes ;
- relief ;
- profondeur ;
- asymétries contrôlées ;
- formes adaptées à leur fonction.

Interdits :
- thème noir global ;
- dashboard SaaS générique ;
- rectangles noirs bordés d'or comme substitut aux formes ;
- cyberpunk/néon gratuit ;
- ancienne DA Ariana/créatrice.

## Branding
Wordmark canonique : `CORTEZIA.`  
Contraintes validées :
- R ouvert ;
- A ouvert ;
- point final.

Le vrai CTZ et le vrai wordmark runtime priment sur tout branding généré dans un PNG.

---

# 13 — TARGETS VISUELS ET ASSETS

## Golden visual targets
Une image de page complète :
- montre la cible finale ;
- sert de comparaison visuelle ;
- **n'est jamais** un background runtime cliquable ;
- ne crée jamais de vérité produit à partir de ses textes/médias fictifs.

Desktop :
- cible 16:9 lorsqu'elle est générée comme écran de référence.

Mobile :
- cible 9:16 lorsqu'elle est générée comme écran de référence.

Arrière-plan des targets :
- transparent quand il représente la couche extérieure, afin de laisser vivre le fond animé runtime.

Footer :
- finit physiquement la page ;
- branding puis barre légale ;
- aucun vide sous la barre légale.

## Architecture hybride runtime
`MARBRE_RUNTIME → MÉDIAS_RUNTIME → SHELL_ARTISTIQUE → DOM/SVG_RUNTIME → ÉTATS/DONNÉES/INTERACTIONS`

La bonne méthode n'est ni :
- une capture entière + hotspots ;
- ni une reconstruction CSS pauvre des formes complexes.

On garde les coques artistiques adaptées et on pose les vrais éléments runtime.

---

# 14 — PIPELINE ASSETS V10

Source : 150 jobs numérotés 001→150.

État le plus récent documenté :
- 50 reçus ;
- 16 PASS ;
- 34 REGENERATE ;
- 0 AMBIGUOUS ;
- 100 MISSING ;
- `COMPLETE=false`.

PASS :
`001,002,003,004,005,006,011,013,014,018,021,025,026,028,029,030`

Règle `REGENERATE` :
- ne jamais supprimer ni oublier ;
- conserver bytes/hash/motif/correction ;
- la nouvelle version ne devient PASS qu'après correction technique **et** validation réelle de la silhouette artistique.

Runtime obligatoire, jamais baked comme vérité :
- CORTEZIA / CTZ ;
- textes/labels ;
- prix/données ;
- médias ;
- play/close/chevrons/toggles/sliders ;
- favoris/bookmark ;
- menus/recherche ;
- états/progressions ;
- copyright/liens légaux.

---

# 15 — WORKFLOW D'AGENTS / MICRO-PACKS

## Principe actif
**UN ÉCRAN = UN MICRO-PACK.**

Rôles :
- continuité/assistant = Bible, Drive, GitHub, sélection assets, préparation des packs ;
- Codex/Claude = exécuteur local ciblé.

Un micro-pack doit contenir uniquement :
- `PROMPT.txt`
- `TARGET.png`
- `SCREEN.json`
- branding strictement nécessaire
- assets strictement nécessaires
- éventuellement un extrait ciblé de la Bible.

Interdits pour l'agent d'exécution lorsque le micro-pack est autonome :
- ne pas relire Drive ;
- ne pas relire GitHub ;
- ne pas rouvrir 27 discussions ;
- ne pas réauditer tout le dépôt ;
- ne pas lancer toute la suite de tests à chaque micro-ajustement.

Workflow :
`TARGET → FICHIERS RUNTIME CIBLÉS → IMPLÉMENTATION → CAPTURE → COMPARAISON → CORRECTION → TESTS CIBLÉS → STOP`

Output minimal :
- STATUS
- FILES_CHANGED
- TESTS
- CAPTURE
- VISUAL_GAPS
- SNAPSHOT

## Carte de chemins confirmés
Conserver un `CORTEZIA_CODEX_MAP` court pour éviter la redécouverte.

Pour SCREEN_01 Gate, le compte-rendu Codex a indiqué :
- `components/legal/AgeGate.tsx`
- `app/styles/cortezia-visual-mission-001-040.css`
- `public/assets/cortezia-visual/`
- `public/assets/cortezia-gate-01/`

Ces chemins sont `SOURCE_BACKED_BY_CODEX_REPORT`, pas revalidés directement contre le worktree dans cette consolidation.

---

# 16 — CURSEURS

Décision stable historique :
- quatre curseurs Cortezia validés ;
- cycle global de 24 h ;
- changement déterministe ;
- coarse pointer/mobile exclus ;
- aucun curseur custom mobile.

Le runtime actuel doit être revalidé avant modification, mais ne pas réinventer une nouvelle famille de curseurs sans décision.

---

# 17 — RESPONSIVE

Desktop et mobile ne sont pas des copies redimensionnées.

À vérifier par surface :
- navigation ;
- hiérarchie ;
- densité ;
- cartes ;
- overlays ;
- player ;
- zones tactiles ;
- footer ;
- clavier/focus ;
- collisions fixes ;
- overflow horizontal.

Audit visuel historique récent :
- `/recherche` cassée desktop/mobile ;
- collisions cookies/navigation mobile ;
- overflows sur `/notifications`, `/nouveautes`, `/boutique/commandes` ;
- certaines cibles tactiles/labels insuffisants ;
- pages secondaires trop génériques ;
- vrai backoffice non prouvé.

Ces constats deviennent STALE seulement pour les surfaces effectivement modifiées.

---

# 18 — SÉCURITÉ / BACKEND — FRONTIÈRES À CONNAÎTRE

La Bible ne duplique pas l'implémentation serveur, mais les invariants suivants ne sont jamais négociables :

- âge officiel côté serveur/fail-closed pour le contenu sensible ;
- entitlement côté serveur ;
- admin autorisé côté serveur ;
- médias privés protégés ;
- paiement/webhooks validés côté serveur ;
- secrets hors Bible/Drive/GitHub public ;
- aucune activation production/paiement/service payant sans approbation.

Le visuel peut être éditable ; ces contrôles ne le sont pas.

---

# 19 — ENVIRONNEMENTS

Trois contextes distincts :
- `local_real`
- `local_simulator`
- `admin_local`

Le simulateur :
- DEV-only ;
- fail-closed ;
- ne remplace pas le vrai site ;
- ne remplace pas le vrai admin.

Local-first :
- le vrai dossier local reste la vérité technique de développement ;
- Drive et GitHub continuité sont de la documentation/mémoire ;
- aucun push/pull/merge/reset/déploiement du site par initiative.

---

# 20 — CONTINUITÉ

Deux miroirs documentaires :
1. Google Drive canonique privé ;
2. GitHub `mrperezthomas-boop/CORTEZIA-CONTINUIT-CANONIQUE-PRIV-E`.

Ils doivent rester sémantiquement synchronisés.

Le dépôt GitHub de continuité :
- n'est PAS le dépôt du site ;
- ne doit contenir aucun secret ;
- sert à la Bible, décisions, méthodes, preuves textuelles et handoffs.

---

# 21 — CE QUI EST SUPERSEDED / À NE PAS RÉINTRODUIRE

- Gate +18 → vérification officielle automatique → accueil : **SUPERSEDED**.
- Multi-abonnements / Standard / Premium / VIP : **SUPERSEDED**.
- abonnement 13,99 / 16,99 / 19,99 : **SUPERSEDED**.
- Ariana/créatrice centrale : **SUPERSEDED**.
- points/crédits/récompenses comme cœur du produit : **NON CANONIQUE**.
- PNG complet utilisé comme page cliquable : **INTERDIT**.
- gros pack Codex + audit global à chaque écran : **SUPERSEDED**.
- `/admin/dev` présenté comme vrai admin : **INTERDIT**.
- maquette comme source de prix/texte/données : **INTERDIT**.
- fond noir global : **INTERDIT**.

---

# 22 — OPEN / À VÉRIFIER

Ne pas inventer :
- provider final de vérification d'âge ;
- points exacts du runtime où la vérification officielle se déclenche ;
- prestataire paiement final/contrat actif ;
- état distant Supabase/migrations/services ;
- domaine/déploiement final ;
- couverture CRUD exacte du vrai admin actuel ;
- identifiants des routes dynamiques sans fixtures ;
- état exact du worktree après les dernières tentatives Codex ;
- implémentation Puck (recommandée mais non encore faite).

---

# 23 — DONE POUR UNE SURFACE

Une surface n'est `DONE` que si :
- comportement fonctionnel réel ;
- bon état utilisateur ;
- destinations/actions réelles ;
- sécurité correspondante préservée ;
- desktop/mobile requis ;
- rendu visuel conforme à la cible validée ;
- loading/error/success/focus pertinents ;
- tests ciblés ;
- capture/rendu final inspecté ;
- preuve liée à l'état exact livré.

---

# 24 — RÈGLE FINALE POUR TOUT AGENT

Ne reconstruis pas Cortezia depuis une vieille conversation.

1. lis cette Bible ;
2. lis uniquement l'état courant ciblé nécessaire ;
3. respecte les décisions actives ;
4. ne transforme aucune maquette en vérité fonctionnelle ;
5. préserve le backend et les droits réels ;
6. pour une tâche écran, utilise un micro-pack minimal ;
7. si l'information n'est pas dans la Bible et qu'elle dépend du runtime, vérifie uniquement le delta nécessaire ;
8. ne réintroduis jamais un élément `SUPERSEDED`.


## Décision éditeur visuel — 2026-09-03

- Puck est **sélectionné** comme éditeur visuel canonique à intégrer dans le vrai admin Cortezia.
- Statut : `SELECTED_NOT_IMPLEMENTED` tant que le vrai worktree n'a pas été modifié et validé.
- Route cible préférée : `/admin/design` (adapter seulement si le routage admin réel impose une convention existante).
- Première intégration : moteur d'éditeur + page Accueil pilote, architecture extensible aux autres surfaces.
- Auth : réutiliser le vrai contrôle admin s'il existe et fonctionne ; sinon bootstrap local uniquement, secret jamais commité, identifiant/mot de passe générés localement par l'agent et remis une fois au propriétaire.
- Les règles sensibles (âge, entitlement, paiement, médias privés, permissions, destinations d'actions sensibles) restent hors édition libre.
