Correspondance de vos données
=============================

Vos données existantes peuvent provenir de sources multiples, certaines sur support électronique ou imprimées sur papier et d'autres font appel la mémoire de vos membres. «La correspondance» fait référence à l'activité consistant à prendre des données existantes organisées d'une certaine manière et à les «placer» dans une structure CiviCRM. Il s'agit d'une étape très importante et ce passage peut causer des conséquences indésirables à l'avenir. Par exemple, il se peut que vous ne puissiez pas contrôler ou organiser les données de la façon dont vous esperez.

Chacun pense différemment à ses données en fonction de l'expérience avec un autre CRM ou pas de CRM du tout. Par exemple, «Dons», «Opportunité» et «Contribution» font tous référence aux sommes versées à votre organisation. CiviCRM a été conçu pour être flexible et adaptable, de sorte que vous ne devriez avoir aucun problème à trouver la place correspondante à chaque élément d'information pertinent pour votre organisation.

Résistez à la tentation d'ajouter des champs personnalisés immédiatement. Exemple: Au lieu d'ajouter un nouveau champ pour saisir manuellement les dates d'expiration des adhésions, découvrez le module d'adhésion de CiviCRM qui automatise la durée de l'adhésion, les rappels d'expiration et de renouvellement. Le fait d'avoir plusieurs champs pour collecter les mêmes données entraînera plus tard une confusion . Évitez la duplication des données en faisant des choix éclairés dès maintenant.

Les sections suivantes vous présenteront les options qu'utilise CiviCRM pour vous proposer des conseils sur la façon d'organiser vos données. Au lieu d'utiliser des feuilles de calcul «insipides», **les relations** lieront vos données ensemble. En utilisant les relations, vous serez en mesure de créer une vue plus complète de la communauté qui participe et soutient votre organisation.

Informations de base sur vos contacts
-------------------------------------

CiviCRM est créé avec des champs par défaut pour stocker les noms de contacts, adresses, numéros de téléphone, courriels, notes et autres informations. CiviCRM a été conçu pour les organismes sans but lucratif, la gestion de vos informations basiques devrait en être que plus facile.

CiviCRM divise en 3 catégories les Types de contacts en fonction de qui ou de ce qu'ils sont:

-   Individuels : Toute personne physique pour qui votre organisation veut conserver des informations. 
-   Organisations : une entreprise, une personne morale, un association, une section de votre organisation, ou un comité. Vous devez nécessairement créer au moins un contact du type Organisation pour représenter votre organisme. Cela est particulièrement utile lorsque vous configurez des abonnements.
-   Familles : Une famille ou un groupe de personnes qui partagent un lieu physique

Chaque type de contact est paramétré de base avec différents champs, en fonction des différents types de données que vous allez suivre. Par exemple, le genre (sexe) ne s'applique qu'aux individuels, ni aux organisations ni aux familles de sorte que ce domaine de genre n'est disponible que pour les types de contacts individuels et les sous-types(étudiants, bénévoles,...)

Pour en savoir plus sur les champs constitués de CiviCRM et comment les utiliser, consultez le chapitre *Contacts* de *Organisation de vos données*.

Informations sur les constituants spécifiques à votre organisation (introduction de base aux champs personnalisés)
---------------------------------------------------------------------------------------------------------------

De nombreuses organisations recueillent des données spécifiques à leur activité, leur mission ou à leur structure. Même si CiviCRM est livré avec des champs pour stocker les données de base que tous les organismes sans but lucratif recueillent, les similitudes entre les organismes à but non lucratif se terminent à un certain point. Par exemple, votre organisation peut être intéressée par des informations sur les allergies (pour les individus) ou au secteur d'activité (organisations).

Lors de l'organisation de vos données dans CiviCRM, décidez si l'information concerne une personne, une organisation ou un ménage. Des informations supplémentaires comme "secteur d'activité" n'ont de sens que pour les organisations. Pour savoir comment créer des champs personnalisés, consultez le chapitre *Champs personnalisés* dans *Organiser vos données*.

Relations entre les enregistrements
----------------------------------

Les relations saisissent les informations actuelles et historiques sur la façon dont deux enregistrements sont liés.

Vous même ou vos collègues en savez probablement plus sur vos contacts que sur ce qui a est écrit. Vous n'avez peut-être pas par le passé recueilli cette information parce qu'il n'y avait pas assez d'espace dans votre feuille de calcul ou que vous l'avez peut-être recueillie mais par vos propres connaissances ou relations avec une personne ou une organisation donnée. Le nom de leurs membres de la famille, le lien avec un employeur et l'interaction avec les autres membres de votre base de données peuvent tous être saisis avec une **Relation**.



CiviCRM comes with a predefined set of relationship Types including
"employer--employee", "parent--child", and "employee--employer". You can
create more relationships to describe your organization specific
relationships, for example you might define a relationship type of
"vicar--church". When you create a new Relationship, you can define when
the Relationship began and, if relevant, ends. Previous relationships
can still be accessed when they end. For example, you can see where
someone used to work even after the relationship has been severed.

The term Household and relationship Types "household member of--head of
the household" confuses many new CiviCRM users. It's useful to group
individuals who share a common address in one household, so that they
only receive one letter. The designation "head of the household" helps
organizations know who the letter should address. For example, you want
to address the parent and not the child.

To read more about configuring and using relationships, please see the
the *Relationships*chapter in *Organising Your Data*. 

Activities
----------

It is important to know how and when constituents engage with your
organization. Knowing that someone gives monthly or volunteers
frequently and renews her membership yearly suggests that she may
respond well to opportunities that strengthen her relationship with your
organization. CiviCRM allows you to record interactions such as phone
calls, emails, and meetings between staff and constituents. These
features help an organization build a lasting memory of its
relationships.

CiviCRM calls these kinds of exchanges Activities. They are tightly
linked to other CiviCRM modules. When you record contributions, event
attendance, membership subscriptions, and emails, CiviCRM will
automatically create a related activity in the Contact record. Decide
whether your organization needs different activity types in addition to
those provide, such as training, review, exam, support etc.

To read more about configuring and using activities, please see the
*Activites* chapter in *Organising Your Data*.

Webinars, events, performances, and meetings (CiviEvents)
---------------------------------------------------------

CiviCRM helps manage and track any occasion in which you bring community
members together at a certain place and time. Webinars, events,
performances, and meetings have specific start and end dates and times,
meeting places (including online) and reasons for bringing people
together. They can be ticketed, RSVP only, or no reservation required.
CiviCRM comes with functionality to promote events and record
registrations. If you have records of who has participated in past
events, you can transfer these valuable records into CiviEvents.

The **Event Types** field helps you to distinguish between different
types of events your organization hosts. This is helpful for evaluating
how many people have participated in a similar series of events or
whether someone prefers one kind of event over another.

To read more about configuring and using relationships, please see the
*Events* section later in this book.

Memberships
-----------

Many organizations offer a structured program in which community members
can sign up to receive certain benefits for a pre-defined period of
time. Members choose from a variety of dues levels that have associated
benefits, generally the more you give the organization the more you get
in return. Organizations can also give membership at no price, perhaps
as an award. For example, a long-time volunteer might receive a
life-time membership to the organization. Common benefits include access
to member directories, extra content, discounts, etc. Individuals,
families or households, and organizations can all sign up for
memberships.

The main difference between membership dues and a donation is that
memberships redefine someone's relationship to the organization for a
period of time. Organizations often expect that memberships will be
renewed from year to year, while a donation is a one-time gift.
Organizations need to send an acknowledgement letter, but they have not
promised to serve the donor advertised benefits in response to a
donation or Contribution in CiviCRM.

Analyze your current membership structure before importing membership
records into CiviCRM. Take time to eliminate unused membership levels or
simplify the benefits you promise. The only information you really need
to transfer for each member is start date, duration, membership dues
paid, and type of membership.

Generally speaking, having more than 10-15 membership types may be hard
to manage. Sometimes organizations may have many membership types in
order to preserve other information about constituents in the membership
record. It's recommended to verify first whether or not CiviCRM already
has existing data fields related to memberships to keep track of that
information before extending membership records.

Some information that you may have recorded as static information before
can now be calculated dynamically, and displayed in reports or other
fields. For example, CiviCRM can dynamically calculate the number of
years a given constituent has been a member based on the
"Membership since" date.

To read more about configuring and managing memberships, please see the
*Memberships*section later in this book.  

Contributions
-------------

Contribution in CiviCRM refers to money, goods, or services coming in to
your organization. Money is still money whether someone buys an event
ticket, signs up for a membership, or any other activity that requires
payment. CiviCRM allows you to record all money coming into your
organization as a Contribution with different Types to preserve
information about where it came from. You will also be able to specify
the date the contribution came in, it's status (you can record a
contribution as pending before the money is deposited to your bank
account) and the form it was delivered in (check, cash, etc.).

If you are planning to keep using an external donations system, you may
leave transactions there. On the other hand, you may want to transfer to
CiviCRM information about past event/webinar registrations because they
tell you the history of constituent involvement in your organization.
Also consider how far back you want to import the history of
contributions. Large contributions should be preserved, but the fact
that someone donated 5 dollars 10 years ago may no longer be relevant. 

To read more about configuring and using relationships, please see the
*Contributions* section later in this book. 

Campaigns
---------

Sometimes organizations host a fundraising gala, send an email appeal,
and record contributions all to support one goal. E.g., raise $50,000
to support a kids camp. Campaigns are usually time limited and tie
together a range of activities and give you a high-level view to compare
how people responded to your initiatives.

You can start taking advantage of campaigns if your organization's
fundraising initiatives fit well into a unique themes. Some examples of
campaigns are year end pledge drives, or project specific fundraisers.
Organizations often send several email appeals encouraging donors to
support a particular project or fundraiser, such as a 'final notice' and
one or more 'countdown' appeals.

Grouping and tagging constituents
---------------------------------

Development directors, volunteer coordinators, and program managers
store a wealth of information in their heads. They often make decisions
about who to invite to an event, who should not receive an appeal,
and/or who would be perfect for a volunteer opportunity.

Groups and tags can store that kind of information and act as the
building blocks for creating email and invitation lists. **Groups** are
useful to identify two or more contacts with something in common, as
opposed to relationships which can only capture information about two
contacts. Groups can also act as mailing lists. A group of people who
subscribe to your newsletter(s) is a good start. 

Organizations can have complex communication strategies, in which they
send different letters to several subsets of their community. One
Individual can be tagged member and volunteer, so that she receives
member specific communications as well as volunteer specific
communications. Groups are also useful to store issue or program
specific communication preferences. For example, consider a group of
people who have specifically requested not to receive fundraising
appeals. When you go to create an email appeal mailing, you can exclude
the group of Individuals who have requested not to receive fundraising
appeals.

Try to avoid creating groups based on information that can be stored by
other fields in CiviCRM. You don't need a group for individuals who have
opted-out of bulk mailings, because that option will be selected on
their Contact record. CiviCRM automatically excludes these constituents
from any bulk mailing. Likewise, you don't need a group called "donors"
because you can run an advanced search to find any **Contact** record
that has a **Contribution** associated with it, even between any date
ranges. Most functions available to groups are also available through
the search results screen.

If you want new records that meet a particular criteria to be
automatically added to a group, create a **Smart Group** from any
**advanced search**. For example, you may want to have a Smart Group
that calls the Contact record of all members who also donated more then
$100 in the past year. When a member makes a new $100 donation after
the group has been created, their record will be added to the Smart
Group.

**Tags** are more like keywords that you want to associate with a
record.  You can easily add or remove tags, but there is no easy way to
see the history of changes. Relationships are a much better tool for
seeing information history.

Profiles
--------

CiviCRM allows you to pull together sets of fields for different
purposes, and help you reduce the amount of time staff spends on
administrative tasks. These sets of fields are known as profiles.

Profiles are about how your data is edited or displayed to your staff or
other groups of users, not how your data is stored.

Read the *Profiles* chapter in this section for detailed information
about how to make use of profiles.

Where next?
-----------

In the sections above we've tried to describe how your existing data may
be mapped into CiviCRM. We've only touched on basic CiviCRM
functionality or "spaces" where your data may fit. To read more about
how CiviCRM can work with your data, please see information in this book
about specific CiviCRM components: **CiviEvent**, **CiviMember**,
**CiviMail**, **CiviContribute**, **CiviCase**, **CiviCampaign**, and
**CiviGrant**.

Each of the above components will help you streamline administrative
tasks related to event management, membership, sending communications,
receiving contributions and donations, case management, conducting
campaigns, administering grants programs, and more.

The sections on **Survey**, **Petition**, and **CiviEngage** (the latter
is actually a Drupal module) relate closely to **CiviCampaign** and
their special functionality is described in the respective chapters.

There is also a separate reporting section related specifically to using
reports and doing analysis on your data for ongoing evaluation of your
work. 
