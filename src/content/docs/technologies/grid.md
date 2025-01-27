---
title: Grid
---

Le module CSS Grid layout (modèle de disposition en grille) est un module de la spécification CSS qui permet de créer
des mises en page en divisant l'espace d'affichage en régions utilisables par une application ou en définissant des
relations de taille, position et d'empilement entre les éléments HTML.

Comme les tableaux, la grille permet d'aligner des éléments sous forme de colonnes et de lignes mais à la différence des
tableaux, la grille n'a pas de structure de contenu. Ainsi, on peut créer de nombreuses mises en page qui n'auraient pas
été possibles avec les tableaux. Ainsi, les éléments fils d'un conteneur en grille peuvent être positionnés afin qu'ils
se chevauchent ou qu'ils se comportent comme des éléments positionnés.

## Example

```HTML
<div class="wrapper">
  <div class="one">Un</div>
  <div class="two">Deux</div>
  <div class="three">Trois</div>
  <div class="four">Quatre</div>
  <div class="five">Cinq</div>
  <div class="six">Six</div>
</div>
```

```CSS
.wrapper {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  grid-gap: 10px;
  grid-auto-rows: minmax(100px, auto);
}
.one {
  grid-column: 1 / 3;
  grid-row: 1;
}
.two {
  grid-column: 2 / 4;
  grid-row: 1 / 3;
}
.three {
  grid-column: 1;
  grid-row: 2 / 5;
}
.four {
  grid-column: 3;
  grid-row: 3;
}
.five {
  grid-column: 2;
  grid-row: 4;
}
.six {
  grid-column: 3;
  grid-row: 4;
}

```