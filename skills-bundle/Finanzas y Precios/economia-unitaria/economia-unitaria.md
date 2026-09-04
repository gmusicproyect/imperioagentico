---
name: economia-unitaria
description: "Calcula la economía unitaria para productos y servicios con margen de contribución, período de payback, y ratios LTV:CAC. Usa cuando evalúes la rentabilidad de cada cliente o unidad."
allowed-tools: Read Write Glob
metadata:
  author: Imperio Digital
  version: "1.0"
---

# Economía Unitaria

## Cuándo Usar Este Skill

Usa este skill cuando necesites:
- Calcular la rentabilidad de cada cliente, venta o transacción
- Determinar LTV, CAC, margen de contribución, y período de payback
- Evaluar si tu modelo de negocio es fundamentalmente viable
- Preparar economía unitaria para presentaciones de inversores o decisiones estratégicas

**NO** uses este skill para proyecciones financieras agregadas (usa proyección-financiera) o estrategia de precios (usa estrategia-precios). Esto es para análisis de rentabilidad por unidad.

---

## Principio Fundamental

SI LA ECONOMÍA UNITARIA NO FUNCIONA PARA UN CLIENTE, NO FUNCIONA PARA MIL — EL ESCALA AMPLIFICA LA ECONOMÍA UNITARIA, NO LA ARREGLA.

---

## Fase 1: Información

### Información Requerida

| Entrada | Qué Preguntar | Por Defecto |
|---------|---------------|------------|
| **Modelo de negocio** | "¿Suscripción, compra única, marketplace, o servicio?" | No hay predeterminado — debe proporcionarse |
| **Ingresos promedio por cliente** | "¿Qué paga un cliente? (por mes, por compra, por proyecto)" | No hay predeterminado — debe proporcionarse |
| **Costo de adquirir cliente (CAC)** | "¿Cuánto gastas en marketing/ventas para obtener un cliente?" | No hay predeterminado — estima si desconocido |
| **Costo de servir cliente** | "¿Qué cuesta entregar el producto/servicio a un cliente?" | No hay predeterminado — debe proporcionarse |
| **Vida útil del cliente** | "¿Cuánto tiempo permanece un cliente? (meses para suscripciones, tasa de repetición para compras)" | 12 meses |
| **Margen bruto** | "¿Qué porcentaje de ingresos queda después de costos directos?" | Calculará |

**PUNTO DE CONTROL: No procedas sin ingresos por cliente y costo de servir.**

---

## Resumen de Entregables

Este skill proporciona:
1. Tabla de Economía Unitaria con LTV, CAC, margen de contribución
2. Evaluación de Salud comparando contra benchmarks de industria
3. Análisis de Sensibilidad mostrando qué maneja la aguja
4. Plan de Acción con prioridades para mejora

---

## Anti-Patrones

- **Usar LTV bruto sin restar costo de servir** — LTV debe representar ganancia bruta, no ingresos brutos
- **Mezclar CAC a través de todos los canales** — calcula CAC por canal. Tu CAC de Google Ads y CAC de referral son probablemente muy diferentes
- **Ignorar ingresos de expansión** — upsells y cross-sells aumentan LTV. Inclúyelos si el rastreo está disponible
- **Cálculos estáticos** — la economía unitaria cambia cuando escalas. Recalcula trimestralmente
- **Asumir churn constante** — el churn temprano suele ser más alto que churn tardío. El análisis de cohort da estimaciones de vida útil más exactas

---

## Recuperación

- **Sin datos de CAC:** Estima basado en gasto total de marketing dividido entre clientes nuevos. Comprométete a rastrear por canal en adelante
- **Sin datos de churn (compras únicas):** Usa tasa de compra repetida en su lugar. LTV = Valor de orden promedio x Número de compras de vida útil promedio
- **Economía unitaria negativa:** Identifica cuál palanca (precio, COGS, CAC, retención) es más fácil de arreglar. Muestra la matemática de qué necesita cambiar para alcanzar 3:1 LTV:CAC
- **Muy temprano (< 50 clientes):** Reconoce que los datos son preliminares. Usa números actuales como hipótesis y planifica validar con 3-6 meses de datos adicionales
