---
name: guia-schema-markup
description: Genera recomendaciones de schema markup con código JSON-LD para artículos, productos, FAQs y negocios locales. Usa cuando añadas datos estructurados a tu sitio web.
allowed-tools: Read Write Glob
author: Imperio Digital
version: "1.0"
---

# Guía de Schema Markup

## Cuándo Usar Este Skill

Usa este skill cuando necesites:
- Generar código de schema markup JSON-LD para tipos de página específicos
- Identificar qué tipos de schema son más valiosos para tu sitio
- Crear datos estructurados de FAQ, Producto, Artículo, NegocioLocal u otros
- Mejorar la apariencia de SERP con fragmentos enriquecidos, calificaciones de estrellas y listados mejorados

**NO** uses este skill para auditorías de SEO generales, optimización de meta tags o escritura de contenido. Esto es específicamente para implementación de datos estructurados.

---

## Principio Fundamental

EL SCHEMA MARKUP AYUDA A LOS MOTORES DE BÚSQUEDA A ENTENDER TU CONTENIDO Y MOSTRARLO MÁS ATRACTIVAMENTE EN RESULTADOS DE BÚSQUEDA — IMPLEMENTA LOS TIPOS QUE COINCIDAN CON TU CONTENIDO Y PUEDAN DISPARAR RESULTADOS ENRIQUECIDOS.

---

## Fase 1: Briefing

### Información Requerida

| Input | Qué Preguntar | Por Defecto |
|-------|------------|---------|
| **URL del sitio web** | "¿Cuál es tu sitio web?" | Sin defecto — debe proporcionarse |
| **Tipos de página** | "¿Qué tipos de páginas tienes? (blog, producto, FAQ, servicios, local)" | Publicaciones de blog y páginas de servicio |
| **Tipo de negocio** | "¿Eres un negocio local, negocio en línea o ambos?" | Negocio en línea |
| **CMS/plataforma** | "¿En qué plataforma está construido tu sitio?" | WordPress |
| **Schema actual** | "¿Tienes algún schema markup ya?" | Ninguno |

**PUNTO DE CONTROL: Confirma antes de generar markup.**

---

## Fase 2: Auditoría de Schema y Recomendaciones

### Tipos de Schema Prioritarios

Basado en el sitio, recomienda qué tipos de schema implementar:

```
## Tipos de Schema Recomendados

| Tipo de Schema | Páginas a Aplicar | Potencial de Resultado Enriquecido |
|-------------|---------------|---------------------|
| Article | Publicaciones de blog | Resultado enriquecido de artículo |
| FAQ | Páginas de FAQ, posts con Q&A | Desplegable de FAQ en SERP |
| HowTo | Posts de tutorial/guía | Resultado enriquecido paso a paso |
| Product | Páginas de producto/ventas | Precio, calificación, disponibilidad |
| LocalBusiness | Homepage, página de contacto | Panel local, mapa |
| Organization | Homepage | Panel de conocimiento |
| BreadcrumbList | Todas las páginas | Navegación de breadcrumb en SERP |
| WebSite | Homepage | Caja de búsqueda de sitelinks |
```

### Prioridad de Implementación

1. Organización o NegocioLocal (homepage) — establece entidad
2. Artículo (publicaciones de blog) — mejora presentación de contenido
3. FAQ (en cualquier lugar con contenido Q&A) — dispara resultado enriquecido de FAQ
4. BreadcrumbList (todas las páginas) — mejora navegación de SERP
5. Producto (si aplica) — habilita resultados enriquecidos de producto

**PUNTO DE CONTROL: Aprueba las prioridades de schema antes de generar código.**

---

## Fase 3: Generar Código de Schema

### Plantillas JSON-LD

**Schema de Artículo:**
```json
<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "Article",
  "headline": "[Título del Artículo]",
  "description": "[Meta descripción]",
  "image": "[URL de imagen destacada]",
  "author": {
    "@type": "Person",
    "name": "[Nombre del Autor]",
    "url": "[URL del Autor]"
  },
  "publisher": {
    "@type": "Organization",
    "name": "[Nombre del Negocio]",
    "logo": {
      "@type": "ImageObject",
      "url": "[URL del Logo]"
    }
  },
  "datePublished": "[YYYY-MM-DD]",
  "dateModified": "[YYYY-MM-DD]"
}
</script>
```

**Schema de FAQ:**
```json
<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "FAQPage",
  "mainEntity": [
    {
      "@type": "Question",
      "name": "[Pregunta 1]",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "[Respuesta 1]"
      }
    },
    {
      "@type": "Question",
      "name": "[Pregunta 2]",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "[Respuesta 2]"
      }
    }
  ]
}
</script>
```

**Schema de NegocioLocal:**
```json
<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "LocalBusiness",
  "name": "[Nombre del Negocio]",
  "description": "[Descripción del negocio]",
  "url": "[URL del Sitio Web]",
  "telephone": "[Teléfono]",
  "address": {
    "@type": "PostalAddress",
    "streetAddress": "[Calle]",
    "addressLocality": "[Ciudad]",
    "addressRegion": "[Estado]",
    "postalCode": "[ZIP]",
    "addressCountry": "ES"
  }
}
</script>
```

---

## Fase 4: Pulir

### 1. Guía de Implementación

- Dónde colocar código JSON-LD (en sección `<head>`)
- Opciones de plugin de WordPress (Yoast, Rank Math, o inserción manual)
- Cómo añadir a páginas individuales vs. plantillas

### 2. Pasos de Validación

- Prueba cada markup en herramienta Rich Results Test de Google
- Verifica errores en Google Search Console bajo Enhancements
- Valida sintaxis JSON antes de desplegar

### 3. Monitoreo

- Rastrea impresiones de resultado enriquecido en Google Search Console
- Monitorea errores de schema después de actualizaciones de sitio
- Revisa nuevos tipos de schema que Google soporta anualmente

---

## Anti-Patrones

- **Marcar contenido que no existe en la página** — el schema debe coincidir con contenido visible de página. El schema invisible es engañoso y viola directrices.
- **Usar tipos de schema deprecados** — verifica schema.org para tipos actuales. Algunos tipos más antiguos ya no disparan resultados enriquecidos.
- **Schema de FAQ en cada página** — solo usa FAQ schema donde preguntas y respuestas genuinas existen. Overuse puede llevar a Google ignorarlo.
- **Propiedades requeridas faltantes** — cada tipo de schema tiene campos requeridos. El markup incompleto no dispará resultados enriquecidos.
- **Schema duplicado en la misma página** — dos schemas de Artículo en una página confunde crawlers. Un tipo de schema por tipo de página.

---

## Recuperación

- **No estoy seguro qué tipos de schema aplican:** Ejecuta la página a través de Google's Rich Results Test para ver qué se detecta actualmente, luego añade lo que falta.
- **Errores de schema en Search Console:** Revisa el mensaje de error específico, arregla el código y revalida usando la herramienta de inspección URL.
- **Sin resultados enriquecidos apareciendo después de implementación:** Los resultados enriquecidos no están garantizados. Asegúrate de que el markup sea válido, contenido sea alta calidad, y espera 2-4 semanas para indexación.
- **Usuario no técnico:** Recomienda un plugin de WordPress (Rank Math o Yoast) que maneja el schema automáticamente para la mayoría de tipos de página.
