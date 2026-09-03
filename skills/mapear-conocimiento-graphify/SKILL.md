# SKILL: Mapeo de Conocimiento y Optimización de Contexto con Graphify

> Guarda este archivo en `/skills/mapear-conocimiento-graphify/SKILL.md`
> Referencia en tu CLAUDE.md: `- /skills/mapear-conocimiento-graphify/SKILL.md → para construir mapas relacionales de proyectos, reducir consumo de tokens con grafos locales y sincronizar con Obsidian o servidores MCP`

---

## Cuándo usar este skill

Cuando el usuario requiera indexar y consultar una base amplia de código, apuntes, documentos (PDFs, Markdown) o transcripciones multimedia sin agotar la ventana de contexto de Claude Code mediante búsquedas ciegas con `grep`. Permite reducir hasta un 76% (4.2x) los tokens por consulta creando un mapa previo de nodos, aristas y comunidades temáticas.

---

## Prerequisitos

- [ ] Python y el gestor `uv` instalados en la máquina local
- [ ] Claude Code CLI instalado y autenticado en el proyecto
- [ ] Directorio de trabajo local con archivos a indexar (código, notas, PDFs o audios)

---

## Pasos

### Paso 1 — Instalar y registrar Graphify en el entorno

1. Instalar la herramienta mediante `uv`:
   ```bash
   uv tool install graphify
   ```
2. Registrar la skill en el workspace actual para que Claude Code aprenda a invocar los comandos automáticamente:
   ```bash
   graphify install
   ```
   *Alternativa asistida:* Enviar el prompt a Claude Code: *"Investígame el repositorio https://github.com/safishamsi/graphify e instálalo en este proyecto con las mejores prácticas"*.

### Paso 2 — Definir el alcance y modo de extracción

Seleccionar la profundidad de análisis según el tipo de proyecto:
- **Modo 1: Solo código:** Análisis 100% gratuito con Tree-sitter (25 lenguajes + relaciones SQL). Ideal para repositorios puros.
- **Modo 2: Código + Documentación (Recomendado):** Incluye Markdown, PDFs y notas de texto. Es el equilibrio perfecto para bases de conocimiento y creadores.
- **Modo 3: Extracción completa (Multimodal):** Activa `faster-whisper` local para audios/videos y análisis semántico de imágenes con subagentes.

### Paso 3 — Construir el grafo inicial

Ejecutar el escaneo del directorio completo:
```bash
/graphify .
```
*(O ejecutar `graphify .` desde la terminal).*
- El proceso tardará de 5 a 25 minutos dependiendo del volumen de archivos.
- Al finalizar, genera el archivo `graph.md` (o visualizador interactivo local) con las comunidades de Leiden identificadas y los nodos principales (*God nodes*).

### Paso 4 — Consultas estructuradas sin relectura de archivos

Para formular preguntas complejas que involucren síntesis sobre múltiples documentos:
```bash
graphify query "¿cuáles son las conexiones principales entre [tema A] y [tema B] según el grafo?"
```
*Mecanismo:* El agente inspecciona únicamente el mapa de relaciones, evitando abrir y leer decenas de archivos completos en disco.

### Paso 5 — Mantenimiento incremental tras cambios

Cuando se agreguen nuevos archivos o se modifiquen partes del proyecto, evitar reindexar todo desde cero:
```bash
graphify update
```
*Función:* Procesa exclusivamente el diferencial (*git diff* / *changelog*) incorporando las nuevas conexiones al grafo existente en segundos.

### Paso 6 — Exportación a Obsidian o Servidor MCP

1. **Generar bóveda de Obsidian:**
   ```bash
   graphify obsidian
   ```
   Crea una estructura navegable de Markdown con enlaces bidireccionales (`[[nota]]`).
2. **Levantar servidor MCP:**
   ```bash
   graphify mcp
   ```
   Permite que cualquier otro agente (Hermes, Codex, Cursor) consuma el grafo relacional sin intermediarios.

---

## Outputs esperados

- Grafo estructurado local con nodos, aristas y comunidades temáticas.
- Ahorro promedio comprobado de 4x en tokens por consulta en preguntas amplias.
- Carpeta `graphify-out/` lista para ser consultada o compartida en equipo.

---

## Errores comunes

| Error | Causa probable | Solución |
|-------|---------------|---------|
| Gasto innecesario de tokens en la fase inicial | Activar modo multimodal en carpetas con cientos de imágenes irrelevantes | Seleccionar *"Código + Documentación"* y excluir carpetas como `node_modules` o temporales |
| Claude ignora el grafo y sigue usando grep | Falta de la directiva en `CLAUDE.md` | Añadir la instrucción: *"Consulta siempre graphify query antes de realizar búsquedas directas con grep"* |
| El comando `graphify update` tarda demasiado | Se borró la carpeta de caché local | Mantener la carpeta `graphify-out/` intacta para permitir comparaciones incrementales |

---

## Variaciones

**Variación A — Estrategia de Creadores de Contenido:** Descargar las transcripciones de videos y los comentarios de YouTube de la audiencia en texto plano dentro de la carpeta. Ejecutar `graphify query` para extraer las objeciones y temas más demandados por la comunidad.

**Variación B — Flujo en Equipo (Team Setup):** Un desarrollador ejecuta el grafo y commitea la carpeta `graphify-out/` al repositorio remoto. Los demás miembros leen el grafo sin costo de computación.

---

## Notas adicionales

Graphify no compite con Obsidian ni con los sistemas RAG: actúa como el puente inteligente que automatiza la extracción relacional y permite a los modelos más costosos operar a una fracción del costo habitual.

---

*Creado: 2026-09-03*
