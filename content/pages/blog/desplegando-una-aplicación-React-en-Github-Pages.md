---
title: Desplegando una aplicación React en GitHub Pages
subtitle: En este tutorial te enseño a desplegar una aplicación de React en GitHub Pages.
excerpt: >-
    En este tutorial te enseño a desplegar una aplicación de React en GitHub Pages.
date: '2022-08-14'
thumb_image: images/19.jpg
thumb_image_alt: Aplicación React en GitHub Pages.
image: images/19.jpg
image_alt: Aplicación React en GitHub Pages.
seo:
    title: Desplegando una aplicación React en GitHub Pages
    description: >-
        En este tutorial te enseño a desplegar una aplicación de React en GitHub Pages.
    extra:
        - name: 'og:type'
          value: article
          keyName: property
        - name: 'og:title'
          value: Desplegando una aplicación React en GitHub Pages
          keyName: property
        - name: 'og:description'
          value: >-
              En este tutorial te enseño a desplegar una aplicación de React en GitHub Pages.
          keyName: property
        - name: 'og:image'
          value: images/19.jpg
          keyName: property
          relativeUrl: true
        - name: 'twitter:card'
          value: summary_large_image
        - name: 'twitter:title'
          value: Desplegando una aplicación React en GitHub Pages
        - name: 'twitter:description'
          value: >-
              En este tutorial te enseño a desplegar una aplicación de React en GitHub Pages.
        - name: 'twitter:image'
          value: images/19.jpg
          relativeUrl: true
layout: post
---

## Tabla de Contenidos

-   [Prerrequisitos](#prerrequisitos)
-   [A la acción](#a-la-acción)
-   [Ingresa a tu app](#ingresa-a-tu-app)

## Prerrequisitos

Para poder desplegar tu aplicación React en GitHub Pages necesitas tener instalado lo siguiente:

1. Node y npm

```
$ node --version
v16.13.2
```

```
$ npm --version
8.1.2
```

Si deseas instalar o manejar las versiones de NodeJs en tu sistema, puedes revisar este otro [artículo.](https://arturomauriciodev.netlify.app/blog/deberia-crear-mis-proyectos-react-con-vite/#resolviendo-problemas-de-versión)

2. Git

```
$ sudo apt install git
```

3. También debes tener una cuenta de [GitHub.](https://github.com/)

## A la acción

1. Crea un repositorio en GitHub.

    - Asegúrate que la visibilidad de tu repositorio sea **público**.

2. Crea tu aplicación React.
   Para ello puedes utilizar el siguiente comando:

```
$ npx create-react-app my-app
```

Ingresa al directorio creado.

```
$ cd my-app
```

Ejecuta la aplicación.

```
$ npm run start
```

Verifica en el navegador que la aplicación esté ejecutándose.

3. Instala el paquete **_gh-pages_**, para ello utiliza el siguiente comando.

```
npm install gh-pages --save-dev
```

Puedes verificar la instalación de **_gh-pages_** en el archivo **_package.json_**.

4. Agrega la propiedad **_homepage_** en el archivo **_package.json_**. Para ello puedes utilizar [Visual Studio Code.](https://code.visualstudio.com/)

_La propiedad homepage tiene el siguiente formato._

```
https://{username}.github.io
```

Debes reemplazar username por el nombre de usuario que tienes en GitHub.

Tu archivo **_package.json_**, quedaría de la siguiente manera.

```
"name": "my-app",
  "version": "0.1.0",
  "homepage": "https://ArturoMauricioDev.github.io/my-app",
  "private": true,
```

5. Agrega los **_scripts_** de predeploy y deploy en tu **_package.json_**, tu archivo quedaría de esta manera.

```
 "scripts": {
    "start": "react-scripts start",
    "build": "react-scripts build",
    "test": "react-scripts test",
    "eject": "react-scripts eject",
    "predeploy": "npm run build",
    "deploy": "gh-pages -d build"
  }
```

6. Conecta tu repositorio local con el remoto (GitHub).

```
$ git remote add origin https://github.com/{username}/{repo-name}.git
```

7. Finalmente, despliega tu aplicación React en GitHub Pages.

```
$ npm run deploy -- -m "Despliegue de la app en GitHub Pages"
```

GitHub Pages automáticamente realizará un commit en la rama _gh-pages_ del repositorio remoto, de esa manera quedará todo listo en cuanto al despliegue. 🚀

## Ingresa a tu app

Para obtener la url de tu app debes ingresar a **_Settings_** de tu repositorio y a la sección **_Pages_**, ahí encontrarás una url similar a https://gitname.github.io/my-app.
