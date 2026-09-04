---
name: documentacion-api
description: "Crea plantillas de documentación de API con descripciones de puntos de acceso, ejemplos de solicitud/respuesta, y guías de autenticación. Usar cuando se documentan APIs REST para desarrolladores."
allowed-tools: Read Write Glob
metadata:
  author: Imperio Digital
  version: "1.0"
---

# Documentación de API

## Cuándo Usar Esta Habilidad

Usa esta habilidad cuando necesites:
- Crear documentación de API para una API REST con referencias de punto de acceso
- Escribir guías de autenticación, ejemplos de solicitud/respuesta, y documentos de manejo de errores
- Construir una guía de introducción para consumidores de API
- Estructurar una referencia completa de API para incorporación de desarrolladores

**NO** uses esta habilidad para documentación de código interno, documentación de SDK, o guías de configuración de webhooks. Esto es para documentación de API REST orientada a externos.

---

## Principio Fundamental

LA DOCUMENTACIÓN DE API SE ESCRIBE PARA DESARROLLADORES QUE QUIEREN INTEGRAR, NO LEER — CADA PÁGINA DEBE RESPONDER "¿CÓMO HAGO ESTO?" CON UN EJEMPLO COPIAR-PEGAR.

---

## Fase 1: Resumen

### Información Requerida

| Información | Qué Preguntar | Predeterminado |
|-------|------------|---------|
| **Propósito de API** | "¿Qué hace esta API en una oración?" | Sin predeterminado — debe proporcionarse |
| **URL base** | "¿Cuál es la URL base para solicitudes de API?" | Sin predeterminado — debe proporcionarse |
| **Método de autenticación** | "¿Cómo se autentican los usuarios? ¿API key, OAuth, Bearer token?" | API key en encabezado |
| **Puntos de acceso para documentar** | "Enumera todos los puntos de acceso con sus métodos HTTP." | Sin predeterminado — debe proporcionarse |
| **Formato de respuesta** | "¿JSON, XML, o ambos?" | JSON |
| **Límites de velocidad** | "¿Hay límites de velocidad? ¿Si es así, cuáles son?" | 100 solicitudes por minuto |

**PUNTO DE CONTROL: Confirma el resumen antes de estructurar la documentación.**

---

## Fase 2: Estructura

### Arquitectura de Documentación

1. **Descripción general** — Qué hace la API, para quién es, URL base
2. **Autenticación** — Cómo obtener y usar claves de API
3. **Inicio Rápido** — Primera llamada de API en menos de 5 minutos
4. **Referencia de Puntos de Acceso** — Documentación de punto de acceso completa
5. **Manejo de Errores** — Códigos de error, mensajes, y resolución
6. **Límites de Velocidad** — Límites, encabezados, y manejo de respuestas 429
7. **Registro de Cambios** — Historial de versión y cambios disruptivos

### Plantilla de Documentación de Punto de Acceso

Para cada punto de acceso, documenta:
- Método HTTP y ruta
- Descripción (una oración)
- Autenticación requerida (sí/no)
- Parámetros de solicitud (ruta, consulta, cuerpo)
- Ejemplo de solicitud (cURL)
- Ejemplo de respuesta (JSON)
- Respuestas de error
- Notas de límite de velocidad

**PUNTO DE CONTROL: Confirma estructura y lista de puntos de acceso antes de escribir.**

---

## Fase 3: Escribe

### Sección de Autenticación

```
## Autenticación

Todas las solicitudes de API requieren una clave de API pasada en el encabezado:

\`\`\`
Authorization: Bearer TU_CLAVE_DE_API
\`\`\`

**Obteniendo tu clave de API:**
1. Inicia sesión en tu dashboard
2. Navega a Configuración → API
3. Haz clic en "Generar Clave de API"
4. Copia y almacena de forma segura — no se mostrará de nuevo

**Seguridad:** Nunca expongas tu clave de API en código del lado del cliente, repositorios públicos, o URLs.
```

### Sección de Inicio Rápido

Escribe un recorrido completo de primera solicitud:
1. Obtén tu clave de API (link a sección de autenticación)
2. Haz tu primera solicitud (ejemplo cURL)
3. Entiende la respuesta
4. Próximos pasos (link a referencia completa)

### Formato de Referencia de Punto de Acceso

```
## [MÉTODO] /ruta/punto-de-acceso

[Descripción de una oración de qué hace este punto de acceso.]

### Parámetros

| Nombre | Tipo | Requerido | Descripción |
|------|------|----------|-------------|
| id | string | Sí | El ID del recurso |
| limit | integer | No | Máximo de resultados (predeterminado: 20, máximo: 100) |

### Ejemplo de Solicitud

\`\`\`bash
curl -X GET "https://api.ejemplo.com/v1/recurso" \
  -H "Authorization: Bearer TU_CLAVE_DE_API" \
  -H "Content-Type: application/json"
\`\`\`

### Ejemplo de Respuesta

\`\`\`json
{
  "data": [...],
  "meta": {
    "total": 42,
    "page": 1,
    "per_page": 20
  }
}
\`\`\`

### Respuestas de Error

| Código | Mensaje | Resolución |
|------|---------|------------|
| 401 | No autorizado | Verifica tu clave de API |
| 404 | No encontrado | Verifica que el ID del recurso exista |
| 429 | Demasiadas solicitudes | Espera y reintenta después del valor del encabezado Retry-After |
```

### Reglas de Escritura

- Cada punto de acceso tiene un ejemplo cURL que se puede copiar y ejecutar inmediatamente
- Los ejemplos de respuesta usan datos realistas (pero falsos)
- Las respuestas de error incluyen pasos de resolución, no solo códigos
- Tabla de parámetros especifica tipo, requerido/opcional, y valores predeterminados
- Usa formato consistente en todos los puntos de acceso

---

## Fase 4: Pulir

### 1. Tabla de Referencia de Errores

```
## Códigos de Error

| Código HTTP | Tipo de Error | Descripción | Resolución |
|-----------|-----------|-------------|------------|
| 400 | Solicitud Incorrecta | Parámetros inválidos | Verifica el cuerpo de la solicitud contra esquema |
| 401 | No Autorizado | Clave de API faltante o inválida | Verifica tu clave de API |
| 403 | Prohibido | Permisos insuficientes | Verifica el nivel de acceso de la API de tu plan |
| 404 | No Encontrado | El recurso no existe | Verifica el ID del recurso |
| 429 | Demasiadas Solicitudes | Límite de velocidad excedido | Reintenta después del valor del encabezado Retry-After |
| 500 | Error del Servidor | Problema del lado del servidor | Reintenta; contacta soporte si persiste |
```

### 2. Sugerencias de SDK y Biblioteca

Enumera SDKs oficiales o comunitarios si están disponibles. Si no existen, proporciona código de ejemplo en 2-3 lenguajes populares (Python, JavaScript, cURL).

### 3. Lista de Verificación de Calidad

```
## Lista de Verificación de Documentación de API

- [ ] La URL base está claramente establecida en la parte superior
- [ ] La sección de autenticación incluye configuración de clave paso a paso
- [ ] El inicio rápido obtiene a un desarrollador su primera respuesta en menos de 5 minutos
- [ ] Cada punto de acceso tiene método, ruta, descripción, parámetros, y ejemplos
- [ ] Los ejemplos cURL están listos para copiar-pegar
- [ ] Los ejemplos de respuesta usan datos falsos realistas
- [ ] Los códigos de error incluyen pasos de resolución
- [ ] La política de límite de velocidad está documentada con orientación de manejo
- [ ] El registro de cambios rastrea cambios disruptivos con fechas
- [ ] No quedan textos de marcador de posición o elementos TODO
```

---

## Ejemplo

**API:** API de gestión de facturas para un SaaS de facturación

**Extracto de inicio rápido:**
```
## Inicio Rápido

Haz tu primera llamada de API en 3 pasos:

### 1. Obtén tu clave de API
Ve a Configuración → API en tu dashboard y genera una clave.

### 2. Lista tus facturas
curl -X GET "https://api.invoicebot.com/v1/invoices" \
  -H "Authorization: Bearer sk_test_abc123"

### 3. Verifica la respuesta
{
  "data": [
    {
      "id": "inv_001",
      "client": "Acme Corp",
      "amount": 2500.00,
      "status": "paid"
    }
  ]
}

Estás listo. Explora la referencia de punto de acceso completa a continuación.
```

---

## Anti-Patrones

- **Sin ejemplos** — documentación sin ejemplos copiar-pegar es inutilizable. Cada punto de acceso necesita una solicitud y muestra de respuesta.
- **Ejemplos desactualizados** — ejemplos que retornan errores destruyen la confianza del desarrollador. Prueba cada ejemplo antes de publicar.
- **Documentación de errores faltante** — los desarrolladores pasan más tiempo manejando errores que rutas felices. Documenta cada código de error.
- **Descripciones llenas de jerga** — "Recupera una colección paginada de entidades de recursos" debe ser "Lista todas las facturas."
- **Sin inicio rápido** — obligar a desarrolladores a leer la referencia completa antes de hacer su primera llamada es un asesino de conversión.

---

## Recuperación

- **La API aún está cambiando:** Marca los docs como "beta" y versiona la API. Documenta limitaciones conocidas por adelantado.
- **Demasiados puntos de acceso para documentar a la vez:** Comienza con los 5 más utilizados. Añade el resto incrementalmente.
- **Sin SDK disponible:** Proporciona ejemplos en cURL, Python (requests), y JavaScript (fetch) para los 3 puntos de acceso principales.
- **La autenticación es compleja (OAuth):** Crea una guía de autenticación dedicada con diagrama de flujo y recorrido paso a paso.
