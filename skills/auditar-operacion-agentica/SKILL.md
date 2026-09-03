# SKILL: Auditoría de Operación Agéntica y Optimización de ROI

> Guarda este archivo en `/skills/auditar-operacion-agentica/SKILL.md`
> Referencia en tu CLAUDE.md: `- /skills/auditar-operacion-agentica/SKILL.md → para auditar consumo de tokens, calcular ROI real frente a tarifas API, revisar salud de memoria y detectar patrones repetitivos para convertirlos en skills`

---

## Cuándo usar este skill

Cuando el usuario requiera auditar el consumo real de tokens y costos en sus sesiones de Claude Code o agentes locales, cuantificar el retorno de inversión (**ROI**) comparando su suscripción fija ($20 Pro / $200 Max) frente a las tarifas oficiales de API, evaluar la **salud de su memoria** detectando archivos de contexto obsoletos, e identificar flujos repetitivos para empaquetarlos en nuevos skills.

---

## Prerequisitos

- [ ] Claude Code CLI instalado con historial de sesiones registrado localmente
- [ ] Tarifa horaria del operador establecida (para traducir horas ahorradas en dinero)
- [ ] Acceso de **solo lectura** a la carpeta de configuración y transcripts (`~/.claude/projects/` o logs locales)

---

## Pasos

### Paso 1 — Escaneo de transcripts e historial de sesiones (Solo Lectura)

1. Localizar los directorios de transcripts y logs de sesiones activas e históricas:
   - Directorio global de Claude Code: `~/.claude/projects/`
   - Logs de sesiones por proyecto: `.system_generated/logs/` o archivos `transcript.jsonl`
2. Extraer los contadores de tokens por interacción:
   - `input_tokens` (tokens de entrada)
   - `output_tokens` (tokens de salida generados)
   - `cache_read_input_tokens` y `cache_creation_input_tokens` (uso de prompt caching)

### Paso 2 — Cuantificar gasto acumulado por modelo a tarifa API

Aplicar las tarifas públicas oficiales de Anthropic para calcular el costo equivalente que habría tenido la operación:
- **Claude Opus:** $15 / millón de input, $75 / millón de output.
- **Claude Sonnet:** $3 / millón de input, $15 / millón de output.
- **Claude Haiku:** $0.25 / millón de input, $1.25 / millón de output.

Calcular el total acumulado en los últimos 28 días:
$$\text{Gasto API Total} = \sum (\text{Tokens Input} \times \text{Tarifa In}) + \sum (\text{Tokens Output} \times \text{Tarifa Out})$$

### Paso 3 — Cálculo del ROI real de la suscripción

1. Comparar el costo real mensual pagado ($20 USD en plan Pro o $200 USD en plan Max) contra el valor total consumido a precio de API:
   $$\text{Multiplicador ROI} = \frac{\text{Gasto API Total}}{\text{Costo de Suscripción Mensual}}$$
2. Determinar si la operación es altamente rentable (ROI > 5x) o si conviene ajustar el plan.

### Paso 4 — Auditoría de salud de la memoria y contexto

1. Inspeccionar los archivos de contexto persistente (`CLAUDE.md`, bóveda de Obsidian o notas indexadas).
2. Medir la antigüedad de la última modificación:
   - **Memoria fresca:** Modificada en los últimos 7 días.
   - **Memoria en riesgo:** Entre 8 y 20 días sin cambios.
   - **Memoria rancia / obsoleta:** Más de 20 días sin actualizarse.
3. Marcar archivos desactualizados que están siendo inyectados al prompt consumiendo tokens innecesarios.

### Paso 5 — Detección de patrones repetitivos ("Rutina del Sueño")

1. Analizar los prompts y secuencias de comandos más frecuentes de los últimos 7 días:
   - Buscar acciones idénticas ejecutadas más de 3 veces (ej. extracción de transcripciones, generación de miniaturas, comandos de build o testing).
   - Identificar tareas donde se utilizó un modelo costoso (Opus) para trabajos que un modelo ligero (Haiku/Sonnet) resuelve idénticamente.
2. Formular propuestas de empaquetado:
   - *"Esta secuencia de 4 pasos para [tarea] debe convertirse en un skill `/skills/[nombre]/SKILL.md`."*

### Paso 6 — Cálculo del Operator Score (0 a 100)

Sintetizar la eficiencia de la operación agéntica en un solo número ponderado:
1. **Puntaje de ROI (0–25 pts):** 25 pts si ROI ≥ 10x; proporcional si es menor.
2. **Adopción de Skills (0–25 pts):** Frecuencia de uso de comandos `/<skill>` frente a prompts manuales no estructurados.
3. **Salud de Memoria (0–25 pts):** Proporción de archivos de contexto vigentes (<20 días) frente a memorias rancias.
4. **Constancia / Racha (0–25 pts):** Días continuos de auditoría y operación activa.

$$\text{Operator Score} = \text{Puntaje ROI} + \text{Puntaje Skills} + \text{Puntaje Memoria} + \text{Puntaje Racha}$$

### Paso 7 — Generación del reporte ejecutivo por capas

Presentar un resumen conciso estructurado según la cabina de mando:
1. **Capa Vista:** Operator Score final (0–100), racha de días activos y ROI multiplicador.
2. **Capa Costo:** Gasto mensual en suscripciones vs costo acumulado a precio API.
3. **Capa Memoria:** Archivos indexados, porcentaje de salud y los 3 archivos más urgentes a refrescar.
4. **Capa Sueño:** 4 prescripciones accionables para el día siguiente (modelos a optimizar y nuevas skills a empaquetar).
5. **Capa Agentes:** Resumen de asistentes activos (Claude Code, Hermes, OpenClaw).

---

## Outputs esperados

- Informe de costos reales y ROI de la suscripción sin estimaciones infladas.
- Diagnóstico de archivos de memoria estancados que perjudican la calidad de las respuestas.
- Lista priorizada de candidatos para nuevos skills empaquetados.

---

## Errores comunes

| Error | Causa probable | Solución |
|-------|---------------|---------|
| El script intenta modificar transcripts originales | Falta de restricción de permisos | Garantizar estrictamente permisos de **solo lectura** sobre los logs |
| ROI distorsionado o negativo | Calcular sobre periodos incompletos o sin prompts reales | Evaluar ventanas de al menos 7 a 28 días de uso activo |
| Contexto saturado crónicamente | Ignorar memorias con más de un mes de obsolescencia | Podar o refrescar los archivos de memoria que superen los 20 días sin tocar |
| Uso desproporcionado de Opus | Dejar Opus como modelo predeterminado para tareas mecánicas | Calibrar Sonnet como modelo base y reservar Opus para arquitectura pesada |

---

## Variaciones

**Variación A — Auditoría de Servidor 24/7 (Mac Mini / VPS):** Ejecutar la auditoría sobre máquinas dedicadas que operan agentes en segundo plano (Hermes, OpenClaw) para comprobar si el retorno de trabajo supera los 20x–40x de ROI.

**Variación B — Monitoreo de Proyecto Individual:** Auditar exclusivamente los tokens y llamadas de una sola carpeta de desarrollo para cotizar costos de IA a un cliente final.

---

## Notas adicionales

Un operador de IA ejecuta comandos en la trinchera; un arquitecto agéntico mira el tablero de control, cuantifica el rendimiento y toma decisiones económicas informadas sobre modelos y memoria.

---

*Creado: 2026-09-03*
