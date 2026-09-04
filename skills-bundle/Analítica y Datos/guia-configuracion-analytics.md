---
name: guia-configuracion-analytics
description: "Planifica la implementación de analítica web con seguimiento de eventos, objetivos, configuración de conversión y configuración de dashboard. Utiliza cuando configures Google Analytics o herramientas similares desde cero."
allowed-tools: Read Write Glob
metadata:
  author: Imperio Digital
  version: "1.0"
---

# Guía de Configuración de Analytics

## Cuándo Usar Este Skill

Utiliza este skill cuando necesites:
- Configurar Google Analytics (GA4) u otra plataforma de analítica web desde cero
- Planificar seguimiento de eventos para un sitio web o aplicación web
- Definir objetivos y seguimiento de conversión para un negocio
- Diseñar dashboards de analítica que impulsen decisiones

**NO** utilices este skill para analítica de redes sociales, analítica de email marketing o dashboards de reporteo financiero. Esto es para implementación de analítica web y aplicación web.

---

## Principio Fundamental

RASTREA LO QUE ACTUARÁS — CADA EVENTO Y OBJETIVO DEBE CONECTAR A UNA DECISIÓN DE NEGOCIO O ES RUIDO.

---

## Fase 1: Brief

### Entradas Requeridas

| Entrada | Qué Preguntar | Por Defecto |
|---------|--------------|------------|
| **Tipo de sitio web** | "¿Qué tipo de sitio? (e-commerce, SaaS, blog, generación de leads, portfolio)" | Sitio de generación de leads |
| **Plataforma** | "¿Qué herramienta de analítica? (GA4, Plausible, Mixpanel, Amplitude)" | Google Analytics 4 |
| **Objetivos de negocio** | "¿Cuáles son tus 3 objetivos principales que este sitio debería impulsar?" | Leads, ventas, engagement |
| **Configuración actual** | "¿Tienes alguna analítica instalada ya?" | Ninguna — comenzando desde cero |
| **Tech stack** | "¿En qué está construido tu sitio? (WordPress, Shopify, personalizado, etc.)" | WordPress |
| **Páginas clave** | "¿Qué páginas importan más? (inicio, precios, registro, checkout)" | Inicio, precios, contacto |

**PUNTO DE CONTROL:** Confirma el brief antes de continuar.

---

## Fase 2: Planificar

### Estructura del Plan de Seguimiento

1. **Seguimiento a nivel de página** — qué pageviews importan y por qué
2. **Seguimiento de eventos** — acciones del usuario a capturar (clics, envíos de formulario, scrolls, reproducción de video)
3. **Objetivos de conversión** — definiciones de conversión primaria y secundaria
4. **Dimensiones personalizadas** — propiedades del usuario vale la pena segmentar
5. **Estrategia UTM** — convenciones de etiquetado de campaña para fuentes de tráfico
6. **Diseño de dashboard** — qué reportes construir y consultar semanalmente

### Convención de Nombres de Eventos

Usa un esquema consistente: `categoria_accion_etiqueta`
- `cta_click_hero` — botón CTA de sección hero clicked
- `form_submit_contact` — formulario de contacto enviado
- `page_scroll_50` — usuario se desplazó 50% de página

**PUNTO DE CONTROL:** Presenta el plan de seguimiento y espera aprobación.

---

## Fase 3: Construir

### Entregables

**1. Hoja de Cálculo Completa del Plan de Seguimiento**
- Cada evento con nombre, disparador, parámetros y propósito de negocio
- Objetivos de conversión con asignaciones de valor
- Convención de nombres UTM con ejemplos

**2. Guía de Implementación**
- Instrucciones paso a paso de configuración para la plataforma elegida
- Configuración de Tag Manager (si aplica)
- Fragmentos de código para eventos personalizados
- Checklist de prueba para verificar que cada evento se dispara correctamente

**3. Blueprinto de Dashboard**
- Widgets y métricas recomendadas por sección de dashboard
- Dashboard de descripción general: tráfico, conversiones, páginas principales, fuentes
- Dashboard de adquisición: desglose de canal, desempeño de campaña
- Dashboard de comportamiento: engagement, profundidad de scroll, mapas de clics

**4. Plantilla de Seguimiento UTM**
- Plantilla de hoja de cálculo para generar parámetros UTM consistentes
- Convenciones de nombres para fuente, medio, campaña, contenido, término

---

## Fase 4: Pulir

### Checklist de Revisión Semanal

- Verifica tasas de conversión vs. semana anterior
- Revisa fuentes de tráfico principales y cualquier anomalía
- Verifica que el seguimiento de eventos siga disparándose (sin etiquetas rotas)
- Nota cualquier brecha de datos o patrón inesperado

### Auditoría Post-Lanzamiento de 30 Días

Después de 30 días de recopilación de datos, revisa: ¿Se disparan todos los eventos? ¿Son precisos los objetivos de conversión? ¿Los datos responden preguntas de negocio?

---

## Ejemplo 1: Sitio Web de Generación de Leads (WordPress, GA4)

**Eventos clave:** Clics de CTA (3 ubicaciones), envío de formulario de contacto, visita a página de precios, scroll de blog post 75%
**Conversiones:** Primaria = envío de formulario. Secundaria = visita a página de precios.
**Dashboard:** Tráfico semanal, tasa de conversión, páginas de destino principales, desglose de fuente.

## Ejemplo 2: Tienda de E-commerce (Shopify, GA4)

**Eventos clave:** Añadir al carrito, comenzar checkout, compra, visualización de producto, uso de filtro de colección
**Conversiones:** Primaria = compra. Secundaria = añadir al carrito.
**Dashboard:** Ingresos, AOV, tasa de conversión por fuente, productos principales, churn rate de carrito.

---

## Anti-Patrones

- **Rastrear todo** — 200 eventos sin plan produce parálisis de datos. Comienza con 10-15 eventos que se mapeen a decisiones de negocio.
- **Sin objetivos de conversión** — pageviews sin objetivos es métricas de vanidad. Define qué significa "éxito" para el sitio.
- **Etiquetas UTM inconsistentes** — `facebook`, `Facebook`, `fb` y `FB` son cuatro fuentes diferentes. Estandariza y documenta.
- **Nunca verificar los datos** — analítica que no revises semanalmente es tiempo de configuración desperdiciado. Construye un hábito de revisión.
- **Ignorar muestreo de datos** — GA4 muestrea datos en volúmenes altos. Sabe cuándo tus reportes están muestreados y contabilízalo.

---

## Recuperación

- **Usuario abrumado por GA4:** Comienza con 3 eventos y 1 objetivo de conversión. Añade complejidad después de que funcionan los básicos.
- **Configuración existente desordenada:** Audita etiquetas actuales, elimina duplicados, documenta qué existe, luego añade piezas faltantes.
- **Sin habilidades técnicas:** Proporciona instrucciones de Tag Manager con capturas de pantalla e instrucciones paso a paso de clics.
- **Preocupaciones de privacidad:** Recomienda configuración de consentimiento de cookie y configura la retención de datos GA4 y configuración de anonimización.