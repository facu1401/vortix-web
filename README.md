#  VortiX Studio

> Marketplace de modelos 3D para mentes creativas — hecho con amor, rotuladores y mucho café ☕

![VortiX Studio](https://img.shields.io/badge/VortiX-Studio-00E5FF?style=for-the-badge&logo=data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHZpZXdCb3g9IjAgMCAyNCAyNCI+PHBhdGggZmlsbD0iI2ZmZiIgZD0iTTEzIDJ2OGg4bC0xMCAxMnYtOEgzbDEwLTEyeiIvPjwvc3ZnPg==)
![HTML](https://img.shields.io/badge/HTML5-puro-E34F26?style=for-the-badge)
![CSS](https://img.shields.io/badge/CSS3-custom-1572B6?style=for-the-badge)
![JS](https://img.shields.io/badge/JavaScript-vanilla-F7DF1E?style=for-the-badge)
![Sin dependencias](https://img.shields.io/badge/dependencias-ninguna-39FF14?style=for-the-badge)

---

## Contenido

- [¿Qué es esto?](#-qué-es-esto)
- [Características](#-características)
- [Estructura del archivo](#-estructura-del-archivo)
- [Cómo usarlo](#-cómo-usarlo)
- [Secciones](#-secciones)
- [Paleta de colores](#-paleta-de-colores)
- [Tipografías](#-tipografías)
- [Internacionalización](#-internacionalización)
- [Temas](#-temas-claro--oscuro)
- [Modales](#-modales)
- [Personalización](#-personalización)

---

## ¿Qué es esto?

**VortiX Studio** es un sitio web para un marketplace de modelos 3D orientado a niños y jóvenes de 10-18 años. 

La estética está diseñada con letras torcidas, post-its de colores, cinta adhesiva, garabatos SVG, botones con sombra desplazada tipo cómic y mucho emoji.

---

## Características

### Funcionalidades principales
- **Catálogo de productos** con grid responsive y filtros por categoría
- **Buscador** en el header
- **Favoritos** con feedback visual por producto
- **Añadir al carrito** con confirmación animada
- **Cargar más productos** dinámicamente
- **Filtro de precio** con slider interactivo
- **Filtros toggle** (nuevos, populares, oferta, gratuitos)
- **Ordenación** (populares / nuevos / precio)

### Modales
- **Modal de producto** — carrusel de 3 imágenes, descripción detallada, precio, tags, botones de carrito y favorito
- **Modal legal** — 3 pestañas (Privacidad / Términos / Cookies) con contenido completo
- Cierre con ✕, clic fuera o tecla `Escape`

### Secciones de contenido
- **Hero** — título animado, tarjeta flotante con stickers, doodles SVG de fondo
- **Banner destacado** — producto del mes con animación y cintas decorativas
- **FAQ** — 8 preguntas en acordeón con colores únicos por ítem
- **Contacto** — formulario con validación, selector de asunto y confirmación
- **Cómo imprimir** — 4 pasos visuales con tips de configuración
- **Footer** completo con links, redes sociales y secciones de navegación

### UX & Diseño
- **Tema oscuro / claro** con transición suave
- **3 idiomas**: Español, English, Português (cambio en tiempo real)
- **Responsive** para móvil, tablet y escritorio
- **Scroll reveal** con animaciones de entrada escalonadas
- **Sistema de badges** (NUEVO / HOT / OFERTA) con rotación al canto

---
## Secciones

### Header fijo
Contiene el logo animado, navegación, buscador, selector de idioma (🇪🇸 🇺🇸 🇧🇷) y botón de tema. Se queda pegado arriba al hacer scroll.

### Hero
Título grande con tipografía `Bangers`, descripción en `Caveat`, dos CTAs y una tarjeta flotante con el producto destacado. El fondo tiene círculos discontinuos, líneas onduladas, estrellas y cruces dibujadas con SVG inline.

### Banner destacado
Caja con bordes cian y sombra púrpura. Cintas decorativas (`EDICIÓN LIMITADA`, `solo 50 uds`) que salen por encima y por debajo. Emoji animado a la derecha.

### Catálogo
Grid de dos columnas: sidebar con filtros (categorías, precio, opciones) y zona principal con las cards. Cada card tiene imagen emoji, badge, botón de favorito, estrellas de valoración, precio y botón "Ver más" que abre el modal de producto.

### FAQ
8 preguntas en acordeón de dos columnas. Solo una pregunta puede estar abierta a la vez. Cada ítem tiene su propio color de acento.

### Contacto
Formulario con nombre, correo, selector de asunto, textarea de mensaje y botón de envío. Incluye validación básica y mensaje de confirmación.

### Cómo imprimir
4 pasos numerados con descripción y tip de configuración (temperatura, porcentaje de relleno, etc.).

### Footer
Descripción de marca, links de redes sociales, columnas de navegación (Explorar / Ayuda / Legal). Los links de Legal abren el modal correspondiente.

---

## Paleta de colores

| Variable | Valor | Uso |
|---|---|---|
| `--cyan` | `#00E5FF` | Color principal, bordes, acentos |
| `--yellow` | `#FFE500` | Cintas adhesivas, precios, highlights |
| `--orange2` | `#FF6B35` | Badges de oferta, botones secundarios |
| `--green` | `#39FF14` | Badges "nuevo", confirmaciones |
| `--orange` | `#FF6B00` | Badges "hot", tips de impresión |
| `--purple` | `#7C4DFF` | Sombras desplazadas, acentos secundarios |
| `--ink` | `#1a1a2e` | Fondo oscuro |
| `--paper` | `#fffef2` | Texto principal modo oscuro |

---

## Tipografías

Todas se cargan desde Google Fonts:

| Fuente | Uso |
|---|---|
| **Bangers** | Títulos principales, nombres de productos, botones |
| **Permanent Marker** | Labels, badges, precios, cintas |
| **Caveat** | Textos descriptivos, navegación, taglines |
| **Patrick Hand** | Cuerpo de texto, formularios, FAQ |

---

## Internacionalización

El sistema i18n es manual y vive en el objeto `T` dentro del `<script>`:

```javascript
const T = {
  es: { nav_home: 'Inicio', hero_cta: '🚀 Explorar catálogo', ... },
  en: { nav_home: 'Home',   hero_cta: '🚀 Explore catalog',  ... },
  pt: { nav_home: 'Início', hero_cta: '🚀 Explorar catálogo',...  },
};
```

Para cambiar un texto, busca su clave en el HTML (`data-i18n="clave"`) y edita el valor en los tres idiomas dentro de `T`.

Para añadir un nuevo elemento traducible:

```html
<!-- En el HTML -->
<span data-i18n="mi_clave">Texto por defecto</span>

<!-- En el JS, dentro de T.es / T.en / T.pt -->
mi_clave: 'Mi texto traducido'
```

El FAQ, los modales de producto y el modal legal tienen sus propios objetos de datos (`FAQS`, `prodDetails`, `LC`) que también están organizados por idioma.

---

## Temas (claro / oscuro)

El tema se controla con el atributo `data-theme` en el `<html>`:

```html
<html data-theme="dark">  <!-- oscuro por defecto -->
<html data-theme="light"> <!-- claro -->
```

Todos los estilos de modo claro usan el selector `[data-theme="light"]`:

```css
[data-theme="light"] body {
  background-color: #eef4ff;
  color: #1a1a2e;
}
```

Para cambiar el tema por defecto, cambia `data-theme="dark"` a `data-theme="light"` en la etiqueta `<html>` y actualiza el emoji del botón (`🌙` → `☀️`) en el botón `#tbtn`.

---

## Modales

### Modal de producto
Se abre al hacer clic en "Ver más" en cualquier card. Recibe el índice del producto (`prods[idx]`) y los detalles extendidos (`prodDetails[idx]`).

Para añadir un producto nuevo:

```javascript
// 1. En el array prods[]
{ e:'🦄', n:'Unicornio Épico', p:14.99, cat:'figures', b:'new', r:5, rv:42, cc:'cc-c' }

// 2. En el array prodDetails[] (mismo índice)
{ slides:['🦄','✨','🌈'], labels:['Vista frontal','Detalle cuerno','Con arcoíris'],
  desc:'Descripción del producto...', tags:['18cm','Articulado','Edición especial'] }
```

### Modal legal
Se abre con `openLegal('privacy')`, `openLegal('terms')` o `openLegal('cookies')`. El contenido de cada sección y cada idioma vive en el objeto `LC`.

---

## 🛠️ Personalización

### Cambiar colores principales
Edita las variables CSS en `:root`:
```css
:root {
  --cyan: #00E5FF;   /* ← cambia aquí */
  --yellow: #FFE500;
  --purple: #7C4DFF;
}
```

### Añadir una categoría de filtro
```html
<!-- En el sidebar HTML -->
<div class="fi" onclick="fcat(this,'mi-cat')">
  <span>Mi Categoría</span><span class="fi-c">0</span>
</div>
```
```javascript
// En catN para las traducciones
'mi-cat': { es:'Mi Categoría', en:'My Category', pt:'Minha Categoria' }
```

### Cambiar el idioma por defecto
Al final del script, cambia:
```javascript
setLang('es');  // → setLang('en') o setLang('pt')
```

---

## Licencia

Proyecto de uso libre para fines educativos y personales. Los emojis son propiedad de sus respectivos autores.

---

<div align="center">
  <p> Vibe coding with <code>Cloude</code></p>
  <p><strong>VortiX Studio</strong> — donde las ideas toman forma</p>
</div>