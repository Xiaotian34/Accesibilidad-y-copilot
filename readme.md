# Proyecto de Mejora de Accesibilidad Web con IA

Este proyecto demuestra el proceso de mejora de un código HTML mal estructurado, mediante el uso de inteligencia artificial (en este caso, GitHub Copilot), para refactorizar y optimizar el código paso a paso, de modo que cumpla con los estándares de accesibilidad establecidos por la normativa WCAG 2.2.

## 1. Código Inicial (Mal Hecho)

A continuación se presenta el código original, que contiene malas prácticas que afectan la accesibilidad, como:

- Contraste de colores inapropiado
- Imágenes sin textos alternativos descriptivos
- Formularios sin etiquetas `label` adecuadas
- Mal uso de etiquetas HTML (por ejemplo, múltiples etiquetas `<h1>`)
- Uso de atributos obsoletos
- Ineficiencia en los scripts
- Falta de estructura semántica

### Previsualización de la página

![Previsualización de la página](ErrorPreview.png)

### Problemas Detectados

1. **Contraste de colores**: El fondo y el texto tienen el mismo color (`#000`), lo que hace que el texto sea ilegible.
2. **Imágenes sin texto alternativo**: Las imágenes en la galería no tienen atributos `alt` descriptivos.
3. **Ineficiencia en el script**: El script tiene un bucle que se ejecuta 100,000 veces, lo que afecta el rendimiento.
4. **Falta de etiquetas de cierre**: El documento HTML no tiene una etiqueta de cierre `</html>`.
5. **Uso de atributos obsoletos**: El atributo `border` en la etiqueta `<table>` está obsoleto; es mejor usar CSS para el estilo.
6. **Falta de etiquetas de formulario accesibles**: Los elementos del formulario no tienen etiquetas `label` adecuadas para mejorar la accesibilidad.
7. **Falta de atributo `lang` en las etiquetas `<html>`**: La etiqueta `<html>` tiene el atributo `lang="es"`, pero es importante asegurarse de que esté presente en todas las páginas.
8. **Falta de manejo de errores en el formulario**: No hay validación ni manejo de errores en el formulario.
9. **Falta de descripción en los botones**: Los botones no tienen descripciones claras sobre su funcionalidad.
10. **Falta de estructura semántica**: El uso de múltiples etiquetas `<h1>` puede ser confuso para los lectores de pantalla. Es mejor usar una estructura jerárquica adecuada con `<h1>`, `<h2>`, etc.

### Resultado de las herramientas de validación de accesibilidad

- **Wave**:
    ![Wave](errorPag.png)

---

## 2. Uso de IA para Mejorar el Código

Para mejorar la accesibilidad del código, se introdujo el siguiente **prompt** en GitHub Copilot:

### Prompt:

"Por favor, modifica el siguiente código HTML para cumplir con las normativas WCAG 2.2 (niveles A, AA y AAA), asegurando que la página sea accesible, legible, tenga buen rendimiento y sea fluida. Los cambios que deben aplicarse son los siguientes:

1. **Contraste adecuado**: Asegúrate de que todos los elementos tengan un buen contraste, siguiendo las pautas de accesibilidad para texto y elementos visuales.
2. **Atributos ARIA**: Añade los atributos ARIA adecuados para describir los elementos interactivos y los cambios de contenido.
3. **Textos alternativos en imágenes**: Añade textos alternativos apropiados para todas las imágenes.
4. **Etiquetas semánticas**: Revisa y añade las etiquetas necesarias, asegurándote de que los encabezados estén jerarquizados correctamente (por ejemplo, h1, h2, h3) y que se sigan buenas prácticas de accesibilidad semántica.
5. **Eliminación de atributos obsoletos**: Elimina todos los atributos obsoletos y utiliza los más modernos y accesibles.
6. **Metas necesarios**: Asegúrate de que se incluyan las etiquetas meta necesarias como charset, viewport, descripción, etc.
7. **Formulario accesible**: Verifica que los formularios sean completamente accesibles, incluyendo etiquetas para los campos, mensajes de error y validaciones.
8. **Estructuras semánticas**: Usa las etiquetas semánticas correctas (por ejemplo, `<header>`, `<main>`, `<footer>`, `<article>`, `<section>`, etc.) para organizar el contenido de manera clara.
9. **Eliminación de elementos innecesarios**: Elimina cualquier código o elemento que no sea necesario para la accesibilidad y el rendimiento.
10. **Atributo title en los marcos**: Si hay marcos o iframes, asegúrate de incluir un atributo `title` que describa su contenido.
11. **Puntos de referencia**: Todo el contenido debe estar dentro de puntos de referencia claros (por ejemplo, un `<nav>`, `<main>`, `<section>`, etc.).
12. **Tamaño adecuado para las imágenes**: Asegúrate de que las imágenes tengan un tamaño adecuado y no sean demasiado grandes, para mejorar el rendimiento."

### Requisitos:

- La página debe ser accesible y tener un buen rendimiento.
- Debe tener un buen contraste (añadir un estilo para los elementos de la página).
- Añadir atributos ARIA para las descripciones.
- Añadir textos alternativos para las imágenes.
- Añadir y eliminar todas las etiquetas necesarias.
- Evitar el uso de atributos obsoletos.
- Añadir los metadatos necesarios.
- Asegurarse de que los encabezados estén jerarquizados.
- Verificar que los formularios sean accesibles.
- Añadir control de errores en el formulario.
- Añadir estructuras semánticas.
- Eliminar todos los elementos innecesarios.
- Los marcos deben tener atributo `title`.
- Todo el contenido de la página debe estar incluido en puntos de referencia.
- Usar un tamaño adecuado para las imágenes.

---

## 3. Código Optimizado

El resultado final tras aplicar las sugerencias de la IA, mediante el prompt proporcionado, se muestra a continuación:

### Previsualización de la página

![Previsualización optimizada](CorreccionPreview.png)

### Resultado de las herramientas de validación de accesibilidad:

- **Wave**:
    ![Wave](image-13.png)

---

## 4. Mejoras Aplicadas

- **Meta tags**: Añadidos `keywords` y `author`.
- **Contraste**: Asegurado un buen contraste en los botones.
- **Atributos ARIA**: Añadidos `aria-label`, `aria-labelledby`, `aria-describedby` y `aria-live`.
- **Textos alternativos**: Añadidos `alt` a las imágenes.
- **Jerarquía de encabezados**: Verificada y corregida.
- **Formularios accesibles**: Añadido control de errores y mensajes de error accesibles.
- **Estructuras semánticas**: Verificadas y corregidas.
- **Tamaño de imágenes**: Asegurado que las imágenes no excedan el tamaño del contenedor.

---

## 5. Conclusión

Este experimento demuestra cómo una IA puede ayudar a mejorar la calidad del código al detectar problemas y sugerir buenas prácticas. Integrar herramientas como Copilot en el desarrollo puede acelerar la refactorización y optimización del código, mejorando la accesibilidad y el rendimiento.

---

## 6. Enlace al Repositorio

[GitHub Repository](enlace-al-repositorio)

---

# Web Accessibility Improvement with AI

This project demonstrates the process of improving a poorly structured HTML code using artificial intelligence (in this case, GitHub Copilot) to refactor and optimize the code step by step, making it comply with the accessibility standards set by WCAG 2.2 guidelines.

## 1. Initial Code (Poorly Structured)

The following shows the original code containing bad practices affecting accessibility, such as:

- Poor contrast
- Images without descriptive alt texts
- Forms lacking proper `label` tags
- Improper use of HTML tags (e.g., multiple `<h1>` tags)
- Use of deprecated attributes
- Inefficient scripts
- Lack of semantic structure

### Page Preview

![Page preview](ErrorPreview.png)

### Detected Issues

1. **Color Contrast**: The background and text have the same color (`#000`), making the text unreadable.
2. **Images without alt text**: The images in the gallery are missing descriptive `alt` attributes.
3. **Inefficient script**: The script has a loop that runs 100,000 times, affecting performance.
4. **Missing closing tags**: The HTML document is missing a closing `</html>` tag.
5. **Deprecated attributes**: The `border` attribute in the `<table>` tag is outdated; using CSS for styling is recommended.
6. **Missing accessible form tags**: The form elements lack appropriate `label` tags for better accessibility.
7. **Missing `lang` attribute**: The `<html>` tag has the `lang="es"` attribute, but it is important to ensure this is on all pages.
8. **Lack of error handling in the form**: No validation or error handling is present.
9. **Button descriptions missing**: Buttons don't have clear descriptions of their functionality.
10. **Lack of semantic structure**: Using multiple `<h1>` tags can confuse screen readers. Proper hierarchical use of `<h1>`, `<h2>`, etc., is recommended.

### Accessibility Validation Results

- **Wave**:
    ![Wave](errorPag.png)

---

## 2. Using AI to Improve the Code

To improve the accessibility of the code, the following **prompt** was introduced in GitHub Copilot:

### Prompt:

"Please modify the following HTML code to comply with WCAG 2.2 standards (levels A, AA, and AAA), ensuring that the page is accessible, readable, performs well, and is smooth. The changes to be applied are as follows:

1. **Adequate contrast**: Ensure that all elements have good contrast, following the accessibility guidelines for text and visual elements.
2. **ARIA attributes**: Add the appropriate ARIA attributes to describe interactive elements and content changes.
3. **Alt text for images**: Add appropriate alt text for all images.
4. **Semantic tags**: Review and add the necessary tags, ensuring that headings are properly hierarchized (e.g., h1, h2, h3) and that best practices for semantic accessibility are followed.
5. **Removal of obsolete attributes**: Remove all obsolete attributes and use the most modern and accessible ones.
6. **Required meta tags**: Ensure that the necessary meta tags such as charset, viewport, description, etc., are included.
7. **Accessible forms**: Verify that forms are fully accessible, including labels for fields, error messages, and validations.
8. **Semantic structures**: Use the correct semantic tags (e.g., <header>, <main>, <footer>, <article>, <section>, etc.) to organize the content clearly.
9. **Removal of unnecessary elements**: Remove any code or elements that are unnecessary for accessibility and performance.
10. **Title attribute in frames**: If there are frames or iframes, ensure that a title attribute describing its content is included.
11. **Landmarks**: All content should be within clear landmarks (e.g., <nav>, <main>, <section>, etc.).
12. **Proper image size**: Ensure that images have an appropriate size and are not too large to improve performance."

### Requirements:

- The page must be accessible and perform well.
- It must have proper contrast (apply styles for page elements).
- Add ARIA attributes for descriptions.
- Add alt texts for images.
- Add and remove all necessary tags.
- Avoid the use of deprecated attributes.
- Add necessary meta tags.
- Ensure headers are properly structured.
- Verify forms are accessible.
- Add error handling to forms.
- Add semantic structures.
- Remove unnecessary elements.
- Frames should have a `title` attribute.
- Ensure all content is contained within landmarks.
- Use an appropriate image size.

---

## 3. Optimized Code

The final result after applying AI suggestions via the provided prompt is shown below:

### Page Preview

![Optimized preview](CorreccionPreview.png)

### Accessibility Validation Results:

- **Wave**:
    ![Wave](image-13.png)

---

## 4. Applied Improvements

- **Meta tags**: Added `keywords` and `author`.
- **Contrast**: Ensured good contrast in buttons.
- **ARIA attributes**: Added `aria-label`, `aria-labelledby`, `aria-describedby`, and `aria-live`.
- **Alt texts**: Added `alt` to images.
- **Header Hierarchy**: Verified and corrected.
- **Accessible Forms**: Added error control and accessible error messages.
- **Semantic Structures**: Verified and corrected.
- **Image Sizes**: Ensured images do not exceed container size.

---

## 5. Conclusion

This experiment demonstrates how AI can help improve code quality by detecting issues and suggesting best practices. Integrating tools like Copilot in development can speed up code refactoring and optimization, improving accessibility and performance.

---

## 6. GitHub Repository Link

[GitHub Repository](repository-link)
