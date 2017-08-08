Gestion des tarifications
=====================
Ce chapitre décrit comment configurer la gestion des tarifications afin que vos contacts puissent:
 
-   S'inscrire à plusieurs sortes d'adhésion en même temps.
-   S'inscrire à plusieurs adhésions en une seule transaction (par exemple, adhésions nationales et locales).
-   Sélectionner des options publiques, non membres, telles que les brochures d'information lorsqu'elles souscrivent à une adhésion.

Voici un exemple de la façon dont une tarification d'adhésion, qui offre toutes ces options, peut ressembler:

![image](../img/4.5_membership_price_sets_complete_price_set.PNG) 
 
La tarification **du Club de natation de Donwell Swim** se compose de cinq **champs de tarif** : 
Adhésion à l'association nationale, Adhésion annuelle au club, Clud d'équipement, Billets de tombola et dons.

Il y a deux types d'adhésion possible:

![image](../img/4.5_membership_price_sets_types_1.PNG) 
 
Ces types d'adhésions doivent être définis avant de créer la tarification.
(Voir le chapitre *Définition des adhésions*)..

Vous devez définir tous les types financiers dont vous aurez besoin avant de pouvoir créer une tarification. (Reportez-vous à la section *Contributions* pour obtenir des informations sur les types financiers)

La tarification des adhésions peut être utilisée dans les pages de jointure ou de renouvellement en ligne ou pour les nouvelles inscriptions de membres traitées manuellement via le système de back office CiviCRM. Cependant, vous ne pouvez pas l'utiliser pour des renouvellements qui sont traités manuellement. Chaque adhésion doit être renouvelée individuellement (voir le chapitre *Renouvellements*) et en plus, vous devrez créer un ensemble de prix de contribution composé des éléments non membres que vous proposez. En outre, vous ne pouvez pas combiner des adhésions qui peuvent être renouvelées automatiquement avec des adhésions qui n'offrent pas de renouvellement automatique ou avec des éléments non membres.

Les tarifications peuvent être configurés de plusieurs façons. Vous devez toujours tester un tarif bien défini avant de l'utiliser directement sur votre site afin de vous assurer que vous l'avez configuré de la manière qui vous convient le mieux.

Créer une nouvelle tarification 
------------------------

![image](../img/4.5_membership_price_sets_new_new_price_set_1.PNG) 

1.  Menu **Adhésions> Nouvelle tarification** ou **Administrer > CiviMember> Nouvelle tarification**.
2.  Entrez le nom de cette tarification **Titre**. Ce nom sera affiché à la fois au public dans le cadre du tarif proposé et au personnel administratif lorsqu'il doit choisir entre les ensembles de tarifs. Assurez-vous que le nom soit suffisamment descriptif pour les deux types d'utilisateurs.
3.  Utilisé pour : choisir  **Adhésion**
4.  Définissez le **Type d'opération par défaut** Le choix que vous faites a des implications comptables et vous devez vous référer à la section *Contributions* pour plus d'informations.
5.  Ajoutez un texte d'aide pré ou post-formulaire si vous le souhaitez.
6.  Assurez-vous que cette tarification soit active et **Enregistrer**

Un formulaire  s'affiche ensuite pour créer le premier **Champ de tarif** de votre **tarification**

![image](../img/4.5_membership_price_sets_new_new_price_field_1.PNG) 

### Creation d'un nouveau champ de tarif 

1.  Entrez un nom dans **Intitulé du champ**. Ce nom sera affiché au public. 

2.  Selectionnez **Type de champ de saisie**. Il y a 4 types d'entrée disponibles pour les tarifs

    -   **Quantité/texte numérique:** Permet de définir une unité **Prix**
        Lorsque le jeu de tarif est affiché, il affiche une zone de texte où une quantité peut être saisie. La quantité saisie est multipliée par le prix unitaire pour calculer le montant.
    -   **Selection:** Affiche un menu déroulant où une option peut être sélectionnée.
    -   **Bouton radio:** Affiche plusieurs options dans une liste, une option peut être sélectionnée.    
    -   **Cases à cocher:** Affiche plusieurs options dans une liste. Des sélections multiples sont autorisées.

   Chacun des ces types d'entrée sera utilisé dans un exemple de ce chapitre 

3.  **Type d'opération** : Sera réglé sur **Type financier par défaut** choisi lorsque ce tarif a été créé. Vous pouvez remplacer cette valeur si nécessaire.

4.  **Afficher le montant ?** : Ceci affiche le montant du tarif à côté de l'étiquette. Si votre étiquette de champ inclut le montant, cela peut être décoché. Sinon, il doit rester coché.

5.  **Numéro d'ordre**, **Aide à propos du champ**, **Obligatoire**and **Actif le** Sont suffisament explicites ou ont une aide adéquate fournie sur le formulaire.

6.  **Actif le** et **Expire le**  peuvent être réglés de sorte que le champ de tarif ne soit pas visible jusqu'à la date **Actif le**, et non visible après la date **Expire le** ou n'est que Visible entre les dates ******Actif le** et **Expire le**. *Par exemple, vous pouvez utiliser ces champs pour augmenter le tarif à 12h00 le 1er janvier 2017 en définissant le tarif avec les anciens tarifs à **Expire le** 12/01/2017 12:00 am et le champ de prix avec les nouveaux prix soit **Actif le**  1/12/2017 12:00 am.***

7. **La visibilité** peut être définie sur **Public** (visible sur votre site Web pour ceux qui peuvent voir la page d'inscription de membre) ou **Admin** (visible uniquement en back-end et uniquement pour les utilisateurs avec les autorisations appropriées).

Conditions d'adhésion multiples :...en cours de traduction...!
-------------------------

The configuration for the National Membership price field illustrates
how you can allow contacts to sign up for multiple membership terms at
the same time and shows the **Radio** input field type. 

![image](../img/4.5_membership_price_sets_multi-term_1.PNG) 

In the **Membership Type** field you select the option you want from
a dropdown list of all the membership types you have configured. When
you select a specific membership type the **Number of terms**auto-fills
with 1 and the **Label**, **Amount** and **Financial Type** are
auto-filled based on the definition of that membership type. All those
values can be changed as needed. The National Association Fees
membership type has a duration of 1 year with a minimum fee of $100.
Setting the **number of terms** to 2 will give 2 years of membership.
The **Label** will need to be changed if you have more than one option
as each option must have a different **Label**. The **Amount** can be
can be increased to any value you want. This lets you offer a concession
and standard fee for for the same number of terms. 

As we have not included the price of each option in its **Label** we
would need to have **Display Amount?** ticked.

Defining a price field in this way will reduce the number of membership
types you need to create. You only need a 1 year National Association
membership type with a minimum fee of $100 for this price field instead
of three membership types. However you need to be aware that your
members will not be able to auto-renew if you use this type of
multi-term configuration. 

Membership of more than one organisation
----------------------------------------

In addition to the National Association Fees, contacts are required to
sign up for a membership with the swim club. The **Select** input field
type has been chosen for this field. 

![image](../img/4.5_membership_price_sets_second_organisation_1.PNG) 


Again, when you select a specific membership type from the drop down
list the **Number of terms**auto-fills with 1 and the **Label**,
**Amount** and **Financial Type** are auto-filled based on the
definition of that membership type. You can change any of these values
as desired.

As we have not included the price of each option in its **Label** we
would need to have **Display Amount?** ticked. 

The combination of the two price fields described so far will let
someone sign up for a minimum of 1 and a maximum of 2 memberships.
Remember the two memberships will need to be linked to two different
organisations as a contact can only have one active membership with a
specific organisation. (See the *Defining memberships* chapter for more
information.)

Non-membership Price fields 
-----------------------------

You can also configure price set fields to offer additional services,
subscriptions or other non-membership options. 
 
 There are three non-membership price fields in our example. The first
offers a selection of club branded swimming gear. The **checkbox** field
type lets people choose more than one item from the options offered.

![image](../img/Membership%20Pricesets%20non-member%20field_1.PNG) 

As these are products rather than memberships the **Membership Type**
and **Number of Terms** fields are left empty. You set the **Label**,
**Amount** and **Financial Type** for each option. 

As we have not included the price of each option in its **Label** we
would need to have **Display Amount?**ticked. 

If you look back at the screen shots of the three price fields discussed
so far you should notice that they all contain the same fields even
though are for three different input field types. **Radio** and
**Select** input types are interchangeable, both allow you to choose
just one option and can be used for membership or non-membership
options. **Checkbox**es must be used if your contacts are allowed to
choose more than one option from a single price field. They also can be
used for either membership or non-membership options.

The fourth input field type is **Text/Numeric Quantity** and it can only
be used for non-membership options. With this field type you usually
include the **unit price** of the item on offer in the **field label**
as shown in the following example or in the **field help**. This means
that **Display Amount?** should not be ticked.

![image](../img/4.5_membership_price_sets_raffle_dates_fields_used.PNG)

This will display as:

![image](../img/membership_price_set_raffle_preview_1.PNG)

This price field will only be visible between the **Active On** and
**Expire On**dates and lets us make sure that the raffle tickets can
only be purchased during the selling period authorised by the relevant
licensing authority.

The final price field is configured to allow people to give a donation.
Notice that the **unit price** is 1 and it is not included in in the
field label although the currency symbol is. The **Display Amount?** is
not ticked. This is the best configuration to allow "any amount"
donations. 

![image](../img/4.5_membership_price_sets_donation.PNG)

For review, here again is how all of these fields look on the final
screen:

![image](../img/Membership%20priceset%20final.PNG) 
