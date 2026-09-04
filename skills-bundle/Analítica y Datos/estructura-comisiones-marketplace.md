---
name: estructura-comisiones-marketplace
description: "Diseña estructuras de comisiones para marketplace con modelos de comisión, niveles premium y análisis competitivo. Utiliza cuando establezca o reestructure precios para un negocio de plataforma."
allowed-tools: Read Write Glob
metadata:
  author: Imperio Digital
  version: "1.0"
---

# Estructura de Comisiones para Marketplace

## Cuándo Usar Este Skill

Utiliza este skill cuando necesites:
- Diseñar una estructura de comisiones para un marketplace bilateral
- Evaluar modelos de comisión, cuotas de listado y niveles de suscripción
- Analizar precios de competidores para encontrar la posición correcta en el mercado
- Crear niveles de vendedor premium con propuestas de valor claras

**NO** utilices este skill para precios de SaaS, precios de productos de e-commerce o modelado financiero. Esto es para diseño de comisiones de plataforma marketplace.

---

## Principio Fundamental

LAS COMISIONES DEL MARKETPLACE DEBEN SER LO SUFICIENTEMENTE BAJAS PARA QUE LOS VENDEDORES PERMANEZCAN EN LA PLATAFORMA Y LO SUFICIENTEMENTE ALTAS PARA CONSTRUIR UN NEGOCIO SOSTENIBLE — LA COMISIÓN NUNCA DEBE EXCEDER EL VALOR QUE CREA LA PLATAFORMA.

---

## Fase 1: Brief

### Entradas Requeridas

| Entrada | Qué Preguntar | Por Defecto |
|---------|--------------|------------|
| **Tipo de marketplace** | "¿Qué conecta tu marketplace?" | Sin valor por defecto — debe proporcionarse |
| **Valor de transacción promedio** | "¿Cuál es el monto de transacción típico?" | Sin valor por defecto — debe proporcionarse |
| **Volumen de transacciones** | "¿Cuántas transacciones por mes (actuales o proyectadas)?" | 100/mes proyectados |
| **Competidores** | "¿Quiénes son tus 3 principales competidores y qué cobran?" | Sin valor por defecto — investigación necesaria |
| **Comisiones actuales** | "¿Qué cobras ahora, si es que algo?" | Nada (pre-ingresos) |
| **Valor proporcionado** | "¿Qué hace la plataforma por los vendedores más allá de conectarlos con compradores?" | Pagos, descubrimiento, confianza |

**PUNTO DE CONTROL:** Confirma el brief antes de diseñar el modelo de comisiones.

---

## Fase 2: Opciones del Modelo de Comisiones

### Modelos Comunes de Comisiones para Marketplace

| Modelo | Cómo Funciona | Mejor Para |
|--------|-------------|----------|
| **Comisión** | % de cada transacción | Marketplaces de alto volumen, precio variable |
| **Cuota de listado** | Cuota fija por listado | Marketplaces de productos con muchos listados |
| **Suscripción** | Cuota mensual para acceso del vendedor | Marketplaces de servicios profesionales |
| **Freemium** | Básico gratuito + características premium pagas | Marketplaces construyendo oferta rápidamente |
| **Cuota por lead** | Cuota por lead o consulta calificada | Marketplaces de servicios con transacciones de alto valor |
| **Híbrido** | Combinación de lo anterior | Marketplaces maduros con necesidades de ingresos diversas |

### Guías de Tasa de Comisión

| Valor de Transacción | Comisión Típica | Fundamento |
|-------------------|-------------------|-----------|
| Menos de $50 | 15-25% | Tasa más alta necesaria para economía unitaria |
| $50-500 | 10-20% | Rango estándar para la mayoría de marketplaces |
| $500-5,000 | 5-15% | Tasa más baja para retener vendedores de alto valor |
| Más de $5,000 | 3-10% | Basado en volumen, vendedores son sensibles al precio |

### Quién Paga la Comisión

| Opción | Ventajas | Desventajas |
|--------|----------|-----------|
| El vendedor paga | Simple, común, oculto del comprador | Los vendedores incluyen la comisión en el precio |
| El comprador paga (cuota de servicio) | El vendedor obtiene el precio completo, transparente | Impacto de precio para el comprador |
| Dividido | Percepción justa | Complejo de comunicar |

**PUNTO DE CONTROL:** Confirma el modelo de comisión y rango de tasa antes de construir la estructura.

---

## Fase 3: Construir la Estructura de Comisiones

### Diseño de Comisión Base

Documenta la estructura de comisión principal:
- **Quién es cobrado:** Comprador, vendedor o ambos
- **Cuándo se cobra:** Al reservar, al completar o mensualmente
- **Tasa:** Cantidad fija, porcentaje o escalonada
- **Comisión mínima:** Cantidad piso por transacción (si aplica)
- **Procesamiento de pagos:** Quién absorbe el costo de procesamiento de 2.9% + $0.30

### Niveles de Vendedor Premium

Diseña 2-3 niveles para vendedores:

```
## Niveles de Vendedor

### Básico (Gratuito)
- Colocación de listado estándar
- [X]% de comisión por transacción
- Analítica básica
- Soporte estándar

### Profesional ($29/mes o comisión reducida)
- Colocación de listado prioritaria
- [X-3]% de comisión por transacción
- Seguimiento de conversiones y analítica avanzada
- Destacado en emails de compradores
- Soporte prioritario

### Empresa (Personalizado)
- Tasas de comisión personalizadas
- Gerente de cuenta dedicado
- Acceso a API
- Opciones de personal brandizadas
- Descuentos por volumen
```

### Plantilla de Análisis Competitivo

| Competidor | Comisión | Cuota de Listado | Suscripción | Otras Comisiones |
|-----------|----------|-------------|-----------|-----------|
| [Competidor 1] | | | | |
| [Competidor 2] | | | | |
| [Competidor 3] | | | | |
| **Tu Plataforma** | | | | |

**Estrategia de posicionamiento:** Precio por debajo del líder del mercado pero por encima de la opción más barata. Compite por valor, no por precio.

---

## Fase 4: Pulir

### 1. Comunicación de Comisiones

Escribe explicaciones claras de comisiones para:

**Orientado al vendedor:**
"Conservas [X]% de cada transacción. Cobramos una comisión de plataforma de [Y]% que cubre procesamiento de pagos, adquisición de compradores, resolución de disputas y mantenimiento de plataforma. Sin comisiones ocultas, sin sorpresas."

**Orientado al comprador (si aplica):**
"Se añade una pequeña cuota de servicio de [X]% a tu orden. Esto cubre pagos seguros, protección al comprador y atención al cliente."

**Entradas de FAQ:**
- ¿Cuándo se cobran las comisiones?
- ¿Cómo se calculan las comisiones en transacciones descontadas o reembolsadas?
- ¿Hay comisiones adicionales más allá de la comisión?
- ¿Cómo me actualizo a un nivel premium?

### 2. Proyecciones de Ingresos por Comisiones

Proporciona una plantilla de proyección simple:
```
Transacciones Mensuales: [X]
Valor Promedio de Transacción: $[Y]
Tasa de Comisión: [Z]%
Ingresos Brutos: X * Y * Z

Menos: Procesamiento de pagos (~2.9% + $0.30 por transacción)
Menos: Reembolsos y disputas (~2-5% de ingresos brutos)
Ingresos Netos de Plataforma: [Resultado]
```

### 3. Checklist de Calidad

```
## Checklist de Estructura de Comisiones

- [ ] Modelo de comisión seleccionado con fundamento
- [ ] Tasa de comisión comparada con 3+ competidores
- [ ] Quién paga (comprador, vendedor o dividido) está decidido y justificado
- [ ] Niveles de vendedor premium definidos con valor claro en cada nivel
- [ ] Comisión de transacción mínima establecida (si aplica)
- [ ] Costos de procesamiento de pagos contabilizados
- [ ] Texto de comunicación de comisiones escrito para vendedores y compradores
- [ ] FAQ cubre cálculo de comisiones, tiempo, reembolsos y actualizaciones
- [ ] Modelo de proyección de ingresos creado
- [ ] Comisión es sostenible (cubre costos + margen) en volumen proyectado
```

---

## Ejemplo

**Marketplace:** Servicios de diseño freelance
**Transacción promedio:** $750

**Estructura de comisiones:**
- 12% de comisión en vendedor (el vendedor recibe $660)
- 5% de cuota de servicio en comprador (el comprador paga $787.50)
- Ingresos totales de plataforma por transacción: $127.50
- Procesamiento de pagos absorbido por la plataforma

**Propuesta de nivel premium:**
"Hazte Pro por $49/mes: Reduce tu comisión de 12% a 8%. En tu proyecto promedio de $750, te ahorras $30 por transacción. Si completas 2+ proyectos al mes, Pro se paga solo."

---

## Anti-Patrones

- **Comisiones ocultas** — sorprender a los vendedores con comisiones inesperadas mata la confianza y genera contracargos. Sé transparente.
- **Cobrar antes de que se entregue valor** — cuotas de listado antes de cualquier venta desalienta la oferta. Los modelos basados en comisión alinean incentivos.
- **Carrera hacia cero** — competir solo en comisiones más bajas atrae vendedores sensibles al precio que se van cuando aparece una opción más barata.
- **Complicar los niveles** — más de 3 niveles crea confusión. Mantenlo simple.
- **Ignorar costos de procesamiento de pagos** — 2.9% + $0.30 por transacción se suma. Contabilízalo en tu modelo de ingresos.

---

## Recuperación

- **Los vendedores resisten la comisión:** Demuestra el valor — ¿qué proporciona la plataforma que justifique el costo? Si no puedes articularla, la comisión es demasiado alta.
- **Los compradores resisten cuotas de servicio:** Prueba absorber la comisión en la comisión del vendedor. Las comisiones ocultas se sienten peor que precios ligeramente más altos.
- **Los ingresos no cubren costos:** Aumenta el volumen (más transacciones) o aumenta la tasa de retención (comisión más alta). Aumentar comisiones en vendedores existentes requiere notificación previa y justificación.
- **El competidor subestima en precio:** Compite por valor, no por precio. Mejores vendedores, más compradores, características de confianza superiores justifican un premium.