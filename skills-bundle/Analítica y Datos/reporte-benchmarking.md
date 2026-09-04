---
name: reporte-benchmarking
description: "Crea reportes de benchmarking industriales comparando métricas de negocio contra estándares y mejores desempeños. Utiliza cuando evalúes cómo se compara tu negocio versus competidores."
allowed-tools: Read Write Glob
metadata:
  author: Imperio Digital
  version: "1.0"
---

# Reporte de Benchmarking

## Cuándo Usar Este Skill

Utiliza este skill cuando necesites:
- Comparar tus métricas de negocio contra promedios industriales
- Identificar brechas de desempeño relativas a competidores de mejor desempeño
- Establecer objetivos realistas basados en puntos de referencia externos
- Crear un reporte de benchmarking para inversionistas, junta directiva o planificación interna

**NO** utilices este skill para recopilación de inteligencia competitiva, auditoría financiera o investigación de mercado. Esto es para comparar tus métricas contra puntos de referencia conocidos.

---

## Principio Fundamental

LOS PUNTOS DE REFERENCIA PROPORCIONAN CONTEXTO, NO RESPUESTAS — UNA MÉTRICA POR DEBAJO DEL PUNTO DE REFERENCIA ES UNA SEÑAL PARA INVESTIGAR, NO AUTOMÁTICAMENTE UN PROBLEMA A ARREGLAR.

---

## Fase 1: Brief

### Entradas Requeridas

| Entrada | Qué Preguntar | Por Defecto |
|---------|--------------|------------|
| **Industria** | "¿En qué industria estás?" | Debe proporcionarse |
| **Modelo de negocio** | "¿SaaS, e-commerce, servicios, marketplace u otro?" | Debe proporcionarse |
| **Métricas a comparar** | "¿Qué métricas quieres comparar? (tasa de crecimiento, márgenes, churn, CAC, conversión)" | Métricas financieras principales + crecimiento |
| **Tus números actuales** | "Comparte tu desempeño actual para cada métrica." | Debe proporcionarse |
| **Etapa de la empresa** | "¿Qué etapa? (pre-ingresos, temprana, crecimiento, madura)" | Etapa temprana |
| **Grupo de pares** | "¿Hay empresas específicas o cohort contra la que quieras comparar?" | Promedios industriales |

**PUNTO DE CONTROL:** Confirma el brief y la lista de métricas antes de continuar.

---

## Fase 2: Investigar

### Fuentes de Puntos de Referencia

Extrae puntos de referencia de estos tipos de fuente (nota la fuente para cada número):
- Reportes industriales (SaaS Benchmarks, reportes de Shopify, etc.)
- Presentaciones de empresa pública (para comparaciones de negocio maduro)
- Datos de encuesta agregados (OpenView, ChartMogul, ProfitWell)
- Puntos de referencia publicados de acelerador/VC (YC, a16z, First Round)

### Categorías de Punto de Referencia

1. **Métricas de crecimiento** — tasa de crecimiento de ingresos, crecimiento de clientes, expansión MRR
2. **Economía unitaria** — CAC, LTV, relación CAC:LTV, período de recuperación
3. **Retención** — tasa de churn, retención de ingresos netos, retención de logo
4. **Rentabilidad** — margen bruto, margen operativo, tasa de quema
5. **Eficiencia** — ingresos por empleado, número mágico, Regla de 40

**PUNTO DE CONTROL:** Presenta los datos de punto de referencia con fuentes y confirma antes de comparar con métricas del usuario.

---

## Fase 3: Construir

### Entregables

**1. Scorecard de Benchmarking**
| Métrica | Tu Número | Mediana Industrial | Cuartil Superior | Estado |
|--------|------------|----------------|--------------|--------|
| Crecimiento anual | 40% | 25% | 80% | Por encima de mediana |
| Margen bruto | 65% | 70% | 85% | Por debajo de mediana |
| Churn mensual | 5% | 3% | 1.5% | Por debajo de mediana |

**2. Análisis de Brecha**
Para cada métrica por debajo de la mediana:
- Cuán por debajo y qué significa en términos de dólares
- Causas probables basadas en contexto de empresa
- Estrategias específicas de mejora

**3. Reconocimiento de Fortalezas**
Para cada métrica por encima de la mediana:
- Qué está impulsando el desempeño fuerte
- Cómo proteger y extender la ventaja

**4. Recomendaciones de Establecimiento de Objetivos**
- Objetivos de 12 meses por métrica basados en trayectorias realistas de mejora
- Clasificación de prioridad: qué brechas cerrar primero para máximo impacto en el negocio

---

## Fase 4: Pulir

### Formato de Reporte

Presenta en un formato apropiado para la audiencia:
- **Deck de inversionista:** 2-3 diapositivas con scorecard y narrativa
- **Planificación interna:** Reporte completo con análisis de brecha y plan de acción
- **Reunión de junta directiva:** Resumen ejecutivo con top 3 fortalezas y top 3 brechas

### Cronograma de Actualización

Los puntos de referencia cambian con el tiempo. Recomienda ejecutar el análisis nuevamente:
- Anualmente para industrias estables
- Semestralmente para sectores de movimiento rápido
- Después de cambios importantes de modelo de negocio

---

## Ejemplo 1: Startup de SaaS (etapa Series A)

**Puntos de referencia utilizados:** OpenView SaaS Benchmarks, medianas de ChartMogul
**Hallazgo clave:** Tasa de crecimiento por encima de mediana pero churn es 2x el punto de referencia — el crecimiento está enmascarando un problema de retención.

## Ejemplo 2: Marca de E-commerce (2 años, $1M ingresos)

**Puntos de referencia utilizados:** Datos de comercio de Shopify, rangos de margen bruto industrial
**Hallazgo clave:** AOV por encima del punto de referencia, tasa de conversión por debajo — los precios son fuertes pero la experiencia del sitio necesita trabajo.

---

## Anti-Patrones

- **Comparar manzanas y naranjas** — una empresa bootstrapped de 5 personas no debería compararse con una empresa financiada por VC de 200 personas. Iguala el grupo de pares.
- **Usar puntos de referencia desactualizados** — puntos de referencia SaaS de 2019 no reflejan la realidad del mercado post-2020. Usa los datos más recientes disponibles.
- **Adoración de punto de referencia** — estar por debajo de un punto de referencia es una señal para investigar, no una garantía de que algo esté mal. El contexto importa.
- **Ignorar tus fortalezas** — fijarse en brechas mientras se ignoran desempeños por encima del punto de referencia pierde el panorama estratégico.
- **Demasiadas métricas** — hacer benchmarking de 30 métricas diluye el enfoque. Elige las 5-8 que más importan para tu etapa y modelo.

---

## Recuperación

- **Sin datos de punto de referencia para el nicho:** Usa puntos de referencia de industria adyacente y nota la aproximación. Algo es mejor que nada.
- **Todas las métricas por debajo del punto de referencia:** Prioriza la 1-2 métricas con el mayor impacto en ingresos. Arregla esas primero.
- **El usuario disputa los puntos de referencia:** Discute la fuente y metodología. Ofrece múltiples fuentes para triangulación.
- **Los puntos de referencia hacen que el usuario se sienta atrás:** Reencuadra — los puntos de referencia muestran el camino, no la línea de meta. La mayoría de las empresas están por debajo de la mediana en algo.