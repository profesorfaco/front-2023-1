# Introducción al Desarrollo Front End con HTML, CSS y JavaScript

### Unidad III: Herramientas para el diseño/desarrollo ágil de sitios y aplicaciones Web

### Jueves 11 de mayo → sesion_08 → Consideraciones de usabilidad desde la primera definición del proyecto

- - - - - -

#### Teoría

Partamos con una definición estándar de **usabilidad**: 

> Usabilidad es el grado en que un sistema, producto o servicio puede ser utilizado por **usuarios específicos** para alcanzar **objetivos específicos** con eficacia, eficiencia y satisfacción en **un contexto de uso específico** ([ISO 9241-11:2018](https://www.iso.org/obp/ui/#iso:std:iso:9241:-11:ed-2:v1:en))

Son tres especificidades que deberían desplazar lejos la idea de "esto le tendría que servir a cualquiera, en cualquier lugar". Una idea que deja a quien diseña con dos opciones: 

La primera opción sería maquillar la interfaz según el gusto del cliente que sabe poco de diseño (quien sepa de diseño no será displicente con lo específico).

![cliente](https://user-images.githubusercontent.com/7999767/170147539-fbecfc9a-1fca-494e-9713-addbb62c5bf3.png) 

La segunda opción sería reducir la interfaz al mínimo, lo que impide resolver operaciones complejas, como pasa con un Tek Pal Universal Remote Control. 

![tek-pal](https://user-images.githubusercontent.com/7999767/170147515-5a16f5e2-a6bd-4bc8-8f34-d7bcfc20e529.jpg)

Para evitarnos los extremos de maquillar o reducir al mínimo, tendremos que definir **para quién** hacemos lo que hacemos. Así poder acotar las posibilidades de decisiones de diseño por y para personas con **determinados objetivos situados**, que pueden ser: 

- *objetivos de experiencia* → Más viscerales → ¿Cómo quiere sentirse la persona? 
- *objetivos de meta* → Más prácticas → ¿Qué quiere hacer la persona?
- *objetivos de vida* → Más re-flexivas → ¿Quién quiere ser la persona?

Se dice objetivos situados porque, probablemente, lo que una persona quiere sentir en un viaje familiar, de vacaciones al campo, es distinto de lo que quiere sentir en una montaña rusa. Lo que quiere hacer cuando rinde su fuerza laboral es distinto de lo que quiere hacer en tiempo de ocio. Y lo que quiere ser en público, con extraños, puede ser distinto de lo que quiere ser en casa con sus más cercanos.

Para más detalles sobre los objetivos, conviene revisar el libro *About Face 4*, de Cooper et al (2014), entre páginas 73 y 78.

Además de los objetivos situados están las **habilidades de cada persona**, **que** desde una perspectiva física **pueden verse limitadas** en distintos contextos de manera permanente, temporal o circunstancial, según se les exija: 

- *Tocar* → mano amputada, mano quemada o mano ocupada. 
- *Ver* → ceguera, cataratas o distracción.
- *Escuchar* → sordera, infección al oído o exceso de ruido. 
- *Hablar* → falta de cuerdas vocales, laringitis o acento con falta de práctica. 

Para más detalles sobre lo recién presentado, conviene revisar los *resources* de [Incluse Design de Microsoft](https://www.microsoft.com/design/winclusive/).

También hay habilidades cognitivas que pueden verse limitadas tal como las físicas, lo que implica diferentes posibilidades de comprensión, aprendizaje y motivación. E incluso hay asuntos técnicos que pueden limitarnos, como ya pudieron experimentarlo por dos años de clases remotas, donde se dependía de *cómo f-ncio--ba la c-nex--n c-d- -ía*, y se vuelve a experimentar en la presencialidad cuando, por ejemplo, el *datashow* cambia los colores como si fuera [daltónico](https://chrome.google.com/webstore/detail/colorblind-dalton-for-goo/afcafnelafcgjinkaeohkalmfececool) (como lo es [1 de cada 12 hombres](https://www.instagram.com/p/CdyxdJws4uu/); en mujeres lo es 1 de cada 200).

- - - - - - - 

Con todo lo presentado, podría hacer sentido el tener que decidir por lo específico varias veces. 

La pregunta ahora podría ser: ¿Cómo mostrar mi decisión? La respuesta en este caso podría reducirse a un concepto común en diseño de experiencia de usuario (UX): *proto persona*.

- ¿Qué son las Proto Personas?: https://blog.ida.cl/experiencia-de-usuario/que-son-las-proto-personas/

- ¿Qué es una proto persona?: https://www.questionpro.com/blog/es/que-es-una-proto-persona/

- ¿Cómo crear una Proto-Persona?: https://carlosguardiola.com/2017/10/14/como-crear-una-proto-persona/

- 3 Persona Types: Lightweight, Qualitative, and Statistical: https://www.nngroup.com/articles/persona-types/

- Personas vs. Archetypes: https://www.nngroup.com/articles/personas-archetypes/

Lo más conveniente es que su decisión, aunque sea específica, reconozca un rango de posibilidades a los dos extremos de lo más típico: https://www.designkit.org/methods/extremes-and-mainstreams

- - - - - - - 

#### Exploración práctica

En esta clase comenzaremos a desarrollar un sitio web o un prototipo avanzado de aplicación web, donde aplicarán [lo aprendido en las primeras sesiones de la asignatura](https://profesorfaco.github.io/front-2023-1/sesion_09/dispersion.html).

El primer paso para este desarrollo será definir sus correspondientes usuarias y usuarios, cada uno junto a objetivos y contextos de uso específicos, mediante: 

- Una página web de diseño adaptativo (*responsive*) en el que se **presenten 3 proto-personas**. 

- Cada proto-persona debe presentarse mediante texto, ilustraciones y gráficos.

Para los datos a presentar en cada gráfico, puede usar alguna de las secciones en el [PDF que se incluye en esta carpeta](https://github.com/profesorfaco/front-2023-1/blob/main/sesion_10/fragmento-sazerac-book.pdf). 

Por ejemplo, usted puede caracterizar a una proto-persona como 8 en cálida, 4 en seria, 5 en innovadora, 1 en ordenada y 10 en popular, y con eso armar un [radar chart](https://www.chartjs.org/docs/latest/charts/radar.html). Las otras dos proto-personas podrían tener otros números para las mismas dimensiones. ¿Y de dónde saqué esas dimensiones? De la primera página del PDF, a la izquierda. 

Otro ejemplo: Un [line chart](https://www.chartjs.org/docs/latest/charts/line.html) que muestre los usos de la conexión a Internet un día normal de la persona, con una línea para Google, otra para Gmail, otra Drive, otra para Instagram, otra para Instagram, etc. En determinadas horas del día (entre 0 y 23), algunas líneas pueden estar más arriba que otras ¿Y de dónde saqué esto de las horas? De la segunda página del mismo PDF, abajo.

¡Otros más! Cómo divide su día laboral en un [gráfico de dona](https://www.chartjs.org/docs/latest/charts/doughnut.html) o todos los días de la semana en un [gráfico de barras apiladas](https://www.chartjs.org/docs/latest/samples/bar/stacked.html)

- - - - - - - 


###### [← SESIÓN ANTERIOR](https://github.com/profesorfaco/front-2023-1/tree/main/sesion_07) — [SIGUIENTE SESIÓN →](https://github.com/profesorfaco/front-2023-1/tree/main/sesion_09)
