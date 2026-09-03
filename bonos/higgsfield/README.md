# Bono: Higgsfield MCP — Agencia Creativa Completa con Claude Code

Higgsfield MCP (`https://mcp.higgsfield.ai/mcp`) transforma a Claude Code en una agencia creativa boutique completa. En lugar de saltar entre múltiples plataformas web pagando suscripciones y APIs fragmentadas, este conector unifica la generación de fotografías de producto hiperrealistas (ChatGPT Image 2), video cinematográfico (Kling 3.0), testimonios UGC (Seedance 2.0), ensamble de landing pages (Claude Design) y miniaturas de YouTube de alta conversión bajo un único pool de créditos y orquestación por terminal.

---

## 🛠️ Stack y Conectores

| Componente | Herramienta | Rol en el pipeline |
|------------|-------------|--------------------|
| **Orquestador Central** | Claude Code (CLI / IDE) | Director creativo, redacción de briefs, iteración y llamadas a herramientas |
| **Pasarela Unificada IA** | Higgsfield MCP | Conector universal a modelos de imagen y video con balance centralizado de créditos |
| **Generación de Imágenes** | ChatGPT Image 2 (`gpt_image_2`) | Creación de fotos de producto en estudio, lifestyle y miniaturas de YouTube |
| **Video Cinematográfico** | Kling 3.0 (`kling3_0`) | Animación sutil de producto (cámara lenta, iluminación cambiante, loops) |
| **Video UGC Testimonial** | Seedance 2.0 (`seedance_2_0`) | Videos verticales (9:16) de personas reales interactuando con el producto |
| **Diseño y Ensamble Web** | Claude Design | Composición visual responsive y animada de landing pages estilo agencia |
| **Hosting y Despliegue** | Vercel | Publicación online instantánea vía comando `/handoff` de Claude Code |

---

## 🔌 Instalación y Configuración del MCP (en 60 segundos)

> ⚠️ **Atención a la URL:** No uses `cloud.higgsfield.ai` (esa es la aplicación web manual). El conector MCP para agentes requiere estrictamente `https://mcp.higgsfield.ai/mcp`.

### Opción A — Desde la aplicación web o de escritorio (Claude.ai)
1. Ve a **Settings** → **Connectors**.
2. Haz clic en **Add custom connector** (`+`).
3. Completa los dos campos:
   - **Name:** `Higgsfield`
   - **URL:** `https://mcp.higgsfield.ai/mcp`
4. Haz clic en **Add** → **Connect** → Inicia sesión en tu cuenta de Higgsfield y selecciona **Allow**.

### Opción B — Directamente en Claude Code (CLI)
Dentro de tu terminal en Claude Code, escribe:
```bash
Conéctame al MCP de Higgsfield.
URL: https://mcp.higgsfield.ai/mcp
```
Aprueba los permisos de conexión permanente (`permitir siempre`). Puedes validar el estado pidiéndole: *"Muéstrame los modelos disponibles y el balance de créditos actual"*.

---

## 📝 El `CLAUDE.md` del Director Creativo ("Agencia Imperial")

Al inicializar tu proyecto (ej. `agente-de-agencias`), establece la personalidad y las restricciones económicas de trabajo en tu `CLAUDE.md`:

```markdown
# CLAUDE.md — Agencia Imperial (Dirección Creativa)

Eres el director creativo y ejecutor de una agencia de diseño boutique de branding elevado.

## Conexiones y Modelos
Te conectas a Higgsfield MCP para operar los siguientes modelos:
- Imágenes: ChatGPT Image 2 (`gpt_image_2`)
- Video cinematográfico: Kling 3.0 (`kling3_0`) por defecto
- Video UGC premium: Seedance 2.0 (`seedance_2_0`)

## Reglas Operacionales de Costo (OBLIGATORIO)
1. Generar SIEMPRE por defecto en quality: LOW y resolución: 1K (0.5 créditos).
2. NUNCA generar en alta resolución de entrada.
3. Solo ejecutar UPSCALE a calidad HIGH (2K/4K) sobre las piezas que el usuario apruebe expresamente.
4. Mantener estética premium: iluminación lateral o cenital suave, fondos limpios (mármol, madera, arena) y evitar el look artificial ("AI slop").
```

---

## 🚀 Pipeline de Producción en 5 Fases

### Fase 1: Fotos de Producto en Batch (Filtra primero, escala después)
Adjunta 1 o 2 imágenes de referencia del producto físico y solicita un lote en baja resolución:

```
A continuación adjunto fotos de referencia de [producto].
Genera 8 fotos profesionales en distintos contextos para campaña publicitaria:
- Modelo: gpt_image_2 vía Higgsfield MCP
- Calidad: low (1k), ratio: 16:9 horizontal
- Ángulos: e-commerce fondo neutro, macro de detalles, lifestyle en uso, luz de atardecer, sobre textura noble.
Muestra los prompts antes de disparar las generaciones en paralelo.
```

- **Estrategia económica:** 50 imágenes en LOW cuestan 25 créditos (~$1 USD). Escalar solo las 5 ganadoras a 2K cuesta 35 créditos (~$1.50 USD). Si generas todo en alta desde el inicio gastarías más de $15 USD en el mismo resultado.

### Fase 2: Animación a Video Cinematográfico
Elige los IDs de las imágenes ganadoras y anímalas con movimiento de cámara sutil:

```
Me gustaron las imágenes B308, B208, B207 y B206.
Anima cada una usando Kling 3.0 vía Higgsfield MCP:
- Movimiento: SUTIL, push-in lento hacia el producto, luz cambiante natural.
- Duración: 6-8 segundos | Resolución: 1080p | Ratio: 16:9
- Termina con un frame casi idéntico al inicial para permitir loop perfecto.
```

### Fase 3: Landing Page Animada con Claude Design
1. **Inspiración:** Selecciona una referencia de alta calidad visual (ej. en *Motion Sites* o las plantillas premium del Classroom de Imperio).
2. **Prompt One-Shot:** Pídele a Claude Code que compile el prompt integrador:
   *"Mapea los videos e imágenes generados a una landing page premium (Hero → Trust → Galería interactiva → Beneficios → Testimonios → CTA). Devuélveme el prompt one-shot para Claude Design."*
3. **Ensamble:** En `claude.ai/design`, sube los videos uno a uno (para evitar límites de subida en lote del navegador), pega el prompt y genera el sitio interactivo.

### Fase 4: Despliegue en Vercel en 1 Minuto
1. En Claude Design, haz clic en **Share** → **Hand to Claude Code** y copia el comando:
   ```bash
   /handoff <id-del-proyecto>
   ```
2. Pega el comando en Claude Code y dile: *"Haz deploy de esta página web en Vercel"*.
3. Claude compila el proyecto y entrega la URL pública accesible globalmente (`tu-proyecto.vercel.app`).

### Fase 5: Contenido UGC Testimonial (Reels / TikToks)
Genera testimonios verticales (9:16) de usuarios reales hablando frente a cámara:

```
Genera contenido UGC testimonial usando Seedance 2.0 para [producto]:
- 3 videos verticales (9:16) en resolución 720p (modo std).
- Personaje en entorno espontáneo (parque, oficina, hogar) sosteniendo el producto.
- Enfoques: A) Antes/después emocional, B) Descubrimiento inesperado, C) Recomendación honesta.
- Lenguaje coloquial natural, sin sonar a anuncio publicitario forzado.
```

---

## 🖼️ Bonus: Sistema de Thumbnails para YouTube (`bencord-thumbnails-pro`)

El mismo pipeline sirve para producir miniaturas de YouTube de alto CTR:
1. Carga una foto de referencia de tu rostro y tu canal en el proyecto.
2. Pide un lote inicial de 20 a 50 miniaturas en `quality: low` (0.5 créditos c/u) explorando diferentes ángulos emocionales (incredulidad, secreto, contraste de cifras).
3. Selecciona las 3 mejores y ejecuta upscale a `high + 2k`. Costo total: ~$2 USD para obtener miniaturas de nivel profesional.

---

## 💰 Desglose Real de Costos vs Agencia Tradicional

### Costos por operación (Plan Higgsfield Plus: $49/mes con 1.000 créditos = ~$0.049/crédito)

| Operación | Modelo utilizado | Créditos | Costo en USD |
|-----------|------------------|----------|--------------|
| **Imagen LOW (1K)** — Prototipado rápido | ChatGPT Image 2 | 0.5 | **$0.02** |
| **Imagen HIGH (2K)** — Upscale ganadora | ChatGPT Image 2 | 7.0 | **$0.27** |
| **Video 6-8s (1080p)** — Kling estándar | Kling 3.0 | 10.0 | **$0.39** |
| **Video 8s (720p)** — Seedance UGC | Seedance 2.0 | 36.0 | **$1.76** |
| **Video 15s (1080p)** — Seedance premium | Seedance 2.0 | 68.0 | **$3.31** |

### Campaña completa producida en la masterclass:

| Entregable | Volumen y resolución | Créditos | Costo USD |
|------------|----------------------|----------|-----------|
| Fotos de producto | 20 fotos en LOW + 3 upscale en 2K | ~31 | $1.21 |
| Videos de producto | 8 videos cinematográficos con Kling 3.0 | ~80 | $3.92 |
| Videos UGC | 5 imágenes verticales + 2 animadas con Seedance | ~75 | $3.68 |
| Landing page | Assets adicionales y ajustes | ~30 | $1.17 |
| Miniaturas de YouTube | 5 thumbnails + 3 upscale en alta | ~31 | $1.21 |
| **TOTAL SISTEMA COMPLETO** | **Todo el paquete de agencia** | **~277** | **~$10.80 USD** |

### Comparativa directa con agencia tradicional:
- Sesión fotográfica de producto: $5.000 – $10.000 USD
- Video comercial cinematográfico: $5.000 – $20.000 USD
- Landing page de diseño a medida: $5.000 – $15.000 USD
- 4 videos UGC con creadores: $1.200 USD
- **Total cotización agencia:** **$17.400 – $35.000+ USD**
- **Costo con Claude Code + Higgsfield MCP:** **~$11 USD** (*más de 1.500x más económico*).

---

## 💼 Modelo de Negocio: Cómo monetizar este servicio

| Servicio ofrecido a marcas | Precio de mercado sugerido | Costo real en créditos | Margen bruto |
|----------------------------|----------------------------|------------------------|--------------|
| **Pack 20 fotos de producto** | $500 – $1.500 USD | ~$1.21 USD | **99%+** |
| **1 Hero video cinematográfico** | $1.000 – $3.000 USD | ~$0.39 – $3.31 USD | **99%+** |
| **Landing page completa con assets** | $2.500 – $7.500 USD | ~$5.00 – $10.00 USD | **99%+** |
| **4 Videos UGC testimoniales** | $400 – $1.200 USD | ~$3.68 USD | **99%+** |
| **Paquete integral de agencia** | $5.000 – $15.000 USD | ~$11.00 USD | **99%+** |

> 💡 **Clave de venta:** No vendas "inteligencia artificial"; vende entregables de calidad comercial con un tiempo de entrega (*turnaround*) de **3 días** frente a las 3 a 4 semanas que tarda una agencia convencional.

---

## ⚠️ Lo que la IA NO reemplaza

1. **La estrategia comercial:** Claude Code ejecuta con maestría lo que tú conceptualices. Si el posicionamiento de marca es confuso o carece de propuesta de valor, solo generarás variantes rápidas de una mala idea (GIGO: *Garbage In, Garbage Out*).
2. **El ojo crítico y la curaduría:** De cada 20 generaciones, una fracción será extraordinaria, otra aceptable y otra descartable. El rol del operador se transforma de artesano creador a curador exigente.

---

## 🛠️ Errores comunes y soluciones

| Error | Causa probable | Solución |
|-------|---------------|---------|
| Fallo al conectar el MCP | Se ingresó la URL web `cloud.higgsfield.ai` | Usar estrictamente la URL del protocolo: `https://mcp.higgsfield.ai/mcp` |
| Créditos agotados rápidamente | Generar en 4K y modo premium desde la primera tirada | Generar siempre en `quality: low` (0.5 créditos) y reservar alta resolución solo para las piezas finales |
| Error al subir assets a Claude Design | El navegador bloquea la carga masiva simultánea de videos | Subir los archivos de video individualmente (uno a uno) |
| Videos con deformaciones visuales | Movimientos de cámara demasiado violentos en el prompt | Usar adjetivos restrictivos: *"movimiento sutil, push-in lento, iluminación estable"* |
