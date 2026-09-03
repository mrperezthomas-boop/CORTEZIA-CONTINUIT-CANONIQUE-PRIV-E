# CORTEZIA — DECISIONS LOG NON VISUAL
Statut : ACTIVE
Règle : n’enregistrer ici que les décisions explicites durables. Une décision remplacée est marquée SUPERSEDED, jamais effacée silencieusement.
## ACTIVE — LOCAL FIRST
Le développement courant se fait en local.
Le local réellement travaillé prime.
Aucune synchronisation Git n’est automatique.
## ACTIVE — PRODUIT RÉEL
Cortezia est un service premium de diffusion de contenus adultes réellement exploitable, pas une vitrine.
## ACTIVE — DESKTOP + MOBILE
Desktop et mobile sont deux cibles réelles du produit.
## ACTIVE — PAS DE CRÉATRICE CENTRALE
Ne pas réintroduire Ariana/personnage/créatrice centrale comme structure du produit final.
## ACTIVE — VIDÉOS RÉSERVÉES
Toute vidéo publiée est réservée.
Accès via abonnement actif ou PPV individuel.
PPV actif établi : 3,99 € par vidéo publiée.
## ACTIVE — INSCRIPTION ≠ ABONNEMENT
Un utilisateur inscrit sans entitlement ne reçoit pas d’accès média par la seule inscription.
## ACTIVE — PREVIEW N’AUGMENTE PAS LES DROITS
Hover, preview, sheet, zoom ou watch ne peuvent révéler plus que ce que l’entitlement de l’utilisateur autorise.
## ACTIVE — ADMIN DEV ≠ ADMIN OPÉRATIONNEL
La simulation DEV n’est pas le back-office réel.
Un parcours admin réel et des opérations réellement persistantes sont requis pour l’exploitation.
## ACTIVE — EXEMPLE PRÉCIS ≠ SCOPE PRÉCIS PAR DÉFAUT
Sauf restriction explicite, un cas précis est un témoin du besoin ; la classe générale doit être recherchée et traitée.
## ACTIVE — APPROBATION AVANT MODIFICATION
L’agent peut auditer et préparer.
Avant mutation, il présente un résumé court et attend validation explicite, sauf dérogation actuelle claire.
## ACTIVE — AUCUNE ACTIVATION EXTERNE SILENCIEUSE
Paiement, abonnement, boutique, service payant, contrat, dépense, migration distante importante et production restent sous approbation utilisateur.
## ACTIVE — SOURCE DE CONTINUITÉ
Le Drive de projet est organisé pour conserver canon, état, décisions, preuves, inconnues et handoffs séparément.
Une synthèse actuelle ne doit jamais dépendre uniquement de l’historique conversationnel
## ACTIVE — ABONNEMENT UNIQUE
Prix final décidé : 14,99 €.
Un seul abonnement. Aucun autre plan ni autre offre d’abonnement.
## ACTIVE — FAVORIS
Les favoris sont réservés aux abonnés actifs.
## ACTIVE — SAFE SHELL AVANT VÉRIFICATION D’ÂGE
Avant vérification réelle de l’âge, Cortezia ne doit exposer aucun contenu pornographique.
Le clic +18 peut servir d’avertissement/entrée SAFE mais ne vaut jamais vérification.
## ACTIVE — BACKEND FIRST
Les droits âge, entitlement, admin, médias privés et paiement sont imposés côté serveur. Une restriction visuelle seule n’est jamais suffisante.
## ACTIVE — ENVIRONNEMENTS DISTINCTS
local_real, local_simulator et admin_local sont des contextes distincts.
Le simulateur ne remplace ni le vrai site local ni le vrai admin local.
## ACTIVE — PAIEMENT PROVISOIRE
CCBill est la direction provisoire principale pour la carte bancaire adulte.
Le provider final peut encore être comparé avant activation ; aucun contrat/compte/paiement réel n’est activé par cette décision.
## ACTIVE — AUDIO
L’audio d’ambiance continue sur watch/paywall/locked/pre-play, se coupe uniquement au vrai événement play et reprend lorsque la lecture s’arrête
## ACTIVE — CONTINUITÉ DRIVE UNIQUEMENT
Le Drive canonique privé est la source de continuité documentaire active.
Le workflow normal ne génère plus de ZIP, Master Source ou pack de fichiers à remplacer/importer.
Une archive ou un export n’est produit que sur demande explicite de l’utilisateur.
Les mises à jour courantes sont effectuées directement dans les documents Drive concernés.
## 2026-09-03 — CONTINUITÉ DUALE DRIVE + GITHUB
Statut : ACTIVE / EXPLICIT_DECISION
Le Drive canonique privé et le dépôt GitHub mrperezthomas-boop/CORTEZIA-CONTINUIT-CANONIQUE-PRIV-E doivent être maintenus en parallèle comme deux miroirs de continuité.
Le dépôt GitHub de continuité n’est PAS le dépôt du site. Il ne doit contenir ni logique de production, ni déploiement du site, ni être confondu avec le futur repository du site.
Les écritures GitHub sont autorisées pour CE dépôt de continuité afin de maintenir la mémoire documentaire. Cette autorisation ne s’étend pas à un futur dépôt du site.
## 2026-09-03 — REGENERATE = CONSERVÉ + RÉPARABLE
Statut : ACTIVE / EXPLICIT_DECISION
Un asset classé REGENERATE n’est jamais supprimé de l’historique. Conserver la version reçue, la raison du rejet et la correction précise permettant de la rendre conforme.
Une version corrigée ne devient PASS qu’après recontrôle réel. La conformité technique ne suffit pas : la silhouette/forme artistique correspondant au job doit aussi être validée. Tant que cette validation visuelle n’existe pas, l’asset reste non-PASS.
## 2026-09-03 — WORKFLOW CODEX MICRO-PACK PAR ÉCRAN
Statut : ACTIVE / EXPLICIT_DECISION
Pour économiser les crédits Codex, ne plus envoyer un gros pack ni demander un audit global pour chaque écran.
Principe : UN ÉCRAN = UN MICRO-PACK ciblé.
Rôles :
- Assistant/continuité = mémoire, sélection des assets, Drive + GitHub, préparation du micro-pack.
- Codex = exécuteur local ciblé.
Codex ne doit pas consulter Drive/GitHub ni relire l'historique pour une mission écran lorsqu'un micro-pack autonome est fourni.
Règles Codex écran :
- DO NOT AUDIT THE WHOLE REPOSITORY.
- ne pas lire les anciens rapports ;
- ne pas rechercher Drive/GitHub ;
- inspecter seulement les fichiers runtime nécessaires à l'écran ;
- préserver l'architecture existante ;
- tests ciblés pendant l'implémentation ;
- suite complète/build global seulement après groupe significatif ou gate global ;
- OUTPUT_MODE=MINIMAL ;
- réponse finale : STATUS, FILES_CHANGED, TESTS, CAPTURE, VISUAL_GAPS, SNAPSHOT.
Une carte courte CORTEZIA_CODEX_MAP doit mémoriser les chemins réellement confirmés afin d'éviter de les rechercher à chaque écran.
## 2026-09-03 — PARCOURS +18 PUIS ACCUEIL SAFE
Statut : ACTIVE / EXPLICIT_DECISION
Le Basic Gate +18 est une déclaration/avertissement. Après acceptation, le parcours initial mène à l’accueil SAFE. La vérification officielle d’âge est un mécanisme distinct et ne constitue pas l’écran suivant automatique. Ses points d’activation exacts doivent être reliés au runtime et aux obligations applicables, jamais inventés depuis une ancienne maquette.
## 2026-09-03 — BIBLE CORTEZIA CANONIQUE
Statut : ACTIVE / EXPLICIT_DECISION
CORTEZIA_BIBLE devient la source canonique compacte pour le produit, l’UI, la navigation, les états utilisateurs, la DA, les exigences admin et le workflow d’agents. Elle évite de relire l’historique complet. L’état technique volatil du code doit toujours être vérifié sur le delta nécessaire.
## 2026-09-03 — ÉDITEUR VISUEL DANS LE VRAI ADMIN
Statut : ACTIVE_REQUIREMENT
L’administrateur doit pouvoir modifier visuellement la composition autorisée du site depuis le vrai admin sans rendre éditables les règles sensibles. Puck est la recommandation actuelle après recherche officielle ; statut PUCK=RECOMMENDED_NOT_IMPLEMENTED jusqu’à intégration et test réels.
## 2026-09-03 — PUCK SÉLECTIONNÉ POUR L’ÉDITEUR VISUEL ADMIN
Statut : ACTIVE / EXPLICIT_DECISION
Puck est sélectionné comme éditeur visuel canonique à intégrer dans le vrai admin Cortezia. Statut d’implémentation : SELECTED_NOT_IMPLEMENTED tant que le vrai worktree n’a pas été modifié et validé. Route cible préférée : /admin/design. Première intégration : moteur d’éditeur + Accueil pilote, extensible aux autres pages. Les règles sensibles restent verrouillées hors édition libre. L’auth existante doit être réutilisée si valide ; sinon bootstrap local uniquement, secret non commité.
.