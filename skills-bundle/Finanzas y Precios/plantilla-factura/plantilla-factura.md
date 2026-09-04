---
name: plantilla-factura
description: "Genera documentos de factura profesionales con artículos de línea, cálculos de impuestos, términos de pago, y políticas de pago tardío, más una plantilla reutilizable para facturas futuras. Usa cuando necesites crear una factura, configurar un sistema de facturación, o estandarizar tu proceso de facturación como freelancer o propietario de pequeño negocio."
allowed-tools: Read Write Glob
metadata:
  author: Imperio Digital
  version: "1.0"
---

# Plantilla de Factura

## Cuándo Usar Este Skill

Usa este skill cuando necesites:
- Generar una factura profesional para un proyecto completado, hito, o período de retainer
- Configurar una plantilla de factura reutilizable con detalles de negocio incrustados
- Calcular artículos de línea, impuestos, descuentos, y totales para un documento de facturación de cliente
- Estandarizar tu proceso de facturación para que cada factura se vea consistente
- Crear un sistema de facturación desde cero como freelancer, consultor, o propietario de pequeño negocio

**NO** uses este skill para:
- Contabilidad o contabilidad (esto genera documentos, no rastreo de pagos)
- Automatización de facturación de suscripción recurrente (documentos estáticos, no procesamiento de pago)
- Reportes de gastos u órdenes de compra (formato de documento diferente)
- Asesoramiento fiscal o cumplimiento fiscal (consulta un contador para cumplimiento fiscal)

---

## Referencia Rápida: Capacidades de Factura

| Característica | Detalles |
|---------|---------|
| Campos de factura | 13 campos estándar por factura |
| Términos de pago | 4 presets (Neto 15, Neto 30, Debido al Recibir, División 50/50) |
| Manejo de impuestos | Basado en porcentaje, multi-tarifa, o exento de impuestos |
| Tipos de artículo de línea | Por hora, fijo, basado en cantidad, y hito |
| Formato de salida | Documento Markdown guardado como `.md` |
| Plantilla reutilizable | Plantilla basada en variable con sintaxis `{{PLACEHOLDER}}` |
| Políticas de pago tardío | 3 presets (porcentaje, plano, escalonado) |

## Referencia Rápida: Campos de Factura

| Campo | Requerido | Ejemplo |
|-------|----------|---------|
| Número de Factura | Sí | FAC-2025-001 |
| Fecha de Factura | Sí | 15 de Enero de 2025 |
| Fecha Vencimiento | Sí | 14 de Febrero de 2025 |
| De (Tu Negocio) | Sí | Acme Design LLC, 123 Main St, Chicago IL 60601 |
| Facturar A (Cliente) | Sí | Sarah Chen, Bright Solutions Inc. |
| Artículos de Línea | Sí | Diseño web - Página de Inicio, 1, $2,500.00 |
| Subtotal | Automático | $5,000.00 |
| Descuento | No | 10% ($500.00) |
| Tasa de Impuesto | No | 8.25% |
| Cantidad de Impuesto | Automático | $371.25 |
| Total | Automático | $4,871.25 (subtotal - descuento + impuesto) |
| Términos de Pago | Sí | Neto 30 |
| Política de Pago Tardío | Sí | 1.5% por mes sobre saldo no pagado |
| Métodos de Pago | Sí | Transferencia bancaria, PayPal, cheque |
| Notas | No | ¡Gracias por tu negocio! |

## Referencia Rápida: Términos de Pago

| Término | Significado | Mejor Para |
|------|---------|----------|
| Debido al Recibir | Pago debido inmediatamente | Trabajos pequeños bajo $500, servicios únicos |
| Neto 15 | Debido 15 días desde fecha de factura | Trabajo de freelance continuo, clientes de confianza |
| Neto 30 | Debido 30 días desde fecha de factura | B2B estándar, retainers |
| División 50/50 | 50% adelantado, 50% al completar | Proyectos grandes sobre $2,500, clientes nuevos |

**DEFAULT: Neto 30** -- estándar más común para freelancers y pequeños negocios.

---

## Workflow Básico

EL NÚCLEO WORKFLOW: NUNCA GENERES UNA FACTURA SIN VERIFICAR PRIMERO TODA LA MATEMÁTICA — CADA CANTIDAD DEBE SER VERIFICADA DE FORMA INDEPENDIENTE.

### Paso 1: Recopila Detalles de Negocio

1. **Nombre del negocio** -- nombre legal o DBA
2. **Dirección del negocio** -- calle, ciudad, estado/provincia, código postal, país
3. **Email de contacto** -- para correspondencia de factura
4. **Teléfono de contacto** -- opcional
5. **Métodos de pago** -- transferencia bancaria, PayPal, Venmo, Stripe, cheque, Zelle
6. **Detalles de pago** -- nombre bancario y últimos 4 dígitos, email de PayPal, handle de Venmo
7. **Términos de pago por defecto** -- default: Neto 30
8. **Política de pago tardío por defecto** -- default: 1.5% por mes
9. **Formato de numeración de factura** -- default: FAC-AAAA-NNN
10. **Estado fiscal** -- tasa o exento; default: exento de impuestos a menos que se especifique

Si el usuario proporciona artículos 1-2 y 5-6, procede con defaults para el resto.

### Paso 2: Recopila Detalles de Factura

1. **Nombre del cliente** -- persona o empresa siendo facturada
2. **Empresa del cliente** -- si diferente del nombre de contacto
3. **Dirección del cliente** -- dirección de correo
4. **Email del cliente** -- donde enviar la factura
5. **Artículos de línea** -- descripción, cantidad/horas, tasa unitaria para cada uno
6. **Descuento** -- porcentaje o cantidad plana; default: ninguno
7. **Tasa de impuesto** -- default del negocio o anulación
8. **Términos de pago** -- default del negocio o anulación
9. **Número de factura** -- siguiente en secuencia o especificado por usuario
10. **Notas** -- referencia de proyecto, gracias, notas de alcance

Si el usuario proporciona artículos 1 y 5, procede con defaults para el resto.

### Paso 3: Genera la Factura

1. **Calcula todos los montos:**
   - Total de artículo de línea = cantidad x tasa
   - Subtotal = suma de todos los totales de artículos de línea
   - Descuento = porcentaje o cantidad plana fuera de subtotal
   - Cantidad gravable = subtotal - descuento
   - Impuesto = cantidad gravable x tasa de impuesto
   - Total = cantidad gravable + impuesto

2. **VERIFICA LA MATEMÁTICA ANTES DE ESCRIBIR EL ARCHIVO:**
   - Recalcula cada valor independientemente
   - **TODOS LOS MONTOS DEBEN COINCIDIR HASTA EL CENTAVO -- ARREGLA CUALQUIER DISCREPANCIA ANTES DE PROCEDER**

3. **Genera la factura en markdown** con esta estructura: encabezado (número de factura, fechas), sección De (detalles de negocio), sección Facturar A (detalles de cliente), tabla de Servicios (artículos de línea con #, descripción, qty, tasa, cantidad), tabla de Resumen (subtotal, descuento, impuesto, total), Términos de Pago (fecha de vencimiento, política de pago tardío), Métodos de Pago (cada método con detalles), Notas

4. **Guarda como `{número-factura}.md`** en el directorio de trabajo del usuario o ubicación especificada

5. **Presenta al usuario** para revisión antes de finalizar

### Paso 4: Crea la Plantilla Reutilizable

Después de la primera factura, crea una plantilla con variables `{{PLACEHOLDER}}` para valores específicos de factura mientras mantienes detalles de negocio incrustados.

**Variables de plantilla:**
`{{NUMERO_FACTURA}}`, `{{FECHA_FACTURA}}`, `{{FECHA_VENCIMIENTO}}`, `{{NOMBRE_CLIENTE}}`, `{{EMPRESA_CLIENTE}}`, `{{DIRECCION_CLIENTE}}`, `{{EMAIL_CLIENTE}}`, `{{ARTICULOS_LINEA}}`, `{{SUBTOTAL}}`, `{{PORCENTAJE_DESCUENTO}}`, `{{CANTIDAD_DESCUENTO}}`, `{{CANTIDAD_GRAVABLE}}`, `{{TASA_IMPUESTO}}`, `{{CANTIDAD_IMPUESTO}}`, `{{TOTAL_DEBIDO}}`, `{{NOTAS}}`

Guarda como `plantilla-factura.md` en el mismo directorio. Presenta instrucciones de uso al usuario.

---

## Anti-Patrones

- **NO generes una factura sin verificar primero la matemática** -- cada cantidad debe ser confirmada independientemente
- **NO asumas tasas de impuesto** -- pregunta o default a 0% con descargo de responsabilidad
- **NO fabrique detalles de cuenta de pago** -- solo incluye lo que el usuario proporciona
- **NO reutilices números de factura** -- cada factura necesita un identificador único
- **NO omitas la política de pago tardío** -- cada factura necesita consecuencias por pago tardío
- **NO entregues sin presentar la factura al usuario para revisión primero**
- **NO proporciones asesoramiento fiscal o legal** -- esto genera documentos, no consejería profesional
- **NO incluyas números de cuenta completos** -- usa últimos 4 dígitos para cuentas bancarias
