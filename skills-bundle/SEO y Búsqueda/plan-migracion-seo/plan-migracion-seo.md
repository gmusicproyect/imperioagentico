---
name: plan-migracion-seo
description: Planifica migraciones de sitio web con mapeo de redirección 301, análisis de tráfico y estrategia de preservación de SEO. Usa cuando muevas, rediseñes o cambies CMS tu sitio.
allowed-tools: Read Write Glob
author: Imperio Digital
version: "1.0"
---

# Plan de Migración de SEO

## Cuándo Usar Este Skill

Usa este skill cuando:
- Cambies dominio o CMS
- Rediseñes tu sitio web
- Consolidar múltiples sitios en uno
- Recolectar contenido duplicado en una versión canónica

---

## Principio Fundamental

UNA MIGRACIÓN DE SITIO MAL PLANIFICADA PUEDE PERDER 80% DEL TRÁFICO ORGÁNICO. PLANIFICACIÓN CUIDADOSA CON REDIRECCIONES 301 Y MAPEO PRESERVA LA AUTORIDAD.

---

## Fases Clave

### Fase 1: Auditoría Pre-Migración

Crea un inventario completo:
- URLs actuales y su estructura
- Conteos de tráfico por página (últimos 6 meses)
- Palabras clave rankeadas por página
- Backlinks (dominios refirientes)
- Meta tags y estructura de encabezados

### Fase 2: Mapeo de Redirección 301

Crea mapeo URL antigua → nueva URL:

```
## Mapeo de Redirección

| URL Antigua | URL Nueva | Tipo de Redirección | Notas |
|-------------|-----------|-----------------|-------|
| /old-page | /new-page | 301 | Migración de página |
| /blog/post-1 | /resources/post-1 | 301 | Reubicación de estructura |
| /product-a | /products/category/product-a | 301 | Reorganización de categoría |
```

### Fase 3: Implementación Pre-Migración

1. Actualiza robots.txt para permitir indexación de nuevas URLs
2. Actualiza XML sitemap
3. Verifica todos los enlaces internos apuntan a nuevas URLs
4. Configura redirecciones 301 (en .htaccess, nginx, o CMS)

### Fase 4: Día de Migración

1. Implementa todos las redirecciones 301
2. Verifica que la migración es exitosa
3. Notifica a Google Search Console con herramienta de cambio de dirección
4. Monitorea tráfico por 2 semanas

### Fase 5: Post-Migración

**Semana 1-2:**
- Monitorea tráfico en Google Analytics
- Verifica que páginas nuevas indexan en Google Search Console
- Reexamina URLs en GSC para encontrar errores

**Mes 1:**
- Los rankings pueden fluctuar — es normal
- Mantén redirecciones activas por mínimo 90 días (mejor 6-12 meses)
- Actualiza backlinks internos donde sea posible

---

## Anti-Patrones

- **Eliminar redirecciones demasiado rápido** — mantenlas por mínimo 90 días, idealmente 1 año
- **No notificar a Google** — usa Google Search Console para cambio de dirección
- **Modificar estructura de URL sin redirecciones** — "Confía en que la gente encontrará contenido nuevo" pierde tráfico
- **Romper enlaces internos** — todos los enlaces internos deben apuntar a nuevas URLs, no a antiguas que redirigen

---

## Recuperación

- **Perdiste tráfico después de la migración:** Verifica que redirecciones 301 estén funcionando (no 302s). Chequea GSC para errors de indexación.
- **Algunas URLs no indexaron:** Verifica que robots.txt las permite. Envía sitemap nuevo a GSC. Espera 2-4 semanas.
- **Rankings bajaron significativamente:** Esto es temporal. Los rankings generalmente se recuperan en 4-8 semanas si la migración se hizo correctamente.
