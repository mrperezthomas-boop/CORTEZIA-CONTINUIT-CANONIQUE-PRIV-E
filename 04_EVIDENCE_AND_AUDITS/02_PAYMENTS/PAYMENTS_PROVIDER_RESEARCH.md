# CORTEZIA — PAYMENTS PROVIDER RESEARCH
Statut : CURRENT_RESEARCH / SOURCE_BACKED
Aucune activation de provider n’est autorisée par ce document.


## BUSINESS CANON
Un seul abonnement : 14,99 €.
Aucun autre plan d’abonnement.
Aucune autre offre d’abonnement.
PPV : 3,99 € par vidéo publiée.
Paiement souhaité : carte bancaire au minimum ; autres moyens uniquement s’ils sont réellement supportés et utiles.


## STRIPE
Statut : EXCLUDED_CURRENT_POLICY
La politique Stripe actuelle interdit explicitement la pornographie, les contenus adultes destinés à la gratification sexuelle, les services adultes et le pay-per-view adulte.
Conclusion : ne pas construire Cortezia autour de Stripe Payments en supposant qu’une approbation sera obtenue.
Sources :
https://stripe.com/legal/restricted-businesses
https://support.stripe.com/questions/prohibited-and-restricted-businesses-list-faqs


## CCBILL
Statut : PRIMARY_CANDIDATE / PROVISIONAL_BUSINESS_DIRECTION
CCBill publie explicitement une offre pour adult content, content platforms, streaming websites/apps, abonnements récurrents et achats ponctuels.
CCBill n’est pas gratuit.
Sa page de prix indique des coûts interchange / assessment / processor markup selon le modèle, plus des frais annuels de registration high-risk pour certains MCC.
La tarification exacte Cortezia doit être obtenue par devis/underwriting.
Sources :
https://ccbill.com/industries/adult-business
https://ccbill.com/industries/streaming-media
https://ccbill.com/pricing


## SEGPAY
Statut : EVALUATE_AS_ALTERNATIVE
Segpay se positionne explicitement sur les marchands high-risk, notamment Adult & Dating, Digital Content et Subscriptions.
À comparer avant décision finale : disponibilité France/UE, cartes, moyens locaux, récurrence, PPV, frais, réserve, chargebacks, payout, API/webhooks, support, conformité adulte et checkout.
Source : https://segpay.com/verticals/


## « GRATUIT »
Statut : NOT_REALISTIC_FOR_CARD_PROCESSING
Un prestataire de carte ne sera pas réellement gratuit : les coûts de réseau, acquisition, risque high-risk, chargebacks et processor markup existent.
Le choix doit optimiser le coût total sans sacrifier stabilité, conformité, taux d’acceptation, chargebacks, récurrence et sécurité.


## DÉCISION AVANT INTÉGRATION
1. obtenir les conditions commerciales CCBill ;
2. obtenir une proposition Segpay comparable ;
3. comparer coût total sur plusieurs scénarios de volume ;
4. comparer abonnement récurrent + PPV ;
5. vérifier conditions France/UE ;
6. choisir explicitement ;
7. seulement ensuite implémenter.


Aucun vrai paiement, contrat ou compte marchand ne doit être activé silencieusement.