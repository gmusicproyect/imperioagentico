# Clase 21 — Framework SMART: Domina Claude de Chatbot a Entorno Agéntico

**Tags:** `Framework SMART` `Skills` `MCP` `Artifacts` `Refine`
**Conecta con:** Clase 03 · Clase 05 · Clase 06 · Clase 11

---

## Idea central

La mayoría de los usuarios opera Claude como un simple chatbot conversacional, desperdiciando el 90% de su capacidad. El **Framework SMART** (*Skills, MCP, Artifacts, Refine, Test*) es la metodología integral para transformar Claude Desktop, Cowork o Claude Code en un entorno agéntico de desarrollo y automatización de alto rendimiento.

---

## El Acrónimo SMART

| Letra | Componente | Rol en el flujo agéntico | Beneficio clave |
|-------|------------|--------------------------|-----------------|
| **S** | **Skills** | Habilidades empaquetadas con reglas y contexto | Erradica el efecto *Garbage In, Garbage Out* |
| **M** | **MCP** | Conectores universales (Notion, Gmail, Calendar, Chrome) | Permite leer, crear y modificar datos externos |
| **A** | **Artifacts** | Mini-aplicaciones y MVPs interactivos en tiempo real | Valida prototipos funcionales antes de tocar código |
| **R** | **Refine** | Supervisión de la barra de progreso (*Reasoning/Tasks*) | Permite intervenir y reorientar pasos en ejecución |
| **T** | **Test** | Ciclo de retroalimentación y autoedición de skills | Cierra el bucle de mejora continua con memoria activa |

---

## 🛠️ Los 5 Pilares en Práctica

### 1. S — Skills (Habilidades Especializadas)
- Evita tener que repetir tu tono, contexto de empresa o reglas de formateo en cada prompt.
- **Directorio abierto:** [skillsmp.com](https://skillsmp.com) reúne más de 87.000 skills comunitarias categorizadas (automatización, desarrollo, productividad, IA).
- **Meta-Skill:** Usa *Skill Creator* para que Claude te entreviste y redacte nuevas skills automáticamente.

### 2. M — MCP (Model Context Protocol)
- El estándar abierto de Anthropic que convierte a Claude de un modelo pasivo en un operador de herramientas.
- Permite interactuar bidireccionalmente con Notion (ej. poblar un *Content OS* con guiones y lead magnets), Google Workspace, Canva, bases de datos o extensiones de Chrome para navegar la web.

### 3. A — Artifacts (Prototipado Visual Rápido)
- Ventana lateral dedicada a renderizar componentes React, páginas web interactivas, dashboards, diagramas SVG o mini-herramientas.
- Ideal para validar un *Proof of Concept* (PoC) visual con clientes en minutos antes de escalarlo a Claude Code o producción.

### 4. R — Refine (Intervención de Tareas en Vivo)
- La barra de progreso de Claude no es un adorno: desglosa la lista de tareas (*todo list*) y el razonamiento del modelo.
- Puedes pausar, inyectar nuevas subtareas o reorientar el entregable mientras el agente está trabajando sin abortar la sesión.

### 5. T — Test (Bucle de Calibración Continua)
- Ninguna tarea termina cuando el modelo entrega el primer borrador; concluye cuando el resultado supera tu estándar de calidad.
- Usa la función **"Editar con Claude"** dentro del menú de Capacidades para retroalimentar la skill con las correcciones detectadas.

---

## ⚙️ Las 2 Configuraciones Críticas que Debes Activar

En la aplicación de escritorio de Claude (Ajustes → Capacidades), activa manualmente estas dos opciones que vienen apagadas por defecto:
1. **Memoria integrada:** Permite que Claude retenga hechos, preferencias y directivas entre distintas sesiones.
2. **Buscar y referenciar conversaciones pasadas:** Otorga contexto histórico amplio sobre proyectos previos sin tener que reexplicar antecedentes.

---

## 🎯 Ejercicio práctico

**Ejercicio:** Implementar una cadena SMART completa en Claude Cowork o Desktop:
1. Activa la *Memoria* y la *Búsqueda en conversaciones* en tus Ajustes.
2. Descarga o genera un skill de creación de contenido o prospección con *Skill Creator*.
3. Conecta un MCP disponible (ej. Notion o Google Drive) desde la sección de Conectores.
4. Pide a Claude que ejecute la tarea guiada por el skill, interviniendo al menos un paso en la barra de progreso (**Refine**).
5. Solicita un **Artifact** interactivo para visualizar el resultado y ajusta la definición de la skill con el feedback final (**Test**).

*Este ejercicio te deja configurada tu cabina operativa de Claude Desktop para proyectos del curso.*

---

## 💡 Tip

No programes un software complejo desde cero en la terminal si todavía no tienes claro el flujo de usuario. Pídele primero a Claude que genere un **Artifact interactivo** en el chat: modifícalo visualmente, valida la experiencia en 5 minutos y luego pásale ese código a Claude Code para llevarlo a producción.

---

## ⚠️ Error común

Creer que los conectores MCP y los Skills son excluyentes. La **Skill da las instrucciones y el criterio** (cómo pensar); el **MCP da las manos y los accesos** (cómo ejecutar). Si usas un MCP sin un skill, Claude cometerá errores de formato en tu base de datos; si usas un skill sin MCP, Claude te dará texto plano que tendrás que copiar y pegar a mano.
