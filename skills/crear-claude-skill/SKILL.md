# SKILL: Creación de Skills Efectivos para Claude

> Guarda este archivo en `/skills/crear-claude-skill/SKILL.md`
> Referencia en tu CLAUDE.md: `- /skills/crear-claude-skill/SKILL.md → para estructurar, redactar y validar nuevos skills agénticos reutilizables`

---

## Cuándo usar este skill

Cuando el usuario necesite estandarizar una tarea recurrente en un procedimiento operativo formal (`SKILL.md`), diseñar una nueva habilidad modular para Claude Code o la app de Claude, o convertir un prompt largo e ineficiente en un componente reutilizable que no sature la ventana de contexto.

---

## Prerequisitos

- [ ] Un proceso que ya se haya ejecutado manualmente con éxito al menos 2 veces
- [ ] Acceso a la plantilla base del repositorio (`recursos/plantillas/skill-template.md`)
- [ ] Identificación clara de si la tarea requiere herramientas externas (MCPs) o solo procesamiento de archivos locales

---

## Pasos

### Paso 1 — Delimitar la tarea y redactar el trigger de activación

1. Asegurar que el skill sea **atómico**: debe resolver un único problema concreto (ej. `redactar-post-linkedin`, `auditar-contrato-legal`, `generar-reporte-ventas`).
2. Redactar la sección **Cuándo usar este skill** con verbos de acción y palabras clave inequívocas que permitan a Claude invocar la habilidad bajo demanda sin ambigüedad.

### Paso 2 — Declarar prerequisitos e integraciones MCP

1. Listar los requisitos de entorno indispensables (archivos de entrada, credenciales en `.env`, dependencias de software).
2. Si el proceso interactúa con servicios externos (Notion, Mercury, Apollo, Instantly, Meta Ads), detallar el servidor MCP que debe estar activo en la máquina host.

### Paso 3 — Desglosar el procedimiento operativo en pasos secuenciales

1. Escribir los pasos en orden cronológico numerado.
2. Cada paso debe contener:
   - La acción precisa que ejecuta el agente.
   - Entradas requeridas.
   - Bloques de código, comandos bash o formatos de prompt específicos a usar.
   - Puntos de validación antes de continuar al siguiente paso.

### Paso 4 — Definir el contrato de outputs esperados

1. Especificar el formato exacto del resultado final (archivo Markdown, tabla comparativa, página web en HTML, payload JSON o registro en base de datos externa).
2. Proporcionar un ejemplo representativo del resultado esperado para anclar el estilo y evitar dispersión ("AI slop").

### Paso 5 — Documentar errores comunes y reglas negativas

1. Identificar las fallas más habituales observadas durante la ejecución manual.
2. Construir la tabla de **Errores comunes** indicando el síntoma, la causa probable y la corrección directa.
3. Especificar qué **no** debe hacer el agente bajo ninguna circunstancia.

### Paso 6 — Validar en frío e iterar

1. Abrir una sesión limpia en Claude Code y solicitar la tarea usando una instrucción en lenguaje natural sin invocar el archivo explícitamente.
2. Confirmar que Claude cargue el `SKILL.md` correcto.
3. Evaluar el output frente a los criterios deseados y refinar las instrucciones si se detectaron desvíos.

---

## Outputs esperados

- Archivo `SKILL.md` estructurado y validado dentro de su propia carpeta en `/skills/[nombre-del-proceso]/`.
- Entrada registrada en el índice de skills (`skills/README.md`) y referenciada en el `CLAUDE.md` del proyecto.
- Ejecución determinística y repetible sin fuga de contexto.

---

## Errores comunes

| Error | Causa probable | Solución |
|-------|---------------|---------|
| Skill demasiado abarcador | Intento de crear un "asistente general" en un solo archivo | Dividir en múltiples skills atómicos e independientes |
| Claude no activa el skill automáticamente | Trigger en "Cuándo usar" vago o ambiguo | Agregar situaciones de uso específicas y palabras clave frecuentes |
| Respuestas genéricas ("AI slop") | Falta de lineamientos estilísticos y ejemplos en el skill | Incluir reglas estrictas de tono, estructura y ejemplos concretos |
| Confusión entre MCP y Skill | Intentar que el skill emule una API sin conectar el MCP | Configurar el conector MCP para datos y usar el skill para el procedimiento |

---

## Variaciones

**Variación A — Skill con scripts complementarios:** Para procesos que demanden cómputo intensivo o transformaciones deterministas, almacenar scripts auxiliares (Python, Node.js, Shell) en una subcarpeta `/scripts/` dentro del skill y referenciarlos en los pasos.

**Variación B — Skill para la app móvil / Web de Claude:** Empaquetar el archivo `SKILL.md` junto con sus archivos de soporte en un archivo `.zip` para importarlo directamente desde *Configuración → Capacidades → Habilidades* en la interfaz web de Claude.

---

## Notas adicionales

Un skill bien diseñado actúa como un multiplicador de productividad: reduce días de trabajo a minutos, protege la ventana de contexto de tokens y permite transferir conocimientos operativos estandarizados entre miembros de un equipo o comunidad sin fricción.

---

*Creado: 2026-09-02*
