# CORTEZIA — HANDOFF CURRENT
Statut : ACTIVE
## OBJECTIF
Permettre à une nouvelle conversation ou un nouvel agent de reprendre Cortezia sans dépendre d’un ancien chat et sans refaire les audits déjà établis.
## ROUTAGE STANDARD
00_START_HERE / 00_READ_ME_FIRST
→ 01_CANON_STABLE / 01_UNIVERSAL_WORKING_RULES
→ 01_CANON_STABLE / 02_CORTEZIA_PROJECT_CONSTITUTION_NON_VISUAL
→ 02_CURRENT_STATE / CURRENT_STATE_NON_VISUAL
→ sources ciblées seulement si nécessaire.
Pour une mission visuelle :
ajouter 06_VISUAL_SEPARATE / README — VISUAL IS SEPARATE.
## ÉTAT VISUEL DE REPRISE LE PLUS RÉCENT
Un audit visuel local complet vient d’être livré et documenté dans 06_VISUAL_SEPARATE.
Statut : PARTIAL / AUDIT_COMPLETE / USER_VALIDATED=false.
Couverture :
- 75 routes documentées ;
- 67 rendues ;
- 8 dynamiques BLOCKED faute de fixture ;
- 450/450 cellules d’états ;
- 184 captures full-page : 92 desktop + 92 mobile ;
- 0 erreur navigation/capture/page ;
- 0 origine externe pendant les captures ;
- worktree inchangé pendant l’audit.
Priorités visuelles :
1. /recherche cassée desktop/mobile ;
2. collisions cookies + navigation basse mobile ;
3. overflows /notifications, /nouveautes, /boutique/commandes ;
4. cibles <44×44 et labels accessibles ;
5. pages secondaires trop génériques ;
6. vrai backoffice non prouvé.
NE PAS REFAIRE l’audit visuel total par défaut.
Reprendre depuis le document visuel actif et ne revalider que les surfaces devenues STALE après modification.
## PREUVE LOCALE ASSOCIÉE
Pack déclaré :
K:\Cortezia Studio\DOSSIER SITE OFFICIEL\CORTEZIA_AUDIT_VISUEL_TOTAL_LOCAL.zip
SHA-256 déclaré :
98693993315BD349BCD97E2C8726DC34CC911702266A43332C7AE86B18E402BA
## ÉTAT NON VISUEL / TECHNIQUE
Le Drive canonique reste LOCAL FIRST.
Pour toute tâche technique qui exige l’état exact du code, auditer uniquement le delta réel nécessaire ; ne pas déduire le runtime courant d’un ancien rapport.
Le bootstrap Drive non visuel reste séparé du visuel.
## GATE DE MODIFICATION
Lecture/audit/recherche : autorisés.
Avant mutation du projet : résumé court d’intervention puis approbation explicite, sauf instruction actuelle non ambiguë d’exécution directe.
Aucun commit/push/pull/merge/reset/déploiement par initiative.
## CONTINUITÉ
Le Drive canonique privé est la continuité documentaire active.
Ne pas demander à l’utilisateur de répéter les informations déjà présentes ici.
Ne produire un ZIP/export de continuité que s’il le demande explicitement.
## REPRISE ASSETS V10 — 2026-09-03
Ne pas recommencer les lots 01–04.
État : 16 PASS / 24 REGENERATE / 110 MISSING / 0 AMBIGUOUS / COMPLETE=false.
Prochain lot séquentiel : LOT_05, IDs 041–050, sauf réception prioritaire d’une correction.
Les versions REGENERATE restent conservées avec leur motif et la manière de les corriger.
PASS exige conformité au job + alpha/runtime corrects + absence de contenu baked interdit + validation de la vraie forme visuelle.
## CONTINUITÉ DUALE
Drive canonique privé + dépôt GitHub de continuité doivent rester synchronisés.
GitHub continuité : mrperezthomas-boop/CORTEZIA-CONTINUIT-CANONIQUE-PRIV-E.
Ce dépôt est une mémoire/documentation de travail, jamais le dépôt du site de diffusion. Le futur dépôt du site sera traité séparément sur ordre explicite.
## ÉCRANS / CODEX — REPRISE 2026-09-03
Cibles disponibles : SCREEN_01 à SCREEN_06.
SCREEN_01_GATE a un micro-pack complet.
État Codex rapporté pour SCREEN_01 :
- snapshot créé : K:\Cortezia Studio\DOSSIER SITE OFFICIEL\implémentation de direction artistique\PRECHANGE_SNAPSHOT\CORTEZIA_GATE_01_20260903_082242
- assets 001 / 031 / 036 déjà vérifiés sous public/assets/cortezia-visual/
- branding ajouté sous public/assets/cortezia-gate-01/
- aucune modification AgeGate.tsx/CSS finalisée au moment du blocage
- fichiers ciblés connus : components/legal/AgeGate.tsx et app/styles/cortezia-visual-mission-001-040.css
- reprise : ne pas réauditer, ne pas recréer snapshot, reprendre le delta déjà audité.
Ce statut provient du compte-rendu Codex fourni par l'utilisateur ; il n'a pas été revalidé directement contre le worktree dans cette conversation.
Workflow actif :
un écran → micro-pack minimal → fichiers runtime ciblés → implémentation → capture → correction visuelle → tests ciblés → STOP.
Drive/GitHub restent la mémoire complète mais ne doivent pas être relus par Codex pendant l'exécution d'un micro-pack autonome.
## REPRISE BIBLE — 2026-09-03
Pour comprendre Cortezia sans relire les conversations, lire en priorité 01_CANON_STABLE / 04_BIBLE / CORTEZIA_BIBLE.md (et JSON pour agent).
Règle d’entrée : Basic Gate +18 → accueil SAFE ; vérification officielle séparée.
Exigence ouverte : éditeur visuel dans le vrai admin. Puck est recommandé, pas encore implémenté.
Pour les écrans Codex/Claude : conserver le mode un écran = un micro-pack ; ne pas faire de ré-audit global.
## HANDOFF PUCK ADMIN — 2026-09-03
Décision active : Puck sélectionné, non encore implémenté.
Pack prêt dans 07_HANDOFFS : CORTEZIA_PUCK_ADMIN.zip.
Codex doit lire PROMPT_CODEX.txt seulement et exécuter de façon ciblée : /admin/design + homepage pilote, auth réelle réutilisée ou bootstrap local, persistance, permissions et tests ciblés. Aucun audit global/Drive/GitHub.
.