Automatiser les tâches
======================

Si vous vous retrouvez à répéter régulièrement les mêmes procédures de gestion dans votre organisation, CiviCRM peut très certainement vous libérer du temps. Automatiser des tâches administratives ou de routine, plus communément appelées processus, est un peu délicat à mettre en place, mais vous fera gagner énormément de temps sur le long term.
Pour commencer, soyez conscient que chaque décision de process peut être prise selon un jeu de critères plus ou moins satisfaits. Nous vous aiderons à réfléchir à la définition de ces critères qui pourraient être utilisés par CiviCRM pour réaliser des opérations répétitives. Ensuite, nous devrons rechercher dans le système les informations testées par ces critères, puis indiquer à CiviCRM les actions à réaliser en conséquence.

En voici un exemple :

> *Objectif*: Automatiser les lettres de remerciement pour un don
>
> *Questions centrales*: Quelles lettres dois-je éditer et quelles informations doivent y apparaitre ? Où puis-je trouver ces informations ? Quelles fonctionnalités de CiviCRM peuvent accomplir cette tâche ?
>
> *Stratégie*: Créer des champs de fusion personnalisés et utiliser la fonction de création de documents PDF de CiviCRM.
>
> *Champs personnalisés*: Fund Name, Tag “Works with Organization,” Tax Receipt Pull-Down (No Tax Receipt, Extra Tax Receipt to Soft Credit, Tax Receipt to Hard Credit), Relationship “Known by Organization Staff”
>
> *Champs existants*: Thank You Letter Sent, Soft Credit
>
> *Champs de fusion personnalisés*: First Gift Date, Financial Type, Soft Credit Address and Main Contact
>
> *Variations en language "Modèle de document"*:
>
> -   Include/Exclude Fund Name - basé sur le fait qu'il s'agisse d'une donation au fonds ou d'une donation générique ;
> -   Include/Exclude Tax Receipt - basé sur le fait que le don donne droit, ou non, à un reçu fiscal ;
> -   Include/Exclude Invitation for Sponsorship - basé sur le fait que le donateur est, ou non, un sponsor de l'organisation ;
> -   Include/Exclude Invitation to Visit Office - basé sur l'adresse du donateur. Si ce dernier est géographiquement proche des locaux de l'organisation, lui envoyer une invitation.

L'objectif indique la tâche de routine que vous souhaitez automatiser. Par exemple, cela peut être :

-   M'envoyer un rapport quotidien par courriel des principaux dons faits à l'organisation ;
-   Envoyer un rappel par courriel aux personnes inscrites à un événement la veille de ce dernier ;
-   Envoyer une notification de renouvellement à toute personne dont l'adhésion est sur le point d'expirer.

CiviCRM a la possibilité de faire tout cela clé en main (pour en savoir plus, vous pouvez vous référer aux chapitres sur les composants CiviCRM concernés). Il est également possible d'automatiser des tâches plus complexes avec un minimum de personnalisation.

Les réponses aux questions centrales demandent de la reflexion et de la recherche.

Answering focus questions will require reflection and research. As an
expert in what you do, try to articulate what piece of information helps
you realize that this person, donation or organization deserves
different treatment. Maybe this individual is personally known by
someone at your organization, maybe this donation requests a unique
language in their acknowledgment letter, maybe this volunteer only wants
to hear about opportunities to support a particular program.

When you make the decision to give someone or something different
treatment, do you have to hunt down any additional information? For
example, do you have to find a spouse's name or the address of someone's
company? Write out what pieces of information you add or what language
you change. If you are familiar with writing conditional statements,
try explaining your decision making process in the following format:

*If the Spouse Name field is not empty, include spouse name in the line
address*

*If last contribution amount is greater than $10,000 and City is within
the Zip Code Range 94110 to 94114, include as the last line in the
opening paragraph: "It looks like you're in the neighborhood. Would you
enjoy stopping by the office to speak more about our work and meet the
staff?"*

CiviCRM has myriad features that can be used to help you automate simple
tasks. Sometimes the hardest part is finding them. The case studies
available on civicrm.org can introduce you to how other organizations
are using CiviCRM and subsequent chapters in this book describe what
features are available and how you can start using them. If you are
poking around the CiviCRM interface, the small speech bubbles can also
be a great source for more information on the capabilities each field
offers. To create a complicated workflow, you will ultimately want to
tie several of these features together.

You will most likely have to create custom fields and custom tokens in
order to accomplish your goal. Once you have planned what task you want
to automate and how, create custom fields from the Administrator
Console. Create custom fields carefully. It's always easy to choose a
text field, but they can be impossible to use later in reports or
searches because everyone enters information differently. It's better to
create fields that have pre-defined answers so spelling mistakes are not
an issue. CiviCRM along with any computer program is great at executing
on the basis of well defined facts. They aren't as good at comparing two
facts that look the same, even if the difference is only one letter in a
differently spelled word. You might also be tempted to create several
Yes/No radio buttons to capture a set of facts that might work better as
a drop down menu.

To be a good database manager, you don't have to understand everything
about relational databases. It can, however, be helpful to understand
your system's underlying structure in order to understand some of the
consequences related to that structure.

For example, you might wonder why you can't create a friend relationship
between two organizations. The organizations might be partners, but if
the database was told to only recognize the relationship type "friend"
between two individuals, that constraint on the database will not let
you freely use relationship "friend" for organizations. A fix to that
relationship definition will fix the problem but people are often
tempted to find a workaround for a problem rather then actually fix the
problem. We strongly recommend looking into the reasons why something
doesn't work for you and addressing the problem at its root instead of
applying a "patch".

CiviCRM comes with multiple pre-defined reports that should cover most
of your needs, but more complicated searches may require creating custom
reports. You may hesitate to hire a professional to create a proper
report to search your specific criteria, but if you are currently
copying/pasting information to spreadsheets, you may consider this one
time expense worthwhile in the long run.

In general, our advice is to have high expectations of your CiviCRM (and
other software) and automate as much of your manual work into the system
as you can to free yourself from daunting administrative activities that
computers can do faster and more accurately.
