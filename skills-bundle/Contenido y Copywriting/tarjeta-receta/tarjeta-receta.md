---
name: tarjeta-receta
description: "Crea tarjetas de receta profesionales con listas de ingredientes, instrucciones paso a paso y cálculos de escalado. Usa al documentar recetas para clientes, contenido u operaciones."
allowed-tools: Read Write Glob
metadata:
  author: Imperio Digital
  version: "1.0"
---

# Tarjeta de Receta

## Cuándo Usar Esta Skill

Usa esta skill cuando necesites:
- Crear tarjetas de receta profesionales para clientes, contenido de blog o redes sociales
- Documentar recetas de restaurante con medidas precisas y escalado
- Construir tarjetas de receta para libros de cocina, ebooks o productos digitales
- Estandarizar recetas de cocina para consistencia entre personal

**NO USES** esta skill para descripciones de menú, análisis nutricional o planificación de comidas. Esta es para creación de tarjetas de receta individual.

---

## Principio Fundamental

UNA TARJETA DE RECETA DEBE SER SEGUIBLE POR ALGUIEN QUE NUNCA HA HECHO EL PLATO — CADA MEDIDA ES EXACTA, CADA PASO ES ACCIONABLE Y NADA ESTÁ ASUMIDO.

---

## Fase 1: Resumen Inicial

### Información Requerida

| Entrada | Qué Preguntar | Predeterminado |
|---------|---------------|--------|
| **Nombre de receta** | "¿Cómo se llama el plato?" | Sin predeterminado — debe proporcionarse |
| **Tamaño de porción** | "¿Cuántas porciones hace esta receta?" | 4 porciones |
| **Nivel de habilidad** | "¿Es para principiantes, intermedios o cocineros caseros avanzados?" | Intermedio |
| **Audiencia** | "¿Para quién es esta receta? Lectores de blog, personal de restaurante, libro de cocina?" | Cocineros caseros / lectores de blog |
| **Notas dietéticas** | "¿Alguna etiqueta dietética? ¿Vegetariano, vegano, sin gluten?" | Nota si aplica |
| **Necesidades de escalado** | "¿Debería la receta incluir escalado para diferentes tamaños de porción?" | Sí — 2x y 0.5x |

**PUNTO DE CONTROL: Confirma el resumen antes de escribir la receta.**

---

## Fase 2: Estructura

### Formato de Tarjeta de Receta

```
## [Nombre de Receta]

**Rendimiento:** [X] porciones
**Tiempo de preparación:** [X] minutos
**Tiempo de cocción:** [X] minutos
**Tiempo total:** [X] minutos
**Dificultad:** Fácil / Intermedia / Avanzada
**Dietético:** [V] [VG] [SG] [SF] (si aplica)

### Descripción
[2-3 oraciones describiendo el plato, su origen o por qué es especial]

### Ingredientes
[Lista organizada con medidas exactas]

### Instrucciones
[Paso a paso numerado]

### Notas
[Consejos, sustituciones e instrucciones de almacenamiento]

### Escalado
[Medidas ajustadas para 2x y 0.5x]
```

**PUNTO DE CONTROL: Confirma el formato antes de escribir.**

---

## Fase 3: Escribir

### Reglas de Lista de Ingredientes

- **Listar en orden de uso** — los ingredientes aparecen en el orden en que se usan en las instrucciones
- **Medidas exactas** — "1 cucharada de aceite de oliva" no "aceite de oliva" o "algo de aceite"
- **Especificar preparación** — "1 cebolla, picada" no solo "1 cebolla"
- **Agrupar por sección** — si la receta tiene partes distintas (marinada, salsa, ensamblaje), agrupa ingredientes bajo subencabezados
- **Incluir tamaños** — "1 huevo grande" no "1 huevo"; "3 dientes de ajo, picados" no "ajo"

### Formato de Ingrediente

```
### Ingredientes

**Para la marinada:**
- 2 cucharadas de salsa de soya
- 1 cucharada de aceite de sésamo
- 3 dientes de ajo, picados
- Pieza de 1 pulgada de jengibre fresco, rallado

**Para el salteado:**
- 1 libra de muslos de pollo deshuesados, cortados en piezas de 1 pulgada
- 2 cucharadas de aceite vegetal
- 1 pimiento rojo, cortado en rodajas
- 1 taza de flores de brócoli
- 2 cebolletas verdes, cortadas (para decoración)
```

### Reglas de Escritura de Instrucciones

- **Una acción por paso** — "Pica la cebolla. Calienta aceite de oliva en una sartén grande a fuego medio-alto." son dos pasos, no uno.
- **Incluir señales sensoriales** — "Cocina hasta dorado, aproximadamente 3-4 minutos" no solo "cocina durante 4 minutos"
- **Especificar niveles de calor** — "fuego medio-alto" no "caliente"
- **Especificar equipo** — "sartén grande," "saucepan mediano," "bandeja de horno"
- **Incluir timing Y señales visuales** — el tiempo solo es confiable. "Sofríe hasta translúcido, aproximadamente 3 minutos."
- **Numerar cada paso**

### Ejemplo de Instrucciones

```
### Instrucciones

1. **Marina el pollo.** En un recipiente mediano, mezcla salsa de soya, aceite de sésamo, ajo y jengibre. Agrega piezas de pollo y mezcla para cubrir. Refrigera por al menos 15 minutos (hasta 2 horas).

2. **Calienta la sartén.** Calienta aceite vegetal en una sartén grande o wok a fuego alto hasta que el aceite brille.

3. **Sella el pollo.** Retira pollo de la marinada (reserva marinada). Agrega pollo a la sartén caliente en una sola capa. Cocina sin revolver durante 2-3 minutos hasta dorado en la parte inferior. Voltea y cocina 2 minutos más.

4. **Agrega vegetales.** Agrega pimiento y brócoli. Saltea durante 3-4 minutos hasta que los vegetales estén crujientes y tiernos y el pollo esté cocido (temperatura interna 165°F).

5. **Termina y sirve.** Vierte marinada reservada sobre el salteado. Cocina 1 minuto hasta que la salsa se espese ligeramente. Retira del fuego. Decora con cebolletas cortadas. Sirve inmediatamente sobre arroz al vapor.
```

### Sección de Notas

Incluye:
- **Almacenamiento:** "Almacena en un recipiente hermético en el refrigerador hasta 3 días. Recalienta en una sartén a fuego medio."
- **Sustituciones:** "Sustituye tofu por pollo para una versión vegetariana. Usa tamari en lugar de salsa de soya para sin gluten."
- **Consejos:** "Seca el pollo con toallas antes de sellar para mejor dorado. No sobrecargues la sartén."
- **Preparación anticipada:** "La marinada puede prepararse hasta 24 horas antes."

### Tabla de Escalado

```
### Guía de Escalado

| Ingrediente | 0.5x (2 porciones) | 1x (4 porciones) | 2x (8 porciones) |
|-----------|-------------------|------------------|------------------|
| Muslos de pollo | 0.5 lb | 1 lb | 2 lb |
| Salsa de soya | 1 cda | 2 cda | 4 cda (¼ taza) |
| Aceite de sésamo | 1.5 cdita | 1 cda | 2 cda |
| Ajo | 2 dientes | 3 dientes | 6 dientes |
```

---

## Fase 4: Pulir

### 1. Notas de Fotografía

Si la receta será publicada con foto:
- Sugiere estilo de presentación y decoración
- Recomienda el mejor ángulo (de arriba para platos planos, 45° para platos altos)
- Nota cualquier momento digno de foto durante cocción (vapor, vertido, decoración)

### 2. Notas de SEO (para recetas de blog)

- Usa el nombre de la receta en el H1 y primer párrafo
- Escribe una introducción de 100 palabras antes de la tarjeta de receta (historia personal o consejos)
- Incluye datos estructurados (esquema de Receta) para motores de búsqueda
- Palabras clave objetivo: "[nombre de plato] receta," "fácil [nombre de plato]," "cómo hacer [nombre de plato]"

### 3. Lista de Verificación de Calidad

```
## Lista de Verificación de Tarjeta de Receta

- [ ] Nombre de receta, rendimiento y tiempos están claramente indicados
- [ ] Ingredientes listados en orden de uso con medidas exactas
- [ ] Detalles de preparación incluidos para cada ingrediente (picado, picado, etc.)
- [ ] Cada paso de instrucción tiene una acción
- [ ] Señales sensoriales emparejadas con tiempos (dorado, 3-4 minutos)
- [ ] Niveles de calor y equipo especificados
- [ ] Las notas incluyen almacenamiento, sustituciones y consejos
- [ ] Guía de escalado proporcionada para al menos 2 variaciones
- [ ] Etiquetas dietéticas incluidas si aplica
- [ ] Receta probada y confirmada para producir el resultado indicado
```

---

## Ejemplo

**Extracto de tarjeta de receta:**

```
## Salmón Ajo Miel

**Rendimiento:** 4 porciones | **Prep:** 10 min | **Cocina:** 15 min | **Total:** 25 min
**Dificultad:** Fácil | **Dietético:** SG, SF

### Descripción
Filetes de salmón crujientes glaseados con salsa pegajosa de ajo miel. Listo en 25 minutos — perfecto para cena entre semana que parece que pasaste una hora.

### Ingredientes
- 4 filetes de salmón (6 oz cada uno), con piel, secados
- 1 cucharada de aceite de oliva
- Sal y pimienta negra al gusto
- 3 cucharadas de miel
- 2 cucharadas de salsa de soya (usa tamari para SG)
- 4 dientes de ajo, picados
- 1 cucharada de jugo de limón fresco
- 1 cucharadita de semillas de sésamo (para decoración)
```

---

## Anti-Patrones

- **Conocimiento asumido** — "Cocina hasta listo" asume que el lector sabe qué se ve "listo". Describe las señales visuales, auditivas y de temperatura.
- **Medidas imprecisas** — "Un puñado de hierbas" varía por tamaño de mano. Usa cucharadas o tazas.
- **Múltiples acciones por paso** — "Pica la cebolla, pica el ajo y calienta la sartén" son tres pasos comprimidos en uno.
- **Sin tiempos o señales visuales** — "Cocina la salsa" ¿durante cuánto tiempo? ¿Hasta qué? Siempre incluye ambos.
- **Recetas no probadas** — publicar una receta que no has hecho produce cocineros frustrados y comentarios furiosos. Prueba cada receta.

---

## Recuperación

- **La receta es demasiado larga:** Divide en sub-recetas (por ejemplo, "Haz la salsa" y "Cocina la proteína") u ofrece versión rápida con menos pasos.
- **Lector reporta resultados diferentes:** Verifica altitud, equipo y diferencias de marca de ingredientes. Agrega notas de troubleshooting.
- **El escalado produce medidas impares:** Redondea a la medida práctica más cercana. "2.5 cucharadas" se convierte en "2 cucharadas más 1.5 cucharaditas."
- **Se solicitan sustituciones dietéticas:** Agrega una sección de sustituciones cubriendo los 3 principales cambios dietéticos (sin lácteos, sin gluten, vegetariano).
