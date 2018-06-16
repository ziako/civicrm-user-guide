Processeurs de paiement
==================

CiviCRM se connecte à une variété de processeurs de paiement différents.

CiviCRM prend en charge environ 15 processeurs de paiement prêts à l'emploi. La communauté des utilisateurs a contribué à l'utilisation de nombreux autres processeurs qui peuvent être téléchargés depuis le répertoire des extensions de CiviCRM.org:

[http://civicrm.org/extensions](http://civicrm.org/extensions "CiviCRM.org Extensions Directory")

Des processeurs de paiement supplémentaires peuvent également être disponibles sur des sites tiers.

CiviCRM ne prend pas en charge les processeurs developpés par la communauté, mais il n'y a aucune raison pour qu'ils ne soient pas aussi fiables que les processeurs prêts à l'emploi. Si vous utilisez un processeur fourni par la communauté, assurez-vous d'avoir accès à une assistance technique adéquate pour ce processeur, soit en interne, auprès de l'auteur du processeur de paiement, soit auprès d'un tiers de confiance.

Vous pouvez comparer ici les nombreux processeurs de paiement disponibles sur : 
[http://wiki.civicrm.org/confluence/display/CRMDOC/Payment+Processors](http://wiki.civicrm.org/confluence/display/CRMDOC/Payment+Processors%20)

Choisir un processeur de paiement   
-----------------------------

Voici une liste de différentes options à considérer lors du choix d'un processeur de paiement. 
Tous les fournisseurs de paiement ne sont pas égaux et il existe des différences significatives entre eux en termes de coût, d'adéquation à votre cas d'utilisation et de disponibilité. Ceci est un guide rapide pour sélectionner un processeur de paiement. Si possible, vous devez en parler à d'autres organisations similaires et proches qui utilisent CiviCRM pour qu'ils vous fassent part de leurs expériences avec les processeurs de paiement. Vous pouvez également configurer plusieurs processeurs de paiement et donner aux utilisateurs interne la possibilité de choisir celui qu'ils préfèrent.


### Processeurs sur site ou externe?

Les processeurs de paiement peuvent être divisés en deux catégories: ceux dans lesquels l'utilisateur entre directement les coordonnées de sa carte de crédit et ceux qui transfèrent l'utilisateur vers un autre site pour effectuer le paiement, puis les retournent sur votre site une fois le paiement effectué. Vous pouvez généralement -dans une certaine mesure -ajouter le nom, le logo et les couleurs de votre organisation, mais le flux de travail est moins homogène et un pourcentage de personnes a tendance à s'y perdre et ne terminent pas l'opération de paiement.

En plus de proposer plus de transparence pour les utilisateurs finaux, les processeurs de paiement sur site permettent aux administrateurs de sites de traiter les paiements par carte (contributions, frais d'adhésion, paiements d'événements, etc.) depuis les pages d'administration de CiviCRM.

L'inconvénient du traitement des paiements directement depuis votre site est que vous aurez besoin d'un certificat SSL pour assurer la sécurité des données de la carte de l'utilisateur telles qu'elles sont transmises sur Internet. Les certificats SSL sont payants (généralement des frais annuels) et ne sont pas simples à configurer. Votre fournisseur d'hébergement ou votre administrateur système peut vous y aider. Vous pouvez également lire le chapitre sur la sécurité dans la section de configuration initiale de ce livre.

**!!! Note** : Il convient de noter à ce stade que CiviCRM ne stocke jamais les détails de la carte de crédit sur votre serveur. Il les transmet uniquement au processeur de paiement.


### Disponibilité régionale  Regional Availability

Dans de nombreux pays, il n'y a pas de processeurs de paiement développés qui soutiennent leur devise. Si vous n'avez pas de support de processeur pour le processeur de paiement que vous souhaitez utiliser, envisagez d'écrire votre propre processeur ou demandez à un tiers de le faire.


### Compte marchand 

La plupart des organisations qui acceptent les paiements par carte de crédit ont leur propre compte marchand par l'intermédiaire  d'une banque, mais elles ont généralement des frais mensuels qui peuvent ne pas convenir aux petites organisations (bien qu'elles aient généralement des paiements en pourcentage inférieurs). Vous pouvez vous attendre à payer des frais pour le compte marchand et le processeur de paiement, bien que ceux-ci puissent être regroupés. Certains, comme World Pay & Paypal, ne nécessitent pas de comptes marchands distincts.


### Soutien aux contributions récurrentes  Support for recurring contributions

La prise en charge des contributions récurrentes et des adhésions à renouvellement automatique est une fonctionnalité importante pour de nombreuses organisations. Cependant, tous les processeurs de paiement disponibles pour CiviCRM ne prennent pas en charge cette fonctionnalité, et certains comme Moneris ont un support "incomplet". Vérifiez le wiki pour les dernières informations.


### Coût d'un processeur de paiement

Déterminer quel processeur de paiement est le moins cher dépend du nombre et de la taille moyenne des transactions que vous traitez. La question n'est donc pas de savoir quel processeur est le moins cher, mais lequel est le moins cher pour vous. Les pourcentages de commissions, les frais par transaction et les frais mensuels fixes varient en fonction des coûts d'installation. En général, si vous traitez de nombreuses transactions, un compte avec des frais mensuels mais une faible commission pourrait être une bonne option. D'un autre côté, si vous prévoyez des transactions peu fréquentes, il est préférable d'éviter les frais mensuels et d'accepter de payer une commission plus élevée.


### Facilité d'utilisation 

Si vous ne collectez pas vous-même les informations de carte de crédit sur votre site, vous devez déterminer si le flux de paiement est intuitif et facile à utiliser. Paypal Standard est souvent déroutant pour les utilisateurs finaux parce qu'ils hésitent de créer ou pas un compte PayPal.
Une telle barrière peut entraîner une diminution des contributions.

Support
-------

CiviCRM prend en charge les processeurs qui sont incorporés dans le coeur du code principal, dans la mesure où ils garantissent leur continuité lors de mise à niveau. Le support et les améliorations des processeurs communautaires sont généralement attendus de la communauté.

Installation
-------

Vous pouvez configurer un ou plusieurs processeurs de paiement dans votre installation CiviCRM.

Vous devrez affecter un processeur de paiement actif à chaque page de contribution en ligne et à chaque événement payé. Si aucun processeur de paiement n'a été configuré pour votre site.

You will then need to assign an active Payment Processor to each Online Contribution Page and each paid Event. If no Payment Processors have been configured for your site,

1. Allez à **Administrer> Paramètres système> Processus de paiement** et cliquez sur **Nouveau processeur de paiement**.
2. Choisissez le type de processeur de paiement dans la liste déroulante.
3. Attribuez un nom descriptif à cette configuration de processeur et une description facultative. Ce nom apparaîtra lorsque vous souhaitez sélectionner un processeur de paiement pour une page de contribution ou un événement. Une description peut être utile si vous configurez plusieurs comptes marchands pour différents chapitres ou sous-organisations de votre site avec le même type de processeur de paiement.
4. Sélectionnez un compte financier. Si vous souhaiter avoir un compte financier distinct pour chaque processeur de paiement votre comptable sera en mesure de vous conseiller au mieux à ce sujet. Le montant versé est enregistré sur le compte financier sélectionné mais pas le type de revenu que vous recevez. La contribution, l'adhésion et le prix d'un événement que vous recevez seront également enregistrés dans différents comptes financiers de recette, en fonction de la configuration des pages de contribution et des événements. Pour une explication partielle de la façon dont cela fonctionne, voir "compte à double Entrées" dans Wikipedia.
5. Activez le processeur afin qu'il soit disponible pour les événements payants et les pages de contribution en ligne. Si le processeur vous permet de collecter des informations de carte de crédit sur votre site Web, votre personnel pourra également l'utiliser pour enregistrer des contributions par carte de crédit et le paiement des adhésions et des événements.
6. Si vous avez plusieurs processeurs de paiement, celui que vous définissez par défaut est sélectionné lorsque vous créez une page de contribution ou d'événement ou un paiement par carte de crédit dans la zone d'administration, mais vous pouvez remplacer cette sélection manuellement.
7. Remplissez le paiement en direct approprié et testez les détails de paiement de votre processeur. Notez que les champs de ces sections varient en fonction du type de processeur de paiement sélectionné.

Vous aurez sans doute besoin de faire quelques réglages supplémentaires sur la passerelle de paiement, mais cela dépasse le cadre de ce livre et devrait être documenté par votre passerelle.

Une fois terminé, le processeur sera disponible dans vos pages payantes et contributions.

Tester les paiements et les processeurs de paiement fictifs 
-----------------------------------------------

Pour les tests, vous pouvez configurer des processeurs de paiement factices.

Si vous utilisez un processeur de paiement factice ou si vous utilisez des pages de paiement en mode test, les détails de carte suivants devraient fonctionner:

-   Type de Carte: Visa
-   Numéro de carte :  4111 1111 1111 1111
-   Cryptogramme: trois chiffres
-   Date d'expiration:  n'importe quelle date dans le futur

Ecrire un nouveau processeur de paiement
--------------------------------

Si vous ne trouvez pas de processeur de paiement vous convenant ou si vous souhaitez utiliser un fournisseur de paiement spécifique actuellement non pris en charge par CiviCRM, vous pouvez écrire une nouvelle intégration de processeur de paiement ou payer quelqu'un d'autre pour le faire.
