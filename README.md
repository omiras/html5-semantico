# HTML: enlaces, imágenes y contenido multimedia

Construiremos una pequeña web para practicar enlaces, rutas, imágenes, audio, vídeo y un formulario de contacto.

## Demo

**Mira esta demo** — enlace pendiente de añadir por el docente.

## Antes de empezar

Abre esta carpeta completa en Visual Studio Code. Instala **Live Server**, de Ritwick Dey, si no lo tienes. Abre con Live Server el `index.html` situado junto a este README.

Esta rama `solution` contiene la solución de las cinco páginas. La rama `main` conserva los archivos iniciales para el alumnado. Abre la portada con Live Server y prueba todos los enlaces.

El vídeo local incluido es una muestra CC0 de los ejemplos de MDN (flores), utilizada como alternativa para que la solución funcione sin descargar otro archivo. Puedes sustituirlo por el vídeo propuesto de Pexels manteniendo el nombre `media/video-files/video.mp4`.

Picsum y la imagen con pie de foto forman parte de la solución de Imágenes.

## Orden de trabajo

| Paso | Archivo | Objetivo |
| --- | --- | --- |
| 1 | `enlaces/index.html` | Enlaces externos |
| 2 | `imagenes/index.html` | Imagen local y texto alternativo |
| 3 | Portada y páginas anteriores | Navegación progresiva |
| 4 | `media/index.html` | Audio y vídeo |
| 5 | `contacto/index.html` | Formulario de contacto sencillo |

Primero completa el contenido de Enlaces e Imágenes. Después construiremos el menú.

## 1. Enlaces externos

En `enlaces/index.html`, crea estos dos enlaces:

- Un enlace a `https://www.google.com/` que se abre en la misma pestaña.
- Un enlace a `https://www.20minutos.es/` que se abre en una pestaña nueva mediante `target="_blank"`.
- Sus textos deben permitir distinguir qué hace cada enlace.

**Pistas:** investiga `a`, `href` y `target`. El texto visible se escribe entre la apertura y el cierre del enlace.

**Resultado esperado:** título y dos enlaces funcionales con comportamientos distintos. Comprueba ambos.

Ayuda: [Crear enlaces (MDN)](https://developer.mozilla.org/es/docs/Learn_web_development/Core/Structuring_content/Creating_links).

## 2. Imágenes locales

En `imagenes/index.html`:

- Inserta `perrito.jpg`, de la carpeta `img`.
- Establece un ancho de **200 píxeles**, conservando sus proporciones.
- Añade un texto alternativo descriptivo y un párrafo debajo de la fotografía.

**Pistas:** utiliza `img`, `src`, `alt` y `width`. `img` no tiene etiqueta de cierre. Desde `imagenes` necesitas subir un nivel para acceder a la carpeta hermana `img`.

**Resultado esperado:** título, imagen visible de 200 píxeles de ancho y párrafo. Si no aparece, revisa la ruta, el nombre y la extensión.

Ayuda: [Imágenes en HTML (MDN)](https://developer.mozilla.org/es/docs/Learn_web_development/Core/Structuring_content/HTML_images).

### Imagen de Picsum

En la misma página de Imágenes, añade un apartado con un `h2` y una fotografía de [Picsum Photos](https://picsum.photos/). Puedes usar `https://picsum.photos/300/200` para solicitar una imagen de 300 por 200 píxeles. Añade un texto alternativo indicando que es una fotografía aleatoria. Necesita Internet; la caché puede hacer que una recarga repita la foto.

### Imagen con pie de foto

Añade otro apartado en Imágenes con una imagen local dentro de `figure` y un pie de foto en `figcaption`. Utiliza `img/gato.jpg`, incluida en la carpeta, con un ancho de 200 píxeles.

- **Texto alternativo sugerido:** «Gato atigrado de pecho blanco sentado al aire libre».
- **Pie de foto:** «Un joven gato atigrado fotografiado en Portugal».
- **Autor y licencia:** Alvesgaspar, [CC BY-SA 3.0](https://creativecommons.org/licenses/by-sa/3.0/). [Fuente: Wikimedia Commons](https://commons.wikimedia.org/wiki/File:Cat_November_2010-1a.jpg). Fotografía sin modificar. Incluye este crédito con sus enlaces en el pie de foto.

 La imagen debe tener su propio `alt`: el pie de foto visible no lo sustituye. Estos dos apartados son parte obligatoria del ejercicio.

**Resultado esperado de Imágenes:** fotografía local de 200 píxeles con su párrafo, fotografía de Picsum y una imagen agrupada con su pie de foto.

## 3. Navegación por etapas

Utiliza una lista de enlaces. No necesitas envolverla en un `div` ni en un `nav`.

1. **Portada → Enlaces:** convierte el texto Enlaces del menú principal en un enlace a `enlaces/index.html`.
2. **Enlaces → Portada:** añade en Enlaces un enlace Inicio que regrese al documento principal.
3. **Entre carpetas:** incorpora Imágenes. Desde Enlaces debes poder ir a Imágenes y desde Imágenes regresar a Inicio o ir a Enlaces.
4. **Multimedia:** después de trabajar Multimedia, incorpora esa página al menú.
5. **Contacto:** incorpora también Contacto, con su formulario. Las cinco páginas deben permitir llegar a las otras cuatro.

Puedes copiar la lista, pero **adapta las rutas a la ubicación de cada documento**.

**Pistas:** `./` parte de la carpeta actual; `../` sube un nivel. Después puedes indicar otra carpeta y archivo. Una URL completa como `https://www.google.com/` lleva a un sitio externo.

Usa rutas relativas. Evita empezar por `/`: apunta a la raíz del servidor de Live Server, que puede no coincidir con esta carpeta.

**Resultado esperado:** puedes recorrer las cinco páginas sin usar el botón Atrás ni encontrar archivos inexistentes.

Ayuda: [Rutas relativas y absolutas](https://lenguajehtml.com/html/texto/enlaces-o-hipervinculos/#rutas-relativas-o-absolutas).

## 4. Audio y vídeo

En `media/index.html`, crea dos apartados con `h2`: Audio y Vídeo.

### Audio

Inserta `audio-files/meowing-cat-sound.mp3`, que ya está incluido. Investiga `audio` y muestra los controles con `controls`. Comprueba reproducción y pausa.

### Vídeo

Fíjate en el vídeo dentro de `media/video-files/`. 

Insértalo con la etiqueta `video`, muestra sus controles y establece un ancho de 400 píxeles. Comprueba que se reproduce. No añadas reproducción automática.

**Pistas:** ambos reproductores admiten `src` y `controls`. Las rutas parten de `media/index.html`. 

**Resultado esperado:** reproductores de audio y vídeo funcionales con controles. Completa también la navegación hacia esta página y desde ella.

Ayuda: [Audio en HTML](https://developer.mozilla.org/es/docs/Web/HTML/Reference/Elements/audio) y [Vídeo en HTML](https://developer.mozilla.org/es/docs/Web/HTML/Reference/Elements/video).

## 5. Contacto

Añade **Contacto** a la lista del menú de todas las páginas. Su destino desde la portada es `contacto/index.html`; desde Enlaces, Imágenes y Multimedia es `../contacto/index.html`.

En `contacto/index.html` encontrarás un formulario sencillo con solo tres campos:

- **Asunto:** texto de una línea, con `input type="text"`.
- **Email:** dirección de correo, con `input type="email"`.
- **Comentarios:** texto de varias líneas, con `textarea`.

Cada campo tiene su `label`, `id` y `name`. El botón **Enviar** permite comprobar los campos obligatorios y el formato del email. Es una práctica de HTML: todavía no hay un servicio que reciba o envíe los mensajes.

Completa la lista de navegación de Contacto para volver a Inicio o visitar Enlaces, Imágenes y Multimedia. Usa `../` para salir de la carpeta Contacto.

**Resultado esperado:** formulario con los tres campos y el botón Enviar, sin CSS ni campos adicionales.

## Comprueba tu trabajo

- Cada página tiene un título de pestaña adecuado, un `h1` y el idioma `es`.
- Todos los enlaces del menú funcionan desde todas las páginas.
- Las imágenes locales tienen un `alt` descriptivo, Picsum carga y hay una imagen con `figure` y `figcaption`.
- El audio y el vídeo se reproducen y tienen controles.
- Contacto aparece en todos los menús y muestra Asunto, Email y Comentarios.
- El código está indentado y correctamente anidado.
- Comprueba cada documento completo en el [validador W3C](https://validator.w3.org/#validate_by_input). Corrige los errores y consulta las advertencias que no entiendas.
