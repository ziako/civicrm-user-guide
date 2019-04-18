Contacts
========

Les contacts sont au coeur de CiviCRM. Toutes les autres interactions gravitent autour d'eux. Ce chapitre explique comment rechercher, consulter, ajouter, modifier et supprimer des contacts. Nous regarderons aussi comment créer de nouveaux types de contacts et comment les personnaliser.

Il y a trois types de contact dans la configuration par défaut :

-   **Individus / Particuliers** - toute personne sur qui vous voulez faire un suivi.
-   **Organisations** - ceci pourrait être un organisme communautaire, une entreprise, un chapitre de votre organisation ou un comité.
-   **Ménages / Foyers** - une famille ou un groupe de personnes résidant à la même adresse physique.

Chaque fiche de contact contient des informations de base à leur sujet, telles que :

- nom, surnom, salutation, titre (formalité)
- site web, adresses courriel, numéros de téléphone
- adresses postales
- mode de communication préféré (incluant ceux qui ne veulent pas être contactés).

Vous pouvez également définir des sous-types de contact, tels que « étudiants », « fermes » ou « cuisines collectives ». Chaque type de contact que vous créez est basé sur un des trois aux types de base. Par exemple, les fiches d'étudiants seraient basés sur le modèle des individus, les fermes seraient basées sur les organisations ou peut-être même sur les ménages, selon vos besoins. 

Un rapide coup d'oeil sur les contacts
--------------------------------------

Les contacts sont organisés en onglets. Le premier onglet qui s'affiche lorsque vous visualisez un contact est l'onglet **résumé**, qui contient quelques informations de base. Puis viennent les autres onglets, affichant chacun des informations correspondant à différents aspects de votre contact. Cette organisation en onglet vous permet de gérer facilement un nombre important de données qu'il est possible de collecter sur votre contact au fil du temps. 

Les onglets qui s'affichent (ou non) dépendent des composants qui sont activés et des autorisations que vous possédez. Par exemple, vous ne verrez que l'onglet Adhésions si le composant CiviMember est actif et que vous avez l'autorisation de visualisation les adhésions. Vous pouvez également définir des onglets supplémentaires capables d'afficher des champs de données personnalisés.

Nous allons voir ci-dessous les parties les plus importantes de votre écran contact.

### Actions sur les contacts 

Juste au dessus des onglets quelques boutons sont disposés. Le premier d'entre eux est le bouton **Actions** qui contient des raccourcis pratiques sur les actions les plus communes à faire avec un contact : ajouter une note, enregistrer une nouvelle contribution, inscription à un événement, etc.

![image](../img/ActionRibbon.PNG)

### Onglet résumé

L'onglet résumé vous montre les informations principales concernant votre contact. Vous y trouverez notamment ses noms, adresses et autre détails de contact ainsi que les moyens pour le contacter.

Certains champs de cet onglet sont propres au type de contact Individu / Particulier (nom, prénom...) et d'autres propres au type de contact organisation (nom de l'organisation...).

![image](../img/ContactSummary.PNG)

#### Champs propres aux individus / particuliers

Les noms des individus / particuliers sont découpés en parties : préfixe, prénom, deuxième prénom, nom, suffixe et surnom (vous n'avaez pas à tous les utiliser). Les préfixes et suffixes sont sélectionnés à l'aide d'une liste déroulante. Vous pouvez la personnaliser en allant à : **Administrer > Personnaliser les données et écrans > Listes déroulantes > Civilité** et **Suffixes**. 

#### Adresses

Vous pouvez enregistrer une ou plusieurs adresses pour un contact. Chaque adresse doit être d'un type différent de localisation (Travail, domicile...). L'une d'entre elle peut être marquée comme principale et sera utilisée pour tout publipostage. Vous pouvez choisir explicitement quel type de localisation sera l'adresse principale, ou laissez par défaut la première adresse qui sera renseignée.

Vous pouvez partager des adresses entre contacts. Par exemple, vous pourriez avoir besoin d'information entre des contacts  de type individus / particuliers et leur lieu de travail (contact de type organisation). Lorsque vous créez ou modifiez l'adresse "Travail" pour un individu / particulier, activez la case à cocher "Partager l'adresse avec". Si son employeur existe déjà dans la base de donnée, vous pouvez le sélectionner depuis la boite de recherche rapide qui apparait. Sinon, vous pouvez créer à la volée l'enregistrement de l'employeur en sélectionnant "Nouvelle organisation" depuis la liste déroulante "Créer un nouveau contact".

Si une personne effectue un paiement par carte de crédit, les informations utilisées par cette opération seront stockées dans l'adresse de facturation du contact. 

Si vous avez un fournisseur de cartographie actif, vous pouvez cliquer sur l'icône à côté de l'adresse pour voir ses coordonnées sur une carte.

#### Numéros de téléphone 

Vous pouvez stocker plusieurs numéros de téléphone pour chaque contact. Ils sont classés par localisation (travail, domicile...) et par type (filaire, mobile, fax...). Veuillez noter que n'importe quel numéro de téléphone de type "mobile" sera disponible pour l'envoi de SMS.

#### Adresses courriel

Vous pouvez stocker plusieurs adresses courriel pour chaque contact. L'une de ces adresses doit être explicitement marquée comme l'adresse recevant tous les courriels de votre organisation tels que les infolettres/newsletters, les annonces (tous les courriels envoyés depuis le composant CiviMAil). Tout courriel n'arrivant pas à son destinataire est, dans CiviMail, marqué "en suspend". Veuillez vous référer à la section Courriel pour plus d'information.

#### Préférence de communication et protection de la vie privée 

Les moyens de communication préférés des contacts (téléphone, courriel...) et les options de protection de leur vie privée (ne pas appeler, ne pas envoyer de courrier postal...) peuvent être définis. Les options de protection de la vie privée sont respectée lors de l'exécution de certaines fonctionnalités de CiviCRM : les étiquettes de publipostage ne sont pas imprimées pour les contacts ayant coché "ne pas envoyer de courrier", et les courriels ne sont pas envoyés à ceux ayant coché "ne pas envoyer de courriel".

Voici une brève explication de chaque option de protection de la vie privée disponible dans la fiche d'un contact :

-   **Ne pas appeler** : L'utilisateur a choisi de ne pas être contacté par téléphone ;
-   **Ne pas envoyer de courriel**- L'utilisateur a choisi de ne pas être contacté par courriel ;
-   **Ne pas envoyer de courrier**- L'utilisateur a choisi de ne pas être contacté par courrier postal ;
-   **Ne pas envoyer de SMS**- L'utilisateur a choisi de ne pas être contacté par SMS ;
-   **Ne pas transmettre les données personnelles**- L'utilisateur a choisi de ne pas partager ses données personnelles (que vous pourriez partager ou vendre à des organisations tierces) ;
-   **Utilisateur s'est exclu des mailings**- Cette case est cochée quand l'utilisateur a cliqué sur le lien d'exclusion fourni dans un courriel géré par CiviMail.

#### Champs de salutation et destinataire

Par défaut, les champs de salutations et destinataires sont calculés à partir des champs de nom du contact. Par exemple, la salutation dans un courrier postal pour un individu / particulier s'appelant "Jean Dupont" sera "Cher Jean".

Les salutations par défaut peuvent être configurées de manière globale en allant à **Administrer > Communications > Formules de salutation par courrier *or* Formules de salutation par courriel *or* Formats de destinataires**.

Différents formats peuvent aussi être paramétrés au niveau de chaque contact.

### Onglet Relations

Les relations sont des connexions entre des enregistrements de contacts dans votre base de donnée. Chaque connexion peut être nommée pour en décrire sa nature, et chaque contact peuvent avoir plusieurs relations avec d'autres contacts dans la base de donnée. Dans l'exemple ci-dessous, vous pouvez voir une liste de relations courantes et de relations inactives.

![Contact-RelatoinshipTab_1](../img/CiviCRM_update-CiviCore-Contact-RelatoinshipTab_1-en.png)

Vous pouvez en savoir plus sur les relations dans le chapitre *Relations* de la section *Organiser vos données*.

### Onglet Activités

L'onglet Activités affiche une liste de toutes vos interactions avec un contact, y compris toutes les activités "métier" de CiviCRM telles que les participations à des événéments, les contributions, les appels téléphoniques... ainsi que toutes les activités personnalisées que vous pourriez ajouter. Il est également possible d'y enregistrer vos interactions avec le contact : Cliquez sur la liste déroulante en haut de l'écran et sélectionnez un type d'activité (Passer un appel téléphonique, Envoyer un courriel...) vous fera afficher un écran sur lequel entrer les détails.

![Contact_ActivityTab](../img/CiviCRM_update-CiviCore-Contact_ActivityTab-en.jpg)

Pour en savoir plus sur les activités, merci de vous référer au chapitre *Activités* de cette section.

### Onglet Mailings

Cet onglet est visible uniquement si vous avez décoché **Permettre à CiviMail de créer une activité à l'envoi** dans **Administrer > CiviMail > Paramètres de composant CiviMail**. Dans ce cas, chaque courriel envoyé en masse est enregistré dans cet onglet plutôt que dans l'onglet Activités. Cela permet d'améliorer la vitesse d'affichage de ce dernier si votre organisation diffuse massivement de nombreux courriels. 

### Onglet Contributions

L'onglet Contributions affiche toutes les contributions financières faite par un contact, ainsi qu'une synthèse (montant total des contributions pour une période donnée, nombre total des contributions ou montant moyen des contributions)

Cet onglet vous permet également d'enregistrer manuellement des contributions qui n'aurait pas été faites en ligne, en utilisant le bouton **Nouvelle contribution**.

![Contact_COntribTab](../img/CiviCRM_update-CiviCore-Contact_COntribTab-en.jpg )

Pour en savoir plus sur ce sujet, veuillez vous référer au chapitre *Contributions* de ce manuel.

### Onglet Adhésions

Cet onglet affiche les adhésions du contact. Vous pouvez également y enregistrer manuellement celles qui n'auraient pas été faites en lignes, en utilisant le bouton **Ajouter une adhésion**. Vous pouvez également renouveler ou supprimer des adhésions depuis le lien "plus" à droite de chaque adhésion associée au contact.

![Contact_MembershipTabs](../img/CiviCRM_update-CiviCore-Contact_MembershipTabs-en.jpg)

Pour en savoir plus sur ce sujet, veuillez vous référer au chapitre *Adhésions* de ce manuel.

### Onglet Événement

Cet onglet affiche les événéments associés au contact. Par exemple, ceux pour lesquels le contact s'est inscrit, ou encore ceux pour lesquels il s'est porté volontaire.

Depuis cette page, vous pouvez inscrire un contact à un événement, et même enregistrer le paiement associé (ce dernier apparaitra alors dans l'onglet Contribution).

Vous pouvez également modifier les informations d'un événement associé au contact en cliquant sur le lien "Modifier". Par exemple, vous pouvez changer le statut d'un contact sur un événement de "Enregistré" à "En attente".

![Contact_Eventstab](../img/CiviCRM_update-CiviCore-Contact_Eventstab-en.jpg)

Pour en savoir plus sur ce sujet, veuillez vous référer au chapitre *Événements* de ce manuel.


### Onglet Groupes

Cet onglet affiche les groupes auxquels appartient le contact. Les groupes sont utilisés de façon très variée : liste de diffusion de courriel, gestion des autorisations d'accès...

Dans cet onglet, vous pouvez ajoutez ou retirer le contact d'un groupe, et en voir l'historique.

La colonne Statut indique l'utilisateur qui a ajouté le contact au groupe. Il est possible d'autoriser les utilisateurs à s'ajouter eux-même à un groupe. Lorsque vous paramétrez la visibilité d'un groupe à "Listes publiques", les utilisateurs peuvent s'y ajouter à travers un formulaire **Profil** (plus d'information à ce sujet dans le chapitre *Les profils* de cette section).

![Contact_GroupsTab](../img/CiviCRM_update-CiviCore-Contact_GroupsTab-en.jpg)

Pour en savoir plus sur ce sujet, veuillez vous référer au chapitre *Groupes et étiquettes* de ce manuel.

### Onglet Notes

Vous pouvez dans cet onglet enregistrer n'importe quelle information concernant le contact. En général, il est conseillé d'utiliser des champs personnalisés pour des données spécifiques que vous souhaitez collecter auprès de vos contacts. Mais dans certains cas, il peut être utile d'enregistrer quelques notes "telles quelles". Toutefois, ce type d'information n'ayant pas de structure propre, il faut rester prudent quant à son utilisation et avoir le réflexe de consulter régulièrement cet onglet. Les champs d'une note (sujet et contenu) sont libres (pas de format imposé).

Vous pouvez spécifier "Auteur uniquement" pour une note. Dans ce cas, seul l'auteur pourra la lire ou la modifier, ou quelqu'un ayant l'autorisation "Voir toutes les notes" dans CiviCRM.

![Contact_NotesTab](../img/CiviCRM_update-CiviCore-Contact_NotesTab-en.jpg)

### Onglet étiquettes

Les étiquettes sont une possibilité de classer vos contacts dans votre base de donnée (les autres moyens sont les groupes et les données personnalisées). Vous pouvez créer autant d'étiquettes que vous le souhaitez pour gérer votre organisation. Vous pouvez faire des recherches sur les étiquettes et créer des groupes dynamiques basés sur ces dernières.

![Contact_TagTab](../img/CiviCRM_update-CiviCore-Contact_TagTab-en.jpg "Contact_TagTab")

Pour en savoir plus sur ce sujet, veuillez vous référer au chapitre *Groupes et étiquettes* de ce manuel.

### Onglet Journal des modifications

Cet onglet vous donne des informations synthétiques sur les modifications faites sur l'enregistrement d'un contact : la date et l'auteur des changements, mais pas ce qui a été changé.

![Contact_ChangeLog](../img/CiviCRM_update-CiviCore-Contact_ChangeLog-en.jpg "Contact_ChangeLog")


Adding contacts
---------------

The simplest way to add a single contact to CiviCRM is to use the
navigation menu at the top of any non-public page. To create a new
Individual, go to: Contacts > New Individual:

![Contact_createIndividual](../img/CiviCRM_update-CiviCore-Contact_createIndividual-en.jpg "Contact_createIndividual")

Note that the Contacts menu item allows you to create every kind of
contact and contact sub-type.

All of the contact creation forms are similarly arranged, with basic
information (name, email etc) at the top of the form and more specific
fields below grouped by type or subject in accordions (such as address
fields, communications preferences and any custom fields that you have
added for the contact type).

For all contact types you can use the **Check for Matching Contacts**
option to help avoid duplicate entries. After entering all of the
information you have in this section, you can click on **Check for
Matching Contacts.**

*For adding an Individual record to the database, first name and last
name OR email address are required. For adding an Organization or
Household record to the database, just Organization/Household name is
required. You can fill out as many of these fields as you like, and
donâ€™t forget, you can always go back and make changes as needed by
using the edit screen.*

Useful things to know when adding contacts:

Address: You can add multiple addresses to a contact record. This allows
you to store someone's home and work addresses, as well as a billing
address if that's different.

You will see a checkbox here to allow you to share the address of either
an existing contact, or create a new contact. If you select new contact,
you will need to select which contact type you wish to create, and a pop
up box will appear to add the new contact record. When a person uses
another contact's address, that address can only be edited from the
"master contact's" record. 

The options available in the countries dropdown will depend on which
ones you have made available at **Administer > Localization >
Languages, Currency, Locations** under Available Countries.

There may be fields here that you do not need. Available address fields
can be edited at **Administer > Localization > Address settings.**The
"Address Name" field which can be used to label a particular address
(for example "Summer Home") is hidden by default, but can be enabled
from that screen.**
**

Tags and Groups: Here you can specify which tags and groups to add your
contact to. Please note that you may only add to existing groups and
tags with existing tags. You can read more about creating tags and
groups in the Groups and Tags chapter of this book.

Once you have filled out the form, you have the choice of three buttons
to click:

-   Save will save the contact record and take you to the contact
    screen.
-   Save and New will save the contact and clear the form so that you
    can add another.
-   Cancel will discard the entered information and return you to your
    CiviCRM dashboard.

Editing contacts
----------------

Editing information on the summary screen is simple. Hovering in the
upper right corner of the block that you wish to edit will bring up the
**Edit Info** link. You can then edit the information directly in the
summary screen.

If you need to edit a lot information for one particular contact, an
alternative is to open the entire contact for editing by clicking on the
edit button above the tabs.

![image](../img/contact%20Screen%20-inline%20edit.png) 

Note that on the rare occasions that two separate admin users edit a
contact at the same time (specifically that they both open the edit
screen, then both save the contact), the second admin user will be
notified of the first admin user's edit and be given the chance to
manually 'merge' the edits.

Deleting contacts
-----------------

At the top right there is a button to Delete the contact. When a
contact is deleted, it does not disappear completely - instead it moves
to the trash, where it can be recovered at a later date (using the
search in trash feature of **advanced search**). See "searching" under
the "working with your data" chapter for more information). 

Deleted contacts are moved to the "trash" by default (and can be
restored later if needed). There are a variety of ways to delete a
contact:

-   **Single contact**: open the contact's record and click the 'delete
    contact' button at the top of the page. Alternatively, run a search
    for the contact and, from the results list, look toward the end of
    the contact's row, click 'More' and select 'Delete Contact'.
-   **Multiple contacts**: run an advanced search, check the boxes of
    each record you wish to delete (or *select all* with the checkbox in
    the header at the top) and in the 'actions' drop-down menu, choose
    'Delete Contacts' to send the contacts to the trash (if enabled) or
    'Delete Permanently'. A warning page will be displayed to verify
    your intention; simply click 'Delete' to continue or 'Cancel' to
    return to the previous screen.

Contact subtypes 
------------------

In addition to the three default contact types (individuals, households
and contacts), you can define additional contact types (sometimes
referred to as contact subtypes) to suit your needs.

Each contact subtype that you define is based on one of the three core
contact types. For example, 'Student' would based on the 'Individual'
contact type, and 'Farm' could be based on the 'Organization' contact
type, or perhaps 'Household' contact type, depending on your use case.

Contact types are very useful when you need to collect and display
different sets of custom data for different types of contacts (e.g. you
may wish to collect information on the subject area and qualifications
of all teachers in your database but not be interested in collecting
these for other individuals.  To do this, you would create a contact
type called Teacher, based on Individual and then create a custom data
set that only extends Individuals of the type Teacher (see custom data
for more information).

Note that the core contact types are mutually exclusive, i.e. a contact
cannot be an organisation and an individual. However, contacts can be
of more than one user-defined contact subtype, i.e. they could be a
Teacher and a Parent, for example.

To edit existing contact types and and create new contact types go to
**Administer > Customize Data and Screens > Contact Types**. Note that
you cannot delete the inbuilt contact types but you can change their
names and the images associated with them. 

To add custom fields to specific contact subtypes, see the chapter on
custom fields.

Customizing the view of contacts
--------------------------------

After working with the contact editing and summary screens for a while,
you may realise that there are sections and/or fields that aren't useful
for your organisation. The good news is that you can easily hide some
fields and sections. For example, if your organisation doesn't need to
store demographics information, you can remove it by configuring the
Site Preferences. Using an account with Administer CiviCRM privileges.

-   Go to: **Administer > Customize Data and Screens > Display
    Preferences**.
-   Clear the Demographics box under Editing Contacts.
-   Click Save.

You can also use this screen to rearrange the order that the information
is displayed in. 

Similarly, if you want to remove (or add) fields in the postal address
section:

-   Go to: **Administer > Localization > Address Settings**.
-   Check or uncheck fields under Address Editing.
-   Click Save.

If you think that some of the tabs are not useful and will not be used
in your deployment, you can disable or enable specific tabs from
**Administer > Customize Data and Screens > Display Preferences**. If
you don't see some of the tabs described below, you may need to enable
them. The visibility of some tabs is dependent on which components are
enabled in your installation. For example, the Contributions tab will be
hidden if the CiviContribute component is disable.
