Recherche
=========

Ce chapitre couvre les différentes méthodes pour trouver les informations que vous avez enregistrées dans CiviCRM. 
Vous trouverez ci-après deux techniques de recherche qui sont les fonctions de base dans CIVICRM : la recherche de contacts et la recherche d'action. Les utilisateurs trouvent ces méthodes très utiles.

Nous allons commencer par quelques recherches simples et ensuite passer à des techniques plus avancées. Les débutants de CiviCRM doivent être familiarisés avec la recherche rapide, la recherche avancée et les recherches de composants. Les utilisateurs les plus avancés peuventt également consulter les rapports, les recherches personnalisées et le Générateur de recherche.

Il y a trois raisons principales de faire des recherches :

-   Pour trouver un contact particulier : le champ de recherche rapide peut trouver des contacts par nom, adresse e-mail ou une variété d'autres caractéristiques.
-   Pour effectuer une action sur un ou plusieurs contacts qui répondent à certains critères: la recherche d'action dans CIVICRM permet de trouver des contacts qui répondent à certains critères, puis effectuer une action sur eux. Par exemple, vous pouvez trouver tous les contacts d'un groupe pour les inviter à une réunion, ou tous ceux dont les adhésions ont récemment expiré pour envoyer un rappel de renouvellement ou bien tous les contacts âgés de moins de 25 ans d'une même ville pour envoyer un courriel sur un événement à venir proche du domicile.
-   Pour créer un rapport spécifique : la recherche est souvent utile pour un type de rapport spécifique mais présente des limites. Par exemple, vous ne pouvez pas grouper les résultats par critères particuliers, résumer ou produire facilement des graphiques des résultats. Pour obtenir des rapports plus avancés consultez la section *CiviReport*.

Recherche rapide
--------------

![Quicksearch](../img/quicksearch.png)

La manière la plus simple de trouver un contact spécifique consiste à utiliser la zone de recherche rapide qui apparaît dans le menu de navigation en haut à gauche de l'écran. Vous pouvez choisir de faire une recherche parmi plusieurs critères. Dès que vous cliquez dans la case, vous pouvez commencer à taper immédiatement pour utiliser la recherche par défaut : "Nom / E-mail".  Vous pouvez aussi cliquer à nouveau pour choisir plusieurs autres critères dans une liste déroulante. Les contacts correspondants au mot que vous entrez apparaîtront dans une liste déroulante sous la boîte. 

Par exemple, si vous recherchez avec Nom / Email et que vous avez laissé le caractère générique de recherche approximative activé, allez dans **Administer> Personnaliser les données et les écrans> Préférences de recherche** pour vérifier.

Ainsi en entrant "pierre", vous trouverez:

-   Les personnes dont le prénom ou le nom de famille est **Pierre**
-   Les personnes qui ont Pierre comme faisant partie de leur nom, ex. Marie **Pierre** LEBRETON
-   Les personnes qui ont Pierre dans leur adresse électronique, ex. jean.**pierre**@gmail.com
-   les organisations avec Pierre en leur nom, ex.  Association **Pierre** Insertion.

Vous n'avez pas besoin de taper le nom complet de la personne... juste les premières lettres.
Remarque: Si vous effectuez une recherche par **téléphone**, vous devrez entrer les chiffres du numéro de téléphone sans aucun formatage. La recherche de **téléphone** est effectuée sur un champ composé uniquement de chiffres dont tous les caractères non numériques ont été retirés.

Recherche multicritère
---------------
![Screen shot of advanced search](../img/user-interface-advanced-search-main-screen.png)

La recherche avancée vous permet de rechercher dans toutes les informations que vous avez sur vos contacts. Par exemple, vous pourriez trouver «tous les contacts en Italie» ou «tous les membres du groupe adhérents». Si vous spécifiez deux catégories d'informations ou plus, la recherche affiche tous les contacts correspondant à toutes les catégories. Vous pouvez aussi combiner les deux critères mentionnés pour trouver «tous les membres du groupe adhérents en Italie».

L'écran "Recherche multicritère" est accessible depuis le menu de navigation  **Recherche> Recherche multicritère**. Sur cet écran, les critères de recherche sont regroupés en sections qui font référence à différents types de données sur lesquelles vous pouvez effectuer une recherche, telles que des données d'adresse, des notes et des informations provenant de composants tels que Contributions ou Evénements. Chaque groupe de critères est représenté sous la forme d'une barre bleue (connue sous le nom d'«accordéon» car elle s'élargit lorsque vous cliquez dessus). Par exemple, si vous souhaitez rechercher toutes les personnes de votre base de données de 16 à 18 ans, cliquez sur l'accordéon de données démographiques. Lorsqu'il s'ouvre, vous pouvez spécifier la période de la date de naissance qui vous intéresse.

#### Paramètres d'affichage des résultats

![Screen shot of Display Results As](../img/user-interface-display-results-as.png)

La Recherche multicritère renvoie vos résultats en tant que "Vue par défaut". Vous pouvez obtenir un autre type d'affichage. Par exemple, vous pouvez rechercher sur l'activité Renouvellement d'adhésion pour trouver tous ceux qui ont renouvelé leur adhésion la semaine dernière, puis afficher les résultats sous la forme d'adhésions afin d'exporter le nom, l'adresse et la date d'expiration de l'adhésion et lister les membres concernés. Il suffit alors de sélectionner le type d'affichage souhaité dans la liste déroulante **Views For Display Contact**.

#### Views for Display Contacts

![Screen shot of Display Contacts](../img/user-interface-new-contact-view-profile.png)

La recherche multicritère vous permet de modifier les colonnes affichées dans vos résultats de recherche. Les colonnes par défaut sont Nom, Adresse, Ville, État, Code Postal, Pays, Email et Téléphone. Si vous souhaitez afficher un ensemble différent de colonnes (peut-être pour inclure un champ personnalisé ou supprimer une colonne dont vous n'avez pas besoin), créez un profil avec l'option de vues de recherche sélectionnée. Assurez-vous que les champs Visibilité de ce profil est activé comme "Exposer publiquement et pour les listes", et que le champ "colonne de résultats" soit activé. (Pour plus d'informations sur la création de profils voir le chapitre Profils de la section Configuration.)

Par exemple, vous pouvez inclure des colonnes pour le sexe et la date de naissance, tout en éliminant le pays.

Créez un profil qui inclut la date de naissance, le sexe et les champs d'adresse.

![Screen shot of Search View setting in a profile](../img/user-interface-profile-search-view-setting.png)

![Screen shot of Visibility setting in a profile](../img/user-interface-profile-search-view-setting-2.png)

![Screen shot of a profile](../img/user-interface-new-contact-view-profile.png)

Pour en savoir plus sur la création de profils consultez la section *Profils* du chapitre *Organisation de vos données*.

La combinaison de cette fonctionnalité avec l'action "Mise à jour par lots via profil" fournit une méthode puissante de visualisation et de mise à jour d'un ensemble spécifique de champs d'un lot d'enregistrements de contacts.

### Paramètres de recherche

L'opérateur de recherche détermine si vos critères sont combinés avec des instructions ET ou OU . Par exemple, vous voulez trouver tous les contacts qui font partie du groupe Volontaires ET qui ont une activité de formation des bénévoles. Dans ce cas, utilisez l'opérateur ET. Si vous avez besoin de trouver tous ceux qui sont dans le groupe des Volontaires OU ont une activité de formation des bénévoles, utilisez l'opérateur OR.

La recherche dans la corbeille vous permet de rechercher des contacts qui ont été supprimés mais pas supprimés définitivement. Lorsqu'un contact est supprimé, le contact et toutes les données associées sont déplacées vers la corbeille. Seuls les utilisateurs disposant de la permission appropriée pourront rechercher dans la corbeille et pourront restaurer le contact de la corbeille.

![Screen shot of Search in Trash](../img/user-interface-search-in-trash.png)

### Le filtre de plage de dates

![Screen shot of Date Range Filter](../img/user-interface-date-filter.png)

La plupart des recherches dans CIVICRM comprennent un filtre de plage de dates. Les images ci-dessous montrent deux exemples:

-   En utilisant une plage de dates absolue, ex. "1er Jan 2010" au "31 juillet 2010"
-   En utilisant une plage de dates relative, ex. "Semaine précédente"

Les plages de dates relatives sont particulièrement utiles pour les recherches que vous souhaitez enregistrer sous forme de groupes intelligents (groupes remplis automatiquement qui sont configurés pour inclure des contacts qui partagent un certain ensemble de caractéristiques ou d'activités). Pour plus d'informations, reportez-vous au chapitre *Groupes et étiquettes*.

![Screen shot of Relative Date Range Filter](../img/user-interface-date-filter-relative.png)

Par exemple, vous pouvez utiliser une recherche relative à la période pour trouver:


-   Contacts ayant contribué au cours des 7 derniers jours (intervalle de date relatif - "Depuis 1 semaine")
-   Les participants aux événement de l'année (Période de référence - «Cette année»)
-   Les contacts qui ont un certain âge

Les filtres de dates relatives basés sur l'intervalle de temps «semaine» supposent que dimanche est le premier jour de la semaine. Ce n'est pas vrai dans tous les pays, par exemple en Europe et dans de nombreux pays de la région Asie / Pacifique le lundi est le premier jour de la semaine. Pour définir quel est le premier jour de la semaine, vous devez aller à **Administrer >> Localisation >> Format de date**.

![Screen shot of how to change the first day of the week](../img/user-interface-searching-week-begins.png)


#### **Combinaison des critères de recherche**

Certains critères peuvent être combinés par "ET". Par exemple, si vous sélectionnez l'étiquette «donateur» et le pays «Italie», la recherche renverra les principaux donateurs d'Italie. La recherche ne renverra pas les  donateurs qui ne sont pas *d'Italie, ni ceux d'Italie qui ne sont pas * donateurs*.

Vous pouvez modifier l'opérateur de recherche par défaut de ET par OU dans les paramètres de recherche.

Dans les groupes de critères qui vous permettent de cocher des cases pour plus de valeurs, ces options sont également combinées par "ET". Par exemple, si vous pouvez rechercher des contacts dont le Moyen de communication préférée est à la fois E-mail *ET*  SMS.

Avec des champs qui vous permettent de sélectionner plus d'une valeur dans une liste déroulante, les valeurs sont toujours combinées avec "OU". Par exemple, vous pouvez trouver des contacts qui vivent en Italie ou en Espagne.

![Screen shot of combining search criteria](../img/user-interface-searching-states.png)

Constructeur de recherche
-------------------------

Advanced search lets you choose from a wide range of criteria in a
user-friendly panel, but this has limitations. Search builder allows you
to define your own search and arrange the criteria according to your
specific needs.

Search Builder allows you to choose from a range of operators:



| Operator  | Purpose | Example |

| -- | -- | -- |
| = | Equals. Matches on the exact value you specify | **"First Name" = "Bob"** will find contacts who's first name is exactly "Bob" |

|  ≠  | Not equals. Matches on everything that is not the specified value. | **"Gender" ≠ "Female"** will find contacts who are not female |
|  > , ≥  | Greater-than, greater-than-or-equal-to | **"Birth Date" ≥ "Jan 1 2000"** will find contacts born on or after Jan 1 2000  |
| < , ≤ | Less-than, less-than-or-equal-to | **"Last Name" < "J"** will find contacts whose name starts with a letter that comes before J in the alphabet  |
| In | Value is one of those you specify | "Group" In "Board Members, Staff" will find contacts who are in either of the specified groups |
| Like| Same as the = operator, but supports the % wildcard character | **"Last Name" Like "Gree%"** will find contacts whose last name begins with "Gree" (Green, Greenberg, etc)  |
| Regex | Same as the = operator, but supports all regular expression operators. See http://en.wikipedia.org/wiki/Regular_expressions | **"Middle Name" Regex "[a-c]"** will find contacts whose middle initial is A, B or C  |
| Is Empty, Not Empty| Empty means the field exists and is equal to the number zero or contains nothing.  | **"City" Is Empty** will find all contacts who do have an address but the city was left blank  |
| Is Null, Not Null | Null means the field does not exist or contains nothing.  | **"City" Is Null** will find all contacts who do not have an address at all  |



Search Builder also allows you to combine criteria with multiple AND and
OR groups. To AND criteria (which means to find results matching all
criteria specified), click **Another search field** and enter criteria
under **Include contacts where**. To OR criteria (which means to find
results matching either one OR the other criterion), enter one
criterion in **Include contacts where** and the other under **Also
include contacts where.** The following example will search for females
born after Jan 1 2000 OR members of the Administrators or Advisory Board
groups:

![Search Builder](../img/Search%20Builder.png)

Your search results will contain each contact's name, plus a column for
each search criteria you've defined. If you export search results, the
export file will contain those same columns.

Just like other searches, you can choose from a list of actions to apply
to the results of your search. If you export results, you can select
fields for export. Note that the fields you searched on will get
exported by default in addition to those you select.

You can also save your Search Builder search as a Smart Group. For more
information on Smart Groups, see the *Groups and Tags* chapter.

Full-text Search
----------------

You can use this to search for text values all fields of the database.
This is particularly useful, for example, if you can remember specific
words that you have used but can't remember where you have put them. For
example, lets say that you recorded an activity with a contact and added
specific words to the description but have now forgot the contact's
name. You can use Full text search to find the contact and activity by
words that you remember from the description.

Component searches
------------------

Most CiviCRM components offer a search on the data they maintain, such
as **Find contributions**, **Find members**, etc. These forms work in a similar
way to **Advanced search** but return rows of the main objects associated
with the components, instead of contacts. **Find Members** returns
memberships, **Find Participants** shows event registrations, **Find
Contributions** returns contributions and so on.

Each component search has its own Action list. See the *Component*
sections for more details.

Note that you can also use the Advanced search in conjunction with
**Display Results As** to search for component objects based on criteria
available in advanced search. For example, you could find all event
attendances from contacts that are also members.

Custom searches
---------------

Custom searches are designed to answer specific questions that can't be
easily answered using **Advanced Search** or **Search Builder.**

Go to **Search** > **Custom Search** in the navigation menu and look at
the list of available custom searches.These customized searches have
been written by members of the CiviCRM community to meet their own
needs, and then contributed back to the community to share with others
who need the same or similar custom searches. It's worth spending some
time exploring these searches as some may be useful to you, and they
will give you an idea of the sorts of things that are possible. Though
some of these searches can be done in the Advanced Search (especially in
later versions), custom searches are also set up to display results
according to your search and may provide more useful columns in the
results for your needs. Here's a short description of the custom
searches available.

### Finding contacts in one group but not in another

This is probably the most popular custom search.

When using Advanced Search, if you select several groups in the Group
list near the top, it will treat the search as an OR search, and return
results for contacts who are in any of the groups you select. If you
want to find contacts who belong to all of the selected groups, you will
need to use Search Builder.

There is also a very useful built-in custom search, "Include/Exclude
Contacts in a Group/Tag", that enables you to find contacts who are in
one group but not in another, which you can find by going to **Search >
Custom Searches** in the navigation menu.

![Include/Exclude Search](../img/IncludeExclude.png)

By combining Include and Exclude options, you can find contacts who are
in one group but remove just the group members who fit another
criterion. For example, you may want to find all the contacts who are
Newsletter Subscribers or volunteers, but exclude members of Advisory
Board, perhaps to create a new mailing list to receive a message
targeted at the most external circles of your constituents.

### **Household Name and State**

Search households in a state or province.

Note: which states or provinces are available in the search depends on
your localization settings. Add additional countries by going to
**Administer** > **Configure** > **Global Settings** >
**Localization**. Add to the column of "Available States and Provinces",
but note this change will also affect profile forms which include
country or state/province fields.

### **Contribution Aggregate**

Find aggregate totals of contributions from contacts within a range of
dates.

### **Postal Mailing**

Search for contacts in a given group and display results with mailing
information. Use this search to batch update contact information, send
an email, export contacts, or other actions.

### **Proximity Search**

Search for contacts located within x miles/kilometres of a specific
geographical area.

1.  Go to **Search > Custom Searches > Proximity Search**
2.  Enter the distance in miles or kilometres.
3.  Enter the country within which you want to search.
4.  Enter any other parameters you wish to give your search.
5.  Click **Search**.

**TIP:** You can also incorporate Proximity Searching in a profile which
you've configured for use as a search form.

### **Event Aggregate**

Search on event-related payments for a given event or event type in a
given date range. You may also limit results to show credit card
payments only or payees only. See also event reports for more useful
event search options.

### **Activity Search**

Find activities using any or all of the activity-related criteria. This
is also possible in Advanced Search by using Display results as.

### **Price Set Details for Event Participants**

Get detailed information about which participants opted for which
different paid options related to an event. For example, see who paid
just the event fee, who paid for the additional workshop and who paid
for dinner.

### **Find Contribution Amounts by Tag**

Search on any tag for contributions within a range of dates.

### **Zip Code Range**

Find contacts in a specified zip code or postal code range. This is
useful for targeted mailings or conducting surveys in a particular
geographical area.

1.  Go to **Search > Custom Searches > Zip Code Range**.

2.  Enter the start and end range of the zip or postal codes.

3.  Click **Search**.

### **Date Added to CiviCRM**

Search for contacts that have been added within a particular time
period. Including a group displays just those added within the specified
time frame who are also in that group. Excluding a group removes those
group members from the results.

### **Custom Group Multiple Values Listing**

A search for multi-value custom data.

### **Contributions made in Year X and not Year Y**

Search for contributions that have been made in one year but not
another. This is useful for following up semi-regular donors and
encouraging them to donate more regularly. See also the LYBUNT and
SYBUNT reports.

None of the fields are required; you can choose whether to search a
specified amount range as well as a time period, and whether you want to
exclude minimum or maximum amounts.

It is possible to write your own custom searches, but you'll need to be
comfortable with MySQL and PHP. See the Developer wiki at
[http://wiki.civicrm.org/confluence/display/CRMDOC/Develop](http://wiki.civicrm.org/confluence/display/CRMDOC/Develop)
for more information about how to do this. If you create a custom search
that you think could be useful for others, consider contributing it back
to the community.

The 'search-action' workflow
----------------------------

After you retrieve your search results, you can perform a number of
actions. An Actions box appears above the results. You can select either
all records or specific records, then carry out an action with the
selected records. Different actions are covered in more detail in the
chapter on Everyday Tasks.

![Screen shot of Action Dropdown](../img/user-interface-searching-actions-dropdown.png)

Some of the most commonly used actions are Add Contacts to Group, Export
Contacts, Map Contacts, and creating and printing Mailing Labels. (To
use Map Contacts, you will need to configure Mapping and Geocoding. You
can read more about this in the *Installation* chapter of the
*Configuration* section of this manual).

For example, to send email to a selected number of contacts, mark the
contacts you are interested in and then select **Send Email to Contacts** in
the dropdown list of actions.

The contact summary pop-up
--------------------------

You can see a pop-up box with detailed information for any contact
listed in your search results by hovering over the contact icon in the
left column, as shown below. You can adjust the fields shown in this
"pop-up view" by modifying the fields included in the "Summary Overlay"
profile (**Administer** > **Customize Data and Screens** >
**Profiles**).

![Screen shot of Contact Summary pop-up](../img/user-interface-searching-summary-overlay.png)

The wildcard (%)
----------------

Understanding wildcards greatly expands your search options. A wildcard
represents any character (letter, numeral or punctuation mark). In
CiviCRM, the wildcard is represented by the % symbol (you may be
familiar with other symbols such as * from other applications). It is
most easily understood through examples.

Suppose that somebody asked you to find a contact with a first name
similar to "Michael", but possible something different such as
"Michelle" or "Michał". If you search for "Mich%" you will find all
these variations, including a contact who is supposed to be named
"Michael" but whose name was misspelled as "Micheal". Wildcards can be
used before, after, or even within words. For example, searching on
'Mich%el' will exclude "Michał" and "Micheal" but still find "Michelle"
and "Michael".  

Case sensitivity
------------------

Note that when you search for character strings, the search is not
case-sensitive. For example, if you search for 'brooklyn', the search
will return strings with capitalised letters if the string exists, e.g.
'Brooklyn' or 'BROOKLYN'. Entering "mi%el" in lowercase will also find
contacts with an upper case 'M' in their name.
