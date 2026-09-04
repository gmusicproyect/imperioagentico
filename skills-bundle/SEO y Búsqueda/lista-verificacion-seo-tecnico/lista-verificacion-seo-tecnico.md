---
name: lista-verificacion-seo-tecnico
description: Proporciona una lista de verificación técnica de SEO para asegurar que tu sitio está optimizado para crawlabilidad, indexación y rendimiento. Usa cuando auditices o lances un nuevo sitio.
allowed-tools: Read Write Glob
author: Imperio Digital
version: "1.0"
---

# Lista de Verificación de SEO Técnico

## Cuándo Usar Este Skill

Usa este skill cuando:
- Estés lanzando un nuevo sitio
- Tu tráfico orgánico haya caído inesperadamente
- Cambies host o CMS
- Quieras asegurar que tu sitio está técnicamente optimizado

---

## Sección 1: Crawlabilidad

- [ ] robots.txt permite crawling de páginas importantes
- [ ] No hay bloqueo de JavaScript/CSS/images en robots.txt
- [ ] XML sitemap existe y es envido a Google Search Console
- [ ] Sitemap incluye todas las páginas importantes
- [ ] Internal links son correctas (no broken links)
- [ ] Redirecciones 301 configuradas correctamente (no 302s)
- [ ] Canonical tags implementadas en páginas duplicadas

---

## Sección 2: Indexación

- [ ] Google Search Console verifica el sitio
- [ ] Google Analytics está instalado
- [ ] No hay noindex tags en páginas que debería indexar
- [ ] Meta robots permiten indexación
- [ ] URL structure es rastreable (sin parámetros innecesarios)
- [ ] No hay blocked resources (JS/CSS) en Search Console

---

## Sección 3: Mobile Friendliness

- [ ] Sitio es responsive en todas las resoluciones
- [ ] Texto es legible sin zoom
- [ ] Botones/links tienen tamaño táctil (mínimo 48px)
- [ ] Sin horizontal scrolling
- [ ] Mobile Core Web Vitals pasan (LCP, FID, CLS)

---

## Sección 4: Velocidad de Página

- [ ] Largest Contentful Paint (LCP) < 2.5 segundos
- [ ] First Input Delay (FID) < 100ms
- [ ] Cumulative Layout Shift (CLS) < 0.1
- [ ] Imágenes optimizadas (WebP format, comprimidas)
- [ ] CSS/JS minificado
- [ ] Caching del navegador configurado
- [ ] CDN implementado (para sitios globales)

**Herramientas para probar:**
- PageSpeed Insights
- GTmetrix
- WebPageTest

---

## Sección 5: Estructura y Seguridad

- [ ] HTTPS implementado (SSL certificate)
- [ ] URL structure es clara y consistente
- [ ] Breadcrumbs implementados (HTML + Schema)
- [ ] No hay contenido duplicado (o canonicalized correctamente)
- [ ] 404 páginas son útiles (no dejan al usuario colgado)
- [ ] 404s no indexadas (X-Robots-Tag: noindex)

---

## Sección 6: Datos Estructurados

- [ ] Schema markup implementado (JSON-LD)
- [ ] Schema válido (pasa Google Rich Results Test)
- [ ] Article schema en blog posts
- [ ] Product schema en páginas de producto
- [ ] LocalBusiness schema en homepage (si aplica)
- [ ] FAQ schema en páginas con Q&A

---

## Sección 7: Monitoreo Continuo

- [ ] Google Search Console monitoreado semanalmente
- [ ] Google Analytics rastreando conversiones
- [ ] Alertas configuradas para tráfico caído o errores de indexación
- [ ] Ranking de palabras clave rastreado (con herramienta o manualmente)
- [ ] Reportes mensuales de SEO generados

---

## Pasos de Corrección Rápida

Si tráfico cayó repentinamente:

1. **Chequea Search Console** — ¿hay errores de indexación o rastreo?
2. **Verifica robots.txt** — ¿bloqueó accidentalmente páginas importantes?
3. **Busca en Google** — `site:tudominio.com` — ¿las páginas se indexaron?
4. **Verifica canonical tags** — ¿alguna página tiene canonical a otro lugar?
5. **Chequea redireccionamientos** — ¿alguna redirect es 302 en lugar de 301?

---

## Anti-Patrones

- **robots.txt bloquea Google Analytics o Ads scripts** — esto impide que Google vea cómo se comportan usuarios
- **Usar JavaScript para contenido importante sin SSR** — Google puede no ver el contenido
- **Cambiar URLs sin redirecciones 301** — pierdes tráfico y ranking equity
- **Usar múltiples versiones de URL** — www vs non-www, http vs https, con/sin trailing slash
- **Usar parámetros para variaciones importantes** — /products?color=blue debería ser /products/blue

---

## Recuperación

- **Penalidad manual por Google** — chequea Google Search Console para mensajes. Arregla el problema y request una revisión.
- **Tráfico bajo pero no hay errores técnicos** — problema es probablemente contenido o backlinks, no técnico.
- **Indexación lenta** — submit sitemap a Search Console. Espera 2-4 semanas para indexación completa.
