Inscription en ligne à un événement
===================================

La possibilité pour les utilisateurs finaux de pouvoir s'enregistrer eux-même à des événements est bénéfique pour tout le monde : les participants peuvent s'inscrire au moment le plus pratique pour eux, et votre organisation économise du travail administratif. Ce chapitre détaille les étapes impliquées à la mise en oeuvre des inscriptions en ligne pour des événements.

Le processus standard pour l'inscription en ligne à un événement est le suivant :

![event_registrationflow_1](../img/CiviCRM-CiviEvent-event_registrationflow_1-en.gif "event_registrationflow_1")

Paramétrer l'inscription en ligne
---------------------------------

Pour afficher les paramètres, cochez **Autoriser l'inscription en ligne**.

![image](../img/event_online_rego_part_1.png)

Confirmez ou modifiez le texte qui s'affichera en tant que lien vers la page d'inscription (par défaut, "S'incrire maintenant"), et indiquez les dates de début et de fin pour les inscriptions en ligne. Ces dernières définissent la période durant laquelle le formulaire d'inscription sera en ligne sur le site. Elle peut se terminer avant la date de l'événement lui-même, afin de vous laisser le temps de réaliser des tâches de préparation selon le nombre de participants.

Activer **Inscrire plusieurs participants** permet l'inscription et le paiement pour plusieurs personnes sur une seule transaction. Par exemple, vous organisez une conférence, et des personnes souhaiteront inscrire également leur partenaire et payer pour les deux en un seul processus.

Par défaut, cette option nécessite un nom et une adresse courriel différents pour chaque personne enregistrée. Cocher **Même adresse électronique ?** permet d'avoir une adresse commune. Dans les deux cas, CiviCRM utilise des enregistrements de contact distincts (soit existants, soit créés à la volée) pour chaque personne inscrite.

La **Règle de dédoublement** est expliquée plus loin dans la sous-section [Correspondance de contact et gestion des doublons](#correspondance-de-contact-et-gestion-des-doublons) de ce chapitre.

**Expiration des inscriptions en attente (en heure)** est le temps alloué aux participants pour confirmer / terminer leur inscription dont le statut est "en attente". Cela fonctionne avec la tâche programmée **Mettre à jour les statuts des participants** (voir **Administrer** > **Paramètres système** > **Travaux programmés**). Si l'un et l'autre sont activés, une inscription en attente doit être finalisée dans la période de temps spécifiée. Dans le cas contraire, l'inscription sera annulée et le participant notifié par courriel. Cette fonctionnalité est très utile lorsqu'elle est combinée avec les rappels automatiques pour gérer automatiquement les inscriptions *En attente de paiment*, si vous avez autorisé l'option de paiement sur votre formulaire d'inscription en ligne (cf le chapitre [Rappels programmés](../email/scheduled-reminders.md) de la section Courriel pour plus d'information).

L'étape suivante consiste à définir le texte et les champs servant à collecter les informations, et qui seront affichés dans la page d'inscription en ligne.

![image](../img/event_online_rego_part_2.png)

Le **Texte d'introduction** sera affiché en haut de la page, et le **Pied de page (texte)** en bas. Tous ou certains champs seront affichés entre les deux : profil, tarif, détail de la carte de crédit...

Collecter les informations sur les participants à l'aide des profils
--------------------------------------------------------------------

La meilleure façon de collecter de l'information durant une inscription en ligne est d'inclure un ou plusieurs profils dans la configuration de votre événement. Vous pouvez en mettre un immédiatement après le message d'introduction, et un ou plusieurs en dessous des tarifs et des détails de paiement (des informations détaillées sont disponibles dans le chapitre [Profils](../organising-your-data/profiles.md) de la section *Organiser vos données*).

Lorsque vous créez un formulaire d'inscription en ligne, le profil *Vos informations d'inscription* est sélectionné par défaut. Il consiste en trois champs : le prénom, le nom et l'adresse courriel. Toutefois, CiviCRM n'a besoin pour ses enregistrements de contact soit du prénom et nom, soit d'une adresse courriel. Vous pouvez donc modifier ce profil, ou en créer un nouveau requérant moins de champs. Si vous choisissez de ne pas collecter les adresses courriel, pensez à décocher l'option **Envoyer un courriel de confirmation ?** en bas.

ATTENTION : si vous modifiez un profil existant pendant le paramétrage de votre page d'inscription en ligne, le changement s'appliquera partout où ce profil est utilisé. Donc à moins qu'un profil existant ne corresponde *exactement* avec vos besoins, vous devriez plutôt faire la copie de l'un d'eux, le renommer, le modifier et enfin l'appliquer à votre page.

Une autre façon de faire est d'en créer un totalement nouveau, sans quitter la configuration de votre page d'inscription en ligne. L'interface *glisser-déposer* vous permet également de créer des champs personnalisés à inclure dans votre profil. Ces champs peuvent être créés pour tous ou certains types d'événements, et tous ou certains rôles de participants (cf. le chapitre [Données personnalisées](./custom-data-for-events.md) de cette section). 


![image](../img/Drag_and_drop_profile_for_event.PNG)


Confirmation d'inscription
--------------------------

Une fois votre page d'inscription configurée, vous aurez besoin d'entrer le texte à afficher sur la page de confirmation, la page de remerciement, et envoyer par courriel les confirmations et accusés de reception (si vous en avez activé l'option).

Pour les événements gratuits, l'étape de confirmation est sautée. Pour les événements payants, le processus de paiement s'effectue entre la page de confirmation et celle de remerciement. 

Pour la plupart des événements, il sera utile d'activer l'option du courriel de confirmation. Pour les événéments payants, ce courriel sert également de reçu. Assurez-vous que l'adresse **Courriel de l'expéditeur pour la confirmation** soit un compte courriel valide de votre serveur de messagerie. Ajoutez une ou plusieurs adresses dans le champ **CC confirmation à** si vous souhaitez informer en temps réel des membres de votre organisation sur les participants.

![OnlineRegEmail](../img/CiviCRM_update-CiviEvent-OnlineRegEmail-en.png "OnlineRegEmail")

Veuillez noter que le contenu du champ **Texte** sera généré en texte brut ET en HTML. Nous ne recommandons donc pas d'y inclure des tags HTML de formatage.


Fonctionnalités optionnelles d'inscription à un événement
---------------------------------------------------------

### Liste d'attente

Un événement peut accueillir un nombre limité de participants (par exemple, 25 personnes pour un atelier). CiviEvent vous permet de configurer un nombre maximum de personnes autorisées à s'inscrire à un événement. Lorsque ce nombre est atteint, CiviEvent désactivera les inscriptions mais enverra un message automatique disant "L'événement est actuellement complet". Vou pouvez personnaliser ce message, et configurer une liste d'attente de type "premier arrivé, premier servi".

Cette liste fonctionne de la manière suivante :

-   Quand une place se libère (par exemple lorsqu'une personne annule son inscription), les participants en liste d'attente auront le statu changé en *En attente (depuis la liste d'attente)* et un courriel automatique leur sera envoyé avec un lien leur permettant de compléter leur inscription (y compris la méthode de paiement si applicable).
-   People will remain pending for a certain amount of time defined in
    Pending participant expiration (hours). This gives them a window of
    opportunity to register. 
    You can set the amount of time, measured in hours, that you set on
    the **Online registration** tab under Pending participant expiration
    hours. If you want, you can set this to 0 for no limit.
-   After this period of time, they will be moved to expired and other
    people on the waitlist will be given the opportunity to register.

If you'd like to enable the Waitlist feature, you must first enable the
related participant statuses **On waitlist** and **Pending from
waitlist**. You can do this in **Administer > CiviEvent > Participant
statuses**. You can then check the **Offer Waitlist** checkbox on
the **Info and settings** tab, and set the message you want displayed on
the event information page when the event is full.

![EventInfo2](../img/CiviCRM_update-CiviEvent-EventInfo2-en.png "EventInfo2")

Note that in order for the status processing to happen, you need to have
the **Update Participant Statuses** scheduled job
running (see **Administer > System Setting > Scheduled jobs**).

### Participant approval

Many events are open to everyone, but there may be times when your
organization invites only specific people to the event. For example, you
could invite volunteers who have donated 100 or more volunteer hours to
an appreciation dinner. The people invited may talk about the event to
their friends, and possibly forward the information. With CiviEvent, you
can check who has registered and approve only the people invited.

If you'd like to enable the 'Participant approval' feature, you must
first enable the related participant statuses Awaiting approval and
pending from approval. This is similar to what you do for waiting lists
and you can do it in **Administer > CiviEvent > Participant
statuses**. You can then check the **Require participant
approval** checkbox on the **Online registration **tab, and set the
message you want displayed in the approval message. You can also limit
the amount of time participants have to complete their registration
after approval by entering the time in hours in the Pending participant
expiration field. For example, if you want to give participants 3 days
to complete their registration, enter "72" in that field. 

Now, when a person registers for the event, they will get a reply that
says, "Your registration has been submitted. Once your registration has
been reviewed, you will receive an email with a link to a web page where
you can complete the registration process." This reply can be customized
to your organisation's needs.

Participants will be placed in 'Awaiting Approval' status. You can
review and approve participants from 'Find Participants' - select the
'Change Participant Status' task. Approved participants will move to
'Pending from approval' status, and will be sent an email with a link to
complete their registration (including paying event fees - if any)

Note that in order for the status processing to happen, you need to have
the **Update Participant Statuses** scheduled job running
(see **Administer > System Setting > Scheduled jobs**).

### Personal Campaign Pages

If you enable Personal Campaign Pages (PCPs), you offer completed event
registrants the ability to create and customize a page of their own to
either:

-   promote the event for which they registered

-   promote an online contribution page

For more information see **Contributions > Personal Campaign Pages** in
this book. This is the last step in creating an event. Click **Save and
Done.**

Correspondance de contact et gestion des doublons 
-------------------------------------------------

Whenever we allow people to interact with our database from 'the
outside' we run the risk of creating duplicate contacts. There are
various ways to deal with this. For example, some websites require you
to be logged in at all times when doing important things and we can do
the same for CiviCRM using permissions (just take away the register for
events permission from anonymous users and give it to logged in users,
or a specific role). Depending on the type of event that you are
running, this might not be a good idea. Lets say you are running a
conference, or AGM and you want as many people as possible to register.
Requiring them to log in wil decrease the amount of registrations.

Lets say, we don't require people to log in to register for an event.
Consider the following situation. James Martin registers for an event.
James Martin is already in our database. How do we match up the James
who is registering with the one that is in the database. What about if
there are two James Martins in our database. One that lives in London,
and one that lives in Paris. How do we know that we have found the right
one? The answer is duplicate rules.

You can read more general and more detailed information about duplicates
and merging in the *Deduping and merging* chapter and we recommend that
you get familiar with that chapter at some point. This section just
covers contact matching and duplicate management in the context of
CiviEvent.

![image](../img/event-duplicate-matching.png)

By default, CiviEvent uses the Unsupervised rule to do matching. When
you configure an event for online registration, you can override the
default by selecting a different duplicate matching rule for matching
participants for this particular event. The rule you select takes effect
for the primary participant and any additional participants. 
 
The Online Registration tab checks for whether the included profiles
have enough fields to have a chance at matching participants to existing
contacts. It reviews the possible combinations of matching fields that
would satisfy the matching rule in effect for the event, and it checks
to see if any of those combinations is present among the fields in the
included profiles. The warning "Duplicate Matching Impossible" appears
if there's no way to match duplicate contacts using the rule, while the
warning "Duplicate Contacts Possible" appears if enough fields are there
but not all of them are required.

Registration permissions
-------------------------

If you've enabled online registration for events on your site you need
to review the Drupal user permissions to ensure that visitors are able
to view event information and complete the registration forms. Navigate
to **Administer > Users > Permissions**.

Most organizations allow anonymous users (users who have not logged in)
to view and register for events. If you want to allow this, you must
assign the following CiviCRM module permissions for the anonymous user
role: 

-   access all custom data - required if you are collecting information
    in custom fields from registrants
-   profile create - required if you've included any profiles in your
    online registration forms
-   register for events
-   view event info
-   view event participants - required if you want to display a listing
    of registered participants. 

If you want to exclude anonymous visitors from viewing or registering
online for events, assign these permissions to an authenticated user
role.

CiviCRM has an additional permissioning system known as Access Control
Lists (ACLs) ACLs allow you control access to CiviCRM data. Note that a
CiviCRM ACL Role is not related to the Drupal Role. Refer to the
*Permissions and access control* chapter for more information. 

If you need to limit access control for specific events, you can use the
Manage Access Control feature to assign access to specific groups of
contacts.

Testing the registration process
--------------------------------

Before revealing your event to the public, you should always test the
event registration process. This can be done as follows:

1.  Navigate to **Events > Manage Events**.
2.  From Event Links, select **Test-drive** to test the registration
    page. Test-drive mode will use the sandbox options for your payment
    processor, if available, and will create a registrant record with a
    test indication so that it can be reviewed and easily removed.
3.  Fill out the registration form and complete the registration
    process.
4.  In order to find the new test participant record, navigate
    to **Events > Find Participants**.
5.  In the search criteria, check the box **Find Test Participants**.
6.  If you need to adjust the event settings, navigate to **Events > Manage Events** and click the **Configure** link for this event.
7.  If you discover elements that you need to edit and adjust,
    select **Configure** to return to the list of event setting pages.
8.  If you have events where anonymous users register for events, you
    should also test the registration when not logged in. Refer to the
    Event Permissions information later in this chapter for details.

Once you are satisfied with the event information and registration form,
it's time to display it on your website. Below are details of how to do
this.
