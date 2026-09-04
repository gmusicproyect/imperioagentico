---
name: investigacion-palabras-clave
description: Realiza investigación de palabras clave con estimaciones de volumen de búsqueda, evaluación de dificultad y recomendaciones de mapeo de contenido. Usa cuando planifiques estrategia de contenido dirigida por SEO.
allowed-tools: Read Write Glob
author: Imperio Digital
version: "1.0"
---

# Investigación de Palabras Clave

## Cuándo Usar Este Skill

Usa este skill cuando necesites:
- Identificar palabras clave objetivo para estrategia de contenido SEO
- Evaluar dificultad de palabras clave y potencial de ranking para tu sitio
- Mapear palabras clave a tipos de contenido e intención de búsqueda
- Construir una lista de palabras clave priorizada para planificación de contenido

**NO** uses este skill para listas de palabras clave de búsqueda pagada (usa google-ads-campaign), investigación de hashtags de redes sociales, u optimización de palabras clave de YouTube (usa youtube-seo). Esto es para investigación de palabras clave de búsqueda orgánica.

---

## Principio Fundamental

LA MEJOR PALABRA CLAVE NO ES LA QUE TIENE MÁS BÚSQUEDAS — ES LA DONDE TU CONTENIDO PUEDE REALÍSTICAMENTE RANKEAR Y EL BUSCADOR ES MÁS PROBABLE QUE SE CONVIERTA EN TU CLIENTE.

---

## Fase 1: Briefing

### Información Requerida

| Input | Qué Preguntar | Por Defecto |
|-------|------------|---------|
| **Negocio/nicho** | "¿Qué hace tu negocio?" | Sin defecto — debe proporcionarse |
| **Temas semilla** | "¿Cuáles son 3-5 temas centrales a tu negocio?" | Sin defecto — debe proporcionarse |
| **Audiencia objetivo** | "¿A quién intentas atraer?" | Clientes potenciales |
| **Dominio del sitio web** | "¿Cuál es tu URL de sitio web?" | Sin sitio existente |
| **Autoridad de dominio** | "¿Conoces tu Domain Authority o Rating?" | Baja (sitio nuevo o pequeño) |
| **Contenido existente** | "¿Cuántas páginas/posts actualmente tienes?" | Menos de 20 |

**PUNTO DE CONTROL: Confirma el briefing antes de comenzar la investigación.**

---

## Fase 2: Descubrimiento de Palabras Clave

### Proceso de Investigación

Para cada tema semilla, genera palabras clave en estas categorías:

**1. Términos Head** (1-2 palabras, alto volumen, alta competencia)
- Ejemplo: "marketing por email"
- Uso: Contenido de conciencia, páginas pilar

**2. Palabras Clave Body** (2-3 palabras, volumen moderado)
- Ejemplo: "estrategia de marketing por email"
- Uso: Páginas de categoría, guías exhaustivas

**3. Palabras Clave Long-Tail** (4+ palabras, volumen bajo, competencia baja)
- Ejemplo: "estrategia de marketing por email para solopreneurs"
- Uso: Artículos de blog, guías específicas — mayor intención de conversión

**4. Palabras Clave de Pregunta** (cómo, qué, por qué, cuándo consultas)
- Ejemplo: "cómo empezar con marketing por email"
- Uso: Páginas de FAQ, guías cómo hacerlo, objetivos de fragmento destacado

**5. Palabras Clave de Intención Comercial** (búsquedas listas para comprar)
- Ejemplo: "mejor herramienta de marketing por email para pequeño negocio"
- Uso: Publicaciones de comparación, contenido de reseña, páginas de destino

### Matriz de Evaluación de Palabras Clave

Para cada palabra clave, evalúa:

```
| Palabra Clave | Vol. Estimado | Dificultad | Intención | Prioridad |
|---------|------------|------------|--------|----------|
| [palabra clave] | [rango] | Bajo/Medio/Alto | Info/Comercial/Transaccional | 1-5 |
```

**Estimaciones de volumen:** Proporciona rangos (p. ej., 100-500/mes) basados en conocimiento de nicho y características de palabras clave.

**Factores de evaluación de dificultad:**
- Resultados actuales de top 10: ¿grandes marcas o pequeños sitios?
- Calidad de contenido de páginas con ranking: ¿puedes hacerlo mejor?
- Autoridad de dominio de sitios con ranking vs. la tuya
- Características de SERP presentes (fragmentos destacados, People Also Ask)

---

## Fase 3: Mapeo de Palabras Clave

### Mapeo de Contenido

Asigna cada palabra clave de prioridad a un tipo de contenido:

```
## Mapa Palabra Clave → Contenido

| Palabra Clave | Tipo de Contenido | Intención de Búsqueda | Página Objetivo |
|---------|-------------|---------------|-------------|
| [palabra clave] | Página pilar | Informacional | /guia/[tema] |
| [palabra clave] | Artículo de blog | Informacional | /blog/[slug] |
| [palabra clave] | Página de destino | Comercial | /[servicio] |
| [palabra clave] | Publicación de comparación | Comercial | /blog/mejor-[tema] |
```

### Clasificación de Prioridad

Clasifica palabras clave por una combinación de:
1. **Relevancia para tu negocio** (¿este tráfico convertirá?)
2. **Rankabilidad** (¿puedes realísticamente llegar a página 1?)
3. **Volumen de búsqueda** (¿hay suficiente tráfico para importar?)
4. **Brecha de contenido** (¿ya existe buen contenido en tu sitio?)

### Palabras Clave de Victoria Rápida

Identifica 5-10 palabras clave donde tienes la mejor oportunidad de rankear rápidamente:
- Baja competencia (pocos resultados de calidad actualmente)
- Intención de búsqueda clara que puedas combinar
- Long-tail con intención comercial o transaccional
- Relacionada a contenido que ya has comenzado

---

## Fase 4: Pulir

### 1. Reporte de Investigación de Palabras Clave

Entrega un output completo en estilo de hoja de cálculo:
- 30-50 palabras clave totales, organizadas por cluster de tema
- Estimaciones de volumen, dificultad, intención y prioridad para cada una
- Top 10 palabras clave "comenzar aquí" destacadas

### 2. Recomendaciones de Calendario de Contenido

Sugiere un plan de contenido de 3 meses basado en prioridades de palabras clave:
- Mes 1: Palabras clave de victoria rápida (long-tail, baja competencia)
- Mes 2: Palabras clave body con guías exhaustivas
- Mes 3: Comienza contenido pilar dirigido a términos head

### 3. Configuración de Rastreo

Recomienda rastrear las palabras clave objetivo:
- Gratis: Google Search Console para datos de impresión y clics
- Pagado: Ahrefs, SEMrush, o similar para rastreo de ranking
- Revisa rankings mensualmente durante los primeros 6 meses

---

## Anti-Patrones

- **Apuntar solo a palabras clave de alto volumen** — un sitio nuevo no puede rankear para "marketing por email". Comienza con palabras clave long-tail y construye autoridad.
- **Ignorar intención de búsqueda** — rankear para "marketing por email" con un artículo de blog cuando Google muestra herramientas y plataformas significa que estás apuntando al tipo de contenido incorrecto.
- **Keyword stuffing basado en investigación** — la investigación identifica objetivos; no significa forzar palabras clave en contenido.
- **Una palabra clave por página solo** — cada página debe dirigirse a una palabra clave primaria y 3-5 palabras clave secundarias relacionadas naturalmente.
- **Nunca revisar la investigación** — los paisajes de palabras clave cambian. Actualiza la investigación cada 6 meses.

---

## Recuperación

- **Sin temas semilla:** Pregunta "¿Qué preguntas hacen tus clientes antes de comprar?" y "¿Por qué buscaría tu cliente ideal?" para generar semillas.
- **Nicho muy competitivo:** Enfócate exclusivamente en palabras clave long-tail con 4+ palabras. Construye autoridad temática antes de apuntar a términos competitivos.
- **Sin sitio web aún:** Construye el mapa de palabras clave primero, luego úsalo para planificar la arquitectura del sitio y el contenido inicial.
- **El usuario quiere volúmenes de búsqueda exactos:** Explica que sin herramientas pagadas, los volúmenes son estimaciones. La prioridad relativa importa más que números exactos para la estrategia.
