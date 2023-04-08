# Introducción al Desarrollo Front End con HTML, CSS y JavaScript

### Unidad II: Tecnologías fundamentales para la construcción de páginas Web

#### Jueves 13 de abril → sesion_05 → HTML y CSS con Bootstrap v5 (2 de 2)

- - - - - - - - 

Recordemos una idea importante: En el [README.md que se encuentra al acceder a este repositorio](https://github.com/profesorfaco/front-2023-1#readme), pudieron leer que para este electivo **corresponde considerar la modalidad de "aula invertida" (*flipped classroom* en inglés)**, modalidad que saca la exposición de contenidos de las horas directas y la confía al tiempo de aprendizaje autónomo de cada estudiante. 

Ante de la clase del 13 de abril, es necesario que lean lo que sigue (bajo el título de [Teoría](#teor%C3%ADa)), es recomendable que visiten los vínculos allí incluidos y hagan el ejercicio de `ejemplo.html`.

- - - - - - - - 

#### Teoría

Bootstrap ofrecer [un estilo CSS que tiene tantas definiciones que llega a las 12.078 líneas](https://cdn.jsdelivr.net/npm/bootstrap@5.3.0-alpha2/dist/css/bootstrap.css). Con definiciones nos referimos a reglas de CSS, con su selector y respectivas declaraciones entre paréntesis de llave, declaraciones que se separan entre sí mediante punto y coma:

![regla](https://user-images.githubusercontent.com/7999767/230624981-4dd78d8c-9a2b-437c-9a7b-4cbf5f5cbbd7.png)

En las primeras líneas del estilo CSS de Bootstrap nos encontramos con un selector especial, el de pseudo-clase `:root`, donde se declaran [variables o propiedades personalizadas de CSS](https://developer.mozilla.org/es/docs/Web/CSS/Using_CSS_custom_properties). Éstas se establecen con dos guiones `--` seguidos, en el caso de **B**oot**s**trap, por `bs-` (por ejemplo, `--bs-blue: #0d6efd;`). Allí tenemos un valor que será accedido en las línea que sigan cada vez que se escriba la función `var()` (por ejemplo, `color: var (--bs-blue);`).

El uso de variables o propiedades personalizadas de CSS nos permite hacer ajustes rápidos; declaramos sólo una vez el valor necesario, y en caso haya un cambio de tal valor: Se cambia una única vez.

Avanzando en las líneas del estilo CSS de Bootstrap nos podemos encontrar con la siguiente estructura: 

```
@media (min-width: 576px) {
  .container-sm, .container {
    max-width: 540px;
  }
}
```

Allí tenemos una [regla at](https://developer.mozilla.org/es/docs/Web/CSS/At-rule) anidada, la [`@media`](https://developer.mozilla.org/es/docs/Web/CSS/@media), que entre paréntesis redondo define una condición que, para este caso, es un ancho de pantalla de 576px. Seguido del paréntesis redondo se abre un paréntesis de llave que contendrá un grupo de reglas que tendrán tales propiedades si es que se cumple tal condición.

Trabajar con lo que es contenido por `:root{}` y `@media(){}` es clave para sacarle un mejor provecho a las 12.078 líneas del estilo CSS de Bootstrap.

**Pero hay más en Bootstrap.** Este *framework* también nos ofrece una biblioteca de JavaScript que asegura la implementación de interacciones que habitualmente encontramos en sitios y aplicaciones web de [diseño responsivo, adaptativo o adaptable](https://es.wikipedia.org/wiki/Dise%C3%B1o_web_adaptable). Por ejemplo:

- [Modal](https://getbootstrap.com/docs/5.3/components/modal/)
- [Offcanvas](https://getbootstrap.com/docs/5.3/components/offcanvas/)
- [Toasts](https://getbootstrap.com/docs/5.3/components/toasts/)

Para usa la biblioteca de JavaScript ofrecida por Bootstrap es necesario contar con [Popper](https://popper.js.org/). 

Se puede optar por ir por los scripts de Bootstrap.js y Popper.js por separado:

```
<script src="https://cdn.jsdelivr.net/npm/@popperjs/core@2.11.7/dist/umd/popper.min.js" integrity="sha384-zYPOMqeu1DAVkHiLqWBUTcbYfZ8osu1Nd6Z89ify25QV9guujx43ITvfi12/QExE" crossorigin="anonymous"></script>
<script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0-alpha3/dist/js/bootstrap.min.js" integrity="sha384-Y4oOpwW3duJdCWv5ly8SCFYWqFDsfob/3GkgExXKV4idmbt98QcxXYs9UoXAB7BZ" crossorigin="anonymous"></script>
```

También está la opción de ir por ambos de una vez, con *Bundle*:

```
<script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0-alpha3/dist/js/bootstrap.bundle.min.js" integrity="sha384-ENjdO4Dr2bkBIFxQpeoTz1HIcje39Wm4jDKdf19U8gI4ddQ3GYNS7NTKfAdVQSZe" crossorigin="anonymous"></script>
```

Corresponde mencionar que hay una tercera opción, donde se van a buscar sólo determinados módulos, pero ello supera el alcance de una introducción.

Si nos quedamos con la segunda opción mencionada, nuestra adaptación de la [Starter template](https://getbootstrap.com/docs/5.3/getting-started/introduction/) tendría que verse como sigue:

```
<!DOCTYPE html>
<html lang="es">
    <head>
        <meta charset="utf-8" />
        <meta name="viewport" content="width=device-width, initial-scale=1" />
        <title>¡Usemos Bootstrap!</title>
        <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0-alpha3/dist/css/bootstrap.min.css" rel="stylesheet" integrity="sha384-KK94CHFLLe+nY2dmCWGMq91rCGa5gtU4mk92HdvYe+M/SXH301p5ILy+dN9+nJOZ" crossorigin="anonymous">
    </head>
    <body>
    <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0-alpha3/dist/js/bootstrap.bundle.min.js" integrity="sha384-ENjdO4Dr2bkBIFxQpeoTz1HIcje39Wm4jDKdf19U8gI4ddQ3GYNS7NTKfAdVQSZe" crossorigin="anonymous"></script>
    </body>
</html>
```

Además del `.CSS` de Bootstrap que está vinculado en la cabeza del documento, ahora necesitamos el `.JS` de Bootstrap que, en este caso, está en el cuerpo.

Copiemos y peguemos el código de arriba en un documento nuevo, al que podemos llamar `ejemplo.html`.

Luego, justo en el espacio entre las etiquetas de apertura de `<body>` y `<script>` podemos comenzar a probar distintos componentes. Uno de ellos puede ser el carrusel:

```
<div class="container">
    <div id="probandoCarrusel" class="carousel slide" data-bs-ride="carousel">
        <div class="carousel-inner">
            <div class="carousel-item active">
                <img src="https://picsum.photos/600/300?random=1" class="d-block w-100" alt="…" />
            </div>
            <div class="carousel-item">
                <img src="https://picsum.photos/600/300?random=2" class="d-block w-100" alt="..." />
            </div>
            <div class="carousel-item">
                <img src="https://picsum.photos/600/300?random=3" class="d-block w-100" alt="..." />
            </div>
        </div>
        <button class="carousel-control-prev" type="button" data-bs-target="#probandoCarrusel" data-bs-slide="prev">
            <span class="carousel-control-prev-icon" aria-hidden="true"></span>
            <span class="visually-hidden">Previous</span>
        </button>
        <button class="carousel-control-next" type="button" data-bs-target="#probandoCarrusel" data-bs-slide="next">
            <span class="carousel-control-next-icon" aria-hidden="true"></span>
            <span class="visually-hidden">Next</span>
        </button>
    </div>
</div>
```

Entre el cierre de la división de identidad `probandoCarrusel` y el cierre de la división de clase `container`, podemos incluir algo más:

```
<div class="row">
    <div class="col-md-4 mx-auto text-center">
        <button type="button" class="btn btn-sm btn-primary my-3" data-bs-toggle="modal" data-bs-target="#probandoModal">
            Más información
        </button>
    </div>
</div>
<div class="modal fade" id="probandoModal" tabindex="-1" aria-labelledby="probandoModalLabel" aria-hidden="true">
    <div class="modal-dialog">
        <div class="modal-content">
            <div class="modal-header">
                <h5 class="modal-title" id="probandoModalLabel">Más información</h5>
                <button type="button" class="btn-close" data-bs-dismiss="modal" aria-label="Close"></button>
            </div>
            <div class="modal-body">
                <p>
                    Lorem ipsum dolor sit amet, consectetur adipiscing elit. Quisque aliquam vitae odio a ullamcorper. Vestibulum justo lorem, gravida et tempor in, vulputate id libero. Etiam feugiat pulvinar aliquam. Pellentesque imperdiet cursus lacus, sit amet lacinia metus posuere at. Maecenas pretium libero leo, non fermentum ipsum mattis ac. Vivamus vel arcu et ligula interdum ultrices. Curabitur ut placerat tellus, quis euismod quam. Quisque tempor, diam id bibendum fringilla, urna sapien imperdiet nulla, at ultrices sapien leo nec metus. Aliquam id arcu tortor.
                </p>
            </div>
            <div class="modal-footer">
                <button type="button" class="btn btn-sm btn-secondary" data-bs-dismiss="modal">Cerrar</button>
            </div>
        </div>
    </div>
</div>
```

Al copiar y pegar estas distintas partes se podría desordenar un poco su código fuente. Para volver a ordenarlo, pueden usar https://webformatter.com/html 

Una vez el código esté ordenado, vean el resultado en su navegador (prefieran Chrome o Firefox, eviten Edge y nunca usen Safari).

- - - - - - - - - -

#### Exploración práctica

Hoy nos aprovecharemos de un [ejemplo](https://getbootstrap.com/docs/5.3/examples/) del sitio web oficial de Bootstrap: https://getbootstrap.com/docs/5.3/examples/album/

Corresponde repetir la operación de copiar el código fuente completo, para pegarlo en un documento recién creado en un editor de código fuente, para luego guardarlo como `index.html` y hacer los ajustes necesario para que se vea tal como está ofrecido en línea. 

Nuevamente, si necesitan ordenar el código, aprovechen https://webformatter.com/html - Y para visualizar prefieran prefieran Chrome o Firefox, eviten Edge y nunca usen Safari (tampoco se confíen de la visualización que ofrece https://phcode.dev/) 

Y si queremos limitar la lectura a lo estrictamente necesario, y con ello mejorar el rendimiento de lo preparado con Bootstrap, conviene aplicar algunos trucos: https://css-tricks.com/how-do-you-remove-unused-css-from-a-site/ 

Acá dejo el "meme" que les debía: 

![20230221_105534](https://user-images.githubusercontent.com/7999767/230698167-31232077-5f0f-4899-af30-764134a31632.jpg)

- - - - - - - 

###### [← SESIÓN ANTERIOR](https://github.com/profesorfaco/front-2023-1/tree/main/sesion_04) — [SIGUIENTE SESIÓN →](https://github.com/profesorfaco/front-2023-1/tree/main/sesion_06)
