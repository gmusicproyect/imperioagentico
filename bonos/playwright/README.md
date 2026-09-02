# Bono: Playwright — Browser Automation

Automatización de browser para apps y sitios que no tienen MCP ni API disponible. Claude Code lee el accessibility tree del navegador (no screenshots) para interactuar con la página.

## Por qué Playwright y no Computer Use

| | Playwright | Computer Use |
|--|-----------|-------------|
| Cómo ve la app | Accessibility tree (texto estructurado) | Screenshots (imágenes) |
| Tokens por acción | Bajos | Muy altos |
| Precisión | Alta — lee la estructura real | Media — puede fallar con UI compleja |
| Velocidad | Rápido | Lento |
| Cuándo usarlo | Apps web estándar | Apps nativas / muy visuales |

## Instalación

No requiere cuenta ni API key. Es local.

```bash
# Conectar el MCP de Playwright desde Claude Code
# Luego en la interfaz: herramientas → Playwright → conectar
```

## Modos de ejecución

```
headed    → con ventana visible  → para desarrollo y debugging
headless  → sin ventana          → para producción y automatización
```

## Casos de uso reales

### 1. Extraer datos de Google Trends

```
Prompt: "Abre Google Trends, busca [keyword], 
extrae los datos de los últimos 12 meses y 
guárdalos en un CSV"
```

### 2. Debugging de UI en distintos viewports

```
Prompt: "Abre mi landing page en [URL], 
captúrala en mobile (375px), tablet (768px) y desktop (1440px), 
dime si hay elementos que se rompen visualmente"
```

### 3. Extraer métricas de Skool

```
Prompt: "Entra a mi comunidad de Skool en [URL],
extrae el número de miembros, posts esta semana
y los 3 posts con más engagement"
```

## Combinación con Skills y Routines

```
Routine diaria 8am
  → Playwright extrae métricas de [sitio]
  → Claude Code procesa y compara con ayer
  → Guarda resumen en Obsidian
  → Manda alerta por Telegram si hay cambio > 20%
```

## Sesiones autenticadas

Para sitios que requieren login, usa perfiles persistentes:

```
"Usa el perfil de Chrome 'mi-perfil-trabajo' 
para acceder a [sitio] — ya tengo la sesión iniciada ahí"
```

## Limitaciones

| Limitación | Descripción |
|-----------|-------------|
| Tokens | Más costoso que MCP directo — úsalo cuando no hay alternativa |
| Anti-bot | Cloudflare y similares pueden bloquearlo |
| Iteración | Los flows raramente funcionan perfecto a la primera |
| Velocidad | Más lento que una API directa |

## Tips

- Siempre empieza en modo **headed** para ver qué hace Claude Code
- Pasa a **headless** solo cuando el flow ya funciona bien
- Para sitios con muchos modales/popups, instrúyele a Claude que los cierre antes de navegar
