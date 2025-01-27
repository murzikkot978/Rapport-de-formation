---
title: Serde
---

Serde est un cadre pour la sérialisation et la désérialisation données Rust structure de manière efficace et générique.

L'écosystème Serde se compose de structures de données qui savent sérialiser et s'éneraliser avec les formats de données
qui savent comment sérialiser et désérialiser d'autres choses. Serde fournit la couche par laquelle ces deux groupes
interagissent l'un avec l'autre, permettant toute donnée supportée structure à sérialiser et désérialiser en utilisant
tout format de données pris en charge.

## Conception

Là où de nombreux autres langages reposent sur la réflexion sur les runtimes pour la sérialisation des données, Serde
est plutôt construit sur le puissant système de traits de Rust. Structure des données qui sait comment s'entérialiser et
se désérialiser est un qui met en œuvre Serde Serialize et Deserialize (ou utilise Serde’s dérivé attribut pour générer
automatiquement des implémentations au moment de la compilation). C'est ce que évite toute rétroaction d'informations de
type réflexion ou d'exécution. En fait, dans l'interaction entre la structure des données et le format des données peut
être complètement optimisés par le compilateur Rust, en laissant Serde sérialisation pour effectuer la même vitesse
qu'un sérialiseur manuscrit pour le sélection spécifique de la structure des données et du format des données.

```rs
// constrain output types to have the `Deserialize` trait
fn deserialize<'a, T>(data: &'a [u8]) -> T where T: Deserialize<'a> {
    let msg = str::from_utf8(data).unwrap();
    serde_json::from_str::<T>(msg).unwrap()
}

// shorthand for the above when `T` isn't needed in the function body
fn serialize(object: &impl Serialize) -> String {
    let msg = serde_json::to_string(object).unwrap();
    return msg;
}
```