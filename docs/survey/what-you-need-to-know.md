Ce que vous devez savoir
========================

Les concepts et les questions suivants vous aideront à tirer le meilleur parti de l'outil de sondage de CiviCampaign.

Concepts clés
-------------

Ces concepts ne concernent pas la création et la réalisation d’enquêtes en général, mais l’utilisation spécifique de l’outil sondage dans CiviCampaign.

### Champs personnalisés et profils

Les sondages CiviCampaign utilisent des profils pour saisir les réponses des participants. Une fois que vous avez choisi vos questions et les types de réponses, vous devez créer des champs personnalisés pour les questions et les réponses avec des valeurs d'option si vous collectez des réponses à choix multiples. Vous pouvez ensuite soit créer un nouveau profil à partir de l'écran de profil principal, soit créer un nouveau profil lorsque vous créez un sondage. Un profil est utilisé pour afficher les questions du sondage.

Pour en savoir plus sur la création de jeux de champs personnalisés, voir le chapitre *Creating Custom Fields* dans le paragraphe *Organising Your Data*. Pour apprendre à créer un profil personnalisé, voir le chapitre Profiles dans le même paragraphe.

### Réservation et libération des répondants

Avant de pouvoir capturer les réponses à votre sondage, vous devez créer un groupe composé des contacts pour lesquels vous recherchez des réponses. Il peut s’agir d’un groupe existant au sein de vos contacts ou de la création d’un groupe spécifique au sondage. Un sondage décrit ce processus comme réservant les répondants. Lorsque le contact a terminé le sondage et que ses données ont été enregistrées, ils sont libérés de ce groupe.

Pour en savoir plus sur la création de groupes, consultez le chapitre *Groupes et étiquettes* dans le paragraphe *Organisation de vos données*.

Les enquêtes sont conçues pour capturer les réponses des contacts existants; Si vous souhaitez obtenir des réponses du grand public, utilisez l'outil Pétition. voir la section Pétitions pour plus d'informations.

### CiviCampaign et CiviEngage

Les sondages font partie des fonctionnalités du composant CiviCampaign. Vous devez donc l'activer pour pouvoir utiliser les sondages. Cependant, vous pouvez créer des sondages qui ne sont pas liés à une campagne spécifique. Par exemple, une organisation peut souhaiter organiser une enquête de satisfaction des membres pour évaluer la performance de son propre service, sans l'associer à une campagne.

Reportez-vous à la section *Campagnes* pour plus d'informations sur la configuration de CiviCampaign.

Les sites Drupal avec le module CiviEngage activé auront des profils d'options de jeu de résultats supplémentaires qui configurent les sondages pour vous permettre de suivre l'état des réponses à ce sondage. Pour en savoir plus sur les améliorations apportées par CiviEngage à la fonction Sondage, consultez la section intitulée Civic Engagement.

### Autorisations Drupal

Si vous utilisez Drupal, vous devez définir des autorisations pour autoriser des rôles spécifiques pour "Réserver" des contacts de campagne et "Libérer" des contacts de campagne lors de la réalisation des enquêtes. Pour en savoir plus sur la définition des autorisations Drupal, consultez la documentation Drupal à l'adresse http://drupal.org/getting-started/6/admin/user/permissions.

Questions clés
--------------

-   Le sondage fait-il partie d’une campagne? Lors de la création d'un sondage, il n'est pas nécessaire de le connecter à une campagne spécifique. un sondage général peut être utilisé pour n’importe quel programme de votre organisation. Mais si vous utilisez les sondages comme stratégie particulière dans une campagne, associer le sondage à la campagne vous permettra d'analyser le sondage ainsi que d'autres stratégies et activités liées à cette campagne.
-   Réfléchissez aux questions spécifiques et aux types de réponses que vous souhaitez recueillir. Voulez-vous un ensemble standard de réponses pour faciliter l'analyse des résultats à des questions spécifiques, par exemple Oui, non, indécis, sans réponse? Ou une question ouverte est-elle plus appropriée pour permettre à la personne de vous fournir un récit?
-   Combien de questions devez-vous poser? S'il en existe plusieurs, vous devrez créer des champs personnalisés. si le nombre de champs est supérieur à trois, envisagez d'utiliser Pétition au lieu de Sondage.
-   Qui mènera le sondage et comment les données seront-elles saisies dans CiviCRM?
-   Quel groupe de vos électeurs (répondants) souhaitez-vous interroger?
