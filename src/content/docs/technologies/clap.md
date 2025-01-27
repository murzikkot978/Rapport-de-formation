---
title: Clap
---

Ligne de commande Argument Parser pour Rust

Il s'agit d'une bibliothèque simple à utiliser, efficace et complète pour analyser les arguments de ligne de commande et
les sous-commandes lors de l'écriture de la console, ou des applications terminales.

## Qu'est que c'est Clap

clap est utilisé pour analyser et valider la chaîne de arguments de ligne de commande fournie par l'utilisateur au
moment de l'exécution. Vous fournissez la liste des possibilités valables, et clap manipule le reste. Cela signifie:
vous vous concentrez sur votre demandes fonctionnalité, et moins sur l'analyse et la validation de arguments.

clap fournit également la version traditionnelle et aide à changer (ou drapeaux) «pour des caractères libres»
automatiquement sans configuration. Il le fait en vérifiant la liste des possibilités valables que vous fourni et
n'ajoutant que ceux que vous n'avez pas déjà définis. Si vous utilisez des sous-commandes, clap sera également
auto-généréa a help sous-commande pour vous en plus des drapeaux traditionnels.

Une fois clap analyse l'utilisateur a fourni une chaîne d'arguments, il retourne les correspondances avec n'importe quel
valeurs applicables. Si l'utilisateur a commis une erreur ou une faute de frappe, clap les informe de l'erreur et sort
gracieusement (ou retourne un Result et vous permet d'effectuer n'importe quel nettoyage avant la sortie). Pour cette
raison, vous pouvez faire des hypothèses raisonnables dans votre code sur la validité de les arguments.

```rs
#[derive(Parser)]
struct Flag {
    #[arg(long)]
    delete: bool,

    #[arg(long)]
    done: bool,

    #[arg(long)]
    undone: bool,

    #[arg(long)]
    due: Option<String>,

    #[arg(long)]
    list: bool,

    #[arg(long)]
    sort: bool,

    #[arg(long, default_value_t = 0)]
    id: usize,
}
```