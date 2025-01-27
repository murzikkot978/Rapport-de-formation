---
title: Fetch
---

fetch() est une API native de JavaScript qui permet de faire des requêtes HTTP/HTTPS (comme GET, POST, PUT, DELETE,
etc.) pour communiquer avec des serveurs et récupérer ou envoyer des données. C'est une méthode moderne, introduite avec
ECMAScript 6 (ES6), qui remplace en partie les anciennes méthodes comme XMLHttpRequest.

## Example

```JS
fetch('https://jsonplaceholder.typicode.com/posts')
  .then(response => {
    if (!response.ok) {
      throw new Error('Erreur : ' + response.status)
    }
    return response.json()
  })
  .then(data => {
    console.log(data)
  })
  .catch(error => {
    console.error('Erreur lors de la requête :', error)
  })
```