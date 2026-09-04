---
name: plan-arquitectura-sitio
description: Planifica arquitectura de sitio web con estructura de URL, categorización de contenido, flujo de enlazado interno y jerarquía. Usa cuando diseñes nuevo sitio o reorganices existente.
allowed-tools: Read Write Glob
author: Imperio Digital
version: "1.0"
---

# Plan de Arquitectura de Sitio

## Cuándo Usar Este Skill

Usa este skill cuando necesites:
- Diseñar la estructura de un sitio nuevo
- Reorganizar la arquitectura de un sitio existente
- Planificar la estructura de URL para SEO
- Crear una jerarquía de contenido clara

---

## Principio Fundamental

LA ARQUITECTURA DE SITIO CLARA AYUDA A USUARIOS Y BUSCADORES A ENTENDER LA JERARQUÍA DE CONTENIDO — MEJOR ARQUITECTURA SIGNIFICA MEJOR INDEXACIÓN Y RANKING.

---

## Estructura de Carpeta Típica

```
/
├── / (Homepage)
├── /blog/
│   ├── /blog/[category]/
│   └── /blog/[post-slug]/
├── /services/ (o /products/)
│   ├── /services/[service-1]/
│   ├── /services/[service-2]/
│   └── /services/[service-2]/faq/
├── /about/
├── /contact/
├── /privacy/
└── /sitemap.xml
```

---

## Directorios de Contenido

### Nivel 1: Categorías Principales

Máximo 5-7 categorías principales (fácil de navegar):
- Blog/Resources
- Services/Products
- About/Company
- Contact
- Legal/Privacy

### Nivel 2: Subcategorías

Dentro de cada categoría principal, crea subcategorías lógicas:
- /services/web-design/
- /services/seo/
- /services/content-marketing/

### Nivel 3: Contenido Individual

Mantén URLs cortas y descriptivas:
- /blog/seo-guide/ (NO /blog/2024/01/15/my-seo-guide/)
- /products/weight-loss-supplement/ (NO /products/supplements/weight/fat-loss/product-123/)

---

## Breadcrumb Navigation

Crea breadcrumbs para claridad:
```
Home > Services > Web Design > Responsive Design Guide

La estructura de URL debería reflejar:
/services/web-design/responsive-design-guide/
```

---

## Planificación de Contenido

```
## Mapa de Contenido

| Sección | Propósito | Tipo | URLs Esperadas |
|---------|----------|------|-----------------|
| Blog | Traffic/SEO | Artículos | 20-50 posts |
| Servicios | Conversión | Landing pages | 5-10 servicios |
| Recursos | Lead magnet | Descargas/Guías | 3-5 recursos |
| FAQ | Conversión | FAQ pages | 1-2 páginas |
```

---

## Mejores Prácticas

1. **Estructura Plana es Mejor:** Máximo 3 niveles profundos
2. **Keywords en URLs:** /services/keyword/ es mejor que /s/1234/
3. **Breadcrumbs:** Implementa en todas las páginas (HTML + Schema)
4. **Sitemap.xml:** Genera automáticamente con CMS
5. **Robots.txt:** Controla qué se indexa

---

## Anti-Patrones

- **URLs demasiado profundas:** /company/about/team/leadership/bio/ es demasiado hondo
- **Parámetros innecesarios en URLs:** /products?id=123&lang=en es pobre para SEO
- **Cambiar estructura sin redirecciones:** Migraciones sin 301s pierden tráfico
- **Demasiadas categorías:** Más de 7-10 hace navegación confusa

---

## Recuperación

- **Sitio existente con estructura pobre:** Planifica migración gradual a nueva arquitectura. No cambies todo de una vez.
- **Contenido duplicado por mala estructura:** Implementa canonicals o consolida contenido.
- **Páginas profundas no rankean:** Promueve con enlaces internos de homepage. Considera mover a nivel 2.
