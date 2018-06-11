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

Une fois votre feuille de calcul créée, vous pouvez effectuer une opération de fusion et publipostage à l'aide de n'importe quel logiciel de traitement de texte (tel qu'OpenOffice, le logiciel de traitement de texte gratuit) qui insérera les champs souhaités dans la lettre.

CiviCRM peut également créer des étiquettes de publipostage pour vous. Effectuez la même recherche que vous avez utilisée à la section précédente pour créer votre liste de destinataires, puis:

1. Dans le menu déroulant **Actions**, sélectionnez **Étiquettes d'adresse - imprimer**.

2. Sélectionnez le numéro de l'étiquette de publipostage, déterminez si vous souhaitez exclure les personnes dont les options de confidentialité ne sont pas cochées (cochées par défaut et recommandées) et si vous souhaitez fusionner deux enregistrements ayant la même adresse postale en un étiquette. Cette dernière option est très utile lorsque vous envoyez un courrier à un ménage ou une organisation et que vous ne voulez pas qu'ils reçoivent des envois en double. Lorsque les enregistrements sont fusionnés, chaque nom à cette adresse apparaît sur sa propre ligne sur l'étiquette.

3. Cliquez sur **Créer des étiquettes de publipostage** et un document PDF imprimable sera créé.

**!!! Note** : CiviCRM imprime les étiquettes dans l'ordre indiqué sur la page de résultats de recherche dans un modèle colonne par colonne.

