# Sorpresa de Cumpleaños Interactiva

Este proyecto es una tarjeta de cumpleaños interactiva con una estética minimalista en tonos rosas pastel. Lo más destacado de este ejercicio académico es que logra interactividad (esconder y revelar contenido) usando **únicamente HTML5 y CSS3**.

## Cómo ejecutar el proyecto

1. Descarga los archivos `index.html` y `styles.css` en una misma carpeta.
2. Abre el archivo `index.html` en cualquier navegador moderno (Chrome, Firefox, Edge, Safari).
3. Escribe la palabra secreta **sorpresa** en el campo de texto para ver la carta.

## El "Truco" Técnico: Interactividad sin JS

Para lograr que la carta aparezca al escribir el código correcto, he utilizado dos potentes funciones nativas de la web:

1.  **Atributo `pattern` (HTML):** En el `<input>`, usamos una expresión regular sencilla (`pattern="sorpresa"`) que marca el campo como "inválido" hasta que el texto coincida exactamente con esa palabra.
2.  **Pseudoclase `:valid` (CSS):** Detectamos desde el CSS cuando el usuario ha cumplido el requisito del `pattern`.
3.  **Selector de hermano general `~` (CSS):** Al activarse `:valid`, enviamos una instrucción al elemento que viene después (la carta) para que cambie su opacidad de `0` a `1` y su altura de `0` a un tamaño visible.

## Personalización Visual

Los estilos principales están gestionados mediante **Variables CSS** en la sección `:root` del archivo `styles.css`. Puedes cambiar los colores fácilmente modificando estos valores:

- `--bg`: Color del fondo general (el lienzo).
- `--card`: Color de la tarjeta contenedora blanca.
- `--card-interior`: Color del papel de la carta.
- `--accent`: Color de los botones y detalles destacados.
- `--text`: Color para la lectura de los párrafos.

## Cómo cambiar el código secreto

Si quieres cambiar la palabra clave "sorpresa" por otra (ej. el nombre de la persona), solo debes:

1. Abrir `index.html`.
2. Buscar la línea del `<input>` y cambiar el atributo `pattern="tupalabra"`.
3. ¡Listo! El CSS reconocerá la nueva clave automáticamente.

---
