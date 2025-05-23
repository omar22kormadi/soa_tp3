# SOA TP3 – API GraphQL de gestion de tâches

Ce projet propose une API Node.js basée sur Express et Apollo Server, permettant de gérer des tâches via GraphQL.

## Fonctionnalités

- **Lister toutes les tâches**
- **Récupérer une tâche par ID**
- **Ajouter une tâche**
- **Marquer une tâche comme complétée**

## Prérequis

- Node.js (>= 14)
- npm

## Installation

1. Clonez le dépôt et placez-vous dans le dossier `tp3` :
   ```bash
   git clone <url-du-repo>
   cd SOAtp/tp3
   ```

2. Installez les dépendances :
   ```bash
   npm install
   ```

3. Lancez le serveur :
   ```bash
   node index.js
   ```

## Utilisation

L’API GraphQL est disponible à l’adresse :  
[http://localhost:5000/graphql](http://localhost:5000/graphql)

### Exemple de requête GraphQL

```graphql
query {
  tasks {
    id
    title
    description
    completed
  }
}
```

### Exemple de mutation

```graphql
mutation {
  addTask(title: "Nouvelle tâche", description: "Description", completed: false) {
    id
    title
    completed
  }
}
```

## Structure du projet

- `index.js` : Point d’entrée, configuration du serveur Express et Apollo.
- `taskSchema.gql` : Schéma GraphQL des tâches.
- `taskSchema.js` : Chargement et compilation du schéma.
- `taskResolver.js` : Résolveurs pour les requêtes et mutations.

## Auteur

- [Amor Kormadi]
