---
name: optimizador-fragmento-destacado
description: Optimiza contenido para ganar fragmentos destacados con análisis de formato, estructura de respuesta y formato. Usa cuando estés apuntando a posición cero en resultados de búsqueda de Google.
allowed-tools: Read Write Glob
author: Imperio Digital
version: "1.0"
---

# Optimizador de Fragmento Destacado

## Cuándo Usar Este Skill

Usa este skill cuando necesites:
- Optimizar contenido existente para ganar fragmentos destacados (posición cero)
- Analizar qué formato de fragmento prefiere Google para una consulta objetivo
- Estructurar respuestas en formato de párrafo, lista o tabla para extracción de fragmento
- Identificar oportunidades de fragmento destacado en tu contenido

**NO** uses este skill para escritura general de contenido SEO, optimización de meta tags o link building. Esto es específicamente para formatear contenido para capturar fragmentos destacados.

---

## Principio Fundamental

LOS FRAGMENTOS DESTACADOS RESPONDEN LA PREGUNTA DIRECTAMENTE, CONCISAMENTE Y EN EL FORMATO QUE GOOGLE PREFIERE — ESTRUCTURA TU CONTENIDO PARA SER LA RESPUESTA MÁS FÁCIL PARA QUE GOOGLE EXTRAIGA.

---

## Fase 1: Briefing

### Información Requerida

| Input | Qué Preguntar | Por Defecto |
|-------|------------|---------|
| **Consultas objetivo** | "¿Para qué preguntas quieres ganar fragmentos?" | Sin defecto — debe proporcionarse |
| **Contenido existente** | "¿Tienes contenido publicado dirigido a estas consultas?" | Sí — URL(s) proporcionado(s) |
| **Ranking actual** | "¿Dónde actualmente rankeas para estas consultas?" | Página 1 o 2 |
| **Tipo de contenido** | "¿Qué formato es tu contenido? (blog, FAQ, guía)" | Artículo de blog |

**PUNTO DE CONTROL: Confirma las consultas objetivo antes de analizar oportunidades de fragmento.**

---

## Fase 2: Análisis de Fragmento

### Evaluación Actual de SERP

Para cada consulta objetivo, documenta:

```
## Análisis de Oportunidad de Fragmento

**Consulta:** [Pregunta objetivo]
**Poseedor actual de fragmento:** [URL / "Sin fragmento actualmente"]
**Formato de fragmento:** Párrafo / Lista numerada / Lista con viñetas / Tabla
**Tu posición actual:** [X]

**Elegibilidad de fragmento:** Alta / Media / Baja
- Alta: Rankeas en página 1 y la consulta tiene un formato de respuesta claro
- Media: Rankeas en página 1-2, existe fragmento pero es débil
- Baja: No rankeas en top 20 o la consulta rara vez dispara fragmentos
```

### Patrones de Formato de Fragmento

```
## Guía de Selección de Formato

**Fragmentos de párrafo** (40-50 palabras) funcionan mejor para:
- Preguntas "Qué es..." definiciones
- Preguntas "Por qué..." explicaciones
- Preguntas factuales de respuesta única

**Fragmentos de lista numerada** funcionan mejor para:
- Procesos paso a paso "Cómo..."
- Procedimientos "Pasos para..."
- Listas clasificadas

**Fragmentos de lista con viñetas** funcionan mejor para:
- "Tipos de..." o "Ejemplos de..."
- Listas de consejos, características o elementos
- Colecciones sin clasificar

**Fragmentos de tabla** funcionan mejor para:
- Comparaciones (X vs Y)
- Datos de precios o especificaciones
- Horarios o datos estructurados
```

**PUNTO DE CONTROL: Presenta el análisis y confirma qué consultas optimizar.**

---

## Fase 3: Optimizar Contenido

### Optimización de Fragmento de Párrafo

```
## Estructura para Fragmentos de Párrafo

**Paso 1:** Usa la consulta exacta como encabezado H2 o H3
Ejemplo: "## ¿Qué es Marketing por Email?"

**Paso 2:** Inmediatamente debajo del encabezado, responde en 40-50 palabras
Ejemplo: "Marketing por email es la práctica de enviar mensajes dirigidos a una lista de suscriptores para construir relaciones, promocionar productos e impulsar conversiones. Sigue siendo uno de los canales de marketing con mayor ROI, generando un retorno promedio de $36 por cada $1 gastado."

**Paso 3:** Sigue con explicación expandida, ejemplos y profundidad
```

### Optimización de Fragmento de Lista

```
## Estructura para Fragmentos de Lista

**Paso 1:** Usa la consulta como encabezado
Ejemplo: "## Cómo Configurar una Lista de Email"

**Paso 2:** Sigue inmediatamente con una lista numerada o con viñetas
Ejemplo:
1. Elige un proveedor de servicio de email
2. Crea un formulario de registro
3. Añade el formulario a tu sitio web
4. Configura un email de bienvenida
5. Impulsa tráfico al formulario de registro

**Paso 3:** Expande cada elemento debajo de la lista con 2-3 oraciones de detalle
```

### Optimización de Fragmento de Tabla

```
## Estructura para Fragmentos de Tabla

**Paso 1:** Usa un encabezado de comparación
Ejemplo: "## Plataformas de Marketing por Email Comparadas"

**Paso 2:** Crea una tabla limpia HTML/Markdown
| Plataforma | Precio | Mejor Para |
|----------|-------|----------|
| ConvertKit | $29/mes | Creadores |
| Mailchimp | $13/mes | Pequeño negocio |

**Paso 3:** Añade párrafos de contexto encima o debajo de la tabla
```

### Recomendaciones de Reestructuración de Contenido

Para cada consulta objetivo, proporciona:
1. Encabezado exacto a usar
2. Texto de respuesta optimizado (listo para fragmento)
3. Dónde colocarlo en el contenido existente
4. Contenido de apoyo adicional a añadir

---

## Fase 4: Pulir

### 1. Lista de Verificación de Implementación

- [ ] Consulta usada como encabezado H2/H3 exacto
- [ ] La respuesta sigue inmediatamente al encabezado (sin preámbulo)
- [ ] La respuesta tiene la longitud correcta (40-50 palabras para párrafo, 5-8 elementos para lista)
- [ ] La respuesta es factualmente precisa y autosuficiente
- [ ] El contenido de apoyo proporciona profundidad más allá del fragmento
- [ ] Contenido publicado y enviado para reindexación

### 2. Oportunidades de "People Also Ask"

Lista preguntas PAA relacionadas que aparecen para cada consulta objetivo — estas son oportunidades de fragmento adicionales dentro del mismo contenido.

### 3. Monitoreo

- Rastrea la propiedad de fragmentos semanalmente para consultas objetivo
- Si se pierde el fragmento, verifica: ¿bajó el ranking? ¿Google cambió la preferencia de formato? ¿Un competidor optimizó mejor?
- Los fragmentos destacados pueden cambiar frecuentemente — la calidad de contenido continuada es la mejor defensa

---

## Anti-Patrones

- **Apuntar a fragmentos para los que no rankeas** — generalmente necesitas rankear en el top 10 para ser considerado para un fragmento. Rankings primero, fragmentos segundo.
- **Sobre-optimizar la respuesta** — llenar la respuesta del fragmento con keywords de forma no natural hace que suene robótica y sea menos probable que sea seleccionada.
- **Formato incorrecto** — proporcionar una respuesta de párrafo cuando Google quiere una lista desperdicia el esfuerzo de optimización.
- **Demasiado largo o demasiado corto** — fragmentos de párrafo sobre 60 palabras se truncan. Listas sobre 8 elementos obtienen "Más elementos..." lo que puede funcionar pero es menos limpio.
- **Sin contenido de apoyo** — una página con solo una respuesta de longitud de fragmento es contenido delgado. El fragmento es el hook; la página debe entregar profundidad.

---

## Recuperación

- **No rankeas en página 1:** Enfócate en mejorar rankings generales antes de optimización de fragmento. Necesitas estar en el top 10 primero.
- **El fragmento sigue yendo a un competidor:** Analiza su formato y estructura. Iguala o supera la calidad de respuesta del fragmento, y asegúrate de que tu página tenga profundidad superior.
- **Google dejó de mostrar un fragmento para la consulta:** Algunas consultas pierden su fragmento con el tiempo. Cambia el enfoque a otras oportunidades de fragmento.
- **Múltiples páginas compitiendo por el mismo fragmento:** Consolida contenido en una página autoritaria para evitar canibalización.
