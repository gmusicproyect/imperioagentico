---
name: constructor-dashboard-kpi
description: "Configura dashboards de seguimiento de KPI en Notion con métricas, objetivos, indicadores de estado y seguimiento de tendencias para cualquier tipo de negocio. Utiliza cuando un usuario desee rastrear desempeño de negocio, necesite un dashboard visual para métricas clave o desee reemplazar hojas de cálculo dispersas con una vista centralizada de KPI."
allowed-tools: Read Write Glob
metadata:
  author: Imperio Digital
  version: "1.0"
---

# Constructor de Dashboard de KPI

## Cuándo Usar Este Skill

- Las métricas de negocio están dispersas en múltiples herramientas y hojas de cálculo
- Desea una vista única de salud empresarial actualizada semanal o mensualmente
- Estableciendo OKRs trimestrales y necesita rastrear progreso
- Incorporando un miembro del equipo que necesita visibilidad del desempeño
- Preparándose para una reunión de junta directiva o actualización de inversionista

## Principio Fundamental

**UN DASHBOARD QUE RASTREA TODO NO RASTREA NADA. Limita a 5-8 KPIs que reflejan directamente la salud empresarial.**

## Workflow

### Paso 1: Identificar Métricas Clave

Pregunta al usuario:
1. ¿Qué tipo de negocio? (e-commerce, SaaS, servicio, creador de contenido)
2. ¿Qué estás intentando mejorar ahora? (ingresos, crecimiento, eficiencia, retención)
3. ¿Con qué frecuencia revisarás esto? (semanal, mensual, trimestral)
4. ¿Quién más verá este dashboard? (solo tú, equipo, inversionistas)

**Mínimo necesario: pregunta 1.**

### Paso 2: Selecciona KPIs por Tipo de Negocio

**E-commerce:**
| KPI | Fórmula | Objetivo Ejemplo | Frecuencia |
|-----|---------|---------------|-----------|
| Ingresos | Ventas totales | $25,000/mes | Semanal |
| Valor Promedio de Pedido | Ingresos / Pedidos | $58 | Semanal |
| Tasa de Conversión | Pedidos / Visitantes | 2.5% | Semanal |
| Costo de Adquisición de Cliente | Gasto de publicidad / Nuevos clientes | < $25 | Mensual |
| Tasa de Devolución | Devoluciones / Pedidos | < 5% | Mensual |

**SaaS / Suscripción:**
| KPI | Fórmula | Objetivo Ejemplo | Frecuencia |
|-----|---------|---------------|-----------|
| MRR | Suma de suscripciones activas | $15,000 | Semanal |
| Tasa de Churn | Clientes perdidos / Clientes totales | < 5%/mes | Mensual |
| LTV | Ingresos promedio por cliente × vida promedio | > $500 | Trimestral |
| CAC | Gasto en ventas + marketing / Nuevos clientes | < $100 | Mensual |
| Relación LTV:CAC | LTV / CAC | > 3:1 | Trimestral |

**Negocio de Servicios / Freelance:**
| KPI | Fórmula | Objetivo Ejemplo | Frecuencia |
|-----|---------|---------------|-----------|
| Ingresos | Monto facturado | $12,000/mes | Mensual |
| Tasa de Utilización | Horas facturables / Horas disponibles | > 70% | Semanal |
| Valor del Pipeline | Suma de valores de propuestas | $50,000 | Semanal |
| Tasa de Cierre | Propuestas ganadas / Propuestas totales | > 40% | Mensual |
| Retención de Cliente | Clientes recurrentes / Clientes totales | > 80% | Trimestral |

**Creador de Contenido:**
| KPI | Fórmula | Objetivo Ejemplo | Frecuencia |
|-----|---------|---------------|-----------|
| Ingresos | Patrocinios + Productos + Afiliados | $8,000/mes | Mensual |
| Tamaño de Lista de Email | Suscriptores totales | 10,000 | Semanal |
| Tasa de Apertura de Email | Abiertos / Entregados | > 40% | Semanal |
| Tasa de Engagement | (Me gusta + Comentarios) / Seguidores | > 3% | Semanal |
| Contenido Publicado | Posts/videos/episodios producidos | 12/mes | Semanal |

### Paso 3: Construir el Dashboard de Notion

Crea una base de datos de Notion con estas propiedades:

- **Nombre de KPI** (Título)
- **Valor Actual** (Número)
- **Objetivo** (Número)
- **Estado** (Seleccionar: En Camino / En Riesgo / Fuera de Camino)
- **Tendencia** (Seleccionar: Arriba / Plano / Abajo)
- **Período** (Seleccionar: Esta Semana / Este Mes / Este Trimestre)
- **Categoría** (Seleccionar: Ingresos / Crecimiento / Eficiencia / Retención)
- **Última Actualización** (Fecha)
- **Notas** (Texto enriquecido — para contexto de cambios)

Añade una **propiedad de fórmula** para % del Objetivo: `(Valor Actual / Objetivo) × 100`

Establece reglas de estado:
- **En Camino:** ≥ 90% del objetivo
- **En Riesgo:** 70-89% del objetivo
- **Fuera de Camino:** < 70% del objetivo

### Paso 4: Crea Vistas de Dashboard

1. **Vista de Resumen** — Vista de galería mostrando todos los KPIs con codificación de color de estado
2. **Revisión Semanal** — Tabla filtrada a KPIs semanales, ordenada por estado
3. **Vista de Tendencia** — Vista de dashboard agrupada por tendencia (Arriba / Plano / Abajo)
4. **Vista de Categoría** — Vista de dashboard agrupada por categoría

### Paso 5: Configura Ritmo de Revisión

Proporciona un checklist de revisión:
- **Semanal (15 min):** Actualiza todos los KPIs semanales, señala cualquier cosa Fuera de Camino
- **Mensual (30 min):** Actualiza todos los KPIs, compara con mes anterior, ajusta objetivos si es necesario
- **Trimestral (60 min):** Revisión completa, establece nuevos objetivos, añade/elimina KPIs

## Ejemplos

### Ejemplo 1: Dashboard de Tienda de E-commerce

**Configuración de Base de Datos de Notion:**

| KPI | Actual | Objetivo | Estado | Tendencia |
|-----|---------|--------|--------|-------|
| Ingresos Mensuales | $22,400 | $25,000 | En Riesgo | Arriba |
| Valor Promedio de Pedido | $62 | $58 | En Camino | Arriba |
| Tasa de Conversión | 1.8% | 2.5% | Fuera de Camino | Plano |
| Nuevos Clientes | 180 | 200 | En Riesgo | Arriba |
| Tasa de Devolución | 3.2% | < 5% | En Camino | Abajo |
| Crecimiento de Lista de Email | +340 | +500 | En Riesgo | Plano |
| ROAS de Anuncios | 3.2x | 3.0x | En Camino | Arriba |

**Notas de Revisión Semanal:**
> Los ingresos tienden al alza pero siguen por debajo del objetivo — la tasa de conversión es el cuello de botella. AOV es fuerte (por encima del objetivo), por lo que la calidad del tráfico puede ser el problema. Acción: Revisa la orientación de anuncios esta semana, verifica la bounce rate de la página de destino.

### Ejemplo 2: Dashboard de Consultor Freelance

| KPI | Actual | Objetivo | Estado | Tendencia |
|-----|---------|--------|--------|-------|
| Ingresos Mensuales | $9,800 | $12,000 | En Riesgo | Plano |
| Tasa de Utilización | 58% | 70% | Fuera de Camino | Abajo |
| Valor del Pipeline | $42,000 | $50,000 | En Riesgo | Arriba |
| Clientes Activos | 3 | 4 | En Riesgo | Plano |
| Tasa de Cierre | 45% | 40% | En Camino | Arriba |
| Valor Promedio de Proyecto | $4,200 | $4,000 | En Camino | Arriba |

**Insight:** La tasa de cierre es fuerte pero el pipeline es ligero. La restricción no es convertir leads — es generarlos. Recomendación: Aumenta actividad de alcance o derivaciones antes de optimizar cualquier otra cosa.

## Recuperación y Respaldos

- **El usuario no sabe qué rastrear:** Comienza con ingresos + una métrica de crecimiento + una métrica de eficiencia. Tres KPIs es mejor que cero KPIs. Expande después del primer mes de seguimiento.
- **El usuario quiere rastrear 20+ métricas:** Rechaza. Un dashboard con 20 métricas es una hoja de cálculo, no un dashboard. Fuerza-clasifica y elige los 5-8 principales.
- **El usuario no usa Notion:** Adapta el dashboard a Google Sheet o Airtable. La estructura es la misma — solo la herramienta cambia.
- **Las métricas no mejoran:** Los dashboards muestran problemas; no los arreglan. Cuando un KPI está Fuera de Camino por 3+ períodos, necesita un plan de acción, no más seguimiento.

## Restricciones

- **NUNCA incluyas más de 8 KPIs** en el dashboard principal — crea una vista "detalle" secundaria para agradables de tener
- Cada KPI debe tener un objetivo definido — una métrica sin objetivo es solo un número
- Incluye indicadores de estado (En Camino / En Riesgo / Fuera de Camino) para lectura de un vistazo
- Siempre incluye un campo "Última Actualización" para evitar que datos obsoletos se vean actuales
- Proporciona el ritmo de revisión — un dashboard que nadie consulta es inútil