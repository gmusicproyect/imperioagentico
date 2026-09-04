---
name: analisis-encuesta
description: "Analiza resultados de encuestas con resúmenes estadísticos, tabulaciones cruzadas, identificación de tendencias y recomendaciones de insights accionables. Utiliza cuando interpretes datos de encuestas para decisiones."
allowed-tools: Read Write Glob
metadata:
  author: Imperio Digital
  version: "1.0"
---

# Análisis de Encuesta

## Cuándo Usar Este Skill

Utiliza este skill cuando necesites:
- Analizar resultados de una encuesta de cliente, empleado o investigación de mercado
- Generar resúmenes estadísticos e identificar patrones significativos
- Crear tabulaciones cruzadas para encontrar diferencias de segmentos
- Convertir datos de encuesta crudos en recomendaciones comerciales accionables

**NO** utilices este skill para diseñar encuestas, ejecutar software estadístico o análisis de investigación académica. Esto es para interpretación de encuestas comerciales prácticas.

---

## Principio Fundamental

LOS DATOS DE ENCUESTA SOLO TIENEN VALOR CUANDO CONDUCEN A UNA DECISIÓN — TODO ANÁLISIS DEBE TERMINAR CON "AQUÍ ESTÁ QUÉ HACER AL RESPECTO."

---

## Fase 1: Brief

### Entradas Requeridas

| Entrada | Qué Preguntar | Por Defecto |
|---------|--------------|------------|
| **Tipo de encuesta** | "¿Qué tipo de encuesta? (satisfacción del cliente, NPS, investigación de mercado, engagement de empleados)" | Satisfacción del cliente |
| **Cantidad de respuestas** | "¿Cuántas respuestas recibiste?" | Debe proporcionarse |
| **Preguntas clave** | "¿Qué preguntas comerciales debería responder el análisis?" | Debe proporcionarse |
| **Formato de datos** | "¿Cómo se almacenan los datos? (CSV, Google Sheets, exportación de plataforma crudos)" | Hoja de cálculo |
| **Segmentos** | "¿Algún segmento a comparar? (tipo de cliente, nivel de plan, demografía)" | Ninguno — análisis general |
| **Puntos de referencia anteriores** | "¿Tienes resultados de encuestas previas o puntos de referencia industriales para comparar?" | Sin datos previos |

**PUNTO DE CONTROL:** Confirma el brief y revisa los datos antes de continuar.

---

## Fase 2: Analizar

### Marco de Análisis

1. **Descripción general de respuestas** — respuestas totales, tasa de respuesta, tasa de finalización
2. **Estadísticas de resumen** — medias, medianas, distribuciones para preguntas cuantitativas
3. **Análisis de frecuencia** — recuentos de respuestas y porcentajes para preguntas categóricas
4. **Tabulaciones cruzadas** — compara respuestas en segmentos clave
5. **Identificación de tendencias** — patrones, valores atípicos y grupos notables
6. **Clasificación de preguntas abiertas** — categoriza respuestas de texto libre en temas

### Directrices Estadísticas

- Reporta la tasa de respuesta y nota si está por debajo de 20% (posible sesgo de no respuesta)
- Usa mediana para distribuciones sesgadas, media para distribuciones normales
- Nota los tamaños de muestra por segmento — no saques conclusiones de grupos menores a 30
- Señala diferencias estadísticamente pequeñas — una brecha de 2% con 50 respuestas es ruido

**PUNTO DE CONTROL:** Presenta hallazgos preliminares y confirma áreas de enfoque antes de construir el reporte completo.

---

## Fase 3: Construir

### Entregables

**1. Resumen Ejecutivo (1 página)**
- Los 3-5 hallazgos principales en lenguaje simple
- Números de métricas clave principales
- Acciones recomendadas

**2. Reporte de Análisis Detallado**
- Sección para cada pregunta de encuesta o grupo de preguntas
- Visualizaciones: gráficos de barras para categóricas, gráficos de distribución para preguntas de escala
- Tablas de tabulación cruzada para comparaciones de segmentos
- Temas de respuestas abiertas con citas representativas

**3. Mapa de Insight-Acción**
| Hallazgo | Implicación | Acción Recomendada | Prioridad |
|---------|------------|-------------------|----------|
| NPS bajó 15 puntos | Sentimiento del cliente declinando | Investiga quejas principales, prioriza arreglos | Alto |

**4. Tablas de Resumen de Datos Crudos**
- Tablas limpias con todos los datos de respuesta agregados
- Lista para copiar-pegar en presentaciones o reportes

---

## Fase 4: Pulir

### Paquete de Presentación

Formatea los hallazgos clave para compartir:
- Estructura de mazo de resumen de 5 diapositivas (descripción general, hallazgos principales, insights de segmento, recomendaciones, próximos pasos)
- Puntos de conversación para cada diapositiva
- Preguntas anticipadas y respuestas

### Recomendaciones de Seguimiento

- Qué investigar más basado en hallazgos
- Preguntas de encuesta de seguimiento sugeridas para el siguiente ciclo
- Cronograma recomendado para la próxima encuesta

---

## Ejemplo 1: Encuesta NPS (200 respuestas, producto SaaS)

**Salidas clave:** Puntuación NPS con desglose promotor/pasivo/detractor, NPS por segmento de cliente, 5 temas principales de comentarios de detractores, 3 acciones prioritarias para mejorar puntuación.

## Ejemplo 2: Encuesta Posterior a Compra (500 respuestas, e-commerce)

**Salidas clave:** Puntuación de satisfacción, razones principales de compra, calificaciones de calidad de producto, calificaciones de experiencia de entrega, probabilidad de recompra, sugerencias de mejora de texto abierto clasificadas y clasificadas por rango.

---

## Anti-Patrones

- **Reportar sin interpretar** — "42% dijo sí" es datos, no análisis. Siempre añade "lo que significa..." y "por lo tanto deberíamos..."
- **Seleccionar resultados** — reportar solo hallazgos favorables socava la confianza. Incluye las malas noticias con recomendaciones.
- **Sobre-interpretar muestras pequeñas** — 10 respuestas de clientes empresariales no es suficiente para sacar conclusiones de segmento. Declara limitaciones.
- **Ignorar respuestas de texto abierto** — las respuestas de texto libre a menudo contienen los insights más accionables. Siempre clasificalos y analízalos.
- **Parálisis de análisis** — un reporte de 50 páginas que nadie lee es peor que un resumen de 2 páginas con acciones claras.

---

## Recuperación

- **Baja tasa de respuesta:** Reconoce la limitación desde el inicio. Enfócate en insights direccionales en lugar de porcentajes precisos.
- **Resultados contradictorios:** Segmenta los datos — las contradicciones a menudo se resuelven cuando divides por tipo de cliente o demografía.
- **Sin hallazgos accionables:** Reencuadra el análisis alrededor de las preguntas comerciales originales. Si la encuesta no las respondió, recomienda mejores preguntas para la próxima vez.
- **Problemas de calidad de datos:** Señala respuestas inválidas o sospechosas (todas las mismas respuestas, combinaciones imposibles). Limpia antes de analizar.