# Clase 06 — MCP & Conectores

**Tags:** `MCP` `Integraciones` `APIs`
**Conecta con:** Clase 05 · Clase 07 · Bono GHL · Bono Higgsfield MCP

---

## Idea central

MCP (Model Context Protocol) es el estándar que permite a Claude Code conectarse con servicios externos. Es la diferencia entre un agente que solo escribe texto y uno que ejecuta acciones reales en el mundo.

---

## MCP vs API directa

| | MCP | API REST directa |
|--|-----|-----------------|
| Configuración | `.mcp.json` | Credentials en CLAUDE.md |
| Acciones disponibles | Las que define el servidor MCP | Todas las del API |
| Facilidad | Alta (plug & play) | Media (hay que conocer endpoints) |
| Cuándo usarlo | Cuando existe el MCP | Cuando el MCP no cubre lo que necesitas |

---

## Configuración básica `.mcp.json`

```json
{
  "mcpServers": {
    "nombre-servidor": {
      "type": "http",
      "url": "https://url-del-mcp/sse",
      "headers": {
        "Authorization": "Bearer TU_TOKEN"
      }
    }
  }
}
```

---

## MCPs más usados en el curso

| Servicio | Para qué |
|----------|---------|
| Go High Level | CRM, contactos, pipelines |
| Meta | Ads, campañas, métricas |
| Airtable | Base de datos, tracking |
| Figma | Diseño, assets |
| Google Drive | Archivos, documentos |

---

## Comando de verificación

```
/mcp
```
Corre esto en Claude Code para ver qué servidores MCP están conectados y disponibles.

---

## 🎯 Ejercicio práctico

**Ejercicio 1:** Crea un archivo `.mcp.json` en la raíz de tu proyecto definiendo la conexión a un servidor MCP (por ejemplo un conector HTTP de prueba o de tu servicio de preferencia, asegurando incluir `"type": "http"`). Abre Claude Code y corre `/mcp` para verificar que el servidor aparezca listado y activo.

**Ejercicio 2 (avanzado):** Añade en tu `CLAUDE.md` una regla de contingencia que indique a Claude Code que si una acción requerida no está disponible mediante las herramientas del MCP, recurra a la API REST directa documentando los parámetros necesarios.

*Este ejercicio te deja configurado el archivo `.mcp.json` y la verificación de conectores externos para tu proyecto.*

---

## 💡 Tip

Si un MCP no cubre una acción que necesitas, instrúyele a Claude Code en el CLAUDE.md que haga fallback a la API REST del mismo servicio usando las mismas credenciales.

---

## ⚠️ Error común

Olvidar el campo `"type": "http"` en el `.mcp.json`. Sin él, Claude Code no reconoce el servidor aunque todo lo demás esté correcto. Es el error más frecuente y no está documentado en la mayoría de MCPs.
