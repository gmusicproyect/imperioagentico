---
name: "Análisis de Costos (COGS)"
description: "Realiza análisis de COGS (costo de bienes vendidos) y por unidad con cálculos de margen y recomendaciones de optimización. Usa cuando analices costos de productos o servicios."
allowed-tools: Read Write Glob
metadata:
  author: Imperio Digital
  version: "1.0"
---

# Análisis de Costos

## Cuándo Usar Este Skill

Usa este skill cuando necesites:
- Calcular el costo verdadero para producir y entregar un producto o servicio
- Determinar costos por unidad, márgenes brutos y márgenes de contribución
- Identificar oportunidades de reducción de costos sin sacrificar calidad
- Construir una estructura de costos para decisiones de precios o presentaciones a inversores

**NO** uses este skill para presupuestación (usa presupuesto), estrategia de precios (usa estrategia-precios), o proyecciones financieras. Esto es específicamente para entender y optimizar tu estructura de costos.

---

## Principio Fundamental

NO PUEDES OPTIMIZAR LO QUE NO HAS MEDIDO — TODO COSTO DEBE SER IDENTIFICADO, CATEGORIZADO Y ASIGNADO A UNA UNIDAD ANTES DE QUE LAS MEJORAS DE MARGEN SEAN POSIBLES.

---

## Fase 1: Inventario de Costos

### Información Requerida

| Entrada | Qué Preguntar | Por Defecto |
|---------|---------------|------------|
| **Producto/servicio** | "¿Para qué producto o servicio estamos analizando costos?" | No hay predeterminado — debe proporcionarse |
| **Precio de venta** | "¿A qué precio lo vendes?" | No hay predeterminado — debe proporcionarse |
| **Unidades vendidas mensualmente** | "¿Cuántas unidades vendes por mes?" | No hay predeterminado — debe proporcionarse |
| **Costos directos conocidos** | "¿Qué costos van directamente en hacer/entregar esto? (materiales, mano de obra, herramientas)" | No hay predeterminado — lista todos |
| **Costos generales** | "¿Cuáles son tus costos mensuales fijos de negocio? (alquiler, software, seguros)" | Estimaré si es desconocido |

**PUNTO DE CONTROL: No procedas sin el producto, precio de venta, y al menos algunos datos de costos.**

---

## Fase 2: Desglose de Costos

### Costos Directos (COGS)

```
## Análisis de Costo Directo: [Producto/Servicio]

| Componente de Costo | Costo Por Unidad | % del Precio | Notas |
|-------------------|-----------------|------------|-------|
| [Materiales crudos / suministros] | $[X] | [X]% | |
| [Mano de obra directa (horas x tasa)] | $[X] | [X]% | |
| [Honorarios de plataforma/transacción] | $[X] | [X]% | |
| [Empaque / entrega] | $[X] | [X]% | |
| [Servicios de terceros] | $[X] | [X]% | |
| **Costo Directo Total** | **$[X]** | **[X]%** | |
```

### Costos Indirectos (Asignación de Gastos Generales)

```
## Asignación de Gastos Generales

| Categoría de Gastos Generales | Costo Mensual | Por Unidad (÷ unidades mensuales) |
|------------------------------|-------------|--------------------------|
| [Software/herramientas] | $[X] | $[X] |
| [Espacio de trabajo/alquiler] | $[X] | $[X] |
| [Seguros] | $[X] | $[X] |
| [Marketing (asignado)] | $[X] | $[X] |
| [Admin/contabilidad] | $[X] | $[X] |
| **Total de Gastos Generales/Unidad** | | **$[X]** |
```

### Cálculos de Margen

```
## Análisis de Margen

| Métrica | Cantidad | Porcentaje |
|---------|----------|-----------|
| Precio de venta | $[X] | 100% |
| Costos directos (COGS) | $[X] | [X]% |
| **Ganancia bruta** | **$[X]** | **[X]%** |
| Gastos generales por unidad | $[X] | [X]% |
| **Ganancia neta por unidad** | **$[X]** | **[X]%** |

### Al Volumen Actual ([X] unidades/mes)
| Métrica | Mensual | Anual |
|--------|---------|--------|
| Ingresos | $[X] | $[X] |
| COGS Total | $[X] | $[X] |
| Ganancia bruta | $[X] | $[X] |
| Gastos generales totales | $[X] | $[X] |
| **Ganancia neta** | **$[X]** | **$[X]** |
```

---

## Fase 3: Optimización

### Oportunidades de Reducción de Costos

```
## Recomendaciones de Optimización de Costos

| Oportunidad | Costo Actual | Costo Potencial | Ahorro/Unidad | Esfuerzo |
|-----------|-------------|---------------|-------------|--------|
| [Compras al por mayor] | $[X] | $[X] | $[X] | Bajo |
| [Negociación con proveedor] | $[X] | $[X] | $[X] | Medio |
| [Automatización de procesos] | $[X] | $[X] | $[X] | Alto |
| [Sustitución de materiales] | $[X] | $[X] | $[X] | Medio |
```

### Sensibilidad de Volumen

Muestra cómo cambian los costos en diferentes volúmenes:

```
## Impacto de Volumen en Economía Unitaria

| Volumen | Costo Directo/Unidad | Gastos Generales/Unidad | Costo Total/Unidad | Margen |
|--------|-----------------|---------------|----------------|--------|
| [Actual] | $[X] | $[X] | $[X] | [X]% |
| [2x actual] | $[X] | $[X] | $[X] | [X]% |
| [5x actual] | $[X] | $[X] | $[X] | [X]% |
```

---

## Fase 4: Entregable

Presenta el análisis de costos completo con una recomendación de resumen.

```
## Resumen

**Producto:** [Nombre]
**Costo verdadero por unidad:** $[X] (incluyendo asignación de gastos generales)
**Margen actual:** [X]%
**Margen objetivo:** [X]%
**3 principales acciones de reducción de costos:**
1. [Acción] — ahorra $[X]/unidad
2. [Acción] — ahorra $[X]/unidad
3. [Acción] — ahorra $[X]/unidad
```

---

## Ejemplo: Curso en Línea

**Precio:** $197. **Costos directos:** $3.50/venta (procesamiento de pago $5.91, hosting $0.50, entrega de email $0.09, costo de creación amortizado $3/venta sobre 1,000 ventas). **Gastos generales/unidad:** $12 (basado en $1,200/mes de gastos generales a 100 ventas/mes). **Costo total:** $15.50. **Margen:** 92%.

**Insight:** Con margen de 92%, enfócate en crecimiento de volumen sobre reducción de costos. El costo de creación amortizado cae a medida que aumenta el volumen.

---

## Anti-Patrones

- **Ignorar costos de tiempo** — tu tiempo tiene valor en dólares. Si gastas 2 horas por unidad y tu tiempo vale $100/hora, eso es $200 en costo.
- **Olvidar honorarios de transacción** — procesadores de pago, honorarios de plataforma, y descuentos de mercado son costos reales. Inclúyelos.
- **Amortizar incorrectamente** — costos únicos (creación de producto, equipo) deben extenderse sobre las unidades esperadas de por vida, no cargadas a la primera venta.
- **Asignación de gastos generales sin contexto de volumen** — el costo por unidad de gastos generales cambia dramáticamente con el volumen. Siempre muestra la suposición de volumen.
- **Optimizar costos que no mueven la aguja** — un ahorro de $0.10/unidad importa a 100K unidades. A 100 unidades, enfócate en margen y precios en su lugar.

---

## Recuperación

- **El usuario no conoce todos sus costos:** Camina a través de cada paso de entrega e identifica costos en cada etapa. Los costos ocultos usualmente viven en tiempo, honorarios y herramientas.
- **Márgenes negativos:** Marca inmediatamente. Muestra qué costos deben reducirse o qué aumento de precio es necesario para alcanzar margen positivo.
- **Negocio de servicios (difícil de cuantificar por unidad):** Define la "unidad" como un compromiso de cliente, un proyecto, o un mes de servicio. Calcula costos contra esa unidad.
- **Múltiples productos que comparten gastos generales:** Asigna gastos generales proporcionalmente por ingresos o por unidades — indica el método y sé consistente.
