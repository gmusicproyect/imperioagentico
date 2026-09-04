---
name: auditoria-pagina-destino
description: Audita páginas de destino para CRO (optimización de conversión) con recomendaciones de layout, copy, social proof y CTA. Usa cuando necesites mejorar la tasa de conversión de una página de destino o identificar por qué una página está teniendo bajo desempeño.
allowed-tools: Read Write Glob
author: Imperio Digital
version: "1.0"
---

# Auditoría de Página de Destino

## Cuándo Usar Este Skill

Usa este skill cuando necesites:
- Auditar una página de destino existente para oportunidades de optimización de conversión
- Identificar por qué una página de destino tiene una baja tasa de conversión
- Obtener recomendaciones accionables para mejorar layout, copy, social proof y CTAs
- Preparar un reporte de auditoría estructurado para un cliente o equipo

**NO** uses este skill para auditorías completas de sitio web, auditorías SEO o construcción de una nueva página de destino desde cero. Esto es específicamente para evaluar y mejorar una página de destino existente.

---

## Principio Fundamental

CADA RECOMENDACIÓN DEBE VINCULARSE DIRECTAMENTE A UN RESULTADO DE CONVERSIÓN — NUNCA SUGIERAIS CAMBIOS POR RAZONES ESTÉTICAS SOLAS.

---

## Fase 1: Ingesta de Página

Antes de auditar, recopila la información necesaria para evaluar la página en contexto.

### Información Requerida

Pregunta al usuario por cada una. Si no proporciona una, usa el por defecto.

| Input | Qué Preguntar | Por Defecto |
|-------|------------|---------|
| **URL de página o contenido** | "Comparte la URL de página de destino o pega el HTML/copy." | Sin defecto — debe proporcionarse |
| **Objetivo de página** | "¿Cuál es la única acción de conversión? (comprar, registrarse, reservar llamada, descargar)" | Captura de leads (opt-in de email) |
| **Audiencia objetivo** | "¿Para quién está diseñada esta página?" | Propietarios de pequeños negocios y solopreneurs |
| **Fuente de tráfico** | "¿De dónde viene la mayoría del tráfico? (anuncios, orgánico, email, social)" | Anuncios pagados |
| **Tasa de conversión actual** | "¿Cuál es la tasa de conversión actual, si se conoce?" | Desconocida |

**PUNTO DE CONTROL: No procedas hasta que el usuario proporcione el contenido o URL de página y confirme el objetivo.**

---

## Fase 2: Marco de Auditoría

Evalúa la página de destino en estos cinco pilares. Califica cada uno 1-10 y proporciona hallazgos específicos.

### 1. Impacto Above-the-Fold (Primera Pantalla)

- **Claridad del encabezado:** ¿Comunica la oferta en menos de 5 segundos?
- **Propuesta de valor:** ¿Es obvio el beneficio sin desplazarse?
- **Jerarquía visual:** ¿Fluye naturalmente el ojo al CTA?
- **Imagen/video héroe:** ¿Apoya el mensaje o distrae?
- **Visibilidad del CTA:** ¿Hay un CTA (call to action) claro y visible above-the-fold?

### 2. Copy y Mensajería

- **Coincidencia encabezado-anuncio:** ¿El encabezado de página coincide con la promesa de fuente de tráfico?
- **Ratio beneficio vs. característica:** ¿Los beneficios lideran, con características apoyando?
- **Especificidad:** ¿Están respaldados los reclamos por números, marcos de tiempo o resultados concretos?
- **Manejo de objeciones:** ¿El copy aborda las 3 principales objeciones de compra?
- **Nivel de lectura:** ¿Es el copy accesible (objetivo 6º-8º grado)?

### 3. Social Proof y Confianza

- **Testimonios:** ¿Hay testimonios específicos y atribuidos con resultados?
- **Insignias de confianza:** ¿Logos, certificaciones, sellos de seguridad, menciones de medios?
- **Números:** ¿Conteo de usuarios, resultados logrados, años en negocio?
- **Reversión de riesgo:** ¿Garantía de devolución de dinero, prueba gratuita, lenguaje sin compromiso?

### 4. CTA y Elementos de Conversión

- **Copy de CTA:** ¿El texto del botón comunica valor (no solo "Enviar")?
- **Frecuencia de CTA:** ¿Hay un CTA al menos cada 2 longitudes de desplazamiento?
- **Fricción de formulario:** ¿Cuántos campos? ¿Se puede eliminar alguno?
- **Urgencia/escasez:** ¿Hay elementos legítimos de urgencia?

### 5. Layout y UX

- **Responsividad móvil:** ¿Funciona en móvil sin desplazamiento horizontal?
- **Velocidad de página:** ¿Hay imágenes pesadas o scripts ralentizando el tiempo de carga?
- **Auditoría de distracción:** ¿Hay enlaces de navegación, barras laterales o enlaces externos distrayendo la atención?
- **Espacio en blanco:** ¿Es la página escaneable o visualmente desordenada?

---

## Fase 3: Reporte

Entrega la auditoría como un reporte estructurado con calificaciones y recomendaciones priorizado.

### Formato de Reporte

```
## Reporte de Auditoría de Página de Destino

**Página:** [URL o nombre de página]
**Objetivo:** [Acción de conversión]
**Fecha de Auditoría:** [Fecha]

### Calificaciones

| Pilar | Calificación (1-10) | Prioridad |
|--------|-------------|----------|
| Above-the-Fold | X | Alto/Medio/Bajo |
| Copy y Mensajería | X | Alto/Medio/Bajo |
| Social Proof y Confianza | X | Alto/Medio/Bajo |
| CTA y Conversión | X | Alto/Medio/Bajo |
| Layout y UX | X | Alto/Medio/Bajo |
| **General** | **X/10** | |

### Top 5 Recomendaciones (Orden de Prioridad)

1. [Cambio específico] — [Impacto esperado] — [Esfuerzo: Bajo/Medio/Alto]
2. ...

### Hallazgos Detallados

[Desglose sección por sección con observaciones específicas y correcciones]
```

---

## Fase 4: Victorias Rápidas

Después del reporte completo, entrega una lista corta de cambios que el usuario puede implementar en menos de 1 hora.

- Identifica 3-5 cambios que requieren esfuerzo mínimo pero impacto alto
- Proporciona copy de encabezado o CTA reescrito si esos obtuvieron calificación baja
- Sugiere ideas de prueba A/B para las 2 principales recomendaciones

---

## Ejemplo: Página de Destino de Prueba Gratuita de SaaS

**Ingesta:** Herramienta de SaaS para gestión de proyectos, dirigida a freelancers, tráfico de Google Ads, tasa de conversión del 2.1%, objetivo es registro de prueba gratuita.

**Extracto de hallazgo:**
- El encabezado dice "Project Management Made Easy" — genérico, sin especificidad. Reescribe: "Manage Every Client Project in One Dashboard — Free for 14 Days"
- El botón CTA dice "Get Started" — reescribe a "Start My Free Trial"
- Sin testimonios above-the-fold — mueve el testimonial más fuerte a la sección hero
- El formulario pregunta por número de teléfono — elimínalo, reduce fricción

---

## Anti-Patrones

- **Sugerir rediseños sin datos** — basa cada recomendación en principios de conversión, no en gusto personal
- **Sobrecargar con 20+ recomendaciones** — prioriza el top 5 que moverá la aguja
- **Ignorar contexto de fuente de tráfico** — una página que recibe tráfico de anuncio frío necesita elementos diferentes que tráfico de email cálido
- **Consejo genérico** — "hazlo mejor" no es accionable. Proporciona reescrituras de copy específicas y cambios de layout
- **Comentario solo estético** — "los colores no coinciden" no es una recomendación de conversión a menos que impacte legibilidad

---

## Recuperación

- **Sin URL o contenido proporcionado:** Pide al usuario que pegue el copy de página, captura de pantalla o HTML. No se puede auditar sin ver la página.
- **Múltiples páginas a auditar:** Audita una a la vez. Ofrece crear una matriz de comparación si tienen 2-3 variantes.
- **El usuario quiere una auditoría completa de sitio web:** Redirige — este skill cubre una página de destino. Sugiere auditar su página con mayor tráfico primero.
- **Sin datos de conversión disponibles:** Procede con la auditoría pero nota que las recomendaciones se basan en mejores prácticas, no en insights basados en datos. Recomienda configurar rastreo.
