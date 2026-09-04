---
name: calculadora-gasto-ad
description: "Calcula presupuestos de gasto en ads basándote en objetivos de ingresos, tasas de conversión y objetivos de costo-por-adquisición. Úsalo cuando planees cuánto gastar en ads para alcanzar metas de ingresos."
allowed-tools: Read Write Glob
metadata:
  author: Imperio Digital
  version: "1.0"
---

# Calculadora de Gasto en Ads

## Cuándo Usar Este Skill

Usa este skill cuando necesites:
- Calcular cuánto gasto en ads es necesario para alcanzar una meta de ingresos
- Determinar objetivos CPA viables basándote en márgenes de producto
- Construir un plan de asignación de presupuesto en plataformas y campañas
- Modelar diferentes escenarios de gasto para encontrar el nivel óptimo de inversión

**NO USES** este skill para presupuestos de marketing orgánico, presupuestación general de negocio, o estrategia de creative de ad. Esto es específicamente para calcular presupuestos de publicidad pagada.

---

## Principio Fundamental

EL GASTO EN ADS ES UNA ECUACIÓN DE INVERSIÓN — CADA DÓLAR QUE ENTRA DEBE PRODUCIR UN RETORNO MEDIBLE, Y LAS MATEMÁTICAS DEBEN FUNCIONAR ANTES DEL PRIMER DÓLAR GASTADO.

---

## Fase 1: Inputs

### Inputs Requeridos

| Input | Qué Preguntar | Default |
|-------|---------------|---------|
| **Meta de ingresos** | "¿Cuál es tu meta de ingresos mensual de ads?" | Sin default — debe ser proporcionado |
| **Valor promedio de orden (AOV)** | "¿Cuál es el valor promedio de venta u orden?" | Sin default — debe ser proporcionado |
| **Margen de ganancia** | "¿Cuál es tu margen de ganancia por venta (después de COGS)?" | 60% |
| **Tasa de conversión actual** | "¿Qué porcentaje de clics de ad se convierten en ventas?" | 2% (promedio de industria) |
| **CPC actual** | "¿Cuál es tu costo promedio por clic?" | $1.50 (estimado) |
| **Plataformas de ad** | "¿Dónde estás ejecutando ads?" | Meta + Google |

**PUNTO DE CONTROL: No procedas sin meta de ingresos y AOV.**

---

## Fase 2: Cálculos Principales

### Matemáticas del Funnel

```
## Calculadora de Gasto en Ads

### Inputs
- Meta de ingresos mensual: $[X]
- Valor promedio de orden: $[X]
- Margen de ganancia: [X]%
- Tasa de conversión: [X]%
- CPC promedio: $[X]

### Métricas Calculadas

| Métrica | Valor | Fórmula |
|---------|-------|---------|
| Ventas necesarias | [X] | Meta de ingresos / AOV |
| Clics necesarios | [X] | Ventas necesarias / Tasa de conversión |
| Gasto en ads requerido | $[X] | Clics necesarios x CPC |
| Costo por adquisición (CPA) | $[X] | Gasto en ads / Ventas necesarias |
| CPA máximo viable | $[X] | AOV x Margen de ganancia |
| ROAS necesario | [X]x | Meta de ingresos / Gasto en ads |
| Ganancia después de gasto en ads | $[X] | Ingresos - COGS - Gasto en ads |
```

### Checklist de Viabilidad

Alerta automáticamente estos:
- CPA excede 50% de AOV — advertencia: márgenes apretados
- CPA excede margen de ganancia — alerta: perdiendo dinero en cada venta
- ROAS requerido excede 5x — alerta: muy agresivo, puede no ser alcanzable
- Gasto mensual excede $10K — nota: recomienda escalado por fases

---

## Fase 3: Modelado de Escenarios

Presenta 3 escenarios para que el usuario elija su nivel de riesgo.

```
## Escenarios

### Conservador (Menor gasto, solo canales probados)
| Métrica | Valor |
|---------|-------|
| Gasto mensual | $[X] |
| Ventas esperadas | [X] |
| Ingresos esperados | $[X] |
| ROAS esperado | [X]x |
| Ganancia después de ads | $[X] |

### Caso Base (Gasto moderado, enfoque balanceado)
| Métrica | Valor |
|---------|-------|

### Agresivo (Mayor gasto, modo escalado)
| Métrica | Valor |
|---------|-------|
```

### Asignación por Plataforma

```
## Asignación de Presupuesto por Plataforma

| Plataforma | % del Presupuesto | Gasto Mensual | ROAS Esperado | Lógica |
|----------|------------------|---------------|--------------|--------|
| Meta | [X]% | $[X] | [X]x | [Por Qué] |
| Google | [X]% | $[X] | [X]x | [Por Qué] |
| [Otro] | [X]% | $[X] | [X]x | [Por Qué] |
```

---

## Fase 4: Plan de Acción

### Calendario de Presupuesto Mensual

```
## Plan de Gasto Mensual

Semana 1: $[X] — Fase de prueba (3-5 ad sets, $X/día cada una)
Semana 2: $[X] — Evalúa, pausa bajo-desempeño
Semana 3: $[X] — Escala ganadores, aumenta presupuestos diarios
Semana 4: $[X] — Mantén y optimiza

Total: $[X]
```

### Checklist de Punto de Equilibrio

```
- [ ] CPA está bajo el máximo viable CPA ($[X])
- [ ] ROAS excede punto de equilibrio ([X]x)
- [ ] Presupuesto diario soporta significancia estadística ($[X]/día mínimo)
- [ ] Tracking de conversión está instalado y verificado
- [ ] Tasa de conversión de landing page está en o arriba [X]%
```

---

## Ejemplo: Creador de Curso (Meta de $10K/mes)

**Inputs:** AOV = $197, margen = 85%, tasa de conversión = 3%, CPC = $2.00

**Resultados:**
- Ventas necesarias: 51/mes
- Clics necesarios: 1,700
- Gasto requerido: $3,400/mes
- CPA: $66.70
- CPA máximo viable: $167.45 (rentable en CPA actual)
- ROAS: 2.94x
- Ganancia después de ads: $5,117/mes

**Veredicto:** Las matemáticas funcionan bien. CPA es 40% del CPA máximo viable — hay espacio para escalar.

---

## Anti-Patrones

- **Ignorar margen de ganancia** — el ROAS de ingresos no significa nada sin contexto de margen. Un ROAS de 3x en márgenes de 20% es punto de equilibrio.
- **Usar tasas de conversión promedio de industria sin pruebas** — siempre nota que los defaults son estimados. Los datos reales reemplazan suposiciones.
- **Calcular sin incluir todos los costos** — incluye tarifas de plataforma, costos de creative, herramientas de landing page, y tiempo de equipo.
- **Suposiciones de escalado lineal** — duplicar el gasto raramente duplica resultados. Factoriza retornos decrecientes en niveles de gasto más altos.
- **Sin checklist de presupuesto diario mínimo** — las plataformas necesitan $20-50/día mínimo por ad set para optimizar. Si el presupuesto no lo soporta, reduce ad sets.

---

## Recuperación

- **Las matemáticas no funcionan (CPA > margen):** Muestra al usuario qué palanca tirar — aumenta AOV, mejora tasa de conversión, baja CPC, o añade upsells/LTV para cambiar la ecuación.
- **Sin datos históricos:** Usa benchmarks de industria pero etiquétalos claramente como estimados. Recomienda un presupuesto de prueba de $500-1,000 antes de comprometer el gasto calculado completo.
- **Múltiples productos en diferentes puntos de precio:** Calcula por separado para cada producto, luego crea una vista de portafolio combinada.
- **Meta de ingresos parece poco realista:** Muestra el gasto requerido y deja que el usuario decida. Si requiere un ROAS arriba de 5x sin datos históricos, señala el riesgo explícitamente.
