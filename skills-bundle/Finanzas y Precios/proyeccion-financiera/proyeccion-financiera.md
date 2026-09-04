---
name: proyeccion-financiera
description: "Construye proyecciones financieras de 12 meses con escenarios de ingresos, pronósticos de gastos y análisis de punto de equilibrio. Úsalo cuando planifiques ingresos y gastos futuros para tu negocio."
allowed-tools: Read Write Glob
metadata:
  author: Imperio Digital
  version: "1.0"
---

# Proyección Financiera

## Cuándo usar esta habilidad

Usa esta habilidad cuando necesites:
- Construir una proyección financiera de 12 meses para un negocio
- Modelar escenarios de crecimiento de ingresos (conservador, base, optimista)
- Pronosticar gastos e identificar cuándo alcanzas rentabilidad
- Crear proyecciones para pitches de inversionistas, solicitudes de préstamo o planificación estratégica

**NO** uses esta habilidad para presupuestación mensual (usa planificador-presupuesto), reportes financieros en tiempo real o planificación financiera personal. Esto es para modelos financieros comerciales prospectivos.

---

## Principio Central

LAS PROYECCIONES NO SON PREDICCIONES — SON SUPUESTOS ESTRUCTURADOS QUE TE AYUDAN A TOMAR DECISIONES HOY BASADO EN A DÓNDE PODRÍAN IR LOS NÚMEROS.

---

## Fase 1: Datos de Base

### Entradas Requeridas

| Entrada | Qué Preguntar | Predeterminado |
|---------|--------------|----------------|
| **Ingresos mensuales actuales** | "¿Cuál es tu ingreso mensual actual?" | Sin predeterminado — debe proporcionarse |
| **Modelo de ingresos** | "¿Cómo haces dinero? (suscripciones, ventas única, retenciones, por hora)" | Ventas única |
| **Gastos mensuales actuales** | "¿Cuáles son tus gastos mensuales totales?" | Sin predeterminado — debe proporcionarse |
| **Supuesto de tasa de crecimiento** | "¿Qué tasa de crecimiento mensual esperas? (o crecimiento histórico si disponible)" | 5-10% mes a mes |
| **Inversiones planeadas** | "¿Algún gasto mayor planeado? (contrataciones, equipo, gasto de marketing)" | Ninguno |
| **Propósito de proyección** | "¿Para qué es esto? (planificación interna, inversionistas, préstamo, estratégico)" | Planificación interna |

**PUNTO DE CONTROL: No continúes sin ingresos actuales, gastos y modelo de ingresos.**

---

## Fase 2: Proyección de Ingresos

### Tres Escenarios

Construye proyecciones para escenarios conservador, base y optimista:

```
## Proyección de Ingresos: Perspectiva de 12 Meses

### Supuestos
- Tasa de crecimiento mensual base: [X]%
- Conservador: [X-2]% crecimiento mensual
- Optimista: [X+3]% crecimiento mensual
- Ingresos mensuales de inicio: $[X]

### Ingresos Mensuales por Escenario

| Mes | Conservador | Base | Optimista |
|-----|------------|------|-----------|
| Mes 1 | $[X] | $[X] | $[X] |
| Mes 2 | $[X] | $[X] | $[X] |
| ... | | | |
| Mes 12 | $[X] | $[X] | $[X] |
| **Total Anual** | **$[X]** | **$[X]** | **$[X]** |
```

### Generadores de Ingresos

Desglosa ingresos en sus generadores componentes:

```
### Desglose de Generador de Ingresos (Caso Base)

| Generador | Mes 1 | Mes 6 | Mes 12 |
|----------|-------|-------|--------|
| [Producto/servicio 1] unidades | [X] | [X] | [X] |
| [Producto/servicio 1] ingresos | $[X] | $[X] | $[X] |
| [Producto/servicio 2] unidades | [X] | [X] | [X] |
| [Producto/servicio 2] ingresos | $[X] | $[X] | $[X] |
| **Total** | **$[X]** | **$[X]** | **$[X]** |
```

---

## Fase 3: Pronóstico de Gastos

### Categorías de Gastos

```
## Proyección de Gastos

### Gastos Fijos (Mensual)
| Categoría | Actual | Mes 6 | Mes 12 | Notas |
|-----------|--------|-------|--------|-------|
| [Renta/espacio] | $[X] | $[X] | $[X] | |
| [Software] | $[X] | $[X] | $[X] | |
| [Seguros] | $[X] | $[X] | $[X] | |

### Gastos Variables (Escalan con Ingresos)
| Categoría | % de Ingresos | Mes 1 | Mes 6 | Mes 12 |
|-----------|--------------|-------|-------|--------|
| [COGS] | [X]% | $[X] | $[X] | $[X] |
| [Marketing] | [X]% | $[X] | $[X] | $[X] |
| [Contratistas] | [X]% | $[X] | $[X] | $[X] |

### Costos de Escalón Planeados
| Inversión | Mes | Costo Mensual | Propósito |
|----------|-----|--------------|-----------|
| [Nueva contratación] | Mes [X] | $[X] | [Justificación] |
| [Mejora de herramienta] | Mes [X] | $[X] | [Justificación] |
```

---

## Fase 4: Resumen de Pérdidas y Ganancias

### P&G Mensual

```
## Pérdidas y Ganancias Proyectadas (Caso Base)

| | M1 | M2 | M3 | M4 | M5 | M6 | M7 | M8 | M9 | M10 | M11 | M12 |
|--|----|----|----|----|----|----|----|----|----|----|-----|-----|
| Ingresos | | | | | | | | | | | | |
| COGS | | | | | | | | | | | | |
| Ganancia Bruta | | | | | | | | | | | | |
| Gastos Operativos | | | | | | | | | | | | |
| **Ganancia Neta** | | | | | | | | | | | | |
| P&G Acumulado | | | | | | | | | | | | |

### Punto de Equilibrio
- Mes de punto de equilibrio: Mes [X] (caso base)
- Ingresos mensuales necesarios para punto de equilibrio: $[X]
- Unidades mensuales necesarias para punto de equilibrio: [X]
```

### Métricas Clave en el Tiempo

```
### Métricas de Salud Financiera

| Métrica | Mes 1 | Mes 6 | Mes 12 |
|---------|-------|-------|--------|
| Margen bruto | [X]% | [X]% | [X]% |
| Margen neto | [X]% | [X]% | [X]% |
| Tasa de quemado mensual | $[X] | $[X] | $[X] |
| Pista de caja (meses) | [X] | [X] | [X] |
```

---

## Ejemplo: Lanzamiento de Producto SaaS

**Entradas:** MRR actual $2,000, crecimiento base 12%/mes, gastos $4,500/mes, contratar VA en mes 4 en $2,000/mes.

**Resultado (Caso Base):** Equilibrio en mes 5. MRR Mes 12: $6,930. Ingresos anuales: $48,400. Ganancia neta meses 5-12: $11,200.

---

## Anti-patrones

- **Proyecciones hockey stick sin justificación** — 50% crecimiento mensual necesita un generador específico, no optimismo
- **Ignorar costos de escalón** — crecimiento de ingresos dispara nuevos gastos (más soporte, infraestructura, equipo). Modélalos.
- **Solo escenario único** — siempre modela al menos conservador y base. Stakeholders necesitan ver el rango.
- **Proyectar ingresos sin economía unitaria** — "haremos $100K" no es una proyección. Muestra unidades, precios y tasas de conversión que producen $100K.
- **Olvidar impuestos** — incluye responsabilidad fiscal estimada en pronóstico de gastos

---

## Recuperación

- **Negocio pre-ingresos:** Comienza con ingresos cero y modela desde primera venta. Enfócate en pista de despegue de gastos — ¿cuántos meses hasta que se acabe dinero?
- **Ingresos altamente variables:** Usa los 3 meses más bajos como base conservadora. Modela estacionalidad si aplicable.
- **Sin datos de tasa de crecimiento:** Usa benchmarks de industria o modela ingresos planos como conservador, 5% como base, 10% como optimista.
- **Proyecciones para inversionistas:** Añade sección "supuestos clave" listando cada supuesto y su fuente. Inversionistas stress-test supuestos, no números.
