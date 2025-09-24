# Visualizador de Geo-editores de Wikimedia

[![Estado](https://img.shields.io/badge/estado-activo-brightgreen)](https://geo-editores.toolforge.org/)
[![Licencia](https://img.shields.io/badge/licencia-MIT-blue)](LICENSE)

Un visualizador de datos interactivo para explorar y analizar la información mensual de editores geolocalizados de los proyectos Wikimedia.

**Visita la aplicación en vivo:** **[https://geo-editores.toolforge.org/](https://geo-editores.toolforge.org/)**



---
## ## Acerca del Proyecto

Este visualizador es una herramienta integral diseñada para facilitar el análisis de los datos públicos de Wikimedia Analytics sobre la distribución geográfica de sus editores. La aplicación permite cargar, visualizar, filtrar y comparar los sets de datos mensuales a través de una interfaz limpia e intuitiva.

La arquitectura cliente-servidor, con un **backend en Node.js** y un **frontend en Vue.js 3**, asegura un rendimiento robusto, elimina problemas de CORS y ofrece una experiencia de usuario fluida y completamente responsiva.

---
## ## Características Principales

✨ **Interfaz Reactiva y Moderna:** Construida con Vue.js 3 y Tailwind CSS para una experiencia de usuario fluida y un diseño adaptable a cualquier dispositivo.

📊 **Visualización Dual de Datos:** Analiza tendencias con un gráfico de líneas y resume volúmenes totales con un gráfico de barras, ambos interactivos y generados con Chart.js.

🔍 **Panel de Filtros Avanzado:** Filtra fácilmente por año, mes, proyecto (wiki) y país con selectores múltiples que incluyen buscadores para manejar grandes listas.

⚖️ **Herramienta de Comparación:** Compara dos conjuntos de datos distintos (ej. Chile vs. Argentina en un mismo mes) en un panel dedicado con tablas y gráficos comparativos.

🎓 **Tutorial Interactivo:** Una guía de bienvenida que introduce a los nuevos usuarios a todas las funcionalidades de la plataforma.

💾 **Exportación a CSV:** Exporta los datos filtrados para un análisis externo en hojas de cálculo u otras herramientas.

---
## ## Construido Con

Este proyecto fue posible gracias a las siguientes tecnologías:

**Backend:**
* [Node.js](https://nodejs.org/)
* [Express.js](https://expressjs.com/)
* [Axios](https://axios-http.com/) (para peticiones HTTP)
* [Cheerio](https://cheerio.js.org/) (para web scraping)

**Frontend:**
* [Vue.js 3](https://vuejs.org/) (con Composition API)
* [Tailwind CSS](https://tailwindcss.com/)
* [Chart.js](https://www.chartjs.org/)
* [Font Awesome](https://fontawesome.com/)

---
## ## Uso Local

Para ejecutar este proyecto en tu propia máquina, sigue estos pasos:

1.  **Prerrequisitos:** Asegúrate de tener [Node.js](https://nodejs.org/) instalado (incluye npm).

2.  **Clona el repositorio:**
    ```sh
    git clone [https://github.com/jordylizana-ship-it/Visualizador-Geo-editores.git](https://github.com/jordylizana-ship-it/Visualizador-Geo-editores.git)
    ```

3.  **Navega a la carpeta del proyecto:**
    ```sh
    cd Visualizador-Geo-editores
    ```

4.  **Instala las dependencias:**
    ```sh
    npm install
    ```

5.  **Inicia el servidor:**
    ```sh
    npm start
    ```
    ¡Listo! La aplicación estará corriendo en `http://localhost:3000`.

---
## ## Licencia

Distribuido bajo la Licencia MIT. Ver `LICENSE` para más información.

---
## ## Contacto

Jordy Lizana - [jordylizana-ship-it](https://github.com/jordylizana-ship-it)
