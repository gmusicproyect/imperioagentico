# SKILL: Operación Agéntica con el Framework SMART

> Guarda este archivo en `/skills/aplicar-framework-smart/SKILL.md`
> Referencia en tu CLAUDE.md: `- /skills/aplicar-framework-smart/SKILL.md → para estructurar flujos en Claude Desktop/Cowork/Code combinando Skills, MCP, Artifacts, Refine y Test`

---

## Cuándo usar este skill

Cuando el usuario requiera ejecutar tareas complejas en el ecosistema Claude (Desktop, Cowork o Code) superando el uso como chatbot tradicional, coordinando habilidades empaquetadas (Skills), conectores universales (MCP), prototipos visuales (Artifacts), supervisión en tiempo real del razonamiento (Refine) y bucles de calibración continua (Test).

---

## Prerequisitos

- [ ] Aplicación de escritorio de Claude (o acceso web / Claude Code)
- [ ] Opciones de *Memoria* y *Búsqueda en conversaciones* habilitadas en Ajustes → Capacidades
- [ ] Conectores MCP requeridos vinculados o autorizados (Notion, Gmail, Chrome, etc.)

---

## Pasos

### Paso 1 — Calibrar la base operativa (Memoria y contexto)

1. En la aplicación de Claude, acceder a **Ajustes** → **Capacidades**.
2. Verificar que estén activadas:
   - **Memoria integrada:** Para retener contexto continuo entre sesiones.
   - **Buscar y referenciar conversaciones pasadas:** Para reutilizar decisiones previas.
   - **Permisos de ejecución local / descargas:** Si se opera en modo Cowork.

### Paso 2 — Cargar o generar la Skill (S)

1. Determinar si existe una habilidad especializada para la tarea:
   - Buscar en el repositorio comunitario [skillsmp.com](https://skillsmp.com) (más de 87.000 opciones).
   - O invocar el meta-skill *Skill Creator* para generar una nueva mediante entrevista interactiva.
2. Cargar el archivo `.md` o agregarlo en la sección de Habilidades de Claude.
3. Asegurar que la skill defina tono, formato de salida y reglas estrictas para evitar el efecto *Garbage In, Garbage Out*.

### Paso 3 — Conectar las herramientas vía MCP (M)

1. Verificar que los conectores necesarios estén activos en Ajustes → Conectores:
   - **Notion MCP:** Para volcar guiones, CRM o bases de datos de contenido.
   - **Google Workspace MCP:** Para sincronizar Gmail y Calendar.
   - **Chrome Extension / Computer Use:** Para navegar o interactuar con plataformas web directamente.
2. Recordar la regla de oro: *El Skill da el criterio; el MCP da las manos.*

### Paso 4 — Supervisar e intervenir el razonamiento en vivo (R - Refine)

1. Iniciar la tarea haciendo llamado explícito a la skill y al conector MCP.
2. Mientras Claude procesa, observar la **barra de progreso** y el desglose de tareas (*todo list*).
3. Si el agente toma una dirección equivocada o se requiere una modificación sobre la marcha:
   - Inyectar el ajuste en tiempo real: *"No crees una subpágina, inserta el contenido en el documento principal"*.
   - Comprobar que Claude reorganice sus pasos antes de continuar.

### Paso 5 — Validar prototipos visuales con Artifacts (A)

1. Para entregables de interfaz, calculadoras, diagramas o dashboards, solicitar un **Artifact interactivo** (React/HTML).
2. Probar la funcionalidad directamente en la ventana lateral:
   - Evaluar diseño, colores y usabilidad.
   - Solicitar ajustes estéticos en lenguaje natural (*"hazlo en tonos naranja"*).
3. Si el prototipo requiere producción final, exportar el código hacia Claude Code o Antigravity.

### Paso 6 — Cerrar el bucle con Test y calibración (T)

1. Evaluar el resultado final contra el estándar deseado:
   - Si el output es excelente: reforzar positivamente para asentar en memoria.
   - Si hubo inconsistencias: abrir la configuración de la habilidad, seleccionar **"Editar con Claude"** y pedirle que ajuste las reglas de la skill para que nunca repita el error.

---

## Outputs esperados

- Flujo de trabajo ejecutado de punta a punta con datos sincronizados en plataformas externas vía MCP.
- Prototipo funcional validado en Artifact sin fricción técnica.
- Skill retroalimentada y memorias actualizadas para sesiones futuras.

---

## Errores comunes

| Error | Causa probable | Solución |
|-------|---------------|---------|
| Claude no recuerda proyectos anteriores | Memoria o búsqueda de historial apagadas | Encender ambos toggles en Ajustes → Capacidades |
| Respuestas genéricas sin estilo propio | Ejecutar el prompt sin invocar una skill | Asignar o referenciar siempre un skill especializado antes de pedir la tarea |
| Errores de escritura en Notion o CRM | Correr el MCP sin instrucciones de formato | Usar siempre un skill que detalle los campos y estructura exacta de la base de datos |
| Pasividad total esperando el output | Ignorar la barra de progreso | Intervenir activamente en la barra para corregir el rumbo antes de que termine |

---

## Notas adicionales

El Framework SMART transforma a Claude de un asistente reactivo en un verdadero copiloto de automatizaciones y desarrollo personal.

---

*Creado: 2026-09-03*
