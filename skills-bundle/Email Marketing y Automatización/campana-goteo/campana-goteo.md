---
name: campana-goteo
description: "Construye campañas de goteo de nutrición con lógica condicional, disparadores de lead scoring y mapeo de contenido por etapa. Úsalo cuando necesites secuencias de email automatizadas que muevan leads a través de tu funnel basado en comportamiento."
allowed-tools: Read Write Glob
metadata:
  author: Imperio Digital
  version: "1.0"
---

# Campaña de Goteo

## Cuándo Usar Este Skill

Usa este skill cuando necesites:
- Construir una secuencia automatizada de email de nutrición que mueva leads hacia una compra
- Diseñar rutas de lógica condicional basadas en comportamiento de suscriptor (aperturas, clics, compras)
- Mapear contenido a cada etapa del customer journey dentro de una secuencia de email
- Configurar disparadores de lead scoring que avancen o redirijan suscriptores

**NO** uses este skill para emails de broadcast único, emails transaccionales (confirmaciones de pedido, recibos), o secuencias SMS. Esto es para campañas de email automatizadas de múltiples pasos con lógica de ramificación.

---

## Principio Fundamental

CADA CAMPAÑA DE GOTEO DEBE MOVER AL SUSCRIPTOR MÁS CERCA DE UNA ACCIÓN ESPECÍFICA — CADA EMAIL GANA PERMISO PARA ENVIAR EL SIGUIENTE ENTREGANDO PRIMERO VALOR.

---

## Fase 1: Resumen de Campaña

Antes de construir cualquier secuencia, recopila los inputs que definen la estructura y objetivos de la campaña.

### Entradas Requeridas

Pregunta al usuario para cada una. Si no proporciona una, usa el valor por defecto.

| Entrada | Qué Preguntar | Por Defecto |
|-------|------------|---------|
| **Objetivo de campaña** | "¿Qué acción deben tomar los suscriptores al final?" | Sin valor por defecto — debe ser proporcionado |
| **Disparador de entrada** | "¿Cómo entran las personas en esta secuencia? (opt-in, compra, etiqueta, etc.)" | Opt-in de email vía lead magnet |
| **Etapa de audiencia** | "¿Estos son leads en frío, warm leads, o clientes existentes?" | Warm leads (optaron pero no compraron) |
| **Número de emails** | "¿Cuántos emails en la secuencia?" | 5-7 emails |
| **Cadencia de envío** | "¿Con qué frecuencia deben enviarse los emails?" | Cada 2-3 días |
| **Plataforma de email** | "¿Qué herramienta de email usas?" | Agnóstica a plataforma |

### Plantilla de Resumen

Presenta esto antes de pasar a Fase 2:

```
## Resumen de Campaña de Goteo

**Objetivo de campaña:** Comprar el curso de $297
**Disparador de entrada:** Descargó guía PDF gratis
**Etapa de audiencia:** Warm leads — interesados pero no comprometidos
**Largo de secuencia:** 7 emails en 18 días
**Cadencia:** Días 0, 2, 5, 8, 11, 14, 18
**Plataforma:** ConvertKit
**Lead scoring:** +5 por apertura, +10 por clic, +25 por visita a página de precios
```

**PUNTO DE CONTROL: No procedes a Fase 2 hasta que el usuario confirme o ajuste el resumen.**

---

## Fase 2: Mapa de Secuencia

Construye la arquitectura completa de la campaña antes de escribir copias de email.

### Reglas de Mapa de Secuencia

1. **Cada email tiene un trabajo único** — educar, construir confianza, crear deseo, o pedir la venta
2. **Las ramas condicionales** deben dispararse en acciones medibles (abierto, clic, página visitada, score arriba del threshold)
3. **Los thresholds de lead scoring** determinan cuándo un suscriptor se mueve a una ruta enfocada en ventas
4. **Las condiciones de salida** eliminan suscriptores que convierten o se desvinculan

---

## Fase 3: Escribir Copias de Email

### Estructura de Email de Goteo

Cada email sigue uno de estos patrones:

**Email de Educación** — entrega un insight o recurso valioso
- Trabaja al construir credibilidad
- Sin CTA de venta
- Abre la siguiente email

**Email de Historia** — construye conexión emocional
- Comparte un caso de estudio o beneficio
- Pequeño CTA (aprende más, lee caso de estudio)
- Califica a los interesados

**Email de Objeción** — elimina barreras finales
- Aborda precio, confianza, o timing
- Proporciona social proof o garantía
- Abre la puerta a ventas

**Email de Venta** — pide la acción final
- Claro CTA para comprar
- Uso de urgencia o escasez
- Respaldo de los emails anteriores

---

## Fase 4: Lead Scoring y Lógica

### Scoring Framework

```
| Acción | Puntos |
|--------|--------|
| Abre email | +5 |
| Clic en enlace | +10 |
| Visita página de precios | +25 |
| Visita página de testimonios | +15 |
| Abre email de objeción | +10 |

Threshold 1: 20+ puntos → Envía secuencia de venta
Threshold 2: <10 puntos después de email 5 → Pausar y re-tag
```

### Condiciones de Salida

- Compra realizada → elimina de secuencia
- Abre email + clic en landing page → acelera a email de venta
- Sin apertura en 7 días → pausa, re-engagement después de 14 días
- 3+ bounces → elimina de lista

---

## Anti-Patrones

- **Emails sin valor** — no hagas fluff. Cada email debe entregar algo.
- **Sin lógica condicional** — enviar los mismos 7 emails a todos es spray and pray.
- **Cadencia inconsistente** — "a veces cada 2 días, a veces cada semana" confunde y reduce engagement.
- **Sin condición de salida** — mantener suscriptores en secuencia después de comprar se siente spammy.
- **Scoring demasiado complejo** — 5-7 acciones máximo. Más que eso no escala.

---

## Recuperación

- **Bajo engagement:** Verifica la semana 1. Si no abren los primeros 2 emails, el problema es de entrega o línea de asunto.
- **Conversión baja:** El problema usualmente es timing. La secuencia es demasiado larga o muy corta.
- **Alto unsubscribe:** Verifica la cadencia. Cada 2-3 días es estándar; cada día se siente agresivo.
- **Leads dicen que "no sabían" qué era el email:** Tu línea de asunto o entrada no preframó claramente el tema.
