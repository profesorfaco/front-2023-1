# Introducción al Desarrollo Front End con HTML, CSS y JavaScript

### Unidad II: Tecnologías fundamentales para la construcción de páginas Web

#### Jueves 20 de abril → sesion_06 →  JavaScript con Bootstrap v5

- - - - - - - - 

Ante de la clase del 20 de abril es necesario que lean lo que sigue (bajo el título de [Teoría](#teor%C3%ADa)), es recomendable que visiten los vínculos allí incluidos y hagan el ejercicio de `ejemplo-1.html` y `ejemplo-2.html`.

- - - - - - - -

#### Teoría

Esta clase abrirá un paréntesis para revisar un aspecto pendiente en JavaScript, aspecto que debe clarificarse antes de la siguiente sesión.

Para comenzar, partamos con un 18261884. 

Si nos entregan tal secuencia de números, sin contexto alguno, resultaría inútil. Pero es distinto de la siguiente manera: 

| País      |  Población       | Superficie     |
|:----------|:-----------------|:---------------|
| Chile     | 18261884         | 756102         |

Entendiendo cómo funciona una tabla, contamos con una clara orientación para la utilización de tal número como información sobre algo concreto: La población en Chile. 

Además del dato de la población de Chile, contamos con su superficie. Si dividimos el primer dato numérico por el segundo, obtenemos la densidad de la población en Chile. El resultado de aquella división es 24,15267252.

Los números 18261884 y 24,15267252 tienen una diferencia que corresponde apuntar:

- **18261884** es un número entero, un `int` (del inglés *integer*).

- **24,15267252** es un número de coma flotante, un `float` (del inglés *floating point number*; y no se olviden de esta diferencia, lo que para nosotros es coma, *for them* es punto, y el *coding* se hace en *english*).

A estos dos tipos de datos, podemos agregar: 

- **true** o **false** como las dos opciones posibles de un [tipo de dato lógico](https://es.wikipedia.org/wiki/Tipo_de_dato_l%C3%B3gico) (bool: *boolean*)

- **"A"** como un carácter (char: *character*)

Notemos que en el tipo de dato numérico y booleano no se usan comillas, pero en el caso del caracter sí. 

Mencionamos `int`, `float`, `bool` y `char` porque son palabras que en lenguajes de programación más clásicos se reservan para **declarar que tal variable almacenará tal tipo de dato**. 

**En JavaScript podemos crear toda variables con una única palabra reservada,`var`**. También podemos usar `let` y `const`. Para entender la diferencia, nos conviene consultar el artículo [Var, let y const. ¿Donde, cuando y por qué?](https://medium.com/@tatymolys/var-let-y-const-donde-cuando-y-por-qu%C3%A9-d4a0ee66883b).

Usando únicamente `var`, en JavaScript podemos asignar como contenido de la variable todas las siguientes alternativas:

```
var a = 18261884;
var b = 24.15267252;
var c = true;
var d = "Lisa the Vegetarian";
var e = ["Marge Simpson", "Homer Simpson", "Bart Simpson", "Lisa Simpson", "Maggie Simpson"];
var f = {
    mom: "Luann Van Houten",
    dad: "Kirk Van Houten",
    child: "Milhouse Van Houten"
};
var g = {
    mom: "Marge Simpson",
    dad: "Homer Simpson",
    children: ["Bart Simpson", "Lisa Simpson", "Maggie Simpson"]
};
var h = [
    {
        mom: "Marge",
        dad: "Homer",
        children: ["Bart", "Lisa", "Maggie"]
    },
    {
        mom: "Manjula",
        dad: "Apu",
        children: ["Poonam", "Sashi", "Pria", "Uma", "Anoop", "Sandeep", "Nabendu", "Gheet"]
    }
];

```

**Lo que cambia viene después del signo igual `=`, que en este caso está asignando contenido a cada variable.** 

Las variables `a`, `b` y `c` no requieren comillas. La variable `d`, que contiene una cadena de caracteres (*string*) sí usa comillas. 

La variable `e`, que contiene un arreglo, usa paréntesis cuadrado y cada elemento, por tratarse de un *string*, usa comillas (si fuesen números o booleanos no las usarían). 

La variable `f`, que contiene un objeto, usa paréntesis de llave que en su interior contiene pares de `nombre:valor`. 

Las variables `g` y `h` son mezclas de las anteriores.

Si necesitamos el valor de las variables `a`, `b`, `c` o `d`, basta con pedirlo directamente. Pero el caso es distinto si necesitamos un valor específico dentro de las variables  `e`, `f`, `g` o `h`.

Vamos con la variable `e`. Digamos que necesitamos a `Marge Simpson`. Para solicitarla tenemos que escribir `e[0]`, porque se encuentra en la primera posición del arreglo asignado como valor a la variable `e`. Si escribimos `e[1]` el resultado sería `Homer Simpson`. Corresponde **recordar que la primera posición es cero, no uno**.

Pasemos a la variable `f`. Si necesitamos escribir la frase `Fue Kirk Van Houten quien intentó dibujar la dignidad`, tendríamos que escribir `'Fue ' + f.dad + ' quien intentó dibujar la dignidad'`.

Vamos por la variable `g`. Si necesitamos escribir la frase `El chupete de Maggie Simpson`, tendríamos que escribir `'El chupete de ' + g.children[2]`.

¿Qué utilidad tienen variables como la `f`, `g` y `h`?

Un ejemplo de su utilidad aparece en el siguiente código, que pueden copiar y pegar en un documento nuevo. Documento que podrían guardar como `ejemplo-1.html` antes de visualizarlo en un navegador web.

```
<!DOCTYPE html>
<html lang="es">
    <head>
        <meta charset="utf-8" />
        <meta name="viewport" content="width=device-width, initial-scale=1" />
        <title>Primer ejemplo</title>
        <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0-alpha3/dist/css/bootstrap.min.css" rel="stylesheet" integrity="sha384-KK94CHFLLe+nY2dmCWGMq91rCGa5gtU4mk92HdvYe+M/SXH301p5ILy+dN9+nJOZ" crossorigin="anonymous" />
    </head>
    <body>
        <main class="p-4">
            <div class="container" id="alla">
                <div class="row row-cols-1 row-cols-sm-2 row-cols-md-3 g-3" id="aca"></div>
            </div>
        </main>
        <script>
            const data = [
                { img: "https://picsum.photos/id/0/800/500.webp", title: "Primer lorem ipsum dolor sit amet, consectetur adipiscing elit." },
                { img: "https://picsum.photos/id/10/800/500.webp", title: "Segundo lorem ipsum dolor sit amet, consectetur adipiscing elit." },
                { img: "https://picsum.photos/id/20/800/500.webp", title: "Tercer lorem ipsum dolor sit amet, consectetur adipiscing elit." },
                { img: "https://picsum.photos/id/30/800/500.webp", title: "Cuarto lorem ipsum dolor sit amet, consectetur adipiscing elit." },
                { img: "https://picsum.photos/id/40/800/500.webp", title: "Quinto lorem ipsum dolor sit amet, consectetur adipiscing elit." },
                { img: "https://picsum.photos/id/50/800/500.webp", title: "Sexto lorem ipsum dolor sit amet, consectetur adipiscing elit." }
            ];
            const donde = document.querySelector("#aca");
            data.forEach((x,i) => {
                donde.innerHTML += '<div class="col"><div class="card shadow-sm"><img class="card-img-top" src="' + x.img + '"><div class="card-body"><p class="card-title">' + x.title + '</p></div></div></div>';
            }); 
        </script>
    </body>
</html>
```

Lo que tenemos en el `ejemplo-1.html` es una variable de nombre `data` declarada como `const`, porque contiene algo que no variará, que permanecerá constante. Esta variable/constante contiene un arreglo que, a su vez, contiene 6 objetos.

En la línea que sigue a la `data` encontramos un `donde`, que es una variable/constante a la que se le asigna como valor un elemento del documento mediante [`querySelector()`](https://developer.mozilla.org/es/docs/Web/API/Document/querySelector).

Más abajo, tal variable de nombre `data` es explorada por un [`forEach()`](https://developer.mozilla.org/es/docs/Web/JavaScript/Reference/Global_Objects/Array/forEach#descripci%C3%B3n). Y por cada elemento presente en el arreglo se agrega (mediante un [`innerHTML`](https://developer.mozilla.org/es/docs/Web/API/Element/innerHTML) seguido del signo `+=`) cierta sintexis HTML al `donde` en el [Modelo de Objeto de Documento (DOM)](https://developer.mozilla.org/es/docs/Glossary/DOM). No se agrega al código fuente.

Y lo que sigue es un código que pueden copiar y pegar en un documento nuevo. Documento que podrían guardar como `ejemplo-2.html` antes de visualizarlo en un navegador web.

```
<!DOCTYPE html>
<html lang="es">
    <head>
        <meta charset="utf-8" />
        <meta name="viewport" content="width=device-width, initial-scale=1" />
        <title>Primer ejemplo</title>
        <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0-alpha3/dist/css/bootstrap.min.css" rel="stylesheet" integrity="sha384-KK94CHFLLe+nY2dmCWGMq91rCGa5gtU4mk92HdvYe+M/SXH301p5ILy+dN9+nJOZ" crossorigin="anonymous" />
    </head>
    <body>
        <main class="p-4">
            <div class="container" id="alla">
                <div class="row row-cols-1 row-cols-sm-2 row-cols-md-3 g-3" id="aca"></div>
            </div>
        </main>
        <script>
            const data = [
                { img: "https://picsum.photos/id/0/800/500.webp", title: "Primer lorem ipsum dolor sit amet, consectetur adipiscing elit." },
                { img: "https://picsum.photos/id/10/800/500.webp", title: "Segundo lorem ipsum dolor sit amet, consectetur adipiscing elit." },
                { img: "https://picsum.photos/id/20/800/500.webp", title: "Tercer lorem ipsum dolor sit amet, consectetur adipiscing elit." },
                { img: "https://picsum.photos/id/30/800/500.webp", title: "Cuarto lorem ipsum dolor sit amet, consectetur adipiscing elit." },
                { img: "https://picsum.photos/id/40/800/500.webp", title: "Quinto lorem ipsum dolor sit amet, consectetur adipiscing elit." },
                { img: "https://picsum.photos/id/50/800/500.webp", title: "Sexto lorem ipsum dolor sit amet, consectetur adipiscing elit." }
            ];
            const donde = document.querySelector("#aca");
            data.forEach((x,i) => {
                donde.innerHTML += '<div class="col"><div class="card shadow-sm"><img class="card-img-top" src="' + x.img + '"><div class="card-body"><p class="card-title"><a href="#" onclick = "detalle('+i+')" class="link-dark">' + x.title + '</a></p></div></div></div>';
            });
            const dondemas = document.querySelector("#alla");
            function detalle(nro) {
                dondemas.innerHTML = '<div class="row"><div class="col-sm-11 col-md-10 col-lg-9 col-xl-8 col-xxl-7 mx-auto"><button onClick="window.location.reload();" class="btn btn-outline-secondary shadow-sm mb-3">&larr; Volver</button><h1 class="title-decoration-underline">' + data[nro].title + '</h1><img class="w-100 my-3 rounded" src="' + data[nro].img + '"><p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Cras nibh turpis, ullamcorper ut urna mattis, pulvinar faucibus massa. Nullam ac pellentesque mauris. Cras porttitor, diam sed malesuada malesuada, nunc turpis porttitor massa, vitae suscipit risus odio vel odio. Donec risus massa, condimentum nec enim non, laoreet feugiat nibh. Vivamus nec nisl in dolor placerat mattis. Proin rutrum non arcu non tempus. Ut at posuere orci. Nam sit amet magna laoreet, scelerisque mauris et, lacinia lectus. Sed felis turpis, facilisis ut nunc a, varius sollicitudin elit. Ut pharetra, mauris at scelerisque posuere, lacus dolor dapibus magna, eu maximus enim est eu quam. Morbi eu odio suscipit, cursus sem in, commodo est.</p></div></div>';  
            }  
        </script>
    </body>
</html>
```

Noten que en este ejemplo se usa un `donde.innerHTML +=` y un `dondemas.innerHTML =`. Son distintas variables a las que se les asigna como valor un elemento distinto del documento mediante `querySelector()`, y son distintos signos siguiendo al `innerHTML`: Un `+=` y un `=`. El primer signo agrega mientras el segundo reemplaza cierta sintexis HTML al [Modelo de Objeto de Documento (DOM)](https://developer.mozilla.org/es/docs/Glossary/DOM).

- - - - - - - - - -

#### Exploración práctica

Hoy nos aprovecharemos nuevamente de un [ejemplo](https://getbootstrap.com/docs/5.3/examples/) del sitio web oficial de Bootstrap: https://getbootstrap.com/docs/5.3/examples/album/

Corresponde repetir la operación de copiar el código fuente completo, para pegarlo en un documento recién creado en un editor de código fuente, para luego guardarlo como `index.html` y hacer los ajustes necesario para que se vea tal como está ofrecido en línea. 

Nuevamente, si necesitan ordenar el código, aprovechen https://webformatter.com/html - Y para visualizar prefieran prefieran Chrome o Firefox, eviten Edge y nunca usen Safari (tampoco se confíen de la visualización que ofrece https://phcode.dev/) 

- - - - - - - - - - 

###### [← SESIÓN ANTERIOR](https://github.com/profesorfaco/front-2023-1/tree/main/sesion_05) — [SIGUIENTE SESIÓN →](https://github.com/profesorfaco/front-2023-1/tree/main/sesion_07)
