# c-skin.scss

[Démo et documentation](https://ita-design-system.github.io/c-skin.scss/)

Composant CSS dédié aux aspects et apparences des éléments. 

## Scope

Liste des propriétés CSS utilisées par le composant

* [background-color](https://developer.mozilla.org/fr/docs/Web/CSS/background-color)
* [border](https://developer.mozilla.org/fr/docs/Web/CSS/border)
* [border-radius](https://developer.mozilla.org/fr/docs/Web/CSS/border-radius)
* [box-shadow](https://developer.mozilla.org/fr/docs/Web/CSS/box-shadow)
* [color](https://developer.mozilla.org/fr/docs/Web/CSS/color)
* [cursor](https://developer.mozilla.org/fr/docs/Web/CSS/cursor)
* [list-style](https://developer.mozilla.org/fr/docs/Web/CSS/list-style)
* [opacity](https://developer.mozilla.org/fr/docs/Web/CSS/opacity)
* [outline](https://developer.mozilla.org/fr/docs/Web/CSS/outline)
* [pointer-events](https://developer.mozilla.org/fr/docs/Web/CSS/pointer-events)

## Typologie d'un composant générique

```scss
// SCSS map
$briks-components-generic: ( 
    // SCSS map | Nom du composant
    NOM_DU_COMPOSANT: ( 
        // Boolean | Composant activé true ou false
        enabled: true, 
        // Boolean | Responsive activé true ou false
        responsive: true, 
        // SCSS map | Liste des propriétés du composant par défaut (c-skin seul)
        defaults: (), 
        // SCSS map | Liste des modifieurs
        modifiers: () 
    )
);
```

## Configuration

Organisation et description du fichier de configuration [_sass/_skin_generic.scss](_sass/_skin_generic.scss).

```scss
/*
    C-SKIN
    v0.1.0
    Composant générique CSS ITADS
    https://github.com/ita-design-system/c-skin.scss
*/
// SCSS map
$briks-components-generic: ( 
    // Nom du composant
    skin: ( 
        // Composant activé true ou false
        enabled: true, 
        // Responsive activé true ou false
        responsive: true, 
        // Liste des propriétés c-skin par défaut
        defaults: (),
        // Rendu: 
        // .c-skin {
        // }
        // Liste des modifieurs contenant chacun une liste de propriétés qui 
        // soit surchargent les propriétés par défaut
        // soit ajoutent des propriétés
        // soit les deux
        modifiers: (
            
        )
    )
);
``` 

## Extensions

Il est possible d'étendre les fonctionnalités du composant en ajoutant simplement un point d'entrée avec une déclaration `$briks-components-generic` à la typologie identique mais avec des propriétés par défaut et des modifieurs qui surchargent ou ajoutent des propriétés CSS.

Exemple:

```scss
/*
    C-SKIN EXTENSION
    Extension du composant générique c-skin
    https://github.com/ita-design-system/c-skin.scss
    Ce fichier doit servir à étendre ou surcharger les fonctionnalités
    du composant c-skin selon les besoins du projet
*/
$briks-components-generic: (
    // Nom du composant, obligatoirement skin
    skin: ( 
        // Extension activée true ou false
        enabled: true, 
        // Responsive activée true ou false pour l'extension
        responsive: true, 
        // Valeurs par défaut de l'extension
        defaults: (),
        // Liste des modifieurs contenant chacun une liste de propriétés qui 
        // soit surchargent les propriétés par défaut
        // soit ajoutent des propriétés
        // soit les deux
        modifiers: ( 
        )
    )
);
```
