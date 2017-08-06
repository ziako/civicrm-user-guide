Entrée manuelle des adhésions
===========================

CiviCRM fournit un ensemble d'outils permettant aux contacts une interaction directe sur le site Web pour devenir membres sans intervention nécessaire de la part du personnel administratif (ce qui est une fonction très puissante permettant un gain de temps au personnel administratif). Il existe de nombreuses situations dans lesquelles les adhésions doivent être traitées manuellement. Ce chapitre décrit les différentes façons dont le personnel administratif (ou les utilisateurs autorisés) peuvent créer et traiter manuellement des adhésions, y compris:

- Créer de nouveaux enregistrements d'adhésion un par un (y compris les adhésions gratuites où le paiement provient d'un contact différent)
- Entrér des données des membres par lots 
- Importer des adhésions   

Contrôle d'accès à CiviMember
-------------------------

Comme pour les autres fonctions de CiviCRM, **Administer> User & Permissions> Permissions** vous permet de contrôler l'accès à diverses fonctionnalités de CiviMember.

Pour les utilisateurs qui doivent chercher et afficher les adhésions :
- Attribuez l'autorisation **Accéder à CiviMember** et **Voir les contributions** si des paiements sont concernés et assurez-vous que l'utilisateur est autorisé pour afficher les contact pour l'enregistrement associé.
Pour les utilisateurs qui doivent créer et afficher les adhésions :
- attribuez l'autorisation **Accéder à CiviMember** et  **Voir les contributions** si des paiements sont concernés et assurez-vous que l'utilisateur affiche les autorisations de contact pour l'enregistrement associé.

Pour plus de précision sur les permissions voir : 
[http://wiki.civicrm.org/confluence/display/CRMDOC/Default+Permissions+and+Roles](http://wiki.civicrm.org/confluence/display/CRMDOC/Default+Permissions+and+Roles)

Création d'un nouveau dossier d'adhésion
--------------------------------

Vous pouvez créer un nouvel enregistrement d'adhésion de deux façons : directement dans le contact ou dans le menu **Adhésions**. L'utilisation du menu **Adhésions** est pratique car vous pouvez créer un nouveau contact en même temps que l'ajout du nouvel enregistrement d'adhésion :**Nouvelle adhésion**

Un des avantages de créer une nouvelle adhésion directement à partir d'un contact existant est que si vous avez configuré un processeur de paiement qui autorise les transactions par carte de crédit sur votre site, vous pouvez sélectionner l'option **Soumettre une carte de crédit** et traiter le paiement de l'adhésion immédiatement.

Lorsque vous utilisez le menu **Adhésions** pour créer une nouvelle adhésion, vous n'avez pas la possibilité de soumettre des informations sur la carte de crédit, mais vous pouvez enregistrer d'autres types de paiements comme les chèques et les espèces.

### Via un enregistrement de contact existant

- À partir du dossier d'un contact, cliquez sur l'onglet **Adhésions** puis cliquez sur "Ajouter Adhésion". Si vous avez configuré un processeur de paiement qui autorise les transactions par carte de crédit directement sur votre site, vous pouvez sélectionner l'option **Soumettre une carte de crédit** et traiter immédiatement le paiement.

![image](../img/manual-add-membership.png) 

Sur le formulaire **Nouvelle adhésion**  plusieurs champs seront complétés automatiquement s'ils sont laissés en blanc. Les champs incluent:

-   **Organisation et type d'adhésion:** Sélectionnez le nom de l'organisation avec laquelle le contact a une adhésion et le type d'adhésion ***OU***

-   **Choisir une tarification**: Sélectionnez "Choisir une tarification" plutôt que l'organisation et le type d'adhésion si vous disposez de diverses structures tarifaires pour différentes catégories d'adhésion. (Voir le chapitre *Gestion des tarifications* pour plus de détails)

-   **Nombre de périodes :** Entrez le nombre de périodes d'adhésion ou les termes associés à ce dossier d'adhésion. La date de fin d'adhésion sera alors définie à une date de fin en fonction du nombre de termes (cette option est cachée lors de l'utilisation de la gestion des tarifications)

-   **Source**: Si elle est laissée vide, le système complète les détails concernant l'enregistrement : transaction hors ligne ou en ligne et qui a rempli l'enregistrement.

-   **Campagne**: Si l'adhésion est associée à une campagne d'action spécifique, sélectionnez le nom de la campagne. Pour en savoir plus, consultez la section *Campagne*.

-   **Membre depuis le**: La date à laquelle l'adhésion a été créée sera rempli automatiquement, mais peut être remplacé si nécessaire. Par défaut: date de saisie.

-   **Date de début**: Si le type d'adhésion est une adhésion "glissante", la date actuelle sera remplie automatiquement. Si le type d'adhésion est une période fixe, CiviCRM déterminera la date de début appropriée en fonction de la configuration du type d'adhésion. Cela peut être remplacé si nécessaire.

-   **Date de fin**: Ce champ est automatiquement calculé à partir de la date de début et rempli en fonction des paramètres du type d'adhésion. Cela peut être annulé si nécessaire.

-   **Auto-renouvellement**: Ce champ n'est affiché que si vous avez choisi un type d'adhésion qui a une fonction de renouvellement automatique définie dans le type d'adhésion et utilise l'option "Soumettre une carte de crédit" pour créer l'adhésion.

-   **Forcer le statut?**: Cochez cette case pour définir manuellement un statut pour l'enregistrement de membre. Comme indiqué par le titre, il remplace l'état automatiquement fourni. Vous devriez faire preuve de prudence avec ce champ car le réglage empêchera l'état de se mettre à jour automatiquement en fonction des statuts de l'adhésion que vous avez configurés (voir le chapitre *Définir les adhésions*)

-   **Enregistrer le paiement de la cotisation ?**: En cochant cette case et en remplissant les champs de transaction affichés, vous enregistrerez le versement de l'adhésion. Un enregistrement de contribution est créé automatiquement en plus du dossier d'adhésion. Après avoir enregistré l'adhésion, vous pourrez voir le dossier d'adhésion et voir l'enregistrement de contribution correspondant.

    -   **Enregistrer le paiement d'un contact différent ?**: Ceci est souvent utilisé pour les attribution de gratuité
    -   **Montant**: Entrez le montant du paiement de l'adhésion.
    -   **Reçu**: Entrez la date et l'heure (heure : facultatif) de réception du paiement.
     -  **Type d'opération**: Sélectionnez le type financier approprié pour ce paiement.
    -   **Méthode de paiement**: Sélectionnez le moyen de paiement par lequel ce paiement a été reçu, par exemple en espèces ou en chèque. Vous pouvez en savoir plus sur la configuration des instruments de paiement dans la section *Contributions*.
     -   **Numéro de chèque**: Si le paiement a été reçu par chèque, entrez le numéro de chèque si désiré.
     -   **ID de Transaction**: Si vous disposez d'un processeur de paiement, CiviCRM stockera un identifiant de transaction généré automatiquement. Pour les transactions manuelles, vous pouvez entrer un identifiant de transfert bancaire ou un autre identifiant, le cas échéant.
     -   **Etat du paiement**: Sélectionnez le statut du paiement de l'adhésion reçue. Vous pouvez en savoir plus sur la configuration des instruments de paiement dans la section *Contributions*.

     -   **Envoi Confirmation et reçu?:** Cochez cette case pour envoyer un courriel au contact confirmant son adhésion
     -   **Réception de :** sélectionnez l'adresse email dont le reçu de confirmation provient de. Si l'adresse e-mail que vous souhaitez utiliser n'est pas répertoriée, vous pouvez l'ajouter en allant dans **Mailings> From Emails**.
    -   **Réception a :** Sélectionnez l'adresse d'envoi du courriel de confirmation . Si l'adresse e-mail que vous souhaitez utiliser n'est pas répertoriée, vous pouvez l'ajouter en allant dans **Mailings> From Emails**.
    -   **Message de réception:** vous pouvez entrer le texte ici pour envoyer un message spécial au membre. Si vous ne saisissez pas de texte, le message de confirmation et de réception par défaut sera utilisé.
    

### **Auto-renouvellement des adhésions via le Back end**

Pour créer manuellement une adhésion qui se renouvellera automatiquement, reportez-vous à l'écran récapitulatif du contact, sélectionnez l'onglet **Adhésions** et cliquez sur **Soumettre l'adhésion par carte de crédit**. Si vous sélectionnez un type d'adhésion qui est configuré pour être récurrent, une case à cocher intitulée **L'adhésion renouvelée automatiquement** sera affichée.


If you check Auto-renew, a recurring payment (subscription) request will
be submitted to the selected payment processor. If the request is
successful, this membership will be automatically renewed on the last
day of the membership period until the recurring payment is cancelled.
Membership payment receipt emails will include a link for the member to
cancel the auto-renewal.

### Via the **Memberships** menu

-   Navigate to **Memberships** **> New Membership**, then select the
    contact or create a new contact. 

![image](../img/memberships%20add%20membership%20new%20contact.JPG)

-   Fill out the New Member form with the appropriate membership and
    payment information as in *Via an existing contact record* above.

![image](../img/memberships%20add%20membership%20via%20menu.JPG) 

Gift Memberships
----------------

When you enter a membership manually you can select **Record Payment
from a Different Contact?** to record the membership as a gift from
someone else. The person paying for the membership (gifter) can be an
existing or a new contact created during the process. The payment will
be recorded on the gifter's record with a soft credit for the membership
on the gift recipient's record. The receipt will be sent to the gifter.
You will need to send a separate email or letter to tell the gift
recipient about their membership. 

![image](../img/gift%20membership.PNG)

Entering batches of membership payments
---------------------------------------

CiviCRM offers a **Batch Data Entry** feature (found in the
**Memberships** menu) that can be used for entering batches of
membership payments that have been received into the office on paper
forms, or similar. It can be used for new and existing contacts and
includes verification of the total amount and count of items against the
payments you’ve recorded on your deposit slip(s). 

This feature has a batch entry grid input screen, which has a couple of
tools that you can use to speed up processing when you have a lot of
memberships to process at the same time. It includes a copy feature to
set all fields to the same value, and allows you to create new contacts
without leaving the batch entry screen. 

The fields of information that you want to collect in the batch entry
input grid for Batches are determined by several CiviCRM reserved
profiles. If you want to collect other kinds of information that are
not currently included in these profiles, you will need to alter these
profiles to reflect the fields you want to display.

You can read more details about the *Batch Entry of Contributions or
Membership Payments* feature in the *Set-Up* chapter of the
*Contributions* section. 
 

Importing Memberships 
-----------------------

The **Importing Memberships** feature is very useful if you have a large
set of membership records that comes from a source outside of CiviCRM.
This feature can also be used to update large numbers of existing
memberships with new information.

You should read the *Importing Data* chapter in the *Common Workflows*
section, before you begin importing memberships since this gives lots of
relevant general information. Here are a few details specific to
membership importing that you should be familiar with.

-   Contact records must exist before you import membership data. If
    you want to import membership data for contacts that do not yet
    exist in CiviCRM, you will first need to import the Contact data.
    Make sure the contact data has an External ID so you can include
    this External ID with your membership data to associate these
    records with the related contacts. If you are importing membership
    data for contacts that already exist, then you will need the
    Internal Contact ID or the fields from your Unsupervised Duplicate
    Matching Rule to associate the related membership data with the
    correct contact.
-   Your import membership data file MUST contain both Membership Type
    and Start Date. The membership types listed must exactly match the
    membership types set up by your CiviCRM Administrator. The start
    date should use the date format specified for your CiviCRM
    installation. If your import file does not contain these fields then
    you will not be able to import it. 
-   You must import membership data for different contact types
    separately. Importing files with more than one contact type will not
    work. (You must import new memberships and renewals separately
    also.) 

Now you are ready to import your membership data:

1. 
Navigate to **Memberships > Import Memberships**.
1. 
On the Upload Data screen:

    -   Select your import data file. It must be a CSV file. 
    -   Select the checkbox if your source data contains column headers. 
    -   Specify the contact type you are importing. 
    -   Indicate what date format you are using.
    -   Click **Continue >>**.
1. 
On the Match Fields screen, map your membership data with the
appropriate CiviCRM fields under the Matching CiviCRM Field column.
Note that you can **Save this field mapping** so you can re-use this
mapping for future imports. 
1. 
On the Preview screen, you will see the preview of the results of your
import. There is a table that lists the Total Rows in the uploaded file,
the number if rows with errors and the number of valid rows. If you
continue with the import, the rows with errors will be skipped. You can
download a file with just these problem records and continue with the
import. You can then edit the errors and do another import with them.
Alternatively, you can fix the errors in your original CSV file and
start the import again.
1. 
If there are no errors or you don't want to correct the found errors,
click **Import Now>>**. You will be shown the progress of the
import until it is complete. When the import is complete, you will see a
summary of the import activity and its results. 

