---
name: recuperacion-carrito-sms
description: "Escribe mensajes SMS de recuperación de carrito con timing, tokens de personalización y disclaimers de cumplimiento. Úsalo cuando necesites recuperar carritos abandonados vía mensaje de texto."
allowed-tools: Read Write Glob
metadata:
  author: Imperio Digital
  version: "1.0"
---

# SMS de Recuperación de Carrito

## Cuándo Usar Este Skill

Usa este skill cuando necesites:
- Escribir mensajes SMS que recuperen carritos de compra abandonados
- Diseñar una secuencia SMS cronometrada disparada por abandono de carrito
- Incluir tokens de personalización y referencias de producto dinámicas
- Asegurar cumplimiento con regulaciones de marketing SMS (TCPA, GDPR)

**NO** uses este skill para recuperación de carrito por email, campañas generales de marketing SMS, o actualizaciones de pedidos transaccionales. Esto es específicamente para recuperación de abandono de carrito basada en SMS.

---

## Principio Fundamental

SMS ES TERRITORIO PERSONAL — CADA MENSAJE DEBE SENTIRSE COMO UN EMPUJÓN ÚTIL DE UNA MARCA EN LA QUE CONFÍAN, NO COMO UNA INTRUSIÓN EN SU TELÉFONO.

---

## Fase 1: Resumen

### Entradas Requeridas

| Entrada | Qué Preguntar | Por Defecto |
|-------|------------|---------|
| **Tipo de producto** | "¿Qué vendes? (físico, digital, servicio)" | Sin valor por defecto — debe ser proporcionado |
| **Valor promedio del carrito** | "¿Cuál es el valor típico del carrito abandonado?" | $50-100 |
| **Incentivo disponible** | "¿Puedes ofrecer descuento o envío gratis para recuperar?" | Código de descuento 10% |
| **Voz de marca** | "¿Casual, profesional, juguetón?" | Amigable y casual |
| **Plataforma SMS** | "¿Qué herramienta SMS usas?" | Agnóstica a la plataforma |
| **Método de opt-in** | "¿Cómo consintieron los clientes al SMS?" | Casilla de opt-in de checkout |

**PUNTO DE CONTROL: Confirma el resumen antes de escribir mensajes.**

---

## Fase 2: Diseño de Secuencia de Mensajes

### Marco de Timing

```
## Secuencia SMS de Recuperación de Carrito

Mensaje 1 — 30 minutos después del abandono
Propósito: Recordatorio suave, sin incentivo
Tono: Útil

Mensaje 2 — 4 horas después del abandono
Propósito: Aborda objeción común o añade social proof
Tono: Conversacional

Mensaje 3 — 24 horas después del abandono
Propósito: Ofrece incentivo (descuento o bonificación)
Tono: Generoso

Mensaje 4 (opcional) — 48 horas después del abandono
Propósito: Última oportunidad, urgencia en incentivo que vence
Tono: Directo
```

### Condiciones de Salida

- Cliente completa compra → detén todos los mensajes inmediatamente
- Cliente responde STOP → elimina de secuencia y todo marketing SMS
- Sin respuesta después del Mensaje 3/4 → termina secuencia, no añadas a futura recuperación de carrito

**PUNTO DE CONTROL: Aprueba el timing de secuencia antes de escribir mensajes.**

---

## Fase 3: Escribir Mensajes

### Reglas de Escritura SMS

- **160 caracteres o menos** por mensaje (evita mensajes de múltiples partes)
- **Incluye nombre de marca** en el primer mensaje para que sepan quién es
- **Un enlace por mensaje** — URL acortada a su carrito
- **Tokens de personalización:** {first_name}, {product_name}, {cart_url}
- **Instrucciones de opt-out** en el primer mensaje: "Responde STOP para optar por no participar"

### Plantillas de Mensajes

**Mensaje 1 (30 min):**
```
¡Hola {first_name}! Dejaste algo en tu carrito en [Marca]. ¿Todavía interesado? Completa tu pedido aquí: {cart_url} Responde STOP para optar por no participar
```

**Mensaje 2 (4 horas):**
```
{first_name}, tu {product_name} todavía te espera. Cientos de clientes felices aman el suyo. Tómalo antes de que se vaya: {cart_url}
```

**Mensaje 3 (24 horas):**
```
¿Todavía lo estás pensando? Aquí hay 10% de descuento en tu carrito en [Marca]. Usa el código SAVE10 en checkout: {cart_url} Vence en 24hrs.
```

**Mensaje 4 (48 horas):**
```
Última oportunidad, {first_name}. Tu código 10% de descuento vence hoy. Completa tu pedido: {cart_url}
```

---

## Fase 4: Pulir

### 1. Lista de Verificación de Cumplimiento

- [ ] Clientes optaron explícitamente en marketing SMS (no casillas pre-marcadas)
- [ ] Primer mensaje incluye identificación de nombre de marca
- [ ] Instrucciones de opt-out STOP incluidas en primer mensaje
- [ ] Todos los mensajes enviados durante horas de cumplimiento (8am-9pm zona horaria del receptor)
- [ ] Códigos de descuento tienen fechas de vencimiento reales
- [ ] Política de privacidad cubre marketing SMS

### 2. Notas de Configuración de Plataforma

- Configuración de acortador de enlace para seguimiento
- Mapeo de token de personalización de datos de carrito
- Disparador de evento de compra para detener secuencia
- Configuración de horas silenciosas por zona horaria

### 3. Benchmarks de Desempeño

- Tasa de recuperación de carrito SMS: 10-15% (vs. 3-5% solo email)
- Tasa de clic: 20-30%
- Tasa de opt-out por mensaje: menos de 2% (por encima de esto, reduce frecuencia)
- Ingresos por mensaje enviado

---

## Anti-Patrones

- **Enviar SMS sin consentimiento explícito** — esto viola TCPA y puede resultar en multas de $500-$1,500 por mensaje.
- **Mensajes superiores a 160 caracteres** — mensajes de múltiples partes se sienten spammy y cuestan más.
- **Sin opción de opt-out** — legalmente requerido y debe ser honrado inmediatamente.
- **Enviar a las 2am** — respeta horas silenciosas. La mayoría de plataformas aplican 8am-9pm hora local.
- **Cuatro mensajes sin incentivo** — si no estás dispuesto a ofrecer descuento, limita a 2 mensajes.
- **Mensajes genéricos** — "¡Olvidaste algo!" sin nombre de producto o marca se siente como spam.

---

## Recuperación

- **Sin incentivo disponible:** Elimina Mensajes 3-4. Usa solo los mensajes de recordatorio y social proof. Máximo dos mensajes.
- **Usuario inseguro sobre cumplimiento:** Proporciona un resumen de cumplimiento pero recomienda consultar un profesional legal para su mercado específico (US/TCPA, EU/GDPR, CA/CASL).
- **Tasa de opt-out alta:** Reduce a 2 mensajes, extiende timing (1 hora y 24 horas), y suaviza el tono.
- **Valor bajo de carrito (menos de $20):** Un único mensaje SMS a 1 hora es suficiente. El costo de múltiples mensajes puede no justificar el valor de recuperación.
