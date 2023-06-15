### Unidad III: Herramientas para el diseño/desarrollo ágil de sitios y aplicaciones Web

### Jueves 15 de junio → sesion_13 → Pre-evaluación de cierre Nº3

- - - - - - -

#### Teoría

**Hay dos pruebas rápidas que se pueden hacer para revisar la accesibilidad en cualquier página web:**

1. Si se está visitando la página **con Chrome**, se puede buscar en el menú la opción Editar > Voz > Empezar a hablar.

2. Si se está visitando la página **con Firefox**, se puede buscar en el menú la opción Ver > Estilo de página > sin estilo.

Revisando lo que se dicte (o hable) y se vea sin estilo, se tiene una primera aproximación al orden que podría hacer un sitio accesible o inaccesible: Si se ordena claramente a ojos cerrados o sin estilo, ya se cumple con algo importante.

**Si se cuenta con más tiempo, conviene complementar las pruebas rápidas recién mencionadas con [WAVE: Web Accessibility Evaluation Tool](https://wave.webaim.org/)**.

Un problema común en la evaluación es la falta de contraste figura/fondo. Este se puede resolver revisando y ajustando los código de colores figura/fondo en https://webaim.org/resources/contrastchecker/

**Para hacer una auditoría que considere rendimiento, además de accesibilidad, buenas práctica de programación, SEO (Search Engine Optimization; posicionamiento en buscadores) y PWA (Progressive Web App), podemos usar [LightHouse](https://developers.google.com/web/tools/lighthouse?hl=es)**.

Lighthouse genera reportes en dos versiones: [resumida](https://github.com/profesorfaco/infografia/tree/main/clase-5/reportes) o extendida, en distintos formatos (hasta en [JSON](https://www.json.org/json-es.html)).

**Es probable que el reporte de LightHouse nos recuerde que**:

1. **algunas imágenes podrían pesar menos** – por las capacidades de almacenaje y transferencia actuales, podemos malacostumbrarnos a omitir el equilibrio entre peso y resolución… *¡Déjala así no más, y mándala por [WeTransfer](https://wetransfer.com/)!* Pero nadie esperará la aparición de una imagen en un sitio o aplicación web tal como se espera la descarga de lo compartido vía WeTransfer; para reencontrar el equilibrio, conviene: 
   
    - optimizar imágenes en [Photoshop](https://helpx.adobe.com/es/photoshop-elements/using/optimizing-images.html);
    - optimizarlas un poco más con [TinyPNG](https://tinypng.com/); e 
    - investigar sobre [WebP](https://developers.google.com/speed/webp)

2. **se podría mejorar el posicionamiento en buscadores** (SEO; Search Engine Optimization) – las máquinas necesitan datos o, mejor dicho, metadatos. Con ellos pueden catalogar cada página web. Para [cuidar los metadatos](https://developers.google.com/search/docs/advanced/crawling/special-tags?hl=es), es recomendable:

    - hacer una revisión con https://www.heymeta.com/
    - hacer una edición con https://megatags.co/

- - - - - - -

#### Exploración práctica

En esta clase continuaremos con el desarrollo de su sitio web o prototipo avanzado de aplicación web.

El cuarto paso consiste en poner a prueba lo avanzado, con las técnicas recién compartidas.

- - - - - - - 

###### [← SESIÓN ANTERIOR](https://github.com/profesorfaco/front-2023-1/tree/main/sesion_11) — [SIGUIENTE SESIÓN →](https://github.com/profesorfaco/front-2023-1/tree/main/sesion_15)
