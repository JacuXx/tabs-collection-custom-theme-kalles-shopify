# 🛍️ Tabs Collection Custom - Sección Personalizada para Shopify

Una sección personalizada avanzada para mostrar colecciones de productos en formato de pestañas con un diseño elegante y responsive, optimizada para el tema Kalles.

## 📋 Tabla de Contenidos
- [Características](#características)
- [Vista Previa](#vista-previa)
- [Instalación](#instalación)
- [Configuración](#configuración)
- [Personalización](#personalización)
- [Soporte](#soporte)

## ✨ Características

### 🎨 Diseño y UX
- **Sistema de pestañas interactivo** con navegación fluida
- **Responsive design** optimizado para móvil y desktop
- **6 diseños de encabezado** diferentes
- **Estilos personalizables** para botones y colores
- **Efectos hover avanzados** (fade, sweep, shadow, etc.)
- **Slider de productos** con navegación por flechas y dots

### 🛠️ Funcionalidades Técnicas
- **Lazy loading** para mejor rendimiento
- **Carga asíncrona** de contenido de pestañas
- **Integración completa** con colecciones de Shopify
- **Iconos personalizables** (imágenes o clases CSS)
- **Múltiples layouts** (inline, stacked, column)
- **Sistema de grid responsive** (2-6 columnas)

### 🎯 Optimizaciones
- **SEO friendly** con estructura semántica
- **Performance optimizado** con carga diferida
- **Cross-browser compatible**
- **Theme editor integrado** para fácil configuración

## 🖼️ Vista Previa

### Desktop

![Banner](https://github.com/JacuXx/tabs-collection-custom-theme-kalles-shopify/blob/main/images/desktop.png)


### Mobile
![Banner](https://github.com/JacuXx/tabs-collection-custom-theme-kalles-shopify/blob/main/images/movil.png)

## 🚀 Instalación

### Requisitos Previos
- Tema Kalles instalado y activo
- Acceso al editor de código del tema
- Conocimientos básicos de Shopify Liquid

### Pasos de Instalación

#### 1. Copiar Archivos

**📁 Sección Principal:**
```bash
/sections/tabs_collection_custom.liquid
```
Copia este archivo a la carpeta `sections/` de tu tema Kalles.

**🎨 Estilos CSS:**
```bash
/assets/tabs_custom.css
```
Copia este archivo a la carpeta `assets/` de tu tema Kalles.

#### 2. Verificar Dependencias

Asegúrate de que tu tema Kalles incluya estos archivos CSS (ya deberían estar presentes):
- `section.css`
- `top-head.css`
- `tabs.css`
- `collection-products.css`
- `slider-settings.css`

#### 3. Activar la Sección

1. Ve al **Personalizador de Temas** de Shopify
2. Selecciona la página donde quieres agregar la sección
3. Haz clic en **"Agregar sección"**
4. Busca **"Tabs collection Custom"**
5. Configura tus pestañas y colecciones

## ⚙️ Configuración

### Configuración Básica

#### 1. Crear Pestañas
- Agrega bloques de tipo "Tab item"
- Configura título y colección para cada pestaña
- Opcionalmente agrega iconos (imagen o clase CSS)

#### 2. Diseño del Encabezado
```liquid
Opciones disponibles:
- Design 01: Básico centrado
- Design 02: Con línea decorativa
- Design 03: Con fondo
- Design 04: Estilo minimalista
- Design 05: Con sombra
- Design 06: Con iconos line-awesome
```

#### 3. Layout de Productos
- **Columnas Desktop:** 2-6 columnas
- **Columnas Mobile:** 1-3 columnas
- **Espaciado:** Configurable entre productos
- **Estilo:** Grid o slider

### Opciones Avanzadas

#### Personalización de Botones
```css
/* Colores personalizables */
--btn-color: #682537;        /* Color principal */
--btn-bg: #F1EDE9;          /* Fondo del botón */
--shadow: 0 4px 3px rgba(0, 0, 0, 0.15); /* Sombra */
```

#### Efectos de Hover
- Default, Fade, Rectangle out
- Sweep (right, left, top, bottom)
- Shutter horizontal, Outline, Shadow

## 🎨 Personalización

### Modificar Estilos CSS

Para personalizar los estilos, edita el archivo `tabs_custom.css`:

```css
/* Personalizar color de pestañas activas */
.custom-tabs .t4s-tab-item .t4s-text-title {
    color: #tu-color-aqui;
    font-weight: 400;
}

/* Personalizar botones de productos */
.ver-btn-product {
    background: #tu-color-de-fondo;
    color: #tu-color-de-texto;
    border-radius: 5px;
}

/* Personalizar título de sección */
.custom-tabs .t4s-section-title.t4s-title {
    font-size: 30px;
    font-weight: 400;
}
```

### Agregar Clases Personalizadas

En la configuración de la sección, usa el campo **"custom-class"** para agregar tus propias clases CSS:

```html
<!-- Ejemplo: -->
custom-class: "mi-clase-personalizada tabs-especiales"
```

### Configurar Colecciones

1. Ve a **Productos > Colecciones** en el admin de Shopify
2. Crea o selecciona las colecciones que quieres mostrar
3. En el configurador de la sección, asigna cada colección a una pestaña

## 📱 Responsive Design

### Breakpoints
- **Mobile:** < 768px (1-2 columnas)
- **Tablet:** 768px - 1024px (2-4 columnas)
- **Desktop:** > 1024px (4-6 columnas)

### Optimizaciones Mobile
- Navegación horizontal de pestañas con scroll
- Productos en slider con dots de navegación
- Botones de tamaño optimizado para touch
- Imágenes con lazy loading

## 🔧 Troubleshooting

### Problemas Comunes

**🚫 Las pestañas no aparecen:**
- Verifica que el archivo CSS esté en la carpeta `assets/`
- Confirma que las colecciones tienen productos
- Revisa que no haya conflictos de CSS

**🎨 Los estilos no se aplican:**
- Limpia la caché del navegador
- Verifica que `tabs_custom.css` esté correctamente enlazado
- Confirma que no hay CSS que sobrescriba los estilos

**📱 Problemas en mobile:**
- Verifica que el tema sea responsive
- Revisa los media queries en el CSS
- Confirma que el JavaScript de Flickity funcione

### Logs de Debug

Para debuggear, agrega esto al final de la sección:

```liquid
{% comment %} Debug info {% endcomment %}
<script>
console.log('Tabs loaded:', {{ section.blocks.size }});
console.log('Section ID:', '{{ section.id }}');
</script>
```

## 🆘 Soporte

### Información del Sistema
- **Compatibilidad:** Shopify 2.0, Tema Kalles
- **Browsers:** Chrome, Firefox, Safari, Edge
- **Versión:** 1.0.0

### Archivos Incluidos
```
tabs-custom-collection/
├── sections/
│   └── tabs_collection_custom.liquid
├── assets/
│   └── tabs_custom.css
└── README.md
```

### Contacto
Si encuentras algún problema o necesitas ayuda adicional:
- Documenta el error específico
- Incluye capturas de pantalla
- Menciona la versión de tu tema Kalles

---

## 📝 Changelog

### v1.0.0
- ✅ Lanzamiento inicial
- ✅ Integración completa con tema Kalles
- ✅ Sistema de pestañas responsive
- ✅ Lazy loading implementado
- ✅ 6 diseños de encabezado
- ✅ Múltiples efectos de hover

---

**💡 Tip:** Para mejores resultados, usa imágenes de productos con dimensiones consistentes (recomendado: 800x800px) y asegúrate de que las colecciones tengan al menos 4-6 productos para una mejor visualización.
