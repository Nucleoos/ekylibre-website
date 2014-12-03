---
title: Ekylibre 0.3.1 en version alpha 1
name: ekylibre-0-3-1-en-version-alpha-1
---
Pour faciliter la maintenance, rendre le code plus lisible et être plus fidèle à l’esprit de Ruby on Rails, il a été nécessaire de revoir tous les contrôleurs pour qu’ils soient plus RESTful.
De MVC1.5 à MVC1

La notion MVC1.5 n’existe pas en tant que telle mais l’ancienne conception d’Ekylibre pourrait en être une définition :

  - MVC1 : x modèles ⇒ x contrôleurs
  - MVC2 : x modèles ⇒ 1 contrôleur

et pour Ekylibre, nous avions :

  - MVC1.5 : x modèles ⇒ y contrôleurs où 1 < y < x

Ainsi dans cette version d’Ekylibre, il sera possible de constater que les 6 contrôleurs principaux correspondant directement aux différents modules ont été éclatés en 93 contrôleurs qui correspondent aux modèles/ressources. À ces derniers s’ajoutent, 3 nouveaux contrôlleurs pour la gestion des tableaux de bords, de certains éléments d’interface et des paramètres globaux.

#### Nouveau menu plus clair

Ce modification a entraîné la révision complète du système de gestion de menus qui se faisait de manière automatique. Maintenant la configuration des menus se fait dans un fichier de configuration dédié config/menus.yml. Grâce à cela, toutes les actions sont répertoriées de manière unique et il est possible de savoir en permanence dans quelle partie de l’application l’action se déroule.

#### Nouvelle barre latérale

La barre latérale qui servait au menu du module a été revue. Dans la nouvelle interface, elle ne contient plus que les actions du sous-menu sélectionné, ce qui laisse de la place libre. Pour cette raison, la barre d’aide a migré a cet emplacement.

La barre latérale (gauche) dédiée à l’aide n’existe plus en tant que telle.

#### Encore en test

Même si l’éclatement des contrôleurs s’est effectué en partie automatiquement, des bugs dû à ce grand changement subsistent encore un peu partout. N’hésitez pas à faire remonter tout bug dans l’application (Téléchargement de la version 0.3.1.a1).
