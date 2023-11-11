# Modulo_HTML_CSS_Responsive

## HTML y su función en el desarrollo web
   - **HTML** (Lenguaje de Marcado de Hipertexto) es el código utilizado para estructurar y desplegar páginas web y sus contenidos. Define la **estructura** de tu contenido, como párrafos, listas, imágenes y tablas. No es un lenguaje de programación, sino un lenguaje de marcado que encierra partes del contenido para darles formato o comportamiento específico. Por ejemplo:
     
     ```html
     <p>Mi gato es muy gruñón</p>
     ```
   - Anatomía de un elemento HTML:
     - Etiqueta de inicio: `<p>` (marca el inicio del párrafo).
     - Etiqueta de cierre: `</p>` (marca el final del párrafo).
     - Contenido: texto dentro del elemento.

### ¿Cuál es la estructura básica de un documento HTML?
   - Un documento HTML tiene tres partes principales:
     - **DOCTYPE**: Especifica el tipo de documento (por ejemplo, `<!DOCTYPE html>` para HTML5).
     - **Etiqueta `<html>`**: Contiene la cabecera y el cuerpo del documento.
     - **Etiqueta `<head>`**: Contiene metadatos (como el título de la página).
     - **Etiqueta `<body>`**: Contiene el contenido visible de la página.

## CSS y su función en el desarrollo web?
   - **CSS** (Hojas de Estilo en Cascada) permite dar estilo y posicionar visualmente los elementos HTML. Se utiliza para cambiar fuentes, colores, tamaños y espaciado, crear diseños y efectos de animación. es buena práctica tener un documento CSS por separado para aplicar los estilos, ¿Porqué esto? Separar la presentación (CSS) de la estructura (HTML) mejora la legibilidad y mantenibilidad del código

### **Selectores CSS y Especificidad:**
- **Selectores CSS**: Los selectores son patrones utilizados para seleccionar elementos HTML a los que se les aplicarán estilos. Algunos tipos comunes de selectores son:
    - **Selector de Clase**: Selecciona elementos por su clase (`.mi-clase`).
    - **Selector de ID**: Selecciona un elemento por su ID (`#mi-id`).
    - **Selector de Elemento**: Selecciona elementos por su tipo (por ejemplo, `p`, `h1`, `div`).
      
- **Especificidad**: Es importante entender la especificidad para resolver conflictos de estilos. Cada selector tiene un peso específico que determina cuál regla CSS se aplicará. La especificidad se calcula en base a tres categorías: ID, Clase y Tipo. Por ejemplo:
    - `#mi-id` tiene mayor especificidad que `.mi-clase`.
    - `h1` tiene menor especificidad que `.mi-clase`.

### 2. **Estilos en Línea, Internos y Externos:**
- **Estilos en Línea (Inline)**:
    - Se aplican directamente a un elemento usando el atributo `style`. Es recomendado para situaciones muy específicas
    - Ejemplo: `<p style="color: red;">Texto rojo</p>`.
    - **Recomendación**: Evita los estilos en línea, ya que dificultan el mantenimiento y la reutilización.
      
- **Estilos Internos (Embedded)**:
    - Se definen en la sección `<style>` dentro del `<head>` del documento HTML.
    - Aplican a todo el documento.
    - Ejemplo:
        ```html
        <style>
            p {
                font-size: 16px;
            }
        </style>
        ```
- **Estilos Externos (External)**:
    - Se almacenan en archivos CSS separados.
    - Se vinculan al documento HTML usando la etiqueta `<link>` o `<style>` en el `<head>`.
    - **Recomendación**: Es la mejor práctica para proyectos grandes y mantenibles.

### Flexbox:
- **Flexbox** es la bendición de muchos programadores de Front-end jeje, es un sistema de diseño en CSS que permite crear diseños flexibles y responsivos. Se utiliza para organizar elementos en una fila o columna, distribuyendo el espacio disponible de manera eficiente.
- Ejemplo de uso:
    ```css
    .container {
        display: flex;
        justify-content: center; /* Centra horizontalmente */
        align-items: center; /* Centra verticalmente */
    }
    ```
- **Ventajas**:
    - Simplifica la alineación y distribución de elementos.
    - Permite crear diseños complejos con menos código.
¡Por supuesto! Vamos a explorar más sobre Flexbox, CSS Grid Layout y diseño responsivo:

### Propiedades y Funciones**
- Aquí pondré algunas propiedades clave:
    - `display: flex;`: Convierte un contenedor en un contenedor flexible.
    - `flex-direction`: Define la dirección principal (fila o columna).
    - `justify-content`: Alinea los elementos a lo largo del eje principal.
    - `align-items`: Alinea los elementos a lo largo del eje secundario.
    - `flex-grow`, `flex-shrink`, `flex-basis`: Controlan el crecimiento, encogimiento y tamaño inicial de los elementos.

## **CSS Grid Layout vs. Flexbox**
- **CSS Grid Layout** es un sistema bidimensional que crea cuadrículas de filas y columnas. A diferencia de Flexbox:
    - Grid es ideal para diseños más complejos y estructuras de cuadrícula.
    - Flexbox es mejor para alinear y distribuir elementos en una sola dimensión (fila o columna).

### **Ejemplo de Cuadrícula con CSS Grid:**
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <style>
        .grid-container {
            display: grid;
            grid-template-columns: repeat(3, 1fr); /* 3 columnas iguales */
            gap: 10px; /* Espacio entre celdas */
        }
        .item {
            background-color: #f0f0f0;
            padding: 10px;
            text-align: center;
        }
    </style>
</head>
<body>
    <div class="grid-container">
        <div class="item">1</div>
        <div class="item">2</div>
        <div class="item">3</div>
    </div>
</body>
</html>
```

## **Diseño Responsivo:**
- El dolor de cabeza de muchos pero que te llevará los diseños de las páginas a otro nivel, y es que el **Diseño Responsivo** se refiere a crear sitios web que se adapten a diferentes dispositivos y tamaños de pantalla, la idea es que el contenido debe reorganizarse y redimensionarse automáticamente.
- Se logra mediante:
    - **Media Queries**: Cambian estilos según el ancho de la pantalla.
    - **Unidades Relativas**: Usar `%`, `em`, `rem` en lugar de valores fijos.
    - **Viewport Units**: `vw`, `vh`, `vmin`, `vmax` para dimensiones relativas al viewport.

### **Técnicas para Diseño Responsivo:**
Unos trucos que aprendí sobre la marcha y que me a ayudado en muchos diseños
1. **Flexibilidad de Imágenes**: Usa `max-width: 100%;` para que las imágenes no se desborden en pantallas pequeñas.
2. **Reorganización de Elementos**: Cambia el orden de los elementos usando Flexbox o Grid.
3. **Breakpoints**: Define puntos de quiebre con Media Queries para ajustar estilos según el tamaño de la pantalla.


