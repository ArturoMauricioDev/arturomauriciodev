---
title: ¿Cómo utilizo atomic design en mis proyectos ReactJs?
subtitle: 'Atomic Design es una metodología concebida por Brad Frost, que pretende acabar con las inconsistencias y optimizar el diseño y desarrollo al máximo en aplicaciones modernas, de ese modo podemos aplicar la composición de componentes en ReactJs.'
excerpt: >-
    Acá te muestro como utilizar atomic design en todos tus proyectos futuros.
date: '2022-09-09'
thumb_image: images/20.jpg
thumb_image_alt: atomic design image
image: images/20.jpg
image_alt: atomic design image
seo:
    title: ¿Cómo utilizo atomic design en mis proyectos ReactJs?
    description: >-
        Acá te muestro como utilizar atomic design en todos tus proyectos futuros.
    extra:
        - name: 'og:type'
          value: article
          keyName: property
        - name: 'og:title'
          value: ¿Cómo utilizo atomic design en mis proyectos ReactJs?
          keyName: property
        - name: 'og:description'
          value: >-
              Acá te muestro como utilizar atomic design en todos tus proyectos futuros.
          keyName: property
        - name: 'og:image'
          value: images/20.jpg
          keyName: property
          relativeUrl: true
        - name: 'twitter:card'
          value: summary_large_image
        - name: 'twitter:title'
          value: ¿Cómo utilizo atomic design en mis proyectos ReactJs?
        - name: 'twitter:description'
          value: >-
              Acá te muestro como utilizar atomic design en todos tus proyectos futuros.
        - name: 'twitter:image'
          value: images/20.jpg
          relativeUrl: true
layout: post
[img1]:
    data: images/20.jpg
---

Atomic Design nace a partir de la inquietud de Brad Frost de aplicar sus clases de química de la secundaria a otros campos e industrias. Su profesor, el Sr. Rae, tenía la reputación de tener una de clases más difíciles en su escuela debido a que sus estudiantes tenían que equilibrar cientos de ecuaciones químicas. Recordando química de secundaria, es bien sabido que las reacciones químicas están representadas por ecuaciones químicas que muestran como los átomos se combinan para formar moléculas. ¡Voilà! ¡Así empezó todo!

El mundo es increíblemente complejo, es natural que este principio sea aplicado a otros campos abordando problemas similares,

Probablemente realizaste muchos proyectos con React, muchos de ellos los creaste utilizando create-react-app. Es normal, esta manera de crear tus proyectos es una práctica muy usual entre los desarrolladores. Pero te preguntaste ¿si hay otras formas de crear proyectos? Por su puesto que sí, hay varias y una de ellas es utilizando Vite.

## Tabla de Contenidos

-   [¿Por qué deberías usar Vite?](#¿por-qué-deberías-usar-vite)
-   [Vamos a la acción](#vamos-a-la-acción)
-   [Resolviendo problemas de versión](#resolviendo-problemas-de-versión)

## ¿Por qué deberías usar Vite?

Si bien con el tiempo, hemos visto herramientas como Webpack, Rollup y Parcel , que mejoraron enormemente la experiencia de desarrollo para los desarrolladores frontend. Hoy en día no es raro que los proyectos a gran escala contengan miles de módulos. Estamos empezando a encontrar un cuello de botella en el rendimiento de las herramientas basadas en JavaScript: a menudo puede llevar una espera excesivamente larga (¡algunas veces hasta minutos!) Para activar un servidor de desarrollo, e incluso con HMR, las ediciones de archivos pueden tardar un par de segundos en reflejarse en el navegador. El ciclo de retroalimentación lento puede afectar en gran medida la productividad y la felicidad de los desarrolladores.

Vite tiene como objetivo abordar estos problemas aprovechando los nuevos avances en el ecosistema: la disponibilidad de módulos ES nativos en el navegador y el surgimiento de herramientas JavaScript escritas en lenguajes de compilación a nativos.

Y ¿De dónde viene toda esta iniciativa para optimizar y resolver estos problemas? Pues del creador de Vue Js, Evan You. Para todos aquellos que no conocen la trayectoria de Evan es bueno mencionar que trabajo para Meteor Development Group y posteriormente paso un par de años en Google Creative Lab donde también formo parte de los inicios de Angular. Fue allí, en Mountain View que decidió ser un rebelde e ir en contra corriente para crear su propia librería de JavaScript, en donde las cosas se mantengan simples y el rendimiento sea el mejor. Es así como nació Vue Js, por eso no me sorprende en nada los objetivos propuestos por Vite Js. También es obvio que existe una coincidencia, ambos proyectos son nombrados con palabras en francés.

## Vamos a la acción.

Evan en su cuenta de Twitter nos indica las diferentes maneras de como podemos iniciar un proyecto con Vite.

![Evan Tweet](https://i49.servimg.com/u/f49/19/27/49/47/1510.png)

Ambas nos ayudarían a lograr nuestro objetivo, pero esta vez yo utilizare:

```
npm init vite@latest
```

Ejecutamos el comando y a continuación nos pregunta el nombre del proyecto. Esta vez lo nombraré como vite-project.

![npm init vite@latest](https://i49.servimg.com/u/f49/19/27/49/47/16268910.png)

Luego debemos indicar el framework a utilizar, elegimos react.

![Elegimos React](https://i49.servimg.com/u/f49/19/27/49/47/16268911.png)

![Elegimos React](https://i49.servimg.com/u/f49/19/27/49/47/16268912.png)

¡Y eso es todo! Ya creamos nuestro primer proyecto con Vite en cuestión de segundos. Para finalizar nos indica 3 sencillos pasos para hacerlo correr.

![Debes ejecutar lo siguiente](https://i49.servimg.com/u/f49/19/27/49/47/16268913.png)

Ahora es cuando a más de uno les habrá saltado un error y comenzaran a sentirse frustrados. Esperen un segundo respiren profundo que acá les traigo la solución. El error más común y por el cual no llega a funcionar es porque la versión de NodeJs no es la adecuada. Para que ViteJs comience a andar necesitamos la versión 12 o posterior. Vamos a solucionarlo.

## Resolviendo problemas de versión.

La manera más sencilla y eficiente de resolver los problemas de versión de NodeJs es utilizando una maravillosa herramienta de gestión de versiones para NodeJs llamada nvm. Para instalarla ejecutamos el siguiente comando.

```
curl -o- https://raw.githubusercontent.com/creationix/nvm/v0.33.11/install.sh | bash
```

Una vez instalado, reinicia tu terminal y ya podemos ver las versiones de NodeJs que tenemos en nuestro sistema con nvm list.

![nvm list](https://i49.servimg.com/u/f49/19/27/49/47/16268914.png)

Luego procedemos a verificar que versiones están disponibles en los repositorios para realizar la instalación de la versión correcta para la tarea que deseamos realizar. Para ello utilizo el comando nvm ls-remote --lts. A continuación nos mostrará una larga lista con las versiones de NodeJs.

![version list](https://i49.servimg.com/u/f49/19/27/49/47/16268915.png)

Una vez identificada la versión que requerimos procedemos a instalar. Para esta tarea en específico instalamos la versión 12.2.

![instalación](https://i49.servimg.com/u/f49/19/27/49/47/16268916.png)

Ahora verificamos con nvm list la versión de NodeJs con la cual está trabajando el sistema. También es bueno mencionar que con nvm podremos cambiar las diferentes versiones de NodeJs de acuerdo a la necesidad que tengamos, sin tener que instalar o desinstalar. Todas las versiones coexistirán, solo tendremos que activarlas o desactivarlas.

![Se verifica la instalación](https://i49.servimg.com/u/f49/19/27/49/47/16268917.png)

¡Ahora si a iniciar el proyecto!

![npm install](https://i49.servimg.com/u/f49/19/27/49/47/16268918.png)

![npm run dev](https://i49.servimg.com/u/f49/19/27/49/47/16268919.png)

Lo logramos ViteJs ya está funcionando.

![Está funcionando, se muestra la url](https://i49.servimg.com/u/f49/19/27/49/47/16268920.png)

¡Felicidades! Acabas de crear tu primer proyecto con ViteJs.

![Proyecto React con Vite funcionando en el navegador](https://i49.servimg.com/u/f49/19/27/49/47/16268921.png)
