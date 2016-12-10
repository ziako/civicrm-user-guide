Ce que vous avez besoin de savoir
=================================

Ce chapitre décrit quelques concepts et questions clés qui sont utiles pour planifier l'utilisation des capacités de  la messagerie de CiviCRM. Ce chapitre doit être lu avant de commencer à envoyer des courriels aux contacts. Vous trouverez des informations détaillées sur la façon d'exécuter les activités mentionnées dans la section **Tâches quotidiennes**.

Les concepts clés
-----------------

Comme on peut s'y attendre pour un CRM basé sur le Web, le courrier électronique joue un rôle central dans CiviCRM. D'une manière générale, il existe trois situations dans lesquelles le courrier électronique est envoyé par CiviCRM:

- aux particuliers et à de petits groupes de personnes via l'action Envoyer un email
- à un groupe important de personnes ou d'organisations comme un mailing de masse via CiviMail
- aux personnes qui déclenchent un courrier électronique dans le cadre de leur tâches de travail dans d'autres composants, par exemple un courrier électronique de confirmation d'enregistrement d'événement

L'avantage d'envoyer un courrier électronique via CiviCRM (plutôt que via votre client de messagerie électronique ou via un outil de messagerie en masse autre que CiviMail) est que chaque email envoyé via l'action Envoyer un e-mail ou utilisant CiviMail est traité comme une activité et est enregistré dans l'historique de l'activité de chaque contact. Cela vous permet de voir, par exemple, que John Doe a fait un don trois jours après qu'il ait reçu votre bulletin d'avril, ou que votre coordonnateur des bénévoles a envoyé un courriel à Jane Smith pour lui demander de fournir un tableau d'information pour un événement à venir.

### Envoi de courriel ou CiviMail ?

CiviCRM offre deux options pour l'envoi d'e-mails aux contacts :

- Envoyer un e-mail en tant qu'activité pour un contact: adapté pour l'envoi des courriels aux individus et aux groupes peu nombreux.
- Envoyer un mailing à un groupe à l'aide de CiviMail:  idéal pour les envois en masse ou les emails planifiés pour les groupes peu nombreux.

Pour envoyer des courriels de masse, le composant CiviMail doit être activé et configuré (voir le chapitre Configuration dans cette section pour plus de détails). L'action Envoyer un message électronique est disponible même lorsque le composant CiviMail est désactivé.

Il existe des différences essentielles entre l'action Envoyer un e-mail et le composant CiviMail :

- Les courriels envoyés par l'intermédiaire de l'action "Envoyer un e-mai"l sont limités à un maximum de 50 adresses e-mail, et il n'y a pas de rapport autre qu'une activité
- Les courriels de CiviMail comportent des traitements et des rapports élaborés.
- CiviMail permet aux destinataires de gérer leurs propres abonnements.
- CiviMail peut être configuré pour suivre automatiquement les réponses.

CiviMail nécessite du travail de configuration, et il y a plusieurs étapes nécessaires. Cependant, une fois que vous avez  configuré et activé CiviMail, vous aurez considérablement amélioré les capacités de messagerie de masse.

La définition de la méthode appropriée pour chaque courrier électronique pourrait ne pas être immédiatement apparente. Avec le temps, de meilleures pratiques et le bon outil pour chaque situation deviendra plus évident et pourra être partagé avec vos utilisateurs.

#### Quand utiliser l'action Envoyer un message électronique ?

Tant que vous contactez moins de 50 destinataires et que vous n'avez pas besoin de vérifier si les destinataires ont ouvert le courrier électronique ou cliqué sur les liens, l'action "Envoyer un e-mail" est plus rapide et plus facile que d'envoyer un courrier électronique massif dans CiviMail.

L'activité Envoyer un courrier électronique offre toutes les fonctionnalités d'envoi via un client de messagerie: vous pouvez joindre des fichiers, des contacts CC et BCC et utiliser des modèles de message. (texte brut ou HTML)

Notez que CiviCRM enregistre uniquement les messages que vous envoyez. Les réponses du destinataire arrivent à votre adresse e-mail et ne sont pas enregistrés dans la base de données. Pour cette raison, vous ne devez pas compter sur l'action Envoyer un e-mail pour effectuer des échanges de courriels étendus. Si vous voulez enregistrer le fait que vous avez eu un échange de courriel avec quelqu'un, vous pouvez créer une activité appelée "Echange d'emails" et copier/coller votre conversation dans le corps du message comme vous feriez l'enregistrement d'un appel téléphonique.

Vous pouvez également enregistrer les courriels envoyés par l'intermédiaire de votre client de messagerie électronique à l'aide de l'option d'envoi automatique de courrier électronique décrite ci-dessous.

#### Quand utiliser CiviMail ?

Si vous souhaitez envoyer du courrier à 50 contacts ou plus à la fois, vous devez utiliser CiviMail.

Vous devez également utiliser CiviMail chaque fois que vous souhaitez avoir des statistiques sur le résultat de votre envoi, y compris les statistiques de rebond et de clics. Pour plus d'informations à ce sujet, voir **Rapport et analyse**.

CiviMail permet également à vos contacts de s'inscrire à vos listes de diffusion sur votre site Web et effectue automatiquement le suivi de leurs demandes de désabonnement ou d'exclusion. Il vous permet également d'enregistrer tous les courriels que vos destinataires envoient comme réponses à l'envoi, et de leur adresser une réponse automatique.

### Choix des destinataires

Envoyer un e-mail vous permet de choisir les destinataires de deux façons:

-  A partir d'un enregistrement de contact et de résultats de recherche.
-  A partir des groupes marqués comme des listes de diffusion (ils doivent être créés avant de configurer votre envoi), et des résultats de recherche. Cependant il faut faire attention avec l'utilisation des résultats de recherche : Tous les courriers envoyés par CiviMail doivent avoir un lien de désabonnement. Si les destinataires sont inclus dans un groupe, les demandes de désinscription doivent simplement les supprimer de la liste de diffusion de ce groupe. Mais s'ils ne sont pas dans un groupe, ils doivent être ajoutés à un seul lorsqu'ils se désabonnent afin que la demande de désinscription puisse être enregistrée dans CiviCRM.

### Personnalisation avec les champs de fusion 

Les courriels envoyés avec Send Email et CiviMail peuvent inclure du texte personnalisé, comme le Nom ou le Prénom d'une personne. Cela se fait avec des Champs de fusion qui sont des espaces réservés que CiviCRM reconnaît et remplace par une valeur appropriée lors de l'envoi de chaque message. Vous pouvez inclure des Champs de fusion pour les champs standards et les champs de données personnalisés que vous avez créés. Notez qu'il existe quelques Champs de fusion disponibles dans CiviMail qui n'existent pas dans l'activité Envoyer un e-mail.

Un Champs de fusion particulièrement utile est la "somme de contrôle" (Checksum). La somme de contrôle vous permet de donner aux personnes des liens vers des formulaires de contribution, des profils, des pétitions et des formulaires d'inscription d'événements qui sont remplis d'informations contenues dans leur dossier de contact.

Cela évite à vos correspondants la peine de remplir des formulaires et augmente les chances qu'ils agissent positivement : par exemple, faire un don, s'inscrire à un événement, signer une pétition. Vous pouvez également demander à vos correspondants de vérifier et de mettre à jour leurs coordonnées : bon moyen simple de garder vos données à jour...

Des instructions détaillées sur l'utilisation des Champs de fusion, y compris les Champs de fusion personnalisés et l'utilisation des sommes de contrôle, sont disponibles dans la section **Tâches quotidiennes** sous la rubrique «Utilisation de Champs de fusion dans les courriels».

### Adresse d'envoi  

L'envoi de mail et les courriels de masse peuvent être envoyés à partir de votre adresse personnelle, d'une adresse électronique générale associée à votre organisation ou de l'adresse d'une autre personne. Par exemple, un assistant peut envoyer des messages électroniques officiels sous le nom de son manager.

### En-têtes et pieds de page

Dans les mailings de masse uniquement, vous pouvez inclure des en-têtes et des pieds de page personnalisés. Vous pouvez configurer ces en-têtes et pieds de page sous **Administer> CiviMail> En-têtes, pieds de page et messages automatisés**.

### Modèles de courriels 

Les modèles de courriels ou de parties d'e-mails aident à rationaliser vos communications en réutilisant des courriels entiers ou des parties d'e-mails tels que des en-têtes et des pieds de page. Les modèles de courrier électronique peuvent être créés à l'avance ou lorsque vous envoyez un courrier électronique, puis modifiés à tout moment.

### Rapports 

CiviMail peut faire le suivi des envois de masse. Civimail apporte des informations utiles pour vous aider à comprendre quels sont les centres d'intêret de vos destinataires et mesurer l'efficacité de vos communications. Vous pouvez suivre ainsi le nombre de destinataires qui ont ouvert le courrier électronique et quels liens dans le courrier électronique étaient les plus consultés.

#### Inscription et désabonnement à la liste d'envoi

CiviCRM vous permet de publier une page d'inscription ou un formulaire (appelé profil) où le public et les contacts peuvent s'inscrire à votre liste de diffusion sur votre site Web. Cela nécessite que vous autorisiez les destinataires à se désabonner de toute liste de diffusion * et * à ne plus recevoir de courrier électronique de votre part. CiviCRM suivra automatiquement ces demandes. Pour plus d'informations, voir le chapitre **Installation**.

### Archivage automatique d'emails externes dans CiviCRM

CiviCRM vous permet d'enregistrer automatiquement les e-mails envoyés via votre client de messagerie habituel dans les enregistrements de contact de votre base de données. Pour ce faire, vous devez configurer une adresse e-mail spéciale que vous incluez dans le champ BCC d'un courrier électronique que vous envoyez. Ceci sera lu par la base de données et converti en une activité. Cette activité est classée dans le dossier du contact correspondant à l'adresse e-mail. Si cette adresse e-mail n'existe pas dans votre base de données, un nouvel enregistrement de contact sera créé. Reportez-vous au chapitre **Configuration du système de messagerie** de la section **Configuration Initiale** pour plus de détails.

Questions clés 
---------------
CONSEIL : Lorsque vous prévoyez l'utilisation des fonctions de messagerie électronique de CiviCRM, il peut être utile de répondre à ces questions pour orienter votre configuration et votre utilisation :

- Avez-vous des types de courriels que vous envoyez régulièrement et souhaitez-vous créer des modèles ?
- Avez-vous du contenu que vous souhaitez inclure dans l'en-tête et/ou le pied de page dans chaque envoi ?
- Voulez-vous une page Web où les personnes puissent s'abonner à vos e-mails?
- Quels types de courriels importants voulez-vous enregistrer dans les dossiers de vos contacts ?

Lorsque vous prévoyez d'envoyer un courriel spécifique par le biais de CiviCRM, il est utile de considérer les éléments suivants:

- A combien de personnes envoyez-vous votre email ?
- Voulez-vous savoir qui ouvre votre courriel et clique sur les liens qu'il contient ?
- Avez-vous créé une liste (un groupe ou un groupe intelligent) à partir de laquelle envoyer votre courriel ?
- Voulez-vous que les destinataires puissent afficher votre courriel dans une fenêtre de navigateur s'ils ont du mal à le consulter à partir de leur navigateur de messagerie électronique ?
- Qui doit être l'expéditeur du courriel?  une adresse générique de l'organisation, ou personnalisée avec le nom d'une personne.

### Relation avec les composants 

De nombreux composants de CiviCRM interagissent avec les fonctionnalités de messagerie et avec CiviMail, par exemple pour envoyer des courriels de confirmation, de remerciement ou de réception. Les sections de ce manuel, relatives à chaque composante, contiendront des informations sur la personnalisation de ces courriels et doivent être lues en parallèle avec cette section. cela vous permettra de comprendre comment fonctionne le courrier électronique dans le contexte plus large de CiviCRM.

#### Questions de confidentialité  

Nous vous encourageons à bien examiner les questions de confidentialité. Certains pays ont des lois différentes concernant la confidentialité des courriels, y compris les options d'exclusion/désabonnement. Il peut également y avoir des problèmes liés aux outils de suivi de CiviMail. Par exemple, vous pouvez éviter de suivre qui a cliqué sur le lien  *«comment traiter les problèmes de drogue»*  sur un envoi spécifique.

En France, l'e-mailing commercial se distingue du spam par une démarche d'opt-in, basée sur le recueil libre, loyal et informé du consentement des destinataires. Les cases précochées de collecte sont bannies, tandis que les modalités d'opposition doivent faire l'objet d'un détail précis. Les seules exceptions à ce principe concernent le démarchage dans le cadre d'une relation-client, sous réserve que les biens et services proposés soient identiques aux achats antérieurs, et les sollicitations liées aux fonctions professionnelles exercées par les destinataires.

Mention d'information à inscrire sur le bulletin d'adhésion (Source CNIL) :  
*Les informations recueillies sont nécessaires pour votre adhésion. Elles font l'objet d'un traitement informatique et sont destinées au secrétariat de l'association. En application des articles 39 et suivants de la loi du 6 janvier 1978 modifiée, vous bénéficiez d'un droit d'accès et de rectification aux informations qui vous concernent.
Si vous souhaitez exercer ce droit et obtenir communication des informations vous concernant, veuillez vous adresser à ......... [indiquez-ici le service en charge de traiter les demandes] *

#### Spam et envoi de courrier électronique

Lors de l'envoi de courriels de masse, il existe toujours un risque que vos e-mails soient marqués comme spam. Cela affecte à la fois la livraison de votre courrier électronique actuel mais également la livraison future de tous les courriels envoyés à partir de votre serveur. La gestion de ces questions est complexe et sort du cadre de ce livre. Si votre organisation ne dispose pas d'un administrateur système, d'un consultant ou d'un service d'hébergement de messagerie connaissant bien ces questions, vous pouvez demander l'avis d'un expert.


