---
name: analisis-precios
description: "Analiza la efectividad de precios con estimaciones de elasticidad, comparación competitiva, percepción de valor y recomendaciones de optimización. Usa cuando evalúes o ajustes tus precios."
allowed-tools: Read Write Glob
metadata:
  author: Imperio Digital
  version: "1.0"
---

# Análisis de Precios

## Cuándo Usar Este Skill

Usa este skill cuando necesites:
- Evaluar si tu precio actual es óptimo
- Comparar tus precios contra competidores
- Analizar el impacto de un cambio de precio antes de implementarlo
- Diseñar una estructura de precios (tiers, bundles, freemium)

**NO** uses este skill para modelado financiero, pronóstico de ingresos, o contabilidad de costos. Esto es para análisis y optimización de estrategia de precios.

---

## Principio Fundamental

PRECIO BASADO EN VALOR ENTREGADO, NO EN COSTO INCURRIDO — TU PRECIO DEBE REFLEJAR LO QUE EL CLIENTE GANA, NO LO QUE TE CUESTA ENTREGAR.

---

## Fase 1: Resumen

### Información Requerida

| Entrada | Qué Preguntar | Por Defecto |
|---------|---------------|------------|
| **Producto/servicio** | "¿Qué estás cotizando?" | Debe proporcionarse |
| **Precio actual** | "¿Qué cobras ahora?" | Debe proporcionarse |
| **Modelo de precios** | "¿Una sola vez, suscripción, por unidad, tiered, basado en uso?" | Debe proporcionarse |
| **Competidores** | "¿Quiénes son tus 3 principales competidores y qué cobran?" | Investigaré |
| **Feedback de clientes** | "¿Han comentado los clientes sobre precio? (muy alto, justo, pagarían más)" | Sin feedback directo |
| **Objetivo** | "¿Qué optimizas? (ingresos, volumen, cuota de mercado, margen)" | Maximización de ingresos |

**PUNTO DE CONTROL: Confirma el resumen antes de proceder.**

---

## Fase 2: Analizar

### Marco de Análisis

1. **Posicionamiento competitivo** — dónde estás en relación a competidores (premium, mid-market, budget)
2. **Alineación de métrica de valor** — ¿tu precio se escala con el valor que los clientes reciben?
3. **Indicadores de sensibilidad de precio** — señales de tasas de conversión, objeciones, o datos de win/loss
4. **Estimación de disposición a pagar** — Van Westendorp u marco comparable
5. **Análisis de margen** — margen bruto a precio actual y alternativas propuestas

### Tabla de Comparación Competitiva

| Competidor | Precio | Modelo | Diferenciador Clave |
|-----------|--------|--------|-------------------|
| Competidor A | $X/mes | Suscripción | Característica X |
| Competidor B | $Y única | De Por Vida | Acceso a comunidad |
| Tú | $Z/mes | Suscripción | Tu diferenciador |

**PUNTO DE CONTROL: Presenta hallazgos y espera dirección antes de hacer recomendaciones.**

---

## Fase 3: Construir

### Entregables

**1. Reporte de Análisis de Precios**
- Comparación competitiva con mapa de posicionamiento
- Fortalezas y debilidades de precios actuales
- Evaluación de sensibilidad de precio
- Estimaciones de impacto en ingresos para cambios propuestos

**2. Recomendaciones de Precios**
- 2-3 opciones de precios con resultados proyectados
- Recomendaciones de estructura de tiers (si aplica)
- Sugerencias de bundling o empaque
- Enfoque de implementación (grandfathering existentes, fase gradual, inmediato)

**3. Modelo de Impacto de Cambio de Precio**
- Tabla de escenarios: precio x volumen estimado = ingresos proyectados
- Escenarios conservador, base y optimista
- Análisis de punto de equilibrio: cuántos clientes puedes perder antes de que el aumento te duela

**4. Plan de Comunicación**
- Cómo anunciar cambios de precio a clientes existentes
- Marco de mensajería que lidera con valor, no costo
- Recomendaciones de política grandfathered
- FAQ para equipo que enfrenta al cliente

---

## Fase 4: Pulir

### Recomendaciones de Prueba

- A/B prueba precio si el tráfico lo permite
- Ofrece nuevo precio a clientes nuevos primero, mantén existentes en plan actual
- Encuesta 10 clientes con "¿Pagarías $X por esto?" antes de comprometerte

### Cadencia de Revisión

Reevalúa precios cada 6-12 meses a medida que cambian valor entregado, costos y panorama competitivo.

---

## Ejemplo 1: Producto SaaS ($29/mes, considerando aumento)

**Hallazgo:** Los competidores cobran $39-$79/mes por características similares. El precio actual señala "herramienta básica" no "solución premium."
**Recomendación:** Aumenta a $49/mes para clientes nuevos, grandfathered existentes a $29 por 12 meses. Esperado: 10% caída de volumen, 55% aumento de ingresos.

## Ejemplo 2: Producto Digital ($97 única, considerando tiers)

**Hallazgo:** Precio único fuerza compradores conscientes del presupuesto y premium en la misma opción.
**Recomendación:** Tres tiers — Básico ($67), Estándar ($127), Premium ($247) — con diferenciación clara de características. Aumento esperado de ingresos: 30% del capture de upsell.

---

## Anti-Patrones

- **Precio cost-plus** — agregar margen a tus costos ignora lo que los clientes valoran. Un curso que cuesta $50 hacer puede valer $500 al comprador.
- **Coincidencia de competidor** — precios al mismo nivel sin diferenciación es una carrera al fondo. El precio refleja posicionamiento.
- **Miedo a aumentar precios** — la mayoría de negocios subestiman precio. Si nadie se queja de tu precio, probablemente es muy bajo.
- **Un precio para todos** — diferentes segmentos tienen diferente disposición a pagar. Tiers o paquetes capturan más valor.
- **Cambiar precio sin comunicar valor** — un aumento sin valor reforzado se siente como un cash grab. Siempre lidera con valor.

---

## Recuperación

- **Sin datos de competidor:** Usa benchmarks de industria, productos comparables en categorías adyacentes, o encuestas de disposición a pagar del cliente.
- **Usuario asustado de aumentar precios:** Comienza con clientes nuevos solamente. Grandfathered existentes para reducir riesgo. Prueba aumentos pequeños primero.
- **Clientes ya dicen que el precio es muy alto:** Investiga si es un problema de precio o un problema de comunicación de valor. Frecuentemente la landing page es el problema, no el precio.
- **Precios genuinamente complejos:** Simplifica primero. Si no puedes explicar tus precios en 10 segundos, los clientes no pueden evaluarlos.