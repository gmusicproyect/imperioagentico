---
name: analisis-cohort
description: "Crea marcos de análisis de cohort para entender retención, ingresos y patrones de comportamiento a lo largo del tiempo. Utiliza cuando midas cómo se desempeñan grupos de usuarios a lo largo de su ciclo de vida."
allowed-tools: Read Write Glob
metadata:
  author: Imperio Digital
  version: "1.0"
---

# Análisis de Cohort

## Cuándo Usar Este Skill

Utiliza este skill cuando necesites:
- Entender tendencias de retención de clientes por mes de registro
- Comparar desempeño de ingresos en cohorts de adquisición
- Identificar qué grupos de clientes se comportan diferentemente en el tiempo
- Construir un marco de análisis de cohort repetible para uso continuo

**NO** utilices este skill para métricas de snapshot único, análisis de cliente individual o monitoreo en tiempo real. Esto es para análisis longitudinal basado en grupos.

---

## Principio Fundamental

LOS PROMEDIOS MIENTEN — EL ANÁLISIS DE COHORTE REVELA SI TU NEGOCIO REALMENTE ESTÁ MEJORANDO COMPARANDO CÓMO DIFERENTES GRUPOS SE COMPORTAN SOBRE LA MISMA ETAPA DEL CICLO DE VIDA.

---

## Fase 1: Brief

### Entradas Requeridas

| Entrada | Qué Preguntar | Por Defecto |
|---------|--------------|------------|
| **Objetivo del análisis** | "¿Qué estás tratando de entender? (retención, ingresos, engagement, churn)" | Retención de cliente |
| **Definición de cohort** | "¿Cómo deberían agruparse las cohorts? (mes de registro, canal de adquisición, nivel de plan)" | Mes de registro |
| **Granularidad de tiempo** | "¿Cohorts semanales, mensuales o trimestrales?" | Mensual |
| **Ventana de observación** | "¿Cuántos períodos rastrear cada cohort?" | 6 meses |
| **Fuente de datos** | "¿Dónde están tus datos de cliente? (Stripe, CRM, base de datos, hoja de cálculo)" | Hoja de cálculo o Stripe |
| **Métrica** | "¿Qué métrica por cohort? (usuarios activos, ingresos, pedidos, logins)" | Usuarios activos (retención) |

**PUNTO DE CONTROL:** Confirma el brief antes de continuar.

---

## Fase 2: Diseñar

### Estructura de Tabla de Cohort

Construye una matriz triangular:
- **Filas** = cohorts (p. ej., registros de enero, registros de febrero)
- **Columnas** = períodos de ciclo de vida (Mes 0, Mes 1, Mes 2...)
- **Celdas** = valor de métrica o porcentaje

### Marco de Análisis

1. **Curva de retención** — cómo declina cada cohort en el tiempo (o no)
2. **Comparación de cohort** — ¿retienen mejor las cohorts más nuevas que las antiguas?
3. **Puntos de inflexión** — ¿dónde ocurre el mayor abandono?
4. **Estabilización** — ¿en qué período se estabilizan las cohorts?
5. **Superposiciones de segmento** — ¿retienen diferentemente segmentos específicos (canal, plan, geografía)?

**PUNTO DE CONTROL:** Presenta el marco de análisis y confirma antes de construir plantillas.

---

## Fase 3: Construir

### Entregables

**1. Plantilla de Análisis de Cohort**
- Estructura de hoja de cálculo o tabla lista para entrada de datos
- Fórmulas para calcular porcentajes de retención
- Reglas de formato condicional (verde = buena retención, rojo = caída pronunciada)
- Plantilla de gráfico para visualizar curvas de retención

**2. Guía de Interpretación**
- Cómo leer la tabla de cohort (filas, columnas, patrones diagonales)
- Qué se ve "bien" de retención para el tipo de negocio
- Patrones comunes y qué significan:
  - Las filas mejoran = el producto está mejorando
  - Caída pronunciada de Mes 1 = problema de onboarding
  - Curvas planas después del Mes 3 = retención central saludable

**3. Plan de Análisis Segmentado**
- Qué segmentos superponer (fuente de adquisición, nivel de precio, geografía)
- Cómo dividir cohorts para sub-análisis
- Plantilla de comparación para segmento vs. segmento

**4. Marco de Recomendaciones de Acción**
- Si la retención de Mes 1 está por debajo de X%, enfócate en onboarding
- Si la retención se estabiliza en Y%, invierte en expansión sobre adquisición
- Si cohorts más nuevas son peores, investiga cambios de producto o mercado

---

## Fase 4: Pulir

### Cadencia de Reporteo

- Mensual: actualiza la tabla de cohort con datos del período más reciente
- Trimestral: análisis completo con superposiciones de segmento y narrativa de tendencia
- Disparador: ejecuta análisis ad hoc cuando se hace un cambio importante (precios, onboarding, producto)

### Plantilla de Presentación

Resumen de una página con: tabla de cohort, gráfico de curva de retención, top 3 insights y acciones recomendadas.

---

## Ejemplo 1: Cohorts de Retención Mensuales de SaaS

Cohorts por mes de registro. Métrica: % de usuarios activos en cada mes subsecuente. Objetivo: identificar si las mejoras de onboarding en marzo mejoraron la retención de Mes 1 vs. cohort de enero.

## Ejemplo 2: Cohorts de Ingresos de E-commerce

Cohorts por mes de primera compra. Métrica: ingresos acumulados por cohort. Objetivo: entender qué canales de adquisición producen clientes de mayor valor de vida útil.

---

## Anti-Patrones

- **Usar promedios en lugar de cohorts** — "La retención promedio es 40%" oculta si las cosas están mejorando o empeorando. Siempre divide por cohort.
- **Demasiadas cohorts** — 52 cohorts semanales en un gráfico es ilegible. Comienza mensual, ve semanal solo para investigaciones específicas.
- **Ignorar tamaño de cohort** — una cohort de 5 usuarios con 80% de retención no es significativa. Nota tamaños de muestra.
- **Comparar diferentes etapas del ciclo de vida** — Mes 3 de una cohort de enero y Mes 1 de una cohort de marzo no son comparables. Alinea por período.
- **Análisis sin acción** — los datos de cohort son diagnósticos. Siempre termina con "¿Así que qué hacemos al respecto?"

---

## Recuperación

- **No hay suficientes datos:** Necesita mínimo 3 cohorts con 3 períodos cada una. Si los datos son escasos, comienza a rastrear ahora y revisa en 3 meses.
- **Sin datos a nivel de cliente:** Usa proxies agregados (usuarios activos mensuales vs. registros) para una vista de cohort aproximada. Planifica implementar seguimiento adecuado.
- **La retención se ve terrible:** Normaliza expectativas — las aplicaciones B2C a menudo ven retención de 20-30% de Mes 1. Compara con puntos de referencia industriales antes de entrar en pánico.
- **El usuario no puede interpretar la tabla:** Camina por una fila en detalle, explicando qué significa cada celda para esa cohort específica.