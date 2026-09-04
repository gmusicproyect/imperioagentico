---
name: constructor-encuestas
description: "Crea encuestas de feedback de cliente con preguntas estratégicamente ordenadas, escalas de respuesta y marcos de análisis para medir satisfacción, recabar feedback de producto o validar nuevas ideas."
allowed-tools: Read Write Glob
metadata:
  author: Imperio Digital
  version: "1.0"
---

# Constructor de Encuestas

## Cuándo Usar Este Skill

Usa este skill cuando necesites:
- Crear una encuesta de satisfacción del cliente (CSAT) o Puntuación de Promotor Neto (NPS)
- Construir una encuesta de feedback de producto para mejorar una oferta existente
- Diseñar una encuesta de validación de mercado antes de construir un nuevo producto o feature
- Escribir una encuesta post-compra para una tienda de ecommerce o producto digital
- Construir una encuesta de salida de churn para entender por qué se van los clientes
- Recopilar feedback estructurado de clientes, estudiantes, miembros o asistentes a eventos

**NO USES** este skill para encuestas de investigación académica o científica, evaluaciones médicas o psicológicas, encuestas de engagement de empleados o RRHH, o cuestionarios, pruebas o evaluaciones con respuestas correctas/incorrectas.

---

## Workflow Central

CADA ENCUESTA COMIENZA CON UN OBJETIVO CLARO ANTES DE ESCRIBIR UNA SOLA PREGUNTA — UNA ENCUESTA SIN PROPÓSITO DEFINIDO PRODUCE DATOS QUE NADIE PUEDE ACTUAR.

### Paso 1: Estrategia

Recopila estos detalles antes de escribir preguntas:

1. **Objetivo de la encuesta** — ¿qué decisión informará este dato? (requerido)
2. **Tipo de encuesta** — CSAT, NPS, Feedback de Producto, Validación de Mercado, Post-Compra, o Salida de Churn (por defecto: inferir del objetivo)
3. **Respondiente objetivo** — ¿quién toma esta encuesta? (requerido)
4. **Método de distribución** — email, popup en-app, enlace en sitio, redes sociales, código QR (por defecto: email)
5. **Presupuesto de preguntas** — ¿cuántas preguntas máximo? (por defecto: 8-12)
6. **Incentivo** — código de descuento, entrada a sorteo, recurso gratuito, ninguno (por defecto: ninguno)

**PUNTO DE CONTROL: No procedes hasta tener: objetivo de encuesta Y respondiente objetivo.**

### Paso 2: Construir

Escribe preguntas siguiendo principios de ciencia de encuestas en este orden exacto:

1. **Comienza con pregunta de calentamiento o screening** — fácil, no amenazante, construye momentum
2. **Agrupa preguntas por tema** — no saltes entre temas
3. **Coloca pregunta ancla temprano** — pregunta central de CSAT o NPS en posición 2-4
4. **Coloca preguntas sensibles en el medio** — precios, quejas, uso competidor
5. **Termina con pregunta abierta** — "¿Hay algo más que quieras compartir?"
6. **Demografía al final** — solo si es necesario, explica por qué preguntas

**Reglas de escritura de preguntas — aplica a CADA pregunta:**
- Un concepto por pregunta. Nunca dos cañones
- Redacción neutral. Nunca indicadora
- Escalas balanceadas. Incluye opciones negativas, neutras y positivas
- Incluye "N/A" o "Prefiero no contestar" donde la pregunta no aplique a todos
- Mantén preguntas bajo 25 palabras
- Evita jerga, abreviaciones y terminología interna

### Paso 3: Presentar

Muestra la encuesta completa para aprobación con:
- Título y texto de introducción (qué es la encuesta, tiempo estimado, incentivo si aplica)
- Todas las preguntas numeradas con tipos, opciones y lógica
- Mensaje de finalización/agradecimiento
- Tiempo estimado total de completación

**PUNTO DE CONTROL: No escribas archivos hasta que el usuario apruebe la encuesta.**

### Paso 4: Entregar

Después de aprobación, entregar en formato Markdown con:
- Encuesta completa con todas las preguntas
- Marco de análisis: cómo calcular métricas principales
- Benchmarks de tasa de respuesta por canal
- Cómo analizar respuestas abiertas
- Cuándo actuar vs. recopilar más datos

---

## Anti-Patrones

- **NO ESCRIBAS** preguntas indicadoras. "¿Cuánto amaste nuestro producto?" asume respuesta positiva. Escribe: "¿Cuán satisfecho estás con nuestro producto?"
- **NO CREES** encuestas más largas que 15 preguntas sin justificación explícita del usuario. Cada pregunta más allá de 12 baja tasas de completación 5-10%.
- **NO USES** preguntas de dos cañones. "¿Cuán satisfecho estás con nuestro producto y servicio al cliente?" mide dos cosas. Divide en dos preguntas.
- **NO COLOQUES** preguntas demográficas primero. Las demografías se sienten invasivas como aperturas e incrementan abandono. Coloca al final, incluye solo si es necesario.
- **NO USES** escalas desbalanceadas. Una escala con "Terrible, Malo, Okay, Bueno, Excelente, Asombroso, Extraordinario" está sesgada hacia respuestas positivas. Usa opciones balanceadas.
- **NO HAGAS** toda pregunta requerida. Preguntas abiertas y sensibles deben ser opcionales. Las abiertas requeridas producen respuestas basura como "N/A".
- **NO USES** jerga o lenguaje interno. "¿Cómo calificarías nuestra optimización de touchpoint NPS?" significa nada para un cliente. Escribe en el lenguaje que los respondientes usan.
- **NO INCLUYAS** "Otro (especifica)" en toda pregunta de opción múltiple. Solo añade cuando la lista genuinamente no puede cubrir todas posibilidades.
- **NO SALTES** el marco de análisis. Una encuesta sin plan para interpretar resultados produce una hoja de cálculo que nadie lee.

---

## Recuperación

- **Usuario no puede articular el objetivo de la encuesta:** Pregunta: "¿Qué decisión tomarás diferente basada en los resultados?" Si sigue vago, ofrece los 3 objetivos más comunes.
- **Usuario quiere más de 15 preguntas:** Explica el trade-off: "Cada pregunta más allá de 12 baja tu tasa de completación 5-10%. Una encuesta de 20 preguntas puede recibir mitad de respuestas que una de 10."
- **Usuario quiere encuestar gente a la que no tiene acceso:** Pregunta cómo llegará a ellos. Si no hay acceso: sugiere construir audiencia primero, ofrece crear encuesta ahora para tener lista.
