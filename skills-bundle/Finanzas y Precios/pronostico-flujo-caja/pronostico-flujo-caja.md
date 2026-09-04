---
name: pronostico-flujo-caja
description: "Proyecta flujo de caja mensual de 3-12 meses a partir de entradas de ingresos y gastos con modelado de escenarios y cálculos de pista de aterrizaje. Úsalo cuando un usuario necesite planificar gastos, evaluar si puede permitirse una contratación o inversión, o quiera entender cuándo se les acabará (o acumularán) efectivo."
allowed-tools: Read Write Glob
metadata:
  author: Imperio Digital
  version: "1.0"
---

# Pronóstico de Flujo de Caja

## Cuándo Usar Este Skill

- Planificar un gasto empresarial importante (contratación, equipo, gasto marketing)
- Evaluar si ingresos soportan la tasa de quema actual
- Preparar proyecciones financieras para un préstamo o inversionista
- Planificación empresarial estacional (anticipar meses lentos)
- Responder "¿cuánto tiempo puedo sostener esto?" o "¿cuándo alcanzo el equilibrio?"

**DESCARGO DE RESPONSABILIDAD: Esta herramienta proporciona estimaciones para propósitos de planificación. No es asesoramiento financiero. Consulta a un contador calificado o asesor financiero para planificación financiera formal.**

## Principio Fundamental

**EL FLUJO DE CAJA NO ES GANANCIA. UN NEGOCIO RENTABLE PUEDE QUEDARSE SIN EFECTIVO. ESTE PRONÓSTICO RASTREADOR CUÁNDO EL DINERO REALMENTE ENTRA Y SALE DE TU CUENTA BANCARIA.**

## Workflow

### Paso 1: Reunir Entradas Financieras

Pregunta al usuario:

1. Efectivo actual en mano (saldo bancario)
2. Fuentes de ingresos mensuales y cantidades (ser específico: clientes retainer, ventas de productos, suscripciones)
3. Gastos fijos mensuales (alquiler, software, suscripciones, salarios)
4. Gastos variables mensuales (anuncios, materiales, contratistas)
5. Cualquier gasto única vez o ingresos próximos (compra de equipo, pago de impuestos, firma de contrato)
6. Período de pronóstico (predeterminado: 6 meses)

**Mínimo necesario: preguntas 1, 2 y 3.**

### Paso 2: Construir la Tabla de Pronóstico

Crea una tabla mes a mes:

| | Mes 1 | Mes 2 | Mes 3 | Mes 4 | Mes 5 | Mes 6 |
|---|---------|---------|---------|---------|---------|---------|
| **Efectivo Inicial** | | | | | | |
| Línea de Ingresos 1 | | | | | | |
| Línea de Ingresos 2 | | | | | | |
| **Total Ingresos** | | | | | | |
| Gasto Fijo 1 | | | | | | |
| Gasto Fijo 2 | | | | | | |
| Gastos Variables | | | | | | |
| Gastos Única Vez | | | | | | |
| **Total Gastos** | | | | | | |
| **Flujo de Caja Neto** | | | | | | |
| **Efectivo Final** | | | | | | |

### Paso 3: Calcular Métricas Clave

- **Tasa de Quema Mensual:** Promedio de gastos totales por mes
- **Ratio de Cobertura de Ingresos:** Ingresos totales / gastos totales (arriba 1.0 = positivo en efectivo)
- **Pista de Aterrizaje de Efectivo:** Efectivo inicial / (gastos mensuales - ingresos mensuales) = meses hasta $0
- **Mes de Equilibrio:** Primer mes donde flujo de caja acumulativo se vuelve positivo
- **Punto de Efectivo Más Bajo:** El mes con el saldo de efectivo final más bajo (zona de peligro)

### Paso 4: Modelado de Escenarios

Construye tres escenarios:

| Escenario | Supuesto de Ingresos | Supuesto de Gasto |
|----------|-------------------|-------------------|
| Conservador | 80% de ingresos proyectados | 110% de gastos proyectados |
| Caso Base | 100% de proyectado | 100% de proyectado |
| Optimista | 120% de ingresos proyectados | 95% de gastos proyectados |

Destaca el **escenario conservador** como línea base de planificación.

### Paso 5: Recomendaciones

Basado en el pronóstico, proporciona:
- Zonas de peligro de efectivo (meses donde efectivo final cae bajo 1 mes de gastos)
- Recomendaciones específicas (cortar gastos, acelerar ingresos, construir reserva)
- Soporte de decisión para la pregunta original del usuario

## Ejemplos

### Ejemplo 1: Diseñador Freelance Considerando Contratación de Tiempo Completo

**Entradas:**
- Efectivo en mano: $28,000
- Ingresos: 3 clientes retainer × $3,500/mo = $10,500/mo + trabajo ocasional ~$2,000/mo
- Gastos fijos: $4,200/mo (alquiler $1,500, software $400, seguros $300, utilidades $200, contabilidad $150, misc $1,650)
- Contratación propuesta: $4,500/mo (salario + impuestos + beneficios)
- Pronóstico: 6 meses

**Pronóstico (Caso Base):**

| | Ene | Feb | Mar | Abr | May | Jun |
|---|-----|-----|-----|-----|-----|-----|
| Efectivo Inicial | $28,000 | $29,800 | $31,600 | $33,400 | $35,200 | $37,000 |
| Ingresos Retainer | $10,500 | $10,500 | $10,500 | $10,500 | $10,500 | $10,500 |
| Ingresos de Proyecto | $2,000 | $2,000 | $2,000 | $2,000 | $2,000 | $2,000 |
| **Total Ingresos** | **$12,500** | **$12,500** | **$12,500** | **$12,500** | **$12,500** | **$12,500** |
| Gastos Actuales | -$4,200 | -$4,200 | -$4,200 | -$4,200 | -$4,200 | -$4,200 |
| Nueva Contratación | -$4,500 | -$4,500 | -$4,500 | -$4,500 | -$4,500 | -$4,500 |
| Contratista (reemplazado) | $0 | $0 | $0 | $0 | $0 | $0 |
| **Total Gastos** | **-$8,700** | **-$8,700** | **-$8,700** | **-$8,700** | **-$8,700** | **-$8,700** |
| **Flujo de Caja Neto** | **$3,800** | **$3,800** | **$3,800** | **$3,800** | **$3,800** | **$3,800** |
| **Efectivo Final** | **$31,800** | **$35,600** | **$39,400** | **$43,200** | **$47,000** | **$50,800** |

**Escenario Conservador** (pierde 1 cliente retainer en mes 3):

| | Ene | Feb | Mar | Abr | May | Jun |
|---|-----|-----|-----|-----|-----|-----|
| Efectivo Final | $31,800 | $35,600 | $35,900 | $31,200 | $26,500 | $21,800 |

**Métricas Clave:**
- Tasa de quema con contratación: $8,700/mo
- Cobertura de ingresos: 1.44x (base) / 1.03x (conservador)
- Pista de aterrizaje (conservador, desde mes 3): 10.2 meses
- Punto de efectivo más bajo: $21,800 (mes 6, conservador)

**Recomendación:** La contratación es financieramente viable. Incluso en el escenario conservador (perder un cliente), mantienes $21,800+ efectivo a través del mes 6 — eso es 2.5 meses de pista de aterrizaje. Procede con la contratación, pero establece un disparador: si efectivo cae bajo $15,000, congela gasto no esencial.

### Ejemplo 2: Tienda de E-commerce Planificación Estacional

**Entradas:**
- Efectivo en mano: $12,000
- Ingresos: $8,000/mo promedio, pero estacional (Nov-Dic: $18,000, Ene-Feb: $4,000)
- Gastos fijos: $3,800/mo
- Variable (COGS): 40% de ingresos
- Compra de inventario Q4: $8,000 en septiembre

**Hallazgo Clave:** Efectivo cae a $1,400 en octubre (después de compra de inventario, antes de ventas de días festivos). Recomendación: asegura $5,000 línea de crédito antes de septiembre o pre-vende paquetes de días festivos en agosto.

## Recuperación y Alternativas

- **El usuario no sabe números exactos:** Usa rangos. "Los ingresos son probablemente $8K-$12K/mo" → modela a $8K (conservador).
- **Los ingresos son altamente variables:** Usa el promedio más bajo de 3 meses como línea base, no el promedio general.
- **El usuario no tiene registros financieros:** Comienza con extractos bancarios. Total de depósitos = ingresos, total de débitos = gastos. Es aproximado pero usable.
- **Pronóstico muestra pista de aterrizaje negativa:** No asustes al usuario. Presenta opciones: cortar gastos específicos, acelerar una iniciativa de ingresos, o puente con ahorros/crédito.

## Restricciones

- **SIEMPRE incluye el descargo de responsabilidad financiero**
- **NUNCA presentar pronósticos como garantías** — son estimaciones basadas en supuestos
- Siempre muestra supuestos debajo de cada proyección
- Usa escenario conservador como línea base de planificación
- Marca cualquier mes donde efectivo final cae bajo 1 mes de gastos
- Redondea a dólares completos — precision falsa ($10,437.83) implica precisión que no existe
