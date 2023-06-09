# bdd-memo.md

**SGBD** = syst de gestion de BDD (principaux = Oracle, MySQL, Microsoft SQL Server, PostgreSQL)
Un système de gestion de base de données (SGBD) est le logiciel qui permet à un ordinateur de stocker, récupérer, ajouter, supprimer et modifier des données. Un SGBD gère tous les aspects primaires d'une base de données, y compris la gestion de la manipulation des données, comme l'authentification des utilisateurs, ainsi que l'insertion ou l'extraction des données. Un SGBD définit ce qu'on appelle le schéma de données ou la structure dans laquelle les données sont stockées.
Les outils que nous utilisons tous au quotidien nécessitent des SGBD en coulisse. Cela comprend les guichets automatiques bancaires, les systèmes de réservation de vols, les systèmes d'inventaire au détail et les catalogues de bibliothèques, par exemple.

**Système d'information** : Le système d’information (SI) est un ensemble de ressources et de dispositifs permettant de collecter, stocker, traiter et diffuser les informations nécessaires au fonctionnement d’une organisation (administration, entreprise…).
Il peut s’agir d’informations fiscales, financières, comptables, commerciales, managériales...
⚠️ Attention : le système d’information ne doit pas être confondu avec le système informatique. Le système informatique est un sous-ensemble du système d’information. Il regroupe l’ensemble des moyens informatiques nécessaires au traitement de l’information : ordinateurs, programmes, réseau, logiciels, etc.

**base de données** : Une base de données est un ensemble d'informations qui est organisé de manière à être facilement accessible, géré et mis à jour. Elle est utilisée par les organisations comme méthode de stockage, de gestion et de récupération de l’informations.
Les données sont organisées en lignes, colonnes et tableaux et sont indexées pour faciliter la recherche d'informations. Les données sont mises à jour, complétées ou encore supprimées au fur et à mesure que de nouvelles informations sont ajoutées. Elles contiennent généralement des agrégations d'enregistrements ou de fichiers de données, tels que les transactions de vente, les catalogues et inventaires de produits et les profils de clients.

**Concepts de Base** : https://www.univ-constantine2.dz/CoursOnLine/Benelhadj-Mohamed/co/Grain_3_1.html
Individu : famille d'objets ayant une existence propre et d'intérêt pour le concepteur. Exemple : Auteur, Livre, ...
Propriété : particule élémentaire d'information appelée aussi caractéristique. Elle décrit un individu ou une relation. Exemple : Nom_Auteur, Prénom_Auteur.
Occurrence : une occurrence d'un individu-type est un membre de la famille d'objets « individu ».
Chaque occurrence doit être distinguable au sein de sa famille. Toutes les occurrences doivent être dotées des mêmes propriétés.
Identifiant : permet de distinguer toutes les occurrences de la famille d'objet.
Entité : L'entité d'un individu est la liste des propriétés décrivant cet individu.

Chaque entité est unique et est décrite par un ensemble de propriétés. Une des propriétés de l'entité est l'identifiant. Cette propriété doit posséder des occurrences uniques et doit être source (partie gauche) des dépendances fonctionnelles avec toutes les autres propriétés de l'entité. Bien souvent, on utilise un code unique spécifique du contexte.

**MCD** (modèle conceptuel de données) : Le modèle conceptuel des données (MCD) a pour but d'écrire de façon formelle les données qui seront utilisées par le système d'information. Il s'agit donc d'une représentation des données, facilement compréhensible, permettant de décrire le système d'information à l'aide d'entités.
Une entité est la représentation d'un élément matériel ou immatériel ayant un rôle dans le système que l'on désire décrire.
https://web.maths.unsw.edu.au/~lafaye/CCM/merise/mcd.htm

On appelle classe d'entité un ensemble composé d'entités de même type, c'est-à-dire dont la définition est la même. Le classement des entités au sein d'une classe s'appelle classification (ou abstraction). Une entité est une instanciation de la classe. Chaque entité est composée de propriétés, données élémentaires permettant de la décrire.

Prenons par exemple une Ford Fiesta, une Renault Laguna et une Peugeot 306. Il s'agit de 3 entités faisant partie d'une classe d'entité que l'on pourrait appeler voiture. La Ford Fiesta est donc une instanciation de la classe voiture. Chaque entité peut posséder les propriétés couleur, année et modèle.

Les classes d'entités sont représentées par un rectangle. Ce rectangle est séparé en deux champs :
le champ du haut contient le libellé. Ce libellé est généralement une abréviation pour une raison de simplification de l'écriture. Il s'agit par contre de vérifier qu'à chaque classe d'entité correspond un et un seul libellé, et réciproquement
le champ du bas contient la liste des propriétés de la classe d'entité

**MLD** (modèle logique de données) : Le modèle logique de données, MLD, consiste à représenter et transposer les entités du modèle conceptuel de données, le MCD sous forme de tables de base de données puis les associations sous forme de clés étrangères ou tables associatives.

**Passer d'un MCD à un MLD** : règles de passage https://www.univ-constantine2.dz/CoursOnLine/Benelhadj-Mohamed/co/grain7_2.html
Propriété: Une propriété devient un attribut.
Individu: Un individu devient une relation (minimum en 3ème forme normale).
Identifiant: L'identifiant d'un individu devient la clé primaire de la relation correspondante.
Association sans propriétés propres

Cardinalités (0,1) ou (1,1) vers (0,n) ou (1,n) : L'association disparaît et la clé de la relation relative à la cardinalité (0,n) ou (1,n) migre vers la relation relative à la cardinalité (0,1) ou (1,1). Cette clé est appelé "clé étrangère".

Cardinalités (0,n) ou (1,n) vers (0,n) ou (1,n): L'association devient une relation avec comme clé la concaténation des clés des 2 relations.

Associations avec propriétés propres : Comme dans le cas précédent, l'association devient une relation ayant comme clé la concaténation des clés des relations associées à chaque individu. Les propriétés propres de l'association deviennent des attributs de cette relation.




**KIT 2**

Créer une BDD --> collection de tableaux, dans chaque tableau on a nos données réelles organisées en col et row
langage utilisé pour manipuler et lire les données

**CREATE DATABASE nomBdd; **

pour visualiser : **SHOW DATABASES;**

Faire un commentaire: **--** commentaire

Créer table / colonnes --> ici colonnes id, email, etc 
**CREATE TABLE NomTable(
    id,
    email,
    etc,
);

types de données qu'on utilise le plus souvent

contraintes utiles colonnes: valeur obligatoire, définir l'id d'une table ?

Comment préciser que la valeur d'une colonne doit être unique ?(pour une adresse email par
exemple) : 
**VALUES (
     'nanana@gmail.com',
);**

Comment insérer des données dans une table ?

Comment récupérer les données insérées ?

Comment ne sélectionner qu'un certain nombre de résultats ? **LIMIT nbdeRésultatsSouhaités; **

Comment trier les résultats ? **ORDER BY**

Comment filtrer les données et chaîner les conditions de filtres ? **WHERE element = 'name'** 

Comment filtrer une colonne avec une valeur commençant par un certain caractère ? **AND** ou **OR** pour être plus précis **AND element LIKE 'type'**

A quoi servent les INDEX ? Comment en créer ? permet de récupérer les données plus rapidement 
**CREATE INDEX type_index ON table(type);**

Comment créer une relation entre 2 tables ? **LEFT/RIGHT/INNER/OUTER JOIN**

Comment sélectionner les données de plusieurs tables ?

Comment ne sélectionner que certaines colonnes et les renommer dans la liste de résultats ?

Comment supprimer une table et une base de données ? **DROP TABLE/DATABASE**

**SQLite** : SQLite est une bibliothèque en langage C qui implémente un moteur de base de données SQL petit , rapide , autonome , hautement fiable et complet . SQLite est le moteur de base de données le plus utilisé au monde. SQLite est intégré à tous les téléphones mobiles et à la plupart des ordinateurs et est fourni avec d'innombrables autres applications que les gens utilisent quotidiennement.



**PHP**

Apach : Apache est le serveur web. Son rôle est d'écouter les requêtes émises par les navigateurs (qui demandent des pages web), de chercher la page demandée et de la renvoyer.

Navigateur : Un navigateur web est un logiciel conçu pour consulter et afficher le World Wide Web. Techniquement, c'est au minimum un client HTTP. Le rôle des navigateurs est de traduire les langages HTML, CSS et JavaScript sous la forme de sites web utilisables par tout le monde.

PHP : PHP est principalement conçu pour servir de langage de script coté serveur, ce qui fait qu'il est capable de réaliser tout ce qu'un script CGI quelconque peut faire, comme collecter des données de formulaire, générer du contenu dynamique, ou gérer des cookies.

Langage client : clients = votre ordinateur qui sert à aller consulter des sites web.Pour construire un site web, on a recours à des langages. Ils servent en quelque sorte à établir les plans d’architecte dont on a besoin pour construire les sites. Ces langages sont principalement : HTML, CSS, JavaScript
Tous ces langages sont désormais indispensables à la réalisation de tous les sites web. On dit que ce sont des langages client ou encore des langages frontend, car ils sont lus par les machines des clients.

Langage serveur : ce sont des ordinateurs spéciaux (souvent très puissants) qui envoient les sites web aux clients. Les serveurs "possèdent" les sites web et les distribuent à ceux qui veulent les visiter. Les langages serveur sont, comme leur nom l’indique, gérés par les serveurs. Les clients n’y touchent pas. Leur rôle est un peu différent :
Les langages client décrivent comment le site web doit s’afficher, les langages serveur décrivent comment le site web doit se comporter. Subtil, mais important !
Avec un langage client, je peux dire "Un menu doit s’afficher à gauche de mon site web".
Avec un langage serveur, je peux dire "Le menu ne doit s’afficher que si cette personne a créé un compte sur mon site".
Quelques exemples : PHP, Java (rien à voir avec JavaScript, attention !), Python, C#

Protocole HTTP : 

Serveur Web :








