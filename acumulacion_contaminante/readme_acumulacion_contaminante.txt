Acumulación de Contaminante en un Radio de 5 km
================================================

Este código simula visualmente la acumulación de un contaminante en un área circular de 5 km de radio desde un punto de derrame. Utiliza D3.js para crear una animación que expande visualmente la concentración del contaminante y calcula la acumulación en tiempo real.

Funcionalidades Principales
---------------------------

### Visualización de Acumulación de Contaminante
- Se genera un círculo que representa la zona de contaminación desde el punto de derrame. La acumulación se extiende gradualmente a medida que aumenta el radio, mostrando cómo la concentración del contaminante disminuye con la distancia.

### Cálculo de la Concentración
- La concentración en función de la distancia radial desde el punto de derrame se calcula mediante una fórmula de concentración inversamente proporcional a la distancia cuadrática:
concentracion(r) = C0 / (1 + r^2)
- Este valor se utiliza para calcular la cantidad acumulada de contaminante en cada "anillo" del área circular.

### Animación de Expansión de la Contaminación
- A través de `requestAnimationFrame`, la visualización de la acumulación se va actualizando en intervalos, aumentando el radio de expansión. Cada nueva "capa" de acumulación se colorea según la concentración, desde rojo (alta concentración) hasta verde (baja concentración).

### Escala de Concentración y Visualización del Total Acumulado
- La interfaz muestra una escala de colores (rojo, amarillo, verde) para ilustrar los niveles de concentración (100 mg/L a 0 mg/L).
- Se muestra en tiempo real el valor de la acumulación total en mg·km²/L, basado en el área cubierta hasta el momento.

### Interacción del Usuario y Tooltip
- Al mover el cursor sobre el área de contaminación, un tooltip muestra la concentración estimada en el punto debajo del cursor.
- El tooltip solo aparece cuando el cursor está dentro del área de 5 km de radio.

### Elementos Visuales Adicionales
- Un ícono de un "barco" indica el punto de derrame en el centro del área.
- Una leyenda en el borde del círculo indica la distancia de 5 km desde el punto de derrame.

Librerías Utilizadas
--------------------
- **D3.js**: Para manipulación y visualización de datos a través de SVG.

Estructura del Código
---------------------
- **HTML**: Define la estructura de la página, la interfaz de usuario y el pie de página con información adicional.
- **CSS**: Estilos para el fondo, el texto, el SVG y otros elementos visuales, incluyendo el tooltip y la escala de concentración.
- **JavaScript**: Contiene la lógica para calcular la concentración, gestionar la animación de expansión de acumulación y mostrar el tooltip interactivo.

Instrucciones para Visualización
--------------------------------
Este archivo HTML puede abrirse en cualquier navegador que soporte JavaScript. Solo es necesario conexión a Internet para cargar la biblioteca D3.js desde el enlace proporcionado.
