Définition des adhésions
====================

Ce chapitre décrit comment configurer un ou plusieurs types d'adhésion que vous pouvez utiliser pour gérer les membres de votre organisation. Cela explique également le concept des statuts d'adhésion et la façon dont votre organisation peut les utiliser pour définir un cycle de vie d'adhésion.

Types d'adhésions
----------------

Les types d'adhésion sont un élément de base pour la gestion des membres dans CiviCRM. En règle générale, une organisation mettra en place un type d'adhésion pour chacune des différentes adhésions qu'elles offrent. Pour les structures d'adhésion les plus simples, un type d'adhésion peut suffire. Pour des structures d'adhésions plus complexes, il est peut-être nécessaire d'utiliser plusieurs types d'adhésion. Par exemple, une organisation peut définir trois types d'adhésion pour les membres «Actifs», «bénévoles» et «Honoraires». Une organisation peut aussi choisir d'utiliser les types d'adhésions comme des abonnements ou souscriptions à leurs différentes publications, gratuites ou payantes.

Plusieurs options peuvent être configurées pour un type d'adhésion, et celles-ci sont paramétrées en fonction du formulaire de type d'adhésion. Une compréhension solide des options vous aidera à décider du nombre de types d'adhésion dont votre organisation a besoin et de la manière dont elles doivent être configurées.

Dans ce chapitre, nous couvrirons la configuration la plus courante pour les types d'adhésion. Certaines organisations, avec des structures d'adhésion plus complexes, ont des exigences qui vont au-delà de ce qui est disponible avec les types d'adhésion seuls. 
Ces organisations trouveront dans le chapitre sur **les Ensembles de prix d'adhésion** la flexibilité supplémentaire dont ils ont besoin. Les ensembles de prix d'adhésion sont un sujet avancé, ils sont expliqués dans le chapitre "*Ensembles de prix d'adhésion*".

Si vous rencontrez des problèmes pour modéliser votre structure d'adhésion dans CiviCRM, demandez sur le forum CIVICRM la réponse aux problèmes que vous rencontrez. Il peut y avoir d'autres façons de modéliser vos données, ou des modifications simples que vous pouvez apporter au comportement de CiviCRM pour mieux répondre à vos besoins.

Pour démarrer la configuration sur les types d'adhésions :

1.  Allez à : **Adminitrer>CiviMember>Types d'adhésion**.
2.  Selectionner : **Ajouter un type d'adhésion**

![image](../img/New_membership_type.png) 

-   **Nom**:
Le nom est affiché dans tout le système, tant sur les pages publiques que dans les pages de backend. Passez donc un peu de temps à penser à un nom qui est approprié aux deux publics. Il peut être changé ultérieurement (bien que cela puisse entraîner un travail supplémentaire dans la mise à jour des reçus d'adhésion s'ils ont été personnalisés en fonction des noms d'adhérents)

- **Description**:
Ceci n'est pas obligatoire, mais vous pouvez indiquer à quel type de contacts il est destiné, etc.

-   **Organisation pour l'adhésion**: 
CiviCRM est capable de gérer les adhésions de plusieurs organisations, c'est-à-dire qu'un club sportif local pourrait utiliser une seule instance de CiviCRM pour gérer les adhésions d'un club de tennis, d'un club de golf et d'un club de judo.
Pour cette raison, lors de la définition d'un type d'adhésion, vous devez spécifier l'organisation pour laquelle le contact deviendra membre. Chaque organisation doit déjà exister en tant que contact dans CiviCRM. De nombreuses d'organisations souhaitent seulement modéliser les adhésions de leur propre organisation. Dans ce cas, vous pouvez simplement choisir l'organisation par défaut.

    Si vous souhaitez activer les inscriptions ou les renouvellements en ligne, le modèle de données CiviCRM exige qu'un contact ne puisse avoir qu'une seule adhésion active avec une seule organisation à un moment donné. Cependant, certaines organisations peuvent vouloir que les gens aient deux membres ou plus à la même organisation simultanément. Par exemple, une organisation axée sur la santé des enfants pourrait vouloir offrir une adhésion aux parents qui comprend un magazine pour les parents et une adhésion aux professionnels de la santé qui comprend un journal professionnel et des réductions pour les événements de formation. Les parents qui sont des professionnels de la santé peuvent vouloir les deux adhésions.
    Une "solution de contournement" pour cela, consiste à créer des organisations "fictives" pour chacune des adhésions simultanées possibles. Dans ce cas particulier, nous devrions créer une organisation supplémentaire pour les professionnels de la santé. Notez que vous ne devez pas exposer l'organisation fictive à vos membres sur le site, uniquement pour des raisons administratives.
   
-   **Cotisation minimum**: Pour des adhésions gratuites, vous devez entrer 0 (zéro) dans ce champ.
Sinon, vous devez entrer le montant minimum qui doit être payé pour ce type d'adhésion. La raison pour laquelle nous appelons ce champ le montant *minimum* est que nous avons une option pour encourager les gens à payer plus que le minimum pour une adhésion s'ils le souhaitent.

-   **Type d'opération**: Le type financier par défaut pour un type d'adhésion est **Cotisations**

Le type par défaut "Cotisation" convient à de nombreuses organisations. Toutefois, si vous avez des besoins comptables plus complexes, vous pouvez spécifier différents types financiers qui vous permettront de comptabiliser différents paiements d'adhésion de différentes façons. Pour plus de détails, consultez le chapitre *Intégration comptable* dans la section *Contributions*. Si vous avez besoin de plus de contrôle fin par rapport aux types financiers, vous voudrez peut-être regarder *les jeux de prix*.

    Notez que le type financier peut être remplacé par des pages d'inscriptions 
    spécifiques pour des contacts publics, ainsi que lors de l'enregistrement 
    d'une adhésion dans le back-end. CiviCRM gère les adhésions payées en liant 
    les enregistrements d'adhésion aux documents de contribution. Un dossier 
    d'adhésion documente la *relation* d'un contact avec l'organisation, tandis
    que la transaction financière correspondante indique la valeur monétaire 
    associée à cette adhésion..
    
![image](../img/membership_contribution.png)


    CiviCRM respects this distinction by storing the membership record under
    the membership tab, storing the financial record under the Contributions
    tab, and then creating a link between the two records.

-   **Auto-renew**: CiviCRM offers an auto-renew functionality that will automatically
submit a repeat transaction to the payment processor when the current
membership expires. This can be a good way to increase membership
retention. This functionality is not available for all payment processor
so you will need to check if yours is configured for recurring payments
before selecting one of the auto-renew options here. For information on
payment processors see
[http://wiki.civicrm.org/confluence/display/CRMDOC/Payment+Processors.](http://wiki.civicrm.org/confluence/display/CRMDOC/Payment+Processors)

    You can offer or require auto-renewal for a membership type. However
    auto-renew memberships can only be offered for memberships that have a
    duration (discussed below) of one year or less.

-   **Duration**: In the **Duration** field you should enter the number of days, months or years that your membership lasts for each time someone signs up or
renews.

-   **Period type**: The options for Period type are rolling and fixed.
 **Rolling** memberships start on the day the member signs up.
**Fixed** memberships start on the particular calendar date you specify.

    When you set the Period type to fixed, extra fields will appear
    depending on the duration you have specified.

    If the Duration is specified in **years** two extra fields will be
    displayed: 

    -       The **Fixed Period Start Date** is the calendar date that all
    memberships start on (eg January 1st or April 15th).

    -   The **Fixed Period Rollover Date** determines the end date for the
    membership when a person signs up part way through your membership
    year. Its use is best illustrated through an example. Consider a
    membership type with a **Duration** of one year, a **Fixed Period
    Start Date** of January 1 and a **Fixed Period Rollover Date** of
    September 1

         *      Anyone signing up between 1 January 2014 and 31 August 2014 will
        have a membership end date of 31 December 2014. 
         -   Anyone signing up on or after 1 September 2014 will have a
        membership end date of 31 December 2015.( ie they will receive
        up to 15 months membership for the 1 year price.)

    If the Duration is specified in **months** one extra field will be
    displayed:
    
    -   The **Fixed Period Rollover Date** determines if the membership
        duration starts at the beginning of the current calendar month or
        the beginning of the next calendar month. Consider a 6 month
        membership type with **Fixed Period Rollover Date** set to 15:
    
        -   Someone signing up on days 1-14 January will have a membership
            end date of 30 June. 
        -   Someone signing up on days 15-31 January would have a membership
            end date of 31 July.

    Example: If **Duration =** 12 months, **Period type** = Fixed, and **Fixed
    Period Rollover Date** = 1, then anyone joining during August 2014 will
    have an expiry date of 31 August 2015. 

-   **Relationship Type**: Memberships can be **inherited** from one contact to another. An example of this would be a professional trade organisation that signs up
a company as the (primary) member and wants employees of the company
receive the benefits of membership.

    In order to support this feature we define a **relationship type** along
    which the membership inherits. 
    
    The pop-up help screen gives examples of the relationship types to
    select for this feature. Once you have selected a relationship type, you
    enter a number in **Max related** to set a maximum for the number of
    inherited memberships linked to each primary member. This would be
    useful, in the example above, to limit the number of employees that can
    become a member by virtue of their employment to 10 maximum. 

 ![image](../img/Membership_relationship_type.png) 

    With inherited memberships, we distinguish between the primary member
    and the members that inherit their membership due to their relationship with the primary member.


-   **Visibility**: Choosing **Public** means that this membership type will be able to be selected for inclusion on online membership sign up forms. If certain
membership types are only to be handled by an administrator manually
(e.g., honorary and lifetime memberships) you should choose **Admin**
here. 

-   **Order**: This determines where this membership type appears in a drop down
options list of membership types, and on membership sign up pages.

-   **Enabled**: If you have membership types that are no longer offered or not yet
available you may wish to untick this box. This will remove these
memberships from the user interface. It will not delete the membership
data and the membership can be re-enabled at a later date.

Membership status rules 
-------------------------

Membership status rules allow you to define a journey that contacts take
through their membership. These rules are defined in terms of the join,
start or end date of the membership. So let's first have a look at what
these dates mean.

Memberships have three primary dates, the join date, start date and end
date. The **join date** is the date the contact first signed up for a
membership with your organisation. Unless it is altered manually it
will never change from that first value. The **start date** is the date
the current *continuous period* of membership began. The **end date**
is the last day of the current membership.

By default the journey through membership statuses is as follows:

-   **Pending:** someone who has requested membership but has not paid.
    This status cannot be amended manually meaning that you can not
    change the status from pending to new unless you update the
    associated contribution record. For example, if you have the pay
    later option enabled for membership and Joe Smith signs up for your
    membership and chooses the pay later option, the status of his
    membership will not be changed to new until you change the
    contribution status of his related payment to Completed. 
-   **New**: member has just signed up for a membership or a pending
    payment has arrived. By default this lasts until 3 months after the
    membership start date. 
-   **Current**: new members move to this status after the new period
    has finished. As might be expected, the current status lasts until
    the membership end date.
-   **Grace**: when the end of the membership period is reached, someone
    who has not renewed membership enters this status for a period of
    time. They are still counted as a member. 
-   **Expired**: when the grace period expires, the member moves to this
    status and is no longer counted as a member.
-   **Deceased**: this status keeps a deceased contact's record in the
    system but removes the contact from all further communications. This
    status is set automatically based on a contact's deceased flag). 

You can force a membership to have its status overridden by selecting
**membership override** on a membership record and choosing a status. As
might be expected, a membership with status override will remain at that
status, and not be updated according to the membership status rules
described above. 

At **Administer > CiviMember > Membership Status Rules** you will find a
summary of the existing status rules.

![image](../img/z-sprint14-membership%20status.png)

To decide on which status should be applied, CiviCRM looks to see if the
membership has a status override. If it does, it applies that status. If
not, it looks at each status in turn starting at the top of the Status
Rules page until it finds one that is valid. That is to say, it looks to
see if today's date is between the start and end date for the membership
status at the top of the list. If it is, it applies that status, if not
it moves to the next status and repeats this process until it finds a
status that matches.

When you edit or add a new membership status the following form appears.

![image](../img/membership_status_rules.png) 

You can add new statuses and edit existing statuses (except for Pending
and Deceased) using this form. To create a new status, you need to
specify when the status should start and stop. This is done in relation
to a membership event (i.e. the join date, start date, or end date).
e.g. 'one month after the membership start date would be configured with
'start date' and '1 month' or 'five days before the membership end date'
would be configured with 'end date' and '-5 days'.

You also specify whether contacts with this membership status should be
considered members or non-members by checking or unchecking the 'Current
membership' tick box. (This results in a Yes or No in the Member column
on the status rules summary page.) Renewing contacts with a status that
defines them as members will have their existing membership end date
extended by the duration of the renewal. Renewing contacts with a
status that defines them as non-members get a new start date for their
membership and an end date based on that new start date.

Keeping membership statuses updated
-----------------------------------

When a membership is added or renewed the membership status is
automatically set based on your status rules. For example, a newly
created membership will be assigned the status "New" by default. If your
membership statuses are not updating automatically, make sure that
the **Update Membership Statuses** scheduled job is enabled and runs at
least once a day. Refer to the [Scheduled
Jobs](http://booki.flossmanuals.net/initial-set-up/scheduled-jobs)
chapter for configuration details and consult your system administrator
if appropriate. 

Collecting additional information about your members 
------------------------------------------------------

Sometimes you want to collect additional information about your
members. You can create one or more custom field sets for this
purpose. Custom field sets can be created for either all memberships or
specific membership types. If the information you want to collect
varies according to the membership type then you should set up more than
one custom field set linking it to the specific membership type(s). 
(Refer to *Custom Fields* chapter in the *Organising Your Data* section
for more details.) 
