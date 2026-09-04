---
name: plan-inventario-estacional
description: "Planifica inventario estacional con pronóstico demanda, cronogramas ordenamiento y estrategia liquidación para maximizar ingresos minimizar stock muerto."
allowed-tools: Read Write Glob
metadata:
  author: Imperio Digital
  version: "1.0"
---

# Plan Inventario Estacional

## Cuándo Usar Este Skill

Usa este skill cuando necesites:
- Planificar compras inventario próxima temporada vendedora
- Pronosticar demanda basada ventas históricas y tendencias mercado
- Crear cronogramas ordenamiento contabilizando lead times proveedor
- Diseñar estrategias liquidación final temporada para minimizar stock muerto

**NO USES** este skill para gestión inventario perpetuo, adquisiciones materias primas o negocios servicios sin productos físicos.

---

## Principio Fundamental

ORDENA BASADO EN DATOS, NO OPTIMISMO — OVERSTOCK MATA FLUJO EFECTIVO Y UNDERSTOCK MATA INGRESOS. EL MEJOR PLAN ESTACIONAL BALANCEA AMBOS RIESGOS.

---

## Fase 1: Definición Temporada

### Entradas Requeridas

| Entrada | Qué Preguntar | Predeterminado |
|-------|------------|---------|
| **Temporada / evento** | "¿Qué temporada o evento planificando?" | Sin predeterminado |
| **Categorías producto** | "¿Cuáles líneas producto son estacionales?" | Sin predeterminado |
| **Datos históricos** | "¿Tienes datos ventas temporada pasada? Comparte números o estimaciones." | Sin datos previos |
| **Lead times proveedor** | "¿Qué tan adelantado necesitas ordenar?" | 6-8 semanas |
| **Presupuesto** | "¿Cuál es presupuesto inventario total temporada?" | Sin predeterminado |

### Resumen Temporada Brief

```
## Resumen Inventario Estacional

**Temporada:** Vacaciones 2024 (1 nov - 31 dic)
**Productos clave:** Conjuntos velas regalo, cerillas aromatizadas, holders cerámicos
**Ingresos año pasado:** $28,000 en 3 líneas producto
**Objetivo crecimiento:** Aumento 30% ($36,400)
**Lead time proveedor:** 8 semanas (ordenar antes 1 sep)
**Presupuesto:** $12,000 inventario
```

**PUNTO DE CONTROL:** Confirma resumen temporada antes construir pronóstico.

---

## Fase 2: Pronóstico Demanda

### Método Pronóstico

1. **Pronóstico base** — usa ventas unitarias año pasado como punto partida
2. **Ajuste crecimiento** — aplica tasa crecimiento basada aumento audiencia, gasto marketing, tendencias mercado
3. **Mix producto** — asigna porcentajes entre categorías basado rendimiento histórico
4. **Stock seguridad** — agrega buffer 15-20% para top sellers, 0% para productos no probados

### Plantilla Pronóstico

```
## Pronóstico Demanda

| Producto | Unidades Año Pasado | Factor Crecimiento | Unidades Pronóstico | Stock Seguridad | Cantidad Orden |
|---------|-----------------|---------------|------------------|--------------|-----------|
| Conjunto vela grande | 120 | 1.3x | 156 | +20% (31) | 187 |
| Conjunto vela pequeño | 200 | 1.3x | 260 | +15% (39) | 299 |
| Cerillas aromatizadas 6-pack | 340 | 1.2x | 408 | +15% (61) | 469 |
| Holder cerámica (nuevo) | 0 | N/A | 80 | 0% | 80 |
```

---

## Fase 3: Cronograma Ordenamiento

### Plantilla Cronograma

Mapea cada milestone hacia atrás desde primer día vendedor:

```
## Cronograma Ordenamiento

**Inicio temporada:** 1 noviembre
**Fechas clave hacia atrás:**

| Fecha | Acción |
|------|--------|
| 15 julio | Finaliza línea producto y cantidades |
| 1 agosto | Ordena con proveedores, coloca compras mayorista |
| 1 sep | Recibe y verifica inventario |
| 15 sep | Fotografía producto y actualiza listados |
| 1 oct | Comienza marketing pre-temporada (email, redes) |
| 15 oct | Venta acceso temprano clientes VIP |
| 1 nov | Lanzamiento temporada completo |
| 15 dic | Monitorea niveles stock — reorden bestsellers posible |
| 26 dic | Comienza precios liquidación |
| 15 ene | Liquidación final — mueve stock restante |
```

---

## Fase 4: Estrategia Liquidación y Post-Temporada

### Cronograma Markdown

```
## Plan Liquidación

| Timing | Descuento | Objetivo |
|--------|----------|------|
| Últimas 2 semanas temporada | 20% off | Mueve slow sellers antes fin temporada |
| 1 semana post-temporada | 30-40% off | Limpia stock seasonal restante |
| 2-3 semanas post-temporada | 50%+ off o bundles | Liquida stock muerto |
| 4+ semanas post-temporada | Dona, repurposea o guarda próximo año | Cero costo carrying |
```

---

## Anti-Patrones

- **Ordenamiento basado esperanza** — "Creo será enorme" sin datos lleva overstock. Usa números.
- **Ignorar lead times** — ordenamiento tarde significa agotamientos pico demanda.
- **Sin plan liquidación** — mantener inventario estacional pasada ventana agota efectivo y almacenamiento.
- **Over-diversificar SKUs** — demasiados productos dispersan presupuesto inventario. Enfócate winners comprobados.
- **Saltar revisión post-temporada** — sin documentar qué pasó, repetirás mismos errores.

---

## Recuperación

- **Sin datos históricos:** Usa investigación competidor, Google Trends y órdenes prueba pequeñas construir baseline. Planifica conservadoramente.
- **Proveedor no puede cumplir cronograma:** Encuentra proveedores backup, reduce cantidades orden o cambia alternativas envío más rápidas.
- **Presupuesto demasiado pequeño para pronóstico:** Prioriza bestsellers, corta productos no probados y planifica lanzamiento más pequeño con triggers reorden.
- **Agotamiento mid-temporada:** Source localmente posible, ofrece pre-órdenes restock e re-dirige marketing productos en stock.
- **Exceso inventario post-temporada:** Implementa plan liquidación inmediatamente — no esperes esperando venda precio completo próxima temporada.
