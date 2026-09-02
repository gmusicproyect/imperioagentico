# Clase 07 — Browser & Playwright

**Tags:** `Browser` `Automatización` `Playwright`
**Conecta con:** Clase 06 · Bono Playwright

---

## Idea central

Playwright permite a Claude Code controlar un navegador para automatizar apps que no tienen MCP ni API. En lugar de ver la pantalla (como Computer Use), lee el accessibility tree — lo que hace que sea más preciso y mucho más barato en tokens.

---

## Playwright vs Computer Use

| | Playwright | Computer Use |
|--|-----------|-------------|
| Cómo ve la app | Accessibility tree (texto) | Screenshot (imagen) |
| Tokens por acción | Bajos | Muy altos |
| Precisión | Alta | Media (puede fallar visualmente) |
| Cuándo usarlo | Apps web estándar | Apps visuales / nativas |

---

## Instalación rápida

```
Conecta el MCP de Playwright a Claude Code y dile:
"Abre Chrome, navega a [URL] y extrae [dato]"
```
No requiere cuenta ni API key — es local.

---

## Casos de uso reales

| Caso | Descripción |
|------|-------------|
| **Google Trends** | Extraer datos de tendencias sin API |
| **UI debugging** | Verificar cómo se ve la app en distintos viewports |
| **Métricas de Skool** | Extraer stats de comunidades sin API pública |

---

## Modos de ejecución

- **Headed** (con ventana visible): para desarrollo y debugging
- **Headless** (sin ventana): para producción y automatización

---

## Combinación con Skills y Routines

```
Routine diaria → activa Playwright → extrae métricas → guarda en Airtable
```

---

## 💡 Tip

Para sesiones autenticadas, usa perfiles persistentes de Chrome. Playwright puede mantener la sesión iniciada entre ejecuciones sin volver a hacer login.

---

## ⚠️ Limitaciones

- Consume más tokens que un MCP directo — úsalo cuando no hay alternativa
- Sitios con anti-bot detection (Cloudflare) pueden bloquearlo
- Los flows necesitan iteración: rara vez funcionan perfecto a la primera
