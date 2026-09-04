---
name: pagina-recetas
description: "Crea tarjetas de recetas profesionales con listas de ingredientes, instrucciones paso a paso y cálculos de escala. Úsalo cuando documentes recetas para clientes, contenido u operaciones."
allowed-tools: Read Write Glob
metadata:
  author: Imperio Digital
  version: "1.0"
---

# Tarjeta de Receta

## Cuándo Usar Esta Habilidad

Usa esta habilidad cuando necesites:
- Crear tarjetas de receta profesionales para clientes, contenido de blog o redes sociales
- Documentar recetas de restaurante con medidas precisas y escalado
- Construir tarjetas de receta para libros de cocina, e-books o productos digitales
- Estandarizar recetas de cocina para consistencia entre el personal

**NO** uses esta habilidad para descripciones de menú, análisis nutricional o planificación de comidas. Esto es solo para creación individual de tarjetas de receta.

---

## Principio Fundamental

UNA TARJETA DE RECETA DEBE SER SEGUIBLE POR ALGUIEN QUE NUNCA HA HECHO EL PLATO — CADA MEDIDA ES EXACTA, CADA PASO ES VIABLE, Y NADA SE ASUME.

---

## Fase 1: Análisis Inicial

### Entradas Requeridas

| Entrada | Qué Preguntar | Predeterminado |
|-------|------------|---------|
| **Nombre de la receta** | "¿Cómo se llama el plato?" | No hay predeterminado — debe proporcionarse |
| **Tamaño de porción** | "¿Cuántas porciones hace esta receta?" | 4 porciones |
| **Nivel de habilidad** | "¿Es esto para cocineros caseros principiantes, intermedios o avanzados?" | Intermedio |
| **Audiencia** | "¿Para quién es esta receta? Lectores de blog, personal de restaurante, libro de cocina?" | Cocineros caseros / lectores de blog |
| **Notas dietéticas** | "¿Hay etiquetas dietéticas? Vegetariano, vegano, sin gluten?" | Nota si es aplicable |
| **Necesidades de escala** | "¿Debería la receta incluir escala para diferentes tamaños de porción?" | Sí — 2x y 0.5x |

**PUNTO DE CONTROL: Confirma el análisis inicial antes de escribir la receta.**

---

## Fase 2: Estructura

### Formato de Tarjeta de Receta

```
## [Nombre de la Receta]

**Rinde:** [X] porciones
**Tiempo de preparación:** [X] minutos
**Tiempo de cocción:** [X] minutos
**Tiempo total:** [X] minutos
**Dificultad:** Fácil / Intermedio / Avanzado
**Dietética:** [V] [VG] [SG] [SF] (si es aplicable)

### Descripción
[2-3 oraciones describiendo el plato, su origen, o por qué es especial]

### Ingredientes
[Lista organizada con medidas exactas]

### Instrucciones
[Paso a paso numerado]

### Notas
[Consejos, sustituciones e instrucciones de almacenamiento]

### Escala
[Medidas ajustadas para 2x y 0.5x]
```

**PUNTO DE CONTROL: Confirma el formato antes de escribir.**

---

## Fase 3: Escritura

### Reglas de Lista de Ingredientes

- **Lista en orden de uso** — los ingredientes aparecen en el orden en que se usan en las instrucciones
- **Medidas exactas** — "1 cucharada de aceite de oliva" no "aceite de oliva" u "algo de aceite"
- **Especifica preparación** — "1 cebolla, picada" no solo "1 cebolla"
- **Agrupa por sección** — si la receta tiene partes distintas (marinada, salsa, ensamblaje), agrupa ingredientes bajo subtítulos
- **Incluye tamaños** — "1 huevo grande" no "1 huevo"; "3 dientes de ajo, picados" no solo "ajo"

### Formato de Ingredientes

```
### Ingredientes

**Para la marinada:**
- 2 cucharadas de salsa de soja
- 1 cucharada de aceite de sésamo
- 3 dientes de ajo, picados
- 1 pieza de jengibre fresco de 1 pulgada, rallada

**Para el salteado:**
- 1 libra de muslos de pollo sin hueso, cortados en piezas de 1 pulgada
- 2 cucharadas de aceite vegetal
- 1 pimiento rojo, rebanado
- 1 taza de floretes de brócoli
- 2 cebolletas, rebanadas (para decoración)
```

### Reglas de Escritura de Instrucciones

- **Una acción por paso** — "Pica la cebolla. Calienta aceite de oliva en una sartén grande a fuego medio-alto." son dos pasos, no uno.
- **Incluye señales sensoriales** — "Cocina hasta que esté dorado, aproximadamente 3-4 minutos" no solo "cocina 4 minutos"
- **Especifica niveles de calor** — "fuego medio-alto" no "caliente"
- **Especifica equipo** — "sartén grande," "saucepan mediano," "bandeja de horno"
- **Incluye tiempo Y señales visuales** — el tiempo solo es poco confiable. "Saltea hasta que esté translúcido, aproximadamente 3 minutos."
- **Numera cada paso**

### Ejemplo de Instrucciones

```
### Instrucciones

1. **Marina el pollo.** En un recipiente mediano, combina salsa de soja, aceite de sésamo, ajo y jengibre. Agrega piezas de pollo y revuelve para cubrir. Refrigera durante al menos 15 minutos (hasta 2 horas).

2. **Calienta la sartén.** Calienta aceite vegetal en una sartén grande o wok a fuego alto hasta que el aceite brille.

3. **Sella el pollo.** Retira el pollo de la marinada (reserva la marinada). Agrega el pollo a la sartén caliente en una sola capa. Cocina sin revolver durante 2-3 minutos hasta que esté dorado en la parte inferior. Voltea y cocina 2 minutos más.

4. **Agrega vegetales.** Agrega pimiento rojo y brócoli. Saltea durante 3-4 minutos hasta que los vegetales estén crujientes y tiernos y el pollo esté completamente cocido (temperatura interna 165°F).

5. **Termina y sirve.** Vierte la marinada reservada sobre el salteado. Cocina 1 minuto hasta que la salsa se espese ligeramente. Retira del fuego. Decorar con cebolletas rebanadas. Sirve inmediatamente sobre arroz al vapor.
```

### Sección de Notas

Incluye:
- **Almacenamiento:** "Almacena en un recipiente hermético en el refrigerador durante hasta 3 días. Calienta en una sartén a fuego medio."
- **Sustituciones:** "Sustituye tofu por pollo para una versión vegetariana. Usa tamari en lugar de salsa de soja para sin gluten."
- **Consejos:** "Seca el pollo antes de sellarlo para el mejor dorado. No sobrecargues la sartén."
- **Preparación previa:** "La marinada puede prepararse hasta 24 horas de antelación."

### Tabla de Escala

```
### Guía de Escala

| Ingrediente | 0.5x (2 porciones) | 1x (4 porciones) | 2x (8 porciones) |
|-----------|-------------------|------------------|------------------|
| Muslos de pollo | 0.5 lb | 1 lb | 2 lb |
| Salsa de soja | 1 cucharada | 2 cucharadas | 4 cucharadas (¼ taza) |
| Aceite de sésamo | 1.5 cucharadita | 1 cucharada | 2 cucharadas |
| Ajo | 2 dientes | 3 dientes | 6 dientes |
```

---

## Fase 4: Pulido

### 1. Notas de Fotografía

Si la receta se publicará con una foto:
- Sugiere estilo de presentación y decoración
- Recomienda el mejor ángulo (vista superior para platos planos, 45° para platos altos)
- Nota cualquier momento digno de foto durante la cocción (vapor, vertido, decoración)

### 2. Notas SEO (para recetas de blog)

- Usa el nombre de la receta en el H1 y primer párrafo
- Escribe una introducción de 100 palabras antes de la tarjeta de receta (historia personal o consejos)
- Incluye datos estructurados (esquema de receta) para motores de búsqueda
- Palabras clave objetivo: "receta de [nombre del plato]," "[nombre del plato] fácil," "cómo hacer [nombre del plato]"

### 3. Lista de Verificación de Calidad

```
## Lista de Verificación de Tarjeta de Receta

- [ ] Nombre de receta, rinde y tiempos están claramente indicados
- [ ] Ingredientes listados en orden de uso con medidas exactas
- [ ] Detalles de preparación incluidos para cada ingrediente (picado, picado fino, etc.)
- [ ] Cada paso de instrucción tiene una acción
- [ ] Señales sensoriales emparejadas con tiempo (dorado, 3-4 minutos)
- [ ] Niveles de calor y equipo especificados
- [ ] Las notas incluyen almacenamiento, sustituciones y consejos
- [ ] Guía de escala proporcionada para al menos 2 variaciones
- [ ] Etiquetas dietéticas incluidas si es aplicable
- [ ] Receta probada y confirmada para producir el resultado indicado
```

---

## Ejemplo

**Extracto de tarjeta de receta:**

```
## Salmón Ajo Miel

**Rinde:** 4 porciones | **Preparación:** 10 min | **Cocción:** 15 min | **Total:** 25 min
**Dificultad:** Fácil | **Dietética:** SG, SF

### Descripción
Filetes de salmón con piel crujiente glaseados con una salsa pegajosa de ajo y miel. Listo en 25 minutos — perfecto para una cena de semana que se ve como si pasaras una hora.

### Ingredientes
- 4 filetes de salmón (6 oz cada uno), con piel, secos
- 1 cucharada de aceite de oliva
- Sal y pimienta negra al gusto
- 3 cucharadas de miel
- 2 cucharadas de salsa de soja (usa tamari para SG)
- 4 dientes de ajo, picados
- 1 cucharada de jugo de limón fresco
- 1 cucharadita de semillas de sésamo (para decoración)
```

---

## Anti-Patrones

- **Conocimiento asumido** — "Cocina hasta que esté listo" asume que el lector sabe qué se ve "listo". Describe las señales visuales, auditivas y de temperatura.
- **Medidas imprecisas** — "Un puñado de hierbas" varía según el tamaño de la mano. Usa cucharadas o tazas.
- **Múltiples acciones por paso** — "Pica la cebolla, pica el ajo y calienta la sartén" son tres pasos metidos en uno.
- **Sin tiempo o señales visuales** — "Cocina la salsa" ¿por cuánto tiempo? ¿Hasta que haga qué? Siempre incluye ambos.
- **Recetas no probadas** — publicar una receta que no has hecho produce cocineros frustrados y comentarios enojados. Prueba cada receta.

---

## Recuperación

- **La receta es demasiado larga:** Divide en subrecetas (p. ej., "Haz la salsa" y "Cocina la proteína") u ofrece una versión rápida con menos pasos.
- **El lector informa de resultados diferentes:** Verifica la altitud, equipo y diferencias de marca de ingredientes. Agrega notas de resolución de problemas.
- **La escala produce medidas extrañas:** Redondea a la medida práctica más cercana. "2.5 cucharadas" se convierte en "2 cucharadas más 1.5 cucharaditas."
- **Se solicitan sustituciones dietéticas:** Agrega una sección de sustituciones cubriendo las 3 principales modificaciones dietéticas (sin lactosa, sin gluten, vegetariano).
