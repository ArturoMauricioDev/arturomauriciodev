---
title: Todo App in React
subtitle: Es un proyecto que tiene como objetivo aplicar teoría de componentes utilizando Atomic Design bajo el principio de responsabilidad única, para los estilos se utilizó el preprocesador de CSS SASS. Se creó la aplicación con Create React App, se utilizó conceptos de estados de componentes y el ciclo de vida de los mismos, además de varios hooks. La aplicación también utiliza persistencia de datos en el Local Storage.
date: '2021-09-22'
thumb_image: images/17.jpg
thumb_image_alt: A Todo App in React image
image: images/17.jpg
image_alt: A Todo App in React image
seo:
    title: Todo App in React
    description: Es un proyecto que tiene como objetivo aplicar teoría de componentes utilizando Atomic Design bajo el principio de responsabilidad única, para los estilos se utilizó el preprocesador de CSS SASS. Se creó la aplicación con Create React App, se utilizó conceptos de estados de componentes y el ciclo de vida de los mismos, además de varios hooks. La aplicación también utiliza persistencia de datos en el Local Storage.
    extra:
        - name: 'og:type'
          value: website
          keyName: property
        - name: 'og:title'
          value: Todo App in React
          keyName: property
        - name: 'og:description'
          value: Es un proyecto que tiene como objetivo aplicar teoría de componentes utilizando Atomic Design bajo el principio de responsabilidad única, para los estilos se utilizó el preprocesador de CSS SASS. Se creó la aplicación con Create React App, se utilizó conceptos de estados de componentes y el ciclo de vida de los mismos, además de varios hooks. La aplicación también utiliza persistencia de datos en el Local Storage.
          keyName: property
        - name: 'og:image'
          value: images/17.jpg
          keyName: property
          relativeUrl: true
        - name: 'twitter:card'
          value: summary_large_image
        - name: 'twitter:title'
          value: Todo App in React
        - name: 'twitter:description'
          value: Es un proyecto que tiene como objetivo aplicar teoría de componentes utilizando Atomic Design bajo el principio de responsabilidad única, para los estilos se utilizó el preprocesador de CSS SASS. Se creó la aplicación con Create React App, se utilizó conceptos de estados de componentes y el ciclo de vida de los mismos, además de varios hooks. La aplicación también utiliza persistencia de datos en el Local Storage.
        - name: 'twitter:image'
          value: images/17.jpg
          relativeUrl: true
layout: project
---

## Tabla de Contenidos

-   [Demo](#demo)
-   [Construcción del proyecto](#construcción-del-proyecto)
    -   [Estructura HTML](#estructura-html)
    -   [Estilos en CSS](#estilos-en-css)
    -   [Manipulando el DOM con JavaScript](#manipulando-el-dom-con-javascript)
-   [Licencia](#licencia)
-   [Bonus](#bonus)
-   [Autor](#autor)

## Demo

El proyecto esta disponible en [https://arturomauriciodev.github.io/todo-app-react-render/](https://arturomauriciodev.github.io/todo-app-react-render/).

En la imagen se observa la pantalla de inicio, donde se pueden agregar las tareas a realizar.

![Inicio de la aplicacion, agregue una tarea a realizar](https://i66.servimg.com/u/f66/20/43/92/62/localh18.png)

Se despliega un modal en el cual se escribe la tarea a realizar y se le da en añadir.

![Escibe un nuevo TODO y has clic en añadir](https://i66.servimg.com/u/f66/20/43/92/62/localh19.png)

Las tareas se agregan cronológicamente, se puede indicar que ya fueron completadas mostrando el total de ellas en la parte superior. También se las puede eliminar para que desaparezcan de la lista. Asimismo, es bueno mencionar que todos los datos son guardados en el local storage de tal modo que si cerramos el navegador los datos persisten para la próxima vez que se abra el navegador e ingrese a la aplicación.

![Has completado 2 tareas de 4](https://i66.servimg.com/u/f66/20/43/92/62/localh20.png)

Se pueden ingresar caracteres y/o palabras para filtrar las tareas a mostrar en la lista.

![Ingreso la i en el cuadro de búsqueda de tareas](https://i66.servimg.com/u/f66/20/43/92/62/localh21.png)

Por ejemplo, si ingreso "im" se desplegaría en la lista de tareas "Implementar estados a mis componentes".

![Se ingresa im en el cuadro de búsqueda dando un resultado](https://i66.servimg.com/u/f66/20/43/92/62/localh22.png)

En caso de no encontrar coincidencias, se despliega un mensaje de "No hay resultados para:" el criterio de su búsqueda.

![Se ingresa reac en el cuadro de búsqueda dando ningun reslutado](https://i66.servimg.com/u/f66/20/43/92/62/localh17.png)

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

Componente Search

Realizar la busqueda

Optimizando con useMemo
