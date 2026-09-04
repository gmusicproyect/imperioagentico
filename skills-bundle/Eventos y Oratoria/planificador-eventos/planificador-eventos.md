---
name: planificador-eventos
description: "Planifica eventos virtuales e in-person con listas de verificación detalladas, cronogramas, documentos de run-of-show, copia promocional y comunicaciones a asistentes, con páginas de planificación opcionales en Notion. Úsalo cuando un usuario esté organizando un workshop, conferencia, meetup, lanzamiento de producto, networking event o cualquier evento que necesite planificación estructurada y materiales de comunicación."
allowed-tools: Read Write Glob mcp__claude_ai_Notion__notion-create-pages mcp__claude_ai_Notion__notion-search mcp__claude_ai_Notion__notion-create-database
metadata:
  author: Imperio Digital
  version: "1.0"
---

# Planificador de Eventos

## Cuándo Usar Este Skill

Usa este skill cuando necesites:
- Planificar un workshop, conferencia, meetup, lanzamiento de producto o networking event desde cero
- Construir una lista de verificación maestra con hitos de cronograma para cualquier tipo de evento
- Crear un documento de run-of-show con programación minuto por minuto
- Escribir copia promocional incluyendo páginas de registro, secuencias de email y posts en redes
- Redactar comunicaciones a asistentes (mensajes de bienvenida, recordatorios, seguimientos)
- Opcionalmente guardar la lista de verificación de planificación y el run-of-show en Notion

**NO** uses este skill para:
- Webinars o presentaciones virtuales con decks (usa webinar-planner en su lugar)
- Contenido de cursos pregrabados (usa course-outline en su lugar)
- Programación de contenido continuo sin un ancla de evento (usa content-calendar en su lugar)
- Secuencias de email sin relación a un evento (usa email-sequence en su lugar)

---

## Principio Fundamental

CADA EVENTO EXISTE PARA LOGRAR UN OBJETIVO MEDIBLE PARA EL ANFITRIÓN Y UN RESULTADO CLARO PARA EL ASISTENTE — SI NO PUEDES ENUNCIAR AMBOS EN UNA ORACIÓN, EL EVENTO NO ESTÁ LISTO PARA PLANIFICAR.

---

## Referencia de Tipos de Evento

| Tipo | Duración Típica | Formato | Logística Clave | Objetivo Predeterminado |
|------|-----------------|--------|---------------|-------------|
| **Workshop** | 2-4 horas | In-person o virtual | Materiales prácticos, espacio de descanso, AV | Educación |
| **Conferencia** | Día completo+ | In-person o híbrido | Múltiples salas, speakers, catering, señalización | Autoridad |
| **Meetup** | 1-2 horas | In-person | Venue casual, name tags, refrigerios ligeros | Comunidad |
| **Lanzamiento de Producto** | 2-3 horas | In-person o virtual | Área de demo, decoración de marca, fotógrafo | Rumor |
| **Networking Event** | 1.5-3 horas | In-person | Plano abierto, activadores de conversación, name tags | Lead gen |

---

## Fase 1: Brief

Recopila todos los detalles del evento antes de crear cualquier material.

1. **Nombre del evento** — cómo se llama el evento (preguntar, sin predeterminado)
2. **Tipo de evento** — workshop, conferencia, meetup, lanzamiento de producto o networking (preguntar, sin predeterminado)
3. **Formato** — in-person, virtual o híbrido (preguntar, sin predeterminado)
4. **Fecha y hora** — cuándo ocurre el evento (preguntar, sin predeterminado)
5. **Objetivo** — leads, ventas, comunidad, educación o conciencia de marca (preguntar, sin predeterminado)
6. **Asistencia esperada** — cuántas personas (50 por predeterminado)
7. **Venue o plataforma** — ubicación física o plataforma virtual (Zoom por predeterminado para virtual)
8. **Rango de presupuesto** — presupuesto total del evento (continuar sin si el usuario declina)
9. **Speakers o anfitriones** — nombres y títulos de quien presente (solo anfitrión por predeterminado)
10. **Audiencia objetivo** — quién debería asistir y qué problema resuelve para ellos (preguntar, sin predeterminado)

### Plantilla de Brief del Evento

```
## Brief del Evento

**Evento:** Kickoff de Content Creator — Networking Night Q2
**Tipo:** Networking event
**Formato:** In-person
**Fecha/Hora:** 18 de abril de 2026 a las 6:00 PM PST
**Objetivo:** Generar 15 leads cálidos para programa de coaching
**Asistencia Esperada:** 40 personas
**Venue:** The Hive Coworking, Portland OR — Espacio de evento principal
**Presupuesto:** $500
**Speakers/Anfitriones:** Jamie Lawson, Business Coach
**Audiencia Objetivo:** Content creators y solopreneurs locales que quieren crecer su red
```

**PUNTO DE CONTROL:** No continúes a la Fase 2 hasta que el usuario confirme tipo de evento, formato, fecha y objetivo. Asistencia, venue, presupuesto y speakers pueden usar predeterminados o quedar como TBD.

---

## Fase 2: Plan

Construye la lista de verificación de planificación maestra, documento de run-of-show y rastreador de presupuesto.

### Lista de Verificación Maestra por Cronograma

**4+ Semanas Antes:**
- [ ] Confirmar venue o plataforma — firmar contrato, pagar depósito, obtener plano o enlace de sala virtual
- [ ] Confirmar speakers o panelistas — enviar emails de confirmación con expectativas
- [ ] Redactar la agenda del evento — bloques de tiempo, títulos de sesión, períodos de descanso
- [ ] Configurar página de registro — Eventbrite, Lu.ma, Google Forms o landing page
- [ ] Crear rastreador de presupuesto de evento — venue, catering, marketing, materiales, contingencia
- [ ] Ordenar materiales de marca — name tags, señalización, banners, agendas impresas

**2-3 Semanas Antes:**
- [ ] Lanzar empujón promocional — email de anuncio, redes sociales, alcance de partners
- [ ] Contactar sponsors si aplica — enviar hoja informativa de patrocinio
- [ ] Preparar materiales de presentación — slides, handouts, worksheets, equipo de demo
- [ ] Arrancar catering o refrigerios — confirmar conteo de cabezas, finalizar menú
- [ ] Asignar roles del día del evento — desk de registro, AV, enlace speaker, fotografía

**1 Semana Antes:**
- [ ] Enviar email de recordatorio a asistentes — fecha, hora, venue/enlace, estacionamiento, qué llevar
- [ ] Realizar tech check para virtual/híbrido — plataforma, screen sharing, grabación, backup
- [ ] Finalizar run-of-show — minuto por minuto con dueño de cada segmento
- [ ] Confirmar todos los vendors — catering, alquiler AV, fotógrafo, contacto venue
- [ ] Imprimir lista de asistentes y name tags (in-person)

**Día del Evento:**
- [ ] Llegar temprano — 90 min antes para in-person, 30 min para virtual
- [ ] Ejecutar tech check final — micrófonos, proyector, WiFi, grabación
- [ ] Briefing a todos los voluntarios — revisar run-of-show, asignar estaciones
- [ ] Configurar área de registro/check-in
- [ ] Probar plan de backup — hotspot, slides backup en USB, número de contacto venue

**Después del Evento:**
- [ ] Enviar email de agradecimiento dentro de 24 horas
- [ ] Enviar encuesta de feedback dentro de 48 horas (3-5 preguntas)
- [ ] Compilar métricas del evento — tasa de asistencia, puntuaciones de feedback, leads recopilados
- [ ] Reutilizar contenido del evento — blog post de resumen, fotos en redes, highlight reel
- [ ] Dar seguimiento a nuevos contactos — emails personalizados dentro de 72 horas

### Plantilla de Run-of-Show

Crea un cronograma minuto por minuto con dueño, cues técnicos y notas para cada segmento. Cada run-of-show debe incluir setup previo al evento, segmentos del evento en vivo y tareas posteriores al evento.

```
## Run-of-Show: Kickoff de Content Creator
## 18 de abril de 2026 | 6:00 PM PST | The Hive Coworking

PRE-EVENTO (4:30 - 6:00 PM)
  4:30  Llegar, confirmar layout de sala          Dueño: Jamie
  5:00  Test AV, configurar mesa de registro    Dueño: Alex
  5:30  Caminata de voluntarios por run-of-show Dueño: Jamie
  5:45  Abrir puertas, música de fondo          Dueño: Alex

EVENTO EN VIVO (6:00 - 8:30 PM)
  6:00  Puertas abren — registro, networking gratuito
        Tech: Playlist de música, slide de bienvenida en proyector
  6:15  Bienvenida + housekeeping (10 min)       Dueño: Jamie
        Cubrir: Wi-Fi, baños, hashtag, formato de la noche
  6:25  Icebreaker — intros estructurados (20 min) Dueño: Jamie
        Dividir en grupos de 10. Cada persona: nombre, qué crean,
        una cosa en la que necesiten ayuda.
  6:45  Charla destacada (15 min)                Dueño: Jamie
        "3 Modelos de Colaboración Que Realmente Funcionan para Creators"
  7:00  Ronda de networking 1 — "Encuentra Tu Match" (20 min)
        Cada persona tiene una tarjeta: su "oferta" y su "necesidad."
  7:20  Descanso — refrigerios, conversación abierta (15 min)
  7:35  Ronda de networking 2 — "Lightning Intros" (30 min)
        Grupos de 5, 2 min cada uno, rotar dos veces.
  8:05  Observaciones de cierre + próximos pasos (10 min) Dueño: Jamie
        Código QR para encuesta de feedback y lista de emails
  8:15  Networking abierto hasta cierre
  8:30  Evento termina — limpieza

POST-EVENTO
  8:30  Recopilar lista de asistentes, debriefing con voluntarios (10 min)
  Al día siguiente: Email de agradecimiento + encuesta de feedback
  Dentro de 72 horas: Emails de seguimiento de leads
```

### Plantilla de Rastreador de Presupuesto

Si el usuario proporciona un presupuesto, crea un rastreador. Salta si no hay presupuesto.

```
| Categoría | Artículo | Estimado | Real | Notas |
|----------|------|-----------|--------|-------|
| Venue | The Hive — alquiler de 4 horas | $150 | — | Incluye mesas, sillas, proyector |
| Catering | Appetizers + bebidas (40 ppl) | $200 | — | Ordenado 2 semanas antes |
| Materiales | Name tags, señalización | $40 | — | Vistaprint |
| Marketing | Eventbrite anuncio promocionado | $50 | — | Opcional |
| Contingencia | Costos inesperados (12%) | $60 | — | Fondo de reserva |
| **Total** | | **$500** | — | |
```

### Opcional: Guardar en Notion

1. Llama a `mcp__claude_ai_Notion__notion-search` para encontrar la página padre
2. Llama a `mcp__claude_ai_Notion__notion-create-pages` con brief del evento, lista de verificación (bloques to-do), run-of-show y rastreador de presupuesto
3. Confirma publicación al usuario

**SI NOTION FALLA DESPUÉS DE 3 INTENTOS:** Entrega como archivos markdown locales.

**PUNTO DE CONTROL:** Presenta la lista de verificación maestra, run-of-show y rastreador de presupuesto. No continúes a la Fase 3 hasta que el usuario apruebe.

---

## Fase 3: Promote

Construye copia de página de registro, secuencia promocional de 3 emails y posts en redes sociales.

### Copia de Página de Registro

Incluye estas secciones: headline + subheadline, 3-5 bullets de beneficios, bio del anfitrión, detalles del evento (fecha, hora con zona horaria, dirección o enlace, estacionamiento/login, precio, capacidad), texto del botón CTA, calificadores "Esto es para ti si..." y "Esto NO es para ti si...".

```
HEADLINE: Kickoff de Content Creator — Q2 Networking Night
Conoce a los Creators Que Harán Tu Próximo Trimestre Contar

SUBHEADLINE: 18 de abril a las 6:00 PM PST | The Hive Coworking, Portland OR | Gratuito

BENEFICIOS:
- Conoce 40+ creators y solopreneurs locales en una sala
- Vete con al menos 3 conexiones emparejadas a tus habilidades y objetivos
- Aprende 3 modelos de colaboración comprobados de la charla destacada de Jamie Lawson
- Networking estructurado que evita las charlas triviales
- Appetizers ligeros y bebidas incluidas

CTA: Reserva Mi Lugar
```

### Secuencia Promocional de 3 Emails

**Email 1: Anuncio (2-3 semanas antes)**

```
Asunto: estás invitado — meetup de content creators el 18 de abril

Hola [NOMBRE],

Estoy organizando una networking night para content creators y solopreneurs
en Portland el 18 de abril a las 6:00 PM.

El objetivo: conectarte con 3+ personas que puedan ayudar tu próximo trimestre
a ser mejor que el último.

- Rondas de networking estructurado (sin merodeamiento incómodo)
- Una charla de 15 minutos sobre 3 modelos de colaboración que realmente funcionan
- Appetizers ligeros y bebidas en The Hive Coworking

40 lugares. Gratuito para asistir. Reserva tu lugar: [ENLACE DE REGISTRO]

Nos vemos el 18,
Jamie

P.S. El evento del trimestre pasado se lleno 10 días antes.
```

**Email 2: Social Proof (1 semana antes)** — Comparte números de registro, destaca el mix de asistentes ya inscritos (roles e industrias), reafirma logística y enlace de registro.

**Email 3: Última Oportunidad (día antes o mañana del evento)** — Lugares restantes, logística rápida (dirección, estacionamiento, hora), recordatorio breve del formato, CTA final.

### Posts en Redes Sociales

Escribe un post nativo para cada canal. LinkedIn: detalle profesional con hashtags al final. Instagram: hook en primera línea, beneficios concisos, CTA a enlace en bio. X/Twitter: punchy, menos de 280 caracteres por tweet, enlace de registro directo.

```
Ejemplo LinkedIn:
Estoy organizando una networking night gratuita para content creators en Portland el 18 de abril.

40 creators. Networking estructurado. Una breve charla sobre modelos de
colaboración que generan ingresos. Comida y bebidas.

El evento del trimestre pasado conectó a un podcaster con un newsletter writer
que ahora se promocionan mutuamente semanalmente. Ese es el resultado que estoy diseñando.

18 de abril | 6 PM | Gratuito | 40 lugares | Enlace en comentarios.

#ContentCreators #PortlandNetworking #Solopreneur
```

**PUNTO DE CONTROL:** Presenta todos los materiales promocionales. No continúes a la Fase 4 hasta que el usuario apruebe.

---

## Fase 4: Execute

Finaliza materiales del día del evento: lista de verificación del día del evento, run-of-show finalizado, mensaje de bienvenida a asistentes y plan de backup técnico.

### Mensaje de Bienvenida a Asistentes (24 horas antes)

```
Asunto: nos vemos mañana — aquí está todo lo que necesitas

Hola [NOMBRE],

El Kickoff de Content Creator es mañana a las 6 PM.

DÓNDE: The Hive Coworking, 1234 SE Division St, Portland OR 97202
CUÁNDO: Puertas a las 6:00 PM, programa a las 6:15 PM
ESTACIONAMIENTO: Estacionamiento gratuito en calle después de las 6 PM
LLEVA: Business cards o teléfono con LinkedIn/Instagram listo

Consejo: Piensa en una cosa en la que necesites ayuda y una cosa que
puedas ofrecer. Eso es tu intro para el icebreaker.

Nos vemos allá,
Jamie
```

### Plan de Backup Técnico

Aborda al menos estos escenarios:

- **El micrófono falla:** Proyecta tu voz desde el centro de la sala; pide al venue un micrófono de backup
- **El proyector falla:** Entrega la charla sin slides; anuncia la URL de encuesta verbalmente
- **WiFi falla:** Usa hotspot móvil; cambia a lista de check-in impresa; recopila emails en papel
- **Catering no aparece:** Envía voluntario para refrigerios básicos usando fondo de contingencia
- **Speaker cancela día del evento:** Extiende rondas de networking; anfitrión entrega charla informal más corta

---

## Fase 5: Follow-Up

### Email de Agradecimiento (Dentro de 24 Horas)

```
Asunto: gracias por presentarte anoche

Hola [NOMBRE],

Gracias por ser parte del Kickoff de Content Creator.

3 cosas que hacer esta semana:
1. Da seguimiento a tus nuevas conexiones — envía un rápido mensaje "fue genial conocerte"
   a las 2-3 personas con las que conectaste
2. Etiquétanos con #ContentCreatorKickoff y compartiré los mejores posts
3. Completa la encuesta de feedback de 2 minutos: [ENLACE ENCUESTA]

Ya estoy planificando el evento de Q3. Responde "Estoy dentro" para acceso prioritario.

Jamie

P.S. Fotos de anoche: [ENLACE ÁLBUM FOTOS]
```

### Encuesta de Feedback (3-5 Preguntas)

1. Calificación general (1-5 estrellas)
2. Parte más valiosa (networking estructurado / charla destacada / networking abierto / otro)
3. ¿Hiciste al menos una conexión significativa? (Sí / No)
4. ¿Qué mejorarías? (texto abierto)
5. ¿Asistirías de nuevo? (Definitivamente / Probablemente / Poco probable)

### Contenido de Resumen

- **Esquema de blog post:** Por qué lo organizamos, cómo funcionó el formato, aprendizajes clave de la charla, resultados y highlights de feedback, anuncio del próximo evento
- **Post de resumen en redes:** Estadística de asistencia, 2-3 resultados específicos (colaboraciones formadas, conexiones establecidas), invitación al próximo evento

### Nutrición de Leads (Dentro de 72 Horas)

Email personalizado a leads cálidos recopilados en el evento. Referencia un detalle específico de la conversación. Incluye: invitación al próximo evento, opt-in de newsletter, enlace para chat 1-a-1.

---

## Ejemplo 1: Workshop Virtual para un Coach

**Solicitud del usuario:** "Estoy ejecutando 'Build Your Content System in 90 Minutes' en Zoom. 50 asistentes, gratuito, necesito el plan completo."

**Ejecución:**

1. **Brief:** Workshop, virtual, 50 asistentes, Zoom, $0, objetivo: educación + lead gen.
2. **Plan:** Lista de verificación adaptada para virtual (sin tareas de venue/catering). Run-of-show: 10 min bienvenida, 25 min bloque de enseñanza 1, 25 min bloque de enseñanza 2, 15 min ejercicio práctico, 10 min Q&A, 5 min cierre. Tech backup: enlace de Zoom backup, dial-in por teléfono.
3. **Promote:** Página de registro para content creators. 3 emails promocionales. Posts en redes para LinkedIn, Instagram, X.
4. **Execute:** Lista de verificación día del evento virtual (tech check 30 min antes, slides cargados, moderador de chat asignado). Mensaje de bienvenida con enlace de Zoom.
5. **Follow-up:** Agradecimiento con enlace de replay, encuesta de feedback, post de resumen en redes, email de nutrición de leads.

**Resultado:** Run-of-show, 8 emails, página de registro, 3 posts en redes, presupuesto cero.

---

## Ejemplo 2: Meetup de Networking In-Person

**Solicitud del usuario:** "Ejecuto una comunidad de entrepreneurs local. 30 personas, venue alquilado, presupuesto de $500."

**Ejecución:**

1. **Brief:** Networking event, in-person, 30 asistentes, $500, objetivo: comunidad + leads cálidos.
2. **Plan:** Lista de verificación completa in-person. Run-of-show para 2 horas: llegada, icebreaker, dos rondas de networking estructurado, descanso, cierre. Rastreador de presupuesto: venue $150, catering $180, materiales $35, contingencia $65.
3. **Promote:** Registro en Eventbrite. 3 emails a lista de comunidad. Posts en LinkedIn e Instagram.
4. **Execute:** Lista de verificación día del evento con setup de venue, desk de registro, AV, briefing de voluntarios. Mensaje de bienvenida con detalles de estacionamiento. Tech backup para contingencias in-person.
5. **Follow-up:** Agradecimiento con fotos, encuesta de feedback, post de resumen, nutrición de leads personalizada a 10 contactos principales.

**Resultado:** Run-of-show, rastreador de presupuesto, 7 emails, página de registro, 2 posts en redes, $500 asignados.

---

## Anti-Patterns

- **NO planifiques sin un objetivo medible.** "Construir comunidad" no es medible. "Recopilar 15 leads cálidos" sí lo es. Sin objetivo, no hay forma de evaluar éxito.
- **NO saltes el plan de backup técnico para eventos virtuales.** Cada evento virtual necesita un enlace de reunión backup, dial-in por teléfono y un plan para fallo de internet del anfitrión.
- **NO envíes seguimientos más de 48 horas después del evento.** Agradecimiento dentro de 24 horas. Encuesta dentro de 48. Los leads se enfrían después de 72.
- **NO crees agendas sin tiempo de amortiguación.** Mínimo 5 minutos de buffer entre segmentos. Sin buffer garantiza que estarás retrasado en el segmento tres.
- **NO sobre-programes eventos de networking.** Al menos 30% del tiempo total debe ser no estructurado. La sobre-programación mata conversaciones orgánicas.
- **NO saltes la lista de verificación del día del evento.** La memoria falla bajo presión. La lista de verificación previene name tags olvidados, micrófonos sin probar y señalización faltante.
- **NO copies-pegues el mismo post promocional en plataformas.** LinkedIn es profesional. Instagram es conciso y visual. X es punchy. Cada uno debe sentirse nativo.
- **NO saltes logística en la página de registro.** Cada página necesita: fecha, hora con zona horaria, dirección o enlace, instrucciones de estacionamiento o login. La logística faltante crea inundaciones de inbox.
- **NO planifiques eventos in-person sin una caminata de venue.** Los planos mienten. Visita el espacio. Confirma AV, capacidad, layout y acceso a baños.
- **NO ignores no-shows.** 30-50% de registrados no asistirán. Envíales un resumen e invítalos al próximo evento. Siguen siendo leads cálidos.

---

## Recuperación

- **El usuario no puede definir el objetivo:** Pregunta "¿Qué quieres que sea verdad 1 semana después de este evento que no es verdad hoy?" Traduce su respuesta en un resultado medible.
- **Presupuesto muy pequeño:** Reduce escala. Elimina catering (sugiere BYOB). Cambia a venue gratuito (biblioteca, oficina de partner). Usa name tags digitales. Un evento de $0 con 15 personas puede golpear el objetivo.
- **El venue falla en el último momento:** (1) Encuentra espacio de coworking backup, (2) pide a un asistente o partner que anfitrione, (3) pivota a virtual como último recurso. Email a registrados con detalles actualizados inmediatamente.
- **El speaker cancela día del evento:** Extiende rondas de networking 15 minutos. El anfitrión entrega charla informal más corta. Anuncia en bienvenida sin sobre-disculparte.
- **La integración de Notion falla:** Entrega lista de verificación, run-of-show y rastreador de presupuesto como archivos markdown locales con formato claro para paste manual.
- **Registros bajos 1 semana antes:** (1) Re-comparte enlace de registro en todos los canales, (2) reescribe copia promocional con beneficios más afilados, (3) pregunta a 3-5 asistentes objetivo qué los está deteniendo. Si sigue bajo, encoge el evento en lugar de cancelar.
- **El evento se extiende en tiempo:** Corta del siguiente descanso o networking abierto, nunca de observaciones de cierre. El cierre recopila sign-ups de encuesta y anuncia el próximo evento.

---

## Lista de Verificación Pre-Entrega

```
  [ ] Brief del evento confirmado antes de que planificación comenzara
  [ ] Lista de verificación cubre todas las 5 fases de cronograma
  [ ] Run-of-show tiene timestamps con dueños para cada segmento
  [ ] Tiempo de amortiguación (mín 5 min) entre segmentos principales
  [ ] Página de registro incluye headline, beneficios, bio del anfitrión, logística, CTA
  [ ] 3 emails promocionales con fechas de envío apropiadas
  [ ] Posts en redes son nativos de plataforma
  [ ] Plan de backup técnico cubre al menos 3 escenarios de fallo
  [ ] Follow-up incluye agradecimiento, encuesta y nutrición de leads
  [ ] Rastreador de presupuesto incluye contingencia (si presupuesto proporcionado)
  [ ] Sin texto placeholder — todos los ejemplos usan contenido real del brief
  [ ] Todos los tiempos incluyen zona horaria
```
