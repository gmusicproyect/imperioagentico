# Clase 18 — LLM Wiki con Obsidian: memoria infinita sin RAG

**Tags:** `Obsidian` `LLM Wiki` `Memoria` `Karpathy`
**Conecta con:** Clase 13 · Clase 04 · Clase 08 · Bono Graphify

---

## Idea central

En lugar de vectorizar PDFs y pagar infraestructura para un RAG tradicional, un LLM Wiki (formato Andrej Karpathy) organiza el conocimiento en archivos Markdown interconectados como Wikipedia. Claude Code navega desde el índice a través de relaciones directas, reduciendo hasta un 95% el gasto de tokens y manteniendo una memoria 100% portable entre agentes.

---

## LLM Wiki vs RAG tradicional

| Dimensión | RAG tradicional | LLM Wiki (Karpathy + Obsidian) |
|-----------|-----------------|--------------------------------|
| Búsqueda | Similaridad semántica (vectores) | Navegación estructurada desde `index.md` |
| Costo e infra | Embeddings, base vectorial, hosting | $0 (archivos Markdown locales) |
| Tokens por query | Altos (múltiples chunks crudos) | Reducción de hasta 95% por ruta dirigida |
| Portabilidad | Atado al pipeline o proveedor | 100% portable (Claude Code, OpenClaw, etc.) |
| Escala óptima | Millones de documentos corporativos | Cientos a miles de notas, videos o SOPs |

---

## Estructura de archivos del Vault

```
/mi-wiki
├── CLAUDE.md       → Reglas del sistema y comportamiento del agente
├── index.md        → Mapa principal que la IA lee primero
├── log.md          → Registro cronológico de cambios
├── raw/            → Fuentes crudas sin clasificar (transcripciones, clips)
└── wiki/           → Archivos procesados con enlaces [[wikilinks]]
    ├── conceptos/  ├── entidades/  ├── fuentes/  └── sintesis/
```

Cada archivo Markdown se enlaza con otros usando `[[nombre-archivo]]`, construyendo el grafo relacional visible en Obsidian.

---

## Las 4 operaciones del sistema

| Operación | Prompt clave | Qué hace el agente |
|-----------|--------------|-------------------|
| **INGEST** | "Digiere este archivo y clasifícalo" | Procesa una fuente, extrae conceptos y crea wikilinks |
| **QUERY** | "Busca en la wiki qué sabemos sobre X" | Navega desde `index.md` por las conexiones relevantes |
| **LINT** | "Revisa archivos huérfanos y conéctalos" | Detecta notas desconectadas e integra relaciones al grafo |
| **BULK INGEST** | "Procesa todos los archivos de raw/" | Clasifica múltiples fuentes secuencialmente y actualiza index |

---

## 🎯 Ejercicio práctico

**Ejercicio 1:** Descarga Obsidian, crea una bóveda llamada `mi-wiki` y ábrela en Claude Code. Genera la estructura base (`CLAUDE.md`, `index.md`, `log.md`, carpetas `raw/` y `wiki/`) y pídele a Claude Code que ingeste una primera fuente en `raw/`, clasificándola en `wiki/` con al menos dos enlaces bidireccionales `[[...]]`.

**Ejercicio 2 (avanzado):** Agrega 3 notas interconectadas, abre la vista de grafo en Obsidian para verificar visualmente los nodos unidos y corre el prompt de LINT en Claude Code para comprobar que no existan notas huérfanas.

*Este ejercicio te deja lista tu propia bóveda de LLM Wiki funcionando como memoria persistente para tus proyectos agénticos.*

---

## 💡 Tip

Abre siempre la carpeta raíz del Vault en Claude Code, no una subcarpeta; así el agente mantiene visibilidad simultánea del `CLAUDE.md`, el índice y todas las categorías de la wiki.

---

## ⚠️ Error común

Agregar documentos a la carpeta `wiki/` sin registrarlos en `index.md` ni vincularlos mediante `[[...]]`. La IA navega siguiendo rutas de enlaces; si un archivo queda huérfano, Claude Code no podrá llegar a él durante las consultas.
