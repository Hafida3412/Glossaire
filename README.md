# Glossaire

##  GLOSSAIRE / QUIZ
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

1) __Quel est l’environnement à installer pour exécuter un script PHP ? Citer 2 exemples de logiciels 
permettant ce contexte?__
   Pour exécuter un script PHP (Hypertext Preprocessor), il faut installer Laragon ou XAMPP(Cross-platform, Apache, MySQL, PHP et Perl).

2) __Qu’est-ce qu’un algorithme?__
   C'est un ensemble d'instructions pour résoudre un problème ou effectuer une tâche, semblable à une recette de cuisine pour obtenir un résultat précis.
  
3) __Qu’est-ce qu’une variable ? Par quel symbole est préfixée une variable en PHP ?__
   Une variable est un élément mesurable qui peut prendre différentes valeurs.
   Exemple: taille, âge, poids...Une variable est préfixée par le symbole: $

4) __Qu’est-ce que la portée d’une variable ?__
   La portée d'une variable correspond à l'espace du script dans laquelle elle va être accessible. 

5) __Qu’est-ce qu’une constante ? Quelle est la différence avec une variable ?__
   Une constante contient toujours la même valeur. A la différence d'une variable qui peut changer ou varier.

6) __Qu’est-ce qu’une superglobale, combien en existent-ils et donner un exemple d’utilisation?__
   Les superglobales $_GET et $_POST sont comme des boîtes où PHP garde les informations envoyées depuis un formulaire sur une page web.
   $_GET récupère les données visibles dans l'URL de la page, tandis que $_POST récupère les données invisibles envoyées de manière sécurisée.
   Et ces boîtes sont disponibles partout dans le code pour que vous puissiez utiliser ces informations comme vous le souhaitez.

8) __Quels sont les différents types (primitifs) que l’on peut associer à une variable en PHP ? Les citer 
   et en donner des exemples (ne pas oublier le type d’une variable sans valeur)__
   Les différents types primitifs que l'on peut associer à une variable en PHP sont:
   null.
   bool.
   int.
   float (nombre à virgule flottante)
   string.
   array.

9) __Existe-t-il plusieurs types de tableaux en PHP, si oui lesquels ?__
   Il existe 2 types de tabeau:
   - les tableaux à index numériques
   - les tableaux associatifs

10) __Quelles sont les différentes structures de contrôles qu’il existe en algorithmie ? Donner un 
exemple pour chacune d’entre elles__
  
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


11) __Quelle est la fonction PHP permettant de demander la longueur d’une chaîne de caractères ?__
    La fonction PHP permettant de demander la longueur d’une chaîne de caractères est strlen().
        Exemple:
        $chaine = "Hello!";
        $longueur = strlen($chaine);
        echo "La longueur de la chaîne est : " . $longueur;

12) __Qu’est-ce qu’une session ? Quelle fonction permet de démarrer une session en PHP ? Donner un 
exemple d’utilisation en PHP__
   Une session en PHP permet de stocker des informations sur un utilisateur et de les rendre disponibles sur toutes les pages
   d'un site web durant sa visite. 
   Cela permet de conserver l'état entre différentes pages web.
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


12) __Qu’est-ce qu’un cookie ? Donner un exemple d’utilisation en PHP__
    C'est un petit fichier que l'on enregistre sur l'ordinateur du visiteur.
    Ce fichier contient du texte et permet d'enregistrer des informations sur le visiteur.

    En PHP, on peut créer un cookie en utilisant la fonction setcookie(). Par exemple, voici comment on pourrait créer un cookie pour stocker
    le nom de l'utilisateur pendant une session :
    
   -> Exemple:
   
   // Définition du nom
    $name = "John Doe";

    // Création du cookie
    setcookie("user_name", $name, time() + 3600, "/");

    echo "Cookie créé avec succès!";


13) __Quelle est la différence entre les instructions « require » et « include » en PHP__
    Elles sont utilisées pour inclure des fichiers externes dans un script.
    Lorsque nous utilisons <<include>>, si le fichier n'est pas trouvé, il affiche un avertissement et continue l'exécution du script.
    Lorsque nous utilisons <<require>>, si le fichier n'est pas trouvé, PHP génère une erreur fatale et arrête l'exécution du script.
    <<require>> est généralement utilisé pour les fichiers essentiels, tandis qu'include est utilisé pour les fichiers optionnels.


14) __Comment effectuer une redirection en PHP ?__
    Pour que la redirection fonctionne, il faut placer le lien url de la nouvelle page dans le header avant tout code 
    HTML(ou texte) 

15) __Définir la partie « front-end » et « back-end » d’une application__
    Le "front-end" est la partie d'un site web que les utilisateurs voient.
    Le "back-end" est la partie en arrière plan qui permet de faire fonctionner le "front-end".
 
16) __Définir le contrôle de version ? Qu’est-ce que Git ?__
    C’est un logiciel qui permet d’enregistrer, de suivre et de gérer plusieurs versions d’un fichier ou d’un code source.
    Il permet d’établir un historique de toutes les modifications effectuées sur un fichier.
    Git est un exemple de logiciel de gestion de versions (Version Control System).

17) __Qu’est-ce qu’un CMS ? Citer au moins 2 exemples__
    (CMS = Content Management System: système de gestion de contenu)
    Il s'agit d'un logiciel en ligne grâce auquel il est possible de créer, de gérer et de modifier facilement un site web.
    Exemple: WordPress et Shopify


 ##  Front-end

1) __Définir HTML__
  (HyperText Markup Language)
  Il est utilisé afin de créer et de représenter le contenu d'une page web et sa structure.

2) __Définir CSS__
  (Cascading Style Sheets)
  C'est un langage informatique qui permet de mettre en forme des pages web.

3) __Définir Javascript__
   C'est un langage de programmation qui permet de créer du contenu de façon dynamique, de contrôler le contenu multimédia,
   d'animer des images...Il est utilisé en complément de HTML et CSS.

4) __Définir JSON. Dans quel contexte ce format est-il utilisé ?__
   (JavaScript Objet Notation)
   -> Le JSON est un format de texte inspiré de la syntaxe des objets JavaScript.
      Il permet de stocker des données de manière organisée et lisible par les humains.
      Les données sont présentées sous forme de paires clé/valeur.

   -> Le JSON est couramment utilisé pour transmettre des données entre un serveur et un client web.
      Par exemple, lorsque vous consultez une page web, le serveur peut envoyer des données au format JSON pour que votre navigateur puisse les afficher.

5) __Peut-on interpréter du Javascript côté serveur ? Si oui, comment ?__
   Oui, on peut utiliser JavaScript sur des ordinateurs serveurs grâce à un outil appelé Node.js.
   Node.js est comme un super programme qui aide les ordinateurs à comprendre et à exécuter JavaScript sans avoir besoin d'un navigateur web,
   ce qui permet de créer des sites web et des applications qui fonctionnent sur des serveurs.

6) __Qu’est-ce qu’un sélecteur CSS ?__
   Les sélecteurs CSS permettent de cibler des éléments HTML présents sur une page web pour leur appliquer une règle CSS.

7) __Quelle balise HTML permet de créer un lien hypertexte ?__
   <a href=".........."</a>
   
8) __Qu’est-ce qu’une requête AJAX ?__
  AJAX permet de demander des informations au serveur sans recharger la page, rendant les mises à jour plus rapides et fluides.
  Cela rend les applications web plus interactives et améliore l'expérience utilisateur sans interruption.

 9) __Quel sélecteur CSS permet de sélectionner tous les éléments d’une classe spécifique ? D’un 
identifiant spécifique ?__
    Le sélecteur de classe (.) sélectionne tous les éléments avec cette classe.
    Le sélecteur d'ID (#) fonctionne de la même manière mais ne peut être utilisé qu'une seule fois par document.

10) __Définir le responsive design__
    Ce design permet de modifier la mise en page d'un site afin que le contenu s'adapte à n'importe quel écran.
    Exemple: smartphone, tablette, ordinateur, TV...

11) __Qu’est-ce que le templating ?__
    Le templating permet de créer des pages web contenant des informations variables en utilisant des modèles pré-définis.
    Cela permet de gagner du temps et de rendre le processus d'affichage de données plus flexible et automatisé.

12) __Qu’est-ce qu’une fonction anonyme en Javascript ?__
    C'est une fonction sans nom.
    Exemple: (function () {
    // ... code à exécuter ici ...
      });
    Elle est pratique pour exécuter du code qui n’est utilisé qu’à un seul endroit dans notre script et qui ne sera pas réutilisé ailleurs.
    Elle permet de gagner du temps et de rendre notre code plus clair en évitant d’encombrer l’espace avec des noms inutiles.

13) __Quelle méthode JavaScript est utilisée pour ajouter un élément à la fin d'un tableau ?__
    On utilise la méthode push()
      // Exemple : Initialisation d'un tableau
         let monTableau = [1, 2, 3];

      // Ajout d'un élément à la fin du tableau
         monTableau.push(4);

     // Affichage du tableau mis à jour
        console.log(monTableau); // Affiche [1, 2, 3, 4]


14) __Qu’est-ce qu’un « media query » ?__
    Le "media query" permet de changer le design d’un site Internet pour qu'il s'adapte à l’écran d'un autre appareil.

15) __Qu’est-ce qu’un pseudo élément en CSS ?__
    Un pseudo-élément en CSS est un mot-clé ajouté à un sélecteur qui permet de mettre en forme certaines parties de l’élément ciblé.
    Par exemple, le pseudo-élément ::first-line permettra de ne cibler que la première ligne d’un élément visé par le sélecteur.
    
16) __Qu’est-ce que Bootstrap ? Donner d’autres exemples équivalent__
   C'est un outil qui permet de créer rapidement des sites web adaptatifs/responsive en fournissant des composants et des styles prédéfinis.
   Cela simplifie grandement la conception et la mise en page des pages web.
    Exemples équivalents:
   - Foundation : un autre framework de développement web populaire
   - Materialize : un framework basé sur le design Material de Google
   - Bulma : un framework CSS moderne et léger

17) __Quand un formulaire HTML est créé, quelles sont les 2 méthodes qui peuvent lui être associées ?
Donner la différence entre ces 2 méthodes.__
- La méthode GET envoie les données dans l'URL, donc elles sont visibles. Elle sert à lire des données.
- La méthode POST envoie les données dans le corps de la requête, donc elles sont cachées. Elle sert à créer ou modifier des données sensibles.

 
 ##  UX / UI

1) __Quelle est la différence entre UX Design et UI Design ?__
- L'UX Design concerne l'expérience globale de l'utilisateur avec un produit ou service.
- L'UI Design se concentre sur l'apparence visuelle de l'interface.
Les deux sont essentiels pour un produit numérique réussi.

2) __Qu’est-ce qu’un wireframe ?__
Un wireframe est un plan visuel simple d'un site web ou d'une interface, utilisé pour organiser les éléments avant la conception et le développement.
Il montre l'emplacement des images, textes, boutons et liens, aidant à visualiser la disposition et l'expérience utilisateur.
Exemple: Figma

3) __Qu’est-ce qu’un prototype ?__
Un prototype UX/UI est une maquette interactive utilisée pour tester et améliorer le design d'une application ou d'un site web avant son développement complet.
Il permet de visualiser l'interface, recueillir des retours des utilisateurs et identifier les problèmes potentiels pour améliorer l'expérience utilisateur.

4) __Qu’est-ce que la hiérarchie visuelle en UI Design ?__
La hiérarchie visuelle en UI design organise les éléments visuels pour guider l'œil de l'utilisateur, mettre en avant ce qui est important et faciliter la navigation.
Elle repose sur la taille, la couleur, le contraste et l'espacement des éléments pour créer une structure claire et une expérience utilisateur agréable.

5) __Qu’est-ce que l’accessibilité en UX Design ?__
L'accessibilité en UX Design consiste à créer des produits numériques utilisables par tous, y compris les personnes handicapées.
Cela implique de considérer les besoins spécifiques de chaque utilisateur pour assurer une expérience optimale.
L'objectif est de rendre les produits faciles à utiliser pour tout le monde.

6) __Qu’est-ce qu’une grille de mise en page ?__
C'est un système de lignes qui organisent l'espace graphique et facilitent la création de designs équilibrés et harmonieux en guidant le positionnement
des éléments visuels comme le texte et les images. Elle est largement utilisée dans le design web, l'édition de magazines, la publicité, etc.

7) __Qu’est-ce que la notion d’affordance en UX Design ?__
L'affordance en UX Design signifie qu'un produit montre comment il peut être utilisé.
Par exemple, un bouton cliquable indique qu'on peut l'actionner.
Les affordances aident à créer une expérience utilisateur intuitive et efficace.

8) __Qu’est-ce qu’un « mobile first design » ?__
Le "mobile first design" signifie concevoir un site web en commençant par la version mobile, puis l'adapter pour les écrans plus grands comme
les tablettes et les ordinateurs. Cela assure une bonne expérience utilisateur sur les petits écrans d'abord.

 ## Programmation orientée objet (POO)

1) __Donner une définition de la programmation orientée objet__
  Cela signifie que dans la programmation orientée objet, on regroupe des informations (comme la couleur d'une voiture) et des actions (comme démarrer)
  dans des boîtes appelées objets. Chaque objet a ses propres caractéristiques et actions spécifiques. Cette organisation facilite la gestion et la compréhension
  du code, car tout est regroupé de manière logique. Cela permet également de réutiliser plus facilement et efficacement le code existant.

2) __Qu’est-ce qu’une classe ? Comment la déclare-t-on ?__
Une classe en POO est comme une boîte à outils qui contient des outils (attributs) et des actions que tu peux faire avec ces outils (méthodes).

class Personne { // propriétés de la classe public $nom; public $prenom; public $age;
// constructeur de la classe
public function __construct($nom, $prenom, $age) {
    $this->nom = $nom;
    $this->prenom = $prenom;
    $this->age = $age;
}

// méthode de la classe
public function afficherInfos() {
    echo "Nom : " . $this->nom . "<br>";
    echo "Prénom : " . $this->prenom . "<br>";
    echo "Age : " . $this->age . "<br>";
}
}

//instancier un objet de la classe Personne $personne1 = new Personne("Doe", "John", 30);

// appeler la méthode afficherInfos pour afficher les informations de la personne $personne1->afficherInfos();

3) __Qu’est-ce qu’un objet ?__
Une classe est un modèle pour créer des objets. Un objet est une instance de cette classe, avec des attributs (données) et
des méthodes (fonctions). Par exemple, une classe "Voiture" peut créer un objet "voiture1" avec des attributs comme
la couleur et des méthodes comme démarrer.

4) __Définir la notion de propriété / attribut / méthode__
En programmation orientée objet, les propriétés stockent des informations sur un objet, les attributs décrivent l'objet en détail et les méthodes sont des actions
que l'objet peut effectuer.

5) __Qu’est-ce que la visibilité d’une propriété ou d’une méthode ? Citer les différents types de visibilité__
La visibilité d'une propriété ou d'une méthode d'une classe en programmation détermine si celle-ci peut être accédée depuis l'extérieur de la classe.
Les différents types de visibilité sont :
- Public : la propriété ou la méthode peut être accédée depuis n'importe quel endroit dans le programme, que ce soit à l'intérieur ou à l'extérieur de la classe.
- Protected : la propriété ou la méthode peut être accédée à l'intérieur de la classe où elle est déclarée, ainsi que dans les classes héritées de celle-ci.
- Private : la propriété ou la méthode ne peut être accédée que depuis l'intérieur de la classe où elle est déclarée. Les classes héritées de cette classe ne peuvent pas y accéder.

6) __Quelle est la méthode spécifique utilisée pour créer un nouvel objet à partir d’une classe ?__
Par exemple, dans une classe "Personne", on pourrait définir un constructeur comme suit :
public class Personne {
    private String nom;
    private int age;
    // Constructeur de la classe Personne
    public Personne(String nom, int age) {
        this.nom = nom;
        this.age = age;
    }
    // Autres méthodes de la classe Personne
}
Lorsqu'un nouvel objet "Personne" est créé en utilisant ce constructeur, les valeurs passées en paramètres seront utilisées pour initialiser les propriétés "nom" et "age" de l'objet.

7) __Qu’est-ce que l’encapsulation ?__
L'encapsulation, c'est comme mettre des données et des actions dans une boîte verrouillée. On ne peut accéder ou modifier ces données qu'en utilisant
des clés spécifiques (méthodes), ce qui protège les données et contrôle les changements.

8) __Définir l’opérateur de résolution de portée__
L'opérateur de résolution de portée "::" permet d'accéder aux membres d'une classe ou d'un objet depuis une autre partie du programme.
Il aide à organiser le code et éviter les conflits en appelant des fonctions ou variables spécifiques d'une classe.

9) __Définir une méthode / propriété statique__
Les méthodes ou propriétés statiques sont des outils spécifiques à une classe qui peuvent être utilisés sans avoir à créer un objet de cette classe.
Ils sont communs à toutes les instances de la classe et peuvent être appelés directement en utilisant le nom de la classe.

10) __Définir le polymorphisme en POO__
Cela signifie qu'une méthode peut avoir des implementations différentes dans différentes classes, ce qui facilite l'écriture de code sans avoir à connaître la classe exacte de l'objet.

11) __Définir une méthode / classe abstraite ?__
Une méthode abstraite n'a pas de corps et doit être définie dans les classes héritées, tandis qu'une classe abstraite contient au moins une méthode abstraite
et sert de modèle pour d'autres classes.

12) __Qu’est-ce que la méthode__ __toString() ? Existe-t-il d’autres méthodes « magiques »__
La méthode __toString() permet de définir comment un objet doit se comporter lorsqu'il est converti en chaîne de caractères en POO.
Elle est appelée automatiquement dans certains cas.

Il existe d'autres méthodes magiques en POO, telles que ____construct()__ pour le constructeur de la classe, __ __destruct()__ pour le destructeur,  ____get()__ et __ __set()__ pour la surcharge des accesseurs, etc. 
Ces méthodes sont appelées automatiquement dans certaines circonstances spécifiques.

13) __Qu’est-ce qu’un « autoload » ?__
L'autoload est une fonctionnalité qui charge automatiquement les classes ou fichiers nécessaires pour un programme, évitant ainsi de devoir les inclure
manuellement à chaque utilisation. Cela simplifie le développement et rend le code plus clair et facile à gérer.

14) __Comment appelle-t-on en français les « getters » et les « setters » ?__
On appelle les « getters » des « accesseurs » et les « setters » des « mutateurs ».

15) __Qu’est-ce que la sérialisation en PHP ?__
La sérialisation en PHP consiste à transformer des données compliquées en une simple chaîne de caractères pour les stocker ou les envoyer plus facilement.
La désérialisation consiste à reconvertir cette chaîne en données d'origine.

 
 ##  Architecture 

1) __Qu’est-ce que l’architecture client / serveur ? Grâce à quel type de requête peut-on interroger le 
serveur. Définir l’acronyme de ce type de requête. Si on ajoute un « S » à cet acronyme, expliquer la différence.__
L'architecture client/serveur répartit les tâches entre un serveur central et des clients qui utilisent ses services. Les requêtes HTTP sont utilisées
pour interroger le serveur, avec l'acronyme GET pour obtenir des informations. Une version sécurisée de cette requête, GETS, implique une connexion HTTPS
pour plus de sécurité.

2) __Donner la définition d’un design pattern. Citer au moins 3 exemples de design pattern__
Un design pattern est une solution réutilisable à un problème courant rencontré lors de la conception de logiciels.
Il s'agit d'un modèle de conception qui fournit des directives sur la façon de résoudre un problème de manière efficace et structurée.

Trois exemples de design pattern couramment utilisés sont:
- Le pattern Singleton: Il garantit qu'une classe ne peut avoir qu'une seule instance et fournit un point d'accès global à cette instance.
- Le pattern Observer: Il permet à un objet de surveiller les changements d'état d'un autre objet et d'être notifié en cas de modification.
- Le pattern Factory: Il définit une interface pour créer des objets dans une classe, mais laisse aux sous-classes le soin de spécifier les types d'objets à créer.

3) __Qu’est-ce que l’architecture MVC ?__
L'architecture MVC (Modèle-Vue-Contrôleur) est un modèle de conception utilisé dans le développement de logiciels.
Il divise une application en trois composants : le modèle, qui gère les données, la vue, qui affiche les données à l'utilisateur,
et le contrôleur, qui traite les actions de l'utilisateur et met à jour le modèle.
Cette séparation des responsabilités permet de rendre le code plus modulaire, maintenable et évolutif.

4) __Quel est le rôle de chaque couche du design pattern MVC : Model, View, Controller ?__
- Le modèle (Model) : C'est la couche qui représente les données de l'application et la logique métier. Elle traite les requêtes et les modifications des données.
- La vue (View) : C'est la couche qui affiche les données au utilisateur et gère l'interface graphique de l'application.
- Le contrôleur (Controller) : C'est la couche qui fait le lien entre le modèle et la vue. Il récupère les requêtes de l'utilisateur, traite les données en conséquence,
et décide quelle vue afficher.

5) __Quels sont les avantages de l’architecture MVC ?__
L'architecture MVC permet de séparer clairement les différents éléments d'une application : le modèle qui représente les données, la vue qui affiche ces données
à l'utilisateur et le contrôleur qui gère les interactions entre le modèle et la vue.
Cela facilite la maintenance, la réutilisation du code et la collaboration entre les développeurs.
De plus, cela permet une meilleure organisation du code et une plus grande flexibilité dans le développement de l'application.

6) __Existe-t-il des variantes à l’architecture MVC ?__
Oui, il existe des variantes à l'architecture MVC, telles que MVVM (Modèle-Vue-VueModèle) et MVP (Modèle-Vue-Présentateur).

7) __Qu’est-ce qu’une API ? Définir l’architecture REST__
Une API est comme un langage commun que les différents logiciels utilisent pour se parler et échanger des informations.
Exemple: pour un groupe de personnes qui parlent différentes langues : une API est comme un traducteur qui permet à tout le monde de se comprendre.

L'architecture REST est une manière spécifique d'organiser et de structurer une API. Elle utilise des URLs pour identifier les informations et des commandes simples 
(GET, POST, PUT, DELETE) pour les manipuler. C'est comme un menu avec des plats différents (les informations) et des instructions simples pour les commander (GET, POST, PUT, DELETE).

L'API est le langage commun, et REST est une façon spécifique de l'organiser pour faciliter la communication entre les logiciels.


## Modélisation / Base de données

1) __Qu’est-ce que la modélisation de données ? Définir la méthode Merise1__
La modélisation de données est le processus de création de modèles qui représentent la manière dont les données sont organisées et
structurées dans une base de données. La méthode Merise est une approche de modélisation de données qui consiste à diviser le processus
en trois étapes principales :
- le modèle conceptuel des données,
- le modèle logique des données et
- le modèle physique des données.
Ces modèles permettent de décrire de manière claire et précise la structure des données et les relations entre elles.

2) __Quelles sont les 3 étapes principales de la méthode Merise ?__
a. Analyse, conception et réalisation
b. Planification, exécution et contrôle
c. Création, modification et suppression

3) __Qu’est-ce qu’un modèle conceptuel de données (MCD) en Merise ?__
Le MCD est un schéma clair qui montrent comment les données sont liées entre elles. Il décrit les entités(=objets), 
leurs propriétés (=données) et leurs relations. C'est une base de travail avant de créer une base de données.

4) __Qu’est-ce qu’un modèle logique de données (MLD) en Merise ?__
Un modèle de données est comme un plan ou un schéma qui montre comment sont organisées et interconnectées les informations dans un système.
Il indique quels sont les éléments (entités) présents, comment ils sont liés les uns aux autres (relations), quelles sont les caractéristiques de
ces éléments (attributs), et quelles sont les règles ou contraintes à respecter pour ces données.
Cela aide à organiser et gérer les données de manière efficace.

5) __Donner la définition des mots suivants :__
a. Entité
 C'est comme un petit dossier où vous pouvez ranger des informations similaires. 
 -> exemple: l'entité "clients"contiendrait des info telles que le nom, l'adresse... 

b. Relation
 Elle permet de lier 2 entités. Elle porte un nom, c'est généralement un verbe.

c. Cardinalité
  Les cardinalités définissent les relations entre les entités. Ce sont des couples de valeurs exprimées sous forme de 
  nombre(0, 1, n)

d. Clé primaire / clé étrangère
1.La clé primaire est utilisée pour identifier de manière unique chaque ligne dans une table de base de données.
2.La clé étrangère permet de récupérer des données de plusieurs tables en même temps.

6) __Que devient une relation de type « Many To Many » dans le modèle logique de données ?__
Une relation de type "Many To Many" devient une table de liaison supplémentaire dans le modèle logique de données.

7) __Qu’est-ce qu’une base de données ?__
   C'est un endroit où on peut stocker et organiser des informations de manière structurée.
   C'est comme une grande bibliothèqte numérique où on peut ranger des livres (=données) pour les retrouver facilement plus tard. 

8) __Définir les notions suivantes :__
a. SQL
   Structured Query Language: « langage de requêtes structurées »
   Il permet de :
   -> Rechercher, ajouter, modifier ou supprimer des données dans les bases de données relationnelles.
   -> Créer et modifier l’organisation des données dans la base de données.
   -> Commencer et terminer des transactions.
   -> Autoriser ou interdire l’accès à certaines données pour certaines personnes.


b. MySQL
   -> MySQL est un système de gestion de bases de données relationnelles (RDBMS).
   -> Il implémente le standard SQL et permet de stocker des données dans des tables.
   -> MySQL est open source et est souvent utilisé dans les applications web.
   -> Il est disponible pour différentes plateformes telles que Linux, Microsoft Windows, Mac OS X et Solaris.
  
   SQL est le langage utilisé pour travailler avec les données dans les bases de données, tandis que MySQL est un produit 
   de base de données qui met en œuvre ce langage.
   MySQL est souvent privilégié pour sa rapidité et son efficacité dans les applications nécessitant des performances élevées

c. SGBD (donner 2 exemples de SGBD) = Systèmes de Gestion de Bases de Données
   -> MySQL
   -> Oracle

Dans une base de données, les données sont stockées dans des TABLES (chaque table représente un type d'entité: exemple: table de commandes). Celles-ci sont constituées de 
lignes appelées ENREGISTREMENT (=lignes dans une table) et de colonnes appelées ATTRIBUTS (=colonne dans une table)

9) __Quelle est la différence entre une base de données relationnelle et non relationnelle ?__
Les bases de données relationnelles utilisent des tables liées par des clés étrangères et suivent un modèle qui assure la fiabilité des transactions (appelé ACID).
Les bases de données non relationnelles sont plus flexibles, faciles à faire évoluer et adaptées pour gérer des informations désorganisées. Elles sont également
meilleures pour obtenir rapidement des résultats fiables.

10) __Qu’est-ce qu’une jointure dans une base de données ? En existe-t-il plusieurs ? Si oui lesquelles ?__
Une jointure dans une base de données est une opération qui permet de combiner des données provenant de deux tables différentes en fonction d'une condition commune entre les deux. Il existe plusieurs types de jointures, les principales sont :

- Jointure interne : Elle ne renvoie que les lignes des tables qui ont une correspondance dans les deux tables.
- Jointure externe : Elle renvoie les lignes des tables, même celles qui n'ont pas de correspondance dans l'autre table.
- Jointure gauche : Elle renvoie toutes les lignes de la table de gauche et les lignes correspondantes dans la table de droite.
- Jointure droite : Elle renvoie toutes les lignes de la table de droite et les lignes correspondantes dans la table de gauche.

11) __A quoi sert une vue dans une base de données ?__
Une vue dans une base de données montre les données de façon organisée et facilite leur manipulation. On peut restreindre l'accès à certaines informations
en cachant des champs ou en filtrant les lignes selon des critères spécifiques.

12) __Qu’est-ce que l’intégrité référentielle dans une base de données ?__
L'intégrité référentielle en base de données consiste à s'assurer que les liens entre les différentes tables sont respectés.
Par exemple, si une table contient une clé étrangère qui fait référence à une clé primaire dans une autre table, il est important que la valeur de
la clé étrangère corresponde toujours à une valeur existante dans la clé primaire. Cela permet d'éviter les erreurs et les incohérences dans les
données de la base de données.

13) __Quelles sont les fonctions d’agrégation en SQL ?__
En SQL, les fonctions d'agrégation sont utilisées pour calculer des valeurs sur un ensemble de données, comme la somme, la moyenne, le maximum ou le minimum.
Elles aident à résumer les données d'une table en fonction de critères spécifiques, comme regrouper les ventes par mois ou par catégorie, en les combinant avec
la clause GROUP BY.

14) __Qu’est ce qu’un CRUD dans le contexte d’une base de données ?__
Le terme CRUD est un acronyme pour Create, Read, Update et Delete. Il fait référence aux opérations de base que l'on peut effectuer sur une base de données :
créer des données, lire des données, mettre à jour des données et supprimer des données.

15) __Quelles sont les clauses qui permettent de :__
a. __Insérer un nouvel enregistrement dans une table__
On utilise généralement la clause __INSERT INTO__. On spécifie le nom de la table dans laquelle on veut insérer les données, puis on précise les valeurs à insérer
dans chaque colonne de la table.
Par exemple :
INSERT INTO nom_table (colonne1, colonne2, colonne3) VALUES (valeur1, valeur2, valeur3);
Cette requête permet d'ajouter un nouvel enregistrement dans la table "nom_table" en spécifiant les valeurs à insérer dans les colonnes "colonne1", "colonne2" et "colonne3".

b. __Modifier un enregistrement dans une table__
Pour modifier un enregistrement dans une table, il faut utiliser la clause SQL "UPDATE" suivie du nom de la table et des colonnes que l'on souhaite modifier. 
Ensuite, on utilise la clause "SET" pour spécifier les nouvelles valeurs pour chaque colonne. 
On peut également ajouter une clause "WHERE" pour spécifier les enregistrements à modifier en fonction de certaines conditions.

c. __Supprimer un enregistrement dans une table__
Il faut utiliser la clause __DELETE FROM__ suivi du nom de la table et de la clause __WHERE__ pour spécifier les critères de suppression. 
Par exemple, DELETE FROM table_nom WHERE condition_de_suppression.

d. __Supprimer la base de données__
Il existe deux types de clauses pour supprimer une base de données:
- Clauses __DROP DATABASE__ : Ces clauses permettent de supprimer complètement une base de données et tous ses objets (tables, index, procédures stockées, etc.).
- Clauses __DROP TABLE__ : Ces clauses permettent de supprimer uniquement une table spécifique de la base de données, sans supprimer la base de données elle-même.

e. __Filtrer les résultats d’une requête SQL:__
-> on utilise les clauses __WHERE__ et __HAVING__.

- La clause __WHERE__ permet de spécifier des critères de sélection pour les lignes à récupérer dans une table. Par exemple, on peut filtrer les résultats en définissant une condition comme "WHERE nom = 'Dupont'".

- La clause __HAVING__ permet de filtrer les résultats d'une requête qui contient une fonction d'agrégation comme SUM, AVG, COUNT, etc.
Par exemple, on peut utiliser la clause HAVING pour filtrer les résultats en spécifiant une condition sur le résultat d'une fonction d'agrégation
comme __"HAVING SUM(quantite) > 100"__.

f. __Trier les résultats d’une requête SELECT__
Pour trier les résultats d'une requête SELECT, on utilise la clause __ORDER BY__. 
Cette clause permet de spécifier sur quelle colonne ou ensemble de colonnes les résultats doivent être triés, et aussi dans quel ordre (croissant ou décroissant). 
Par exemple, ORDER BY nom ASC triera les résultats par ordre alphabétique croissant du champ nom.

g. __Regrouper les résultats d'une requête SELECT en fonction d'une colonne spécifique__
Pour regrouper les résultats d'une requête SELECT en fonction d'une colonne spécifique, on utilise la clause __GROUP BY__ dans la requête SQL. 
Cette clause permet de spécifier la colonne sur laquelle on souhaite regrouper les données. 
Une fois regroupées, on peut utiliser des fonctions d'agrégation comme COUNT, SUM, AVG, etc. pour obtenir des informations sur les groupes de données.

h. __Concaténer 2 chaînes de caractères__ 
Pour concaténer deux chaînes de caractères, vous pouvez utiliser l'opérateur de concaténation "+" qui permet de les mettre bout à bout. 
Par exemple, si vous avez deux chaînes "Bonjour" et "monde", en les concaténant avec l'opérateur "+", vous obtiendrez la chaîne "Bonjourmonde".

16) __Comment se connecter à une base de données en PHP ? Quelle est la classe native utilisée ?__
Exemple : abstract class Connect{

    const HOST = "localhost";
    const DB = "cinema_hafida";
    const USER = "root";
    const PASS = "";

   public static function seConnecter(){
        try{
            return new \PDO( //la barre "\" devant PDO indique au framework que PDO est une classe native et non une classe du projet
                "mysql:host=".self::HOST.";dbname=".self::DB.";charset=utf8",
                self::USER,
                self::PASS
            );
        }
            catch(\PDOException $ex){
            return $ex->getMessage();  
}
}
}

 ## Symfony

1) __Qu’est-ce que Symfony ?__
Symfony est un outil gratuit en PHP pour créer des sites web plus facilement et plus rapidement. Il offre des fonctionnalités prêtes à l'emploi pour
simplifier le développement et la maintenance des projets web.

2) __Sur quel langage de programmation et design pattern repose Symfony ?__
Symfony repose sur le langage de programmation PHP et utilise principalement le design pattern MVC (Modèle-Vue-Contrôleur).

3) __Quelle est la dernière version en date de Symfony ?__
La dernière version en date de Symfony est la version 5.4.

4) __Qu’est-ce qu’un bundle ?__
Un bundle Symfony est un ensemble de fichiers contenant du code réutilisable pour organiser et partager des fonctionnalités dans une application Symfony.
Cela permet de structurer le code et de le réutiliser entre différentes applications.

5) __Quel est le moteur de template utilisé par défaut dans Symfony ?__
Le moteur de template utilisé par défaut dans Symfony est Twig.

6) __Qu’est-ce qu’un ORM ? Quel est son utilité et comment s’appelle-t-il au sein de Symfony ?__
L'ORM (Object-Relational Mapping) est un outil qui relie une base de données à un langage de programmation objet.
Doctrine est l'ORM principal utilisé dans Symfony pour simplifier la manipulation des données en les représentant sous forme d'objets PHP.

7) __Qu’est-ce que l’injection de dépendances ? Quel est l’outil utilisé dans ce contexte et quel fichier 
contient l’intégralité des dépendances du projet ?__
L'injection de dépendances, c'est donner à un objet les éléments dont il a besoin plutôt que de les créer à l'intérieur.
Cela rend le code plus facile à lire et à modifier. Spring Framework est un outil très utilisé en Java pour gérer ce processus.
Dans un projet Spring, le fichier applicationContext.xml est utilisé pour définir les objets (beans) et les éléments dont ils ont besoin (leurs dépendances)
pour que l'injection de dépendances fonctionne correctement.

9) __Que permet le bundle Maker au sein de Symfony ?__
Le bundle Maker de Symfony permet de créer rapidement des éléments de code comme des entités, des contrôleurs et des formulaires, ce qui facilite le développement
en automatisant des tâches récurrentes.

10) __Quel est le langage de requêtage exploité au sein d’un projet Symfony ?__
Symfony utilise le langage SQL pour les requêtes dans un projet, mais grâce à Doctrine, il est possible de manipuler les données de la base de données en utilisant
des objets PHP plutôt que du SQL directement.

11) __Quel est le composant qui garantit l’authentification et l’autorisation des utilisateurs ?__
Le composant qui garantit l'authentification et l'autorisation des utilisateurs est un système de gestion des identités, souvent abrégé en
IAM (Identity and Access Management). Ce système permet de vérifier l'identité des utilisateurs, de gérer leurs droits d'accès à différents systèmes et ressources,
et de garantir la sécurité des informations sensibles.

## Sécurité

1) __Qu’est-ce que l’injection SQL ? Comment s’en prémunir ?__
L'injection SQL est une attaque informatique qui utilise du code malveillant pour accéder, modifier ou supprimer des données en infiltrant un système.
Pour se protéger, il est important d'utiliser des requêtes préparées, valider et nettoyer les données entrantes, limiter les privilèges d'accès,
installer un pare-feu d'application web et mettre à jour régulièrement les logiciels et applications.

2) __Qu’est-ce que la faille XSS ? Comment s’en prémunir ?__
Une faille XSS permet à un attaquant d'injecter du code malveillant sur un site web.
Pour se protéger, il est important de filtrer et valider les données utilisateur, utiliser des outils de sécurité, d'échapper les caractères spéciaux et
d'utiliser les en-têtes HTTP de sécurité. 

3) __Qu’est-ce que la faille CSRF ? Comment s’en prémunir ?__
La faille CSRF (Cross-Site Request Forgery) est une attaque qui exploite la confiance d'un site web envers l'utilisateur pour effectuer des actions non autorisées
en son nom.
L'attaque consiste à envoyer des requêtes HTTP légitimes à un site web en utilisant les informations d'identification de l'utilisateur sans son consentement.

4) __Définir l’attaque par force brute et l’attaque par dictionnaire__
L'attaque par force brute teste toutes les combinaisons de caractères pour trouver un mot de passe, tandis que l'attaque par dictionnaire utilise une liste de mots
courants pour deviner le mot de passe.
Il est important de choisir des mots de passe complexes pour se protéger.

5) __Existe-t-il d’autres failles de sécurité ? Citer celles-ci et expliquer simplement leur comportement__
- Débordement de tampon (Buffer Overflow) : Cette faille se produit lorsqu'un programme écrit en mémoire en dehors de la zone prévue pour cela,
ce qui peut conduire à l'exécution de code malveillant.

- Contre-mesure d’en-tête HTTP (HTTP Header Injection) : Cette faille permet à un attaquant d'injecter du code malveillant dans les en-têtes HTTP d'une requête,
ce qui peut entraîner une altération des données ou des attaques de redirection.

- Déni de service (Denial of Service) : Cette faille vise à saturer un serveur ou un système cible en envoyant un grand nombre de requêtes, ce qui empêche les
utilisateurs légitimes d'accéder aux services.

- Injection de code (Code Injection) : Cette faille permet à un attaquant d'injecter du code malveillant dans une application afin d'exécuter des actions non autorisées
ou d'accéder à des données sensibles.

- Contournement de l'authentification (Authentication Bypass) : Cette faille permet à un attaquant de contourner les mécanismes d'authentification d'une application pour
accéder à des fonctionnalités ou des données privilégiées.

6) __A quoi servent l’authentification et l’autorisation dans un contexte d’application web ?__
L'authentification vérifie l'identité de l'utilisateur avec un nom d'utilisateur et un mot de passe, tandis que l'autorisation détermine les actions autorisées
en fonction du rôle de l'utilisateur.

Ces deux processus permettent de contrôler l'accès aux fonctionnalités et données de l'application web, renforçant ainsi sa sécurité et préservant la confidentialité 
des informations.

L'authentification vérifie l'identité, tandis que l'autorisation contrôle les actions permises, garantissant que seuls les utilisateurs légitimes accèdent 
aux données et fonctionnalités appropriées.

7) __Définir la notion de hachage d’un mot de passe et citer des algorithmes de hachage__
Le hachage d'un mot de passe transforme le mot de passe en une chaîne aléatoire pour le protéger.
Il existe plusieurs algorithmes de hachage, certains obsolètes et d'autres sécurisés comme SHA-256 ou bcrypt.
Il est important d'utiliser des algorithmes sécurisés pour protéger les données en ligne.

8) __Qu’est-ce qu’une politique de mots de passe forts ?__
Une politique de mots de passe forts aide à protéger les comptes en imposant des règles comme des mots de passe complexes
et leur changement régulier, pour éviter les piratages.

9) __Qu’est-ce que l’hameçonnage ?__
L'hameçonnage est une arnaque où les fraudeurs se font passer pour des entités légitimes pour voler des informations personnelles,
en utilisant des e-mails ou des messages qui semblent réels. Il faut être vigilant et ne jamais donner ses informations en réponse à ces messages.

10) __Définir la « validation des entrées »__
La validation des entrées consiste à vérifier et filtrer les données de l'utilisateur avant de les utiliser dans un système informatique pour
assurer la sécurité et l'intégrité du système.
Cela permet d'éviter les erreurs et les manipulations de données malveillantes.   

 
 ## RGPD

1) __Qu’est-ce que le RGPD ?__
Règlement Général sur la Protection des Données

2) __Quel est son objectif principal ?__
Protéger les données personnelles des citoyens de l'Union européenne.

3) __Quelle est la date d’entrée en vigueur du RGPD ?__
   En mai 2018

4) __Quelles sont les sanctions possibles en cas de non-respect du RGPD ?__
En cas de non-respect du RGPD, les sanctions possibles incluent des avertissements, des mises en demeure, des restrictions sur le traitement des données,
des amendes administratives pouvant aller jusqu'à 20 millions d'euros ou 4 % du chiffre d'affaires annuel mondial de l'organisme, et des actions
en justice pour obtenir réparation du préjudice.

5) __En France, quel est l’autorité administrative qui s’occupe de faire appliquer le RGPD ?__
La Commission nationale de l'informatique et des libertés (CNIL) 

6) __Quel est le consentement valide selon le RPGD ?__
Pour utiliser les informations personnelles d'une personne, il faut son autorisation.
Cette autorisation doit être donnée librement, clairement, et de manière explicite. La personne doit être bien au courant de ce qu'elle autorise.

7) __Qu’est-ce qu’une politique de confidentialité ?__
Une politique de confidentialité est un document qui explique comment une entreprise gère les informations personnelles de ses utilisateurs.
Elle décrit comment l'entreprise collecte, conserve et protège ces informations.
C'est comme un contrat entre l'entreprise et ses utilisateurs, qui explique comment les informations seront utilisées et protégées.

8) __Quelle est la durée de conservation maximale des données personnelles selon le RGPD ?__
Le RGPD stipule que les données personnelles ne doivent être conservées que le temps nécessaire à leur finalité et impose aux entreprises de déterminer une
durée de conservation raisonnable en fonction de divers critères.

9) __Quels sont les droits des utilisateurs selon le RGPD ?__
Le droit d'accès, le droit de rectification, le droit à l'effacement, le droit à la limitation du traitement, le droit à la portabilité des données,
le droit d'opposition et le droit de ne pas faire l'objet d'une décision individuelle automatisée.
Ces droits visent à protéger la vie privée des utilisateurs et à leur donner plus de contrôle sur leurs informations personnelles.

10) __Qu’est-ce que le principe de minimisation des données selon le RGPD ?__
Le principe de minimisation des données signifie que les organisations doivent uniquement collecter les données nécessaires pour leur objectif
et ne doivent pas conserver les données plus longtemps que nécessaire.
Cela permet de protéger la vie privée des personnes et de réduire les risques de fuite de données.
 

 ## SEO

1) __Qu’est-ce que le SEO ?__
Search Engine Optimization

2) __Quel est l’objectif principal du SEO ?__
Le SEO vise à améliorer le classement d'un site web dans les résultats des moteurs de recherche en optimisant divers aspects tels que le contenu,
les balises, les liens et la vitesse de chargement, afin d'attirer plus de visiteur sur le site (sans payer) et augmenter sa visibilité en ligne.

3) __Existe-t-il plusieurs types de référencement ? Lesquels ?__
Il existe plusieurs types de référencement, tels que le référencement naturel (SEO), le référencement payant (SEA), le référencement local, le référencement
sur les réseaux sociaux, le référencement vidéo et le référencement mobile.
Ces stratégies peuvent être combinées pour renforcer la présence en ligne d'une entreprise et augmenter son audience.

4) __Qu’est-ce que la densité de mots-clés en SEO ?__
La densité de mots-clés en SEO mesure combien un mot-clé est utilisé par rapport au nombre de mots sur une page web.
Il est important de l'utiliser de manière équilibrée pour améliorer le classement sur les moteurs de recherche, sans en abuser,
pour ne pas nuire à la visibilité.
Il est primordial d'offrir un contenu pertinent et utile aux utilisateurs.

5) __Qu’est-ce qu’une balise « alt » ?__
La balise "alt" en HTML décrit les images pour les personnes aveugles et pour les moteurs de recherche. Elle est importante pour l'accessibilité
et le référencement naturel.

6) __Qu’est-ce que la balise « meta description » ?__
La balise meta description est une étiquette HTML qui donne une brève description du contenu d'une page web visible dans les résultats de recherche.
Elle aide les utilisateurs à comprendre le contenu de la page avant de cliquer et influence le classement de la page dans les résultats de recherche.

7) __Qu’est-ce que le « nofollow » en SEO ?__
En SEO, le "nofollow" est un attribut HTML qui indique aux moteurs de recherche de ne pas suivre certains liens sur une page web. Cela aide à éviter
les pénalités liées à des liens de mauvaise qualité.

8) __Quelle est l'importance du contenu de qualité pour le référencement d'un site web ?__
Un contenu de qualité est crucial pour le référencement d'un site web car il améliore la pertinence, attire du trafic organique, augmente le temps
passé par les utilisateurs sur le site, réduit le taux de rebond, favorise les liens entrants naturels, et améliore l'autorité et la crédibilité du site.
Cela contribue à un meilleur classement dans les résultats des moteurs de recherche.

9) __Pourquoi est-il important d'utiliser des balises de titre (h1, h2, h3, etc.) de manière structurée ?__
L'utilisation structurée des balises de titre est essentielle pour améliorer l'accessibilité, le référencement, la clarté du contenu et la cohérence visuelle d'un site web.
Cela facilite la navigation pour les utilisateurs malvoyants, améliore le classement dans les moteurs de recherche, rend le contenu plus clair et organisé,
et assure une présentation uniforme.

10) __Quelle est la recommandation pour les URL d'un site web bien référencé ?__
Pour améliorer le référencement de votre site web, il faut:
- utiliser des URL simples, descriptives et contenant des mots-clés pertinents.
- favoriser les tirets pour séparer les mots et gardez les URLs constantes.
- éviter les redirections et les modifications fréquentes qui peuvent nuire au référencement.

11) __Qu'est-ce que le maillage interne et pourquoi est-il important pour le référencement ?__
Le maillage interne d'un site web consiste à organiser les liens entre les pages pour aider les moteurs de recherche à les trouver et les classer.
Cela améliore le référencement et l'expérience des utilisateurs en facilitant la navigation.

12) __Qu'est-ce que l'optimisation des images pour le référencement ?__
L'optimisation des images pour le référencement consiste à rendre les images d'un site web plus visibles et pertinentes pour les moteurs de recherche,
en utilisant des balises appropriées, des fichiers compressés, des noms de fichiers pertinents et des dimensions adaptées. Cela améliore le positionnement
des images dans les résultats de recherche et attire plus de visiteurs qualifiés sur le site.

13) __Qu'est-ce qu'un plan de site (sitemap) et pourquoi est-il important pour le référencement ?__
Un plan de site est un fichier qui liste toutes les pages d'un site web et aide les moteurs de recherche à comprendre et indexer le contenu du site pour un
meilleur référencement.

## Gestion de projets / DevOps

1) __Qu’est-ce que la gestion de projet ?__
La gestion de projet en programmation consiste à planifier, organiser et contrôler les différentes tâches pour mener à bien un projet de développement logiciel.
Cela implique de définir les objectifs, estimer les ressources, créer un calendrier, suivre la progression et garantir l'efficacité et la qualité du processus
de développement.

2) __Qu’est-ce qu’une méthode Agile de gestion de projet ?__
La méthode Agile est une façon de gérer des projets qui met l'accent sur la capacité à s'adapter et à travailler ensemble.
Elle aide les équipes à mieux faire face aux imprévus et à répondre aux besoins des clients. En livrant régulièrement des produits de bonne qualité,
cette méthode rend le travail plus efficace et permet à tout le monde de mieux comprendre ce qui se passe.

3) __Expliquer la méthode MoSCoW en quelques lignes et citer ses avantages__
La méthode MoSCoW est un moyen de décider quelles fonctionnalités sont les plus importantes en les classant en quatre groupes : indispensables, souhaitables,
optionnelles et rejetées (Must have, Should have, Could have et Won't have). Elle aide à clarifier les priorités et à gérer efficacement le temps et les ressources.
Cela améliore la communication et réduit les risques dans les projets.

4) __A quoi sert la méthodologie MVP ? Citer les caractéristiques clés__
La méthode MVP (Minimum Viable Product) consiste à créer un produit basique avec seulement les fonctionnalités essentielles pour écouter les besoins des utilisateurs.
Cela permet de réduire les coûts, d'obtenir rapidement des retours et d'améliorer le produit rapidement. En gros, c'est une façon d'économiser temps et argent
tout en testant une idée.

5) __Qu’est-ce que la planification itérative ?__
La planification itérative divise le travail en cycles répétitifs, permettant de réaliser et d'évaluer une partie du projet à la fois.
Cela aide à obtenir des résultats rapidement et à s'adapter aux changements. Bien que courante dans le développement logiciel, cette méthode peut aussi être
utilisée pour d'autres projets.

6) __Citer 3 méthodes Agiles dans le cadre d’un projet informatique__
- Scrum est une méthode agile populaire basée sur des itérations de développement appelées "sprints"
- Kanban est une méthode visuelle de gestion du travail basée sur des cartes
- Extreme Programming se concentre sur la qualité du code et la collaboration au sein de l'équipe de développement.

7) __Qu’est-ce qu’une réunion de revue de projet ?__
La réunion de revue de projet est un moment clé pour évaluer, ajuster et prendre des décisions importantes afin de garantir la réussite du projet.
Elle favorise la transparence, la communication et la collaboration au sein de l'équipe.

8) __Qu’est-ce qu’un livrable dans un projet ?__
Un livrable est un résultat concret à produire dans un projet, comme un document ou un produit. Au début, on définit ce qui est attendu, puis on vérifie
régulièrement que tout est conforme. Cela aide à suivre l'avancement et à atteindre les objectifs du projet.

9) __Quels sont les 3 piliers SCRUM ?Définir chacun d’entre eux__
Les trois piliers de SCRUM:
- La transparence permet à l'équipe et aux parties prenantes de voir et comprendre le processus de travail.
- L'inspection consiste à vérifier régulièrement les progrès lors de réunions comme les revues de sprint, permettant d'identifier des problèmes.
- L'adaptation implique que l'équipe ajuste ses méthodes et priorités en fonction des résultats inspectés.
Ensemble, ces principes favorisent l'amélioration continue dans les projets complexes.

10) __Qu’est-ce que le DevOps et quel est son objectif principal ?__
Le DevOps encourage la coopération entre les équipes de développement et d'opérations pour livrer rapidement des logiciels de qualité.
Il automatise les étapes de développement, de test et de déploiement. L’objectif est d'assurer une livraison continue tout en maintenant la stabilité et
en favorisant un esprit d'équipe.

11) __Qu’est-ce que l’intégration continue ?__
L'intégration continue est une méthode qui automatise l'intégration des codes sources pour repérer et corriger rapidement les erreurs. Elle garantit la qualité
et la cohérence du code en utilisant des outils pour compiler, tester et déployer les modifications. Cela aide à réduire les risques dans le développement logiciel.

12) __Qu’est-ce que Docker ? Et en quoi est-il utile dans le cadre du DevOps ?__
Docker est une plateforme qui aide à créer, déployer et gérer des conteneurs logiciels. Elle facilite le fonctionnement des applications dans différents
environnements, évitant les problèmes de compatibilité. Avec Docker, les équipes peuvent automatiser le déploiement et rendre les processus de développement
plus efficaces, tout en économisant des ressources et en rendant les applications plus faciles à adapter.

13) __Qu’est-ce qu’un test unitaire ?__
Les tests unitaires consistent à vérifier automatiquement des parties spécifiques d'un logiciel pour s'assurer qu'elles fonctionnent correctement.
Cela aide à détecter les erreurs rapidement et à garantir la qualité du code. Cette méthode facilite également la maintenance et soutient le développement agile.

14) __Quelle est l'unité de code testée lors d'un test unitaire ?__
Un test unitaire vérifie le bon fonctionnement d'une petite partie d'un programme, comme une fonction ou une méthode, en se concentrant uniquement sur celle-ci.
L'objectif est de s'assurer qu'elle produit les résultats attendus dans différentes situations. En résumé, c'est un contrôle ciblé pour garantir la fiabilité d'un
morceau de code.

15) __Quelles sont les caractéristiques d'un bon test unitaire ?__
Les bons tests unitaires sont des vérifications que l'on fait sur de petites parties d'un programme pour s'assurer qu'elles fonctionnent correctement. 
Ils sont:
- Indépendants : Pas d'impact d'un test à l'autre.
- Isolés : Un seul point de vérification par test.
- Répétables : Résultats constants à chaque exécution.
- Rapides : Exécution rapide pour un développement fluide.
- Lisibles : Code de test clair et compréhensible.
- Pertinents : Vérification des fonctionnalités essentielles.
- Fiables : Résultats cohérents et précis.
- Bien documentés : Explications claires pour chaque test.
Ils aident à améliorer la qualité du code et à réduire les erreurs dans les applications logicielles.

16) __Qu'est-ce qu'une assertion dans un test unitaire ?__
Avec les assertions, on vérifie si une partie du code se comporte comme prévu lors d'un test unitaire. Si une assertion échoue,
le test échoue et le code ne fonctionne pas correctement. Les assertions sont importantes pour garantir la qualité du code.

 
 ## English
_
1) __What does JavaScript enable you to do on a website ?__
a. Add interactive behavior and dynamic content

2) __Which programming language is primarily used for server-side web development ?__
a. PHP

3) __What is the purpose of a web browser ?__
a. To render and display web pages

4) __What is the difference between GET and POST methods in HTTP ?__
a. GET retrieves data from a server, while POST submits data to a server
GET method is used to retrieve data from a server without modifying it, while POST method is used to submit data to a server to create or update resources.
GET requests are less secure and have limitations on the amount of data that can be sent, while POST requests are more secure and have no limitations on data size.

5) __What is the purpose of version control systems (e.g., Git) in web development ?__
a. To track changes and manage collaborative development
Version control systems like Git are essential in web development to track changes made to the codebase, allowing developers to revert to previous versions if
needed and maintain an organized record of changes. It also enables collaboration between team members by managing simultaneous edits to the codebase and merging
changes seamlessly. Overall, version control systems help streamline the development process and ensure code quality and consistency.

6) __What is the purpose of a framework in web development ?__
a. To provide a structured environment for building web applications
Frameworks in web development provide a pre-built structure and set of tools to streamline the process of building web applications. They offer libraries,
templates, and best practices that help developers organize code, improve efficiency, and maintain consistency throughout a project.Frameworks also often include
built-in security features, database access, and other functionalities that can help developers create robust and reliable web applications.

7) __What does NoSQL stand for ?__
a. Not Only SQL

8) __Which of the following is a characteristic of NoSQL databases ?__
c. Scalability and flexible data models
