Maintenir des listes de diffusion à jour
========================================

Dans le précédent chapitre, nous avons parlé de la création et du paramétrage des listes de diffusion. Dans ce chapitre, nous allons creuser un peu plus le sujet de la gestion des listes et parler conformité. Il est important de garder ses listes de diffusion avec un taux de rebonds faible et peu de désabonnements.

Il y a également le risque de la redoutée "blacklist" si vous avez un taux de rebond très élevé, ou celui d'être réprimandé par votre fournisseur smtp pour la même raison. Quoiqu'il en soit, gérer les taux de rebonds et les désabonnements représente un important et compliqué enjeu pour votre organisation.

Comprendre les rebonds de courriel
----------------------------------

Chaque fois que vous faites un envoi massif de courriels depuis CiviMail, il est possible que certains d'entre eux rebondissent, c'est à dire qu'un courriel d'erreur spécifique à un destinataire est renvoyé en retour. Les rebonds se produisent pour plusieurs raisons, certaines temporaires et d'autres permanentes.

### Pourquoi les courriels rebondissent ?

Si un courriel d'erreur est renvoyé, celui veut dire qu'il n'a jamais atteint sa destination. Les raisons peuvent être les suivantes :

1.  il y a une erreur de frappe dans l'adresse courriel ;
2.  l'adresse courriel n'existe plus ;
3.  la boite de réception du destinataire est pleine et ne peut temporairement plus accepter de messages supplémentaires ;
4.  le destinaire a configuré un message de réponse automatique (absence temporaire, etc).

CiviCRM gère ces différents types de rebonds différemment. Les rebonds temporaires n'affecte pas l'enregistrement d'un contact, et CiviCRM tentera de renvoyer le courriel plus tard. En revanche, le système mettra en **Suspendu** tout courriel de contact provoquant un rebond permanent. Dans ce cas, aucun courriel ne sera plus envoyé à cette adresse, jusqu'à ce que quelqu'un resolve le problème et retire ce statut.

Une table détaillée indiquant le nombre par type de rebonds acceptés par CiviCRM avant que ce dernier ne mette l'adresse du contact en **suspendu** est disponible dans le manuel adminsitrateur à la page [inbound mail](https://docs.civicrm.org/sysadmin/en/latest/setup/civimail/inbound/)


### Que dois-je faire si une adresse courriel est suspendue ?

Vous avez basiquement deux options : enlever le statut "suspendu" à l'adresse courriel, ou corriger/supprimer l'adresse.

Pour enlever le statut "Suspendu" :
1.  Aller dans **Recherche avancée**
2.  Dans **Critères de base**, cochez "**Courriels suspendus**
![image](../img/Mailing%20Basic%20Search.png)
3.  Une fois obtenu la liste des contacts concernés, selectionnez les et choisissez l'action **Enlevez la suspension** de la liste déroulante et cliquez sur **Lancer**

Pour corriger / mettre à jour les adresses, vous devez d'abord créer un groupe (destiné à contenir les adresses en erreur), puis :
1.  Dans le menu supérieur, allez à **Rapports**
2.  Sélectionnez **Rapport des rebonds de courriels**
3.  Le rapport vous montrera la listes des contacts pour lesquels les courriels rebondissent.
4.  Vous pouvez alors ouvrir **Critères de rapport** dans la partie supérieur pour filtrer le rapport à un type précis de rebond
5.  À partir d'ici, vous pouvez ajouter les contacts issus de votre recherche au groupe précédemment créé.
6.  Listez le groupe via **Recherche avancée**, en cochant à nouveau **Courriel suspendu** au cas où des mises à jour auraient déjà été effectuées sur certains contacts.
7.  Select **Batch Update via Profile** for all the results whose email
    addresses you can correct/update. This will require a profile in
    place that contains *just* **Primary Email**.
8.  Select this profile and click **Update**.

### The difference between on hold emails and unsubscribes

Emails that have been held are different from emails that have been
unsubscribed. Unsubscribers have clicked the linked text in an email
that said “unsubscribe from this mailing”. This link is created by one
of these tokens in an email: **{action.unsubscribe}** or
**{action.unsubscribeUrl}**

Email recipients who unsubscribe from a single mailing list will simply
be removed from the group you used as a mailing list to send to.

### What is the difference between opting out and unsubscribing?

Email recipients also have the option of not receiving any bulk emails
from you by clicking a link you provide in every mass email. This is
called "opting out". You can still send individual or small volume
emails to someone who has opted out using the **Send Email** action
which is accessible via the contact's record or after a search.
Scheduled reminders will also still be sent to contacts who have opted
out. You should be very careful about the emails you send to someone who
has opted out if you do not want to be accused of sending spam. 

To opt out, an email recipient can click the linked text in an email
created by one of these opt-out tokens: **{action.optOut}
{action.optOutUrl}**

You can include these tokens directly in the body of your mailing or in
a footer message. (For more on tokens, see here:
[http://wiki.civicrm.org/confluence/display/CRMDOC/Tokens.](http://wiki.civicrm.org/confluence/display/CRMDOC/Tokens.)
For more on footers, see the previous section in this chapter, *Set up > Creating headers and footers.*)

### What does the privacy option 'Do not email' mean?

If a contact has this option selected then you will not be able to send
them individual or small volume emails using the **Send Email** action
reached via the contact's record or after a search. They will not
receive bulk emails sent through CiviMail, either. However they will
still be sent scheduled reminders unless you specifically exclude them
from those reminders. If the **Do not email** option is set manually
after someone has contacted you in person, it is probably a good idea to
exclude them from scheduled reminders. The *Schedule Reminders* chapter
outlines how to do that.

### How can I make sure a contact doesn't receive any emails?

Due to user error, there is always a chance that someone could change
CiviCRM settings incorrectly or manually misuse an email address. The
only way to fully guarantee that a contact doesn't receive any emails is
to remove all email addresses from the contact's record. However, in
this case the contact would not be able to log in to your website.
