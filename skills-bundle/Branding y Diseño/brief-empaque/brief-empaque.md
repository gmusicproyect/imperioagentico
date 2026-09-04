---
name: brief-empaque
description: "Escribe briefs de diseño de empaque de producto con consideraciones de dimensiones, materiales, jerarquía de mensajería, requisitos de cumplimiento y especificaciones de vendedor. Úsalo cuando diseñes empaque físico."
allowed-tools: Read Write Glob
metadata:
  author: Imperio Digital
  version: "1.0"
---

# Brief de Empaque

## Cuándo Usar Este Skill

Usa este skill cuando necesites:
- Hacer un brief a un diseñador sobre empaque de producto para un producto físico
- Definir requisitos de empaque incluyendo dimensiones, materiales y mensajería
- Planificar empaque para un lanzamiento de producto de e-commerce
- Crear especificaciones para un fabricante de empaque

**NO** uses este skill para empaque de producto digital, logística de caja de envío o procesos de cumplimiento de almacén. Esto es para diseño de empaque de producto de cara al consumidor.

---

## Principio Fundamental

EL EMPAQUE ES TU ÚLTIMO VENDEDOR — DEBE COMUNICAR TU PROPUESTA DE VALOR, DIFERENCIARTE DE COMPETIDORES Y CREAR UNA IMPRESIÓN POSITIVA EN MENOS DE 3 SEGUNDOS.

---

## Fase 1: Brief

### Entradas Requeridas

| Entrada | Qué Preguntar | Predeterminado |
|---------|------------|---------|
| **Producto** | "¿Qué producto necesita empaque?" | Debe ser proporcionado |
| **Dimensiones** | "¿Dimensiones del producto y peso?" | Debe ser proporcionado |
| **Retail o DTC** | "¿Dónde se venderá? (estante retail, DTC en línea, ambos)" | DTC en línea |
| **Directrices de marca** | "¿Tienes colores, fuentes y archivos de logo de marca?" | Debe ser proporcionado o referenciar guía-identidad-marca |
| **Presupuesto por unidad** | "¿Costo objetivo de empaque por unidad?" | $1-3 por unidad |
| **Cantidad** | "¿Tamaño de la primera corrida de producción?" | 500-1,000 unidades |
| **Sostenibilidad** | "¿Requisitos de sostenibilidad? (reciclable, compostable, mínimo)" | Reciclable preferido |
| **Cumplimiento** | "¿Algún texto requerido, certificaciones o códigos de barras?" | Info básica de producto |

**PUNTO DE CONTROL: Confirma brief antes de proceder.**

---

## Fase 2: Diseñar

### Jerarquía de Mensajería

Define qué aparece en cada cara del empaque, clasificado por importancia:

1. **Cara frontal (héroe):** Nombre de marca, nombre de producto, imagen o visual clave, reclamo de beneficio principal
2. **Cara trasera:** Descripción de producto, características/ingredientes, instrucciones de uso, certificaciones
3. **Paneles laterales:** Info secundaria, handles sociales, sitio web, código de barras/SKU
4. **Fondo/superior:** Texto de cumplimiento, info de fabricación, símbolos de reciclaje

### Consideraciones de Material

| Material | Mejor Para | Sostenibilidad | Costo |
|----------|---------|---------------|------|
| Cartón kraft | Marcas eco-friendly, productos livianos | Reciclable, biodegradable | Bajo |
| Caja rígida | Experiencia de desempaque premium/lujo | Reciclable | Alto |
| Sobre poly | Bienes blandos, ropa, bajo costo de envío | Varía (opciones recicladas) | Muy bajo |
| Moldeado personalizado | Productos frágiles, accesorios tech | Varía | Alto (costo de molde) |

**PUNTO DE CONTROL: Presenta el concepto de empaque y recomendación de material antes de detallar especificaciones.**

---

## Fase 3: Construir

### Entregables

**1. Brief Completo de Empaque**
- Dimensiones del producto y empaque (especificaciones de plantilla de despliegue)
- Recomendaciones de material y acabado (mate, brillante, spot UV, foil)
- Especificaciones de color (CMYK, Pantone para colores de marca)
- Jerarquía de mensajería con copia exacta para cada panel
- Directrices de colocación de imagen y gráfico

**2. Solicitud de Plantilla de Despliegue**
- Dimensiones para que el fabricante de empaque cree la plantilla de despliegue
- Layout de panel con zonas para cada área de contenido
- Especificaciones de sangría, recorte y zona segura

**3. Documento de Copia**
- Todo el texto que aparece en el empaque, organizado por panel
- Texto de cumplimiento y cumplimiento verificado
- Requisitos de colocación y tamaño de código de barras

**4. Hoja de Especificación de Vendedor**
- Material, dimensiones, acabado y cantidad
- Método de impresión (offset, digital, flexográfico)
- Requisitos de prueba (prueba digital, prueba impresa, muestra de producción)
- Cronograma: diseño → prueba → producción → entrega

---

## Fase 4: Pulir

### Lista de Verificación Pre-Producción

- [ ] Plantilla de despliegue aprobada por fabricante
- [ ] Toda la copia revisada por dos personas
- [ ] Texto de cumplimiento verificado para la región de venta
- [ ] Prueba de color revisada en iluminación natural
- [ ] Empaque probado con producto real adentro
- [ ] Durabilidad de envío probada (prueba de caída, prueba de compresión)
- [ ] Costo por unidad confirmado con fabricante

### Revisión Post-Lanzamiento

Después de que las primeras 100 unidades se envíen, evalúa: tasa de daño, feedback del cliente sobre desempaque, razones de devolución relacionadas con empaque.

---

## Anti-Patrones

- **Diseñar antes de dimensionar** — diseñar empaque sin dimensiones de producto confirmadas lleva a rediseños costosos. Dimensiones primero.
- **Demasiado texto** — el empaque no es un folleto. Prioriza sin piedad. Si no pueden leerlo en 3 segundos, córtalo.
- **Ignorar competencia de estante** — diseña en contexto. ¿Cómo se ve tu empaque al lado de competidores en un estante o cuadrícula de resultados de búsqueda?
- **Olvidar cumplimiento** — falta de texto requerido (ingredientes, advertencias, códigos de barras) significa reimprimir toda la corrida. Verifica temprano.
- **Sorpresa de MOQ bajo** — el empaque personalizado frecuentemente tiene cantidades mínimas de pedido de 500-5,000. Confirma que los MOQs coincidan con tu plan de producción.

---

## Recuperación

- **Sin directrices de marca aún:** Usa la skill guía-identidad-marca primero, o define elementos de marca mínimos (logo, 2 colores, 1 fuente) antes de hacer brief sobre empaque.
- **Presupuesto demasiado bajo para empaque personalizado:** Usa empaque de stock (cajas kraft simples, sobres poly de stock) con stickers o sellos personalizados para V1. Actualiza con volumen.
- **Las dimensiones del producto no están finalizadas:** Usa dimensiones estimadas con una nota de que el brief debe actualizarse antes de la producción. No ordenes empaque para productos sin terminar.
- **Vendiendo internacionalmente:** Señala requisitos de cumplimiento por mercado (EU, UK, Asia tienen diferentes requisitos de etiquetado). Recomienda revisión regulatoria.
