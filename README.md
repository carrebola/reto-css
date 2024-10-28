# Práctica: Creación de una Página Web Paso a Paso

Bienvenido a esta guía paso a paso sobre cómo crear una página web desde cero usando HTML y CSS. Esta guía está pensada para principiantes, por lo que se explican todos los conceptos detalladamente para que puedas entender cada parte del proceso. ¡Vamos allá!

## Paso 1: Configuración Inicial del Proyecto
1. **Crea una carpeta para tu proyecto** y dentro de ella crea un archivo llamado `index.html`.
   - Puedes crear la carpeta en tu computadora con el nombre que desees, por ejemplo: `mi_primera_web`.
2. Abre el archivo `index.html` en un editor de texto. Puedes usar un editor como **VS Code**, **Sublime Text**, o incluso el bloc de notas de tu computadora. VS Code es muy popular y fácil de usar.
3. Escribe la estructura básica de un documento HTML5. A continuación se muestra cómo debe quedar:
   ```html
   <!DOCTYPE html>
   <html>
     <head>
       <meta charset="UTF-8">
       <title>Mi Primera Página Web</title>
     </head>
     <body>
       <!-- Todo el contenido visible irá aquí dentro del body -->
     </body>
   </html>
   ```
   - **`<!DOCTYPE html>`**: Esto indica que estamos usando HTML5, la versión más moderna de HTML.
   - **`<html>`**: Esta etiqueta es la que define el comienzo y el fin de nuestro documento HTML.
   - **`<head>`**: Aquí se define la información sobre nuestra página, como el título, enlaces a archivos CSS, y otras configuraciones importantes.
   - **`<meta charset="UTF-8">`**: Asegura que nuestra página pueda mostrar caracteres especiales, como letras con acentos.
   - **`<title>`**: Define el título de la página. Este es el texto que aparece en la pestaña del navegador.
   - **`<body>`**: Todo lo que queremos mostrar al usuario irá dentro de esta etiqueta.

## Paso 2: Estructura del Contenido
### Creación del Encabezado y la Navegación
1. **Agrega un `<header>`** dentro del `<body>`. Este `header` se usará para mostrar el menú de navegación.
   ```html
   <header>
     <nav>
       <ul>
         <li><a href="#inicio">Inicio</a></li>
         <li><a href="#sobre-mi">Sobre Mí</a></li>
         <li><a href="#servicios">Servicios</a></li>
       </ul>
     </nav>
   </header>
   ```
   - **`<header>`**: Se usa para definir una cabecera o encabezado de la página.
   - **`<nav>`**: Este elemento se usa para definir la navegación.
   - **`<ul>`**: Crea una lista no ordenada.
   - **`<li>`**: Define un elemento de la lista.
   - **`<a>`**: Define un enlace que lleva al usuario a otra parte del documento o sitio web. El atributo `href` indica a dónde va el enlace.

## Paso 3: Creación de Secciones Adicionales
### Sección de Inicio
1. **Agrega una sección de inicio** después del `header` usando la etiqueta `<section>`:
   ```html
   <section id="inicio">
     <h1>Bienvenido a Mi Primera Página Web</h1>
     <p>Aquí podrás aprender sobre mí y lo que ofrezco.</p>
     <img src="imagen.jpg" alt="Imagen de bienvenida">
   </section>
   ```
   - **`<section>`**: Se usa para dividir el contenido en secciones diferentes.
   - **`id="inicio"`**: Define un identificador único que nos permitirá enlazar esta sección desde el menú de navegación.
   - **`<h1>`**: Encabezado principal de la sección.
   - **`<p>`**: Un párrafo de texto.
   - **`<img>`**: Muestra una imagen. El atributo `src` indica el archivo de la imagen, y `alt` describe la imagen para quienes no puedan verla.

### Sobre Mí
1. **Agrega otra sección** con información sobre ti:
   ```html
   <section id="sobre-mi">
     <h2>Sobre Mí</h2>
     <p>Soy un desarrollador web en formación.</p>
     <ul>
       <li>Me gusta el desarrollo web.</li>
       <li>Aprendo HTML, CSS y JavaScript.</li>
     </ul>
   </section>
   ```
   - **`<h2>`**: Este encabezado es un subnivel del `h1` anterior, usado para marcar una nueva sección importante.
   - **`<ul>`**: Lista no ordenada para destacar puntos clave.

## Paso 4: Creación del Footer
1. **Agrega un pie de página** (footer) al final del `body`:
   ```html
   <footer>
     <p>&copy; 2024 Mi Primera Página Web. Todos los derechos reservados.</p>
   </footer>
   ```
   - **`<footer>`**: Contiene información de pie de página, como derechos de autor.

## Paso 5: Crear un Archivo CSS para Estilos
1. **Crea un archivo llamado `styles.css`** en la misma carpeta del proyecto.
2. **Vincula el CSS** a tu archivo HTML:
   ```html
   <head>
     <link rel="stylesheet" href="styles.css">
   </head>
   ```
   - **`<link rel="stylesheet" href="styles.css">`**: Vincula el archivo CSS para que los estilos se apliquen al documento HTML.

## Paso 6: Agregar Estilos con CSS
Ahora que tienes el archivo CSS, vamos a agregar algunos estilos para mejorar la apariencia.

### Estilos Globales
1. **Aplica un estilo básico al `body`**:
   ```css
   body {
     font-family: Arial, sans-serif;
     background-color: #f0f0f0;
     color: #333;
     margin: 0;
     padding: 0;
   }
   ```
   - **`font-family`**: Define la fuente que se usará en el texto.
   - **`background-color`**: Cambia el color de fondo de la página.
   - **`color`**: Define el color del texto.
   - **`margin` y `padding`**: Eliminan los espacios predeterminados del navegador.

### Estilo del Header y Navegación
1. **Aplica estilo al `header` y al menú de navegación**:
   ```css
   header {
     background-color: #333;
     padding: 1em;
     text-align: center;
   }

   nav ul {
     list-style: none;
     padding: 0;
     margin: 0;
   }

   nav ul li {
     display: inline;
     margin-right: 15px;
   }

   nav ul li a {
     color: white;
     text-decoration: none;
   }

   nav ul li a:hover {
     text-decoration: underline;
   }
   ```
   - **`background-color`**: Cambia el color de fondo del header a gris oscuro.
   - **`list-style: none;`**: Elimina los puntos de la lista.
   - **`display: inline;`**: Hace que los elementos de la lista se alineen horizontalmente.
   - **`color: white;`**: Cambia el color del texto del menú a blanco.
   - **`text-decoration: underline;`**: Subraya los enlaces cuando pasas el ratón sobre ellos.

### Estilo de Secciones
1. **Estiliza las secciones de la página**:
   ```css
   section {
     margin: 20px auto;
     padding: 20px;
     max-width: 800px;
     background-color: white;
     border-radius: 8px;
     box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
   }
   ```
   - **`max-width`**: Limita el ancho máximo de la sección.
   - **`border-radius`**: Redondea las esquinas de la sección.
   - **`box-shadow`**: Agrega una sombra para dar profundidad.

### Estilo del Footer
1. **Dale estilo al footer**:
   ```css
   footer {
     background-color: #333;
     color: white;
     text-align: center;
     padding: 10px;
   }
   ```
   - **`text-align: center;`**: Centra el texto del footer.
   - **`padding`**: Agrega un espacio alrededor del texto.

## Resultado Final
Al seguir estos pasos, deberías tener una página web básica pero bien estructurada con una cabecera de navegación, una sección de inicio, una sección sobre ti, y un pie de página con información de derechos de autor.

¿Necesitas más ayuda o quieres hacerla más avanzada? Estoy aquí para ayudar a que continúes aprendiendo y mejorando tus habilidades de desarrollo web.
