Relations entre contacts
=============

CiviCRM vous permet de représenter les connexions entre les contacts en créant des relations. Exemple, si une mère et son fils sont tous les deux dans votre base de données, il peut être utile de pouvoir regarder l'un ou l'autre des dossiers et voir qu'ils sont liés l'un à l'autre.

Vous pouvez également suivre les relations entre les organisations, ou entre les contacts individuels et les organisations. Par exemple, la saisie d'une organisation dans le domaine de l'employeur actuel de l'enregistrement d'un contact individuel crée automatiquement une relation «employé de l'individu à l'organisation", et une relation «employeur de l'organisation à l'individu".

Creating relationships between contacts
---------------------------------------

![image](../img/4.5%20Add%20Relationship.png)

1. Accédez à l'un des enregistrements que vous souhaitez relier.
2. Cliquez sur **Ajouter une relation** dans le bouton **Actions** du résumé de contact ou dans l'onglet Relations
3. Sélectionnez le type de relation. Dans ce cas, ce serait soit «Enfant de» ou «Parent de».
4. Commencez à saisir le nom de famille de la ou des personne(s) concernée(s). Si le contact que vous souhaitez connecter n'existe pas encore dans la base de données, vous pouvez créer un nouveau contact à partir de cet écran.
5. Vous pouvez également saisir des informations supplémentaires, notamment la date de début et la date de fin (dans le cas où la relation est limitée dans le temps), la description et les notes. Il existe également deux options d'autorisation, qui permettent aux utilisateurs de la base de données de modifier cet enregistrement. Enfin, la zone Activé, qui est cochée par défaut, indique que la relation est active, .
6. Lorsque vous avez effectué les modifications souhaitées, cliquez sur **Enregistrer la relation**.

Relier les employés et les employeurs
-------------------------------------

Une façon rapide de relier les employés (qui sont stockés dans CiviCRM en tant qu'individus) aux employeurs (stockés en tant qu'organisations) consiste à utiliser le champ Employeur actuel dans le dossier d'une personne. Cela définira le champ employeur actuel dans l'enregistrement de contact et créer une relation entre les contacts.

1. Accédez à l'enregistrement de l'individu que vous souhaitez connecter à une organisation.
2. Cliquez sur le bouton Modifier pour modifier l'enregistrement de l'individu.
3. Commencez à taper le nom de l'organisation dans le champ Employeur actuel. Au fur et à mesure que vous tapez, les noms correspondants des organisations qui existent déjà en tant que contacts dans CiviCRM apparaissent dans une liste déroulante de saisie semi-automatique sous le champ Employeur actuel. Si l'organisation est déjà un contact dans CiviCRM, vous pouvez la sélectionner dans la liste déroulante en appuyant sur la flèche vers le bas ou en cliquant dessus. Si l'organisation n'existe pas déjà en tant que contact CiviCRM, entrez simplement le nom complet de l'organisation.
4. Une fois que le nom complet de l'organisation est entré dans le champ Employeur actuel, appuyez sur la touche Entrée ou cliquez sur le bouton Enregistrer. Si l'organisation est un contact préexistant, une relation Employé / Employeur sera créée entre le particulier et l'organisation. Si l'organisation n'existe pas déjà, un nouveau contact d'organisation sera créé et la relation sera créée entre l'individu et l'organisation. Vous pouvez cliquer sur l'onglet Relations pour afficher votre relation nouvellement créée et voir les relations existantes.

Ajout de contacts aux organisations
-----------------------------------

1. Sélectionnez les contacts souhaités dans vos résultats de recherche comme décrit ci-dessus.
2. Sélectionnez **Ajouter une relation - à l'organisation dans le menu déroulant** dans le menu Actions.
3. Dans l'écran **Ajouter des contacts à l'organisation**, sélectionnez **Type de relation** dans le menu déroulant.
4. Entrez une partie du nom de l'organisation souhaitée dans le champ **Rechercher l'organisation cible**, puis cliquez sur **Rechercher**.
5. Les organisations qui correspondent à votre recherche apparaîtront dans la zone **Marquez les contacts cibles pour cette relation** située sous les boutons Rechercher et Annuler. Si l'organisation que vous recherchez apparaît dans cette liste, cliquez sur le bouton radio en regard de cette organisation, puis cliquez sur le bouton **Ajouter à l'organisation** ci-dessous. Si l'organisation que vous recherchez n'apparaît pas dans cette liste, essayez d'entrer quelque chose de différent dans le champ **Trouver une organisation cible** et de cliquer sur **Rechercher** à nouveau. Si vous ne parvenez toujours pas à trouver votre organisation souhaitée, elle peut ne pas exister. Cliquez sur **Annuler**, ajoutez une nouvelle organisation et réessayez.
6. Une fois que vous avez choisi une organisation et cliquez sur le bouton **Ajouter à l'organisation**, vous devriez voir un message indiquant que le nombre de participants que vous avez sélectionné a été ajouté à l'organisation.
7. Cliquez sur **Terminé** pour revenir aux résultats de votre recherche.

Ajout de contacts aux ménages
-----------------------------

1. Sélectionnez les contacts souhaités dans vos résultats de recherche comme décrit ci-dessus.
2. Sélectionnez **Ajouter une relation - au ménage** dans le menu déroulant **Actions**.
3. Sélectionnez le **Type de relation** dans le menu déroulant. Notez que si CiviCRM ne vous empêche pas d'ajouter plusieurs contacts comme **chef de ménage** pour un seul ménage, cela peut causer des problèmes plus tard dans toute situation où vous attendez **chef de ménage** de se référer à un seul Par ménage. Par conséquent, l'option **membre du ménage de** peut être le meilleur choix dans la plupart des situations.
4. Entrez une partie du nom du ménage auquel vous ajoutez des contacts (tel qu'un nom de famille partagé par les membres du ménage) dans le champ **Rechercher ménage cible**, puis cliquez sur **Rechercher**.
5. Les ménages qui correspondent à votre recherche apparaîtront dans la zone **Marquez les contacts cibles pour cette relation** située sous les boutons Rechercher et Annuler. Si le ménage que vous recherchez apparaît dans cette liste, cliquez sur le bouton radio en regard de ce ménage, puis cliquez sur le bouton **Ajouter au ménage** ci-dessous. Si le ménage que vous recherchez n'apparaît pas dans cette liste, essayez d'entrer quelque chose de différent dans le champ **Rechercher un ménage cible** et de cliquer **Recherche** à nouveau. Si vous ne trouvez toujours pas le ménage désiré, il peut ne pas exister. Cliquez sur le bouton **Annuler**, ajoutez un nouveau ménage et réessayez.
6. Une fois que vous avez choisi un ménage et cliqué sur le bouton **Ajouter au ménage**, vous devriez voir un message indiquant que le nombre de participants que vous avez sélectionné a été ajouté au ménage.
7. Cliquez sur **Terminé** pour revenir aux résultats de votre recherche.

Création de nouveaux types de relations
---------------------------------------


-----Traduction en cours ------


CiviCRM comes with a set of common relationship types that can be
    used to indicate relationships between contacts. If you need to
    track different types of relationships between your contacts, you
    can create your own custom relationship types.

1.  In the navigation menu, go to: **Administer > Customize Data and
    Screens > Relationship Types**.
2.  Review the list of existing relationship types to ensure that you
    are not creating a duplicate.
3.  If the relationship type you need does not already exist, click the
    **New Relationship Type** button.
4.  Enter descriptive labels for the relationship type you are creating
    in the **Relationship Label-A to B** and **Relationship Label-B to A**
    fields. The **Relationship Label-A to B** field describes the
    relationship between Contact A and Contact B; the **Relationship
    Label-B to A** field describes the relationship between Contact B and
    Contact A.  
      -  Some relationships can be described by the same label in both
    directions; in these cases you can enter the Relationship Label once
    in the **Relationship Label-A to B** field. For example, when
    describing the relationship between two domestic partners named
    Sylvia and Audre, you can say that Sylvia is the "Partner of" Audre
    and Audre is the "Partner of" Sylvia. Therefore you would enter the
    "Partner of" label only in **Relationship Label-A to B** field,
    leaving the **Relationship Label-B to A** field blank.
      -  In other situations one Relationship Label cannot be applied in both
    directions; in these cases you need to enter different Relationship
    Labels in each of the Relationship Label fields. For example, you
    can say that Kiyoshi is the "Grandparent of" Yuki but you cannot say
    that Yuki is the "Grandparent of" Kiyoshi. Therefore you would enter
    the "Grandparent of" label in the **Relationship Label-A to B** field
    and either "Grandchild of" or "Grandparent is" in the **Relationship
    Label-B to A** field.
7.  Use the **Contact Type A** and **Contact Type B** fields to designate which
    contact types are being linked by your relationship. Remember to
    check that the contact types you select for Contact A and Contact B
    make sense when corresponded to your Relationship Labels.
8.  Optionally enter **Description** for this relationship type. This is
    especially useful if the intended purpose of this relationship type
    may not be obvious to other users.
9.  Leave the **Enabled** box checked unless you intend to create this
    relationship type but not allow users to utilise it until a future
    date.
10. Click **Save**. You will see a message telling you that the relationship
    type has been saved and you will see your new Relationship Type in
    the list below.


Disabling or deleting unneeded relationship types
-------------------------------------------------

If an existing relationship type is no longer useful or relevant for
your organisation you can either disable or delete it so it is no longer
presented as an option for new relationships. Disabling rather than
deleting the relationship type has two significant advantages: you will
still be able to see existing data on relationships of this type, and
you can easily enable the relationship type again should you find you
need it later.

1.  In the navigation menu, go to: **Administer > Option Lists >
    Relationship Types**.
2.  Click the **More** link in the row of the relationship type that you'd
    like to disable or delete.
3.  Select either **Disable** or **Delete** from the pop-up menu.
4.  If you select Disable, a pop-up confirmation bubble will appear. If
    you select Delete, you will be directed to an additional screen that
    provides a more serious warning and requests confirmation. Review
    the information provided in either confirmation message and if you
    are sure you'd like to complete this action, click the **Delete**
    button otherwise **Cancel**.
5.  If you have chosen to disable the relationship type it will appear
    in red in the Relationship Types list and relationships of this type
    will still be visible when viewing contacts. If you have chosen to
    delete the relationship type it will no longer appear in the
    Relationship Types list or in contact relationships data. In either
    case users will no longer be able to create new relationships of
    this type.
6.  To enable a previously disabled relationship type, follow steps 1
    and 2 above and select **Enable** from the **more** pop-up menu.
