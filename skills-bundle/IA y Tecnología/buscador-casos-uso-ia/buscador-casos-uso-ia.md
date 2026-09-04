---
name: buscador-casos-uso-ia
description: "Identifica oportunidades de automatización con IA en workflows empresariales con evaluación de viabilidad y estimaciones de ROI. Úsalo cuando evalúes dónde la IA puede ahorrar tiempo y dinero en tu negocio."
allowed-tools: Read Write Glob
metadata:
  author: Imperio Digital
  version: "1.0"
---

# Buscador de Casos de Uso con IA

## Cuándo Usar Este Skill

Usa este skill cuando necesites:
- Identificar qué tareas empresariales pueden ser automatizadas o mejoradas con IA
- Evaluar la viabilidad y ROI de adopción de IA para workflows específicos
- Priorizar oportunidades de implementación de IA por impacto y esfuerzo
- Crear una roadmap de adopción de IA para un emprendedor o pequeño negocio

**NO USES** este skill para construir modelos de IA, escribir prompts o evaluar herramientas específicas de IA. Esto es para identificar y priorizar dónde encaja la IA en tu negocio.

---

## Principio Fundamental

LA IA DEBE AUTOMATIZAR LO REPETITIVO PARA QUE TÚ PUEDAS ENFOCARTE EN LO ESTRATÉGICO — LOS MEJORES CASOS DE USO DE IA AHORRAN TIEMPO MEDIBLE EN TAREAS QUE YA HACES, NO EN TAREAS QUE IMAGINAS HACER.

---

## Fase 1: Brief

### Inputs Requeridos

| Input | Qué Preguntar | Default |
|-------|------------|---------|
| **Tipo de negocio** | "¿Qué hace tu negocio?" | Sin default — debe proporcionarse |
| **Tamaño del equipo** | "¿Cuántas personas trabajan en el negocio?" | Individual (1 persona) |
| **Tareas semanales** | "Lista las tareas en las que pasas más tiempo cada semana." | Sin default — debe proporcionarse |
| **Pain points** | "¿Cuáles tareas odias o desearías poder delegar?" | Sin default — pedir los 3 principales |
| **Uso actual de IA** | "¿Usas ya herramientas de IA? ¿Cuáles?" | Ninguna o ChatGPT básico |
| **Presupuesto** | "¿Cuál es tu presupuesto mensual para herramientas y software?" | Menos de $100/mes |

**PUNTO DE CONTROL: Confirma el brief y lista de tareas antes de analizar oportunidades.**

---

## Fase 2: Auditoría e Identificación

### Marco de Auditoría de Tareas

Para cada tarea que listó el usuario, evalúa:

| Tarea | Horas/Semana | Frecuencia | ¿Repetitiva? | ¿Requiere Juicio? | Potencial de IA |
|------|-----------|-----------|-------------|--------------------|----|
| [Tarea 1] | | | Sí/No | Bajo/Medio/Alto | Alto/Medio/Bajo |
| [Tarea 2] | | | Sí/No | Bajo/Medio/Alto | Alto/Medio/Bajo |

### Puntuación de Oportunidad de IA

Puntúa cada tarea en tres dimensiones:

| Dimensión | Puntuación 1-5 | Descripción |
|-----------|-----------|-------------|
| **Ahorro de tiempo** | 1=mínimo, 5=horas ahorradas semanales | ¿Cuánto tiempo ahorrará la IA? |
| **Viabilidad** | 1=complejo, 5=herramientas existen hoy | ¿Pueden las herramientas actuales manejar esto? |
| **Impacto** | 1=agradable, 5=afecta ingresos | ¿Cuál es el impacto empresarial de automatizar esto? |

**Puntuación de Prioridad de IA = Ahorro de Tiempo × Viabilidad × Impacto (máx 125)**

### Casos de Uso de IA Comúnmente Valiosos

| Área Empresarial | Tarea | Solución con IA | Tiempo Ahorrado |
|---------------|------|------------|-----------|
| **Contenido** | Escribir primeros borradores | LLM (Claude, ChatGPT) | 5-10 hrs/semana |
| **Email** | Redactar respuestas | Herramientas de email con IA | 3-5 hrs/semana |
| **Redes sociales** | Escribir captions y publicaciones | LLM + herramienta de programación | 2-4 hrs/semana |
| **Investigación** | Investigación de mercado y competencia | Búsqueda de IA + resumir | 2-3 hrs/semana |
| **Admin** | Notas de reuniones y resúmenes | Transcripción con IA | 1-2 hrs/semana |
| **Finanzas** | Categorización de facturas y gastos | Herramientas de contabilidad con IA | 1-2 hrs/semana |
| **Soporte a clientes** | Respuestas a FAQ | Chatbots, IA templated | 3-5 hrs/semana |
| **Diseño** | Creación básica de gráficos | Generación de imágenes con IA | 1-3 hrs/semana |

**PUNTO DE CONTROL: Presenta oportunidades puntuadas y confirma las 3-5 principales para desarrollar.**

---

## Fase 3: Construir el Plan de Implementación

### Para Cada Oportunidad Principal

```
## Oportunidad: [Nombre de Tarea]

**Estado actual:** [Cómo se realiza la tarea ahora]
**Solución de IA:** [Herramienta específica o enfoque]
**Tiempo ahorrado:** [Horas por semana]
**Costo:** [Costo mensual de herramienta]
**ROI:** [Tiempo ahorrado × tarifa horaria] vs. [Costo de herramienta]
**Esfuerzo de implementación:** [Horas para configurar]
**Riesgo:** [Qué podría salir mal]

### Pasos de Configuración
1. [Paso 1]
2. [Paso 2]
3. [Paso 3]

### Métrica de Éxito
[Cómo medir si esto está funcionando]
```

### Roadmap de Implementación

Secuencia oportunidades por ganancias rápidas primero:

| Fase | Cronograma | Tareas a Automatizar | Ahorros Esperados |
|-------|----------|-------------------|-----------------|
| Ganancias rápidas | Semana 1-2 | [Tareas bajo esfuerzo, alto impacto] | [X] hrs/semana |
| Fundación | Semana 3-4 | [Tareas de esfuerzo medio] | [X] hrs/semana |
| Avanzado | Mes 2-3 | [Tareas de mayor esfuerzo, mayor recompensa] | [X] hrs/semana |

---

## Fase 4: Pulir

### 1. Resumen de ROI

```
## Resumen de ROI de Adopción de IA

**Tareas totales auditadas:** [X]
**Tareas con potencial de IA:** [X]
**Ahorro de tiempo semanal estimado:** [X] horas
**Costos de herramientas mensuales:** $[X]
**Valor mensual de tiempo ahorrado:** $[X] (a $[tarifa horaria]/hora)
**ROI neto mensual:** $[X]
**Período de amortización:** [X] semanas
```

### 2. Evaluación de Riesgo

Para cada implementación de IA recomendada:
- **Riesgo de calidad:** ¿La salida de IA cumplirá con tus estándares? (Mitigación: revisión humana)
- **Riesgo de dependencia:** ¿Qué pasa si la herramienta se cierra? (Mitigación: evitar puntos únicos de fallo)
- **Riesgo de costo:** ¿Aumentará el precio? (Mitigación: monitorear uso y alternativas)

### 3. Lista de Verificación de Calidad

```
## Lista de Verificación del Buscador de Casos de Uso de IA

- [ ] Todas las tareas semanales principales auditadas con estimaciones de tiempo
- [ ] Cada tarea puntuada en ahorro de tiempo, viabilidad e impacto
- [ ] 3-5 oportunidades principales identificadas y priorizadas
- [ ] Herramientas de IA específicas recomendadas para cada oportunidad
- [ ] ROI calculado (tiempo ahorrado vs. costo de herramienta)
- [ ] Pasos de implementación delineados para cada oportunidad
- [ ] Roadmap secuencia ganancias rápidas primero
- [ ] Riesgos identificados con estrategias de mitigación
- [ ] Métricas de éxito definidas para cada implementación
- [ ] Ahorros de tiempo total proyectado y ROI resumidos
```

---

## Ejemplo

**Negocio:** Consultor de marketing autónomo
**Oportunidad principal:**

```
## Oportunidad: Escritura de Reportes de Clientes

**Estado actual:** Compilar manualmente análisis en reportes, escribir resúmenes. Toma 4 horas por cliente al mes × 6 clientes = 24 horas/mes.
**Solución de IA:** Claude + plantilla. Alimenta datos de análisis, genera borrador de reporte narrativo, revisión humana y customización.
**Tiempo ahorrado:** 16 horas/mes (de 24 a 8)
**Costo:** $20/mes (Claude Pro)
**ROI:** 16 horas × $75/hora = $1,200/mes de valor ahorrado por $20 de costo
**Esfuerzo de implementación:** 3 horas para crear plantillas y probar
**Métrica de éxito:** El tiempo de creación de reporte cae por debajo de 1.5 horas por cliente
```

---

## Anti-Patrones

- **Automatizar tareas que deberías eliminar** — si una tarea no agrega valor, no la automatices. Deja de hacerla.
- **Comenzar con el caso de uso más difícil** — empieza con las tareas más simples y repetitivas. Construye confianza antes de tareas complejas.
- **Ignorar requisitos de calidad** — los borradores de IA necesitan revisión humana. Incluye tiempo de revisión en tu estimación de ahorro de tiempo.
- **Acumulación de herramientas** — registrarse en 10 herramientas de IA crea complejidad. Comienza con 1-2 herramientas que cubran la mayoría de casos.
- **Esperar perfección** — IA que ahorra el 70% del tiempo en una tarea es una victoria. Esperar automatización del 100% significa esperar para siempre.

---

## Recuperación

- **Usuario no puede identificar tareas repetitivas:** Camina a través de una semana típica de trabajo hora por hora. Las tareas se hacen visibles cuando se mapean al tiempo.
- **Todas las tareas parecen requerir alto juicio:** Desglosa tareas en sub-pasos. Los sub-pasos de investigación, borrador y formato son frecuentemente automatizables incluso cuando la decisión final no.
- **El presupuesto es cero:** Enfócate en capas gratuitas de herramientas de IA (ChatGPT gratis, Claude gratis, Canva gratis). Muchas herramientas ofrecen planes generosos gratuitos.
- **Usuario abrumado por opciones:** Elige UNA tarea, UNA herramienta y UNA semana para probar. Expande solo después de la primera victoria.
