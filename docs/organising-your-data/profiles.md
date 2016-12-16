# Profils

Un profil est une sélection de champs de votre base de données. Les profils sont un outil puissant qui ont de nombreuses utilisations différentes dans tous les composants de CiviCRM. Les profils sont utilisés pour collecter des données (par exemple, sur un formulaire d'inscription) et pour afficher des données à l'utilisateur (par exemple, en tant que liste de membres). Ils peuvent être utilisés à la fois en interne (par exemple, pour créer des écrans de saisie de données simplifiés pour le personnel) et à l'externe (pour afficher des informations actualisées de la base de données).

Vous pouvez ajouter tous les champs de base et personnalisés à un profil, y compris les champs personnalisés à plusieurs valeurs. Il y a également quelques autres champs spéciaux que vous pouvez ajouter aux profils, à savoir, Groupes, qui inclura toutes les cases à cocher (une pour chacun de vos groupes publics)  et des étiquettes, qui incluent toutes les étiquettes  publiques.

En créant un Profil, vous êtes en mesure de sélectionner et de choisir uniquement les champs pertinents dans un but spécifique. Le diagramme ci-dessous fournit une explication visuelle de la façon dont les champs existants deviennent une partie d'un profil.

![Profiles](../img/CiviCRM-Icons-db1-en.png "Profiles")

Cette section explique comment utiliser les profils pour collecter et partager des données ainsi que plusieurs façons d'utiliser des profils permettant de gagner du temps pour toute personne qui gère des données dans votre organisation.

## Différentes utilisations des Profils

Cette section décrit brièvement plusieurs façons dont les profils peuvent être utilisés. Vous trouverez des instructions détaillées pour créer et utiliser les profils plus loin dans ce chapitre.

### Collecte d'informations sur les pages publiques

Un profil peut être utilisé pour recueillir des informations auprès de vos membres ou du public. Les profils peuvent être affichés sur des pages autonomes ou incorporés dans des pages de contribution, d'inscription de membre ou d'enregistrement à un événement. Vous pouvez ajouter plus d'un profil sur une page. Vous pouvez également choisir les champs requis et ajouter du texte dans le profil pour aider les utilisateurs à remplir le formulaire.

Exemples:

- Un formulaire d'inscription de volontaires contenant les champs prédéfinis pour le prénom, le nom de famille, l'adresse postale et un champ personnalisé pour les motivations des volontaires.
- Un profil contenant des champs personnalisés sur les préférences alimentaires qui peut être ajouté aux pages d'inscription pour tout événement où des repas seront servis.

Dans l'exemple ci-dessous, un profil est utilisé pour recueillir des informations d'adresse sur une page de don.

![image](../img/baykeeper-profile.png)

### Affichage d'informations sur les pages publiques

Un profil peut afficher des informations, à partir de la base de données, sur des pages publiques. Cela permet d'économiser du temps, car vous n'avez plus à saisir des informations dans votre base de données, plutôt que dans votre base de données *et* sur votre site Web.

Par exemple, une organisation peut afficher un répertoire d'adhérents consultable sur son site Web, mis à jour automatiquement dès qu'un nouveau membre est enregistré. De même, une organisation qui veut remercier ses donateurs publiquement peut inscrire leurs noms sur une page Web dès que les contributions sont versées.

Une mini étude de cas: Native Americans in Philanthropy (NAP) voulait créer un répertoire d'adhérents que leurs membres pourrait utiliser pour rechercher et se connecter les uns avec les autres. Avant CiviCRM, ils créaient un répertoire d'impression annuel très coûteux et l'envoyait par la poste à chaque membre. Ce processus était long et onéreux, et certaines données étaient périmées avant que les membres ne reçoivent leur répertoire. L'utilisation d'un profil consultable sur leur site Web a généré d'importantes économies de ressources. Le site Web est devenu un portail permettant aux membres de se connecter entre eux et a contribué à faire progresser leur mission dans de meilleures conditions.

Les détails sur l'utilisation des profils de cette façon sont inclus plus loin dans ce chapitre.

### Personnalisation de votre interface utilisateur

Les formulaires de profil peuvent également être utilisés comme formulaires simplifiés de saisie de données. Si vous avez des bénévoles ou des stagiaires qui effectuent une saisie manuelle de données pour votre organisation, vous pouvez faciliter leur tâche en créant un formulaire de profil qui ne montre que les champs dont ils ont besoin pour saisir. Cela simplifie grandement la saisie des données et réduit la possibilité de saisie incorrecte des données.

Vous pouvez également utiliser un profil pour afficher les champs sélectionnés dans les résultats d'une recherche avancée. Par exemple, vous pouvez créer un profil qui inclut le champ numéro de téléphone et un champ personnalisé pour les intérêts des bénévoles. Lorsqu'il est utilisé pour afficher les résultats de recherche, il proposera une liste de contacts à appeler pour votre coordonnateur de bénévolat.

Les détails sur l'utilisation des profils de cette façon sont disponibles dans le chapitre *Personnaliser l'interface utilisateur* de *Configuration initiale*.

### Mise à jour de plusieurs enregistrements en même temps

Il est souvent nécessaire de mettre à jour un grand nombre d'enregistrements à la fois. Par exemple, après un événement, vous pouvez avoir une liste de présence importante, et vous voulez enregistrer toutes les personnes inscrites comme Présent ou Absent mais aussi mettre à jour le champ de remerciement envoyé pour une semaine de dons...cela en une seule fois 

Les actions qui vont vous permettre de mettre à jour plusieurs enregistrements en même temps sont disponibles dans le menu déroulant **Actions** pour la plupart des types de résultats de recherche. (Recherche, Recherche avancée, Rechercher des contributions, Trouver des membres, Rechercher des participants et Rechercher des activités) et des listes de participants à l'événement générées à partir de l'écran Gérer les événements.

La fonction **Update multiple ...** affiche une vue de vos résultats de recherche contenant les champs de votre profil et vous permet de modifier le contenu des champs sur un seul écran et de les enregistrer tous à la fois. Les détails sur l'utilisation de profils de cette façon sont inclus plus loin dans ce chapitre.

### Gérer les listes de courriels

Une autre utilisation de Profils est de présenter un formulaire où les personnes peuvent s'inscrire pour recevoir des courriels, newsletter et diverses infos de votre organisation. Les groupes que vous utilisez pour suivre des listes de diffusion différentes peuvent être ajoutés sous forme de cases à cocher et lorsque les visiteurs de votre site Web soumettent le formulaire, ils sont automatiquement ajoutés aux listes de courrier électronique qu'ils ont cochées.

Pour plus d'informations sur l'utilisation des profils pour gérer les listes de diffusion, reportez-vous au chapitre *Configuration* de la section *Email* de ce manuel.

## Planification de vos profils

Parce que les profils peuvent être utilisés à des fins différentes, il ya beaucoup de choix à faire et de paramètres à configurer lors de leur mise en place. Il ya des paramètres pour le profil dans son ensemble et des paramètres pour chaque champ que vous ajoutez, ainsi que le choix de ces champs. Les choix que vous faites sur un aspect affecteront les choix que vous pouvez faire sur les autres. Par exemple, certains types de profils limitent les types de champs que vous pouvez inclure et certaines combinaisons de champs ne sont autorisées dans aucun type de profil. En raison de cette complexité, il est important de comprendre les conséquences de certains paramètres et de planifier soigneusement ce que vous utiliserez dans votre profil et ce dont vous avez besoin avant de le créer. Vous devrez peut-être faire probablement quelques essais ou erreurs avant de trouver la bonne solution pour réaliser votre objectif.

Voici quelques conseils sur les champs qui peuvent être ajoutés à un profil:

- Les profils utilisés pour les affichages de recherche peuvent contenir uniquement les champs des enregistrements de contact (et les différents types de contact, par exemple individuels).
- Les champs de contact sont disponibles dans tous les profils. Toutefois, vous ne pouvez pas mélanger les champs de différents types de contact (par exemple, individuel et organisation).
- Pour ajouter des champs (comme l'adresse ou l'e-mail) qui s'appliquent à plusieurs types de contacts, choisissez les champs de Contacts plutôt que le type spécifique. Le menu des champs Organisation, par exemple, contient uniquement les champs qui ne s'appliquent pas également à d'autres types de contacts.
- Sauf dans les profils de résultats de recherche, vous pouvez combiner les champs de contact avec les champs d'un et d'un seul autre type d'enregistrement : Activité, Participants, Contributions et Adhésion.
- Si vous essayez de combiner des champs avec une combinaison non prise en charge de types d'enregistrements, vous obtiendrez une erreur lorsque vous essayez d'enregistrer le champ.

## Création et gestion de profils

La création d'un profil est un processus en plusieurs étapes. Tout d'abord, vous créez le profil et choisissez ses paramètres. Il existe des paramètres de base et des paramètres avancés. Ensuite, vous ajoutez les champs et choisissez également ses paramètres.

### Création d'un profil et compréhension des paramètres de profil

Cette section vous guide à travers tous les paramètres du profil et explique comment ils affectent le fonctionnement de vos profils. Comme vous le voyez, vous pouvez remarquer que la liste des paramètres est assez longue. Il est important de comprendre que la plupart des paramètres s'appliquent uniquement à un type d'utilisation de profil. Chaque fois que vous créez un profil, vous serez en mesure d'ignorer de nombreux paramètres, car ils ne s'appliquent pas à votre utilisation prévue.

1. Allez dans : **Administrer> Personnaliser les données et les écrans> Profils** et cliquer sur **Ajouter un profil**.
2. **Nom du profil** : Donnez au profil un nom significatif.
3. **Utilisé pour** : Vos choix sont "Formulaire ou liste autonome" ou "Vue des résultats". Vous pouvez cocher plusieurs cases dans ce champ pour rendre votre profil disponible à plusieurs utilisations. N'oubliez pas que la vérification des "Vues de résultats" limitera vos choix de champ aux enregistrements de type Contact et Contact uniquement.
4. **Numéro d'ordre** : Ce champ détermine l'ordre dans lequel les profils sont présentés lorsque plusieurs profils sont inclus dans une page. Les nombres inférieurs sont affichés devant des nombres plus élevés. Le champ est automatiquement rempli lors de la création d'un Profil. Changer le nombre si vous le souhaitez.
5. **Aide avant formulaire** et **Aide après formulaire** : Ces champs vous permettent d'écrire du texte qui apparaît avant ou après votre profil pour guider les utilisateurs à remplir les formulaires.
6. **Ce profil CiviCRM est-il actif ?** : Cette case est cochée automatiquement. C'est ce qui permet au profil d'apparaître comme options pour l'insertion dans des formulaires et l'utilisation de la fonction de mise à jour de lot. Lorsque vous créez des profils, vous devez évidemment la laisser cochée. Ultérieurement, si vous souhaitez supprimer un profil vous pouvez modifier le profil et désélectionner cette case.

### Paramètres avancés

Les profils ont un certain nombre de paramètres avancés qui sont applicables dans des contextes différents. Tout ce qui est répertorié sous Paramètres avancés s'applique à tous les profils. Certains ne s'appliquent qu'à des utilisations spécifiques du profil. Vous pouvez ignorer tous les paramètres qui ne s'appliquent pas à la façon dont vous utiliserez votre profil. Pour accéder aux paramètres avancés, cliquez sur la barre de paramètres avancés gris et un ensemble de champs apparaîtra

#### **Restreindre les listes à un groupe spécifique ?**

Ceci est important uniquement pour les profils qui seront utilisés pour afficher des informations sur votre site Web (par exemple, si vous autorisez les visiteurs Web à rechercher vos données, comme dans un répertoire d'adhésion).

1. Sélectionnez le groupe dont vous voulez afficher les informations à partir du menu déroulant de ce champ. Par exemple, si vous souhaitez afficher un répertoire de membres actifs, créez un groupe dynamique de tous les membres ayant un statut de nouveau, de courant et de grâce.
2. Choisissez le groupe intelligent dans ce champ. (Rappelez-vous que les groupes dynamiques sont des listes d'enregistrements et lors de l'ajout de nouvelles appartenances, le contact correspondant sera automatiquement inclus dans le répertoire.)
3. Si vous ne choisissez pas un groupe dans le menu déroulant de ce champ, par défaut CiviCRM permettra une recherche pour afficher chaque enregistrement de votre base de données. Dans la plupart des cas, c'est une très mauvaise idée !, car vous ne voulez probablement pas que n'importe qui, visitant votre site Web, sache qui est dans votre base de données entière.

#### **Ajouter de nouveaux contacts à un groupe**

Tous les *nouveaux* contacts qui remplissent ce profil seront ajoutés a un groupe. Vous pouvez, par exemple, ajouter une personne qui remplit votre formulaire d'inscription à un groupe de bénévoles. Notez que par défaut, les contacts ne reçoivent aucune confirmation quand ils ont été ajoutés à ce groupe ou quand ils doivent valider leur adresse électronique. Pour que les contacts qui remplissent le formulaire de profil reçoivent un courriel, allez à **Administer > CiviMail > CiviMail Component Settings** et cochez la case **"Activer le double opt-in pour les profils qui utilisent le paramètre "Ajouter au groupe" "**. Ils doivent répondre (opt-in) avant d'être ajoutés au groupe.

![Screen shot of dobule opt-in setting](../img/organizing-data-double-opt-in.png)

Notez que si vous souhaitez proposer plus d'un groupe, il est préférable d'utiliser le champ Profil de groupe.

#### **Notifier quand le formulaire de profil est envoyé**

Ce paramètre, qui est applicable uniquement lors de l'utilisation d'un profil en tant que formulaire d'inscription, vous permet d'envoyer un message automatiquement chaque fois que le formulaire est envoyé. Par exemple, votre coordonnateur des bénévoles peut vouloir envoyer un courriel chaque fois que quelqu'un remplit le formulaire d'inscription des bénévoles. Entrez simplement l'adresse e-mail dans le champ. Si vous souhaitez envoyer un e-mail à plusieurs adresses, séparez-les par une virgule.

#### **URL de redirection**

Ceci s'applique uniquement aux profils qui sont utilisés comme des formulaires autonomes. La redirection ne s'applique pas lorsque le profil est incorporé dans un formulaire d'inscription ou de contribution. Le champ URL de redirection vous permet de diriger les personnes vers une page Web spécifique après avoir soumis un formulaire. Par exemple, vous pouvez créer une page Web qui remercie les gens de soumettre leurs informations. Si ce champ est laissé vide, les gens seront dirigés vers une page qui affiche les informations qu'ils viennent d'entrer.

#### **Annuler l'URL de redirection**

S'exécute exactement de la même manière que l'URL de redirection, sauf qu'elle s'applique lorsque les utilisateurs annulent leur soumission de formulaire.

#### **Inclure reCAPTCHA ?**

Concerne lorsque les profils sont remplis par des utilisateurs anonymes. CAPTCHA est un type de logiciel anti-spam qui oblige le visiteur à remplir le texte affiché dans un fichier graphique. Cela empêche les robots automatisés de naviguer sur le Web et de remplir un formulaire. Il est fortement recommandé de l'inclure.

Vous devez configurer un compte reCAPTCHA et saisir quelques informations de configuration dans CiviCRM pour utiliser cette fonctionnalité. Allez dans **Administer> Paramètres système> Undelete, Logging et ReCAPTCHA** pour configurer votre compte. Les instructions d'inscription sont incluses sur cette page.

#### **Option d'enregistrement de compte utilisateur Drupal**

Ce paramètre s'applique aux profils qui sont utilisés dans les pages publiques et détermine si les personnes peuvent ou doivent utiliser votre formulaire pour avoir un compte utilisateur sur votre site Web avant de soumettre les informations du formulaire. Cela peut être utile pour s'assurer que les personnes qui doivent s'inscrire à un compte d'utilisateur peuvent devenir membre ou s'inscrire à un événement.

#### **Option d'inscription au compte utilisateur WordPress**

Comme Drupal, Wordpress permet aux profils CiviCRM de créer des comptes comme décrit ci-dessus. Dans WordPress **Paramètres> Général** "Adhésion [] N'importe qui peut s'inscrire" doit être cliqué.

Traduction en cours :

#### **What to do upon duplicate match**

This setting applies to Profiles that are used in public pages.
It controls what happens when the contact data submitted from the
Profile matches an existing contact record. You must choose one of these
options. "Issue warning and do not save" is chosen by default. Matching
in Profiles uses on the **Unsupervised** deduplication rule (see the
*Deduping and Merging* chapter in the *Working with Your Data* section
for more information about deduplication rules). Note that if there are
multiple matching contacts, the first matching record is used.

Here are the options and their effects how your form works:

-   "Issue warning and do not save" This option is ignored if the
    Profile is embedded in an online contribution, membership sign-up or
    event registration form. In these cases, a contact match results in
    the transaction being linked to the matching contact. In other
    cases, the user will receive a message that a record already exists
    in the database, and they will be unable to submit the form.
-   "Update the matching contact" adds new information from the form to
    the contact record and, if there are any form fields that are
    already filled-out in the record, overwrites the existing record
    fields. For example, if the form includes address fields, the text
    that the user enters in the form will replace what was already in
    the database address fields.
-   "Allow duplicate contact to be created" ignores any potential
    matches and creates a new contact record for all submitted forms.
    This means that all form submissions will be saved and no data will
    be overwritten; however, it may produce a lot of duplicate records
    that will need to be deduped later (see the *Deduping and Merging*
    chapter in the *Working with Your Data* section).

#### **Proximity search**

This applies if you are using the Profile for a searchable
directory; it adds a proximity search block to the search criteria. This
block contains a field for start address, and another that allows the
user to set a search radius (how far from the start address they want to
search). Choose None if proximity search is not relevant to your
directory, Optional if you want to offer proximity search to your users,
and Required if you want to force the user to enter a start address and
a search radius.

#### **Enable mapping for this profile?**

This applies only if you are using the Profile for a searchable
directory; it adds a map to the search results.

#### **Include profile edit links in search results?**

This applies only if you are using the Profile for a searchable
directory; it adds a link in the results listings to edit the Profile
fields in the returned contact records. Only users with permission to
edit the result contacts will see this link.

#### **Include Drupal user account information links in search results?**

This applies only if you are using the Profile for a searchable
directory; it includes a link in the results to the resulting contacts'
Drupal user account information (i.e., their My Account page). This link
will be included for only result contacts who have a user account on
your website.

Once you've saved the profile settings, it's time to add fields to the
profile. If you plan to reference custom fields in a profile form, make
sure that those fields have already been created.

## Adding fields and choosing field settings in Profiles

This section walks you through all the field settings and explains how
they affect how your Profiles work. As with the overall Profile
settings, not all of them are necessary to consider for each use.

1.  Click **Add Field**.
2.  **Field Name**: Choose the record type where your desired field
    appears from the **- select -** dropdown menu. This will bring up a
    secondary dropdown menu listing all available fields for that record
    type. Choose the field you want to add to your Profile.
3.  **Field Label**: This is the field label that will display on all
    uses of your Profile. It is prefilled with the default field label.
    However, the default field labels are often confusing for users of
    your forms, so you can rewrite them here. For example, the Postal
    Code field can be renamed Zip Code if your audience is more familiar
    with that term.
4.  **Required?**: Check this box to make this required anytime the
    Profile is used. This is most useful when you want to make sure that
    certain information (e.g., First Name, Last Name, Email) is always
    included in a form submission. (This is not relevant to Search Views
    usages [known as Search Results in 4.1 and previous].)
5.  **View Only?**: Check this box to allow users to view but not edit
    this field. If your Profile is used to expose search results, fields
    marked View Only will not be included. This setting is not relevant
    when a Profile is being used only to collect information.
6.  **Visibility**: If the Profile is being used for a searchable
    directory, set the Visibility of any fields you want to include on
    the search form to Public Pages or Public Pages and Listings. For
    fields that will be used on sign-up forms, set Visibility to User
    and User Admin only. This ensures that other visitors to the form
    can't view any data from the database. To use fields for Search
    Views, you must set Visibility to Public Pages or Public Pages and
    Listings. Choosing either of the Public Page options pops up two
    additional settings:
    -   **Searchable?**: This applies only to searchable directory uses.
        Check the box if you want to include the field in the search
        form.
    -   **Results Column?**: This applies only to Search Views (known as
        Search Results in 4.1 and previous). Check it or the field will
        not appear in your Search View.

7.  **Field Pre Help** and **Field Post Help**: These fields allow you
    to write text that appears in the user interface to guide people in
    filling out forms. Field pre help appears inline. Field post help
    will create a small speech bubble which when clicked appear in a
    yello
8.  **Order**: You can use this field to control the order in which
    fields display in the Profile. Lower numbers are displayed ahead of
    higher numbers.
9.  **Active?**: Leave this box checks to ensure that the field appears
    when the Profile is used.
10. Click **Save and New** to add more fields to the Profile, or
    **Save** if you have no more fields to add.

## Managing Profiles

All your profiles are available for viewing and editing at **Administer > Customize Data and Screens > Profiles**. You can add fields and edit
field settings (at the **Fields** link) and change Profile settings (at
**Settings**). You can also look at how your Profiles will appear, get
links and embed code for your Profiles, and copy Profiles to use as a
basis for building other Profiles (at **more**).

## Using Profiles

This section contains specific instructions for the different profile
uses discussed above.

### Standalone forms with Profiles

There are two ways in Drupal and Joomla! to use standalone forms once
you have created your Profile according to the instructions above:

-   Use the page created automatically by CiviCRM to hold the Profile.
    Get the link to this page at **Administer > Customize Data and
    Screens > Profiles**. Click the **more** link next to your Profile
    and choose **Use Profile-Create Mode** from the pop-up menu. You can
    then publish this link wherever you want: in an email, on a blog,
    etc.
-   Paste the HTML code for the form in a page you've built on your
    website. Get the code at **Administer > Customize Data and Screens > Profiles**. Click the **more** link next to your Profile and
    choose **HTML Form Snippet** from the pop-up menu. Copy the code
    that appears on the next screen and paste it wherever you want.

In WordPress, there is an additional third way. When creating or editing
a post, click on the CiviCRM button to insert a CiviCRM shortcode into
the post.

![image](../img/2013-09-04_15-29-47_1.png)

On the popup form, select Profile as the desired frontend element.

![image](../img/2013-09-04_15-15-35.png)

Use the second select widget to specify the profile you would like to
use. Finally, select the purpose of the form — create, edit or view —
and click Insert Form.

![image](../img/2013-09-04_15-16-45.png)

### Multi-value fields in profiles

Multi-value custom field sets allow you to have more than one set of
custom data per contact. They are handy for modelling data that repeats,
for example, work experience data. You can expose these multiple value
custom fields via profiles. In the screen shot below, we have created a
profile that is used to collect name and work experience data. Notice
that the multi-value custom data appears slightly differently in the
profile to facilitate adding, editing and deleting multiple instances of
these records.

![image](../img/multi-value-profile.png)

### Making directories with Profiles

To put a directory onto your website:

1.  Create your Profile as described above. Be sure to consider these
    Advanced Settings, as they are especially helpful when using
    profiles for directories.

 -   **Enable mapping**: a really cool feature available in CiviCRM is
     giving visitors the ability to map contacts in your directory
     using Google or Yahoo! maps. They can then obtain directions to a
     record's address dynamically. To use this feature, you must have
    already enabled mapping under **Administer > System Settings >
     Mapping and Geocoding**.
 -   **Include profile edit links:** check this box if you want to
     include a link in the directory listings to allow people to edit
     data in the profile's fields. Only users with permission to edit
     the contact will see this link. More often than not you will not
     need to enable this setting, as it is not commonly used in the
     membership directory scenario.
 -   **Include Drupal user information** (Drupal only): check this box
     if you want to include a link in the directory listings to view a
     contacts' Drupal user account information (e.g. their My Account
     page). This link will only be included for contacts who have a
     user account on your website.

    ![profile_adv_settings](../img/CiviCRM-CapturingExposing-buildprofile-profile_adv_settings-en.jpg "profile_adv_settings")

Now it's time to include the fields that will make up the directory. For
profiles used as directories you have total control over which fields:

-   are searchable in the directory
-   appear in the results columns of your search
-   appear in the record detail View page.

The important options you must configure in the fields for directory
purposes are shown below:

![directory_fields](../img/CiviCRM-CapturingExposing-buildprofile-directory_fields-en.jpg "directory_fields")

-   Visibility for all fields in your directory must be set to **Public
    Pages** or **Public Pages and Listings**. The difference between these
    two options is that those configured as Public Pages and Listings
    will have the field in detail view hot-linked, enabling the user to
    generate a follow-up search for other records which also have that
    same field value. For example, you might set City to Public Pages
    and Listings. After the user conducts a search and views the details
    for a record they can click on the city value and run an immediate
    search. The search will run as if they had selected that city in the
    profile search screen.
-   The **Searchable** option determines if visitors to your directory
    can search the directory by this field. In common directory uses,
    almost every field is set to searchable. The more fields you set to
    searchable, the more power you provide to your visitors to find the
    information they need.
-   The **Results Column** check-box determines if the field is
    displayed as a column in the list of results. For example, your
    directory may have a field for website, and if you set the website
    field to appear in the results column, it will appear in the results
    table. If you do not check the results column the field will still
    appear in the view mode for a record. In other words, checking
    Results Column? will allow the field to appear in the results column
    AND in detail view mode.

The image below shows the search mode for our membership directory.

![Member Directory Search
Form](../img/CiviCRM-CapturingExposing-buildprofile-MemberDirSearchForm-en.png "MemberDirSearchForm")

Once you hit search you get this result set. Profile fields that have
Results Column checked are shown in the listing.

![MemberDirResults](../img/CiviCRM-CapturingExposing-buildprofile-MemberDirResults-en.png "MemberDirResults")

Clicking the view link gives you more details about the constituent,
showing all profile fields.

![Profile Member
View](../img/CiviCRM-CapturingExposing-buildprofile-MemberView-en.png "MemberView")

As we've seen, building a directory for your website can provide a
valuable tool for your constituents.

### **Linking to your directory**

You have several options to link to your directory:

-   **Drupal:** link to the directory search page using this path:
    http://www.myorganization.org/civicrm/profile?reset=1&gid=N where N
    is the ID of the profile directory.
    -   If you add **&force=1** to the above URL it will directly show a
        result set.
    -   If you add **&force=1&search=0**it will hide the search criteria
        and directly show the result set.
-   **Joomla!:** use the Menu Manager to create a front-end menu item.
    After creating a new menu item, select CiviCRM and choose the
    profile search option. In the parameters pane, choose the specific
    profile to use.
-   **Wordpress:** this feature is not yet implemented.
-   You can also prepopulate any search criteria in the URL. These
    options are described here:
    [http://wiki.civicrm.org/confluence/display/CRMDOC/Linking+Profiles](http://wiki.civicrm.org/confluence/display/CRMDOC/Linking+Profiles)

### Updating multiple records at the same time

You can **Update multiple memberships** from the results of a **Find memberships** search or from the advanced search results when **Display results as** is set to **Memberships**. You will need a profile that contains only membership fields.

Similarly you need contact, contribution, activity or participant search results and profiles containing only contact, only contribution, only activity or only participant fields to update multiple contacts, multiple contributions, muliple activities or multiple participants respectively.

You can update up to 100 records at one time using the **Update multiple ...**
functions.

____
**Example:**

You have a custom contact field called "Diving Skill Level" and you have just run a Intermediate Diving course.  You want to set the "Diving Skill level" to "Intermediate" for all people who attended the course.

Go to the Advanced Search screen and set the appropriate filters in the Event accordion. Leave **Display Results As** set to **Contacts** as you want to update a contact custom field. CLick on **Search**.

You will go to the "Update multiple contacts" screen.

  ![Update Multiple Records](../img/update-multiple-records.PNG)

From the drop-down list, choose the Profile you want to use and click **Continue**.

The next screen will contain a grid. Each row shows the contact's name and the fields in your profile. You should update the field values for each contact as needed.

![Update Multiple Records Profile View](../img/update-multiple-records-profile.PNG)


To set a field to the same value for all rows, enter that value for the first contact and then click the Copy icon (the image of two documents that is next to each column title). The value will automatically be copied into all the records displayed.

Click **Update Contacts** to save all your changes or **Cancel** to cancel the changes.
 ____
 
**Batch update limitations**

-   You cannot perform batch updates for different types of contacts
    (say, individuals and organisations) at the same time.
-   If you wish to update participant fields, you must do the update
    from a Find Participants search (and only include participant fields
    in your profile).
-   You can perform a batch update for up to 100 records at a time. If you find that updating a batch of 100 records is taking a long time, it may be quicker to update 4 batches of 25 records rather than one batch of 100 records.

### View/edit user account /new user registration with Profiles

For websites that have logged-in users, you may want to allow people to
provide additional information as they register for an account on your
website. Similarly, when people fill out a profile form you may want to
encourage (or force) them to sign up for a user account.

To include a profile form during the user registration process:

1.  Create a profile that is used for User Registration:

    ![addprofile_usedfor_reg](../img/CiviCRM-CapturingExposing-buildprofile-addprofile_usedfor_reg-en.jpg "addprofile_usedfor_reg")
2.  Add the fields you want people to fill out as they register, using
    the same process described above. Make sure the field visibility is
    set to Public User Pages.

**Including profiles in Drupal's My Account screen**

You can embed one or more CiviCRM profiles directly into Drupal's My
Account screen. This makes it easy for logged-in users to review and
update their information whenever they visit their My Account page.

To create a profile for this purpose:

1.  Create a new profile, or navigate to an existing profile and click
    Settings.
2.  Select View/Edit User Account in Used For.
3.  Click Save.
4.  Add the fields you want people to be able to edit from their Drupal
    My Account page.

Note: the profile must include only fields related to the Individual
contact type.

**New account creation during profile sign-up**

If you want your constituents to create a Drupal or Joomla! account when
filling out a profile, you can enable this with the "User account
registration option" under **Customize Data and Screens > Profiles**  click **Settings** against a profile. Anonymous (not-logged-in) users will then be invited (or required) to create an account when they visit the profile. Logged-in users will just see the
profile fields.

![Profile user registration
options](../img/CiviCRM-CapturingExposing-buildprofile-CMS_user_reg-en.png "CMS_user_reg")

You must include a Primary Email Address field in the profile for this
feature to function properly. This feature also works when the profile
is embedded in an online contribution page or event registration page.
Hence you can invite or force anonymous visitors to sign-up for an
account when they register for an event.

### Including Profiles in forms in CiviCRM components

Often you will want to define certain fields for inclusion in event
registration and contribution pages. The only significant difference is
that you can include fields in your profile that are specific to
participant records (for event registration forms) and contributions
(for contribution pages). Read about including Profiles in contribution
pages, event registration pages, and membership sign-up pages in the
*Set-up* chapter of *Contributions*, *Events*, and *Memberships.*

Other sources of information about Profiles
-------------------------------------------

Read more about Profiles in the following chapters:

-   In the *Customizing the user interface* chapter of *Intitial Set-up*
-   In the *Set-up* chapter of *Email*
-   In the *Set-up* chapter of *Contributions*
-   In the *Set-up* chapter of *Events*
-   In the *Set-up* chapter of *Memberships*

Alternatives to Profiles
------------------------

As you have seen, profiles can be put to a lot of different uses. It is
worth bearing in mind that there are alternative approaches for many of
these use cases. The alternatives available to you depend on the CMS
that you are using and your skill set, and have advantages and
disadvantages We've listed a few of the common ones below for you to
investigate.

### Drupal specific alternatives

-   The Drupal Views module can be used to make sophisticated displays
    of CiviCRM data. For example you might want to display a list of
    members on your public website using Views.
-   Drupal Webform-Integration is the most powerful form-builder for
    CiviCRM and includes many features missing from profiles, such as
    the ability to work with multiple contacts, events, memberships, and
    relationships, and offers greater flexibility in how forms are
    displayed, offering pagination, draft-saving, advanced spam-control,
    and conditional fields. For more information see the Drupal
    Integration chapter
    or https://drupal.org/project/webform_civicrm](https://drupal.org/project/webform_civicrm).
-   [](https://drupal.org/project/webform_civicrm)You can add fields
    directly to Drupal user accounts without using an embedded profile.
    These fields won't be available in CiviCRM but they will be more
    available in Drupal, so depending on why you are collecting this
    information, that may be appropriate for you.



### The API

With some basic coding skills (which if you are keen and reasonably
technically minded you might be able to pick up in a day or so) you
could use the API to flexibly display data on your website. See the
*Developer Documentation wiki*
[(http://wiki.civicrm.org/confluence/display/CRMDOC/Develop](http://wiki.civicrm.org/confluence/display/CRMDOC/Develop))
for an introduction to using the API.
