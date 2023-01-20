# c-skin.scss

[Démo et documentation](https://ita-design-system.github.io/c-skin.scss/)

Composant CSS dédié aux aspects et apparences des éléments. 

## Scope

Liste des propriétés CSS utilisées par le composant

* [background](https://developer.mozilla.org/fr/docs/Web/CSS/background)
* [border](https://developer.mozilla.org/fr/docs/Web/CSS/border)
* [border-radius](https://developer.mozilla.org/fr/docs/Web/CSS/border-radius)
* [box-shadow](https://developer.mozilla.org/fr/docs/Web/CSS/box-shadow)
* [color](https://developer.mozilla.org/fr/docs/Web/CSS/color)
* [cursor](https://developer.mozilla.org/fr/docs/Web/CSS/cursor)
* [list-style](https://developer.mozilla.org/fr/docs/Web/CSS/list-style)
* [opacity](https://developer.mozilla.org/fr/docs/Web/CSS/opacity)
* [outline](https://developer.mozilla.org/fr/docs/Web/CSS/outline)
* [pointer-events](https://developer.mozilla.org/fr/docs/Web/CSS/pointer-events)
* [transition](https://developer.mozilla.org/fr/docs/Web/CSS/transition)

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
        defaults: (
            pseudo-classes: (
                // c-skin:disabled uniquement pour les <button>
                disabled: (
                    pointer-events: none,
                    color: grey,
                    background-color: lightgrey
                )
            )
        ),
        // Rendu: 
        // c-skin {
        // }
        // Liste des modifieurs contenant chacun une liste de propriétés qui 
        // soit surchargent les propriétés par défaut
        // soit ajoutent des propriétés
        // soit les deux
        modifiers: ( 
            // c-skin m-cur-pointer
            cur-pointer: (
                cursor: pointer
            ),
            // c-skin m-transition-1
            transition-1: (
                transition: all 300ms
            ),
            // c-skin m-opa-0
            opa-0: (
                opacity: 0
            ),
            // c-skin m-ls-none
            ls-none: (
                list-style: none
            ),
            // c-skin m-b-0
            b-0: (
                border: none
            ),
            // c-skin m-brad-0
            brad-0: (
                border-radius: 0
            ),
            // c-skin m-c-0
            c-0: (
                color: transparent
            ),
            // c-skin m-bc-0
            bc-0: (
                background-color: transparent
            ),
            // c-skin m-pe-none
            pe-none: (
                pointer-events: none
            ),
            // c-skin m-disabled
            disabled: (
                pointer-events: none,
                color: grey,
                background-color: lightgrey
            )
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
        defaults: (
            pseudo-classes: (
                // c-skin:disabled uniquement pour les <button>
                disabled: (
                    pointer-events: none,
                    color: grey,
                    background-color: yellow
                )
            )
        ),
        // Liste des modifieurs contenant chacun une liste de propriétés qui 
        // soit surchargent les propriétés par défaut
        // soit ajoutent des propriétés
        // soit les deux
        modifiers: ( 
            // c-skin m-scheme-1
            scheme-1: (
                background-color: my-color(primary-500),
                color: my-color(neutral-900),
                pseudo-classes: (
                    hover: (
                        background-color: my-color(primary-700),
                        color: my-color(neutral-900),
                    )
                )
            ),
            // c-skin m-disabled
            disabled: (
                pointer-events: none,
                color: grey,
                background-color: lightgrey
            )
        )
    )
);
```
