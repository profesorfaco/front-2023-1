# Introducción al Desarrollo Front End con HTML, CSS y JavaScript

### Unidad II: Tecnologías fundamentales para la construcción de páginas Web

#### Jueves 6 de abril → sesion_04 → HTML y CSS con Bootstrap v5 (1 de 2)

- - - - - - - - 

Por la modalidad a aula invertida, antes la cuarta sesión corresponde revisar algo de contenido en EL SIGUIENTE ORDEN:

- PRIMERO: [Aprende Bootstrap en 10 minutos](https://youtu.be/XXllX0A_9KQ)

- SEGUNDO: Leer lo que sigue (bajo el título de [Teoría](#teor%C3%ADa))

- TERCERO: [Bootstrap grid examples](https://getbootstrap.com/docs/5.3/examples/grid/) (en inglés)

- - - - - - - - 

#### Teoría

**Existen marcos de trabajo (*frameworks*) de código abierto que nos permitirán avanzar más rápido desde relaciones predefinidas de HTML y CSS, con un poco de JS**. Por su popularidad, corresponde mencionar a:

- [Bootstrap](https://getbootstrap.com/): *The world’s most popular front-end open source toolkit, featuring Sass variables and mixins, responsive grid system, extensive prebuilt components, and powerful JavaScript plugins.*

- [Foundations](https://get.foundation/): *The most advanced responsive front-end framework in the world* 

- [Semantic UI](https://semantic-ui.com/): *A development framework that helps create beautiful, responsive layouts using human-friendly HTML*

Nos quedaremos con el primero de los mencionados, en su versión más reciente, la 5.3. 

[Bootstrap](https://getbootstrap.com/) nos permite implementar tanto prototipos rápidos como productos acabados, esto mediante el uso de elementos HTML relacionados con [reglas de CSS predefinidas](https://cdn.jsdelivr.net/npm/bootstrap@5.3.0-alpha1/dist/css/bootstrap.css).

Hay distintas maneras de comenzar a trabajar con Boostrap. Nosotros vamos a partir con [la rápida](https://getbootstrap.com/docs/5.3/getting-started/introduction/#quick-start): 

```
<!doctype html>
<html lang="en">
  <head>
    <meta charset="utf-8">
    <meta name="viewport" content="width=device-width, initial-scale=1">
    <title>Bootstrap demo</title>
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0-alpha1/dist/css/bootstrap.min.css" rel="stylesheet" integrity="sha384-GLhlTQ8iRABdZLl6O3oVMWSktQOp6b7In1Zl3/Jr59b6EGGoI1aFkw7cmDA6j6gD" crossorigin="anonymous">
  </head>
  <body>
    <h1>Hello, world!</h1>
    <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0-alpha1/dist/js/bootstrap.bundle.min.js" integrity="sha384-w76AqPfDkMBDXo30jS1Sgez6pr3x5MlQ1ZAGC+nuZB+EYdgRZgiwxhTBTkF7CXvN" crossorigin="anonymous"></script>
  </body>
</html>
```

Luego, en el cuerpo de tal documento HTML (`<body></body>`) podemos comenzar a utilizar las clases con las que Bootstrap define el *layout*, siguiendo un principio general de tomar entre 1 y 12 columnas (`class="col"`) dentro de cada fila (`class="row"`) que, a su vez, está dentro de un contenedor (`class="container"`). En el `ejemplo.html` creado, reemplacen los puntos suspensivos (`…`) por lo siguiente:

```
<div class="container">
  <div class="row">
    <div class="col-6"><p>¿Usemos Bootstrap?</p></div>
    <div class="col-6"><p>Bueno, ya.</p></div>
  </div>
</div>
```

Si guardan y ven el resultado en un navegador web, podrán notar que en toda condición de pantalla tenemos el párrafo de `¿Usemos Boostrap?` junto al párrafo donde se lee `Bueno, ya`. Esto es así porque tomamos 6 de 12 columnas (`class="col-6"`). Esto es tomar la mitad de espacio disponible a lo ancho, en tal fila (`class="row"`) dentro del contenedor (`class="container"`).

Pero podemos indicar excepciones que respondan al tamaño de ventana de navegador en que se despliegue la página, sea esta muy pequeña, pequeña (`-sm-`), mediana (`-md-`), grande (`-lg-`), extra grande (`-xl-`) o extra-extra grande (`-xxl-`). Por ejemplo, podemos modificar las dos clases para tomar 6 y 6 columnas desde la ventana mediana:

```
<div class="col-md-6"><p>¿Usemos Bootstrap?</p></div>
<div class="col-md-6"><p>Bueno, ya.</p></div> 
```

Para vetanas más angostas que la mediana se asumirá que se quieren tomar 12 columnas (todo el ancho disponible). Por eso quedará la pregunta arriba y la respuesta abajo cuando el ancho de la ventana del navegador sea chica o muy chica. 

Los tamaños en pixeles de cada pantalla los pueden revisar en los [*Breakpoints* de Bootstrap]([https://getbootstrap.com/docs/5.3/layout/breakpoints/](https://getbootstrap.com/docs/5.3/layout/breakpoints/#available-breakpoints)).

- - - - - - 

#### Práctica (horas directas)

**Pueden asomarse al código fuente del [eslabón que les dejo en esta carpeta](https://profesorfaco.github.io/front-2023-1/sesion_04/eslabon.html) para relacionar lo tratado en las tres primeras sesiones y [Bootstrap](https://getbootstrap.com/).**

En el sitio web oficial de Bootstrap encontrarán [documentación detallada](https://getbootstrap.com/docs/5.1/getting-started/introduction/) sobre cada clase, utilidad y componente que ofrece. Allí también encontrarán [ejemplos](https://getbootstrap.com/docs/5.1/examples/). 

En la exploración práctica de esta sesión nos aprovecharemos de *Grid*: https://getbootstrap.com/docs/5.1/examples/grid/

Metámonos al código fuente de tal ejemplo, para compiarlo completo y luego pegarlo en un documento creado en un editor de código fuente. Documento que tenemos que guardar como `index.html` ¡Pero ojo! No funcionará de inmediato, porque tenemos que arreglar algunos vínculos. 

Una vez tengamos la página funcionando, viendose idéntica al ejemplo en línea, podríamos agregar [texto](https://www.lipsum.com/) e [imágenes](https://picsum.photos/) y luego hacer algo respecto del código que no lleguemos a usar: 

**Boostrap nos ofrece un estilo CSS muy grande, de 11.783 líneas cuando no está minimizado**. Todas esas líneas tienen que ser leídas por el navegador antes de mostrar la página. Pero rara vez usamos tanto (le pedimos al navegador leer más de diez mil líneas en cada carga de página creada con Boostrap, cuando usamos apenas una centena de ellas). Si queremos limitar la lectura a lo estrictamente necesario, y con ello mejorar el rendimiento de lo preparado con Bootstrap, conviene aplicar algunos trucos: https://css-tricks.com/how-do-you-remove-unused-css-from-a-site/ 

Entre los trucos del artículo recién referido, se menciona https://purifycss.online/ - Cuando tengamos nuestro trabajo en línea, con GitHub Pages, contaremos con una Website URL para darle un "Clean up CSS". Luego haremos unos cambios en los documentos en el repositorio, para aprovechar el "download combined, purified & minified CSS".


- - - - - - - 

###### [← SESIÓN ANTERIOR](https://github.com/profesorfaco/front-2023-1/tree/main/sesion_03) — [SIGUIENTE SESIÓN →](https://github.com/profesorfaco/front-2023-1/tree/main/sesion_05)
