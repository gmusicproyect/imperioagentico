---
name: auditoria-seo
description: Realiza análisis de SEO en la página con title tags, meta descripciones, estructura de encabezados, brechas de palabras clave y recomendaciones técnicas. Usa cuando un usuario quiera mejorar rankings de búsqueda, lanza un nuevo sitio o necesita diagnosticar por qué sus páginas no rankean.
allowed-tools: Read Write Glob
author: Imperio Digital
version: "1.0"
---

# Auditoría de SEO

## Cuándo Usar Este Skill

Usa este skill cuando:
- Las páginas del sitio web no rankean para palabras clave objetivo
- Estés lanzando un nuevo sitio web y quieras comenzar con SEO sólido
- Estés rediseñando un sitio y necesites preservar/mejorar SEO
- No hayas revisado SEO en 6+ meses
- Un competidor te está superando y quieres saber por qué

## Principio Fundamental

**EL SEO SE TRATA DE COINCIDIR CON INTENCIÓN DE BÚSQUEDA, NO DE RELLENAR PALABRAS CLAVE. Google recompensa páginas que mejor responden la pregunta del buscador.**

---

## Workflow

### Paso 1: Recopilar Inputs

Pregunta al usuario:
1. ¿Cuál es la URL o contenido de página a auditar?
2. ¿Para qué palabras clave quieres rankear? (1-3 palabras clave primarias)
3. ¿Cuál es tu audiencia objetivo?
4. ¿Quiénes son tus top 2 competidores?

**Mínimo necesario: pregunta 1. Si no se proporcionan palabras clave, infiere del contenido de página.**

### Paso 2: Auditoría de SEO En-Página

Analiza cada elemento y califica como PASAR, NECESITA TRABAJO o FALLAR:

| Elemento | Qué Verificar | Mejor Práctica |
|---------|--------------|---------------|
| Title Tag | Longitud, ubicación de palabra clave, unicidad | 50-60 caracteres, palabra clave primaria cerca del frente |
| Meta Description | Longitud, CTA, inclusión de palabra clave | 150-160 caracteres, incluye palabra clave + verbo de acción |
| H1 Tag | Existe, contiene palabra clave, solo uno por página | Un H1 por página, incluye palabra clave primaria |
| Estructura de Encabezados | H2s y H3s usan jerarquía lógica | Palabras clave en H2s, sin niveles saltados |
| Estructura de URL | Corta, descriptiva, incluye palabra clave | /palabra-clave-primaria, sin fechas o IDs |
| Enlaces Internos | Enlaza a/desde otras páginas relevantes | 3-5 enlaces internos por 1,000 palabras |
| Alt Text de Imagen | Descriptivo, incluye palabras clave donde es natural | Cada imagen tiene alt text |
| Longitud de Contenido | Suficiente para profundidad de tema | Iguala o supera la longitud de competidores que rankean |
| Densidad de Palabra Clave | Uso natural, no relleno | 1-2% para palabra clave primaria |
| Compatibilidad Móvil | Responsive, legible sin zoom | Todo contenido accesible en móvil |

### Paso 3: Análisis de Brecha de Contenido

Compara la página contra competidores que rankean en el top:
1. ¿Qué subtemas cubren competidores que esta página no?
2. ¿Qué preguntas responden competidores que esta página salta?
3. ¿Qué formatos de contenido usan competidores (tablas, listas, videos)?

### Paso 4: Entregar Recomendaciones

Prioriza arreglos por impacto:

**Crítico (hacer primero):**
- Title tags faltantes o duplicados
- Sin H1 o múltiples H1s
- Meta descripción faltante
- Contenido delgado (bajo 300 palabras para un tema que necesita profundidad)

**Alto Impacto:**
- Palabra clave no en title tag o H1
- Sin enlaces internos
- Alt text de imagen faltante
- URL contiene parámetros innecesarios

**Impacto Medio:**
- Meta descripción demasiado larga/corta
- Problemas de jerarquía de encabezados
- Brechas de contenido vs. competidores

**Impacto Bajo (agradable tener):**
- Schema markup faltante
- Tags Open Graph incompletos
- Ajustes menores de densidad de palabra clave

---

## Ejemplo: Página de Homepage de Negocio de Coaching

**Análisis de contenido de URL:**

```
RESULTADOS DE AUDITORÍA — www.sarahcoaching.com

Title Tag: "Sarah Johnson — Life Coach"
→ NECESITA TRABAJO — Falta palabra clave primaria "executive coaching."
  Recomendado: "Executive Coaching for Women Leaders | Sarah Johnson"

Meta Description: (ninguno encontrado)
→ FALLAR — Sin meta descripción. Google auto-generará una.
  Recomendado: "Transform your leadership with 1-on-1 executive coaching
  for women in corporate roles. Book a free discovery call with Sarah Johnson."

H1: "Welcome to My Website"
→ FALLAR — Genérico, sin palabras clave.
  Recomendado: "Executive Coaching for Women Who Lead"

Estructura de Encabezados:
  H2: "About Me" → NECESITA TRABAJO — Debería ser "About Your Executive Coach"
  H2: "Services" → PASAR
  H2: "Testimonials" → PASAR
  H3: (ninguno) → NECESITA TRABAJO — Añade H3s bajo Services para cada oferta

URL: www.sarahcoaching.com → PASAR (homepage)

Enlaces Internos: 0 enlaces a blog o páginas de servicio
→ FALLAR — Añade enlaces a páginas de servicio, publicaciones de blog y página de reserva

Longitud de Contenido: 247 palabras
→ FALLAR — Homepage debería tener mínimo 500-800 palabras para negocio de servicios

CORRECCIONES DE PRIORIDAD:
1. Añade meta descripción (arreglo de 5 minutos, impacto inmediato)
2. Reescribe H1 con palabra clave primaria (arreglo de 5 minutos)
3. Reescribe title tag (arreglo de 5 minutos)
4. Añade 300+ palabras de contenido sobre servicios y resultados
5. Añade enlaces internos a páginas de servicio y blog
```

---

## Recuperación y Fallbacks

- **Usuario no puede compartir su URL:** Pídele que pegue el source HTML de página o solo el contenido visible. Audita lo que puedas ver.
- **Usuario tiene cientos de páginas:** Comienza con las 5 páginas con mayor tráfico o ingresos. Una auditoría 80/20 es mejor que una auditoría completa que nunca sucede.
- **Usuario no conoce palabras clave objetivo:** Sugiere 3-5 basadas en contenido de página y tipo de negocio. Déjale confirmar antes de auditar.
- **Se encontraron problemas de SEO técnico:** Señálalo pero aclara que SEO técnico (velocidad de sitio, rastreabilidad, redireccionamientos) requiere herramientas de desarrollador. Esta auditoría se enfoca en SEO de contenido en-página.

---

## Restricciones

- **NUNCA garantices rankings o números de tráfico específicos** — los resultados de SEO dependen de muchos factores
- Enfócate en recomendaciones accionables y específicas — no consejo genérico
- Siempre prioriza arreglos por impacto (no abrumar con 50 elementos de baja prioridad)
- Distingue entre SEO en-página (esta auditoría) y SEO técnico (alcance diferente)
- Incluye el texto específico recomendado para title tags, meta descripciones y H1s — no solo digas "mejóralo"
