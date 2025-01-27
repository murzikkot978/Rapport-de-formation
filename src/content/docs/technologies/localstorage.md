---
title: Localstorage
---

La propriété localStorage vous permet d'accéder à un objet local Storage. Le localStorage est similaire au
sessionStorage. La seule différence : les données stockées dans le localStorage n'ont pas de délai d'expiration, alors
que les données stockées dans le sessionStorage sont nettoyées quand la session navigateur prend fin — donc quand on
ferme le navigateur.

## Example

```JS
localStorage.setItem("monChat", "Tom")
```

```JS
var cat = localStorage.getItem("monChat")

```