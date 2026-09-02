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

## 💡 Tip

Usa auto-accept solo cuando el flow ya está probado y sabes exactamente qué va a hacer Claude Code. Para flows nuevos, confirma cada paso para entender qué está ejecutando.

---

## ⚠️ Error común

Dejar auto-accept activado en un proyecto nuevo. Si Claude Code interpreta mal una instrucción, puede hacer cambios no deseados sin pedirte confirmación.
