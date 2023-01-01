# Introducción al Desarrollo Front End con HTML, CSS y JavaScript

### Unidad I: Bocetos de introducción a la programación

### Jueves 16 de marzo → sesion_01 → p5.js

En el [README.md](https://github.com/profesorfaco/front-2023-1#readme) que se encuentra al acceder a este repositorio, se indica que **corresponde considerar la modalidad de "aula invertida" (flipped classroom en inglés)**. 

Por la modalidad a considerar, antes de la primera clase cada estudiante debería consultar el texto que sigue y tres videos en YouTube. 

Lo recomendable es hace la consulta en el siguiente orden:

- PRIMERO: Tomarse casi 15 minutos para ver [1.1: Introducción - Git y GitHub para Poetas](https://youtu.be/BCQHnlnPusY)

- SEGUNDO: Tomarse casi 15 minutos para ver [1.1: ¡Código! Programación para Principiantes con p5.js](https://www.youtube.com/watch?v=yPWkPOfnGsw)

- TERCERO: Leer lo que sigue (bajo el título de [Teoría](https://github.com/profesorfaco/front-2023-1/tree/main/sesion_01#teor%C3%ADa))

- CUARTO: Tomarse un poco más de 7 minutos para ver [1.2: Editor Web p5.js - Tutorial p5.js](https://youtu.be/MXs1cOlidWs) ¡Pero no hagan "sign up" llenando todos los casillero! Mejor sería hacer "log in" con cuenta personal en GitHub. 

- - - - - - - - 

#### Teoría

Para lanzarnos a la piscina sin haber averiguado su profundidad, aprovecharemos "el flotador" que nos ofrece [p5.js](https://p5js.org/es/):

> ¡**p5.js** es una biblioteca de JavaScript para la programación creativa, que busca hacer que programar sea accesible e inclusivo para artistas, diseñadores, educadores, principiantes y cualquier otra persona! **p5.js** es gratuito y de código abierto porque creemos que el software y las herramientas para aprenderlo deben ser accesibles para todos.

Esta biblioteca fue creada por [Lauren McCarthy](http://lauren-mccarthy.com/) y es desarrollada por una comunidad de colaboradores, con apoyo de [Processing Foundation](https://processingfoundation.org/). Entre los colaboradores hay 2 chilenos, que se han encargado de la traducción de referencias, tutoriales y [un libro](https://processingfoundation.press/product/introduccion-a-p5-js/) al castellano; ellos son: [Guillermo Montecinos](https://guillemontecinos.cl/) y [Aarón Montoya-Moraga](https://montoyamoraga.io/).

[p5.js](https://p5js.org/es/) fue creada como una reinterpretación de [Processing](https://processing.org/) para la web. 

En Processing, que se basa en [Java](https://es.wikipedia.org/wiki/Java_(lenguaje_de_programaci%C3%B3n)), cada *sketch* debe tener dos partes:

- `void setup()`; y 
- `void draw()`. 
 
Hay un `setup` que se ejecuta una única vez, en la partida. Y hay un `draw` que, por defecto, se ejecuta una y otra vez. 

Ahora, cambiemos el `void` de Java por el `function` de [JavaScript](https://es.wikipedia.org/wiki/JavaScript), y tenemos:

- `function setup()`; y 
- `function draw()`. 

Cuando ingresamos al [editor web de p5.js](https://editor.p5js.org/) podemos encontrar la misma estructura, que incluye la creación del [elemento HTML `canvas`](https://developer.mozilla.org/es/docs/Web/HTML/Element/canvas) con ancho y alto determanidos (creación que se ejecuta una única vez), y una definición para el color de fondo del mismo, que se dibuja (o pinta) una y otra vez:

```
function setup() {
  createCanvas(400, 400);
}

function draw() {
  background(220);
}
```

El tamaño del [`createCanvas`](https://p5js.org/es/reference/#/p5/createCanvas) se indica en pixeles (son 400 x 400 pixeles en el caso recién presentado). El color del [`background`](https://p5js.org/es/reference/#/p5/background) utiliza, por defecto, el modelo RGB; cuando se indica solo un número, se asume que se está definiendo algo entre negro (0,0,0) y blanco (255,255,255), porque sería un mismo número repitiéndose tres veces.

En el mismo [editor web de p5.js](https://editor.p5js.org/) podemos hacer cambios para asegurarnos de comprender las diferencias entre el `setup` y el `draw`. Podríamos crear un canvas más ancho que alto, donde la velocidad del re-dibujar no sea de 30 cuadros por segundo sino 2. Y podríamos pintar cada vez el fondo de un color distinto, dejando los valores de rojo, verde y azul al azar entre 0 y 255:

```
function setup() {
  createCanvas(400, 100);
  frameRate(2);
}

function draw() {
  background(random(0,255),random(0,255),random(0,255));
}
```

Utilizamos `createCanvas()`, `frameRate()`, `background()`, `random()`, que son parte de

> un conjunto completo de funcionalidades para dibujar. Sin embargo, no estás limitado solo a dibujar. Puedes tomar toda la página del navegador como tu bosquejo, incluyendo los objetos HTML5 para texto, entrada, video, cámara web y sonido.

Para enteder cómo es que esta biblioteca de JavaScript nos permite dibujar en el canvas o tomar toda la página del navegador, conviene agregar una nota sobre el [Modelo de Objeto de Documento (DOM)](https://developer.mozilla.org/es/docs/Glossary/DOM): **A través del DOM, los programas escritos en JavaScript pueden acceder y modificar la interpretación del contenido, estructura y estilo de la página web**. 

Para no entrar en tecnisismos, quedemonos con que JavaScript no modifica lo escrito, lo que modifica es la comprensión de lectura del navegador. Como el resultado está a la vista, quizá convenga la siguiente analogía para establecer la diferencia entre código fuente y DOM: Si capturaste una imagen con 3 elementos y agregas un cuarto "photoshopénadolo", en ningún caso modificas la escena capturada, pero todos podrán ver una imagen con 4 elementos. 

Estirando la analogía: Podríamos encontrar inconcruencias en los despliegue de (1) código fuente de la página y (2) elementos de la página. Esto es así porque en el código fuente de la página está lo capturado originalmente, mientras que en la vista de elementos de la misma página está lo "photoshopeado", y esto último coincide con la comprensión de lectura del navegador.

**Ahora volvamos al *Preview* del [editor web de p5.js](https://editor.p5js.org/): Lo que allí vemos al presionar *play* es lo "photoshopeado"**.

- - - - - - - - - - - - -

#### Exploración práctica

Continuaremos la exploración del *conjunto completo de funcionalidades para dibujar* en el [editor web de p5.js](https://editor.p5js.org/). 

Después pasaremos al editor de código fuente, copiando y pegando los tres archivos que genera el [editor web de p5.js](https://editor.p5js.org/), para trabajarlo de manera local.

Además del editor de código fuente, es muy necesario disponer de un navegador Firefox o Chrome, y saber como **ver código fuente**, [inspeccionar elementos](https://support.hostinger.es/es/articles/2333029-como-inspeccionar-los-elementos-del-sitio-web) y [abrir consola](https://transferwise.com/es/help/articles/2954851/como-abrir-la-consola-de-tu-navegador) en el que dispongan.

- - - - - - - 

###### [SIGUIENTE SESIÓN →](https://github.com/profesorfaco/front-2023-1/tree/main/sesion_02)
