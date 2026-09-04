---
name: propuesta-catering
description: "Escribe propuestas de catering con opciones de menú, precios en tiers, descripciones de servicio y detalles de logística. Úsalo cuando estés ofertando trabajos de catering o formalizando ofertas de catering."
allowed-tools: Read Write Glob
metadata:
  author: Imperio Digital
  version: "1.0"
---

# Propuesta de Catering

## Cuándo Usar Este Skill

Usa este skill cuando necesites:
- Escribir una propuesta profesional de catering para un evento
- Crear opciones de menú en tiers con precios por persona
- Detallar niveles de servicio, personal y logística para un trabajo de catering
- Presentar una propuesta pulida que gane contratos de catering

**NO** uses este skill para diseño de menú de restaurante, planificación de eventos o planes de negocios food truck. Esto es para propuestas y ofertas específicas de catering.

---

## Principio Fundamental

UNA PROPUESTA DE CATERING VENDE CONFIANZA — EL CLIENTE NO SOLO ESTÁ COMPRANDO COMIDA, ESTÁ COMPRANDO LA PAZ MENTAL DE QUE SU EVENTO SERÁ MANEJADO SIN ERRORES.

---

## Fase 1: Brief

### Inputs Requeridos

| Input | Qué Preguntar | Predeterminado |
|-------|------------|---------|
| **Tipo de evento** | "¿Cuál es el evento? ¿Boda, corporativo, fiesta, fundraiser?" | Sin predeterminado — debe proporcionarse |
| **Conteo de huéspedes** | "¿Cuántos huéspedes se esperan?" | Sin predeterminado — debe proporcionarse |
| **Fecha y hora del evento** | "¿Cuándo es el evento?" | Sin predeterminado — debe proporcionarse |
| **Venue** | "¿Dónde es el evento? ¿Tiene cocina el venue?" | Sin predeterminado — debe proporcionarse |
| **Rango de presupuesto** | "¿Cuál es el presupuesto del cliente por persona o total?" | Sin presupuesto específico compartido |
| **Requerimientos dietéticos** | "¿Restricciones dietéticas? ¿Vegetariano, vegano, sin gluten, alergias?" | Mix estándar |
| **Estilo de servicio** | "¿Buffet, plated, family-style, cocktail reception o stations?" | Buffet |
| **Preferencia de cocina** | "¿Preferencia de cocina o tema?" | Flexible |

**PUNTO DE CONTROL:** Confirma el brief antes de construir la propuesta.

---

## Fase 2: Estructura

### Esquema de Propuesta

1. **Portada** — Nombre de negocio, nombre del evento, fecha, nombre del cliente
2. **Introducción** — Breve sobre tu negocio de catering y enfoque
3. **Resumen del Evento** — Detalles confirmados (fecha, venue, conteo de huéspedes, estilo)
4. **Opciones de Menú** — 2-3 paquetes en tiers
5. **Detalles de Servicio** — Personal, equipo, setup, cronograma
6. **Precios** — Por-persona y total, itemizado
7. **Términos y Condiciones** — Depósitos, cancelaciones, plazo de confirmación de conteo
8. **Próximos Pasos** — Cómo confirmar e instrucciones de depósito

### Estrategia de Tier de Menú

Ofrece 2-3 tiers:

| Tier | Nombre | Por Persona | Posicionamiento |
|------|------|-----------|-------------|
| Tier 1 | Essential | $[X] | Cubre lo básico hermosamente |
| Tier 2 | Premium | $[X] | Proteínas mejoradas, cursos adicionales |
| Tier 3 | Signature | $[X] | Experiencia completa, ingredientes top, servicio premium |

**PUNTO DE CONTROL:** Confirma estructura de propuesta y estrategia de tier antes de escribir.

---

## Fase 3: Write

### Introducción

"[Nombre del Negocio] se especializa en catering de [cocina/estilo] para [tipos de evento]. Traemos [X] años de experiencia y pasión por crear experiencias gastronómicas memorables. Cada evento es customizado — desde desarrollo de menú hasta ejecución día del evento — para que te enfoques en tus huéspedes mientras nosotros manejamos la comida."

### Formato de Opción de Menú

```
## [Nombre del Tier] — $[X] por persona

### Appetizers (selecciona 2)
- [Artículo 1] — [descripción breve]
- [Artículo 2] — [descripción breve]
- [Artículo 3] — [descripción breve]
- [Artículo 4] — [descripción breve]

### Entrées (selecciona 2)
- [Artículo 1] — [descripción breve]
- [Artículo 2] — [descripción breve]
- [Artículo 3] — [descripción breve]

### Acompañamientos (incluidos)
- [Acompañamiento 1]
- [Acompañamiento 2]
- [Acompañamiento 3]

### Postre (selecciona 1)
- [Artículo 1] — [descripción breve]
- [Artículo 2] — [descripción breve]

### Bebidas
- [Qué está incluido: agua, té helado, café, limonada]

*Modificaciones dietéticas disponibles para todos los artículos del menú. Por favor infórmanos de cualquier alergia.*
```

### Detalles de Servicio

```
## Detalles de Servicio

**Estilo de servicio:** [Buffet/Plated/Stations]
**Personal proporcionado:** [X] meseros, [X] bartenders, [X] personal de cocina
**Equipo incluido:** Chafing dishes, utensilios de servicio, platos, servilletas, cubiertos
**Tiempo de setup:** [X] horas antes del inicio del evento
**Tiempo de breakdown:** [X] horas después del fin del evento
**Degustaciones:** Degustación gratuita para eventos de [X]+ huéspedes

**Cronograma del Evento:**
- [Hora]: Equipo de catering llega, comienza setup
- [Hora]: Preparación de comida y plating comienza
- [Hora]: Servicio de appetizers
- [Hora]: Servicio de plato principal
- [Hora]: Servicio de postre
- [Hora]: Breakdown y limpieza completa
```

### Sección de Precios

```
## Resumen de Precios

| Artículo | Por Persona | Cantidad | Total |
|------|-----------|----------|-------|
| Menú [Nombre del Tier] | $[X] | [huéspedes] | $[total] |
| Servicio de bar (si aplica) | $[X] | [huéspedes] | $[total] |
| Personal | Incluido | | — |
| Alquiler de equipo (si aplica) | — | — | $[total] |
| Tarifa de viaje/entrega | — | — | $[total] |
| **Subtotal** | | | **$[total]** |
| Impuestos ([X]%) | | | $[total] |
| Cargo de servicio ([X]%) | | | $[total] |
| **Total** | | | **$[total]** |
```

### Términos y Condiciones

- **Depósito:** [X]% debido al momento de la reservación para confirmar la fecha
- **Conteo final:** Debido [X] días antes del evento
- **Pago final:** Debido [X] días antes del evento
- **Cancelación:** Reembolso completo si se cancela [X]+ días. Depósito no reembolsable dentro de [X] días.
- **Conteo mínimo de huéspedes:** [X] huéspedes (la factura se basa en conteo confirmado o asistencia real, lo que sea mayor)
- **Sobras:** El cliente puede llevarse comida sobrante. El caterer no es responsable por seguridad alimentaria después del evento.

---

## Fase 4: Polish

### 1. Presentación de Propuesta

- Formatea como PDF limpio con tu marca (logo, colores, fonts)
- Incluye 3-5 fotos de alta calidad de tu comida y eventos previos
- Mantén el documento total bajo 5 páginas
- Usa formato consistente: mismos fonts, espaciado y estilos de tabla a lo largo

### 2. Plan de Seguimiento

- Envía propuesta dentro de 24 horas de la investigación
- Da seguimiento 3 días después si no hay respuesta
- Ofrece degustación si el cliente está decidiendo entre caterers
- Sé preparado para customizar menú basado en feedback

### 3. Lista de Verificación de Calidad

```
## Lista de Verificación de Propuesta de Catering

- [ ] Detalles del evento confirmados (fecha, venue, conteo de huéspedes, estilo)
- [ ] 2-3 tiers de menú presentados con precios claros
- [ ] Descripciones de menú son apetitosas y específicas
- [ ] Opciones de modificación dietética mencionadas
- [ ] Detalles de servicio incluyen conteo de personal, equipo y cronograma
- [ ] Precios completamente itemizados (sin cuotas ocultas)
- [ ] Términos cubren depósito, plazo de conteo final, cancelación y pago
- [ ] Propuesta formateada profesionalmente (PDF con marca)
- [ ] Fotos de trabajo anterior incluidas
- [ ] Próximo paso claro e información de contacto proporcionada
```

---

## Ejemplo

**Evento:** Fiesta de vacaciones corporativa, 75 huéspedes, cocktail reception + dinner stations

**Excerpto de Tier 2 (Premium):**
```
## Paquete Premium — $65 por persona

### Appetizers Pasados (selecciona 3)
- Dátiles envueltos en tocino con queso de cabra y miel
- Shooters de cóctel de camarones con crema de rábano picante
- Trio de bruschetta: tomate albahaca, champiñón y pimiento asado
- Mini cangrejo cakes con salsa remoulade

### Estaciones de Cena
**Estación de Tallado:** Prime rib a las hierbas con au jus y crema de rábano picante
**Estación de Pasta:** Penne hecho al momento con opción de marinara, alfredo o pesto
**Estación Estacional:** Display de vegetales asados con granos, verduras y vinagres

### Postre
Display de mini postres surtido: trufas de chocolate, tarts de fruta y tazas de tiramisú

### Bebidas
Estación de café, té, agua mineral y limonada (servicio de bar cotizado por separado)
```

---

## Anti-Patterns

- **Una opción, tómala o déjala** — siempre ofrece 2-3 tiers. Los clientes quieren sentir que tienen opción y control sobre presupuesto.
- **Precios vagos** — "Comenzando en $50 por persona" sin detalles crea sospecha. Itemiza todo.
- **Sin cronograma** — los clientes se preocupan por logística. Un cronograma detallado de día del evento muestra que has planeado cada detalle.
- **Descripciones genéricas** — "Pollo entré" pierde contra "Pollo de airline a la sartén con mantequilla de limón y hierbas y espárrago asado."
- **Términos faltantes** — propuestas sin términos de cancelación y pago llevan a disputas. Siempre incluye.

---

## Recuperación

- **El presupuesto es más bajo que tus tiers:** Ofrece menú simplificado — menos opciones de appetizer, proteínas más simples, buffet en lugar de plated. No comprometas calidad.
- **El cliente quiere artículos no en ningún tier:** Construye paquete custom. Cotiza artículos individuales y suma 10% por customización.
- **Compitiendo contra oferta más baja:** Enfatiza qué está incluido (personal, equipo, setup, cleanup) que competitors podrían cobrar extra. Detalla tu experiencia y referencias.
- **El cliente no responde después de propuesta:** Da seguimiento dos veces (Día 3 y Día 7). Después de eso, envía email de "cerrando archivo" final — esto frecuentemente genera respuesta.
