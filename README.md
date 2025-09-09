Visualizador de Datos Geo-editores de Wikimedia
Una aplicación web interactiva y de una sola página (SPA) construida con Vue.js para cargar, visualizar, filtrar y analizar los datos públicos del directorio de análisis de geo-editores de Wikimedia.

Descripción del Proyecto
Este visualizador es una herramienta diseñada para facilitar el análisis de los datos mensuales sobre los editores de los proyectos Wikimedia, clasificados por ubicación geográfica. La aplicación carga dinámicamente todos los archivos de datos disponibles desde la fuente oficial, los procesa y los presenta en una interfaz limpia e intuitiva, permitiendo al usuario explorar la información a través de filtros y múltiples gráficos interactivos.

Características Principales
Carga Dinámica de Datos: Se conecta en tiempo real al directorio de Wikimedia Analytics para obtener siempre la lista más actualizada de archivos de datos.

Interfaz Reactiva con Vue.js: Construida con Vue.js 3 y la Composition API, la interfaz se actualiza automáticamente en respuesta a las acciones del usuario y los cambios en los datos.

Panel de Filtros Avanzado: Permite filtrar los datos por Año, archivo de origen, proyecto (wiki) y país. Los filtros de selección múltiple facilitan análisis complejos y cruzados.

Visualización Dual de Datos:

Gráfico de Líneas (Tendencias Temporales): Un gráfico de líneas que muestra la evolución mensual de los editores por nivel de actividad. Es ideal para identificar patrones, estacionalidad y tendencias a lo largo del tiempo.

Gráfico de Barras (Resumen Agregado): Un gráfico de barras que resume el número total de editores por nivel de actividad para el período de tiempo seleccionado, ofreciendo una vista general del volumen total.

Tabla de Resultados Paginada: Muestra los datos filtrados en una tabla limpia y fácil de leer, con paginación para manejar grandes volúmenes de información de manera eficiente.

Exportación a CSV: Permite exportar la selección de datos filtrados a un archivo .csv para su uso en otras herramientas de análisis como Excel o Google Sheets.

Diseño Moderno y Responsivo: La interfaz está diseñada con Tailwind CSS para ser profesional, limpia y completamente funcional en diferentes tamaños de pantalla, desde móviles hasta computadoras de escritorio.

Tecnologías Utilizadas
Este proyecto es una aplicación de una sola página que no requiere un proceso de compilación (build). Todas las librerías se cargan a través de una CDN para simplificar su despliegue.

Lenguaje Principal: JavaScript (ES6+)

Framework de Frontend: Vue.js 3 (cargado a través de CDN), utilizando la API de Composición.

Librería de Estilos: Tailwind CSS (cargado a través de CDN).

Librería de Gráficos: Chart.js con chartjs-plugin-datalabels.

Librería de Iconos: Font Awesome.

APIs y Conexiones Externas
API de Datos de Wikimedia Analytics:

Endpoint: https://analytics.wikimedia.org/published/datasets/geoeditors_monthly/

Descripción: La aplicación realiza una petición fetch a esta URL para obtener el listado de todos los archivos de datos en formato .tsv. Posteriormente, realiza peticiones individuales para descargar cada uno de estos archivos.

Proxy CORS:

Servicio: corsproxy.io

Descripción: Para evitar problemas de políticas de CORS (Cross-Origin Resource Sharing), todas las peticiones fetch se enrutan a través de este proxy.

Instalación y Uso
Dado que es una aplicación autocontenida, no se requiere instalación ni dependencias complejas.

Descarga el archivo index.html.

Ábrelo en un navegador web moderno (como Chrome, Firefox, Edge, etc.).

¡Listo! La aplicación comenzará a funcionar.

Importante: Se requiere una conexión a internet activa para que la aplicación pueda conectarse a la API de Wikimedia y cargar los datos.

Estructura del Código
Todo el código de la aplicación (HTML, CSS y JavaScript) se encuentra dentro del archivo index.html.

<style>: Contiene las variables de CSS y estilos personalizados que complementan a Tailwind CSS.

<div id="app">: Es el punto de montaje de la aplicación Vue.js. Todo el HTML de la interfaz se encuentra aquí, estructurado con componentes de Vue.

<script type="module">: Contiene toda la lógica de la aplicación.

Instancia Principal de Vue: Creada con createApp, contiene el estado reactivo (ref, reactive), las propiedades computadas (computed) y los métodos principales.

Componentes de Vue: La aplicación se divide en componentes reutilizables para una mejor organización: stats-panel, filters-panel, editors-over-time-chart, activity-chart, y results-table.