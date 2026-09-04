---
name: plantilla-reporte-cliente
description: "Diseña plantillas de informes de cliente con resúmenes ejecutivos, visualizaciones de datos y recomendaciones de próximos pasos."
allowed-tools: Read Write Glob
metadata:
  author: Imperio Digital
  version: "1.0"
---

# Plantilla de Reporte de Cliente

## Cuándo Usar Este Skill

Usa este skill cuando necesites:
- Crear plantillas de informes recurrentes de cliente (semanal, mensual, trimestral)
- Estructurar resúmenes ejecutivos que los tomadores de decisiones ocupados realmente lean
- Presentar datos con visualizaciones claras y contexto narrativo
- Incluir recomendaciones de próximos pasos accionables en cada reporte

**NO USES** este skill para informes de equipo interno, estados financieros o entregables de proyectos únicos. Esto es para informes recurrentes de progreso y desempeño orientados al cliente.

---

## Principio Fundamental

UN REPORTE DE CLIENTE DEBE TOMAR 3 MINUTOS PARA ESCANEAR Y 10 MINUTOS PARA LEER COMPLETAMENTE — SI EL CLIENTE TIENE QUE PREGUNTAR "¿Y ESO QUÉ?" DESPUÉS DE LEERLO, EL REPORTE FRACASÓ.

---

## Fase 1: Requisitos de Reporte

### Información Requerida

| Información | Qué Preguntar | Valor por Defecto |
|-------|------------|---------|
| **Tipo de reporte** | "¿Es semanal, mensual o trimestral?" | Mensual |
| **Área de servicio** | "¿Sobre qué estás informando — marketing, desarrollo, consultoría, otro?" | Sin valor por defecto — debe proporcionarse |
| **Métricas clave** | "¿Cuáles son los 3-5 KPIs que más importan a tu cliente?" | Sin valor por defecto — debe proporcionarse |
| **Objetivo del cliente** | "¿Cuál es el resultado por el cual el cliente te está pagando?" | Sin valor por defecto — debe proporcionarse |
| **Audiencia** | "¿Quién lee esto — fundador, director de marketing, C-suite?" | Dueño de negocio / fundador |

**PUNTO DE CONTROL: Confirma estructura de reporte y KPIs antes de construir la plantilla.**

---

## Fase 2: Plantilla de Reporte

### Estructura del Reporte

```
## Reporte de [Nombre de Cliente] — [Mes/Período]
**Preparado por:** [Tu nombre]
**Fecha:** [Fecha]
**Período de reporte:** [Fecha inicio] — [Fecha fin]

---

### Resumen Ejecutivo

[3-4 oraciones máximo. Establece el resultado superior, la tendencia más importante,
y la acción #1 recomendada. Un CEO ocupado debe poder leer solo
esta sección y entender cómo van las cosas.]

**Línea de fondo:** [Una oración — ¿estamos en el camino, adelantados o atrasados del objetivo?]

---

### Dashboard de Métricas Clave

| Métrica | Este Período | Período Anterior | Cambio | Objetivo | Estado |
|--------|-----------|------------|--------|--------|--------|
| [KPI 1] | [valor] | [valor] | [+/-X%] | [objetivo] | ✓ En Camino / ⚠ Vigilar / ✗ Atrás |
| [KPI 2] | [valor] | [valor] | [+/-X%] | [objetivo] | ✓ / ⚠ / ✗ |
| [KPI 3] | [valor] | [valor] | [+/-X%] | [objetivo] | ✓ / ⚠ / ✗ |

---

### Lo Que Hicimos

[Lista de punto de actividades completadas y entregables este período.
Mantenlo factual — acciones tomadas, no solo planes hechos.]

- [Actividad 1] — [resultado o salida]
- [Actividad 2] — [resultado o salida]
- [Actividad 3] — [resultado o salida]

---

### Qué Funcionó

[Destaca 1-2 victorias con contexto. Explica POR QUÉ funcionó para que
el cliente entienda la estrategia, no solo el resultado.]

---

### Qué Necesita Atención

[Señala 1-2 áreas de preocupación con evaluación honesta. Incluye qué
estás haciendo al respecto — nunca presentes un problema sin un plan.]

---

### Recomendaciones y Próximos Pasos

1. **[Elemento de acción]** — [Por qué e impacto esperado]. Responsable: [quién]. Para: [fecha].
2. **[Elemento de acción]** — [Por qué e impacto esperado]. Responsable: [quién]. Para: [fecha].
3. **[Elemento de acción]** — [Por qué e impacto esperado]. Responsable: [quién]. Para: [fecha].

---

### Apéndice (Opcional)

[Tablas de datos detalladas, capturas de pantalla, desglose de campañas, o
información de apoyo para clientes que quieren profundizar.]
```

---

## Fase 3: Presentación de Datos

### Directrices de Visualización

| Tipo de Dato | Mejor Formato | Evitar |
|-----------|------------|-------|
| Tendencia a lo largo del tiempo | Gráfico de líneas | Gráfico circular |
| Comparación entre categorías | Gráfico de barras | Gráficos 3D |
| Parte de un todo | Barra apilada o tabla simple | Gráficos circulares complejos |
| Número clave único | Número grande en negrita con contexto | Enterrado en un párrafo |
| Antes/después | Comparación lado a lado | Descripción narrativa larga |

### Reglas de Narrativa

- Cada número necesita contexto — "2.400 visitantes" no significa nada sin "arriba 35% desde el mes anterior"
- Compara con el objetivo, no solo el período anterior
- Explica anomalías — picos y caídas necesitan explicaciones de una oración
- Usa lenguaje simple — "tasa de conversión mejorada" no "observamos un delta positivo en CR"

---

## Fase 4: Entrega y Seguimiento

### Lista de Verificación de Entrega

- [ ] El resumen ejecutivo tiene menos de 4 oraciones
- [ ] Todos los KPIs muestran comparación período a período y estado de objetivo
- [ ] Cada sección responde "¿y eso qué?" — no solo datos, sino interpretación
- [ ] Las recomendaciones son específicas, asignadas y con límite de tiempo
- [ ] El reporte está formateado limpiamente — fuentes consistentes, alineación, espaciado
- [ ] Revisado para precisión — un número equivocado destruye la credibilidad

### Mejores Prácticas de Entrega

- Envía el reporte 24 horas antes de cualquier reunión de revisión
- Incluye un resumen de una oración por email: "Ingresos arriba 18% — reporte completo adjunto"
- Programa una llamada de 15-30 minutos para caminar el reporte y discutir próximos pasos
- Archiva todos los reportes para análisis de tendencias y revisiones anuales

---

## Anti-Patrones

- **Vertedero de datos sin narrativa** — números crudos sin interpretación hacen que los clientes sientan que están haciendo tu trabajo.
- **Enterrando malas noticias** — esconder el underperformance en un apéndice erosiona la confianza. Dirígete a ello de frente con un plan.
- **Reportes que toman 30+ minutos en leer** — si el cliente necesita una reunión solo para entender el reporte, es demasiado largo.
- **Sin recomendaciones** — un reporte sin próximos pasos es una lección de historia. Siempre di al cliente qué hacer.
- **Formato inconsistente** — cambiar el diseño del reporte cada mes hace imposible comparar períodos.
- **Solo métricas de vanidad** — reportando impresiones y seguidores cuando el cliente se importa de ingresos y leads.

---

## Recuperación

- **Cliente nunca lee el reporte:** Acórtalo drásticamente. Lidera con el resumen ejecutivo y ofrece detalles bajo solicitud.
- **Cliente cuestiona un número:** Ten siempre los datos fuente listos. Muestra el cálculo y metodología transparentemente.
- **Las métricas no mejoran:** Reconócelo directamente. Presenta el diagnóstico y una estrategia revisada. No hagas spin de resultados malos.
- **Cliente quiere diferentes métricas:** Actualiza el dashboard de KPIs inmediatamente. Pregunta por qué las nuevas métricas importan para alinear tu trabajo.
- **El reporte toma demasiado tiempo en crear:** Templatiza todo. Usa la misma estructura cada período y solo actualiza datos y narrativa.
