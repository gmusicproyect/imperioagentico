---
name: plan-prueba-ab
description: "Diseña planes de prueba A/B con hipótesis, variantes, cálculos de tamaño de muestra, métricas de éxito y criterios de significancia estadística. Utiliza cuando optimices conversiones o UX."
allowed-tools: Read Write Glob
metadata:
  author: Imperio Digital
  version: "1.0"
---

# Plan de Prueba A/B

## Cuándo Usar Este Skill

Utiliza este skill cuando necesites:
- Planificar una prueba A/B para una página de destino, email, anuncio o función
- Calcular el tamaño de muestra requerido y la duración de la prueba
- Definir criterios de éxito claros antes de ejecutar un experimento
- Documentar resultados de prueba y decidir si implementar el ganador

**NO** utilices este skill para pruebas multivariantes con 5+ variables, experimentos de investigación científica o ejercicios de estadística teórica. Esto es para pruebas A/B prácticas de negocio.

---

## Principio Fundamental

TODA PRUEBA DEBE TENER UNA HIPÓTESIS ESCRITA ANTES DE QUE COMIENCE LA PRUEBA — SI NO PUEDES DECIR QUÉ ESPERAS Y POR QUÉ, ESTÁS ADIVINANDO, NO PROBANDO.

---

## Fase 1: Brief

### Entradas Requeridas

| Entrada | Qué Preguntar | Por Defecto |
|---------|--------------|------------|
| **Qué probar** | "¿Qué estás probando? (titular, CTA, página de precios, línea de asunto de email, creatividad de anuncio)" | Debe proporcionarse |
| **Métrica actual** | "¿Cuál es la tasa de conversión actual o la métrica que deseas mejorar?" | Debe proporcionarse o estimarse |
| **Objetivo** | "¿Qué mejora sería significativa? (p. ej., +20% tasa de conversión)" | 10-20% de mejora relativa |
| **Tráfico/volumen** | "¿Cuánto tráfico o cuántas impresiones obtiene este activo por semana?" | Debe proporcionarse |
| **Herramienta** | "¿Qué herramienta de prueba usarás? (Google Optimize, VWO, Optimizely, nativa)" | Google Optimize o plataforma nativa |
| **Tolerancia al riesgo** | "¿Qué tan confiado necesitas estar? (90%, 95%, 99%)" | 95% de significancia estadística |

**PUNTO DE CONTROL:** Confirma el brief antes de continuar.

---

## Fase 2: Diseño

### Marco de Hipótesis

Escribe la hipótesis usando este formato:

**"Si cambiamos [cambio], entonces [métrica] se [mejorará/aumentará/disminuirá] porque [razón basada en insight de comportamiento del usuario]."**

Ejemplo: "Si cambiamos el texto del botón CTA de 'Saber más' a 'Comenzar Prueba Gratuita', entonces la tasa de clics aumentará 15% porque establece una expectativa más clara del siguiente paso."

### Elementos de Diseño de Prueba

1. **Control (A)** — versión actual, descrita específicamente
2. **Variante (B)** — versión modificada, con una única diferencia clara
3. **Métrica primaria** — la métrica única que determina el ganador
4. **Métricas secundarias** — métricas de soporte para observar efectos no intencionados
5. **Cálculo del tamaño de muestra** — visitantes mínimos por variante
6. **Duración de la prueba** — días para ejecutar basados en tráfico y tamaño de muestra
7. **Segmentación** — cualquier segmento de audiencia para analizar por separado

### Orientación del Tamaño de Muestra

Proporciona el contexto de la fórmula:
- Tasa de conversión basal + efecto mínimo detectable + nivel de significancia = muestra requerida por variante
- Regla general: en 5% basal, detectar un 20% de elevación relativa a 95% de significancia requiere ~4,000 visitantes por variante

**PUNTO DE CONTROL:** Presenta el plan de prueba y espera aprobación.

---

## Fase 3: Construir

### Entregables

**1. Documento Completo del Plan de Prueba**
- Declaración de hipótesis
- Descripciones de control y variante con notas de mockup visual
- Métricas primarias y secundarias
- Estimación de tamaño de muestra y duración
- Fechas de inicio y fin
- Criterios de decisión (qué puntuación significa "ganador")

**2. Checklist Previo al Lanzamiento**
- [ ] Hipótesis documentada
- [ ] Control y variante construidos y probados en QA
- [ ] Seguimiento verificado en ambas versiones
- [ ] División de tráfico configurada (50/50 por defecto)
- [ ] Sin otras pruebas ejecutándose en la misma página/audiencia
- [ ] Duración mínima comprometida (no mires antes)

**3. Plantilla de Documentación de Resultados**
- Tabla de desempeño de variantes (métrica, muestra, tasa de conversión, intervalo de confianza)
- Declaración de ganador con nivel de confianza
- Recomendación: implementar, iterar o descartar
- Aprendizajes para futuras pruebas

---

## Fase 4: Pulir

### Marco de Análisis Posterior a la Prueba

1. **¿Alcanzó significancia?** Si no, extiende o llámalo inconcluso — nunca declares un ganador por debajo del umbral.
2. **Verifica métricas secundarias** — ¿hirió el ganador algo más? (p. ej., más clics pero tasa de compra más baja)
3. **Análisis de segmentos** — ¿ganó la variante en todos los segmentos o solo en específicos?
4. **Documenta el aprendizaje** — incluso las pruebas fallidas enseñan algo. Registra el insight.

### Recomendación de Velocidad de Prueba

Sugiere una cadencia de pruebas: 1-2 pruebas por mes para pequeños negocios. Mantén una cartera de pruebas clasificada por impacto potencial.

---

## Ejemplo 1: Prueba de Titular de Página de Destino

**Hipótesis:** Cambiar el titular de enfocado en beneficio ("Ahorra 10 Horas por Semana") a enfocado en dolor ("Deja de Perder 10 Horas en Tareas que AI Puede Manejar") aumentará la tasa de registro 15%.
**Duración:** 3 semanas con 500 visitantes/semana. **Métrica primaria:** Tasa de registro de email.

## Ejemplo 2: Prueba de Línea de Asunto de Email

**Hipótesis:** Añadir el nombre del destinatario a la línea de asunto aumentará la tasa de apertura 10%.
**Duración:** Envío único a 5,000 suscriptores, dividido 50/50. **Métrica primaria:** Tasa de apertura.

---

## Anti-Patrones

- **Probar sin hipótesis** — cambios aleatorios no enseñan nada. Declara tu predicción y razonamiento primero.
- **Mirar resultados temprano** — verificar diariamente y parar cuando "se vea bien" infla falsos positivos. Comprométete con la duración.
- **Probar demasiadas variables** — si cambias el titular, la imagen Y el CTA, no puedes atribuir el resultado. Un cambio por prueba.
- **Tamaños de muestra diminutos** — 50 visitantes por variante no prueba nada. Calcula el mínimo antes de comenzar.
- **Ignorar métricas secundarias negativas** — un titular que obtiene más clics pero menos compras no es un ganador.

---

## Recuperación

- **No hay suficiente tráfico:** Prueba cambios de mayor impacto (efecto mínimo detectable más grande necesita muestra más pequeña). O prueba en email/anuncios donde el volumen es controlable.
- **Prueba es inconclusa:** No declares un ganador. Extiende la prueba o acepta que la diferencia es demasiado pequeña para importar y continúa.
- **El interesado quiere elegir el ganador por intuición:** Muestra las matemáticas. Si los resultados no son significativos, implementar el "ganador" es un lanzamiento de moneda.
- **Sin presupuesto de herramienta de prueba:** Usa herramientas gratuitas (sucesor de Google Optimize, divisiones incorporadas de plataforma de email) o divisiones de URL manuales con seguimiento de analítica.