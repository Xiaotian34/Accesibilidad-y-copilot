Version ESPAÑOL

Este proyecto demuestra el proceso de mejora de un código mal estructurado mediante el uso de inteligencia artificial, en este caso Copilot, para refactorizar y optimizar el código paso a paso.

1. Código Inicial (Mal Hecho)

A continuación, se presenta el código original, que contiene malas prácticas, como poca accesibilidad y un mal contraste para la accesibilidad.

![alt text](image-1.png)
![alt text](image-2.png)

Previsualización de la página:

![alt text](image-6.png)

Problemas Detectados

    Contraste de colores:

        El fondo y el texto tienen el mismo color (#000), lo que hace que el texto sea ilegible.

    Imágenes sin texto alternativo:

        Las imágenes en la galería no tienen atributos alt descriptivos, lo que afecta la accesibilidad.
        Ineficiencia en el script:

    El script en la parte inferior del documento tiene un bucle que se ejecuta 100,000 veces, lo que puede afectar el rendimiento.

    Falta de etiquetas de cierre:

    El documento HTML no tiene una etiqueta de cierre </html>.

    Uso de atributos obsoletos:

        El atributo border en la etiqueta <table> está obsoleto. Es mejor usar CSS para el estilo.

    Falta de etiquetas de formulario accesibles:

        Los elementos del formulario no tienen etiquetas label adecuadas para mejorar la accesibilidad.

    Falta de atributos lang en las etiquetas html:

        La etiqueta <html> tiene el atributo lang="es", lo cual es correcto, pero es importante asegurarse de que esté presente en todas las páginas.

    Falta de manejo de errores en el formulario:

        No hay validación ni manejo de errores en el formulario.

    Falta de descripción en los botones:

        Los botones no tienen descripciones claras sobre su funcionalidad.

    Falta de estructura semántica:

        El uso de múltiples etiquetas <h1> puede ser confuso para los lectores de pantalla. Es mejor usar una estructura jerárquica adecuada con <h1>, <h2>, etc.

Resultado de las herramientas de validacion de accesibilidad:

Lighthouse:
![alt text](image.png)
![alt text](image-3.png)

Wave:
![alt text](image-4.png)

Axe DevTools:
![alt text](image-5.png)

2. Uso de IA para Mejorar el Código

Se introdujo el siguiente prompt en Copilot para solicitar mejoras en el código:

Objetivo: 
Hacer que la pagina cumpla con las normativas A, AA y AAA de WCAG 2.2, hacerla accesible, legible, que mantenga un buen, rendimiento, que sea fluida, y que tenga varias practicas recomendadas.

Requisitos: 
Que la página sea accesible y tenga un buen rendimiento. 
Que tenga un buen contraste (añadir un estilo para los elementos de la pagina). 
Añade atributos aria para las descripciones. 
Añade textos alternativos para las imagenes. 
Añade y elimina todas las etiquetas necesarias. 
Evita el uso de atributos obsoletos. 
Añade los metas necesarios. 
Asegurate de que los encabezados estan jerarquizados. 
Verifica que los formularios sean accesibles. 
Añade control de errores en el formulario. 
Añade estructuras semánticas. 
Hazlo todo en este html. 
Elimina todos los elementos innecesarios. 
Los marcos deben tener atributo title. 
Todo el contenido de la pagina debe estar incluido en puntos de referencia. 
Usa un tamaño adecuado para las imagenes.


3. Código Optimizado

El resultado final tras aplicar las sugerencias de la IA:

![alt text](image-7.png)
![alt text](image-8.png)
![alt text](image-9.png)
![alt text](image-10.png)

Previsualización de la página:
![alt text](image-11.png)
![alt text](image-12.png)

Resultado de las herramientas de validacion de accesibilidad:

Lighthouse:
![alt text](image-15.png)

Wave:
![alt text](image-13.png)

Axe DevTools:
![alt text](image-14.png)


Mejoras Aplicadas

Meta tags: Añadidos keywords y author.
Contraste: Asegurado buen contraste en los botones.
Atributos ARIA: Añadidos aria-label, aria-labelledby, aria-describedby, y aria-live.
Textos alternativos: Añadidos alt a las imágenes.
Jerarquía de encabezados: Verificada y corregida.
Formularios accesibles: Añadido control de errores y mensajes de error accesibles.
Estructuras semánticas: Verificadas y corregidas.
Tamaño de imágenes: Asegurado que las imágenes no excedan el tamaño del contenedor.


4. Conclusión

Este experimento demuestra cómo una IA puede ayudar a mejorar la calidad del código al detectar problemas y sugerir buenas prácticas. Integrar herramientas como Copilot en el desarrollo puede acelerar la refactorización y optimización del código.

Y además concluimos que un ejemplo de un prompt perfecto sería la ya mencionada:

Objetivo: 
Hacer que la pagina cumpla con las normativas A, AA y AAA de WCAG 2.2, hacerla accesible, legible, que mantenga un buen, rendimiento, que sea fluida, y que tenga varias practicas recomendadas.

Requisitos: 
Que la página sea accesible y tenga un buen rendimiento. 
Que tenga un buen contraste (añadir un estilo para los elementos de la pagina). 
Añade atributos aria para las descripciones. 
Añade textos alternativos para las imagenes. 
Añade y elimina todas las etiquetas necesarias. 
Evita el uso de atributos obsoletos. 
Añade los metas necesarios. 
Asegurate de que los encabezados estan jerarquizados. 
Verifica que los formularios sean accesibles. 
Añade control de errores en el formulario. 
Añade estructuras semánticas. 
Hazlo todo en este html. 
Elimina todos los elementos innecesarios. 
Los marcos deben tener atributo title. 
Todo el contenido de la pagina debe estar incluido en puntos de referencia. 
Usa un tamaño adecuado para las imagenes.
