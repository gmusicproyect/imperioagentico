---
name: flujo-incorporacion
description: "Diseña flujos de onboarding de clientes con pasos de bienvenida, disparadores de hitos y puntos de control de éxito para reducir el churn y acelerar el tiempo hasta el valor."
allowed-tools: Read Write Glob
metadata:
  author: Imperio Digital
  version: "1.0"
---

# Flujo de Onboarding

## Cuándo Usar Este Skill

Usa este skill cuando necesites:
- Diseñar una secuencia de onboarding de clientes desde la compra hasta el primer éxito
- Crear emails de bienvenida, disparadores de hitos y puntos de control de éxito
- Reducir el churn temprano ayudando a los clientes a llegar al valor más rápido
- Estandarizar la experiencia post-compra

**NO** uses este skill para onboarding de empleados (usa checklist-incorporacion), embudos de venta o demos de producto. Esto es para la experiencia DESPUÉS de que alguien se convierte en cliente.

---

## Principio Fundamental

EL OBJETIVO DE LA INCORPORACIÓN NO ES ENSEÑAR TODO — ES LLEVAR AL CLIENTE A SU PRIMERA VICTORIA LO MÁS RÁPIDO POSIBLE, PORQUE LAS VICTORIAS TEMPRANAS CREAN RETENCIÓN.

---

## Fase 1: Definir el Éxito

Identifica cómo luce el éxito del cliente antes de diseñar el flujo.

### Información Requerida

| Dato | Qué Preguntar | Predeterminado |
|------|---------------|----------------|
| **Producto/servicio** | "¿Qué acaba de comprar el cliente?" | Sin predeterminado |
| **Primera victoria** | "¿Cuál es el primer momento de éxito para un nuevo cliente?" | Sin predeterminado |
| **Tiempo hasta el valor** | "¿Qué tan rápido debería el cliente experimentar esa primera victoria?" | Dentro de 7 días |
| **Onboarding actual** | "¿Qué pasa después de que alguien compra hoy?" | Solo email de bienvenida |
| **Puntos de abandono** | "¿Dónde se atascan o dejan de interactuar los nuevos clientes?" | Sin predeterminado |
| **Método de entrega** | "¿Cómo entregas? (autoservicio, hecho-contigo, hecho-para-ti)" | Autoservicio |

**PUNTO DE CONTROL: Confirma la definición de primera victoria antes de diseñar el flujo.**

---

## Fase 2: Mapear el Flujo

Diseña la secuencia de incorporación paso a paso.

### Plantilla del Flujo de Onboarding

```
## Flujo de Onboarding del Cliente: [Nombre del Producto/Servicio]

**Objetivo:** Llevar al cliente a [primera victoria] dentro de [plazo]

### Paso 1: Bienvenida (Inmediato — dentro de minutos de la compra)
**Disparador:** Compra confirmada
**Acción:** Enviar email de bienvenida
**Contenido:**
- Agradecerles y confirmar lo que compraron
- Establecer expectativas (qué sigue, cuándo esperarlo)
- Proporcionar UNA primera acción clara (no cinco)
- Incluir contacto de soporte para preguntas

### Paso 2: Inicio Rápido (Día 1)
**Disparador:** Email de bienvenida abierto o 24 horas post-compra
**Acción:** [Enviar guía de inicio rápido / Agendar llamada de inicio / Dar acceso]
**Contenido:**
- El camino más simple a la primera victoria
- Eliminar toda fricción (plantillas pre-llenadas, configuración predeterminada, paso 1 de 3)
- Video tutorial si aplica

### Paso 3: Primer Hito (Día 2-3)
**Disparador:** El cliente completa la primera acción O pasan 48 horas
**Acción:** Email o mensaje de seguimiento
**Contenido:**
- Si completaron la acción: celebrar y guiar al siguiente paso
- Si no: recordatorio gentil con oferta de ayuda "¿estás atascado?"

### Paso 4: Primera Victoria (Día 3-7)
**Disparador:** El cliente alcanza la primera métrica de éxito
**Acción:** Mensaje de felicitaciones + próximos pasos
**Contenido:**
- Reconocer la victoria
- Mostrar lo que es posible después
- Introducir funciones avanzadas o valor de siguiente nivel

### Paso 5: Formación de Hábito (Día 7-30)
**Disparador:** Basado en tiempo o uso
**Acción:** Secuencia de engagement continuo
**Contenido:**
- Tips, casos de uso e historias de éxito
- Funciones destacadas que no han usado
- Invitación a comunidad o recursos avanzados
```

**PUNTO DE CONTROL: Presenta el flujo para revisión antes de escribir el contenido real.**

---

## Fase 3: Escribir Contenido

Crea los mensajes y materiales específicos para cada paso.

### Plantilla de Email de Bienvenida

```
Asunto: ¡Estás dentro! Aquí está tu primer paso

Hola [Nombre],

¡Bienvenido/a a [Producto/Servicio]!

Esto es exactamente lo que debes hacer ahora:

**Paso 1:** [Acción única y clara con enlace]

Eso es todo. Haz esa única cosa y [beneficio] para [plazo].

Si te atascas, responde a este email — leo todos.

[Nombre]

P.D. [Establecer expectativa del siguiente contacto: "Mañana te enviaré..."]
```

### Plantilla de Email de Seguimiento

```
Asunto: Verificación rápida — ¿hiciste [acción]?

Hola [Nombre],

Solo verificando — ¿tuviste oportunidad de [acción específica del onboarding]?

**Si sí:** ¡Genial! Tu siguiente paso es [siguiente acción + enlace].

**Si no:** Sin problema. Aquí está la forma más fácil de empezar:
[Instrucción simplificada de 1-2 oraciones]

La mayoría de los clientes que [completan este paso] ven [beneficio específico] dentro de [plazo].

¿Necesitas ayuda? [Enlace de soporte u opción de respuesta]

[Nombre]
```

### Plantilla de Celebración de Hito

```
Asunto: ¡Lo lograste! — [logro específico]

Hola [Nombre],

Acabas de [hito específico]. Eso es muy importante.

Esto es lo que hacen los clientes como tú después:
1. [Siguiente función o acción]
2. [Caso de uso avanzado]

Sigue así — estás construyendo impulso.

[Nombre]
```

---

## Fase 4: Optimizar

Configura seguimiento y mejora continua.

### Métricas de Onboarding

```
## Dashboard de Onboarding

| Métrica | Objetivo | Actual |
|---------|----------|--------|
| Tasa de apertura de email de bienvenida | 70%+ | — |
| Tasa de completación de primera acción | 50%+ dentro de 48 horas | — |
| Tiempo hasta primera victoria | [X días] | — |
| Tasa de retención a 30 días | 85%+ | — |
| Tickets de soporte durante incorporación | Decreciente | — |
```

### Análisis de Abandono

En cada paso, rastrea cuántos clientes pasan al siguiente paso. Arregla primero el paso con mayor abandono.

### Revisión Trimestral

1. ¿Dónde se atascan los clientes?
2. ¿Qué preguntas surgen repetidamente? (Agrega respuestas a la incorporación)
3. ¿Qué tan rápido llegan los clientes a la primera victoria vs. objetivo?
4. ¿Qué tienen en común los clientes retenidos durante la incorporación?

---

## Anti-Patrones

- **Bombardeo de información el Día 1** — enviar una guía de 10 páginas abruma. Una acción por punto de contacto.
- **Sin primera acción** — decir "explora la plataforma" no es una acción. "Haz clic aquí para crear tu primer [X]" sí lo es.
- **Onboarding genérica** — si es posible, personaliza por caso de uso, nivel de plan u objetivo declarado.
- **Sin seguimiento después de la bienvenida** — un email no es incorporación. Los primeros 7-30 días necesitan una secuencia diseñada.
- **Asumir que los clientes lo descubrirán** — no lo harán. Se irán. Guíalos explícitamente.

---

## Recuperación

- **Los clientes no abren los emails de bienvenida:** Mejora la línea de asunto, envía desde un nombre personal (no "noreply") y prueba la hora de envío.
- **Los clientes completan la incorporación pero aún se van:** La primera victoria puede no ser lo suficientemente significativa. Redefine cómo luce el éxito.
- **El usuario no tiene herramienta de automatización de email:** Comienza con emails manuales para los primeros 10 clientes. Las plantillas hacen esto factible. Automatiza una vez que el flujo esté probado.
- **El producto es muy complejo para incorporación de 7 días:** Extiende el plazo pero mantén la primera victoria dentro de 48 horas. El impulso temprano importa más que el entrenamiento completo.
- **El usuario vende un producto único (no suscripción):** La incorporación aún importa — impulsa reseñas, referidos y compras repetidas. Enfócate en ayudarles a USAR lo que compraron.
