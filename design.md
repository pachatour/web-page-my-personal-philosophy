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

```
/miFilosofia
├── assets/                     // Archivos estáticos
│   ├── css/                    // Todo el CSS vive aquí
│   │   ├── _variables.css        // (D-01: Colores, fuentes, espaciado como CSS Custom Properties)
│   │   ├── _base.css             // (Estilos de Reset, Tipografía base, Body)
│   │   ├── _layout.css           // (Media Queries, Grid, Flexbox)
│   │   └── style.css             // Archivo principal que importa todos los anteriores
│   ├── js/                     // Archivos JavaScript
│   │   └── main.js               // Lógica principal (navegación, interacciones)
│   └── img/                    // Imágenes y logos (incluye favicons)
├── data/                       // Archivos de contenido (si los quieres externos al HTML)
│   ├── ikigai.json             // Citas o datos de Ikigai (Ejemplo)
│   └── nietzsche.txt           // Textos largos (Ejemplo)
├── content/                    // Archivos del contenido de la pagina (pdfs, etc)
├── index.html                  // (Página de Inicio)
├── ikigai.html                 // Página dedicada a Ikigai
├── estoicismo.html             // Página dedicada al Estoicismo
└── nietzsche.html              // Página dedicada a Nietzsche
```
## Plan Responsivo

#### 1. Principio de Diseño: Mobile First

* **Metodología:** Los estilos base se definen para la **pantalla más pequeña (móvil)**.
* **Mejora:** Se utiliza `min-width` en las Media Queries para aplicar estilos *adicionales* solo en pantallas más grandes.

#### 2. Definición de Breakpoints (Puntos de Ruptura)

Se utilizarán tres breakpoints clave para manejar la transición del diseño:

| Nombre (Referencia) | Valor (min-width) | Uso Principal |
| :--- | :--- | :--- |
| **Móvil (Base)** | 0px | Diseño por defecto (una columna, máxima legibilidad). |
| **Tablet/Medio (MD)** | **768px** | Ajustes de padding, aumento de tamaño de fuentes, potencial barra lateral simple. |
| **Escritorio/Grande (LG)** | **1200px** | Layout de contenido principal de dos o tres columnas (si es necesario) y ancho máximo de página. |
