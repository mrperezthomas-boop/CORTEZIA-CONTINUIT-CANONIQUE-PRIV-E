# CORTEZIA — CURRENT STATE NON VISUAL
Statut : ACTIVE / MUST_BE_RESYNCED
But : photographie de reprise. Les faits techniques volatils doivent être revalidés sur le local avant utilisation comme vérité actuelle.


## ÉTABLI DE MANIÈRE DURABLE
- Mode de travail : LOCAL FIRST.
- Produit : service premium réel de diffusion de contenus adultes, pas vitrine.
- Desktop + mobile requis.
- Pas de créatrice centrale comme modèle produit.
- Vidéos publiées réservées ; accès par abonnement actif ou PPV individuel.
- PPV actuellement établi : 3,99 € par vidéo publiée.
- Inscription seule ne donne pas accès au média.
- Preview et surfaces secondaires n’accordent aucun droit supplémentaire.
- Données et médias finaux doivent rester dynamiques.
- Vrai admin opérationnel requis ; /admin/dev ne suffit pas.
- Paiement, services payants, migration distante et production nécessitent approbation.
- Sécurité sensible côté serveur, secrets protégés.


## DERNIER ÉTAT TECHNIQUE DOCUMENTÉ — HISTORIQUE, PAS VÉRIFIÉ AUJOURD’HUI
Des audits transmis précédemment ont indiqué un projet local situé sous :
K:\Cortezia Studio\Sit Officiel Cortezia
et ont rapporté notamment Next.js 15, React 19, TypeScript 5.7.x, npm, des migrations Supabase locales et diverses validations.
Ces éléments sont SOURCE_BACKED_HISTORICAL. Ils doivent être re-audités avant toute affirmation actuelle.


## ÉTAT DE VALIDATION
USER_VALIDATED = false tant qu’une validation humaine finale explicite n’a pas été donnée sur l’état concerné.
Les anciens résultats build/tests/E2E restent valables uniquement pour l’état exact sur lequel ils ont été exécutés.


## SERVICES
La présence passée de variables locales n’établit pas l’état distant.
CONFIGURED_LOCAL ≠ VERIFIED_REMOTE.


## ADMIN
Le besoin d’un back-office réel est établi.
Le chemin d’accès, les credentials et la couverture CRUD réellement opérationnelle sur l’état local actuel ne sont pas établis par le Drive à ce stade.


## RÈGLE DE REPRISE
Avant toute tâche qui dépend de l’état technique :
1. vérifier le vrai dossier local ;
2. vérifier fichiers/runtime/tests concernés ;
3. comparer à ce CURRENT_STATE ;
4. marquer les preuves devenues STALE ;
5. mettre ce document à jour par delta
## DÉCISIONS COURANTES AJOUTÉES
- Abonnement unique : 14,99 €.
- Aucun autre plan/offre d’abonnement.
- PPV : 3,99 € par vidéo publiée.
- Favoris : abonnés actifs uniquement.
- SAFE SHELL avant vérification d’âge ; +18 seul n’est pas une preuve d’âge.
- CCBill = provider paiement adulte provisoire principal ; Stripe = exclu par politique actuelle ; Segpay = alternative à évaluer.
- local_real / local_simulator / admin_local doivent rester distincts.
- Backend-first : âge + entitlement + admin + médias privés + paiement doivent être contrôlés côté serveur.
- Audio d’ambiance : continue en watch/paywall/locked/pre-play ; coupure uniquement au vrai play ; reprise à l’arrêt.


## DIFFUSION EN LIGNE — FUTUR
Le projet doit être diffusé en ligne à terme.
GitHub est un choix probable/recommandable pour source control + CI/CD, mais il n’est pas techniquement obligatoire pour héberger le site et aucune synchronisation Git n’est autorisée maintenant sans demande explicite.
Architecture de déploiement finale = OPEN


## CONTINUITÉ DOCUMENTAIRE ACTIVE
Source de reprise : Drive canonique privé.
Aucun ZIP/Master n’est requis pour la maintenance courante.
Toute nouvelle information durable ou tout changement d’état doit être propagé directement au bon document Drive.


## CONTINUITÉ ACTIVE — 2026-09-03
- Google Drive canonique privé : ACTIVE.
- GitHub de continuité : ACTIVE, repository mrperezthomas-boop/CORTEZIA-CONTINUIT-CANONIQUE-PRIV-E.
- Le GitHub de continuité est séparé du futur repository du site.
- Visibilité GitHub observée : PUBLIC ; l’utilisateur a explicitement autorisé qu’il reste public si le réglage privé n’est pas disponible via l’outil.
- Aucun secret ne doit y être stocké.
- Canon textuel : miroir Drive + GitHub.
- Binaires V10/batches/pack : stockés dans Drive et indexés dans GitHub tant que la surface GitHub connectée reste text-only.
- Pipeline V10 courant : 16 PASS / 24 REGENERATE / 110 MISSING / COMPLETE=false.




## CODEX MICRO-PACK MODE — 2026-09-03
Mode actif pour les écrans visuels : Codex exécuteur local ciblé.
La continuité Drive + GitHub ne doit pas être rechargée par Codex à chaque écran.
La carte de chemins connus doit être réutilisée pour minimiser l'exploration.
SCREEN_01 Gate reste un état de reprise source-backed par le compte-rendu Codex, pas une implémentation déclarée terminée.
V10 courant : 50 reçus, 16 PASS, 34 REGENERATE conservés, 100 MISSING.
.