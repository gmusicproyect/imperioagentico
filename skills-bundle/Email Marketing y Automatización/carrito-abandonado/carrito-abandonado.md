---
name: carrito-abandonado
description: "Escribe secuencias de email para carrito abandonado con timing, líneas de asunto, escalada de incentivos y notas de imágenes de producto. Úsalo cuando recuperes ventas perdidas de clientes que dejaron artículos en su carrito."
allowed-tools: Read Write Glob
metadata:
  author: Imperio Digital
  version: "1.0"
---

# Email de Carrito Abandonado

## Cuándo Usar Este Skill

Usa este skill cuando necesites:
- Escribir una secuencia de email de carrito abandonado (2-4 emails) para recuperar ventas perdidas
- Crear líneas de asunto, timing y estrategias de escalada de incentivos
- Diseñar emails con colocación de imágenes de producto y elementos de urgencia
- Construir un sistema de recuperación de carrito para un negocio de e-commerce o productos digitales

**NO** uses este skill para emails promocionales generales, secuencias de bienvenida, o boletines. Esto es específicamente para recuperación de carrito abandonado.

---

## Principio Fundamental

LOS EMAILS DE CARRITO ABANDONADO FUNCIONAN PORQUE EL CLIENTE YA QUERÍA EL PRODUCTO — TU TRABAJO ES ELIMINAR LA FRICCIÓN QUE LOS DETUVO, NO VENDER DESDE CERO.

---

## Fase 1: Resumen

### Entradas Requeridas

| Entrada | Qué Preguntar | Por Defecto |
|-------|------------|---------|
| **Tipo de producto** | "¿Qué fue abandonado? ¿Producto físico, producto digital, curso, suscripción?" | Sin valor por defecto — debe ser proporcionado |
| **Valor promedio del carrito** | "¿Cuál es el valor típico del carrito?" | Sin valor por defecto — debe ser proporcionado |
| **Objeciones comunes** | "¿Por qué los clientes típicamente abandonan? ¿Precio, envío, comparación?" | Precio y distracción |
| **Presupuesto de incentivo** | "¿Puedes ofrecer un descuento, envío gratis, o bonificación para recuperar carritos?" | Descuento del 10% disponible |
| **Plataforma de email** | "¿Qué herramienta de email usas?" | Cualquiera (proporcionaré plantillas genéricas) |
| **Número de emails** | "¿Cuántos emails en la secuencia? (2-4 recomendados)" | 3 emails |

**PUNTO DE CONTROL: Confirma el resumen antes de escribir la secuencia.**

---

## Fase 2: Esquema

### Arquitectura de Secuencia

```
## Secuencia de Carrito Abandonado

**Email 1:** Recordatorio (1 hora después del abandono)
- Tono: Útil, no invasivo
- Propósito: Recuérdales que su carrito los espera
- Sin incentivo aún

**Email 2:** Eliminador de Objeciones (24 horas después del abandono)
- Tono: Tranquilizador, social proof
- Propósito: Aborda la razón por la que dudaron
- Incentivo ligero (opcional)

**Email 3:** Última Oportunidad (48-72 horas después del abandono)
- Tono: Urgencia + incentivo
- Propósito: Crea urgencia y ofrece el incentivo más fuerte
- Incentivo completo desplegado
```

**PUNTO DE CONTROL: Aprueba el timing y la estructura de la secuencia antes de escribir.**

---

## Fase 3: Escribir

### Email 1: El Recordatorio (1 hora después del abandono)

```
## Email 1: Recordatorio Suave

**Tiempo de envío:** 1 hora después del abandono del carrito
**Opciones de línea de asunto:**
1. "Dejaste algo atrás"
2. "¿Todavía lo estás pensando?"
3. "Tu carrito te espera"

**Texto de vista previa:** "Tu [nombre del producto] está reservado — completa tu pedido antes de que se vaya."

**Cuerpo:**

Hola [Nombre],

Parece que dejaste [nombre del producto] en tu carrito.

[IMAGEN DEL PRODUCTO: Muestra el/los artículo(s) exacto(s) que abandonaron]

Sin problemas — sucede. Tu carrito está guardado y listo cuando lo estés.

[BOTÓN CTA: "Completa Mi Pedido →"]

Si tuviste algún problema en el checkout, simplemente responde este email y te ayudaré.

[Despedida]

**Notas de diseño:**
- Imagen del producto mostrada prominentemente
- Botón CTA único
- Diseño limpio y minimalista
- Optimizado para móvil
```

### Email 2: Eliminador de Objeciones (24 horas)

```
## Email 2: Aborda la Indecisión

**Tiempo de envío:** 24 horas después del abandono
**Opciones de línea de asunto:**
1. "¿Todavía dudas sobre [producto]?"
2. "Aquí está lo que dicen los clientes de [producto]"
3. "Pregunta rápida sobre tu pedido"

**Texto de vista previa:** "[Fragmento de social proof — p.ej., '500+ clientes felices y contando']"

**Cuerpo:**

Hola [Nombre],

Noté que aún no completaste tu pedido. Totalmente comprensible — aquí hay algo que podría ayudarte a decidir:

[TESTIMONIAL: "Cita sobre el producto específico de un cliente real" — Nombre, Ubicación]

[Aborda la objeción principal:]
- Si es precio: "Esta es una inversión que se paga sola en [período/ahorros]"
- Si es envío: "Envío gratis en pedidos superiores a $[X]" o "Envía dentro de 24 horas"
- Si es confianza: "[Garantía] — pruébalo sin riesgo durante [X] días"

[IMAGEN DEL PRODUCTO]

[BOTÓN CTA: "Completa Mi Pedido →"]

[Incentivo ligero opcional: "Usa el código SAVE10 para 10% de descuento — solo para ti."]

[Despedida]
```

### Email 3: Última Oportunidad (48-72 horas)

```
## Email 3: Urgencia + Mejor Oferta

**Tiempo de envío:** 48-72 horas después del abandono
**Opciones de línea de asunto:**
1. "Última oportunidad: [X]% de descuento en tu carrito (vence hoy)"
2. "Tu carrito vence pronto — [incentivo] adentro"
3. "Recordatorio final + una oferta especial solo para ti"

**Texto de vista previa:** "Tu [incentivo] vence a medianoche."

**Cuerpo:**

Hola [Nombre],

Este es mi último recordatorio sobre tu carrito — después de hoy, [incentivo vence / carrito se borra / precio sube de nuevo].

[IMAGEN DEL PRODUCTO]

**Tu carrito:**
- [Nombre del producto] — $[precio]
- [Descuento aplicado]: -$[cantidad]
- **Tu precio: $[precio final]**

[BOTÓN CTA: "Obtén [X]% de Descuento Ahora →"]

[Elemento de urgencia: "Esta oferta vence a medianoche hoy."]

Si [nombre del producto] no es lo correcto para ti, sin resentimientos. Pero si estabas planeando comprar, ahora es el mejor momento.

[Despedida]

P.S. [Reafirma la garantía o beneficio clave una vez más]
```

### Timing y Escalada de Incentivos

```
## Timing de Secuencia

| Email | Timing | Incentivo | Tono |
|-------|--------|-----------|------|
| 1 | 1 hora después del abandono | Ninguno | Recordatorio útil |
| 2 | 24 horas | Ligero (10% de descuento o envío gratis) | Tranquilizador + social proof |
| 3 | 48-72 horas | Completo (mejor descuento + urgencia) | Urgencia + última oportunidad |

**Si solo son 2 emails:** Envía Email 1 a 1 hora, Email 3 a 48 horas.
**Si son 4 emails:** Añade un email de "educación del producto" entre Email 2 y 3 enfocado en beneficios y casos de uso.
```

### Directrices de Imagen de Producto

```
## Visualización de Producto

- Muestra el EXACTO artículo(s) en su carrito (contenido dinámico si tu plataforma de email lo soporta)
- Imagen de producto de alta calidad en fondo blanco o lifestyle
- Incluye precio y cualquier descuento visualmente
- Si es producto digital: muestra mockup (portada de ebook, captura de pantalla de dashboard, vista previa del curso)
- Una imagen de producto por email — no abrumes
```

---

## Fase 4: Pulir

### 1. Lista de Verificación de Secuencia

```
## Lista de Verificación de Secuencia de Carrito Abandonado

- [ ] Email 1 se envía dentro de 1 hora del abandono
- [ ] Las líneas de asunto son probables para A/B test (proporciona 2-3 opciones por email)
- [ ] La imagen del producto se muestra prominentemente en cada email
- [ ] El incentivo escala en la secuencia (ninguno → ligero → completo)
- [ ] Cada email tiene un único botón CTA
- [ ] Social proof aparece en al menos un email
- [ ] Garantía o inversión de riesgo se menciona
- [ ] La línea P.S. se incluye en el email final
- [ ] El elemento de urgencia tiene una fecha límite real
- [ ] Los emails son amigables para móvil (párrafos cortos, botón CTA grande)
- [ ] Enlace para desuscribirse incluido (cumplimiento)
```

### 2. Benchmarks de Tasa de Recuperación

```
## Qué Esperar

- Tasa promedio de recuperación de carrito de la industria: 5-15%
- Buena tasa de recuperación con esta secuencia: 10-20%
- Rastrear: tasas de apertura, tasas de clic e ingresos recuperados por email
- Prueba líneas de asunto con divisiones A/B en Email 1 (volumen más alto)
```

---

## Ejemplo: Recuperación de Carrito para un Curso Online de $97

```
Email 1 (1 hr): "Tu lugar en [Nombre del Curso] está reservado"
- Sin descuento, solo un recordatorio con imagen del curso y fragmento de testimonial

Email 2 (24 hrs): "Aquí está lo que los estudiantes de [Curso] están logrando"
- Dos testimoniales de estudiantes + código de descuento del 10%

Email 3 (72 hrs): "Última oportunidad — tu descuento del 15% vence hoy"
- Descuento completo + urgencia + reafirmación de garantía de devolución de dinero
- P.S. "500+ estudiantes inscritos. Únete a ellos sin riesgo."
```

---

## Anti-Patrones

- **Liderar con el descuento en Email 1** — entrena a los clientes para abandonar carritos por un descuento. Siempre comienza con un recordatorio sin incentivo.
- **Sin imagen de producto** — el cliente necesita ver lo que dejó atrás. Siempre muestra el producto.
- **Demasiados emails** — más de 4 emails de recuperación de carrito se siente agresivo. 3 es el punto dulce.
- **Líneas de asunto genéricas** — "Completa tu compra" es olvidadizo. Sé específico: incluye el nombre del producto o incentivo.
- **Sin urgencia en el email final** — "Compra cuando quieras" no da razón para actuar ahora. Establece una fecha límite real.
- **Enviar Email 1 demasiado tarde** — después de 4+ horas, la intención de compra se desvanece rápido. Envía dentro de 1 hora.

---

## Recuperación

- **La plataforma de email no soporta triggers de carrito:** Usa un proceso manual — exporta carritos abandonados diariamente y envía un email en lote.
- **Sin testimoniales disponibles:** Reemplaza el email de social proof con un email de beneficios del producto destacando los 3 resultados principales.
- **No puedes ofrecer descuentos:** Reemplaza el incentivo con una bonificación (plantilla gratis, módulo extra, prueba extendida) o enfatiza la garantía.
- **Bajas tasas de apertura:** Prueba líneas de asunto agresivamente. Intenta personalización (incluye el nombre del producto), curiosidad, o urgencia.
- **Los clientes dicen que abandonaron por un bug:** Primero arregla el flujo de checkout. Ninguna secuencia de email supera un carrito roto.
