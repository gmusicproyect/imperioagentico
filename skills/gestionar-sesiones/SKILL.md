# SKILL: Gestión de Sesiones y Control Remoto en Claude Code

> Guarda este archivo en `/skills/gestionar-sesiones/SKILL.md`
> Referencia en tu CLAUDE.md: `- /skills/gestionar-sesiones/SKILL.md → para persistir, retomar y compartir sesiones de trabajo entre dispositivos`

---

## Cuándo usar este skill

Cuando el usuario necesite continuar una sesión interrumpida sin perder contexto, recuperar una sesión anterior específica por nombre o ID, compartir una sesión local para operarla desde celular o tablet en tiempo real vía `/remote-control`, o configurar identificadores determinísticos para scripts y arquitecturas multi-agente (`--session-id`).

---

## Prerequisitos

- [ ] Claude Code CLI instalado (versión 2.1.51+ requerida para `/remote-control`)
- [ ] Directorio de trabajo local configurado con Git
- [ ] Dispositivo secundario con navegador o app de Claude (si se usa Remote Control)

---

## Pasos

### Paso 1 — Asignar un nombre descriptivo a la sesión

Al iniciar cualquier sesión importante en Claude Code, ejecutar inmediatamente el comando de renombrado para facilitar su identificación futura:

```bash
/rename [nombre-del-proyecto-o-tarea]
# Ejemplo: /rename landing-page-v2
```

### Paso 2 — Retomar la sesión más reciente del directorio

Si la terminal se cerró accidentalmente o la computadora entró en suspensión:

```bash
# Navegar al directorio del proyecto y ejecutar:
claude -c

# O con una instrucción directa:
claude -c "continúa con la tarea pendiente"
```

### Paso 3 — Seleccionar sesiones históricas con el picker interactivo

Para recuperar sesiones de días o semanas anteriores:

```bash
# Abrir el menú interactivo:
claude -r

# O reanudar directamente por el nombre asignado en el Paso 1:
claude -r "landing-page-v2"
```

*Tip:* En el picker interactivo, pulsar `/` para buscar por palabras clave en todo el historial.

### Paso 4 — Iniciar y conectar Remote Control (móvil / tablet)

Para continuar trabajando desde otro dispositivo manteniendo la ejecución en la máquina local:

1. Ejecutar desde dentro de la sesión o al lanzarla:
   ```bash
   /remote-control --name "nombre-sesion"
   # O al iniciar: claude --remote-control --name "nombre-sesion"
   ```
2. Escanear el código QR generado con la app móvil de Claude, o abrir `claude.ai/code` y seleccionar la sesión activa (marcada con ícono de computadora y punto verde 🟢).
3. Verificar que la máquina anfitriona permanezca encendida para mantener el enlace activo.

### Paso 5 — Usar session-id determinista para automatización o agentes

Cuando se lancen scripts, rutinas o agentes especializados que deban mantener su propio hilo de memoria:

```bash
# ID fijo para roles específicos o ramas de Git:
claude --session-id "agente-auditor-$(git branch --show-current)" -p "revisa los cambios recientes"
```

### Paso 6 — Exportación y mantenimiento de contexto

- Para respaldar la conversación completa en Markdown: `/export sesion-backup.md`.
- Para reducir el tamaño de contexto acumulado antes de continuar: `/compact`.
- Para reiniciar la memoria de la sesión activa: `/clear`.

---

## Outputs esperados

- Sesiones etiquetadas y recuperables en cualquier momento vía `claude -r`.
- Cero pérdida de contexto técnico tras cierres de terminal o reinicios.
- Conexión remota fluida en tiempo real desde dispositivos secundarios.
- Archivos de transcript y metadata correctamente almacenados en `~/.claude/projects/`.

---

## Errores comunes

| Error | Causa probable | Solución |
|-------|---------------|---------|
| `claude -c` carga otra conversación | Se ejecutó en una carpeta diferente | Verificar con `pwd` estar en el directorio raíz del proyecto correcto |
| Desconexión en Remote Control | La computadora host entró en reposo profundo o se apagó | Configurar la máquina para no suspenderse durante tareas largas |
| Imposible identificar sesión en el historial | No se ejecutó `/rename` al inicio | Nombrar siempre la sesión en los primeros turnos de diálogo |
| Fallo en Remote Control | Versión de CLI desactualizada (< v2.1.51) | Actualizar Claude Code a la última versión disponible |

---

## Variaciones

**Variación A — Bifurcación (Fork) vía SDK:** Cuando se requiere probar dos soluciones divergentes desde un mismo punto de partida sin alterar la sesión principal, usar la API programática de Claude Code con `{ fork: { session_id: original.session_id } }`.

**Variación B — Modo no interactivo para pipelines CI/CD:** Combinar flags `-c -p "prompt"` o `--session-id "..." -p "prompt"` para integrar en scripts bash o workflows desatendidos.

---

## Notas adicionales

Todas las sesiones se registran automáticamente en `~/.claude/projects/[proyecto]/` en formato JSONL sin fecha de caducidad, lo que permite reconstruir el historial íntegro de herramientas, comandos y razonamiento incluso meses después.

---

*Creado: 2026-09-02*
