

## Sommaire

Structure du document
Scénario/Énoncé du problème

Présentation de l’état Power BI Desktop

Tâche 1 : configurer Power BI Desktop dans l’environnement de labo

Tâche 2 : analyser l’état Power BI Desktop

Tâche 3 : examiner les requêtes Power Query

Références

## Structure du document
Le labo comprend des étapes à suivre par l’utilisateur, ainsi que des captures d’écran associées qui fournissent une aide visuelle. Dans chaque capture d’écran, des sections sont mises en évidence avec des encadrés orange afin de souligner la ou les zones sur laquelle/lesquelles l’utilisateur doit se concentrer.
Remarque : certaines captures d’écran peuvent être obsolètes en raison des mises à jour produit en cours.

## Scénario/Énoncé du problème
Fabrikam, Inc. est un grossiste en produits innovants. Ses clients sont majoritairement des sociétés qui revendent aux particuliers. Fabrikam vend à des clients de détail à travers les États-Unis, notamment des magasins spécialisés, des supermarchés, des magasins d’informatique et des magasins d’attractions touristiques. Fabrikam vend également à d’autres grossistes au moyen d’un réseau d’agents qui font la promotion des produits au nom de Fabrikam. Bien que tous les clients de Fabrikam soient actuellement basés aux États-Unis, la société a l’intention de favoriser son expansion dans d’autres pays/régions.

Vous êtes analyste de données au sein de l’équipe commerciale. Vous recueillez, nettoyez et interprétez des jeux de données pour résoudre des problèmes métier. Vous créez également des visualisations telles que des tableaux et des graphiques, rédigez des états et les présentez aux décideurs de l’organisation.

Afin de tirer de précieux insights des données, vous extrayez les données de plusieurs systèmes, les nettoyez et les agrégez.

   •	Données Sales : proviennent du système ERP et sont stockées dans une base de données ADLS Gen2. Elles sont mises à jour au quotidien à midi.

   •	Données fournisseur : proviennent de différents fournisseurs et les données sont stockées dans une base de données Snowflake. Elles sont mises à jour au quotidien à minuit.

   •	Données client : proviennent de Customer Insights et les données sont stockées dans Dataverse. Les données sont systématiquement à jour.

   •	Données collaborateur : proviennent du système RH ; elles sont stockées sous forme de fichier d’exportation dans un dossier SharePoint. Elles sont mises à jour tous les matins à 9 h.

Vous créez actuellement un jeu de données dans Power BI Premium qui extrait les données des systèmes sources ci-dessus pour répondre à vos besoins en matière de reporting et fournir un libre-service aux utilisateurs finaux. Vous mettez à jour votre modèle à l’aide de Power Query. 

Vous êtes confronté aux défis suivants :

   •	Vous devez actualiser votre jeu de données au moins trois fois par jour pour tenir compte des différentes heures de mise à jour des différentes sources de données.

   •	Vos actualisations prennent beaucoup de temps, car vous devez effectuer chaque fois une actualisation complète pour capturer toutes les mises à jour survenues sur les systèmes sources.

   •	Toute erreur dans l’une des sources de données à partir desquelles vous extrayez des données entraîne une interruption de l’actualisation de votre jeu de données. Il arrive souvent que le fichier collaborateur ne soit pas chargé à temps, ce qui aboutit à une interruption de l’actualisation de votre jeu de données.
 
   •	Apporter des modifications à votre modèle de données est un processus chronophage, car Power Query prend beaucoup de temps pour actualiser vos aperçus, compte tenu du gros volume de données et des transformations complexes. 

   •	Vous avez besoin d’un PC Windows pour utiliser Power BI Desktop, même si le standard de l’entreprise est Mac.

Vous avez entendu parler de Microsoft Fabric et décidé de l’essayer pour voir s’il peut relever vos défis.

## Présentation de l’état Power BI Desktop

Avant de prendre en main Fabric, examinons l’état actuel dans Power BI Desktop pour comprendre les transformations et le modèle.

### Tâche 1 : configurer Power BI Desktop dans l’environnement de labo

1. 	Ouvrez le fichier FAIAD.pbix situé dans le dossier Reports sur le Bureau de votre environnement de labo. Le fichier s’ouvre alors dans Power BI Desktop.

2. 	La boîte de dialogue Entrez votre adresse e-mail s’ouvre alors. Accédez à l’onglet Détails de l’environnement sur le volet droit dans l’environnement de labo.

3. 	Copiez la valeur Informations d’identification du champ Nom d’utilisateur et collez-la dans la zone de texte E-mail de la boîte de dialogue.

4. 	Cliquez sur Continuer.

5. 	La boîte de dialogue Se connecter s’ouvre alors. Saisissez à nouveau la valeur Informations d’identification du champ Nom d’utilisateur en la copiant depuis l’onglet Détails de l’environnement.

6. 	Cliquez sur Suivant.

7. 	Dans la boîte de dialogue suivante, saisissez la valeur Informations d’identification du champ Mot de passe en la copiant depuis l’onglet Détails de l’environnement.

8. 	Cliquez sur Se connecter.




