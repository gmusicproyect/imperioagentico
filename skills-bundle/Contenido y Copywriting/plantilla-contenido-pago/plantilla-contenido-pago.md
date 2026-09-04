---
name: plantilla-contenido-pago
description: "Escribe copia de página de donaciones con urgencia, encuadre de impacto, ánimo de donaciones recurrentes, y señales de confianza."
allowed-tools: Read Write Glob
metadata:
  author: Imperio Digital
  version: "1.0"
---

# Copia de Página de Donaciones

## Cuándo Usar Esta Habilidad

Usa esta habilidad cuando necesites:
- Escribir copia para una página de donaciones en línea que convierta visitantes en donadores
- Crear niveles de donación encuadrados de impacto con elementos de urgencia y confianza
- Optimizar una página de donaciones existente para mayor conversión y donaciones recurrentes
- Construir copia de página de donaciones para campañas, impulsos de fin de año, o donaciones siempre activas

**NO** uses esta habilidad para cartas de recaudación de fondos, solicitudes de subvenciones, o campañas de crowdfunding. Esto es específicamente para la página de donaciones donde ocurre la transacción.

---

## Principio Fundamental

UNA PÁGINA DE DONACIONES TIENE UN TRABAJO: ELIMINAR CADA BARRERA ENTRE EL DESEO DEL VISITANTE DE AYUDAR Y LA TRANSACCIÓN COMPLETADA — CADA PALABRA DEBE CREAR CONFIANZA O REDUCIR FRICCIÓN.

---

## Fase 1: Análisis Inicial

### Entradas Requeridas

| Entrada | Qué Preguntar | Predeterminado |
|-------|------------|---------|
| **Organización** | "¿Cuál es la organización y misión?" | No hay predeterminado — debe proporcionarse |
| **Tipo de página** | "¿Página de donaciones siempre activa o específica de campaña?" | Siempre activa |
| **Niveles de donación** | "¿Qué montos de donación quieres sugerir?" | $25, $50, $100, $250 |
| **Declaraciones de impacto** | "¿Qué logra cada monto de dólar?" | No hay predeterminado — debe proporcionarse |
| **Donación recurrente** | "¿Quieres alentar donaciones mensuales?" | Sí |
| **Señales de confianza** | "¿Tienes calificaciones, certificaciones o insignias de transparencia? (GuideStar, Charity Navigator)" | Ninguna disponible |

**PUNTO DE CONTROL: Confirma el análisis inicial antes de escribir.**

---

## Fase 2: Estructura de Página

### Arquitectura de Página de Donaciones

```
1. Titular — emocional, orientado a beneficio, 8 palabras o menos
2. Sub-titular — una oración expandiendo el titular
3. Declaración de impacto — qué logran las donaciones (2-3 oraciones)
4. Niveles de donación — montos preestablecidos con descripciones de impacto
5. Alternancia de donación recurrente — opción de donaciones mensuales con encuadre
6. Monto personalizado — opción para donadores que quieren un monto diferente
7. Señales de confianza — calificaciones, datos de transparencia, insignias de seguridad
8. Formulario de información del donador — nombre, email, pago (mantén mínimo)
9. Opción de dedicación/tributo — dona en honor de alguien
10. Social proof — conteo de donadores, regalos recientes, testimonios
```

### Diseño de Nivel de Donación

```
| Monto | Declaración de Impacto | Predeterminado Recomendado |
|--------|-----------------|-------------------|
| $25 | [Resultado tangible] | |
| $50 | [Resultado tangible] | Sí (preseleccionado) |
| $100 | [Resultado tangible] | |
| $250 | [Resultado tangible] | |
| Otro | "Ingresa tu monto" | |
```

Preselecciona la opción del medio. Ancla las expectativas sin intimidar.

**PUNTO DE CONTROL: Presenta la estructura de página para aprobación.**

---

## Fase 3: Escritura

### Elementos de Copia

**Opciones de Titular (elige una):**
- "Da [Resultado] a [Beneficiario]"
- "Tu Regalo Cambia Todo para [Beneficiario]"
- "[Número] [Personas] Están Contando Contigo"

**Sub-titular:**
Una oración que conecte la acción del donador con el resultado. "Cuando donas hoy, [impacto específico]."

**Sección de Impacto:**
```
Cada dólar que das va directamente a [misión]. Aquí está lo que tu regalo hace posible:

$25 — [Resultado específico y tangible]
$50 — [Resultado específico y tangible]
$100 — [Resultado específico y tangible]
$250 — [Resultado específico y tangible]
```

**Encuadre de Donación Recurrente:**
```
## Conviértete en un Donador Mensual
Los regalos mensuales proporcionan financiamiento estable que nos permite planificar y servir más [beneficiarios].

$25/mes = $300/año = [impacto anual]
$50/mes = $600/año = [impacto anual]

Los donadores mensuales reciben: [actualizaciones de impacto trimestrales, contenido exclusivo, reconocimiento]
```

**Sección de Señales de Confianza:**
```
## Tu Regalo Es Seguro y Efectivo
- [X]% de fondos van directamente a programas
- [Calificación/certificación si está disponible]
- Procesamiento de pago seguro a través de [Stripe/PayPal]
- Deducible de impuestos — recibirás un recibo inmediatamente
```

**Social Proof:**
```
Únete a [X] donadores que ya han donado este [mes/año].
"[Breve testimonio de donador sobre por qué dona]" — [Nombre, Ciudad]
```

---

## Fase 4: Pulido

### 1. Optimización de Conversión

```
## Lista de Verificación de Optimización de Página

- [ ] La página carga en menos de 3 segundos
- [ ] El formulario tiene 5 o menos campos (nombre, email, monto, pago)
- [ ] El monto preseleccionado es el nivel medio
- [ ] La donación mensual se presenta como predeterminada o destacadamente presentada
- [ ] La experiencia móvil es fluida (50%+ de donaciones son móviles)
- [ ] La página de confirmación agradece y muestra impacto
- [ ] El email de recepción automática se dispara inmediatamente
```

### 2. Página de Agradecimiento

Después de donar, muestra:
- Mensaje de agradecimiento sincero
- Impacto específico de su monto de regalo
- Botones para compartir en redes sociales ("Cuéntales a tus amigos")
- Opción de hacerlo recurrente (si fue única vez)
- Enlace al reporte de impacto

### 3. Ideas para Prueba A/B

- Titular: emocional vs. orientado a datos
- Monto predeterminado: $25 vs. $50 vs. $100
- Mensual vs. única como selección predeterminada
- Con testimonio de donador vs. sin
- Foto de beneficiario vs. sin foto

---

## Ejemplo 1: Página de Donación de Organización de Educación

```
Titular: "Dale a Un Niño el Regalo de la Lectura"
$25 — Proporciona 5 libros para biblioteca de aula
$50 — Financia un mes de tutoría después de la escuela
$100 — Patrocina un estudiante por un semestre
$250 — Financia completamente el programa de lectura de un niño por un año
Encuadre mensual: "$25/mes significa que un niño siempre tiene un tutor esperando"
```

## Ejemplo 2: Página de Donación de Rescate de Animales

```
Titular: "Salva Una Vida Hoy"
$25 — Alimenta un animal rescatado por un mes
$50 — Cubre vacunas para un animal
$100 — Financia cuidado veterinario de emergencia
$250 — Patrocina un rescate y rehabilitación completos
Señal de confianza: "98 centavos de cada dólar va a cuidado de animales"
```

---

## Anti-Patrones

- **Demasiados campos de formulario** — cada campo adicional reduce conversiones. Nombre, email, pago. Eso es.
- **Sin encuadre de impacto** — "$50" no significa nada. "$50 alimenta a una familia por una semana" significa todo.
- **Enterrar donaciones recurrentes** — los donadores mensuales son 5x más valiosos con el tiempo. Destaca esto prominentemente.
- **Sin señales de confianza** — los donadores necesitan saber que su dinero es seguro y bien utilizado. Muestra seguridad y transparencia.
- **Carga de página lenta** — cada segundo de tiempo de carga reduce la conversión un 7%. Optimiza sin piedad.
- **Agradecimiento genérico** — "Gracias por tu donación" desperdicia el momento de mayor participación. Muestra impacto específico y alienta compartir.

---

## Recuperación

- **Sin datos de impacto disponibles:** Estima basado en presupuesto. Si gastas $100,000 en programas sirviendo a 500 personas, cada persona cuesta $200 para servir. Encuadra niveles de donador en consecuencia.
- **Sin señales de confianza o calificaciones:** Declara la relación de gasto de programa. "X centavos de cada dólar va a programas" es una poderosa señal de confianza que puedes calcular tú mismo.
- **Baja tasa de donación recurrente:** Prueba hacer que el valor predeterminado sea mensual, encuadrando el impacto anual, y ofreciendo un pequeño incentivo (actualizaciones trimestrales, insignia de donador).
- **La página existe pero convierte mal:** Audita contra la lista de verificación. Los problemas más comunes son demasiados campos de formulario, sin monto preseleccionado, y encuadre de impacto faltante.
