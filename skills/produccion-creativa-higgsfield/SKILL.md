# SKILL: Producción Creativa con Higgsfield MCP

> Guarda este archivo en `/skills/produccion-creativa-higgsfield/SKILL.md`
> Referencia en tu CLAUDE.md: `- /skills/produccion-creativa-higgsfield/SKILL.md → para generar fotos de producto, escalar resolución y animar videos cinematográficos o UGC vía Higgsfield MCP`

---

## Cuándo usar este skill

Cuando el usuario requiera producir activos audiovisuales de nivel profesional (fotografía publicitaria de producto, videos cinematográficos de alta fidelidad, animaciones para anuncios o testimonios UGC verticales) directamente desde Claude Code utilizando el servidor **Higgsfield MCP** (`https://mcp.higgsfield.ai/mcp`), controlando estrictamente el consumo de créditos.

---

## Prerequisitos

- [ ] Higgsfield MCP conectado en Claude Code o Claude.ai (`https://mcp.higgsfield.ai/mcp`)
- [ ] Cuenta de Higgsfield con créditos activos (plan Starter o Plus)
- [ ] 1 o 2 imágenes de referencia del producto físico o sujeto (para mantener consistencia)
- [ ] Directorio de proyecto con un `CLAUDE.md` que establezca la estética y personalidad de la marca

---

## Pasos

### Paso 1 — Comprobar conexión y balance disponible

Antes de disparar tareas en lote, verificar el estado del conector en la terminal:
```bash
Consulta mi balance de créditos y modelos disponibles en Higgsfield MCP.
```

### Paso 2 — Generar lote de exploración en baja resolución (LOW + 1K)

1. Enviar las imágenes de referencia del producto físico.
2. Solicitar un lote inicial de 8 a 20 imágenes especificando explícitamente el modelo y la política de ahorro de créditos:
   ```
   Genera 8 fotografías profesionales de [producto] en distintos ángulos y contextos:
   - Modelo: gpt_image_2 vía Higgsfield MCP
   - Calidad: low (1k de resolución)
   - Formato: 16:9 horizontal (para web/ads) o 9:16 vertical (para redes)
   - Estilo: iluminación suave, fondos elegantes (madera, piedra, mármol), producto centrado.
   Muestra los 8 prompts conceptuales antes de generar.
   ```
   *Costo:* 0.5 créditos por imagen (~$0.02 USD).

### Paso 3 — Curaduría y Upscale selectivo (HIGH + 2K)

1. Revisar los resultados generados en la carpeta local o en la pestaña de *Assets* de Higgsfield.
2. Identificar únicamente las piezas ganadoras (top 3 a 5).
3. Solicitar el escalado de calidad exclusivamente sobre esas referencias:
   ```
   Me gustaron las imágenes [IDs/nombres].
   Ejecuta upscale a calidad HIGH y resolución 2K únicamente sobre estas selecciones.
   ```
   *Costo:* 7 créditos por imagen (~$0.27 USD).

### Paso 4 — Animar a video cinematográfico de producto

Para dotar de movimiento a las imágenes escaladas:
1. Usar **Kling 3.0** por defecto para animación estándar (gran balance costo/calidad):
   ```
   Anima las imágenes [IDs ganadoras] usando Kling 3.0 vía Higgsfield MCP:
   - Movimiento: sutil, push-in lento hacia el producto, luz natural cambiante.
   - Duración: 6-8 segundos | Resolución: 1080p | 16:9.
   - Frame final similar al inicial para facilitar reproducción en loop.
   ```
   *Costo:* ~10 créditos por video (~$0.39 USD).
2. Reservar **Seedance 2.0** únicamente para planos hero principales de máxima exigencia visual (36 a 68 créditos).

### Paso 5 — Producir videos UGC testimoniales (Vertical 9:16)

Para anuncios de conversión en Instagram Reels o TikTok:
```
Genera 3 videos testimoniales verticales (9:16) de un cliente sosteniendo [producto] usando Seedance 2.0 vía Higgsfield MCP:
- Duración: 8 segundos | Resolución: 720p (modo std).
- Entornos espontáneos: oficina, cafetería, sala de estar.
- Tono natural y creíble, evitando posturas publicitarias sobreactuadas.
```

### Paso 6 — Consolidación de archivos locales

Confirmar que todos los archivos `.jpg`, `.png` y `.mp4` se hayan descargado en la carpeta de assets del proyecto local para su posterior uso en campañas de Meta Ads o ensamble de landing pages en Claude Design.

---

## Outputs esperados

- Lote de 8 a 20 fotos de producto en baja resolución para filtrado rápido.
- 3 a 5 imágenes finales escaladas en 2K/4K sin deformaciones.
- 3 a 8 videos cinematográficos en formato loop de 1080p.
- Videos UGC testimoniales listos para anuncios en redes.
- Registro completo de archivos en disco local con un gasto total inferior a $12 USD.

---

## Errores comunes

| Error | Causa probable | Solución |
|-------|---------------|---------|
| Desgaste masivo de saldo en los primeros minutos | Generar lotes exploratorios en 4K o usar Seedance para todo | Generar en LOW (1K) con GPT Image 2 y usar Kling 3.0 por defecto |
| Conector MCP no responde | Se configuró el dominio web en vez del endpoint API | Validar que la URL sea `https://mcp.higgsfield.ai/mcp` |
| Movimientos caóticos en el video | Prompts de animación demasiado genéricos o dinámicos | Indicar explícitamente: *"movimiento de cámara sutil, push-in lento, producto estable"* |
| Pérdida de identidad del producto | No se pasaron imágenes físicas de referencia | Adjuntar siempre 1 o 2 fotos del producto real antes de generar |

---

## Variaciones

**Variación A — Sistema de Miniaturas para YouTube:** Aplicar el flujo solicitando 20 a 50 thumbnails exploratorios con la cara del creador en baja resolución (0.5 créditos), seleccionar las 3 mejores variantes emocionales y escalar en 2K.

**Variación B — Catálogo E-commerce:** Mantener fondo blanco o gris neutro con iluminación de estudio para generar de 10 a 30 vistas técnicas y de detalle de un producto físico.

---

## Notas adicionales

El valor de este pipeline radica en desacoplar la producción de la dependencia de agencias externas: un solo operador puede estructurar, generar y validar una campaña publicitaria completa en 3 días con más de un 99% de margen sobre el costo en créditos.

---

*Creado: 2026-09-03*
