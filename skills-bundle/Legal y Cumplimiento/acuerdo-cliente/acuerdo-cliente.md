---
name: acuerdo-cliente
description: "Redacta acuerdos de servicio al cliente con alcance, entregables, plazos, límites de revisión y términos de pago. Usa cuando crees contratos para compromisos con clientes."
allowed-tools: Read Write Glob
metadata:
  author: Imperio Digital
  version: "1.0"
---

# Acuerdo de Cliente

## Cuándo Usar Este Skill

Usa este skill cuando necesites:
- Redactar un acuerdo de servicio para un compromiso con cliente
- Definir alcance, entregables, plazos y límites de revisión
- Establecer términos de pago, políticas de cancelación y propiedad intelectual
- Crear una plantilla de acuerdo de cliente reutilizable

**NO USES** este skill para acuerdos de contratista (usa independent-contractor-agreement), términos SaaS (usa saas-agreement), o acuerdos de asociación. Esto es para acuerdos donde TÚ proporcionas servicios a un CLIENTE. Haz que un abogado revise antes de usar.

---

## Principio Fundamental

UN ACUERDO DE CLIENTE EXISTE PARA PREVENIR SCOPE CREEP, DISPUTAS DE PAGO Y EXPECTATIVAS DESALINEADAS — CUANTO MÁS CLARA ES LA CARTA, MÁS SUAVE ES EL COMPROMISO.

---

## Fase 1: Detalles del Compromiso

### Información Requerida

| Entrada | Qué Preguntar | Por Defecto |
|---------|---------------|------------|
| **Nombre de tu negocio** | "¿Cuál es tu nombre legal de negocio?" | Sin defecto — debe proporcionarse |
| **Nombre del cliente** | "¿Cuál es el cliente?" | Sin defecto — debe proporcionarse |
| **Servicios** | "¿Qué servicios proporcionarás?" | Sin defecto — debe proporcionarse |
| **Entregables** | "¿Cuáles son los entregables específicos?" | Sin defecto — debe proporcionarse |
| **Línea de tiempo** | "¿Cuál es la línea de tiempo del proyecto?" | Sin defecto — debe proporcionarse |
| **Precios** | "¿Cómo se fija precio? (proyecto, por hora, retención)" | Basado en proyecto |
| **Revisiones** | "¿Cuántas rondas de revisión se incluyen?" | 2 rondas |

**PUNTO DE CONTROL:** No procedas sin servicios, entregables y precios.

---

## Fase 2: Estructura del Acuerdo

```
## Acuerdo de Servicio al Cliente

**Este Acuerdo** se celebra a partir de [Fecha] entre:

**Proveedor de Servicios:** [Nombre Legal del Negocio] ("Proveedor")
**Cliente:** [Nombre/Negocio del Cliente] ("Cliente")

### 1. Servicios

El Proveedor se compromete a realizar los siguientes servicios:

[Descripción detallada de servicios]

### 2. Entregables y Línea de Tiempo

| # | Entregable | Descripción | Fecha de Entrega |
|---|-----------|------------|------------------|
| 1 | [Entregable] | [Descripción específica] | [Fecha] |
| 2 | [Entregable] | [Descripción específica] | [Fecha] |
| 3 | [Entregable] | [Descripción específica] | [Fecha] |

**Fecha de inicio del proyecto:** [Fecha]
**Finalización estimada:** [Fecha]

Las líneas de tiempo están supeditadas a que el Cliente proporcione materiales requeridos y comentarios por fechas acordadas. Los retrasos en las respuestas del Cliente extenderán proporcionalmente la línea de tiempo del proyecto.

### 3. Revisiones

- Se incluyen [2] rondas de revisiones en la tarifa del proyecto
- Una "revisión" se define como cambios en la dirección, contenido o diseño dentro del alcance aprobado
- Se facturan rondas de revisión adicionales a $[X]/hora o $[X] por ronda
- Se consideran revisiones solicitadas más de [30] días después de la presentación del entregable como trabajo nuevo y se cotizan por separado

### 4. Compensación

| Componente | Monto |
|-----------|--------|
| Tarifa del proyecto | $[X] |
| Programa de pagos | [50]% al firmar / [50]% al completar |
| Trabajo adicional (fuera de alcance) | $[X]/hora o cotizado por solicitud |
| Método de pago | [ACH / tarjeta de crédito / cheque] |
| Términos de pago | Debido dentro de [15] días de factura |
| Cargo por pago atrasado | [1.5]% por mes en saldos vencidos |

[Para retenciones:]
Retención mensual de $[X] vencida el [1º] de cada mes. La retención cubre [X] horas de trabajo. Las horas no utilizadas [se transfieren por 1 mes / vencen].
Las horas que exceden la retención se facturan a $[X]/hora.

### 5. Responsabilidades del Cliente

El Cliente se compromete a:
- Proporcionar materiales, contenido, acceso y comentarios necesarios por fechas acordadas
- Designar un único punto de contacto para comunicación y aprobaciones
- Responder a solicitudes de comentarios dentro de [3-5] días hábiles
- Proporcionar aprobación oportuna de entregables

El incumplimiento de estas responsabilidades puede resultar en retrasos de proyecto y cargos adicionales.

### 6. Propiedad Intelectual

**Opción A — Proveedor transfiere PI:**
Al pago completo, todos los derechos de propiedad intelectual en los entregables se transfieren al Cliente. El Proveedor retiene el derecho de mostrar el trabajo en su portafolio a menos que el Cliente lo solicite por escrito.

**Opción B — Proveedor otorga licencia PI:**
El Proveedor retiene la propiedad de todos los entregables y otorga al Cliente una licencia [no exclusiva / exclusiva] para usar los entregables para [propósitos específicos]. El Proveedor retiene derechos de portafolio.

[Selecciona la opción apropiada para el compromiso]

### 7. Confidencialidad

Ambas partes se comprometen a mantener información confidencial privada durante y después del compromiso. La información confidencial incluye estrategias comerciales, datos de clientes, información financiera e información marcada como confidencial. Esta obligación sobrevive [2] años después de la terminación.

### 8. Cancelación y Terminación

**Cancelación del cliente:**
- Antes de que comience el trabajo: Reembolso completo menos [10]% de honorarios administrativos
- Después de que comience el trabajo: El Cliente paga por trabajo completado más [cualquier pago anticipado es no reembolsable]
- Después de [50]% de finalización: El Cliente paga por trabajo completado; sin reembolso de pago anticipado

**Cancelación del proveedor:**
- El Proveedor puede terminar con [14] días de notificación
- El Cliente recibe todo el trabajo completado y un reembolso por servicios no realizados

**Para retenciones:**
Cualquiera de las partes puede cancelar con [30] días de notificación escrita. Sin reembolso de la retención del mes actual.

### 9. Limitación de Responsabilidad

La responsabilidad total del Proveedor no excederá el total de honorarios pagados según este Acuerdo. El Proveedor no es responsable de daños indirectos, consecuentes o incidentales, incluyendo pérdida de ganancias o ingresos.

### 10. Indemnificación

El Cliente indemnizará al Proveedor contra reclamaciones que surjan de materiales del Cliente, instrucciones o uso de los entregables de manera no contemplada por este Acuerdo.

### 11. Resolución de Disputas

Las disputas se resolverán mediante [mediación / arbitraje] en [jurisdicción] antes de que cualquiera de las partes pueda perseguir litigio.

### 12. Disposiciones Generales

- **Acuerdo Completo:** Este es el acuerdo completo.
- **Enmiendas:** Requieren acuerdo escrito de ambas partes.
- **Ley Aplicable:** Leyes de [Estado].
- **Fuerza Mayor:** Ninguna parte es responsable por retrasos debido a circunstancias más allá del control razonable.

---

**Proveedor:**
Firma: _______________ Fecha: _______________

**Cliente:**
Firma: _______________ Fecha: _______________
```

---

## Fase 3: Anexo de Alcance de Trabajo

```
## Anexo A: Alcance de Trabajo

### Resumen del Proyecto
[Descripción detallada del proyecto]

### Dentro del Alcance
- [Elemento específico 1]
- [Elemento específico 2]
- [Elemento específico 3]

### Fuera del Alcance
- [Elemento explícitamente no incluido 1]
- [Elemento explícitamente no incluido 2]

### Suposiciones
- [Suposición sobre herramientas, acceso o materiales]
- [Suposición sobre línea de tiempo o disponibilidad]

### Proceso de Orden de Cambio
Cualquier trabajo fuera del alcance definido requiere una orden de cambio escrita firmada por ambas partes antes de que comience el trabajo. Las órdenes de cambio incluirán alcance, línea de tiempo y costo del trabajo adicional.
```

---

## Fase 4: Finalización

```
## Lista de Verificación del Acuerdo

- [ ] El alcance de trabajo es específico y medible
- [ ] Los entregables están claramente definidos con fechas de vencimiento
- [ ] El programa y monto de pagos son claros
- [ ] Se indican los límites de revisión
- [ ] La propiedad intelectual se aborda explícitamente
- [ ] Los términos de cancelación protegen ambas partes
- [ ] Se definen las responsabilidades del Cliente
- [ ] Se enumeran los elementos fuera del alcance para prevenir scope creep
- [ ] Ambas partes han firmado
- [ ] El acuerdo fue revisado por asesoría legal
```

---

## Ejemplo: Consultor de Estrategia de Marca

**Servicios:** Posicionamiento de marca, marco de mensajería y guía de identidad visual. **Entregables:** Informe de auditoría de marca (Semana 2), declaración de posicionamiento y marco de mensajería (Semana 4), guía de identidad visual (Semana 6). **Tarifa:** $5,000 — $2,500 por adelantado, $2,500 al final. **Revisiones:** 2 rondas por entregable. **PI:** Se transfiere al cliente al pago completo. **Cancelación:** Depósito no reembolsable después de la Semana 1.

---

## Anti-Patrones

- **Sin alcance de trabajo** — "ayuda con marketing" no es un alcance. Sin entregables específicos, scope creep es garantizado.
- **Sin pago antes de que comience el trabajo** — siempre cobra un depósito. Confirma compromiso y protege contra falta de pago.
- **Revisiones ilimitadas** — "revisiones hasta que estés feliz" suena generoso pero conduce a ciclos infinitos. Establece un número.
- **Sin lista de fuera del alcance** — indicar explícitamente qué NO se incluye previene suposiciones.
- **Acuerdos verbales para algo que supere $500** — ponlo por escrito. Siempre.

---

## Recuperación

- **Cliente solicitando trabajo fuera del alcance:** Referencia el acuerdo, señala la lista fuera del alcance, y propone una orden de cambio con costo y línea de tiempo adicionales.
- **Cliente no respondiendo a solicitudes de comentarios:** Envía un recordatorio citando la línea de tiempo de respuesta del acuerdo. Documenta retrasos. Después de [10] días hábiles, coloca el proyecto en espera con notificación escrita.
- **El pago está atrasado:** Sigue los términos de pago atrasado en el acuerdo. Envía recordatorios a 1, 7 y 14 días de atraso. Pausa el trabajo a 15+ días de atraso.
- **Sin acuerdo firmado y trabajo ya comenzó:** Detente y obten la firma inmediatamente. Incluso un email simple con términos clave confirmados por ambas partes es mejor que nada.
