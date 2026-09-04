---
name: analisis-propiedad-inversion
description: "Analiza propiedades inversion alquiler con proyecciones flujo efectivo, cálculos cap rate y escenarios ROI."
allowed-tools: Read Write Glob
metadata:
  author: Imperio Digital
  version: "1.0"
---

# Análisis Propiedad Inversión

## Cuándo Usar Este Skill

Usa este skill cuando necesites:
- Analizar viabilidad financiera propiedad alquiler antes comprar
- Calcular flujo efectivo, cap rate, retorno efectivo cash y proyecciones ROI
- Comparar múltiples propiedades inversión usando métricas consistentes
- Presentar análisis inversión cliente comprador o portafolio tuyo

**NO USES** este skill para análisis bienes raíces comercial, inversión REITs o tasaciones propiedad.

---

## Principio Fundamental

DECISIONES INVERSIÓN BASADAS NÚMEROS, NO SENTIMIENTOS — EJECUTA ANÁLISIS CON SUPUESTOS CONSERVADORES DEJA MATEMÁTICAS DIGAN SI COMPRAR.

---

## Fase 1: Datos Propiedad

### Entradas Requeridas

| Entrada | Qué Preguntar | Predeterminado |
|-------|------------|---------|
| **Dirección propiedad** | "¿Qué propiedad analizas?" | Sin predeterminado |
| **Precio compra** | "¿Precio venta u oferta?" | Sin predeterminado |
| **Alquiler esperado** | "¿Alquiler mensual estimado?" | Sin predeterminado |
| **Enganche** | "¿Cuánto poniendo enganche?" | 25% (standard propiedad inversión) |
| **Tasa interés** | "¿Tasa hipoteca estimando?" | Tasa mercado actual |
| **Impuestos propiedad** | "¿Cantidad impuesto propiedad anual?" | 1.2% precio compra |
| **Seguro** | "¿Costo seguro anual?" | $1,200/año |
| **Condición actual** | "¿Necesita reparaciones? ¿Costo rehab estimado?" | Listo mudanza |

**PUNTO DE CONTROL:** Confirma todas entradas financieras antes correr cálculos.

---

## Fase 2: Análisis Financiero

### Análisis Flujo Efectivo Mensual

```
## Análisis Flujo Efectivo — [Dirección Propiedad]

### Ingresos
| Fuente | Mensual | Anual |
|--------|---------|--------|
| Alquiler bruto | $[X] | $[X] |
| Otro ingreso (lavandería, estacionamiento, almacenamiento) | $[X] | $[X] |
| **Ingresos brutos** | **$[X]** | **$[X]** |

### Asignación Vacancia
| Factor | Tasa | Mensual | Anual |
|--------|------|---------|--------|
| Vacancia | 5-8% | -$[X] | -$[X] |
| **Ingresos brutos efectivos** | | **$[X]** | **$[X]** |

### Gastos Operativos
| Gasto | Mensual | Anual |
|---------|---------|--------|
| Impuestos propiedad | $[X] | $[X] |
| Seguro | $[X] | $[X] |
| Gestión propiedad (8-10%) | $[X] | $[X] |
| Reserva mantenimiento (5-10%) | $[X] | $[X] |
| Reserva gastos capital (5%) | $[X] | $[X] |
| Tarifas HOA | $[X] | $[X] |
| Servicios públicos (si propietario paga) | $[X] | $[X] |
| **Total gastos operativos** | **$[X]** | **$[X]** |

### Ingreso Operativo Neto (NOI)
**NOI = Ingresos Brutos Efectivos - Gastos Operativos**
**NOI = $[X]/año**

### Servicio Deuda
| Factor | Monto |
|--------|--------|
| Monto préstamo | $[X] |
| Tasa interés | [X]% |
| Plazo préstamo | 30 años |
| **Pago mensual (P&I)** | **$[X]** |
| **Servicio deuda anual** | **$[X]** |

### Flujo Efectivo Mensual
**Flujo efectivo = NOI/12 - Pago servicio deuda mensual = $[X]/mes**
**Flujo efectivo anual = $[X]**
```

---

## Fase 3: Métricas Retorno

### Métricas Clave

```
## Métricas Inversión — [Dirección Propiedad]

### Cap Rate
NOI / Precio Compra = $[X] / $[X] = [X]%
[Objetivo: 5-10% dependiendo mercado]

### Retorno Efectivo Cash
Flujo Efectivo Anual / Total Efectivo Invertido = $[X] / $[X] = [X]%
[Objetivo: 8-12% para acuerdo sólido]

### Total Efectivo Invertido
| Artículo | Monto |
|---------|--------|
| Enganche | $[X] |
| Costos cierre (3-5%) | $[X] |
| Rehab/reparaciones | $[X] |
| Reservas (3 meses gastos) | $[X] |
| **Total efectivo necesario** | **$[X]** |

### Multiplicador Alquiler Bruto (GRM)
Precio Compra / Alquiler Bruto Anual = [X]
[Más bajo mejor — bajo 15 típicamente favorable]

### Verificación Regla 1%
Alquiler mensual / Precio compra = [X]%
[Objetivo: 1% o superior — $2,000/mes alquiler en compra $200K]

### Razón Cobertura Servicio Deuda (DSCR)
NOI / Servicio Deuda Anual = [X]
[Objetivo: 1.25+ para cobertura cómoda]
```

---

## Anti-Patrones

- **Ignorar vacancia** — asumir ocupancia 100% infla retornos. Siempre factor 5-10% vacancia.
- **Olvidar gestión propiedad** — incluso auto-gestionando, incluye costo. Tu tiempo valioso.
- **Sin reservas mantenimiento** — propiedades requieren reparos continuos. Presupuesta 5-10% alquiler bruto mínimo.
- **Usar estimados alquiler optimistas** — basa análisis comps mercado actual, no "qué podría ser después upgrades."
- **Ignorar gastos capital** — techos, HVAC y calentadores agua no son "si" gastos, son "cuándo."
- **Enamorarse propiedad** — decisiones inversión son matemática. Si números no funcionan, camina.

---

## Recuperación

- **Números borderline:** Negocia precio compra menor. Incluso $10-20K reducción puede cambiar retornos significativamente.
- **Flujo efectivo negativo precio actual:** Calcula precio compra break-even y úsalo máxima oferta.
- **Sin datos alquiler comparable:** Verifica estimados alquiler Zillow, Rentometer o llamada gestores propiedad local opiniones mercado.
- **Costos reparación inesperados descubiertos:** Ajusta total efectivo invertido recalcula todas métricas retorno antes proceder.
- **Alquiler mercado declinando:** Factor alquileres declinantes escenarios. Si acuerdo solo funciona alquileres subiendo, demasiado riesgoso.
