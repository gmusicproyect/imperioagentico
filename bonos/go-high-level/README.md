# Bono: Go High Level + Claude Code

Integración completa de Claude Code con Go High Level (GHL) para gestionar el CRM desde terminal sin abrir la interfaz web.

## Qué puedes hacer

- Crear y actualizar contactos
- Mover oportunidades entre etapas del pipeline
- Agregar notas y tags
- Consultar métricas de conversión
- Automatizar seguimientos

## Prerequisitos

- Cuenta GHL (subcuenta, no agencia)
- Node.js instalado
- Claude Code con plan Pro o superior

## Paso 1 — Crear el Private Integration Token (PIT)

1. En tu **subcuenta** de GHL → Settings → Private Integrations
2. Crear nueva integración → nombre: `claude-code-ghl`
3. **Select all** en permisos (incluye los 130+ scopes)
4. Copiar el token — solo se muestra una vez
5. El token empieza con `ghl_`

> ⚠️ Usa el token de **subcuenta**, no de agencia. Son diferentes y el de agencia no funciona para este MCP.

## Paso 2 — Configurar `.mcp.json`

```json
{
  "mcpServers": {
    "ghl": {
      "type": "http",
      "url": "https://services.leadconnectorhq.com/mcp/",
      "headers": {
        "Authorization": "Bearer TU_PIT_AQUI",
        "Version": "2021-07-28",
        "locationId": "TU_LOCATION_ID"
      }
    }
  }
}
```

> ⚠️ El campo `"type": "http"` es **obligatorio**. Sin él, Claude Code no reconoce el servidor aunque todo lo demás esté correcto. No está documentado en la mayoría de guías.

## Paso 3 — Obtener tu Location ID

En GHL → Settings → Business Profile → Location ID (un string alfanumérico)

## Paso 4 — Verificar conexión

En Claude Code, escribe: `/mcp`

Deberías ver `ghl` en la lista con estado `connected`.

## Paso 5 — System prompt recomendado

```
Eres mi asistente de CRM. Tienes acceso a Go High Level vía MCP.

Antes de asignar un contacto a un pipeline, lista los pipelines disponibles
y confirma el nombre exacto conmigo.

Si una acción no está disponible vía MCP, usa la API REST de GHL 
directamente con las mismas credenciales.
```

## Errores comunes

| Error | Causa | Solución |
|-------|-------|---------|
| MCP no aparece en `/mcp` | Falta `"type": "http"` en `.mcp.json` | Agregar el campo |
| 401 Unauthorized | Token de agencia en vez de subcuenta | Generar PIT desde la subcuenta |
| Pipeline not found | Nombre del pipeline no coincide exactamente | Pedir a Claude que liste los pipelines primero |
| Action not supported | El MCP cubre 36 acciones — no todas | Usar la API REST como fallback |
