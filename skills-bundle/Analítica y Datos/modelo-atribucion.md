---
name: modelo-atribucion
description: "Diseña modelos de atribución de marketing con mapeo de canal, lógica de ponderación, recomendaciones de reporteo y pasos de implementación. Utiliza cuando comprendas qué canales impulsan conversiones."
allowed-tools: Read Write Glob
metadata:
  author: Imperio Digital
  version: "1.0"
---

# Modelo de Atribución

## Cuándo Usar Este Skill

Utiliza este skill cuando necesites:
- Entender qué canales de marketing impulsan la mayoría de conversiones
- Elegir un modelo de atribución para decisiones de asignación de presupuesto
- Diseñar un marco de atribución multi-toque
- Reportar en ROI de marketing por canal

**NO** utilices este skill para configurar píxeles de seguimiento, configurar plataformas de publicidad o construir software de atribución. Esto es para diseñar el modelo y marco de reporteo.

---

## Principio Fundamental

LA ATRIBUCIÓN PERFECTA ES IMPOSIBLE — ELIGE UN MODELO QUE SEA LO SUFICIENTEMENTE BUENO PARA TOMAR MEJORES DECISIONES DE PRESUPUESTO QUE ADIVINAR, Y SÉ HONESTO SOBRE SUS LIMITACIONES.

---

## Fase 1: Brief

### Entradas Requeridas

| Entrada | Qué Preguntar | Por Defecto |
|---------|--------------|------------|
| **Canales** | "¿Qué canales de marketing estás usando? (anuncios pagos, SEO, email, redes sociales, referral, directo)" | Debe proporcionarse |
| **Tipo de conversión** | "¿Qué es una conversión? (compra, registro, reserva de demostración, envío de formulario de lead)" | Envío de formulario de lead |
| **Ciclo de ventas** | "¿Cuánto tiempo desde primer toque hasta conversión? (mismo día, días, semanas, meses)" | 1-2 semanas |
| **Presupuesto** | "¿Gasto de marketing mensual en todos los canales?" | $1,000-$5,000 |
| **Configuración de seguimiento** | "¿Qué seguimiento tienes? (UTMs, GA4, CRM, seguimiento de píxel)" | GA4 + UTMs |
| **Necesidad de decisión** | "¿Qué decisión ayudará? (dónde gastar más, qué cortar)" | Asignación de presupuesto |

**PUNTO DE CONTROL:** Confirma el brief antes de continuar.

---

## Fase 2: Diseñar

### Selección de Modelo

Presenta las opciones con pros y contras para el contexto del usuario:

| Modelo | Cómo Funciona | Mejor Para |
|--------|-------------|----------|
| **Último toque** | 100% crédito al canal final | Ciclos de ventas cortos, configuraciones simples |
| **Primer toque** | 100% crédito al canal de descubrimiento | Entender drivers de conciencia |
| **Lineal** | Crédito igual en todos los puntos de contacto | Línea base justa, multi-canal |
| **Decaimiento de tiempo** | Más crédito a toques recientes | Ciclos de ventas más largos |
| **Basado en posición** | 40% primero, 40% último, 20% medio | Crédito equilibrado conciencia + conversión |
| **Impulsado por datos** | Algorítmico basado en rutas reales | Alto volumen, configuraciones sofisticadas |

### Lógica de Modelo Recomendado

Para la mayoría de solopreneurs y pequeños negocios: comienza con **basado en posición** o **último toque** con un reporte de overlay de primer toque. Gradúa a impulsado por datos cuando tengas 500+ conversiones por mes.

**PUNTO DE CONTROL:** Presenta recomendación de modelo y espera aprobación.

---

## Fase 3: Construir

### Entregables

**1. Documento de Modelo de Atribución**
- Modelo seleccionado con fundamento
- Mapa de canal con todos los puntos de contacto y cómo se rastrean
- Lógica de ponderación explicada con ejemplos
- Puntos ciegos conocidos y limitaciones

**2. Mapa de Ruta de Canal-Conversión**
- Viajes típicos de cliente por combinación de canal
- Rutas de ejemplo: Anuncio de redes sociales → Publicación de blog → Email → Compra
- Definiciones de punto de contacto: qué cuenta como "toque" por canal

**3. Plantilla de Reporteo**
- Estructura de reporte de atribución mensual
- Métricas por canal: conversiones, conversiones asistidas, costo por adquisición, ROAS
- Comparación: conversiones atribuidas vs. conversiones reportadas por plataforma (diferirán)

**4. Checklist de Implementación**
- [ ] Parámetros UTM estandarizados en todos los canales
- [ ] Eventos de conversión GA4 configurados
- [ ] Seguimiento de CRM conectado (si aplica)
- [ ] Ventana de atribución definida (7 días, 30 días, 90 días)
- [ ] Primer reporte generado y validado

---

## Fase 4: Pulir

### Validación de Modelo

Después de 30 días, verifica:
- ¿Los números de atribución tienen sentido intuitivo dado tu gasto y esfuerzo?
- ¿Hay canales recibiendo cero crédito a pesar de actividad conocida?
- ¿El modelo cambia tus decisiones de asignación de presupuesto?

### Revisión Trimestral

Reevalúa el ajuste del modelo cada trimestre a medida que los canales, gasto y volumen cambian.

---

## Ejemplo 1: Negocio de Servicios Solo (3 canales, ciclo de ventas corto)

**Canales:** Google Ads, Instagram orgánico, referral
**Modelo:** Último toque (simple, decisivo, suficiente para 3 canales)
**Reporte:** Costo mensual por lead por canal, compara con tasa de cierre

## Ejemplo 2: Marca de E-commerce (6 canales, multi-toque)

**Canales:** Anuncios Meta, anuncios Google, email, SEO, influencer, directo
**Modelo:** Basado en posición (40/20/40) con ventana de atribución de 30 días
**Reporte:** ROAS semanal por canal, conteo de conversión asistida, análisis de ruta

---

## Anti-Patrones

- **Solo reportado por plataforma** — cada plataforma de publicidad toma crédito completo. Facebook y Google ambos reclamarán la misma conversión. Usa seguimiento independiente.
- **Ignorar conversiones asistidas** — un canal con cero conversiones de último toque puede estar generando todos tus primeros toques. Verifica conversiones asistidas antes de cortar.
- **Sobre-ingeniería temprana** — atribución impulsada por datos con 50 conversiones mensuales es ruido, no señal. Haz coincidir complejidad de modelo con volumen de datos.
- **Configurar y olvidar** — los modelos de atribución necesitan recalibración a medida que tu mezcla de canales cambia.
- **Tratar el modelo como verdad** — todos los modelos están equivocados. Úsalos para tomar *mejores* decisiones, no perfectas.

---

## Recuperación

- **Sin seguimiento UTM en lugar:** Comienza etiquetando todos los enlaces hoy. No puedes atribuir lo que no rastreas. Proporciona una guía de configuración UTM.
- **Muy pocas conversiones para multi-toque:** Usa atribución de último toque y complementa con datos cualitativos (encuesta "¿Cómo te enteraste?").
- **Los números de plataforma no coinciden GA4:** Esto es normal. Documenta la discrepancia y usa una fuente de verdad para decisiones.
- **El usuario quiere atribuir todo perfectamente:** Establece expectativas de que 70-80% de precisión es excelente para atribución. Perfect no es alcanzable.