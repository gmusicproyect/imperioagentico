---
name: estrategia-descuentos
description: "Planifica campañas de precios promocionales con tipos de descuento, timing, guardarraíles seguros de margen, y calendarios de promoción. Úsalo cuando un usuario quiere ejecutar una venta, crear oferta promocional, o planear descuentos estacionales sin destruir márgenes de ganancia."
allowed-tools: Read Write Glob
metadata:
  author: Imperio Digital
  version: "1.0"
---

# Estrategia de Descuentos

## Cuándo Usar Este Skill

- Usuario quiere ejecutar venta o campaña de precios promocionales
- Usuario necesita elegir entre tipos de descuento
- Usuario está planeando promociones estacionales o de vacaciones
- Usuario está preocupado por descontar demasiado agresivamente y dañar márgenes

## Principio Fundamental

NUNCA DESCUENTES SIN UN FLOOR DE MARGEN — CADA PROMOCIÓN DEBE TENER UN UMBRAL DE GANANCIA MÍNIMO CALCULADO ANTES DEL LANZAMIENTO.

## Workflow

### Fase 1: Entiende la Economía de Negocio

1. Reúne números baseline:
   - Punto de precio del producto/servicio
   - Costo de bienes vendidos (COGS) o costo de entrega de servicio
   - Porcentaje de margen bruto actual
   - Valor promedio de orden (AOV)
   - Ingresos y volumen mensual

2. Calcula el floor de margen

3. **PUNTO DE CONTROL: Si margen bruto está bajo 30%, recomienda promociones de valor-añadido (bonuses, bundles) en lugar de cortes de precio**

### Fase 2: Selecciona Tipo de Descuento

| Tipo de Descuento | Mejor Para | Impacto en Margen | Ejemplo |
|------------------|----------|-------------------|---------|
| Porcentaje off | Liquidar inventario, ventas estacionales | Medio-Alto | 20% off todos |
| Cantidad en dólares off | Productos AOV más alto | Medio | $15 off órdenes >$75 |
| Descuento en bundle | Aumentar AOV | Bajo | Compra 3, obtén 15% off |
| BOGO/Gift with purchase | Mover stock lento | Medio | Compra shampoo, obtén travel size gratis |
| Free shipping threshold | Aumentar AOV | Bajo | Envío gratis órdenes >$50 |
| Early-bird pricing | Lanzamientos, cursos | Bajo | $197 primeros 50 (regular $297) |
| Tiered discount | Bulk/wholesale | Bajo-Medio | 10% off 2+, 15% off 4+, 20% off 6+ |
| Flash limitado en tiempo | Urgencia, activación de lista | Alto | 40% off 24 horas |

## Anti-Patrones

- **NUNCA recomiendes descuento que caiga margen bruto bajo 20%** — este es el floor absoluto para negocio sostenible
- No recomiendes descuentos porcentaje-off mayores a 40% a menos que liquides inventario muerto
- Toda promoción debe tener fecha final dura — sin ventas abiertas-indefinidas
- No recomiendes descuento stacking a menos que usuario explícitamente lo solicite
- Siempre calcula volumen de punto de equilibrio antes de recomendar cualquier corte de precio
- Desalienta descuentos site-wide porcentaje para negocios de servicios — desvalorizan experiencia
- Advierte si usuario está ejecutando promociones más frecuentes que cada 3 semanas

## Recuperación

- Usuario no sabe su COGS: Ayuda estimar — para productos físicos suma materiales + packaging + envío; para servicios usa tarifa horaria x tiempo; para productos digitales usa solo tarifas de plataforma
- Margen bruto bajo 30%: Pivotea a promociones de valor-añadido en lugar de cortes de precio
