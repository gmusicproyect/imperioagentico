---
name: encuesta-satisfaccion
description: "Crea encuestas de satisfacción del cliente (CSAT/NPS) (CSAT) con preguntas específicas por punto de contacto y marcos de benchmarking para medir la calidad del servicio."
allowed-tools: Read Write Glob
metadata:
  author: Imperio Digital
  version: "1.0"
---

# Encuesta de Satisfacción

## Cuándo Usar Este Skill

Usa este skill cuando necesites:
- Crear una encuesta CSAT vinculada a puntos de contacto específicos del cliente
- Diseñar preguntas que produzcan feedback accionable y medible
- Construir marcos de benchmarking para rastrear la satisfacción a lo largo del tiempo
- Establecer un programa recurrente de medición de satisfacción

**NO** uses este skill para encuestas NPS (usa encuesta-nps), investigación de mercado o formularios de feedback de producto. Esto es específicamente para medir la satisfacción del cliente con interacciones y experiencias.

---

## Principio Fundamental

CSAT MIDE QUÉ TAN BIEN CUMPLISTE UNA PROMESA ESPECÍFICA EN UN MOMENTO ESPECÍFICO — A DIFERENCIA DE NPS (LEALTAD) O CES (ESFUERZO), CSAT TE DICE SI EL CLIENTE OBTUVO LO QUE ESPERABA AHORA MISMO.

---

## Fase 1: Definir Puntos de Contacto

Identifica qué interacciones con el cliente medir.

### Información Requerida

| Dato | Qué Preguntar | Predeterminado |
|------|---------------|----------------|
| **Tipo de negocio** | "¿Qué producto o servicio proporcionas?" | Sin predeterminado |
| **Puntos de contacto** | "¿En qué momentos interactúas con los clientes? (compra, onboarding, soporte, entrega)" | Sin predeterminado |
| **Objetivo de medición** | "¿Estás midiendo una interacción específica o la satisfacción general?" | Punto de contacto específico |
| **Método de distribución** | "¿Cómo enviarás las encuestas? (email, in-app, post-interacción)" | Email |
| **Línea base CSAT actual** | "¿Has medido la satisfacción antes?" | Sin línea base |

### Mapa de Puntos de Contacto

```
## Plan de Medición por Punto de Contacto

| Punto de Contacto | Cuándo Encuestar | Método | Tasa de Respuesta Objetivo |
|-------------------|-----------------|--------|---------------------------|
| Post-compra | Dentro de 24 horas | Email | 25%+ |
| Post-onboarding | Día 7-14 | Email | 30%+ |
| Post-soporte | Después de cerrar ticket | Link en ticket | 20%+ |
| Post-entrega | Después de recibir entregable | Email | 25%+ |
| Check-in periódico | Trimestral | Email | 30%+ |
```

**PUNTO DE CONTROL: Confirma los puntos de contacto antes de diseñar la encuesta.**

---

## Fase 2: Construir Encuesta

Crea encuestas CSAT específicas por punto de contacto.

### Formato de Pregunta CSAT

```
¿Qué tan satisfecho/a estuviste con [interacción específica]?

[ 1 - Muy Insatisfecho ]
[ 2 - Insatisfecho ]
[ 3 - Neutral ]
[ 4 - Satisfecho ]
[ 5 - Muy Satisfecho ]
```

**Puntuación CSAT = (# de 4s y 5s / Total de respuestas) x 100**

### Plantillas de Encuesta por Punto de Contacto

**Encuesta Post-Compra:**
```
1. ¿Qué tan satisfecho/a estás con tu experiencia de compra? (1-5)
2. ¿Qué tan fácil fue el proceso de compra? (1-5)
3. ¿Qué, si algo, casi te detuvo de comprar? [Texto abierto]
4. ¿Algo que podamos mejorar? [Texto abierto]
```

**Encuesta Post-Soporte:**
```
1. ¿Qué tan satisfecho/a estás con el soporte que recibiste? (1-5)
2. ¿Se resolvió tu problema? (Sí / Parcialmente / No)
3. ¿Cómo describirías el tiempo de respuesta? (Muy lento / Adecuado / Rápido)
4. ¿Alguna sugerencia para mejorar nuestro soporte? [Texto abierto]
```

**Encuesta Post-Entrega:**
```
1. ¿Qué tan satisfecho/a estás con lo entregado? (1-5)
2. ¿El entregable cumplió tus expectativas? (Superó / Cumplió / Por debajo)
3. ¿Qué te gustó más? [Texto abierto]
4. ¿Qué podría mejorarse? [Texto abierto]
```

**Encuesta General Trimestral:**
```
1. En general, ¿qué tan satisfecho/a estás con [Nombre del Negocio]? (1-5)
2. ¿Con qué área estás más satisfecho/a? [Opción múltiple: Producto / Soporte / Comunicación / Valor]
3. ¿Qué área necesita más mejora? [Mismas opciones]
4. ¿Hay algo específico que te gustaría que cambiáramos? [Texto abierto]
```

### Plantilla de Email para Encuesta

```
Asunto: ¿Feedback rápida? (Toma 60 segundos)

Hola [Nombre],

[Una oración sobre la interacción reciente — "Acabas de [completar tu compra / recibir soporte / obtener tu entregable]."]

Me encantaría tu feedback rápida:

**¿Qué tan satisfecho/a estuviste?** [Haz clic en un número: 1-5]

Tu respuesta nos ayuda a mejorar. ¡Gracias!

[Nombre]
```

**PUNTO DE CONTROL: Presenta la encuesta para revisión antes de construir los benchmarks.**

---

## Fase 3: Benchmarking

Establece marcos de medición y seguimiento.

### Dashboard CSAT

```
## Dashboard CSAT — [Período]

### General
| Período | Respuestas | Puntuación CSAT | Tendencia |
|---------|-----------|----------------|-----------|
| [Mes 1] | [#] | [%] | — |
| [Mes 2] | [#] | [%] | [+/-%] |

### Por Punto de Contacto
| Punto de Contacto | Respuestas | Puntuación CSAT | Objetivo | Estado |
|-------------------|-----------|----------------|----------|--------|
| Post-compra | [#] | [%] | 85%+ | En/Fuera de Objetivo |
| Post-soporte | [#] | [%] | 90%+ | En/Fuera de Objetivo |
| Post-entrega | [#] | [%] | 85%+ | En/Fuera de Objetivo |
```

### Benchmarks de la Industria

| Industria | CSAT Promedio |
|-----------|-------------|
| SaaS | 78% |
| E-commerce | 80% |
| Servicios profesionales | 82% |
| Salud | 74% |

Objetivo: 5-10 puntos por encima del promedio de tu industria.

### Análisis de Segmentación

Desglosa el CSAT por segmento de cliente para encontrar patrones ocultos:
- Por antigüedad del cliente (nuevos vs. largo plazo)
- Por nivel de plan (gratis vs. pagado vs. premium)
- Por caso de uso o línea de producto

---

## Fase 4: Actuar

Convierte los datos de satisfacción en mejoras.

### Protocolo de Respuesta

```
## Acciones de Respuesta CSAT

| Puntuación | Acción | Plazo |
|-----------|--------|-------|
| 1-2 (Insatisfecho) | Contacto personal para entender y resolver | Dentro de 48 horas |
| 3 (Neutral) | Email de seguimiento preguntando qué mejoraría la experiencia | Dentro de 1 semana |
| 4-5 (Satisfecho) | Email de agradecimiento + solicitud de reseña o referido | Dentro de 1 semana |
```

### Revisión Mensual de CSAT

1. ¿Cuál es la tendencia general del CSAT?
2. ¿Qué punto de contacto tiene la puntuación más baja? ¿Por qué?
3. ¿Qué temas aparecen en las respuestas de texto abierto?
4. ¿Qué cambio único mejoraría el punto de contacto con menor puntuación?
5. ¿Las mejoras previas han impactado las puntuaciones?

### Cerrar el Ciclo

Después de implementar cambios basados en feedback CSAT:
- Notifica a los encuestados que su feedback generó cambios
- Vuelve a medir el punto de contacto para confirmar la mejora
- Comparte las mejoras de CSAT con el equipo

---

## Anti-Patrones

- **Encuestar cada interacción** — enviar una encuesta después de cada email genera fatiga. Encuesta solo en momentos clave.
- **Encuestas largas** — más de 5 preguntas mata las tasas de completación. Mantén las encuestas CSAT en menos de 2 minutos.
- **No actuar sobre puntuaciones bajas** — recopilar datos de satisfacción sin seguimiento es peor que no preguntar.
- **Solo medir satisfacción general** — el CSAT por punto de contacto revela dónde están los problemas. El CSAT general los oculta.
- **Celebrar puntuaciones altas sin investigar** — 90% CSAT con 10% tasa de respuesta puede significar que solo los clientes felices responden.

---

## Recuperación

- **Tasas de respuesta bajas:** Acorta la encuesta a 1-2 preguntas. Mejora el asunto del email. Envía dentro de 1 hora de la interacción.
- **La puntuación CSAT cae repentinamente:** Busca un incidente específico o cambio de proceso que coincida con la caída. No asumas una tendencia de un solo período.
- **Todas las respuestas son 4-5 (sospechosamente alto):** Agrega una pregunta de texto abierto que invite a la crítica: "¿Cuál es la ÚNICA cosa que podríamos hacer mejor?"
- **El usuario no tiene herramienta de encuestas:** Usa un Google Form simple o Typeform gratuito. Incluso un formato de responder-a-este-email funciona a pequeña escala.
- **El usuario no sabe qué puntos de contacto medir:** Comienza con post-soporte (mayor señal para mejoras) y post-compra (mayor señal para marketing).
