---
name: diseno-dashboard-datos
description: "Planifica diseños de dashboards de KPIs de datos con selección de métricas, tipos de visualización, frecuencia de actualización y diseño enfocado en el usuario. Utiliza cuando construyas dashboards que impulsen decisiones."
allowed-tools: Read Write Glob
metadata:
  author: Imperio Digital
  version: "1.0"
---

# Diseño de Dashboard de Datos

## Cuándo Usar Este Skill

Utiliza este skill cuando necesites:
- Diseñar un diseño de dashboard de métricas de negocio
- Seleccionar las visualizaciones correctas para diferentes tipos de métricas
- Planificar una jerarquía de dashboard (ejecutivo, operacional, a nivel de equipo)
- Especificar requisitos para un desarrollador o configuración de herramienta BI

**NO** utilices este skill para construir dashboards en código, crear gráficos reales o configurar herramientas BI específicas. Esto es para planificación y diseño de dashboards.

---

## Principio Fundamental

UN DASHBOARD QUE REQUIERE EXPLICACIÓN HA FRACASADO — TODA MÉTRICA DEBERÍA RESPONDER UNA PREGUNTA QUE EL ESPECTADOR YA TIENE EN 5 SEGUNDOS O MENOS.

---

## Fase 1: Brief

### Entradas Requeridas

| Entrada | Qué Preguntar | Por Defecto |
|---------|--------------|------------|
| **Audiencia** | "¿Quién verá este dashboard? (fundador, líderes de equipo, inversionistas, equipo completo)" | Fundador / CEO |
| **Propósito** | "¿Qué decisiones debería informar este dashboard?" | Revisión semanal de salud comercial |
| **Preguntas clave** | "¿Qué 3-5 preguntas debería alguien responder mirando esto?" | Debe proporcionarse |
| **Fuentes de datos** | "¿Dónde viven tus datos? (Stripe, GA4, CRM, hojas de cálculo)" | Múltiples fuentes |
| **Herramienta** | "¿En qué lo construirás? (Google Sheets, Looker, Tableau, Databox, Notion)" | Google Sheets o Looker Studio |
| **Frecuencia de actualización** | "¿Con qué frecuencia deberían actualizarse los datos? (tiempo real, diario, semanal)" | Diario |

**PUNTO DE CONTROL:** Confirma el brief antes de continuar.

---

## Fase 2: Diseño

### Arquitectura de Dashboard

1. **KPIs principales** — 3-5 números grandes en la parte superior respondiendo "¿Cómo estamos en general?"
2. **Gráficos de tendencia** — serie temporal mostrando dirección en los últimos 30/90 días
3. **Desgloses** — dimensiones que explican los números principales (por canal, producto, segmento)
4. **Contexto de comparación** — vs. período anterior, vs. objetivo, vs. punto de referencia
5. **Disparadores de acción** — umbrales que señalan cuándo algo necesita atención

### Reglas de Selección de Visualización

| Tipo de Datos | Mejor Visualización | Evitar |
|-----------|-------------------|-------|
| KPI Único | Número grande con flecha de tendencia | Gráfico de pastel |
| Tendencia en tiempo | Gráfico de línea | Gráfico de barras para 30+ puntos de datos |
| Parte del todo | Barra apilada o dona | Gráficos de pastel 3D (siempre) |
| Comparación entre categorías | Gráfico de barras horizontal | Barras verticales con 10+ categorías |
| Correlación | Gráfico de dispersión | Gráfico de línea |
| Geográfico | Mapa / mapa de calor | Tabla con nombres de ubicación |

**PUNTO DE CONTROL:** Presenta el wireframe del dashboard y espera aprobación.

---

## Fase 3: Construir

### Entregables

**1. Documento de Especificación de Dashboard**
- Diseño completo con secciones, métricas y tipos de visualización
- Mapeo de fuente de datos para cada métrica
- Requisitos de filtro y desglose
- Cronograma de actualización y notas de latencia de datos

**2. Definiciones de Métricas**
- Cómo se calcula cada métrica (fórmula)
- Fuente de datos y referencias de tabla/campo
- Rango esperado y umbrales de alerta

**3. Diseño de Wireframe**
- Diseño basado en texto o esbozo mostrando colocación de cada elemento
- Orden de lectura: superior izquierdo a inferior derecho, más importante primero
- Consideraciones móviles si se ve en teléfonos

**4. Checklist de Implementación**
- [ ] Fuentes de datos conectadas y verificadas
- [ ] Cálculos de métricas validados contra fuente
- [ ] Filtros de fecha funcionando correctamente
- [ ] Períodos de comparación precisos
- [ ] Tiempo de carga bajo 5 segundos
- [ ] Diseño móvil revisado

---

## Fase 4: Pulir

### Cadencia de Revisión

- Semana 1: Verifica que todos los números coincidan con datos de fuente
- Semana 4: Encuesta a usuarios — ¿hay algo faltando o confuso?
- Mes 3: Elimina métricas que nadie consulta, añade nuevas preguntas

### Reglas de Higiene de Dashboard

- No más de 10 métricas en una sola vista — si necesitas más, crea sub-dashboards
- Toda métrica tiene una definición en tooltip o nota al pie
- La codificación de color es consistente (verde = bien, rojo = necesita atención)

---

## Ejemplo 1: Dashboard de Fundador de SaaS

**Principal:** MRR, Usuarios Activos, Tasa de Churn, NPS
**Tendencias:** Crecimiento MRR (12 meses), tendencia de registros (30 días)
**Desgloses:** Ingresos por nivel de plan, registros por canal de adquisición

## Ejemplo 2: Dashboard Semanal de E-commerce

**Principal:** Ingresos, Órdenes, AOV, Tasa de Conversión
**Tendencias:** Ingresos diarios (30 días), tráfico (30 días)
**Desgloses:** Ingresos por categoría de producto, tráfico por fuente, conversión por dispositivo

---

## Anti-Patrones

- **Sobrecarga de dashboard** — 30 métricas en una pantalla significa que nadie lee ninguna. Prioriza sin piedad.
- **Métricas de vanidad** — vistas de página totales sin contexto no tiene sentido. Siempre muestra métricas que se conectan a ingresos o retención.
- **Sin contexto de comparación** — un número sin punto de referencia es solo un número. Muestra vs. período anterior, vs. objetivo o vs. industria.
- **Codificación de color arcoíris** — 8 colores para 8 categorías crea ruido visual. Usa máximo 2-3 colores con gris para elementos secundarios.
- **Datos obsoletos** — un dashboard que se actualiza mensualmente cuando las decisiones ocurren semanalmente es inútil.

---

## Recuperación

- **El usuario no puede definir preguntas clave:** Pregunta "¿Qué verificas primera cosa el lunes por la mañana? ¿Qué número te mantiene despierto?" Extrae requisitos de dashboard de las respuestas.
- **Demasiadas fuentes de datos:** Comienza con 1-2 fuentes para el dashboard MVP. Añade fuentes incrementalmente.
- **Sin herramienta BI:** Google Sheets con gráficos y un botón de actualización es un dashboard V1 válido para pequeños negocios.
- **Problemas de calidad de datos:** Señala métricas con problemas de calidad conocidos. Una métrica con asterisco es mejor que una métrica faltante.