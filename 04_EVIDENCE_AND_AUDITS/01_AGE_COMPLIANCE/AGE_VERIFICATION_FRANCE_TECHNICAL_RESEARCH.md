# CORTEZIA — AGE VERIFICATION FRANCE
Statut : CURRENT_RESEARCH / SOURCE_BACKED
Portée : architecture produit et backend. Ceci est une recherche de conformité technique, pas un avis juridique définitif.


## CONCLUSION OPÉRATIONNELLE
Le clic « +18 » peut servir d’avertissement / déclaration d’intention, mais NE CONSTITUE PAS une vérification d’âge suffisante.
La loi française impose qu’aucun contenu à caractère pornographique ne soit affiché tant que l’âge n’a pas été vérifié.


La stratégie Cortezia retenue est donc :
1. visiteur non vérifié → SAFE SHELL uniquement ;
2. aucun contenu pornographique rendu, téléchargé, préchargé ou exposé par URL ;
3. vérification d’âge conforme via tiers indépendant ;
4. seulement après preuve valide → accès aux surfaces adultes, sous réserve des droits produit ;
5. l’entitlement commercial reste séparé : abonnement actif OU achat PPV.


## SAFE SHELL — DESIGN CONSERVATEUR
Avant vérification d’âge, autoriser uniquement des surfaces non pornographiques et explicitement sûres : branding général, navigation non explicite, pages légales/confidentialité/aide, création de compte/connexion, explication du service, placeholders neutres et informations commerciales formulées sans contenu pornographique.
Si une miniature, un titre, une description, un poster, une preview ou une métadonnée peut être pornographique/explicite, NE PAS la rendre avant vérification.
Le statut SAFE doit être décidé côté serveur / données, pas obtenu par simple blur CSS.


## INVARIANT BACKEND
Aucun asset pornographique ne doit être envoyé au client avant preuve d’âge valide :
- aucune miniature adulte ;
- aucun poster adulte ;
- aucune URL Bunny/CDN privée ;
- aucun token signé média ;
- aucune preview sensible ;
- aucun HTML contenant un média adulte simplement masqué ;
- aucune API ne retourne des données sensibles uniquement parce que le frontend est censé les cacher.


## PREUVE D’ÂGE
Le site ne doit pas collecter lui-même l’identité, la date de naissance ou les documents utilisés par la solution de vérification.
Le prestataire doit être juridiquement et techniquement indépendant du service pornographique.
Le service doit proposer au moins une solution répondant au principe de « double anonymat » selon le référentiel Arcom.
Pour ce niveau de protection, le référentiel attend aussi au moins deux méthodes de génération de preuve d’âge et une disponibilité pour au moins 80 % de la population majeure résidant en France.


## DURÉE / SESSION
Le référentiel Arcom indique qu’une nouvelle vérification est attendue après interruption de consultation / nouvel accès.
Il considère notamment que la validité doit s’interrompre à la fin de session, à la fermeture du navigateur, à la mise en veille du système et au plus tard après une heure d’inactivité.
Il est attendu que la preuve d’âge ne soit pas conservée dans le compte utilisateur du service.


Architecture recommandée :
- assertion opaque et éphémère de majorité pour la session ;
- aucun document d’identité dans Cortezia ;
- aucune donnée biométrique brute dans Cortezia ;
- aucune preuve durable attachée au profil utilisateur ;
- invalidation fail-closed.


## +18 BUTTON
Le bouton « +18 » : informe, peut accepter les conditions d’entrée dans le SAFE SHELL, n’accorde aucun droit adulte, ne remplace jamais le provider de vérification et n’ouvre jamais une URL média adulte.


## RELATION ÂGE / ABONNEMENT / PPV
AGE = non_verified | verified_for_current_session
ENTITLEMENT = none | subscription_active | ppv_owned(asset)
ADMIN = no | authorized


Pour obtenir un média sensible : AGE == verified_for_current_session ET (subscription_active OU ppv_owned(asset)).
L’inscription seule ne donne aucun accès média.


## PROVIDER
Aucun provider n’est déclaré conforme uniquement sur son marketing.
Le fournisseur final doit être audité contre le référentiel Arcom, les exigences CNIL, le double anonymat, l’indépendance, les méthodes couvertes, la disponibilité France, l’intégration serveur, le coût, le contrat, la conservation des données et l’auditabilité.
Yoti reste un CANDIDAT à évaluer, pas un provider « validé par l’Arcom » dans ce corpus.


## SOURCES PRIMAIRES
Légifrance — LCEN, article 10 : https://www.legifrance.gouv.fr/loda/article_lc/LEGIARTI000006421554/2025-06-10
Arcom — Référentiel technique : https://www.arcom.fr/se-documenter/espace-juridique/textes-juridiques/referentiel-technique-sur-la-verification-de-lage-pour-la-protection-des-mineurs-contre-la-pornographie-en-ligne
CNIL — Avis sur le référentiel Arcom : https://cnil.fr/fr/verification-de-lage-en-ligne-la-cnil-rend-son-avis-sur-le-referentiel-de-larcom
CNIL — Vérification de l’âge et vie privée : https://www.cnil.fr/fr/verification-de-lage-en-ligne-trouver-lequilibre-entre-protection-des-mineurs-et-respect-de-la-vie


## STATUT
SAFE_SHELL_ARCHITECTURE = RECOMMENDED / SOURCE_BACKED
SIMPLE_18_DECLARATION_AS_VERIFICATION = REJECTED
FINAL_PROVIDER = OPEN
FINAL_LEGAL_SIGNOFF = OPEN