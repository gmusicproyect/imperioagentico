---
name: modelo-ingresos
description: "Diseña modelos de ingresos con tiers de pricing, economía unitaria, cálculos de LTV y proyecciones de crecimiento. Úsalo cuando planifiques o valides tu estrategia de ingresos empresarial."
allowed-tools: Read Write Glob
metadata:
  author: "Imperio Digital"
  version: "1.0"
---

# Modelo de Ingresos

## Cuándo Usar Este Skill

Usa este skill cuando necesites:
- Diseñar un modelo de ingresos con tiers de pricing y economía unitaria
- Calcular el valor de vida del cliente (LTV) y objetivos de costo de adquisición (CAC)
- Construir proyecciones financieras para los próximos 12-24 meses
- Validar si una idea de negocio o estrategia de pricing es financieramente viable

**NO** uses este skill para estados financieros completos, pitch decks para inversores o planificación fiscal. Esto es para análisis de modelado de ingresos y economía unitaria.

---

## Principio Fundamental

UN MODELO DE INGRESOS NO ES UNA LISTA DE DESEOS — CADA NÚMERO DEBE ESTAR FUNDAMENTADO EN DATOS REALES O SUPOSICIONES DEFENDIBLES, Y EL MODELO DEBE MOSTRAR EL CAMINO DESDE DÓNDE ESTÁS HASTA DÓNDE QUIERES ESTAR.

---

## Fase 1: Resumen Ejecutivo

### Inputs Requeridos

| Input | Qué Preguntar | Por Defecto |
|-------|--------------|---------|
| **Tipo de negocio** | "¿Qué vendes?" | Sin defecto — debe proporcionarse |
| **Ingresos actuales** | "¿Cuánto estás haciendo ahora? (mensual o anual)" | Sin ingresos o etapa temprana |
| **Objetivo de ingresos** | "¿Cuál es tu objetivo de ingresos en 12 meses?" | Sin defecto — debe proporcionarse |
| **Pricing** | "¿Qué cobras? (único, suscripción, por proyecto)" | Sin defecto — debe proporcionarse |
| **Cantidad de clientes** | "¿Cuántos clientes/clientes tienes?" | Menos de 50 |
| **Canales de adquisición** | "¿Cómo consigues clientes?" | Orgánico + referidos |
| **Márgenes** | "¿Cuál es tu margen de ganancia aproximado por venta?" | 70%+ para digital, varía para servicios |

**PUNTO DE CONTROL:** Confirma los inputs antes de construir el modelo.

---

## Fase 2: Arquitectura de Ingresos

### Mapeo de Fuentes de Ingresos

```
## Fuentes de Ingresos

**Fuente 1: [Producto/Servicio Principal]**
- Tipo: [Único / Suscripción / Por proyecto]
- Precio: $[X]
- Frecuencia: [Mensual / Anual / Por engagement]
- Margen: [X]%

**Fuente 2: [Producto/Servicio Secundario]**
- Tipo: [Único / Suscripción / Por proyecto]
- Precio: $[X]
- Frecuencia: [Mensual / Anual / Por engagement]
- Margen: [X]%

**Fuente 3: [Ingresos Adicionales]** (si aplica)
- Tipo: [Afiliados / Ads / Licensing / etc.]
```

### Economía Unitaria

```
## Economía Unitaria

**Ingresos Promedio Por Cliente (ARPC):** $[X]
**Costo de Bienes Vendidos (COGS):** $[X] por cliente
**Margen Bruto Por Cliente:** $[X] ([X]%)
**Costo de Adquisición de Cliente (CAC):** $[X]
**Período de Recuperación CAC:** [X] meses
**Valor de Vida del Cliente (LTV):** $[X]
**Ratio LTV:CAC:** [X]:1 (objetivo: 3:1 o superior)

**Tasa de Churn (si suscripción):** [X]% mensual
**Vida Promedio del Cliente:** [X] meses
```

**PUNTO DE CONTROL:** Aprueba la arquitectura de ingresos antes de ejecutar proyecciones.

---

## Fase 3: Proyecciones Financieras

### Proyección de Ingresos de 12 Meses

Construye una proyección mes a mes:

```
## Proyección de Ingresos Mensual

| Mes | Clientes Nuevos | Clientes Totales | Ingresos | Acumulado |
|-------|--------------|-----------------|---------|------------|
| 1 | [X] | [X] | $[X] | $[X] |
| 2 | [X] | [X] | $[X] | $[X] |
| ... | | | | |
| 12 | [X] | [X] | $[X] | $[X] |

**Ingresos Anuales:** $[X]
**Ingresos Promedio Mensual:** $[X]
**Tasa de Crecimiento:** [X]% mes a mes
```

### Análisis de Escenarios

```
## Tres Escenarios

**Conservador (80% confianza):**
- [X] clientes nuevos/mes, [X]% churn
- Ingresos anuales: $[X]

**Caso Base (50% confianza):**
- [X] clientes nuevos/mes, [X]% churn
- Ingresos anuales: $[X]

**Agresivo (20% confianza):**
- [X] clientes nuevos/mes, [X]% churn
- Ingresos anuales: $[X]
```

### Palancas de Ingresos

Identifica las 3-5 mayores palancas para crecer ingresos:
1. Aumentar volumen de adquisición de clientes
2. Subir precios o agregar tier premium
3. Reducir churn (para modelos de suscripción)
4. Aumentar valor de orden promedio (upsells, cross-sells)
5. Introducir nuevas fuentes de ingresos

---

## Fase 4: Pulido Final

### 1. Documento de Supuestos Clave

Lista cada suposición en la que se basa el modelo:
- Tasa y crecimiento de adquisición de clientes
- Supuestos de tasa de churn
- Estabilidad de pricing
- Restricciones de tamaño de mercado
- Fluctuaciones estacionales

### 2. Análisis de Punto de Equilibrio

Calcula la cantidad de clientes o ingresos necesarios para cubrir:
- Costos fijos (herramientas, software, gastos generales)
- Costos variables (cumplimiento, soporte)
- Salario deseado del propietario

### 3. Cronograma de Revisión del Modelo

- Mensual: compara real vs. proyectado, ajusta supuestos
- Trimestral: revisa la proyección completa de 12 meses
- Anualmente: reconstruye el modelo desde cero con datos actualizados

---

## Anti-Patrones

- **Proyecciones hockey-stick sin base** — mostrar crecimiento 10x sin un plan para adquirir clientes es fantasía, no modelado.
- **Ignorar churn** — modelos de suscripción sin estimaciones de churn son salvajemente inexactos. Incluso 5% de churn mensual pierde la mitad de tus clientes en un año.
- **Planificación de un solo escenario** — modelar solo el mejor caso te deja sin preparación para la realidad.
- **Olvidar CAC** — los ingresos no significan nada si la adquisición de clientes cuesta más de lo que vale el cliente.
- **Pricing estático** — el modelo debe mostrar cómo los cambios de precio afectan la proyección completa. Construye flexibilidad.

---

## Recuperación

- **Sin datos para basar proyecciones:** Comienza con benchmarks de industria y tu tasa actual de adquisición. Modela desde la realidad, no desde deseos.
- **Negocio sin ingresos:** Construye el modelo alrededor del punto de equilibrio primero. ¿Cuántos clientes a qué precio cubre costos?
- **Múltiples productos, modelo complejo:** Enfócate en el stream de ingresos principal primero. Agrega streams secundarios después de que el modelo principal sea sólido.
- **Usuario quiere números garantizados:** Explica que los modelos son estimaciones basadas en supuestos. El valor está en entender las palancas, no en predecir números exactos.
