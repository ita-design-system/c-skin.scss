# c-skin.scss

[Démo et documentation](https://ita-design-system.github.io/c-skin.scss/)

Composant CSS dédié aux aspects et apparences des éléments. 

## Scope

<details>
    <summary>Liste des propriétés CSS prises en charge par c-skin</summary>
* animation
* animation-delay
* animation-direction
* animation-duration
* animation-fill-mode
* animation-iteration-count
* animation-name
* animation-play-state
* animation-timing-function
* appearance
* backface-visibility
* background
* background-attachment
* background-clip
* background-color
* background-image
* background-origin
* background-position
* background-repeat
* background-size
* border
* border-bottom
* border-bottom-color
* border-bottom-left-radius
* border-bottom-right-radius
* border-bottom-style
* border-bottom-width
* border-collapse
* border-color
* border-image
* border-image-outset
* border-image-repeat
* border-image-slice
* border-image-source
* border-image-width
* border-left
* border-left-color
* border-left-style
* border-left-width
* border-radius
* border-right
* border-right-color
* border-right-style
* border-right-width
* border-spacing
* border-style
* border-top
* border-top-color
* border-top-left-radius
* border-top-right-radius
* border-top-style
* border-top-width
* border-width
* box-shadow
* caption-side
* color
* counter-increment
* counter-reset
* cursor
* filter
* list-style
* list-style-image
* list-style-position
* list-style-type
* mask
* mask-border
* mask-border-mode
* mask-border-outset
* mask-border-repeat
* mask-border-slice
* mask-border-source
* mask-border-width
* mask-clip
* mask-composite
* mask-image
* mask-mode
* mask-origin
* mask-position
* mask-repeat
* mask-size
* mask-type
* mix-blend-mode
* offset
* offset-anchor
* offset-distance
* offset-path
* offset-position
* offset-rotate
* opacity
* outline
* outline-color
* outline-offset
* outline-style
* outline-width
* page-break-after
* page-break-before
* page-break-inside
* pointer-events
* print-color-adjust
* quotes
* resize
* scrollbar-color
* scrollbar-gutter
* scrollbar-width
* shape-image-threshold
* shape-margin
* shape-outside
* tab-size
* touch-action
* transition
* transition-delay
* transition-duration
* transition-property
* transition-timing-function
* user-select
* -webkit-appearance
</details>


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
            // BACKGROUND
            // c-skin m-bg-0
            bg-0: (
                background: none
            ),
            // c-skin m-bg-none
            bg-none: (
                background: none
            ),
            // BACKGROUND SIZE
            // c-skin m-bsize-cover
            bsize-cover: (
                background-size: cover
            ),
            // c-skin m-bsize-contain
            bsize-contain: (
                background-size: contain
            ),
            // BACKGROUND REPEAT
            // c-skin m-brep-no-repeat
            brep-no-repeat: (
                background-repeat: no-repeat
            ),
            // c-skin m-brep-repeat-x
            brep-repeat-x: (
                background-repeat: repeat-x
            ),
            // c-skin m-brep-repeat-y
            brep-repeat-y: (
                background-repeat: repeat-y
            ),
            // BACKGROUND POSITION
            // c-skin m-bpos-center
            bpos-center: (
                background-position: center
            ),
            // POINTER
            // c-skin m-cur-pointer
            cur-pointer: (
                cursor: pointer
            ),
            // TRANSITION
            // c-skin m-transition-0
            transition-0: (
                transition: none
            ),
            // c-skin m-transition-1
            transition-1: (
                transition: all 300ms
            ),
            // OPACITY
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
