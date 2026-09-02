# Clase 09 — Permisos & Comandos de Sesión

**Tags:** `Permisos` `Comandos` `Seguridad`
**Conecta con:** Clase 08 · Clase 10

---

## Idea central

Claude Code pide confirmación antes de ejecutar acciones con consecuencias (borrar archivos, hacer llamadas a APIs, ejecutar código). Los modos de permiso controlan cuánta autonomía le das al agente.

---

## Modos de permiso

| Modo | Comportamiento | Cuándo usarlo |
|------|---------------|--------------|
| **Default** | Pide confirmación en acciones importantes | Proyectos nuevos |
| **Auto-accept** | Ejecuta sin pedir — más rápido | Tareas bien definidas y probadas |
| **Read-only** | Solo lee, no modifica | Auditorías, revisiones |

---

## Comandos de sesión más útiles

| Comando | Qué hace |
|---------|---------|
| `/mcp` | Lista los MCPs conectados y su estado |
| `/compact` | Compacta el historial para liberar contexto |
| `/clear` | Limpia la sesión completamente |
| `/cost` | Muestra cuántos tokens se han usado |
| `/model` | Cambia el modelo en mitad de sesión |

---

## 🎯 Ejercicio práctico

**Ejercicio 1:** Abre Claude Code en modo Default (con permisos manuales) y solicita una acción que modifique el sistema de archivos (ej. crear `test-permisos.sh`). Observa cómo el agente se detiene a pedir confirmación antes de ejecutar. Luego, prueba en la misma sesión los comandos `/cost`, `/model` y `/clear`.

**Ejercicio 2 (avanzado):** Prueba a ejecutar una tarea de análisis indicándole que actúe en modo solo lectura (read-only) para auditar un archivo sin alterar nada en el disco, comprobando que no solicite permisos de escritura.

*Este ejercicio te deja dominado el control de permisos y los comandos esenciales para operar Claude Code con seguridad.*

---

## 💡 Tip

Usa auto-accept solo cuando el flow ya está probado y sabes exactamente qué va a hacer Claude Code. Para flows nuevos, confirma cada paso para entender qué está ejecutando.

---

## ⚠️ Error común

Dejar auto-accept activado en un proyecto nuevo. Si Claude Code interpreta mal una instrucción, puede hacer cambios no deseados sin pedirte confirmación.
