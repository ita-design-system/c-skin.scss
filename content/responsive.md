---
title: Responsive
description: Fonctionnalités responsive du composant c-skin
layout: libdoc/page-split
order: 100
separator: true
---
Si le paramètre `responsive: true` est activé, les modifieurs du composant c-skin sont adaptables à chaque design token de taille d'écran `$briks-screen-sizes` comme suit.

## Classes responsives

Un modifieur peut être appliqué sur des design tokens de tailles d'écrans via des classes CSS

```html
<!-- Avec des classes CSS -->
<HTMLTag class="c-skin m-NOM_DU_MODIFIEUR--TOKEN_TAILLE_ECRAN"></HTMLTag>
```

## Attributs responsives

En parallèle des classes CSS, la syntaxe par attribut permet d'appliquer la même fonctionnalité d'un modifieur sur plusieurs tailles d'écran en une seule fois.

```html
L'attribut responsive du modifieur
<HTMLTag class="c-skin" m-NOM_DU_MODIFIEUR="TOKEN_TAILLE_ECRAN_1, TOKEN_TAILLE_ECRAN_2, TOKEN_TAILLE_ECRAN_3"></HTMLTag>

a le même effet que les classes CSS
<HTMLTag class="c-skin m-NOM_DU_MODIFIEUR--TOKEN_TAILLE_ECRAN_1 m-NOM_DU_MODIFIEUR--TOKEN_TAILLE_ECRAN_2 m-NOM_DU_MODIFIEUR--TOKEN_TAILLE_ECRAN_3"></HTMLTag>
```

```html
<!-- Avec des classes responsives -->
<ul class="c-skin m-ls-none--xs">
    <li>Pas de list-style en taille d'écran xs</li>
    <li>Pas de list-style en taille d'écran xs</li>
</ul>
<!-- Avec l'attribut responsive -->
<ul class="c-skin" m-ls-none="xs,sm">
    <li>Pas de list-style en tailles d'écran sm et xs</li>
    <li>Pas de list-style en tailles d'écran sm et xs</li>
</ul>
<!-- DEMO UNIQUEMENT -->
<style>
    body {
        padding: var(--ita-spacing-4);
        background-color: var(--ita-color-primary-900);
        color: var(--ita-color-primary-200);
        font-family: var(--ita-font-family-mono);
        font-size: 1rem;
        line-height: 1.5rem;
        padding-bottom: 50vh;
    }
</style>
```
{:.playground title="Exemples responsives"}