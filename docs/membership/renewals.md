Les renouvellements de cotisations
===========================
Ce chapitre traite des différentes façons dont vos contacts peuvent renouveler leur adhésion. Ceci inclus les renouvellements automatiques, les renouvellements en ligne et les renouvellements manuels soit sur une base individuelle, soit par la mise à jour par lots des membres via le profil. Tout d'abord, nous présenterons les moyens de faire savoir à vos membres que leur adhésion devrait être renouvelée.


Les concepts de renouvellement 
-------------------------

Il existe une distinction importante entre l'ajout d'une nouvelle adhésion et le renouvellement d'une adhésion existante. Si quelqu'un s'approche de sa date de fin d'adhésion et veut continuer à être membre, dans la plupart des cas, vous voudrez renouveler l'adhésion existante en utilisant le processus de renouvellement de CiviMember plutôt que de créer une nouvelle adhésion.

Les membres ont trois dates principales. **Membre depuis**qui n'est pas modifié quand une adhésion est renouvelée. **Date de début** et **Date de fin** qui peut changer en fonction du statut d'adhésion en vigueur lorsque le renouvellement est traité.

- Si le renouvellement est traité lorsque le statut de membre a **Oui** dans la colonne **membre** sur **Administrateur> CiviMember> Règles de statut d'adhésion** alors la **Date de début** ne change pas et la date de fin est prolongée par la durée du renouvellement.
- Si le renouvellement est traité lorsque le statut de membre a **Non** dans la colonne **membre** sur **Administrateur> CiviMember> Règles de statut d'adhésion**, alors la **Date de début** est modifiée à la date actuelle et **la date de fin** est calculée à partir de la nouvelle date de début.

Le cas échéant, pour le type d'adhésion, une contribution (financière) est enregistrée dans le cadre du processus de renouvellement. Cela créera un enregistrement de contribution lié au dossier d'adhésion. Au fil du temps, et après quelques renouvellements, le dossier d'adhésion sera un enregistrement de membre unique dont la date de fin est prolongée, avec plusieurs transactions financières connexes représentant chaque cotisation de renouvellement.

### Choix d'une Adhésion

L'adhésion en ligne permet aux contacts de modifier le type d'adhésion dans le cadre du processus de renouvellement. Si un contact lié à une organisation renouvelle avec un autre type d'adhésion appartenant à la même organisation, l'adhésion existante sera changée par cet autre type d'adhésion ainsi que l'historique d'adhésion associé. La date de participation et les contributions seront conservés. La date de fin existante sera prolongée par la durée du nouveau type d'adhésion. Si ce n'est pas ce que vous voulez, vous devrez lier vos types d'adhésion à différentes organisations. (cela peut être une organisation fictive créée uniquement à cette fin et invisible à l'utilisateur. Voir le chapitre **Définition des membres** pour une explication plus détaillée.)

Si vous utilisez CiviCRM pour gérer des adhésions pour plusieurs organisations, notez que le type d'adhésion d'un contact ne peut pas être modifié par un type d'adhésion provenant d'une autre organisation

Rappels de renouvellement 
-----------------

Faire savoir à un membre que son adhésion est sur le point de finir est la première étape dans le processus de renouvellement. CiviCRM facilite les communications avec vos membres par courrier électronique ou par courrier postal.

### Rappel par courriel 

Un ou plusieurs courriels de rappel de renouvellement peuvent être envoyés automatiquement à l'aide de la fonction Rappels programmés (**Administration> Communications> Schedule Reminders**). Ceci est particulièrement utile quand les types d'adhésion, peuvent se terminer à tout moment au cours de l'année. Reportez-vous au chapitre [Rappels de renouvellements] (http://booki.flossmanuals.net/email/scheduled-reminders) dans la section *Email* de ce livre pour les étapes impliquées dans l'envoi d'un rappel planifié une fois que vous avez composé votre message .

Ce que vous devez dire dans vos e-mails de rappel dépendra du type d'adhésion en relation avec la date de fin d'adhésion. Par exemple, les rappels de renouvellement envoyés trois mois à l'avance aux personnes qui se sont inscrites au nom des organisations (pour leur donner suffisamment de temps pour préparer un bon de commande et le paiement par leur département comptable) doivent être différents de ceux envoyés une semaine après à un contact individuel 

Toutefois, si les membres peuvent renouveler en ligne, tous les rappels par courrier électronique de renouvellement doivent contenir dans le message un lien «spécial» Civimail : {contact.checksum}, (dans ce cas-ci vers la page de renouvellement de l'adhésion). Lorsqu'une personne clique sur le lien spécial, elle  remplira le formulaire de renouvellement avec toutes les données qui existent dans son dossier. Le lien spécial dure sept jours à compter du moment où il a été envoyé (bien que cela puisse être changé à **Administer> Paramètres du système> Divers (Undelete, PDF, Limits, Logging, Captcha, etc.)** Comme les pages d'adhésion sont un Type de pages de contribution, le lien {contact.checksum} à utiliser dans les e-mails de renouvellement où **N** est l'identifiant de votre page de renouvellementest :

-   Drupal:
    http://www.myorganization.org/civicrm/contribute/transact?reset=1&id=N&{contact.checksum}&cid={contact.contact_id}  
-   Joomla!:
    http://www.myorganization.org/index.php?option=com_civicrm&task=civicrm/contribute/transact&reset=1&id=N&{contact.checksum}&cid={contact.contact_id}
-   WordPress:
    http://www.myorganization.org/?page=CiviCRM&q=civicrm/contribute/transact&reset=1&id=N&{contact.checksum}&cid={contact.contact_id}
    
Comme pour tous les e-mails que vous envoyez, vous devez prévoir le temps de tester les modèles de rappel de renouvellement, surtout si vous avez des structures d'adhésion complexes et souhaitez personnaliser les messages en fonction des types de membres ou d'autres paramètres.

Rappelez-vous que, par défaut, des rappels planifiés seront envoyés à des personnes qui l'ont opté pour la plupart ou pour recevoir tous les emails, sauf si vous excluez spécifiquement ces personnes. Si les contacts peuvent choisir de renouveler automatiquement leur adhésion, vous devez exclure les membres qui ont choisi cette option à partir des rappels planifiés.

### Rappels postaux 

Vous pouvez également envoyer des lettres à tous les membres qui doivent renouveler ou simplement envoyer des lettres à ceux qui ne possèdent pas d'adresse électronique et à ceux qui ont opté pour un envoi de tous les courriels. Reportez-vous à *Communications par courrier postal* dans la section *Flux de travail communs* pour trouver les moyens de générer ces lettres.

Renouvellement automatique des adhésions
---------------------------------

Pour les membres qui ont choisi cette option lorsqu'ils ont adhérés pour la première fois, le paiement sera prélevé automatiquement à partir de leur carte de crédit préautorisée à leur date de renouvellement. Leur date de fin d'adhésion sera mise à jour et ils recevront les remerciements et les reçus appropriés de CiviCRM. (Voir *Définition d'adhésions* , *Adhésions en ligne inscrivez-vous* et *Entrée manuelle des adhésions* chapitre sur les détails de la mise en place des adhésions renouvelables automatiquement.)

Renouvellements en ligne
---------------
CiviCRM utilise la même page pour les nouvelles adhésions et les renouvellements. La seule différence est que le titre de la page et le message d'introduction sont le texte que vous avez entré dans les champs de renouvellement dans l'onglet adhésions lors de la configuration de votre page d'adhésion en ligne. La page de renouvellement s'affiche automatiquement à la même URL que la page de jointure de membre lorsqu'elle est vue par un visiteur du site qui possède une adhésion en cours valide ou expirée.

Lorsque vous configurez des pages d'adhésion, il convient de rappeler que les membres actuels ne verront que la page de renouvellement s'ils sont connectés. S'ils ne sont pas connectées, ils verront la page d'inscription. S'ils remplissent cette page et, en fonction de leurs informations de contact, CiviCRM peut trouver leur dossier de contact existant, puis leur adhésion sera renouvelée. Si CiviCRM ne peut pas trouver son enregistrement de contact existant (peut-être dû à un changement de leur adresse de courriel), un nouvel enregistrement de contact et une adhésion seront créés. Il s'agit d'une source de doublons dans votre base de données et vous devez minimiser les chances que cela se produise. Deux façons de le faire sont d'inclure toujours un jeton de somme de contrôle dans les courriels de rappel de renouvellement et d'ajouter du texte au message d'introduction du nouveau membre pour rappeler aux personnes qu'ils doivent se connecter avant de renouveler.

###  Page par défaut de Renouvellement d'Adhésion En ligne 

Lorsqu'une adhésion est souscrite à l'aide de la page d'inscription de l'adhésion en ligne (service en libre-service), le tableau de contact de cet utilisateur contiendra un lien "renouvelable" qui pointe vers cette page. Cependant, ce lien n'apparaîtra pas pour les membres dont l'adhésion initiale a été saisie manuellement, sauf si vous configurez une **page de renouvellement d'adhésion en ligne par défaut** comme suit:

1. Si cela n'existe pas, créez une page d'adhésion qui inclut toutes les adhésions actuellement disponibles. (Vous devrez peut-être utiliser un prix établi pour cela si les frais d'adhésion doivent être attribués à plus que sur le type financier. Reportez-vous à *Ensembles de prix* pour plus de détails.)

2. Accédez à **Administrer> CiviMember> Paramètres du composant CiviMember**
3. Pour la page Default Renouvellement d'adhésion en ligne, choisissez la page d'adhésion contenant tous vos types d'adhésion

Un lien "renouvelable" qui pointe vers cette page sera alors affiché dans le tableau de bord de contact pour toute adhésion qui a été introduite manuellement.

![image](../img/z_sprint14_renewalpage.png)

Renouvellement manuel d'une adhésion pour un seul contact
---------------------------------------------------

1. Accédez à la page récapitulative du contact.
2. Cliquez sur l'onglet **Adhésions**
3. Cliquez sur **PLUS** à côté du dossier d'adhésion
4. Sélectionnez **Renouveler** pour entrer: espèces, chèque ou EFT ou **Renew-Credit Card** pour traiter le renouvellement par votre processeur de paiement en ligne.

![image](../img/z_sprint14_renewmembership_1.png)

Mise à jour par lot des membres via le profil
----------------------------------

You can use the **Batch Update Members Via Profile** feature to update
multiple*existing* membership records (don't confuse this with the
**Batch Data Entry** feature that is used for adding *new* memberships
and member payments).

To use the Batch Update Members Via Profile, you can either use the
CiviCRM default reserved profiles, **Membership Batch
Entry** and **Contribution Batch Entry**, or you can create and
configure a profile that contains fields pertaining to membership
information that you want to display and update. You can read more about
how to configure profiles in the *Profiles* chapter of the *Organising
Your Data* section.

To use the **Batch Update Members Via Profile** feature:

1.  Find the memberships you would like to update by selecting
    **Memberships** > **Find Members.** Enter your search criteria and
    click **Search**.
2.  From the Find Members results screen, select the membership records
    and select **Batch Update Members Via Profile** from the
    **-actions-** dropdown box and click **Go**. 
3.  From the Batch Profile Update for Membership screen, in **Select
    Profile**, select the profile you want to use from the dropdown box
    and click **Continue >>**. You can read more about setting up a
    membership profile for batch update in the *Profiles* chapter of the
    *Organising your data* section. 
4.  From the Batch Update for Members screen, you can update the
    information that is displayed based on the profile you selected.
    You can use the "auto-copy" icon at the top of a column to copy and
    paste the value from the field of the first record of that column to
    the rest of the fields below in the column. Once you are done
    updating, click **Update Memberships**. 

    Below is an example of a Batch Update for Members screen that is using
    a membership profile configured to display the **Membership Type** and
    the **Membership Start Date** fields for use with the **Batch Update
    Members Via Profile**. 

![image](../img/Memberships-Everydaytasks-batchupdateviaprofile-batchupdateformembers.jpg)

