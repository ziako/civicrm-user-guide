# Entrée manuelle des contributions 

Lorsque votre organisation reçoit une contribution d'un contact, vous pouvez l'ajouter à son enregistrement. Ceci sera fait automatiquement si le paiement est effectué via CiviCRM (par exemple: une cotisation, un abonnement ou le règlement de frais d'événement avec une inscription en ligne) mais les paiements hors ligne (espèces, chèques, etc.) devront être enregistrés manuellement pour s'assurer que les rapports générés par CiviCRM soient précis.


## Ajouter des contributions manuellement une par une

Si le donneur n'existe pas déjà dans la base de données, vous devez d'abord créer un nouvel enregistrement de contact. Voir [Contacts](../ organisation-vos-données / contacts) pour des informations sur la façon de procéder. Une fois l'enregistrement créé, vous pouvez entrer la contribution.

Pour entrer manuellement une contribution pour un contact dans votre base de données:

1. Recherchez l'enregistrement du contact à l'aide de l'un des outils de recherche de contacts, par exemple **Rechercher> Rechercher des contacts**.
2. Sélectionnez l'onglet **Contributions** du contact.
3. Cliquez sur **Enregistrer la contribution (Chèque, Espèces...)**. Si vous avez configuré un processeur de paiement qui autorise les transactions par carte de crédit directement sur votre site, vous pouvez sélectionner l'option **Soumettre la carte de crédit** et traiter le paiement immédiatement.
4. Remplissez le nouveau formulaire de contribution. La capture d'écran suivante montre le formulaire de contribution hors ligne (c'est-à-dire les contributions par chèque, espèces, etc.). Si vous avez choisi d'enregistrer une contribution par carte de crédit, le formulaire de carte de crédit est presque identique à l'exception des champs liés au paiement.

![Image](../img/New%20Contribution%20by%20Contact.png)

5. Notez le type financier, le montant, la date de réception (la date par défaut est la date du jour), la date de réception (indiquée sur le reçu généré par le système) et le statut (la valeur par défaut est Terminé). Tous les champs personnalisés pour les contributions apparaîtront également sur ce formulaire.
6. Le champ **Bénéficiaire (Soft Credit To)** fonctionne avec les pages de campagne personnelles (PCP) qui exploitent la participation de vos contacts pour les campagnes. Lorsque vous saisissez un don manuellement sur le formulaire de contribution du contributeur, vous pouvez attribuer un crédit souple au propriétaire du PCP. Il y a plus d'informations sur les PCP et les pages de collecte de fonds de campagne dans le chapitre "Configuration" de la section CiviContribute.
7. La section **Détails supplémentaires** près du bas de l'écran offre d'autres options, y compris l'ajout d'une note sur la contribution et la saisie de la date à laquelle une lettre de remerciement a été envoyée.
8. Les deux dernières sections vous permettent d'indiquer si la contribution était en l'honneur de quelqu'un d'autre (**Renseignements sur le bénéficiaire**) et s'il y a une prime associée à la contribution (**Information sur les primes**).
9. Cliquez sur **Enregistrer** ou sur **Enregistrer et Nouveau** si vous entrez d'autres contributions.

Si vous constatez que vous devez saisir plusieurs contributions en même temps, pensez à utiliser la méthode **Entrées de données par lot**.

## Inscription par lots de la contribution, de l'adhésion ou des paiements d'engagement

La fonction **Entrées de données par lot** vous permet d'entrer des contributions hors ligne, des adhésions ou des dons que vous avez reçus à l'aide d'un écran de saisie par lots où vous pouvez utiliser les icônes «autocopy» en haut de chaque colonne pour remplir rapidement les valeurs des champs. Ceci facilite la saisie de données lorsque vous avez beaucoup de paiements à enregistrer en même temps. Cela vous permet également de vérifier le montant total et le nombre d'articles du lot par rapport aux paiements enregistrés sur votre ou vos bordereaux de dépôt.

Chaque lot contient des paiements de cotisations ou des paiements d'adhésion ou des paiements de dons. Pendant la saisie des données par lot, vous pouvez créer de nouveaux contacts à la volée. Vous pouvez enregistrer le lot et revenir plus tard pour continuer à entrer les paiements. Si vous disposez des autorisations appropriées, vous pouvez également modifier le nombre total et le nombre d'éléments dans la définition du lot si nécessaire.

Voici un mémo simple pour la saisie de données en masse:

1. Créez un nouveau lot pour la saisie de données.
2. Entrez les cotisations, les cotisations ou les paiements de gage (chèque, espèces, etc.).
3. Validez et traitez les totaux du lot ou sauvegardez le lot.

Les détails de chaque étape sont énumérés ci-dessous.

### 1. Créer un nouveau lot pour la saisie de données 

Créez un nouveau lot pour conserver les multiples paiements que vous souhaitez enregistrer:  

Dans le menu, cliquez sur **Contributions> Entrée de données par lots** ou **Adhésion> Entrée de données par lots**.
 
![image](../img/New%20Data%20Entry.png)

Entrez les informations suivantes:

- **Nom du lot**: CiviCRM créera un nom de lot par défaut ("Lot N" + date d'ouverture), que vous pouvez modifier (champ obligatoire)
- **Type**: sélectionnez le type de paiement, par ex. Contribution, adhésion ou dons. Cela permet de sélectionner le profil réservé approprié à afficher dans l'écran de la grille de saisie par lots (profil d'entrée de lot de contribution, profil d'entrée de lot d'adhésion ou profil d'entrée de lot de paiement de don)
- **Statut**: la valeur par défaut sera "Ouvert" (Note: une fois qu'un lot a un "statut fermé", le lot ne sera plus modifiable)
- **Nombre d'articles**: total des postes de paiement dans le lot (champ obligatoire)
- **Montant total**: montant total de tous les postes de paiement du lot (champ obligatoire)

Vous pouvez modifier ou supprimer des informations sur les lots ultérieurement en retournant à l'écran **Entrée de données par lots**, puis en cliquant sur **Modifier** ou **Supprimer** à côté du lot souhaité.

![image](../img/CiviCRM-Contributions-everydaytasks-batches-lists.jpg)

### 2. Saisie de paiements de contribution, d'adhésion ou don (chèque, espèces, etc.) 

Dès que vous avez entré les informations sur le lot, vous pouvez commencer à saisir des paiements sur chaque ligne.

![image](../img/CiviCRM-Contributions-everydaytasks-batchentrycontrib.jpg)

Il y a huit champs qui apparaissent pour tous les lots:

-  **Contact**. Dans cette colonne, vous pouvez:
- Commencez à entrer le nom d'un contact existant et CiviCRM renverra une liste de noms de contacts potentiels pour que vous puissiez sélectionner, OU
- créez un nouveau contact en cliquant sur la liste déroulante pour "créer un nouveau contact" et en sélectionnant le type de contact que vous souhaitez créer: **Nouvelle individuel**, **Nouvelle organisation** ou **Nouveau ménage** et entrez les informations sur le contact ici.
Remarque: Si des informations de contact telles que le numéro de téléphone ou l'adresse e-mail sont incluses dans la grille du profil, ces valeurs renseignées pour un contact existant peuvent être mises à jour si nécessaire.
-   **Type financier**
-   **Montant**
-   **(Statut) de paiement**
-   **Reçu - Date et heure**
-   **Envoyer un reçu: cochez la case si vous voulez envoyer un reçu par courriel**
-   **Bénéficiaire (Soft Credit)**
-   **type de Bénéficiaire (Soft Credit Type)**

Lorsque vous saisissez par lot des paiements de contribution, les champs supplémentaires du profil standard sont:

- **Source**: entrez du texte qui décrit la source du paiement
- **Payé par**: entrez le type de moyen de paiement, par ex. espèce, chèque, etc.
- **Numéro de chèque**: si payé par chèque
- **ID de facture**

Lorsque vous saisissez par lots les paiements d'adhésion, vous pouvez choisir d'ajouter un nouvel abonnement ou de renouveler un abonnement existant. Les champs supplémentaires dans le profil standard sont:

- **Type**: Pour un nouvel abonnement, vous sélectionnez l'organisation et le type d'adhésion. Pour le renouvellement, vous pouvez changer le type d'adhésion.
- **Membre depuis:**  Lorsque vous ouvrez le formulaire de saisie par lots, celui-ci est rempli avec la date actuelle. Si vous choisissez de renouveler un abonnement, il changera pour afficher la date de début de cette adhésion mais elle peut être modifié au besoin.
- **Date de début** (réservé): Ce champ est vide. Vous n'avez besoin de remplir ce champ que si vous souhaitez que la date de début soit différente de la valeur par défaut.
- **Date de fin** (réservé): Si cette case est laissée vide, CiviCRM utilisera les règles d'adhésion pour la mettre à la bonne date.
- **Source**: entrez du texte qui décrit la source du paiement
- **Payé par**: entrez le type de moyen de paiement, par ex. espèce, chèque, etc.
- **Numéro de chèque**: si payé par chèque
- **ID de facture**

Lorsque vous saisissez par lots des paiements de promesse de dons, vous pouvez affecter le paiement à l'un des engagements en attente pour ce contact. Si vous disposez des autorisations appropriées, vous pouvez également modifier le montant ou le calendrier du paiement de nantissement. (Cliquez sur **ajuster le montant du paiement** à côté du champ **Montant**.) Les champs supplémentaires dans le profil standard sont:

- **Source**: entrez du texte qui décrit la source du paiement
- **Payé par**: entrez le type de moyen de paiement, par ex. espèce, chèque, etc.
- **Numéro de chèque**: si payé par chèque
- **ID de facture**

### 3. Valider et traiter les totaux du lot ou sauvegarder le lot

Vous pouvez saisir toutes les transactions pour le lot en une seule session, ou simplement enregistrer le lot et compléter l'entrée de données ultérieurement.

Si vous souhaitez continuer à entrer des informations dans ce lot ultérieurement, cliquez sur **Enregistrer et continuer plus tard**.

Pour rechercher et ajouter ou modifier plus de transactions dans le lot ultérieurement:

- Dans le menu, cliquez sur **Contributions> Entrées de données par lot** ou cliquez sur **Cotisation> Entrées de données par lot**, puis cliquez sur **Enter Records** à côté du lot que vous voulez
Ensuite, continuez à entrer d'autres transactions dans le lot

Une fois que vous avez saisi les paiements dans le lot, cliquez sur **Valider et traiter le lot**. Le statut du lot sera défini sur "**Fermé**" et sera disponible pour les recherches et les rapports ultérieurs.





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
