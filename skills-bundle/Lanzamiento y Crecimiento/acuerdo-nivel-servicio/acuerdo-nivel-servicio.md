---
name: acuerdo-nivel-servicio
description: "Redacta acuerdos de nivel de servicio (SLA) con tiempos de respuesta, compromisos de disponibilidad, estructuras de penalización y créditos, y métricas de rendimiento."
allowed-tools: Read Write Glob
metadata:
  author: Imperio Digital
  version: "1.0"
---

# Acuerdo de Nivel de Servicio

## Cuándo Usar Este Skill

Usa este skill cuando necesites:
- Redactar un acuerdo de nivel de servicio (SLA) para clientes o socios
- Definir tiempos de respuesta, compromisos de disponibilidad y estándares de calidad
- Crear estructuras de penalización y créditos por incumplimiento del SLA
- Formalizar expectativas de servicio en un acuerdo medible

**NO** uses este skill para contratos legales completos (consulta a un abogado), OKRs internos o alcances de proyecto. Esto es para redactar la porción de SLA de una relación comercial.

---

## Principio Fundamental

UN SLA ESTABLECE EL PISO, NO EL TECHO — DEFINE EL NIVEL MÍNIMO ACEPTABLE DE SERVICIO PARA QUE AMBAS PARTES SEPAN EXACTAMENTE QUÉ ESPERAR Y QUÉ SUCEDE CUANDO LAS EXPECTATIVAS NO SE CUMPLEN.

---

## Fase 1: Definir Términos

Establece el alcance y contexto del SLA.

### Información Requerida

| Dato | Qué Preguntar | Valor por Defecto |
|------|--------------|-------------------|
| **Descripción del servicio** | "¿Qué servicio estás proporcionando?" | Sin valor por defecto |
| **Tipo de cliente** | "¿Quién es el cliente? (empresa grande, PyME, consumidor)" | PyME |
| **Modelo de servicio** | "¿Cómo se entrega el servicio? (SaaS, retainer, proyecto, soporte)" | Retainer |
| **Compromisos actuales** | "¿Qué estás prometiendo informalmente actualmente?" | Sin valor por defecto |
| **Pain points** | "¿Qué problemas de servicio han causado fricción con clientes?" | Tiempo de respuesta |
| **Herramientas de medición** | "¿Cómo rastreas el rendimiento del servicio?" | Básico (email, herramienta de proyecto) |

**PUNTO DE CONTROL: Confirma el alcance del servicio antes de redactar el SLA.**

---

## Fase 2: Redactar SLA

Escribe el acuerdo de nivel de servicio.

### Plantilla de SLA

```
# Acuerdo de Nivel de Servicio

**Entre:** [Nombre de Tu Negocio] ("Proveedor")
**Y:** [Nombre del Cliente] ("Cliente")
**Fecha de vigencia:** [Fecha]
**Fecha de revisión:** [Fecha — típicamente anual]

---

## 1. Descripción del Servicio

[2-3 oraciones describiendo el servicio cubierto por este SLA]

## 2. Disponibilidad del Servicio (si aplica)

| Métrica | Compromiso |
|---------|-----------|
| Objetivo de uptime | [99.5% / 99.9%] mensual |
| Ventana de mantenimiento programado | [Día/hora — con aviso de 48 horas] |
| Tiempo de inactividad excluido | [Mantenimiento programado, fuerza mayor, caídas de terceros] |

## 3. Tiempos de Respuesta

| Prioridad | Descripción | Tiempo de Respuesta | Objetivo de Resolución |
|-----------|------------|-------------------|----------------------|
| Crítica | Servicio caído / impacto mayor al negocio | [1 hora] | [4 horas] |
| Alta | Funcionalidad afectada / impacto significativo | [4 horas] | [1 día hábil] |
| Media | Problema menor / hay solución alternativa | [8 horas] | [3 días hábiles] |
| Baja | Pregunta o solicitud de mejora | [1 día hábil] | [5 días hábiles] |

**Horario comercial:** [Horas y zona horaria]
**Soporte fuera de horario:** [Disponible / No disponible / Solo emergencias]

## 4. Métricas de Rendimiento

| Métrica | Objetivo | Método de Medición | Frecuencia de Reporte |
|---------|----------|-------------------|---------------------|
| [Cumplimiento de tiempo de respuesta] | [95%+] | [Seguimiento en herramienta de soporte] | [Mensual] |
| [Puntuación de calidad] | [Objetivo] | [Método de medición] | [Frecuencia] |
| [Puntualidad de entregables] | [95%+] | [Seguimiento en herramienta de proyecto] | [Mensual] |

## 5. Remedios y Créditos

| Incumplimiento del SLA | Crédito / Remedio |
|------------------------|------------------|
| Uptime por debajo del [X]% en un mes | [X]% de crédito en la tarifa mensual |
| Tiempo de respuesta incumplido 3+ veces en un mes | [X]% de crédito o extensión de servicio gratuita |
| Problema crítico sin resolver más allá de [X] horas | [Escalamiento a equipo senior + crédito] |

**Tope de créditos:** Los créditos totales no excederán el [X]% de las tarifas mensuales del servicio.
**Proceso de crédito:** El cliente debe solicitar el crédito dentro de [30] días del incumplimiento.

## 6. Exclusiones

Este SLA no aplica a:
- Problemas causados por acciones del cliente o sistemas de terceros
- Eventos de fuerza mayor
- Mantenimiento programado (con aviso previo)
- Funcionalidades o servicios no cubiertos por el acuerdo

## 7. Reportes

El Proveedor entregará un reporte mensual de servicio que incluya:
- Porcentaje de uptime
- Cumplimiento de tiempos de respuesta
- Problemas abiertos y resueltos
- Cualquier incumplimiento del SLA y remedios aplicados

## 8. Revisión y Enmiendas

Este SLA se revisará [anualmente / en la renovación del contrato]. Los cambios requieren acuerdo escrito de ambas partes.

---

**Firma del Proveedor:** _______________  Fecha: ___
**Firma del Cliente:** _______________  Fecha: ___
```

**PUNTO DE CONTROL: Presenta el borrador del SLA para revisión y negociación.**

---

## Fase 3: Personalizar

Adapta el SLA al servicio y relación específicos.

### Adiciones Específicas por Servicio

**Para SaaS / Productos Digitales:**
- Frecuencia de respaldo de datos y tiempo de recuperación
- Cronograma de notificación de incidentes de seguridad
- Uptime de API y límites de tasa

**Para Retainer / Servicios de Agencia:**
- Límites de revisiones de entregables
- Expectativas de respuesta en comunicación
- Proceso de cambio de alcance

**Para Servicios Administrados:**
- Compromisos de monitoreo proactivo
- Cadencia regular de reportes
- Procedimientos de escalamiento con contactos designados

### Guías para Estructura de Créditos

- Los créditos deben ser lo suficientemente significativos para incentivar el rendimiento pero no para quebrar al proveedor
- Rango típico: 5-25% de la tarifa mensual por tipo de incumplimiento
- Tope de créditos totales al 50-100% de las tarifas de un mes
- Siempre requiere que el cliente solicite los créditos (no los apliques automáticamente)

---

## Fase 4: Operacionalizar

Configura el seguimiento y los reportes para cumplir con los compromisos del SLA.

### Panel de Seguimiento del SLA

```
## Reporte Mensual del SLA — [Mes]

| Métrica | Objetivo | Real | Estado |
|---------|----------|------|--------|
| Uptime | [X]% | [X]% | Cumplido / No cumplido |
| Tiempo promedio de respuesta (Crítica) | [X horas] | [X horas] | Cumplido / No cumplido |
| Puntualidad de entregables | [X]% | [X]% | Cumplido / No cumplido |

**Incumplimientos este mes:** [#]
**Créditos adeudados:** $[X]
**Notas:** [Contexto para cualquier fallo]
```

### Alertas Internas

Configura notificaciones antes de incumplir el SLA:
- Alerta al 50% de la ventana de tiempo de respuesta ("Te quedan 2 horas para este ticket crítico")
- Alerta cuando el uptime se acerca al umbral
- Revisión semanal de cumplimiento del SLA

---

## Anti-Patrones

- **Prometer lo que no puedes cumplir** — establece objetivos que puedas cumplir consistentemente, luego supéralos. Promete poco, entrega mucho.
- **Sin sistema de medición** — un SLA sin seguimiento es solo palabras. Necesitas datos.
- **SLAs excesivamente complejos** — un SLA de 10 páginas para un retainer de $500/mes es excesivo. Ajusta la complejidad a la relación.
- **Sin exclusiones** — sin exclusiones claras, eres responsable por fallas de terceros y actos de la naturaleza.
- **Créditos sin tope** — créditos sin tope pueden arruinar tu negocio en un mal mes. Siempre establece un tope.

---

## Recuperación

- **El cliente exige términos de SLA poco realistas:** Responde con datos sobre estándares de la industria. Ofrece un nivel premium con SLAs más estrictos a un precio mayor.
- **Se incumplió el SLA:** Reconócelo proactivamente, aplica el crédito antes de que te lo pidan, y explica qué estás haciendo para prevenir que se repita.
- **El usuario no tiene herramientas de seguimiento:** Comienza con una hoja de cálculo simple. Rastrea tiempos de respuesta manualmente hasta que el volumen justifique invertir en una herramienta.
- **El cliente nunca lee el SLA:** Revisa los compromisos clave en una reunión. Destaca lo que pueden esperar y cómo reportar problemas.
- **El SLA es demasiado caro de cumplir:** Los objetivos del SLA pueden ser demasiado agresivos, o los precios no contemplan el nivel de servicio requerido. Ajusta uno o ambos.
