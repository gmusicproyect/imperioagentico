---
name: copia-pagina-donacion
description: "Escribe copia de página de donación con urgencia, encuadre de impacto, incentivo de donación recurrente y señales de confianza."
allowed-tools: Read Write Glob
metadata:
  author: Imperio Digital
  version: "1.0"
---

# Copia de Página de Donación

## Cuándo Usar Esta Skill

Usa esta skill cuando necesites:
- Escribir copia para una página de donación en línea que convierta visitantes en donantes
- Crear niveles de donación con encuadre de impacto, urgencia y elementos de confianza
- Optimizar una página de donación existente para mayor conversión y donaciones recurrentes
- Construir copia de página de donación para campañas, recaudaciones de fin de año o donaciones permanentes

**NO USES** esta skill para cartas de recaudación de fondos, solicitudes de subvenciones o campañas de crowdfunding. Esta es específicamente para la página de donación donde ocurre la transacción.

---

## Principio Fundamental

UNA PÁGINA DE DONACIÓN TIENE UN TRABAJO: ELIMINAR CADA BARRERA ENTRE EL DESEO DEL VISITANTE DE AYUDAR Y LA TRANSACCIÓN COMPLETADA — CADA PALABRA DEBE CONSTRUIR CONFIANZA O REDUCIR FRICCIÓN.

---

## Fase 1: Resumen Inicial

### Información Requerida

| Entrada | Qué Preguntar | Predeterminado |
|---------|---------------|--------|
| **Organización** | "¿Cuál es la organización y misión?" | Sin predeterminado — debe proporcionarse |
| **Tipo de página** | "¿Página de donación permanente o específica de campaña?" | Permanente |
| **Niveles de donación** | "¿Qué montos de donación quieres sugerir?" | $25, $50, $100, $250 |
| **Declaraciones de impacto** | "¿Qué logra cada monto en dólares?" | Sin predeterminado — debe proporcionarse |
| **Donación recurrente** | "¿Quieres alentar donaciones mensuales?" | Sí |
| **Señales de confianza** | "¿Tienes calificaciones, certificaciones o insignias de transparencia? (GuideStar, Charity Navigator)" | Ninguna disponible |

**PUNTO DE CONTROL: Confirma el resumen antes de escribir.**

---

## Fase 2: Estructura de Página

### Arquitectura de Página de Donación

```
1. Titular — emocional, impulsado por beneficio, 8 palabras o menos
2. Subtítulo — una oración expandiendo el titular
3. Declaración de impacto — qué logran las donaciones (2-3 oraciones)
4. Niveles de donación — montos preestablecidos con descripciones de impacto
5. Alternancia de recurrencia — opción de donación mensual con encuadre
6. Monto personalizado — opción para donantes que desean otro monto
7. Señales de confianza — calificaciones, datos de transparencia, insignias de seguridad
8. Formulario de información de donante — nombre, correo electrónico, pago (mantén mínimo)
9. Opción de dedicación/homenaje — donar en honor de alguien
10. Social proof — recuento de donantes, obsequios recientes, testimonios
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

Preselecciona la opción central. Ancla expectativas sin intimidar.

**PUNTO DE CONTROL: Presenta la estructura de la página para aprobación.**

---

## Fase 3: Escribir

### Elementos de Copia

**Opciones de Titular (elige una):**
- "Proporciona [Resultado] a [Beneficiario]"
- "Tu Donación Lo Cambia Todo para [Beneficiario]"
- "[Número] [Personas] Cuentan Contigo"

**Subtítulo:**
Una oración que conecte la acción del donante con el resultado. "Cuando donas hoy, [impacto específico]."

**Sección de Impacto:**
```
Cada dólar que donas va directamente a [misión]. Aquí está lo que tu donación hace posible:

$25 — [Resultado específico y tangible]
$50 — [Resultado específico y tangible]
$100 — [Resultado específico y tangible]
$250 — [Resultado específico y tangible]
```

**Encuadre de Donación Recurrente:**
```
## Conviértete en Donante Mensual
Las donaciones mensuales proporcionan financiamiento estable que nos permite planificar con anticipación y servir a más [beneficiarios].

$25/mes = $300/año = [impacto anual]
$50/mes = $600/año = [impacto anual]

Donantes mensuales reciben: [actualizaciones de impacto trimestrales, contenido exclusivo, reconocimiento]
```

**Sección de Señales de Confianza:**
```
## Tu Donación Es Segura y Efectiva
- [X]% de los fondos van directamente a programas
- [Calificación/certificación si está disponible]
- Procesamiento de pago seguro mediante [Stripe/PayPal]
- Deducible de impuestos — recibirás un recibo inmediatamente
```

**Social Proof:**
```
Únete a [X] donantes que ya han donado este [mes/año].
"[Testimonio corto de un donante sobre por qué donan]" — [Nombre, Ciudad]
```

---

## Fase 4: Pulir

### 1. Optimización de Conversión

```
## Lista de Verificación de Optimización de Página
- [ ] La página carga en menos de 3 segundos
- [ ] El formulario tiene 5 o menos campos (nombre, correo electrónico, monto, pago)
- [ ] El monto preseleccionado es el nivel central
- [ ] La donación mensual se presenta como predeterminada o destacada prominentemente
- [ ] La experiencia móvil es fluida (50%+ de donaciones son móviles)
- [ ] La página de confirmación agradece y muestra impacto
- [ ] El correo electrónico de recepción automática se dispara inmediatamente
```

### 2. Página de Agradecimiento

Después de donación, muestra:
- Mensaje de agradecimiento sentido
- Impacto específico del monto de su donación
- Botones de compartición social ("Cuéntale a tus amigos")
- Opción de hacerlo recurrente (si fue una sola vez)
- Enlace al informe de impacto

### 3. Ideas de Prueba A/B

- Titular: emocional vs. impulsado por datos
- Monto predeterminado: $25 vs. $50 vs. $100
- Mensual vs. una sola vez como selección predeterminada
- Con testimonio de donante vs. sin
- Foto de beneficiario vs. sin foto

---

## Ejemplo 1: Página de Donación de ONG de Educación

```
Titular: "Dale a un Niño el Regalo de la Lectura"
$25 — Proporciona 5 libros para una biblioteca de aula
$50 — Financia un mes de tutoría extraescolar
$100 — Patrocina a un estudiante durante un semestre
$250 — Financia completamente el programa de lectura de un niño durante un año
Encuadre mensual: "$25/mes significa un niño siempre tiene un tutor esperando"
```

## Ejemplo 2: Página de Donación de Rescate de Animales

```
Titular: "Salva una Vida Hoy"
$25 — Alimenta a un animal rescatado durante un mes
$50 — Cubre vacunas para un animal
$100 — Financia cuidado veterinario de emergencia
$250 — Patrocina un rescate completo y rehabilitación
Señal de confianza: "98 centavos de cada dólar van al cuidado de animales"
```

---

## Anti-Patrones

- **Demasiados campos de formulario** — cada campo adicional reduce conversiones. Nombre, correo electrónico, pago. Eso es todo.
- **Sin encuadre de impacto** — "$50" no significa nada. "$50 alimenta a una familia durante una semana" lo significa todo.
- **Enterrar donaciones recurrentes** — los donantes mensuales son 5x más valiosos con el tiempo. Destaca esto prominentemente.
- **Sin señales de confianza** — los donantes necesitan saber que su dinero es seguro y bien utilizado. Muestra seguridad y transparencia.
- **Carga de página lenta** — cada segundo de tiempo de carga reduce la conversión en 7%. Optimiza sin parar.
- **Agradecimiento genérico** — "Gracias por tu donación" desperdicia el momento de mayor engagement. Muestra impacto específico y alienta compartición.

---

## Recuperación

- **Sin datos de impacto disponibles:** Estima basado en presupuesto. Si gastas $100,000 en programas sirviendo a 500 personas, cada persona cuesta $200 servir. Encuadra niveles de donante en consecuencia.
- **Sin señales de confianza o calificaciones:** Indica la proporción de gastos de programas. "X centavos de cada dólar van a programas" es una poderosa señal de confianza que puedes calcular tú mismo.
- **Baja tasa de donación recurrente:** Prueba predeterminar mensual, encuadrar el impacto anual y ofrecer un pequeño incentivo (actualizaciones trimestrales, insignia de donante).
- **Página existe pero convierte mal:** Audita contra la lista de verificación. Los problemas más comunes son demasiados campos de formulario, sin monto preseleccionado y encuadre de impacto faltante.
