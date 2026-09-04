---
name: configuracion-contabilidad
description: "Establece sistemas de contabilidad con plan de cuentas, categorización de transacciones y procedimientos de conciliación. Úsalo cuando estés organizando la contabilidad de tu negocio."
allowed-tools: Read Write Glob
metadata:
  author: Imperio Digital
  version: "1.0"
---

# Configuración de Contabilidad

## Cuándo Usar Este Skill

Utiliza este skill cuando necesites:
- Establecer un plan de cuentas para un negocio nuevo
- Organizar categorías de transacciones para un seguimiento financiero limpio
- Crear procedimientos de conciliación y cronogramas
- Establecer workflows contables desde cero

**NO uses este skill** para preparación fiscal (usa tax-prep-checklist), proyecciones financieras, o elegir software de contabilidad. Esto es para configurar la estructura contable en sí.

---

## Principio Fundamental

LOS LIBROS LIMPIOS COMIENZAN CON UN PLAN DE CUENTAS SIMPLE Y CATEGORIZACIÓN CONSISTENTE — LA COMPLEJIDAD DEBE AGREGARSE SOLO CUANDO EL NEGOCIO LA REQUIERA.

---

## Fase 1: Perfil del Negocio

### Información Requerida

| Entrada | Qué Preguntar | Predeterminado |
|-------|------------|---------|
| **Tipo de negocio** | "¿Qué tipo de negocio? (servicio, producto, SaaS, consultoría)" | Basado en servicios |
| **Tipo de entidad** | "¿Persona física, LLC, S-corp, C-corp?" | LLC de un solo miembro |
| **Flujos de ingresos** | "¿Cómo ganas dinero?" | Sin predeterminado — debe proporcionarse |
| **Método contable** | "¿Base de caja o devengo?" | Base de caja |
| **Software** | "¿Qué software contable usas o planeas usar?" | QuickBooks Online |
| **Volumen mensual de transacciones** | "¿Aproximadamente cuántas transacciones por mes?" | Menos de 100 |

**PUNTO DE CONTROL: No procedas sin el tipo de negocio y flujos de ingresos.**

---

## Fase 2: Plan de Cuentas

### Plan de Cuentas Estándar

```
## Plan de Cuentas: [Nombre del Negocio]

### Activos (1000-1999)
| # | Nombre de la Cuenta | Tipo | Propósito |
|---|-------------|------|---------|
| 1000 | Cuenta Corriente Comercial | Banco | Cuenta operativa principal |
| 1010 | Cuenta de Ahorros Comercial | Banco | Reserva / ahorros fiscales |
| 1100 | Cuentas por Cobrar | Activo Circulante | Facturas pendientes de clientes |
| 1200 | Gastos Pagados por Adelantado | Activo Circulante | Suscripciones anuales pagadas por adelantado |

### Pasivos (2000-2999)
| # | Nombre de la Cuenta | Tipo | Propósito |
|---|-------------|------|---------|
| 2000 | Cuentas por Pagar | Pasivo Circulante | Facturas adeudadas a proveedores |
| 2100 | Tarjeta de Crédito | Pasivo Circulante | Saldo de tarjeta de crédito comercial |
| 2200 | Impuesto sobre Ventas por Pagar | Pasivo Circulante | Impuesto sobre ventas cobrado adeudado |
| 2300 | Pasivos de Nómina | Pasivo Circulante | Impuestos de nómina adeudados |

### Patrimonio (3000-3999)
| # | Nombre de la Cuenta | Tipo | Propósito |
|---|-------------|------|---------|
| 3000 | Patrimonio del Propietario | Patrimonio | Inversión del propietario en el negocio |
| 3100 | Retiro del Propietario | Patrimonio | Dinero retirado por el propietario |
| 3200 | Ganancias Retenidas | Patrimonio | Ganancias acumuladas |

### Ingresos (4000-4999)
| # | Nombre de la Cuenta | Tipo | Propósito |
|---|-------------|------|---------|
| 4000 | [Ingresos Primarios de Servicio/Producto] | Ingresos | Flujo de ingresos principal |
| 4100 | [Ingresos Secundarios] | Ingresos | Ingresos adicionales |
| 4200 | Otros Ingresos | Ingresos | Intereses, reembolsos, etc. |

### Costo de Bienes Vendidos (5000-5999)
| # | Nombre de la Cuenta | Tipo | Propósito |
|---|-------------|------|---------|
| 5000 | Pagos a Contratistas | COGS | Freelancers/subcontratistas |
| 5100 | Materiales / Suministros | COGS | Costos de proyecto directo |
| 5200 | Comisiones de Plataforma | COGS | Procesamiento, comisiones de mercado |

### Gastos Operativos (6000-6999)
| # | Nombre de la Cuenta | Tipo | Propósito |
|---|-------------|------|---------|
| 6000 | Publicidad y Marketing | Gasto | Gasto en anuncios, herramientas marketing |
| 6100 | Software y Suscripciones | Gasto | Herramientas SaaS, aplicaciones |
| 6200 | Suministros de Oficina | Gasto | Suministros, equipo menos de $2,500 |
| 6300 | Servicios Profesionales | Gasto | Contabilidad, honorarios legales |
| 6400 | Seguros | Gasto | Seguros comerciales |
| 6500 | Comidas y Entretenimiento | Gasto | Comidas de negocios (50% deducible) |
| 6600 | Viajes | Gasto | Viajes de negocios |
| 6700 | Educación y Capacitación | Gasto | Cursos, libros, conferencias |
| 6800 | Alquiler / Coworking | Gasto | Costos de espacio de trabajo |
| 6900 | Teléfono e Internet | Gasto | Porción comercial |
| 6950 | Comisiones Bancarias | Gasto | Comisiones mensuales, transferencias |
```

Personaliza números de cuenta y nombres según el negocio específico.

---

## Fase 3: Procedimientos

### Reglas de Categorización de Transacciones

```
## Guía de Categorización

| Tipo de Transacción | Categoría | Cuenta | Notas |
|-----------------|----------|---------|-------|
| Depósitos Stripe/PayPal | Ingresos | 4000 | Separa por producto si hay múltiples |
| Pagos a Contratistas | COGS | 5000 | Emitir 1099 si es $600+ |
| Software mensual (Slack, etc.) | Gasto | 6100 | |
| Anuncios Facebook/Google | Gasto | 6000 | |
| Transferencia personal del propietario | Patrimonio | 3100 | NO es un gasto |
| Pago trimestral de impuestos | Patrimonio | 3100 | NO es un gasto — retiros para impuestos |
| Pago de tarjeta de crédito | Pasivo | 2100 | NO es un gasto — reducción de pasivo |
```

### Cronograma de Conciliación

```
## Procedimientos de Conciliación

### Semanal (15 minutos)
- [ ] Categorizar todas las transacciones nuevas
- [ ] Revisar artículos sin categorizar
- [ ] Marcar cualquier cosa inusual para revisión

### Mensual (1 hora, antes del día 10)
- [ ] Conciliar todas las cuentas bancarias
- [ ] Conciliar tarjetas de crédito
- [ ] Revisar cuentas por cobrar — hacer seguimiento de facturas vencidas
- [ ] Revisar cuentas por pagar — pagar facturas pendientes
- [ ] Ejecutar reporte P&L y comparar con presupuesto
- [ ] Respaldar datos

### Trimestral (2 horas)
- [ ] Revisar plan de cuentas — agregar o fusionar según sea necesario
- [ ] Ejecutar P&L y Balance Sheet trimestral
- [ ] Calcular y pagar impuestos estimados
- [ ] Revisar pagos a contratistas por umbral 1099

### Anual (medio día, enero)
- [ ] Conciliación completa del año
- [ ] Preparar 1099s para contratistas
- [ ] Generar P&L y Balance Sheet anuales
- [ ] Preparar documentos fiscales para CPA
- [ ] Revisar y actualizar plan de cuentas para nuevo año
```

---

## Fase 4: Entregable

```
## Configuración del Sistema Contable Completa

### Entregado
1. Plan de cuentas (personalizado para tu negocio)
2. Guía de categorización
3. Cronograma de conciliación
4. Reglas y procedimientos clave

### Próximos Pasos
- [ ] Ingresar plan de cuentas en [software]
- [ ] Conectar alimentación de bancos y tarjetas de crédito
- [ ] Configurar transacciones recurrentes para gastos regulares
- [ ] Programar sesiones contables semanales de 15 minutos
- [ ] Establecer recordatorio de conciliación mensual para el día 5
```

---

## Ejemplo: Consultor Independiente

**Cuentas necesarias:** 15 total (2 bancos, 1 tarjeta de crédito, 1 AR, 3 patrimonio, 2 ingresos, 6 gastos). No se necesitan cuentas COGS — el tiempo es el producto. Sin nómina — solo retiro del propietario. Regla clave: el retiro del propietario NO es un gasto.

---

## Anti-Patrones

- **Demasiadas cuentas** — un trabajador autónomo no necesita 50 categorías de gastos. Comienza con 10-15 y agrega solo cuando necesites granularidad de reportes.
- **Mezclar personal y comercial** — una cuenta bancaria comercial, una tarjeta de crédito comercial. Sin excepciones.
- **Categorizar retiro del propietario como gasto** — el pago del propietario es patrimonio, no un gasto. Este error infla gastos y subestima ganancias.
- **Conciliación una vez al año** — la conciliación mensual detecta errores temprano. La conciliación anual se convierte en una investigación forense.
- **Ignorar cuentas por cobrar** — si facturas a clientes, rastrrea qué está pendiente. El dinero facturado no es dinero recibido.

---

## Recuperación

- **Libros existentes desordenados:** Comienza limpio desde el mes actual. Vuelve atrás y corrige meses anteriores solo si la declaración fiscal lo requiere — de lo contrario, enfócate hacia adelante.
- **Sin software de contabilidad:** Configura QuickBooks Online, Wave (gratuito), o Xero. Cualquiera funciona para pequeños negocios. No uses hojas de cálculo después del primer año.
- **Cuentas personales y comerciales mezcladas:** Abre una cuenta bancaria comercial inmediatamente. Mueve todas las transacciones comerciales allá. Separa transacciones históricas como mejor puedas.
- **Atrás en conciliación:** Bloquea 2-4 horas y concilia mes a mes comenzando desde el último mes limpio. No saltes adelante.
