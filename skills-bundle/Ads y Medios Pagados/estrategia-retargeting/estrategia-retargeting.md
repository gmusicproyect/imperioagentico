---
name: estrategia-retargeting
description: "Diseña campañas de retargeting con segmentación de audiencia, mensajes por etapa del funnel y frequency caps. Úsalo cuando re-engaging visitantes de sitio web que no convirtieron."
allowed-tools: Read Write Glob
metadata:
  author: Imperio Digital
  version: "1.0"
---

# Estrategia de Retargeting

## Cuándo Usar Este Skill

Usa este skill cuando necesites:
- Diseñar campañas de retargeting en Meta, Google u otras plataformas de ad
- Segmentar audiencias de retargeting por comportamiento y etapa del funnel
- Crear estrategias de mensajes específicas para donde los prospects se detuvieron
- Establecer frequency caps y exclusiones para evitar fatiga de ad

**NO USES** este skill para targeting de audiencia fría, secuencias de retargeting de email, o remarketing orgánico. Esto es para retargeting pagado de visitantes de sitio web y audiencias engaged.

---

## Principio Fundamental

EL RETARGETING NO ES MOSTRAR EL MISMO AD A TODOS QUE VISITARON TU SITIO — ES ENTREGAR EL MENSAJE CORRECTO BASÁNDOSE EN CUÁN LEJOS LLEGARON EN TU FUNNEL Y POR QUÉ SE DETUVIERON.

---

## Fase 1: Brief

### Inputs Requeridos

| Input | Qué Preguntar | Default |
|-------|---------------|---------|
| **Tráfico de sitio web** | "¿Cuántos visitantes mensuales de sitio web tienes?" | Sin default — debe ser proporcionado |
| **Pixel/tracking** | "¿Tienes Meta Pixel y/o Google Tag instalados?" | Necesita verificación |
| **Acción de conversión** | "¿Qué cuenta como conversión? (compra, signup, booking)" | Compra |
| **Etapas del funnel** | "¿Qué páginas visitan las personas antes de convertir?" | Homepage → Producto → Checkout |
| **Plataformas de ad** | "¿Dónde ejecutarás retargeting? (Meta, Google, ambas)" | Meta (Facebook/Instagram) |
| **Presupuesto para retargeting** | "¿Qué presupuesto puedes asignar específicamente a retargeting?" | 20% del presupuesto total de ad |

**PUNTO DE CONTROL: Confirma antes de diseñar la arquitectura de retargeting.**

---

## Fase 2: Segmentación de Audiencia

### Tiers de Audiencia de Retargeting

```
## Segmentos de Audiencia

**Tier 1: Abandoners de Carrito/Checkout** (Más hot)
- Definición: Agregó a carrito o llegó a checkout pero no compró
- Ventana: Últimos 7 días
- Prioridad: Más alta — más cercanos a conversión
- Presupuesto: 40% del presupuesto de retargeting

**Tier 2: Visitantes de Página de Producto/Ventas**
- Definición: Vio página de producto o ventas pero no agregó a carrito
- Ventana: Últimos 14 días
- Prioridad: Alta — mostraron fuerte interés
- Presupuesto: 25% del presupuesto de retargeting

**Tier 3: Engagers de Contenido**
- Definición: Leyó posts, vio videos, o pasó 30+ segundos en sitio
- Ventana: Últimos 30 días
- Prioridad: Media — interesados pero no listos
- Presupuesto: 20% del presupuesto de retargeting

**Tier 4: Visitantes Generales**
- Definición: Cualquier visitante de sitio web no en Tiers 1-3
- Ventana: Últimos 60 días
- Prioridad: Más baja — nivel de conciencia
- Presupuesto: 15% del presupuesto de retargeting
```

### Exclusiones

```
## Exclusiones Críticas

- Compradores recientes (últimos 30 días) — NO retargetees compradores con el mismo producto
- Clientes existentes — sepáralos en audiencias de venta cruzada si aplica
- Visitantes que rebotaron (bajo 5 segundos en sitio) — se fueron inmediatamente, no vale la pena retargetear
- Personas que ya convirtieron en esta campaña
```

**PUNTO DE CONTROL: Aprueba segmentos de audiencia antes de escribir ad creative.**

---

## Fase 3: Mensajes por Segmento

### Tier 1: Abandoners de Carrito

```
Ángulo de ad: Urgencia + manejo de objeciones
Copy: "Dejaste algo. Completa tu orden y obtén [incentivo]."
Creative: Muestra el producto específico que abandonaron (ads dinámicos)
CTA: Vuelve al Carrito
Incentivo: Envío gratis, 10% off, o bonus limitado
Frequency cap: 1 impresión por día
```

### Tier 2: Visitantes de Página de Ventas

```
Ángulo de ad: Social proof + refuerzo de beneficio
Copy: "¿Todavía pensando en [producto]? Aquí está lo que [nombre de cliente] dijo..."
Creative: Imagen o video enfocado en testimonial
CTA: Aprende Más / Compra Ahora
Frequency cap: 1 impresión por día
```

### Tier 3: Engagers de Contenido

```
Ángulo de ad: Valor primero + CTA suave
Copy: "¿Te gustó nuestra guía en [tema]? Aquí cómo tomar el siguiente paso..."
Creative: Contenido educativo u oferta de lead magnet
CTA: Descarga / Registrate / Lee Más
Frequency cap: 1 impresión cada 2 días
```

### Tier 4: Visitantes Generales

```
Ángulo de ad: Conciencia de marca + credibilidad
Copy: "[Brand] ayuda [audiencia] lograr [resultado]. Ve cómo."
Creative: Video de historia de marca u overview
CTA: Aprende Más
Frequency cap: 1 impresión cada 3 días
```

### Retargeting Dinámico (E-commerce)

Si aplica, configura ads dinámicos de producto:
- Muestra exactamente los productos que vieron
- Incluye precio, imagen de producto, y descripción corta
- Añade urgencia "Back in stock" o "Low stock" si es verdad

---

## Fase 4: Pulido

### 1. Gestión de Frecuencia

```
## Frequency Caps

- Abandoners de carrito: máx 1/día por 7 días, luego detén
- Visitantes de página de ventas: máx 1/día por 14 días
- Engagers de contenido: máx 1/cada 2 días por 30 días
- Visitantes generales: máx 1/cada 3 días por 60 días

Si la frecuencia excede 4 sin conversión, mueve a "cool down" (excluye por 14 días).
```

### 2. Cronograma de Refresh de Creative

- Refresca creative de ad cada 2-3 semanas
- Rota entre 3-4 variaciones de creative por audiencia
- Retira creatives cuando CTR cae bajo 0.5%

### 3. Benchmarks de Desempeño

| Métrica | Audiencia Fría | Retargeting | Objetivo |
|---------|---------------|------------|---------|
| CTR | 0.5-1.5% | 2-5% | Más alto para retargeting |
| CPC | $1-3 | $0.50-2 | Más bajo para retargeting |
| Tasa de conversión | 1-3% | 5-15% | Mucho más alto para retargeting |
| ROAS | 1-3x | 5-15x | Retargeting es tu mejor ROAS |

---

## Anti-Patrones

- **Una audiencia, un ad para todos** — un visitante primario y un abandoner de carrito necesitan mensajes completamente diferentes.
- **Sin frequency caps** — mostrar el mismo ad 20 veces crea molestia, no conversiones. Cap en 1-2 por día.
- **Retargetear compradores con el mismo producto** — felicitaciones, ya los vendiste. Excluye compradores o muévelos a campañas de venta cruzada.
- **Ventanas de retargeting demasiado largas** — alguien que visitó hace 90 días te ha olvidado. Ventanas más de 60 días para la mayoría de segmentos desperdician presupuesto.
- **Sin pixel instalado** — no puedes retargetear sin tracking. Instala pixels antes de dirigir tráfico pagado.

---

## Recuperación

- **Tráfico bajo de sitio web (bajo 1,000/mes):** Las audiencias de retargeting serán muy pequeñas. Enfócate en construir tráfico primero, luego activa retargeting cuando audiencias alcancen 1,000+ por segmento.
- **Sin datos de pixel aún:** Instala el pixel ahora y déjalo reunir datos por 2-4 semanas antes de lanzar campañas de retargeting.
- **Alta frecuencia, bajas conversiones:** El mensajería es incorrecto o la audiencia decidió no. Refresca creative, cambia la oferta, o excluye y sigue adelante.
- **Fatiga de ad en todos los creatives:** Pausa retargeting por 2 semanas para dejar que audiencias se enfríen, luego re-lanza con ángulos de creative completamente nuevos.
