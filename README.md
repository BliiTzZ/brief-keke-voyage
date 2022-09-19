# Conception de la base de données

## Table des matières
 1. [Contexte du projet](#contexte-du-projet)
 2. [Critères de performance](#critères-de-performance)
 3. [Livrable](#livrable)  
   3.1. [Pour la base de données](#pour-la-base-de-données)  
   3.2. [Pour l'application](#pour-lapplication)
 4. [Règles de gestion](#règles-de-gestion)
 5.  [Dictionnaire de données](#dictionnaire-de-données)

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
- [x] Des règles de gestion,
- [ ] Un diagramme de cas d'utilisation,
- [ ] Un diagramme de classe,
- [ ] Un diagramme de séquence.

## Règles de gestion

### Client

- Peut réserver pour un ou plusieurs passagers.

### Réservation

- Concerne qu'un seul vol et un seul passager,
- Peut être annulée ou confirmée,
- Contient un numéro de réservation,
- Contient un nom, prénom et numéro de téléphone.

### Vol

- Contient un numéro de vol,
- Contient un aéroport de départ, une date et une heure,
- Contient un aéroport d'arrivée, une date et une heure,
- Contient un ou plusieurs passagers,
- Peut être ouvert à la réservation ou non par la compagnie,
- Peut être annulé par la compagnie,
- Peut faire des escales dans un aéroport,
- Est un trajet d'un aéroport de départ à un aéroport d'arrivé.

### Aéroport

- Se trouve dans une ville.

### Escale

- Se fait dans un aéroport,
- Contient une date et une heure d'arrivée,
- Contient une date et une heure de départ.

### Compagnie

- Propose différents vols,
- Contient un nom.

### Ville

- Contient un nom.

### Pays

- Contient un nom.

## Dictionnaire de données

| Code mnémonique         | Désignation                                                                                          | Type | Taille | Remarque                     |
| ----------------------- | ---------------------------------------------------------------------------------------------------- | ---- | ------ | ---------------------------- |
| number_booking          | Numéro de réservation                                                                                | AN   | 20     |                              |
| passeport_booking       | Code d'identification du passager                                                                    | AN   | 9      |                              |
| last_name_booking       | Nom du passager                                                                                      | A    | 50     |                              |
| first_name_booking      | Prénom du passager                                                                                   | A    | 50     |                              |
| date_of_birth_booking   | Âge du passager                                                                                      | DATE |        | Au format AAAA-JJ-MM         |
| email_booking           | Mail du passager ou d'un contact pour envoyer des documents par exemple : envoyer le billet          | AN   | 100    |                              |
| phone_number_booking    | Téléphone du passager ou de contact                                                                  | AN   | 15     |                              |
| price_booking           | Prix du vol                                                                                          | N    | 15     |                              |
| state_booking           | Définit le statut de la réservation, en attente, confirmer par la compagnie, annuler par le passager | N    |        |                              |
| date_booking            | Date de la réservation                                                                               | DATE |        | Au format AAAA-JJ-MM         |
| date_departure_flight   | Date et l'heure du départ du vol                                                                     | DATE |        | Au format AAAA-JJ-MM h\:m\:s |
| date_arrival_flight     | Date et l'heure du arrivée du vol                                                                    | DATE |        | Au format AAAA-JJ-MM h\:m\:s |
| number_of_flight        | Numéro d'identification du vol                                                                       | AN   | 10     |                              |
| state_flight            | Définit le statut du vol, annuler, ouvert, fermer                                                    | N    |        |                              |
| date_departure_stopover | Date et l'heure du départ de l'escale                                                                | DATE |        | Au format AAAA-JJ-MM h\:m\:s |
| date_arrival_stopover   | Date et l'heure du arrivée de l'escale                                                               | DATE |        | Au format AAAA-JJ-MM h\:m\:s |
| name_company            | Nom de la compagnie                                                                                  | AN   | 50     |                              |
| iata_code_company       | Identifiant de la compagnie aérienne                                                                 | AN   | 10     |                              |
| nom_airport             | Nom de l'aéroport                                                                                    | A    | 50     |                              |
| iata_code_airport       | Identifiant de localisation                                                                          | AN   | 10     |                              |
| name_city               | Nom d'une ville                                                                                      | A    | 50     |                              |
| name_country            | Nom d'un pays                                                                                        | A    | 50     |                              |

*Ce projet a été réalisé en travail de groupe par :*
- ***Yacine Ponsot***
- ***Sébastien Mouret***
- ***Julie Napoli***