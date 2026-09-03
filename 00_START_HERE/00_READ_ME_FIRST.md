# CORTEZIA — CONTINUITY ROUTER
Statut : ACTIVE
But : point d’entrée unique de continuité. Toute demande substantielle liée à Cortezia doit commencer ici, puis charger uniquement les sources utiles.


## RÈGLE DE LECTURE
Ne pas relire tout le Drive à chaque demande.


Ordre par défaut :
1. ce document ;
2. 01_CANON_STABLE / 01_UNIVERSAL_WORKING_RULES ;
3. 01_CANON_STABLE / 02_CORTEZIA_PROJECT_CONSTITUTION_NON_VISUAL ;
4. 02_CURRENT_STATE / CURRENT_STATE_NON_VISUAL ;
5. 03_DECISIONS / DECISIONS_LOG_NON_VISUAL seulement si l’origine ou l’historique d’une décision est utile ;
6. 05_OPEN_AND_UNCERTAIN si la tâche touche un point non confirmé ;
7. 04_EVIDENCE_AND_AUDITS seulement pour vérifier une affirmation, une version ou un résultat ;
8. 06_VISUAL_SEPARATE uniquement pour une mission visuelle.


## HIÉRARCHIE DE VÉRITÉ
1. consigne utilisateur actuelle, explicite, récente et précise ;
2. état local/runtime réellement observé sur le projet concerné ;
3. décisions explicites actives ;
4. canon stable du projet ;
5. état courant documenté, s’il est encore frais ;
6. preuves/audits liés à un état exact ;
7. historique et archives ;
8. inférence.


Une ancienne capture, un ancien audit, une ancienne maquette ou une ancienne conversation ne devient jamais une vérité actuelle sans vérification.


## RÈGLE DE CONTINUITÉ
Pour chaque demande :
- comprendre l’objectif réel ;
- consulter le minimum de contexte à haut signal ;
- rechercher le réel avant de demander à l’utilisateur ce qui peut être trouvé ;
- vérifier ce qui est vérifiable ;
- distinguer VERIFIED / SOURCE_BACKED / EXPLICIT_DECISION / INFERRED / UNKNOWN ;
- ne jamais présenter une preuve d’un ancien état comme preuve de l’état actuel ;
- mettre à jour uniquement le document canonique concerné lorsqu’une décision ou un état change ;
- ne pas dupliquer le même fait dans plusieurs fichiers si un lien/référence suffit.


## RÈGLE DE MODIFICATION
Lecture/audit/recherche : autorisés sans mutation.
Avant mutation du projet : résumé court d’intervention puis approbation explicite, sauf instruction actuelle non ambiguë d’exécution directe.
Une généralisation du scope n’est pas une autorisation d’élargir les side effects.


## RÈGLE D’ARCHIVE
Une décision remplacée n’est pas effacée : elle est marquée SUPERSEDED et conservée dans 08_ARCHIVE_SUPERSEDED ou dans le journal de décisions.
Une preuve obsolète reste historique mais ne sert plus à conclure sur l’état actuel.


## VISUEL
Le visuel est volontairement séparé. Rien dans 06_VISUAL_SEPARATE ne doit modifier silencieusement les règles produit, business, sécurité, droits, données ou architecture


## LIENS DIRECTS DU SYSTÈME
- Universal rules: https://docs.google.com/document/d/1EfooSUxSA7LeKFdy2AcB7xE29d2l3hKYFAcIq7SgAS4/edit
- Constitution non visuelle: https://docs.google.com/document/d/1Z5rlZPbdOb10uWNCcjcrNm6qX0QbUcJSFrQZrGKHkqk/edit
- Current State: https://docs.google.com/document/d/1_RSfLvoaH3e4UwHq21O17RTRj69PjxwFyosvuQVTwr8/edit
- Source Manifest: https://docs.google.com/document/d/1U7vuXUfGf7UDxtnF94unU5vFxPu2-htPjAmVoQylnug/edit
- Decisions Log: https://docs.google.com/document/d/19pk7cM4DhlrLrxoW5MmwzzayOFDPcXYh1Rlc2ExRGJk/edit
- Evidence Index: https://docs.google.com/document/d/1drmXaIP1o1Ud7xzvtQVxGJhUCYfoowSCxW84y6N7bD8/edit
- Open / Unverified: https://docs.google.com/document/d/1sv_6vitFCkxmPOhabpZFmyUVSMoq3eM6w14VXbdrabo/edit
- Current Handoff: https://docs.google.com/document/d/16jrY6jZdheZZXxdlSpMxyGpAThwj0sNEnbLU_UjyRQM/edit


## ROUTAGE SPÉCIALISÉ
- Backend / sécurité / droits / médias / admin → lire 01_CANON_STABLE / 03_BACKEND_SECURITY_INVARIANTS.
- Vérification d’âge France → lire 04_EVIDENCE_AND_AUDITS / 01_AGE_COMPLIANCE.
- Paiements / provider → lire 04_EVIDENCE_AND_AUDITS / 02_PAYMENTS.
- Codex / skills / plugins / tooling / génération d’images → lire 04_EVIDENCE_AND_AUDITS / 03_CODEX_TOOLING.


Racine canonique privée : https://drive.google.com/drive/folders/1YcfsCYsYq5XDRnSYn98-ljlDWRLay4TA


## RÈGLE DE CONTINUITÉ SIMPLIFIÉE
Le Drive canonique privé ET le dépôt GitHub de continuité sont les deux miroirs actifs de la continuité Cortezia.
Pour Cortezia, utiliser le Drive directement pour la continuité documentaire et maintenir en parallèle le dépôt GitHub de continuité. Le dépôt GitHub de continuité n’est jamais le dépôt du site.
Toute mise à jour durable va au document Drive correspondant ET au fichier miroir GitHub correspondant. Les deux doivent rester synchronisés au niveau sémantique.
Ne produire un export/ZIP que si l’utilisateur le demande explicitement..