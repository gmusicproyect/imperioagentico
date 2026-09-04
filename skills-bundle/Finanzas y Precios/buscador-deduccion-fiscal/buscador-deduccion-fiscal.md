---
name: buscador-de-deducciones-fiscales
description: Identifica deducciones fiscales empresariales comúnmente pasadas por alto por industria y tipo de entidad con listas de categorías y requisitos de documentación. Utiliza esta habilidad cuando un trabajador independiente o propietario de pequeña empresa se está preparando para la temporada fiscal, desea reducir su factura fiscal o necesita saber qué gastos empresariales son deducibles.
allowed-tools: Read Write Bash(ls)
author: Imperio Digital
---

# Buscador de Deducciones Fiscales

## Cuándo Usar Esta Habilidad

- El usuario se está preparando para la temporada fiscal y desea maximizar deducciones
- El usuario es un trabajador independiente o empresario individual que no sabe qué puede deducir
- El usuario desea una lista de control de deducciones comúnmente pasadas por alto para su industria
- El usuario necesita conocer los requisitos de documentación para deducciones específicas
- El usuario acaba de iniciar un negocio y no sabe qué califica como gasto empresarial

## Principio Fundamental

CADA DEDUCCIÓN LEGÍTIMA PASADA POR ALTO ES DINERO DEJADO EN LA MESA — PERO CADA DEDUCCIÓN SIN APOYO ES UN RIESGO DE AUDITORÍA. DOCUMENTA TODO.

## Descargo de Responsabilidad Fiscal

**IMPORTANTE: Esta habilidad proporciona información educativa general sobre deducciones empresariales comunes. No constituye asesoramiento fiscal. Las leyes fiscales varían según la jurisdicción, cambian frecuentemente y dependen de circunstancias individuales. Siempre consulta a un CPA calificado o profesional fiscal antes de reclamar deducciones. La información aquí se basa en principios fiscales federales estadounidenses generales y puede no aplicarse a tu situación específica.**

## Workflow

### Fase 1: Perfil del Negocio

1. Determina el tipo de negocio y estructura de entidad:
   - Propietario individual / LLC de miembro único (Schedule C)
   - Asociación / LLC de múltiples miembros (Formulario 1065)
   - S-Corporation (Formulario 1120-S)
   - C-Corporation (Formulario 1120)
2. Identifica la industria/nicho (trabajador independiente, comercio electrónico, consultor, creador de contenido, etc.)
3. Pregunta si el usuario trabaja desde casa (elegibilidad de deducción de oficina en casa)
4. Pregunta si el usuario usa un vehículo personal para negocios

### Fase 2: Generar Lista de Deducciones

5. Presenta la lista de control universal de deducciones (aplica a la mayoría de negocios):

**Deducciones Comúnmente Pasadas por Alto — Universales:**

| Categoría | Ejemplos | ¿Frecuentemente Pasado por Alto? |
|-----------|----------|-----------------------------------|
| Oficina en Casa | Espacio de trabajo dedicado, porcentaje de renta/hipoteca, servicios, internet | SÍ — muchos lo saltan |
| Vehículo/Mileaje | Millas de negocio a la tarifa estándar del IRS, estacionamiento, peajes | SÍ — no registran las millas |
| Seguro de Salud | Deducción de prima de seguro de salud de autoempleado (Schedule 1) | SÍ — los empresarios individuales lo pierden |
| Contribuciones de Jubilación | SEP-IRA, Solo 401(k), SIMPLE IRA | SÍ — ahorros fiscales enormes ignorados |
| Impuesto de Autoempleo | Deduce 50% del impuesto SE en Schedule 1 | SÍ — automático pero frecuentemente desconocido |
| Desarrollo Profesional | Cursos, certificaciones, conferencias, libros relacionados con negocio | SÍ |
| Software y Suscripciones | Herramientas SaaS, aplicaciones de diseño, gestión de proyectos, software de contabilidad | A veces |
| Seguro Empresarial | Responsabilidad civil, E&O, indemnización profesional, seguro cibernético | A veces |
| Servicios Profesionales | Honorarios de CPA, honorarios legales, contabilidad, coaching empresarial | A veces |
| Comisiones Bancarias y de Procesamiento | Comisiones de Stripe, comisiones de PayPal, comisiones de cuenta de comerciante, comisiones bancarias empresariales | SÍ |
| Marketing y Publicidad | Anuncios, patrocinios, tarjetas de visita, hosting de sitio web, nombres de dominio | Raramente pasado por alto |
| Suministros y Equipos de Oficina | Computadoras, escritorios, sillas, impresoras (Sección 179 para artículos grandes) | A veces |
| Viaje | Vuelos de negocio, hoteles, 50% de comidas de negocio | A veces |
| Teléfono e Internet | Porcentaje de negocio de factura personal de teléfono/internet | SÍ |
| Costos de Inicio | Hasta $5,000 en gastos de inicio del primer año (si el total es menor de $50K) | SÍ |
| Deuda Incobrable | Invoices que no pudiste cobrar | SÍ |
| Educación Continua | Cursos y capacitación que mantienen o mejoran habilidades actuales | A veces |

6. Agrega deducciones específicas de la industria basadas en el tipo de negocio del usuario

### Fase 3: Deducciones Específicas de la Industria

7. Presenta adiciones relevantes:

**Creadores de Contenido (YouTube, Podcast, Redes Sociales):**
- Cámara, iluminación, micrófono y equipo de audio
- Software de edición (Final Cut Pro, Adobe Premiere, Descript)
- Props, fondos y materiales de set
- Estudio o espacio de grabación (alquiler o porción de oficina en casa)
- Herramientas de diseño de miniaturas o honorarios de diseñador independiente
- Productos comprados para revisión (si son necesarios para el contenido)
- Comisiones de licencia de música (Epidemic Sound, Artlist)

**Vendedores de Comercio Electrónico:**
- Costo de bienes vendidos (materiales, fabricación, venta al por mayor)
- Suministros de empaque y envío
- Fotografía de productos
- Almacenamiento de inventario (almacén, unidad de almacenamiento)
- Devoluciones y reembolsos (ajusta ingresos, no es una deducción per se)
- Muestras de productos
- Comisiones de ferias comerciales y puestos en mercados

**Trabajadores Independientes y Consultores:**
- Membresía en espacio de coworking
- Entretenimiento de clientes (50% de comidas con propósito comercial documentado)
- Hosting y diseño de sitio web de portafolio
- Membresías en asociaciones profesionales
- Comisiones de certificación y renovación de licencias
- Regalos a clientes (hasta $25 por persona por año)

**Entrenadores y Creadores de Cursos:**
- Comisiones de plataforma de cursos (Teachable, Kajabi, Thinkific)
- Software de webinarios (Zoom Pro, Crowdcast)
- Costos de plataforma comunitaria (Circle, planes pagos de Slack)
- Materiales de estudiantes y cuadernos de trabajo
- Costos del programa de certificación (si son necesarios para coaching)

### Fase 4: Requisitos de Documentación

8. Para cada categoría de deducción, especifica qué registros mantener:

| Deducción | Documentación Requerida |
|-----------|------------------------|
| Oficina en Casa | Metraje cuadrado de oficina vs. casa total, declaraciones de arrendamiento/hipoteca, facturas de servicios |
| Vehículo/Mileaje | Registro de mileaje (fecha, destino, propósito comercial, millas), recibos de gasolina si usas método de gasto real |
| Comidas | Recibo + nota de quién asistió y propósito comercial discutido |
| Viaje | Itinerario, recibos, documentación de propósito comercial |
| Equipo (>$2,500) | Recibo de compra, fecha puesta en servicio, porcentaje de uso comercial |
| Desarrollo Profesional | Recibo de curso, descripción de cómo se relaciona con negocio actual |
| Todos los gastos | Recibo o estado de cuenta bancaria/tarjeta de crédito mostrando cantidad, fecha y proveedor |

9. **CRÍTICO: Recomienda al usuario mantener recibos por un mínimo de 3 años (estatuto de limitaciones del IRS), idealmente 7 años**

### Fase 5: Entregar

10. Genera la lista de control de deducciones personalizada
11. Genera los requisitos de documentación
12. Proporciona rango de ahorros fiscales estimados si el usuario comparte su categoría fiscal
13. Recuérdales que consulten a un CPA

## Ejemplo 1: Diseñadora Gráfica Freelance (Propietario Individual)

**Perfil:** Diseñadora gráfica en solitario, trabaja desde casa, gana $85,000/año, usa auto personal para reuniones con clientes, paga su propio seguro de salud.

**Tu Lista de Control de Deducciones Personalizada:**

```
LISTA DE CONTROL DE DEDUCCIÓN FISCAL
Negocio: Diseño Gráfico Freelance (Schedule C)
Año Fiscal: 2025

COMÚNMENTE PASADO POR ALTO (verifica estos primero):
[x] Deducción de Oficina en Casa
    - Oficina: 150 pies cuadrados de 1,200 pies cuadrados = 12.5%
    - Método simplificado: $5/pies cuadrados x 150 = $750
    - Método regular: 12.5% de alquiler ($1,800/mes x 12 = $21,600)
      = $2,700 + 12.5% de servicios
    - USA MÉTODO REGULAR: ahorra ~$1,950 más

[x] Seguro de Salud de Autoempleado
    - Prima mensual: $420/mes = $5,040/año
    - Deducido en Schedule 1 (arriba de la línea, reduce AGI)
    - Esto NO es una deducción detallada — reduce ingreso sujeto a impuestos directamente

[x] Jubilación: Contribución SEP-IRA
    - Puede contribuir hasta 25% del ingreso neto de autoempleo
    - En ingreso neto de $85,000: hasta ~$17,700
    - Plazo: fecha de presentación de impuestos (incluyendo prórroga)

[x] Mileaje de Vehículo
    - 2,400 millas de negocio x $0.70/milla (tarifa 2025) = $1,680
    - Mantén una aplicación de registro de mileaje (MileIQ, Everlance, o manual)

[x] Deducción de Impuesto de Autoempleo
    - Automático: deduce 50% del impuesto SE en Schedule 1
    - En $85K: impuesto SE ~$12,010, deducción = ~$6,005

[x] Teléfono e Internet (porcentaje de negocio)
    - Teléfono: 60% uso de negocio x $85/mes x 12 = $612
    - Internet: 50% uso de negocio x $70/mes x 12 = $420

DEDUCCIONES ESTÁNDAR:
[x] Software: Adobe CC ($55/mes), Figma ($15/mes), Notion ($8/mes)
    = $936/año
[x] Hardware: MacBook Pro comprado en marzo 2025 ($2,499)
    — Sección 179: deduce cantidad total en año de compra
[x] Desarrollo profesional: Conferencia de diseño ($800),
    curso en línea ($297) = $1,097
[x] Marketing: Hosting de portafolio ($200), dominio ($15),
    LinkedIn Premium ($360) = $575
[x] Comisiones bancarias y de procesamiento: Comisiones de Stripe en invoices
    ~2.9% de $85,000 = $2,465
[x] Servicios profesionales: Contador ($150/mes x 12) = $1,800
[x] Suministros de oficina: Papel, tinta, unidad externa = ~$350

DEDUCCIONES TOTALES ESTIMADAS: $41,329
EN CATEGORÍA FISCAL 22%: ~$9,092 en ahorros fiscales federales
EN IMPUESTO SE 15.3%: ahorros adicionales ~$6,323 en impuesto SE
```

## Ejemplo 2: Negocio de Velas Artesanales de Comercio Electrónico (LLC de Miembro Único)

**Perfil:** Negocio de velas hechas a mano, trabaja desde estudio en casa, $48,000 de ingresos, asiste a 4 ferias artesanales por año.

**Tu Lista de Control de Deducciones Personalizada:**

```
LISTA DE CONTROL DE DEDUCCIÓN FISCAL
Negocio: Ember & Sage Candle Co. (Schedule C / LLC de Miembro Único)
Año Fiscal: 2025

COMÚNMENTE PASADO POR ALTO:
[x] Oficina en Casa (Espacio de Estudio)
    - Estudio dedicado: 200 pies cuadrados de 1,500 pies cuadrados = 13.3%
    - Método regular: 13.3% de interés de hipoteca, impuesto a la propiedad,
      servicios, seguros, reparaciones
    - Deducción estimada: $3,200

[x] Costos de Inicio (si el negocio comenzó este año)
    - Puede deducir hasta $5,000 en costos de inicio inmediatamente
    - Incluye: investigación de mercado, branding, configuración de inventario inicial,
      honorarios legales para formación de LLC

[x] Mileaje de Vehículo
    - Viajes a oficina postal, recogidas de proveedores, viaje a ferias artesanales
    - Millas estimadas 1,800 x $0.70 = $1,260

[x] Teléfono e Internet (40% uso de negocio)
    - $65/mes teléfono + $70/mes internet = $648/año

COSTO DE BIENES VENDIDOS:
[x] Cera, aceites de fragancia, mechas, tintes = $8,400
[x] Frascos, tapas, etiquetas = $3,200
[x] Empaque (cajas, papel de seda, pegatinas) = $1,400
[x] Suministros de envío = $1,100
    Total COGS: $14,100

GASTOS DE OPERACIÓN:
[x] Suscripción de Shopify ($79/mes x 12) = $948
[x] Canva Pro ($13/mes x 12) = $156
[x] Email marketing (Mailchimp, $20/mes x 12) = $240
[x] Anuncios de Instagram/Facebook = $2,400
[x] Sesión de fotografía de producto = $500
[x] Comisiones de puestos en ferias artesanales (4 x $200) = $800
[x] Viaje a ferias artesanales (hoteles, comidas al 50%) = $1,100
[x] Seguro de responsabilidad de producto = $500/año
[x] Comisión de cuenta bancaria empresarial ($10/mes x 12) = $120
[x] Comisiones de procesamiento de pagos (Stripe/Shopify ~2.9%) = $1,392
[x] Comisión de presentación anual de LLC = $50
[x] Contador ($100/mes x 12) = $1,200

DEDUCCIONES TOTALES ESTIMADAS: $29,564
EN $48,000 DE INGRESOS: ingreso sujeto a impuestos reducido a ~$18,436
```

## Recuperación y Alternativa

- Si el usuario no conoce su tipo de entidad, asume propietario individual (Schedule C) a menos que mencione incorporación — esto cubre la mayoría de empresarios individuales
- Si el usuario no está seguro de si algo califica como deducción, aplica la prueba de "ordinario y necesario": ¿Es común en tu industria? ¿Es útil para tu negocio? Si ambos son sí, es probable que sea deducible — pero recomienda confirmar con un CPA
- Si el usuario no tiene recibo para un gasto, puede usar estados de cuenta bancarios o de tarjeta de crédito como documentación de apoyo — pero los recibos originales son más fuertes
- Si el usuario no ha estado registrando deducciones todo el año, ayuda a reconstruir desde estados de cuenta bancarios categorizando las transacciones de los últimos 12 meses

## Restricciones

- **Siempre incluye el descargo de responsabilidad fiscal** — esto es educativo, no asesoramiento fiscal
- No calcules responsabilidad fiscal exacta — proporciona estimaciones como rangos y recomienda un CPA para números exactos
- No aconsejes estrategias de defensa de auditoría — eso requiere experiencia legal
- No recomiendes deducciones agresivas o cuestionables (100% de vehículo personal como negocio, artículos de lujo sin propósito comercial claro)
- Las tasas de mileaje del IRS cambian anualmente — nota que el usuario debe verificar la tarifa actual
- No proporciones orientación fiscal específica del estado — las reglas de deducción estatal varían significativamente
- Siempre recomienda separar finanzas personales y empresariales (cuenta bancaria empresarial dedicada)
- Los límites de contribución de jubilación cambian anualmente — recomienda verificar los límites actuales con el IRS o un CPA
