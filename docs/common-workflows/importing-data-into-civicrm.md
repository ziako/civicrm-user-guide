Importer des données dans CiviCRM
=================================

Beaucoup d'organisations possèdent des données dont la source ne provient pas de CiviCRM, telle que des plateformes de base de données utilisées à l'origine, des feuilles de calcul créées à la volée pour des événements spécifiques ou pour d'autres besoins, et des annuaires d'adresses courriel. Parce qu'entrer manuellement une grande quantité de données peut être fastidieux, CiviCRM fournit un moyen d'importer des données en masse si la source peut être exportée dans un format répandu tel qu'un fichier CSV (Comma Separated Value).

L'importation peut également être utilisée pour mettre à jour des données existantes. Ce point sera abordé dans la dernière section de ce chapitre.

Considérations avant d'importer
-------------------------------

Pour plus de détails sur la façon d'organiser vos données avant de les importer dans CiviCRM, merci de lire la section "Organiser vos données", et plus particulièrement "Comment organiser vos données".

Preparer les données à importer
-------------------------------

Importer des données requiert un soin et une attention extrêmes, nous allons par conséquent vous présenter certains concepts que vous devriez connaître avant de commencer votre première importation. Vous pouvez importer des données métier CiviCRM ainsi que des données personnalisées pour les contacts, mais aussi des données concernant la participation à des événements, des activités, des adhésions et des contributions. Ce chapitre se focalisera sur le processus d'importation pour les contacts. Les processus pour les autres données sont similaires.

Il existe deux façons d'importer des données :

-   Depuis des fichiers CSV. La plupart des bases de données et des applications de feuille de calcul (par ex. OpenOffice.org Calc, Google Spreadsheets, Microsoft Excel) peuvent créer et manipuler des fichiers dans ce format. Il est souvent plus facile de visualiser et nettoyer vos données lorsqu'elles sont dans un fichier CSV plutôt qu'encore enregistrées dans votre vieille base de données.

    Chaque colonne de votre fichier CSV doit correspondre à un champ de CiviCRM, assurez-vous donc d'associer une colonne propre à chaque type d'information.

    Selon votre pays ou région, les champs de votre fichier CSV peuvent être séparés par des points-virgules (;) à la place des virgules (,). Si c'est le cas, vous aurez besoin de changer la valeur du champ Séparateur de champs pour l'import / export dans les paramètres de localisation en allant dans le menu de navigation et en choisissant Administrer > Configurer > Paramètres généraux > Localisation.

-   Depuis une autre base de donnée SQL ou MySQL stockée sur le même serveur, en utilisant une requête SQL (cette option n'est à considérer que par les utilisateurs avancés maitrisant les techniques d'administration des serveurs et des bases de données). 

Si vous ne maîtrisez pas parfaitement la structure de vos données existantes et comment les faire correspondre aux champs CiviCRM, vous rencontrerez frustrations et problèmes durant vos essais d'importation. Merci de vous renseigner sur le type de chaque donnée dans les autres sections de ce manuel CiviCRM et de visiter la documentation en ligne de CiviCRM pour plus d'information :
[http://wiki.civicrm.org/confluence/display/CRMDOC/Importing+Data](http://wiki.civicrm.org/confluence/display/CRMDOC/Importing+Data)

Les règles et recommandations suivantes vous aideront à importer vos données en minimisant les problèmes :

-   Testez toujours l'importation de vos données avec un échantillon représentatif de vos enregistrements. Après avoir effectué le test, vérifiez vos enregistrements dans CiviCRM et assurez-vous que les données ont été importées et fonctionnent telles que vous l'escomptiez.    
-   Il peut être utile de créer un contact de test qui possède tous les attributs que vous avez définis dans votre jeu de données existant. Importez ensuite votre contact et vérifiez le résultat pour vous assurer que toutes les données sont correctement affichées dans CiviCRM.    
-   Lorsque, durant l'importation, vous faites correspondre les colonnes ou les champs de vos données sources vers les champs CiviCRM, ce dernier peut sauvegarder cette correspondance en tant que *table de correspondance* pour une utilisation future. Cela s'avère pratique si vous avez de multiples fichiers à importer ayant la même structure. Pour sauvegarder une table de correspondance pour une utilisation future, cliquez sur la case à cocher "Sauvegarder cette correspondance" en bas de l'écran Correspondance de champ de l'assistant d'importation et entrez un nom approprié et une description. Pour réutiliser une correspondance d'importation, sélectionnez-la depuis le menu déroulant Load Saved Field Mapping sur l'écran Import des données (étape 1) de l'assistant d'importation.    
-   Si vos importations dépasse le temps autorisé ou prennent trop de temps, essayez de découper vos fichiers en des lots plus petits. Si vous avez les autorisations adéquates sur votre serveur web, vous pouvez également augmenter les valeurs memory_limit et max_execution_time dans le fichier php.ini.
    
-   Vous pouvez ajouter lors d'un import des nouveaux (ou existants) groupes ou étiquettes à tous vos contacts importés. Tous les contacts au sein d'une même importation se verront attribués les mêmes groupes et étiquettes. Cette limitation a un double effet sur votre importation :
    -   Soyez sûr d'attribuer des groupes et des étiquettes qui soient applicables à chaque contact de votre jeu de données à importer. Si vous avez besoin d'attribuer des groupes ou des étiquettes contact par contact, importez-les par petits lots distincts dans lesquels tous les contacts partagent des groupes et des étiquettes identiques. Ou alors, vous pouvez créer des champs de données personnalisées dans CiviCRM contenant les noms des groupes et étiquettes que vous souhaitez attribuer à chaque contact. Après l'importation, vous pouvez ensuite effectuer des recherches par rapport à ces champs et utiliser les actions de traitements par lot "Ajouter Contacts au Groupe" ou "Étiquetter les contacts" sur les résultats de recherche.
    -   Vous pouvez utiliser cette fonctionnalité pour gérer vos importations. Ajoutez des contacts à un nouveau groupe ou une nouvelle étiquette indiquant de quel lot d'importation vos contacts font partie. Cela vous permettra d'identifier facilement quand un contact a été importé et supprimer une importation entière si nécessaire.
-   CiviCRM stocke les prénoms et noms dans deux champs séparés, ils devraient donc apparaître dans deux colonnes distinctes dans votre fichier CSV. C'est la même chose pour le nom de ville et code postal. La plupart des feuilles de calcul contiennent des outils qui automatise le processus de séparation d'une chaine de caractère en deux champs distincts.
-   Assurez-vous que vos noms de pays soient de la même forme que ceux stockés dans CiviCRM, par ex., "États-Unis" et non "États-unis d'Amérique", et "Royaume-Uni" et non pas "Grande-Bretagne".
-   Si vous importez plusieurs adresses de contact, la première adresse sera paramétrée comme adresse principale. Vous voudrez peut-être déplacer vos colonnes pour vous assurer que la bonne adresse devienne l'adresse principale. Vous aurez peut-être également besoin de séparer votre fichier d'importation de telle sorte que certains enregistrements aient telle adresse principale, tandis que d'autres en aient une différente.
-   Si vous importez des données dans des champs personnalisés de choix multiples (par ex. des cases à cocher ou des boutons radio), la source de vos données peut soit utiliser le libellé (que l'utilisateur peut voir sur le front end de CiviCRM) ou la valeur (qui est la valeur véritablement stockée dans la base de donnée par rapport au libellé). CiviCRM saura reconnaitre la donnée et l'importera de façon appropriée. Lorsque vous importez des champs métier de données à choix multiple, vous ne pouvez que spécifier la ou les valeurs dans votre source de données, et non le libellé.
-   Si vous mettez à jour des options à choix multiples, les nouvelles valeurs écraseront totalement le champ. Par exemple, si vous mettez à jour la valeur du champ Couleurs sur "orange" pour un contact qui a actuellement paramétré Couleurs sur "bleu", il en résultera que Couleurs sera paramétré sur orange et non orange et bleu.
-   Assurez-vous que la source de vos données utilise un format de date valide et que vous ayez sélectionné le même format de date dans la rubrique Format de date de l'assistant d'importation.  
-   Assurez-vous que tous les préfixes et suffixes de nom que vous utilisez aient été paramétrés dans l'interface d'administration (aller à Administrer > Listes déroulantes**** dans le menu de navigation).
-   Si vous prévoyez de faire des importations additionnelles de données liées à vos données de contact, par ex. des données de contribution, de participation à des événements, d'adhésion, vous pouvez vous faciliter la tâche en vous assurant que vos enregistrements de contact possèdent un identifiant unique qui soit également associé à vos données liées. Au moment de l'importation initiale de vos données de contact, importez ces identifiants uniques et faites les correspondre au champ ID externe de CiviCRM, vous pourrez ainsi utiliser ces identifiants pour importer ultérieurement des données liées aux enregistrements des contacts.
-   Master Address Belongs To est un champ d'importation spécial qui ne fonctionne qu'avec CiviCRM_Address.id. L'information à renseigner dans ce champ n'est disponible que directement depuis les tables de la base de données MySQL. Elles n'apparaissent nulle part dans CiviCRM, y compris dans les écrans de données, les liens urls, les profils et les exports. [De l'information sur la façon d'utiliser ce champ spécial est disponible sur le Wiki](http://wiki.civicrm.org/confluence/display/CRMDOC/Importing+Data+-+Notes "CiviCRM Wiki - Importing Data").

Required Fields for Contact Imports
-----------------------------------

When preparing your data import it is helpful to know what fields are
required for Import. You'll want to be sure that these fields are
included in your CSV import file. Below is a list of the required
fields. They are marked red and starred in the interface. In case you
have less data, **selecting one field is enough**. The External
Identifier field is only useful if you want to update existing contacts.
Please note that the field with the identifier **(Match to Contact)**is
required for deduplication purposes.

-   **Email (Match to Contact)**
-   **External Identifier**
-   **First Name**
-   **Last Name**

Setting up a CSV file for importing
-----------------------------------

Example of spreadsheet .csv format

![student_sample](../img/CiviCRM-student_sample-en.png)

When thinking about setting up your spreadsheet, think about the data
that you are collecting and plan out your column headings. Keep in mind
that you may need to create more than one .csv file and perform multiple
imports before you are finished.

If you plan to import related data that pertains to a specific contact,
e.g. event participant information, contribution data, etc., you will
need to make sure that each contact record has a unique identifier or
the contact record should have First Name, Last Name and Email, so that
you can link their related data during later imports. If you have
unique ID, you would map the ID to CiviCRM's External Identifier on
import.

Running an import
-----------------

The import process has four steps.

### Step 1: Setup

Setup lets you specify the basic details of your import, including the
source of the data. Data can come from either a CSV file, or an SQL
query of a database on your server. A check-box lets you indicate
whether the first row of your file contains column headers.

![image](../img/Screen%20Shot%202015-04-29%20at%203.54.21%20PM.png)

Note that imports use the default **unsupervised** rule to decide
whether a contact record is a duplicate (refer to the *Deduping and
Merging* chapter in this section for information on duplicate matching
rules in CiviCRM). You can specify what action to take when an import
encounters a duplicate:

-   **Skip**: skip the duplicate contact, i.e. leave the original record
    as it is.
-   **Update**: update the original record with the database fields from
    the import data. Fields that are not included in the import data
    will be left as they are.
-   **Fill**: fill in the additional contact data, if it contains fields
    that are missing or blank in the original records, and leave fields
    which currently have values as they are.
-   **No Duplicate Checking**: this inserts all valid records without
    comparing them to existing contact records for possible duplicates.

![image](../img/Import%20Options.png)

**Import mappings** tell CiviCRM how the fields of data in your import
file correspond to the fields in CiviCRM. The first time you import from
a particular data source, it's a good idea to check the box to "Save
this field mapping" at the bottom of the page before continuing. The
saved mapping can then be easily reused the next time similar data is
imported, by requesting that it be loaded at this step.

### Step 2: Match the fields

If you had column headings in your file, these headings will appear in
the first column on the left-hand side of the Field Map, while the next
two columns show two rows of data in your file to be imported, and the
fourth column is the Matching CiviCRM Field. If you loaded an import
mapping in Step 1, your choices will be reflected here. You can change
them if they are inappropriate for this import.

![ImportMatchFields](../img/CiviCRM_update-CiviCore-ImportMatchFields-en.png "ImportMatchFields")

The matching CiviCRM fields include standard CiviCRM data such as First
Name and Last Name as well as any custom data fields that have been
configured for use with contact records on your site. Match the fields
by clicking the dropdown list and selecting the appropriate data. For
example, if the heading of the second column in your input is Surname,
you should choose Last Name as your Matching CiviCRM Field.

Select "- do not import -" for any columns in the import file that you
don't want to import into CiviCRM.

If you have a saved mapping for a specific set of spreadsheet columns,
and your spreadsheet layout has changed (for instance, you need to
import additional fields, so you add the appropriate columns of data in
the spreadsheet), you can modify and save the field mapping. One tip to
ease the mapping process when you need to import additional fields is to
place the additional columns of data in your import spreadsheet to the
right of the columns you've previously mapped in CiviCRM. This allows
you to use the existing saved field mapping to map the initial import
fields, and then continue mapping the new data fields.

![Step2d](../img/CiviCRM-AddingImporting-Step2d-en.png "Step2d")

Note that if you add new data columns in your spreadsheet and do not
position the columns AFTER the columns you previously mapped, you then
can't use the saved mapping and will have to map all your import fields
again.

Once you've mapped your fields, you can decide if you want to keep the
original saved mapping unchanged, or check the box to "Update this field
mapping" to include the new field mappings.

### Step 3: Preview

This screen previews the results of importing your data, reports the
number of rows to be imported, and allows you to double check your field
matches.

If some of the rows in your spreadsheet contain data that doesn't match
CiviCRM's requirements for one or more fields, you'll see an error
message with a count of the invalid rows (see the screenshot below).
Click the Download Errors link and review the errors reported in the
downloaded file, so you can fix them before doing the import.

![ImportPreviewErrs](../img/CiviCRM_update-CiviCore-ImportPreviewErrs-en.png "ImportPreviewErrs")

At the bottom of the form, you can choose to add the contacts to an
existing group, import to a new group, create a new tag, or tag imported
records. Adding imported records to a separate group is strongly
recommended in order to be able to quickly find the imports and, if
necessary, delete and reimport them.

![Step3b_1](../img/CiviCRM-AddingImporting-Step3b_1-en.png "Step3b_1")

### Step 4: Summary

The final screen reports the successful imports along with Duplicate
Contacts and Errors. If you have set the import to add all contacts to a
Group or Tag, you can click through to see your imported contact
records.

![Step4a_2](../img/CiviCRM-AddingImporting-Step4a_2-en.png "Step4a_2")

At this point it makes sense to check to make sure that your import has
worked as expected. Search for the contacts that you just imported and
examine their fields and custom data to make sure all is as expected.

Importing relational data
-------------------------

We have just described the process of importing one data file. But what
about if you want to import related data, like organizational addresses
with employees, parent child relationships, activities, contributions,
etc.? For each type of data you want to import, you will need to import
a separate CSV file.

CiviCRM has specific tools for importing related contact data and a set
of specific import tools for contributions, memberships, event
participation etc. (and you should see specific chapters for details of
how to use these tools). To import relationships, you should run
multiple contact imports.

For example if we want to import data for children and then for both
parents, we run three imports, one for the child, one for the father and
one for the mother.

We first import the child remembering to include an external identifier
that we can use to match the child to their parents. We then import the
father, and then the mother, as related contacts, linking them to the
child using the child's external identifier.

In the example below we have one CSV file which contains father and
mother information. We use this CSV file twice as part of the import.
Have a look at the fields below to understand what is happening.

![Parent1a](../img/CiviCRM-AddingImporting-Parent1a-en.png "Parent1a")

![Parent1b](../img/CiviCRM-AddingImporting-Parent1b-en.png "Parent1b")

We are linking the father to the original child using the external
identifier and are then importing the related father name using the
'Child of' relationship type.

When the import is done, go back and verify the data by searching for
the parent and examining the relationship tab. They should have a
relationship linking them to the child.

You can then repeat this process for the mother, and also for other
relationships as necessary.

Address standardisation
------------------------

For many organisations, an important element of cleaning your data is
standardising addresses. In the US, this means conform to conventions
defined by the United States Postal Service's Standards for Addresses.
Standardising how addresses are entered into CiviCRM will allow for more
accurate search results when searching by address, as CiviCRM can parse
addresses based on the USPS standards if you choose to do so. To find
out more about how Address Parsing is handled and used in CiviCRM, refer
to the Installation chapter of the Configuration section of this manual.
When adding or editing contacts, you will enter and edit such address
elements as street number, street name, and Apt/Unit/Suite number
according to these standards.

Import Activities
-----------------

When preparing your data import it is helpful to know what fields are
required for Import. You'll want to be sure that these fields are
included in your CSV import file. Below is a list of the required
fields. The Contact ID field is used to cross reference and attach the
activity to the contact so it must match the contact ID of the contact
in the system exactly.

-   Activity Date
-   Activity Type IDs
-   Activity Type Label
-   Contact ID (Match to Contact)
-  Subject

The import tool for Activities is similar to that of contacts, but there
are some pre-requisites which must be met before running the import.
Firstly, Activities cannot be imported unless the contacts and Activity
Types already exist in the database. If you need to import Activities
for contacts that are not yet available, run a contact import first,
preferably including a unique external identifier (most often an ID
assigned by the database or application you are importing records from).

Remember, CSV files must be less than 2MB in size. If the file size
exceeds this, create multiple CSV files and distribute the data between
them.

Import Contributions
--------------------

You can insert new contributions or update existing ones.

If you **insert new contributions,** your CSV file must include at least
the following fields:

-   Contact Id or External Identifier or all the fields used in your
    Unsupervised Duplicate Matching rule (to match to an existing
    contact)
-   Financial Type
-   Total Amount

If you want to **update existing contributions,** your CSV file must
include at least the following fields:

-   Transaction ID or Invoice ID or Payment ID (to match to an existing
    contribution)
-   Financial Type
-   Total Amount

You can use also use **update existing contributions** to import new or
change existing data in other core or custom contribution fields. When
doing this you will still need to include an ID to match to an existing
contribution and the Financial Type and Total Amount fields in you CSV
file, even if the values you import for those fields are no different
from the values already in your database.

Import Memberships
------------------

You can insert new memberships or update existing memberships.

If you **insert new memberships** your CSV file must include at
least the following fields:

-   Contact Id or External Identifier or all the fields used in your
    Unsupervised Duplicate Matching rule (to match to an existing
    contact)
-   Membership Type
-   Membership Start Date

If you want to **update existing memberships** your CSV file must
include at least the following fields:

-   Membership Id (to match to an existing membership)
-   Membership Type
-   Membership Start Date

You can use also use **update existing memberships** to import new or
change existing data in other core or custom membership fields. When
doing this you will still need to include Membership ID to match to an
existing membership, and the Membership Type and Membership Start Date
fields in you CSV file, even if the values you import for those fields
are no different from the values already in your database.

Import Participants
-------------------

In each import session you can either insert new registrations or update
existing participant records.

If you **insert new registrations**you need to decide whether to
restrict registrations for each event to just one per person (set **On
duplicate entries** to **Skip)** or to allow duplicate registrations for
the same event from a given contact (set **On duplicate entries** to
**No Duplicate Checking)**. In either case your CSV file must include
at least the following fields:

-   Contact Id or External Identifier or all the fields used in your
    Unsupervised Duplicate Matching rule (to match to an existing
    contact)
-   Event ID
-   Participant Status

If you want to **update existing registrations,** you should set **On
duplicate entries** to **Update**. Your CSV file must include at least
the following fields:

-   Participant ID (to match to an existing registration)
-   Event ID or Event Title
-   Participant Status

You can use also use **update existing registrations** to import new or
change existing data in custom participant fields. When doing this you
will still need to include Participant ID to match to an existing
registration, and the Event ID or Event Title and Participant Status
fields in you CSV file, even if the values you import for those fields
are no different from the values already in your database.

Import Tags
------------

There is currently no inbuilt way of importing tags or tag sets. You can
use [this advanced
extension](https://civicrm.org/extensions/api-csv-import-gui "API csv Import GUI")
though.

If you want to assign individual tags during your contacts import, you
will have to either:

-   split your CSV file by individual tags and import each subset
    separately as described above,
-   create temporary custom fields and import tags into them as standard
    data, then after the import use advanced searches to isolate
    contacts with particular values and mass tag them. Once you're done,
    you can remove the custom fields.
