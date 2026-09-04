---
name: run-of-show-evento
description: "Crea documentos de run-of-show detallados con cronogramas minuto por minuto, dueños de segmentos y notas técnicas."
allowed-tools: Read Write Glob
metadata:
  author: Imperio Digital
  version: "1.0"
---

# Run-of-Show de Evento

## Cuándo Usar Este Skill

Usa este skill cuando necesites:
- Crear un documento de run-of-show detallado para el día del evento
- Especificar cada segmento con propietarios, tiempos y notas técnicas
- Documenta cambios de escena, introducción de speakers y transiciones
- Construir un plan de backup para problemas técnicos

**NO** uses esto como el documento de planificación maestra. Esto es el documento ejecutable que controla cada minuto.

---

## Principio Fundamental

UN RUN-OF-SHOW ES UN CONTRATO ENTRE EL ANFITRIÓN, EL EQUIPO Y LA AUDIENCIA — SI NO ESTÁ ESCRITO, TODOS ADIVINAN, Y EL EVENTO SE SIENTE DESORGANIZADO.

---

## Estructura de Documento

### Encabezado

```
== RUN-OF-SHOW ==
[Nombre del Evento]
[Fecha] | [Hora] | [Venue]
Última actualización: [Fecha]
Preparado por: [Tu nombre]
```

### Sección Pre-Evento

```
## PRE-EVENTO SETUP (incluye todas las tareas antes de que comiencen los asistentes)

[Start Time] - [End Time] | [Duration]
[Task] | Owner: [Name] | Notes: [Technical notes, dependencies]

Ejemplo:
2:00 PM - 2:15 PM | 15 min
Llegar, confirmar layout | Owner: Jamie | Notes: Walk the space, confirm AV location, check WiFi strength
```

### Sección del Evento en Vivo

```
## EVENTO EN VIVO

[Start Time] - [End Time] | [Duration]
[Segment Name] | Owner: [Name]
[Technical cues] | [Transitions]
[Notes]

Ejemplo:
6:00 PM - 6:15 PM | 15 min
Welcome + Housekeeping | Owner: Jamie
Audio: Fade in house music at 5:55 PM. Kill at 6:00 AM when Jamie walks on.
Slides: "Welcome" slide on screen. Logo in corner.
Notes: Cover: WiFi SSID/password (display on screen), bathroom locations, hashtag #EventName, format of the night (4 segments, 20 min breaks).
```

### Sección Post-Evento

```
## POST-EVENTO

[Start Time] - [End Time]
[Task] | Owner: [Name] | Notes:

Ejemplo:
8:30 PM - 8:45 PM
Breakdown and thank you | Owner: Alex | Notes: Collect name badges, strike signage, brief volunteers
```

---

## Ejemplo Completo (Virtual Event)

```
== RUN-OF-SHOW ==
Content Creator Kickoff Summit 2026
April 14-15, 2026 | Zoom Webinar
Last updated: April 1, 2026
Prepared by: Sarah Chen

== PRE-EVENT (April 14, 8:30 AM PT) ==

8:30 AM - 8:45 AM | 15 min
Tech check final | Owner: Miguel (AV Tech)
- Test speakers' microphones (James + Alex)
- Test screen sharing (James from main computer + backup laptop)
- Test chat moderation tools
- Play welcome video (60 sec) to verify playback
- Verify recording is enabled in Zoom settings
Notes: James should be in Zoom 20 min early to test his setup.

== DAY 1: CONTENT CREATOR KICKOFF ==

9:00 AM - 9:05 AM | 5 min
Welcome + tech check | Owner: James
Audio: Background music (from YouTube playlist) fades at 8:59 AM. Stop at 9:00 AM when James appears.
Slides: Title slide displayed. Chat moderator (Clara) is live and monitoring.
Notes: James says: "Welcome to Content Creator Kickoff. We have 1,200+ people in the room from 45+ countries. Stick around to the end — we have prizes."

9:05 AM - 9:50 AM | 45 min
Keynote: "The 3-Part Content System That Made 50+ Creators 6-Figures" | Owner: James (Speaker)
Audio: Ensure James's microphone is unmuted. Chat is muted (no questions yet).
Slides: Pre-loaded deck. Advance slides on James's command. NO auto-advance.
Notes: James will take 40 min, leave 5 min for questions in chat. Clara will screen questions and James will read 3-4 best ones.

9:50 AM - 10:00 AM | 10 min
Questions + Transition | Owner: Clara (Chat Moderator), James (Answering)
Notes: James answers top 3-4 questions from chat. At 9:58, I say "We're moving to breakout sessions. Click the link in chat to choose your track."

10:00 AM - 10:00 AM | 0 min (Breakout rooms open)
Attendees select track and join breakout | Owner: Miguel (Tech)
Notes: Breakout rooms open simultaneously. Facilitators (Alex, Jordan) are already in rooms waiting.

10:00 AM - 10:45 AM | 45 min
Breakout Session 1A: "Platform Strategy" | Owner: Alex (Facilitator)
Notes: 200 people. Alex does 35 min talk, 10 min Q&A. Recording is on. Share link to Google Doc for questions.

10:00 AM - 10:45 AM | 45 min
Breakout Session 1B: "Content Operations" | Owner: Jordan (Facilitator)
Notes: 300 people. Jordan does 35 min talk, 10 min Q&A. Recording is on.

[... continue for every segment ...]

8:30 PM - 8:35 PM | 5 min
Thank you + next steps | Owner: James
Notes: James plugs the community (Slack invite link in chat), next event (May 15), optional office hours tomorrow.

8:35 PM
Event ends | Recording stops and uploads to folder

== POST-EVENT ==

8:35 PM - 8:50 PM | 15 min
Debrief with facilitators | Owner: Sarah (Producer)
Notes: Quick check: Any major issues? Any attendees who need follow-up? Capture top feedback.

9:00 PM
Send thank you email to all 1,200 attendees | Owner: Sarah
Subject: "Thank you for the Kickoff"
Includes: Replay link (will be live in 24 hours), community invite, next event info, feedback survey link

== TECHNICAL BACKUP PLAN ==

IF Zoom goes down: Switch to YouTube Live streaming. Announce in email that viewers should go to YouTube.
IF WiFi fails: Use mobile hotspot. Have backup laptop tethered.
IF speaker fails to show: James will facilitate live Q&A with attendees using chat. No keynote, move directly to breakouts.
IF recording fails: No replay available, but email attendees summary slides + video clips from facilitators' recordings.
```

---

## Anti-Patrones

- **Sin propietarios específicos** — "someone" será nadie.
- **Suponer que el equipo sabe** — escribe CADA paso. No asumas nada.
- **Sin plan de backup** — "esperar y rezar" no es un plan.
- **Escritura ambigua** — "más tarde" vs. "3:15 PM". Sé específico.

---

## Checklist Pre-Lanzamiento

```
- [ ] Cada segmento tiene un propietario específico
- [ ] Todos los tiempos son claros (no "después del almuerzo")
- [ ] Notas técnicas cubren audio, video, slides, chat
- [ ] Se incluyen transiciones entre segmentos
- [ ] Plan de backup cubre 3-5 escenarios de fallo
- [ ] Todo el equipo ha revisado y confirmado
```
