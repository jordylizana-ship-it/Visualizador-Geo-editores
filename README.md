Visualizador de Datos Geo-editores de Wikimedia (Full-Stack)
Una aplicación web interactiva con una arquitectura cliente-servidor para cargar, visualizar, filtrar y analizar los datos públicos del directorio de análisis de geo-editores de Wikimedia.

Descripción del Proyecto
Este visualizador es una herramienta diseñada para facilitar el análisis de los datos mensuales sobre los editores de los proyectos Wikimedia, clasificados por ubicación geográfica.

La aplicación utiliza un backend de Node.js para obtener los datos directamente desde la fuente oficial de Wikimedia Analytics, eliminando la necesidad de proxies externos y garantizando una conexión estable. El frontend, construido con Vue.js 3, consume estos datos y los presenta en una interfaz limpia e intuitiva, permitiendo al usuario explorar la información a través de filtros y múltiples gráficos interactivos.

Arquitectura del Proyecto
Backend (server.js): Un servidor Node.js con Express que actúa como un intermediario robusto. Se encarga de:

Comunicarse directamente con la API de Wikimedia Analytics.

Procesar la lista de archivos disponibles.

Servir los datos al frontend a través de una API REST local.

Frontend (public/index.html): Una Single-Page Application (SPA) construida con Vue.js 3 que se ejecuta en el navegador del usuario. Se encarga de toda la presentación, interactividad y visualización de datos.

Características Principales
Arquitectura Cliente-Servidor Robusta: Elimina problemas de CORS y dependencias de servicios de terceros.

Interfaz Reactiva con Vue.js: Construida con Vue.js 3 y la Composition API para una interfaz fluida y un estado bien gestionado.

Panel de Filtros Avanzado: Permite filtrar datos por Año, archivo, proyecto (wiki) y país, con componentes de selección múltiple con buscador.

Visualización Dual de Datos:

Gráfico de Líneas: Muestra la evolución mensual de los editores para identificar tendencias.

Gráfico de Barras: Resume el volumen total de editores por nivel de actividad.

Tabla de Resultados Paginada: Maneja grandes volúmenes de datos de manera eficiente.

Exportación a CSV: Permite exportar los datos filtrados para análisis externo.

Diseño Moderno y Responsivo: Creado con Tailwind CSS para una experiencia de usuario óptima en cualquier dispositivo.

Tecnologías Utilizadas
Backend
Entorno de Ejecución: Node.js

Framework: Express.js

Peticiones HTTP: Axios

Web Scraping: Cheerio (para parsear la lista de archivos del HTML de Wikimedia)

Frontend
Framework: Vue.js 3 (Composition API)

Estilos: Tailwind CSS

Gráficos: Chart.js con chartjs-plugin-datalabels

Iconos: Font Awesome

Instalación y Uso
Para ejecutar este proyecto en tu máquina local, sigue estos pasos:

Prerrequisitos
Tener instalado Node.js (que incluye el gestor de paquetes npm).

Pasos
Clona o descarga el repositorio en tu computadora.

Abre una terminal en la carpeta raíz del proyecto.

Instala las dependencias del servidor: Este comando leerá el archivo package.json e instalará Express, Axios, etc.

npm install

Inicia el servidor:

npm start

Si todo va bien, verás un mensaje en la consola: ¡Servidor listo! Abre tu navegador en http://localhost:3000.

Abre la aplicación: Abre tu navegador web y ve a la dirección http://localhost:3000.

Estructura del Código
/
├── public/               # Contiene todos los archivos del frontend
│   ├── index.html        # El HTML principal con la app de Vue
│   ├── logo.png          # Y otros assets (CSS, JS, imágenes)
│   └── ...
├── node_modules/         # Dependencias del backend (creado por npm)
├── package.json          # Define el proyecto y sus dependencias
├── package-lock.json     # Registro de versiones de las dependencias
└── server.js             # El corazón del backend (servidor Express y lógica de la API)

server.js: Define las rutas de la API (/api/files, /api/file/:filename) que el frontend utiliza para obtener los datos. También sirve los archivos estáticos de la carpeta public.

public/index.html: Contiene la aplicación Vue.js completa, dividida en componentes reutilizables (stats-panel, filters-panel, etc.) y toda la lógica de la interfaz de usuario.