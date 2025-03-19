# Fundamentos del Desarrollo Web: HTML, CSS y JavaScript explicados con este repo de teachable machine

## Descripción del Curso
Este curso de 90 minutos proporciona una introducción práctica a los pilares del desarrollo web moderno. Los participantes aprenderán los fundamentos de HTML para estructurar contenido, CSS para estilizar páginas web y JavaScript para añadir interactividad, culminando con la creación de un proyecto web básico que integra estas tres tecnologías.

## Prerrequisitos
- Conocimientos básicos de informática
- Editor de texto (como Visual Studio Code, Sublime Text o similar)
- Navegador web moderno

## Sección 1: Fundamentos de HTML (20 minutos)

### Contenido

En esta primera sección exploraremos HTML (HyperText Markup Language), el lenguaje fundamental para crear la estructura de cualquier página web. HTML no es un lenguaje de programación, sino un lenguaje de marcado que define la arquitectura y organización del contenido web.

Comenzaremos entendiendo la sintaxis básica de HTML, que se basa en elementos o etiquetas. Cada elemento HTML tiene una etiqueta de apertura como `<p>` y generalmente una de cierre como `</p>`, con contenido entre ambas. Esta estructura de etiquetas permite al navegador interpretar correctamente cómo debe mostrarse el contenido.

La anatomía básica de un documento HTML incluye:

```html
<!DOCTYPE html>
<html>
<head>
    <meta charset="UTF-8">
    <title>Título de la página</title>
</head>
<body>
    <!-- Aquí va el contenido visible -->
    <h1>Encabezado principal</h1>
    <p>Un párrafo de texto.</p>
</body>
</html>
```

Es esencial comprender que:
- La declaración `<!DOCTYPE html>` indica que estamos usando HTML5.
- El elemento `<html>` envuelve todo el contenido.
- El `<head>` contiene metadatos e información para el navegador.
- El `<body>` contiene todo lo que se muestra en la página.

Trabajaremos con las etiquetas semánticas más importantes:
- Encabezados (`<h1>` a `<h6>`) para jerarquizar el contenido.
- Párrafos (`<p>`) para agrupar texto.
- Listas ordenadas (`<ol>`) y desordenadas (`<ul>`) con sus elementos (`<li>`).
- Enlaces (`<a>`) para conectar con otros recursos usando el atributo `href`.
- Imágenes (`<img>`) con sus atributos `src` y `alt`.
- Contenedores genéricos como `<div>` y `<span>`.

También introduciremos etiquetas semánticas de HTML5 como `<header>`, `<nav>`, `<main>`, `<section>`, `<article>` y `<footer>`, que proporcionan significado a las diferentes partes de la página, mejorando la accesibilidad y el SEO.

### Actividad práctica
Crearemos la estructura HTML básica de una página de blog personal, incluyendo encabezado, navegación, secciones de contenido y pie de página, utilizando etiquetas semánticas adecuadas.

## Sección 2: Estilización con CSS (25 minutos)

### Contenido

CSS (Cascading Style Sheets) es el lenguaje que nos permite dar estilo y diseño a nuestras páginas web. Sin CSS, las páginas serían documentos de texto plano sin formato.

Exploraremos las tres formas de incorporar CSS en un documento HTML:
1. CSS en línea: usando el atributo `style` directamente en elementos HTML.
2. CSS interno: mediante la etiqueta `<style>` en el `<head>` del documento.
3. CSS externo: vinculando un archivo `.css` con la etiqueta `<link>`.

```html
<!-- CSS externo (método recomendado) -->
<link rel="stylesheet" href="estilos.css">
```

La sintaxis básica de CSS consiste en selectores, propiedades y valores:

```css
selector {
    propiedad: valor;
    otra-propiedad: otro-valor;
}
```

Analizaremos los distintos tipos de selectores:
- Selectores de elementos (`p`, `h1`, `div`)
- Selectores de clase (`.clase`)
- Selectores de ID (`#identificador`)
- Selectores descendientes (`div p`)
- Pseudo-clases (`:hover`, `:active`)

El modelo de caja (box model) es fundamental en CSS, determinando cómo se calcula el espacio que ocupa un elemento:
- Content (contenido): el texto o imagen dentro del elemento
- Padding (relleno): espacio entre el contenido y el borde
- Border (borde): línea alrededor del padding
- Margin (margen): espacio exterior al borde

Aprenderemos propiedades esenciales de CSS:
- Colores (`color`, `background-color`)
- Texto (`font-family`, `font-size`, `text-align`)
- Espaciado (`margin`, `padding`)
- Bordes (`border`, `border-radius`)
- Dimensiones (`width`, `height`)

Introduciremos conceptos más avanzados:
- Posicionamiento (`position: relative/absolute/fixed`)
- Visualización (`display: block/inline/flex`)
- Flexbox para layouts modernos y responsive
- Media queries para diseño adaptable a diferentes dispositivos

```css
@media (max-width: 768px) {
    /* Reglas específicas para pantallas pequeñas */
    body {
        font-size: 14px;
    }
}
```

### Actividad práctica
Aplicaremos estilos a la estructura HTML creada anteriormente, diseñando un layout responsivo utilizando flexbox, personalizando colores, tipografías y espaciado, e implementando una media query simple para adaptarse a dispositivos móviles.

## Sección 3: Programación con JavaScript (30 minutos)

### Contenido

JavaScript es el lenguaje de programación que da vida a las páginas web, permitiendo crear experiencias interactivas y dinámicas. A diferencia de HTML y CSS, JavaScript es un lenguaje de programación completo.

Para integrar JavaScript en una página HTML, usamos la etiqueta `<script>`:

```html
<!-- JavaScript interno -->
<script>
    // Código JavaScript aquí
</script>

<!-- JavaScript externo (recomendado) -->
<script src="script.js"></script>
```

Comenzaremos con los fundamentos del lenguaje:

**Variables y tipos de datos:**
```javascript
// Declaración de variables
let nombre = "María"; // String
const edad = 25;      // Number
var activo = true;    // Boolean

// Arrays
let colores = ["rojo", "verde", "azul"];

// Objetos
let persona = {
    nombre: "Juan",
    edad: 30,
    profesion: "desarrollador"
};
```

**Operadores y expresiones:**
```javascript
// Aritméticos: +, -, *, /, %
let suma = 5 + 3;

// Comparación: ==, ===, !=, !==, >, <, >=, <=
let esIgual = (5 === "5"); // false, compara valor y tipo

// Lógicos: &&, ||, !
let resultado = (edad > 18 && activo);
```

**Estructuras de control:**
```javascript
// Condicionales
if (edad >= 18) {
    console.log("Es mayor de edad");
} else {
    console.log("Es menor de edad");
}

// Bucles
for (let i = 0; i < colores.length; i++) {
    console.log(colores[i]);
}

// forEach (método moderno)
colores.forEach(color => {
    console.log(color);
});
```

**Funciones:**
```javascript
// Función declarativa
function saludar(nombre) {
    return "¡Hola, " + nombre + "!";
}

// Función de expresión
const despedir = function(nombre) {
    return "¡Adiós, " + nombre + "!";
};

// Función flecha (arrow function)
const multiplicar = (a, b) => a * b;
```

Exploraremos la interacción con el DOM (Document Object Model), que es la representación programática de nuestra página HTML:

```javascript
// Seleccionar elementos
const titulo = document.getElementById("titulo");
const parrafos = document.querySelectorAll("p");
const boton = document.querySelector(".btn-principal");

// Modificar contenido
titulo.textContent = "Nuevo título";
titulo.innerHTML = "Título con <em>énfasis</em>";

// Modificar estilos
titulo.style.color = "blue";
titulo.classList.add("destacado");

// Eventos
boton.addEventListener("click", function() {
    alert("¡Botón pulsado!");
});
```

También cubriremos conceptos fundamentales como:
- Ámbito (scope) de variables
- Métodos de arrays (map, filter, reduce)
- Promesas y manejo de asincronía básica
- Local Storage para almacenamiento en el navegador

```javascript
// Ejemplo de Local Storage
localStorage.setItem("usuario", "María");
const usuarioGuardado = localStorage.getItem("usuario");
```

### Actividad práctica
Añadiremos interactividad a nuestra página de blog, implementando un formulario de comentarios con validación, un botón para cambiar entre modo claro/oscuro, y una galería de imágenes simple con navegación. Utilizaremos manipulación del DOM y eventos para lograr estas funcionalidades.

## Sección 4: Integración y Proyecto Final (15 minutos)

### Contenido

En esta sección final, consolidaremos todo lo aprendido integrando HTML, CSS y JavaScript para crear una experiencia web completa y funcional. Entenderemos cómo estos tres pilares del desarrollo web trabajan juntos:

- HTML proporciona la estructura y el contenido
- CSS maneja la presentación y el diseño
- JavaScript añade comportamiento e interactividad

Analizaremos las mejores prácticas para organizar nuestros archivos en un proyecto web:

```
proyecto/
├── index.html        # Página principal
├── css/
│   └── style.css     # Estilos principales
├── js/
│   └── script.js     # JavaScript principal
├── img/              # Carpeta de imágenes
└── assets/           # Otros recursos
```

Exploraremos conceptos importantes en el desarrollo web moderno:

1. **Diseño responsive**: Asegurar que nuestra aplicación funcione bien en todos los dispositivos.

2. **Rendimiento web**: Optimización básica para mejorar la velocidad de carga:
   - Minificación de archivos
   - Optimización de imágenes
   - Carga eficiente de recursos

3. **Accesibilidad web**: Prácticas para hacer nuestro sitio accesible a todos los usuarios:
   - Etiquetas semánticas
   - Atributos ARIA
   - Contraste adecuado
   - Texto alternativo para imágenes

4. **Depuración y herramientas de desarrollo**:
   - Uso de la consola del navegador
   - Panel Elements/Inspector
   - Panel Network
   - Breakpoints para depurar JavaScript

### Actividad práctica
Finalizaremos el proyecto de blog personal, integrando todas las partes creadas anteriormente y añadiendo elementos adicionales como un menú de navegación responsivo y un formulario de contacto funcional. Revisaremos el proyecto completo para asegurar las mejores prácticas y el correcto funcionamiento en diferentes dispositivos.

## Conclusión (5 minutos)

En este curso intensivo, hemos explorado los fundamentos esenciales del desarrollo web front-end moderno: HTML para estructurar el contenido, CSS para estilizarlo y JavaScript para hacerlo interactivo.

Recapitulando los puntos clave:
- HTML es el esqueleto de cualquier sitio web, proporcionando estructura semántica.
- CSS permite crear experiencias visuales atractivas y adaptables a diferentes dispositivos.
- JavaScript añade dinamismo, permitiendo responder a las acciones del usuario.
- La integración de estas tres tecnologías es crucial para crear experiencias web completas.

Para continuar su aprendizaje, recomendamos:
- Explorar frameworks como Bootstrap para CSS o React/Vue para JavaScript
- Practicar creando proyectos personales como portafolios o aplicaciones web simples
- Participar en comunidades de desarrollo web como freeCodeCamp o MDN
- Profundizar en aspectos de desarrollo back-end para construir aplicaciones completas

Recuerden que el desarrollo web es un campo en constante evolución, por lo que el aprendizaje continuo es esencial para mantenerse actualizado con las últimas tendencias y mejores prácticas.
