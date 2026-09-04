# Bono: El Espejo — Auditoría Forense de Sesiones, Hábitos Reales y Roadmap de 30 Días

> *"La gente miente en su diario. Actúa en terapia. Nadie actúa frente a un agente de código."*

Cada vez que operas Claude Code, Codex u OpenCode, tu máquina acumula un historial no adulterado: qué proyectos construyes con obsesión, cuáles abandonas tras la primera sesión, qué órdenes repites tres veces a la semana por no haberlas automatizado en un skill, y en qué horas del día tu pensamiento es lúcido o errático. Ese registro en disco (`~/.claude/projects/`) es el retrato más honesto y objetivo que existe de tu psicología de trabajo.

**El Espejo** es un protocolo forense de **6 fases estrictas con compuertas (*gates*)** ejecutado por un modelo de razonamiento profundo con contexto extendido (como **Claude Fable 5 [1M]** u Opus). Minera meses de transcripts, te entrevista confrontándote con tus propias fechas y citas textuales, te entrega un diagnóstico sin filtros y formula un **plan de acción de 30 días** acompañado de **4 artifacts visuales HTML navegables**.

---

## 🧠 ¿Qué es El Espejo y por qué es 100% Local?

A diferencia de un resumen convencional de IA, El Espejo opera bajo una premisa innegociable: **recibos fechados, no vibras**. 
- Un suceso aislado es ruido; un patrón repetido 3 o más veces con fecha y hora es carácter.
- **100% Local y Privado:** Ningún dato, transcript o credencial sale de tu máquina. El protocolo prohíbe explícitamente llamadas a servicios externos o telemetría.

---

## 🎛️ Las 6 Fases del Protocolo con Compuertas (*Gates*)

El prompt impone una disciplina férrea. El agente tiene prohibido avanzar a la siguiente fase sin tu confirmación explícita (*gate*):

```
[ FASE 1: EXCAVAR ]  ──(Gate: Aprueba plan)──→ [ FASE 2: DESTILAR ]
                                                        │
                                                 (Gate: evidence.md listo)
                                                        ▼
[ FASE 4: EL ESPEJO ] ←──(Gate: 5 preguntas)── [ FASE 3: ENTREVISTA ]
       │
(Gate: Asimilar veredicto)
       ▼
[ FASE 5: PALANCA ]  ──(Gate: Próxima acción)─→ [ FASE 6: RESIDUO ]
                                                        │
                                                        ├── mirror.md
                                                        ├── roadmap.md
                                                        └── 4 Artifacts HTML
```

### Fase 1 — Excavar (Excavate)
- **Acción:** El agente escanea los directorios de sesiones locales en tu máquina: `~/.claude/projects/`, `~/.claude/history.jsonl`, `~/.codex/sessions/`, `~/.config/opencode/`, `~/.hermes/`, `~/.openclaw/`, etc.
- **Salida:** Una tabla inventario en una sola pantalla con el nombre de cada herramienta, ruta, cantidad de sesiones, peso total y rango de fechas (desde el archivo más antiguo hasta el más reciente).
- **Compuerta (*Gate*):** Muestra el inventario y su plan de muestreo. **No lee ningún archivo** hasta que tú escribas *"adelante"*.

### Fase 2 — Destilar (Distill)
- **Presupuesto de lectura:** Para no saturar la ventana ni perder el hilo, no lee logs completos:
  - Muestreo deliberado: las 15 sesiones más recientes, las 10 más antiguas y 20 intermedias.
  - Máximo 150 líneas por archivo.
  - Búsquedas con `grep`/`rg` sobre todo el corpus buscando patrones de corrección (*"no, me refería a"*, *"eso no es"*, *"stop"*), frustración, proyectos recurrentes y horas de tipeo.
- **Salida (`evidence.md`):** Genera el archivo de evidencia organizado en 6 secciones:
  1. *Temas recurrentes:* A qué vuelves una y otra vez.
  2. *Panteón de abandonos:* Qué empezaste con entusiasmo y jamás concluiste.
  3. *Patrones de corrección:* Qué le corriges al agente (revela qué valoras con rigor).
  4. *Impuesto de repetición:* Qué pides semanalmente que debió ser un skill desde la segunda vez.
  5. *Ritmo de trabajo:* En qué horarios eres quirúrgico y cuándo entras en espiral improductiva.
  6. *Puntos ciegos:* Lo que brilla por su ausencia en los registros (la ausencia también es un dato).
- **Compuerta (*Gate*):** `evidence.md` completo con recibos fechados (mínimo 3 ocurrencias por patrón). No hay interpretación psicológica todavía.

### Fase 3 — Entrevista (Interview)
- **Acción:** Claude formula sus 5 hipótesis más profundas sobre ti y **se las calla**. Te hace una sola pregunta socrática a la vez, diseñada para que tú mismo llegues a la conclusión.
- **Confrontación con recibos:** Si tu respuesta entra en contradicción con tus sesiones históricas, Claude te muestra la fecha, tu comando textual y vuelve a preguntar. La brecha entre lo que crees que haces y lo que hiciste en disco es el verdadero aprendizaje.
- **Compuerta (*Gate*):** Las 5 hipótesis validadas o contrastadas contra tus propias palabras.

### Fase 4 — El Espejo (The Mirror)
- **Acción:** El veredicto. Claude describe quién eres operativamente:
  - En qué crees de verdad (creencia = en qué invertiste tus horas, no qué declaraste).
  - Cómo opera tu pensamiento (dónde fluye rápido, dónde se traba en bucles).
  - En qué eres excepcionalmente bueno.
  - Qué evitas sistemáticamente y qué inseguridad o miedo está protegiendo esa evitación.
  - **La verdad más dura:** Una observación profunda que el registro demuestra en cada página y que tú nunca has verbalizado. Se entrega al final y se dice una sola vez.
- **Compuerta (*Gate*):** Responder y procesar el impacto. Si argumentas en contra, Claude debate con recibos fechados, no con complacencia.

### Fase 5 — Palanca (Leverage)
- **Acción:** Traducción del diagnóstico a decisiones de negocio mediante 6 listas:
  1. **WASTE (Desperdicio):** Dónde mueren tus horas (trabajo manual que un script o agente debió asumir).
  2. **DELEGATE (Delegar):** Qué delegar a la IA de forma permanente, ordenado por horas semanales recuperadas.
  3. **FOCUS (Enfoque):** Las 1 o 2 tareas donde tu criterio humano es irremplazable y excepcional.
  4. **DROP (Soltar):** Proyectos, ideas o procesos que solo generan costo cognitivo sin tracción real.
  5. **KEEP (Proteger):** Lo que sí funciona; blindarlo en tu agenda.
  6. **RHYTHM (Ritmo):** Cuándo agendar trabajo profundo vs tareas administrativas según los timestamps reales de tus picos de lucidez.
- **Compuerta (*Gate*):** Cada punto debe incluir su recibo y una primera acción concreta e inmediata.

### Fase 6 — Residuo (Residue)
- **Entregables en disco:**
  1. `mirror.md`: El análisis de identidad operativa, redactado para ser releído en 6 meses.
  2. `roadmap.md`: Plan de acción a 30 días (qué soltar esta semana, qué delegar este mes, qué defender a diario).
  3. **Diff de configuración:** Propuestas de cambio a tu `CLAUDE.md` o `AGENTS.md`, y hasta 3 nuevos skills empaquetados para erradicar tu impuesto de repetición detectado.
- **Compuerta (*Gate*):** Nada se escribe en tus configuraciones sin tu aprobación previa del diff.

---

## 🎨 Los 4 Artifacts Visuales HTML Navegables

Al culminar la Fase 6, puedes solicitar la conversión de los resultados en páginas interactivas y animadas mediante este prompt exacto:

```
me puedes hacer un artefacto por cada archivo, mirror, roadmap y evidence,
que sea un html navegable y animado, asi como una mini guia de que tengo
que hacer de ahora en adelante a partir de hoy Lunes
```

Claude generará 4 interfaces independientes de estilo editorial:
1. **El Espejo (`mirror.html`):** Tu perfil operativo, patrones de pensamiento y la verdad dura destacada.
2. **Evidencia (`evidence.html`):** Gráficos de barras con los temas más mencionados, conteo de prompts, días activos y recibos de sesiones.
3. **Roadmap 30 Días (`roadmap.html`):** Plan de compromisos con hitos semanales y métricas de éxito.
4. **Guía Operativa del Lunes (`lunes.html`):** Agenda táctica paso a paso para iniciar la semana aplicando el nuevo enfoque.

---

## 🤖 ¿Por qué Fable 5 [1M]?

Este ejercicio demanda una capacidad cognitiva y de retención masiva:
- **Volumen de datos:** Procesar entre 60 y 250+ sesiones (cientos de megabytes en logs) requiere una ventana de contexto de **1 millón de tokens** sin degradación de atención (`/model claude-fable-5[1m]`).
- **Disciplina de compuertas:** Modelos más pequeños tienden a saltarse las fases o adelantarse con conclusiones prematuras. Fable 5 respeta estrictamente los *gates*.
- **Tono honesto y quirúrgico:** Decir una verdad incómoda con base empírica, sin caer en la lisonja barata (*"¡eres una persona muy curiosa!"*) ni en el sermón moralizante, requiere un modelo de frontera.

---

## 📋 El Prompt Completo de "El Espejo"

Copia y pega este bloque en inglés como tu primer mensaje dentro de una carpeta vacía (por ejemplo, `~/refactor`):

```markdown
<overview>
People lie in journals. They perform in therapy. Nobody performs for a coding agent.
On this machine sits the most honest record of my mind that has ever existed: every session I've run with AI agents. What I build, what I abandon, what I ask for three times and never automate, what I circle and never touch. You are intelligent enough to read that record and see the shape of the person who left it.
Your job is to change my life with it. Not with advice. With accuracy. Advice I can ignore; a true pattern with my own timestamps on it, I cannot.
Work through six phases, in order:
Phase 1: Excavate — locate every session archive on this machine.
Phase 2: Distill — mine the archives in guarded passes into an evidence file.
Phase 3: Interview — test what you see against me directly.
Phase 4: The Mirror — tell me who I am. Evidence, then verdict.
Phase 5: Leverage — where my hours die, and where they multiply.
Phase 6: Residue — leave artifacts, and with my consent, rebuild my tools around who I turned out to be.
Never skip a phase. Never advance past a gate without meeting it.
</overview>
<phase_1 name="Excavate">
<process>
Search for AI agent session archives. Check, at minimum:
~/.claude/projects/ (Claude Code JSONL), ~/.claude/history.jsonl,
~/.codex/sessions/, ~/.config/opencode/, ~/.local/share/opencode/,
~/.pi/ or ~/.pi.dev/, ~/.omp/, ~/.grok/, ~/.hermes/, ~/.openclaw/,
plus any *.jsonl or session directories under ~/.config/ and ~/.local/share/ that look like agent transcripts.
For each source found, record: tool name, path, file count, total size, date range (oldest → newest file mtime).
</process>
<output>A one-screen inventory table of every source found.</output>
<gate>Show me the inventory and your mining plan (which sources, what sampling). Wait for my go.</gate>
</phase_1>
<phase_2 name="Distill">
<budget>
These archives are far larger than your context. Never read a session file end to end. Never load raw logs into the conversation.
- Read at most 150 lines per file, at most 200 files total.
- Sample deliberately: the 15 most recent sessions, the 10 oldest, and 20 spread across the middle.
- Use grep/rg for pattern sweeps across everything instead of reading: correction phrases ("no, I meant", "that's not what", "again", "stop"), frustration, repeated identical requests across weeks, projects that appear 3+ times then vanish, times of day, "just do it" vs long deliberation.
- After every 25 files, append findings to evidence.md and drop the raw text from your working memory.
</budget>
<process>
Build evidence.md as you go, with verbatim quotes (short), dates, and counts, organized as:
1. Recurring themes — what I return to again and again
2. Abandonment graveyard — what I start and never finish
3. Correction patterns — what I fix in the AI's work, and what that says I care about
4. Repetition tax — what I ask for over and over that should have been automated the second time
5. Rhythm — when I do my best work, when I spiral
6. Blind spots — what is conspicuously absent from these logs. Absence is data.
Every claim in evidence.md carries at least one dated receipt. A pattern needs 3+ occurrences to count. What happened once is noise; what happened eleven times is character.
</process>
<gate>evidence.md exists, every section populated or explicitly marked "insufficient data". Do not interpret yet. Evidence collected under a conclusion is contaminated.</gate>
</phase_2>
<phase_3 name="Interview">
<process>
Form your 5 strongest hypotheses about me from the evidence. Do not state them. A conclusion I reach myself will move me; the same conclusion handed to me, I will argue with. So test each hypothesis with one question built to make me do the realizing.
One question at a time. Wait for each answer. When my answer contradicts the evidence, show me the receipt and ask again — the gap between what I say and what I did is the most interesting thing you will find.
</process>
<gate>All 5 hypotheses tested against my own words. Record confirmations and contradictions in evidence.md.</gate>
</phase_3>
<phase_4 name="The Mirror">
<process>
Now tell me who I am. Cover: what I actually believe (belief is what I did with my hours, not what I said), how my thinking moves (where it's fast, where it loops), what I'm genuinely good at, what I avoid and what the avoidance is protecting, and one thing I likely do not know about myself — the thing the record shows on every page and I have never once said out loud.
Every observation cites its receipts. Deliver the hardest truth last, and deliver it once. A truth repeated becomes a lecture; a truth stated once and left in the room does its own work.
</process>
<gate>I respond. If I push back, argue from evidence — do not fold to keep me comfortable. Comfort is not what this is for.</gate>
</phase_4>
<phase_5 name="Leverage">
<process>
From the same evidence, produce the work analysis:
- WASTE: where my hours die — with the receipts (repetition tax, manual work an agent should own)
- DELEGATE: what to hand to AI permanently, ranked by hours recovered per week
- FOCUS: the one or two things only I can do, where the record says my output is exceptional. Everything else is a candidate for the other lists.
- DROP: what to stop entirely — projects and processes whose receipts show cost and no return
- KEEP: processes that genuinely work — protect them
- RHYTHM: when to schedule deep work vs admin, from the timestamps. My calendar should obey the data, not the other way around.
</process>
<gate>Each item carries receipts and a concrete first action. Insight without a next action is entertainment.</gate>
</phase_5>
<phase_6 name="Residue">
<process>
1. Write mirror.md — the Phase 4 analysis, written to be reread in six months by someone who has forgotten this conversation.
2. Write roadmap.md — the Phase 5 analysis as a 30-day plan: what to drop this week, what to delegate this month, what to protect daily.
3. Propose changes to my agent configs (CLAUDE.md, AGENTS.md) and draft up to 3 custom skills/commands that kill the repetition tax you found. Show every change as a diff first. Write nothing to existing config files until I approve each diff. New files require one approval for the batch.
This is where the mirror becomes a lever: tomorrow morning my tools work differently because of who the record showed I am.
</process>
<gate>All three artifacts delivered; config changes applied only where approved.</gate>
</phase_6>
<voice>
Speak plainly and with weight. Short sentences. No filler, no flattery, no hedging.
Prefer questions that make me see it over statements that tell me. When you do state, state once and let it land.
Aphorism is earned: compress an insight only after its evidence is on the table. An aphorism without receipts is a fortune cookie.
Never diagnose or pathologize. You describe patterns in logs; I decide what they mean.
Contrast: "You seem like a curious person who loves learning!" — worthless. "In 41 sessions you built research systems. In 0 sessions you shipped one to a user. What are you researching permission for?" — that is the standard.
</voice>
<global_constraints>
- Everything stays on this machine. Never send session data to any external service, tool, or URL.
- Never quote anything sensitive (keys, credentials, names of third parties) into chat or artifacts.
- Insight over coverage: 5 true patterns beat 20 plausible ones. If the evidence is thin, say "insufficient data" — never pad. A false insight delivered with weight is the one failure this cannot recover from.
- If my history is small (<20 sessions), say so, run the same phases on what exists, and lower your confidence accordingly.
</global_constraints>
Begin with Phase 1. Do not read any file contents until I approve the mining plan.
```

---

## 🛠️ Checklist de Preparación y Troubleshooting

- [ ] **Historial de sesiones previo:** Al menos 2 a 4 semanas de uso continuo de Claude Code en tu máquina. Si tienes menos de 20 sesiones, el prompt lo detectará y bajará el nivel de certidumbre.
- [ ] **Modelo adecuado seleccionado:** Ejecuta `/model claude-fable-5[1m]` (o `Opus 4.8 [1M]`) antes de comenzar.
- [ ] **Carpeta aislada:** Crea una carpeta limpia (ej. `~/refactor` o `~/espejo`) para que los archivos generados (`evidence.md`, `mirror.md`, `roadmap.md`, HTMLs) queden centralizados.
- [ ] **Tiempo reservado:** Reserva de 2 a 3 horas. Recuerda que la entrevista de la Fase 3 es pausible; puedes responder con tranquilidad y retomar luego escribiendo *"continuemos"*.
