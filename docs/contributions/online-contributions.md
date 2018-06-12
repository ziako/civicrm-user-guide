Création de pages de contribution
-----------------------------

Cette section décrit la mise en place de pages de contribution en ligne dans lesquelles les visiteurs de votre site Web peuvent contribuer à votre organisation.
CiviContribute est très flexible, adaptable et inclut de nombreux champs et fonctionnalités optionnelles tels que des contributions récurrentes, des promesses de dons et des pages de campagne personnelle. Cela peut rendre la mise en place de pages de contribution comme une tâche lourde, mais pas insurmontable comme le montrent les deux premières procédures ci dessous.


## La page de contribution la plus simple (réception envoyée uniquement par le processeur de paiement.)

1. Assurez-vous d'avoir un [processeur de paiement configuré](../contributions/payment-processors).
2. Allez à **Contributions> Nouvelle page de contribution**.
3. Entrez le **titre** de la page pour votre site Web.
4. Sélectionnez le **type financier** approprié.
5. Cliquez sur **Continuer**.
6. Sur la page suivante, laissez tout tel quel, sauf en cochant la case **Autoriser d'autres montants** et en réglant les montants **minimum * et / ou **maximum** si vous le souhaitez.
7. Cliquez sur **Enregistrer et Terminé**.
8. Suivez les étapes de votre CMS pour [afficher cette page sur votre site web](#publicizing-your-contribution-page).  


## Une page de contribution très simple incluant l'accusé de réception 

1. Assurez-vous d'avoir un [processeur de paiement configuré](../contributions/payment-processors).
2. Allez à **Contributions> Nouvelle page de contribution**.
3. Entrez le **titre** de la page pour votre site Web.
4. Sélectionnez le **type financier** approprié.
5. Cliquez sur **Continuer**.
6. Sur la page suivante, laissez tout tel quel, sauf en cochant la case **Autoriser d'autres montants** et en réglant les montants **minimum * et / ou **maximum** si vous le souhaitez.
7. Cliquez sur **Enregistrer**.
8. Sélectionnez l'onglet **Reçu**.
9. Entrez le **titre** pour votre page de remerciement.
10. Cochez **Reçu de courrier électronique au contributeur**.
11. Entrez l'adresse email "DE" dans **Receipt From Email**.
12. Cliquez sur **Enregistrer et Terminé**.

Suivez les étapes de votre CMS pour [afficher cette page sur votre site](#publicizing-your-contribution-page).


## Mise en place d'une page de contribution - détails complets.

Accédez à **Contribution> Nouvelle page de contribution**. (**Contribution> Gérer les pages de contribution> Ajouter une page de contribution**) vous amène à cet écran :

![New Contribution Page](../img/civicontribute-new-contribution-page.png)

- Le titre de la page et le type financier sont les seuls champs obligatoires. CiviCRM est livré avec quatre types financiers standards, mais vous pouvez en [créer plus](../contributions/concepts-clés-et-configurations) pour répondre aux besoins comptables de votre organisation :
- Lier cette page de contribution à une [campagne](../campaign/what-is-civicampaign). (Optionnel)
- Composez votre message d'introduction. (optionnel)
- Composez votre message de pied de page. (optionnel)
- Définir un montant d'objectif. (optionnel)
- Cette page de contribution doit être activée ou désactivée manuellement, mais vous pouvez définir une **date de début** et une **date de fin** qui s'appliqueront pour un widget de contribution et [Pages de campagne personnelles](../contributions/personnel-campaign-pages). (optionnel)
- Choisissez si vous acceptez ou non : [Créditer un bénéficiaire](../contributions/soft-credits)
- Choisissez d'utiliser une page de confirmation où les utilisateurs peuvent vérifier que tous les détails sont corrects ou de traiter le paiement dès que le formulaire de contribution est soumis.
- Choisissez d'afficher ou non les liens de médias sociaux sur les pages en ligne et dans le reçu automatiquement envoyé par courriel (s'il est envoyé).
- Décidez si la page de contribution doit être active ou non.
- Cliquez sur **Continuer**. (C'est à ce moment que votre nouvelle page de contribution est enregistrée pour la première fois.) Vous pourrez revenir en arrière et modifier tous les aspects de cette page à tout moment en cliquant sur l'onglet **Titre** et Paramètres.

Vous allez ensuite à l'onglet (Contributions) **Montants**. Toutes les autres fonctionnalités sont alors visibles dans les onglets en haut de page. Nous les explorons un à un ci-dessous.

--- TRADUCTION EN COURS ----

### Amounts tab
![Contributions Amounts Page](../img/civicontribute-online-contribution-amounts.png)

-  The **Execute real-time monetary transactions** box is checked by default.
You would uncheck this box if you are using this contribution page for free
membership signup or to solicit in-kind (non-monetary) donations, or when you
want **all** users to submit their payments offline.
-  Select the **Currency**.
-  Select one or more previously configured [Payment Processors](../contributions/payment-processors)
for this page. Some organizations find it is a good idea to offer a choice of
processors. You can do this by setting up multiple processors, and checking the
    corresponding boxes on this form.
-  Check the **Pay Later** box if you want to give users the option to
    submit payment offline (e.g. mail in a cheque, call in a credit card, deposit directly into your bank account etc.). If you allow pay later contributions you will need to decide on a checkbox label to display to your users and the instructions for submitting these delayed payments.
-  If you uncheck the **Contribution Amounts Section Enabled** the remaining fields on this page will vanish. You will only be able accept fixed-amount membership fees, or, if you configure a membership price set, fixed-amount memberships fees and other contributions as specified in the price set all charged in a **single** transaction.
-  Select a pre-defined **Price Set** (for more complex payment
    options), OR enter up to 10 fixed contribution amounts in the table at the bottom of the page.)
-  You can check **Recurring contributions** if you payment processor and its integration with CiviCRM support recurring billing and you want to allow this feature. (There are restrictions on recurring payments when [membership fees](../membership/defining-memberships) are being paid.) If you check **Recurring contributions** further settings become visible.
-  Check the **Pledges** box to give users the opportunity to [pledge
    future payments](../pledges/what-is-civipledge).
-  Decide on the label for the Contribution amount area on your page.
-  Check **Allow other amounts** to give users the option to pay any
    amount they choose. You can set a minimum and a maximum amount for "Other Amount" contributions if you want to.
-  Click **Save and Done**.

### Memberships tab

This is covered in detail in  [Memberships](../memberships/online-membership-sign-up).

### Profile tab

If you want to collect information from contributors beyond the essential fields
required to make a contribution, such as age, interests and skills,
you can include existing CiviCRM Profiles at the beginning or end of a
contribution page. You can also create new profiles.

Profiles used in a contribution page can ONLY contain fields which
belong to:

-   contact records
-   contribution records

Profiles which include fields associated with any other record types
will not be available for this purpose.

Contribution pages will always include a required email address field,
regardless of whether you include any other fields in your profile(s).

1.  Navigate to Manage Contribution Pages then for the page you wish to
    configure, click on **Configure > Include Profiles**.
2.  Select a CiviCRM profile from the dropdown menu to be included at
    the top of the contribution page and/or at the bottom of the page.
    You can then preview your selection(s), edit an existing profile,
    copy an existing profile or create a new profile.
    When you edit or create a new profile you will use the profile drag
    and drop interface pictured here.

    ![image](../img/Contribution-page-edit-profile2.gif)

    WARNING: If you modify an existing profile whilst configuring your
    Contribution page, the changes you make will apply everywhere that
    profile is being used. So unless an existing profile **exactly**
    matches your requirements you should copy the profile, then rename
    and edit the copy as required.
3.  Click **Save** or **Save and Done** or **Save and Next**.

For more information read [Profiles](../organising-your-data/profiles).

Automatic Contribution Recording
--------------------------------

Regardless of how donors get to your contribution page, CiviCRM
automatically records their donations, freeing your staff from doing
manual data entry. If the donors already exist in the database, CiviCRM
adds the contribution to their existing record. If they don't exist,
CiviCRM creates a new record for them.

In situations where people have multiple email addresses, or where more
than one person shares an email address, it can be possible for
contributions to be credited to the wrong contact. To mitigate the
chance of this happening, you can adjust CiviCRM's default duplicate
matching rules. For instructions on how to do this, read
[Deduping and Merging](../common-workflows/deduping-and-merging).

### Receipt TabThank-you and Receipting

Once you have created your contribution page, you can customise the
Thank-you and Receipt emails that are sent to contributors.

1.  Navigate to **Administer > CiviContribute > Manage Contribution
    Pages**.
2.  Use the **Configure** link at the right-hand side of a contribution
    page in the list to access and edit the page.
3.  Click on **Thank-you and Receipting** and enter the information that
    you wish to appear in the thank-you email. Donors usually expect a
    receipt as soon as their transaction is complete, so it is
    recommended to enable the automatic Email Receipt.
4.  Click **Save and Done**.

## Publicizing your contribution page

Now that you've created your contribution page, it's time to bring
people to the page so they can contribute. You will probably want to
display a link to the page prominently on your website through a donate
button or menu item. Here are some additional tips for promoting a
contribution page in different CiviCRM configurations:

### Menu item in Joomla!

The most direct way to expose your contribution page or membership
signup/renewal page on the front of your web site is by creating a menu
item.

1.  Navigate to a menu and create a new CiviCRM item.
2.  From the list of menu options, choose Contributions.
3.  In the basic parameters section, select the contribution page you
    would like exposed from the dropdown menu.
4.  Save the menu item and view the website to confirm the page's
    functionality.

### Menu item in Drupal

From the contribution page listing, select Live Page to view the
finished page. You can then copy the URL and include it in a content
page or assign it to a menu item.

### Page or Post in WordPress

You can easily embed your contribution page in a post or page on your
WordPress front-end site.

1.  Login to the administration dashboard of your WordPress site.
2.  Click on **Pages** or **Posts > Add New**
3.  Click on the CiviCRM icon next to Upload / Insert
4.  Select Contribution Page as your Frontend Element
5.  Select the desired contribution page
6.  Save the page or post, and your contribution page will automatically
    be embedded within your site's theme on that page.

### "Pretty" URLs

CiviContribute contribution pages have "ugly" URLs - in other words,
they are difficult to remember. An example is *:*

*www.myorganization.org/civicrm/contribute/transact?reset=1&id=1*

On the other hand, "pretty" URLs are much easier to remember and use in
your organization's outreach, for example:

*www.myorganization.org/donate*

A pretty URL is simply a URL redirect (automatically taking people from
one page of your web site to another). Drupal provides a helpful module
called Path Redirect
([http://drupal.org/project/path_redirect](http://drupal.org/project/path_redirect))
that lets you can create URL redirects from the user interface without
complicated web server configuration. Joomla! users also have a
work-around if Search Engine Friendly URLs are enabled in Global
Settings. You can then create a menu link to the contribution page and
define the "pretty" URL using the alias field.

### Personalised Email

Emailing your current membership is the other critical way to publicize
the campaign. The CiviMail component of CiviCRM allows you to send
targeted emails to any group of contacts in your database. Within a
CiviMail message you can include links to the contribution form and use
CiviMail's tracking capability to see how many people click on that
link.

One time-tested way to increase contributions is to send each targeted
constituent a personalized email with a link to the contribution form
that has all of their contact information already filled in. This saves
them the hassle of filling it out and raises the chances that they
donate. Using CiviMail, you can use this feature by creating a special
link in the body of your CiviMail message that includes a *checksum
token*. A checksum is a unique and pseudo-random number assigned to each
recipient of the mailing that points back to their contact information,
securely stored in your database.

When people click on the special link, CiviCRM looks them up in the
database and pre-fills fields on the contribution form (core fields or
fields exposed via a profile) with any information in their contact
record. To read more on how to do this and what the link path must be,
visit:
[http://wiki.civicrm.org/confluence/display/CRMDOC/Tokens](http://wiki.civicrm.org/confluence/display/CRMDOC/Tokens)
