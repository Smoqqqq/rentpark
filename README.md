# PROJET LOCATION GARAGES

## DEMANDE

- proposer la location de garages par des utilisateurs
- permettre la mise en relation entre loueur et client
- offrir une interface de mise en ligne d'annonce pour les garages par les loueurs

## PAGES

- inscription
- connexion
- mon compte
- ajout d'une annonce
- mes annonces
- liste des annonces
- réservation d'une annonce

## TECHNOLOGIES

- BACK END:
    - NodeJs
    - Mongo ou MySql ?

- FRONT END:
    - React ?
    - Bootstrap

- App mobile:
    - Kotlin ?

# RÉPARTITION

Mehdi:
    - Back end + front

Jong:
    - Back end + front

Paul:
    - Application mobile

Alexis ?

## ENTITÉES BASE DE DONNÉE

### Garage
| COLUMN NAME   | COLUMN TYPE                   | NULLABLE      |
|---------------|-------------------------------|---------------|
| id            | Integer                       |               |
| name          | String                        |               |
| description   | String                        | true          |
| volume        | Float                         |               |
| width         | Float                         |               |
| height        | Float                         |               |
| owner         | FOREIGN KEY (user::id)        |               |
| address       | FOREIGN KEY (address::id)     |               |

### User
| COLUMN NAME   | COLUMN TYPE   | NULLABLE      | ATTRIBUTES    |
|---------------|---------------|---------------|---------------|
| id            | Integer       |               |               |
| username      | String        |               |               |
| email         | String        |               | UNIQUE        |
| passdword     | String        |               |               |
| roles         | JSON          |               |               |
| about         | String        | true          |               |

### Address
| COLUMN NAME   | COLUMN TYPE   | NULLABLE      |
|---------------|---------------|---------------|
| id            | Integer       |               |
| line1         | String        |               |
| line2         | String        | true          |
| zipcode       | Integer       |               |
| city          | String        |               |
| country       | String        |               |

### Booking
| COLUMN NAME   | COLUMN TYPE                   | NULLABLE      |
|---------------|-------------------------------|---------------|
| id            | Integer                       |               |
| user          | FOREIGN KEY (user::id)        |               |
| garage        | FOREIGN KEY (garage::id)      |               |
| startDate     | Date                          |               |
| endDate       | Date                          |               |
| price         | Float                         |               |