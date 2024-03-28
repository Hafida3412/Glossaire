# Glossaire

GLOSSAIRE / QUIZ
Ce glossaire est prévu pour valider les connaissances après chaque exercice clé de votre formation. 
L’idée est de réussir à définir les différentes notions en une à 3 phrases maximum et d’adopter le 
vocabulaire technique approprié. Ce document vous servira comme base de révisions.
A chaque fois qu’un acronyme est cité dans le glossaire, il sera impératif de donner la signification 
de chaque lettre initiale.
• Général
• Front-end
• UX / UI
• Programmation orientée objet
• Architecture
• Modélisation / base de données
• Symfony
• Sécurité
• RGPD
• SEO
• Gestion de projets / DevOps
• English
 ##  Général
1) Quel est l’environnement à installer pour exécuter un script PHP ? Citer 2 exemples de logiciels 
permettant ce contexte?
   Pour exécuter un script PHP, il faut installer Laragon ou XAMMPP.

2) Qu’est-ce qu’un algorithme ?
   C'est la description d'une suite d'étapes permettant d'obtenir un résultat à partir d'éléments fournis au départ.
   Exemple: une recette de cuisine est un algorithme permettant d'obtenir un plat à partir d'ingrédients.

3) Qu’est-ce qu’une variable ? Par quel symbole est préfixée une variable en PHP ?
   Une variable est un élément mesurable qui peut prendre différentes valeurs.
   Exemple: taille, âge, poids...

4) Qu’est-ce que la portée d’une variable ?
   La portée d'une variable correspond à l'espace du script dans laquelle elle va être accessible. 

5) Qu’est-ce qu’une constante ? Quelle est la différence avec une variable ?
   Une constante contient toujours la même valeur. A la différence d'une variable qui peut changer ou varier.

6) Qu’est-ce qu’une superglobale, combien en existent-ils et donner un exemple d’utilisation?
   Elles sont écrites en majuscules et commencent toutes par un underscore $_GET et $_POST
   Les superglobales sont toutes des array.
   Ces variables sont automatiquement créées par PHP à chaque fois qu'une page est chargée. Ces variables existent
   sur toutes les pages et sont accessibles partout : au milieu de 
   code, au début, dans les fonctions etc...

8) Quels sont les différents types (primitifs) que l’on peut associer à une variable en PHP ? Les citer 
et en donner des exemples (ne pas oublier le type d’une variable sans valeur)
   Les différents types primitifs que l'on peut associer à une variable en PHP sont:
   null.
   bool.
   int.
   float (nombre à virgule flottante)
   string.
   array.

9) Existe-t-il plusieurs types de tableaux en PHP, si oui lesquels ?
   Il existe 2 types de tabeau:
   - les tableaux à index numériques
   - les tableaux associatifs

10) Quelles sont les différentes structures de contrôles qu’il existe en algorithmie ? Donner un 
exemple pour chacune d’entre elles
  
   - Il existe 3 principales structures de contrôle:
   
   1.Séquence: c'est la structure de base. Les instructions sont exécutées les unes après les autres de manière  
   linéaire.
   -> exemple:
   // Calcul de la somme de deux nombres:
      $a = 3;
      $b = 1;
      $somme = $a + $b;
      echo "La somme est : $somme";

   2.Sélection (ou condition): elle permet de prendre des décisions en fonction des conditions
     -> exemple avec une structure conditionnelle simple:
      // Vérification si un nombre est positif ou négatif
         $nombre = -2;
         if ($nombre >= 0) {
         echo "Le nombre est positif.";
         } else {
         echo "Le nombre est négatif.";
         }

     -> exemple avec une structure conditionnelle alternative (ou “si-sinon”)
     // Vérification si un nombre est pair ou impair
        $nombre = 7;
        if ($nombre % 2 == 0) {
        echo "Le nombre est pair.";
        } else {
        echo "Le nombre est impair.";
        }
   
   3.Répétition (ou boucle): la répétition permet d’exécuter un bloc d’instructions plusieurs fois.
     -> Exemple avec une boucle “tant que” 
     // Affichage des nombres de 1 à 5
        $i = 1;
        while ($i <= 5) {
        echo $i;
        $i++;
        }
    
     -> Exemple avec une boucle “pour” 
     // Affichage des carrés des nombres de 1 à 5
        for ($i = 1; $i <= 5; $i++) {
        $carre = $i ** 2;
        echo "Le carré de $i est : $carre";
        }


11) Quelle est la fonction PHP permettant de demander la longueur d’une chaîne de caractères ?
        $nbCaracteres = strlen($chaineDeCaracteres);

12) Qu’est-ce qu’une session ? Quelle fonction permet de démarrer une session en PHP ? Donner un 
exemple d’utilisation en PHP
    Les sessions permettent de stocker des données individuelles pour chaque utilisateur en utilisant un identifiant de session unique.
    La fonction qui permet de démarrer une session PHP est: session_start()
  
   -> exemple:
    // Démarrer la session
       session_start();

    // Stocker des données dans la session
       $_SESSION['nom'] = 'Jean Dupont';
       $_SESSION['age'] = 35;

    // Récupérer des données de la session
       echo 'Nom : ' . $_SESSION['nom'];
       echo 'Age : ' . $_SESSION['age'];
       ?>


13) Qu’est-ce qu’un cookie ? Donner un exemple d’utilisation en PHP
    C'est un petit fichier que l'on enregistre sur l'ordinateur du visiteur.
    Ce fichier contient du texte et permet d'enregistrer des informations sur le visiteur.

14) Quelle est la différence entre les instructions « require » et « include » en PHP 
    Elles sont utilisées pou inclure des fichiers externes dans un script.
    Lorsque nous utilisons <<include>>, si le fichier n'est pas trouvé, il affiche un avertissement et continue 
    l'exécution du script.
    Lorsque nous utilisons <<require>>, si le fichier n'est pas trouvé, PHP génère une erreur fatale et arrête
    l'exécution du script.
   
15) Comment effectuer une redirection en PHP ?
    Pour que la redirection fonctionne, il faut placer le lien url de la nouvelle page dans le header avant tout code 
    HTML(ou texte) 

16) Définir la partie « front-end » et « back-end » d’une application
    Le "front-end" est la partie d'un site web que les utilisateurs voient.
    Le "back-end" est la partie en arrière plan qui permet de faire fonctionner le "front-end".
 
17) Définir le contrôle de version ? Qu’est-ce que Git ?
    C’est un logiciel qui permet d’enregistrer, de suivre et de gérer plusieurs versions d’un fichier ou d’un code source.
    Il permet d’établir un historique de toutes les modifications effectuées sur un fichier.
    Git est un exemple de logiciel de gestion de versions (Version Control System).

18) Qu’est-ce qu’un CMS ? Citer au moins 2 exemples
    (CMS = Content Management System: système de gestion de contenu)
    Il s'agit d'un logiciel en ligne grâce auquel il est possible de créer, de gérer et de modifier facilement un site 
    web.
    Exemple: WordPress et Shopify
    
 ##  Front-end
1) Définir HTML
  (HyperText Markup Language)
  Il est utilisé afin de créer et de représenter le contenu d'une page web et sa structure.

2) Définir CSS
  (Cascading Style Sheets)
  C'est un langage informatique qui permet de mettre en forme des pages web.

3) Définir Javascript
   C'est un langage de programmation qui permet de créer du contenu de façon dynamique, de contrôler le contenu multimédia,
   d'animer des images...Il est utilisé en complément de HTML et CSS.

4) Définir JSON. Dans quel contexte ce format est-il utilisé ?
   (JavaScript Objet Notation)
   -> Le JSON est un format de texte inspiré de la syntaxe des objets JavaScript.
      Il permet de stocker des données de manière organisée et lisible par les humains.
      Les données sont présentées sous forme de paires clé/valeur.

   -> Le JSON est couramment utilisé pour transmettre des données entre un serveur et un client web.
      Par exemple, lorsque vous consultez une page web, le serveur peut envoyer des données au format JSON pour que 
      votre navigateur puisse les afficher.

6) Peut-on interpréter du Javascript côté serveur ? Si oui, comment ?

7) Qu’est-ce qu’un sélecteur CSS ?
   Les sélecteurs CSS permettent de cibler des éléments HTML présents sur une page web
   pour leur appliquer une règle CSS.

8) Quelle balise HTML permet de créer un lien hypertexte ?
   <a href=".........."</a>
   
9) Qu’est-ce qu’une requête AJAX ?


11) Quel sélecteur CSS permet de sélectionner tous les éléments d’une classe spécifique ? D’un 
identifiant spécifique ?
    Le sélecteur de classe commence par un point . et sélectionne tout élément du document auquel cette classe est appliquée. 
    Un sélecteur d'ID commence par un # , il est utilisé de la même manière qu'un sélecteur de classe.
    En revanche, l'ID ne peut être utilisé qu'une seule fois par document.

13) Définir le responsive design
    Ce design permet de modifier la mise en page d'un site afin que le contenu s'adapte à n'importe quel écran.
    Exemple: smartphone, tablette, ordinateur, TV...

14) Qu’est-ce que le templating ?


15) Qu’est-ce qu’une fonction anonyme en Javascript ?


16) Quelle méthode JavaScript est utilisée pour ajouter un élément à la fin d'un tableau ?
    On utilise la méthode push()
      // Exemple : Initialisation d'un tableau
         let monTableau = [1, 2, 3];

      // Ajout d'un élément à la fin du tableau
         monTableau.push(4);

     // Affichage du tableau mis à jour
        console.log(monTableau); // Affiche [1, 2, 3, 4]


17) Qu’est-ce qu’un « media query » ?
    Le "media query" permet de changer le design d’un site Internet pour qu'il s'adapte à l’écran d'un autre appareil.

18) Qu’est-ce qu’un pseudo élément en CSS ?


19) Qu’est-ce que Bootstrap ? Donner d’autres exemples équivalent


20) Quand un formulaire HTML est créé, quelles sont les 2 méthodes qui peuvent lui être associées ?
Donner la différence entre ces 2 méthodes

 ##  UX / UI
1) Quelle est la différence entre UX Design et UI Design ?
2) Qu’est-ce qu’un wireframe ?
3) Qu’est-ce qu’un prototype ?
4) Qu’est-ce que la hiérarchie visuelle en UI Design ?
5) Qu’est-ce que l’accessibilité en UX Design ?
6) Qu’est-ce qu’une grille de mise en page ?
7) Qu’est-ce que la notion d’affordance en UX Design ?
8) Qu’est-ce qu’un « mobile first design » ?
Programmation orientée objet (POO)
1) Donner une définition de la programmation orientée objet 
2) Qu’est-ce qu’une classe ? Comment la déclare-t-on ?
3) Qu’est-ce qu’un objet ?
4) Définir la notion de propriété / attribut / méthode
5) Qu’est-ce que la visibilité d’une propriété ou d’une méthode ? Citerles différentstypes de visibilité
6) Quelle est la méthode spécifique utilisée pour créer un nouvel objet à partir d’une classe ?
7) Qu’est-ce que l’encapsulation ?
8) Que signifie « étendre une classe » ? Quelle est le concept clé mis en œuvre ? Donner un exemple
9) Définir l’opérateur de résolution de portée
10) Définir une méthode / propriété statique
11) Définir le polymorphisme en POO
12) Définir une méthode / classe abstraite ?
13) Définir le chaînage de méthodes
14) Qu’est-ce que la méthode __toString() ? Existe-t-il d’autres méthodes « magiques »
15) Qu’est-ce qu’un « autoload » ?
16) Comment appelle-t-on en français les « getters » et les « setters » ?
17) Qu’est-ce que la sérialisation en PHP ?

 ##  Architecture 
1) Qu’est-ce que l’architecture client / serveur ? Grâce à quel type de requête peut-on interroger le 
serveur. Définir l’acronyme de ce type de requête. Si on ajoute un « S » à cet acronyme, expliquer 
la différence
2) Donner la définition d’un design pattern. Citer au moins 3 exemples de design pattern
3) Qu’est-ce que l’architecture MVC ?
4) Quel est le rôle de chaque couche du design pattern MVC : Model, View, Controller ?
5) Quels sont les avantages de l’architecture MVC ?
6) Existe-t-il des variantes à l’architecture MVC ?
7) Qu’est-ce qu’une API ? Définir l’architecture REST
Modélisation / Base de données
1) Qu’est-ce que la modélisation de données ? Définir la méthode Merise
2) Quelles sont les 3 étapes principales de la méthode Merise ?
a. Analyse, conception et réalisation
b. Planification, exécution et contrôle
c. Création, modification et suppression
3) Qu’est-ce qu’un modèle conceptuel de données (MCD) en Merise ?
4) Qu’est-ce qu’un modèle logique de données (MLD) en Merise ?
5) Donner la définition des mots suivants :
a. Entité
b. Relation
c. Cardinalité
d. Clé primaire / clé étrangère
6) Que devient une relation de type « Many To Many » dans le modèle logique de données ?
7) Qu’est-ce qu’une base de données ?
8) Définir les notions suivantes :
a. SQL
b. MySQL
c. SGBD (donner 2 exemples de SGBD)
9) Dans une base de données, les données sont stockées dans des ___. Celles-ci sont constituées de 
lignes appelées ___ et de colonnes appelées ___
10) Quelle est la différence entre une base de données relationnelle et non relationnelle ?
11) Qu’est-ce qu’une jointure dans une base de données ? En existe-t-il plusieurs ? Si oui lesquelles ?
12) A quoi sert une vue dans une base de données ?
13) Qu’est-ce que l’intégrité référentielle dans une base de données ?
14) Quelles sont les fonctions d’agrégation en SQL ?
15) Qu’est ce qu’un CRUD dans le contexte d’une base de données ?
16) Quelles sont les clauses qui permettent de :
a. Insérer un nouvel enregistrement dans une table
b. Modifier un enregistrement dans une table
c. Supprimer un enregistrement dans une table
d. Supprimer la base de données
e. Filtrer les résultats d’une requête SQL
f. Trier les résultats d’une requête SELECT
g. Regrouper les résultats d'une requête SELECT en fonction d'une colonne spécifique
h. Concaténer 2 chaînes de caractères 
17) Comment se connecter à une base de données en PHP ? Quelle est la classe native utilisée ?

 ## Symfony
1) Qu’est-ce que Symfony ?
2) Sur quel langage de programmation et design pattern repose Symfony ?
3) Quelle est la dernière version en date de Symfony ?
4) Qu’est-ce qu’un bundle ?
5) Quel est le moteur de template utilisé par défaut dans Symfony ?
6) Qu’est-ce qu’un ORM ? Quel est son utilité et comment s’appelle-t-il au sein de Symfony ?
7) Qu’est-ce que l’injection de dépendances ? Quel est l’outil utilisé dans ce contexte et quel fichier 
contient l’intégralité des dépendances du projet ?
8) Que permet le bundle Maker au sein de Symfony ?
9) Quel est le langage de requêtage exploité au sein d’un projet Symfony ?
10) Quel est le composant qui garantit l’authentification et l’autorisation des utilisateurs ?
Sécurité
1) Qu’est-ce que l’injection SQL ? Comment s’en prémunir ?
2) Qu’est-ce que la faille XSS ? Comment s’en prémunir ?
3) Qu’est-ce que la faille CSRF ? Comment s’en prémunir ?
4) Définir l’attaque par force brute et l’attaque par dictionnaire
5) Existe-t-il d’autres failles de sécurité ? Citer celles-ci et expliquer simplement leur comportement
6) A quoi servent l’authentification et l’autorisation dans un contexte d’application web ?
7) Définir la notion de hachage d’un mot de passe et citer des algorithmes de hachage
8) Qu’est-ce qu’une politique de mots de passe forts ?
9) Qu’est-ce que l’hameçonnage ?
10) Définir la « validation des entrées »
    
 ## RGPD
1) Qu’est-ce que le RGPD ?
2) Quel est son objectif principal ?
3) Quelle est la date d’entrée en vigueur du RGPD ?
4) Quelles sont les sanctions possibles en cas de non-respect du RGPD ?
5) En France, quel est l’autorité administrative qui s’occupe de faire appliquer le RGPD ?
6) Quel est le consentement valide selon le RPGD ?
7) Qu’est-ce qu’une politique de confidentialité ?
8) Quelle est la durée de conservation maximale des données personnelles selon le RGPD ?
9) Quels sont les droits des utilisateurs selon le RGPD ?
10) Qu’est-ce que le principe de minimisation des données selon le RGPD ?

 ## SEO
1) Qu’est-ce que le SEO ?
2) Quel est l’objectif principal du SEO ?
3) Existe-t-il plusieurs types de référencement ? Lesquels ?
4) Qu’est-ce que la densité de mots-clés en SEO ?
5) Qu’est-ce qu’une balise « alt » ?
6) Qu’est-ce que la balise « meta description » ?
7) Qu’est-ce que le « nofollow » en SEO ?
8) Quelle est l'importance du contenu de qualité pour le référencement d'un site web ?
9) Pourquoi est-il important d'utiliser des balises de titre (h1, h2, h3, etc.) de manière structurée ?
10) Quelle est la recommandation pour les URL d'un site web bien référencé ?
11) Qu'est-ce que le maillage interne et pourquoi est-il important pour le référencement ?
12) Qu'est-ce que l'optimisation des images pour le référencement ?
13) Qu'est-ce qu'un plan de site (sitemap) et pourquoi est-il important pour le référencement ?
Gestion de projets / DevOps
1) Qu’est-ce que la gestion de projet ?
2) Qu’est-ce qu’une méthode Agile de gestion de projet ?
3) Expliquer la méthode MoSCoW en quelques lignes et citer ses avantages
4) A quoi sert la méthodologie MVP ? Citer les caractéristiques clés
5) Qu’est-ce que la planification itérative ?
6) Citer 3 méthodes Agiles dans le cadre d’un projet informatique
7) Qu’est-ce qu’une réunion de revue de projet ?
8) Qu’est-ce qu’un livrable dans un projet ?
9) Quels sont les 3 piliers SCRUM ? Définir chacun d’entre eux
10) Qu’est-ce que le DevOps et quel est son objectif principal ?
11) Qu’est-ce que l’intégration continue ?
12) Qu’est-ce que Docker ? Et en quoi est-il utile dans le cadre du DevOps ?
13) Qu’est-ce qu’un test unitaire ?
14) Quelle est l'unité de code testée lors d'un test unitaire ?
15) Quelles sont les caractéristiques d'un bon test unitaire ?
16) Qu'est-ce qu'une assertion dans un test unitaire ?

 ## English
1) What does JavaScript enable you to do on a website ?
a. Add interactive behavior and dynamic content
b. Define the layout and design of web pages
c. Handle server-side operations
2) Which programming language is primarily used for server-side web development ?
a. PHP
b. JavaScript
c. HTML
3) What is the purpose of a web browser ?
a. To render and display web pages
b. To execute serve-side code
c. To manage databases
4) What is the difference between GET and POST methods in HTTP ?
a. GET retrieves data from a server, while POST submits data to a server
b. GET submits data to a server, while POST retrieves data from a server
c. GET and POST methods are interchangeable
5) What is the purpose of version control systems (e.g., Git) in web development ?
a. To track changes and manage collaborative development
b. To optimize website loading speed
c. To handle server-side scripting
6) What is the purpose of a framework in web development ?
a. To provide a structured environment for building web applications
b. To handle network protocols and data transfer
c. To create visual designs and layouts for websites
7) What does NoSQL stand for ?
a. Not Only SQL
b. Non-Structured Query Language
c. New Object-Oriented Language
8) Which of the following is a characteristic of NoSQL databases ?
a. Strict schema enforcement
b. Support for complex transactions
c. Scalability and flexible data models
