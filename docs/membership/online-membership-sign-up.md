Adhésion des membres en ligne
=========================

Ce chapitre explique comment permettre aux visiteurs de votre site Web de s'inscrire en tant que membres de votre organisation. Nous examinerons les étapes nécessaires pour créer des pages d'abonnement d'adhésion, certaines éléments sont à considérer lors de cette opération, y compris le test de vos pages d'adhésion et la façon dont vous pouvez integrer les pages d'adhésion sur votre site public.    

Avant de lire ce chapitre, il est souhaitable d'avoir pris connaissance du chapitre *Définir les adhésions* qui donne un panorama utile à de nombreux concepts (comme les types d'adhésion, les statuts de l'adhésion, etc.).

À propos des pages d'adhésion
-------------------------------------------

Les pages d'adhésions sont créées de la même manière que les pages de contribution en ligne. Essentiellement, vous créez une page de contribution en ligne, puis ajoutez à cette page la possibilité d'adhésion. La raison pour laquelle nous faisons cela est parce que la méthode réelle pour devenir membre d'une organisation est normalement assez similaire à la méthode de contribution financière à une organisation. Les lier ensemble permet aux pages d'adhésion de profiter d'une grande partie de la fonctionnalité qu'ont les pages de contribution, par exemple, vous pouvez offrir des cadeaux dans le cadre de nouvelles adhésions.

Notez que, même si votre adhésion est gratuite, vous devez toujours utiliser une page de contribution pour l'adhésion en ligne (voir les adhésions gratuites ci-dessous pour obtenir les instructions sur la façon de le faire).

Les pages de contribution sont très puissantes et ont de nombreuses options regroupées en onglets. Dès que vous avez donné un nom à votre page de contribution, ces onglets sont affichés en haut de la page lorsque vous travaillez dans le reste du processus de configuration.

![image](../img/membership-tabs.png)

Dans ce chapitre, nous nous concentrerons sur les onglets et les options des pages de contribution qui sont les plus utiles pour les adhésions. Quelques onglets méritant d'être mis en évidence incluent l'onglet Adhésions, contenant la majeure partie de la configuration de l'adhésion. L'onglet Profils vous permet de collecter des informations sur les personnes ou les organisations qui remplissent votre formulaire d'adhésion.

Nous vous recommandons également de consulter les chapitres sur la création de [pages de contribution en ligne](.../ contributions/contributions en ligne) qui vous permettront de mieux comprendre tous les outils dont vous disposez lors de la création de pages d'adhésion.
- Menu : Adminitrer>civi contribute>Nouvelle page de contribution

### L'onglet Titre  

L'onglet titre (c'est la première page que vous voyez lorsque vous créez une nouvelle page d'adhésion) vous permet de définir le titre de la page d'adhésion et de définir certaines informations de base comme le type financier, etc., qui seront enregistrées pour les adhésions qui sont réalisées par cette page.

Cet onglet vous permet également d'inclure un message d'introduction à afficher sur votre page d'adhésion. Vous pouvez inclure des images et du code HTML simple dans ce texte d'introduction.

### Cotisation au nom d'une organisation

L'onglet titre contient une case à cocher "*Permettre aux individus de contribuer et/ou d'adhérer au nom d'une organisation*" qui  permet  aux utilisateurs d'identifier une organisation comme donateur ou adhérent, ce qui est la manière recommandée d'offrir des adhésions aux organisations. La contribution ou l'adhésion sera attribuée à cette organisation. Lorsque cette case est activée, l'utilisateur est invité à sélectionner un profil (voir le chapitre des profils pour plus d'informations) utilisé pour collecter des informations sur l'organisation. Cette inscription pour une organisation peut être facultative ou obligatoire.
Une fois cette page remplie cliquer sur **Suivant**

![image](../img/Title%20settings%201%20.jpg)

### L'onglet Montant 

L'onglet des montants vous permet de définir diverses options financières, y compris le processeur de paiement qui est utilisé sur la page. Notez que vous pouvez sélectionner plus d'un processeur de paiement pour donner le choix aux personnes qui acceptent. Pour plus d'informations sur la configuration des processeurs de paiement et sur les points à considérer lors du choix d'un processeur de paiement, voir le chapitre *Processeurs de paiement*.

![image](../img/contribution%20amounts.jpg)

Notez que l'onglet des montants *n'est pas* l'endroit où les frais d'adhésion sont configurés : ils sont configurés dans l'onglet Adhésions. Si vous souhaitez utiliser cette page pour collecter des montants d'adhésion et *ne* souhaitez pas solliciter des contributions supplémentaires, laissez la case **Section des montants de contribution activée** non cochée. Si vous *désirez solliciter des contributions en plus des frais d'adhésion*, cochez la case et ajoutez des options de contribution proposées ou configurez un ensemble de prix de contribution*.

### Adhésions gratuites

Si vous offrez **Adhésions gratuites**, vous devez laisser la boîte "Exécuter des transactions monétaires en temps réel" non cochée et choisir un type d'adhésion avec un tarif minimum de valeur zéro.

### L'onglet Adhésions

Puisque nous utilisons cette page de contribution pour l'inscription et le renouvellement des adhésions, nous devons vérifier la **Section d'adhésion activée** pour utiliser cette page de contribution pour les adhésions.

Les zones de texte (Message d'introduction — Nouvelles adhésions et Message d'introduction — Renouvellements) vous permettent d'ajouter du texte qui sera affiché lorsque cette page est utilisée pour l'inscription initiale et pour les renouvellements. Lorsqu'un utilisateur enregistré avec une adhésion actuelle ou expirée affiche la page d'inscription de membre, CiviCRM remplace automatiquement la page d'inscription de membre par une page de renouvellement d'adhésion qui contient le texte de la zone de renouvellement.

![image](../img/membership%20signup%201.jpg)

Après ces zones de texte, vous trouverez quelques options que vous pouvez utiliser pour configurer les types d'adhésion disponibles sur le formulaire d'adhésion.

![image](../img/MembershipTabOnlineCintribConfiguration.PNG)

Envisagez d'abord les cas d'utilisations simples. Sélectionnez les types d'adhésion qui devraient être disponibles sur la page, ceux qui devraient être par défaut et qui peuvent être renouvelés automatiquement (vous devrez configurer vos types d'adhésion comme renouvellement automatique avec un processeur de paiement qui supporte les paiements périodiques automatiques).

Si vous activez le renouvellement automatique pour une adhésion, puis sur la page Web, les utilisateurs verront "Veuillez renouveler mon abonnement automatiquement". (*Vos frais d'adhésion initiaux seront traités une fois que vous aurez terminé l'étape de confirmation. Vous pourrez annuler les renouvellements automatiques à tout moment en vous connectant à votre compte ou en nous contactant*)". Les e-mails de réception de paiement d'adhésion incluentt un lien pour que le membre annule le renouvellement automatique.

Si vous le souhaitez, vous pouvez avoir une inscription d'adhésion optionnelle. Ceci est souvent utile si vous avez une page de contribution sur laquelle vous souhaitez offrir la possibilité de devenir membre, mais ne l'exigez pas (vous devrez cocher la case "Section des montants des contributions activés" dans l'onglet Montants). Vous pouvez décider si ces paiements sont enregistrés séparément des paiements des frais d'adhésion.

Si vous ne pouvez pas réaliser ce dont vous avez besoin en utilisant les "Types d'adhésion" (par exemple, si vous souhaitez offrir un abonnement à deux adhésions en même temps ou créer des inscriptions avec plusieurs statuts d'adhésion), vous devez utiliser un ensemble de prix d'adhésion (voir le chapitre *Gestion des tarifications*).

Ce que vous pouvez faire avec la Gestion des tarifications :

-   Permettre  aux utilisateurs de s'inscrire à plusieurs types d'adhésion en même temps(par exemple, les adhésions «nationales» et «locales») 
-   Permettre aux utilisateurs de se connecter à plusieurs statuts d'adhésion en même temps
-   Offrir d'autres options telles que la souscription à des options payantes en plus de l'adhésion. 

### L'onglet Réception

Une fois que le visiteur du site a complété le formulaire d'inscription ou de renouvellement de l'adhésion, il sera redirigé vers une page de remerciement et pourra recevoir un reçu électronique généré et envoyé automatiquement. Cette quatrième étape vous permet de configurer cette option. Vous pouvez personnaliser le message qui s'ajoute au reçu d'adhésion sur cette page et l'adresse électronique d'envoi du reçu. Si vous souhaitez personnaliser davantage le modèle de courrier électronique de réception, vous pouvez le faire en utilisant l'écran **Civimail> Modèles de messages**.

Vous pouvez également choisir l'envoi "CC ou BCC" pour chaque reçu d'adhésion à un membre du personnel afin qu'ils soient alerté immédiatement chaque fois que quelqu'un devient membre.

![image](../img/membership%20page%20receipt%201.jpg)

![image](../img/membership%20page%20receipt%202.jpg)

### L'onglet Recommander à un ami


CiviCRM allows you to add a tell-a-friend feature to the thank-you page.
The page lets your members share details about your organization with
their friends by emailing them a link and information. Those friends
that are told about the membership sign up will also be added to CiviCRM
if they do not already exist and their source field will show that they
were added via tell-a-friend.

![image](../img/tell%20a%20friend.jpg)

###Collecting information as part of membership sign up (the Profiles tab)

You can use profiles to collect information about your members as they
fill in the sign up form. By default, contribution pages will include
only an email field. Adding a profile to the contribution form will add
a collection of fields that CiviCRM will display as part of the
membership sign up form. You can use profiles to collect extra
information about the contact, for example their address, their
interests, etc. If the person signing up to become a member is logged
in, their profile fields will be populated with data from CiviCRM where
available. Don't add a membership profile. Collection of that
information occurs automatically during the online membership sign up
process.

![image](../img/membership-profiles.png)

The profiles tab allows you to select an already existing profile to
include on your membership page, and if you have permission, to edit an
existing profile or create a new profile to be included on this page.
**WARNING:** If you edit an existing profile here, it will be changed in
all places where that profile is used.

###Premiums tab

Premiums are thank you gifts and incentives offered to people that
donate to your organisation. They are most commonly associated with
tiered donation levels (e.g. donate $50 to receive a T-shirt) but can
also be used in conjunction with your membership pages. Before
including premiums on a contribution page, you must configure them
through **Contributions > Premiums (Thank-you Gifts)**.

The Premiums tab of the contribution page wizard controls the
introductory text, contact information, and other premium-related
details.

![image](../img/membership-profiles.png)

Testing membership sign up pages
--------------------------------

Once you finish configuring and setting up your membership page, you are
advised to test drive the process to make sure everything is working
according to your expectations. Test functionality is available on
**Contributions** > **Manage Contribution Pages**, click **Links** next
to your membership sign-up/renewal page and click **Test-drive**. Any
membership data you send through the form in test mode will be added to
CiviCRM as test data and not be included in any membership stats or when
searching for members, etc. If you want to find and delete test
memberships, you can do so by clicking the 'is test' check box in **Find
Memberships**.

Try and put yourself in the eyes of someone who wants to become a member
of your organisation and go through the process a number of times, with
different combinations of fields each time. Make sure that the data all
appears as you would expect in CiviCRM. Once you've tested the process
and have made any necessary changes, get other members of staff or
friends from outside your organisation to test the process.

When using the Test-drive Registration option, you see the same
registration pages as a regular user, but the online payment isn't
really debited from your card (see *Payment processors*for more
information on dummy processors and card details you can use for test
transactions).

It is worthwhile periodically testing and reviewing your membership
process to make sure that it is as smooth as possible. You will receive
indirect feedback from your members as they use the form. If they are
not entering data in the way you intended then you will need to make
some changes. From time to time, you may want to solicit direct
feedback from people who have recently become members to see how easy it
was for them to become a member and ask their opinions on ways in which
you could improve your form.

Adding membership sign up pages to your website
-----------------------------------------------

Once you've made your contribution page, you need to make it visible on
your website. The method for this depends on the CMS. Instructions for
each CMS are below.

Membership sign up pages are built to inherit your website theme and
should look reasonably nice out of the box. You can include images on
the HTML text areas in the page to make them look more attractive. Many
organisations want to spend time improving the look and feel of their
membership pages in order to increase membership sign up rates. The
methods for changing the design of these pages are outside the scope of
this book but a website designer who is familiar with your CMS and
CiviCRM will be able to help.

### In Drupal

Go to **Contributions** > **Manage Contribution Pages** > click
**Links** next to your membership sign-up/renewal page > click **Live
Page** to view the finished page. You can then copy the URL and include
it in a content page or assign it to a menu item.

### In Wordpress

Go to **Contributions** > **Manage Contribution Pages** > click
**Links** next to your membership sign-up/renewal page > click **Live
Page. **Copy the URL and insert it into an HTML link or menu.

*Or* use a plugin such as Page Links To create a URL 'slug'.

*Or* click the Wordpress shortcode icon to insert a form into any page
or post.

![image](../img/Wordpress-Shortcodes-small.png)

### In Joomla!

The most direct way to expose your membership signup/renewal page to the
front of your website in Joomla is by creating a menu item.

-   Navigate to a menu and create a new CiviCRM item.
-   From the list of menu options, choose Contributions.
-   In the basic parameters section, select the contribution page you
    would like exposed from the dropdown menu.
-   Save the menu item and view the website to confirm the page's
    functionality.

Permissions needed for online membership sign up/renewal.
---------------------------------------------------------

Anonymous and Authenticated roles need the following CMS permissions to
be able to join or renew online:

-   Profile listings and forms: This will let you collect core contact
    information ( name, address etc.) when people sign up.
-   Access all custom data: You must enable this permission to collect
    custom data.
-   Make online contributions: This permission must be granted unless
    your memberships are free and you have no interest in accepting
    donations when people sign up or renew.
