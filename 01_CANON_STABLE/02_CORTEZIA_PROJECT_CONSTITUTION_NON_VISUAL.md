# CORTEZIA — PROJECT CONSTITUTION NON VISUAL
Statut : ACTIVE / STABLE
Portée : produit, business, architecture, sécurité, données, workflow. Le visuel est volontairement exclu.


## 1. SOURCE DE VÉRITÉ ET MODE DE TRAVAIL
Cortezia est actuellement LOCAL FIRST.
Le dossier local réellement travaillé est la référence opérationnelle principale.
GitHub, anciens déploiements, anciens rapports et captures servent d’historique/comparaison et ne remplacent pas silencieusement le local.
Pas de push, pull, merge, reset, clean, publication ou synchronisation Git par initiative.


## 2. NATURE DU PRODUIT
Cortezia doit être un véritable service premium de diffusion de contenus pour adultes, exploitable au quotidien, pas une simple vitrine.
Le produit final n’est pas centré sur une créatrice/personnage. Les anciens concepts Ariana/créatrice centrale ne doivent pas être réintroduits comme vérité produit.


## 3. DESKTOP ET MOBILE
Desktop et mobile sont deux expériences de production à traiter réellement. Une capacité importante n’est pas DONE si l’un des deux formats principaux reste non traité.


## 4. DONNÉES ET CONTENUS
Les vidéos, photos, titres, séries, dates, prix, états, droits et données d’administration doivent rester dynamiques et provenir du runtime/admin réel.
Les anciens contenus de maquette sont des placeholders tant qu’ils ne sont pas validés.
Ne pas hardcoder une donnée fictive comme vérité produit.


## 5. DROITS VIDÉO
Toute vidéo publiée est un contenu réservé.
Voies d’accès actives établies :
- abonnement actif ;
- achat individuel PPV au tarif actif actuellement établi à 3,99 € par vidéo publiée.
Inscription ≠ abonnement.
Un compte simplement inscrit ne reçoit pas d’accès média par cette seule inscription.
Une preview/hover/sheet/watch ne doit jamais augmenter le niveau de révélation ou d’accès du média sans entitlement réel supplémentaire.


## 6. ADMINISTRATION
Cortezia doit disposer d’un vrai back-office opérationnel.
L’admin doit pouvoir gérer réellement, selon le modèle existant : création, consultation, modification, suppression, classement et organisation des vidéos, photos et autres contenus administrables pertinents.
Une surface /admin/dev ou « Administration DEV / Simulation locale » ne constitue pas la preuve de ce back-office réel.
Les contrôles sensibles doivent être appliqués côté serveur.


## 7. ARCHITECTURE
Toujours auditer l’existant avant une modification importante.
Préserver l’architecture viable.
Préférence : delta minimal, adaptation, migration progressive, refonte ciblée, refonte totale uniquement si nécessité démontrée.
Ne pas inventer fichiers, routes, variables, dépendances, tables, services, clés ou fonctionnalités.


## 8. SÉCURITÉ
Pour auth, admin, paiement, upload, données personnelles, permissions et contenu sensible :
- contrôle serveur ;
- validation des entrées ;
- moindre privilège ;
- protection des secrets ;
- gestion d’erreurs adaptée ;
- preuve observable ;
- tests proportionnés au risque.
Une protection visible dans le code n’est pas automatiquement une protection effective.


## 9. SERVICES EXTERNES
Supabase, Bunny/CDN, paiement, Yoti/âge, SMTP/email, Vercel/hébergement et autres services doivent être audités sur leur état réel avant conclusion.
Distinguer CONFIGURÉ LOCAL / VÉRIFIÉ DISTANT / PARTIEL / MANQUANT / BLOQUÉ / UNKNOWN.
Aucun service payant, paiement, abonnement, boutique, contrat, dépense, migration distante importante ou publication production ne doit être activé sans validation utilisateur explicite.


## 10. SECRETS
Aucun token, mot de passe, clé API, cookie de session, secret ou credential ne doit entrer dans les Sources/Drive de continuité.


## 11. CONFORMITÉ ADULTE
Avant mise en production, les obligations actuelles applicables à la vérification d’âge et à l’accès des mineurs doivent être revérifiées à partir de sources officielles actuelles.
Ne pas figer une ancienne interprétation juridique comme vérité permanente.


## 12. OUTILS DE DÉVELOPPEMENT TEMPORAIRES
Les tunnels, outils réseau, diagnostics ou utilitaires qui ne doivent pas être livrés avec Cortezia restent hors du dossier source du site lorsque possible.


## 13. SCOPE ET CORRECTIONS
Une capture, une page ou un bug précis est un cas témoin sauf restriction explicite.
Si le défaut appartient à une classe générale : inventorier les occurrences, corriger la source commune, traiter les variantes et valider plusieurs surfaces représentatives.


## 14. APPROBATION
Workflow par défaut pour un agent de code :
AUDIT / LECTURE → CONVERGENCE → RÉSUMÉ COURT D’INTERVENTION → APPROBATION UTILISATEUR → EXÉCUTION → VALIDATION → HANDOFF.
La convergence et la généralisation du scope ne valent pas autorisation d’écrire
## 15. BUSINESS / ACCÈS — DÉCISIONS ACTIVES
- Un seul abonnement : 14,99 €.
- Aucun autre plan d’abonnement et aucune autre offre d’abonnement.
- PPV : 3,99 € par vidéo publiée.
- Les favoris sont réservés aux abonnés actifs.
- Inscription seule ≠ abonnement ≠ droit média.


## 16. VÉRIFICATION D’ÂGE — SAFE SHELL
Avant preuve d’âge valide, Cortezia peut présenter uniquement une interface explicitement non pornographique et SAFE.
Le clic « +18 » est un avertissement/déclaration, jamais une preuve d’âge.
Tout contenu potentiellement pornographique doit être bloqué côté serveur avant rendu, préchargement ou délivrance d’URL.
Le provider final reste OPEN jusqu’à audit contre le référentiel Arcom/CNIL ; au moins une solution double-anonymat doit être prévue.
Voir 01_CANON_STABLE / 03_BACKEND_SECURITY_INVARIANTS et 04_EVIDENCE_AND_AUDITS / 01_AGE_COMPLIANCE.


## 17. PAIEMENTS
CCBill est la direction provisoire principale pour le paiement adulte par carte, sans activation implicite.
Stripe Payments est exclu au regard de sa politique actuelle sur les contenus adultes.
Segpay est une alternative à comparer avant décision finale.
La sélection finale du prestataire et tout contrat restent soumis à approbation utilisateur.


## 18. ENVIRONNEMENTS
local_real, local_simulator et admin_local sont trois contextes distincts et ne doivent jamais être confondus.
Le simulateur reste fail-closed, DEV-only, loopback et flag explicite.
Le vrai admin local doit être audité comme back-office réel, indépendamment de /admin/dev.


## 19. AUDIO
L’audio d’ambiance continue sur les surfaces watch/paywall/locked/pre-play tant qu’aucune lecture réelle n’a commencé. Il se coupe uniquement sur le vrai événement play et reprend lorsque la lecture s’arrête


## 20. CONTINUITÉ — DRIVE UNIQUE
Décision active : le Google Drive Cortezia est la source de continuité documentaire active.
Les nouvelles décisions, recherches, états, preuves et handoffs doivent être écrits directement dans les documents Drive correspondant à leur rôle.
Ne pas générer de ZIP, Master Source, pack de remplacement ou série de fichiers à faire gérer par l’utilisateur sauf demande explicite de sa part.
Ne pas demander à l’utilisateur de réimporter manuellement des fichiers pour maintenir la continuité courante.
Les anciens ZIP/Master restent au mieux des archives historiques et ne font plus partie du workflow normal.
La racine canonique privée active est : https://drive.google.com/drive/folders/1YcfsCYsYq5XDRnSYn98-ljlDWRLay4TA


## CONTINUITÉ DOCUMENTAIRE DUALE
Statut : ACTIVE / EXPLICIT_DECISION — 2026-09-03
Deux miroirs documentaires sont maintenus : le Drive canonique privé et le dépôt GitHub de continuité mrperezthomas-boop/CORTEZIA-CONTINUIT-CANONIQUE-PRIV-E.
Ils doivent rester sémantiquement synchronisés. Le GitHub de continuité est strictement séparé du futur dépôt du site.
LOCAL FIRST continue de gouverner le développement du vrai site ; l’autorisation d’écrire dans le dépôt GitHub de continuité n’autorise aucun push/sync sur un futur dépôt du site.


## GATE VISUEL DES ASSETS
Un asset REGENERATE reste conservé et traçable. Une nouvelle version ne peut devenir PASS qu’après validation réelle de la correction demandée ET validation de sa forme/silhouette artistique pour le job.
.