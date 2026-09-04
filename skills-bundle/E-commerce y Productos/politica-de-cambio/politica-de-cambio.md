---
name: politica-de-cambio
description: "Escribe políticas de cambio con criterios de elegibilidad, pasos de proceso, plantillas de comunicación del cliente y manejo de excepciones."
allowed-tools: Read Write Glob
metadata:
  author: Imperio Digital
  version: "1.0"
---

# Política de Cambio

## Cuándo Usar Este Skill

Usa este skill cuando necesites:
- Escribir una política de cambio clara para tu tienda de e-commerce
- Diseñar el workflow del proceso de cambio de solicitud a resolución
- Crear plantillas de comunicación del cliente para escenarios de cambio
- Establecer directrices de manejo de excepciones para casos fronterizos

**NO USES** este skill para políticas de reembolso, reclamaciones de garantía o capacitación de servicio al cliente. Esto es para políticas y procesos de cambio de producto específicamente.

---

## Principio Fundamental

UNA BUENA POLÍTICA DE CAMBIO MANTIENE LOS INGRESOS Y AL CLIENTE — HACER CAMBIOS MÁS FÁCIL QUE DEVOLVER Y LOS CLIENTES ELEGIRÁN QUEDARSE.

---

## Fase 1: Resumen

### Entradas Requeridas

| Entrada | Qué Preguntar | Predeterminado |
|-------|------------|---------|
| **Tipos de producto** | "¿Qué productos son elegibles para cambio? (todos, solo prendas, categorías específicas)" | Todos los productos |
| **Ventana de cambio** | "¿Cuántos días después de la compra pueden cambiar los clientes?" | 30 días |
| **Requisitos de condición** | "¿Deben estar sin usar, sin ponerse, con etiquetas?" | Sin usar, empaque original |
| **Tipos de cambio** | "¿Mismo producto diferente tamaño/color, o cambio por producto diferente?" | Mismo producto, variante diferente |
| **Costo de envío** | "¿Quién paga cambio de envío? (cliente, empresa, dividir)" | Empresa paga |
| **Pain points actuales** | "¿Qué problemas de cambio manejas más?" | Cambios de tamaño, proceso lento |
| **Plataforma** | "¿Plataforma de e-commerce? (Shopify, WooCommerce, etc.)" | Shopify |

**PUNTO DE CONTROL:** Confirma resumen antes de escribir la política.

---

## Fase 2: Diseño

### Marco de Política de Cambio

1. **Elegibilidad** — qué puede cambiarse, qué no
2. **Período de tiempo** — días desde compra o entrega
3. **Condición** — condición de producto requerida para cambio
4. **Proceso** — cómo iniciar y completar un cambio
5. **Envío** — quién paga, cómo se proporcionan etiquetas
6. **Excepciones** — artículos en venta, personalizados, venta final
7. **Tiempo de procesamiento** — cuánto tiempo desde recepción hasta nuevo envío

### Workflow de Cambio

```
Cliente solicita cambio → Equipo revisa elegibilidad →
Aprobado: se envía etiqueta prepago → Cliente envía artículo →
Se recibe e inspecciona artículo → Se envía nuevo artículo →
Se envía rastreo al cliente → Cambio completado
```

**PUNTO DE CONTROL:** Presenta el marco de política para aprobación antes de escribir el documento completo.

---

## Fase 3: Construir

### Entregables

**1. Política de Cambio Frente al Cliente**
- Política en lenguaje simple para el sitio web
- Organizada con encabezados claros (Qué, Cuándo, Cómo, Excepciones)
- Sección FAQ respondiendo las 5 preguntas principales sobre cambios
- Proceso de cambio paso a paso (numerado, sin ambigüedad)

**2. SOP de Cambio Interno**
- Proceso paso a paso para el equipo que maneja cambios
- Árbol de decisiones para evaluación de elegibilidad
- Criterios de inspección para artículos recibidos
- Gestión de inventario (retorna artículo cambiado a stock o descuenta)

**3. Plantillas de Comunicación del Cliente**
- Email de reconocimiento de solicitud de cambio
- Email de cambio aprobado (con etiqueta e instrucciones)
- Email de cambio denegado (con razón y alternativas)
- Email de confirmación de nuevo artículo enviado
- Email de seguimiento de cambio completado

**4. Guía de Manejo de Excepciones**
| Escenario | Política | Acción |
|----------|--------|--------|
| Artículo fuera de ventana de cambio | Denegar si supera 45 días, considerar si 31-45 | Discreción del gerente |
| Artículo usado/dañado por cliente | Denegar cambio | Ofrecer descuento en compra nueva |
| Artículo agotado en tamaño solicitado | Ofrecer alternativa o crédito tienda | Cliente elige |
| Cambio internacional | Cliente paga envío retorno | Proporciona guía aduanal |
| Cambio de regalo (sin recibo) | Cambio por crédito tienda a precio actual | Verifica que producto se venda |

---

## Fase 4: Pulir

### Colocación de Política

- Enlaza prominentemente desde páginas de producto, carrito y navegación del pie
- Incluye resumen de política de cambio en email de confirmación de orden
- Agrega a página de FAQ y base de conocimiento de servicio al cliente

### Medición

Rastrear mensualmente:
- Volumen de solicitud de cambio (como % de órdenes)
- Razones principales de cambio (tamaño, color, defecto, preferencia)
- Tasa de finalización de cambio (iniciado vs. completado)
- Tiempo para resolver (solicitud a nuevo artículo entregado)
- Retención post-cambio (¿compran clientes de cambio de nuevo?)

### Revisión de Política

- Trimestral: revisa datos de cambio y ajusta política para problemas recurrentes
- Estacionalmente: ajusta para cambios de regalo de temporada (ventana extendida en dic-ene)
- Al disparo: actualiza cuando agregues nuevas categorías de producto o vendas internacionalmente

---

## Ejemplo 1: Marca de Prendas (Cambios de Tamaño)

**Política:** Cambios gratis dentro de 30 días de entrega. Los artículos deben estar sin ponerse con etiquetas adheridas. Se proporciona etiqueta de retorno prepago. Nuevo tamaño enviado dentro de 2 días hábiles de recibir la devolución. Ventana de cambio extendida a 60 días durante temporada de vacaciones (15 nov - 15 ene).

## Ejemplo 2: Tienda de Artículos para el Hogar (Cambios de Producto)

**Política:** Cambios dentro de 14 días de entrega para artículos de igual valor o mayor (cliente paga diferencia). Los artículos deben estar sin usar y en empaque original. Cliente paga envío de retorno. Cambios procesados dentro de 5 días hábiles.

---

## Anti-Patrones

- **Oculta o difícil de encontrar** — una política enterrada en letra pequeña crea clientes frustrados que llaman al soporte. Hazla visible y fácil de encontrar.
- **Demasiado restrictiva** — "Sin cambios bajo ninguna circunstancia" pierde clientes y genera rechazos. Algo de flexibilidad construye lealtad.
- **Demasiado generosa sin rastreo** — cambios ilimitados sin rastreo habilita abuso. Monitorea patrones.
- **Procesamiento lento** — un proceso de cambio de 3 semanas hace que los clientes deseen haber devuelto y recomprado. La velocidad construye confianza.
- **Hacer cambios más difícil que devoluciones** — si devolver para reembolso es más fácil que cambiar, los clientes elegirán el reembolso. Haz cambios el camino de menor resistencia.

---

## Recuperación

- **Tasa alta de cambio en un producto:** Investiga la causa raíz. Si el problema es tamaño, mejora la guía de tamaños. Si es calidad, aborda el producto.
- **Cliente quiere cambio pero fuera de ventana:** Usa criterio. Un cliente en día 35 de ventana 30 días que es cortés y leal merece una excepción. Documenta la excepción.
- **Artículo de cambio está agotado:** Ofrece crédito tienda, producto alternativo o reembolso. Nunca dejes al cliente en espera de restock.
- **Preocupaciones de fraude:** Rastrea patrones de cambio por cliente. Señala cuentas con frecuencia de cambio inusualmente alta para revisión. Implementa verificación para cambios de alto valor.
