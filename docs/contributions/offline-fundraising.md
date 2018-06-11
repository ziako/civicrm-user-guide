# Levée de fonds hors ligne

Votre organisation peut recueillir des dons lors d'événements, de campagnes ou solliciter des dons par courrier postal et d'autres méthodes hors ligne. Tout l'argent collecté via des activités hors ligne doit être saisi manuellement dans CiviCRM afin de garantir que le rapport final soit exact.

Dans CiviCRM la collecte de fonds hors ligne comprend trois étapes: la création de vos listes, la création de vos publipostages et [la saisie manuelle des contributions](../contributions/manual-entry-of-contributions).


## Créer vos listes

Ce processus est assez simple si vous connaissez les capacités de recherche de CiviCRM.

Allez à **Recherche> Trouver des contacts** pour créer une liste d'enregistrements qui par exemple seront appellés par téléphone. (il peut s'agir éventuellement de l'ensemble de votre base de données).

Si vous souhaitez suivre l'efficacité d'un publipostage ou recevoir certains appels, enregistrez les résultats de la recherche en tant que groupe. Utilisez la case à cocher pour tout sélectionner et choisissez l'option appropriée dans le menu déroulant **Action** : **Groupe - ajouter des contacts** ou **Groupe - créer un groupe intelligent**. Par la suite, vous pourrez marquer tous les membres de ce groupe comme destinataires de cette action en utilisant l'option **Ajouter une activité** dans le menu déroulant **Actions**.

Si vous voulez créer des lettres pour des envois postaux, vous pouvez le faire en utilisant la fonction interne **Lettres PDF - impression** de CiviCRM. Vous pouvez aussi exporter la liste sous forme de fichier CSV et utiliser la fusion dans un traitement de texte.

Pour exporter une liste:

1. Sélectionnez tous les enregistrements ou un sous-ensemble à l'aide des cases à cocher et dans le menu déroulant **Actions**, choisissez **Exporter les contacts**.
2. Choisissez d'exporter **les champs PRIMARY** ou **Sélectionnez les champs à exporter**. Si vous choisissez d'exporter les champs primaires, le fichier CSV sera immédiatement généré lorsque vous cliquerez sur **Continuer**. Si vous choisissez de sélectionner les champs que vous souhaitez exporter, cliquez sur **Continuer** et une liste des options déroulantes s'affichera.
3. Sélectionnez les champs requis. Si vous souhaitez enregistrer la liste des champs exportés en tant que mappage d'exportation pour une utilisation ultérieure, cochez la case **Enregistrer ce mappage de champ**.
4. Cliquez sur **Export** pour générer le fichier CSV.
5. Cliquez sur **OK** lorsque vous avez terminé pour revenir à la liste de contacts.


## Création de mailings postaux


Once you spreadsheet is created, you can do a mail merge using any word
processing software (such as OpenOffice, the free software word
processor) that will insert any fields you want in the letter.

CiviCRM can also create mailing labels for you. Perform the same search
you used in the previous section to create your list of recipients,
then:

1.  From the **Actions** dropdown menu, select **Mailing
    labels - print**.
2.  Select the mailing label number, determine whether you want to
    exclude people with "do not mail" checked in their privacy options
    (checked by default and recommended), and whether you want to merge
    two records that have the same mailing address into one label. This
    last option is very useful when you are mailing a household or
    organization and you don't want them to receive duplicate mailings.
    When the records are merged, each name at that address appears on
    its own line on the label.
3.  Click **Make Mailing Labels** and a printable PDF document will be
    created.

Note that CiviCRM prints labels in the order shown on the research results page
in a column-by-column pattern.
