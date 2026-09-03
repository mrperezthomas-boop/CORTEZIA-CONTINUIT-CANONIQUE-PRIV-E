# CORTEZIA — CODEX / SKILLS / TOOLING
Statut : ACTIVE_WORKFLOW
But : utiliser les bons outils sans charger ni connecter tout aveuglément.


## PRINCIPE
Un Skill = workflow réutilisable. Un plugin peut regrouper des skills, apps ou connexions.
Avant une mission importante :
1. inventorier les skills/plugins/MCP/outils réellement disponibles ;
2. sélectionner uniquement ceux utiles au scope ;
3. charger le skill avant le domaine correspondant ;
4. utiliser les outils natifs du projet en priorité ;
5. tracer TOOLS / SKILLS USED dans le handoff ;
6. ne jamais prétendre avoir utilisé un skill non chargé.


## OBSERVÉ RÉELLEMENT DANS CODEX CORTEZIA
### cortezia-visual-director
Statut : OBSERVED_USED
Chemin observé : .codex/skills/cortezia-visual-director/SKILL.md
Usage : DA, frontend public/admin, responsive, cartes, PreviewCardLayer, PreviewSheet, paywalls, formulaires, compte, player, footer/légal, curseurs/motion, intégration d’assets et QA visuelle.
Workflow visuel : CODE → RUNTIME → BROWSER → SCREENSHOT → INSPECTION → REPAIR → RECAPTURE.
Une lecture CSS/TSX seule ne valide pas une DA.


### Supabase skill
Statut : OBSERVED_USED + AVAILABLE
Règles utiles : vérifier docs/changelog actuels ; RLS sur tables exposées ; ne jamais exposer service_role/secret ; user_metadata non fiable pour l’autorisation ; tester après changement ; policies adaptées au vrai modèle d’accès.


## OUTILS / SKILLS À PRIVILÉGIER
### Browser / Playwright / agent-browser
Statut : HIGH_PRIORITY
Pour localhost réel, desktop/mobile, captures, interactions, console, navigation, auth, age gate, preview, paywall, admin, overflow et E2E.


### Full-story verification
Statut : RECOMMENDED_IF_AVAILABLE
Vérifie le flux complet browser → UI trigger → API → données/service → réponse UI.
Particulièrement important pour backend/auth/admin/entitlements.


### Next.js
Statut : RECOMMENDED_IF_AVAILABLE
Pour App Router, Server Components/Actions, routes API, middleware/proxy, rendering et boundaries serveur/client.


### React best-practices reviewer
Statut : RECOMMENDED_READ_ONLY_AFTER_TSX_CHANGES
Après plusieurs modifications TSX : structure, hooks, accessibilité, performance, TypeScript.


### Security reviewer
Statut : RECOMMENDED_READ_ONLY
Revue ciblée age gate, auth, RLS, média privé, signed URLs, entitlements, admin, assertAdminCritical, simulateur DEV, flags/loopback/non-prod et paiements/webhooks.
Un reviewer ne remplace jamais tests/runtime/E2E.


### Vercel firewall / observability
Statut : FUTURE_DEPLOYMENT_TOOLING
À utiliser seulement pendant la phase de diffusion en ligne / production : DDoS/WAF, rate limiting, bot protection, logs/observability.
Ne pas activer maintenant.


## MULTI-AGENT
Un seul agent écrit dans le worktree.
Les reviewers/subagents restent READ-ONLY.
Aucun second agent ne modifie les mêmes fichiers en parallèle.


## IMAGE GENERATION
Règle dure Cortezia : 1 prompt = 1 génération indépendante = 1 fichier image individuel.
Jamais planche, grille, mosaïque ou collage sauf demande explicite.
Codex intègre les assets validés ; il n’invente pas de nouvel asset artistique si la mission ne le demande pas.
Les références servent de langage visuel, pas de faux layout runtime.
Les médias/textes/prix restent dynamiques.
Workflow : PROMPT → GÉNÉRATION IMAGE DÉDIÉE → CONTRÔLE VISUEL → VALIDATION → NOMMAGE → INTÉGRATION CODEX → BROWSER QA.


## RÉPONSE OPTIMALE / CONVERGENCE
Le « plugin d’optimisation de réponse » n’est pas traité comme un plugin installé tant qu’il n’est pas réellement observé.
Le comportement attendu est le protocole universel déjà canonisé : INTENTION → SOLUTION → CRITIQUE → VÉRIFICATION → AMÉLIORATION → FINAL GATE.


## BONNES PRATIQUES CODEX
Les recommandations officielles OpenAI convergent vers :
- tâches bien délimitées ;
- prompts structurés comme une issue technique ;
- chemins de fichiers / composants / références quand pertinents ;
- AGENTS.md court comme carte, pas encyclopédie ;
- documentation structurée comme système de référence ;
- plans/decisions/handoffs persistants ;
- feedback loops et validations réelles ;
- skills pour les workflows répétables.


Sources :
https://openai.com/business/guides-and-resources/how-openai-uses-codex/
https://openai.com/index/harness-engineering/
https://openai.com/academy/skills/


## CONNEXIONS DISTANTES
LOCAL FIRST : ne pas connecter en écriture GitHub, Vercel, Supabase distant, Bunny, CCBill, Yoti ou production pour une mission qui n’en a pas besoin.
Quand une phase distante devient nécessaire : AUDIT → PLAN → APPROBATION → ACCÈS MINIMUM → EXÉCUTION → PREUVE
## PLUGINS / APPS — STATUT OBSERVÉ DANS CET ENVIRONNEMENT
- Google Drive : CONNECTED_USED — lecture, organisation, création et mise à jour du corpus de continuité.
- Supabase : TOOL_SURFACE_AVAILABLE — à utiliser seulement quand une tâche Supabase réelle l’exige ; état de connexion distante non déduit de cette disponibilité.
- Vercel : TOOL_SURFACE_AVAILABLE — à réserver à la phase déploiement/observabilité/firewall lorsque validée.
- GitHub : TOOL_SURFACE_AVAILABLE — aucune écriture/synchronisation pendant LOCAL FIRST sans ordre explicite.
- Figma : TOOL_SURFACE_AVAILABLE — optionnel si une mission design-to-code Figma réelle le justifie ; ne pas imposer au workflow visuel existant.
- Image generation : capacité native distincte d’un plugin ; à utiliser pour créer les assets demandés, un fichier indépendant par génération.


## POLITIQUE D’INSTALLATION
Ne jamais « installer tous les plugins ».
Ordre : outils déjà présents → capacité native → skill/plugin existant → rechercher une extension seulement si une capacité indispensable manque.
Avant installation : auteur/source, permissions, portée, maintenance, risque, credential, coût et side effects.
Tout plugin demandant accès distant sensible ou coût reste sous approbation utilisateur.


## GITHUB DE CONTINUITÉ — EXCEPTION AUTORISÉE
Statut : ACTIVE / EXPLICIT_DECISION — 2026-09-03
Repository : mrperezthomas-boop/CORTEZIA-CONTINUIT-CANONIQUE-PRIV-E.
Rôle : miroir machine/versionné du Drive canonique et source de contexte pour Codex.
Ce repository n’est jamais le repository du site.
L’écriture GitHub est autorisée pour maintenir CE dépôt de continuité. La règle LOCAL FIRST et l’interdiction de push par initiative continuent de s’appliquer au vrai projet du site.
Codex doit lire AGENTS.md puis les documents ciblés ; il ne doit pas traiter ce repo comme worktree applicatif.




## MICRO-PACK SCREEN WORKFLOW — ACTIVE 2026-09-03
Pour une mission visuelle écran :
- ne pas donner à Codex les 150 JSON ni tous les assets ;
- fournir TARGET + SCREEN.json + PROMPT court + uniquement les assets/brand nécessaires ;
- garder un CORTEZIA_CODEX_MAP avec les vrais chemins déjà découverts ;
- ne pas refaire l'exploration des composants connus ;
- ne pas ouvrir Drive/GitHub pendant l'exécution locale ;
- ne pas lancer audit global, build global ou toute la suite Playwright à chaque écran ;
- utiliser lint/typecheck/tests fonctionnels ciblés et capture de la page ;
- faire les validations globales après un groupe significatif d'écrans ou avant validation finale ;
- OUTPUT_MODE=MINIMAL ; aucune narration d'exploration.


Exemple de chemins actuellement source-backed par le handoff Gate :
- components/legal/AgeGate.tsx
- app/styles/cortezia-visual-mission-001-040.css
- public/assets/cortezia-visual/
- public/assets/cortezia-gate-01/
Ces chemins doivent être réutilisés sans recherche tant que le worktree concerné n'a pas matériellement changé ; leur état exact reste à revalider si nécessaire.
.