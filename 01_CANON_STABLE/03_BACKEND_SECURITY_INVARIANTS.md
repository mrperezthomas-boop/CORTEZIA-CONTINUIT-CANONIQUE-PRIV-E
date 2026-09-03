# CORTEZIA — BACKEND SECURITY INVARIANTS
Statut : ACTIVE / STABLE
Portée : règles d’architecture obligatoires. Ne décrit pas l’état actuel du code tant qu’il n’a pas été audité.


## 1. BACKEND FIRST
Pour Cortezia, les règles d’accès ne sont jamais des effets visuels.
Le backend / serveur / stockage doit être la source d’autorité pour l’âge, l’auth, l’entitlement, l’admin, les médias privés, le paiement, les uploads et les permissions.
Blur, overlay, bouton caché, route client ou CSS ne constituent jamais un contrôle d’accès.


## 2. ÉTATS DISTINCTS
IDENTITY = guest | authenticated
AGE = non_verified | verified_current_session
ENTITLEMENT = none | subscription_active | ppv_owned(asset)
ADMIN = no | authorized | critical_authorized
ENV = local_real | local_simulator | production
Chaque décision d’accès utilise seulement les dimensions nécessaires.


## 3. MÉDIA ADULTE
Avant de délivrer un contenu sensible : âge vérifié pour la session courante ET abonnement actif OU achat PPV de cet asset.
Sans ces conditions : pas de signed URL, pas de token CDN, pas de thumbnail explicite, pas de preview explicite, pas de source vidéo, pas de téléchargement caché dans le DOM et pas de données sensibles dans une API.


## 4. SAFE SHELL
Avant âge vérifié : uniquement données/assets explicitement SAFE.
UNKNOWN = DENY.
Toute donnée pouvant être pornographique est exclue côté serveur.
Le bouton +18 n’accorde aucun accès média.


## 5. FAVORIS
Les favoris sont réservés aux abonnés actifs.
Cette règle doit être contrôlée côté serveur pour toute mutation/lecture concernée, pas seulement dans l’UI.


## 6. ADMIN
Un vrai admin doit authentifier, autoriser côté serveur, appliquer le moindre privilège, distinguer actions normales et critiques, valider inputs/uploads, journaliser les opérations sensibles sans secrets et protéger les endpoints indépendamment de l’UI.
/admin/dev ou simulation locale ≠ vrai admin.


## 7. LOCAL / SIMULATOR / ADMIN LOCAL
local_real : runtime local destiné à tester les vrais parcours pré-production selon la configuration locale.
local_simulator : faux états et bypass uniquement DEV, conditionnés par non-production + loopback + flag explicite ; aucun vrai paiement/provider âge ; fail-closed dès qu’une condition manque.
admin_local : vrai back-office local à auditer séparément, avec vraie auth admin locale et vraies opérations persistant dans la cible locale prévue.
Les cookies/state/flags du simulateur ne deviennent jamais une autorité production.


## 8. PAIEMENT
Le backend est autorité pour la création de session de paiement, le prix canonique, la validation webhook, l’idempotence, l’état transaction et l’activation/révocation entitlement.
Le client ne peut jamais s’auto-attribuer abonnement ou PPV.


## 9. SUPABASE
Si Supabase est la source de données : RLS sur toute table exposée ; policies selon le vrai modèle ; service_role/secret jamais navigateur ; metadata utilisateur éditable jamais autorité admin/entitlement ; storage policies cohérentes ; tests négatifs obligatoires.


## 10. UPLOAD / MÉDIA
À auditer/garantir : taille/type/MIME, quotas, nommage, stockage, scan/modération selon besoin, absence d’exécution, accès privé par défaut, URLs temporaires/signées si nécessaire, suppression cohérente et logs sans secret.


## 11. RATE LIMIT / ABUSE
À la production, auth, login/reset, callbacks âge, checkout/webhooks, APIs sensibles et admin doivent disposer de protections adaptées contre brute-force, abus et replay.
La couche plateforme/WAF complète l’application mais ne remplace pas les contrôles applicatifs.


## 12. TESTS NÉGATIFS
Tester au minimum : non authentifié ; non vérifié âge ; sans entitlement ; mauvais asset PPV ; non-admin ; admin sans niveau critique ; production avec flag simulateur ; requête non-loopback en simulateur ; webhook invalide/rejoué ; URL média expirée/forgée.


## 13. PREUVE
Une sécurité n’est DONE que si le comportement refusé est réellement testé sur l’état final exact.