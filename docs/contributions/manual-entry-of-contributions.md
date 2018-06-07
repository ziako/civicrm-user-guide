# Entrée manuelle des contributions 

Lorsque votre organisation reçoit une contribution d'un contact, vous pouvez l'ajouter à son enregistrement. Ceci sera fait automatiquement si le paiement est effectué via CiviCRM (par exemple, un abonnement ou un frais d'événement avec une inscription en ligne) mais les paiements hors ligne (espèces, chèques, etc.) devront être enregistrés manuellement pour s'assurer que les rapports générés par CiviCRM seront précis.


## Ajouter des contributions manuellement une par une


## Adding contributions manually one by one

Si le donneur n'existe pas déjà dans la base de données, vous devez d'abord créer un nouvel enregistrement de contact. Voir [Contacts] (../ organisation-vos-données / contacts) pour des informations sur la façon de procéder. Une fois l'enregistrement créé, vous pouvez entrer la contribution.

Pour entrer manuellement une contribution pour un contact dans votre base de données:

1. Recherchez l'enregistrement du contact à l'aide de l'un des outils de recherche de contacts, par exemple **Rechercher> Rechercher des contacts**.
2. Sélectionnez l'onglet **Contributions** du contact.
3. Cliquez sur **Enregistrer la contribution (Chèque, Espèces, EFT ...)**. Alternativement, si vous avez configuré un processeur de paiement qui autorise les transactions par carte de crédit directement sur votre site, vous pouvez sélectionner l'option **Soumettre la carte de crédit** et traiter le paiement immédiatement.
4. Remplissez le nouveau formulaire de contribution. La capture d'écran suivante montre le formulaire de contribution hors ligne (c'est-à-dire les contributions par chèque, espèces, EFT, etc.). Si vous avez choisi d'enregistrer une contribution par carte de crédit, le formulaire de carte de crédit est presque identique à l'exception des champs liés au paiement.

![Image](../ img / New% 20Contribution% 20by% 20Contact.png)

5. Notez le type financier, le montant, la date de réception (la date par défaut est la date du jour), la date de réception (indiquée sur le reçu généré par le système) et le statut (la valeur par défaut est Terminé). Tous les champs personnalisés pour les contributions apparaîtront également sur ce formulaire.
6. Le champ **Soft Credit To** fonctionne avec les pages de campagne personnelles (PCP) qui exploitent l'aide de vos contacts pour les campagnes. Lorsque vous saisissez un don manuellement sur le formulaire de contribution du contributeur, vous pouvez attribuer un crédit souple au propriétaire du PCP. Il y a plus d'informations sur les PCP et les pages de collecte de fonds de la campagne dans le chapitre "Configuration" de la section CiviContribute.
7. La section **Détails supplémentaires** près du bas de l'écran offre d'autres options, y compris l'ajout d'une note sur la contribution et la saisie de la date à laquelle une lettre de remerciement a été envoyée.
8. Les deux dernières sections vous permettent d'indiquer si la contribution était en l'honneur de quelqu'un d'autre (**Renseignements sur le bénéficiaire**) et s'il y a une prime associée à la contribution (**Information sur les primes**).
9. Cliquez sur **Enregistrer** ou sur **Enregistrer et Nouveau** si vous entrez d'autres contributions.

Si vous constatez que vous saisissez plus de quelques contributions en même temps, pensez à utiliser la méthode **Entrées de données par lot**.

## Inscription par lots de la contribution, de l'adhésion ou des paiements d'engagement

La fonction **Entrées de données par lot** vous permet d'entrer des contributions hors ligne, des adhésions ou des promesses de dons que vous avez reçues à l'aide d'un écran de saisie par lots où vous pouvez utiliser les icônes «autocopy» en haut de chaque colonne pour remplir rapidement dans les valeurs de champ. Il facilite la saisie de données lorsque vous avez beaucoup de paiements à enregistrer en même temps. Il vous permet également de vérifier le montant total et le nombre d'articles du lot par rapport aux paiements enregistrés sur votre ou vos bordereaux de dépôt.

Chaque lot contient des paiements de cotisations ou des paiements d'adhésion ou des paiements de dons. Pendant la saisie des données par lot, vous pouvez créer de nouveaux contacts à la volée. Vous pouvez enregistrer le lot et revenir plus tard pour continuer à entrer les paiements. Si vous disposez des autorisations appropriées, vous pouvez également modifier le nombre total et le nombre d'éléments dans la définition du lot si nécessaire.

Voici un mémo simple pour la saisie de données en masse:

1. Créez un nouveau lot pour la saisie de données.
2. Entrez les cotisations, les cotisations ou les paiements de gage (chèque, espèces, TEF, etc.).
3. Validez et traitez les totaux du lot ou sauvegardez le lot.

Les détails de chaque étape sont énumérés ci-dessous.



### 1. Créer un nouveau lot pour la saisie de données 

Créez un nouveau lot pour conserver les multiples paiements que vous souhaitez enregistrer:  

Dans le menu, cliquez sur **Contributions> Entrée de données par lots** ou **Adhésion> Entrée de données par lots**.
 
![image](../img/New%20Data%20Entry.png)

Entrez les informations suivantes:

- **Nom du lot**: CiviCRM créera un nom de lot par défaut ("Lot N" + date d'ouverture), que vous pouvez modifier (champ obligatoire)
- **Type**: sélectionnez le type de paiement, par ex. Contribution, adhésion ou paiement de dons. Cela permet de sélectionner le profil réservé approprié à afficher dans l'écran de la grille de saisie par lots (profil d'entrée de lot de contribution, profil d'entrée de lot d'adhésion ou profil d'entrée de lot de paiement de don)
- **Statut**: la valeur par défaut sera "Ouvert" (Note: une fois qu'un lot a un "statut fermé", le lot ne sera plus modifiable)
- **Nombre d'articles**: total des postes de paiement dans le lot (champ obligatoire)
- **Montant total**: montant total de tous les postes de paiement du lot (champ obligatoire)

Vous pouvez modifier ou supprimer des informations sur les lots ultérieurement en retournant à l'écran **Entrée de données par lots**, puis en cliquant sur **Modifier** ou **Supprimer** à côté du lot souhaité.

![image](../img/CiviCRM-Contributions-everydaytasks-batches-lists.jpg)

### 2. Saisie de paiements de contribution, d'adhésion ou don (chèque, espèces, TEF, etc.) 

Dès que vous avez entré les informations sur le lot, vous pouvez commencer à entrer des paiements sur chaque ligne.

![image](../img/CiviCRM-Contributions-everydaytasks-batchentrycontrib.jpg)

Il y a huit champs qui apparaissent pour tous les lots:

-  **Contact**. In this column you can:
    -   start entering the name of an existing contact and CiviCRM will
    return a list of potential contact names for you to select, OR
    -   create a new contact by clicking the drop-down box for “-create new
    contact-“ and selecting the type of contact you want to create: **New
    Individual**, **New Organization**, or **New Household** and enter the
    information about the contact here.
    Note: If contact information such as phone number or email address
are included in the grid profile, those values will be populated for
an existing contact and can be updated as needed.
-   **Financial Type**
-   **Amount**
-   **(Payment) Status**
-   **Received – Date and Time**
-   **Send Receipt:** check the box if you want to send a receipt via email
-   **Soft Credit**
-   **Soft Credit Type**

When batch entering contribution payments the additional fields in the
standard profile are:

-   **Source** : enter text that describes the source of the payment
-   **Paid by**: enter the type of payment vehicle, e.g. cash, check,
    EFT, etc.
-   **Check Number**: if paid by check
-   **Invoice ID**

When batch entering membership payments you can choose to add a new
membership or renew an existing membership. The extra fields in the
standard profile are:

-   **Type**: For a new membership you will select the organisation and
    type of membership. For the renewal you can change the membership
    type.
-   **Member Since:** When you open the batch entry form, this is
    populated with the current date If you choose to renew a membership
    it will change to display the start date for that membership. It can
    be edited as needed.
-   **Start Date**(reserved): This is blank. You only need to fill in
    this field if you want the start date to be other than the default.
-   **End Date(reserved)**: If this is left empty, CiviCRM will use the
    membership rules to set it to the correct date.
-   **Source**: Enter text that describes the source of the payment.
-   **Paid by**: Enter the type of payment vehicle, e.g. cash, check,
    EFT, etc.
-   **Check Number**: Enter if paid by check.
-   **Invoice ID**

When batch entering pledge payments you can assign the payment to any of
the pending pledges for that contact. If you have the appropriate
permissions, you can also alter the amount or schedule for the pledge
payment. (Click on **adjust payment amount** next to the **Amount**
field.)The extra fields in the standard profile are:

-   **Source**: enter text that describes the source of the payment
-   **Paid by**: enter the type of payment vehicle, e.g. cash, check,
    EFT, etc.
-   **Check Number**: if paid by check
-   **Invoice ID**

### 3. Validate and Process the Batch Totals or Save the Batch

You can enter all transactions for the batch in one session, or simply
save the batch and complete the data entry at a later time.

If you want to continue entering information into this batch at a later
time, click **Save & Continue Later**.

To find and add/edit more transactions into the batch later:

-   From the menu, click on **Contributions > Batch Data Entry** or
    click on **Membership > Batch Data Entry**, then click on**Enter
    Records** next to the batch you want

Then continue entering more transactions in the batch

Once you are finished entering payments into a batch, click **Validate &
Process the Batch**. The status of the batch will be set to
“**Closed**” and will available for searches and reporting later.

If the total amount or count of items do not match the values you
entered when you created the Batch, you will be alerted when closing if
the count or total don't match. In this case, you either:

-   You can override the entered count and total by clicking**Ignore
    Mismatch & Process the Batch?** button, in which case the batch
    values are updated to match the transactions in the batch, and then
    the status of the batch will be set to “**Closed**”, OR
-   You can continue entering or editing the payments for the batch,
    then **Validate & Process the Batch** again.

![image](../img/CiviCRM-Contributions-everydaytasks-ignoremismatchbatch.jpg)

### Search for contribution, membership or pledge payments in verified and processed batches

You can search for contribution or membership payments in verified and
processed batches in a several ways:

-   From the menu, click on **Searches > Find Contributions** , enter
    criteria for the contributions, and under **Batch Name**, select the
    batch you want;
-   From the menu, click on **Searches > Advanced Search**, enter
    criteria about the contact, then open the Contributions area and
    enter any contribution criteria, and under **Batch Name**, select
    the batch you want;
-   From the menu, click on **Contributions > Batches** , then select
    **Closed** in the **Status**field;
-   From the menu, click on **Memberships > Batches** , then select
    **Closed** in the **Status** field;
-   From the menu, click on **Pledge Payments > Batches**, then
    select **Closed** in the **Status** field;
-   From the menu, click **Reports > Create Reports from Templates**,
    then click **Contribution Report Detail**, enter your report
    criteria and under Set Filters area, next to**Batch Name**, select
    “**is one of**” or “**is not one of**” and select the name(s) of the
    batch(es) you want.

### Configuring Profiles for Batch Entry of Contribution, Membership and Pledge Payments

To alter the profile used when you want to create a new contact for an
Individual, Household, or Organization while recording the contribution,  update the reserved
profiles called **New Individual**, **New Household**,
or **New Organization** accordingly. To change the fields of
information you want to collect for these contacts:

-   Go to the menu and click **Administer > Customize Data and Screens > Profiles**, then click on **Reserved Profiles** tab. Click on
    **Fields** next to called **New Individual, New Household**, or
    **New Organization**.
-   You can then add, edit or rearrange the fields as you want to see
  them in the batch entry input grid. *To find out more about how to
  use profiles, see the chapter called “Profiles” in the “User
  Interface” section*.

**TIP:** Reserved profiles for **New Individual, New Organization**,
and **New Household**, are used in other areas of CiviCRM. Be aware
that if you alter these profiles for use with **Batches**, these same
changes you’ve made will also appear on other screens where you have the
option to create a new contact inline.

  ![image](../img/CiviCRM-Contributions-SetUp-new-individual-profile.jpg)

Above is CiviCRM’s default configuration of the New Individual profile,
which is used when you select to create a new contact for an individual
during batch entry of contributions or membership payments.

To alter the profile of fields of information you want to collect for
contributions or membership payments, you will need to update the
reserved profiles called **Contribution Batch Entry** or **Membership
Batch Entry**:

-   Go to the menu and click **Administer > Customize Data and Screens >
Profiles**, then click on **Reserved Profiles** tab. Click on
    **Fields** next to **Contribution Batch Entry** profile or the
    **Membership Batch Entry** profile.
-   You can then add, edit , or rearrange the fields in this profile,
    e.g. you may have other custom contribution fields you would like to
    display and collect information, and display in the batch entry
    input grid. To find out more read [Profiles](../organising-your-data/profiles).

  ![image](../img/CiviCRM-Contributions-SetUp-contribution-batch-entry-profile.jpg)

  Above is CiviCRM’s default configuration for the Contribution Batch
  Entry profile, which is used when you record information about a
  contact’s contribution or pledge payment.



  ![image](../img/CiviCRM-Contributions-SetUp-membership-batch-entry-profile.jpg)

  Above is CiviCRM’s default configuration for the Membership Batch Entry
  profile, which is used when you record information about a contact’s
  membership payment.

## Importing contributions

If you have not imported data before, please read [Importing data into civicrm](../common-workflows/importing-data-into-civicrm).

When preparing your data import it is helpful to know what fields are
required for Import. You'll want to be sure that these fields are
included in your CSV import file. Below is a list of the required
fields. Please note that you only need one of the fields marked **(Match to
  Contact)**
  -   **Contact ID (Match to Contact)**
  -   **Email (Match to Contact)**
  -   **External Identifier (Match to Contact)**
  -   **Financial Type**
  -   **Total Amount**

The import tool for contributions is similar to that of contacts, but
contributions cannot be imported unless the
contributors already exist in the database as contacts. If you need to
import contributions for contacts that are not yet available, run a
contact import first, preferably including a unique external identifier
(most often an ID assigned by the database or application you are
importing records from). There are two ways to match a contribution to a
contact:

-   Use the external ID of the contact by including the ID in a column
    of the CSV file (if this ID was not imported with contacts, but you
    have them on record, a second contact import could be run to update
    this field, after which you may import contributions).
-   Alternatively, you can match contributions to contacts based on your
    contact de-dupe rules, e.g. through including the first name, last
    name and email address of the donor against each contribution in the
    file. If a contact matches these three fields, the contribution will
    be assigned to it.

Remember, CSV files must be less than 2MB in size. If the file size
exceeds this, create multiple CSV files and distribute the data between them.
