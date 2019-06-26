# Intégration avec Drupal

Des trois CMS pouvant intégrer CiviCRM, Drupal est celui ayant reçu le plus d'attention, et offrant le plus d'options d'intégration. Cela est dû en partie parce que la communauté Drupal est principalement une communauté de développeurs.

Lorsque l'on pense à l'intégration à un site web avec Drupal, il est important de comprendre le concept de *modules Drupal*. Un module peut être considéré comme une application fournissant au CMS des fonctionnalités supplémentaires. Par exemple, le module *Calendar* vous permet d'afficher des calendriers sur votre site web. La distributation Drupal de CiviCRM contient plusieurs modules Drupal facilitant son intégration, et ce de différentes façons.

## Rôles et permissions Drupal

Lorsque vous créez un nouvel *Utilisateur* sur un site Drupal et que CiviCRM y est intégré, alors ce dernier créera automatiquement un enregistrement *Contact* lui correspondant. *Utilisateur* et *Contact* possède tous deux une identification / numéro d'index différents.

*Voir également le chapitre [Autorisations et contrôle d'accès](../initial-set-up/permissions-and-access-control.md) de la section* Configuration initiale *pour une discussion générale sur le contrôle d'accès.*

Votre site Drupal vous permet de créer différents *Rôles*. Ces rôles sont assignés à des utilisateurs du site, et chaque rôle contient des *permissions* qui vous permettent de réaliser une certaine série de tâches (voir, modifier, supprimer, et administrer des contacts) ou accéder à un certain jeu d'information (contacts CiviCRM, CiviMail, CiviEvents, Drupal USers, etc.)

Pour plus d'information sur les rôles Drupal, merci de lire la documentation disponible sur drupal.org :

-   Utilisateur : paramètres d'accès et de gestion [http://drupal.org/documentation/modules/user](http://drupal.org/documentation/modules/user)
-   Gérer les contrôles d'accès avec les rôles et les permissions Drupal [http://drupal.org/node/22275](http://drupal.org/node/22275)

Les *permissions* Drupal vous permet de définir quelles tâches un *rôle* particulier de Drupal peut executer, et à quelles informations il a accès. Les *permissions* déterminent également le niveau d'accès qu'un certain type d'utilisateur a sur la configuration des modules, l'affichage, l'édition, les utilisateurs ou les informations de contact CiviCRM.

Pour plus d'information sur le paramétrage des permissions Drupal, veuillez lire la documentation sur drupal.org :

-   Associer des permissions et des utilisateurs à des rôles [http://drupal.org/node/22278](http://drupal.org/node/22278)

-   Ajuster les permissions après l'ajout d'un module [http://drupal.org/node/22279](http://drupal.org/node/22279)
-   Références permissions [http://drupal.org/node/132202](http://drupal.org/node/132202)
-   Visualiser les permissions de module [http://drupal.org/node/1089746](http://drupal.org/node/1089746)


Les rôles Drupal sont globaux et écraseront les contrôles d'accès (voir le chapitre [Autorisations et contrôle d'accès](../initial-set-up/permissions-and-access-control.md) dans la section *Configuration initiale*) définis dans CiviCRM.
Par exemple, si vous définissez un contrôle d'accès pour limiter l'accès à certains contacts mais qu'un rôle Drupal possède la permission *Accéder à tous les contacts*, alors toute personne associée à ce rôle pourra voir l'ensemble des contacts.


Taxinomies Drupal, accès au contenu ou tout autre module d'accès basé sur un rôle utilisateur
---------------------------------------------------------------------------------------------

Il existe plusieurs modules Drupal pouvant déterminer quel rôle Drupal a accès à un certain type de contenu dans votre site web. Cela peut être basé sur les taxinomies, en sélectinnant un accès à des noeux spécifiques, des paramètres sur des vues spécifiques, pages ou paneaux, ou basé sur un certain contexte ou règle. Voici ci-dessous quelques uns de ces modules :

-   Views [https://www.drupal.org/project/views](https://www.drupal.org/project/views)
-   Panels [http://drupal.org/project/panels](http://drupal.org/project/panels)
-   Chaos Tools Suite and Page
    Manager [http://drupal.org/project/ctools](http://drupal.org/project/ctools)
-   Context [http://drupal.org/project/context](http://drupal.org/project/context)
-   Content
    Access [http://drupal.org/project/content_access](http://drupal.org/project/content_access)
-   Taxonomy Access
    Control [http://drupal.org/project/taxonomy_access](http://drupal.org/project/taxonomy_access)

Vues Drupal
-----------

[Views](https://www.drupal.org/project/views) est un puissant module Drupal vous permettant d'afficher du contenu de site web comme, par exemple, les dernières nouvelles de votre page d'acceuil. CiciCRM intégré avec ce module permet d'afficher les données CiviCRM sur le site web. Par exemple, si vous souhaitez créer une page appelée *Organisations partenaires* et que vous souhaitez l'afficher au grand public, vous pourriez utiliser la procédure suivante :

1. Sélectionnez le critère déterminant le jeu de contacts à prendre en compte, tel que :
   * Contacts de type *Organisation* uniquement ;
   * Ceux tagués "Partenaire" dans CiviCRM ;
   * Ceux ayant un statut d'adhésion *Nouveau* ou *En cours*.
2. Choisissez quelles données seront affichées, telles que :
   * Nom de l'organisation ;
   * Région ;
   * Site web ;
   * Numéro de téléphone.
3. Choisissez le format d'affichage (table ou paragraphe) ;
4. Autorisez le public à filtrer le résultat, par exemple par région.

Il s'agit ici d'un simple exemple, les possibilités de jouer avec les vues Drupal et les données CiviCRM étant bien plus vastes.

### Configuration

Si vos bases de données Drupal et CiviCRM sont distinctes, ajouter le support CiviCRM au module *Vues* requiert un brin de configuration. Il s'agit d'indiquer aux vues où trouver les données CiviCRM.
Allez à **Administrer** > **Paramètres système** > **Intégration à la base de donnée du CMS**. Vous pourrez visualiser les lignes de code à recopier après le code du fichier *settings.php* de Drupal. En cas de problème, vous pouvez demander de l'aide dans le [forum](http://forum.civicrm.org/) or [engager un consultant](http://civicrm.org/what/experts). Si vous utilisez des jeux de données personnalisées, et à chaque fois que vous en ajouterez, vous devrez répéter le processus.

### Créer des vues utilisant des données CiviCRM

Les vues font partie de la section **Structure** du menu d'administration Drupal. Lorsque vous créez une vue, nommez-là et sélectionnez le type de données que vous souhaitez afficher.

De façon générale, si votre vue concerne des contacts, vous sélectionnerez Afficher: Contacts CiviCRM. Si vous souhaitez afficher d'autres détails comme des événements, des relations, des contributions ou des activités, il existe des options vous permettant d'enrichir votre vue.

![image](../img/Views-CiviCRM-Partner-1.png)

Quand la vue est créée, ajustez les champs, filtres, affichage et autres configurations pour adapter la page à vos besoins.

![image](../img/Views-CiviCRM-Partner-3.png "sample configuration using Views 3 in a Drupal 7 environment")  


### Ce que peuvent également faire les vues et CiviCRM

-   Liste des événements à venir ;
-   Construction de rapport sur les contributions, activités ou participants ;
-   Liste des donateurs les plus récents ;
-   Listes de comité, conseil d'administration, bureau... ;
-   Liste des membres de votre organisation ;
-   et plus encore !

Intégration du Webform CiviCRM 
------------------------------

Tout comme les vues peuvent *sortir* les données de multiples façons, le module Webform peut les faire *entrer* exactement de la façon que vous souhaitez : vous pouvez créer et mettre à jour des contacts, des inscriptions à des groupes, à des étiquettes, des champs personnalisés et effectuer des paiement en ligne. Le module Webform offre une souplesse d'utilisation encore plus importante que l'utilisation des profils CiviCRM.

Par exemple, vous pouvez :
  - créer un formulaire pour ajouter dans vos contacts une famille complète avec toutes les relations définies ;
  - créer une nouvelle activité lorsqu'une personne complète un formulaire.
  
Le module Webform CiviCRM possède une documentation en ligne très complète. Pour plus d'information, veuillez vous référer au chapitre [Webform CiviCRM Integration](https://docs.civicrm.org/sysadmin/en/latest/integration/drupal/webform/) (en anglais) du manuel de l'administrateur système de CiviCRM.

CiviCRM Organic Groups Sync
---------------------------

Le module [Organic Groups CiviCRM](https://www.drupal.org/project/og_civicrm) permet d'intégrer les groupes organiques de Drupal aux groupes CiviCRM. Cela s'avère utile pour les groupes requérant la fonctionnalité *Groupe organique* sur le site web mais dont les changements doivent également se refléter au sein de CiviCRM. Une fois les utilisateurs Drupal d'un groupe organique intégrés à CiviCRM, le groupe peut être utilisé pour de la diffusion massive de courriel, du suivi d'activité, ou tout autre chose liée aux contacts.

Une fois le module Organic Groups CiviCRM installé et activé dans Drupal, ce dernier créé automatiquement deux groupes CiviCRM pour chaque groupe organique Drupal existant :
-   Un groupe régulier contenant un enregistrement de contact pour chaque utilisateur Drupal d'un groupe organique. Ce groupe possède le même nom que le groupe organique ;
-   un groupe ACL contenant l'enregistrement de contact de l'administrateur du groupe organique correspondant. Cela donne à ce dernier la possibilité de visualiser et de modifier les membres du groupe normal correspondant dans CiviCRM.

ATTENTION : La synchronisation de ces groupes ne se fait que dans le sens groupe organique Drupal vers les groupes CiviCRM.

Lorsqu'un nouvel utilisateur est ajouté dans un groupe organique, il est automatiquement ajouté dans le groupe CiviCRM correspondant. S'il quitte le groupe organique, il est également dissocié du groupe CiviCRM. Si un groupe organique est supprimé, les groupes CiviCRM sont également supprimés. Toutefois, l'inverse n'est pas vrai : un contact ajouté dans un groupe CiviCRM ne sera pas ajouté dans le groupe organique correspondant. Idem pour sa suppression. L'administration de ces groupe doit donc se faire du côté du site Drupal.

CiviGroup Roles Sync
--------------------

The CiviGroup Roles Sync module allows administrators of Drupal Websites
to streamline the user experience for donors and staff. The CiviGroup
Roles Sync module allows you to:

-   Allow board members, committees, staff, and volunteers to access
    specific content or perform specific tasks.
-   Provide customized experiences for users of specific groups when
    they access your website. For example, when a major donor logs into
    the website display a letter from the President thanking the donor
    for his contribution and participation, or provide a major donors
    with pre-registration access to upcoming events and exclusive news
    or resources.

You should spend some time assessing the different ways that different
sorts of users interact with your website, being sure to ask yourself
whether or not the user experience is dependent on specific organized
groups, teams, committees, or task forces or on whether or not a contact
meets a specific set of criteria, or if you should apply roles to users
manually.

In essence, it allows you to synchronize Drupal users that have a
certain role with CiviCRM contacts in a certain group.

### Preparation


Before using CiviGroup Roles Sync module you should have the following
prepared:

-   your organization's Groups should be created.
-   the roles you will need for each use case should be created in
    Drupal.
-   if you are using additional modules to fine-tune access, you should
    have all modules you need installed and configured

When determining what Groups and what Drupal Roles you should create it
is important to remember that multiple Group Types may grant the same
Drupal Role and each Group can be used to grant multiple Drupal roles.

You should enable the module from the Drupal module administration
screen.

### Syncing CiviCRM Groups to Drupal Roles

-   Navigate to the CiviGroup Role Sync configuration screen.

-   Click on **Add Association Rule.**

-   Under **CiviCRM Group** select the Group that you want a user to
    have in order to be granted a specific Drupal Role.
-   Under **Drupal Role** select the Drupal Role that should be granted.
-   Click on **Add Association Rule** when you are finished configuring
    your new association rule.

You can always edit or delete existing association rules from the same
configuration screen.

CiviMember Roles Sync
---------------------

The CiviMember Roles Sync module allows administrators of Drupal
Websites to streamline the user experience for organization members. The
CiviMember Roles Sync module allows you to.

-   Automatically grant a Drupal Role to a user based on the type of
    membership he/she has with your organization and whether or not
    he/she is currently in good standing.
-   Allow a user to access member-only content or perform specific
    member-only tasks.
-   Restrict a non-member or expired member user from accessing
    member-only content or performing member-only tasks until he/she
    registers or renews membership with your organization.

### Scenario: Member-only Content

The Retail Baker's Association of America (RBA) connects bakery
suppliers and owners across the country to foster a community that
encourages exchange of business and industry information, networking,
mentoring, and business opportunities, and establish industry standards
through certification, research, and school programs.

Visitors to their website fall into three different user experiences:

-   Non-Members who purchase resources and materials from RBA's online
    boutique. A non-Member must register for a user account to make a
    transaction so that he or she can keep track of purchase history, so
    that RBA can petition him or her for membership in the future.
-   Current members in good standing who have access to member-only
    resources including discussion boards, programs, marketing
    materials, and digital version of RBA publications.
-   Members with expired memberships or former members who need to renew
    need to log into the RBA website to renew their membership, but
    should not have access to member-only resources until their
    membership has been reactivated.

In order to save their staff from having to grant the Drupal Role
"Active Member" to a user each time he or she renews his or her
membership and then remove the "Active Member" role if that user cancels
his or her membership or allows his or her membership to expire, RBA
uses CiviMember Role Sync to grant the "Active Member" role to any user
who is either a new or current member and any user who's membership has
fallen into the grace period. Now when a user registers or renews his or
her membership he or she will automatically be granted access to RBA's
Member-Only web content.

### What You Need to Know

This section covers what you need to think about before beginning to
work with CiviMember Role Sync.

You should spend some time assessing the different ways that different
sorts of users interact with your website, being sure to ask yourself
whether or not the use case is dependent on your membership structure
or dependent on the organization of committees, teams, and contacts
meeting a specific set of criteria, or if your workflow simply does not
warrant the use of CiviMember Role Sync at all.

### CiviCRM Membership Types

You should have a full understanding of CiviCRM Membership Types and
CiviCRM Membership Statuses before you begin working with the CiviMember
Role Sync module. You can learn more about the CiviMember component by
reviewing the **MEMBERSHIP** chapter.

### Configuring CiviMember Roles Sync

Before using CiviMember Roles Sync module you should have the following
prepared:

-   your organization's Membership Types and Membership Statuses should
    be created and configured in the CiviMember component.
-   the roles you will need for each use case should be created in
    Drupal.
-   what content each Membership Type should grant permissions to should
    be agreed upon by your staff
-   what tasks each Membership Type should grant permission to should be
    agreed upon by your staff
-   if you are using additional modules to fine-tune access, you should
    have all modules you need installed and configured

When determining what Membership Types and what Drupal Roles you should
create it is important to remember that multiple Membership Types may
grant the same Drupal Role and each Membership Type can be used to grant
multiple Drupal roles.

*For example: The Retail Bakers Association of America has five
different membership types: Corporate Sponsor, Bakery, Individual,
Student, and Retired Bakery. Having any one of the five Membership Types
will grant a user the "Active Member" Drupal Role that gives access to
the member-only content. In addition to this, users with the Corporate
Sponsor Membership Type should have access to additional exclusive
content. RBA decides calls the Drupal role used to access this
additional exclusive content "Corporate Member" and user with the
Corporate Sponsor Membership Type will be granted the "Corporate Member"
role in addition to the "Active Member" role.*

#### Enabling CiviMember Roles Sync Module

1.
To enable the CiviMember Roles Sync Module navigate to your list of
installed Drupal modules.

    -   Drupal 6: Go to **Administer > Site Building > Modules**
    -   Drupal 7: Go to **Modules** from the Administration Menu at the
    top of your screen.

1.
Find the Module **CiviMember Roles Sync** and check the box to the left
of the module's name.

1.
Click on **Save Configuration**.

#### Syncing CiviCRM Membership Types to Drupal Roles

1.
Navigate to the CiviMember Role Sync configuration screen.

    -   Drupal 6: Go to *Administer > Site Configuration > CiviMember
    Roles Sync*
    -   Drupal 7: Go to *Configuration > CiviMember Roles Sync*

1.
Click on **Add Association Rule.**

1.
Under **Select a CiviMember Membership Type** select the Membership Type
that you want a user to have in order to be granted a specific Drupal
Role.

1.
Under **Select a Drupal Role** select the Drupal Role that should be
granted.
*Example: RBA wants any user with a Current Bakery Membership Type to be
granted the "Active Member" role, so the RBA staff creates a new
Association Rule and selects Bakery under Select a CiviMember Membership
Type and selects "Active Member" under Select a Drupal Role.*

1.
Under **Current Status** select the Membership Status that a user
should have to be granted your selected Drupal Role.
*Example: RBA wants to grant any user who has a Membership Status of
either New, Current, or Grace access to the member-only website content,
so the RBA staff checks the boxes next to those three Membership
Statuses.*

1.
Under **Expired Status** select the Membership Status that will revoke
the Drupal Role from the user. *Example: RBA wants to make sure that any user
whose membership expires
or who cancels their membership has their access to the member-only website
content revoked, so the RBA staff checks the boxes next to Expired and
Canceled.*

1.
Click on **Add Association Rule** when you are finished configuring your
new association rule.

1.
The page will reload, and you should see the message "Your Association
Rule has been added."

1.
Repeat steps 1-8 to add all necessary association rules for your
organization. Once you have finished adding all of your association
rules, move on to step 10.

1.
Click on the tab **Manually Synchronize**

1.
Click on **Synchronize CiviMember Membership Types to Drupal Roles
Now**. This will put your new CiviMember Role Sync Association Role
immediately into effect.

#### Editing Existing Association Rules

You can always edit or delete existing association rules.

1.
To edit or delete an existing Association Rule, Navigate to the
CiviMember Role Sync configuration screen.

    -   Drupal 6: Go to *Administer > Site Configuration > CiviMember
    Roles Sync*
    -   Drupal 7: Go to *Configuration > CiviMember Roles Sync*

1.
You should now see a list of all existing CiviMember Role Sync
Association Rules. If not, click on **List Association Rule(s)** tab.

    *   Edit an Existing Association Rule
        *   Find the Association Rule you want to make changes to and click
on **edit** for that Association rule.
        *   Make the changes to your Association Rule and when yo are finished click
on **Edit association rule**.

    *   Delete an Association Rule

        *  Find the Association Rule you want to remove and click on **delete** for
that Association Rule.

        *  Your association rule will be deleted. You will not need to confirm
deletion.

#### Configure when Synchronization Should Happen

 You can select several different options for when synchronization
should occur by navigating to the CiviMember Role Sync Configure screen.

-   Drupal 6: Go to **Administer > Site Configuration > CiviMember
    Roles Sync > Configure**
-   Drupal 7: Go to **Configuration > CiviMember Roles Sync >
    Configure**

#### Automatic Synchronization Methods:

-   Synchronize whenever someone logs in or logs out: This method will
    trigger synchronization only after a user logs in or out of his or
    her account. You should be careful when using this method because if
    you have long user sessions a user could continue to have access to
    actions or content until he or she finally logs out. (This is the
    default setting)
-   Synchronize when a Drupal Cron occurs: This method relies on a cron
    to trigger synchronization. Learn more about Drupal Cron at:
    [http://drupal.org/cron](http://drupal.org/cron)
-   Synchronize when membership is updated: This method will synchronize
    when the user registers for or renews his or her membership and when
    the organization staff updates a user's membership information from
    the back office.
-   Disable Automatic Synchronization: This method relies on an
    organization staff member to manually trigger synchronization. To
    manually trigger synchronization, go to **CiviMember Roles Sync
    settings**, click on the Manually Synchronize tab, and click
    on Synchronize CiviMember Membership Types to Drupal Roles Now.

Be sure to click **Save Configuration** after making any changes.
