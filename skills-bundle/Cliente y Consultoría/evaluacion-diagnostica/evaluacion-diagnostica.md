---
name: evaluacion-diagnostica
description: "Construye herramientas de evaluación diagnóstica para engagement de consultoría con puntuación, benchmarking y lógica de recomendación."
allowed-tools: Read Write Glob
metadata:
  author: Imperio Digital
  version: "1.0"
---

# Evaluación Diagnóstica

## Cuándo Usar Este Skill

Usa este skill cuando necesites:
- Construir una herramienta de evaluación con puntuación para evaluar el estado actual de un cliente
- Crear criterios de benchmarking que comparen el desempeño contra estándares
- Diseñar lógica de recomendación que mapee puntuaciones de evaluación a acciones específicas
- Desarrollar un diagnóstico de generación de leads que demuestre experiencia

**NO USES** este skill para evaluaciones de desempeño de empleados, evaluaciones médicas o encuestas de satisfacción del cliente. Esto es para herramientas de diagnóstico de consultoría y coaching.

---

## Principio Fundamental

UNA EVALUACIÓN DIAGNÓSTICA HACE DOS COSAS — MUESTRA AL CLIENTE DÓNDE ESTÁN Y HACE OBVIO EL CAMINO ADELANTE. LA PUNTUACIÓN REVELA LA BRECHA. LAS RECOMENDACIONES LA CIERRAN.

---

## Fase 1: Diseño de Evaluación

### Información Requerida

| Información | Qué Preguntar | Valor por Defecto |
|-------|------------|---------|
| **Tema de evaluación** | "¿Qué área evalúa esta evaluación?" | Sin valor por defecto — debe proporcionarse |
| **Audiencia objetivo** | "¿Quién toma esta evaluación — dueños de negocio, equipos, individuos?" | Dueños de negocio |
| **Número de categorías** | "¿Cuántas áreas debería cubrir la evaluación?" | 5-7 categorías |
| **Propósito** | "¿Es para engagement de cliente, generación de leads o ambos?" | Engagement de cliente |
| **Modelo de puntuación** | "¿Puntuación simple (1-5) o puntuación ponderada?" | Escala simple 1-5 |

**PUNTO DE CONTROL: Confirma tema y categorías antes de construir preguntas.**

---

## Fase 2: Estructura de Evaluación

### Diseño de Categoría

Define 5-7 categorías de evaluación:

```
## [Nombre de Evaluación] — Categorías

1. [Categoría 1] — [Lo que evalúa]
2. [Categoría 2] — [Lo que evalúa]
3. [Categoría 3] — [Lo que evalúa]
4. [Categoría 4] — [Lo que evalúa]
5. [Categoría 5] — [Lo que evalúa]
```

### Formato de Pregunta

Escribe 3-5 preguntas por categoría:

```
## Categoría: [Nombre de Categoría]

**P1:** [Declaración para calificar]
Califica 1-5: (1 = Muy en Desacuerdo, 5 = Muy de Acuerdo)

**P2:** [Declaración para calificar]
Califica 1-5

**P3:** [Declaración para calificar]
Califica 1-5

**Puntuación de Categoría:** Suma de respuestas / Número de preguntas = [X/5]
```

### Reglas de Escritura de Preguntas

- Escribe declaraciones, no preguntas — "Tenemos un proceso documentado para X" vs. "¿Tienes un proceso?"
- Haz cada nivel distinguible — una puntuación de 2 debe verse claramente diferente de una puntuación de 4
- Evita declaraciones de dos cañones — un concepto por pregunta
- Incluye tanto indicadores positivos como negativos para prevenir puntuaciones todas altas
- Prueba con 3-5 personas para asegurar que las preguntas se entienden consistentemente

---

## Fase 3: Puntuación y Benchmarks

### Matriz de Puntuación

```
## Guía de Puntuación

### Puntuaciones de Categoría
| Puntuación | Nivel | Significado |
|-------|-------|---------|
| 1.0-2.0 | Crítico | Brechas significativas requieren atención inmediata |
| 2.1-3.0 | Desarrollando | Existe fundación pero mejoras principales necesarias |
| 3.1-4.0 | Competente | Desempeño sólido con espacio para optimización |
| 4.1-5.0 | Avanzado | Desempeño fuerte — enfócate en refinamiento |

### Puntuación General
| Rango | Grado | Resumen |
|-------|-------|---------|
| 5-12 | Necesita Fundación | Múltiples áreas críticas — prioriza fundamentos |
| 13-20 | Construyendo | Algunas fortalezas, brechas significativas permanecen |
| 21-28 | Creciendo | Fundación buena — mejoras estratégicas acelerarán resultados |
| 29-35 | Optimizando | Fuerte en todo — refina por excelencia |
```

### Presentación de Resultados

```
## Resultados de Evaluación — [Nombre del Cliente]

**Fecha:** [Fecha]
**Puntuación General:** [X/35] — [Nivel de Grado]

### Desglose de Categoría

| Categoría | Puntuación | Nivel | Prioridad |
|----------|-------|-------|----------|
| [Categoría 1] | X/5 | [Nivel] | [Alto/Med/Bajo] |
| [Categoría 2] | X/5 | [Nivel] | [Alto/Med/Bajo] |
| [Categoría 3] | X/5 | [Nivel] | [Alto/Med/Bajo] |

### Fortalezas (Puntuaciones 4+)
- [Categoría] — [Lo que están haciendo bien]

### Brechas Prioritarias (Puntuaciones bajo 3)
- [Categoría] — [Lo que necesita atención inmediata]

### Acciones Recomendadas
1. **[Acción]** — Aborda [categoría]. Impacto esperado: [resultado].
2. **[Acción]** — Aborda [categoría]. Impacto esperado: [resultado].
3. **[Acción]** — Aborda [categoría]. Impacto esperado: [resultado].
```

---

## Fase 4: Implementación

### Como Herramienta de Generación de Leads

- Ofrece la evaluación como recurso gratuito en tu sitio web
- Automatiza puntuación y entrega de resultados instantáneamente por email
- Incluye CTA: "¿Quieres ayuda mejorando tu puntuación? Reserva una consulta."
- Segmenta leads por nivel de puntuación para seguimiento dirigido

### Como Herramienta de Engagement de Cliente

- Usa la evaluación durante la primera sesión de cada engagement
- Repite la evaluación al final para mostrar mejora medible
- Compara contra promedios de la industria si los datos están disponibles
- Incluye resultados de evaluación en tu propuesta para justificar el engagement

### Opciones de Entrega de Evaluación

| Formato | Mejor Para | Esfuerzo |
|--------|----------|--------|
| Hoja de cálculo PDF | Evaluaciones en persona o por llamada | Bajo |
| Google Form + hoja de puntuación automática | Auto-servicio o generación de leads | Medio |
| Herramienta web interactiva (Typeform, ScoreApp) | Generación de leads a escala | Alto |
| Taller facilitado | Evaluaciones grupales o diagnósticos de equipo | Alto |

---

## Anti-Patrones

- **Demasiadas preguntas** — más de 25 preguntas causa abandono. Mantenlo ajustado y enfocado.
- **Sin recomendaciones accionables** — una puntuación sin próximos pasos es solo una tarjeta de calificación. Mapea cada rango de puntuación a acciones específicas.
- **Puntuación subjetiva sin anclajes** — "Califica tu marketing 1-5" significa cosas diferentes para diferentes personas. Usa descriptores de comportamiento.
- **Recomendaciones de talla única** — "mejora tu marketing" independientemente de la puntuación. Personaliza las recomendaciones al tamaño de la brecha.
- **Sin seguimiento** — enviar resultados sin ofrecerte a discutirlos desperdicia el valor del diagnóstico.

---

## Recuperación

- **Los resultados de evaluación son todos puntuaciones altas:** O el cliente es genuinamente avanzado (cambia a optimización) o las preguntas son demasiado fáciles. Añade preguntas más discriminantes.
- **El cliente no está de acuerdo con su puntuación:** Camina a través de las preguntas específicas y respuestas. Pregunta qué evidencia cambiaría la puntuación.
- **La evaluación es demasiado larga:** Reduce a 3 preguntas por categoría. Enfócate en las preguntas que más diferencian desempeño fuerte de débil.
- **No hay benchmarks de la industria disponibles:** Usa tus propios datos de cliente para construir benchmarks con el tiempo. Comienza con niveles cualitativos (principiante, intermedio, avanzado).
- **Cliente abrumado por resultados:** Prioriza las 2-3 mejoras superiores. Preséntalas como fases, no una lista de tareas simultáneas.
