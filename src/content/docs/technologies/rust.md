---
title: Rust
---

![Rust logo](/Rapport-de-formation/rust-logo.svg)

Rust est un langage de programmation compilé multi-paradigme qui met l'accent sur la performance, la sûreté des types et
la concurrence. Il assure la sécurité mémoire (en), ce qui signifie que toutes les références pointent vers une mémoire
valide, sans nécessiter l'utilisation de techniques de gestion de la mémoire automatisée telles que le ramasse-miettes.
Afin d'assurer la sécurité de la mémoire et d'empêcher une situation de compétition aux données, son « vérificateur
d'emprunts » suit la durée de vie des objets de toutes les références dans un programme à la compilation.

## Performance

Rust est terriblement rapide et économe en mémoire : sans environnement d'exécution, ni ramasse-miettes, il peut
dynamiser des services à hautes performances, s'exécuter dans des systèmes embarqués, et s'intégrer facilement à d'
autres langages.

## Fiabilité

Le puissant système de typage et le modèle d’ownership de Rust garantissent la sécurité mémoire ainsi que la sécurité
des threads — et vous permettent d'éliminer de nombreuses variétés de bugs dès la compilation.

## Productivité

Rust dispose d'une excellente documentation, d'un compilateur bienveillant, avec des messages d'erreur utiles, et
d'outils de premier ordre — un gestionnaire de paquet et de compilation intégré, divers éditeurs intelligents avec
auto-complétion et analyse de type, un outil de mise en forme automatique et plus encore. 