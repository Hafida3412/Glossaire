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
   Pour exécuter un script PHP (Hypertext Preprocessor), il faut installer Laragon ou XAMMPP.

2) __Qu’est-ce qu’un algorithme?__
   C'est la description d'une suite d'étapes permettant d'obtenir un résultat à partir d'éléments fournis au départ.
   Exemple: une recette de cuisine est un algorithme permettant d'obtenir un plat à partir d'ingrédients.

3) __Qu’est-ce qu’une variable ? Par quel symbole est préfixée une variable en PHP ?__
   Une variable est un élément mesurable qui peut prendre différentes valeurs.
   Exemple: taille, âge, poids...

4) __Qu’est-ce que la portée d’une variable ?__
   La portée d'une variable correspond à l'espace du script dans laquelle elle va être accessible. 

5) __Qu’est-ce qu’une constante ? Quelle est la différence avec une variable ?__
   Une constante contient toujours la même valeur. A la différence d'une variable qui peut changer ou varier.

6) __Qu’est-ce qu’une superglobale, combien en existent-ils et donner un exemple d’utilisation?__
   Les superglobales $_GET et $_POST sont des arrays automatiquement créées par PHP lors du chargement de chaque page.
   Elles sont accessibles partout et existent sur toutes les pages, que ce soit au milieu du code, au début ou dans les fonctions.
   Ces variables permettent de récupérer respectivement les données envoyées en GET et en POST dans les requêtes HTTP.


7) __Quels sont les différents types (primitifs) que l’on peut associer à une variable en PHP ? Les citer 
   et en donner des exemples (ne pas oublier le type d’une variable sans valeur)__
   Les différents types primitifs que l'on peut associer à une variable en PHP sont:
   null.
   bool.
   int.
   float (nombre à virgule flottante)
   string.
   array.

8) __Existe-t-il plusieurs types de tableaux en PHP, si oui lesquels ?__
   Il existe 2 types de tabeau:
   - les tableaux à index numériques
   - les tableaux associatifs

9) __Quelles sont les différentes structures de contrôles qu’il existe en algorithmie ? Donner un 
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


10) __Quelle est la fonction PHP permettant de demander la longueur d’une chaîne de caractères ?__
    La fonction PHP permettant de demander la longueur d’une chaîne de caractères est strlen().
        Exemple:
        $chaine = "Hello!";
        $longueur = strlen($chaine);
        echo "La longueur de la chaîne est : " . $longueur;

11) __Qu’est-ce qu’une session ? Quelle fonction permet de démarrer une session en PHP ? Donner un 
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
    Lorsque nous utilisons <<include>>, si le fichier n'est pas trouvé, il affiche un avertissement et continue 
    l'exécution du script.
    Lorsque nous utilisons <<require>>, si le fichier n'est pas trouvé, PHP génère une erreur fatale et arrête
    l'exécution du script.
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
      Par exemple, lorsque vous consultez une page web, le serveur peut envoyer des données au format JSON pour que 
      votre navigateur puisse les afficher.

5) __Peut-on interpréter du Javascript côté serveur ? Si oui, comment ?__
   Oui, on peut utiliser JavaScript sur des ordinateurs serveurs grâce à un outil appelé Node.js.
   Node.js est comme un super programme qui aide les ordinateurs à comprendre et à exécuter JavaScript sans avoir besoin d'un navigateur web,
   ce qui permet de créer des sites web et des applications qui fonctionnent sur des serveurs.

6) __Qu’est-ce qu’un sélecteur CSS ?__
   Les sélecteurs CSS permettent de cibler des éléments HTML présents sur une page web
   pour leur appliquer une règle CSS.

7) __Quelle balise HTML permet de créer un lien hypertexte ?__
   <a href=".........."</a>
   
8) __Qu’est-ce qu’une requête AJAX ?__
  AJAX permet de demander des informations au serveur sans recharger la page, ce qui économise du temps et de la bande passante.
Cela rend les mises à jour de la page plus rapides et fluides. Grâce à AJAX, les applications web peuvent être plus interactives et réactives,
améliorant ainsi l'expérience utilisateur sans interruption.

 9) __Quel sélecteur CSS permet de sélectionner tous les éléments d’une classe spécifique ? D’un 
identifiant spécifique ?__
    Le sélecteur de classe commence par un point . et sélectionne tout élément du document auquel cette classe est appliquée. 
    Un sélecteur d'ID commence par un # , il est utilisé de la même manière qu'un sélecteur de classe.
    En revanche, l'ID ne peut être utilisé qu'une seule fois par document.

10) __Définir le responsive design__
    Ce design permet de modifier la mise en page d'un site afin que le contenu s'adapte à n'importe quel écran.
    Exemple: smartphone, tablette, ordinateur, TV...

11) __Qu’est-ce que le templating ?__
    Cela consiste à utiliser des modèles tout prêts pour afficher des données de façon automatique et qui change en fonction des données.

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
    Par exemple, le pseudo-élément ::first-line permettra de ne cibler que la première ligne d’un élément visé par le sélecteur1.
    
16) __Qu’est-ce que Bootstrap ? Donner d’autres exemples équivalent__
    C'est un framework de développement web qui permet de créer rapidement et facilement des sites web responsives.
    Il contient des composants et des styles prédéfinis qui facilitent la conception et la mise en page des pages web.
    Exemples équivalents:
   - Foundation : un autre framework de développement web populaire
   - Materialize : un framework basé sur le design Material de Google
   - Bulma : un framework CSS moderne et léger

17) __Quand un formulaire HTML est créé, quelles sont les 2 méthodes qui peuvent lui être associées ?
Donner la différence entre ces 2 méthodes.__
- La méthode GET envoie les données à traiter via l'URL, ce qui signifie que les données seront visibles dans l'URL.
Cette méthode est généralement utilisée pour les requêtes de lecture de données.

- La méthode POST envoie les données à traiter dans le corps de la requête HTTP, ce qui signifie que les données ne sont pas visibles dans l'URL.
Cette méthode est généralement utilisée pour les requêtes de création ou de modification de données sensibles.

 ##  UX / UI

1) __Quelle est la différence entre UX Design et UI Design ?__
L'UX Design concerne l'expérience globale de l'utilisateur avec un produit ou un service, tandis que l'UI Design se concentre sur l'apparence visuelle
et l'esthétique de l'interface utilisateur. Les deux aspects sont importants pour créer un produit numérique réussi.

2) __Qu’est-ce qu’un wireframe ?__
Un wireframe est un plan visuel simple d'un site web ou d'une interface utilisateur, utilisé pour organiser les éléments et la structure avant de commencer
à concevoir et développer. Il est composé de lignes et de formes pour indiquer l'emplacement des images, du texte, des boutons et des liens, permettant de
visualiser la disposition des éléments et l'expérience utilisateur.

3) __Qu’est-ce qu’un prototype ?__
Un prototype UX/UI est une maquette interactive d'une interface utilisateur pour tester le design d'une application ou d'un site web avant son développement
complet. Ils permettent de visualiser et tester l'interface, recueillir des retours des utilisateurs et identifier les problèmes potentiels pour améliorer
l'expérience utilisateur avant le lancement du produit final.

4) __Qu’est-ce que la hiérarchie visuelle en UI Design ?__
La hiérarchie visuelle en UI design organise les éléments visuels pour guider l'œil de l'utilisateur, mettre en avant ce qui est important et faciliter la navigation.
Elle repose sur la taille, la couleur, le contraste et l'espacement des éléments pour créer une structure claire et une expérience utilisateur agréable.

5) __Qu’est-ce que l’accessibilité en UX Design ?__
L'accessibilité en UX Design consiste à concevoir des produits numériques accessibles à tous, y compris aux personnes en situation de handicap.
Cela implique de prendre en compte les besoins spécifiques de chaque utilisateur pour garantir une expérience utilisateur optimale.
L'objectif est de rendre les produits numériques faciles à utiliser, quel que soit le profil de l'utilisateur.

6) __Qu’est-ce qu’une grille de mise en page ?__
C'est un système de lignes qui organisent l'espace graphique et facilitent la création de designs équilibrés et harmonieux en guidant le positionnement
des éléments visuels comme le texte et les images. Elle est largement utilisée dans le design web, l'édition de magazines, la publicité, etc.

7) __Qu’est-ce que la notion d’affordance en UX Design ?__
L'affordance en UX Design signifie la capacité d'un produit à suggérer comment il peut être utilisé. Par exemple, un bouton cliquable sur un site Web indique
à l'utilisateur qu'il peut déclencher une action. Les affordances sont essentielles pour créer une expérience utilisateur intuitive et efficace en guidant
les utilisateurs dans l'interaction avec un produit.

8) __Qu’est-ce qu’un « mobile first design » ?__

 ## Programmation orientée objet (POO)

1) __Donner une définition de la programmation orientée objet__
   Elle regroupe des informations et des actions liées dans des objets, dotés d'attributs et de méthodes.
   Par exemple, un objet 'voiture' peut avoir des attributs comme la couleur et des méthodes comme 'démarrer'.
   Cette approche permet une organisation logique et structurée du code, facilitant sa gestion, sa compréhension et sa réutilisation.

3) __Qu’est-ce qu’une classe ? Comment la déclare-t-on ?__
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
En programmation orientée objet (POO), un objet est une instance d'une classe. Une classe est un modèle ou un plan pour créer des objets.
Les objets sont des entités qui contiennent des données (attributs) et des méthodes (fonctions) qui agissent sur ces données.

Par exemple, si vous avez une classe "Voiture", un objet "voiture1" créé à partir de cette classe aurait des attributs tels que la couleur, la marque et le modèle, ainsi que des méthodes pour démarrer la voiture, accélérer, freiner, etc.

4) __Définir la notion de propriété / attribut / méthode__
En programmation orientée objet, on utilise des propriétés pour garder des informations sur un objet, des attributs pour décrire cet objet
et des méthodes pour dire à l'objet comment se comporter. Ces idées aident à bien représenter les objets dans un programme informatique.

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
L'encapsulation consiste à enfermer les données et les méthodes dans une boîte verrouillée, permettant de protéger les données et d'éviter les modifications non contrôlées.
Les données sont accessibles et modifiables uniquement à travers des méthodes spécifiques, assurant un contrôle total sur les opérations effectuées sur ces données.
Par exemple, une classe "Personne" peut encapsuler les données telles que le nom et l'âge, en offrant des méthodes pour y accéder et les modifier de manière contrôlée.

8) __Définir l’opérateur de résolution de portée__
L'opérateur de résolution de portée, souvent noté "::", permet d'accéder aux membres d'une classe ou d'un objet dans un programme orienté objet.
Cela signifie qu'on peut utiliser cet opérateur pour appeler des fonctions ou des variables définies dans une classe à partir d'une autre partie du programme.
Cela permet d'organiser et de structurer le code de manière plus claire et de limiter les conflits entre différents éléments d'un programme.

9) __Définir une méthode / propriété statique__
Une méthode ou propriété statique est une fonction ou une variable spécifique à une classe qui peut être appelée ou utilisée sans avoir besoin d'instancier
un objet de cette classe.
Cela signifie que la méthode ou propriété statique est partagée entre toutes les instances de la classe et peut être appelée directement en utilisant le nom de la classe.

10) __Définir le polymorphisme en POO__
C'est un concept qui permet à un objet de se comporter de différentes manières, en fonction du contexte dans lequel il est utilisé.
Cela signifie qu'un même nom de méthode peut avoir des implémentations différentes dans différentes classes.
Cela permet d'écrire un code plus générique et flexible, car on peut utiliser un objet de différentes manières sans avoir à connaître sa classe exacte.

11) __Définir une méthode / classe abstraite ?__
Une méthode abstraite est une méthode qui n'a pas de corps ou d'implémentation dans une classe, mais qui doit être définie dans les classes qui en héritent.
Une classe abstraite est une classe qui contient au moins une méthode abstraite et qui ne peut pas être instanciée directement, mais qui sert de modèle pour
d'autres classes qui vont en hériter et implémenter les méthodes abstraites.

12) __Définir le chaînage de méthodes__
C'est une technique qui consiste à appeler plusieurs méthodes d'un objet les unes après les autres dans une seule instruction. Cela permet de simplifier
le code et d'améliorer la lisibilité en évitant la répétition de code.

13) __Qu’est-ce que la méthode__ __toString() ? Existe-t-il d’autres méthodes « magiques »__
La méthode __toString() est une méthode spéciale en programmation orientée objet (POO) qui permet de définir comment un objet doit se comporter lorsqu'il
est converti en chaîne de caractères. Elle est appelée automatiquement lorsque l'objet est utilisé dans un contexte où une chaîne de caractères est attendue.

Il existe d'autres méthodes magiques en POO, telles que __construct() pour le constructeur de la classe, __destruct() pour le destructeur, __get() et __set() 
pour la surcharge des accesseurs, etc. Ces méthodes sont appelées automatiquement dans certaines circonstances spécifiques.

14) __Qu’est-ce qu’un « autoload » ?__
L'autoload est une fonctionnalité qui permet de charger automatiquement les classes ou les fichiers nécessaires au bon fonctionnement d'un programme.
Cela évite d'avoir à inclure manuellement chaque classe ou fichier à chaque fois qu'ils sont nécessaires, ce qui simplifie le processus de développement
et rend le code plus clair et facile à maintenir.

15) __Comment appelle-t-on en français les « getters » et les « setters » ?__
On appelle les « getters » des « accesseurs » et les « setters » des « mutateurs ».

16) __Qu’est-ce que la sérialisation en PHP ?__
La sérialisation en PHP est le processus de conversion d'objets ou de tableaux en une chaîne de caractères afin de les stocker ou de les transférer plus facilement.
Cela permet de transformer des données complexes en une forme simple qui peut être utilisée ultérieurement. La désérialisation est l'opération inverse qui consiste
à convertir la chaîne de caractères en objet ou en tableau d'origine.

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
et le contrôleur, qui traite les actions de l'utilisateur et met à jour le modèle. Cette séparation des responsabilités permet de
rendre le code plus modulaire, maintenable et évolutif.

4) __Quel est le rôle de chaque couche du design pattern MVC : Model, View, Controller ?__
- Le modèle (Model) : C'est la couche qui représente les données de l'application et la logique métier. Elle traite les requêtes et les modifications des données.
- La vue (View) : C'est la couche qui affiche les données au utilisateur et gère l'interface graphique de l'application.
- Le contrôleur (Controller) : C'est la couche qui fait le lien entre le modèle et la vue. Il récupère les requêtes de l'utilisateur, traite les données en conséquence,
et décide quelle vue afficher.

5) __Quels sont les avantages de l’architecture MVC ?__
L'architecture MVC permet de séparer clairement les différents éléments d'une application : le modèle qui représente les données, la vue qui affiche ces données
à l'utilisateur et le contrôleur qui gère les interactions entre le modèle et la vue. Cela facilite la maintenance, la réutilisation du code et la collaboration
entre les développeurs. De plus, cela permet une meilleure organisation du code et une plus grande flexibilité dans le développement de l'application.

6) __Existe-t-il des variantes à l’architecture MVC ?__
Oui, il existe des variantes à l'architecture MVC, telles que MVVM (Modèle-Vue-VueModèle) et MVP (Modèle-Vue-Présentateur).
Ces variantes sont des adaptations de l'architecture MVC pour répondre à des besoins spécifiques ou pour améliorer la séparation
des préoccupations dans une application.
Elles sont utilisées dans le développement de logiciels pour organiser le code de manière claire et modulaire.

7) __Qu’est-ce qu’une API ? Définir l’architecture REST__
Une API est un ensemble de règles et de conventions qui permettent à des logiciels différents de communiquer entre eux.
Cela permet d'échanger des données et de fonctionner ensemble de manière harmonieuse.

L'architecture REST (Representational State Transfer) est un style d'architecture qui définit comment les ressources d'un système web doivent être adressées et 
comment les actions doivent être effectuées. Elle repose sur l'utilisation d'URLs pour identifier les ressources et l'utilisation de méthodes HTTP 
(GET, POST, PUT, DELETE) pour effectuer des actions sur ces ressources. Elle est souvent utilisée pour concevoir des APIs web simples et efficaces.


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
Il décrit les entités, les relations entre les entités, les attributs des entités, ainsi que les contraintes et les règles
métier liées aux données. Il permet de modéliser les données d'un système de manière logique et structurée afin de
faciliter leur manipulation et leur gestion.

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
La relation "Many To Many" est modélisée par une table intermédiaire qui facilite la gestion des associations entre les entités concernées.

7) __Qu’est-ce qu’une base de données ?__
   C'est un endroit où on peut stocker et organiser des informations de manière structurée.
   C'est comme une grande bibliothèqte numérique où on peut ranger des livres (=données) pour les retrouver facilement 
   plus tard. Elles sont essentielles pour les applications Web, les systèmes de gestion...


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
Les bases de données relationnelles stockent des données sous forme de tables liées entre elles par des clés étrangères, suivent le modèle ACID et conviennent aux
données structurées et aux relations complexes. Les bases de données non relationnelles stockent des données de manière flexible, sont conçues pour être
hautement évolutives et adaptées aux données semi-structurées ou non structurées. Elles ne suivent pas nécessairement le modèle ACID et sont adaptées aux environnements
nécessitant une haute performance et disponibilité.

10) __Qu’est-ce qu’une jointure dans une base de données ? En existe-t-il plusieurs ? Si oui lesquelles ?__
Une jointure dans une base de données est une opération qui permet de combiner des données provenant de deux tables différentes en fonction d'une condition commune entre les deux. Il existe plusieurs types de jointures, les principales sont :

- Jointure interne : Elle ne renvoie que les lignes des tables qui ont une correspondance dans les deux tables.
- Jointure externe : Elle renvoie les lignes des tables, même celles qui n'ont pas de correspondance dans l'autre table.
- Jointure gauche : Elle renvoie toutes les lignes de la table de gauche et les lignes correspondantes dans la table de droite.
- Jointure droite : Elle renvoie toutes les lignes de la table de droite et les lignes correspondantes dans la table de gauche.

11) __A quoi sert une vue dans une base de données ?__
Une vue dans une base de données permet de voir les données d'une ou plusieurs tables de manière organisée et structure, et de manipuler ces données plus facilement.
On peut aussi limiter l'accès à certaines données en cachant des champs ou en ne montrant que certaines lignes qui correspondent à des critères spécifiques.

12) __Qu’est-ce que l’intégrité référentielle dans une base de données ?__
L'intégrité référentielle en base de données consiste à s'assurer que les liens entre les différentes tables sont respectés.
Par exemple, si une table contient une clé étrangère qui fait référence à une clé primaire dans une autre table, il est important que la valeur de
la clé étrangère corresponde toujours à une valeur existante dans la clé primaire. Cela permet d'éviter les erreurs et les incohérences dans les
données de la base de données.

13) __Quelles sont les fonctions d’agrégation en SQL ?__
En SQL, les fonctions d'agrégation sont utilisées pour effectuer des calculs sur un ensemble de valeurs, telles que la somme, la moyenne, le maximum, le minimum, etc.
Elles permettent de regrouper et de résumer les données d'une table en fonction de critères spécifiques, comme par exemple regrouper les ventes par mois ou par catégorie.
Les fonctions d'agrégation sont souvent utilisées avec la clause GROUP BY pour regrouper les données avant d'appliquer les calculs.

14) __Qu’est ce qu’un CRUD dans le contexte d’une base de données ?__
Le terme CRUD est un acronyme pour Create, Read, Update et Delete. Il fait référence aux opérations de base que l'on peut effectuer sur une base de données :
créer des données, lire des données, mettre à jour des données et supprimer des données.
Ces opérations permettent de gérer les informations stockées dans une base de données de manière simple et efficace.

15) __Quelles sont les clauses qui permettent de :__
a. __Insérer un nouvel enregistrement dans une table__
On utilise généralement la clause INSERT INTO. On spécifie le nom de la table dans laquelle on veut insérer les données, puis on précise les valeurs à insérer dans chaque colonne de la table. Par exemple :

INSERT INTO nom_table (colonne1, colonne2, colonne3) VALUES (valeur1, valeur2, valeur3);

Cette requête permet d'ajouter un nouvel enregistrement dans la table "nom_table" en spécifiant les valeurs à insérer dans les colonnes "colonne1", "colonne2" et "colonne3".

b. __Modifier un enregistrement dans une table__
Pour modifier un enregistrement dans une table, il faut utiliser la clause SQL "UPDATE" suivie du nom de la table et des colonnes que l'on souhaite modifier. 
Ensuite, on utilise la clause "SET" pour spécifier les nouvelles valeurs pour chaque colonne. 
On peut également ajouter une clause "WHERE" pour spécifier les enregistrements à modifier en fonction de certaines conditions.

c. __Supprimer un enregistrement dans une table__
Il faut utiliser la clause DELETE FROM suivi du nom de la table et de la clause WHERE pour spécifier les critères de suppression. 
Par exemple, DELETE FROM table_nom WHERE condition_de_suppression.

d. __Supprimer la base de données__
Il existe deux types de clauses pour supprimer une base de données:
- Clauses DROP DATABASE : Ces clauses permettent de supprimer complètement une base de données et tous ses objets (tables, index, procédures stockées, etc.).
- Clauses DROP TABLE : Ces clauses permettent de supprimer uniquement une table spécifique de la base de données, sans supprimer la base de données elle-même.

e. __Filtrer les résultats d’une requête SQL:__
-> on utilise les clauses WHERE et HAVING.

- La clause WHERE permet de spécifier des critères de sélection pour les lignes à récupérer dans une table. Par exemple, on peut filtrer les résultats en définissant une condition comme "WHERE nom = 'Dupont'".

- La clause HAVING permet de filtrer les résultats d'une requête qui contient une fonction d'agrégation comme SUM, AVG, COUNT, etc.
Par exemple, on peut utiliser la clause HAVING pour filtrer les résultats en spécifiant une condition sur le résultat d'une fonction d'agrégation
comme "HAVING SUM(quantite) > 100".

f. __Trier les résultats d’une requête SELECT__
Pour trier les résultats d'une requête SELECT, on utilise la clause ORDER BY. 
Cette clause permet de spécifier sur quelle colonne ou ensemble de colonnes les résultats doivent être triés, et aussi dans quel ordre (croissant ou décroissant). 
Par exemple, ORDER BY nom ASC triera les résultats par ordre alphabétique croissant du champ nom.

g. __Regrouper les résultats d'une requête SELECT en fonction d'une colonne spécifique__
Pour regrouper les résultats d'une requête SELECT en fonction d'une colonne spécifique, on utilise la clause GROUP BY dans la requête SQL. 
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

7) Qu’est-ce que l’injection de dépendances ? Quel est l’outil utilisé dans ce contexte et quel fichier 
contient l’intégralité des dépendances du projet ?

8) Que permet le bundle Maker au sein de Symfony ?
Le bundle Maker de Symfony permet de créer rapidement des éléments de code comme des entités, des contrôleurs et des formulaires, ce qui facilite le développement
en automatisant des tâches récurrentes.

9) Quel est le langage de requêtage exploité au sein d’un projet Symfony ?
Symfony utilise le langage SQL pour les requêtes dans un projet, mais grâce à Doctrine, il est possible de manipuler les données de la base de données en utilisant
des objets PHP plutôt que du SQL directement.

10) Quel est le composant qui garantit l’authentification et l’autorisation des utilisateurs ?
Le composant qui garantit l'authentification et l'autorisation des utilisateurs est un système de gestion des identités, souvent abrégé en
IAM (Identity and Access Management). Ce système permet de vérifier l'identité des utilisateurs, de gérer leurs droits d'accès à différents systèmes et ressources,
et de garantir la sécurité des informations sensibles.

## Sécurité

1) Qu’est-ce que l’injection SQL ? Comment s’en prémunir ?
L'injection SQL est une attaque informatique qui utilise du code malveillant pour accéder, modifier ou supprimer des données en infiltrant un système.
Pour se protéger, il est important d'utiliser des requêtes préparées, valider et nettoyer les données entrantes, limiter les privilèges d'accès,
installer un pare-feu d'application web et mettre à jour régulièrement les logiciels et applications.

2) Qu’est-ce que la faille XSS ? Comment s’en prémunir ?
Une faille XSS (Cross-Site Scripting) est une faille de sécurité courante sur les sites web qui permet à un attaquant d'injecter du code malveillant dans des
pages web consultées par d'autres utilisateurs. Ce code peut être du JavaScript, du HTML ou d'autres langages et peut être utilisé pour voler des informations sensibles,
rediriger les utilisateurs vers des sites malveillants, ou détourner des sessions utilisateurs.

Pour se prémunir contre les attaques XSS, voici quelques bonnes pratiques à mettre en place :

-> Filtrer et valider les données utilisateur : Toute donnée entrée par l'utilisateur et affichée sur le site doit être correctement filtrée et validée pour éviter toute injection de code malveillant.

-> Utiliser des outils de sécurité : Les pare-feu d'application web (WAF) et les outils de sécurité comme OWASP ZAP peuvent aider à détecter et bloquer les attaques XSS.

-> Échapper les caractères spéciaux : Les données utilisateur affichées sur le site doivent être correctement échappées pour neutraliser tout code malveillant potentiel.

-> Utiliser les en-têtes de sécurité HTTP : Les en-têtes de sécurité comme Content-Security-Policy et X-XSS-Protection peuvent aider à renforcer la protection contre les attaques XSS en limitant les sources des scripts exécutés sur le site.

En suivant ces bonnes pratiques et en restant vigilant sur la sécurité de votre site web, vous pouvez limiter les risques liés aux attaques XSS et protéger les données sensibles de vos utilisateurs.

3) Qu’est-ce que la faille CSRF ? Comment s’en prémunir ?
La faille CSRF (Cross-Site Request Forgery) est une attaque qui exploite la confiance d'un site web envers l'utilisateur pour effectuer des actions non autorisées en son nom. L'attaque consiste à envoyer des requêtes HTTP légitimes à un site web en utilisant les informations d'identification de l'utilisateur sans son consentement.

Pour se prémunir contre la faille CSRF, voici quelques bonnes pratiques à mettre en place :

-> Utiliser des jetons CSRF : les jetons CSRF sont des balises uniques générées par le serveur et incluses dans les formulaires et les requêtes HTTP. Ils permettent de vérifier que la requête provient bien de l'utilisateur légitime.

-> Limiter la validité des jetons CSRF : les jetons CSRF doivent être générés de manière aléatoire et non prédictible, et ils doivent expirer après une durée limitée pour limiter leur réutilisation.

-> Utiliser des en-têtes Origin et Referrer : ces en-têtes permettent de vérifier l'origine de la requête et de s'assurer qu'elle provient bien du site web légitime.

-> Mettre en place des mesures de sécurité au niveau du serveur : les développeurs doivent mettre en place des contrôles de sécurité au niveau du serveur pour détecter et prévenir les attaques CSRF.

En suivant ces bonnes pratiques, les développeurs peuvent réduire les risques liés à la faille CSRF et renforcer la sécurité de leurs applications web.

4) Définir l’attaque par force brute et l’attaque par dictionnaire
L'attaque par force brute teste toutes les combinaisons de caractères pour trouver un mot de passe, tandis que l'attaque par dictionnaire utilise une liste de mots
courants pour deviner le mot de passe. Il est important de choisir des mots de passe complexes pour se protéger.

5) Existe-t-il d’autres failles de sécurité ? Citer celles-ci et expliquer simplement leur comportement
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

6) A quoi servent l’authentification et l’autorisation dans un contexte d’application web ?
L'authentification vérifie l'identité de l'utilisateur avec un nom d'utilisateur et un mot de passe, tandis que l'autorisation détermine les actions autorisées
en fonction du rôle de l'utilisateur.

Ces deux processus permettent de contrôler l'accès aux fonctionnalités et données de l'application web, renforçant ainsi sa sécurité et préservant la confidentialité 
des informations.

En résumé, l'authentification vérifie l'identité, tandis que l'autorisation contrôle les actions permises, garantissant que seuls les utilisateurs légitimes accèdent 
aux données et fonctionnalités appropriées.

7) Définir la notion de hachage d’un mot de passe et citer des algorithmes de hachage
Le hachage d'un mot de passe transforme le mot de passe en une chaîne aléatoire pour le protéger.
Il existe plusieurs algorithmes de hachage, certains obsolètes et d'autres sécurisés comme SHA-256 ou bcrypt.
Il est important d'utiliser des algorithmes sécurisés pour protéger les données en ligne.

8) Qu’est-ce qu’une politique de mots de passe forts ?
Une politique de mots de passe forts aide à protéger les comptes en imposant des règles comme des mots de passe complexes
et leur changement régulier, pour éviter les piratages.

9) Qu’est-ce que l’hameçonnage ?
L'hameçonnage est une arnaque où les fraudeurs se font passer pour des entités légitimes pour voler des informations personnelles,
en utilisant des e-mails ou des messages qui semblent réels. Il faut être vigilant et ne jamais donner ses informations en réponse à ces messages.

10) Définir la « validation des entrées »
La validation des entrées consiste à vérifier et filtrer les données de l'utilisateur avant de les utiliser dans un système informatique pour
assurer la sécurité et l'intégrité du système.
Cela permet d'éviter les erreurs et les manipulations de données malveillantes.   

 
 ## RGPD

1) Qu’est-ce que le RGPD ?
Règlement Général sur la Protection des Données

2) Quel est son objectif principal ?
Protéger les données personnelles des citoyens de l'Union européenne.

3) Quelle est la date d’entrée en vigueur du RGPD ?
   En mai 2018

4) Quelles sont les sanctions possibles en cas de non-respect du RGPD ?
En cas de non-respect du RGPD, les sanctions possibles incluent des avertissements, des mises en demeure, des restrictions sur le traitement des données,
des amendes administratives pouvant aller jusqu'à 20 millions d'euros ou 4 % du chiffre d'affaires annuel mondial de l'organisme, et des actions
en justice pour obtenir réparation du préjudice. Il est crucial pour les organismes de se conformer au RGPD pour éviter ces conséquences sévères.

5) En France, quel est l’autorité administrative qui s’occupe de faire appliquer le RGPD ?
La Commission nationale de l'informatique et des libertés (CNIL) 

6) Quel est le consentement valide selon le RPGD ?
Le consentement valide selon le RGPD doit être donné librement, spécifiquement, de manière éclairée et univoque par la personne concernée, et doit être explicite. Les organisations doivent s'assurer de recueillir un tel consentement pour se conformer à la législation sur la protection des données.

7) Qu’est-ce qu’une politique de confidentialité ?
C'est un document qui informe les individus sur la manière dont une organisation collecte, stocke et protège leurs informations personnelles.
Elle est souvent utilisée sur les sites internet, les applications et les plateformes en ligne. Les entreprises doivent respecter leur propre politique
de confidentialité et se conformer aux lois en vigueur en matière de protection des données.

8) Quelle est la durée de conservation maximale des données personnelles selon le RGPD ?
Le RGPD stipule que les données personnelles ne doivent être conservées que le temps nécessaire à leur finalité et impose aux entreprises de déterminer une
durée de conservation raisonnable en fonction de divers critères. Il est essentiel de définir une politique de conservation des données pour respecter les principes
de minimisation et de limitation de la durée de conservation.

9) Quels sont les droits des utilisateurs selon le RGPD ?
Le droit d'accès, le droit de rectification, le droit à l'effacement, le droit à la limitation du traitement, le droit à la portabilité des données, le droit d'opposition et le droit de ne pas faire l'objet d'une décision individuelle automatisée. Ces droits visent à protéger la vie privée des utilisateurs et à leur donner plus de contrôle sur leurs informations personnelles.

10) Qu’est-ce que le principe de minimisation des données selon le RGPD ?
Les organisations doivent réfléchir soigneusement à quelles données elles collectent, pourquoi elles en ont besoin et pendant combien de temps elles doivent les conserver.
Elles doivent également informer les individus de la manière dont leurs données seront utilisées et obtenir leur consentement avant de collecter leurs données.

En appliquant le principe de minimisation des données, les organisations peuvent réduire les risques de violation de la vie privée et de fuite de données, tout en renforçant la confiance des individus dans la manière dont leurs données sont traitées. Il s'agit d'un élément clé de la conformité au RGPD et de la protection efficace des données personnelles.
 
 
 ## SEO

1) Qu’est-ce que le SEO ?
Search Engine Optimization

2) Quel est l’objectif principal du SEO ?
Le SEO vise à améliorer le classement d'un site web dans les résultats des moteurs de recherche en optimisant divers aspects tels que le contenu,
les balises, les liens et la vitesse de chargement, afin d'attirer plus de trafic organique et augmenter sa visibilité en ligne.

3) Existe-t-il plusieurs types de référencement ? Lesquels ?
Il existe plusieurs types de référencement, tels que le référencement naturel (SEO), le référencement payant (SEA), le référencement local, le référencement
sur les réseaux sociaux, le référencement vidéo et le référencement mobile. Chacun de ces types vise à améliorer la visibilité d'une entreprise en ligne sur
les moteurs de recherche, les réseaux sociaux ou les plateformes vidéo, en fonction de ses besoins et objectifs spécifiques. Ces différentes stratégies de
référencement peuvent être utilisées de manière complémentaire pour renforcer la présence en ligne d'une entreprise et augmenter son audience.

4) Qu’est-ce que la densité de mots-clés en SEO ?
La densité de mots-clés en SEO est la fréquence à laquelle un mot-clé est utilisé par rapport au nombre total de mots sur une page web.
C'est un facteur important pour l'optimisation des moteurs de recherche, mais l'abus de mots-clés peut être préjudiciable au classement.
Il est essentiel de maintenir une densité naturelle tout en offrant un contenu pertinent et utile aux utilisateurs.

5) Qu’est-ce qu’une balise « alt » ?
La balise "alt" en HTML est utilisée pour décrire le contenu des images aux personnes aveugles ou malvoyantes, ainsi qu'aux navigateurs qui ne peuvent
pas charger les images.
Elle est également bénéfique pour le référencement naturel car elle permet aux moteurs de recherche de mieux comprendre le contenu des images.

6) Qu’est-ce que la balise « meta description » ?
La balise meta description est une étiquette HTML permettant de définir une courte description du contenu d'une page web.
Elle apparaît dans les résultats des moteurs de recherche, sous le titre de la page, afin de donner aux utilisateurs une idée du contenu avant de cliquer.
Elle influence également le référencement naturel de la page, les moteurs de recherche l'utilisant pour déterminer la pertinence de la page par rapport à
une requête de recherche.

7) Qu’est-ce que le « nofollow » en SEO ?
Le "nofollow" en SEO est une valeur d'attribut dans les balises HTML qui indique aux moteurs de recherche de ne pas suivre les liens d'une page web,
ce qui peut aider à éviter les pénalités liées à des liens de faible qualité ou non naturels.

8) Quelle est l'importance du contenu de qualité pour le référencement d'un site web ?
En résumé, un contenu de qualité est crucial pour le référencement d'un site web car il améliore la pertinence, attire du trafic organique, augmente le temps
passé par les utilisateurs sur le site, réduit le taux de rebond, favorise les liens entrants naturels, et améliore l'autorité et la crédibilité du site.
Cela contribue à un meilleur classement dans les résultats des moteurs de recherche.

9) Pourquoi est-il important d'utiliser des balises de titre (h1, h2, h3, etc.) de manière structurée ?
L'utilisation structurée des balises de titre est essentielle pour améliorer l'accessibilité, le référencement, la clarté du contenu et la cohérence visuelle d'un site web.
Cela facilite la navigation pour les utilisateurs malvoyants, améliore le classement dans les moteurs de recherche, rend le contenu plus clair et organisé, et assure une présentation uniforme.

10) Quelle est la recommandation pour les URL d'un site web bien référencé ?
Pour un bon référencement de votre site web, utilisez des URL conviviales, simples, descriptives et contenant des mots-clés pertinents. Évitez les URL complexes,
privilégiez les tirets pour séparer les mots et maintenez des URLs cohérentes et statiques. Évitez les redirections et modifications fréquentes qui pourraient
affecter le référencement.

11) Qu'est-ce que le maillage interne et pourquoi est-il important pour le référencement ?
Le maillage interne d'un site web consiste en la structure des liens internes entre les différentes pages, ce qui aide les moteurs de recherche à indexer et classer les pages.
Il favorise le transfert de pertinence et de popularité entre les pages, améliorant ainsi le référencement et l'expérience utilisateur.
En résumé, le maillage interne est essentiel pour l'optimisation du site, son référencement et la navigation des visiteurs.

12) Qu'est-ce que l'optimisation des images pour le référencement ?
L'optimisation des images pour le référencement vise à améliorer la visibilité et la pertinence des images sur un site web afin d'optimiser leur référencement dans
les moteurs de recherche. Cela implique l'optimisation du balisage des images, la compression des fichiers, le choix de noms de fichiers pertinents et des dimensions
adaptées, ainsi que la création de sitemaps dédiés aux images. Cette pratique permet d'améliorer le positionnement des images dans les résultats de recherche et d'attirer
plus de trafic qualifié sur le site.

13) Qu'est-ce qu'un plan de site (sitemap) et pourquoi est-il important pour le référencement ?
Un plan de site (sitemap) est un fichier XML qui répertorie toutes les pages d'un site web et indique leur structure, leur organisation et leurs liens entre elles.
Il permet aux moteurs de recherche de comprendre en profondeur le contenu du site et de l'indexer de manière plus efficace.
Un plan de site bien conçu est essentiel pour optimiser le référencement d'un site web en aidant les moteurs de recherche à indexer efficacement son contenu et à
le classer plus efficacement dans les résultats de recherche.

## Gestion de projets / DevOps

1) Qu’est-ce que la gestion de projet ?
La gestion de projet en programmation consiste à planifier, organiser et contrôler les différentes tâches pour mener à bien un projet de développement logiciel.
Cela implique de définir les objectifs, estimer les ressources, créer un calendrier, suivre la progression et garantir l'efficacité et la qualité du processus
de développement.

2) Qu’est-ce qu’une méthode Agile de gestion de projet ?
Grâce à sa flexibilité et sa capacité à s'adapter aux changements, la méthode Agile est devenue de plus en plus populaire dans de nombreux secteurs,
notamment le développement logiciel, le marketing, la gestion de projet, les ressources humaines, etc. En adoptant une approche Agile, les équipes peuvent
mieux gérer les risques et les imprévus, tout en restant focalisées sur la satisfaction des clients et la livraison de produits de qualité.

En résumé, la méthode Agile est une approche de gestion de projet innovante qui favorise la collaboration, l'adaptabilité et la livraison continue de produits de haute qualité. Elle permet aux équipes de travailler de manière efficace et transparente, en s'adaptant rapidement aux changements et aux retours des parties prenantes.

3) Expliquer la méthode MoSCoW en quelques lignes et citer ses avantages
La méthode MoSCoW est une technique de priorisation des besoins qui consiste à classer les fonctionnalités en quatre catégories : Must have, Should have, Could have
et Won't have. Elle permet de définir clairement les besoins essentiels, de hiérarchiser les fonctionnalités et de faciliter la prise de décision, la gestion des
attentes et la planification des ressources. Ses avantages incluent une meilleure compréhension des priorités, une approche pragmatique pour gérer les contraintes
de temps et de ressources, une communication claire et une réduction des risques.

4) A quoi sert la méthodologie MVP ? Citer les caractéristiques clés
La méthodologie MVP consiste à développer un produit ou un service avec un minimum de fonctionnalités pour répondre aux besoins des utilisateurs.
Les avantages incluent des coûts réduits, une rapide acquisition de retours des utilisateurs, des tests de viabilité et une rapide itération pour optimiser
le produit, ainsi qu'une économie de temps dans la conception et le développement.

5) Qu’est-ce que la planification itérative ?
La planification itérative est une méthode de gestion de projet qui consiste à diviser le travail en cycles répétitifs. Chaque itération correspond à une période
pendant laquelle une partie du travail est réalisée et évaluée. Cette approche permet d'obtenir des résultats plus rapidement, de s'adapter aux changements
et d'améliorer la planification grâce aux retours d'expérience. Utilisée principalement dans le développement logiciel, elle peut être appliquée à d'autres
types de projets.

6) Citer 3 méthodes Agiles dans le cadre d’un projet informatique
- Scrum est une méthode agile populaire basée sur des itérations de développement appelées "sprints"
- Kanban est une méthode visuelle de gestion du travail basée sur des cartes
- Extreme Programming se concentre sur la qualité du code et la collaboration au sein de l'équipe de développement.

7) Qu’est-ce qu’une réunion de revue de projet ?
La réunion de revue de projet est un moment clé pour évaluer, ajuster et prendre des décisions importantes afin de garantir la réussite du projet.
Elle favorise la transparence, la communication et la collaboration au sein de l'équipe.

8) Qu’est-ce qu’un livrable dans un projet ?
Un livrable dans un projet est un élément concret ou tangible qui doit être produit, achevé ou remis à un moment donné lors du déroulement du projet.
Il contribue à l'atteinte des objectifs du projet et peut prendre différentes formes, telles que des rapports, des prototypes, des plans, des documentations,
des logiciels, des installations, etc. Les livrables sont définis dès le début du projet et font l'objet de validations et de vérifications tout au long du projet.

9) Quels sont les 3 piliers SCRUM ? Définir chacun d’entre eux
les 3 piliers de SCRUM sont la transparence, l'inspection et l'adaptation. Ils sont essentiels pour assurer le bon déroulement d'un projet SCRUM en favorisant
la communication, l'évaluation continue du travail et la capacité d'ajustement face aux changem

10) Qu’est-ce que le DevOps et quel est son objectif principal ?
Le DevOps favorise la collaboration entre les équipes de développement et d'opérations pour améliorer la qualité et la rapidité de livraison des logiciels
en automatisant les processus de développement, de test et de déploiement. Son objectif est d'assurer une livraison continue et rapide des produits logiciels
tout en garantissant leur stabilité et leur fiabilité, et de promouvoir une culture de collaboration et de responsabilité partagée au sein des équipes.

11) Qu’est-ce que l’intégration continue ?
L'intégration continue est une pratique qui vise à automatiser le processus d'intégration des codes source pour détecter et résoudre rapidement les erreurs,
assurer la cohérence et la qualité du code, et réduire les risques liés au développement logiciel. Cette méthode repose sur l'utilisation d'outils et de
processus automatisés pour compiler, tester et déployer les modifications du code source dans un environnement de développement partagé.

12) Qu’est-ce que Docker ? Et en quoi est-il utile dans le cadre du DevOps ?
Docker est une plateforme logicielle permettant de créer, déployer et gérer des conteneurs logiciels, facilitant ainsi le déploiement et la gestion des
applications dans le cadre du DevOps. En utilisant des conteneurs Docker, les équipes de développement peuvent garantir une uniformité de fonctionnement sur
tous les environnements, évitant ainsi les problèmes liés aux différences entre ces environnements. Docker permet également de mettre en place des
pipelines CI/CD efficaces, d'automatiser le déploiement des applications et de réaliser des économies en termes de ressources matérielles tout en facilitant
la scalabilité des applications.

13) Qu’est-ce qu’un test unitaire ?
Les tests unitaires sont une pratique de programmation visant à tester de manière isolée et automatique une partie spécifique du code source d'un logiciel,
afin de garantir son bon fonctionnement et de détecter rapidement les erreurs. Cette approche permet d'assurer la qualité du logiciel, d'améliorer sa maintenance
et sa fiabilité, tout en favorisant le développement agile.

14) Quelle est l'unité de code testée lors d'un test unitaire ?
L'unité de code testée lors d'un test unitaire est généralement une fonction ou une méthode spécifique dans le code source. Cette unité de code est testée
de manière isolée pour vérifier son bon fonctionnement dans différentes conditions.

15) Quelles sont les caractéristiques d'un bon test unitaire ?
Les bons tests unitaires sont indépendants, isolés, répétables, rapides, lisibles, pertinents, fiables et bien documentés.
Ils aident à améliorer la qualité du code et à réduire les erreurs dans les applications logicielles.

16) Qu'est-ce qu'une assertion dans un test unitaire ?
Avec les assertions, on vérifie si une partie du code se comporte comme prévu lors d'un test unitaire. Si une assertion échoue,
le test échoue et le code ne fonctionne pas correctement. Les assertions sont importantes pour garantir la qualité du code.

 
 ## English

1) What does JavaScript enable you to do on a website ?
a. Add interactive behavior and dynamic content

2) Which programming language is primarily used for server-side web development ?
a. PHP

3) What is the purpose of a web browser ?
a. To render and display web pages

4) What is the difference between GET and POST methods in HTTP ?
a. GET retrieves data from a server, while POST submits data to a server
GET method is used to retrieve data from a server without modifying it, while POST method is used to submit data to a server to create or update resources.
GET requests are less secure and have limitations on the amount of data that can be sent, while POST requests are more secure and have no limitations on data size.

5) What is the purpose of version control systems (e.g., Git) in web development ?
a. To track changes and manage collaborative development
Version control systems like Git are essential in web development to track changes made to the codebase, allowing developers to revert to previous versions if
needed and maintain an organized record of changes. It also enables collaboration between team members by managing simultaneous edits to the codebase and merging
changes seamlessly. Overall, version control systems help streamline the development process and ensure code quality and consistency.

6) What is the purpose of a framework in web development ?
a. To provide a structured environment for building web applications
Frameworks in web development provide a pre-built structure and set of tools to streamline the process of building web applications. They offer libraries,
templates, and best practices that help developers organize code, improve efficiency, and maintain consistency throughout a project.Frameworks also often include
built-in security features, database access, and other functionalities that can help developers create robust and reliable web applications.

7) What does NoSQL stand for ?
a. Not Only SQL

8) Which of the following is a characteristic of NoSQL databases ?
c. Scalability and flexible data models
