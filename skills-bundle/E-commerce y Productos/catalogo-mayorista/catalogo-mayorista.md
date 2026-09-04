---
name: catalogo-mayorista
description: "Crea catálogos mayorista con listados producto, precios escalonados, MOQs e información ordenamiento para compradores retail."
allowed-tools: Read Write Glob
metadata:
  author: Imperio Digital
  version: "1.0"
---

# Catálogo Mayorista

## Cuándo Usar Este Skill

Usa este skill cuando necesites:
- Crear catálogo mayorista pitch productos minoristas
- Estructurar precios escalonados mínimos órdenes
- Escribir descripciones producto dirigidas decisiones compra B2B
- Construir proceso ordenamiento fácil minoristas compren

**NO USES** este skill para catálogos producto consumidor, páginas proveedor dropshipping o documentos inventario interno. Esto es materiales venta mayorista B2B.

---

## Principio Fundamental

UN CATÁLOGO MAYORISTA VENDE RENTABILIDAD AL MINORISTA — CADA DESCRIPCIÓN PRODUCTO, PUNTO PRECIO Y NOTA MARGEN DEBE RESPONDER: "¿SE VENDERÁ EN MI TIENDA Y ME HARÁ DINERO?"

---

## Fase 1: Resumen Catálogo

### Entradas Requeridas

| Entrada | Qué Preguntar | Predeterminado |
|-------|------------|---------|
| **Línea producto** | "¿Cuáles productos disponibles mayorista?" | Sin predeterminado |
| **Precio retail (MSRP)** | "¿Cuál es precio retail sugerido cada producto?" | Sin predeterminado |
| **Precios mayorista** | "¿Qué descuento mayorista ofreces — 50% off MSRP, escalonado, otro?" | 50% off MSRP |
| **MOQs mínimos** | "¿Cuáles son MOQs — por SKU y por orden?" | 12 unidades por SKU, mínimo $200 orden |
| **Minoristas objetivo** | "¿Qué tipo tiendas buscas — boutiques, specialty, chains?" | Boutiques independientes y tiendas specialty |

**PUNTO DE CONTROL:** Confirma lista producto, precios y MOQs antes construir catálogo.

---

## Fase 2: Estructura Catálogo

### Diseño Catálogo

```
## [Nombre Marca] Catálogo Mayorista — [Estación/Año]

### Tabla Contenidos
1. Historia Marca y Valores
2. Líneas Producto
3. Precios y MOQs
4. Información Ordenamiento
5. Envío y Términos
6. Contacto
```

### Introducción Marca (1 párrafo)

Escribe historia marca concisa respondiendo:
- ¿Qué haces y por qué?
- ¿Quién es cliente final?
- ¿Qué hace tus productos vender bien al retail?
- Incluye prensa notable, premios o alianzas retail

### Formato Listado Producto

Para cada producto:

```
### [Nombre Producto]
**SKU:** [Número SKU]
**MSRP:** $XX.XX
**Mayorista:** $XX.XX (XX% margen para minorista)
**MOQ:** XX unidades
**Variantes disponibles:** [Colores, tamaños, sabores]
**Dimensiones/Peso:** [Para cálculos envío]
**Puntos venta clave:** [2-3 bullets para personal ventas minorista]
**Estado bestseller:** [Sí/No — destaca top performers]
```

---

## Fase 3: Precios y Términos

### Tabla Precios Escalonados

```
## Tiers Precios Mayorista

| Tamaño Orden | Descuento off MSRP | Margen Minorista |
|-----------|-------------------|----------------|
| 12-47 unidades | 50% | 50% |
| 48-99 unidades | 55% | 55% |
| 100+ unidades | 60% | 60% |

**Mínimo orden apertura:** $200
**Mínimo reorden:** $100
**Términos pago:** Net 30 (después aprobación crédito) o prepago tarjeta crédito
```

### Políticas y Términos

Incluye estas secciones:
- **Términos pago** — Net 30, COD, opciones prepago
- **Envío** — quién paga, costos estimados, preferencias transportista
- **Daños y devoluciones** — política producto defectuoso, sin devoluciones artículos sin daño
- **Política MAP** — Requisitos Precio Anunciado Mínimo, si aplica
- **Exclusividad** — términos exclusividad territorial o online, si ofrecida

---

## Fase 4: Ordenamiento y Entrega

### Plantilla Formulario Orden

```
## Formulario Orden Mayorista

**Nombre minorista:** _______________
**Nombre contacto:** _______________
**Email:** _______________
**Dirección envío:** _______________
**Tax ID / Certificado resale #:** _______________

| SKU | Producto | Variante | Cant. | Precio Unit. | Total Línea |
|-----|---------|---------|-----|-----------|------------|
| | | | | | |

**Subtotal:** ___
**Envío:** ___
**Total:** ___

**Método pago:** [ ] Net 30  [ ] Tarjeta Crédito  [ ] Prepago
```

---

## Anti-Patrones

- **Descripciones enfocadas consumidor** — minoristas no se preocupan experiencia unboxing emocional. Les importa márgenes, sell-through y tasas reorden.
- **Sin MSRP listado** — minoristas necesitan ver su margen vista rápida. Siempre muestra mayorista y sugerido retail.
- **MOQs ocultos** — enterrar mínimos letra pequeña desperdicia tiempo todos. Declara claramente por adelantado.
- **Sin fotos producto** — compradores mayorista aún necesitan ver qué compran. Incluye shots producto limpios.
- **Ordenamiento demasiado complejo** — si colocar orden requiere llamada teléfono y tres formas, perderás compradores. Hazlo simple.

---

## Recuperación

- **Pushback minorista en precios:** Muestra matemática margen. Si 50% margen no suficiente, explora tiers volumen o bundles producto exclusivo mayorista.
- **Sin experiencia mayorista:** Comienza PDF catálogo simple y ordenamiento email directo. Actualiza portal online conforme creces.
- **Productos no adecuados mayorista:** No todos productos funcionan márgenes mayorista. Si COGS demasiado alto para 50% off MSRP, considera línea producto específica mayorista.
- **Pedidos iniciales bajos:** Ofrece trial libre-riesgo — orden apertura menor con proceso reorden fácil. Baja barrera primera compra.
- **Minorista quiere exclusividad:** Considera exclusividad territorial cambio compromisos compra mínimos anuales.
