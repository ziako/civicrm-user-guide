Qu'est-ce CiviReport?
===================

Les rapports aident votre organisation à évaluer son impact et à atteindre ses objectifs.
Parfois, c'est une exigence pour les bailleurs de fonds ou autre
parties prenantes. CiviReport vous permet de créer, exécuter et planifier des rapports
en fonction des données que CiviCRM stocke sur vos contacts et leurs interactions
avec votre organisation.

Ces rapports sont des requêtes sur la base de données qui utilisent les critères et les champs
disponibles dans un modèle de rapport. Les rapports peuvent être affichés sur une page
lorsque vous les exécutez, comme un lien sur le tableau de bord ou un courriel planifié
qui peut inclure un fichier CSV ou un fichier PDF.

Scénario: un rapport simple pour aider à collecter des fonds
--------------------------------------------------

1two3, organisation d'aide pour les travailleurs de rues, a lancé une campagne capitale pour recueillir des fonds pour la construction d'un nouvel hébergement. Anne, la directrice du développement voulait contacter les donateurs qui ont fait un don important l'année dernière mais n'ont pas donné d'argent cette année.

Elle a créé une instance du rapport LYBUNT ("L'année dernière mais pas celle-ci") qui filtre les données pour lister les personnes qui ont donné plus de 500 € l'année dernière, puis a exécuté le rapport et utilisé le bouton "Ajouter au groupe" pour mettre ces donateurs dans un nouveau groupe afin qu'elle puisse envoyer un courriel à tous les membres du groupe avec des informations sur cette campagne capitale.

Enfin, elle a ajouté ce rapport à son tableau de bord CiviCRM afin qu'elle puisse examiner les progrès obtenus pour que ce groupe d'anciens donateurs contribue à la campagne actuelle. Quiconque fait un don sortira automatiquement de cette liste puisqu'il ne répond plus aux critères, et la liste restante pourra être utilisée comme base de suivi des appels téléphoniques ou d'autres contacts personnalisés.

Scénario: rapport financier périodique
-------------------------------------

WAM est une association universitaire avec environ 1 500 membres.
Leurs membres renouvellent leur adhésion en ligne et paient par carte ou hors ligne par prélèvement automatique. Marc, le comptable, a besoin de plusieurs rapports pour suivre les recettes financières. L'automatisation de ce processus a été une des principales raisons de la mise en œuvre de CiviCRM. 
Tous ces rapports lui sont envoyés periodiquement par courrier électronique avec un fichier joint en CSV afin qu'il puisse importer les détails dans son logiciel de comptabilité ou leur interface bancaire en ligne. 
Alors que quelques-uns des principaux rapports sont décrits ici, les exigences de WAM étaient assez complexes et des modèles de rapports personnalisés étaient nécessaires aux côtés des rapports standards

Tous les lundi matin, Marc reçoit une liste de tous les paiements en ligne enregistrés de la semaine précédente pour l'importer dans Sage. Ce rapport contient le montant et l'heure du paiement avec son origine (adhésion ou événement) et un identifiant de référence afin qu'il puisse être suivi dans CiviCRM. À la fin de chaque mois, il reçoit une liste de tous les membres qui paient par prélèvement automatique et dont l'adhésion expire le mois suivant. Cela lui permet de configurer les paiements de débit direct pour ces renouvellements d'adhésion en important une partie de la liste dans l'interface bancaire en ligne.

Ces rapports par courrier électronique font gagner à Marc plusieurs heures par mois ce qui lui permet de se concentrer sur des tâches qui contribuent davantage à la gestion efficace des ressources financières de WAM.

Scenario: détermination des contributions totales pour un ménage
---------------------------------------------------------
Une organisation à but non lucratif en Ohio conserve des dossiers individuels organisés par ménages. Une situation courante est que le mari dans le ménage a assisté à un certain nombre d'événements payants, tandis que sa femme s'est également inscrite à d'autres événements et a fait des dons distincts.

Le personnel de l'organisation souhaite voir le total des contributions reçues du ménage afin que lorsque quelqu'un appelle le bureau pour se renseigner sur un don ou un paiement d'événement effectué par quelqu'un d'autre de la famille, toutes les informations pertinentes soient à portée de main. Le personnel peut consulter le rapport de synthèse de dons du ménage selon les besoins, en utilisant le nom du ménage pour trouver toutes les contributions et les informations pertinentes pour répondre aux questions de l'appelant.

