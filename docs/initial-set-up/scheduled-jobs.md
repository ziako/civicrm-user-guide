Travaux programmés
==================

CiviCRM s'appuie sur un certain nombre d'actions planifiées qui sont exécutés régulièrement pour maintenir les données à jour et pour effectuer certaines tâches. Ces travaux doivent être déclenchés par un [cron](http://fr.wikipedia.org/wiki/Cron) qui s'exécute régulièrement sur votre serveur d'hébergement Web.

Voici des exemples d'actions planifiés:

-   Le traitement des adhérents, pour mettre à jour les statuts d'adhésion.
-   Inviter les personnes en liste d'attente à s'inscrire aux événements lorsque des places sont disponibles.
-   Le script  d'envoi et de traitement de CiviMail qui gère l'envoi et le traitement des emails
-   Les scripts CiviReport qui gèrent l'envoi périodique de documents par courrier électronique  

Certains travaux doivent être exécutés très fréquemment, par exemple la tâche d'envoi de courrier électronique a tendance à être exécuté une fois toutes les 5 ou 10 minutes. D'autres doivent être exécutés moins fréquement, par exemple le script de mise à jour d'adhésions peut n'être exécuté qu'une fois par jour.

Il existe deux façons de configurer les tâches planifiées:

-   Via l'interface utilisateur, que vous pouvez configurer à l'option **Administer> Paramètres système> Travaux programmés**.
-   En configurant plusieurs jobs cron pour des tâches spécifiques.

Ces méthodes sont développées ci-dessous.

## Qu'est-ce que un cron ?

Cron (pensez "**cron** ology" ou "**cron** ograph") est un planificateur automatique basé sur le temps qui déclenche certains programmes à exécuter sur votre serveur web. D'une manière générale, cron (également connu sous le nom «cronjob») peut être configuré dans votre panneau de contrôle d'hébergement Web ou par l'administrateur du serveur en charge de votre hébergement web. Nous vous recommandons de choisir l'hébergement web qui offre cron comme un service gratuit.

Avant que les tâches planifiées configurées via l'interface utilisateur ne fonctionnent réellement, vous devrez configurer un travail CRON sur le serveur Web. Il existe des exemples de configuration CRON dans la page wiki : [Exécution des scripts de ligne de commande via URL] (http://wiki.civicrm.org/confluence/display/CRMDOC/Running+Command-line+Scripts+via+URL) .

## Configuration des travaux programmés via l'interface utilisateur

L'interface utilisateur des travaux programmés est conçue pour faciliter la configuration des tâches planifiées et éviter de devoir créer ou modifier une tâche cron chaque fois que vous souhaitez effectuer une modification pour un travail planifié. Dans la plupart des petites installations les actions doivent être bien configurées pour exécuter les tâches planifiées via l'interface utilisateur. Les sites plus importants devraient envisager de créer pour chaque tâche un cron de la manière habituelle. Cela nécessite certaines compétences en administration système.

La page Tâches périodiques (**Administer**> **Paramètres système**> **Travaux programmés**) est conçue pour faciliter la configuration des tâches planifiées et le contrôle de leur dernière exécution. Elle affiche une liste de tous les travaux planifiés disponibles par défaut. Vous pouvez modifier chacun d'eux et régler sa fréquence (horaire, quotidienne, hebdomadaire, mensuelle, trimestrielle, annuelle ou chaque fois que le cron est exécuté, ce qui est généralement toutes les 5-10 minutes), les paramètres pertinents et la date/heure la plus ancienne pour la Première/Prochaine exécution de la tâche

Vous pouvez trouver une liste à jour de tous les travaux planifiés et des paramètres sur la page wiki : [Gestion des tâches planifiées] (http://wiki.civicrm.org/confluence/display/CRMDOC/Managing+Scheduled+Jobs).

Certaines tâches effectuent des actions spéciales de mise à jour des données et ne sont pas conçues pour être exécutées automatiquement ou à plusieurs reprises. Ce sont: "Mettre à jour les salutations et les destinataires" et "Fixer les dates de rappel du renouvelement". Les détails sur la façon de les exécuter sont expliqués sur la page wiki : [Gestion des tâches planifiés] (http://wiki.civicrm.org/confluence/display/CRMDOC/Managing+Scheduled+Jobs).

## Exécution manuelle des tâches planifiées

La page des tâches planifiées peut également être utilisée pour exécuter des tâches ponctuelles. Cela est utile pour certains travaux planifiés qui sont conçus pour être exécutés sur une base moins régulière comme l'actualisation du géocodage, les salutations et les destinataires. Exécutez l'action manuellement en cliquant sur le lien **Plus> Exécuter maintenant** pour le job choisi dans **Administer> Paramètres système> travaux programmés**.

## Planification des tâches spécifiques via des tâches cron individuelles

Les administrateurs système parlent plus souvent de tâches planifiés que de tâches cron. Si vous exécutez un grand nombre de tâche planifiées sur de grands ensembles de données il est souhaitable d'avoir un administrateur système expérimenté pour les configurer à l'aide du cron. Cela permettra un contrôle plus précis au moment de l'exécution de ces tâches, ce qui peut être utile si ces processus ont une charge importante sur votre serveur.

Notez que les tâches planifiées qui ont été exécutées via une action cron individuelle n'apparaissent pas automatiquement ici. Elles doivent être configurées pour le faire. Des détails sur le déclenchement de tâches spécifiques via la ligne de commande, l'URL, Drush et d'autres méthodes peuvent être trouvés sur la page : [Gestion des emplois planifiés] (http://wiki.civicrm.org/confluence/display/CRMDOC/Managing+Scheduled+Jobs).

