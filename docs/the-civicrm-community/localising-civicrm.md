Régionalisation de CiviCRM
==================

Le code, les interfaces et la documentation de CiviCRM ont été initialement développés en anglais. Cependant, le logiciel a été conçu pour pouvoir s'adapter à toutes les organisations peu importe où elles sont. Ces organisations doivent pouvoir adapter le logiciel selon leurs circonstances, sans qu'il soit nécessaire de modifier le code d'origine.

Pour régionaliser CiviCRM (ou tout autre logiciel), il ne suffit pas de simplement pouvoir changer la langue des textes affichés à  l'écran. Considérons par exemple, la devise monétaire utilisée dans un pays (USD ou $ aux États-Unis, GBP ou £ au Royaume-Uni), le format de la date et de l'heure (le 16 novembre 2016 pourrait être écrit sous la forme de 11/16/2016 aux États-Unis, mais 16.11.2016 en Russie) ou le format des chiffres (1 234 567,89 en Slovakie ou Hongrie, mais 1,234,567**.**89 au Japan ou aux États-Unis).

CiviCRM offre plusieurs fonctionnalités pour s'adapter aux besoins qui peuvent varier selon la langue et selon la région. L'équipe de développement de CiviCRM développe régulièrement de nouveaux outils pour simplifier ce processus. L'écran de Régionalisation (ou Localisation) affiché dans la saisie d'écran ci-dessous permet de configurer les bons paramètres de préférences régionales de CiviCRM. Pour y accéder, se rendre à Administrer > Localisation > Langue, devises et localisation.

![2](../img/CiviCRM_update-CiviCore-2-en.png "2")

Traductions
------------

CiviCRM peut s'adapter à plusieurs langues, cependant l'équipe de développement dépend de la communauté pour traduire les textes qui sont affichés à l'écran.

Un certain nombre de traductions sont déjà disponibles. Certaines traductions sont complétées à 90%, d'autres seulement 5%. Vous pouvez consulter le résumé du projet CiviCRM sur Transifex ([http://www.transifex.net/projects/p/civicrm/](http://www.transifex.net/projects/p/civicrm/)) pour voir l'état de la traduction d'une langue. Vous pouvez télécharger et installer la traduction dans votre instance de CiviCRM pour évaluer si cela répondra à vos besoins.

Il peut arriver que dans certaines situations, la traduction soit correcte, mais que vous auriez préféré utiliser un autre terme dans votre contexte. Dans ce cas, nous vous recommandons d'entrer en contact avec les autres traducteurs pour en discuter.

Les aides à la traduction
-------------------------
Bien que certaines soient encore en cours de développement, un certain nombre d'aides dans CiviCRM soutiennent la communauté dans ses efforts de traduction. Notamment :

1.  Transifex est un outil en ligne qui permet aux groupes de traducteurs de traduire des chaînes de texte et de garder un aperçu de ses progrès. Inscrivez-vous, recherchez votre langue, rejoignez l'équipe ou, si votre langue n'est pas disponible, commencez à traduire.
2.  Un glossaire 
    ([http://wiki.civicrm.org/confluence/display/CRM/Glossary+for+translations](http://wiki.civicrm.org/confluence/display/CRM/Glossary+for+translations))  
    Le wiki de CiviCRM vous aidera à maintenir la cohérence de vos traductions. Il vous aidera également à obtenir un aperçu de la quantité de travail à fournir pour traduire les chaînes de texte que vos utilisateurs verront le plus souvent et qu'il serait donc le plus utile à traduire.    
3.  Une page wiki sur les astuces 
    ([http://wiki.civicrm.org/confluence/display/CRMDOC/Localisation+community+building+howto](http://wiki.civicrm.org/confluence/display/CRMDOC/Localisation+community+building+howto))
    Explique comment aborder le processus de localisation. 
4.  Une FAQ
    ([http://wiki.civicrm.org/confluence/display/CRMDOC/Internationalisation+FAQ)](http://wiki.civicrm.org/confluence/display/CRMDOC/Internationalisation+FAQ)
    Sur le wiki CiviCRM couvre les questions les plus fréquentes sur la localisation.

Comment commencer ? 
---------------

Vous souhaitez aider la communauté à traduire CiviCRM dans une nouvelle langue ou améliorer la traduction en cours? Voici comment le faire (à condition d'avoir un peu d'expérience technique) :

1.  Aller sur transifex.net et créer un compte.
2.  Recherchez votre langue sur  
    [http://www.transifex.net/projects/p/civicrm/teams/](http://www.transifex.net/projects/p/civicrm/teams/)
    ...et rejoignez une équipe, ou demandez la création d'un nouveau language si nécessaire.
3.  Commencez à traduire!

### Un travail d'équipe

Le flux de travail de traduction de CiviCRM est encore en cours jusqu'à ce que le processus devienne plus mature, vous pouvez  vous référer à cette page pour de plus récentes instructions : 
[http://wiki.civicrm.org/confluence/pages/viewpage.action?pageId=88408149](http://wiki.civicrm.org/confluence/pages/viewpage.action?pageId=88408149)

Le travail de traduction est fortement basé sur le travail d'équipe. J'espère que vous avez déjà une équipe de traducteurs pour votre langue. Cette équipe doit construire un glossaire, lancer un jeu de traduction, réviser vos traductions et apporter une critique constructive. Si une telle équipe n'existe pas encore, c'est l'occasion de créer la vôtre.

Composants et fichiers
--------------------

Il ya beaucoup de chaînes (phrases) à traduire dans CiviCRM. Pour faciliter la traduction de la partie qui vous intéresse (espérons celle que vous connaissez le mieux), les chaînes qui ont besoin de traduction ont été divisées en *composants*, qui sont des plugins de CiviCRM (CiviCRM, CiviMail, CiviContribute, etc. .). Un composant distinct est disponible pour chaque version de CiviCRM, à partir de la version 3.2 

Chaque composant contient un certain nombre de fichiers, qui contiennent eux-mêmes les chaînes à traduire. Le composant principal "CiviCRM" (le *noyau*) contient près de 20 fichiers (pour *Pays*, *Provinces*, *Menu*, etc.).

Outils et détails techniques
---------------------------

Vous avez deux processus pour effectuer la traduction : en ligne ou hors ligne selon votre choix. La traduction en ligne ne nécessite pas l'installation d'un logiciel. La traduction hors ligne se fait en téléchargeant les fichiers à partir du site de traduction, avec un logiciel qui offre plus de fonctionnalités que le système en ligne.

### Traduction en ligne 

Transifex est l'outil à utiliser pour la traduction en ligne. Il n'a pas autant de fonctionnalités qu'un outil hors ligne tel que PoEdit, mais c'est la manière la plus simple de contribuer aux traductions et de faire des corrections rapides et occasionnelles. Chaque traducteur doit avoir un compte sur le site Transifex, car les équipes de traduction utilisent les forums et le système de messagerie pour coordonner leur travail.

Les étapes de base de la traduction en ligne sont les suivantes:



1.  Sélectionnez un composant sur  
    [http://www.transifex.net/projects/p/civicrm/](http://www.transifex.net/projects/p/civicrm/). 
    Cela affiche la liste des équipes linguistiques pour ce composant.
2.  Cliquez sur l'icône dans la colonne Options à côté de la langue qui vous intéresse. Cela vous amène à la liste des fichiers de ce composant.
3.  Cliquez sur l'icône "crayon et papier". Cela vous amène à l'écran de traduction en ligne, qui répertorie toutes les chaînes traduisibles dans ce fichier.
4.  Pour chaque chaîne, vous pouvez saisir une traduction.
5.  Lorsque vous avez terminé, cliquez sur le bouton «Envoyer pour examen» à la fin de la page.

### Construire une mémoire de traduction

PoEdit et d'autres logiciels de traduction vous aideront à construire une mémoire de traduction pour votre langue. Cette mémoire de traduction peut soit être restreinte aux traductions effectuées dans CiviCRM, soit inclure des traductions d'autres projets. Si vous incluez d'autres projets, la traduction automatique peut traduire plus de chaînes, mais vous perdrez la cohérence et la plupart des chaînes seront marquées comme floues. Cela pourrait être cependant un moyen de démarrer une nouvelle traduction.

Construire une mémoire de traduction basée sur des mots du glossaire peut être un travail assez long pour assurer la cohérence du travail de votre équipe.
 
### Utilisation du contrôle de version (principalement pour les programmeurs)

Transifex conserve les fichiers dans un système de contrôle de version : 
[http://github.com/civicrm/l10n](http://github.com/civicrm/l10n). Ceci est utile à certains utilisateurs qui trouvent l'interaction avec le site Github plus facile que le téléchargement de chaque fichier séparément par Transifex. 

### Cohérence et consensus 

Afin d'assurer une bonne cohérence dans la traduction, chaque équipe est encouragée à construire et à utiliser un glossaire et à utiliser l'examen par les pairs. Vous pouvez trouver un glossaire de termes communs sur
[http://wiki.civicrm.org/confluence/display/CRM/Glossary+for+translations](http://wiki.civicrm.org/confluence/display/CRM/Glossary+for+translations). 
Vous devez absolument traduire ces termes dans votre langue et vous assurer que votre équipe parvienne à un consensus sur tous les termes définis.

Construire et partager une mémoire de traduction commune est comme un glossaire spécialisé qui peut être utilisé automatiquement par des outils de traduction contribue également à assurer la cohérence. Le système d'aide de PoEdit explique comment construire cette base de données (la plupart des autres logiciels de traduction en font autant).


Team building and sprints
-------------------------

A good way to make progress in translation is to organize *translation
sprints*. This means getting as many people as possible together in the
same room to translate as many documents as they can. Here are a few
things to keep in mind when organizing a translation sprint:

-   Choose a good location, where people will be able to get online
    (enough computers for everybody, or desks to set up laptops and with
    a decent Internet connection). 
-   Provide instructions in advance on how to install an offline
    translation tool such as PoEdit, and have people ready to help
    others install and use it. 
-   Create the glossary in advance. Present the glossary, discuss terms
    which do not have consensus, make sure everybody has access to a
    copy of the glossary, and print a sufficient amount of copies
    beforehand.
-   Determine goals for the sprint: which component will be translated,
    and what percentage your team is trying to achieve.
-   Make sub-teams with clear objectives: per component or file or a
    part of it.
-   If your translators are not familiar with CiviCRM, do a demo of the
    features your team is about to translate.
-   Clearly designate someone who can be interrupted in order to answer
    questions.
-   Make sure you've got enough coffee, tea, chocolate, etc. in reserve
    to keep everybody going through the night.
-   At the end of the sprint, present the result of the translation in a
    demo CiviCRM installation.
-   Discuss whether the team has reached its goal and how to improve
    further.

