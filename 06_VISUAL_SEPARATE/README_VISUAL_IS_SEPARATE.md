# VISUAL — SEPARATE SCOPE / CURRENT STATE
Statut : ACTIVE / PARTIAL / AUDIT_COMPLETE / USER_VALIDATED=false


Ce dossier est réservé à la direction artistique, aux assets, références, captures, prompts, règles visuelles et preuves visuelles Cortezia.
Il n’est pas chargé par défaut pour une demande produit, business, sécurité, architecture ou état technique.


Règle fondamentale :
une référence visuelle ne décide jamais silencieusement des droits, prix, offres, routes, données, textes, sécurité, paiements, admin ou conformité.


## DERNIER AUDIT VISUEL LOCAL COMPLET
Source : handoff utilisateur issu de CORTEZIA_AUDIT_VISUEL_TOTAL_LOCAL.zip.
Nature : audit non destructif du site local, sans correction du runtime.
Statut global observé : PARTIAL.


### Couverture vérifiée
- 75 routes inventoriées et documentées.
- 67 routes réellement rendues.
- 8 routes dynamiques BLOCKED faute de fixture locale réelle.
- 450/450 cellules de matrice utilisateur analysées (6 états × 75 routes).
- 184 captures full-page : 92 desktop + 92 mobile.
- 184 réponses HTTP 200.
- 0 erreur de navigation.
- 0 erreur de capture.
- 0 erreur JavaScript de page.
- 0 origine externe contactée pendant les captures.
- 2 captures avec le même 403 sur une vidéo sans droit, documenté.
- 90 assets publics catalogués et reliés au code/runtime.
- Worktree strictement inchangé entre début et fin de l’audit.


### Pack de preuve
Chemin local déclaré :
K:\Cortezia Studio\DOSSIER SITE OFFICIEL\CORTEZIA_AUDIT_VISUEL_TOTAL_LOCAL.zip


Taille déclarée : 80 177 043 octets.
SHA-256 déclaré :
98693993315BD349BCD97E2C8726DC34CC911702266A43332C7AE86B18E402BA


Le Drive conserve ici l’état de reprise et les métriques de l’audit. Le ZIP complet reste une preuve locale externe tant qu’il n’est pas importé dans le Drive canonique.


## CANON VISUEL OBSERVÉ / CONFIRMÉ
- Fond global blanc/ivoire animé : présent et global.
- Onyx/noir : majoritairement local ; exceptions contextuelles cohérentes sur portail d’âge, lecteur et admin DEV.
- Or : accent, filet, coque ou état actif, clairement identifiable.
- Vraies miniatures/données/médias : présentes dans catalogues et lecteur.
- États abonné / PPV / verrouillé : distincts sur la fixture vidéo.
- Mobile : composition réelle mais qualité partielle.
- Direction générale à préserver : luxe, matière, profondeur, courbes, précision, marbre clair global, onyx local, or champagne/poli contrôlé.


## PROBLÈMES PRIORITAIRES OBSERVÉS
P1
1. /recherche cassée desktop et mobile : résultats tassés dans une colonne étroite et cartes qui se chevauchent.
2. Bannière cookies + navigation basse mobile : recouvrent contenu, formulaires, cartes, boutons et informations de compte.
3. Débordements horizontaux mesurés sur /notifications, /nouveautes et /boutique/commandes.


P2
4. Accessibilité observable : au moins une cible < 44 × 44 px dans les 184 captures ; recherche et commentaire avec nom accessible non détecté.
5. Incohérence de qualité : pages secondaires trop génériques, trop vides ou dominées par des panneaux blancs.
6. Vrai backoffice non prouvé : routes d’administration observées via le shell local Administration DEV ; cela ne valide pas le backoffice opérationnel.


## ROUTES DYNAMIQUES ENCORE BLOQUÉES
- /admin/commandes/[id]
- /admin/conformite/performers/[id]
- /admin/recompenses/[slug]
- /admin/series/[slug]
- /admin/support/[id]
- /admin/videos/[slug]
- /boutique/commandes/[id]
- /series/[slug]


Pour clôturer ces 8 détails visuellement, il faut des identifiants/fixtures locales valides. Ne jamais inventer un slug ou un ID.


## ORDRE DE CORRECTION RECOMMANDÉ
1. /recherche.
2. collisions cookies/navigation mobile.
3. overflows.
4. tailles de cibles et labels accessibles.
5. cohérence visuelle des pages secondaires.
6. preuve séparée du vrai backoffice.


Toute correction future doit être une mission séparée, réversible, validée desktop + mobile, sans modifier silencieusement les données dynamiques ni les règles d’accès.


## RÈGLE DE CONTINUITÉ
NE PAS RECOMMENCER cet audit tant que l’état local pertinent n’a pas changé matériellement.
Pour une mission visuelle, commencer par ce document puis consulter les preuves/captures du pack local si disponibles.
Si le runtime a changé depuis cet audit, les preuves visuelles deviennent STALE uniquement pour les surfaces affectées et doivent être recapturées de façon ciblée, pas par ré-audit total automatique.




## PIPELINE ASSETS V10 — ÉTAT ACTIF 2026-09-03
Statut : PARTIAL / USER_VALIDATED=false
Source canonique : CORTEZIA_LAYOUTS_V10, 150 jobs numérotés 001→150.


État courant :
- expected = 150
- received = 40
- PASS = 16
- REGENERATE = 24
- AMBIGUOUS = 0
- MISSING = 110
- COMPLETE = false


PASS :
001, 002, 003, 004, 005, 006, 011, 013, 014, 018, 021, 025, 026, 028, 029, 030.


REGENERATE :
007, 008, 009, 010, 012, 015, 016, 017, 019, 020, 022, 023, 024, 027, 031, 032, 033, 034, 035, 036, 037, 038, 039, 040.


MISSING :
041→150.


RÈGLE DE CONSERVATION DES REJETS :
REGENERATE ne signifie jamais supprimer, oublier ou jeter la version reçue. Chaque version rejetée reste tracée avec ID, lot, hash si disponible, défaut précis, correction nécessaire et historique de remplacement. Elle ne doit simplement pas entrer dans ASSETS_FINAL tant qu’elle n’est pas revalidée.


RÈGLE DE SORTIE DE REGENERATE :
une nouvelle version sort de REGENERATE seulement après contrôle réel de la correction demandée. La conformité technique seule ne suffit pas : la vraie forme/silhouette artistique destinée au job doit aussi être visuellement validée. Tant que la forme n’est pas validée, le statut reste non-PASS.


RÈGLE BAKED/RUNTIME :
BAKED autorisé = matière, onyx, ivoire, or, relief, coque, cadre, courbes, ornements, structure, séparations et puits visuellement vides.
RUNTIME obligatoire = CORTEZIA., CTZ, logo, textes, labels, prix, données, médias, miniatures, play, close X, chevrons, toggles, sliders, favoris, bookmark, recherche, menus, états actifs, progressions, copyright et liens légaux.


Dossiers Drive actifs :
- 01_ASSET_PIPELINE_V10
- 02_SOURCE_SPECS_V10
- 03_VALIDATED_ASSETS
- 04_BATCHES_RECEIVED
- 05_REFERENCE_DA.




## FILE DE RÉGÉNÉRATION DÉTAILLÉE — 001→040
Règle : chaque version ci-dessous est CONSERVÉE dans les batches reçus. Elle est interdite dans ASSETS_FINAL tant qu’elle n’est pas PASS, mais sa forme reste candidate à validation. FORM_VALIDATION = PENDING sauf validation explicite ultérieure.


007 — défaut : X baked. Correction : conserver la coque/forme, laisser le puits de fermeture vide ; SVG/DOM runtime.
008 — défaut : pictogramme d’alerte baked. Correction : conserver la forme, supprimer le symbole ; icône runtime.
009 — défaut : progression/état dynamique baked. Correction : rail visuel neutre ; progression/état runtime.
010 — défaut : X + toggles baked. Correction : conserver les puits ; contrôles runtime.
012 — défaut : cloche + pastille d’état baked. Correction : garder uniquement les puits ; icône et état runtime.
015 — défaut : faux médias floutés + flèches baked. Correction : aucune image inventée ; zones média vides/alpha selon job ; contrôles runtime.
016 — défaut : progressions + Play/Favori/Signet/Flèche baked. Correction : conserver ouvertures alpha et puits ; retirer états/icônes.
017 — défaut : flèches de navigation baked. Correction : conserver puits latéraux sans pictogrammes.
019 — défaut : flèches, Play, cœur, signet, menu et CTA fléché baked. Correction : retirer contrôles/icônes ; forme décorative conservée pour revalidation.
020 — défaut : Play baked dans les ouvertures média. Correction : retirer triangles Play ; vrais contrôles runtime.
022 — défaut : chevrons de menus baked. Correction : garder puits neutres ; chevrons runtime.
023 — défaut : chevrons de filtres baked. Correction : retirer tous les pictogrammes de contrôle.
024 — défaut : deux chevrons baked. Correction : conserver uniquement les puits décoratifs.
027 — défaut : chevrons + poignée/état de slider baked. Correction : retirer contrôles et état ; DOM runtime.
031 — défaut : faux CTZ/CORTEZIA + navigation/icônes baked. Correction : garder coque et puits ; branding/navigation/icônes runtime.
032 — défaut : CORTEZIA + icônes/contrôles baked. Correction : retirer branding/pictogrammes ; préserver forme candidate.
033 — défaut : faux CTZ + recherche/fermeture/play/favoris/flèches baked. Correction : ouvertures alpha + puits neutres ; tout contrôle/branding runtime.
034 — défaut : faux CTZ baked. Correction : laisser médaillon vierge ; vrai branding runtime.
035 — défaut : faux CTZ + chevron baked. Correction : laisser emblème/action vides ; runtime.
036 — défaut : wordmark + liens légaux + copyright baked. Correction : footer structurel sans texte/branding ; tout contenu légal/runtime.
037 — défaut : texte cookies + icônes + boutons/fermeture baked. Correction : coque et puits uniquement ; vrais contrôles/textes DOM.
038 — défaut : faux CTZ + X baked. Correction : crest et puits fermeture vides ; branding/X runtime.
039 — défaut : branding, textes, poubelle, flèche, boutons et X baked. Correction : coque neutre uniquement ; tout fonctionnel en DOM/SVG.
040 — défaut : X + symbole d’état baked. Correction : laisser puits STATUS/ACTION neutres ; runtime.


GATE DE REVALIDATION POUR CHAQUE ID :
1. nouvelle version reçue ;
2. correspondance ID/job non ambiguë ;
3. correction du défaut précis réellement constatée ;
4. alpha/ouvertures techniques conformes ;
5. aucun texte, branding, média, donnée, état ou contrôle runtime baked ;
6. comparaison à la DA Cortezia et au rôle fonctionnel ;
7. validation de la vraie silhouette/forme artistique ;
8. PASS seulement après 1→7.
Si 1→6 passent mais que 7 n’est pas validé : rester REGENERATE / FORM_VALIDATION=PENDING, ne pas exclure la forme de l’historique.




## ASSETS LOT_05 + ÉCRANS + MICRO-PACKS — 2026-09-03
### LOT_05 041–050
Reçu et contrôlé contre les jobs V10.
- PASS : 0
- REGENERATE : 10
- AMBIGUOUS : 0
- FORM_VALIDATION : PENDING pour 041–050
- Les dix versions sont conservées comme candidates de forme ; aucune n'est supprimée.


Motifs :
041 cadenas baked.
042 Play/timeline/fullscreen/favori/états baked.
043 couronnes/emblèmes d'état baked.
044 Play/timeline/menu/cadenas + faux métadonnées baked.
045 pictogramme horloge/état baked.
046 chevrons/knobs de filtres baked.
047 X/chevrons/toggles/slider/favoris/états baked.
048 faux contenu/métadonnées baked dans la zone de copie.
049 cadenas/Play/cœur/progression/faux métadonnées baked.
050 faux contenu/métadonnées baked dans la zone runtime.


État global V10 : 50 reçus / 16 PASS / 34 REGENERATE / 0 AMBIGUOUS / 100 MISSING / COMPLETE=false.
Prochain ID jamais reçu : 051.


### BATCH_06 retrouvé
La spécification de génération 051–060 a été retrouvée dans la bibliothèque de continuité :
051 Hero accueil visiteur
052 Hero accueil abonné
053 Hero accueil acheteur PPV
054 Bloc média mis en avant
055 Rail continuer à regarder
056 Rail favoris
057 Rail nouveautés
058 Rail séries
059 Panneau les plus vues
060 Résumé compte accueil.
Aucun lot de 10 PNG 051–060 n'a été retrouvé/confirmé : 051–060 restent MISSING.


### ÉCRANS COMPLETS
Cibles reçues :
- SCREEN_01_GATE — micro-pack complet CORTEZIA_GATE_01
- SCREEN_02 — vérification officielle d'âge
- SCREEN_03 — connexion
- SCREEN_04 — inscription
- SCREEN_05 — accès premium verrouillé
- SCREEN_06 — vérifié sans entitlement
Les PNG d'écran sont GOLDEN VISUAL TARGETS, jamais backgrounds cliquables. Leurs textes, médias, prix et données visibles ne deviennent pas automatiquement canoniques.


Dossiers Drive :
- 06_SCREEN_TARGETS
- 07_CODEX_MICRO_PACKS
- 08_GENERATION_SPECS
.