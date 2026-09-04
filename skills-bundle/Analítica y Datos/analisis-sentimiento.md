---
name: analisis-sentimiento
description: "Analiza el sentimiento del cliente desde reseñas, redes sociales y tickets de soporte con seguimiento de tendencias, categorización de temas y recomendaciones de alerta. Utiliza para monitoreo de salud de marca."
allowed-tools: Read Write Glob
metadata:
  author: Imperio Digital
  version: "1.0"
---

# Análisis de Sentimiento

## Cuándo Usar Este Skill

Utiliza este skill cuando necesites:
- Analizar el sentimiento del cliente desde reseñas, posts en redes sociales o tickets de soporte
- Rastrear tendencias de percepción de marca en el tiempo
- Categorizar temas de feedback para priorizar mejoras de producto o servicio
- Configurar un marco de monitoreo de sentimiento para uso continuo

**NO** utilices este skill para creación de contenido de redes sociales, escritura de respuestas de servicio al cliente o construcción de modelos NLP. Esto es para interpretar y actuar sobre datos de sentimiento del cliente.

---

## Principio Fundamental

EL SENTIMIENTO ES UN INDICADOR ADELANTADO — EL SENTIMIENTO DECLINANTE PREDICE CHURN, RESEÑAS NEGATIVAS Y PÉRDIDA DE INGRESOS ANTES DE QUE APAREZCAN EN TUS FINANZAS.

---

## Fase 1: Brief

### Entradas Requeridas

| Entrada | Qué Preguntar | Por Defecto |
|---------|--------------|------------|
| **Fuentes de datos** | "¿Dónde está la feedback? (reseñas de Google, App Store, redes sociales, tickets de soporte, encuestas)" | Debe proporcionarse |
| **Volumen** | "¿Aproximadamente cuántas piezas de feedback analizar?" | 50-200 |
| **Período de tiempo** | "¿Qué rango de fechas?" | Últimos 90 días |
| **Enfoque** | "¿Qué quieres entender? (sentimiento general, producto específico, comparación de competidores)" | Sentimiento general de marca |
| **Segmentos** | "¿Algún segmento a analizar por separado? (línea de producto, nivel de cliente, canal)" | General primero |
| **Seguimiento existente** | "¿Tienes algún seguimiento de sentimiento en lugar?" | Ninguno |

**PUNTO DE CONTROL:** Confirma el brief antes de continuar.

---

## Fase 2: Analizar

### Marco de Puntuación de Sentimiento

Clasifica cada pieza de feedback:
- **Positivo** — elogio, satisfacción, recomendación
- **Neutral** — factual, sin emoción fuerte, mixto
- **Negativo** — queja, frustración, advertencia a otros

### Categorización de Temas

Etiqueta cada pieza de feedback con 1-2 temas:
- Calidad del producto, precios, servicio al cliente, entrega/velocidad, usabilidad, solicitudes de características, menciones de competidores, problemas de facturación

### Dimensiones de Análisis

1. **Distribución de sentimiento general** — % positivo, neutral, negativo
2. **Sentimiento por tema** — ¿qué tópicos generan la mayoría negatividad?
3. **Tendencia de sentimiento** — ¿el sentimiento mejora o declina con el tiempo?
4. **Tendencia de volumen** — ¿habla más gente? (aumento de volumen + sentimiento negativo = alarma)
5. **Menciones competitivas** — ¿cuán a menudo mencionan clientes a competidores y en qué contexto?

**PUNTO DE CONTROL:** Presenta hallazgos preliminares y confirma áreas de enfoque para el reporte completo.

---

## Fase 3: Construir

### Entregables

**1. Reporte de Análisis de Sentimiento**
- Puntuación de sentimiento general y distribución
- Desglose de sentimiento tema por tema
- Gráfico de tendencia en el período de análisis
- Top 10 citas representativas (positivas y negativas)
- Resumen de menciones competitivas

**2. Matriz de Prioridad de Problemas**
| Tema | Sentimiento | Volumen | Tendencia | Prioridad |
|------|-----------|--------|----------|----------|
| Servicio al cliente | Negativo | Alto | Empeorando | Crítico |
| Calidad del producto | Positivo | Alto | Estable | Proteger |
| Precios | Mixto | Medio | Estable | Monitorear |

**3. Marco de Alerta**
Define disparadores para monitoreo continuo:
- El sentimiento negativo excede 30% en cualquier semana
- Aparece nuevo tema negativo que no se rastreaba previamente
- La calificación de estrellas cae por debajo de 4.0 en cualquier plataforma de reseña
- El competidor se menciona positivamente más del 10% del tiempo

**4. Playbook de Respuesta**
- Plantillas de respuesta para temas negativos comunes
- Criterios de escalación para quejas serias
- Disparadores de alcance proactivo para clientes en riesgo

---

## Fase 4: Pulir

### Especificación de Dashboard de Monitoreo

Recomienda un sistema de seguimiento simple:
- Puntuación de sentimiento semanal por fuente
- Seguimiento de tendencia de temas (mensual)
- Registro de alerta para notificaciones disparadas

### Revisión de Sentimiento Trimestral

Plantilla para un análisis profundo trimestral comparando sentimiento actual con trimestre anterior con actualizaciones del plan de acción.

---

## Ejemplo 1: Reseñas de App Store (150 reseñas, app móvil SaaS)

**Hallazgo:** 72% positivo, 18% negativo, 10% neutral. Tema negativo superior: confusión de onboarding (8 menciones). Positivo superior: características de ahorro de tiempo.
**Acción:** Mejora flujo de onboarding, crea videos de tutorial.

## Ejemplo 2: Reseñas de Google (80 reseñas, negocio de servicio local)

**Hallazgo:** 4.2 estrellas promedio. Las reseñas negativas se agrupan alrededor de tiempos de espera (6 menciones) y claridad de facturación (4 menciones). Las reseñas positivas destacan calidad del personal.
**Acción:** Aborda comunicación de tiempo de espera, simplifica facturas de facturación.

---

## Anti-Patrones

- **Ignorar feedback negativa** — 1 reseña negativa a menudo representa 10 clientes silenciosos que se van. Toma las quejas en serio.
- **Contar estrellas sin leer texto** — una reseña de 3 estrellas con feedback específica es más útil que un "¡Excelente!" de 5 estrellas. Lee el contenido.
- **Analizar una vez y olvidar** — el sentimiento cambia con el tiempo. Configura monitoreo continuo, no reportes únicos.
- **Responder defensivamente** — el análisis de sentimiento negativo debería impulsar mejora, no respuestas PR defensivas.
- **Reaccionar excesivamente a una mala reseña** — busca patrones. Una queja es una anécdota; cinco sobre el mismo tema es una tendencia.

---

## Recuperación

- **Muy pocas reseñas para analizar:** Complementa con datos de ticket de soporte, comentarios en redes sociales o entrevistas directas con clientes.
- **Abrumadoramente positivo (sospechoso):** Profundiza — ¿se incentivan las reseñas? Verifica patrones sugerentes de reseñas falsas.
- **El usuario toma feedback negativa personalmente:** Reencuadra como una ventaja competitiva — ahora sabes exactamente qué arreglar. Los competidores están adivinando.
- **Sin recursos de monitoreo continuo:** Configura Google Alerts y una revisión mensual de 30 minutos. El monitoreo de bajo esfuerzo supera a ningún monitoreo.