---
name: estrategia-venta-cruzada
description: "Mapea oportunidades de venta cruzada con lógica de emparejamiento de productos, disparadores de temporización y plantillas de mensajes. Úsalo cuando quieras aumentar los ingresos de clientes existentes."
allowed-tools: Read Write Glob
metadata:
  author: Imperio Digital
  version: "1.0"
---

# Estrategia de Venta Cruzada

## Cuándo Usar Este Skill

Usa este skill cuando necesites:
- Identificar oportunidades de venta cruzada en tu catálogo de productos
- Diseñar lógica de emparejamiento de productos basada en comportamiento de compra
- Crear plantillas de mensajes para emails de venta cruzada y recomendaciones en sitio
- Construir disparadores de temporización que presenten la oferta correcta en el momento correcto

**NO USES** este skill para upselling (versión superior del mismo producto), aumentos de pedido en el checkout, o adquisición de nuevos clientes. Esto es para vender productos complementarios a clientes existentes.

---

## Principio Fundamental

LA VENTA CRUZADA NO SE TRATA DE EMPUJAR MÁS PRODUCTOS — SE TRATA DE RECONOCER QUÉ NECESITA EL CLIENTE A CONTINUACIÓN BASÁNDOSE EN LO QUE YA COMPRÓ Y PRESENTARLO COMO UN PASO NATURAL.

---

## Fase 1: Brief

### Inputs Requeridos

| Input | Qué Preguntar | Default |
|-------|---------------|---------|
| **Catálogo de productos** | "Lista todos tus productos/servicios con precios." | Sin default — debe ser proporcionado |
| **Más vendidos** | "¿Qué productos se venden más?" | Sin default — debe ser proporcionado |
| **Datos de clientes** | "¿Sabes qué compran los clientes juntos?" | Conocimiento anecdótico |
| **Canales de comunicación** | "¿Cómo alcanzas a clientes existentes? (email, in-app, SMS)" | Email |
| **Compras promedio** | "¿Cuántos productos compra un cliente típico?" | 1-2 |

**PUNTO DE CONTROL: Confirma antes de mapear oportunidades de venta cruzada.**

---

## Fase 2: Mapa de Venta Cruzada

### Matriz de Emparejamiento de Productos

```
## Emparejamientos de Venta Cruzada

| Si Compraron | Recomienda | Por Qué | Timing |
|--------------|-----------|--------|--------|
| [Producto A] | [Producto C] | [Beneficio complementario] | 7 días post-compra |
| [Producto A] | [Producto D] | [Paso lógico siguiente] | 14 días post-compra |
| [Producto B] | [Producto A] | [Resuelve problema adyacente] | Después de onboarding |
| [Producto B] | [Producto E] | [Potencia resultados] | 30 días post-compra |
```

### Disparadores de Temporización

```
## Cuándo Hacer Venta Cruzada

**Inmediato (checkout/página de agradecimiento):** Solo si la venta cruzada es obvia
**7 días post-compra:** Después de que hayan tenido tiempo de usar el producto inicial
**Basado en hitos:** Después de completar un hito de uso u onboarding
**Estacional:** Cuando un producto complementario se alinea con temporada o evento
**Basado en comportamiento:** Cuando ven página de producto relacionado, abren contenido relacionado o hacen pregunta de soporte relacionada
```

**PUNTO DE CONTROL: Aprueba el mapa de venta cruzada antes de escribir mensajes.**

---

## Fase 3: Escribe Mensajes de Venta Cruzada

### Plantillas de Email

**Plantilla 1: Paso Natural Siguiente**
```
Asunto: Ahora que has [logrado X], aquí viene lo siguiente

Hola {nombre},

Has estado usando [Producto A] por [X] días, y basándome en [hito o comportamiento], parece que estás obteniendo resultados reales.

¿El paso natural siguiente? [Producto B] — [beneficio específico que se construye sobre Producto A].

[1-2 oraciones explicando cómo los dos productos funcionan juntos]

[CTA: Descubre Producto B →]
```

**Plantilla 2: Oferta Solo para Clientes**
```
Asunto: Exclusiva para clientes de [Producto A]

{nombre}, porque ya tienes [Producto A], quiero darte acceso anticipado a [Producto B] — y un precio especial.

[Descripción rápida de qué hace Producto B y por qué importa a usuarios de Producto A]

Precio solo para clientes: $[X] (precio regular: $[Y])

[CTA: Obtén Tu Precio de Cliente →]
```

### Texto de Recomendación en Sitio

Escribe tarjetas cortas de venta cruzada para páginas de productos, páginas de agradecimiento y dashboards de clientes:
```
"Clientes que compraron [Producto A] también aman [Producto B]"
"Completa tu conjunto: Añade [Producto B] para [beneficio]"
"Recomendado para ti basándose en tu compra"
```

---

## Fase 4: Pulido

### 1. Proyección de Impacto en Ingresos

- Valor promedio actual de pedido: $[X]
- Tasa de captación de venta cruzada proyectada: 10-20%
- Ingresos adicionales por 100 clientes: $[X]
- Estimación de aumento anual de ingresos: $[X]

### 2. Checklist de Implementación

- [ ] Emparejamientos de productos definidos y documentados
- [ ] Disparadores de temporización configurados en plataforma de email
- [ ] Plantillas de email escritas y cargadas
- [ ] Recomendaciones en sitio añadidas (si aplica)
- [ ] Tracking configurado (atribución de venta cruzada)
- [ ] Exclusiones configuradas (no recomiendes productos que ya poseen)

### 3. Ciclo de Optimización

- Mensual: revisa tasas de conversión de venta cruzada por emparejamiento
- Trimestral: añade nuevos emparejamientos basándote en datos de comportamiento de clientes
- Elimina o reemplaza emparejamientos con menos de 3% de conversión

---

## Anti-Patrones

- **Recomendar productos que ya poseen** — verifica historial de compras antes de cada punto de venta cruzada.
- **Venta cruzada inmediata después de compra** — déjales que experimenten el primer producto antes de empujar el siguiente. Espera al menos 7 días.
- **Emparejamientos irrelevantes** — si los productos no tienen conexión lógica, la recomendación se siente aleatoria y comercial.
- **Demasiadas recomendaciones** — recomienda 1-2 productos máximo. Una pared de opciones causa parálisis de decisión.
- **Sin beneficio solo para clientes** — los clientes existentes deben sentirse recompensados. Un precio especial o acceso anticipado hace la venta cruzada sentir exclusiva.

---

## Recuperación

- **Solo un producto:** La venta cruzada requiere múltiples productos. Recomienda construir un producto complementario primero, luego vuelve a este skill.
- **Sin datos de compra:** Comienza con emparejamientos lógicos basados en función de producto y necesidad del cliente, luego refina con datos con el tiempo.
- **Tasas bajas de venta cruzada (bajo 3%):** Prueba diferentes tiempos, ángulos de mensajes y emparejamientos de productos. El match de producto puede ser incorrecto.
- **Clientes se sienten sobre-comercializados:** Reduce frecuencia de venta cruzada a un punto de contacto por producto comprado. Calidad sobre cantidad.
