# Lubricentro La Esquina - Plataforma Web Corporativa

[![Astro](https://img.shields.io/badge/Astro-5.0-BC52EE?style=flat-square&logo=astro&logoColor=white)](https://astro.build/)
[![Tailwind CSS](https://img.shields.io/badge/Tailwind_CSS-4.0-06B6D4?style=flat-square&logo=tailwindcss&logoColor=white)](https://tailwindcss.com/)
[![Vite](https://img.shields.io/badge/Vite-Bundler-646CFF?style=flat-square&logo=vite&logoColor=white)](https://vitejs.dev/)
[![TypeScript](https://img.shields.io/badge/TypeScript-Ready-3178C6?style=flat-square&logo=typescript&logoColor=white)](https://www.typescriptlang.org/)
[![Estado](https://img.shields.io/badge/Estado-Completado_y_Entregado-success?style=flat-square)](https://lubricentrolaesquina.cl)

---

## Descripcion General

Plataforma web corporativa y catalogo digital desarrollado como proyecto freelance para **Lubricentro La Esquina**, empresa especializada en mantenimiento automotriz, lubricacion y venta de insumos tecnicos en Chile.

El proyecto fue concebido para transformar la presencia digital del negocio, ofreciendo a los clientes una experiencia rapida, intuitiva y optimizada para dispositivos moviles, facilitando la consulta de servicios, la exploracion de productos por especificacion tecnica y la conversion directa hacia canales de atencion inmediata.

---

## Contexto y Desafio de Negocio

El cliente requeria superar las limitaciones de una presencia web tradicional mediante:

- **Visibilidad de catalogo:** Presentar de manera clara y estructurada una amplia gama de lubricantes, aceites y fluidos con especificaciones tecnicas (viscosidad, normativa, capacidad y aplicacion recomendada).
- **Generacion de prospectos (Leads):** Reducir la friccion de contacto conectando a los usuarios directamente con los canales de atencion del taller via WhatsApp, llamada directa y formularios interactivos.
- **Autoridad y confianza:** Transmitir la trayectoria del negocio (mas de 15 anos de experiencia), certificaciones tecnicas, alianzas con marcas lideres del rubro automotriz y opiniones verificadas de clientes.
- **Rendimiento extremo:** Garantizar tiempos de carga inferiores a 1 segundo para minimizar la tasa de rebote en conexiones moviles.

---

## Solucion Implementada y Funcionalidades

### 1. Catalogo Digital de Productos e Insumos
- Organizacion de lubricantes y fluidos por viscosidades y tipos de motor (gasolina, diesel, gas, sinteticos, semisinteticos y post-tratamiento).
- Fichas descriptivas por producto con detalle de aplicacion, volumen y precio.
- Componente de gestion de disponibilidad de stock (`Stock.astro`) con indicadores visuales de estado: disponible, unidades limitadas y agotado.

### 2. Portafolio de Servicios Automotrices
- Desglose de servicios especializados: cambio de aceite de motor, transmisiones, direccion hidraulica, filtros y mantenciones preventivas.
- Detalle de valor agregado: diagnostico express sin cita previa, uso de insumos 100% originales y respaldo tecnico garantizado.

### 3. Sistema de Conversion y Contacto Multicanal
- Menu flotante de acceso rapido (`Speed Dial`) siempre visible en la interfaz para contacto inmediato con un clic hacia WhatsApp, linea telefonica o seccion de contacto.
- Formulario de cotizacion y consulta directa.
- Informacion de ubicacion fisica, mapas y horarios de atencion segmentados por dia.

### 4. Prueba Social y Confianza de Marca
- Slider infinito continuo (*marquee*) con logotipos de marcas oficiales asociadas (Mobil, Shell, Liqui Moly, Castrol, Motul, Valvoline, Repsol, Lubrax, Pennzoil, Petro Canada).
- Seccion de resenas y testimonios verificados de clientes recurrentes para consolidar la credibilidad del taller.

### 5. Seccion Institucional y Metricas de Impacto
- Cronologia y valores del negocio en la seccion "Nosotros".
- Metricas cuantitativas destacadas: mas de 35 anos de trayectoria combinada, mas de 10,000 servicios realizados y un 98% de satisfaccion de clientes.

---

## Arquitectura y Stack Tecnologico

El proyecto fue desarrollado adoptando una arquitectura de generacion estatica (SSG) para asegurar la maxima velocidad de respuesta, seguridad y eficiencia en el consumo de recursos.

| Tecnologia / Herramienta | Proposito en el Proyecto |
| :--- | :--- |
| **Astro 5** | Framework principal orientado a contenido y rendimiento, renderizando HTML puro con cero sobrecarga de JavaScript en el cliente por defecto. |
| **Tailwind CSS 4** | Sistema de diseno y estilos utilitarios modernos con integracion directa mediante `@tailwindcss/vite`. |
| **TypeScript / JS Moderno** | Tipado estatico en componentes y logica de navegacion, sliders y animaciones de interfaz. |
| **Astro Sitemap** | Generacion automatica de mapas de sitio XML para optimizacion de indexacion en motores de busqueda. |
| **Onest Font Variable** | Tipografia moderna de alta legibilidad integrada mediante `@fontsource-variable/onest`. |
| **Vite Engine** | Bundler y optimizador de assets para produccion con minimizacion de recursos estaticos. |

---

## Decisiones de Diseno y Experiencia de Usuario (UI/UX)

- **Direccion visual:** Paleta de colores sobria y profesional basada en tonos oscuros (gris pizarra / grafito), fondos neutros y toques en rojo corporativo para llamadas a la accion y jerarquia de elementos.
- **Animaciones y microinteracciones:** Implementacion de un sistema de aparicion progresiva (`FadeIn.astro`) basado en la API nativa de `IntersectionObserver`, logrando transiciones fluidas al hacer scroll sin penalizar el rendimiento.
- **Efectos de profundidad:** Cabeceras con efecto parallax optimizado (`ParallaxHero.astro`) que responden suavemente al desplazamiento vertical.
- **Adaptabilidad total (Responsive Design):** Navegacion adaptada con cajon lateral interactivo en telefonos moviles y menu horizontal extendido en pantallas de escritorio.

---

## Optimizacion, SEO y Rendimiento

- **HTML Semantico y Accesibilidad:** Estructura basada en etiquetas semanticas (`header`, `main`, `nav`, `section`, `footer`), jerarquia estricta de encabezados H1-H3 y atributos de accesibilidad (`aria-label`, `aria-hidden`).
- **SEO Tecnico Local:** Metadatos Open Graph, etiquetas de descripcion contextualizadas para busquedas de servicios automotrices locales y dominio canonico configurado.
- **Optimizacion de Multimedia:** Imagenes en formatos modernos de compresion (`.webp`, `.svg`), con directivas de carga `eager` para el contenido *Above the Fold* y carga diferida en secciones inferiores.

---

## Estructura del Codigo Fuente

```
project/
├── public/
│   ├── img/
│   │   ├── banners/          # Imagenes de cabecera y fondos parallax
│   │   ├── logo/             # Identidad visual corporativa y logotipos de marcas
│   │   ├── productos/        # Imagenes de catalogo de lubricantes
│   │   └── avatars/          # Fotografias de testimonios de clientes
│   └── favicon.svg           # Icono del sitio
├── src/
│   ├── components/
│   │   ├── Container.astro   # Contenedor centralizado con limites de ancho
│   │   ├── FadeIn.astro      # Controlador de animaciones por scroll
│   │   ├── Footer.astro      # Pie de pagina corporativo con horarios y enlaces
│   │   ├── Header.astro      # Barra de navegacion principal y menu responsive
│   │   ├── ParallaxHero.astro# Hero section con efecto de profundidad
│   │   ├── Resenas.astro     # Modulo de testimonios y valoraciones
│   │   └── Stock.astro       # Badge dinamico de disponibilidad de stock
│   ├── layouts/
│   │   └── Layout.astro      # Plantilla base (metatags, fuentes, speed-dial flotante)
│   ├── pages/
│   │   ├── index.astro       # Pagina principal (Home)
│   │   ├── servicios.astro   # Pagina de servicios automotrices
│   │   ├── productos.astro   # Pagina de catalogo de productos
│   │   ├── nosotros.astro    # Pagina institucional y valores
│   │   └── contacto.astro    # Pagina de contacto, formulario y mapa
│   └── styles/
│       └── global.css        # Importacion de Tailwind CSS y animaciones clave
├── astro.config.mjs          # Configuracion de integraciones (Sitemap, Vite, Tailwind)
├── package.json              # Dependencias y scripts del proyecto
├── tsconfig.json             # Configuracion de compilacion TypeScript
└── README.md                 # Documentacion tecnica del proyecto
```

---

## Informacion del Proyecto y Creditos

- **Proyecto:** Sitio Web Corporativo y Catalogo Digital
- **Cliente:** Lubricentro La Esquina
- **Desarrollo:** devSantos (Desarrollo Web Freelance)
- **Tipo de Proyecto:** Encargo Freelance / Produccion Web
- **Estado:** Entregado y Operativo
