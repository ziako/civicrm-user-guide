Qu'est-ce que CiviContribute?
=======================

CiviContribute est le composant qui vous permet d'enregistrer et d'éditer un compte-rendu sur les contributions financières et en nature à votre organisation. Cela vous permet de:

-  accepter les dons et autres contributions financières ou en nature
-  traiter les inscriptions et les renouvellements de membres
-  gérer les frais des événements.
-  organiser des campagnes de financement spécifiques
-  recueillir des fonds grâce à des pages de campagne personnalisées
-  saisir rapidement les contributions et les paiements d'adhésion en utilisant les "lots"
-  exporter des lots de transactions financières vers votre logiciel de comptabilité
-  faire des compte-rendus et évaluer les résultats et les tendances des collectes de fonds

Dans CiviCRM, nous utilisons le terme *Contribution* pour désigner toute transaction financière ou paiement intervenant dans le cadre de la gestion du système... comme un don, un paiement de frais d'événement, un paiement de cotisation, ou des contributions en nature.

Scenario: Contributing to Leadership
------------------------------------

A community arts group, Arts in Action, conducts leadership workshops for youth under 25 throughout the year. They use CiviCRM extensively in the planning and execution of these workshops, combining the CiviEvent and CiviContribute components to make the administration of the workshops as efficient as possible.

The workshops are funded in three ways: participant fees, local arts
funding, and donations. Most of the donations are from previous workshop
participants who have continued as Arts in Action constituents. Twice a
year a call for donations towards the workshops is sent out using
CiviMail, providing a link to a donations page on the site. Some donors
make recurring donations, while others make one-off donations. A
thank-you email and receipt is automatically sent to every donor when a
payment is successfully processed. All donations are tagged for the
workshops, so that Arts in Action staff can run reports showing total
workshop donations and look at individual contact records to see who has
donated.

Participants register and pay for the workshops via an online form.
There is a flat fee for registration, with additional fees for optional
workshops, food and lodging preferences. The participants make these
choices in the form and pay with a credit card. If they are not already
a contact within the database, a new record is created at the time of
registration, and the payment is recorded in that contact's contribution
record which is also linked to the workshop event.

Arts in Action allows participants to pay later, as many of the
participants do not have a credit card and need to pay in cash at the
workshop. CiviContribute distinguishes between an actual payment and a
commitment to pay, and this information is included in the registrants
report that is printed out and used on the day to check participant
attendance and payment. A computer at the registration desk at the
workshop is used to manually input cash and cheque payments to the
participant's contribution record.

Because Arts in Action has assessed that the most effective publicity
for the workshop is by word of mouth and participants bringing friends,
they also enable participants to forward the registration link to
friends via the "tell-a-friend" mechanism. After completing the
registration form, participants can easily forward it via email or
social networking platforms to their friends and colleagues who may also
be interested in attending.

After every workshop, the Arts in Action accountant generates a report
that shows the total income from each of the three sources for the
workshop, using a report template. She also tracks trends in donations
and ensures that the Board are aware of who the larger donors are. Key
statistics are displayed graphically on staff members' CiviCRM
dashboard.
