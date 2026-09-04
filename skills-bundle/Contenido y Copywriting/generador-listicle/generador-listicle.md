---
name: generador-listicle
description: "Crea artículos listicle atractivos con estructura de entrada consistente, ejemplos y optimización SEO. Usa al escribir publicaciones de listas numeradas como 'Top 10' o 'Mejor X para Y'."
allowed-tools: Read Write Glob
metadata:
  author: Imperio Digital
  version: "1.0"
---

# Generador de Listicle

## Cuándo Usar Esta Skill

Usa esta skill cuando necesites:
- Escribir un artículo de lista numerada (top 5, 10 consejos, 7 errores, etc.)
- Crear una publicación recopilatoria "lo mejor de" optimizada para búsqueda
- Producir contenido de lista escaneable y de alto engagement para un blog
- Construir un listicle con estructura consistente en todas las entradas

**NO USES** esta skill para artículos de comparación (usa comparison-article skill) o guías largas sin numerar. Esta es para publicaciones de listas estructuradas.

---

## Principio Fundamental

CADA ELEMENTO EN UN LISTICLE DEBE GANAR SU LUGAR — SI UNA ENTRADA PODRÍA CORTARSE SIN QUE EL LECTOR LO NOTARA, NO DEBERÍA ESTAR.

---

## Fase 1: Resumen Inicial

### Información Requerida

| Entrada | Qué Preguntar | Predeterminado |
|---------|---------------|--------|
| **Tema / premisa de lista** | "¿De qué trata esta lista?" | Sin predeterminado — debe proporcionarse |
| **Número de elementos** | "¿Cuántos elementos en la lista?" | 7-10 |
| **Palabra clave objetivo** | "¿Por qué palabra clave debería clasificarse esto?" | Derivada del tema |
| **Audiencia** | "¿Quién leerá esto?" | Emprendedores individuales y propietarios de negocios |
| **Tipo de lista** | "¿Consejos, herramientas, errores, estrategias, ejemplos o recursos?" | Consejos |
| **Recuento de palabras** | "¿Longitud objetivo?" | 1,500-2,000 palabras |

**PUNTO DE CONTROL: Confirma el resumen antes de construir la lista.**

---

## Fase 2: Esquema

### Arquitectura de Listicle

```
**H1:** [Número] [Cosas] [Sobre Tema] [Beneficio o Hook]

**Introducción** (~100-150 palabras) — Por qué esta lista importa

**H2: 1. [Título del Elemento]** (~[palabras])
**H2: 2. [Título del Elemento]** (~[palabras])
...
**H2: [N]. [Título del Elemento]** (~[palabras])

**Bonificación / Menciones Honoríficas** (opcional)

**Conclusión + CTA** (~100 palabras)
```

### Estrategia de Orden

Elige un enfoque de ordenamiento:
- **Orden de prioridad** — lo más importante primero (mejor para consejos/estrategias)
- **Impacto ascendente** — construye hacia lo mejor (mejor para herramientas/recursos)
- **Secuencia lógica** — sigue una progresión natural (mejor para pasos)

**PUNTO DE CONTROL: Aprueba elementos de lista y orden antes de escribir.**

---

## Fase 3: Escribir

### Estructura de Entrada (consistente para cada elemento)

Cada entrada de lista sigue este formato:

```
## [N]. [Título del Elemento]

[Explicación de 1-2 oraciones de qué es este elemento y por qué importa]

[Ejemplo concreto, punto de datos o instrucción accionable — 2-4 oraciones]

[Consejo profesional, advertencia o "cómo implementar esto" — 1-2 oraciones]
```

### Reglas de Escritura

| Regla | Detalle |
|------|--------|
| **Estructura consistente** | Cada entrada sigue el mismo formato — explicación, ejemplo, acción |
| **La longitud variable está bien** | Algunos elementos merecen 200 palabras, otros 100 — pero mantente dentro de 100-300 por entrada |
| **Específico sobre genérico** | "Envía facturas dentro de 24 horas de finalización del proyecto" no "Envía facturas de manera oportuna" |
| **Negrita el título del elemento** | Los hojeadores deberían obtener valor solo escaneando los H2s |
| **H2 para cada elemento** | Cada entrada de lista es un H2 — crítico para SEO y escanabilidad |
| **Sin entradas de relleno** | Si no puedes escribir 100 palabras significativas sobre un elemento, córtalo |
| **Intro engancha rápido** | 2-3 oraciones máximo antes de que comience el primer elemento de la lista |

### Plantilla de Introducción

```
[Apertura audaz — estadística, pregunta o pain point]

[Por qué esta lista importa al lector — 1-2 oraciones]

[Lo que se llevarán — 1 oración]

Vamos a profundizar.
```

### Plantilla de Conclusión

```
## [Cierre / Conclusión Clave]

[Una oración resumiendo el tema en todos los elementos]

[Dile al lector cuál 1-2 elementos implementar primero]

[CTA — qué hacer después]
```

---

## Fase 4: Pulir

### 1. Lista de Verificación de Listicle

```
## Lista de Verificación Pre-Publicación

- [ ] H1 incluye el número y palabra clave objetivo
- [ ] Cada entrada de lista sigue el mismo formato estructural
- [ ] Cada entrada incluye un ejemplo concreto o paso accionable
- [ ] Sin entradas de relleno — cada elemento gana su lugar
- [ ] Los encabezados H2 son descriptivos suficientemente para proporcionar valor por sí solos
- [ ] La introducción está bajo 150 palabras
- [ ] La conclusión recomienda dónde comenzar
- [ ] Palabra clave objetivo en H1, primeras 100 palabras y meta descripción
- [ ] El recuento de palabras está dentro del 10% del objetivo
- [ ] El orden de la lista es intencional (prioridad, ascendente o secuencial)
```

### 2. Meta Descripción

```
[Número] [tema] que [beneficio]. De [ejemplo de elemento] a [ejemplo de elemento] — guía de [audiencia] con consejos accionables.
```

### 3. Resumen de Imagen Destacada

```
Concepto: El número [N] mostrado prominentemente con iconos visuales representando los elementos principales de la lista
Dimensiones: 1200x630px
Estilo: Limpio, audaz, colores de marca
```

---

## Ejemplo: "7 Errores de Factura Que Cuestan Dinero a Freelancers" (1,500 palabras)

```
H1: 7 Errores de Factura Que Cuestan Dinero a Freelancers (Y Cómo Arreglar Cada Uno)

1. No Incluir Términos de Pago — lleva a situaciones de "pagaré cuando pueda"
2. Enviar Facturas Tarde — cuanto más esperes, más esperarán ellos
3. Usar Elementos de Línea Vagos — "consultoría" no le dice nada al cliente
4. Olvidar Numerar Tus Facturas — hace el seguimiento imposible
5. No Hacer Seguimiento de Pagos Vencidos — el silencio no es una estrategia de cobranza
6. Saltar la Línea de Tarifa Tardía — incluso si nunca la cobras, acelera el pago
7. Hacer Difícil Pagar — sin opción de pago en línea = pago retrasado

Conclusión: Arregla #1 y #6 esta semana — toman 5 minutos y tienen el mayor impacto.
```

---

## Anti-Patrones

- **Entradas de relleno** — rellenar una lista de "10 consejos" con 3 elementos débiles para alcanzar el número. Mejor publicar 7 elementos excelentes que 10 mediocres.
- **Formato de entrada inconsistente** — algunas entradas tienen 50 palabras, otras 400. Mantén estructura consistente.
- **H2s genéricos** — "Consejo 3: Comunicación" no le dice nada al lector. "Consejo 3: Envía una Actualización de Estado Semanal Cada Lunes" es útil por sí solo.
- **Sin ejemplos** — consejo abstracto sin ejemplos concretos es olvidable. Cada entrada necesita especificidad.
- **Enterrar los mejores elementos** — si el elemento más fuerte es #8 de 10, la mayoría de lectores nunca lo verán. Pon los mejores elementos temprano (a menos que construyas hacia un clímax).
- **Intros largas** — los lectores de listicle quieren la lista. Llega al elemento #1 dentro de 150 palabras.

---

## Recuperación

- **No puedes alcanzar el número objetivo:** Baja el número. "5 Consejos Esenciales" supera a "10 Consejos (5 de los cuales son relleno)."
- **Todos los elementos se sienten similares:** Diferencia añadiendo categorías distintas (mentalidad vs táctica vs herramientas) o fusiona elementos similares.
- **Demasiados elementos para el recuento de palabras:** O corta elementos u opta por aumentar el recuento de palabras. No exprimas 15 elementos en 1,000 palabras.
- **El usuario quiere elementos en los que no tiene experiencia:** Sugiere reemplazar con elementos que puedan hablar auténticamente, o investiga a fondo y nota fuentes.
- **La lista se siente obvia:** Añade un "La mayoría de personas se pierden esto" o "Consejo Avanzado" para cada elemento para elevar más allá de consejo de nivel de superficie.
