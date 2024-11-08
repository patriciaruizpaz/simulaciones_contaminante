Simulación de Derrame de Contaminante en un Río

Este proyecto simula la dispersión de un derrame de contaminante en un río, visualizando la concentración del contaminante en función de la distancia desde el punto de origen.

Funcionalidad Principal

1. Cálculo de la Concentración:
   - La concentración de contaminante se calcula utilizando la fórmula `concentracion(x, y)`, donde `x` y `y` son las coordenadas respecto al punto de origen.
   - La concentración en el centro es `C0 = 100 mg/L` y disminuye conforme aumenta la distancia, hasta un límite de 5 km.

2. Visualización de la Dispersión:
   - Se utilizan círculos concéntricos de colores para representar visualmente la dispersión del contaminante desde el punto de origen.
   - Cada círculo se colorea en función de la concentración, calculada mediante `colorConcentracion(concentracion)`. Los colores pasan de rojo a verde para indicar alta y baja concentración, respectivamente.
   - La visualización se actualiza en tiempo real para simular el crecimiento de la zona de contaminación.

3. Interactividad y Tooltip:
   - Al mover el cursor sobre la visualización, un tooltip muestra la concentración exacta de contaminante en la posición actual del cursor (dentro de 5 km del punto de origen).
   - La concentración es calculada dinámicamente según la posición del mouse.

4. Animación del Derrame:
   - La dispersión del contaminante está animada. La función `animarContaminante()` incrementa el radio del derrame progresivamente hasta alcanzar un radio máximo (200 px, equivalente a 5 km).
   - Se utiliza `requestAnimationFrame` para una animación fluida que actualiza el color y el tamaño de la zona contaminada en cada frame.

5. Indicadores de Ubicación:
   - Se añaden elementos de referencia visual como el ícono de una ciudad situada a 5 km del derrame y un barco en movimiento en el borde de la zona contaminada.

Estructura del Código

El código incluye las siguientes secciones clave:

- HTML y Estilos CSS:
  - Define el estilo visual y la estructura de los elementos principales de la página, incluyendo el fondo, la escala de concentración, el pie de página, y el tooltip.

- JavaScript con D3.js:
  - Define las funciones para el cálculo de concentración, la visualización y actualización de la dispersión del derrame, y la interactividad.
  - Utiliza la biblioteca D3.js para manipulación SVG y animación de los elementos de la simulación.

Requisitos

Para ejecutar este proyecto, es necesario:
- Una conexión a internet para cargar la biblioteca D3.js desde el CDN de D3.js.
- Un navegador moderno que soporte HTML5 y SVG para la animación y visualización de la dispersión.
