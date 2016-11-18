Autorisations et contrôle d'accès
=================================

Les autorisations (concept connexe de listes de contrôle d'accès ou ACL) sont des ensembles de règles qui définissent l'accès à différentes zones d'action du système. Pratiquement, vous créez des rôles pour votre site, donnez à ces rôles des autorisations pour effectuer certaines tâches et affectez les rôles à certaines personnes autorisées.

Les autorisations et les listes de contrôle d'accès vous permettent d'accéder à:

-  Différents composants de CiviCRM (par exemple : CiviContribute, CiviCase et CiviMail) pour permettre les tâches dont l'utilisateur est responsable 
-  Les données au sein du système (par exemple : les contacts, les contributions, etc.) et comment l'utilisateur peut interagir ou opérer avec elles.(créer, voir, modifier, supprimer)

Comme les permissions définissent qui peut voir et agir sur votre site, il est important, d'un point de vue de sécurité de bien les comprendre. Il est très facile de vérifier un paramètre d'autorisation sans comprendre complètement ce qu'il fait. Un site avec des autorisations mal configurées peut exposer par inadvertance les données de vos contacts.

Quelle différence entre les autorisations CMS et les ACL CiviCRM ?
------------------------------------------------------------------

Les autorisations et les ACL sont définis en deux endroits distincts: dans le système de gestion de contenu (CMS) et dans CiviCRM lui-même. De nombreuses organisations peuvent faire simplement avec les autorisations du CMS. D'autres doivent utiliser les ACL de CiviCRM pour obtenir un contrôle d'accès plus précis.

Les autorisations CMS vous permettent d'accorder (ou non) l'accès à des sections entières de CiviCRM ainsi qu'à des rôles d'utilisateurs tels que CiviMail, CiviEvent, etc... Elles permettent également de restreindre la capacité de l'utilisateur à afficher, éditer, ajouter et supprimer des enregistrements tels que des contacts , Événements et contributions. Cependant, il s'agit d'une approche «tout ou rien»: vous ne pouvez pas différencier les contacts qui sont dans différents groupes, par exemple :

Les ACL CiviCRM natives donnent un contrôle plus précis, ainsi vous pouvez limiter l'accès pour afficher, modifier, créer, supprimer et rechercher dans:

-   Les goupes et les contacts
-   Un profil (il s'agit d'une serie de champs existants et/ou personnalisés, voir "*Profils*")
-   Un ensemble de champs personnalisés
-   Certains événement (Par exemple, un utilisateur peut accéder à un événement, mais pas à d'autres)

En règle générale, vous pouvez commencer avec les autorisations CMS et si vous ne pouvez pas faire ce que vous souhaitez, configurez alors les ACL de CiviCRM pour renforcer plus précisement les droits d'accès.

Pour clarifier, voici deux exemples d'instances où les listes ACL de CiviCRM devraient être utilisées plutôt que celles de Drupal, Joomla! Ou WordPress:

1.  Une organisation a un siège social, et trois bureaux régionaux répartis à travers le pays. Le responsable des événements travaillant à partir du bureau central doit être en mesure de visualiser tous les événements à travers chaque bureau. Chaque bureau régional est seulement autorisé à l'accès à ses propres événements pour voir et modifier. Étant donné qu'une liste de contrôle d'accès CMS ne peut restreindre l'accès aux événements pour voir/modifier/ajouter/supprimer, *une ACL CiviCRM doit être utilisée.*

2. Deux ensembles de champs personnalisés ont été crées, l'un pour une équipe d'employés travaillant à Paris et un autre pour les donateurs à Londres. Chaque équipe doit uniquement pouvoir accéder aux données contenues dans son propre ensemble de champs personnalisés. Une liste de contrôle d'accès CMS ne peut leur donner accès qu'à toutes les informations personnalisées, ou à aucune d'entre elles. Dans ce cas, toute règle CMS contrôlant l'accès aux champs personnalisés doit être désactivée et une ACL CiviCRM doit être utilisée.

Autorisations CMS 
-----------------

Tous les CMS possèdent le même ensemble d'autorisations de CiviCRM, mais chacun se trouve dans des endroits différents et diffère légèrement en apparence.


### Autorisations dans Drupal

Pour acceder aux autorisation Drupal allez au menu Drupal et coisissez l'option **People** et cliquez sur l'onglet **Permissions** dans le coin supérieur droit de la fenêtre popup. Vous trouverez ici une liste de toutes les opérations ou actions possibles qu'un utilisateur peut effectuer dans CiviCRM et Drupal, avec des colonnes pour chaque type de rôle existant. La vérification d'une option dans l'une des colonnes confère à ce rôle la capacité d'exécuter l'action
Vous pouvez créer de nouveaux rôles et modifier ceux déjà existants. Pour modifier les rôles, dans l'onglet **Permis**, cliquez sur le bouton **Rôles** en haut à droite de la page.

![image](../img/CiviCRM_Drupal_Roles.png) 

Les rôles peuvent être attribués aux utilisateurs de la manière suivante:

- Ouvrez l'enregistrement de contact d'un utilisateur (un contact dans CiviCRM avec un compte d'utilisateur), appuyez sur le bouton **Actions** en haut et sélectionnez **Enregistrement utilisateur** dans le menu. Lorsque l'écran suivant apparaît, cliquez sur l'onglet **Modifier** (en haut à droite), puis faites défiler la page vers la section intitulée **Rôles**, vous pourrez alors changer leur niveau d'accès.

- En tant qu'administrateur, accédez au menu Drupal et sélectionnez l'option **Personne**. Lorsque la liste des utilisateurs actifs s'affiche, cliquez sur le nom souhaité pour ouvrir leur profil utilisateur Drupal, accédez à l'onglet **Modifier** en haut à droite de la page, puis faites défiler jusqu'à la section **Rôles**.



### Autorisations dans Joomla!

Les autorisations dans Joomla! peuvent être trouvées comme suit:

1.  Connectez-vous à Joomla! en tant qu'administrateur. Vous accedez au Panneau d'administration : choisir **Configuration**
2.  Dans la liste des **Composants** sélectionnez **CiviCRM** 
3.  Lorsque l'écran suivant apparaît, cliquez sur l'onglet **Droits**, vous pourrez alors changer les niveaux d'accès.
4.  Une fois les modifications effectuées cliquez sur **Enregistrer et fermer** en haut à gauche. 

Joomla! a une méthode différente d'attribution des autorisations. Les droits d'accès des différents groupes dans Joomla sont organisés de manière hiérachique, chaque groupe héritant des droits de son parent. Chaque groupe d'utilisateurs (rôle) est un parent ou un enfant d'un autre groupe d'utilisateurs. Les groupes d'utilisateurs enfants (ceux de la table inférieure) héritent des autorisations définies pour les groupes au-dessus d'eux. Par conséquent, lors de la modification des autorisations attribuées à un groupe d'utilisateurs dans la table, vous pouvez choisir entre:

-   **Hérité**: Si le groupe d'utilisateurs supérieur a cette autorisation, il sera également en mesure d'effectuer l'action donnée
-   **Autorisé**: Les utilisateurs de ce groupe sont autorisés à effectuer l'action. 
-   **Non autorisé**: Les utilisateurs de ce groupe ne peuvent pas effectuer l'action

Notez que Joomla! a deux autorisations supplémentaires non utilisées par Drupal ou Wordpress: **Configurer Joomla! AC ** (l'utilisateur peut configurer les listes ACL de Joomla! affectées à toutes les autorisations CiviCRM) et **Voir le composant CiviCRM** (l'utilisateur peut voir CiviCRM dans la liste des Composants).

![image](../img/joomla%20permissions_1.PNG)

Enfin, pour affecter un de ces groupes à un utilisateur ou pour modifier son groupe existant, assurez-vous d'être connecté en tant qu'administrateur, puis effectuez l'une des opérations suivantes:

-   Accédez à l'enregistrement de contact de l'utilisateur dans CiviCRM, cliquez sur le bouton **Action** et sélectionnez l'option **Group add contacts** Il suffira de sélectionner le groupe et valider par **Ajouter au groupe** 

-   Dans l'administration de Joomla!, sous le menu **Utilisateur**. Tous les utilisateurs disponibles y sont répertoriés, et en cliquant sur un nom, vous ouvrirez un écran avec la possibilité de modifier les paramètres de leur compte, y compris le groupe d'utilisateurs : **Attribuer cet utilisateur à un ou plusieurs groupe**. N'oubliez pas de cliquer sur **Enregistrer et fermer**


### Access Control (Permissions) in Wordpress 

In CiviCRM go to **Administer** > **User and Permissions** >
**Permissions (Access Control)**. Select the **Wordpress Access
Control**link. Here you can adjust the CiviCRM settings for each of the
predefined User Roles from Wordpress.

![image](../img/z_sprint14_wordpressacl_menu.png)

![image](../img/z_sprint14_wordpressACL.png)

Roles can be assigned to users in the following ways:

-   Open a user's contact record (a contact in CiviCRM with a user
    account), hit the **Actions** button at the top and select **User
    Record** from the menu. This will open the **Edit User** screen
    where you can change their **Role** to change their level of access.
-   Within the WordPress Site Admin area, select the **Users** menu item
    to see a list of all users. Clicking on a name will open the **Edit
    User** screen where you can change their **Role** to change their
    level of access.



### 

### Anonymous and Authenticated roles

You will encounter both these role types as you work with the access
controls. Although they may be named differently on different CMSes, the
basic principle is the same.

The **anonymous** role (**public** in Joomla!) applies to all visitors
to the website who have *not* logged in. This role will have the lowest
level of permissions. The default CiviCRM permissions for this role
are:

-   make online contributions/donations
-   view event information
-   register for events through online forms
-   vew event participants
-   subscribe and unsubscribe from mailing lists
-   access all custom data (ie see/enter information in custom data
    fields in forms)
-   access uploaded files ( ie view/print content of uploaded files)
-   view, create and edit profiles ( or profile listings and forms) 

The **authenticated** role (**registered** in Joomla, **subscriber** in
WordPress) is applied to all visitors to the site that have logged in .
This is the default role for all new user accounts, and cannot be
deleted. By default CiviCRM permissions for this role are the same as
those for the **anonymous** role.

You can alter the permissions for anonymous and authenticated users if
you need to as the following common scenarios show.

#### Taking online contributions

If you only want contributions from logged in users you would remove
the**make online contributions** permission from the "anonymous" or
"public" role.

#### Viewing event info and registering for events

If "view event info" and "register for events" are enabled for the
anonymous and authenticated roles then all visitors to your site will
be able to register for any event. If you wish to give only
specific users the ability to view or register for *some* events, you
must use a CiviCRM ACL, allowing a role "view" access to events if they
should only be able to view event information, and the "edit" permission
if they can register. However for this to function, the CMS "register
for events" ACL must be disabled, as it will override these settings.

e.g. A charity holds occasional fundraising events for the public and
separate evening dinners for some of its corporate donors. Any visitor
to the website can register and participate in a fundraising event,
however the dinners are private and must only be available to some of
their donors. In this instance, CiviCRM ACLs should be used instead of
the CMS rule "register for events" as they can specify the specific
events each group of users can access.

#### Editing profile data in online forms

Profiles are collections of default and custom fields, and can be used
in online forms to collect additional information from visitors, or
build searchable directories (see "Profiles").

If you have a standalone profile in an online form used to search for
and edit data in CiviCRM (e.g. not part of an event registration page),
only authenticated users may edit. The permission "profile edit" can be
given to the anonymous role, but visitors who are not logged in will
still be unable to edit the data unless they have a checksum (a unique
URL to one page where they may edit their own data; read "Everyday
tasks" in the email section for more information). For checksum tokens
to work, anonymous users must have the "profile edit" permission.

#### Collecting data from anonymous visitors using profiles 

If you have built profiles to collect data from anonymous visitors
through online forms (e.g. event registration pages, contribution pages
and standalone profile forms), the permission "profile create" will need
to be given to the "anonymous" role. Furthermore, should the profile
contain any custom fields, an additional permission will need to be
given, depending on the circumstances. Read "Accessing custom data"
below. 

#### Creating searchable directories for the public 

Profiles can be used to build searchable directories; a form of search
criteria able to gather a list of results from the database (e.g.
finding organisations held in the database by location). If you would
like to give a group of users access to search pages published on the
website, check the "profile listings" option for that role/user group.

#### Profile view

Where profiles have been embedded within online pages (e.g. to display
an organisation's name, description and contact details from the
database), the visitor must have the permission"profile view" to see it.

#### Using the "Profile listings and forms" permission

This access right should be assigned with care, and only to trusted
roles. The permission grants access to:

-   Add data through profiles in online forms
-   Edit data displayed in standalone profiles on public pages, if the
    option is given (e.g. contact information)
-   Use public searchable directories

Where possible, each of these access rights should be assigned to a role
separately, not through this 'allow all actions' permission. "Profile
listings and forms" is not enabled for the "anonymous" and
"authenticated" roles by default.

Note that if this role were given to anonymous users, in order to edit
data, the visitor must either be logged in or using a checksum token
(see "Everyday tasks" in the section on email). 

#### Accessing custom data

If custom data fields have been used on an online form or within
profiles, the user will not be able to interact with it unless they have
been given permission to view and/or edit custom data. There are two
ways of assigning this ability:

1.  Enable the "access all custom data" permission against the roles you
    wish to give both view and edit access. If this were given to the
    "anonymous" role, for example, they would be able to view and edit
    all custom fields in online forms (e.g. custom data fields within a
    profile that has been incorporated into an event registration page).
    However, this is an 'all or nothing' approach.
2.  Alternatively, CiviCRM ACLs can be created to give roles access to
    only *specific*sets of custom data fields. Use this option when you
    want to give groups of users access to different sets of data, e.g.
    a team in Amsterdam may only have access to custom volunteer fields,
    while the head office in Scotland has access access to both custom
    volunteer fields and custom donor fields. Note that these ACLs will
    not function if the "access all custom data" permission is used in
    the CMS; that permission in Drupal or Joomla! will override these
    settings in CiviCRM.

#### Accessing uploaded files

Enable the "access uploaded files" permission for any role that needs to
view images, photos and files attached to CiviCRM records and pages. Be
sure to assign this permission to the "anonymous" role if you want
visitors to see photos attached to contact records, personal campaign
pages, documents intended for public consumption, etc.

#### Giving users the ability to view their contact dashboard

You can provide authenticated (logged in) users with access to a screen
where they can review the mailing groups they have subscribed to, their
contributions, memberships and event registrations (where applicable).
Assign the "access contact dashboard" permission to roles whose users
are to be given access to this feature. **Do not** enable this for the
"anonymous" role.

### Other CMS Roles 

Each CMS also has other predefined roles giving varying amounts of
access to CiviCRM. Again you can change the permissions granted to
these roles but you must make sure that there is always one role
(Administrator/Super Users/Admin) that has the ability to administer
CiviCRM including managing access control.

You may also want to add additional roles to allow for very graduated
access to CiviCRM functionality.

More information on CiviCRM permissions (access control options)
including permissions required to perform certain back office functions
can be found
at [http://wiki.civicrm.org/confluence/display/CRMDOC/Default+Permissions+and+Roles](http://wiki.civicrm.org/confluence/display/CRMDOC/Default+Permissions+and+Roles).


Native CiviCRM ACLs
-------------------

As discussed earlier, CiviCRM ACLs are a more advanced and granular way
of managing user access to records through contact groups, assigned to
ACL roles. While an access control in the CMS can 'turn
off' visibility of entire sections of CiviCRM, and determine whether a
user can view/edit/delete/create data in the different areas of the
system, they cannot sub-divide these rules into access to different
record types. For example:

> A charity based in Chicago has three regional offices, and needs to
> give its fundraising staff the ability to create and edit contact
> records for prospective donors. They have decided that the fundraising
> department in each office can only have access to its local contacts.
> While the permission "add contacts" can be granted to authenticated
> users in the CMS (Drupal, Joomla! or WordPress), if "view all
> contacts" and "edit all contacts" were also assigned in this way,
> there would be no way to differentiate between the three groups of
> donors (locations). This could only be achieved with a CiviCRM ACL.

To begin, go to **Administer** > **User and Permissions** >
**Permissions (Access Control)**. This screen will link you to the CMS
access control list, and the three steps to managing those native to
CiviCRM.

### Manage Roles

This is where you can create ACL roles. By default you will have
"administrator" and "authenticated" (logged in), but only the
administrator role may be edited; "authenticated" is a reserved role and
core to the system.

Clicking "Add Acl Role" will present a screen for creating a new role
with the following options:

-   **Label**: this is the name of the role, and will be visible to users
-   **Description**: create and format a description of the role
-   **Weight**: give the role a number to determine its place in the list
    (e.g. "1" places the role at the top, while "20" might send it to
    the bottom; lower numbers appear before higher ones)
-   **Enabled?**: is the role active or not? If you disable this option,
    functionality may cease to work for some users



![image](../img/CiviCRM_ACL_civicrm-manage-roles.png)



### Assign Users to CiviCRM ACL Roles

Once the roles are configured, you can begin to assign them to users. In
CiviCRM this is done in two steps:

First create an access control group for a selection of users that are
to have the same level of access. There are multiple ways to do this,
outlined in the chapter "Groups and tags".

The ACL contact group can now be assigned to a role. Click the second
step on the access control menu screen ("Assign Users to CiviCRM ACL
Roles") and hit "Add Role Assignment". Complete the following:

-   **ACL Role**: select an available ACL role
-   **Assigned To**: choose a contact group to assign to the role
-   **Enabled?**: is this assignment active or not?

![image](../img/CiviCRM_ACL_civicrm-assign-users.png) 

### Manage ACLs 

The third step is where the ACLs are finally created. They can be broken
down into the following questions:

1.  Which role will have permission to perform this action?
2.  What is the action/operation? Is it the ability to
    view/edit/delete/create, etc?
3.  Which set of data can the action be carried out on?

To begin creating these ACLs, return to the Access Control screen
(**Administer > User and Permissions > Permissions...**) and
click "manage ACLs". A list of existing controls will be displayed,
likely including one for administrators giving them permission to edit
all contacts in the database. To add a new one, click "Add ACL" and fill
in the following:
-   **Description**: write a clear description of what the ACL does

-   **Role**: choose a role to assign the ACL to from the drop-down list


-   **Operation**: select the action this role is allowed to perform (e.g. view,
edit, create, delete...)

-   **Type of Data**: choose the data type the operation relates to:

    -   A group of contacts
    -   A profile
    -   A set of custom data fields
    -   Events

-   **Group/Profile/Custom Data/Event**: The label on this field is set by your selection in **Type of Data**. This is where you select the specific
group of contacts, profile, custom data or event for this ACL

- **Enabled?**: is the ACL active?

![image](../img/CiviCRM_ACL_civicrm-create-ACL.png)




