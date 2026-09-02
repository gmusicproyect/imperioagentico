# SKILL: Gestionar LLM Wiki (Ingest, Query, Lint y Bulk Ingest)

> Guarda este archivo en `/skills/gestionar-llm-wiki/SKILL.md`
> Referencia en tu CLAUDE.md: `- /skills/gestionar-llm-wiki/SKILL.md → para operar y mantener la base de conocimiento tipo LLM Wiki`

---

## Cuándo usar este skill

Cuando el usuario pide incorporar fuentes crudas (transcripciones, notas, artículos, clips de web), consultar información consolidada, o auditar notas huérfanas en una base de conocimiento tipo LLM Wiki (formato Karpathy con Obsidian y Claude Code).

---

## Prerequisitos

- [ ] Bóveda de Obsidian abierta en Claude Code en su directorio raíz
- [ ] Estructura base creada: `CLAUDE.md`, `index.md`, `log.md`, `raw/` y `wiki/` (con `conceptos/`, `entidades/`, `fuentes/`, `sintesis/`)
- [ ] Contenido a procesar en `raw/` o texto/URL provisto en el prompt

---

## Pasos

### Paso 1 — Identificar la operación solicitada

Determinar cuál de las 4 operaciones nucleares corresponde ejecutar:
- **INGEST:** Para una fuente nueva individual.
- **QUERY:** Para consultar y sintetizar información existente.
- **LINT:** Para mantenimiento y conexión de notas huérfanas.
- **BULK INGEST:** Para procesar un lote de archivos acumulados en `raw/`.

### Paso 2 — Flujo de INGEST (ingesta de fuente individual)

1. Leer la fuente cruda (en `raw/` o provista en el prompt).
2. Extraer conceptos clave, entidades y tags relevantes.
3. Crear el archivo procesado en la subcarpeta correspondiente de `wiki/` (`conceptos/`, `entidades/`, `fuentes/` o `sintesis/`).
4. Añadir enlaces bidireccionales con formato `[[nombre-archivo]]` hacia notas ya existentes.
5. Actualizar `index.md` agregando la nueva entrada en la sección temática adecuada.
6. Registrar el cambio en `log.md` con timestamp y descripción breve.

```
Prompt de ejecución:
"Ingiere este contenido en la wiki: [contenido o ruta en raw/]. Clasifícalo en la categoría correcta,
extrae los conceptos clave, y linkea con archivos existentes usando [[nombre]]. Actualiza index.md y log.md."
```

### Paso 3 — Flujo de QUERY (consulta estructurada)

1. Abrir primero `index.md` para ubicar el área temática y notas raíz relacionadas.
2. Navegar siguiendo los enlaces `[[...]]` hacia los archivos de conceptos o fuentes relevantes.
3. Consolidar la respuesta citando expresamente los archivos consultados.

```
Prompt de ejecución:
"Busca en la wiki todo lo relacionado con [tema]. Empieza desde el index.md,
navega las conexiones relevantes y entrégame un resumen indicando qué archivos consultaste."
```

### Paso 4 — Flujo de LINT (mantenimiento y conexiones)

1. Explorar todos los archivos dentro de `wiki/`.
2. Identificar notas huérfanas (archivos sin enlaces entrantes ni salientes, o ausentes en `index.md`).
3. Proponer conexiones con archivos conceptuales existentes.
4. Aplicar los enlaces `[[...]]` y actualizar `index.md` tras confirmación.

```
Prompt de ejecución:
"Revisa todos los archivos de la wiki y encuentra los que están huérfanos (sin enlaces entrantes o salientes).
Propón conexiones con archivos existentes y aplícalas para integrarlos al grafo."
```

### Paso 5 — Flujo de BULK INGEST (ingesta masiva)

1. Listar los archivos pendientes en la carpeta `raw/`.
2. Procesar cada archivo uno por uno ejecutando los pasos de INGEST.
3. Consolidar al final la actualización global de `index.md` y `log.md`.

---

## Outputs esperados

- Archivos procesados en `wiki/` con estructura limpia y enlaces bidireccionales `[[...]]`
- `index.md` actualizado como mapa de navegación central
- `log.md` con historial cronológico de ingestas y modificaciones
- Grafo relacional en Obsidian conectado sin notas huérfanas

---

## Errores comunes

| Error | Causa probable | Solución |
|-------|---------------|---------|
| Claude Code no ve los archivos | Se abrió una subcarpeta en vez de la raíz del Vault | Abrir siempre la carpeta raíz donde residen `CLAUDE.md` e `index.md` |
| Notas huérfanas desconectadas | Se guardaron notas sin wikilinks ni registro en index | Correr el flujo de LINT periódicamente |
| Enlaces no renderizan como link | Obsidian está en Edit View en vez de Reading View | Alternar vista en Obsidian con Ctrl/Cmd + E |
| Clasificación imprecisa | Reglas ambiguas en `CLAUDE.md` | Definir taxonomía explícita por categoría en las reglas de `CLAUDE.md` |

---

## Variaciones

**Variación A — Ingesta vía Obsidian Web Clipper:** El usuario envía artículos o tweets desde la extensión de Chrome a `raw/clippings/`. Claude Code ejecuta INGEST tomando los clippings como insumo.

**Variación B — Agente alternativo (OpenClaw, Manus, Genspark):** La bóveda es 100% portable. Para usar otro agente, se apunta a la misma carpeta y se replica el contenido de `CLAUDE.md` en el archivo de reglas correspondiente (`AGENTS.md` o similar).

---

## Notas adicionales

El sistema LLM Wiki de Andrej Karpathy sustituye la complejidad y costo de un pipeline de embeddings por la capacidad de los modelos modernos para seguir índices estructurados y grafos en Markdown, logrando ahorros de hasta 95% en tokens por consulta.

---

*Creado: 2026-09-02*
