# bdd-memo.md

**SGBD** = syst de gestion de BDD
Un système de gestion de base de données (SGBD) est le logiciel qui permet à un ordinateur de stocker, récupérer, ajouter, supprimer et modifier des données. Un SGBD gère tous les aspects primaires d'une base de données, y compris la gestion de la manipulation des données, comme l'authentification des utilisateurs, ainsi que l'insertion ou l'extraction des données. Un SGBD définit ce qu'on appelle le schéma de données ou la structure dans laquelle les données sont stockées.
Les outils que nous utilisons tous au quotidien nécessitent des SGBD en coulisse. Cela comprend les guichets automatiques bancaires, les systèmes de réservation de vols, les systèmes d'inventaire au détail et les catalogues de bibliothèques, par exemple.

**Système d'information** : Le système d’information (SI) est un ensemble de ressources et de dispositifs permettant de collecter, stocker, traiter et diffuser les informations nécessaires au fonctionnement d’une organisation (administration, entreprise…).
Il peut s’agir d’informations fiscales, financières, comptables, commerciales, managériales...
⚠️ Attention : le système d’information ne doit pas être confondu avec le système informatique. Le système informatique est un sous-ensemble du système d’information. Il regroupe l’ensemble des moyens informatiques nécessaires au traitement de l’information : ordinateurs, programmes, réseau, logiciels, etc.


**base de données** : Une base de données est un ensemble d'informations qui est organisé de manière à être facilement accessible, géré et mis à jour. Elle est utilisée par les organisations comme méthode de stockage, de gestion et de récupération de l’informations.
Les données sont organisées en lignes, colonnes et tableaux et sont indexées pour faciliter la recherche d'informations. Les données sont mises à jour, complétées ou encore supprimées au fur et à mesure que de nouvelles informations sont ajoutées. Elles contiennent généralement des agrégations d'enregistrements ou de fichiers de données, tels que les transactions de vente, les catalogues et inventaires de produits et les profils de clients.
Généralement, l’administrateur de la base de données régule les accès des utilisateurs afin de contrôler leurs actions et d’analyser les usages. Pour garantir la cohérence des données et l'intégralité des transactions, toutes les transactions réalisées sur une base de données doivent répondre aux exigences de la conformité ACID :
Le principe d’Atomicité garantit la bonne exécution de la transaction. Les transactions de base de données, comme les atomes, peuvent être décomposées en plus petites parties. Si une partie d'une transaction échoue, toute la transaction sera annulée.
La propriété de Cohérence signifie que seules les données qui suivent des règles prédéfinies peuvent être écrites dans la base de données.
L’isolement fait référence à la capacité de traiter simultanément plusieurs transactions de manière indépendante.
La durabilité requiert de rendre les défaillances invisibles pour l'utilisateur final. Les données sont sauvegardées une fois la transaction terminée, même en cas de panne de courant ou de défaillance du système.


**MCD** (modèle conceptuel de données) : Le modèle conceptuel des données (MCD) a pour but d'écrire de façon formelle les données qui seront utilisées par le système d'information. Il s'agit donc d'une représentation des données, facilement compréhensible, permettant de décrire le système d'information à l'aide d'entités.
Une entité est la représentation d'un élément matériel ou immatériel ayant un rôle dans le système que l'on désire décrire.
https://web.maths.unsw.edu.au/~lafaye/CCM/merise/mcd.htm

On appelle classe d'entité un ensemble composé d'entités de même type, c'est-à-dire dont la définition est la même. Le classement des entités au sein d'une classe s'appelle classification (ou abstraction). Une entité est une instanciation de la classe. Chaque entité est composée de propriétés, données élémentaires permettant de la décrire.

Prenons par exemple une Ford Fiesta, une Renault Laguna et une Peugeot 306. Il s'agit de 3 entités faisant partie d'une classe d'entité que l'on pourrait appeler voiture. La Ford Fiesta est donc une instanciation de la classe voiture. Chaque entité peut posséder les propriétés couleur, année et modèle.

Les classes d'entités sont représentées par un rectangle. Ce rectangle est séparé en deux champs :

le champ du haut contient le libellé. Ce libellé est généralement une abréviation pour une raison de simplification de l'écriture. Il s'agit par contre de vérifier qu'à chaque classe d'entité correspond un et un seul libellé, et réciproquement
le champ du bas contient la liste des propriétés de la classe d'entité


**MLD** (modèle logique de données) : Le modèle logique de données, MLD, consiste à représenter et transposer les entités du modèle conceptuel de données, le MCD sous forme de tables de base de données puis les associations sous forme de clés étrangères ou tables associatives.













