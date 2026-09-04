---
name: metricas-marketplace
description: "Define y rastrea métricas/KPIs de salud de marketplace incluyendo liquidez, take rate, GMV y balance de oferta/demanda. Utiliza cuando midas y optimices desempeño de marketplace."
allowed-tools: Read Write Glob
metadata:
  author: Imperio Digital
  version: "1.0"
---

# Métricas de Marketplace

## Cuándo Usar Este Skill

Utiliza este skill cuando necesites:
- Definir las métricas de salud central para un marketplace bilateral
- Construir un dashboard de métricas para rastrear desempeño de marketplace
- Identificar desbalances oferta/demanda y problemas de liquidez
- Crear marcos de reporteo para análisis de crecimiento de marketplace

**NO** utilices este skill para métricas de SaaS (usa saas-metrics-dashboard), modelado financiero o reporteo a inversionistas. Esto es para métricas operacionales de salud de marketplace.

---

## Principio Fundamental

LA SALUD DEL MARKETPLACE NO SE TRATA DE USUARIOS TOTALES — SE TRATA DE SI LA OFERTA Y DEMANDA SE ESTÁN ENCONTRANDO ENTRE SÍ. LA LIQUIDEZ ES LA MÉTRICA QUE MÁS IMPORTA.

---

## Fase 1: Brief

### Entradas Requeridas

| Entrada | Qué Preguntar | Por Defecto |
|---------|--------------|------------|
| **Tipo de marketplace** | "¿Qué conecta tu marketplace?" | Sin valor por defecto — debe proporcionarse |
| **Modelo de transacción** | "¿Cómo funcionan las transacciones? Compra instantánea, reserva, subasta, mensajería?" | Compra instantánea |
| **Modelo de ingresos** | "¿Comisión, suscripción, cuota de listado o híbrido?" | Comisión |
| **Escala actual** | "¿Cuántos compradores activos, vendedores y transacciones mensuales?" | Pre-lanzamiento o etapa temprana |
| **Alcance geográfico** | "¿Mercado único o múltiples mercados?" | Mercado único |
| **Preocupación clave** | "¿De qué estás más preocupado? Oferta, demanda o matching?" | Balance oferta/demanda |

**PUNTO DE CONTROL:** Confirma el brief antes de definir el marco de métricas.

---

## Fase 2: Definir Métricas Principales

### Nivel 1: Salud del Marketplace (Rastrea Semanalmente)

| Métrica | Fórmula | Qué Te Dice |
|--------|---------|-------------------|
| **GMV** | Valor total de todas las transacciones | Tamaño general del marketplace |
| **Take Rate** | Ingresos de plataforma / GMV | Cuánto capturas por dólar transaccionado |
| **Liquidez** | % de listados que resultan en transacción dentro de 30 días | Si la oferta cumple con la demanda |
| **Relación Oferta/Demanda** | Vendedores activos / Compradores activos | Balance entre lados |
| **Tasa de Match** | Búsquedas de comprador que resultan en listado relevante / Búsquedas totales | Si los compradores encuentran lo que quieren |

### Nivel 2: Específico de Lado (Rastrea Mensualmente)

**Métricas de Oferta:**

| Métrica | Fórmula | Objetivo |
|--------|---------|--------|
| Vendedores activos | Vendedores con al menos 1 listado en 30 días | Crecimiento mes a mes |
| Listados por vendedor | Listados totales / Vendedores activos | 3-5+ para marketplaces de producto |
| Tasa de activación de vendedor | Nuevos vendedores con primera transacción / Nuevos registros de vendedor | 30%+ |
| Retención de vendedor | Vendedores activos este mes que fueron activos mes pasado | 70%+ |

**Métricas de Demanda:**

| Métrica | Fórmula | Objetivo |
|--------|---------|--------|
| Compradores activos | Compradores con al menos 1 transacción en 30 días | Crecimiento mes a mes |
| Frecuencia de comprador | Transacciones por comprador por mes | Aumentando con el tiempo |
| Tasa de activación de comprador | Nuevos compradores con primera transacción / Nuevos registros de comprador | 20%+ |
| Tasa de comprador recurrente | Compradores con 2+ transacciones / Compradores totales | 30%+ |

### Nivel 3: Economía Unitaria (Rastrea Trimestralmente)

| Métrica | Fórmula | Objetivo |
|--------|---------|--------|
| **Buyer LTV** | Gasto promedio por comprador sobre vida útil | 3x+ buyer CAC |
| **Seller LTV** | Ingresos promedio generados por vendedor sobre vida útil | 3x+ seller CAC |
| **Buyer CAC** | Gasto total de adquisición de comprador / Nuevos compradores | Sostenible relativo a LTV |
| **Seller CAC** | Gasto total de adquisición de vendedor / Nuevos vendedores | Típicamente más bajo que buyer CAC |
| **Margen de contribución** | (Ingresos de take rate - costos variables) / GMV | Positivo y mejorando |

**PUNTO DE CONTROL:** Confirma qué métricas priorizar antes de diseñar el dashboard.

---

## Fase 3: Construir el Dashboard

### Diseño de Dashboard

**Fila superior (tarjetas KPI):**
GMV | Take Rate | Liquidez | Compradores Activos | Vendedores Activos

**Fila 2 (Tendencias):**
- Tendencia de GMV (12 meses, gráfico de línea)
- Tendencia oferta vs. demanda (gráfico de línea de doble eje)

**Fila 3 (Indicadores de salud):**
- Liquidez por categoría (gráfico de barras)
- Tendencia de tasa de match (gráfico de línea)
- Embudos de activación comprador/vendedor (gráficos de embudo)

**Fila 4 (Análisis de cohort):**
- Retención de cohort de comprador (mapa de calor)
- Retención de cohort de vendedor (mapa de calor)

### Umbrales de Alerta

| Métrica | Alerta Cuando | Causa Posible |
|--------|-----------|----------------|
| Liquidez cae por debajo de 20% | Oferta excede demanda | Demasiados vendedores, insuficientes compradores |
| Relación oferta/demanda excede 5:1 | Sobre-oferta | Adquisición de vendedor superando demanda |
| Tasa de match por debajo de 50% | Selección pobre o búsqueda | Brechas de categoría o algoritmo de búsqueda malo |
| Tasa de comprador recurrente por debajo de 20% | Satisfacción baja de comprador | Problemas de calidad o brechas de confianza |
| Take rate en declive | Presión competitiva | Vendedores negociando o transaccionando fuera de plataforma |

---

## Fase 4: Pulir

### 1. Marco Diagnóstico de Marketplace

Cuando una métrica se ve mal, diagnostica con este diagrama de flujo:

**GMV es plano o declina:**
→ Verifica cuenta de comprador. ¿Está creciendo? Si no → problema de demanda.
→ Verifica valor promedio de transacción. ¿Está cayendo? Si sí → cambio de precios o mix.
→ Verifica frecuencia de transacción. ¿Está cayendo? Si sí → problema de engagement o calidad.

**Liquidez es baja:**
→ ¿Demasiada oferta? → Aumenta barra de calidad de vendedor, pausa reclutamiento de vendedor.
→ ¿Insuficiente demanda? → Aumenta gasto de adquisición de comprador.
→ ¿Problema de matching? → Mejora búsqueda, categorías o recomendaciones.

### 2. Plantilla de Reporteo

```
## Reporte Mensual de Marketplace — [Mes Año]

### Métricas Clave
| Métrica | Este Mes | Mes Pasado | Cambio |
|--------|-----------|-----------|--------|
| GMV | | | |
| Take Rate | | | |
| Liquidez | | | |
| Compradores Activos | | | |
| Vendedores Activos | | | |
| Tasa de Comprador Recurrente | | | |

### Destacados
- [Logro principal o hito]
- [Crecimiento en una métrica clave]

### Preocupaciones
- [Métrica tendiendo en dirección equivocada]
- [Acción siendo tomada para abordarlo]

### Enfoque para Próximo Mes
1. [Prioridad 1]
2. [Prioridad 2]
```

### 3. Checklist de Calidad

```
## Checklist de Métricas de Marketplace

- [ ] GMV rastreado y tendencia mensual
- [ ] Take rate calculado correctamente (ingresos / GMV)
- [ ] Liquidez medida por categoría (no solo general)
- [ ] Oferta y demanda rastreadas por separado con tasas de activación
- [ ] Tasa de match o tasa de éxito de búsqueda se mide
- [ ] Retención de comprador y vendedor rastreada por cohort
- [ ] Economía unitaria (LTV, CAC) calculada trimestralmente
- [ ] Umbrales de alerta establecidos para métricas críticas
- [ ] Plantilla de reporteo mensual está en uso
- [ ] Marco diagnóstico disponible para cuando las métricas declinen
```

---

## Ejemplo

**Marketplace:** Servicios para el hogar local
**Snapshot mensual:**
```
GMV: $145,000 (+12% MoM)
Take Rate: 14%
Ingresos de Plataforma: $20,300
Liquidez: 34% (34 de 100 contratistas listados obtuvieron una reserva)
Compradores Activos: 280
Vendedores Activos: 100
Relación Oferta/Demanda: 1:2.8
Tasa de Comprador Recurrente: 41%
```

**Diagnóstico:** "Liquidez a 34% sugiere que tenemos más contratistas que la demanda de comprador puede absorber. Recomendación: pausa reclutamiento de contratistas, aumenta gasto de adquisición de comprador 30%, y lanza programa de referencia para compradores."

---

## Anti-Patrones

- **Rastrear GMV sin take rate** — GMV significa nada si no capturas ingresos. Siempre emparéjalos.
- **Ignorar liquidez** — un marketplace con 10,000 listados y sin transacciones es un cementerio. La liquidez es el verdadero indicador de salud.
- **Tratar ambos lados igual** — las métricas de comprador y vendedor deben rastrearse por separado. Un lado de comprador saludable puede enmascarar un lado de vendedor muriendo.
- **Métricas de vanidad** — registros totales, pageviews y descargas de app no te dicen nada sobre salud de marketplace. Rastrea actividad y transacciones.
- **Sin análisis de cohort** — la retención agregada oculta si las cohorts nuevas se desempeñan mejor o peor que las antiguas.

---

## Recuperación

- **Sin datos de transacción aún (pre-lanzamiento):** Rastrea métricas del lado de oferta (listados, registros de vendedor, calidad de listado) y señales de demanda (registros waitlist, consultas de búsqueda).
- **Liquidez muy baja:** Estrecha el alcance del marketplace. Enfócate en una categoría o geografía hasta que liquidez exceda 30%.
- **No puedes calcular LTV aún:** Comienza con valor de transacción promedio y tasa recurrente. El cálculo de LTV se vuelve significativo después de 6+ meses de datos.
- **Las métricas son inconsistentes:** Define cada fórmula en un diccionario de datos. Asegura que definiciones de comprador, vendedor y transacción se usen consistentemente.