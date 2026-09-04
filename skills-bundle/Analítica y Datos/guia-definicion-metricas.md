---
name: guia-definicion-metricas
description: "Crea glosarios de métricas definiendo cómo se calcula, rastrea e interpreta cada KPI de negocio con fórmulas, fuentes de datos y propiedad. Utiliza para alineación de equipo en números."
allowed-tools: Read Write Glob
metadata:
  author: Imperio Digital
  version: "1.0"
---

# Guía de Definición de Métricas

## Cuándo Usar Este Skill

Utiliza este skill cuando necesites:
- Definir cómo se calcula y rastrea cada métrica de negocio
- Crear un glosario de métricas para alineación de equipo
- Resolver desacuerdos sobre qué significa un número
- Incorporar nuevos miembros del equipo sobre cómo interpretar KPIs clave

**NO** utilices este skill para construir dashboards, analizar datos o establecer objetivos. Esto es para definir qué significan las métricas y cómo se calculan.

---

## Principio Fundamental

SI DOS PERSONAS EN TU EMPRESA CALCULAN LA MISMA MÉTRICA DIFERENTEMENTE, NO TIENES UNA MÉTRICA — TIENES CONFUSIÓN. DEFINE UNA VEZ, USA EN TODAS PARTES.

---

## Fase 1: Brief

### Entradas Requeridas

| Entrada | Qué Preguntar | Por Defecto |
|---------|--------------|------------|
| **Métricas a definir** | "¿Qué KPIs rastrea tu equipo o debería rastrear?" | Debe proporcionarse |
| **Modelo de negocio** | "¿SaaS, e-commerce, servicios, marketplace?" | Debe proporcionarse |
| **Fuentes de datos** | "¿Dónde viven tus datos? (Stripe, GA4, CRM, hojas de cálculo)" | Múltiples |
| **Audiencia** | "¿Quién usará esta guía? (equipo completo, liderazgo, nuevas incorporaciones)" | Equipo completo |
| **Confusión conocida** | "¿Hay métricas que tu equipo define o calcula diferentemente?" | Desalineación general |

**PUNTO DE CONTROL:** Confirma la lista de métricas antes de continuar.

---

## Fase 2: Definir

### Plantilla de Definición de Métrica

Para cada métrica, documenta:

1. **Nombre** — el nombre oficial de la métrica (un nombre, sin sinónimos en reporteo oficial)
2. **Definición** — explicación en lenguaje simple de una oración
3. **Fórmula** — cálculo exacto con numerador y denominador especificados
4. **Fuente de datos** — dónde vienen los números
5. **Frecuencia** — con qué frecuencia se calcula (diario, semanal, mensual)
6. **Propietario** — quién es responsable de rastrear e informar esta métrica
7. **Objetivo/punto de referencia** — qué se ve "bien"
8. **Notas de interpretación** — advertencias, quirks conocidos, patrones estacionales

**PUNTO DE CONTROL:** Presenta las primeras 3-5 definiciones para aprobación de formato antes de completar la guía completa.

---

## Fase 3: Construir

### Entregables

**1. Glosario Completo de Métricas**
- Todas las métricas definidas usando la plantilla estándar
- Organizado por categoría (crecimiento, ingresos, engagement, operaciones)
- Formato searchable (tabla de contenidos con enlaces de anclaje)

**2. Mapa de Relación de Métricas**
- Cómo se relacionan las métricas (p. ej., el churn afecta LTV que afecta relación CAC:LTV)
- Clasificación de indicador adelantado vs. rezagado
- Qué métricas observar juntas

**3. Ejemplos de Cálculo**
- Ejemplo resuelto para cada fórmula usando datos de muestra realistas
- Casos límite: qué sucede con valores cero, números negativos o datos faltantes

**4. Tarjeta de Referencia Rápida**
- Resumen de una página con nombres de métricas, fórmulas y objetivos
- Diseñado para referencia de escritorio o mensaje de Slack fijado

---

## Fase 4: Pulir

### Revisión y Gobernanza

- Revisa definiciones trimestralmente para precisión
- Cuando se propone una nueva métrica, debe pasar por la plantilla de definición antes de entrar en cualquier reporte
- Control de versión: marca de fecha de actualizaciones y notas de cambios

### Integración de Onboarding

Incluye la guía de métricas en onboarding de nuevas incorporaciones. Programa un recorrido de 30 minutos de las 10 principales métricas durante la primera semana.

---

## Ejemplo 1: Métricas de SaaS

**MRR:** Ingreso Recurrente Mensual. Suma de todos los montos de suscripción activa a fin de mes. Fuente: Stripe. Mensual. Objetivo: 10% crecimiento MoM.
**Tasa de Churn:** Clientes perdidos / Clientes al inicio del período. Fuente: Stripe + CRM. Mensual. Objetivo: Menos de 3%.
**NRR:** Retención de Ingresos Netos. (MRR inicial + Expansión - Contracción - Churn) / MRR inicial. Fuente: Stripe. Mensual. Objetivo: Más de 110%.

## Ejemplo 2: Métricas de E-commerce

**AOV:** Valor Promedio de Pedido. Ingresos Totales / Número de Pedidos. Fuente: Shopify. Semanal. Objetivo: $75+.
**Tasa de Conversión:** Pedidos / Sesiones. Fuente: GA4 + Shopify. Semanal. Objetivo: 2-3%.
**ROAS:** Retorno en Gasto de Publicidad. Ingresos de Anuncios / Gasto de Anuncios. Fuente: Plataformas de anuncios + Shopify. Semanal. Objetivo: 3x+.

---

## Anti-Patrones

- **Múltiples definiciones para la misma métrica** — si marketing calcula "clientes" diferentemente que finanzas, los reportes nunca estarán de acuerdo. Una definición por métrica.
- **Denominadores sin definir** — "tasa de conversión" significa nada sin especificar qué divide qué en qué período de tiempo.
- **Conocimiento tribal** — si solo una persona sabe cómo se calcula una métrica, no es una métrica, es la opinión de esa persona.
- **Demasiadas métricas** — 50 KPIs significa cero enfoque. Define 8-12 métricas primarias y categoriza el resto como apoyo.
- **Nunca actualizar definiciones** — a medida que el negocio cambia, las definiciones de métricas deben evolucionar. Revisa trimestralmente.

---

## Recuperación

- **El equipo no puede ponerse de acuerdo en una definición:** Presenta 2-3 opciones con pros y contras. Deja que el responsable de la decisión elija una y documéntala como estándar.
- **Las fuentes de datos dan números diferentes:** Identifica la fuente de discrepancia. Elige un sistema de registro para cada métrica y documenta por qué.
- **Demasiadas métricas para definir:** Comienza con las 10 métricas que aparecen en el reporteo de liderazgo. Añade otras en lotes.
- **El usuario inseguro de qué métricas importan:** Comienza con las métricas estándar del modelo de negocio (SaaS: MRR, churn, CAC, LTV; E-commerce: AOV, conversión, ROAS, tasa de repetición).