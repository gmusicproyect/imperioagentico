# SKILL: Auditoría Forense de Sesiones con El Espejo

> Guarda este archivo en `/skills/ejecutar-el-espejo/SKILL.md`
> Referencia en tu CLAUDE.md: `- /skills/ejecutar-el-espejo/SKILL.md → para auditar historial de sesiones locales, detectar patrones de trabajo y abandonos, y generar roadmap de 30 días con artefactos visuales`

---

## Cuándo usar este skill

Cuando el usuario requiera auditar de forma honesta y cuantitativa su historial acumulado de sesiones de Claude Code, Codex u otros arneses de IA en su máquina local (`~/.claude/projects/`), para identificar patrones recurrentes de trabajo, proyectos abandonados, tareas repetitivas candidatas a convertirse en skills, picos de productividad horaria y derivar un plan de acción de 30 días con interfaces visuales interactivas.

---

## Prerequisitos

- [ ] Claude Code CLI instalado con historial de sesiones previas (mínimo 2–4 semanas de uso)
- [ ] Carpeta de trabajo aislada y vacía (ej. `~/refactor` o `~/espejo`)
- [ ] Modelo de razonamiento profundo con contexto extendido de 1M tokens activado (`/model claude-fable-5[1m]` u `opus`)
- [ ] Disponibilidad para una sesión interactiva de reflexión (2 a 3 horas, pausible)

---

## Pasos

### Paso 1 — Preparación del entorno y selección de modelo

1. Crear y acceder a una carpeta limpia dedicada exclusivamente al ejercicio:
   ```bash
   mkdir -p ~/refactor && cd ~/refactor
   ```
2. Iniciar Claude Code y verificar que el modelo seleccionado soporte 1M de tokens:
   ```
   /model claude-fable-5[1m]
   ```
   *(Si Fable 5 no está disponible, seleccionar `Opus 4.8 [1M]`).*

### Paso 2 — Carga del prompt maestro y Fase 1 (Excavación)

1. Pegar el prompt maestro de "El Espejo" en inglés (ver `bonos/el-espejo/README.md`) sin modificaciones.
2. Esperar a que el agente complete la búsqueda de directorios (`~/.claude/projects/`, `~/.codex/sessions/`, etc.) y renderice la tabla de inventario en pantalla.
3. **Compuerta 1 (*Gate*):** Revisar la cantidad de sesiones y el plan de muestreo propuesto. Escribir *"adelante"* o *"go"* para autorizar la lectura.

### Paso 3 — Supervisión de la Fase 2 (Destilación y `evidence.md`)

1. El agente ejecutará un muestreo controlado (máximo 150 líneas por archivo, barridos con `grep`/`rg` y muestreo de sesiones recientes, viejas e intermedias).
2. Verificar que se construya el archivo `evidence.md` con sus 6 secciones obligatorias:
   - Temas recurrentes
   - Panteón de abandonos
   - Patrones de corrección
   - Impuesto de repetición
   - Ritmo de trabajo
   - Puntos ciegos
3. **Compuerta 2 (*Gate*):** Comprobar que cada patrón contenga al menos 3 ocurrencias con fechas verificables.

### Paso 4 — Responder a la Fase 3 (Entrevista socrática)

1. El agente formulará 5 preguntas individuales, una a la vez, derivadas de sus hipótesis no reveladas.
2. Responder con total transparencia en español.
3. Si el agente detecta discrepancias entre lo que afirmas y lo registrado en tus logs, te mostrará el recibo fechado. Reflexionar sobre la brecha antes de responder la siguiente pregunta.

### Paso 5 — Veredicto de la Fase 4 (El Espejo) y Fase 5 (Palanca)

1. Leer el análisis de identidad operativa de la Fase 4: qué demuestran tus horas invertidas, cómo opera tu pensamiento, qué tareas evitas y la verdad dura final.
2. Revisar la matriz de palanca de la Fase 5:
   - **WASTE:** Horas perdidas en tareas manuales.
   - **DELEGATE:** Tareas a delegar permanentemente a agentes.
   - **FOCUS:** Las 1–2 fortalezas irremplazables del operador.
   - **DROP:** Proyectos a abandonar definitivamente.
   - **KEEP:** Procesos exitosos a blindar.
   - **RHYTHM:** Calibración de horarios de trabajo profundo según tus picos de lucidez.

### Paso 6 — Entrega de artefactos (Fase 6) y generación visual

1. Confirmar la generación de los archivos de cierre en disco:
   - `mirror.md`: Diagnóstico para releer en 6 meses.
   - `roadmap.md`: Plan de acción de 30 días con métricas.
   - Propuestas de diff para `CLAUDE.md`/`AGENTS.md` y hasta 3 nuevos skills.
2. Solicitar los artifacts visuales navegables enviando:
   ```
   me puedes hacer un artefacto por cada archivo, mirror, roadmap y evidence,
   que sea un html navegable y animado, asi como una mini guia de que tengo
   que hacer de ahora en adelante a partir de hoy Lunes
   ```
3. Abrir los 4 archivos HTML resultantes en el navegador local.

---

## Outputs esperados

- Archivo `evidence.md` con inventario de patrones y recibos fechados.
- Archivo `mirror.md` con el perfil operativo honesto del usuario.
- Archivo `roadmap.md` con metas y compromisos a 30 días.
- 4 Artifacts interactivos HTML (`mirror.html`, `evidence.html`, `roadmap.html`, `lunes.html`).
- Diffs de configuración aprobados para optimizar el `CLAUDE.md` del usuario.

---

## Errores comunes

| Error | Causa probable | Solución |
|-------|---------------|---------|
| El agente lee archivos completos y satura contexto | Saltarse el presupuesto de la Fase 2 | Recordarle la regla: *"Máximo 150 líneas por archivo y barridos con grep"* |
| Respuestas condescendientes o halagos vacíos | Usar un modelo pequeño sin disciplina de voz | Asegurar el uso de `claude-fable-5[1m]` u `Opus` |
| El agente concluye antes de la entrevista | Ignorar las compuertas (*gates*) del prompt | Frenar la respuesta y exigir cumplir la compuerta actual |
| Menos de 20 sesiones en el historial | Usuario nuevo en Claude Code | Dejar que el agente active el modo de bajo volumen con nivel de certidumbre ajustado |

---

## Notas adicionales

El Espejo no es un ejercicio de autoayuda; es una auditoría de eficiencia y arquitectura operativa basada en datos de disco no adulterados.

---

*Creado: 2026-09-03*
