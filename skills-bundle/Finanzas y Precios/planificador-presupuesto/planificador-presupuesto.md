---
name: planificador-presupuesto
description: "Crea presupuestos mensuales y anuales del negocio con desglose de categorías, seguimiento de varianza y disparadores de ajuste. Úsalo cuando estés construyendo o revisando un presupuesto empresarial."
allowed-tools: Read Write Glob
metadata:
  author: Imperio Digital
  version: "1.0"
---

# Planificador de Presupuesto

## Cuándo Usar Este Skill

Utiliza este skill cuando necesites:
- Crear un presupuesto mensual o anual empresarial desde cero
- Organizar gastos en categorías con objetivos de asignación
- Construir seguimiento de varianza para comparar presupuesto vs. gasto real
- Configurar disparadores de ajuste para cuando el gasto se desvíe

**NO uses este skill** para presupuestos personales, proyecciones financieras (usa financial-projection), o planificación de inversiones. Esto es para presupuesto operativo empresarial.

---

## Principio Fundamental

UN PRESUPUESTO ES UNA HERRAMIENTA DE TOMA DE DECISIONES, NO UNA HOJA DE CÁLCULO — CADA LÍNEA DEBE VINCULARSE A UNA PRIORIDAD EMPRESARIAL Y TENER UN PROPIETARIO CLARO.

---

## Fase 1: Instantánea del Negocio

### Información Requerida

| Entrada | Qué Preguntar | Predeterminado |
|-------|------------|---------|
| **Ingresos mensuales** | "¿Cuáles son tus ingresos mensuales actuales o esperados?" | Sin predeterminado — debe proporcionarse |
| **Tipo de negocio** | "¿Qué tipo de negocio? (servicio, producto, SaaS, consultoría)" | Basado en servicios |
| **Tamaño del equipo** | "¿Cuántas personas? (solo tú, contratistas, empleados)" | Solo con contratistas |
| **Top 3 categorías de gasto** | "¿Cuáles son tus costos más grandes?" | Software, marketing, contratistas |
| **Período del presupuesto** | "¿Presupuesto mensual o anual?" | Mensual |
| **Objetivos de crecimiento** | "¿Alguna inversión planificada o gasto de crecimiento?" | Ninguno especificado |

**PUNTO DE CONTROL: No procedas sin ingresos mensuales y tipo de negocio.**

---

## Fase 2: Marco del Presupuesto

### Estructura de Categorías

Construye el presupuesto usando estas categorías estándar, ajustadas para tipo de negocio:

```
## Presupuesto: [Nombre del Negocio] — [Mes/Año o Anual]

### Ingresos
| Fuente | Presupuestado | Notas |
|--------|----------|-------|
| [Ingresos primarios] | $[X] | |
| [Ingresos secundarios] | $[X] | |
| **Total Ingresos** | **$[X]** | |

### Costos Fijos (No cambian mes a mes)
| Categoría | Presupuestado | % de Ingresos | Notas |
|----------|----------|-------------|-------|
| Alquiler/espacio de trabajo | $[X] | [X]% | |
| Software/suscripciones | $[X] | [X]% | |
| Seguros | $[X] | [X]% | |
| Salarios (si aplica) | $[X] | [X]% | |
| **Total Fijo** | **$[X]** | **[X]%** | |

### Costos Variables (Escalan con ingresos)
| Categoría | Presupuestado | % de Ingresos | Notas |
|----------|----------|-------------|-------|
| Marketing/publicidad | $[X] | [X]% | |
| Contratistas/freelancers | $[X] | [X]% | |
| COGS/cumplimiento | $[X] | [X]% | |
| Comisiones transaccionales | $[X] | [X]% | |
| **Total Variable** | **$[X]** | **[X]%** | |

### Inversiones de Crecimiento (Discrecional)
| Categoría | Presupuestado | % de Ingresos | Notas |
|----------|----------|-------------|-------|
| Herramientas/equipo nuevo | $[X] | [X]% | |
| Educación/capacitación | $[X] | [X]% | |
| Contratación | $[X] | [X]% | |
| **Total Crecimiento** | **$[X]** | **[X]%** | |

### Resumen
| | Cantidad | % de Ingresos |
|--|--------|-------------|
| Total Ingresos | $[X] | 100% |
| Total Gastos | $[X] | [X]% |
| **Ganancia Neta** | **$[X]** | **[X]%** |
```

### Asignaciones de Referencia (Trabajador Autónomo/Pequeño Negocio)

| Categoría | Rango Saludable |
|----------|--------------|
| Costos fijos | 15-30% de ingresos |
| Marketing | 5-15% de ingresos |
| Contratistas | 10-25% de ingresos |
| Pago del propietario | 30-50% de ingresos |
| Reserva de ganancia | 10-20% de ingresos |
| Reserva fiscal | 25-30% de ganancia |

---

## Fase 3: Seguimiento de Varianza

### Plantilla de Seguimiento Mensual

```
## Reporte de Varianza: [Mes]

| Categoría | Presupuestado | Real | Varianza | % Varianza |
|----------|----------|--------|----------|------------|
| [Categoría] | $[X] | $[X] | +/-$[X] | +/-[X]% |

### Indicadores de Varianza
🔴 Sobre presupuesto >15%: [Listar categorías]
🟡 Sobre presupuesto 5-15%: [Listar categorías]
🟢 En o bajo presupuesto: [Listar categorías]
```

### Disparadores de Ajuste

Define cuándo tomar acción:

```
## Disparadores de Ajuste

| Disparador | Acción |
|---------|--------|
| Ingresos caen >10% del plan | Cortar gasto discrecional, pausar inversiones de crecimiento |
| Cualquier categoría excede presupuesto >20% | Revisar y reasignar o cortar antes del próximo mes |
| Ingresos superan plan >15% | Asignar superávit: 50% reserva ganancia, 30% crecimiento, 20% bonificación propietario |
| Reserva de efectivo cae bajo 2 meses gastos | Congelar todo gasto no esencial |
| Gasto marketing excede 15% sin aumento correspondiente de ingresos | Auditar ROI campaña, pausar bajo rendimiento |
```

---

## Fase 4: Entregable

Presenta el documento presupuestario completo y proporciona recordatorios de revisión trimestral.

```
presupuesto/
└── presupuesto-[YYYY].md (o presupuesto-[YYYY-MM].md para mensual)
```

Incluye: Objetivos de ingresos, gastos categorizados, benchmarks de porcentaje, plantilla de seguimiento de varianza, y disparadores de ajuste.

---

## Ejemplo: Consultor Trabajador Autónomo ($12K/mes Ingresos)

| Categoría | Cantidad | % |
|----------|--------|---|
| Ingresos | $12,000 | 100% |
| Software/herramientas | $400 | 3% |
| Marketing | $1,200 | 10% |
| Contratistas | $1,800 | 15% |
| Comisiones transaccionales | $360 | 3% |
| Educación | $200 | 2% |
| Reserva fiscal | $2,400 | 20% |
| Pago del propietario | $4,500 | 38% |
| Reserva de ganancia | $1,140 | 10% |

---

## Anti-Patrones

- **Presupuestar basado en esperanzas en lugar de datos** — usa ingresos reales de los últimos 3-6 meses, no proyecciones en el mejor caso
- **Sin reserva fiscal** — trabajadores autónomos que no apartan 25-30% para impuestos se sorprenden a tiempo de impuestos
- **Cero amortiguador** — siempre presupuesta 5-10% para gastos inesperados
- **Configurar y olvidar** — un presupuesto revisado trimestralmente es una sugerencia. Revisa mensualmente, ajusta según sea necesario.
- **Cortar marketing primero** — marketing impulsa ingresos. Corta marketing bajo ROI, no todo marketing.

---

## Recuperación

- **Ingresos irregulares:** Presupuesta basado en el promedio de los últimos 6 meses. Crea un "presupuesto mínimo viable" para meses bajos y un "presupuesto de crecimiento" para meses altos.
- **Sin datos históricos (negocio nuevo):** Construye un presupuesto conservador basado en ingresos esperados, luego actualiza mensualmente con datos reales durante los primeros 6 meses.
- **Los gastos exceden ingresos:** Marca inmediatamente. Identifica qué costos pueden cortarse o diferirse, y qué aumento de ingresos se necesita para alcanzar equilibrio.
- **Múltiples flujos de ingresos:** Divide ingresos en líneas separadas pero mantén gastos consolidados a menos que se vinculen directamente a un flujo.
