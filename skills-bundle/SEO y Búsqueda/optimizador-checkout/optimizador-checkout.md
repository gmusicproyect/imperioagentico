---
name: optimizador-checkout
description: Audita flujos de pago en tiendas de comercio electrónico y recomienda mejoras para reducir fricciones y aumentar las tasas de conversión. Usa este skill cuando un usuario tenga problemas de abandono de carrito, bajas tasas de finalización de compra o quiera optimizar el flujo de compra de su tienda en línea.
allowed-tools: Read Write Bash(ls) WebFetch
author: Imperio Digital
version: "1.0"
---

# Optimizador de Checkout

## Cuándo Usar Este Skill

- El usuario reporta altas tasas de abandono de carrito (promedio de la industria es ~70%)
- El usuario quiere mejorar la tasa de finalización de compra o la tasa de conversión
- El usuario está lanzando una nueva tienda y quiere las mejores prácticas de checkout
- El usuario está cambiando de plataforma de comercio electrónico y necesita diseñar el flujo de pago
- El usuario nota caídas en un paso específico de su funnel de checkout

## Principio Fundamental

CADA CAMPO ADICIONAL, CLIC O PÁGINA EN EL CHECKOUT ES UNA RAZÓN PARA IRSE — ELIMINA TODO LO QUE NO COMPLETE DIRECTAMENTE LA COMPRA.

## Workflow

### Fase 1: Recopilar Estado Actual

1. Identifica la plataforma de comercio electrónico (Shopify, WooCommerce, Squarespace, personalizada)
2. Obtén métricas actuales si están disponibles:
   - Tasa de abandono de carrito
   - Tasa de finalización de checkout
   - Valor de pedido promedio
   - Páginas de salida principales en el embudo
3. Mapea los pasos actuales del checkout (cuántas páginas/pasos hay desde el carrito hasta la confirmación)
4. Lista todos los campos de formulario actualmente requeridos

### Fase 2: Auditar Contra Lista de Fricciones

5. Califica el checkout contra estos 15 puntos de fricción:

| # | Punto de Fricción | Impacto | Estado |
|---|---------------|--------|--------|
| 1 | Checkout de invitado disponible (sin creación de cuenta forzada) | CRÍTICO | |
| 2 | Checkout de una sola página o acordeón (no multipágina) | ALTO | |
| 3 | Solo campos de formulario esenciales (nombre, correo, dirección, pago) | ALTO | |
| 4 | Auto-relleno habilitado para campos de dirección y pago | ALTO | |
| 5 | Opciones de pago express (Apple Pay, Google Pay, PayPal) | ALTO | |
| 6 | Resumen de pedido visible durante todo el checkout | MEDIO | |
| 7 | Costos de envío mostrados antes del checkout (sin tarifas sorpresa) | CRÍTICO | |
| 8 | Insignias de confianza visibles (SSL, logos de pago, garantía) | MEDIO | |
| 9 | Indicador de progreso mostrando el paso actual | MEDIO | |
| 10 | Optimizado para móvil (objetivos de toque grandes, sin desplazamiento horizontal) | CRÍTICO | |
| 11 | Mensajes de error intercalados y específicos (no en la parte superior de la página) | MEDIO | |
| 12 | Campo de código promocional contraído (no mostrado prominentemente) | BAJO | |
| 13 | Persistencia del carrito (artículos guardados si el usuario se va y regresa) | ALTO | |
| 14 | Política de devolución e información de contacto accesible desde checkout | MEDIO | |
| 15 | Página de confirmación con número de pedido y próximos pasos | BAJO | |

6. **PUNTO DE CONTROL: Cualquier elemento CRÍTICO marcado como fallido debe ser la recomendación principal**

### Fase 3: Generar Recomendaciones

7. Produce una lista de correcciones priorizada, ordenada por impacto:
   - Prioridad 1 (hacer inmediatamente): Puntos de fricción CRÍTICOS que están fallando
   - Prioridad 2 (hacer esta semana): Puntos ALTOS que están fallando
   - Prioridad 3 (hacer este mes): Elementos MEDIO y BAJO

8. Para cada recomendación, proporciona:
   - El cambio específico a realizar
   - Cómo implementarlo en su plataforma
   - Impacto esperado (con rango de mejora de conversión realista)

### Fase 4: Recuperación de Carrito Abandonado

9. Si el abandono de carrito es la preocupación principal, añade una secuencia de recuperación:
   - Email 1 (1 hora después del abandono): Recordatorio de carrito con imágenes de productos
   - Email 2 (24 horas): Destacar social proof o reseñas
   - Email 3 (72 horas): Último empujón con incentivo pequeño (envío gratis o 10% de descuento)

10. Proporciona plantillas de correo para cada contacto

### Fase 5: Entregar

11. Genera el cuadro de mando de auditoría completo
12. Genera recomendaciones priorizado con pasos de implementación
13. Si es aplicable, genera la secuencia de correos de carrito abandonado

## Ejemplo 1: Tienda Shopify que Vende Joyas Hechas a Mano

**Estado actual:**
- Plataforma: Shopify
- Abandono de carrito: 78%
- Checkout: Checkout de 3 páginas (información, envío, pago)
- Campos de formulario: 14 campos incluyendo teléfono, nombre de empresa, apto/suite
- Sin checkout de invitado (requiere cuenta)
- Sin opciones de pago express
- Los costos de envío solo se muestran en la página 2

**Cuadro de Mando de Auditoría:**

| # | Punto de Fricción | Estado | Notas |
|---|---------------|--------|-------|
| 1 | Checkout de invitado | FALLAR | Se requiere cuenta — corrección principal |
| 2 | Checkout de una sola página | FALLAR | Actualmente 3 páginas |
| 3 | Solo campos esenciales | FALLAR | 14 campos, deberían ser 8 |
| 4 | Auto-relleno habilitado | PASAR | Valor por defecto de Shopify |
| 5 | Pagos express | FALLAR | Sin Apple Pay, Google Pay o PayPal |
| 6 | Resumen de pedido visible | PASAR | Resumen de barra lateral en escritorio |
| 7 | Costos de envío pre-checkout | FALLAR | Oculto hasta la página 2 |
| 8 | Insignias de confianza | FALLAR | Sin insignias visibles |
| 9 | Indicador de progreso | PASAR | Migas de pan predeterminadas de Shopify |
| 10 | Optimizado para móvil | PASAR | Responsive predeterminado de Shopify |
| 11 | Mensajes de error intercalados | PASAR | Valor por defecto de Shopify |
| 12 | Campo de código promocional contraído | FALLAR | Campo prominente causando salida para buscar códigos |
| 13 | Persistencia del carrito | PASAR | Valor por defecto de Shopify |
| 14 | Política de devolución accesible | FALLAR | Sin enlace en checkout |
| 15 | Página de confirmación | PASAR | Shopify estándar |

**Puntuación: 7/15 pasando**

**Recomendaciones Priorizado:**

**Prioridad 1 — Hacer inmediatamente:**

1. **Habilitar checkout de invitado**
   - Shopify Admin > Configuración > Checkout > Cuentas de cliente > "Las cuentas son opcionales"
   - Impacto esperado: 5-10% de reducción en abandono

2. **Mostrar costos de envío en páginas de producto o carrito**
   - Añade widget de calculadora de envío a la página de carrito
   - O usa envío de tarifa plana y muéstralo en páginas de producto: "Envío de tarifa plana $5.95"
   - Impacto esperado: 8-12% de reducción en abandono

3. **Habilitar opciones de pago express**
   - Shopify Admin > Configuración > Pagos > Habilitar Shopify Payments (incluye Apple Pay, Google Pay)
   - Añade PayPal Express como opción secundaria
   - Impacto esperado: 3-7% de aumento en conversiones móviles

**Prioridad 2 — Hacer esta semana:**

4. **Eliminar campos de formulario innecesarios**
   - Elimina: Nombre de empresa, Apto/Suite (haz opcional), Teléfono (haz opcional)
   - Mantén: Correo, Nombre, Apellido, Dirección, Ciudad, Estado, ZIP, País
   - Shopify Admin > Configuración > Checkout > Opciones de formulario
   - Impacto esperado: 2-4% de mejora en tasa de finalización

5. **Contraer el campo de código promocional**
   - Usa el toggle "Mostrar campo de código de descuento" de Shopify o una solución CSS personalizada para contraerlo detrás de un enlace "¿Tienes un código?"
   - Impacto esperado: Reduce salidas de usuarios que se van a buscar códigos de descuento

**Prioridad 3 — Hacer este mes:**

6. **Añade insignias de confianza** — logos de métodos de pago e insignia "Checkout Seguro" cerca del botón de pago
7. **Añade enlace de política de devolución** — enlace de pie de página en checkout a tu página de devoluciones
8. **Cambia a checkout de una sola página** — Shopify ahora ofrece checkout de una página para todos los planes

## Ejemplo 2: Tienda WooCommerce que Vende Café Especial

**Estado actual:**
- Plataforma: WooCommerce
- Abandono de carrito: 72%
- Checkout: Una sola página (valor por defecto de WooCommerce)
- 11 campos de formulario
- Checkout de invitado habilitado
- Sin pagos express
- Envío gratis en umbral de $50 pero no comunicado hasta el carrito

**Puntuación de Auditoría: 9/15 pasando**

**Top 3 Recomendaciones:**

1. **Añade pago express (Stripe + PayPal Express)**
   - Instala el plugin WooCommerce Stripe Gateway
   - Habilita Apple Pay y Google Pay en el dashboard de Stripe
   - Añade plugin WooCommerce PayPal Checkout para botones PayPal Express
   - Coloca botones de pago express encima del formulario estándar
   - Impacto esperado: 4-8% de mejora en conversión móvil

2. **Mostrar progreso de envío gratis en páginas de producto y carrito**
   - Añade un banner: "Envío gratis en pedidos sobre $50 — ¡te faltan $XX!"
   - Usa el plugin "Free Shipping Progress Bar" o añade código personalizado a la página de carrito
   - Impacto esperado: 10-15% de aumento en AOV para pedidos entre $30-$49

3. **Reduce campos de formulario de 11 a 7**
   - Elimina: Empresa, Teléfono (o haz opcional), Notas de pedido
   - Combina Nombre/Apellido en un solo campo "Nombre Completo" si es posible
   - Impacto esperado: 2-3% de mejora en tasa de finalización

**Recuperación de Carrito Abandonado — Email 1 (1 hora):**

```
Asunto: Dejaste un excelente café atrás

Hola [Nombre],

Parece que estabas checando nuestro [Nombre del Producto] pero no terminaste tu pedido.

Sin preocupaciones — tu carrito está guardado y listo cuando tú estés.

[CONTENIDOS DE CARRITO CON IMAGEN DE PRODUCTO]
[Nombre del Producto] — [Tamaño] — $XX.XX

Completa Tu Pedido → [Botón enlazando al carrito guardado]

¿Preguntas sobre nuestro café? Solo responde este correo — somos personas reales que amamos hablar de café.

Saludos,
El Equipo de Summit Roasters

P.S. Los pedidos sobre $50 tienen envío gratis.
```

## Recuperación y Fallback

- Si el usuario no puede proporcionar métricas actuales, usa puntos de referencia de la industria: 70% de abandono de carrito es promedio, 3% de conversión de checkout es típico para pequeño comercio electrónico
- Si el usuario está en una plataforma que limita la personalización del checkout (como Squarespace básico), enfócate en lo que se puede cambiar: pagos express, reducción de campos y mejoras pre-checkout
- Si la auditoría revela que el checkout ya está bien optimizado (12+ pasando), cambia el enfoque a fricción pre-checkout: claridad de página de producto, comunicación de envío y diseño de página de carrito
- Si el usuario carece de capacidad técnica para implementar cambios, prioriza cambios de configuración nativos de plataforma sobre soluciones de código personalizado

## Restricciones

- No recomiendes eliminar correo del checkout — es requerido para confirmación de pedido y recibos
- No recomiendes eliminar campos de dirección para tiendas de productos físicos
- Los estimados de mejora de conversión deben darse como rangos, no números exactos
- No recomiendes aplicaciones o plugins específicos sin confirmar compatibilidad de plataforma
- Nunca sugierais patrones oscuros (tarifas ocultas, upsells forzados bloqueando checkout, opt-outs confusos)
- Todas las recomendaciones deben ser implementables sin un desarrollador a menos que se indique lo contrario
- Enfócate en los 3-5 cambios con mayor impacto, no una lista exhaustiva de 20 ajustes menores
