---
title: Ekylibre 0.3.1 alpha 1 has been released
name: ekylibre-0-3-1-alpha-1
---
This version normalize code in order to have a true MVC1 RESTful system.

#### From MVC1.5 to MVC1

The notion of MVC1.5 doesn't exist but the older conception of Ekylibre could be its definition:

  - MVC1 : *x* models ⇒ *x* controllers
  - MVC2 : *x* models ⇒ *1* controller

and in Ekylibre, we had:

  - MVC1.5 : *x* models ⇒ *y* controllers where 1 < *y* < *x*

We can see now that the former 6 controllers were exploded into 93 resource controllers. 3 new controllers appears too: Dashboards, Interfacers and Settings.

#### New clean menu

The controllers changes required the rewrite of the menu management system. Now menu structure is defined in a config file *config/menu.rb*. This system keep the concept : Only one way to go to a part of the application.

#### New side bar

The side bar contains now only the actions of the selected sub-menu. It leaves place for the help which comes here now.

Consequence: standalone help panel doesn't exist anymore.

#### Always instable

It remains bugs across the app due to the main change on controllers.
