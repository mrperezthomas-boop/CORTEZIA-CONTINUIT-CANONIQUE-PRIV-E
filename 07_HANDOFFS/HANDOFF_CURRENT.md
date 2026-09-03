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
.