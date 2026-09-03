# Bono: Graphify — Mapeo de Conocimiento, Ahorro de Tokens y Memoria Multimodal

**Graphify** ([github.com/safishamsi/graphify](https://github.com/safishamsi/graphify)) es una herramienta gratuita y de código abierto que construye un **grafo de conocimiento local** sobre tus proyectos, repositorios y carpetas de contenido. 

En lugar de que Claude Code o Codex operen haciendo búsquedas ciegas con `grep` (abriendo, leyendo y descartando decenas de archivos completos en cada prompt), Graphify genera un mapa previo compuesto por **nodos** (archivos, conceptos, entidades, funciones), **conexiones** explícitas y **comunidades temáticas** agrupadas con el algoritmo de Leiden. Al consultar este mapa, el agente navega con precisión quirúrgica, reduciendo el consumo de tokens en un **76% (4.2x menos tokens)** y acelerando drásticamente las respuestas.

---

## 🧭 ¿Qué es Graphify? (Grep a ciegas vs Grafo de Conocimiento)

Cuando un agente agéntico se enfrenta a una carpeta caótica (apuntes, código, PDFs, transcripciones de reuniones, videos), su mecanismo por defecto es ejecutar un `grep` extensivo: busca cadenas de texto, lee archivos enteros, agota su ventana de contexto y con frecuencia se desvía del objetivo.

```
[ Búsqueda tradicional con GREP ]
Prompt → Escaneo secuencial a ciegas (lee 35+ archivos enteros) → 67.000 tokens → Riesgo de alucinación

[ Búsqueda asistida con GRAPHIFY ]
Prompt → Consulta al Grafo / Índice relacional → Lee solo el mapa estructurado → 16.000 tokens (4.2x ahorro)
```

Graphify se sitúa en el punto de equilibrio óptimo:
- **Más estructurado y automatizado que Obsidian:** No requiere que enlaces manualmente cada archivo en Markdown.
- **Mucho más ligero y determinista que un RAG:** No utiliza bases de datos vectoriales pesadas ni embeddings de similitud probabilística para el código.

---

## ⚙️ Las 3 Fases de Extracción Interna

Graphify procesa tu carpeta en tres etapas estrictamente optimizadas para no desperdiciar dinero:

| Fase | Tipo de contenido | Motor utilizado | Costo en tokens |
|------|-------------------|-----------------|-----------------|
| **Fase 1: Código** | Clases, funciones, imports, llamadas, AST y SQL | **Tree-sitter** (local determinista en 25 lenguajes; SQL extrae tablas, vistas y JOINs) | **$0 (Cero tokens)** |
| **Fase 2: Audio y Video** | Grabaciones, videos de YouTube (`yt-dlp`), podcasts | **faster-whisper** (modelo local en tu máquina; resultados cacheados) | **$0 (Cero tokens)** |
| **Fase 3: Documentación** | PDFs, documentos Office, imágenes y notas Markdown | **Subagentes de Claude Code** en paralelo (análisis semántico de relaciones complejas) | **Tokens variables según el lote** |

---

## 🔌 Instalación Paso a Paso

Graphify es agnóstico del arnés que uses: funciona nativamente en Claude Code, Codex, Cursor, Hermes, OpenClaw, Gemini, VS Code y GitHub Copilot.

### Opción A — La vía asistida por IA (Recomendada)
Abre Claude Code dentro de tu proyecto y dile:
```
Investígame el repositorio https://github.com/safishamsi/graphify y después instálalo con las mejores prácticas en este proyecto.
```
Claude Code clona, compila y registra automáticamente el comando y la skill dentro de `.claude/` y tu `CLAUDE.md`.

### Opción B — Instalación manual vía CLI
```bash
# 1. Instalar la herramienta globalmente con uv
uv tool install graphify

# 2. Registrar el skill en tu entorno de trabajo
graphify install

# (Opcional) Si usas otra plataforma:
graphify install --platform codex
graphify install --platform cursor
```

### Módulos opcionales detectados durante la instalación:
- `faster-whisper`: Transcripción local de audio y video.
- `yt-dlp`: Descarga y procesamiento directo de canales y videos de YouTube.
- `pdf/office`: Procesamiento semántico de PDFs y documentos ofimáticos.
- `postgres / neo4j`: Exportación de grafos a bases de datos relacionales o de grafos.
- `mcp`: Servidor MCP para consultar el grafo desde cualquier modelo remoto.

---

## 🕹️ Los 2 Comandos Fundamentales

No necesitas memorizar decenas de flags; la skill registrada instruye a tu agente para que los utilice automáticamente. Como operador, solo requieres dos comandos:

| Comando | Para qué sirve | Cuándo ejecutarlo |
|---------|----------------|-------------------|
| **`/graphify .`** (o `graphify .`) | Construye el grafo completo del directorio actual (el `.` abarca todo el workspace). Tarda de 5 a 30 min según el volumen. | La primera vez que indexas una carpeta o proyecto nuevo |
| **`graphify update`** | Re-extrae **únicamente** los archivos que fueron modificados o agregados recientemente (tipo changelog / git diff incremental). | Al agregar un nuevo video, PDF o archivo de código sin reindexar todo |

### Comandos complementarios para consultas:
- **`graphify query "tu pregunta"`**: Responde basándose estrictamente en las conexiones del grafo, sin releer archivos individuales en disco.
- **`graphify obsidian`**: Genera una bóveda (*vault*) completa de Obsidian con enlaces bidireccionales (`[[nota]]`) a partir del grafo.
- **`graphify mcp`**: Expone el grafo como servidor MCP para ser consumido por otros agentes.

---

## 🎯 Modos de Extracción (Elige bien y optimiza tokens)

Al disparar `/graphify .`, el sistema te solicita la profundidad de análisis:
1. **Solo código:** Lo más rápido y económico. Ideal para explorar librerías, dependencias y repositorios de software.
2. **Código + Documentación:** Procesa apuntes, guiones, PDFs y transcripciones. Es la opción recomendada para bases de conocimiento personal o canales de contenido.
3. **Extracción completa (Multimodal):** Incluye imágenes y audio. Úsala únicamente si el contenido visual aporta valor indispensable al grafo.

---

## 💡 El Truco para Creadores: Tus Comentarios al Grafo

No indexes únicamente tus guiones o transcripciones de video: descarga también los **comentarios de tu audiencia** (mediante la API de YouTube o `yt-dlp`) y colócalos en texto plano dentro de la carpeta antes de indexar.

Al ejecutar:
```bash
graphify query "según los comentarios de mis videos, ¿cuáles son las dudas, dolores y objeciones que mi audiencia repite más?"
```
El grafo identifica las comunidades temáticas donde se concentran las preguntas de tus seguidores. La respuesta es, literalmente, el calendario editorial de tus próximos videos con demanda previamente validada.

---

## 📊 El Número Honesto de Tokens (Por qué el "70x" es un mito)

En internet prolifera la afirmación de que Graphify ahorra "70 veces" los tokens. Es una cifra inflada que asume un caso imposible: leer el disco duro completo en cada interacción.

### Medición real y comprobable (Vault de 294 archivos y 4 millones de palabras):

| Escenario de consulta | Tokens consumidos | Factor de ahorro |
|-----------------------|-------------------|------------------|
| **Sin Graphify** (Claude leyó ~35 archivos relevantes completos con grep) | ~67.000 tokens | 1.0x (Línea base) |
| **Con Graphify** (Claude leyó únicamente el mapa relacional estructurado) | ~16.000 tokens | **4.2x menos (76% de ahorro real)** |

### La matemática con modelos costosos (Fable 5 / Opus):
Si un modelo de razonamiento superior cuesta el doble pero consume **4 veces menos tokens** gracias al grafo de Graphify, **la consulta final resulta un 50% más económica** que utilizar un modelo estándar sin índice.

---

## 🔄 ¿Cuánto cuesta mantener el grafo actualizado?

- **Material estático (libros, papers, apuntes):** Se procesa una sola vez. Costo de mantenimiento = $0.
- **Creadores de contenido:** Basta con ejecutar `graphify update` al publicar un nuevo video o documento; únicamente procesa la diferencia incremental en segundos.
- **Equipos de desarrollo (Team Setup):** Un integrante del equipo ejecuta el mapeo y realiza el commit de la carpeta `graphify-out/` al repositorio; el resto de los colaboradores y sus agentes leen directamente el mapa sin gastar tokens adicionales.

---

## 🤝 Graphify + Obsidian: Cómo se complementan

No son herramientas rivales, sino dos mitades del mismo sistema:
- **Obsidian:** Es la interfaz humana y el wiki legible que tú abres, lees y mantienes en Markdown.
- **Graphify:** Es el motor algorítmico que analiza el caos de tu disco, identifica comunidades y exporta con `graphify obsidian` una bóveda viva y conectada.

Ambos se integran a la perfección con el **Motor Agéntico**, que audita la frescura de los nodos y previene que el agente trabaje con memorias rancias.

---

## 🛠️ Errores Comunes y Troubleshooting

| Problema | Causa probable | Solución |
|----------|---------------|---------|
| La extracción inicial tarda más de 30 min | Se seleccionó el modo multimodal sobre una carpeta gigante | Seleccionar *"Código + Documentación"* y excluir carpetas prescindibles (ej. `node_modules`, `dist`) |
| `faster-whisper` da error de memoria | Falta de VRAM o dependencias de C++ | Desactivar la transcripción de audio local si solo se procesa texto, o correr en CPU con modelo `tiny`/`base` |
| El agente no usa el grafo en sus respuestas | No se registró la skill en el proyecto | Ejecutar `graphify install` para asegurar que el skill esté listado en `.claude/` y referenciado en `CLAUDE.md` |
| Grafo desactualizado tras cambios de código | No se corrió la actualización incremental | Ejecutar `graphify update` al finalizar jornadas de desarrollo intensivo |
