# Clase 14 — Proyecto Real: Media Buyer Agent

**Tags:** `Proyecto` `Meta` `Hailuo` `Agente Real`
**Conecta con:** Clase 10 · Clase 06 · Clase 12

---

## Idea central

Construcción de un agente de media buying completo que gestiona campañas de Meta, genera creativos con Hailuo y reporta métricas — todo desde Claude Code sin abrir el Ads Manager.

---

## Stack del proyecto

| Herramienta | Rol en el agente |
|-------------|-----------------|
| **Meta MCP** | Leer métricas, pausar/activar ads, ajustar presupuestos |
| **Hailuo** | Generación de video para creativos |
| **Airtable** | Tracking de creativos y performance |
| **Telegram** | Alertas y reportes diarios |

---

## Flujo del agente

```
1. Extrae métricas de ads activos (Meta MCP)
2. Identifica ads con bajo performance (CPA > umbral)
3. Pausa los ads malos
4. Genera nuevos creativos (Hailuo)
5. Sube los creativos y lanza nuevos ad sets
6. Guarda registro en Airtable
7. Envía resumen por Telegram
```

---

## Configuración del CLAUDE.md para este proyecto

```markdown
# Media Buyer Agent

Eres un media buyer especializado en Meta Ads.
Tu objetivo es mantener el CPA por debajo de [X] en todas las campañas activas.

## Reglas de pausa
- Pausa cualquier ad con CPA > $[X] después de $[Y] de gasto
- No pauses ads con menos de $10 gastados (sin datos suficientes)

## Herramientas
- Meta MCP: gestión de campañas
- Hailuo API: generación de creativos
- Airtable MCP: registro de cambios
```

---

## 💡 Tip

Define umbrales claros en el CLAUDE.md antes de darle autonomía al agente. Sin reglas numéricas explícitas, Claude Code puede ser demasiado conservador o demasiado agresivo al pausar ads.

---

## ⚠️ Error común

No configurar un límite de gasto diario máximo al que el agente puede operar. Sin este límite, un error en la lógica puede resultar en gasto no controlado.
