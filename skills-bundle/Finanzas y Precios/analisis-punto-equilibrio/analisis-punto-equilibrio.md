---
name: analisis-punto-equilibrio
description: "Realiza análisis de punto de equilibrio con desglose de costos fijos/variables, cálculos de margen y modelado de escenarios. Úsalo cuando necesites determinar cuántas ventas necesitas para cubrir costos."
allowed-tools: Read Write Glob
metadata:
  author: Imperio Digital
  version: "1.0"
---

# Análisis de Punto de Equilibrio

## Cuándo Usar Este Skill

Utiliza este skill cuando necesites:
- Calcular cuántas unidades o ventas necesitas para alcanzar el punto de equilibrio
- Analizar costos fijos vs. variables para encontrar el punto de equilibrio
- Modelar escenarios de punto de equilibrio para diferentes estructuras de precios o costos
- Evaluar la viabilidad de un nuevo producto, servicio o negocio

**NO uses este skill** para proyecciones financieras completas o estrategia de precios. Esto es específicamente para determinar el punto de equilibrio.

---

## Principio Fundamental

EL PUNTO DE EQUILIBRIO ES EL NÚMERO VIABLE MÍNIMO — TE DICE EL PISO, NO LA META. SI NO PUEDES ALCANZAR EL PUNTO DE EQUILIBRIO, EL MODELO DE NEGOCIO NECESITA CAMBIAR ANTES QUE NADA.

---

## Fase 1: Entradas de Costos

### Información Requerida

| Entrada | Qué Preguntar | Predeterminado |
|-------|------------|---------|
| **Producto/servicio** | "¿Qué estamos analizando?" | Sin predeterminado — debe proporcionarse |
| **Precio de venta por unidad** | "¿Cuánto cobras por unidad/venta/proyecto?" | Sin predeterminado — debe proporcionarse |
| **Costo variable por unidad** | "¿Qué cuesta cada venta? (materiales, envío, comisiones)" | Sin predeterminado — debe proporcionarse |
| **Costos fijos mensuales** | "¿Cuáles son tus costos mensuales que no cambian con volumen de ventas?" | Sin predeterminado — debe proporcionarse |
| **Período de tiempo** | "¿Analizar mensual o anualmente?" | Mensual |

**PUNTO DE CONTROL: No procedas sin precio, costo variable y costos fijos.**

---

## Fase 2: Cálculo del Punto de Equilibrio

```
## Análisis de Punto de Equilibrio: [Producto/Servicio]

### Estructura de Costos
| Categoría | Cantidad |
|----------|--------|
| Precio de venta por unidad | $[X] |
| Costo variable por unidad | $[X] |
| **Margen de contribución por unidad** | **$[X]** |
| **Margen de contribución %** | **[X]%** |
| Costos fijos mensuales | $[X] |

### Punto de Equilibrio
| Métrica | Valor | Fórmula |
|--------|-------|---------|
| **Unidades punto de equilibrio (mensual)** | **[X] unidades** | Costos fijos / Margen de contribución |
| **Ingresos punto de equilibrio (mensual)** | **$[X]** | Unidades punto de equilibrio x Precio |
| Unidades punto de equilibrio (anual) | [X] unidades | Mensual x 12 |
| Ingresos punto de equilibrio (anual) | $[X] | Mensual x 12 |
| Unidades por día necesarias | [X] | Mensual / 30 |
| Unidades por semana necesarias | [X] | Mensual / 4.3 |

### Margen de Seguridad
En ventas actuales de [X] unidades/mes:
| Métrica | Valor |
|--------|-------|
| Unidades mensuales actuales | [X] |
| Unidades punto de equilibrio | [X] |
| Margen de seguridad (unidades) | [X] |
| Margen de seguridad (%) | [X]% |
```

---

## Fase 3: Modelado de Escenarios

```
## Análisis de Escenarios

### Sensibilidad de Precio
| Punto de Precio | Margen de Contribución | Unidades Punto de Equilibrio | Ingresos Punto de Equilibrio |
|------------|--------------------|-----------------|--------------------|
| $[X] (-20%) | $[X] | [X] | $[X] |
| $[X] (-10%) | $[X] | [X] | $[X] |
| **$[X] (actual)** | **$[X]** | **[X]** | **$[X]** |
| $[X] (+10%) | $[X] | [X] | $[X] |
| $[X] (+20%) | $[X] | [X] | $[X] |

### Escenarios de Costo Fijo
| Escenario | Costo Fijo Mensual | Unidades Punto de Equilibrio | Notas |
|----------|-------------|-----------------|-------|
| Eficiente (cortar no esenciales) | $[X] | [X] | [Qué se corta] |
| **Actual** | **$[X]** | **[X]** | |
| Crecimiento (agregar contratación/herramienta) | $[X] | [X] | [Qué se agrega] |

### Escenarios de Costo Variable
| Escenario | Costo Variable/Unidad | Unidades Punto de Equilibrio |
|----------|-------------------|-----------------|
| Optimizado (reducir COGS) | $[X] | [X] |
| **Actual** | **$[X]** | **[X]** |
| Aumentado (mayor calidad) | $[X] | [X] |
```

---

## Fase 4: Plan de Acción

```
## Recomendaciones

### Ruta al Punto de Equilibrio
- Ventas mensuales actuales: [X] unidades
- Meta punto de equilibrio: [X] unidades
- Brecha: [X] unidades ([X]% aumento necesario)

### Palancas Más Rápidas
1. **[Palanca]** — [Impacto en punto de equilibrio]
2. **[Palanca]** — [Impacto]
3. **[Palanca]** — [Impacto]

### Cronograma al Punto de Equilibrio
A tasa de crecimiento mensual [X]%: [X] meses para alcanzar volumen punto de equilibrio.
```

---

## Ejemplo: Curso Online ($197 precio)

**Costos:** Variable $8/venta (procesamiento + hosting). Fijo $3,200/mes (software, anuncios, contratistas). Margen de contribución: $189/venta.

**Punto de equilibrio:** 17 ventas/mes ($3,349/mes ingresos). En 12 ventas/mes actuales, necesitas 42% más ventas. A crecimiento mensual del 10%, punto de equilibrio en 4 meses.

**Escenario:** Si el precio aumenta a $247, punto de equilibrio baja a 13.4 ventas/mes — ya rentable al volumen actual.

---

## Anti-Patrones

- **Olvidar costos variables ocultos** — comisiones de procesamiento, envío, empaque y comisiones de plataforma son costos variables. Inclúyelos todos.
- **Tratar salario del propietario como opcional** — si planeas pagarte, inclúyelo en costos fijos. Un negocio "rentable" que no paga al propietario no es rentable.
- **Solo análisis estático** — siempre incluye al menos 3 escenarios (cambio de precio, cambio de costo, cambio de volumen).
- **Ignorar la línea de tiempo** — punto de equilibrio en 2 meses es excelente. Punto de equilibrio en 24 meses puede significar que se te acaba el efectivo primero.
- **Asumir escalado lineal** — en volúmenes altos, costos variables pueden cambiar (descuentos por volumen o infraestructura adicional). Nota el rango de volumen donde tus números se mantienen.

---

## Recuperación

- **Punto de equilibrio parece inalcanzable:** Muestra qué cambio único (aumento de precio, reducción de costo, o flujo de ingresos adicional) tiene el mayor impacto. A veces un aumento de precio del 15% lo cambia todo.
- **Múltiples productos:** Calcula punto de equilibrio por producto, luego crea análisis combinado usando el margen de contribución promedio ponderado.
- **Negocio de servicio (sin "unidad" clara):** Define la unidad como un cliente, un proyecto, o un mes de servicio. Calcula basado en eso.
- **Pre-lanzamiento (sin datos de ventas):** Usa análisis de punto de equilibrio para establecer objetivos. "Necesitas X ventas/mes a $Y precio para cubrir costos" se convierte en la meta de lanzamiento.
