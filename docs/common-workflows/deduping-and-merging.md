Dédoublonner et fusionner
=========================

Qu'est-ce que dédoublonner ?
----------------------------

Des contacts peuvent apparaitre en doublon pour plusieurs raisons. Par exemple : 
-   des erreurs d'utilisateurs créant un contact sans réaliser qu'un enregistrement existe déjà dans CiviCRM ;
-   des doublons non traités dans un processus d'importation ;
-   des personnes remplissant des formulaires d'enregistrement sans réaliser qu'elles se sont déjà enregistrées auparavant.


Outils CiviCRM pour dédoublonner les contacts
-------------------------------------------

CiviCRM dispose de plusieurs moyens pour traiter les contacts en doublon. Certains sont utilisés pour en éviter la création, tandus que d'autres permettent de les rechercher, de les identifier et de fusionner les données d'un même contact.

Elles permettent de :

-   scanner la base de donnée selon une règle de déboublonnage (voir ci-dessous) pour en rechercher les doublons et les fusionner au besoin ;
-   sélectionner deux contacts après une rechercher et choisir de les fusionner ;
-   scanner automatiquement la base de données et avertir des possibles doublons lors de la saisie ou la modification d'un contact via l'interface utilisateur ;
-   Fusionner automatiquement les détails d'une personne vers un contact existant quand elle réalise des opérations en ligne telles qu'une inscription à un événement, une adhésion, une contribution... ; 
-   Fusionner automatiquement les détails d'une personne lors du processus d'importation de contacts.


Les règles de dédoublonnage
---------------------------

Les règles de dédoublonnage est une façon de spécifier à CiviCRM les critères selon lesquels des contacts sont considérés ou non comme des doublons. Par exemple, une règle pourrait dire que deux contacts sont des doublons s'ils ont tous les deux la même adresse courriel et le même prénom.

Si vous ne souhaitez pas configurer vos propres règles de dédoublonnage, il existe une règle par défaut que vous pouvez utiliser.

Pour visualiser les règles de dédoublonnage, aller à **Contacts > Rechercher et fusionner les contacts en double** dans le menu principal. Vous arriverez à l'écran suivant :

![Duplicate Choose Find Rule](../img/duplicates-choose-find-rule.png)

Différentes règles par défaut (supervisé et non-supervisé) existent pour chaque type de contact (Individu / Particulier, organisations et ménage / foyer). Les règles par défaut sont utilisées par CiviCRM pour des vérifications automatique, que nous allons expliquer un peu plus bas.

Comprendre les règles de dédoublonnage : Supervisé, Non-supervisé et Général
----------------------------------------------------------------------------

CiviCRM dispose de trois catégories de règles de dédoublonnage :

**Non-supervisé** : Les règles "non-supervisé" sont automatiquement utilisées pour chaque type de contact quand ces derniers sont créés à travers des enregistrements en ligne, tels que les événements, les adhésions, les contributions et les pages de profil. Elles sont également sélectionnées par défaut pour l'importation des contacts. Elles sont optimisées pour s'approcher au mieux de la définition stricte de ce que peut être un doublon, afin d'éviter les faux positifs.

**Supervisé** : Les règles "supervisé" sont automatiquement utilisées pour chaque type de contact quand ces derniers sont créés ou modifiés à l'aide de l'interface utilisateur. Ce dernier recevra une alerte en cas de doublon détecté à l'aide de l'une de ces règles, et pourra décider de continuer ou non en toute connaissance de cause. Les règles de cette catégorie devraient être configurées en suivant une définition large de ce que peut être un doublon, l'utilisateur pouvant décider d'agir en conséquence.

**Général** : vous ne pouvez configurer qu'une seule règle "Non-supervisé" et une seule règle "Supervisé" pour chaque type de contact, mais vous n'avez pas de limite pour les règles "Général" qui vous permettent de définir des critères supplémentaires de détection de doublons.

Configurer les règles
---------------------

Pour déterminer si deux contacts sont des doublons, CiviCRM peut vérifier jusqu'à cinq champs que vous aurez spécifiés. Vous pouvez également préciser sur quelle longueur de chaine de caractère la comparaison de deux champs doit se faire. Par exemple, si vous indiquez une longueur de deux sur le champ **Prénom**, les prénoms "Mike" et "Mickael" seront considérés comme des doublons. En revanche, cela ne sera pas le cas si vous indiquez une longueur de 3 ou plus. Si cette valeur est laissée vide, la comparaison se fera sur la longueur totale des champs.

Chaque champ se voit également associé un "poids numérique" qui détermine le degré d'importance d'une correspondance sur ce dernier. Quand un doublon est détecté par rapport à ce champ, ce poids est ajouté au poids total de la règle. Lorsque tous les champs sont vérifiés, le poids total est comparé au seuil numérique de la règle : si le poids est égal ou plus important, les contacts sont considérés comme des doublons potentiels.

Utiliser les règles et fusionner les contacts en doublon manuellement
---------------------------------------------------------------------

1.  Dans le menu principale, allez à **Contacts > Rechercher et fusionner les contacts en doublon**.
2.  Cliquez sur le lien **Utilisez cette règle** pour scanner des éventuels doublons

3.  Vous pouvez faire une recherche sur l'ensemble des contacts, ou la limiter sur un groupe en particulier. Pour ce dernier cas, CiviCRM recherchera des doublons dont au moins l'un des contacts appartient au groupe concerné.

    ![duplicates-select-group](../img/duplicates-select-group.png)  

    Lors du scan, si le poids numérique entre deux contacts est égal ou supérieur à la valeur de seuil, ces derniers sont affichés sur l'écran suivant en tant que possible doublons. Une liste sera alors affichée en dessous de quelques cases à cocher Afficher / cacher : rue, code postal, conflits et seuil.  

![List of Possible Duplicates](../img/duplicates-list-of-possibles.png)  

4.  Cliquer sur **Fusionner** pour une paire de contacts fait afficher une table montrant les détails de ces derniers. CiviCRM indique l'enregistrement en doublon dans la colonne de gauche, et l'enregistrement original dans la colonne de droite. En cas de fusion, les valeurs de la colonne de gauche remplaceront celles de la colonne de droite.
5.  Si vous souhaitez que l'opération se fasse de la droite vers la gauche, il suffit de cliquer sur **Inverser les contacts en doublons et les originaux** en haut de la page.

![Duplicate Merge Screen](../img/duplicate-merge-screen.png)  

6.  Les lignes de l'écran de fusion ont des codes couleurs.
    -  Le vert indique de l'information est la même pour chaque contact. Ces derniers peuvent être cachés en cliquant sur **Afficher / cacher les lignes ayant des données identiques pour chaque enregistrement de contact**.
    -  Le rouge indique que l'information est différente entre les deux contacts. Pour chaque champ, vous pouvez décider s'il faut garder la valeur originale (laissez la case à cocher au milieu inactive) ou s'il faut utiliser la valeur de l'enregistrement en doublon (cliquez sur la case à cocher). Pour les adresses courriel et les numéros de téléphone, vous pouvez également décider de garder les deux valeurs en cochant la case à cocher dans la colonne du milieu et celle ("ajouter nouveau") de la colonne de droite.
    -  Le jaune indique que l'option par défaut est une case à cocher active. Cela signifie que les données du champ de l'enregistrement en doublon seront ajoutées à celles de l'enregistrement original. Cela s'applique aux étiquettes, aux groupes et aux données d'activités (participation aux événements, contribution...) Si vous décochez cette case, les données de l'enregistrement en doublon seront perdues.
7.  Cliquez sur **Fusionner...** pour lancer l'action, ou sur **Marquer cette paire comme non doublon** si vous pensez que les deux contacts ne sont pas les même.
8.  Quand un contact est marqué "n'est pas un doublon", il est exclu des résultats de toutes les détections de doublons.

Fusionner plusieurs contacts simultanement
------------------------------------------

Parfois, il est plus efficace de fusionner plusieurs paires de doublons en même temps. Vous pouvez le faire depuis l'écran des doublons sur lequel vous pouvez lister jusqu'à 100 lignes.

![List of Possible Duplicates Batch Merge](../img/duplicate-list-of-possibles-detail.png)

Vous pouvez **Fusionner par lot tous les doublons** (cela fusionnera **tous** les doublons détectés, pas uniquement ceux listés à l'écran) ou **Fusionner par lot les doublons sélectionnés** (ceux dont la case à cocher à gauche de leur ligne est active). Ces options de fusion sont affichées en dessous de la liste des doublons détectés. Vous y trouverez également la possiblité d'**Inverser les doublons sélectionnés**. Quand des contacts sont fusionnés, Contact 1 est conservé et Contact 2 est fusionné puis supprimé. Cette option permet d'inverser les rôles.


La fonctionnalité de fusion par lot ne traite que les doublons pour lesquels il n'y a pas de conflit de donnée. Si un champ de l'enregistrement en doublon contient une valeur différente du champ de l'enregistrement original, la paire de doublon sera ignorée par le processus et les contacts ne seront pas fusionnés.

Une fois la fusion par lot effectuée, you will be returned to the
original list. If any of the records were skipped due to a data conflict
like the example above, the message shown below will be displayed. To
view an updated list of duplicate contacts (those that were not merged
by the duplicate process) you must click **Refresh Duplicates**; the
page will not refresh automatically, just in case your database is very
large, and searching for duplicates would cause a significant delay. You
may then continue to assess and merge the remaining duplicates manually.

![image](../img/CiviCRM_dedupe_batchmerge.PNG)

**WARNING:** before you begin to consider using batch dedupe, please
take note of the following:

1.  This feature is intended for use with large data sets that have
    strictly managed field structures. If you have a small database with
    only a few duplicates, we recommend you merge them manually using
    your own judgement.
2.  Once merged, the links between the duplicate contact and records
    elsewhere in the system will be transferred to the original contact
    (e.g. event participant records, groups, tags, contributions,
    activities, cases and memberships). You will NOT be able to reverse
    this change.
3.  Duplicate records, once merged, will be deleted and are not
    recoverable. We strongly recommend backing up your data before
    running a batch merge.

## A multi-stage deduping process

Often just using one deduping rule will mean some duplicate remain in your system.
One process way to apply multiple systematically is given below. If you individual unsupervised rule is strict enough then you may be able to batch de-dupe during the first stage then dedupe manually for the second stage.
1.  Start by looking for dupes using the "Individual unsupervised" rule:
    click the **Use Rule** link (contact type "Individual" at the usage
    "unsupervised").
2.  Select **All Contacts** or a particular group.
3.  Click **Continue**.
4.  If duplicates are found, merge or delete the duplicate contacts.
5.  Now look for duplicates using a "supervised" or "general" rule to
    find those that were missed with the stricter rule: click the **Use
    Rule** link for "Individual supervised" (contact type "Individual"
    at the usage "supervised").
6.  Select **All Contacts** or a particular group.
7.  Click **Continue**.
8.  If duplicates are found, merge or mark them as 'not a duplicate'.


##  Merging contacts from search results

If you notice duplicate contacts within a set of search results you can
quickly merge them directly from the search results instead of using the
separate **Find and Merge Duplicate Contacts** process. This is a great
way to clean up your database during your everyday workflow with minimal
disruption.

1.  Select the duplicate contacts from your search results by clicking
    the check box at the left side of each record.
2.  Select **Merge Contacts** from the ** Actions** menu.
3.  Follow the normal steps for merging duplicate contacts.
