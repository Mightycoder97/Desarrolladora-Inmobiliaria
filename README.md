<p align="center">
  <img src="public/favicon.svg" alt="Dharsain Inmobiliaria Logo" width="80" height="80" />
</p>

<h1 align="center">Dharsain Inmobiliaria</h1>

<p align="center">
  <strong>Plataforma web inmobiliaria profesional — Proyectos, terrenos e inversiones en Lima, Perú.</strong>
</p>

<p align="center">
  <a href="https://dharsain-inmobiliaria.vercel.app">
    <img src="https://img.shields.io/badge/🌐_Sitio_Web-Live-22c55e?style=for-the-badge" alt="Live Site" />
  </a>
  <img src="https://img.shields.io/badge/Astro-6.x-FF5D01?style=for-the-badge&logo=astro&logoColor=white" alt="Astro" />
  <img src="https://img.shields.io/badge/Vercel-Deployed-000000?style=for-the-badge&logo=vercel&logoColor=white" alt="Vercel" />
  <img src="https://img.shields.io/badge/TypeScript-Strict-3178C6?style=for-the-badge&logo=typescript&logoColor=white" alt="TypeScript" />
  <img src="https://img.shields.io/badge/License-Private-gray?style=for-the-badge" alt="License" />
</p>

---

## 📋 Tabla de Contenidos

- [Descripción del Proyecto](#-descripción-del-proyecto)
- [Características Principales](#-características-principales)
- [Stack Tecnológico](#-stack-tecnológico)
- [Arquitectura del Proyecto](#-arquitectura-del-proyecto)
- [Requisitos Previos](#-requisitos-previos)
- [Instalación y Configuración](#-instalación-y-configuración)
- [Comandos Disponibles](#-comandos-disponibles)
- [Estructura de Páginas](#-estructura-de-páginas)
- [Despliegue](#-despliegue)
- [Variables de Entorno](#-variables-de-entorno)
- [SEO y Performance](#-seo-y-performance)
- [Contribución](#-contribución)
- [Licencia](#-licencia)

---

## 🏗️ Descripción del Proyecto

**Dharsain Inmobiliaria** es una plataforma web corporativa diseñada para una desarrolladora inmobiliaria con sede en Lima, Perú. El sitio tiene como objetivo principal la captación de leads, la presentación profesional de proyectos inmobiliarios y la generación de confianza en potenciales inversionistas y compradores.

El proyecto está construido con **Astro 6.x** utilizando una arquitectura **SSG (Static Site Generation)** con adaptador **Vercel** para entornos serverless, garantizando tiempos de carga ultra rápidos y excelente posicionamiento SEO.

---

## ✨ Características Principales

| Categoría | Detalle |
|---|---|
| 🏠 **Landing Page** | Hero con CTA de conversión, servicios destacados, contadores animados y sección de testimonios |
| 🏗️ **Proyecto** | Galería interactiva, tabla de precios, planes de financiamiento y mapa de ubicación |
| 🏢 **Servicios** | Cards interactivas con asesoría, compra/venta y administración de propiedades |
| 🔍 **Terrenos** | Catálogo filtrable de terrenos disponibles con detalles y contacto directo |
| 💰 **Inversionistas** | Propuesta de valor, datos de rentabilidad (ROI) y formulario exclusivo |
| 📖 **Nosotros** | Misión, visión, valores y equipo directivo |
| 📱 **WhatsApp Flotante** | Botón de contacto siempre visible en todas las páginas |
| 🔍 **SEO Optimizado** | Meta tags, Open Graph, Schema.org y sitemap automático |
| 📱 **Responsive Design** | Diseño 100% adaptable a dispositivos móviles, tablets y desktop |

---

## 🛠️ Stack Tecnológico

| Tecnología | Rol | Versión |
|---|---|---|
| [Astro](https://astro.build) | Framework (SSG/SSR) | `^6.0.4` |
| [TypeScript](https://www.typescriptlang.org) | Tipado estricto | Strict mode |
| CSS Custom Properties | Sistema de estilos | Vanilla CSS |
| [Vercel](https://vercel.com) | Hosting & Serverless | Edge Runtime |
| [`@astrojs/sitemap`](https://docs.astro.build/en/guides/integrations-guide/sitemap/) | Sitemap automático | `^3.7.1` |
| [`@astrojs/vercel`](https://docs.astro.build/en/guides/deploy/vercel/) | Adaptador de despliegue | `^10.0.0` |

---

## 📁 Arquitectura del Proyecto

```
dharsain-inmobiliaria/
├── public/                     # Archivos estáticos (favicon, imágenes)
│   ├── favicon.ico
│   └── favicon.svg
├── src/
│   ├── assets/                 # Assets del proyecto (SVGs, imágenes)
│   │   ├── astro.svg
│   │   └── background.svg
│   ├── components/             # Componentes reutilizables de Astro
│   │   ├── Header.astro        # Navegación principal con menú responsive
│   │   ├── Footer.astro        # Footer con redes sociales y sitemap
│   │   ├── WhatsAppFloat.astro # Botón flotante de WhatsApp
│   │   └── Welcome.astro       # Componente de bienvenida
│   ├── layouts/
│   │   └── Layout.astro        # Layout base con SEO (meta, OG tags)
│   ├── pages/                  # Páginas del sitio (file-based routing)
│   │   ├── index.astro         # Home / Landing page
│   │   ├── proyecto.astro      # Detalle del proyecto inmobiliario
│   │   ├── servicios.astro     # Servicios inmobiliarios
│   │   ├── terrenos.astro      # Catálogo de terrenos
│   │   ├── inversionistas.astro# Portal de inversionistas
│   │   └── nosotros.astro      # Sobre la empresa
│   └── styles/
│       └── global.css          # Estilos globales y design tokens
├── astro.config.mjs            # Configuración de Astro (site, integraciones)
├── tsconfig.json               # Configuración TypeScript (strict)
├── package.json                # Dependencias y scripts
└── README.md                   # Documentación del proyecto
```

### Patrones Arquitectónicos

- **File-based Routing**: Cada archivo `.astro` en `src/pages/` genera una ruta automáticamente.
- **Layout Pattern**: El `Layout.astro` centraliza la estructura HTML, meta tags y componentes transversales (Header, Footer, WhatsApp).
- **Island Architecture**: Componentes con hidratación parcial — cero JavaScript innecesario enviado al cliente.
- **CSS Custom Properties**: Sistema de diseño basado en variables CSS para tematización consistente.

---

## 📌 Requisitos Previos

Asegúrate de contar con las siguientes herramientas instaladas:

| Herramienta | Versión Mínima | Verificar instalación |
|---|---|---|
| **Node.js** | `≥ 22.12.0` | `node --version` |
| **npm** | `≥ 10.x` | `npm --version` |
| **Git** | `≥ 2.x` | `git --version` |

---

## 🚀 Instalación y Configuración

### 1. Clonar el repositorio

```bash
git clone https://github.com/Mightycoder97/Desarrolladora-Inmobiliaria.git
cd Desarrolladora-Inmobiliaria
```

### 2. Instalar dependencias

```bash
npm install
```

### 3. Iniciar el servidor de desarrollo

```bash
npm run dev
```

El sitio estará disponible en **`http://localhost:4321`**.

---

## 🧞 Comandos Disponibles

Todos los comandos se ejecutan desde la raíz del proyecto:

| Comando | Acción |
|:--|:--|
| `npm install` | Instala las dependencias del proyecto |
| `npm run dev` | Inicia el servidor de desarrollo en `localhost:4321` |
| `npm run build` | Genera el build de producción en `./dist/` |
| `npm run preview` | Previsualiza el build de producción localmente |
| `npm run astro ...` | Ejecuta comandos del CLI de Astro (`add`, `check`, etc.) |
| `npm run astro -- --help` | Muestra la ayuda del CLI de Astro |

---

## 🗺️ Estructura de Páginas

| Ruta | Página | Descripción |
|---|---|---|
| `/` | **Home** | Landing principal con hero, CTA de conversión, servicios destacados y contadores |
| `/proyecto` | **El Proyecto** | Galería interactiva, precios, financiamiento y mapa de ubicación |
| `/servicios` | **Servicios** | Asesoría, compra/venta y administración de propiedades |
| `/terrenos` | **Terrenos** | Catálogo filtrable de terrenos disponibles |
| `/inversionistas` | **Inversionistas** | Propuesta de valor, ROI y formulario exclusivo para inversores |
| `/nosotros` | **Nosotros** | Misión, visión, valores y equipo directivo |

### Componentes Transversales

| Componente | Descripción |
|---|---|
| `Header.astro` | Navegación fija con menú hamburguesa responsive + CTA "Contáctanos" |
| `Footer.astro` | Redes sociales, mapa del sitio y datos legales |
| `WhatsAppFloat.astro` | Botón flotante de WhatsApp siempre visible (bottom-right) |
| `Layout.astro` | Layout base con SEO automático: `<title>`, `<meta>`, Open Graph |

---

## 🌐 Despliegue

El proyecto está configurado para **despliegue continuo con Vercel**.

### Flujo de despliegue

```
┌─────────────┐       ┌──────────────┐       ┌──────────────────┐
│  Desarrollo │──────▶│   Staging     │──────▶│   Producción      │
│  (local)    │       │ (Preview URL) │       │ vercel.app        │
│ localhost   │       │ Pull Requests │       │ dominio propio    │
└─────────────┘       └──────────────┘       └──────────────────┘
```

| Entorno | Trigger | URL |
|---|---|---|
| **Producción** | Push a `main` | [dharsain-inmobiliaria.vercel.app](https://dharsain-inmobiliaria.vercel.app) |
| **Preview** | Pull Request | URL generada automáticamente por Vercel |
| **Local** | `npm run dev` | `http://localhost:4321` |

### Despliegue manual

```bash
# Build de producción
npm run build

# Preview del build
npm run preview
```

---

## 🔒 Variables de Entorno

Crea un archivo `.env` en la raíz del proyecto (no incluido en el repositorio por seguridad):

```env
# Ejemplo de variables de entorno
# PUBLIC_GOOGLE_MAPS_API_KEY=tu_api_key
# PUBLIC_GA4_MEASUREMENT_ID=G-XXXXXXXXXX
```

> ⚠️ **Nota**: Los archivos `.env` y `.env.production` están excluidos del repositorio vía `.gitignore`.

---

## 🔍 SEO y Performance

El sitio implementa las mejores prácticas de SEO y rendimiento:

| Aspecto | Implementación |
|---|---|
| **Meta Tags** | `<title>`, `<meta description>`, `<meta author>` por página |
| **Open Graph** | `og:title`, `og:description`, `og:image`, `og:type` configurados |
| **Sitemap XML** | Generado automáticamente con `@astrojs/sitemap` |
| **Canonical URL** | Configurada via `site` en `astro.config.mjs` |
| **Imágenes** | Optimizadas con componente `<Image>` de Astro (WebP/AVIF, lazy loading) |
| **SSL/HTTPS** | Certificado automático incluido con Vercel |
| **Core Web Vitals** | Optimizado para LCP < 2.5s y CLS < 0.1 gracias a SSG |
| **Idioma** | `lang="es"` declarado en `<html>` |

---

## 🤝 Contribución

1. Haz un **fork** del repositorio
2. Crea una rama para tu feature: `git checkout -b feature/nueva-funcionalidad`
3. Realiza tus cambios y haz commit: `git commit -m "feat: agregar nueva funcionalidad"`
4. Sube tu rama: `git push origin feature/nueva-funcionalidad`
5. Abre un **Pull Request** describiendo tus cambios

### Convención de Commits

Este proyecto sigue [Conventional Commits](https://www.conventionalcommits.org/):

| Prefijo | Uso |
|---|---|
| `feat:` | Nueva funcionalidad |
| `fix:` | Corrección de bugs |
| `docs:` | Cambios en documentación |
| `style:` | Cambios de estilo (CSS, formato) |
| `refactor:` | Refactorización de código |
| `perf:` | Mejoras de rendimiento |
| `chore:` | Tareas de mantenimiento |

---

## 📄 Licencia

Este proyecto es **privado** y propiedad de **SFO Estudio Web**. Todos los derechos reservados.

---

<p align="center">
  <sub>Desarrollado con ❤️ usando <a href="https://astro.build">Astro</a> · Desplegado en <a href="https://vercel.com">Vercel</a></sub>
</p>
