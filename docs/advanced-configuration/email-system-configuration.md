Configuration de la messagerie électronique
===========================================

Ce chapitre traite de la configuration système nécessaire pour que CiviCRM puisse envoyer et recevoir des courriels. Il s'agit d'une tâche complexe qui nécessite des compétences du niveau administrateur système. La configuration correcte de votre système de courrier électronique est cruciale pour empêcher votre serveur de recevoir des spam ou des black lists.

Reportez-vous à la "Section des courriers électroniques" au chapitre "Configuration des tâches" pour configurer l'envoi des messages après que les paramètres de configuration du courrier électronique soient effectués.

Certaines parties de la configuration sont une fonctionnalité native de CiviCRM (envoi et réception de courriels de base) alors que d'autres (envoi groupé) nécessitent l'activation du composant CiviMAIL.

Vous aurez peut-être besoin de modifier la configuration de votre DNS, créer des comptes de messagerie, configurer une tâche cron, lire les en-têtes des messages électroniques et éventuellement modifier la configuration de votre serveur SMTP.

Ce chapitre suppose que vous exécutez CiviCRM sur un serveur Linux et que vous êtes à l'aise pour travailler avec le shell et exécuter des commandes simples. La plupart de ces étapes seront similaires sur d'autres systèmes d'exploitation, mais vous devrez les adapter à votre système et à vos outils.

La configuration décrite ici fonctionne bien pour les envois jusqu'à environ 10 000 personnes. Si vous prévoyez d'envoyer des courriels à des centaines de milliers de contacts, vous devriez comparer plusieurs options et envisager un serveur SMTP dédié. Cette configuration plus complexe est en dehors de la portée de ce livre, mais vous pouvez trouver des instructions fournies par la communauté sur le wiki de documentation CiviCRM : ([http://wiki.civicrm.org/confluence/display/CRMDOC/CiviMail+Installation](http://wiki.civicrm.org/confluence/display/CRMDOC/CiviMail+Installation)).

Dans ce chapitre, nous utiliserons une adresse de boîte aux lettres Gmail externe pour tester la configuration. Donc la première étape est de créer un compte Gmail si vous n'en avez pas déjà. Vous pouvez également utiliser une autre adresse pour tester les procédures de ce chapitre, mais vous devrez pouvoir afficher la source des messages reçus

Une fois que votre système est correctement configuré, nous allons utiliser un cron CiviCRM dans **Travaux programmés** et s'assurer que vos envois programmés sont bien envoyés.

Configuration du service de messagerie sortant
----------------------------------------------
Les paramètres de messagerie sortante sont configurés sur: **Administer> Paramètres système> Courriel sortant (SMTP / Sendmail)**. Les choix sont : 

![Screen shot of mail choices](../img/Administer-System Settings-Outbound Email.png)

-   **mail()**: C'est l'option par défaut et si elle fonctionne pour vous, vous devez l'utiliser.
-   **SMTP**: Si vous avez un serveur de messagerie externe dédié, veuillez en spécifier les détails ici. Les messages de rebond générés avec SMTP sont légèrement plus complets que ceux de mail (), mais il n'y a aucun avantage pratique à utiliser SMTP si vous pouvez utiliser mail ().
-   **Sendmail**: Cette option est conservée pour la compatibilité avec les anciennes versions CiviCRM.
-   **Désactiver l'envoi de courriels**: Fonctionne comme indiqué.
-   **Redirection vers base de données**: Tous les e-mails seront enregistrés comme des envois archivés au lieu d'être envoyés. Ils peuvent être trouvés dans la table civicrm_mailing_spool de la base de données CiviCRM.

Après avoir fait votre choix, envoyez un email de test à votre adresse sur Gmail et vérifiez que vous le recevez.

Si vous recevez le message d'erreur suivant, vous devrez configurer une adresse de courrier électronique "DE" par défaut (Voir chapitre sur la configuration de CiviMail).

```
Sorry. A non-recoverable error has occurred.
The site administrator needs to enter a valid 'FROM Email Address' in
Administer -> Configure -> Domain Information.
The email address used may need to be a valid mail account with your email service provider.

```
Dès que vous avez reçu le courrier électronique, vous devrez consulter la source. Cela se fait dans Gmail en cliquant sur "Afficher l'original" dans l'e-mail que vous avez reçu. Le courrier électronique doit contenir une en-tête qui ressemblent à ce qui suit :

```
Received: from yourmailserver.example.org (xxx.example.org
[12.45.120.30])
by mx.google.com with ESMTP id e31si4519230wej.3.2010.04.26.00.38.16;
Mon, 26 Apr 2010 00:38:17 -0700 (PDT) Received-SPF: pass
google.com: best guess record for domain of
[youremail@example.org](mailto:youremail@example.org) designates
12.45.120.30 as permitted sender) client-ip=12.45.120.30

```

Explications : 

*"Received: from..."* Doit correspondre à votre serveur de messagerie et être correctement configuré. Il se peut que cette entête contienne des informations sur votre fournisseur d'hébergement au lieu de votre nom de domaine. Ce n'est pas un problème tant que le serveur de messagerie est correctement configuré. Si vous avez une adresse IP dédiée à votre serveur, vous devez essayer de configurer un DNS inverse qui représente votre organisation au lieu du nom par défaut.

*"Received-SPF"*  L'en-tête doit indiquer "pass" ou "neutral". Sender Policy Framework (SPF) est décrit plus loin en détail.

L'envoi de courrier en nombre important nécessite beaucoup de ressources. Nous ne recommandons pas d'envoyer des messages électroniques à partir de fournisseurs d'hébergement "low-cost". Le temps que vous passerez en dépannage coûtera souvent plus cher que l'abonnement chez un hôte plus professionnel. Vérifiez avec votre fournisseur d'hébergement  les limitations du nombre d'envoi par 24 heures ou par heure et s'il exécute PHP en mode sans échec.

Certains serveurs de messagerie de vos destinataires utilisent DNSBL (services de liste noire) qui gardent une liste noire d'adresses IP susceptibles d'envoyer du spam. Le courrier de ces serveurs sera marqué comme spam et n'atteindra pas sa destination. Si votre serveur est mis en liste noire (par exemple, parce que un nombre suffisant de destinataires ont marqué votre courrier électronique comme du spam, ou parce qu'un autre site Web sur votre serveur a été marqué comme spam), vous devrez contacter les organisations qui vous ont mis en liste noire et les convaincre de votre bonne foi.

Il existe plusieurs sites Web qui vous aident à tester si vous êtes dans un DNSBL. Une recherche sur le Web pour "blacklisting email" va transformer certains envois. Testez régulièrement pour savoir si vous êtes sur une liste noire.

Configuration du Sender Policy Framework (SPF)
----------------------------------------------

Par défaut, Internet permet à tout serveur de messagerie d'envoyer un courrier électronique prétendant appartenir à n'importe qui. Cela permet aux spammeurs de fabriquer facilement des adresses et d'envoyer du spam à l'aide de votre adresse de courrier électronique (ou de tout autre). SPF vous permet de créer un enregistrement DNS spécial répertoriant les adresses IP des serveurs de messagerie qui peuvent légitimement envoyer des e-mails à partir de @*votredomaine.org

Si votre nom de domaine a déjà un enregistrement SPF, assurez-vous qu'il inclut l'adresse IP de votre serveur de messagerie CiviCRM (qui peut être différent de l'hôte utilisé pour le serveur Web ou de vos serveurs de messagerie). Si ce n'est pas le cas, ajoutez cette adresse IP.

Si vous n'avez pas d'enregistrement SPF, pensez à en ajouter un. Vous devrez ajouter au moins votre serveur de messagerie et le serveur CiviCRM (s'ils sont différents) à l'enregistrement SPF.

Vous pouvez en savoir plus sur le SPF ici : [http://www.openspf.org](http://www.openspf.org)

## Configuration du traitement des e-mails entrants

Cette section explique la configuration du traitement des rebonds et le réception automatique des courriels entrants. La configuration de **Tâches planifiées** pour effectuer le traitement des rebonds réels est développée plus loin dans ce chapitre.

### Traitement des rebonds

CiviCRM peut recevoir automatiquement la [notification d'email renvoyée] (http://en.wikipedia.org/wiki/Bounce_message) et, selon le [type de rebond] (http://tools.ietf.org/html/rfc3463) signalé par le serveur du destinataire, impactant vos contacts en conséquence. Pour ce faire, vous devrez configurer une boîte aux lettres de messagerie pour recevoir des e-mails non reçus ainsi qu'un calendrier **job - Bounces Fetcher**  qui lira périodiquement cette boîte aux lettres et mettra à jour vos contacts dans CiviCRM.

Administration> Paramètres système> Emplois planifiés

![Screen shot of bounce fetcher scheduled job](../img/administer-scheduledjobs.png)

L'adresse e-mail de rebond est une adresse e-mail "invisible" que l'on voit uniquement dans les champs cachés qui précèdent les en-têtes et le message ajouté par l'utilisateur. Choisissez un nom significatif pour cela. Dans cet exemple, nous avons choisi *return*, l'adresse email que nous devons configurer sur un serveur de messagerie *example.org*  est *return@example.org*.

Pour chaque e-mail envoyé via la fonctionnalité d'envoi massif de CiviMail, une nouvelle adresse d'expéditeur "invisible" unique est créée à l'aide du [chemin de retour d'enveloppe variable ou 

For each email sent via CiviMail's mass mailing feature, a new unique "invisible" sender address is created using the [variable envelope return path ou VERP](http://en.wikipedia.org/wiki/Variable_envelope_return_path). Lorsque CiviCRM reçoit un rebond, il regarde l'adresse de l'expéditeur invisible pour décider quel email a rebondi. 

CiviCRM examine ensuite le modèle et le type de rebond pour décider de l'action à entreprendre. Les types de rebond se répartissent en deux catégories de base: les défaillances permanentes (hard bounce) et les défaillances transitoires (soft bounce). Un seul défaut permanent déclenche CiviCRM pour définir l'adresse e-mail du contact en attente. Pour les défaillances transitoires, CiviCRM attend plusieurs rebonds avant de définir l'email du contact en attente.

Le [seuil spécifique pour chaque type de rebond] (http://wiki.civicrm.org/confluence/display/CRMDOC43/Bounce+Handling) se trouve dans les tables "civcirm_mailing_bounce_pattern" et "civicrm_mailing_bounce_type". Plusieurs motifs de réponse de rebond différents sont liés à un type et un seuil donné.

### **Email-to-Activity processing**

CiviCRM can automatically retrieve email from a specified inbox and file
it as an email activity against contacts of type Individual corresponding to
sender and recipients of the email. New individual contacts are created for
email addresses not already assigned to individuals in the database.

**NOTE**: This features only works for the Individual contact type. If the
incoming email comes from an email address already recorded against an
organization, a new individual contact with that same email address will be
created and the activity will be recorded against that new individual contact,
not against the organization.

There are two ways to do this (either or both ways can be setup at same
time):

-   **Special email address:** Set up a special email address for your
    organization, e.g. civiemails@example.com. Users can then add this
    address in the Bcc field for your outbound emails; they will get
    auto filed in CiviCRM as described above. No one who receives the
    email will see this special address if the Bcc field is used.
-   **IMAP folder:** Set up a folder in your IMAP Inbox where you can
    drag emails that you want filed in CiviCRM. This works with both
    inbound and outbound emails (this requires that your email be set
    up using IMAP.)

### Special email address for incoming email

There are several ways of configuring your incoming mailbox:

-   **Sub-addressing:** Your mail service might allow you to append a
    +*tag* or -*tag* qualifier to your e-mail address (e.g.
    *return+test@example.org*). Several mail servers, including Gmail,
    Yahoo! and Postfix provide this sub-addressing by default.

    Try to send yourself an email, adding a +*tag* or -*tag*. If you
    received the mail you sent with a tag, it means that you can
    directly use the mailbox you created (*return@example.org* in our
    example) as the [VERP](http://en.wikipedia.org/wiki/Variable_envelope_return_path).

-   **"Catch-all" account:** If sub-addressing doesn't work on your mail
    server, you need to define the mail account you created
    (*return@example.org*) as the "catch-all" account. Every mail sent
    to an address that isn't a real mail account will end up there,
    including all the bounced email messages.

-   **External address**: If neither of the preceding methods works,
    consider creating a new account on a service such as Gmail and use
    it to receive the bounced emails. You will have to set filters in
    this account so it doesn't discard as spam all the bounced email it
    will receive.

### Adding an incoming email account for processing bounces and/or email-to-activities

Once you have created your email account to receive bounces or emails
for auto filing, you need to set up CiviMail so it knows how to read it:
**Administer > CiviMail > Mail accounts** as the default email
address.

![Screen shot of the email box selection screen](../img/administer-civimail-mailaccount.png)

![Screen Shot of adding an email box](../img/administer-civimail-mailaccount-edit.png)

-   Specify the mail **server, username, and password** you used when
    creating the account.
-   The **local part** is optional and only relevant if you were able to
    set up an account using sub-addressing. It should be the account you
    created with '+' or '-' appended , e.g., "return+" or "return-".
-   The **email domain** is the domain of your email address
    (example.org).
-   You can leave the **return path** empty.
-   If your mail server supports it, specify IMAP **protocol** and check
    **SLL**, otherwise use POP.
-   You can specify an IMAP folder in the **source** field using the
    syntax INBOX.CiviMail. **Note:** Some exchange servers may not be
    configured in a compatible way. In that case, you can configure a
    script like fetchmail and use Maildir.
-   In the **Used for?** field you can choose whether you want to use
    the email account for **Bounce Processing** or **Email-to-Activity
    Processing** (or Auto filing). You can have multiple accounts
    specified for auto filing but only one for bounce processing. This
    will be marked as default.

Once the **Bounce Processing** mailbox is configured, you will need to
configure CiviMail to empty it, read all these bounced messages and
identify the related bounced contacts. This is performed by the
Scheduled Jobs feature of CiviCRM .

We recommend testing the bounce process by running the process manually
before setting up CiviCRM to process the bounced email messages
automatically. This can be done in **Administer > System Settings >
Scheduled Jobs**. Locate **Fetch Bounces** and select **more > Execute
Now**. Check the Job Log for any error messages.

Once you have verified that CiviCRM can properly handle the bounce, you
can set it up to automatically process the replies and bounces on a
regular basis.

##Scheduling inbound and outbound mail processing

As discussed in the earlier chapter, mail processing and other jobs may
be automated through the Scheduled Jobs administrative page, cron or a
combination of both. The full range of options is discussed in the
[Manage Scheduled Jobs wiki
page](http://wiki.civicrm.org/confluence/display/CRMDOC43/Managing+Scheduled+Jobs),
but below are specific examples for enabling CiviCRM mail processing.

### Scheduling using the Scheduled Jobs administrative page

Mass mailings are generated via the CiviMail web interface and are
queued to be sent to their recipients. To schedule the regular
processing of this queue and any bounces that are returned go
to **Administer > System Settings > Scheduled Jobs** and find
the **Fetch Bounces** and **Send Scheduled Mailings** jobs. Edit each in
turn, setting their scheduled **Frequency** to "Hourly," "Daily" or
"Every time cron is run." The defaults should be fine for small
installations. Then select **more > Enable** for each.

In this example using the jobs' default frequency and [cron configured
to run at 15 minute
intervals](http://wiki.civicrm.org/confluence/display/CRMDOC/Managing+Scheduled+Jobs),
scheduled mailings would be sent every 15 minutes and bounces would be
fetched and processed hourly.

If you need to send some email from CiviCRM right away, without waiting
for the cron job, you can trigger the sending process by
visiting **Administer > System Settings > Scheduled
Jobs **select **more > Execute Now**. Use this capability sparingly. It
could utilize a lot of server resources and cause CiviCRM to slow down
noticeably. The administrative settings for sending email are usually
configured to minimize the load on the server, and the scheduling the
job is a more efficient way to send mass email.

### Scheduling only the mail jobs using the command-line interface

As an alternative on Linux and other Unix or Unix-like systems,
individual cron jobs may be used to schedule inbound and outbound mail
processing rather than the **Scheduled Jobs** page. This approach gives
experienced system administrators more granular control over these
processes by configuring specific cron jobs apart from other scheduled
jobs.

The cron job needs to run using an account recognized by your CMS.
Create an account dedicated to this task (e.g., *mailprocess, civimail,
etc*), give it a long, secure password (e.g. *seol-lzprm42amv-psyc*) and
grant it access to CiviCRM, CiviMail, and view all contacts. Do not
change the account password without changing the password in the
configuration files of this cron job.

To set up your cron job, first, find out whether php-cli is installed.
From the shell, type *php -v*. If you see **(cli)** in the result, as
in:

```
PHP 5.2.3-1ubuntu6.5 (cli) (built: Feb 11 2009 19:55:53) Copyright (c)
1997-2007
The PHP Group Zend Engine v2.2.0, Copyright (c) 1998-2007
Zend Technologies with eAccelerator v0.9.5.3, Copyright (c) 2004-2006
eAccelerator, by eAccelerator

```

This means you have php-cli installed and you should use it, because it
has several advantages:

-   You can run a PHP script at a lower priority than your web server,
    so that even if it takes a lot of CPU, it won't interfere with the
    regular users of your site.
-   You can set different memory limits for the php-cli process and the
    PHP process used by your web server.
-   You avoid the overhead of the web server and the HTTP layer.
-   You won't have any timeout problems.

The following is complete cron configuration to handle CiviCRM's mail
requirements:

```
# This must be set to the directory where civicrm is installed.
CIVI_ROOT=/var/www/civicrm

# Comment: I believe these two lines are unnecessary.
# USER=www-data
# MAILTO="you@example.org"

# Location of the PHP Command Line Interface binary.
# nice -19 forces to run at a lower priority than the web server

PHP=nice -n19 /usr/bin/php

# line to be modified according to the informations below
# like this: PARAMS= -j -s<default or domain> -u<user>
-p<password> -e Job -a process_mailing

PARAMS= -j -sdefault -umailprocess -pseol-lzprm42amv-psyc -e Job -a
process_mailing
PARAMSBOUNCE= -j -sdefault -umailprocess -pseol-lzprm42amv-psyc -e Job
-a fetch_bounces

# cronjob send
# m h dom mon dow command
*/5 * * * * cd $CIVI_ROOT; $PHP bin/cli.php $PARAMS
*/15 * * * * cd $CIVI_ROOT; $PHP bin/cli.php $PARAMSBOUNCE

```

The user that run the scripts (*www-data* in this example) needs to be
able to write into the temporary folder. Your configuration might
specify a different user.

You don't have to run both scripts at the same frequency. The preceding
crontab file verifies every 5 minutes whether mail messages need to be
sent, but only every 15 minutes whether bounced email needs to be
processed.

**PARAMS** contains:

1.  The site you used, which is **-sdefault** on Drupal. If you run
    multiple CiviCRM sites on a single server, you need to specify your
    site's domain, such as **-sexample.org**.
2.  The user login account (**-umailprocess**).
3.  The password you defined (**-pseol-lzprm42amv-psyc**).
