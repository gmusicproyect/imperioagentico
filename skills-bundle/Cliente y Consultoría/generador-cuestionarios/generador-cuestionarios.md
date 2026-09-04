---
name: generador-cuestionarios
description: "Genera cuestionarios y evaluaciones con opción múltiple, verdadero/falso y preguntas de respuesta corta con claves de respuesta."
allowed-tools: Read Write Glob
metadata:
  author: Imperio Digital
  version: "1.0"
---

# Generador de Cuestionarios

## Cuándo Usar Este Skill

Usa este skill cuando necesites:
- Generar cuestionarios para cursos, programas de entrenamiento o certificaciones
- Crear múltiples tipos de preguntas — opción múltiple, verdadero/falso, respuesta corta
- Construir claves de respuesta con explicaciones para respuestas correctas e incorrectas
- Diseñar evaluaciones que prueben diferentes niveles cognitivos

**NO USES** este skill para cuestionarios de personalidad, cuestionarios de generación de leads o diseño de encuestas. Esto es para cuestionarios de evaluación de conocimiento que verifican aprendizaje.

---

## Principio Fundamental

UN BUEN CUESTIONARIO NO SOLO PRUEBA MEMORIA — PRUEBA SI EL APRENDIZ PUEDE APLICAR LO QUE APRENDIÓ. LAS PREGUNTAS DEBEN REQUERIR PENSAMIENTO, NO SOLO RECUERDO.

---

## Fase 1: Resumen de Cuestionario

### Información Requerida

| Información | Qué Preguntar | Valor por Defecto |
|-------|------------|---------|
| **Tema** | "¿Qué tema cubre este cuestionario?" | Sin valor por defecto — debe proporcionarse |
| **Material fuente** | "¿En qué contenido deben basarse las preguntas — lección, manual, módulo?" | Sin valor por defecto — debe proporcionarse |
| **Número de preguntas** | "¿Cuántas preguntas?" | 10 preguntas |
| **Tipos de preguntas** | "¿Opción múltiple, verdadero/falso, respuesta corta o mezcla?" | Mezcla de todos |
| **Nivel de dificultad** | "¿Principiante, intermedio o avanzado?" | Intermedio |
| **Puntuación para pasar** | "¿Qué puntuación se requiere para pasar?" | 70% |

**PUNTO DE CONTROL: Confirma tema y material fuente antes de generar preguntas.**

---

## Fase 2: Diseño de Preguntas

### Directrices de Tipo de Pregunta

**Opción Múltiple (4 opciones):**
- Una respuesta claramente correcta
- Tres distractores plausibles (respuestas incorrectas que tienen sentido)
- Evita "todos los anteriores" y "ninguno de los anteriores" — debilitan la evaluación
- Evita negativos en la raíz ("Cuál NO es...") — reformula positivamente cuando sea posible
- Todas las opciones deben ser similares en longitud y estructura

**Verdadero/Falso:**
- La declaración debe ser inequívocamente verdadera o falsa — sin "depende" respuestas
- Evita dobles negativos
- Prueba un concepto por declaración
- Equilibrio aproximado 50/50 verdadero y falso

**Respuesta Corta:**
- La pregunta debe tener una respuesta específica y defendible (no interpretable)
- Proporciona la longitud de respuesta esperada ("En 1-2 oraciones...")
- Incluye criterios de calificación en la clave de respuesta

### Distribución de Nivel Cognitivo

| Nivel | % del Cuestionario | Estilo de Pregunta |
|-------|-----------|---------------|
| Recordar/Recall | 20-30% | Definiciones, hechos, terminología |
| Entender | 20-30% | Explica conceptos, compara ideas |
| Aplicar | 30-40% | Escenarios, resolución de problemas, "qué harías" |
| Analizar/Evaluar | 10-20% | Casos de estudio, mejor enfoque, justifica decisión |

---

## Fase 3: Plantilla de Cuestionario

### Formato de Cuestionario

```
## [Título de Cuestionario]

**Tema:** [Tema]
**Preguntas:** [X]
**Límite de tiempo:** [X] minutos (opcional)
**Puntuación para pasar:** [X]%

---

### Pregunta 1 (Opción Múltiple)

¿Cuál es el propósito principal de [concepto]?

a) [Distractor — plausible pero incorrecto]
b) [Respuesta correcta]
c) [Distractor — concepto erróneo común]
d) [Distractor — relacionado pero incorrecto]

---

### Pregunta 2 (Verdadero/Falso)

[Declaración sobre el tema.]

Verdadero / Falso

---

### Pregunta 3 (Respuesta Corta)

En 1-2 oraciones, explica [concepto o proceso].

---

[Continúa para todas las preguntas...]
```

### Formato de Clave de Respuesta

```
## Clave de Respuesta — [Título de Cuestionario]

### Pregunta 1: **B**
[Explicación de por qué B es correcta y por qué las otras opciones están mal.
Este es el momento de enseñanza — las claves de respuesta deben educar, no solo confirmar.]

### Pregunta 2: **Falso**
[Explicación: La declaración es falsa porque... La información correcta es...]

### Pregunta 3: **Respuesta de Muestra**
"[Modelo de respuesta que recibiría crédito completo.]"

**Criterios de calificación:**
- Debe mencionar [concepto clave 1] (1 punto)
- Debe mencionar [concepto clave 2] (1 punto)
- Explicación precisa y clara (1 punto)

### Pregunta 4: **C**
[Explicación con razonamiento de por qué C es el mejor enfoque en este escenario.]
```

---

## Fase 4: Entrega y Análisis de Cuestionario

### Opciones de Entrega

| Formato | Mejor Para | Herramientas |
|--------|----------|-------|
| Papel / PDF | Entrenamiento en persona, handouts impresos | Word, Google Docs |
| Formulario en línea | Aprendizaje de ritmo propio, auto-calificación | Google Forms, Typeform |
| Integración LMS | Cursos con seguimiento y certificación | Teachable, Thinkific, Kajabi |
| Verbal en vivo | Talleres, verificaciones rápidas de pulso | Sin herramientas necesarias |

### Análisis de Cuestionario

Después de administrar, revisa:

| Métrica | Lo Que Te Dice |
|--------|------------------|
| Tasa de aprobación general | ¿Es el cuestionario apropiadamente difícil? |
| Puntuación promedio | ¿Están los aprendices entendiendo el material? |
| Análisis por pregunta | ¿Qué preguntas tuvieron tasa correcta más baja? |
| Análisis de distractor | ¿Las respuestas incorrectas atraen respuestas uniformemente? |
| Tiempo para completar | ¿Es el cuestionario demasiado largo o demasiado corto? |

### Lista de Verificación de Cuestionario

- [ ] Las preguntas se alinean con objetivos de aprendizaje establecidos
- [ ] Mezcla de tipos de preguntas y niveles cognitivos incluidos
- [ ] Los distractores de opción múltiple son plausibles (no obviamente incorrectos)
- [ ] Sin preguntas truco o redacción ambigua
- [ ] La clave de respuesta incluye explicaciones, no solo respuestas correctas
- [ ] La puntuación de aprobación es apropiada para el nivel de dificultad
- [ ] El cuestionario ha sido probado por alguien que conoce el material (para atrapar errores)
- [ ] El cuestionario ha sido probado por alguien que NO conoce el material (para verificar claridad)

---

## Anti-Patrones

- **Preguntas truco** — preguntas diseñadas para confundir en lugar de evaluar aprendizaje son injustas e informativas.
- **Probando trivialidades en lugar de entendimiento** — "¿En qué año se inventó X?" prueba memoria, no competencia.
- **Solo preguntas de recall** — si cada pregunta es "define este término," el cuestionario no prueba aplicación del mundo real.
- **Respuestas incorrectas obvias** — si tres de cuatro opciones son absurdas, el cuestionario no evalúa nada.
- **Sin explicaciones de respuesta** — un cuestionario sin explicaciones en la clave de respuesta desperdicia una oportunidad de aprendizaje.
- **Demasiadas preguntas** — fatiga de cuestionario reduce precisión después de 15-20 preguntas. Mantenlo enfocado.

---

## Recuperación

- **Tasa de fallo alta:** Revisa las preguntas — ¿son demasiado dificultosas, ambiguas o probando contenido no enseñado?
- **Todos obtienen puntuación perfecta:** El cuestionario es demasiado fácil. Añade preguntas de aplicación y análisis que requieran pensamiento más profundo.
- **Una pregunta tiene tasa correcta muy baja:** O el contenido no fue enseñado bien o la pregunta está mal escrita. Investiga ambas posibilidades.
- **Los aprendices se quejan de injusticia:** Revisa con ojos frescos. Retira cualquier pregunta que pudiera interpretarse múltiples formas.
- **Necesita más preguntas para banco de preguntas:** Escribe 3x las preguntas que necesitas y rota a través de versiones de cuestionario para prevenir compartición de respuestas.
