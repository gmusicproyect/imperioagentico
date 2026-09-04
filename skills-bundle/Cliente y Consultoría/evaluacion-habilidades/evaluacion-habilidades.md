---
name: evaluacion-habilidades
description: "Construye herramientas de evaluación de competencias con niveles de competencia, rúbricas de evaluación y recomendaciones de desarrollo."
allowed-tools: Read Write Glob
metadata:
  author: Imperio Digital
  version: "1.0"
---

# Evaluación de Habilidades

## Cuándo Usar Este Skill

Usa este skill cuando necesites:
- Construir una herramienta de evaluación de competencias para evaluar habilidades en diferentes niveles de dominio
- Crear rúbricas para calificar trabajo de estudiantes, entregables de contratistas o capacidades de equipos
- Diseñar cuestionarios de autoevaluación con recomendaciones de ruta de desarrollo
- Producir instrumentos de evaluación para contratación, entrenamiento o programas de certificación

**NO USES** este skill para pruebas de personalidad, encuestas de satisfacción del cliente o cuestionarios generales. Esto es para medir competencias específicas contra estándares definidos.

---

## Principio Fundamental

UNA EVALUACIÓN SOLO ES ÚTIL SI DISTINGUE CLARAMENTE ENTRE NIVELES DE HABILIDAD Y LE DICE A LA PERSONA EXACTAMENTE QUÉ HACER DESPUÉS — MEDICIÓN SIN UNA RUTA DE DESARROLLO ES SOLO UNA ETIQUETA.

---

## Fase 1: Resumen

### Información Requerida

| Información | Qué Preguntar | Valor por Defecto |
|-------|------------|---------|
| **Dominio de habilidad** | "¿Qué habilidad o área de competencia estás evaluando?" | Sin valor por defecto — debe proporcionarse |
| **Propósito de evaluación** | "¿Es para contratación, colocación de entrenamiento, certificación o autodesarrollo?" | Autodesarrollo |
| **Niveles de competencia** | "¿Cuántos niveles? (3, 4 o 5)" | 4 niveles (Principiante, Intermedio, Avanzado, Experto) |
| **Formato de evaluación** | "¿Cuestionario de autoevaluación, rúbrica de evaluador o prueba práctica?" | Cuestionario de autoevaluación |
| **Audiencia** | "¿Quién será evaluado?" | Emprendedores individuales y dueños de pequeñas empresas |

**PUNTO DE CONTROL: Confirma el resumen antes de proceder.**

---

## Fase 2: Marco de Competencias

### Construir el Mapa de Competencias

Divide el dominio de habilidad en 4-6 subcompetencias. Para cada una:

```
## Subcompetencia: [Nombre]

| Nivel | Descripción | Comportamientos Observables |
|-------|------------|---------------------|
| Principiante | [Lo que se parece] | [Acciones específicas que pueden/no pueden hacer] |
| Intermedio | [Lo que se parece] | [Acciones específicas] |
| Avanzado | [Lo que se parece] | [Acciones específicas] |
| Experto | [Lo que se parece] | [Acciones específicas] |
```

### Reglas de Definición de Niveles

- Cada nivel debe ser objetivamente distinguible de los otros
- Usa comportamientos observables, no juicios subjetivos ("puede escribir una página de ventas con conversión superior al 2%" vs. "escribe buena copia")
- Cada nivel se construye sobre el anterior — sin saltos
- El nivel de experto debe representar un desempeño del top 10%, no perfección

**PUNTO DE CONTROL: Presenta el marco de competencias para aprobación.**

---

## Fase 3: Construir la Evaluación

### Para Cuestionarios de Autoevaluación

Crea 3-5 preguntas por subcompetencia. Cada pregunta describe un escenario y ofrece opciones de respuesta alineadas al nivel:

```
P: Cuando necesitas [escenario de habilidad], típicamente:
A) [Comportamiento de principiante] — 1 punto
B) [Comportamiento intermedio] — 2 puntos
C) [Comportamiento avanzado] — 3 puntos
D) [Comportamiento de experto] — 4 puntos
```

### Para Rúbricas de Evaluador

Crea una grilla de puntuación:

```
| Criterio | 1 - Principiante | 2 - Intermedio | 3 - Avanzado | 4 - Experto | Puntuación |
|----------|-------------|-----------------|-------------|-----------|-------|
| [Criterio 1] | [Descripción] | [Descripción] | [Descripción] | [Descripción] | /4 |
```

### Puntuación e Interpretación

```
## Guía de Puntuación

**Total posible:** [X puntos]
**Principiante:** 0-25% — [Lo que esto significa + siguiente paso inmediato]
**Intermedio:** 26-50% — [Lo que esto significa + siguiente paso]
**Avanzado:** 51-75% — [Lo que esto significa + siguiente paso]
**Experto:** 76-100% — [Lo que esto significa + siguiente paso]
```

---

## Fase 4: Pulir

### 1. Recomendaciones de Desarrollo

Para cada nivel de competencia, proporciona:
- Top 3 habilidades a desarrollar después
- Recursos recomendados o ejercicios
- Tiempo estimado para alcanzar el siguiente nivel
- Una victoria rápida que puedan implementar esta semana

### 2. Verificación de Validez

Revisa la evaluación para:
- Cada subcompetencia es cubierta por al menos 3 preguntas
- Ninguna pregunta puede ser respondida "correctamente" sin habilidad real
- Las preguntas progresan en dificultad dentro de cada subcompetencia
- El lenguaje es claro y libre de jerga que la audiencia no conocería

### 3. Formato de Entrega

```
## Paquete de Evaluación
- Cuestionario de evaluación (listo para usar en Google Forms, Typeform o PDF)
- Guía de puntuación con descripciones de niveles
- Mapa de desarrollo por nivel
- Línea de tiempo de reevaluación (recomienda retomar cada 90 días)
```

---

## Anti-Patrones

- **Descripciones vagas de niveles** — "bueno escribiendo" no es medible. Usa comportamientos observables.
- **Demasiadas subcompetencias** — más de 6 hace la evaluación agotadora. Combina áreas relacionadas.
- **Preguntas que indican la respuesta** — no hagas obvio cuál es la respuesta "correcta". Todas las opciones deben sonar razonables.
- **Sin ruta de desarrollo** — etiquetar a alguien como "principiante" sin decirle cómo mejorar es desmoralizante.
- **Puntuación binaria** — preguntas sí/no pierden matices. Usa respuestas con escala.
- **Evaluación sin reevaluación** — las habilidades crecen. Construye una línea de tiempo para retomar.

---

## Recuperación

- **Dominio de habilidad demasiado amplio:** Pregunta "Si alguien dominara solo una parte de esto, ¿cuál parte importaría más para su negocio?" Comienza ahí.
- **Usuario quiere aprobado/reprobado, no niveles:** Crea un umbral de competencia mínima con criterios claros. Puntuación superior = aprobado.
- **Usuario no puede definir nivel experto:** Pídele que describa la mejor persona que ha visto realizar esta habilidad. Usa eso como referencia de experto.
- **Evaluación demasiado larga:** Limita a 20 preguntas totales. Prioriza las 3 subcompetencias más críticas para el negocio.
