# DRIVE STRUCTURE POLICY
Statut : ACTIVE


## OBJECTIF
Rendre la reprise de Cortezia rapide, fiable et peu coûteuse en contexte : un agent doit savoir où chercher sans parcourir tout le Drive.


## PRINCIPES
- Un point d’entrée unique : 00_START_HERE.
- Un canon stable unique : 01_CANON_STABLE.
- L’état volatil est séparé : 02_CURRENT_STATE.
- Les décisions ont un journal propre : 03_DECISIONS.
- Les preuves et audits ne gouvernent pas le projet : 04_EVIDENCE_AND_AUDITS.
- Les inconnues sont explicites : 05_OPEN_AND_UNCERTAIN.
- Le visuel est isolé : 06_VISUAL_SEPARATE.
- Les reprises sont compactes : 07_HANDOFFS.
- Les anciennes versions sont conservées mais sorties du chemin actif : 08_ARCHIVE_SUPERSEDED.
- Les apports non classés arrivent dans 09_INBOX_RAW avant tri.


## NOMMAGE
- noms courts, explicites, stables ;
- préfixes numériques pour l’ordre de lecture ;
- éviter FINAL_FINAL_V3 ;
- pour les documents actifs, préférer un même fichier avec historique de versions ;
- créer une nouvelle version logique seulement si le changement nécessite un état distinct et traçable.


## DUPLICATION
Une information canonique ne doit avoir qu’un seul original actif.
Si elle doit être visible ailleurs, utiliser un renvoi/raccourci plutôt qu’une copie divergente.


## ARCHIVE
Les anciens états, audits et décisions remplacées sont conservés pour l’historique, mais clairement marqués HISTORICAL / SUPERSEDED / OBSOLETE.


## SÉCURITÉ
Aucun secret, mot de passe, token, cookie, clé privée ou credential ne doit être stocké dans ce corpus de continuité.
Les permissions du dossier doivent être suffisamment restrictives pour qu’un tiers ne puisse pas modifier le canon.