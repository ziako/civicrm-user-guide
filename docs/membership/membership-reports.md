Rapports sur les adhésions 
==================

Il existe plusieurs techniques pour obtenir un rapport et analyser vos adhésions.

Le tableau de bord des membres donne un résumé rapide de vos adhésions actuelles, affichant des informations pour chaque type d'adhésion, telles que le total actuel des membres, une ventilation pour le dernier mois, le mois en cours et les totaux de l'année en cours. Vous pouvez également rechercher des détails d'adhésions en utilisant **Recherche avancée** ou **Trouver des membres**. Pour en savoir plus sur le tableau de bord des adhésions et comment utiliser les fonctions de recherche pour trouver une adhésion, consultez le chapitre «Trouver des membres».

Ce chapitre vous montrera comment afficher et créer des rapports d'adhésion ainsi que d'exporter ces informations afin que vous puissiez effectuer d'autres analyses.

Affichage des rapports d'adhésion
--------------------------
CiviCRM est livré avec plusieurs rapports d'adhésions conçus pour vous permettre une analyse de vos adhésions:

![image](../img/membership%20report%20list_1.PNG) 

Le rapport  **Membership Summary** affiche des informations sur les membres regroupés selon une fréquence de date que vous spécifiez, comme le mois, la semaine, le trimestre, l'année. Par exemple, vous pouvez consulter le nombre de membres qui vous ont rejoint chaque mois pendant une période, des types d'adhésion ou toute autre donnée personnalisée que vous collectez à leur sujet.

![image](../img/membership%20summary%20report.PNG)

Si vous cliquez sur un champ en surbrillance, vous verrez le rapport **Membership Detail** correspondant pour cette ligne. Alors cliquez sur **Mai 2015** pour le type d'adhésion **Général** montre:

![image](../img/membership%20detail%20from%20summary%20report.PNG)

Le rapport **Membership Detail** affiche des informations pour chaque fiche d'adhérent en fonction des critères sélectionnés.

![image](../img/membership%20detail%20report.PNG) 
 
Le rapport **Lapsed Memberships** fournit une liste des adhésions qui ont expiré ou seront caduques avant la date que vous avez spécifiée.

![image](../img/membership%20lapsed%20report.PNG) 

Le rapport **Contribution et Membership Details** affiche les informations détaillées des contributions ainsi que les contributions liées à une adhésion en fonction des critères sélectionnés.

![image](../img/membership%20contribution%20report.PNG) 

Creating New Membership Reports
-------------------------------

If you find that you want to create and save new membership reports with
different criteria other than the out-of-the-box membership reports
offer , you can do so by using the membership templates.

-   Click on **Reports > Membership Reports >** click the **New Member
    Report** button
-   On the Create New Report Template screen, click on one of the
    membership report templates, and begin entering your criteria

![image](../img/memberships%20create%20new%20membership%20report_1.JPG)

-   Once you've entered your criteria, click the **Preview Report**
    button to check your results
-   If you like what you see, you can then save this report as a new
    membership report by clicking **Create Report**, then enter the
    information you want to save this as a new membership report.

To learn more about working with reports, see the "Reporting" section.

Exporting membership records
----------------------------

You may decide to export membership records so that you can do more
analysis, perform document mail merges, or create a specific type of
reports outside of CiviCRM. Exporting membership records allows you to
select a default set of primary fields or choose fields that are
specific to the membership record for export.

You will need to first search for the specific membership records you
would like to export. To learn more about how to search for membership
records, refer to the "Finding Memberships" chapter.

To export membership records:

-   Click on **Memberships > Find Members >**, enter your search
    criteria
-   Then on the "Find Members" search results screen, select the records
    you want to import and in **-actions-** drop down, select **Export
    Members**.
-   You can select **Export PRIMARY fields** or **Select fields for
    import ** and click the **CONTINUE** button

![image](../img/memberships%20export%20memberships%20screen.JPG)

-   If you selected **Export PRIMARY fields**, a file called
    CiviCRM_Member_Search.csv will be created containing the
    membership records based on your search criteria
-   If you selected**Select fields for import**, then include the
    fields you would like to export, check the box for **Save this field
    mapping** if you want to re-use this field mapping for a future
    export, then click the**EXPORT** button. A file called
    CiviCRM_Member_Search.csv will be created containing the
    membership records based on your search criteria and the fields you
    selected to export.

![image](../img/memberships%20select%20fields%20to%20export.JPG)
