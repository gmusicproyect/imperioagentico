---
name: calculadora-roi
description: "Construye calculadoras de ROI para decisiones de negocio con entradas de costo, proyecciones de beneficio, y análisis de período de payback. Usa cuando evalúes si una inversión de negocio vale la pena."
allowed-tools: Read Write Glob
metadata:
  author: Imperio Digital
  version: "1.0"
---

# Calculadora de ROI

## Cuándo Usar Este Skill

Usa este skill cuando necesites:
- Calcular el retorno sobre inversión para una decisión de negocio
- Comparar múltiples opciones de inversión usando el mismo marco
- Determinar período de payback para una nueva herramienta, contratación, o iniciativa
- Construir un caso de negocio con justificación financiera

**NO** uses este skill para ROI del mercado de valores, análisis de inversión personal, o modelado financiero general. Esto es para decisiones de inversión operativa de negocio.

---

## Principio Fundamental

EL ROI ES UNA HERRAMIENTA DE DECISIÓN — EL OBJETIVO NO ES PRECISIÓN SINO CLARIDAD SOBRE SI UNA INVERSIÓN VALE LA PENA HACER Y CUÁNTO TIEMPO HASTA QUE SE PAGUE A SÍ MISMA.

---

## Fase 1: Contexto de Inversión

### Información Requerida

| Entrada | Qué Preguntar | Por Defecto |
|---------|---------------|------------|
| **Descripción de inversión** | "¿En qué estás considerando invertir? (herramienta, contratación, campaña, equipo)" | No hay predeterminado — debe proporcionarse |
| **Costo total** | "¿Cuál es el costo total? (upfront + ongoing mensual/anual)" | No hay predeterminado — debe proporcionarse |
| **Horizonte de tiempo** | "¿Sobre qué período debo medir ROI? (6 meses, 1 año, 2 años)" | 12 meses |
| **Beneficios esperados** | "¿Qué esperas ganar? (ingresos, tiempo ahorrado, reducción de costos)" | No hay predeterminado — debe proporcionarse |
| **Línea base actual** | "¿Cuál es el estado actual sin esta inversión?" | No hay predeterminado — describe proceso/costo actual |

**PUNTO DE CONTROL: No procedas sin el costo de inversión y beneficios esperados.**

---

## Fase 2: Análisis de Costos

```
## Desglose de Costo de Inversión

### Costos Iniciales
| Artículo | Costo | Notas |
|------|------|-------|
| [Honorario de compra/configuración] | $[X] | Una sola vez |
| [Implementación/capacitación] | $[X] | Una sola vez |
| [Costos de migración/conmutación] | $[X] | Una sola vez |
| **Total Inicial** | **$[X]** | |

### Costos Continuos (Mensual)
| Artículo | Costo Mensual | Costo Anual |
|------|-------------|-------------|
| [Suscripción/licencia] | $[X] | $[X] |
| [Mantenimiento/soporte] | $[X] | $[X] |
| [Mano de obra adicional] | $[X] | $[X] |
| **Total Mensual** | **$[X]** | **$[X]** |

### Costo Total de Propiedad ([X]-Mes Horizonte)
| | Cantidad |
|--|--------|
| Costos iniciales | $[X] |
| + Costos continuos ([X] meses) | $[X] |
| **= Inversión total** | **$[X]** |
```

---

## Fase 3: Cuantificación de Beneficio

```
## Análisis de Beneficio

### Beneficios de Ingresos
| Beneficio | Valor Mensual | Valor Anual | Confianza |
|---------|-------------|-------------|------------|
| [Nuevos ingresos habilitados] | $[X] | $[X] | Alto/Med/Bajo |
| [Aumento de ingresos de eficiencia] | $[X] | $[X] | Alto/Med/Bajo |

### Ahorros de Costos
| Beneficio | Ahorros Mensual | Ahorros Anual | Confianza |
|---------|----------------|----------------|------------|
| [Herramienta/servicio reemplazado] | $[X] | $[X] | Alto |
| [Costos de mano de obra reducidos] | $[X] | $[X] | Med |

### Ahorros de Tiempo
| Tarea | Horas Ahorradas/Mes | Valor (hrs x tasa) | Valor Anual |
|------|------------------|-------------------|-------------|
| [Tarea 1] | [X] hrs | $[X] | $[X] |
| [Tarea 2] | [X] hrs | $[X] | $[X] |

### Beneficios Totales
| Categoría | Mensual | Anual |
|----------|---------|--------|
| Beneficios de ingresos | $[X] | $[X] |
| Ahorros de costos | $[X] | $[X] |
| Valor de ahorro de tiempo | $[X] | $[X] |
| **Beneficios totales** | **$[X]** | **$[X]** |
```

---

## Fase 4: Cálculo de ROI y Decisión

```
## Resumen de ROI

### Métricas Principales
| Métrica | Valor |
|--------|-------|
| Inversión total ([X] meses) | $[X] |
| Beneficios totales ([X] meses) | $[X] |
| Retorno neto | $[X] |
| **Porcentaje de ROI** | **[X]%** |
| Período de payback | [X] meses |
| Beneficio neto mensual (después payback) | $[X] |

### Fórmula de ROI
ROI = (Beneficios Totales - Inversión Total) / Inversión Total x 100

### Marco de Decisión
| Rango de ROI | Recomendación |
|-----------|---------------|
| Más de 200% | Fuerte sí — invierte inmediatamente |
| 100-200% | Sí — retorno sólido, procede |
| 50-100% | Probablemente sí — si alineación estratégica existe |
| 0-50% | Quizás — considera alternativas |
| Negativo | No — a menos que beneficios intangibles lo justifiquen |

### Recomendación
[Recomendación clara basada en números con advertencias clave]
```

---

## Ejemplo: Contratar un Asistente Virtual

**Inversión:** $2,000/mes ($24,000/año). **Beneficios:** Ahorra fundador 40 horas/mes de trabajo administrativo valuado a $100/hr = $4,000/mes en tiempo recapturado. Más $500/mes en tareas hechas mejor (gestión de bandeja de entrada reduciendo oportunidades perdidas).

**ROI:** ($54,000 - $24,000) / $24,000 = 125% ROI anual. Payback: Inmediato — positivo neto desde mes 1.

---

## Anti-Patrones

- **Solo contar retornos de dólar duro** — ahorros de tiempo y costo de oportunidad son beneficios reales. Cuantifícalos.
- **Ignorar costos de conmutación** — migración, capacitación, y pérdida de productividad durante transición son costos reales
- **Proyecciones de beneficio sobreconfiadas** — usa estimaciones conservadoras. Si ROI funciona en números conservadores, definitivamente funciona en práctica.
- **Comparar contra hacer nada** — a veces la alternativa no es "no hacer nada" sino "hacer algo diferente." Compara contra la mejor alternativa.
- **Horizonte de tiempo infinito** — siempre establece período definido. Una inversión que toma 5 años para payback en una herramienta que puedes reemplazar en 2 años es mala oferta.

---

## Recuperación

- **Beneficios difíciles de cuantificar:** Asigna valor dólar conservador a beneficios intangibles. "Mejor experiencia de cliente" = churn reducido = $X ingresos retenidos.
- **Múltiples opciones para comparar:** Construye tabla de comparación lado-a-lado con ROI para cada opción. Recomienda ROI más alto con riesgo aceptable.
- **ROI es negativo pero se siente necesario:** Identifica el beneficio mínimo necesario para equilibrar y evalúa si es alcanzable. Algunas inversiones son estratégicas incluso con ROI de corto plazo negativo.
- **Sin datos de línea base:** Estima el costo actual del problema siendo resuelto. Rastrea 2-4 semanas si es posible antes de hacer la inversión.
