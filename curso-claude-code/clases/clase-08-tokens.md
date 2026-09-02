# Clase 08 — Tokens & Contexto

**Tags:** `Tokens` `Contexto` `Optimización`
**Conecta con:** Clase 03 · Clase 09

---

## Idea central

Claude Code trabaja con una ventana de contexto limitada. Saber cómo se consumen los tokens y cómo gestionarlos es lo que separa proyectos que funcionan bien de los que se rompen a mitad de tarea.

---

## Cómo se consumen tokens en Claude Code

| Fuente | Impacto |
|--------|---------|
| CLAUDE.md | Se carga en cada sesión |
| Skills leídos | Se suman al contexto |
| Historial de conversación | Crece con cada turno |
| Outputs de herramientas | Pueden ser muy largos (ej. screenshots) |
| Archivos leídos | Depende del tamaño |

---

## Estrategias de gestión

**Compactación automática:** Claude Code compacta el historial cuando se acerca al límite. Puedes forzarla con `/compact`.

**Contexto selectivo:** No incluyas archivos completos si solo necesitas una sección. Pídele a Claude que lea solo las líneas relevantes.

**Skills cortos:** Un SKILL.md de 50 líneas es mejor que uno de 500. El contexto que no se necesita es contexto desperdiciado.

**Monitoreo:** Usa `/cost` en cualquier momento para ver cuántos tokens llevas consumidos en la sesión actual.

---

## Señales de contexto saturado

- Claude Code empieza a "olvidar" instrucciones del CLAUDE.md
- Respuestas que contradicen lo establecido al inicio
- Errores extraños en tareas que antes funcionaban

**Solución:** Empieza una nueva sesión o usa `/compact` para limpiar el historial.

---

## 🎯 Ejercicio práctico

**Ejercicio 1:** Inicia una sesión en Claude Code, revisa el consumo de tokens inicial con `/cost`, pídele analizar un archivo mediano de tu proyecto y vuelve a ejecutar `/cost` para comprobar con exactitud cuántos tokens de entrada y salida consumió esa operación.

**Ejercicio 2 (avanzado):** Ejecuta el comando `/compact` para forzar la reducción del historial de la sesión. Luego, hazle una pregunta que dependa directamente de una regla definida al comienzo de tu `CLAUDE.md` para verificar que el contexto esencial sobrevivió a la compactación.

*Este ejercicio te deja dominada la técnica de monitoreo de gasto y compactación de memoria para sesiones de trabajo extensas.*

---

## 💡 Tip

Estructura el CLAUDE.md de lo más importante a lo menos importante. Si el contexto se compacta, lo que está al principio tiene más probabilidad de sobrevivir.
