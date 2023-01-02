# Introducción al Desarrollo Front End con HTML, CSS y JavaScript

### Unidad I: Bocetos de introducción a la programación

### Jueves 23 de marzo → sesion_02 → HTML, CSS y p5.js (una biblioteca de JavaScript)

Repitamos una idea. En el [README.md](https://github.com/profesorfaco/front-2023-1#readme) que se encuentra al acceder a este repositorio, pudieron leer que para este electivo **corresponde considerar la modalidad de "aula invertida" (*flipped classroom* en inglés)**, modalidad que saca la exposición de contenidos de las horas directas y la confía al tiempo de aprendizaje autónomo de cada estudiante. 

Por la modalidad a considerar, antes la segunda sesión también corresponde revisar algo de contenido en EL SIGUIENTE ORDEN:

- PRIMERO: [1.1: ¡Código! Programación para Principiantes con p5.js](https://www.youtube.com/watch?v=yPWkPOfnGsw)

- SEGUNDO: Leer lo que sigue (bajo el título de [Teoría](#teor%C3%ADa))

- TERCERO: Leer [JavaScript Para Gatos: Una introducción para nuevos programadores](https://jsparagatos.com/) hasta el subtítulo *Código de terceros*.

- - - - - - - - 

#### Teoría

En esta sesión vamos a echarle un primer vistazo al fondo de la piscina a la que ya nos lanzamos.

En el [editor web de p5.js](https://editor.p5js.org/) podrán encontrar a la izquierda, justo debajo de *play*, este símbolo: `>`. Después del clic se desplegará una ventana de izquierda a derecha, dentro de la que se ven tres archivos:

- `index.html` 
- `sketch.js` 
- `style.css`

Si volvemos a la analogía del photoshopeo de la sesión pasada: En el `index.html` se describen los elementos de la captura original a mostrar, en el `style.css` se describe cómo mostrarlos y en el `sketch.js` se programa el "photoshopeo" (eso que se muestre, bajo ciertas condiciones, que puede ser distinto de lo que se describe originalmente en el `index.html`).

No corresponde pensar en tales `.html`, `.css` y `.js` como extensiones de archivos que deben abrirse en programas determinados, así como el `.psd` se abre y edita con Photoshop y el `.ai` con Illustrator. HTML, CSS y JavaScript son lenguajes que se pueden escribir en cualquier editor de código fuente, incluso con un block de notas: ¡Guardamos lo escrito como `.txt`, luego cambiamos la extensión por la que corresponda y listo!

Dos de los lenguajes mencionados sirven para describir y uno sirve para programar:

- **HTML (HyperText Markup Language)**. Lenguaje estándar que describe la estructura de las páginas web (qué es lo que contiene la página). HTML5 es la versión más reciente de este lenguaje. El bloque constructivo más básico del HTML es el elemento. Cada elemento de HTML se escribe, generalmente, entre etiquetas: `<etiqueta>contenido</etiqueta>` → [Entonces, ¿qué es HTML en realidad?](https://developer.mozilla.org/es/docs/Learn/Getting_started_with_the_web/HTML_basics#entonces_%C2%BFqu%C3%A9_es_html_en_realidad)

- **CSS (Cascading Style Sheets)**. Lenguaje estándar que describe la presentación de las páginas web (cómo se muestra lo que contiene la página). CSS3 es la versión más reciente de este lenguaje. Su unidad más básica es la regla. Cada regla se inicia con un selector, seguido de paréntesis de llave `{…}`. Tal paréntesis contiene un bloque de declaraciones. En tal bloque cada declaración se separa de otra mediante punto y coma `;`. Una declaración se compone del par `propiedad: valor`. Con todo lo dicho, una regla se escribirá, generalmente, de la siguiente manera: `selector{ propiedad: valor; }` → [Entonces ¿qué es CSS, realmente?](https://developer.mozilla.org/es/docs/Learn/Getting_started_with_the_web/CSS_basics#entonces_%C2%BFqu%C3%A9_es_css_realmente)

- **JS (JavaScript)**. Lenguaje de programación que controla el comportamiento de las páginas web (qué hace la página). Con JS se pueden escribir secuencias de instrucciones con las que una computadora realizará una tarea determinada en el navegador. Su estructura puede variar dependiendo de la lógica de cada instrucción, la [versión](https://www.w3schools.com/js/js_versions.asp) en uso, la biblioteca (*library*) de JavaScript en la que nos apoyemos, o el *framework* de programación en el que se basa el trabajo; podemos imaginar que una biblioteca es como una selección de ingredientes listos para poder preparar determinado tipo de comida, mientras que el *framework* te permite preparar un banquete si es que ya tienes suficiente experiencia en la cocina → [¿Qué es JavaScript realmente?](https://developer.mozilla.org/es/docs/Learn/Getting_started_with_the_web/JavaScript_basics#%C2%BFqu%C3%A9_es_javascript_realmente)

- - - - - - - - - - - - - - 

#### Práctica (horas directas)

Volvamos al [editor web de p5.js](https://editor.p5js.org/) y desplieguen la caja donde se ven los tres archivos:

1. En el `index.html` pueden leer: 

```
<!DOCTYPE html>
<html lang="en">
  <head>
    <script src="https://cdnjs.cloudflare.com/ajax/libs/p5.js/1.5.0/p5.js"></script>
    <script src="https://cdnjs.cloudflare.com/ajax/libs/p5.js/1.5.0/addons/p5.sound.min.js"></script>
    <link rel="stylesheet" type="text/css" href="style.css">
    <meta charset="utf-8" />

  </head>
  <body>
    <main>
    </main>
    <script src="sketch.js"></script>
  </body>
</html>
```

2. En el `sketch.js` pueden leer:

```
function setup() {
  createCanvas(400, 400);
}

function draw() {
  background(220);
}
```

3. En el `style.css` pueden leer:

```
html, body {
  margin: 0;
  padding: 0;
}
canvas {
  display: block;
}
```

Ahora, asegurémonos de haber hecho *log in* al [editor web de p5.js](https://editor.p5js.org/) y guardemos el *sketch* para después descargarlo.

Pongamos lo descargado en un lugar accesible (no en la carpeta de descargas, podría ser en el escritorio), y allí borren 2 de los 5 archivos descargados, para quedarnos sólo con los 3 ya varias veces referidos. 

Una vez tengamos la carpeta lista, vamos a crear un nuevo proyecto en https://phcode.dev/

Y pronto haremos una modificación para la que será necesario contar con este vínculo: https://cdnjs.com/libraries/p5.js

- - - - - - - 

###### [← SESIÓN ANTERIOR](https://github.com/profesorfaco/front-2023-1/tree/main/sesion_01) — [SIGUIENTE SESIÓN →](https://github.com/profesorfaco/front-2023-1/tree/main/sesion_03)
