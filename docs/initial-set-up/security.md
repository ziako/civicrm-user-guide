Sécurité
========

CiviCRM est une solution basée sur le Web, et en tant que tel, nécessite un serveur web pour fonctionner. Lorsque les serveurs Web stockent des données sensibles et sont accessibles au public sur Internet - comme CiviCRM est conçu pour le permettre - la sécurité est un aspect important à considérer. L'approche recommandée pour sécuriser les données CRM consiste à utiliser un VPN (Virtual Private Network) pour encapsuler les données transférées sur des réseaux publics dans des paquets cryptés. L'une des méthodes les plus simples consiste à forcer l'utilisation de tunnels cryptés lors de l'accès au serveur via divers protocoles de données (par exemple SSH, SSL et FTPS, explorés ci-dessous). Cet environnement protège efficacement les données dans un shell de protection, qui ne peut être ouvert que par le navigateur Web de l'utilisateur et par le serveur. 

Transfert de données cryptées
-----------------------------

Il existe un certain nombre de protocoles ou de méthodes différentes pour transférer des données d'un point à un autre.


-   **FTPS**: Pour télécharger des fichiers sur le serveur en dehors de l'interface CiviCRM, (admin uniquement), vous pouvez utiliser un client FTPS (Secure File Transfer Protocol). Vous devez, configurez des comptes FTPS avec des noms d'utilisateur et des mots de passe.

-   **SSH**: Le SSH (Secure Shell) est une méthode qui peut être utilisée pour authentifier des utilisateurs - par mot de passe ou avec une clé - et les encapsuler dans le serveur pour exécuter des instructions en ligne de commande.
   
-   **SSL**: Secure Sockets Layer affecte vos utilisateurs quotidiens accédant à CiviCRM via un navigateur Web. SSL crypte les données soumises sur une page par un utilisateur et les envoie au serveur (la seule entité détenant la «clé» pour déchiffrer les données et vice versa). SSL peut être nécessaire pour la conformité PCI, ou tout simplement pour empêcher l'interception d'informations sensibles pendant le transit. Par défaut, CiviCRM est *non* sécurisé pour l'accès au navigateur, veuillez lire la section «Configuration de SSL» pour les instructions de configuration.

Remarque: assurez-vous que les mots de passe utilisés par une personne à travers plusieurs protocoles sont différents, car chacun comporte des niveaux de contrôle variables.


Dois-je utiliser un SSL (Secure Sockets Layer)? 
-----------------------------------------------

### Conformité PCI

American Express, Discover Financial Services, JCB International, MasterCard International et Visa Inc. travaillent ensemble pour élaborer des normes pour le traitement des paiements en ligne (voir [https://www.pcisecuritystandards.org/organization_info/index.php](https://www.pcisecuritystandards.org/organization_info/index.php)).

L'hébergement des sites Web qui acceptent les paiements par carte de paiement, à l'aide de CiviContribute et CiviEvent, doit être conforme aux normes PCI. Le plug-in que vous utiliserez doit conduire l'utilisateur vers des pages externes pour le traitement des paiements (par exemple: PayPal Standard redirige les utilisateurs vers les pages PayPal pour effectuer la transaction avant de revenir à votre site Web, et devrait donc satisfaire à ces normes).

Si les informations de carte de crédit *sont traitées ou stockées* sur votre serveur, il y a un certain nombre de normes de sécurité des données de paiement PCI (PCI PA-DSS) qui doivent être respectées, y compris le choix d'utiliser SSL. Chaque installation CiviCRM doit également être testée pour sa conformité PCI tous les 4 à 12 mois. Choisissez avec soin la méthode de traitement des paiements que vous avez l'intention d'utiliser avant de la mettre en œuvre. Utilisez SSL si vous optez pour un processeur de paiement par carte de crédit et vérifiez les normes de sécurité si vous décidez de stocker des informations de carte de crédit sur votre serveur (mais ce n'est pas recommandé).

Pour plus d'informations, voir ici: [https://www.pcisecuritystandards.org/merchants/index.php](https://www.pcisecuritystandards.org/merchants/index.php).

### Accès aux données non autorisé

Outre le besoin potentiel de respecter la conformité PCI, vous devez utiliser un certificat SSL si vous souhaitez vous assurer que:

-   Vos données ne peuvent pas être lues par des utilisateurs non autorisés (par exemple en interceptant des données non chiffrées pendant le transit entre l'utilisateur et le serveur).
-   La session d'un utilisateur n'est pas "hi-jacked" par l'acquisition du cookie utilisé pour authentifier leur accès. Si cela se produit, une personne non autorisée peut assumer son identité et procéder à l'utilisation du système via son compte.

Configuration SSL
-----------------
Avant de choisir un fournisseur de serveur Web, vérifiez qu'il prenne bien en charge les certificats SSL. Comme expliqué ci-dessus, SSL crypte les données transférées entre le navigateur Web d'un utilisateur et le serveur, mais ceci n'est *pas activé* lors de l'installation car cela nécessite l'achat d'un certificat SSL auprès d'un fournisseur de confiance. Pour installer SSL:

1.  Déterminez les exigences ou les procédures de votre serveur pour activer un certificat SSL. Sur les serveurs partagés, cela peut nécessiter l'achat d'une adresse IP statique à partir de votre hôte. **Important**: votre hôte doit être disposé à ne pas installer le certificat sur votre *domaine* à un niveau supérieur. CiviCRM ne prend pas en charge le SSL partagé.
2.  Achetez un certificat SSL auprès d'un fournisseur de sécurité.
3.  Installez le protocole SSL sur votre serveur en suivant la procédure décrite à l'étape 1.
4.  Activez la redirection HTTPS sur votre site CiviCRM pour que les pages de connexion, de contribution en ligne, de membre, d'événement et d'administrateur utilisent le cryptage SSL. CiviCRM dispose d'une option dans les paramètres globaux pour vérifier le certificat et activer SSL pour ces pages (**Administer> System Settings> Resource URLs**). Pour utiliser SSL sur *toutes les pages CiviCRM*, modifiez le fichier apache ".htaccess" du serveur pour forcer le SSL et rediriger les requêtes HTTP vers HTTPS ou activer l'option dans votre CMS.

Les sauvegardes et leur sécurité
--------------------------------

Tous les systèmes informatiques sont enclins à des défaillances - matériel et logiciel.
Il est conseillé de créer des sauvegardes périodiques de toutes les données existantes (et éventuellement du logiciel) pour atteindre deux objectifs importants: la récupération et la rétention. En ce qui concerne la récupération, l'organisation peut s'assurer que les données recueillies et stockées dans sa base de données ne sont pas perdues en cas d'échec. Les sauvegardes peuvent également contribuer au renforcement de la continuité des services. Dans certaines situations, il est essentiel que les opérations de collecte ou d'analyse de données ne cessent pas et que la possibilité de construire un outil de travail à partir d'une sauvegarde (pendant que le problème est traité) minimise le temps d'arrêt. Inversement, la rétention est utile lorsque l'organisation doit vérifier l'état des données recueillies à un moment donné dans le passé.

Une fois faites, les sauvegardes elles-mêmes doivent également être sécurisées contre les catastrophes naturelles, le feu, le vandalisme et le vol. Il est recommandé de crypter les sauvegardes et de les dupliquer, de garder une copie sur les lieux et d'envoyer l'autre vers un autre emplacement externe.

Aspect juridique des données
----------------------------

CiviCRM peut être exécuté sur un serveur web géré par votre organisation, ou par un fournisseur d'hébergement externe. Lorsque vous travaillez sur des questions liées aux droits de la personne ou si votre organisation recueille des informations sensibles sur le gouvernement d'un pays ou ses fonctionnaires, il peut être important de savoir où sont stockées vos données. Envisager de recueillir des informations détaillées sur l'emplacement physique des serveurs et sur le pays dont les données relèveront de la compétence d'un organisme gouvernemental.

Autres problèmes de sécurité
----------------------------
Les données peuvent être consultées par des personnes non autorisées à travers une variété de méthodes, dont beaucoup ne sont pas directement liées à la sécurité de CiviCRM. Entre autres, les critères suivants doivent être respectés:

-   Accès physique au serveur: le bâtiment qui héberge les serveurs doit être protégé de manière adéquate contre les intrusions.
-   Mots de passe: une politique organisationnelle doit être mise en œuvre pour que les mots de passe soient d'une complexité et d'une longueur suffisante (par exemple 8 caractères minimum, y compris lettres, majuscules et chiffres) et ne doivent pas être partagés ou divulgués lors de communications non sécurisées telle que le courrier électronique.

