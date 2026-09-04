---
name: estrategia-precios
description: "Desarrolla estrategias de precios con posicionamiento de mercado, análisis de valor percibido, y prueba de sensibilidad de precio. Usa cuando establecas o revises precios para productos o servicios."
allowed-tools: Read Write Glob
metadata:
  author: Imperio Digital
  version: "1.0"
---

# Estrategia de Precios

## Cuándo Usar Este Skill

Usa este skill cuando necesites:
- Establecer precios para un producto o servicio nuevo
- Evaluar y ajustar precios existentes
- Diseñar estructuras de precios en tiers o basadas en valor
- Analizar precios de competidor y posicionar tu oferta

**NO** uses este skill para crear tarjetas de tasa (usa tarjeta-tarifa-freelance), estructuras de comisión, o análisis de costos sin contexto de precios. Esto es para decisiones de precios estratégicos.

---

## Principio Fundamental

EL PRECIO ES UNA SEÑAL — COMUNICA VALOR, POSICIONA TU MARCA, Y DETERMINA QUIÉN ES TU CLIENTE. NUNCA ESTABLEZCA PRECIOS BASADOS ÚNICAMENTE EN COSTO.

---

## Fase 1: Entradas de Precios

### Información Requerida

| Entrada | Qué Preguntar | Por Defecto |
|---------|---------------|------------|
| **Producto/servicio** | "¿Qué estás cotizando?" | No hay predeterminado — debe proporcionarse |
| **Costo de entregar** | "¿Qué te cuesta entregar esto? (COGS, tiempo, materiales)" | No hay predeterminado — debe proporcionarse |
| **Cliente objetivo** | "¿Quién es el comprador ideal? (nivel de presupuesto, sofisticación)" | Solopreneurs y pequeños negocios |
| **Precios competidores** | "¿Qué cobran competidores por ofertas similares?" | Desconocido — investigaré |
| **Precio actual (si existe)** | "¿Qué estás cobrando ahora?" | Producto nuevo — sin precio actual |
| **Modelo de ingresos** | "¿Única vez, suscripción, retainer, o basado en uso?" | Compra única |

**PUNTO DE CONTROL: No procedas sin el producto, costo de entregar, y cliente objetivo.**

---

## Fase 2: Análisis de Precios

### Fundación Cost-Plus

```
## Análisis de Costo

| Componente | Costo |
|-----------|------|
| Costo directo (materiales, COGS, entrega) | $[X] |
| Costo de tiempo (horas x tarifa horaria) | $[X] |
| Asignación de gastos generales | $[X] |
| **Costo total de entregar** | **$[X]** |

| Markup | Precio | Margen |
|--------|--------|--------|
| 2x costo | $[X] | 50% |
| 3x costo | $[X] | 67% |
| 5x costo | $[X] | 80% |
```

### Precios Basados en Valor

```
## Análisis de Valor

| Elemento de Valor | Descripción | Valor Estimado para Cliente |
|--------------|-------------|---------------------------|
| Tiempo ahorrado | [Horas ahorradas x valor horario del cliente] | $[X] |
| Ingresos generados | [Impacto de ingresos esperado] | $[X] |
| Costo evitado | [Costos eliminados al usar producto] | $[X] |
| Riesgo reducido | [Problemas prevenidos] | $[X] |
| **Valor total entregado** | | **$[X]** |

**Rango de precio basado en valor:** 10-20% del valor total entregado = $[X] - $[X]
```

### Posicionamiento Competitivo

```
## Posicionamiento de Mercado

| Competidor | Precio | Posicionamiento |
|-----------|--------|-------------|
| [Comp 1] | $[X] | [Premium / Mid / Budget] |
| [Comp 2] | $[X] | [Premium / Mid / Budget] |
| [Comp 3] | $[X] | [Premium / Mid / Budget] |

**Tus opciones de posicionamiento:**
- **Premium (encima de mercado):** Requiere diferenciación, social proof, experiencia premium
- **Tasa de mercado (competitivo):** Seguro pero sin diferenciación, compite en características
- **Debajo de mercado (penetración):** Gana volumen rápido pero difícil de subir después, señala calidad inferior
```

---

## Fase 3: Estructura de Precios

### Modelo de Precios Recomendado

Elige y presenta la estructura correcta:

**Precio único:**
Mejor para: Productos simples, valor claro, compras de consideración baja

**Precios en Tiers (Bueno/Mejor/Mejor):**
Mejor para: SaaS, cursos, paquetes de servicio

**Suscripción:**
Precios mensuales vs anuales con descuento por compromiso anual (típicamente 15-20% descuento mensual)

**Pago por resultado:**
Precio vinculado a resultados entregados — captura de valor más alta, riesgo más alto

### Anclaje de Precio

- Presenta el tier más alto primero para anclar percepción
- El tier medio debe ser el objetivo — la mayoría de clientes lo elige
- Incluye un tier señuelo si es necesario para hacer el tier objetivo verse como mejor valor

---

## Anti-Patrones

- **Precio cost-plus únicamente** — tus costos son irrelevantes al comprador. Precio sobre valor entregado, no costo incurrido.
- **Copiar precios de competidor** — tu diferenciación debe justificar diferente precios. Copia el modelo, no el número.
- **Miedo a subir precios** — la mayoría de negocios subestiman precio. Si nadie se queja, probablemente sea muy bajo.
- **Demasiados tiers** — máximo 3 tiers. Más crea parálisis de decisión.
- **Nunca probar** — establece precio, pruébalo, ajusta. Los precios son iterativos, no permanentes.

---

## Recuperación

- **Sin datos de competidor:** Precio basado en análisis de valor. Usa regla de 10-20% del valor entregado como punto de partida.
- **Producto commodity (sin diferenciación):** Compite en experiencia, bundling, o garantías — no precio. O encuentra nicho donde puedas diferenciar.
- **Necesita aumento de precio en producto existente:** Grandfathering clientes existentes, aumento para nuevos clientes. Comunica valor agregado con el aumento.
- **Clientes dicen que es caro:** Esto es normal — 20-30% de prospectos deberían encontrarte caro. Si nadie lo hace, estás muy barato.
