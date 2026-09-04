---
name: constructor-taller
description: Diseña currículos completos de talleres incluyendo agendas, ejercicios, handouts y guías para facilitadores. Úsalo cuando el usuario quiera planificar un taller pagado o gratuito, una sesión de capacitación, webinar con elementos interactivos o un evento educativo en vivo y necesite un currículo estructurado con timing y materiales.
allowed-tools: Read Write Bash(mkdir:*)
author: Imperio Digital
version: "1.0"
---

# Constructor de Taller

## Cuándo Usar Este Skill

- El usuario quiere crear un taller, sesión de capacitación o evento educativo en vivo
- El usuario dice "construye me un taller" o "planifica una capacitación" o "diseña una clase"
- El usuario tiene experiencia para enseñar pero necesita estructura, timing y ejercicios
- El usuario está planeando un taller pagado y necesita un currículo profesional
- El usuario quiere convertir contenido existente (curso, blog, charla) en formato de taller en vivo

## Principio Fundamental

TODO TALLER DEBE TENER UNA SOLA TRANSFORMACIÓN: los asistentes llegan en Estado A y se van en Estado B. TODO el contenido, ejercicios y timing sirven esa transformación.

## Workflow

### Fase 1: Define la Transformación

Recopila del usuario:

1. **Tema** — ¿De qué trata el taller?
2. **Transformación** — ¿Qué pueden HACER los asistentes después del taller que no podían hacer antes?
3. **Duración** — ¿Cuánto dura la sesión? (predeterminado: 90 minutos)
4. **Formato** — ¿Presencial, virtual o híbrido?
5. **Audiencia** — ¿Quiénes son los asistentes? ¿Qué ya saben?
6. **Tamaño** — Número esperado de asistentes (afecta el diseño del ejercicio)

Si el usuario proporciona un tema vago como "marketing", pregunta: "¿Cuál es el resultado específico que los asistentes deberían llevar?"

### Fase 2: Diseña la Agenda

Construye la agenda usando esta estructura probada:

| Bloque | % del Tiempo | Propósito |
|--------|-----------|---------|
| **Hook de Apertura** | 5-10% | Captura atención, establece expectativas, crea seguridad |
| **Fundación** | 15-20% | Enseña el concepto/marco central |
| **Ejercicio 1** | 15-20% | Aplica el concepto a su propia situación |
| **Inmersión Profunda** | 15-20% | Agrega matices avanzados o segundo concepto |
| **Ejercicio 2** | 15-20% | Aplica todo junto en un escenario realista |
| **Preguntas/Conversaciones** | 10-15% | Aborda situaciones individuales |
| **Cierre + Próximos Pasos** | 5-10% | Resume, asigna acción, presenta oferta (si aplica) |

**Reglas de timing:**
- Ningún bloque de clase más de 15 minutos sin interacción
- Cada ejercicio incluye: instrucciones claras, límite de tiempo, y debriefing
- Construye 5 minutos de buffer para un taller de 90 min, 10 minutos para 3+ horas
- Talleres virtuales: agrega descanso de 5 minutos cada 45 minutos

### Fase 3: Diseña Ejercicios

Cada ejercicio debe especificar:

1. **Tipo** — Reflexión individual, diálogo de parejas, pequeño grupo, sala completa o práctico
2. **Indicación** — La pregunta o tarea exacta (escrita, no resumida)
3. **Duración** — Tiempo para la actividad + tiempo para debriefing
4. **Materiales** — Qué necesitan los asistentes (hoja de trabajo, notas adhesivas, pizarrón, etc.)
5. **Método de debriefing** — Cómo compartir (voluntarios, popcorn, galería)

**Guía de selección de ejercicios:**
- Menos de 15 personas: diálogo de parejas, conversaciones activas, workshopping en vivo
- 15-50 personas: breakouts en grupos pequeños, caminatas de galería, encuestas
- 50+ personas: respuestas en chat, encuestas, reflexión individual con voluntarios

### Fase 4: Crea Materiales

Produce estos entregables:

1. **Guía del Facilitador** — Script minuto a minuto con talking points, transiciones e instrucciones de ejercicios
2. **Hoja de Trabajo para Asistentes** — Documento rellenable que los asistentes completan durante ejercicios
3. **Esquema de Diapositivas** — Recomendaciones de contenido diapositiva por diapositiva (no diapositivas reales)
4. **Pre-trabajo** (opcional) — Qué deberían hacer los asistentes antes de llegar
5. **Email de Seguimiento** — Plantilla para enganche post-taller

### Fase 5: Prueba de Estrés del Diseño

Verifica cada uno de estos antes de la entrega:

- [ ] ¿Un facilitador de primer uso puede ejecutar esto con solo la guía?
- [ ] ¿La transformación es lograble en el tiempo asignado?
- [ ] ¿Cada ejercicio sirve directamente a la transformación?
- [ ] ¿Las instrucciones son lo suficientemente específicas para que los asistentes sepan exactamente qué hacer?
- [ ] ¿Hay un plan para si se atrasa? (marca secciones opcionales para cortar)

## Ejemplo 1: Taller Pagado — "Escribe Tu Primera Secuencia de Email en 90 Minutos"

**Transformación:** Los asistentes llegan sin secuencia de email. Se van con una secuencia de bienvenida de 5 emails completa redactada y lista para cargar en su ESP.

**Formato:** Virtual vía Zoom, 20 asistentes, 90 minutos

```
AGENDA DEL TALLER: Escribe Tu Primera Secuencia de Email en 90 Minutos
==============================================================

0:00 - 0:08  HOOK DE APERTURA (8 min)
             - Muestra una secuencia de bienvenida real que generó $12K en 30 días
             - "Al final del día de hoy, tendrás tu propia versión de esto"
             - Encuesta rápida: "¿Cuántos de ustedes tienen una secuencia de bienvenida ahora?"
             - Establece reglas: cámaras encendidas, usa chat para preguntas, nos moveremos rápido

0:08 - 0:22  FUNDACIÓN: El Framework de 5 Emails (14 min)
             - Email 1: La Bienvenida + Quick Win (cumple la promesa)
             - Email 2: La Historia de Origen (por qué haces este trabajo)
             - Email 3: El Agitador de Problema (muestra que entiendes su dolor)
             - Email 4: La Social Proof (caso de estudio o testimonio)
             - Email 5: La Oferta Suave (invita al próximo paso)
             - Muestra un ejemplo real de cada uno (2 min por email)

0:22 - 0:42  EJERCICIO 1: Redacta Emails 1-3 (20 min)
             Tipo: Escritura individual con hoja de trabajo
             Indicación: "Abre tu hoja de trabajo. Para cada uno de los primeros 3 emails,
                      escribe la línea de asunto y los primeros 2 párrafos.
                      Usa las plantillas en la página 2 como punto de partida.
                      Tienes 15 minutos. Adelante."
             Materiales: Hoja de trabajo del taller (PDF pre-distribuido)
             Debriefing (5 min): 2 voluntarios comparten su línea de asunto de Email 1
                              + párrafo de apertura. Facilitador da feedback en vivo.

0:42 - 0:52  INMERSIÓN PROFUNDA: Qué Separa Buenas de Excelentes Secuencias (10 min)
             - La técnica del "open loop" entre emails
             - Fórmulas de línea de asunto que logran 40%+ tasas de apertura
             - El error que mata secuencias: vender demasiado temprano

0:52 - 1:12  EJERCICIO 2: Redacta Emails 4-5 + Refina (20 min)
             Tipo: Escritura individual, luego diálogo de parejas
             Indicación: "Redacta emails 4 y 5 usando tu hoja de trabajo. Luego vuelve
                      y agrega un open loop a cada uno de tus primeros 3 emails.
                      Después de 12 minutos, te emparejarás para revisar mutuamente
                      solo el Email 1. Tu pareja da un 'esto es fuerte' y
                      una pieza 'considera cambiar' de feedback."
             Materiales: Hoja de trabajo, salas de descanso (parejas)
             Debriefing (3 min): 1 pareja comparte su línea de asunto favorita

1:12 - 1:22  PREGUNTAS/CONVERSACIONES ACTIVAS (10 min)
             - Toma 2-3 preguntas del chat
             - Si hay tiempo: 1 conversación activa — voluntario comparte secuencia completa,
               facilitador edita en vivo

1:22 - 1:30  CIERRE + PRÓXIMOS PASOS (8 min)
             - Repasa el framework de 5 emails
             - Acción: "Carga tu secuencia en tu ESP antes del viernes.
               Responde mi follow-up email con una captura de pantalla y
               la revisaré de forma gratuita."
             - Oferta (si aplica): "Mi curso profundiza en secuencias automatizadas — enlace en chat"
             - Agradece a los asistentes

BUFFER: 5 minutos incorporados en bloque de preguntas (reducir a 5 min si se atrasa)
CORTA SI SE ATRASA: Reduce diálogo de parejas de Ejercicio 2 de 5 min a 2 min
```

**Hoja de Trabajo para Asistentes (esquema):**
```
Página 1: El Framework de 5 Emails (diagrama de referencia)
Página 2: Plantillas de email con secciones rellenables
Página 3: Hoja de trucos de fórmulas de línea de asunto (10 fórmulas)
Página 4: Ejemplos de open loop
Página 5: Espacio de redacción en blanco para los 5 emails
```

## Ejemplo 2: Taller Gratuito — "Encuentra Tus Primeros 3 Clientes de Coaching Este Mes"

**Transformación:** Los asistentes llegan inseguros de cómo conseguir clientes. Se van con un plan de adquisición específico de 30 días con acciones diarias.

**Formato:** Virtual vía Zoom, 40 asistentes, 60 minutos

```
AGENDA DEL TALLER: Encuentra Tus Primeros 3 Clientes de Coaching Este Mes
===============================================================

0:00 - 0:05  HOOK DE APERTURA (5 min)
             - "Obtuve mis primeros 3 clientes en 22 días sin sitio web,
                sin anuncios, sin una gran audiencia. Aquí está cómo."
             - Encuesta: "¿Dónde estás ahora? A) 0 clientes B) 1-2 clientes
                      C) 3+ pero inconsistente"

0:05 - 0:18  FUNDACIÓN: El Sistema de Adquisición de Clientes de 3 Canales (13 min)
             - Canal 1: Alcance cálido (personas que ya conoces)
             - Canal 2: Enganche en comunidad (grupos de Facebook, LinkedIn)
             - Canal 3: Conversaciones de contenido (estrategia de DM de posts)
             - Por qué solo necesitas 3 canales, no 10
             - Muestra las matemáticas: 10 conversaciones/día x 22 días = 3+ clientes

0:18 - 0:30  EJERCICIO 1: Construye Tu Lista de Prospectos (12 min)
             Tipo: Reflexión individual con participación en chat
             Indicación: "Abre tu hoja de trabajo. Escribe 20 nombres de personas
                      que ya sea A) podrían ser tu cliente, o B) conocen a alguien
                      que podría ser tu cliente. No filtres — solo lista.
                      Cuando llegues a 20, escribe 'LISTO' en el chat."
             Materiales: Página 1 de hoja de trabajo
             Debriefing (2 min): "¿Cuántos de ustedes se sorprendieron de poder
                               listar 20? Ese es tu mercado cálido."

0:30 - 0:40  INMERSIÓN PROFUNDA: El Framework de Conversación (10 min)
             - La secuencia de 4 mensajes DM (no vendedor, no raro)
             - Mensaje 1: Cumplido genuino o pregunta
             - Mensaje 2: Pregunta sobre su desafío actual
             - Mensaje 3: Comparte un insight rápido (valor gratuito)
             - Mensaje 4: "¿Te ayudaría si habláramos sobre esto durante 20 minutos?"
             - Demo en vivo: muestra una conversación real de DM que llevó a un cliente

0:40 - 0:50  EJERCICIO 2: Escribe Tus Primeros 3 Mensajes (10 min)
             Tipo: Escritura individual
             Indicación: "Elige una persona de tu lista. Escribe mensajes 1-3
                      usando el framework. Haz el mensaje 1 específico para
                      algo real sobre esa persona. Tienes 7 minutos."
             Materiales: Página 2 de hoja de trabajo
             Debriefing (3 min): 2 voluntarios comparten su Mensaje 1 en chat.
                              Facilitador califica y sugiere ajustes.

0:50 - 0:55  PREGUNTAS (5 min)
             - Toma 2 preguntas del chat
             - Aborda objeción común: "¿No se verá como presión?"

0:55 - 1:00  CIERRE + PRÓXIMOS PASOS (5 min)
             - Acción: "Envía 3 Mensaje 1s hoy. No mañana. Hoy."
             - "Responde mi follow-up email con lo que pasó y te guiaré
               a través del próximo paso — gratis."
             - Oferta: "Para aquellos que quieren el sistema completo con plantillas,
                       scripts y coaching semanal — enlace en chat."

CORTA SI SE ATRASA: Reduce preguntas a 2 minutos
BUFFER: Incorporado en bloque de preguntas
```

## Formato de Guía del Facilitador

Para cada bloque de agenda, la guía del facilitador incluye:

```
BLOQUE: [Nombre] — [Duración]
SAY: "[Línea de apertura exacta a decir]"
DO: [Acción física/técnica — compartir pantalla, abrir encuesta, iniciar temporizador]
SHOW: [Qué está en pantalla — número de diapositiva, demo, página de hoja de trabajo]
TRANSITION: "[Oración puente al próximo bloque]"
WATCH FOR: [Problemas comunes — caras confundidas, chat muerto, ejecutándose largo]
IF BEHIND: [Qué cortar o comprimir]
```

## Recuperación y Respuesta

- Si el usuario no puede articular la transformación, sugiere 3 opciones basadas en su tema y pídele que elija uno
- Si el taller es menor de 45 minutos, usa una estructura simplificada de 4 bloques: Hook, Enseña, Ejercicio, Cierre
- Si el taller es mayor a 3 horas, agrega descansos estructurados cada 60-75 minutos y una actividad energética a mitad
- Si el usuario quiere cubrir demasiados temas, aplica: "Una transformación por taller. ¿Cuál es el tema que, si se domina, haría que los asistentes digan que valió la pena?"
- Si los ejercicios parecen demasiado complejos, usa como predeterminado reflexión individual con uso compartido en chat (fricción más baja)

## Restricciones

- **NUNCA diseñes un taller sin ejercicios** — eventos solo de conferencia son presentaciones, no talleres
- **SIEMPRE incluye timing para cada bloque** — al minuto
- **SIEMPRE especifica qué cortar si se atrasa** — marca al menos 2 secciones cortables
- **SIEMPRE incluye una transición del facilitador** entre cada bloque
- Una transformación por taller — rechaza scope creep
- Los talleres virtuales deben tener interacción cada 10 minutos como máximo
- Los ejercicios deben incluir indicaciones exactas, no resúmenes como "que hagan lluvia de ideas"
