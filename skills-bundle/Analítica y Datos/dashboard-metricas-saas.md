---
name: dashboard-metricas-saas
description: "Configura dashboards de métricas/KPIs SaaS rastreando MRR, churn, LTV, CAC, ingresos de expansión y retención de cohort. Utiliza cuando construyas o mejores analítica de negocio de suscripción."
allowed-tools: Read Write Glob
metadata:
  author: Imperio Digital
  version: "1.0"
---

# Dashboard de Métricas SaaS

## Cuándo Usar Este Skill

Utiliza este skill cuando necesites:
- Definir y rastrear métricas SaaS principales para un negocio de suscripción
- Diseñar un diseño de dashboard de métricas con KPIs y visualizaciones
- Configurar análisis de retención de cohort y seguimiento de ingresos
- Crear una cadencia de reporteo para stakeholders o revisión personal

**NO** utilices este skill para modelos de pronóstico financiero, decks de reporteo a inversionistas o dashboards de analítica de marketing. Esto es para métricas de salud empresarial SaaS principal.

---

## Principio Fundamental

RASTREA LAS MÉTRICAS QUE IMPULSAN DECISIONES — UN DASHBOARD CON 50 MÉTRICAS ES UN DASHBOARD QUE NADIE USA. ENFÓCATE EN LOS 8-12 NÚMEROS QUE TE DICEN SI TU NEGOCIO ESTÁ SALUDABLE.

---

## Fase 1: Brief

### Entradas Requeridas

| Entrada | Qué Preguntar | Por Defecto |
|---------|--------------|------------|
| **Producto y precios** | "¿Cuál es tu producto SaaS y cuáles son los precios del plan?" | Sin valor por defecto — debe proporcionarse |
| **MRR actual** | "¿Cuál es tu ingreso recurrente mensual actual?" | Desconocido — establece seguimiento |
| **Modelo de facturación** | "¿Mensual, anual o ambos? ¿Algún componente basado en uso?" | Suscripciones mensuales |
| **Fuentes de datos** | "¿Dónde viven tus datos de facturación? ¿Stripe, Paddle, personalizado?" | Stripe |
| **Tamaño del equipo** | "¿Quién revisa este dashboard? ¿Solo tú o un equipo?" | Fundador solo |
| **Seguimiento actual** | "¿Qué métricas rastreas actualmente, si las hay?" | Solo ingresos |

**PUNTO DE CONTROL:** Confirma el brief antes de definir el marco de métricas.

---

## Fase 2: Definir Métricas

### Nivel 1: Debe-Rastrear (Revisión Diaria/Semanal)

| Métrica | Fórmula | Por Qué Importa |
|--------|---------|---------------|
| **MRR** | Suma de todo ingresos de suscripción activos | Indicador de salud principal |
| **Tasa de Crecimiento MRR** | (MRR este mes - MRR mes pasado) / MRR mes pasado | Velocidad de crecimiento |
| **Tasa de Churn** | Clientes perdidos / Clientes al inicio del período | Salud de retención |
| **Retención de Ingresos Netos** | (MRR inicio + expansión - contracción - churn) / MRR inicio | Crecimiento sin nuevas ventas |

### Nivel 2: Estratégico (Revisión Mensual)

| Métrica | Fórmula | Por Qué Importa |
|--------|---------|---------------|
| **LTV** | ARPU / Tasa churn mensual | Valor de vida del cliente |
| **CAC** | Gasto total de adquisición / Nuevos clientes adquiridos | Costo para adquirir |
| **Relación LTV:CAC** | LTV / CAC | Salud de economía unitaria (objetivo 3:1+) |
| **MRR de Expansión** | Ingresos de upgrades y add-ons | Crecimiento de clientes existentes |
| **ARPU** | MRR / Clientes activos | Ingresos promedio por usuario |

### Nivel 3: Inmersiones Profundas (Trimestral)

| Métrica | Fórmula | Por Qué Importa |
|--------|---------|---------------|
| **Retención de Cohort** | % de cohort aún activo en mes N | Retención verdadera en el tiempo |
| **Churn de Ingresos vs. Churn de Logo** | Ingresos perdidos vs. clientes perdidos | Revela si cuentas grandes o pequeñas se van |
| **Período de Recuperación** | CAC / (ARPU x Margen Bruto) | Meses para recuperar costo de adquisición |

**PUNTO DE CONTROL:** Confirma qué métricas incluir antes de diseñar el diseño.

---

## Fase 3: Diseñar el Dashboard

### Recomendaciones de Diseño

**Fila superior (tarjetas KPI):** MRR, Tasa de Crecimiento MRR, Clientes Activos, Tasa de Churn
**Segunda fila (gráficos):** Tendencia MRR (gráfico de línea, 12 meses), Desglose de ingresos (barra apilada: nuevo, expansión, contracción, churn)
**Tercera fila:** Tabla de retención de cohort (mapa de calor), Tendencia LTV:CAC
**Fila inferior:** Feed de actividad reciente (nuevos registros, churns, upgrades)

### Especificaciones de Dashboard

Para cada métrica, documenta:
- Nombre de métrica y definición
- Fuente de datos y método de cálculo
- Tipo de visualización (número, gráfico, tabla)
- Frecuencia de actualización (tiempo real, diario, mensual)
- Umbral de alerta (p. ej., churn excede 5%)

### Recomendaciones de Herramienta

| Herramienta | Mejor Para | Rango de Precio |
|------|----------|-------------|
| **Dashboard de Stripe** | MRR y churn básico | Gratis con Stripe |
| **Baremetrics/ChartMogul** | Métricas SaaS completas | $50-250/mes |
| **Google Sheets** | Cálculos personalizados | Gratis |
| **Notion** | Seguimiento manual para etapa temprana | Gratis-$10/mes |

---

## Fase 4: Pulir

### 1. Cadencia de Reporteo

```
## Cronograma de Revisión

- **Diario:** MRR, nuevos registros, churns (vistazo a tarjetas KPI)
- **Semanal:** Tasa de crecimiento MRR, conversiones de prueba, volumen de ticket de soporte
- **Mensual:** Revisión completa de dashboard, análisis de cohort, verificación LTV:CAC
- **Trimestral:** Inmersión profunda en cohorts de retención, tendencias CAC, disparador de evaluación de precios
```

### 2. Sistema de Alerta

Define alertas automatizadas:
- MRR cae más del 5% mes a mes
- Tasa de churn excede umbral objetivo
- Relación LTV:CAC cae por debajo de 3:1
- Sin nuevos registros por 3+ días consecutivos
- Cuenta grande cancela o reduce

### 3. Checklist de Calidad

```
## Checklist de Dashboard

- [ ] MRR se rastrea y actualiza diariamente
- [ ] Tasa de churn se calcula correctamente (logo e ingresos)
- [ ] LTV y CAC se definen con fórmulas claras
- [ ] Retención de ingresos netos se rastrea mensualmente
- [ ] Tabla de retención de cohort se configura (mínimo vista de 6 meses)
- [ ] Dashboard carga rápidamente y no es desordenado
- [ ] Alertas se configuran para umbrales críticos
- [ ] Cadencia de revisión se documenta y sigue
- [ ] Todas las métricas tienen definiciones claras (sin ambigüedad)
- [ ] La fuente de datos es confiable y automatizada (no entrada manual)
```

---

## Ejemplo

**Producto:** SaaS de gestión de proyectos, planes $19/$49/$99
**MRR:** $12,400
**Clientes:** 340 activos

**Diseño de Tarjeta KPI:**
```
| MRR: $12,400 (+8.2%) | Activos: 340 (+12) | Churn: 3.2% | ARPU: $36.47 |
```

**Ejemplo de alerta:**
"Alerta: La tasa de churn mensual alcanzó 4.1% (objetivo: bajo 3.5%). Tres cuentas en el plan de $99 se cancelaron esta semana. Revisa razones de cancelación en encuestas de salida."

---

## Anti-Patrones

- **Métricas de vanidad en el dashboard** — registros totales (todo el tiempo) no te dice nada. Rastrea clientes activos y MRR.
- **Entrada de datos manual** — si las métricas requieren actualizaciones manuales, se volverán obsoletas. Automatiza el pipeline de datos.
- **Demasiadas métricas** — máximo 8-12 métricas principales. Todo lo demás es un reporte, no un dashboard.
- **Sin definiciones** — si dos personas calculan churn diferentemente, la métrica es inútil. Documenta cada fórmula.
- **Ignorar cohorts** — el churn agregado oculta si la retención está mejorando con el tiempo. El análisis de cohort revela la verdad.

---

## Recuperación

- **Sin acceso a datos de facturación:** Comienza con un rastreador manual de Google Sheet. Registra MRR, nuevos clientes y churns semanalmente hasta que puedas automatizar.
- **Muy temprano para métricas significativas:** Rastrea MRR y cantidad de cliente. Añade churn y LTV una vez tengas 3+ meses de datos.
- **Múltiples modelos de precios:** Desglosa métricas por nivel de plan. Los promedios combinados ocultan problemas específicos de nivel.
- **Las métricas se ven mal:** Ese es el punto. Un dashboard que solo muestra buenos números no está haciendo su trabajo. Identifica la métrica peor y enfoca mejora ahí.