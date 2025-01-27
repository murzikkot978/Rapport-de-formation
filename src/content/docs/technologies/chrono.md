---
title: Chrono
---

Chrono est le nom d'un en-tête, mais aussi d'un sous-espace de prénom: Tous les éléments de cet en-tête (sauf pour le
type commun les spécialisations) ne sont pas définies directement dans le cadre de la std espace de noms (comme la
plupart de la bibliothèque standard) mais sous le std::chrono espace de noms.

```rs
use chrono::prelude::*;

let utc: DateTime<Utc> = Utc::now(); // e.g. `2014-11-28T12:45:59.324310806Z`
```

```rs
use chrono::prelude::*;

let local: DateTime<Local> = Local::now(); // e.g. `2014-11-28T21:45:59.324310806+09:00`
```