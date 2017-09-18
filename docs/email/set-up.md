Configuration
========

Ce chapitre décrit comment configurer des informations telles que  l'adresse électronique d'envoi des mails, des groupes de liste de diffusion et des modèles de courrier électronique. Cela suppose que la fonctionnalité de base nécessaire à votre serveur pour envoyer et traiter des courriels a déjà été configurée. Voir *Configuration du système de messagerie* dans *Configuration avancée* pour plus de détails.

Configuration des coordonnées de votre organisation
---------------------------------------------------

Afin d'envoyer des courriels de masse, vous devez remplir quelques informations de base : le nom de votre organisation, une brève description, votre adresse de courrier électronique et votre adresse postale. CiviMail requiert que vous incluiez l'adresse postale de l'expéditeur ainsi que les liens de désabonnement/d'exclusion dans tout envoi de masse afin de vous conformer aux lois sur la protection de la vie privée. Ces informations sont mises à disposition via des champs de fusion et doivent être obligatoirement incluses dans tout courriel envoyé avec CiviMail.

Pour configurer ces informations, allez à: **Administrer> Communications> Adresse de l'organisation et informations de contact**.

Groupes de diffusion
--------------

CiviMail utilise les Groupes pour organiser les destinataires des envois en masse. Pour créer un groupe, allez dans **Contacts> Nouveau groupe**. Lorsque vous créez et configurez un groupe à cet effet, assurez-vous de vérifier la liste de diffusion sous "Type de groupe" pour qu'il soit disponible en tant que liste de diffusion dans CiviMail. Vous pouvez ensuite effectuer une recherche et ajouter des contacts au groupe.

Vous pouvez également créer des groupes dynamiques basés sur les résultats de recherche, ce qui mettra à jour le groupe avec tous les contacts qui correspondent aux critères de recherche. Par exemple, en fonction des résultats de la Recherche avancée, vous pouvez créer un groupe dynamique de contacts qui ont des abonnements actifs ou un groupe dynamique de contacts dans une ville donnée. À mesure que les personnes deviennent membres ou déménagent dans la ville que vous avez recherchée, ils seront automatiquement ajoutés au groupe dynamique. Cela permet d'envoyer des courriels sans avoir à mettre à jour les contacts d'un groupe.

Pour créer un groupe dynamique consultez la section "Groupe dynamique" dans le chapitre "Organisez vos données"

Permettre aux personnes de s'inscrire à vos listes de diffusion en ligne
-------------------------------------------------------

CiviCRM permet aux personnes de s'inscrire eux-mêmes à vos listes de diffusion en ligne.

Pour cela, vous devez désigner le groupe comme une liste de diffusion. Si vous n'avez pas fait cela lorsque vous avez créé le groupe, allez dans **Contacts**> **Gérer les groupes**. Cliquez sur **Paramètres** dans le groupe qui contient vos destinataires et vérifiez la liste de diffusion en regard de Type de groupe. Vous devez également modifier la visibilité des pages publiques.

Pour que cela fonctionne pour les utilisateurs public ou anonymes qui n'ont pas de connexion à votre CiviCRM, vous devez vous assurer que les utilisateurs anonymes de Drupal, Joomla, Wordpress ont la permission suivante cochée: "Accès aux pages d'abonnement/désabonnement de CiviMail".

### Utilisation du lien d'abonnement

Pour permettre aux utilisateurs de s'abonner à une liste de courriels en ligne vous devez les diriger vers www. *votre_site.fr* /civicrm/mailing/subscribe. Quiconque accède à ce lien peut s'abonner aux groupes de liste de diffusion disponibles.

### Utilisation d'un profil

Vous pouvez aussi recueillir d'autres d'informations lorsque les gens s'inscrivent à vos listes de diffusion par l'utilisation d'un profil qui est ensuite affiché sur une page publique. Pour plus d'informations sur les profils, leur fonctionnement et leur configuration, reportez-vous au chapitre **Profiles**

CONSEIL : vous pouvez créer un nouveau profil appelé Bulletin d'inscription. Ajouter à ce profil les champs d'informations que vous souhaitez obtenir pour les personnes qui veulent s'inscrire à votre liste de diffusion. Chacun des champs du profil doit avoir sa visibilité définie sur Pages publiques.

Pour chaque champ que vous incluez, vous pouvez choisir s'il est obligatoire ou facultatif pour les personnes qui remplissent le formulaire public. La seule exception est que le profil doit inclure **obligatoirement** un champ de courrier électronique. C'est pour qu'un email de confirmation puisse être envoyé à la personne qui souhaite s'inscrire à la liste de diffusion. dans l'attente de leur confirmation les inscrits  auront un statut de «En attente» dans le groupe de liste de diffusion.

Il existe deux façons d'afficher le profil en mode public :

1. Partager un lien directement : Retournez à la liste des profils (**Administer> Données et écrans personnalisés> Profils**) et cliquez sur **Plus** à l'extrême droite de votre profil. Cliquez sur **Utiliser le mode de création de profil**. Votre navigateur ouvrira la page publique. Vous pouvez publier ce lien pour permettre aux utilisateurs de s'inscrire à vos listes de diffusion.

2. Intégrez cet ensemble de champs comme un formulaire dans votre site Web : Retournez à la liste des profils (**Administer> Données et écrans personnalisés> Profils**) et cliquez sur **Plus** à l'extrême droite de votre profil. Sélectionnez **Extrait de formulaire HTML**. Cela ouvrira une fenêtre dans votre navigateur avec le code HTML de ce profil. Copiez et collez le contenu de la boîte dans une page de votre site Web. Les visiteurs du site pourront s'inscrire à vos listes de diffusion sur cette page.

Pour Wordpress, vous pouvez afficher le formulaire publiquement en utilisant un code court. Sur n'importe quelle page Wordpress, cliquez sur le bouton **CiviCRM** au-dessus de l'éditeur. Pour **Type de page** sélectionnez **Profil**. Dans la liste déroulante suivante, sélectionnez le nom du profil que vous avez créé. Sélectionnez **Modifier** dans l'option du bouton radio juste en dessous des menus déroulants, afin que vous puissiez accéder aux données de votre base de données (c'est-à-dire ajouter leur adresse électronique et leur nom à votre base de données). Cliquez **Insérer formulaire** et le code court sera ajouté à l'éditeur.

### Utilisation d'un formulaire Web (Drupal)

Beaucoup d'administrateurs de sites Drupal préfèrent utiliser un formulaire Web au lieu d'un profil pour créer leur abonnement au bulletin, car il offre des fonctionnalités supplémentaires telles que le contrôle du spam avancé et un thème flexible. Pour plus d'informations, voir:
[http://wiki.civicrm.org/confluence/display/CRMDOC/Webform+CiviCRM+Integration](http://wiki.civicrm.org/confluence/display/CRMDOC/Webform+CiviCRM+Integration)

### Ajout de personnes à votre groupe de liste de diffusion à l'aide d'un profil

Pour qu'un utilisateur soit automatiquement ajouté à vos groupes de liste de diffusion lorsqu'ils remplissent votre formulaire d'inscription à la newsletter (profil CiviCRM), vous avez deux options:

Option 1 : Dans le profil, vous pouvez ajouter un champ pour que les utilisateurs puissent vous inscrire dans les groupes de listes de diffusion. Accédez aux champs du profil et cliquez sur **Ajouter champ**. Pour le "Nom du champ", sélectionnez "Contacts". Lorsque les sélections possibles sont affichées dans le deuxième champ, sélectionnez "Groupe(s)". Dans l'étiquette de champ, vous pouvez laisser "Groupe(s)" ou vous pouvez le modifier pour un terme plus intuitif aux visiteurs de votre site Web tel que «inscrivez-vous à la newsletter». La visibilité de ce champ doit être définie sur Pages publiques. Lorsque le profil s'affiche publiquement ce champ affiche des cases à cocher pour tous les groupes de liste de diffusion dont la visibilité est définie sur Pages publiques. De cette façon, les utilisateurs peuvent s'ajouter à tous vos groupes de liste de diffusion qu'ils souhaitent en cochant les cases appropriées.

Option 2 : Accédez aux paramètres du profil. Dans la section Paramètres avancés, sélectionnez le groupe de liste de diffusion souhaité pour **Ajouter de nouveaux contacts à un groupe**. Maintenant, lorsque les utilisateurs remplissent votre formulaire, ils seront automatiquement ajoutés à ce groupe.

### Suivi de confirmation d'inscription à une liste de diffusion

Pour que cela fonctionne, vérifiez d'abord que vous avez coché les options **Enable Double Opt-in** dans **Administer> Console d'administration> Paramètres du composant CiviMail**.

Une fois abonné aux groupes de liste de diffusion - via le lien d'abonnement ou un profil - CiviCRM enverra automatiquement un courriel demandant de confirmer l'abonnement. Jusqu'à ce qu'ils cliquent sur le lien de confirmation dans le courrier électronique, leurs coordonnées apparaîtront dans CiviCRM avec leur abonnement de groupe défini "En attente". Lorsqu'ils confirment, CiviCRM va automatiquement modifier leur statut d'abonnement de groupe à "Ajouté" et il sera envoyé un message de bienvenue. (Remarque: lorsque les utilisateurs s'abonnent à plusieurs groupes à la fois, un e-mail de confirmation est envoyé pour chaque groupe séparément.)

Tâches planifiées et jobs cron
----------------------------

Après que les personnes se soient inscrites à votre mailing list, vous êtes en mesure de leur envoyer des envois de masse. Vous pourrez également gérer automatiquement tous les messages électroniques renvoyés. Ces rubriques sont traitées en détail dans les parties **tâches journalières** et **Maintien d'une liste de courriel** de ce livre. Ici, nous allons examiner quelques options backend et serveur qui permettent l'envoi de mailings de masse et comment le rebond se produit.

Allez dans **Administration> Paramètres système> Tâches planifiés** et vous verrez tous les travaux planifiés que CiviCRM utilise pour effectuer certaines tâches régulièrement. Une telle tâche est l'envoi réel des envois de masse, qui est géré par   **Envoyez des mailings programmés**. Une autre tâche est le traitement des e-mails renvoyés, pour lesquels la  tâche planifiée  **Fetch Bounces** est responsable. Vous devez activer ces deux tâches planifiées (et toutes celles que vous souhaitez exécuter régulièrement). Sans ces deux, CiviMail n'envoie pas d'envois et ne traitera pas les rebonds.

Maintenant, les "Tâches planifiées" de CiviCRM ne peuvent pas s'auto-déclencher d'elles-mêmes. Une action sur votre serveur doit les déclencher. L'option la plus courante consiste à configurer une tâche cron sur votre serveur. Cette tâche cron peut déclencher une ou plusieurs (ou toutes) les tâches planifiées. Pour des explications plus détaillées et des exemples de la façon de le faire, consultez la page wiki [Gestion des tâches planifiées](http://wiki.civicrm.org/confluence/display/CRMDOC/Managing+Scheduled+Jobs).

Gestion automatisée des messages et des listes de diffusion
------------------------------------------------

CiviCRM envoie des emails automatiquement lorsque vos participants font certaines actions :

- Quand quelqu'un s'inscrit pour une liste de diffusion, il recoit un email de confirmation avec un lien sur lequel il doit cliquer.
- Lorsqu'il confirme, il reçoit un courriel de bienvenue.
- Lorsqu'il se désabonne de tous les courriels de votre site ou qu'ils se réinscrit à une liste dont il a déjà été désabonné, il reçoit un courriel de confirmation qui ne nécessite aucune action.
- Lorsqu'il répond à un message que vous avez envoyé via CiviMail, vous pouvez configurer une réponse automatique à sa réponse.

Dans CiviCRM, nous appelons cela des messages automatisés. Vous pouvez les modifier et en ajouter de nouveaux dans **publipostage> en-têtes, pieds de page et messages automatisés**.

Pour plus d'informations sur la gestion des listes d'e-mails, reportez-vous au chapitre **Gestion des listes de courrier électronique**, qui explore comment CiviCRM gère les désabonnements, les rebonds, etc...

Création et maintenance de modèles de messages
----------------------------------------------

Les modèles de messages aident à rationaliser vos communications en vous permettant de réutiliser des courriels entiers ou des parties de courriels dans les envois de masse et lors de l'utilisation de l'activité Envoyer par courrier électronique.

La manière la plus simple de créer un nouveau modèle de message consiste à cocher la case Enregistrer comme nouveau modèle sur l'écran de création de message. Cette fonction est disponible à la fois lors de l'utilisation de l'activité Envoyer un e-mail et lors d'un envoi de masse.

Vous pouvez également créer des modèles de messages à partir de zéro ou modifier des modèles existants en allant dans **Mailings> Modèles de message** ou **Administrer> Communications> Modèles de message**.

1. Cliquez sur ** Ajouter modèle de message **.
2. Entrez un titre et un sujet de message. Vous pouvez choisir d'utiliser des champs de fusion pour personnaliser votre ligne d'objet.
3. Faites défiler jusqu'à la section Format HTML et créez votre modèle. CONSEIL : Il existe des ressources en ligne, non spécifiques à CiviCRM, qui offrent des instructions sur la création d'un modèle de courrier électronique HTML. Vous pouvez trouver et copier un modèle de courrier électronique à partir d'un site Web qui propose des échantillons.
4. Dans la barre d'outils de l'éditeur WYSIWYG, il ya une icône appelée "Source" (l'apparence et l'étiquetage de cette icône varient selon que vous utilisez Drupal, Joomla ou WordPress). .Lorsque vous cliquez dessus, le modèle modifie la vue pour afficher le code HTML utilisé. Vous devez passer à cette vue si vous souhaitez coller en HTML à partir d'un modèle que vous avez trouvé à l'extérieur, ou si vous souhaitez écrire directement le code HTML dans votre modèle ou modifier le code HTML que vous avez créé avec l'éditeur WYSIWYG.

Les modèles de messages sont disponibles même lorsque CiviMail est désactivé.

### Conseils pour la création de modèles

Le code HTML autorisé dans les courriels est plus restreint que le HTML utilisé pour les pages Web. Par exemple, il doit utiliser des tables pour la mise en page, CSS en ligne, et ne doit pas inclure des images d'arrière-plan. Voici quelques conseils pour créer un modèle qui sera correct dans tous les clients de messagerie:

- **Table border** : L'élément HTML (table) inclut un attribut de bordure facultatif. Comme la valeur par défaut est 0, elle n'apparaît que si vous choisissez de l'utiliser. Si vous l'ajoutez (ou si vous l'éditez s'il est disponible) et que vous le définissez sur 1 (par exemple, `<table border =" 1 ">`), vous pouvez voir les contours de votre table et les identifier. Veuillez noter que les modèles de courrier électronique HTML comportent généralement plusieurs tables et tables imbriquées (tables à l'intérieur des tables). Effectuez les modifications une à une et passez à la vue HTML pour afficher les résultats. Une table a généralement plus d'un paramètre, alors assurez-vous de placer des espaces entre les paramètres.
- **Table cellpadding et cellspacing** : ces paramètres de table sont très utiles lorsque vous essayez d'améliorer la lisibilité de votre email. Jouez avec ces paramètres dans différentes tables et voyez ce qui fonctionne pour vous.
- **Width** : N'envoyez pas un email de plus de 600 pixels pour assurer une compatibilité maximale entre les différents clients de messagerie. Assurez-vous que votre table extérieure ne dépasse pas 600 pixels. Faites de même pour toutes les autres tables à l'intérieur de votre table principale. Assurez-vous également que la largeur totale de chaque image ne dépasse pas 600 pixels. Les images ont un paramètre de largeur, mais elles peuvent également avoir un paramètre de rembourrage horizontal qui, s'il est défini, peut augmenter la largeur de l'image.
- **Images**: Elles doivent être en ligne et accessibles pour que vous puissiez les utiliser. Commencez par modifier votre image afin que sa largeur et sa hauteur conviennent à votre modèle de courrier électronique. Ensuite, enregistrez-le pour que sa taille de fichier soit aussi petite que possible. Si vous n'avez pas de logiciel de retouche d'image ou si vous ne savez pas comment l'utiliser, il existe des ressources en ligne gratuites qui peuvent vous aider à redimensionner votre image.
- **Editeur HTML**: CiviCRM est livré avec deux éditeurs WYSIWYG (CKEditor et TinyMCE) et Textarea, un éditeur de texte brut. Si vous avez un autre éditeur configuré dans le cadre de votre installation Drupal, Joomla ou WordPress, vous pouvez choisir de l'utiliser à la place. Aller à: **Administer**> **Personnaliser les données et les écrans**> **Préférences d'affichage**> et sélectionner un autre éditeur WYSIWYG.

Pour voir des exemples de modèles de messages, consultez :  
[http://wiki.civicrm.org/confluence/display/CRMDOC/Sample+CiviMail+Messages](http://wiki.civicrm.org/confluence/display/CRMDOC/Sample+CiviMail+Messages)
[](http://wiki.civicrm.org/confluence/display/CRMDOC41/Sample+CiviMail+Messages).

### Texte brut et format HTML

Tous les messages peuvent être envoyés en texte brut ou en HTML. Aujourd'hui, la grande majorité des gens utilisent des clients de courrier électronique qui peuvent lire les messages reçus en HTML. Cependant, une bonne pratique consiste à offrir la possibilité d'envoyer une version de courrier électronique en texte brut pour s'assurer que tous les destinataires peuvent afficher le message. Les lecteurs de courrier électronique en texte brut peuvent afficher un message HTML vierge. Le courrier électronique HTML peut également présenter des problèmes d'accessibilité aux personnes utilisant des lecteurs d'écran.

Toutefois, si les utilisateurs modifient un courrier électronique à partir d'un modèle contenant du texte brut et du HTML, ils peuvent oublier de modifier la version texte de ce message. Cela signifie que les personnes utilisant des clients de messagerie texte uniquement recevront un message incorrect ou incomplet.

CONSEIL : Une solution à ce problème est soit d'utiliser des courriels en texte brut uniquement ou de définir des modèles sans l'option de texte brut et de demander aux utilisateurs de créer une version de texte brut avant d'envoyer leurs mailings.

Créer une version texte d'un message HTML:

1. Copiez et collez le texte du champ Format HTML dans le champ Format de texte brut. Lorsque vous effectuez cette opération, assurez-vous que vous n'êtes pas dans la vue Source... Vous ne voulez pas tout le code, juste le texte ! Lorsque vous copiez à partir de la vue WYSIWYG, le champ de texte brut supprimera automatiquement la mise en forme et tous les autres éléments qui ne fonctionnent pas en texte brut.
2. Copiez éventuellement les URL de tous les liens vers les endroits appropriés dans le champ Format de texte brut.
3. Si la version HTML contenait des tables, modifiez la mise en page de votre texte manuellement pour vous assurer que la version texte est lisible.

Création d'en-têtes et de pieds de page
----------------------------

Les en-têtes et les pieds de page ne peuvent être utilisés que dans les envois de masse à l'aide de CiviMail. Ils ne sont disponibles que si CiviMail est activé.

L'en-tête est la zone en haut de l'e-mail. Elle doit inclure les éléments que vous souhaitez afficher avant le corps du contenu principal, comme le logo de votre organisation et le titre du bulletin.

Le pied de page est toujours la fin du courrier électronique. Le pied de page est un endroit idéal pour les champs obligatoires de désinscription  (voir **Ce que vous devez savoir** pour plus d'informations).

Vous pouvez gérer le contenu des en-têtes et des pieds de page dans **Envois> En-têtes, Pieds de page et Messages automatisés**. Vous pouvez créer différents en-têtes et pieds de page à des fins différentes. Par exemple, vous pouvez créer un ensemble d'en-têtes avec différentes images et titres pouvant être utilisés pour différentes campagnes ou programmes. Il est recommandé de les styler de manière similaire afin de présenter une identité visuelle cohérente à travers tous vos messages.

Une fois les en-têtes et les pieds de page configurés, le personnel qui prépare un nouvel envoi pourra les sélectionner dans les en-têtes et les pieds de page disponibles. Cela aide le personnel à créer des envois normalisés avec des éléments qui aident vos lecteurs à identifier le contenu de l'envoi ou à trouver des informations.

Comme les modèles de message, les en-têtes et les pieds de page ont à la fois un texte et une version HTML. Contrairement aux modèles de message, cependant, les pages de création d'en-tête et de pied de page n'offrent pas d'éditeur WYGIWYG. Vous devrez écrire l'en-tête et le pied de page HTML directement ou utiliser un autre éditeur HTML pour produire le code HTML.

Tester vos modèles de message
-----------------

Une fois que vos modèles sont prêts, nous vous recommandons fortement de les tester dans différents clients de messagerie tels que Mozilla Thunderbird, MS Outlook, Mac Mail et courrier électronique sur le Web tels que Gmail, Yahoo et Hotmail. CONSEIL : Une façon simple de le faire est de créer un groupe qui comprend un contact de test pour chacune de ces destinations et de l'utiliser chaque fois que vous créez un nouvel envoi.

CONSEIL : Comme les clients de messagerie peuvent afficher le code HTML très différemment, nous vous recommandons de conserver un code HTML aussi simple que possible et d'utiliser uniquement des CSS ou des tables en ligne pour le formatage. Inclure autant que possible de la mise en page dans les modèles de sorte que chaque nouvel envoi ne nécessite pas trop de révision, puisque le modèle aura déjà été testé.

Conversion automatique d'e-mails dans CiviCRM
------------------------------------------

Il est possible d'envoyer des courriels vers et depuis votre client de messagerie ordinaire automatiquement dans CiviCRM. Cela se fait en incluant une adresse e-mail désignée dans le champ À, Cc ou Cci (Bcc est recommandé, car il est invisible pour le destinataire). Les e-mails qui incluent ce courrier électronique désigné sont classés comme une activité pour le(s) contact(s) qui correspondent aux adresses de messagerie dans les champs De, To et Cc. Si l'une de ces adresses de messagerie ne se trouve pas déjà dans le système, un nouvel enregistrement de contact sera créé. (Techniquement, cela peut également fonctionner pour les courriels entrants, mais cela dépend de la personne qui vous envoie le courrier, y compris l'adresse de dépôt automatique dans le champ À, Cc ou Cci.)

Pour cela, votre administrateur doit avoir configuré IMAP ou d'autres comptes de messagerie et les configurer dans CiviMail (voir **Configuration du système de messagerie**, en particulier **Ajout d'un compte de messagerie entrant pour le traitement des rebonds ou le dépôt automatique à CiviMail**, **Initial Set-Up **  pour plus de détails).

