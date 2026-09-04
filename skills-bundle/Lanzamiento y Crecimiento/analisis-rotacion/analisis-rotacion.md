---
name: analisis-rotacion
description: "Diagnostica patrones de rotación de clientes y crea estrategias de intervención para retención con señales de advertencia, disparadores de recuperación y guías de prevención. Usa cuando un usuario está perdiendo clientes o suscriptores, quiere entender por qué se van, o necesita reducir la tasa de rotación de una suscripción o servicio recurrente."
allowed-tools: Read Write Glob
metadata:
  author: Imperio Digital
  version: "1.0"
---

# Análisis de Rotación y Planificador de Retención

## Cuándo Usar Esta Competencia

- La tasa de rotación de suscripción o membresía está por encima del promedio industrial
- Los clientes se van y no sabes por qué
- Quieres construir un sistema de alerta temprana para clientes en riesgo
- Estás perdiendo ingresos por cancelaciones más rápido que adquiriendo clientes nuevos
- Necesitas priorizar qué esfuerzos de retención invertir

## Principio Fundamental

**LA ROTACIÓN ES UN SÍNTOMA, NO LA ENFERMEDAD. CADA CLIENTE QUE SE FUE TUVO UN MOMENTO DONDE EL VALOR QUE RECIBÍA CAYÓ POR DEBAJO DEL PRECIO QUE PAGABA. ENCUENTRA ESE MOMENTO.**

## Workflow

### Paso 1: Define el Panorama de Rotación

Pregunta al usuario:
1. ¿Cuál es tu modelo de negocio? (suscripción, membresía, retainer, compra repetida)
2. ¿Cuál es tu tasa de rotación actual? (mensual o anual)
3. ¿Cómo cancelan los clientes? (autoservicio, correo, teléfono, simplemente dejan de comprar)
4. ¿Tienes datos de encuesta de salida o razones de cancelación?
5. ¿Cuál es el tiempo de vida promedio del cliente y el LTV?

**Mínimo necesario: preguntas 1 y 2. Si no conocen la tasa de rotación, ayúdales a calcularla: clientes perdidos este mes / clientes al inicio del mes.**

### Paso 2: Identifica Patrones de Rotación

Analiza por segmento:

| Segmento | Patrón Típico de Rotación | Causa Raíz |
|---------|--------------------------|-----------|
| Rotación temprana (0-30 días) | Nunca se activó o comprometió | Onboarding deficiente, expectativas incumplidas |
| Rotación a mediano plazo (1-6 meses) | Lo usó, luego paró | No encontró valor continuo, encontró alternativa |
| Rotación a largo plazo (6+ meses) | Leal luego se fue de repente | Aumento de precio, mala experiencia, cambio de vida |
| Rotación estacional | Caídas predecibles | Ciclos presupuestarios, relevancia estacional |
| Rotación involuntaria | Fallos de pago | Tarjetas expiradas, fondos insuficientes |

### Paso 3: Construye Señales de Advertencia

Crea un panel de alerta temprana:

| Señal de Advertencia | Nivel de Riesgo | Plazo | Acción |
|-------------------|---------------|-------|--------|
| Sin login/compra en 14 días | Medio | Dispara en día 14 | Envía correo de reactivación |
| Ticket de soporte sin resolver 48+ hrs | Alto | Inmediato | Escala y da seguimiento |
| Plan degradado | Alto | Dentro de 7 días | Contacto personal del gerente de cuenta |
| Uso caído 50%+ del promedio | Alto | Dispara semanalmente | Envía "Te echamos de menos" + recordatorio de valor |
| Pago fallido | Crítico | Mismo día | Secuencia de dunning (3 correos en 7 días) |
| Visualizó página de cancelación | Crítico | Tiempo real | Dispara oferta de retención o ventana de chat |

### Paso 4: Crea Intervenciones de Retención

Para cada segmento de rotación, construye una intervención:

**Prevención de Rotación Temprana:**
- Mejora la incorporación (configuración guiada, ganancias rápidas en primeras 48 horas)
- Envía correos "¿Sabías que?" destacando características no utilizadas
- Asigna compañero de incorporación o llamada de verificación

**Retención a Mediano Plazo:**
- Resúmenes de valor mensuales ("Esto es lo que lograste este mes")
- Anuncios de características vinculadas a su caso de uso
- Invitaciones de participación comunitaria

**Lealtad a Largo Plazo:**
- Reconocimiento y recompensas de aniversario
- Acceso exclusivo a nuevas características o contenido
- Construcción de relación personal (notas manuscritas, regalos sorpresa)

**Recuperación de Rotación Involuntaria:**
- Pre-dunning: Recuerda a los clientes antes de que la tarjeta expire
- Secuencia de dunning: 3 correos en 7 días con enlace fácil de actualización
- Período de gracia: Mantén acceso activo 7 días después del pago fallido

### Paso 5: Entrega Plan de Reducción de Rotación

Proporciona un plan de acción priorizado con impacto esperado.

## Ejemplos

### Ejemplo 1: Herramienta SaaS de Gestión de Proyectos ($29/mes)

**Estado Actual:** Rotación mensual 8.5% (promedio industrial: 5-7%)
**Análisis:**

| Segmento de Rotación | % de Rotación Total | Razón Primaria |
|-------------------|------------------|-----------------|
| Temprana (0-30 días) | 45% | Los usuarios se suscriben pero nunca crean un proyecto |
| Mediano plazo (1-6 meses) | 30% | "Cambié a Notion" o "Demasiado complejo para mis necesidades" |
| Largo plazo (6+ meses) | 10% | Aumentos de precio, recortes presupuestarios |
| Involuntaria | 15% | Pagos fallidos |

**Intervenciones Prioritarias:**

> **#1 — Arregla la Onboarding (objetivo: reduce rotación temprana 50%)**
> - Agrega un asistente "Crea Tu Primer Proyecto" que se completa en 2 minutos
> - Envía correo "Inicio Rápido" 1 hora después del registro con guía de 3 pasos
> - Dispara correo personal del fundador si no se crea proyecto por día 3
> - Impacto esperado: Reduce rotación temprana de 45% a 22% del total, bajando rotación general a ~6.4%
>
> **#2 — Recupera Pagos Fallidos (objetivo: recupera 40% de rotación involuntaria)**
> - Correo 1 (día 0): "Tu pago no pasó — actualiza en 30 segundos" [enlace directo]
> - Correo 2 (día 3): "Tu cuenta está en riesgo — sería triste perderte"
> - Correo 3 (día 7): "Última oportunidad para mantener tu cuenta activa"
> - Mantén cuenta activa con acceso de solo lectura 14 días después del fallo
> - Impacto esperado: Recupera 6% de rotación total, bajando a ~6.0%

### Ejemplo 2: Membresía de Fitness Online ($47/mes)

**Estado Actual:** Rotación mensual 12%
**Razones principales de cancelación (de encuesta de salida):**

| Razón | % | Intervención |
|------|---|-------------|
| "No estoy viendo resultados" | 35% | Agrega check-ins de progreso mensuales + seguimiento antes/después |
| "No tengo tiempo" | 25% | Lanza serie de entrenamientos express de 10 minutos |
| "Demasiado caro" | 20% | Ofrece plan anual a 30% descuento antes de cancelación |
| "Aburrido/repetitivo" | 15% | Libera contenido nuevo semanalmente, envía correo "Nuevo Esta Semana" |
| Otro | 5% | Contacto personal |

**Flujo de Cancelación Salvaguarda:**
> Cuando el miembro hace clic en "Cancelar":
> 1. Muestra: "Antes de irte — ¿cuál es la razón #1?" (selecciona de lista)
> 2. Basado en respuesta, muestra oferta dirigida:
>    - "No viendo resultados" → Sesión 1-a-1 gratis con entrenador
>    - "No tengo tiempo" → "Prueba nuestros nuevos entrenamientos express de 10 min"
>    - "Demasiado caro" → Plan anual a $29/mes (38% ahorros)
>    - "Aburrido" → Vista previa de contenido nuevo que lanza próxima semana
> 3. Si cancela de todas formas: "Guardamos tu progreso. Vuelve en cualquier momento a tu tasa actual."

## Recuperación y Alternativas

- **Usuario no tiene datos de rotación:** Empieza a rastrear hoy. Configura una hoja de cálculo simple: fecha, nombre de cliente, razón para irse, fecha de última actividad. Incluso 30 días de datos revelan patrones.
- **La tasa de rotación parece fina pero los ingresos bajan:** Revisa degradaciones (clientes que se mueven a planes más baratos) — esto es "rotación de ingresos" incluso sin rotación de clientes.
- **Usuario no puede implementar disparadores automatizados:** Empieza con intervenciones manuales. Un correo personal del fundador a clientes en riesgo cuesta nada y tiene la tasa de salvaguarda más alta.
- **La rotación es estacional y predecible:** No luches contra ella. En su lugar, carga los ingresos con planes anuales, descuentos de prepago o empaques estacionales.

## Restricciones

- **NUNCA recomienda descuentos como estrategia primaria de retención** — entrena a los clientes a amenazar cancelación para descuentos
- Enfócate en encontrar y arreglar la brecha de VALOR, no la brecha de PRECIO
- Prioriza intervenciones por facilidad de implementación E impacto esperado
- Siempre separa rotación voluntaria (cliente eligió irse) de rotación involuntaria (fallo de pago)
- Incluye métricas específicas y objetivos para cada intervención
- Las encuestas de salida deben ser 1-2 preguntas máximo — encuestas largas no se completan
