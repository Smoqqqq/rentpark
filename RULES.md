# Règles à respecter pour un projet en groupe

Créer une branche pour développer la fonctionnalitée
-> une fois la fonctionnalitée développée et testée, créer une pull request
-> demander la validation de la pull request à quelqu'un (merge la pull request)
-> retourner sur la branche `main / master` 
-> git pull
-> git merge main pour mettre à jour une ancienne branche

# Conventions 

## Routes
les routes API se présente comme ci dessous (exemple avec garage):

| Action    | URL                   | "Verbe" / méthode HTTP    |
| ----------|-----------------------|---------------------------|
| Create    | /garage/create        | POST                      |
| Read      | /garage/:id           | GET                       |
| Update    | /garage/:id/update    | POST / PATCH              |
| Delete    | /garage/:id/delete    | DELETE                    |

## Variables
Case à utiliser: camelCase (premier mot sans majuscule, les suivants avec une majuscule):

✅ nomDeVariable
❌ NomDeVariable
❌ nom_de_variable
❌ nomdevariable

### Nom des variables
Donner un nom clair qui exprime clairement ce que représente la variable :

```javascript
// BAD ❌ 
let x = 15;
let y = 10;

let z = x + y;
let v = x * 0.2;

// GOOD ✅
let prix = 15;
let livraison = 10;

let total = prix + livraison;
let tva = prix * 0.2;
```