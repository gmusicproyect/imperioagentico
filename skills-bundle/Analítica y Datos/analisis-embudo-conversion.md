---
name: analisis-embudo-conversion
description: "Mapea y analiza embudos de conversión con identificación de abandono, prioridades de optimización y benchmarking. Utiliza cuando diagnostiques dónde se pierden prospectos en tu proceso de ventas."
allowed-tools: Read Write Glob
metadata:
  author: Imperio Digital
  version: "1.0"
---

# Análisis de Embudo de Conversión

## Cuándo Usar Este Skill

Utiliza este skill cuando necesites:
- Mapear tu customer journey desde conciencia hasta compra
- Identificar dónde ocurren los mayores abandonos en tu embudo
- Priorizar esfuerzos de optimización para máximo impacto de conversión
- Comparar tu desempeño de embudo contra estándares industriales

**NO** utilices este skill para diseño de prueba A/B, optimización de campaña de publicidad o gestión de pipeline de CRM. Esto es para analizar y diagnosticar desempeño de embudo.

---

## Principio Fundamental

ARREGLA LA FUGA MÁS GRANDE PRIMERO — UNA MEJORA DE 10% EN EL PEOR PUNTO DE ABANDONO SUPERA UNA MEJORA DE 50% EN UN PASO QUE YA CONVIERTE BIEN.

---

## Fase 1: Brief

### Entradas Requeridas

| Entrada | Qué Preguntar | Por Defecto |
|---------|--------------|------------|
| **Tipo de embudo** | "¿Qué embudo? (sitio web, checkout de e-commerce, registro SaaS, pipeline de ventas)" | Embudo de lead de sitio web |
| **Etapas de embudo** | "Enumera cada paso desde la primera visita hasta la conversión final." | Debe proporcionarse |
| **Datos actuales** | "¿Tienes números para cada etapa? (visitantes, leads, pruebas, compras)" | Debe proporcionarse o estimarse |
| **Período de tiempo** | "¿Qué período de tiempo cubren los datos?" | Últimos 30 días |
| **Objetivo** | "¿Qué tasa de conversión estás buscando para el embudo completo?" | Punto de referencia industrial |
| **Problemas conocidos** | "¿Hay etapas que ya sospechas están bajo desempeño?" | Desconocido |

**PUNTO DE CONTROL:** Confirma el brief y los datos antes de continuar.

---

## Fase 2: Mapear

### Visualización de Embudo

Construye un embudo etapa por etapa con:
- **Volumen** en cada etapa (números absolutos)
- **Tasa de conversión** entre cada etapa
- **Tasa de abandono** en cada etapa (inversa de conversión)
- **Conversión acumulativa** de arriba a abajo

### Comparación de Punto de Referencia

Proporciona puntos de referencia relevantes por etapa:

| Tipo de Embudo | Etapa | Conversión Típica |
|-------------|-------|-------------------|
| Generación de lead de sitio web | Visita → Lead | 2-5% |
| SaaS | Registro → Prueba activa | 40-60% |
| SaaS | Prueba → Pago | 15-25% |
| E-commerce | Visita → Añadir al carrito | 8-12% |
| E-commerce | Carrito → Compra | 40-65% |

**PUNTO DE CONTROL:** Presenta el mapa del embudo y confirma precisión antes de analizar.

---

## Fase 3: Analizar

### Entregables

**1. Reporte de Desempeño de Embudo**
- Tasas de conversión y abandono etapa por etapa
- Comparación a puntos de referencia: arriba, en o debajo de industria
- La "fuga más grande" — la etapa con mayor oportunidad absoluta

**2. Diagnóstico de Abandono**
Para cada etapa bajo desempeño, diagnostica causas probables:
- **Visita → Lead:** CTA débil, proposición de valor unclear, tiempo de carga lento
- **Lead → Calificado:** Orientación pobre, expectativas no coinciden, sin nutrición
- **Calificado → Cierre:** Fricción de precio, falta de urgencia, fortaleza de competidor
- Proporciona 3-5 hipótesis por etapa bajo desempeño

**3. Matriz de Prioridad de Optimización**
| Etapa | Churn Rate | Potencial de Mejora | Esfuerzo | Prioridad |
|-------|--------------|-----------------|--------|----------|
| Carrito → Checkout | 65% | Alto | Bajo | 1 |
| Visita → Registro | 97% | Medio | Medio | 2 |

**4. Plan de Acción**
- Top 3 arreglos clasificados por relación impacto-esfuerzo
- Recomendaciones específicas para cada arreglo
- Plan de medición: cómo verificar que el arreglo funcionó

---

## Fase 4: Pulir

### Especificación de Dashboard de Monitoreo

Recomienda un simple dashboard de embudo con:
- Tasas de conversión etapa por etapa semanales
- Líneas de tendencia para detectar degradación temprano
- Umbrales de alerta para cada etapa

### Cadencia de Revisión

- Semanal: verificación rápida de salud del embudo
- Mensual: análisis completo con superposiciones de segmento
- Trimestral: revisión de rediseño de embudo — ¿siguen siendo correctas las etapas?

---

## Ejemplo 1: Embudo de Prueba Gratuita de SaaS

**Etapas:** Visita Sitio Web → Registro → Prueba Activa → Funcionalidad Activada → Pago
**Hallazgo clave:** Abandono 70% entre Registro y Prueba Activa — onboarding roto
**Arreglo superior:** Reduce tiempo de registro a valor con flujo de onboarding guiado

## Ejemplo 2: Embudo de Compra de E-commerce

**Etapas:** Visita → Visualización de Producto → Añadir al Carrito → Checkout → Compra
**Hallazgo clave:** Abandono de carrito 55% — por encima del punto de referencia de 35%
**Arreglo superior:** Añade insignias de confianza, simplifica checkout, implementa email de abandono de carrito

---

## Anti-Patrones

- **Optimizar la parte superior cuando la parte inferior gotea** — duplicar tráfico a una página de checkout rota duplica la frustración, no los ingresos. Arregla la parte inferior primero.
- **Ignorar números absolutos** — una tasa de conversión 50% en 10 visitantes es 5 clientes. A veces el problema es volumen, no tasa.
- **Obsesión con métrica única** — la tasa de conversión general enmascara problemas específicos de etapa. Siempre desglosa por etapa.
- **Benchmarking sin contexto** — una tasa de conversión de sitio web 1% podría ser excelente para bienes de lujo y terrible para una herramienta gratuita. Usa puntos de referencia relevantes.
- **Analizar sin segmentar** — móvil vs. escritorio, nuevo vs. recurrente, y embudos específicos de canal a menudo cuentan historias muy diferentes.

---

## Recuperación

- **Sin datos de embudo disponibles:** Ayuda a definir las etapas y configura seguimiento básico. Proporciona un plan de recopilación de datos de 30 días antes del análisis.
- **Etapas de embudo unclear:** Mapea el customer journey desde su perspectiva, no el proceso interno. Pregunta "¿Qué HACE el cliente en cada paso?"
- **Todo se ve mal:** Prioriza sin piedad. Elige la única etapa con el mayor impacto absoluto y comienza ahí.
- **El usuario quiere rediseñar el embudo completo:** Optimiza el embudo existente primero. Rediseña solo después de agotar ganancias rápidas.