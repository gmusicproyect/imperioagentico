---
name: lista-verificacion-impuestos
description: "Crea listas de verificación de preparación fiscal organizadas por tipo de entidad con recopilación de documentos y rastreo de plazos. Usa cuando prepares para temporada de presentación fiscal de negocio."
allowed-tools: Read Write Glob
metadata:
  author: Imperio Digital
  version: "1.0"
---

# Lista de Verificación de Preparación Fiscal

## Cuándo Usar Este Skill

Usa este skill cuando necesites:
- Organizar documentos e información para presentación de impuestos comerciales
- Crear una lista de verificación integral de preparación fiscal personalizada a tu tipo de entidad
- Rastrear plazos de impuestos y requisitos de presentación
- Prepararte para una reunión con tu contador o preparador de impuestos

**NO** uses este skill para asesoramiento fiscal, preparación de declaración de impuestos, o estrategia fiscal legal. Esta es una herramienta de organización de documentos solamente. Siempre consulta un profesional fiscal calificado.

---

## Principio Fundamental

LA PREPARACIÓN FISCAL ES UN EJERCICIO DE RECOPILACIÓN DE DOCUMENTOS — LA LISTA DE VERIFICACIÓN ASEGURA QUE NADA SE PIERDA PARA QUE TU CONTADOR PUEDA HACER SU TRABAJO EFICIENTEMENTE Y PAGUES SOLO LO QUE DEBES.

---

## Fase 1: Perfil de Negocio

### Información Requerida

| Entrada | Qué Preguntar | Por Defecto |
|---------|---------------|------------|
| **Tipo de entidad** | "¿Cuál es tu entidad comercial? (propietario único, LLC, S-corp, C-corp, sociedad)" | Propietario único / LLC de un solo miembro |
| **Año fiscal** | "¿Para qué año fiscal te estás preparando?" | Año calendario anterior |
| **Rango de ingresos** | "¿Ingresos anuales aproximados?" | Bajo $250K |
| **Tiene empleados** | "¿Tienes empleados W-2?" | No — solo contratistas |
| **Estado(s)** | "¿En cuál(es) estado(s) operás?" | Un solo estado |
| **Contador** | "¿Tienes un CPA o preparador de impuestos?" | Sí |

**PUNTO DE CONTROL: No procedas sin tipo de entidad y año fiscal.**

---

## Fase 2: Lista de Verificación de Documentos

### Documentos Universales (Todos los Tipos de Entidad)

```
## Lista de Verificación de Preparación Fiscal: [Año Fiscal]

### Información de Negocio
- [ ] EIN (Número de Identificación de Empleador)
- [ ] Nombre legal de negocio y DBA
- [ ] Dirección de negocio
- [ ] Fecha en que el negocio comenzó (si es nuevo)
- [ ] Declaración de impuestos del año anterior (para referencia)

### Documentación de Ingresos
- [ ] Ingresos brutos totales para el año
- [ ] Formularios 1099-NEC recibidos (para trabajo contratado realizado)
- [ ] Formularios 1099-K (reportes del procesador de pago — PayPal, Stripe, etc.)
- [ ] Formularios 1099-MISC recibidos
- [ ] Otra documentación de ingresos (intereses, inversiones, alquiler)
- [ ] Reportes de ingresos mensuales/anuales de sistema de contabilidad

### Documentación de Gastos
- [ ] Estados de cuenta bancarios (todas las cuentas de negocio, todos los 12 meses)
- [ ] Estados de cuenta de tarjeta de crédito (todas las tarjetas de negocio, todos los 12 meses)
- [ ] Reporte de gastos categorizado de software de contabilidad
- [ ] Recibos para compras sobre $75 (o el umbral de tu contador)
- [ ] Registro de millas de vehículo (si reclamas millas de negocio)
- [ ] Mediciones de oficina en casa y metraje cuadrado total de casa (si aplica)
```

### Documentos Específicos de Entidad

**Propietario Único / LLC de Un Solo Miembro:**
```
- [ ] Categorías de Schedule C preparadas (ingresos, COGS, gastos)
- [ ] Registros de pagos de impuestos estimados (4 pagos trimestrales)
- [ ] Cálculo de impuesto de trabajo autónomo
- [ ] Registros de prima de seguro de salud (para deducción SE de salud)
- [ ] Contribuciones de jubilación (SEP IRA, Solo 401k)
```

**S-Corp / LLC gravada como S-Corp:**
```
- [ ] Compensación de oficiales (W-2 para ti)
- [ ] Registros de distribución de accionista
- [ ] Presentaciones de impuestos de nómina (Forma 941 trimestral)
- [ ] Forma W-3 (resumen anual de salarios)
- [ ] Documentación de compensación razonable
- [ ] Documentación de préstamo de accionista (si aplica)
```

**Sociedad / LLC de Múltiples Miembros:**
```
- [ ] Acuerdo de sociedad (para asignación de ganancias/pérdidas %)
- [ ] Registros de cuenta de capital para cada socio
- [ ] Registros de contribución y distribución de socio
- [ ] Datos de preparación de Schedule K-1
```

---

## Fase 3: Plazos Clave

```
## Plazos Fiscales: [Año Fiscal]

| Formulario | Tipo de Entidad | Plazo | Plazo de Extensión |
|------|------------|----------|-------------------|
| Schedule C (con 1040) | Propietario Único | 15 de Abril | 15 de Octubre |
| Forma 1065 | Sociedad | 15 de Marzo | 15 de Septiembre |
| Forma 1120-S | S-Corp | 15 de Marzo | 15 de Septiembre |
| Forma 1120 | C-Corp | 15 de Abril | 15 de Octubre |
| 1099-NEC (a contratistas) | Todos | 31 de Enero | Sin extensión |
| W-2 (a empleados) | Todos | 31 de Enero | Sin extensión |

### Pagos Fiscales Estimados (Próximo Año)
| Trimestre | Período | Fecha Vencimiento |
|---------|--------|----------|
| Q1 | Enero-Marzo | 15 de Abril |
| Q2 | Abril-Junio | 15 de Junio |
| Q3 | Julio-Agosto | 15 de Septiembre |
| Q4 | Septiembre-Diciembre | 15 de Enero |
```

---

## Fase 4: Paquete de Preparador

Organiza todos los documentos en esta estructura para tu preparador de impuestos:

```
tax-prep-[AÑO]/
├── income/
├── expenses/
├── contractor-docs/
├── payroll/ (si aplica)
├── prior-year-return/
└── notes-and-questions.md
```

---

## Anti-Patrones

- **Tratar esto como asesoramiento fiscal** — esta es una herramienta de preparación y organización. Siempre defiere a un profesional fiscal calificado para estrategia fiscal.
- **Esperar hasta Abril** — comienza a reunir documentos en Enero. Cuanto más temprano comiences, más deducciones encontrarás.
- **Mezclar gastos personales y de negocio** — solo incluye gastos de negocio claros. Si las cuentas están mezcladas, sepáralas antes de entregar al CPA.
- **Ignorar pagos de impuestos estimados** — solopreneurs que saltan pagos trimestrales enfrentan penalizaciones. Rastrea los cuatro pagos.
- **Caja de zapatos de recibos** — registros digitales categorizados ahorran tiempo de tu contador (y tu factura). Organiza antes de entregar.

---

## Recuperación

- **Sin sistema de contabilidad:** Camina a través de estados de cuenta bancarios y tarjeta de crédito mes a mes. Categoriza gastos en categorías de Schedule C. Recomienda configurar contabilidad para próximo año.
- **Faltando recibos:** Muchas deducciones bajo $75 no requieren recibos — estados de cuenta bancarios/tarjeta de crédito son suficientes. Para compras grandes, revisa email para recibos digitales.
- **Perdí pagos de impuestos trimestrales:** Calcula exposición de penalización y incluye fondos extras en el pago final. Configura autopago para próximo año.
- **Primer año en negocio:** Sígnala deducciones de costo de inicio, asegura documentos de formación de entidad en archivo, y configura pagos de impuestos trimestrales en adelante.
