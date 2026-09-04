---
name: analisis-retroalimentacion
description: "Analiza datos de feedback del cliente para identificar temas, patrones de sentimiento y prioridades de mejora accionables para decisiones de producto y servicio."
allowed-tools: Read Write Glob
metadata:
  author: Imperio Digital
  version: "1.0"
---

# Análisis de Feedback

## Cuándo Usar Este Skill

Utiliza este skill cuando necesites:
- Analizar una colección de feedback del cliente para encontrar patrones accionables
- Identificar temas recurrentes y tendencias de sentimiento en reseñas, encuestas o tickets de soporte
- Priorizar mejoras basadas en frecuencia de feedback e impacto comercial
- Crear un reporte de resumen de feedback para la toma de decisiones

**NO** utilices este skill para recopilar feedback (usa satisfaction-survey o nps-survey), responder a reseñas individuales o construir sistemas de recopilación de feedback. Esto es para analizar datos de feedback existentes.

---

## Principio Fundamental

LA RETROALIMENTACIÓN DEL CLIENTE ES RUIDOSA — EL VALOR NO ESTÁ EN NINGUNA RESPUESTA INDIVIDUAL SINO EN LOS PATRONES A TRAVÉS DE MUCHAS. TU TRABAJO ES ENCONTRAR LA SEÑAL EN EL RUIDO Y CONVERTIRLA EN ACCIÓN.

---

## Fase 1: Recopilar Datos

Recopila y organiza la feedback antes del análisis.

### Entradas Requeridas

| Entrada | Qué Preguntar | Por Defecto |
|---------|--------------|------------|
| **Fuente de feedback** | "¿Dónde está la feedback? (encuestas, reseñas, tickets de soporte, redes sociales, emails)" | Múltiples fuentes |
| **Volumen** | "¿Aproximadamente cuántas piezas de feedback analizaremos?" | 20-100 |
| **Período de tiempo** | "¿Qué período de tiempo cubre esta feedback?" | Últimos 90 días |
| **Producto/servicio** | "¿A qué producto o servicio se relaciona esta feedback?" | Sin valor por defecto |
| **Problemas conocidos** | "¿Hay problemas que ya sospechas que aparecerán?" | Sin valor por defecto |

### Organización de Datos

```
## Inventario de Feedback

| Fuente | Cantidad | Rango de Fechas | Formato |
|--------|----------|---------|---------|
| Respuestas de encuesta | [#] | [Rango] | Calificaciones + texto abierto |
| Reseñas en línea | [#] | [Rango] | Calificación de estrellas + texto |
| Tickets de soporte | [#] | [Rango] | Texto |
| Menciones en redes sociales | [#] | [Rango] | Texto |
| Emails directos | [#] | [Rango] | Texto |
| **Total** | **[#]** | | |
```

**PUNTO DE CONTROL:** Confirma las fuentes de datos y volumen antes de comenzar el análisis.

---

## Fase 2: Analizar

Identifica temas, sentimiento y patrones.

### Identificación de Temas

Agrupa la feedback en temas etiquetando cada pieza:

```
## Análisis de Temas

| Tema | Frecuencia | % del Total | Sentimiento | Citas de Muestra |
|------|-----------|-----------|-------------|---------------|
| [Tema 1] | [#] menciones | [%] | Positivo/Negativo/Mixto | "[Cita]" |
| [Tema 2] | [#] menciones | [%] | Positivo/Negativo/Mixto | "[Cita]" |
| [Tema 3] | [#] menciones | [%] | Positivo/Negativo/Mixto | "[Cita]" |
```

### Desglose de Sentimiento

```
## Sentimiento General

| Sentimiento | Cantidad | % del Total |
|-----------|---------|-----------|
| Positivo | [#] | [%] |
| Neutral | [#] | [%] |
| Negativo | [#] | [%] |

**Sentimiento neto:** [% Positivo - % Negativo]
**Tendencia vs período anterior:** Mejorando / Estable / Declinando
```

### Matriz de Tema-Sentimiento

Cruza referencias de temas con sentimiento para encontrar dónde se agrupan problemas y fortalezas:

```
## Matriz Tema x Sentimiento

| Tema | Positivo | Neutral | Negativo | Neto |
|------|----------|---------|----------|-----|
| Calidad del producto | [#] | [#] | [#] | [+/-] |
| Soporte al cliente | [#] | [#] | [#] | [+/-] |
| Precio/valor | [#] | [#] | [#] | [+/-] |
| Facilidad de uso | [#] | [#] | [#] | [+/-] |
```

**PUNTO DE CONTROL:** Presenta el análisis para revisión antes de construir recomendaciones.

---

## Fase 3: Priorizar

Convierte el análisis en elementos de acción priorizados.

### Matriz de Impacto-Esfuerzo

Puntúa cada tema por impacto comercial y esfuerzo para arreglarlo:

```
## Matriz de Prioridad de Mejora

| Tema | Frecuencia | Impacto Comercial (1-5) | Esfuerzo para Arreglarlo (1-5) | Puntuación de Prioridad | Acción |
|------|-----------|---------------------|--------------------|--------------:|--------|
| [Tema] | [#] | [X] | [X] | [Impacto x Frecuencia / Esfuerzo] | Arreglar Ahora / Planificar / Monitorear |
```

### Plan de Acción

```
## Plan de Acción Impulsado por Feedback

### Arreglar Ahora (Alto impacto, esfuerzo manejable)
1. **[Tema]:** [Acción específica] — Responsable: [Nombre] — Fecha límite: [Fecha]
2. **[Tema]:** [Acción específica] — Responsable: [Nombre] — Fecha límite: [Fecha]

### Planificar para Próximo Trimestre (Alto impacto, alto esfuerzo)
1. **[Tema]:** [Enfoque y cronograma]

### Monitorear (Baja frecuencia, pero observar crecimiento)
1. **[Tema]:** Revisar de nuevo en [marco de tiempo]

### Celebrar (Temas positivos para amplificar)
1. **[Tema]:** Usar en marketing, testimonios y casos de estudio
```

---

## Fase 4: Reportar

Entrega un resumen claro de feedback para las stakeholders.

### Plantilla de Resumen Ejecutivo

```
## Análisis de Feedback del Cliente — [Período]

### Números Clave
- **Feedback analizada:** [#]
- **Sentimiento general:** [X]% positivo, [X]% negativo
- **Tema positivo principal:** [Tema] ([#] menciones)
- **Tema negativo principal:** [Tema] ([#] menciones)

### 3 Hallazgos Principales
1. [Hallazgo con punto de datos]
2. [Hallazgo con punto de datos]
3. [Hallazgo con punto de datos]

### Acciones Recomendadas
1. [Acción + impacto esperado]
2. [Acción + impacto esperado]
3. [Acción + impacto esperado]

### Citas Notables
- "[Cita poderosa del cliente — positiva]"
- "[Cita poderosa del cliente — negativa]"
```

### Cierra el Ciclo

Después de implementar cambios, comunica de vuelta a los clientes:
- Email o post "Preguntaste, escuchamos"
- Referencia temas de feedback específicos y qué cambió
- Esto genera confianza y fomenta feedback futura

---

## Anti-Patrones

- **Seleccionar feedback** — analizar solo respuestas positivas o solo negativas sesga el panorama. Incluye todo.
- **Actuar en una queja fuerte** — un email enojado es anecdótico. Tres personas diciendo lo mismo es un patrón.
- **Análisis sin acción** — un reporte que se queda en una carpeta no cambia nada. Todo análisis necesita un plan de acción.
- **Ignorar feedback positiva** — los temas positivos revelan tu ventaja competitiva. Amplificalos en marketing.
- **Analizar sin contexto** — 10 quejas sobre precio después de un aumento de precio es esperado, no alarmante. El contexto importa.

---

## Recuperación

- **No hay suficiente feedback para encontrar patrones:** Menos de 20 respuestas, trata cada pieza individualmente. Los patrones emergen en 30+ respuestas.
- **Toda la feedback es positiva (parece demasiado bueno):** Verifica el sesgo de selección — ¿solo responden clientes felices? Añade preguntas de seguimiento que inviten crítica constructiva.
- **Abrumado por volumen:** Comienza con los últimos 30 días. Busca temas en la feedback negativa primero — ahí es donde viven los insights de mayor valor.
- **Feedback se contradice a sí misma:** Segmenta por tipo de cliente. Usuarios de poder y usuarios nuevos a menudo tienen feedback opuesta. Ambas son válidas para su segmento.
- **El usuario no sabe qué hacer con los hallazgos:** Comienza con el tema negativo de mayor frecuencia. Arregla esa una cosa. Luego repite.