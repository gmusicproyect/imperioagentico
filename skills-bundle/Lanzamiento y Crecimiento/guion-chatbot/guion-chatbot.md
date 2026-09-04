---
name: guion-chatbot
description: "Diseña flujos de conversación de chatbot con árboles de decisión, disparadores de entrega de control y respuestas de alternativa para interacciones automatizadas de clientes."
allowed-tools: Read Write Glob
metadata:
  author: Imperio Digital
  version: "1.0"
---

# Guión de Chatbot

## Cuándo Usar Esta Competencia

Usa esta competencia cuando necesites:
- Diseñar flujos de conversación para un chatbot cara a los clientes
- Construir árboles de decisión con lógica de bifurcación y respuestas de alternativa
- Definir cuándo el chatbot debe pasar control a un agente humano
- Crear un guión de chatbot para ventas, soporte u incorporación

## Principio Fundamental

UN CHATBOT DEBERÍA RESOLVER PREGUNTAS SIMPLES INSTANTÁNEAMENTE Y ENRUTAR PREGUNTAS COMPLEJAS A HUMANOS GRACEFULLY — EL PEOR CHATBOT ES UNO QUE HACE BUCLES SIN FIN SIN AYUDAR.

## Fase 1: Define Alcance

Determina lo que el chatbot hará y no hará.

### Entradas Requeridas

| Entrada | Qué Preguntar | Predeterminado |
|---------|-------------|--------------|
| **Propósito del chatbot** | "¿Cuál es el objetivo primario? (responder FAQs, calificar leads, enrutar soporte, incorporar usuarios)" | Responder FAQs |
| **Plataforma** | "¿Dónde vivirá el chatbot? (sitio web, Facebook Messenger, WhatsApp, en-app)" | Sitio web |
| **Escenarios principales** | "¿Cuáles son las 5-10 preguntas o solicitudes más comunes de clientes?" | Sin predeterminado |
| **Tono** | "¿Cómo debería sonar el chatbot? (profesional, amigable, casual)" | Amigable |
| **Horario de negocio** | "¿Cuándo está disponible un humano para entrega de control?" | 9 AM - 5 PM entre semana |
| **Nombre del chatbot** | "¿Debería tener nombre el chatbot?" | Ninguno / usa nombre de negocio |

## Fase 2: Construye Flujos

Diseña los árboles de decisión de conversación.

### Flujo de Bienvenida

```
## Mensaje de Bienvenida

Bot: "Hola! Soy [Nombre/Bot] de [Negocio]. Puedo ayudarte con:

1. Precios y planes
2. Cómo empezar
3. Soporte técnico
4. Hablar con una persona

¿Con qué puedo ayudarte?"

[Usuario selecciona o escribe]
```

### Plantilla de Flujo de Conversación

Para cada escenario, mapea la conversación completa:

```
## Flujo: [Nombre de Escenario]

**Disparador:** [Usuario selecciona opción o escribe palabra clave]

Bot: "[Mensaje de apertura — reconoce lo que necesitan]"

Bot: "[Pregunta aclaratoria si es necesaria]"
  → Opción A: [Camino de respuesta A]
  → Opción B: [Camino de respuesta B]
  → Opción C: [Enrutar a flujo diferente]

Bot: "[Respuesta o acción]"

Bot: "¿Respondió esto tu pregunta?
  → Sí: "¡Excelente! ¿Hay algo más con lo que pueda ayudarte?" → [Volver al menú principal o terminar]
  → No: "Déjame conectarte con [Nombre] quien puede ayudarte más." → [Entrega de control]
```

## Fase 3: Casos Extremos

Maneja las situaciones donde el chatbot no conoce la respuesta.

### Respuestas de Alternativa

```
## Alternativa: Bot No Entiende

**Después de 1 intento fallido:**
Bot: "No capté eso bien. ¿Podrías intentar reformular, o seleccionar de estas opciones?
[Mostrar opciones de menú principal]"

**Después de 2 intentos fallidos:**
Bot: "Quiero asegurar que obtengas la ayuda que necesitas. Déjame conectarte con una persona real.
[Disparador de entrega de control]"

**Nunca haz bucles más de 2 veces** — después de 2 malentendidos, enruta a humano.
```

## Fase 4: Prueba y Optimización

Valida el guión y planifica la mejora.

### Lista de Verificación de Prueba de Guión

```
- [ ] Cada flujo tiene un punto de entrada y salida claro
- [ ] Sin caminos sin salida (cada rama va a algún lugar)
- [ ] Respuesta de alternativa se dispara después de 2 malentendidos
- [ ] La entrega de control funciona durante y después de horario de negocio
- [ ] Tono es consistente en todos los flujos
- [ ] Todos los enlaces y recursos son correctos
- [ ] El bot no hace promesas excesivas o da información inexacta
```

## Anti-Patrones

- Fingir que el bot es humano — los usuarios se sienten engañados cuando descubren que es bot
- Demasiadas opciones de menú — más de 5 opciones a la vez abruma
- Bucles infinitos — "No entendí" repetido 5 veces destruye confianza
- Sin opción de entrega de control — siempre da a los usuarios una forma de alcanzar un humano
- Personalidad sobre función — un chatbot que cuenta chistes pero no puede responder preguntas es un pasivo

## Recuperación

- Los usuarios ignoran el chatbot: El mensaje de bienvenida puede ser demasiado agresivo. Prueba un enfoque pasivo: muestra el bot solo después de 30 segundos o en páginas específicas.
- Demasiadas entregas de control: El alcance del bot es demasiado estrecho. Agrega flujos para las razones principales de entrega de control.
- Los usuarios escriben libre y el bot falla: Agrega reconocimiento de palabra clave para frases comunes.
- Usuario todavía no tiene plataforma de chatbot: Entrega el guión como documento. Funciona para cualquier plataforma.
