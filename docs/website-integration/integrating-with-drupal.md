# Integration avec Drupal

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

Just as Views can *output* data in virtually any way imaginable, this
module allows you to have data *input* exactly the way you want. The
webform CiviCRM integration is extensive and offers many different
options for things that can happen as part of the form submission.

You can create and update contacts, group subscriptions, tags,
relationships, cases, custom data, activities, memberships, event
participants and take payments online via webforms. They can offer
greater flexibility when compared to standard CiviCRM Profiles.

For example, you can create a form which adds a family with all
relationships / you can add a new member form with a multi-page form
which includes question logic / you can create a new activity when
someone submits the form. Webform CiviCRM has extensive online
documentation which you should read to make the most out of its
functionality.

For more information see:
[http://wiki.civicrm.org/confluence/display/CRMDOC/Webform+CiviCRM+Integration](http://wiki.civicrm.org/confluence/display/CRMDOC/Webform+CiviCRM+Integration)

CiviCRM Organic Groups Sync
---------------------------

The Organic Groups CiviCRM module
([http://drupal.org/project/og_civicrm](http://drupal.org/project/og_civicrm))
integrates Organic Groups from a Drupal site with CiviCRM groups. This
is useful for groups that require Organic Group functionality on their
website but also need to be tracked within CiviCRM. Once an Organic
Group of Drupal users are integrated into CiviCRM, the Drupal group can
be used for mailings, tracking address information, tracking activities
or anything else normally done with CiviCRM contacts.

Once the Organic Groups CiviCRM module is installed and enabled in
Drupal it automatically creates two CiviCRM groups for each existing
Drupal Organic Group:

-   A normal group containing a contact record for each corresponding
    user who is part of an Organic Group. This group is assigned the
    same name as the linked Organic Group.
-   An access control group containing the contact record of the
    administrator of the corresponding Organic Group. This gives the OG
    group admin the ability to view and edit members of their group in
    CiviCRM.

The groups are synchronised one way only, from the Drupal Organic Groups
to CiviCRM groups. When a new user is added to or signs up for an
Organic Group, they are automatically added to the corresponding CiviCRM
group. If they leave the Organic Group then they are removed from the
CiviCRM group. If an Organic Group is deleted, the CiviCRM group is also
deleted. However, the reverse of each of this situations is not true; a
contact added to the CiviCRM group will not appear in the Drupal Organic
Group, a contact removed from the CiviCRM group will still remain in the
Drupal Organic Group, and if you delete the CiviCRM group, the Drupal
Organic Group will still remain. Therefore, this integration is meant to
be used when you administer the group from the Drupal side.

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
