# Introducción al Desarrollo Front End con HTML, CSS y JavaScript

### Unidad II: Tecnologías fundamentales para la construcción de páginas Web

#### Jueves 6 de abril → sesion_04 → HTML y CSS con Bootstrap v5 (1 de 2)

- - - - - - - - 

Recordemos una idea importante: En el [README.md que se encuentra al acceder a este repositorio](https://github.com/profesorfaco/front-2023-1#readme), pudieron leer que para este electivo **corresponde considerar la modalidad de "aula invertida" (*flipped classroom* en inglés)**, modalidad que saca la exposición de contenidos de las horas directas y la confía al tiempo de aprendizaje autónomo de cada estudiante. 

Ante de la clase del 6 de abril, es necesario que revisen los siguientes contenidos:


- PRIMERO: Leer lo que sigue (bajo el título de [Teoría](#teor%C3%ADa))

- SEGUNDO: Ver el video [Aprende Bootstrap en 10 minutos](https://youtu.be/XXllX0A_9KQ)

- TERCERO: Consultar la página [Bootstrap grid examples](https://getbootstrap.com/docs/5.3/examples/grid/) (en inglés)

- - - - - - - - 

#### Teoría

**Existen marcos de trabajo (*frameworks*) para el desarrollo de *front-end* responsivo que nos permitirán avanzar más rápido desde relaciones predefinidas de HTML y CSS, con un poco de JS**. Por su popularidad, corresponde mencionar a:

- [Bootstrap](https://getbootstrap.com/): *The world’s most popular front-end open source toolkit, featuring Sass variables and mixins, responsive grid system, extensive prebuilt components, and powerful JavaScript plugins.*

- [Foundations](https://get.foundation/): *The most advanced responsive front-end framework in the world* 

- [Semantic UI](https://semantic-ui.com/): *A development framework that helps create beautiful, responsive layouts using human-friendly HTML*

Nos quedaremos con el primero de los mencionados, en su versión más reciente, la 5.3. 

[Bootstrap](https://getbootstrap.com/) nos permite implementar tanto prototipos rápidos como productos acabados, esto mediante el uso de elementos HTML relacionados con [reglas de CSS predefinidas, que pueden ojear acá](https://cdn.jsdelivr.net/npm/bootstrap@5.3.0-alpha2/dist/css/bootstrap.css).

Hay distintas maneras de comenzar a trabajar con Boostrap. Nosotros vamos a partir con una adaptación de [la rápida](https://getbootstrap.com/docs/5.3/getting-started/introduction/#quick-start): 

```
<!doctype html>
<html lang="es">
  <head>
    <meta charset="utf-8">
    <meta name="viewport" content="width=device-width, initial-scale=1">
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0-alpha2/dist/css/bootstrap.min.css" rel="stylesheet" integrity="sha384-aFq/bzH65dt+w6FI2ooMVUpc+21e0SRygnTpmBvdBgSdnuTN7QbdgL+OapgHtvPp" crossorigin="anonymous">
    <title>Mi Primera Página con Bootstrap</title>
  </head>
  <body>
    <!--remplaza esto-->
    <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0-alpha1/dist/js/bootstrap.bundle.min.js" integrity="sha384-w76AqPfDkMBDXo30jS1Sgez6pr3x5MlQ1ZAGC+nuZB+EYdgRZgiwxhTBTkF7CXvN" crossorigin="anonymous"></script>
  </body>
</html>
```
En un documeto vacío podemos pegar el código de arriba, y luego guardar el documento con el nombre `ejemplo.html`.

En el cuerpo del documento recién guardado (dentro de `<body></body>`) podemos comenzar a utilizar las clases con las que Bootstrap define el *layout*, siguiendo un principio general de tomar entre 1 y 12 columnas (`class="col"`) dentro de cada fila (`class="row"`) que, a su vez, está dentro de un contenedor (`class="container"`). 

En el `ejemplo.html` pueden cambiar el comentario `<!--reemplaza esto-->` por lo siguiente:

```
<div class="container">
  <div class="row">
    <div class="col-6 bg-primary-subtle"><p>¿Usemos Bootstrap?</p></div>
    <div class="col-6 bg-info-subtle"><p>Bueno, ya.</p></div>
  </div>
</div>
```

Si guardan y ven el resultado en un navegador web, podrán notar que en toda condición de pantalla tienen el párrafo de `¿Usemos Boostrap?` al lado del párrafo donde se lee `Bueno, ya`. Esto es así porque tomamos 6 de 12 columnas (`class="col-6"`). Esto es tomar la mitad de espacio disponible a lo ancho en tal fila (`class="row"`), que está dentro del contenedor (`class="container"`).

Pero, mediante interfijos, podemos indicar excepciones que respondan al tamaño de ventana de navegador en que se despliegue la página, sea que esta ventana tenga un ancho muy pequeño (), pequeño (`-sm-`), mediano (`-md-`), grande (`-lg-`), extra grande (`-xl-`) o extra-extra grande (`-xxl-`). Por ejemplo, podemos modificar las dos clases para tomar 6 y 6 columnas desde la ventana de ancho medio con el prefijo `col` - el interfijo `md` - el sufijo `6`:  

```
<div class="col-md-6 bg-primary-subtle"><p>¿Usemos Bootstrap?</p></div>
<div class="col-md-6 bg-info-subtle"><p>Bueno, ya.</p></div> 
```

Para ventanas más angostas que la mediana, se asumirá que cada división toma 12 columnas (todo el ancho disponible). Por eso quedará la pregunta arriba y la respuesta abajo cuando el ancho de la ventana del navegador sea chica o muy chica.

Si quisieramos que se muestre dividido aún en las pantallas más angostas, habrá que volver al prefijo `col` - sin interfijo - sufijo `6`, tal como en el ejemplo de más arriba. O sea, no se usa interfijo cuando queremos definir un número de columnas a tomar en casos de pantallas de ancho muy pequeño (<576px). 

Pueden revisar en los [*Breakpoints* de Bootstrap](https://getbootstrap.com/docs/5.3/layout/breakpoints/#available-breakpoints) los tamaños en pixeles correspondientes a ancho muy pequeño (), pequeño (`-sm-`), mediano (`-md-`), grande (`-lg-`), extra grande (`-xl-`) o extra-extra grande (`-xxl-`). Y pueden revisar los anchos de pantalla de diversos dispositivos en https://screensiz.es/

Al existir tal diversidad de anchos posibles, se hace necesario hacer desarrollo de [*front-end* responsivo, adaptativo o adaptable](https://es.wikipedia.org/wiki/Dise%C3%B1o_web_adaptable).

- - - - - - 

#### Práctica (horas directas)

**Partamos con [lo que les dejo en esta carpeta](https://profesorfaco.github.io/front-2023-1/sesion_04/index.html) para relacionar lo tratado en las tres primeras sesiones y [Bootstrap](https://getbootstrap.com/).**

Para avanzar, corresponde considerar que en el sitio web oficial de Bootstrap se ofrece una [documentación detallada](https://getbootstrap.com/docs/5.3/getting-started/introduction/) sobre cada clase, utilidad y componente ofrecido por este marco de trabajo (**framework**). 

**Es tanto lo que Boostrap nos ofrece que, para algunos proyectos, termina siendo muy pesado. 

![20230221_105534](https://user-images.githubusercontent.com/7999767/230698167-31232077-5f0f-4899-af30-764134a31632.jpg)

Consideren, por ejemplo, que su estilo CSS tiene 12.078 líneas cuando no está minimizado**. Todas esas líneas tienen que ser leídas por el navegador antes de mostrar la página. Pero rara vez usamos tanto (le pedimos al navegador leer más de diez mil líneas en cada carga de página creada con Boostrap, cuando usamos apenas una centena de ellas). Si queremos limitar la lectura a lo estrictamente necesario, y con ello mejorar el rendimiento de lo preparado con Bootstrap, conviene aplicar algunos trucos: https://css-tricks.com/how-do-you-remove-unused-css-from-a-site/ 

Entre los trucos del artículo recién referido, se menciona https://purifycss.online/ - Cuando tengamos nuestro trabajo en línea, con GitHub Pages, contaremos con una Website URL para darle un "Clean up CSS". Luego haremos unos cambios en los documentos en el repositorio, para aprovechar el "download combined, purified & minified CSS".


- - - - - - - 

###### [← SESIÓN ANTERIOR](https://github.com/profesorfaco/front-2023-1/tree/main/sesion_03) — [SIGUIENTE SESIÓN →](https://github.com/profesorfaco/front-2023-1/tree/main/sesion_05)
