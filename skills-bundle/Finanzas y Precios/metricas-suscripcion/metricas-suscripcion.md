---
name: metricas-suscripcion
description: "Calcula e informa sobre métricas/KPIs de suscripción (MRR, ARR, churn rate) de suscripción incluyendo MRR, ARR, tasa de churn, LTV, y CAC. Usa cuando rastrées la salud de un negocio basado en suscripción."
allowed-tools: Read Write Glob
metadata:
  author: Imperio Digital
  version: "1.0"
---

# Métricas de Suscripción

## Cuándo Usar Este Skill

Usa este skill cuando necesites:
- Calcular métricas principales de negocio de suscripción (MRR, ARR, churn, LTV, CAC)
- Crear un dashboard o reporte de métricas de suscripción
- Analizar la salud de un negocio de ingresos recurrentes
- Identificar tendencias y áreas de mejora en desempeño de suscripción

**NO** uses este skill para negocios de compra única, reporte financiero general, o cálculos de ingresos ad hoc. Esto es para modelos de negocio de ingresos recurrentes.

---

## Principio Fundamental

LOS NEGOCIOS DE SUSCRIPCIÓN VIVEN Y MUEREN POR RETENCIÓN — EL CRECIMIENTO DE MRR NO SIGNIFICA NADA SI EL CHURN LO ESTÁ COMIENDO DESDE ABAJO.

---

## Resumen de Métricas de Suscripción

Este skill calcula:
- **Métricas de Ingresos:** MRR, ARR, nuevos MRR, MRR de expansión, tasa de crecimiento de MRR, ARPU
- **Métricas de Clientes:** Suscriptores activos, nuevos suscriptores, suscriptores cancelados, neto crecimiento de suscriptor, tasa de logo churn, tasa de churn de ingresos, retención de ingresos netos
- **Economía Unitaria:** CAC, LTV, relación LTV:CAC, período de payback, margen bruto

---

## Fase 1: Recopilación de Datos

### Información Requerida

| Entrada | Qué Preguntar | Por Defecto |
|---------|---------------|------------|
| **MRR actual** | "¿Cuál es tu ingresos recurrentes mensales actuales?" | No hay predeterminado — debe proporcionarse |
| **Total de suscriptores activos** | "¿Cuántos suscriptores pagadores tienes?" | No hay predeterminado — debe proporcionarse |
| **Nuevos suscriptores este mes** | "¿Cuántos suscriptores nuevos se unieron este mes?" | No hay predeterminado — debe proporcionarse |
| **Suscriptores cancelados este mes** | "¿Cuántos suscriptores cancelaron este mes?" | No hay predeterminado — debe proporcionarse |
| **Ingresos de expansión** | "¿Algún ingresos de actualización o add-on este mes?" | $0 |
| **Gasto total de marketing** | "¿Cuánto gastaste en adquisición este mes?" | No hay predeterminado — estima si desconocido |
| **Tiers de precios** | "¿Cuáles son tus puntos de precio de suscripción?" | Tier único |

**PUNTO DE CONTROL: No procedas sin MRR, contador de suscriptor, nuevos suscriptores, y suscriptores cancelados.**

---

## Fase 2: Cálculos de Métricas Principales

[Incluir tablas de cálculo]

---

## Anti-Patrones

- **Calcular LTV con churn de ingresos en lugar de churn de logo** — usa el tipo de churn correcto para la métrica correcta. Churn de ingresos para LTV de ingresos.
- **Ignorar ingresos de expansión** — retención de ingresos netos es una métrica más significativa que churn bruto solo
- **Métricas mensuales sin tendencias** — un mes de datos es una captura instantánea, no insight. Rastrea al menos 3-6 meses para tendencias.
- **Mezclar usuarios libres y pagos** — solo incluye suscriptores pagadores en estos cálculos. Los usuarios libres son una etapa de embudo diferente.
- **Usar promedios cuando los cohorts difieren** — si tienes múltiples tiers de precios, calcula métricas por tier. Los promedios mezclados ocultan problemas.

---

## Recuperación

- **Sin datos históricos:** Comienza a rastrear ahora. Crea el primer reporte como línea base y comprométete a actualizaciones mensuales.
- **Muy temprana (< 50 suscriptores):** Los tamaños de muestra pequeños hacen que los porcentajes sean poco confiables. Reporta números crudos junto a porcentajes e indica la advertencia de tamaño de muestra.
- **Datos de churn no disponibles:** Usa cambio neto de suscriptor como proxy. Configura rastreo de churn apropiado inmediatamente — esta es tu métrica más importante.
- **Modelo freemium:** Separa completamente métricas libres y pagadas. Rastrea tasa de conversión libre-a-pagada como KPI adicional.
