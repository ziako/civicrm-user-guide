Ce que vous avez besoin de savoir
=================================

Afin de pouvoir utiliser CiviPledge, vous devez l'activer pour votre installation si ce n'est pas encore le cas. Aller à **Administrer** > **Paramètres système** > **Composants**, et déplacez CiviPledge dans la colonne de droite.

Nouvelles promesses de don
--------------------------

Pour créer une nouvelle promesse de don au nom d'un contact, aller à **Contributions** > **Promesses de don** > **Nouvelle promesse de don** (notez qu'un particulier peut faire lui-même sa promesse de don : cf. le chapitre [Contributions en ligne](../contributions/online-contributions.md) pour plus de détails.).

Les options suivantes sont disponibles :

-   **Sélectionnez le contact** : entrez le nom d'un contact existant, ou créez-en un nouveau avant de renseigner la promesse de don (une nouvelle fenêtre s'ouvrira) ;
-   **Montant total de la promesse de don** : entrez le montant total qui sera donné ;
-   **À payer en**: spécifiez le nombre de versements et, s'il est supérieur à un, leur périodicité ;
-   **Les paiements sont dûs le** : choisissez le jour de la période auquel chaque versement est fait (par ex. le deuxième jour de la semaine / mois / année) ;
-   **Promesse de don faite le** : sélectionnez la date à laquelle la promesse de don a été faite ;
-   **Début des paiements** : indiquez la date de départ du premier versement ;
-   **Envoyez accusé de réception ?** : si les courriels sortants sont configurés, et que le contact dispose d'une adresse courriel, vous pouvez activer cette case à cocher pour lui envoyer une notification ;
-   **Date de réception** : date à laquelle le contact a été notifié de la création de sa promesse de don (remplie automatiquement si un courriel a été envoyé - cf. option précédente) ;
-   **Type d'opération** : choisissez le type financier pour les paiements liés à cette promesse de don (don, abandon de frais...) ;
-   **Campagne** : Si elle est disponible, vous pouvez associer la promesse de don à une campagne de levée de fond ;
-   **Page de paiment en ligne** : donne au donateur la possibilité de faire lui-même le paiement à travers un formulaire de paiment en ligne ;
-   **Contributions faites en l'honneur de %1** : vous pouvez également donner le nom de la personne à qui vous dédiez votre promesse de don ;


![image](../img/new_pledge2.png)

Rappels de paiement
-------------------

Un ou plusieurs rappels de paiement peuvent être envoyés par courriel au donateur avant leur date d'échéance. Si une page de paiement en ligne a été renseignée (voir plus bas), le courriel inclura un lien pointant sur cette dernière.

Pour que les rappels puissent être envoyés :

1.  La tâche planifiée *Process Pledges (process_pledge)* doit être active afin d'automatiquement mettre à jour le statut des promesses de don et envoyer les rappels de paiement par courriel. Ou bien un cronjob peut être planifié pour faire tourner cette tâche en dehors des autres tâches planifiées. Pour plus d'information, veuillez vous référer au chapitre [Travaux programmés](../initial-set-up/scheduled-jobs.md) ;
2.  Le donateur doit avoir une adresse courriel valide et ne pas avoir coché l'option "Ne pas envoyer de courriel" dans sa fiche contact ;

Once these pre-requisites have been met, you can choose the payment
reminder schedule for an individual when creating a new pledge. The
settings are:

-   **Send initial reminder**: enter the number of days, prior to the
    payment date, that a reminder will be sent
-   **Send up to**: specify the maximum number of reminders an
    individual will receive for one scheduled payment
-   **Send additional reminders**: set the interval period between
    reminders, by the number of days, e.g. 5 days before the next
    reminder is sent.

Self service payments
---------------------

A donor can be given the option to make a scheduled payment online if a
contribution page (with payment processor) has been created. To do this,
select a contribution page from the drop-down menu 'self-service
payments page' when creating a new pledge. If reminders have been
enabled for the pledge, a link to this page will be included in the body
of the emails.

Finding Pledges
---------------

To search for existing pledges, go to: **Contributions > Pledges >  Find Pledges**. You may search by name, email address, or any
discrete feature of the pledges themselves (e.g. payment start date,
pledge status and honoree information). The search results page will
display a summary of the pledges found, and view, edit and delete
options are available for each record at the end of the rows. If the
status of a pledge is 'in progress', there is also an option to cancel
the pledge.

![image](../img/pledge_menu.png)

Dashboard
---------

You can view a list of recent pledges and a summary table of pledges
recorded over the current month and past year on the pledges dashboard.
This can be reached through the Contributions menu: **Contributions >
Pledges > Dashboard**.

![image](../img/pledge%20table.png)
