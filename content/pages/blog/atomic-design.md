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

Atomic Design nace a partir de la inquietud de Brad Frost de aplicar sus clases de química de la secundaria a otros campos e industrias. Su profesor, el Sr. Rae, tenía la reputación de tener una de clases más difíciles en su escuela debido a que sus estudiantes tenían que equilibrar cientos de ecuaciones químicas. Recordemos un poco sobre química de secundaria, sabemos que las reacciones químicas están representadas por ecuaciones químicas que muestran como los átomos se combinan para formar moléculas. ¡Voilà! ¡Es así como empezó todo!

El mundo es increíblemente complejo, es natural que este principio sobre las reacciones químicas sea aplicado a otros campos abordando problemas similares, por ejemplo el diseño de aplicaciones para distintos dispositivos como teléfonos móviles, tabletas, smart TVs, consolas de juegos, lentes de VR y AR, etc. este proceso es realmente complejo y se requieren procesos que faciliten este desarrollo y eviten los errores. Atomic Design utiliza este principio de química de secundaria, y viene a dar en el clavo, uniendo disciplinas como el diseño de aplicaciones y el desarrollo bajo un mismo concepto, el de _`diseñar por componentes`_.

## Tabla de Contenidos

-   [Composición de componentes](#composición-de-componentes)
-   [Los elementos de Atomic Design](#los-elementos-de-atomic-design)
    -   [Átomos](#átomos)
    -   [Moléculas](#moléculas)
    -   [Organismos](#organismos)
    -   [Plantillas](#plantillas)
    -   [Páginas](#páginas)
-   [Llevando todo a código](#llevando-todo-a-código)
    -   [ProductRow](#productrow)
    -   [ProductCatergoryRow](#productcatergoryrow)
    -   [ProductTable](#producttable)
    -   [SearchBar](#searchbar)
    -   [FilterableProductTable](#filterableproducttable)

## Composición de componentes

La composición de componentes es un principio fundamental en ReactJS, te ayuda a diseñar tus componentes de modo que sean muy flexibles, y que se integren entre sí para cambiar un resultado visual o su funcionamiento dentro de la aplicación sin dificultades. Se crean componentes de fácil acoplamiento, es así como son fáciles de reutilizar, mover e incluso eliminar.

![Piezas de lego](https://i49.servimg.com/u/f49/19/27/49/47/blokoc10.jpg)

Son como piezas de lego cada unidad con su forma, color y estructura propia, que combinándolos de una manera se podría construir un edificio y si los combinamos de otra manera podríamos construir un tractor o lo que nuestra propia creatividad e imaginación nos permita hacerlo. A esto le llamamos composición de componentes.

![Construyendo con piezas de lego](https://i49.servimg.com/u/f49/19/27/49/47/imagen10.jpg)

Para realizar la composición de componentes utilizando la metodología Atomic Design debemos comenzar desde los elementos más pequeños de una aplicación, integrándolos uno a uno para formar componentes más grandes que irán convirtiéndose eventualmente en plantillas y páginas. Pero, ¿cómo vamos estructurándolos uno a uno? Lo haremos con:

> El principio de responsabilidad única.

🤯 ¿En qué consiste este principio? Para dar una buena explicación acerca de este principio debemos conocer y seguir las siguientes reglas.

-   **Los átomos** son los componentes básicos, cada átomo como cada elemento químico tiene propiedades distintas a cualquier otro átomo y no se lo puede descomponer más sin perder su significado. Son la unidad funcional más pequeña.

-   **Las moléculas** son grupos de dos o más átomos que se mantienen unidos. Esta combinación entre átomos adquiere por sí misma sus propias propiedades únicas y funcionan en conjunto brindando una única funcionalidad.

-   **Los organismos** son conjuntos de moléculas que funcionan juntas como una unidad brindando una única funcionalidad, estas estructuras son relativamente complejas, varían desde organismos unicelulares hasta organismos sofisticados, y todas ellas tienen un límite de responsabilidad.

En esta descripción, se simplifican muchas cosas de la composición química, pero en sí nos da la esencia básica para la composición de componentes, utilizando el principio de responsabilidad única en nuestras aplicaciones. A continuación precisemos aún más estos 5 elementos que componen esta metodología.

## Los elementos de Atomic Design.

### Átomos

Son componentes básicos, estos no se los puede desglosar más sin dejar de ser funcionales. Cada átomo tienen sus propias propiedades únicas. Pueden ser: botones, avatares, inputs de formularios, párrafos, etc.

### Moléculas

Son grupos de átomos unidos entre sí que adquieren nuevas propiedades distintas, funcionan juntos como una unidad. Por ejemplo:

Un input de búsqueda y un botón pueden unirse para crear una molécula que forma parte de un formulario de búsqueda. Cuando se combinan estos átomos llegan a tener un propósito. Esta molécula llega a ser un componente simple, portátil y reutilizable que se puede colocar en cualquier lugar donde se necesite realizar búsquedas.

La creación de componentes simples ayuda a los diseñadores y desarrolladores a emplear el principio de responsabilidad única. Dicho en otras palabras "hacer una cosa y hacerlo bien"

### Organismos

Son componentes relativamente complejos, compuestos por grupos de moléculas y/o átomos y/u otros organismos. Estos organismos forman secciones distintas. Por ejemplo, cuando unimos el logo, los iconos, texto y una molécula de búsqueda para crear una navegación en la aplicación. La navegación en sí es una sección independiente con sus propias propiedades, en mobile se puede ver con su burguer menu de una manera diferente a la versión desktop donde no se muestra el burguer menu, ya que se despliega sus opciones directamente.

### Plantillas

En esta instancia, la plantilla contiene los componentes creados en las anteriores instancias y articulan la estructura de la app. Se compone principalmente de grupos de organismos unidos para formar una vista de la aplicación. Aquí se empieza a ver ya el diseño en acción. Con las plantillas los clientes comienzan a ver el diseño final de la aplicación.

Las plantillas definen el esqueleto de la aplicación, muestran componentes clave en acción, demuestra su contenido con respecto a tamaños, espacios que ocupa y la longitud de los textos y caracteres.

### Páginas

Las páginas llegan a ser instancias de las plantillas, dicho de otra manera, las páginas son plantillas con contenido específico y real que muestran como se ve una interfaz de la aplicación. Los usuarios verán e interactuarán obteniendo una experiencia de su uso y utilizando las funcionalidades que la aplicación les brinda.

En esta etapa se realiza una revisión de que todo se llegue a ver bien y de que todo funcione correctamente. En caso de que algo no se vea coherente y no brinde la función esperada, se debe retroceder y modificar las moléculas, organismos y plantillas para resolver las necesidades de los usuarios.

## Llevando todo a código

A continuación, vamos a dividir una interfaz de usuario en una jerarquía de componentes utilizando el principio de responsabilidad única. Y lo llevaremos a código utilizando ReactJS.

Como se observa tenemos una aplicación que muestra productos de deportes y productos electrónicos con sus respectivos precios. Estos productos están divididos por sus categorías. También, se cuenta con una barra de búsquedas la cual filtra el producto deseado de las listas de productos, asimismo se considera solo mostrar los productos que tienen stock.

Ahora comenzaremos a identificar los diferentes componentes de acuerdo con la metodología atomic design.

1. **FilterableProductTable** (café): Contiene la totalidad de componentes.

2. **SearchBar** (azul): Componente para realizar búsquedas y filtrado, su responsabilidad es mostrar los productos de acuerdo con los parámetros que el usuario vaya ingresando.

3. **ProductTable** (verde): Muestra la colección de productos de todas las categorías según el nombre y el precio.

4. **ProductCategoryRow** (turquesa): Muestra los productos de una categoría en específico.

5. **ProductRow** (rojo): Muestra un producto, su nombre y precio en una fila.

### ProductRow

De esta manera quedaría el código del componente ProductRow.

```
import React from 'react'

import '../styles/ProductRow.css'

function ProductRow(props) {
    const producto = props.name
    const precio = props.price
    const theme = 'product-row ' + props.theme

    return (
        <div className={theme}>
            <span>{producto}</span><span>{`$${precio}`} </span>
        </div>
    )
}

export { ProductRow }
```

### ProductCatergoryRow

Este componente recibe el título que mostrará en su categoría y el arreglo de productos que pertenecen a dicha categoría, con esa información puede construirse por sí mismo. También crea componentes ProductRow por cada producto reutilizando código.

### ProductTable

Se construye este componente sobre la base de los anteriores componentes, para el ejemplo se utiliza dos categorías, por lo cual se le envía el título y el arreglo de productos correspondiente.

### SearchBar

Este componente quedaría de la siguiente manera.

### FilterableProductTable

Finalmente, todos los componentes anteriormente construidos son utilizados en este componente. También es bueno resaltar que cada uno de ellos es independiente en sus propiedades y estados. Para conseguir la funcionalidad esperada, los componentes interactúan unos con otros utilizando useContext.

Para obtener toda la información correspondiente a este ejemplo puedes visitar el siguiente [GitHub](https://github.com/ArturoMauricioDev/product-table).

Ahora es tu turno, ya puedes construir tu siguiente aplicación utilizando la metodología Atomic Design.
