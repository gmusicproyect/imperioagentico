---
name: formulario-feedback-estudiante
description: "Crea formularios de evaluación de cursos con escalas de calificación, preguntas abiertas y categorías enfocadas en mejora para recopilar feedback accionable de estudiantes."
allowed-tools: Read Write Glob
author: Imperio Digital
version: "1.0"
---

# Formulario de Feedback de Estudiante

## Cuándo Usar Este Skill

Usa este skill cuando necesites:
- Crear un formulario de evaluación de curso para recopilar feedback de estudiantes o participantes
- Construir encuestas de feedback con escalas de calificación y preguntas abiertas
- Diseñar formularios de evaluación enfocados en mejora para talleres, programas o capacitación
- Generar instrumentos de feedback estructurados que producen insights accionables

**NO** uses este skill para encuestas de satisfacción del cliente, formularios de feedback de producto o reseñas de rendimiento del empleado. Es específicamente para evaluación de programas educativos y capacitación.

---

## Principio Fundamental

TODO FORMULARIO DE RETROALIMENTACIÓN DEBE GENERAR DATOS ACCIONABLES QUE INFORMEN DIRECTAMENTE LAS MEJORAS DEL CURSO — NO SOLO MÉTRICAS DE VANIDAD QUE CONFIRMEN LO QUE YA CREES.

---

## Fase 1: Resumen

Recopila los inputs que dan forma al formulario. Sin resumen, sin formulario.

### Entradas Requeridas

Pide al usuario cada una. Si no la proporciona, usa el predeterminado.

| Entrada | Qué Preguntar | Predeterminado |
|---------|--------------|--------|
| **Nombre del curso/programa** | "¿Para qué curso o programa es este formulario de feedback?" | Sin predeterminado — debe proporcionarse |
| **Formato** | "¿Es para un taller en vivo, curso online, programa de cohort o curso autorritmado?" | Curso online |
| **Duración** | "¿Cuánto dura el programa? (sesión única, multi-semana, etc.)" | Multi-semana |
| **Áreas clave a evaluar** | "¿Qué aspectos específicos quieres feedback? (contenido, instructor, materiales, ritmo, etc.)" | Calidad de contenido, ritmo, efectividad del instructor, materiales, satisfacción general |
| **Formato de respuesta** | "¿Quieres un formulario digital, PDF imprimible o ambos?" | Formulario digital |

### Plantilla de Resumen

Presenta esto antes de avanzar:

```
## Resumen de Formulario de Feedback

**Curso:** [Nombre]
**Formato:** Curso online, 6 semanas
**Áreas a evaluar:** Relevancia del contenido, ritmo, claridad del instructor, calidad de apoyo, takeaways accionables
**Formato de respuesta:** Formulario digital (Google Forms / Typeform compatible)
**Tiempo estimado de finalización:** 5-7 minutos
```

**PUNTO DE CONTROL: No procedes a la Fase 2 hasta que el usuario confirme o ajuste el resumen.**

---

## Fase 2: Estructura

Diseña la arquitectura del formulario con flujo de secciones y tipos de preguntas.

### Reglas de Estructura de Formulario

1. **Sección de bienvenida** — intro breve explicando propósito y tiempo estimado (menos de 3 oraciones)
2. **Secciones de calificación** — agrupa preguntas relacionadas bajo encabezados de categoría claros
3. **Secciones abiertas** — coloca después de secciones de calificación para capturar insights cualitativos
4. **Sección de cierre** — calificación general, permiso de testimonio y opt-in de seguimiento

### Directrices de Tipo de Pregunta

- **Escalas Likert:** Usa escalas de 5 puntos (Totalmente en desacuerdo a Totalmente de acuerdo) para consistencia
- **Escalas de calificación:** Usa 1-10 para satisfacción general, 1-5 para atributos específicos
- **Opción múltiple:** Úsala solo para preguntas demográficas o de preferencia
- **Abiertas:** Limita a 3-5 preguntas máximo para prevenir fatiga de encuesta
- **Net Promoter Score:** Incluye una pregunta NPS para comparación

### Plantilla de Sección

```
## Sección: [Nombre de Categoría]
Preguntas: [cantidad]
Tipo: [Likert / Calificación / Abiertas / Mixtas]

1. [Texto de pregunta] — [Tipo de pregunta]
2. [Texto de pregunta] — [Tipo de pregunta]
```

**PUNTO DE CONTROL: Presenta la estructura del formulario y espera aprobación del usuario antes de escribir preguntas completas.**

---

## Fase 3: Escribe

Construye el formulario de feedback completo con todas las preguntas, instrucciones y opciones de respuesta.

### Componentes del Formulario

**1. Mensaje de Bienvenida**
- Declara el propósito (mejorar el curso, no calificar al estudiante)
- Confirma anonimato si aplica
- Declara tiempo estimado de finalización

**2. Secciones de Calificación (por categoría)**
- Calidad del Contenido: relevancia, profundidad, claridad, aplicabilidad en el mundo real
- Instructor/Facilitador: conocimiento, comunicación, responsividad, enganche
- Materiales y Recursos: calidad, accesibilidad, utilidad
- Ritmo y Estructura: velocidad, flujo lógico, balance de carga de trabajo
- Apoyo y Comunidad: interacción entre pares, acceso Q&A, apoyo técnico

**3. Preguntas Abiertas**
- "¿Cuál fue lo más valioso que aprendiste?"
- "¿Qué cambiarías de este curso?"
- "¿Qué tema merecía más tiempo o profundidad?"
- "¿Recomendarías este curso? ¿Por qué o por qué no?"

**4. Sección de Cierre**
- Satisfacción general (1-10)
- NPS: "¿Qué tan probable es que recomiendes este curso?" (0-10)
- Permiso de usar feedback como testimonio
- Opcional: nombre y email para seguimiento

### Reglas de Formato

- Numera cada pregunta secuencialmente a través de todas las secciones
- Incluye etiquetas claras de opción de respuesta (no solo números)
- Agrega opción "N/A" para preguntas que pueden no aplicar a todos los estudiantes
- Mantén formulario total bajo 25 preguntas para mantener tasas de finalización arriba del 70%

---

## Fase 4: Pulida

### 1. Optimización de Tasa de Finalización

Revisa el formulario para riesgos de fatiga de encuesta:
- Las preguntas totales no deben exceder 25
- Tiempo estimado de finalización debe mantenerse bajo 8 minutos
- Las preguntas requeridas deben limitarse solo a escalas de calificación
- Las preguntas abiertas siempre deben ser opcionales

### 2. Guía de Análisis

Proporciona una breve guía para interpretar resultados:

```
## Cómo Usar Esta Feedback

**Datos cuantitativos:** Calcula promedios por categoría. Marca cualquier categoría puntuando abajo de 3.5/5.
**Datos cualitativos:** Codifica respuestas abiertas en temas. Busca patrones mencionados 3+ veces.
**Umbral de acción:** Cualquier item abajo de 4.0 promedio o mencionado negativamente 3+ veces = prioridad de mejora inmediata.
**Minería de testimonio:** Las respuestas a pregunta "más valioso" son tu mejor fuente para copy de marketing.
```

### 3. Recomendaciones de Distribución

- Envía dentro de 24 horas de finalización del curso
- Incluye deadline (7 días) para mantener calidad de respuesta
- Envía un reminder en el punto medio
- Comparte resumen de cambios realizados desde feedback para cerrar el loop

---

## Ejemplo 1: Evaluación de Curso Online de 6 Semanas

**Fragmento de sección de calificación:**
```
## Calidad del Contenido (escala 1-5)
1. El contenido del curso fue relevante para mis necesidades empresariales
2. El material fue presentado a profundidad apropiada
3. Puedo aplicar inmediatamente lo que aprendí
4. Los ejemplos y casos de estudio fueron realistas y útiles
```

**Fragmento abierto:**
```
15. ¿Cuál fue el takeaway más valioso de este curso?
16. Si pudieras cambiar una cosa de este curso, ¿cuál sería?
```

---

## Ejemplo 2: Feedback de Taller en Vivo (Sesión Única)

**Fragmento de sección de calificación:**
```
## Experiencia del Taller (escala 1-5)
1. El taller cumplió mis expectativas basadas en la descripción
2. El facilitador fue enganchante y conocedor
3. Los ejercicios prácticos fueron útiles
4. El ritmo permitió suficiente tiempo para preguntas
```

---

## Anti-Patrones

- **Preguntas leading** — "¿Qué tan asombroso fue el instructor?" sesga respuestas. Usa frases neutrales.
- **Preguntas de doble barril** — "¿Fue el contenido relevante y bien organizado?" pregunta dos cosas. Divídelas.
- **Demasiadas preguntas abiertas** — más de 5 tanques tasas de finalización. Sé selectivo.
- **Sin garantía de anonimato** — los estudiantes dan feedback honesta solo cuando se sienten seguros. Decláralo al inicio.
- **Ignorar los datos** — recopilar feedback que nunca actúas destruye la confianza. Siempre cierra el loop.
- **Solo métricas de vanidad** — "¿Disfrutaste?" no te dice nada accionable. Pregunta qué mejorar.

---

## Recuperación

- **Usuario inseguro qué evaluar:** Usa como predeterminado las cinco categorías estándar (contenido, instructor, materiales, ritmo, apoyo). Estas cubren el 90% de casos de uso.
- **Formulario demasiado largo:** Corta a 15 preguntas principales. Prioriza escalas de calificación sobre abiertas.
- **El usuario quiere calificar estudiantes, no recopilar feedback:** Redirige al skill de evaluación de habilidades. Este skill es para mejora del programa, no evaluación del estudiante.
- **Tasas de respuesta bajas en formularios anteriores:** Recomienda acortar a menos de 10 preguntas, agrega un incentivo, envía dentro de 24 horas de finalización.
