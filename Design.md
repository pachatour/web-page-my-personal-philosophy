# DOCUMENTATION de Diseño

**ID Tarea/Referencia:** D-01

**Título:** Definición de la identidad Visual (Cólores y Tipografía)

**Objetivo:** Establecer la palata de colores primarios y secundarios, junto con la jerarquía tipografía, para asegurar la consistencia y el reconocimeinto de la marca a lo largo de todas las plataforas digitales.

## Paleta de Colores (Colors)

<img width="472" height="472" alt="image" src="https://github.com/user-attachments/assets/eb4fae13-f09a-452a-85a4-b69b308e9ad8" />

| Nombre (Variable SCSS/CSS) | Código HEX | Código RGB | Rol en la UI (Uso) |
| :--- | :---: | :---: | :--- |
| **$color-enfasis-principal** | #E67E22 | rgb(230, 126, 34) | Acciones Principales (CTAs), Botones Clave, Elementos Interactivos. |
| **$color-fondo-oscuro** | #628141 | rgb(98, 129, 65) | Fondo de Secciones, Tarjetas/Contenedores, Pie de Página, Barras Laterales. |
| **$color-secundario** | #8BAE66 | rgb(139, 174, 102) | Énfasis en Contenido Secundario, Iconografía, Citas, badges o tooltips |
| **$color-fondo-claro** | #EBD5AB | rgb(235, 213, 171) | Fondo Principal de la Página, Superficies para Lectura de Texto Largo (simula pergamino). |

## Tipografía (Fonts)

<img width="799" height="424" alt="image" src="https://github.com/user-attachments/assets/13aa9bb0-662c-48ed-b93b-3c04c1431a58" />

| Estilo (Clase CSS) | Fuente | Tamaño (px/rem) | Peso (Weight) | Rol en la UI (Uso) |
| :--- | :--- | :---: | :---: | :--- |
| **H1** (.heading-1) | **Playfair Display** | 80px (5rem) | Bold (700 o 900) | **Título principal de la página.** (Lazo 80 PT BOLD) Transmite sofisticación y autoridad. |
| **H2** (.heading-2) | **Playfair Display** | 28px (1.75rem) | Medium/SemiBold (500 o 600) | Títulos de sección importantes, encabezados clave. (Lazo 28 PT) Mantiene la elegancia del título principal. |
| **Body Default** (.text-base) | **Lora** | 14px (0.875rem) | Regular (400) | **Texto estándar del cuerpo,** párrafos de lectura, listas. (Lazo 14 PT Cuerpo) Una serif clásica y legible, ideal para el texto de filosofía. |
| **Body Small** (.text-sm) | Lora | 12px (0.75rem) | Regular (400) | Notas al pie, metadatos, captions, texto legal. |

## EStructura de Archivo y Arquitectura CSS

/mi-web-filosofia

├── public/                 // Archivos estáticos (favicon, manifest, robots.txt)

├── src/

│   ├── assets/             // Recursos de la web (Imágenes, SVGs)

│   ├── data/               // Contenido en JSON/Markdown (Citas, Conceptos Clave)

│   ├── theme/              // **Configuración de la Identidad Visual (D-01)**

│   │   ├── colors.js         // Definición de la paleta (D-01)

│   │   ├── fonts.js          // Definición de tipografía (D-01)

│   │   └── theme.js          // Objeto principal que agrupa `colors` y `fonts`

│   ├── components/         // Componentes UI reutilizables

│   │   ├── GlobalStyles/     // Estilos de Reset/Base y globales

│   │   │   └── GlobalStyles.js

│   │   ├── Layout/           // Estructura de la página (Header, Footer)

│   │   │   ├── Header.jsx

│   │   │   └── Footer.jsx

│   │   ├── Button/           // Componente básico y reutilizable

│   │   │   └── Button.jsx

│   │   └── Card/             // Componente para presentar ideas/citas

│   │       └── Card.jsx

│   ├── pages/              // Páginas principales (vistas)

│   │   ├── Home.jsx          // Página de inicio

│   │   ├── Ikigai.jsx        // Página dedicada a Ikigai

│   │   ├── Estoicismo.jsx    // Página dedicada al Estoicismo

│   │   └── Nietzsche.jsx     // Página dedicada a Nietzsche

│   ├── App.jsx             // Componente raíz (manejo de rutas)

│   └── index.js            // Punto de entrada del proyecto

├── .gitignore

├── package.json

└── README.md
