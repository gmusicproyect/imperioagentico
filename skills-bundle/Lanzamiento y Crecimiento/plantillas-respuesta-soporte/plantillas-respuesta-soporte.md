---
name: plantillas-respuesta-soporte
description: "Escribe plantillas de respuesta de soporte al cliente para escenarios comunes con pautas de tono, indicadores de personalización y disparadores de escalamiento."
allowed-tools: Read Write Glob
metadata:
  author: Imperio Digital
  version: "1.0"
---

# Plantillas de Respuesta de Soporte

## Cuándo Usar Este Skill

Usa este skill cuando necesites:
- Crear respuestas plantilla para escenarios comunes de soporte al cliente
- Estandarizar el tono y la calidad en las interacciones de soporte
- Construir un marco de escalamiento con criterios claros de activación
- Ahorrar tiempo en respuestas repetitivas de soporte sin sonar robótico

**NO** uses este skill para artículos de centro de ayuda, guiones de chatbot o marcos de resolución de quejas. Esto es para plantillas de mensajes de soporte enviados por humanos.

---

## Principio Fundamental

LAS PLANTILLAS DE SOPORTE AHORRAN TIEMPO EN LA ESTRUCTURA PARA QUE PUEDAS INVERTIR TIEMPO EN LA PERSONALIZACIÓN — UNA BUENA PLANTILLA ES 70% REUTILIZABLE Y 30% PERSONALIZADA PARA EL CLIENTE ESPECÍFICO.

---

## Fase 1: Auditoría de Escenarios

Identifica los escenarios de soporte más comunes.

### Información Requerida

| Dato | Qué Preguntar | Predeterminado |
|------|---------------|----------------|
| **Tipo de negocio** | "¿Qué producto o servicio soportas?" | Sin predeterminado |
| **Canales de soporte** | "¿Dónde te contactan los clientes? (email, chat, redes sociales, teléfono)" | Email |
| **Top 10 preguntas** | "¿Cuáles son las 10 solicitudes de soporte más comunes que recibes?" | Sin predeterminado |
| **Plantillas actuales** | "¿Tienes alguna plantilla o respuesta predefinida existente?" | Ninguna |
| **Tono** | "¿Cómo deberían sentirse las respuestas de soporte? (formal, amigable, casual)" | Amigable y profesional |
| **Objetivo de tiempo de respuesta** | "¿Cuál es tu tiempo de respuesta objetivo?" | Menos de 4 horas |

### Categorización de Escenarios

```
## Mapa de Escenarios de Soporte

| Categoría | Escenario | Frecuencia | Complejidad | Prioridad de Plantilla |
|-----------|----------|-----------|------------|----------------------|
| Pre-venta | Pregunta de precios | Alta | Baja | ALTA |
| Onboarding | Ayuda con configuración | Alta | Media | ALTA |
| Técnico | Función no funciona | Media | Alta | ALTA |
| Facturación | Solicitud de reembolso | Media | Media | ALTA |
| General | Verificación de estado | Alta | Baja | MEDIA |
```

**PUNTO DE CONTROL: Confirma la lista de escenarios antes de escribir plantillas.**

---

## Fase 2: Escribir Plantillas

Crea plantillas de respuesta para cada escenario prioritario.

### Formato de Plantilla

Cada plantilla sigue esta estructura:

```
## Plantilla: [Nombre del Escenario]

**Usar cuando:** [Disparador específico para usar esta plantilla]
**Tono:** [Empático / Informativo / Celebratorio / De disculpa]
**Personalizar:** [Qué personalizar antes de enviar — marcado con [corchetes]]

---

Asunto: [Línea de asunto]

Hola [Nombre],

[Cuerpo — con [marcadores de personalización] para personalización]

[Cierre + siguiente paso]

[Firma]

---

**Disparador de escalamiento:** [Cuándo NO usar esta plantilla y escalar en su lugar]
```

### Biblioteca de Plantillas Comunes

**Reconocimiento / Estamos en Ello:**
```
Asunto: Recibimos tu mensaje — esto es lo que sigue

Hola [Nombre],

Gracias por contactarnos. He recibido tu [pregunta/solicitud sobre tema específico] y lo estoy revisando ahora.

Puedes esperar una respuesta completa dentro de [plazo].

Si algo cambia o tienes detalles adicionales, simplemente responde a este email.

[Nombre]
```

**Cómo Hacer / Instructivo:**
```
Asunto: Así se hace [acción]

Hola [Nombre],

¡Buena pregunta! Así se hace [acción]:

1. [Paso 1]
2. [Paso 2]
3. [Paso 3]

[Captura de pantalla o enlace si aplica]

Si tienes algún problema con estos pasos, avísame y te guío.

[Nombre]
```

**Reembolso/Problema de Facturación:**
```
Asunto: Tu reembolso ha sido procesado

Hola [Nombre],

He procesado tu reembolso de $[monto]. Deberías verlo en tu cuenta dentro de [3-5 días hábiles].

[Si aplica: Esto es lo que pasó y lo que hemos hecho para prevenirlo.]

Lamento la inconveniencia. Si hay algo más en lo que pueda ayudar, aquí estoy.

[Nombre]
```

**Disculpa / Algo Salió Mal:**
```
Asunto: Fallamos — así lo estamos arreglando

Hola [Nombre],

Tienes razón — [reconocer el problema específico]. Esa no es la experiencia que deberías tener, y lo siento.

Esto es lo que he hecho:
- [Acción 1 — solución inmediata]
- [Acción 2 — medida preventiva]

[Compensación si aplica: Como gesto, he [crédito/descuento/extensión].]

Si hay algo más que pueda hacer, por favor házmelo saber directamente.

[Nombre]
```

**Resultado Positivo / Celebración:**
```
Asunto: Buenas noticias sobre tu [solicitud/problema]

Hola [Nombre],

Buenas noticias — [resultado positivo].

[Detalles de lo que se hizo]

¿Necesitas algo más? Encantado de ayudar.

[Nombre]
```

**PUNTO DE CONTROL: Presenta la biblioteca de plantillas para revisión y personalización.**

---

## Fase 3: Guía de Tono

Define la voz y las barreras para toda la comunicación de soporte.

### Pautas de Tono

```
## Guía de Tono de Soporte

**Siempre:**
- Usa el nombre del cliente
- Reconoce su problema antes de resolverlo
- Sé específico con los plazos ("dentro de 24 horas" no "pronto")
- Termina con un siguiente paso claro u oferta de ayuda adicional

**Nunca:**
- Usar voz pasiva para la responsabilidad ("se cometieron errores")
- Culpar al cliente ("deberías haber...")
- Usar jerga que el cliente puede no entender
- Enviar una plantilla sin personalizar los campos [entre corchetes]

**Lenguaje de escalamiento:**
- "Estoy trayendo a [Nombre/Rol] que se especializa en esto" (no "No puedo ayudarte")
- "Déjame asegurarme de que la persona correcta maneje esto para ti" (no "Eso no es mi departamento")
```

### Matriz de Escalamiento

```
| Disparador | Escalar A | Plazo |
|-----------|----------|-------|
| El cliente menciona acción legal | [Dueño/Legal] | Inmediatamente |
| Problema sin resolver después de 2 respuestas | [Soporte senior] | El mismo día |
| Reembolso mayor a $[monto] | [Dueño/Finanzas] | El mismo día |
| Cliente amenaza con reseña pública | [Dueño] | Dentro de 1 hora |
| Problema técnico fuera del alcance de soporte | [Líder técnico] | Dentro de 4 horas |
```

---

## Fase 4: Mantener

Mantén las plantillas actualizadas y efectivas.

### Calendario de Revisión de Plantillas

- **Mensual:** Revisa plantillas que necesiten actualización (cambios de producto, cambios de política)
- **Trimestral:** Analiza cuáles plantillas se usan más y refínalas
- **Después de cualquier cambio de producto:** Actualiza plantillas afectadas inmediatamente

### Seguimiento de Rendimiento

```
| Métrica | Objetivo | Actual |
|---------|----------|--------|
| Tiempo promedio de respuesta | Menos de [X] horas | — |
| Tasa de resolución en primer contacto | 70%+ | — |
| Satisfacción del cliente después de soporte | 4.5+/5 | — |
| Tasa de uso de plantillas | 60%+ de respuestas | — |
```

---

## Anti-Patrones

- **Enviar plantillas sin personalización** — una respuesta claramente enlatada se siente peor que una personal lenta. Siempre personaliza.
- **Plantilla para cada caso extremo** — escribe plantillas para el 80% principal de escenarios. Maneja los casos extremos personalmente.
- **Sin empatía antes de la solución** — saltar a la solución sin reconocer la frustración se siente despectivo.
- **Plazos vagos** — "Te contactaremos pronto" crea ansiedad. "Dentro de 24 horas" crea confianza.
- **Misma plantilla para diferentes niveles de severidad** — un error de facturación y una brecha de datos requieren tonos muy diferentes.

---

## Recuperación

- **El cliente responde enojado a una plantilla:** Discúlpate, reconoce que se sintió impersonal y responde con un mensaje totalmente personalizado.
- **Las plantillas no se están usando:** Pueden ser muy difíciles de encontrar o muy rígidas. Organiza por escenario y fomenta la personalización.
- **Los tiempos de respuesta siguen lentos a pesar de las plantillas:** El cuello de botella puede ser la toma de decisiones, no la escritura. Pre-aprueba respuestas para escenarios comunes.
- **El usuario maneja todo el soporte solo:** Prioriza los 5 escenarios más comunes. Incluso 5 buenas plantillas ahorran tiempo significativo.
- **El problema del cliente no encaja en ninguna plantilla:** Escribe una respuesta personalizada. Registra el escenario — si pasa 3+ veces, crea una nueva plantilla.
