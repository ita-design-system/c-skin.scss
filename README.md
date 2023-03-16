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
            // c-skin m-opa-1
            opa-1: (
                opacity: 0.1
            ),
            // c-skin m-opa-2
            opa-2: (
                opacity: 0.2
            ),
            // c-skin m-opa-3
            opa-3: (
                opacity: 0.3
            ),
            // c-skin m-opa-4
            opa-4: (
                opacity: 0.4
            ),
            // c-skin m-opa-5
            opa-5: (
                opacity: 0.5
            ),
            // c-skin m-opa-5
            opa-6: (
                opacity: 0.6
            ),
            // c-skin m-opa-7
            opa-7: (
                opacity: 0.7
            ),
            // c-skin m-opa-8
            opa-8: (
                opacity: 0.8
            ),
            // c-skin m-opa-9
            opa-9: (
                opacity: 0.9
            ),
            // c-skin m-opa-10
            opa-10: (
                opacity: 10
            ),
            // c-skin m-ls-none
            ls-none: (
                list-style: none
            ),
            // BORDERS
            // BORDER STYLE
            // c-skin m-bstyle-solid
            bstyle-solid: (
                border-style: solid
            ),
            // c-skin m-btstyle-solid
            btstyle-solid: (
                border-top-style: solid
            ),
            // c-skin m-brstyle-solid
            brstyle-solid: (
                border-right-style: solid
            ),
            // c-skin m-bbstyle-solid
            bbstyle-solid: (
                border-bottom-style: solid
            ),
            // c-skin m-blstyle-solid
            blstyle-solid: (
                border-left-style: solid
            ),
            // BORDER WIDTH
            // c-skin m-bwidth-1
            bwidth-1: (
                border-width: 1px
            ),
            // c-skin m-btwidth-1
            btwidth-1: (
                border-top-width: 1px
            ),
            // c-skin m-brwidth-1
            brwidth-1: (
                border-right-width: 1px
            ),
            // c-skin m-bbwidth-1
            bbwidth-1: (
                border-bottom-width: 1px
            ),
            // c-skin m-blwidth-1
            blwidth-1: (
                border-left-width: 1px
            ),
            // c-skin m-bwidth-2
            bwidth-2: (
                border-width: 2px
            ),
            // c-skin m-btwidth-2
            btwidth-2: (
                border-top-width: 2px
            ),
            // c-skin m-brwidth-2
            brwidth-2: (
                border-right-width: 2px
            ),
            // c-skin m-bbwidth-2
            bbwidth-2: (
                border-bottom-width: 2px
            ),
            // c-skin m-blwidth-2
            blwidth-2: (
                border-left-width: 2px
            ),
            // c-skin m-bwidth-3
            bwidth-3: (
                border-width: 3px
            ),
            // c-skin m-btwidth-3
            btwidth-3: (
                border-top-width: 3px
            ),
            // c-skin m-brwidth-3
            brwidth-3: (
                border-right-width: 3px
            ),
            // c-skin m-bbwidth-3
            bbwidth-3: (
                border-bottom-width: 3px
            ),
            // c-skin m-blwidth-3
            blwidth-3: (
                border-left-width: 3px
            ),
            // c-skin m-b-0
            b-0: (
                border: none
            ),
            // c-skin m-bt-0
            bt-0: (
                border-top: none
            ),
            // c-skin m-br-0
            br-0: (
                border-right: none
            ),
            // c-skin m-bb-0
            bb-0: (
                border-bottom: none
            ),
            // c-skin m-bl-0
            bl-0: (
                border-left: none
            ),
            // BORDER RADII
            // c-skin m-brad-0
            brad-0: (
                border-radius: 0
            ),
            // c-skin m-bradtl-0
            bradtl-0: (
                border-top-left-radius: 0
            ),
            // c-skin m-bradtr-0
            bradtr-0: (
                border-top-right-radius: 0
            ),
            // c-skin m-bradbr-0
            bradbr-0: (
                border-bottom-right-radius: 0
            ),
            // c-skin m-bradbl-0
            bradbl-0: (
                border-bottom-left-radius: 0
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
            // c-skin m-pe-auto
            pe-auto: (
                pointer-events: auto
            ),
            // c-skin m-disabled
            disabled: (
                pointer-events: none,
                color: grey,
                background-color: lightgrey
            ),
            // c-skin m-appearance-none
            appearance-none: (
                -webkit-appearance: none
            ),
            // c-skin m-bs-0
            bs-0: (
                box-shadow: none
            ),
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
