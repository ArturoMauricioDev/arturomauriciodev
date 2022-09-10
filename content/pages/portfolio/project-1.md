---
title: Room home page
subtitle: Es un proyecto que tiene como objetivo aplicar una maquetación en HTML, CSS y JavaScript. El proyecto forma parte de la escuela de Desarrollo Web de Platzi utilizando el challenge de Frontend Mentor.
date: '2020-09-28'
thumb_image: images/15_thumb.jpg
thumb_image_alt: 'Room home page image'
image: images/15_thumb.jpg
image_alt: 'Room home page image'
seo:
    title: Room home page
    description: Es un proyecto que tiene como objetivo aplicar una maquetación en HTML, CSS y JavaScript. El proyecto forma parte de la escuela de Desarrollo Web de Platzi utilizando el challenge de Frontend Mentor.
    extra:
        - name: 'og:type'
          value: website
          keyName: property
        - name: 'og:title'
          value: Room home page
          keyName: property
        - name: 'og:description'
          value: Es un proyecto que tiene como objetivo aplicar una maquetación en HTML, CSS y JavaScript. El proyecto forma parte de la escuela de Desarrollo Web de Platzi utilizando el challenge de Frontend Mentor.
          keyName: property
        - name: 'og:image'
          value: images/15_thumb.jpg
          keyName: property
          relativeUrl: true
        - name: 'twitter:card'
          value: summary_large_image
        - name: 'twitter:title'
          value: Room home page
        - name: 'twitter:description'
          value: Es un proyecto que tiene como objetivo aplicar una maquetación en HTML, CSS y JavaScript. El proyecto forma parte de la escuela de Desarrollo Web de Platzi utilizando el challenge de Frontend Mentor.
        - name: 'twitter:image'
          value: images/15_thumb.jpg
          relativeUrl: true
layout: project
---

## Demo

El proyecto esta disponible en [https://room.js.org/](https://room.js.org/). Asimismo este es su [repositorio](https://github.com/ArturoMauricioDev/roomHomepage).

## Tabla de Contenidos

-   [Descripción](#descripción)
    -   [Mobile](#para-mobile)
    -   [Desktop](#para-desktop)
    -   [El reto](#el-reto)
    -   [Créditos por el diseño y reto](#créditos-por-el-diseño-y-reto)
-   [Construcción del proyecto](#construcción-del-proyecto)
    -   [Estructura HTML](#estructura-html)
    -   [Estilos en CSS](#estilos-en-css)
    -   [Manipulando el DOM con JavaScript](#manipulando-el-dom-con-javascript)
-   [Licencia](#licencia)
-   [Bonus](#bonus)
-   [Autor](#autor)

<!-- toc -->

## Descripción

Este proyecto realizará la maquetación del siguiente reto en `HTML`, `CSS` y `JavaScript` considerando los siguientes requerimientos:

### Para mobile

![Design preview for the Room homepage coding challenge - mobile](https://github.com/ArturoMauricioDev/roomHomepage/raw/master/design/mobile-design.jpg)

### Para desktop

![Design preview for the Room homepage coding challenge - desktop](https://github.com/ArturoMauricioDev/roomHomepage/raw/master/design/desktop-preview.jpg)

### El reto

El reto consiste en construir esta página inicial de una e-commerce logrando que se parezca lo más posible al diseño.

Los usuarios deberían poder:

-   Ver el diseño óptimo para el sitio según el tamaño de pantalla de su dispositivo (`Mobile First` es requerido)
-   Ver el estado hover para todos los elementos interactivos en la página.
-   Navegar con el slider.

También se utilizó el archivo de `style-guide.md`, que contiene la información necesaria, de la paleta de colores y fuentes.

### Créditos por el diseño y reto

Este reto pertenece a la lista de retos de [Frontend Mentor](https://www.frontendmentor.io/dashboard). Para más información puede visitar [este enlace](https://www.frontendmentor.io/challenges/room-homepage-BtdBY_ENq).

## Construcción del proyecto

Se construyó utilizando la metodología `mobile first` para dispositivos de 375px, 1024px y 1440px. Asimismo, para los estilos se hace el uso de la metodología `BEM`. También se utiliza `JavaScript` Vanilla para la `manipulación del DOM` en el menú de la aplicación mobile y en el slider tanto en mobile como en desktop.

A continuación se mostrará algunos detalles y buenas prácticas:

### Estructura HTML

_Carga independiente de las hojas de estilos._

```
<link rel="stylesheet" href="./styles/style.css">
<link rel="stylesheet" href="./styles/desktop1024.css" media="screen and (min-width: 1024px)">
<link rel="stylesheet" href="./styles/desktop1440.css" media="screen and (min-width: 1440px)">
```

_Optimización de carga de imágenes según el dispositivo._

```
<picture>
  <source media="(min-width:1024px)" srcset="./images/desktop-image-hero-1.jpg">
  <img src="./images/mobile-image-hero-1.jpg" alt="">
</picture>
```

### Estilos en CSS

_Uso de variables_

```
:root{
    --DarkGray: hsl(0, 0%, 63%);
    --Black: hsl(0, 0%, 0%);
    --White: hsl(0, 0%, 100%);
    --VeryDarkGray: hsl(0, 0%, 27%);
    font-family: 'Spartan', sans-serif;
}
```

_Uso de un toggle para el menú mobile_

```
.menu.toggle{
    display: none;
}

.menu{
    position: absolute;
    background: var(--White);
    display: flex;
    justify-content: space-between;
    height: 80px;
    width: 100%;
    transition: .3s;
}
```

_Uso de flexbox_

```
.topContainer{
    display: flex;
    position: absolute;
    width: 50%;
}
```

### Manipulando el DOM con JavaScript

_Uso de toggle para el menú_

```
let menu = document.getElementById('menu')
let burger = document.getElementById('burger')
let closeButton = document.getElementById('close')

function toggleMenu(){
    menu.classList.toggle('toggle')
}

burger.addEventListener('click', toggleMenu)
closeButton.addEventListener('click', toggleMenu)
```

## Licencia

> Este proyecto esta bajo la licencia de MIT.

## Bonus

Se puede acceder al proyecto por medio del dominio [https://room.js.org/](https://room.js.org/). Para utilizarlo en este proyecto se realizó la integración del proyecto [https://js.org/](https://js.org/), para más información visita su [sitio.](https://js.org/)

## Autor

Made with 💜 by [ArturoMauricioDev](https://arturomauricio.bio.link/)
