---
name: planificador-presupuesto-eventos
description: "Crea presupuestos de eventos con artículos de línea, planificación de contingencia, cálculos de offset de sponsor y proyecciones de ROI."
allowed-tools: Read Write Glob
metadata:
  author: Imperio Digital
  version: "1.0"
---

# Planificador de Presupuesto de Eventos

## Cuándo Usar Este Skill

Usa este skill cuando necesites:
- Crear un presupuesto detallado de evento con artículos de línea y estimaciones de costo
- Planificar reservas de contingencia y offsets de ingresos de patrocinio
- Proyectar ROI de evento incluyendo ingresos de tickets, patrocinio y valor indirecto
- Construir plantilla de rastreo de presupuesto para fases pre-evento, día del evento y post-evento

**NO** uses este skill para presupuestos generales de negocio, presupuestos de campañas de marketing o planificación de eventos personales. Esto es para planificación financiera de eventos profesionales o de negocio.

---

## Principio Fundamental

UN PRESUPUESTO DE EVENTO ES UNA HERRAMIENTA DE TOMA DE DECISIONES, NO SOLO UNA HOJA DE CÁLCULO — CADA ARTÍCULO DEBE CONECTAR CON LA EXPERIENCIA DEL ASISTENTE O GENERACIÓN DE INGRESOS, Y CADA DÓLAR DEBE TENER UN PLAN DE CONTINGENCIA.

---

## Fase 1: Brief

### Inputs Requeridos

| Input | Qué Preguntar | Predeterminado |
|-------|------------|---------|
| **Tipo de evento** | "¿Qué tipo de evento? (conferencia, workshop, summit, meetup, gala)" | Conferencia |
| **Asistencia esperada** | "¿Cuántos asistentes?" | 100-200 |
| **Duración** | "¿Cuánto tiempo? (medio día, día completo, multi-día)" | Día completo |
| **Formato** | "¿In-person, virtual o híbrido?" | In-person |
| **Presupuesto total** | "¿Cuál es tu presupuesto máximo?" | Sin predeterminado — debe proporcionarse |
| **Fuentes de ingresos** | "¿Venta de tickets, patrocinios, ambos o evento gratuito?" | Tickets + patrocinios |

**PUNTO DE CONTROL:** Confirma el brief antes de construir el presupuesto.

---

## Fase 2: Marco de Presupuesto

### Categorías de Gasto

```
## Categorías de Presupuesto (% del total para eventos in-person)

| Categoría | Rango % | Incluye |
|----------|---------|----------|
| Venue | 25-35% | Alquiler, seguros, permisos |
| Catering | 20-30% | Comidas, descansos, bebidas, dietas |
| AV/Tecnología | 10-15% | Sonido, pantallas, streaming, wifi |
| Speakers | 5-15% | Honorarios, viaje, hotel, regalos |
| Marketing | 5-10% | Anuncios, email, diseño, impresión |
| Materiales | 3-5% | Señalización, programas, name badges, swag |
| Staff/Voluntarios | 3-5% | Coordinador, staff día del evento, costos voluntarios |
| Contingencia | 10-15% | Gastos inesperados |
```

### Proyecciones de Ingresos

```
## Fuentes de Ingresos

**Venta de Tickets:**
| Tier | Precio | Cantidad Esperada | Ingresos |
|------|-------|-------------|---------|
| Early bird | $[X] | [Y] | $[Z] |
| Regular | $[X] | [Y] | $[Z] |
| VIP | $[X] | [Y] | $[Z] |
| **Total ingresos de tickets** | | | **$[X]** |

**Patrocinio:**
| Tier | Precio | Disponible | Vendidos Esperados | Ingresos |
|------|-------|-----------|-------------|---------|
| Title | $[X] | 1 | 1 | $[X] |
| Gold | $[X] | 3 | 2 | $[X] |
| Silver | $[X] | 5 | 3 | $[X] |
| **Total ingresos de patrocinio** | | | | **$[X]** |

**Total ingresos proyectados: $[X]**
```

**PUNTO DE CONTROL:** Presenta marco de presupuesto y proyecciones de ingresos para aprobación.

---

## Fase 3: Construir

### Presupuesto de Artículos de Línea Detallado

```
## Detalle de Gasto

### Venue
| Artículo | Estimado | Real | Varianza | Notas |
|------|----------|--------|----------|-------|
| Alquiler de sala | $[X] | | | |
| Seguros | $[X] | | | |
| Estacionamiento | $[X] | | | |
| **Subtotal** | **$[X]** | | | |

### Catering
| Artículo | Por Persona | Cantidad | Estimado | Real |
|------|-----------|-----|----------|--------|
| Desayuno | $[X] | [Y] | $[Z] | |
| Almuerzo | $[X] | [Y] | $[Z] | |
| Descanso PM | $[X] | [Y] | $[Z] | |
| Bebidas | $[X] | [Y] | $[Z] | |
| Acomodaciones dietéticas | Flat | | $[Z] | |
| **Subtotal** | | | **$[X]** | |

[Continúa para cada categoría...]
```

### Análisis de Punto de Equilibrio

```
## Cálculo de Punto de Equilibrio

**Costos fijos totales:** $[X] (venue, AV, speakers — costos sin importar asistencia)
**Costo variable por asistente:** $[Y] (catering, materiales, badges)
**Ingresos promedio de ticket por asistente:** $[Z]
**Ingresos de patrocinio (fijos):** $[W]

**Asistentes de punto de equilibrio:** (Costos Fijos - Patrocinio) / (Precio Ticket - Costo Variable)
= ($[X] - $[W]) / ($[Z] - $[Y])
= [Número] asistentes
```

### Cronograma de Flujo de Efectivo

```
## Cuándo Se Mueve el Dinero

**6 meses antes:** Depósito de venue (50%), depósitos de speakers
**3 meses antes:** Balance de venue, depósito AV, comienzan gastos de marketing
**1 mes antes:** Conteo final de catering + pago, impresión de materiales
**Semana del evento:** Pagos de staff, suministros de último minuto
**Día del evento:** Efectivo para emergencias, fondo de propinas
**Post-evento:** Facturas finales, pagos de speakers, reconciliación de contingencia
```

---

## Fase 4: Pulir

### 1. Planificación de Contingencia

```
## Escenarios de Contingencia

**Si las ventas de tickets están 25% por debajo del objetivo:**
- Cortar: [Artículos específicos a reducir — swag, catering mejorado, AV extra]
- Ahorros: $[X], impacto mínimo en experiencia del asistente

**Si un patrocinador mayor se va:**
- Plan de relleno: [Enfocar próximos prospectos de tier, ofrecer paquetes custom]
- Cortar: [Artículos financiados por patrocinio]

**Si la asistencia excede capacidad:**
- Tapa de registro en [X]
- Gestión de lista de espera
- Considera agregar opción de live stream
```

### 2. Plantilla de Rastreo de Presupuesto

```
## Revisión de Presupuesto Semanal (durante fase de planificación)

| Categoría | Presupuestado | Comprometido | Gastado | Restante | Estado |
|----------|----------|-----------|-------|-----------|--------|
| Venue | $[X] | $[X] | $[X] | $[X] | On track |
| Catering | $[X] | $[X] | $[X] | $[X] | Over |
| ... | | | | | |
| Contingencia | $[X] | $[X] | $[X] | $[X] | |
| **Total** | **$[X]** | **$[X]** | **$[X]** | **$[X]** | |
```

### 3. Cálculo de ROI

```
## ROI del Evento

**Ingresos directos:** Tickets ($[X]) + Patrocinios ($[X]) = $[Total]
**Gastos totales:** $[X]
**Ganancia/Pérdida directa:** $[X]

**Valor indirecto (estimado):**
- Crecimiento de lista de email: [X nuevos suscriptores] × $[valor por sub] = $[X]
- Leads de clientes generados: [X leads] × [tasa conversión] × [valor promedio cliente] = $[X]
- Exposición de marca: [impresiones] — valor cualitativo
- Asociaciones formadas: [conteo] — valor cualitativo

**ROI total estimado:** $[X] / $[Gastos totales] = [X]%
```

---

## Ejemplo 1: Conferencia de Negocio de 150 Personas

```
Presupuesto: $30,000
Ingresos: $25,000 tickets + $12,000 patrocinio = $37,000
Costos principales: Venue $8,000, Catering $9,000, AV $4,000, Speakers $3,500
Contingencia: $3,000 (10%)
Punto de equilibrio: 85 asistentes
Ganancia proyectada: $7,000
```

## Ejemplo 2: Meetup Comunitario Gratuito (50 Personas)

```
Presupuesto: $2,000
Ingresos: $1,500 patrocinio + $0 tickets
Costos principales: Venue $500 (espacio coworking), Catering $800, Materiales $200
Contingencia: $200 (10%)
Punto de equilibrio: N/A (financiado por sponsor)
ROI: Medido en leads y crecimiento de comunidad
```

---

## Anti-Patterns

- **Sin línea de contingencia** — cada evento tiene sorpresas. Presupuesta 10-15% para lo inesperado.
- **Subestimar catering** — costos de comida aumentan con conteos finales y solicitudes dietéticas. Acolcha por 15%.
- **Ignorar costos ocultos de venue** — seguros, surcargas AV, cuotas de horas extras y cargos de limpieza se suman. Pide breakdown completo.
- **Proyecciones de tickets optimistas** — planifica para 70% de tu objetivo, no 100%. El presupuesto debe funcionar en el número conservador.
- **Sin planificación de flujo de efectivo** — tener el dinero y tenerlo en el momento correcto son cosas diferentes. Mapea cuándo se vencen los pagos.
- **Olvidar costos post-evento** — pagos finales de speakers, regalos de agradecimiento, edición de grabaciones y facturas finales vienen después del evento.

---

## Recuperación

- **El presupuesto excede fondos disponibles:** Corta en orden: swag primero, luego reduce catering, luego reduce complejidad AV. Nunca cortes la contingencia.
- **Las ventas de tickets son lentas:** Aumenta gasto en marketing desde contingencia, agrega urgencia (precios límite), u ofrece descuentos de grupo.
- **Los ingresos de patrocinio no alcanzan objetivo:** Crea opciones de patrocinio a la carta a puntos de precio más bajos. Ofrece tier "community sponsor" a $250-500.
- **El usuario nunca ha presupuestado un evento:** Comienza con directrices de porcentaje y costos de un evento comparable como benchmarks. Ajusta después del primer evento.
