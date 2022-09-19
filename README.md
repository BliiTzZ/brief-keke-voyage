# Conception de la base de données

## Table des matières
 1. [Contexte du projet](#contexte-du-projet)
 2. [Critères de performance](#critères-de-performance)
 3. [Livrable](#livrable)  
   3.1. [Pour la base de données](#pour-la-base-de-données)  
   3.2. [Pour l'application](#pour-lapplication)

## Contexte du projet

Votre client, une agence de voyages, souhaite proposer la possibilité de réserver en ligne des billets d'avion à leurs clients.
Votre mission est de concevoir à l'aide du standard UML la modélisation de la plateforme.
La plateforme devra permettre que :

- Un vol est ouvert à la réservation et refermé sur ordre de la compagnie.
- Un vol peut être annulé par la compagnie
- Un client peut réserver un ou plusieurs vols, pour des passagers différents.
- Une réservation concerne un seul vol et un seul passager.
- Une réservation peut être annulée ou confirmée.
- Un vol a un aéroport de départ et un aéroport d’arrivée.
- Un vol a un jour et une heure de départ, et un jour et une heure d’arrivée.
- Un vol peut comporter des escales dans des aéroports.
- Une escale a une heure d’arrivée et une heure de départ.
- Chaque aéroport dessert une ou plusieurs villes.
- Des compagnies aériennes proposent différents vols.

## Critères de performance

Un readme répertoriant les informations principales.
Tous les diagrammes doivent correspondre à la notation officielle du standard UML et Merise
Les diagrammes doivent être exportés en format images facilement consultables (jpeg, png).
Minimum d'un commit par diagramme.

La conception Merise doit respecter au minimum les 3 premières formes normales.

## Livrable

### Pour la base de données

- [ ] Un MCD,
- [ ] Un MLD,
- [ ] Un MPD.

### Pour l'application

- [ ] Un dictionnaire de données,
- [ ] Des règles de gestion,
- [ ] Un diagramme de cas d'utilisation,
- [ ] Un diagramme de classe,
- [ ] Un diagramme de séquence.
  
*Ce projet a été réalisé en travail de groupe par :*
- ***Yacine Ponsot***
- ***Sébastien Mouret***
- ***Julie Napoli***