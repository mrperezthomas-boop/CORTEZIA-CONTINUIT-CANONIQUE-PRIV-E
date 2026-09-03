# EVIDENCE INDEX
Statut : ACTIVE


## RÈGLE
Chaque preuve doit préciser :
- objet vérifié ;
- source/outil ;
- état ou version concernée ;
- résultat ;
- fraîcheur ;
- statut PASS / FAIL / STALE / HISTORICAL.


Une preuve appartient à l’état exact audité. Après modification pertinente, elle devient STALE pour les surfaces affectées.


## PREUVES DE STRUCTURATION DU DRIVE
- Le Drive canonique privé a été structuré par rôle : START_HERE, CANON_STABLE, CURRENT_STATE, DECISIONS, EVIDENCE_AND_AUDITS, OPEN_AND_UNCERTAIN, VISUAL_SEPARATE, HANDOFFS, ARCHIVE_SUPERSEDED, INBOX_RAW.
- Les règles universelles, le canon Cortezia non visuel et les recherches spécialisées actives sont séparés.
- La racine canonique privée a été vérifiée comme espace de continuité actif.


## PREUVES SPÉCIALISÉES ACTIVES
- Âge France : recherches officielles Légifrance / Arcom / CNIL.
- Paiements : recherches provider avec distinction politique/compatibilité ; à revalider avant contrat/production.
- Codex/tooling : workflow et skills documentés ; à revalider selon environnement réel.


## PREUVE VISUELLE LOCALE — AUDIT TOTAL
Objet :
état visuel du site Cortezia local sur l’état exact audité.


Source :
CORTEZIA_AUDIT_VISUEL_TOTAL_LOCAL.zip, produit par audit navigateur/runtime non destructif.


Résultats déclarés et repris dans 06_VISUAL_SEPARATE :
- 75 routes inventoriées/documentées ;
- 67 routes rendues ;
- 8 routes dynamiques BLOCKED sans fixture réelle ;
- 450/450 cellules utilisateur ;
- 184 captures full-page : 92 desktop + 92 mobile ;
- 184 HTTP 200 ;
- 0 erreur navigation ;
- 0 erreur capture ;
- 0 erreur JavaScript page ;
- 0 origine externe contactée ;
- 5 captures avec overflow horizontal sur 3 routes ;
- 2 consoles avec le même 403 vidéo sans droit ;
- cibles <44×44 détectées dans 184/184 captures ;
- worktree inchangé du début à la fin.


Pack local déclaré :
K:\Cortezia Studio\DOSSIER SITE OFFICIEL\CORTEZIA_AUDIT_VISUEL_TOTAL_LOCAL.zip


Taille déclarée :
80 177 043 octets.


SHA-256 déclaré :
98693993315BD349BCD97E2C8726DC34CC911702266A43332C7AE86B18E402BA


Statut :
PASS pour la mission d’audit/documentation elle-même ;
PARTIAL pour l’état visuel du produit ;
BLOCKED pour 8 détails dynamiques sans fixture ;
USER_VALIDATED=false.


Fraîcheur :
preuve actuelle pour l’état audité. Si le local change, marquer STALE uniquement les surfaces impactées.


## IMPORTANT
Ne jamais utiliser cet index comme autorisation de correction.
Les corrections sont des missions séparées soumises au gate d’approbation.
.