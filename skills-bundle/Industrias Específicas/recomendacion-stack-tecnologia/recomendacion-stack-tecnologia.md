---
name: recomendacion-stack-tecnologia
description: "Recomienda stacks de tecnología para tipos de negocios específicos con selección de herramientas, justificación de costos, y orden de implementación. Usar cuando construyas tu fundación de software empresarial."
allowed-tools: Read Write Glob
metadata:
  author: Imperio Digital
  version: "1.0"
---

# Recomendación de Stack de Tecnología

## Cuándo Usar Esta Habilidad

Usa esta habilidad cuando necesites:
- Seleccionar un stack de tecnología completo para un nuevo negocio o proyecto
- Recomendar herramientas en múltiples funciones empresariales (comunicación, finanzas, marketing, etc.)
- Diseñar un plan de implementación por fases para adoptar múltiples herramientas
- Equilibrar costo, capacidad y simplicidad para un solista o equipo pequeño

**NO** uses esta habilidad para evaluar una sola herramienta (usa saas-evaluation), auditar un stack existente (usa tool-stack-audit), o arquitectura de TI empresarial. Esto es para diseño de stack de tecnología para pequeños negocios.

---

## Principio Fundamental

EL MEJOR STACK DE TECNOLOGÍA ES EL MÁS PEQUEÑO QUE CUBRE TUS NECESIDADES — CADA HERRAMIENTA ADICIONAL SUMA COSTO, COMPLEJIDAD Y MANTENIMIENTO. COMIENZA CON LOS ESENCIALES Y AÑADE SOLO CUANDO UN PROBLEMA REAL LO DEMANDA.

---

## Fase 1: Resumen

### Información Requerida

| Información | Qué Preguntar | Predeterminado |
|-------|------------|---------|
| **Tipo de negocio** | "¿Qué tipo de negocio? Servicio, producto, SaaS, e-commerce, contenido?" | Sin predeterminado — debe proporcionarse |
| **Etapa del negocio** | "¿Previo al lanzamiento, lanzado, o escalando?" | Lanzado, menos de $100K ingresos |
| **Tamaño del equipo** | "¿Cuántas personas necesitan usar estas herramientas?" | Solo (1 persona) |
| **Presupuesto mensual** | "¿Cuál es tu presupuesto total para todas las herramientas de software?" | Menos de $200/mes |
| **Herramientas actuales** | "¿Qué herramientas usas ya y quieres mantener?" | Google Workspace o ninguna |
| **Necesidades prioritarias** | "¿Qué funciones empresariales necesitan herramientas más urgentemente?" | Sin predeterminado — clasifica top 3 |

**PUNTO DE CONTROL: Confirma el resumen antes de diseñar el stack.**

---

## Fase 2: Mapea Funciones Empresariales

### Inventario de Funciones

Para el tipo de negocio, identifica cuáles funciones necesitan herramientas:

| Función | Prioridad | Estado |
|----------|----------|--------|
| **Comunicación** (email, mensajería) | Esencial | |
| **Sitio web** (hosting, CMS) | Esencial | |
| **Finanzas** (facturación, contabilidad, banca) | Esencial | |
| **CRM / Contactos** | Alto | |
| **Gestión de Proyectos** | Alto | |
| **Marketing** (email, social, anuncios) | Alto | |
| **Creación de Contenido** (diseño, escritura, video) | Medio | |
| **Analítica** (web, negocio) | Medio | |
| **Almacenamiento de Archivos** (documentos, activos) | Medio | |
| **Programación** (calendario, citas) | Medio | |
| **Legal** (contratos, cumplimiento) | Bajo | |
| **Herramientas IA** (escritura, automatización, investigación) | Medio | |

Marca cada como: Necesario Ahora / Necesario Pronto / Aún No / No Aplicable

**PUNTO DE CONTROL: Confirma cuáles funciones abordar antes de recomendar herramientas.**

---

## Fase 3: Recomienda

### Formato de Recomendación de Stack

Para cada función, recomienda una herramienta principal:

```
## Stack de Tecnología Recomendado

### Comunicación
**Herramienta:** [Nombre] — $[X]/mes
**Por qué:** [Justificación de una oración]
**Alternativa:** [Opción secundaria si difiere presupuesto o necesidades]

### Sitio Web
**Herramienta:** [Nombre] — $[X]/mes
**Por qué:** [Justificación de una oración]
**Alternativa:** [Opción secundaria]

[Repite para cada función...]
```

### Arquetipos de Stack

**El Stack Bootstrap (menos de $50/mes):**
- Google Workspace ($7/mes) — email, docs, almacenamiento
- Carrd o WordPress ($0-12/mes) — sitio web
- Wave o Stripe ($0) — facturación y pagos
- Notion ($0-10/mes) — CRM, gestión de proyectos, docs
- Canva Gratuito ($0) — diseño
- Mailchimp Gratuito ($0) — email marketing
- Claude Gratuito ($0) — escritura y investigación IA

**El Stack de Crecimiento ($100-200/mes):**
- Google Workspace ($14/mes) — email, almacenamiento
- WordPress + hosting ($20-30/mes) — sitio web
- QuickBooks ($30/mes) — contabilidad
- Notion o ClickUp ($10-15/mes) — gestión de proyectos
- ConvertKit ($29/mes) — email marketing
- Canva Pro ($13/mes) — diseño
- Claude Pro ($20/mes) — IA
- Calendly ($0-8/mes) — programación
- Zapier ($20/mes) — automatización

### Resumen de Costos

```
## Resumen de Costo Mensual

| Función | Herramienta | Costo |
|----------|------|------|
| Comunicación | [Herramienta] | $[X] |
| Sitio Web | [Herramienta] | $[X] |
| Finanzas | [Herramienta] | $[X] |
| CRM / PM | [Herramienta] | $[X] |
| Marketing | [Herramienta] | $[X] |
| Diseño | [Herramienta] | $[X] |
| IA | [Herramienta] | $[X] |
| **Total** | | **$[X]/mes** |
| **Anual** | | **$[X]/año** |
```

---

## Fase 4: Pulir

### 1. Orden de Implementación

Secuencia la adopción de herramientas para evitar abrumarse:

| Fase | Cronograma | Herramientas a Configurar | Por Qué Primero |
|-------|----------|----------------|-----------|
| Semana 1 | Esencial | Email, sitio web, facturación | Habilitando ingresos |
| Semana 2 | Operaciones | Gestión de proyectos, almacenamiento de archivos | Fundación de workflow |
| Semana 3 | Crecimiento | Email marketing, CRM | Relaciones con clientes |
| Semana 4 | Optimización | Diseño, IA, automatización | Ganancias de eficiencia |

### 2. Mapa de Integración

Muestra cómo se conectan las herramientas recomendadas:

```
[Sitio Web] → leads → [Email Marketing] → nutre → [CRM]
[CRM] → proyectos → [Gestión de Proyectos] → facturas → [Finanzas]
[Automatización] conecta [todas las herramientas] a través de disparadores y acciones
```

### 3. Lista de Verificación de Calidad

```
## Lista de Verificación de Stack de Tecnología

- [ ] Todas las funciones empresariales prioritarias tienen una herramienta recomendada
- [ ] Cada herramienta tiene una justificación clara (no solo porque es popular)
- [ ] El costo mensual total está dentro del presupuesto
- [ ] Se proporcionan alternativas para herramientas clave (en caso de preferencia)
- [ ] La implementación es por fases durante 4 semanas (no todo a la vez)
- [ ] Los puntos de integración entre herramientas se identifican
- [ ] Se aprovechan planes gratuitos y pruebas donde es posible
- [ ] El stack evita redundancia (sin dos herramientas para el mismo trabajo)
- [ ] Se verifica portabilidad de datos (¿puedes exportar y dejar cada herramienta?)
- [ ] Se calcula el costo anual para planificación presupuestaria
```

---

## Ejemplo

**Negocio:** Escritor autónomo de copywriting, recién lanzado, presupuesto de $100/mes

```
## Stack Recomendado — $87/mes

| Función | Herramienta | Costo |
|----------|------|------|
| Email + Docs | Google Workspace | $7 |
| Sitio Web | Carrd | $9 |
| Facturación | Stripe Invoicing | $0 (cuotas por transacción) |
| CRM + PM | Notion | $10 |
| Email Marketing | MailerLite | $0 (gratuito hasta 1K suscriptores) |
| Diseño | Canva Pro | $13 |
| Escritura IA | Claude Pro | $20 |
| Programación | Calendly | $0 (plan gratuito) |
| Contratos | HelloSign | $15 |
| Automatización | Zapier | $20 |
| **Total** | | **$94/mes** |
```

**Orden de implementación:** Semana 1: Google Workspace, Carrd, Stripe. Semana 2: Notion, Calendly. Semana 3: MailerLite, HelloSign. Semana 4: Canva, Claude, Zapier.

---

## Anti-Patrones

- **Herramientas empresariales para negocios en solitario** — Salesforce para un negocio de una persona es como usar una manguera de incendios para regar una planta de casa.
- **Adoptar todo a la vez** — la fatiga de configuración es real. Implementa por fases durante mínimo 4 semanas.
- **Elegir herramientas que tus amigos usan** — la selección de herramientas debe coincidir con TUS necesidades empresariales, no con las de alguien más.
- **Ignorar planes gratuitos** — muchas herramientas ofrecen planes generosos gratuitos. Úsalos hasta que crezcas más allá.
- **Construir en lugar de comprar** — a menos que tu negocio SEA software, compra la herramienta. Tu tiempo se usa mejor en clientes e ingresos.

---

## Recuperación

- **Presupuesto demasiado ajustado para recomendaciones:** Comienza con solo planes gratuitos. Google Workspace, Notion Free, Canva Free y Mailchimp Free cubren 80% de necesidades a $0.
- **El usuario se siente abrumado por opciones:** Elige UN arquetipo (Bootstrap o Crecimiento) e impleméntalo tal cual. Personaliza más tarde.
- **Una herramienta recomendada no se ajusta después de intentarla:** Cámbiala por la alternativa. La mayoría de herramientas en la misma categoría son intercambiables.
- **El usuario ya tiene herramientas que quiere mantener:** Construye el stack alrededor de sus conservadores. Llena solo los huecos.
