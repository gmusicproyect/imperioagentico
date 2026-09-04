---
name: esquema-programa-fitness
description: "Diseña programas de fitness con estructura de fases, lógica de progresión, selección de ejercicios y modificaciones para clientes."
allowed-tools: Read Write Glob
author: Imperio Digital
version: "1.0"
---

# Esquema de Programa de Fitness

## Cuándo Usar Este Skill

Usa este skill cuando necesites:
- Diseñar un programa de fitness multifase para clientes o un grupo
- Crear lógica de progresión que avance a los clientes de forma segura
- Seleccionar ejercicios apropiados para el nivel de fitness deseado
- Incluir opciones de modificación para diferentes niveles de habilidad

**NO** uses este skill para planes de nutrición, protocolos de rehabilitación o prescripciones de ejercicio médico. Es para diseño general de programas de fitness. Siempre recomienda a los clientes consultar a un médico antes de comenzar.

---

## Principio Fundamental

UN GRAN PROGRAMA DE FITNESS NO ES UNA LISTA DE EJERCICIOS — ES UNA PROGRESIÓN ESTRUCTURADA QUE CUMPLE CON LAS PERSONAS DONDE ESTÁN Y LAS MUEVE HACIA UN OBJETIVO ESPECÍFICO.

---

## Fase 1: Resumen del Programa

### Entradas Requeridas

| Entrada | Qué Preguntar | Predeterminado |
|---------|--------------|--------|
| **Objetivo** | "¿Cuál es el objetivo principal — fuerza, pérdida de peso, resistencia, fitness general?" | Sin predeterminado — debe proporcionarse |
| **Nivel del cliente** | "¿Principiante, intermedio o avanzado?" | Principiante |
| **Duración** | "¿Cuántas semanas tiene el programa?" | 8-12 semanas |
| **Frecuencia** | "¿Cuántos días por semana?" | 3-4 días/semana |
| **Equipo disponible** | "¿Qué equipo tienen — gimnasio completo, mancuernas en casa, solo peso corporal?" | Acceso a gimnasio completo |
| **Limitaciones** | "¿Hay lesiones, condiciones o movimientos a evitar?" | Ninguno mencionado |

**PUNTO DE CONTROL: Confirma el objetivo, nivel y equipo antes de diseñar el programa.**

---

## Fase 2: Estructura del Programa

### Diseño de Fases

```
## [Nombre del Programa] — Programa de [Duración] Semanas

### Fase 1: Fundación (Semanas 1-4)
**Enfoque:** Construir patrones de movimiento, establecer hábitos, acondicionamiento base
**Volumen:** 3 series x 10-12 reps (fuerza), cardio moderado
**Intensidad:** RPE 5-7 (esfuerzo moderado)
**Períodos de descanso:** 60-90 segundos entre series

### Fase 2: Construcción (Semanas 5-8)
**Enfoque:** Aumentar intensidad, agregar complejidad, sobrecarga progresiva
**Volumen:** 3-4 series x 8-10 reps (fuerza), duración de cardio aumentada
**Intensidad:** RPE 7-8 (desafiante)
**Períodos de descanso:** 45-75 segundos entre series

### Fase 3: Pico (Semanas 9-12)
**Enfoque:** Empujar el rendimiento, probar progreso, variaciones avanzadas
**Volumen:** 4 series x 6-8 reps (fuerza), integración HIIT
**Intensidad:** RPE 8-9 (difícil)
**Períodos de descanso:** 30-60 segundos entre series
```

### Plantilla Semanal

```
## Horario Semanal

| Día | Enfoque | Duración |
|-----|---------|----------|
| Lunes | Fuerza de tren superior | 45-60 min |
| Martes | Cardio / acondicionamiento | 30-40 min |
| Miércoles | Fuerza de tren inferior | 45-60 min |
| Jueves | Descanso o recuperación activa | — |
| Viernes | Cuerpo completo / funcional | 45-60 min |
| Sábado | Opcional: cardio o actividad al aire libre | 30-45 min |
| Domingo | Descanso | — |
```

---

## Fase 3: Selección de Ejercicios

### Categorías de Ejercicios

Para cada día de entrenamiento, selecciona de estas categorías:

| Categoría | Propósito | Ejemplos |
|-----------|---------|---------|
| Push compuesto | Fuerza push de tren superior | Press de banco, press de hombros, flexiones |
| Pull compuesto | Fuerza pull de tren superior | Remos, dominadas, jalones lat |
| Patrón de sentadilla | Quad-dominante de tren inferior | Sentadillas, estocadas, prensa de piernas |
| Patrón de bisagra | Cadena posterior de tren inferior | Deadlifts, empujes de cadera, RDLs |
| Core | Estabilidad y anti-rotación | Planks, press Pallof, bugs muertos |
| Cardio | Acondicionamiento cardiovascular | Caminar, ciclismo, remo, intervalos |
| Movilidad | Salud articular y flexibilidad | Estiramientos dinámicos, foam rolling |

### Niveles de Modificación

Para cada ejercicio, proporciona tres niveles:

```
## Ejercicio: Sentadilla

**Principiante:** Sentadilla de peso corporal a una caja/silla
**Intermedio:** Sentadilla con copa con mancuerna
**Avanzado:** Sentadilla frontal con barra

## Ejercicio: Flexión

**Principiante:** Flexión inclinada (manos en banco)
**Intermedio:** Flexión estándar
**Avanzado:** Flexión con déficit o flexión con peso
```

### Reglas de Progresión

1. **Aumenta peso cuando** el cliente completa todas las series y reps prescritas con buena forma durante 2 sesiones consecutivas
2. **Aumenta peso por** 5 lbs para tren superior, 10 lbs para tren inferior (o el incremento más pequeño disponible)
3. **Deload cada 4ta semana** — reduce volumen en 40% para permitir recuperación
4. **No progreses si** la forma se rompe o el cliente reporta dolor

---

## Fase 4: Entrega del Programa

### Formato de Tarjeta de Entrenamiento

```
## Día 1: Fuerza de Tren Superior — Fase 1

**Calentamiento (5-10 min):** Círculos de brazos, pull-aparts con banda, cardio ligero

| # | Ejercicio | Series | Reps | Descanso | Peso/Notas |
|---|----------|--------|------|---------|-------------|
| A1 | Press de mancuerna | 3 | 10-12 | 60s | Comienza ligero, encuentra peso de trabajo |
| A2 | Remo con cable | 3 | 10-12 | 60s | Controla el movimiento excéntrico |
| B1 | Press de hombros | 3 | 10-12 | 60s | Sentado si es necesario |
| B2 | Jalón lat | 3 | 10-12 | 60s | Rango completo de movimiento |
| C1 | Elevación lateral | 2 | 12-15 | 45s | Peso ligero, tempo lento |
| C2 | Curl de bíceps | 2 | 12-15 | 45s | — |
| D | Plank | 3 | 30-45s | 30s | Escala según habilidad |

**Enfriamiento (5 min):** Estiramiento de pecho, estiramiento de lats, estiramiento de hombros
```

### Lista de Verificación del Programa

- [ ] Cada día de entrenamiento tiene calentamiento y enfriamiento
- [ ] Los movimientos compuestos vienen antes de los ejercicios de aislamiento
- [ ] El balance push/pull se mantiene durante la semana
- [ ] El plan de progresión es claro para cada fase
- [ ] Se proporcionan modificaciones para cada ejercicio
- [ ] Se incluyen recomendaciones de días de descanso
- [ ] La semana de deload está programada
- [ ] Se aconseja al cliente consultar a un médico antes de comenzar

---

## Anti-Patrones

- **Sin plan de progresión** — hacer el mismo peso y reps durante 12 semanas no produce adaptación. Construye sobrecarga progresiva.
- **Demasiado volumen para principiantes** — 3 ejercicios por grupo muscular no se necesitan en la semana uno. Comienza simple y agrega complejidad.
- **Ignorar calentamientos y enfriamientos** — saltar preparación y recuperación aumenta el riesgo de lesión.
- **Variedad de ejercicios sobre consistencia** — cambiar ejercicios cada semana previene sobrecarga progresiva. Mantén movimientos centrales estables durante 4+ semanas.
- **Sin opciones de modificación** — un programa sin regresiones excluye a cualquiera que no pueda realizar el movimiento prescrito.

---

## Recuperación

- **El cliente no puede realizar un ejercicio:** Sustituye con la modificación de principiante inmediatamente. Ningún ejercicio es obligatorio.
- **El cliente no está progresando:** Verifica recuperación (sueño, nutrición, estrés), verifica forma, considera una semana de deload.
- **El programa es demasiado fácil:** Avanza a la siguiente fase temprano o aumenta la intensidad dentro de la fase actual.
- **El cliente pierde múltiples sesiones:** Ajusta el programa a menos días por semana en lugar de intentar "recuperarse" con sesiones duplicadas.
- **El cliente reporta dolor durante un movimiento:** Detén ese ejercicio inmediatamente. Sustituye y recomienda evaluación médica si el dolor persiste.
