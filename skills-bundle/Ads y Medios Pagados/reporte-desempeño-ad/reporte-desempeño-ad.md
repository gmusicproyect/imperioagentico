---
name: reporte-desempeño-ad
description: "Crea plantillas de reporte de desempeño de ad con análisis de ROAS, insights de creative, y recomendaciones de optimización. Úsalo cuando necesites reportes estructurados de campañas de ad."
allowed-tools: Read Write Glob
metadata:
  author: Imperio Digital
  version: "1.0"
---

# Reporte de Desempeño de Ad

## Principio Fundamental

CADA MÉTRICA EN EL REPORTE DEBE LLEVAR A UNA ACCIÓN — SI UN NÚMERO NO INFORMA UNA DECISIÓN, REMUÉVELO.

## Cuándo Usar

- Crear reporte semanal o mensual de desempeño de ad
- Analizar ROAS, CPA y otras métricas clave de publicidad
- Entregar insights de desempeño de creative y recomendaciones de optimización
- Construir plantilla de reporte reutilizable para campañas continuas

## Fase 1: Setup del Reporte

### Inputs Requeridos

| Input | Qué Preguntar | Default |
|-------|---------------|---------|
| **Plataformas de ad** | "¿Qué plataformas? (Meta, Google, TikTok, LinkedIn, todas)" | Meta + Google |
| **Período de reporte** | "¿Qué rango de fechas? (semanal, mensual, custom)" | Últimos 30 días |
| **Objetivos de campaña** | "KPI primario? (ROAS, CPA, leads, tráfico)" | ROAS |
| **Gasto total** | "¿Cuál fue el gasto total este período?" | Sin default — debe ser proporcionado |
| **Ingresos o conversiones** | "¿Qué ingresos o conversión resulto?" | Sin default — debe ser proporcionado |
| **Período de comparación** | "¿Comparar contra qué? (período previo, año pasado)" | Período previo |

---

## Fase 2: Análisis de Métricas

### Métricas Principales

```
## Métricas Principales

| Métrica | Este Período | Período Pasado | Cambio |
|---------|------------|-------------|--------|
| Gasto Total | $X | $X | +/-X% |
| Ingresos | $X | $X | +/-X% |
| ROAS | X.Xx | X.Xx | +/-X% |
| CPA/CPL | $X | $X | +/-X% |
| Impresiones | X | X | +/-X% |
| Clics | X | X | +/-X% |
| CTR | X.X% | X.X% | +/-X% |
| CPC | $X.XX | $X.XX | +/-X% |
| Conversiones | X | X | +/-X% |
| Tasa de Conversión | X.X% | X.X% | +/-X% |
```

### Desglose por Plataforma

```
## Desempeño por Plataforma

| Plataforma | Gasto | Ingresos | ROAS | CPA | CTR |
|----------|-------|---------|------|-----|-----|
| Meta | $X | $X | X.Xx | $X | X.X% |
| Google | $X | $X | X.Xx | $X | X.X% |
```

---

## Fase 3: Insights y Recomendaciones

### Desempeño de Creative

```
## Creatives Con Mejor Desempeño

1. [Nombre/ID de Creative] — ROAS: X.Xx, Gasto: $X, CPA: $X
   Por qué funciona: [Análisis de hook, formato, mensajería]

## Creatives Con Bajo Desempeño

1. [Nombre/ID de Creative] — ROAS: X.Xx, Gasto: $X, CPA: $X
   Recomendación: [Pausa / revisa hook / cambia audiencia]
```

### Recomendaciones de Optimización

Proporciona 3-5 acciones específicas, priorizadas:

```
## Acciones Recomendadas

1. **[Acción]** — [Lógica] — Impacto esperado: [Alto/Medio/Bajo]
2. **[Acción]** — [Lógica] — Impacto esperado: [Alto/Medio/Bajo]
3. **[Acción]** — [Lógica] — Impacto esperado: [Alto/Medio/Bajo]
```

---

## Anti-Patrones

- **Data dumps sin insight** — una tabla de números no es un reporte. Cada métrica necesita contexto y recomendación
- **Reportar métricas vanidosas** — impresiones y reach sin tying a ingresos es ruido
- **Missing comparison context** — números crudos no significan nada sin período-a-período o comparación de benchmark
- **Enterrar recomendaciones** — lidera con qué hacer, luego soporta con datos
- **Reportar demasiado infrequentemente** — mensual es mínimo. Semanal para campañas gastando $5K+/mes

---

## Recuperación

- **Data incompleto:** Nota qué métricas faltan y por qué. Proporciona análisis en data disponible con caveats
- **ROAS bajo 1.0:** Señala inmediatamente. Recomienda pausar bajo-desempeño, reallocar presupuesto, o revisar creative
- **Sin conversion tracking:** No puedes producir reporte significativo. Ayuda al usuario configu tracking como prerequisite
- **Primer mes de ads (sin data de comparación):** Usa benchmarks de industria como baseline de comparación
