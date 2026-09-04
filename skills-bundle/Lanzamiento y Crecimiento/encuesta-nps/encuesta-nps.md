---
name: encuesta-nps
description: "Crea encuestas Net Promoter Score con preguntas de seguimiento, lógica de segmentación y planes de acción por respuesta para medir la lealtad del cliente."
allowed-tools: Read Write Glob
metadata:
  author: Imperio Digital
  version: "1.0"
---

# Encuesta NPS

## Cuándo Usar Este Skill

Usa este skill cuando necesites:
- Crear una encuesta Net Promoter Score con preguntas de seguimiento
- Diseñar lógica de segmentación para promotores, pasivos y detractores
- Construir planes de acción basados en las respuestas NPS
- Configurar un programa recurrente de medición NPS

**NO** uses este skill para encuestas CSAT (usa encuesta-satisfaccion), formularios de feedback de producto o investigación de mercado. Esto es específicamente para medición NPS.

---

## Principio Fundamental

NPS NO ES SOLO UN NÚMERO — ES UN SISTEMA PARA IDENTIFICAR A TUS MAYORES FANS Y TUS CLIENTES MÁS EN RIESGO, Y LUEGO ACTUAR SOBRE AMBOS.

---

## Fase 1: Diseño de Encuesta

Define la estructura de la encuesta y el target audience.

### Información Requerida

| Dato | Qué Preguntar | Valor por Defecto |
|------|--------------|-------------------|
| **Tipo de negocio** | "¿Qué producto o servicio estás midiendo?" | Sin valor por defecto |
| **Tamaño de base de clientes** | "¿Aproximadamente cuántos clientes tienes?" | Menos de 100 |
| **Momento de la encuesta** | "¿Cuándo debería enviarse la encuesta? (post-compra, trimestral, anual)" | Trimestral |
| **Método de distribución** | "¿Cómo la enviarás? (email, in-app, SMS)" | Email |
| **NPS actual** | "¿Tienes un puntaje NPS de referencia?" | Sin referencia |

**PUNTO DE CONTROL: Confirma los parámetros de la encuesta antes de redactar.**

---

## Fase 2: Construir Encuesta

Crea la encuesta NPS con lógica de seguimiento.

### Pregunta Principal NPS

```
En una escala del 0 al 10, ¿qué tan probable es que recomiendes [Nombre del Negocio/Producto] a un amigo o colega?

[0] [1] [2] [3] [4] [5] [6] [7] [8] [9] [10]
Nada probable                         Extremadamente probable
```

### Preguntas de Seguimiento (Condicionales)

**Para Detractores (0-6):**
```
Lamentamos escuchar eso. ¿Cuál es la razón principal de tu puntuación?
[ ] Calidad del producto/servicio
[ ] Atención al cliente
[ ] Precio/valor
[ ] Funcionalidades faltantes
[ ] Otro: ___________

¿Qué necesitaríamos cambiar para que nos califiques más alto?
[Campo de texto abierto]
```

**Para Pasivos (7-8):**
```
Gracias por tu opinión. ¿Qué haría que tu experiencia fuera excepcional?
[Campo de texto abierto]

¿Qué casi te hizo calificarnos más alto?
[Campo de texto abierto]
```

**Para Promotores (9-10):**
```
¡Nos alegra mucho escucharlo! ¿Qué es lo que más valoras de [Negocio/Producto]?
[Campo de texto abierto]

¿Estarías dispuesto/a a compartir tu experiencia como reseña o testimonio?
[ ] Sí, contáctenme
[ ] No, gracias
```

### Plantilla de Email de Encuesta

```
Asunto: Una pregunta rápida — 30 segundos

Hola [Nombre],

Una pregunta: ¿Qué tan probable es que recomiendes [Negocio] a un amigo o colega?

[Haz clic en tu puntuación: 0-10]

Tu opinión da forma directamente a lo que construimos y mejoramos.

Gracias,
[Nombre]
```

**PUNTO DE CONTROL: Presenta la encuesta completa para aprobación.**

---

## Fase 3: Plan de Respuesta

Define qué sucede después de cada respuesta.

### Cálculo de NPS

```
NPS = % Promotores (9-10) - % Detractores (0-6)

Rango de puntuación: -100 a +100
- Debajo de 0: Crítico — más detractores que promotores
- 0-30: Necesita mejora
- 30-50: Bueno
- 50-70: Excelente
- 70+: Clase mundial
```

### Matriz de Acciones por Respuesta

```
## Acciones de Respuesta NPS

### Detractores (0-6) — Recuperar
**Plazo:** Responder dentro de 24 horas
**Acción:**
1. Email o llamada personal del [dueño/gerente]
2. Reconocer el problema específicamente
3. Ofrecer una resolución concreta
4. Dar seguimiento dentro de 1 semana para confirmar satisfacción
**Objetivo:** Convertir a pasivo o prevenir la baja

### Pasivos (7-8) — Convertir
**Plazo:** Responder dentro de 1 semana
**Acción:**
1. Agradecerles por la feedback
2. Abordar la brecha específica que identificaron
3. Compartir una mejora próxima relevante a su feedback
**Objetivo:** Mover a territorio de promotor

### Promotores (9-10) — Activar
**Plazo:** Responder dentro de 1 semana
**Acción:**
1. Agradecerles personalmente
2. Si aceptaron dar testimonio, dar seguimiento con una plantilla simple
3. Invitar al referral program o grupo asesor
4. Pedir una reseña pública (Google, G2, etc.)
**Objetivo:** Convertir la lealtad en promoción activa
```

---

## Fase 4: Configuración del Programa

Construye un sistema recurrente de medición NPS.

### Cadencia de Medición

```
## Programa NPS

**Frecuencia:** [Trimestral / Semestral]
**Ventana de encuesta:** [2 semanas abiertas para respuestas]
**Recordatorio:** [Enviar un recordatorio después de 5 días a quienes no respondieron]
**Tasa de respuesta objetivo:** 30%+ (no ofrecer incentivos — NPS debe medir sentimiento genuino)
```

### Panel de Seguimiento

```
## Tendencia NPS

| Período | Respuestas | Promotores | Pasivos | Detractores | Puntuación NPS | Cambio |
|---------|-----------|-----------|---------|-------------|---------------|--------|
| Q1 | [#] | [%] | [%] | [%] | [Puntuación] | — |
| Q2 | [#] | [%] | [%] | [%] | [Puntuación] | [+/-] |
```

### Revisión Trimestral de NPS

1. ¿Cómo cambió el NPS vs. el período anterior?
2. ¿Qué temas aparecen en la feedback de los detractores?
3. ¿Las acciones del trimestre pasado mejoraron las puntuaciones?
4. ¿Cuántos promotores fueron activados (reseñas, referidos)?
5. ¿Qué cambio único tendría el mayor impacto en NPS el próximo trimestre?

---

## Anti-Patrones

- **Encuestar con demasiada frecuencia** — trimestral es suficiente. Las encuestas NPS mensuales causan fatiga de encuestas y bajan las tasas de respuesta.
- **No actuar sobre las respuestas** — recolectar NPS sin responder a los detractores es peor que no encuestar en absoluto.
- **Incentivar respuestas** — tarjetas de regalo por completar la encuesta sesgan los resultados hacia arriba. Mide sentimiento real.
- **Solo rastrear el número** — la puntuación NPS es menos valiosa que la feedback en texto abierto. Lee cada respuesta.
- **Seleccionar el momento** — encuestar solo después de interacciones positivas infla la puntuación y oculta problemas.

---

## Recuperación

- **Tasa de respuesta baja (menos del 20%):** Acorta la encuesta (pregunta NPS + un solo seguimiento), mejora la línea de asunto, envía desde una dirección de email personal.
- **NPS es negativo:** Enfócate en los 3 temas principales de los detractores. Corrige esos antes del próximo ciclo de encuestas.
- **El usuario tiene muy pocos clientes para significancia estadística:** NPS todavía funciona cualitativamente a pequeña escala. Lee cada respuesta como una conversación con el cliente, no como un dato estadístico.
- **Los promotores aceptan dar testimonios pero nunca cumplen:** Envía un testimonio pre-escrito para su aprobación en lugar de pedirles que escriban uno desde cero.
- **NPS no cambia a pesar de las mejoras:** Verifica si las mejoras abordan las quejas reales. A menudo los negocios arreglan lo que es fácil, no lo que los clientes pidieron.
