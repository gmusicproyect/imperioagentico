# Bono: Ads Cabrones IA v2.3

Pipeline automático de producción de anuncios cinematográficos con IA. Conecta cuatro servicios para producir un video completo desde un brief en texto.

## Stack

| Servicio | Rol | MCP/API |
|----------|-----|---------|
| **Higgsfield** (Seedance 2.0 + GPT Image 2) | Generación de imagen y video | MCP |
| **ElevenLabs** | Voiceover y música | API |
| **Airtable** | Tracking de proyectos | MCP |
| **ffmpeg** | Ensamblaje de video | CLI local |

## Los 3 inputs requeridos

```
1. Money shot     → La escena más impactante del ad (en palabras)
2. Concept board  → Referencia visual o descripción de estilo
3. Brief libre    → Qué vende, a quién, qué emoción busca generar
```

## Flujo del pipeline

```
Brief → Director Creativo (Claude) → JSON de 6 escenas
     → Higgsfield genera imagen + video por escena
     → ElevenLabs genera voiceover + música
     → ffmpeg ensambla todo
     → Airtable registra el proyecto
```

## Estructura de 6 escenas

| Escena | Propósito |
|--------|-----------|
| 1 | Hook — captura atención en los primeros 3 segundos |
| 2 | Problema — el dolor del cliente |
| 3 | Agitación — por qué el problema importa |
| 4 | Solución — el producto/servicio |
| 5 | Prueba — resultado o testimonio |
| 6 | CTA — llamada a la acción clara |

## Duración por tipo de escena

| Tipo | Duración |
|------|----------|
| Hook | 3s |
| Escenas principales | 4-6s |
| CTA | 4s |
| **Total** | ~30-35s |

## Costo estimado por ad

~$4–8 USD dependiendo de la resolución y duración

## Instalación

```bash
# 1. Conecta el MCP de Higgsfield en tu Claude Code
# 2. Agrega las credenciales de ElevenLabs y Airtable
# 3. Asegúrate de tener ffmpeg instalado localmente
ffmpeg -version  # verificar instalación
```

## Errores comunes

| Error | Causa | Solución |
|-------|-------|---------|
| Video no ensambla | ffmpeg no instalado | `brew install ffmpeg` (Mac) |
| Escenas no conectan | Brief muy vago | Especifica el money shot con más detalle |
| Voiceover desincronizado | Duración de escenas inconsistente | Usa las duraciones de la tabla de arriba |
