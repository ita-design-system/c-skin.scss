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
<div class="c-skin m-main-end--xs">
    <div>Je m'aligne au bout de l'axe "main"<br> sur la taille d'écran xs<br> via des classes CSS</div>
</div>
<!-- Avec l'attribut responsive - 1 taille d'écran -->
<div class="c-skin" m-main-end="xs">
    <div>Je m'aligne au bout de l'axe "main"<br> sur la taille d'écran xs<br> via l'attribut responsive</div>
</div>
<!-- Avec l'attribut responsive - multiples tailles d'écrans -->
<div class="c-skin" m-main-end="xs,sm">
    <div>Je m'aligne au bout de l'axe "main"<br> sur les tailles d'écran xs et sm<br> via l'attribut responsive</div>
</div>
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
    .c-skin {
        background-color: var(--ita-color-primary-800);
    }
    .c-skin > * {
        background-color: var(--ita-color-primary-500);
        color: var(--ita-color-primary-900);
        border: var(--ita-border-6);
        padding: var(--ita-spacing-4);
    }
    .c-skin + .c-skin {
        margin-top: var(--ita-spacing-4);
    }
    .c-skin + h2 {
        margin-top: var(--ita-spacing-12);
    }
</style>
```
{:.playground title="Exemples responsives"}