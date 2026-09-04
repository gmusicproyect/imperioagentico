---
name: plan-recuperacion-servicio
description: "Diseña protocolos de recuperación de servicio para cuando las cosas salen mal, con guiones de respuesta, pautas de compensación y procedimientos de seguimiento."
allowed-tools: Read Write Glob
metadata:
  author: Imperio Digital
  version: "1.0"
---

# Plan de Recuperación de Servicio

## Cuándo Usar Este Skill

Usa este skill cuando necesites:
- Diseñar protocolos proactivos para recuperarse de fallos de servicio
- Crear guiones de respuesta y pautas de compensación para diferentes tipos de fallo
- Construir procedimientos de seguimiento que conviertan fallos de servicio en oportunidades de lealtad
- Estandarizar cómo tu negocio maneja las cosas cuando salen mal

**NO** uses este skill para respuestas individuales a quejas (usa resolucion-quejas), comunicación de crisis o planificación de continuidad de negocio. Esto es para diseñar el sistema general de recuperación de servicio.

---

## Principio Fundamental

LA PARADOJA DE LA RECUPERACIÓN DE SERVICIO ES REAL — LOS CLIENTES QUE EXPERIMENTAN UN FALLO QUE SE RECUPERA BIEN A MENUDO SE VUELVEN MÁS LEALES QUE LOS CLIENTES QUE NUNCA TUVIERON UN PROBLEMA.

---

## Fase 1: Inventario de Fallos

Identifica qué puede salir mal y con qué frecuencia ocurre.

### Información Requerida

| Dato | Qué Preguntar | Predeterminado |
|------|---------------|----------------|
| **Tipo de negocio** | "¿Qué producto o servicio proporcionas?" | Sin predeterminado |
| **Fallos comunes** | "¿Cuáles son las 5 cosas principales que salen mal para los clientes?" | Sin predeterminado |
| **Recuperación actual** | "¿Cómo manejas las cosas cuando salen mal hoy?" | Ad hoc |
| **Presupuesto de compensación** | "¿Qué puedes permitirte ofrecer cuando fallas? (reembolsos, créditos, trabajo gratis)" | Flexible |
| **Incidentes pasados** | "Describe el peor fallo de servicio que hayas experimentado." | Sin predeterminado |

### Clasificación de Fallos

```
## Tipos de Fallo de Servicio

| Tipo de Fallo | Severidad | Frecuencia | Impacto en el Cliente | Ejemplo |
|--------------|----------|-----------|----------------------|---------|
| Retraso de entrega | Medio | [A/M/B] | Inconveniente | Entregable 3 días tarde |
| Problema de calidad | Alto | [A/M/B] | Retrabajo o insatisfacción | Entregable no cumple el brief |
| Brecha de comunicación | Bajo-Medio | [A/M/B] | Confusión o frustración | Sin actualización por 1 semana |
| Error de facturación | Medio | [A/M/B] | Impacto financiero | Cobro excesivo o doble cobro |
| Fallo completo | Crítico | [Bajo] | Impacto mayor al negocio | Servicio no entregado en absoluto |
```

**PUNTO DE CONTROL: Confirma el inventario de fallos antes de construir planes de recuperación.**

---

## Fase 2: Protocolos de Recuperación

Diseña procedimientos específicos de recuperación para cada tipo de fallo.

### Marco de Recuperación: EAER

```
## Modelo de Recuperación EAER

### E — Escuchar
Deja que el cliente describa su experiencia completamente. No interrumpas ni te defiendas.
"Ayúdame a entender exactamente qué pasó."

### A — Aceptar
Valida su experiencia y toma responsabilidad.
"Tienes razón — no entregamos lo que prometimos y asumo total responsabilidad."

### E — Ejecutar
Entrega una solución específica con un cronograma.
"Esto es exactamente lo que voy a hacer y cuándo: [acción] para [fecha]."

### R — Recuperación Plus
Ve más allá de arreglar el problema. Entrega valor inesperado.
"Además de [la solución], también voy a [gesto adicional]."
```

### Protocolo de Recuperación por Tipo de Fallo

```
## Protocolos de Recuperación

### Retraso de Entrega
**Reconocer dentro de:** 2 horas de conocerse el retraso
**Guión de respuesta:** "Quiero ser transparente — tu [entregable] se retrasará [X días] de lo prometido. Es mi responsabilidad. Aquí está el nuevo cronograma: [fecha]. [Compensación si corresponde]."
**Compensación:** 10-15% de descuento en proyecto actual, o prioridad de agenda para el siguiente proyecto
**Seguimiento:** Día de entrega + 3 días después

### Problema de Calidad
**Reconocer dentro de:** El mismo día que se reporta
**Guión de respuesta:** "Gracias por señalar esto. La calidad no está donde debería. Voy a [rehacer/revisar] esto y tendré una versión mejorada para ti el [fecha]."
**Compensación:** Revisión gratuita + 10% de crédito en el siguiente proyecto
**Seguimiento:** Después de entregar revisión + 1 semana después

### Brecha de Comunicación
**Reconocer dentro de:** 4 horas
**Guión de respuesta:** "No deberías haber tenido que perseguirme por una actualización. Me disculpo por el silencio. Aquí está el estado actual: [actualización]. De ahora en adelante, voy a [nuevo compromiso de comunicación]."
**Compensación:** Generalmente no necesaria — la comunicación mejorada es la recuperación
**Seguimiento:** Actualización proactiva dentro de 48 horas

### Error de Facturación
**Reconocer dentro de:** El mismo día
**Guión de respuesta:** "Tienes razón — hubo un error de facturación. He [corregido / emitido un reembolso] inmediatamente. Deberías ver [monto] de vuelta en tu cuenta dentro de [plazo]."
**Compensación:** Reembolso + pequeño crédito por la inconveniencia
**Seguimiento:** Confirmar reembolso recibido dentro de 3 días

### Fallo Completo
**Reconocer dentro de:** Inmediatamente
**Guión de respuesta:** "Necesito ser honesto contigo — [lo que pasó]. No hay excusa. Esto es lo que estoy haciendo: [remedio completo]. [Compensación significativa]."
**Compensación:** Reembolso completo + rehacer sin costo O reembolso completo + crédito adicional
**Seguimiento:** Llamada personal dentro de 48 horas + verificación a 1 semana + verificación a 30 días
```

**PUNTO DE CONTROL: Presenta los protocolos de recuperación para revisión.**

---

## Fase 3: Pautas de Compensación

Define qué ofrecer y cuándo.

### Matriz de Compensación

```
## Pautas de Compensación

| Severidad | Nuestra Culpa (100%) | Responsabilidad Compartida | Inconveniente Menor |
|----------|---------------------|---------------------------|-------------------|
| Baja | Disculpa + solución expedita | Disculpa + solución | Disculpa |
| Media | Solución + 10-20% crédito | Solución + 10% crédito | Solución + gesto de buena voluntad |
| Alta | Solución + 25-50% reembolso | Solución + 15-25% reembolso | Solución + 10% crédito |
| Crítica | Reembolso completo + rehacer gratis | Reembolso completo | Reembolso parcial + solución |
```

### Reglas de Compensación

- Siempre arregla el problema PRIMERO, luego discute la compensación
- Ofrece compensación proactivamente — no esperes a que el cliente la exija
- Nunca ofrezcas más que el valor total del proyecto/suscripción
- Compensación monetaria por impacto monetario; compensación de tiempo por tiempo perdido
- Documenta toda compensación para seguimiento financiero

---

## Fase 4: Prevención y Medición

Usa datos de recuperación para prevenir fallos futuros.

### Prevención de Fallos

Después de cada incidente recuperado, documenta:
```
## Revisión Post-Incidente

**Fallo:** [Qué pasó]
**Causa raíz:** [Por qué pasó]
**Recuperación ejecutada:** [Qué se hizo]
**Resultado con el cliente:** [Retenido / Perdido / Lealtad mejorada]
**Acción preventiva:** [Qué cambios para prevenir recurrencia]
**Responsable:** [Quién implementa el cambio]
**Fecha límite:** [Cuándo]
```

### Métricas de Recuperación

```
## Dashboard de Recuperación de Servicio

| Métrica | Objetivo | Actual |
|---------|----------|--------|
| Tiempo promedio de reconocimiento | Menos de [X horas] | — |
| Tiempo promedio de resolución | Menos de [X días] | — |
| Tasa de satisfacción de recuperación | 80%+ | — |
| Retención de clientes después de fallo | 85%+ | — |
| Tasa de fallos repetidos (mismo tipo) | Decreciente | — |
```

### Revisión Trimestral de Recuperación

1. ¿Cuántos fallos de servicio ocurrieron?
2. ¿Qué tipos son más comunes?
3. ¿Cuál es la tasa de retención después de la recuperación?
4. ¿Las acciones preventivas están reduciendo las tasas de fallo?
5. ¿El presupuesto de compensación está dentro de lo planeado?

---

## Anti-Patrones

- **Negar el fallo** — los clientes saben cuando algo salió mal. La negación insulta su inteligencia y mata la confianza.
- **Sobre-compensar** — regalar todo por un retraso menor entrena a los clientes a esperar compensación excesiva.
- **Sub-compensar** — un 5% de descuento por un fallo catastrófico es insultante. Iguala la recuperación al impacto.
- **Sin seguimiento** — arreglar el problema sin dar seguimiento deja la relación en el limbo. Cierra el ciclo.
- **Mismo fallo repitiéndose** — si el mismo fallo pasa 3+ veces, el plan de recuperación no es el problema — el proceso lo es.

---

## Recuperación

- **El usuario nunca ha construido un plan de recuperación:** Comienza con el tipo de fallo más común. Un protocolo es mejor que ninguno.
- **El cliente rechaza la oferta de recuperación:** Pregunta qué lo haría correcto para ellos. A veces no se trata de compensación — se trata de ser escuchado.
- **El usuario no puede pagar compensación monetaria:** Ofrece recuperación no monetaria: servicio prioritario, atención personal, tiempo de consulta gratuito, acceso anticipado a nuevas funciones.
- **La recuperación falló y el cliente se va:** Realiza una salida elegante. Pide feedback, discúlpate sinceramente y deja la puerta abierta. Algunos clientes regresan después.
- **El equipo no sigue los protocolos de recuperación:** Practica escenarios durante reuniones de equipo. Haz los protocolos accesibles (no enterrados en un documento que nadie lee).
