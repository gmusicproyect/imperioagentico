---
name: calendario-contenido
description: "Genera un calendario de contenido de 30 días como una base de datos de Notion con publicaciones asignadas a pilares de contenido, plataformas y fechas, más plantillas gráficas de inicio en Canva para cada pilar de contenido. Usa cuando un usuario necesite planificar su contenido del mes, quiera un cronograma de publicación estructurado o necesite crear contenido por lotes en múltiples plataformas."
allowed-tools: Read Write Glob
metadata:
  author: Imperio Digital
  version: "1.0"
---

# Calendario de Contenido

## Cuándo Usar Esta Skill

Usa esta skill cuando el usuario necesite:
- Planificar 30 días de contenido en una o más plataformas
- Construir un cronograma de publicación estructurado asignado a pilares de contenido y tipos de publicación
- Crear una base de datos de Notion para rastrear el estado del contenido desde idea hasta publicado
- Generar plantillas gráficas de inicio en Canva para cada pilar de contenido
- Planificar contenido por lotes para Instagram, LinkedIn, X/Twitter, YouTube, TikTok, newsletter o podcast

**NO USES** esta skill para:
- Escribir publicaciones de blog de forma larga o artículos (usa una skill de escritura de contenido)
- Crear gráficos de redes sociales individuales bajo demanda (usa social-media-graphics)
- Gestionar un calendario de contenido existente que ya vive en Notion (el usuario debe editarlo directamente)
- Creación de publicación única sin plan mensual más amplio

---

## Marco de Pilar de Contenido

Cada calendario se construye sobre 3-5 pilares de contenido. Los pilares previenen publicación aleatoria y hacen posible la creación por lotes.

| Tipo de Pilar | Propósito | Ejemplo (Coach de Fitness) | Ejemplo (Fundador SaaS) |
|-------------|---------|------------------------|----------------------|
| **Educación** | Enseña a tu audiencia algo accionable | "3 ejercicios para trabajadores de escritorio" | "Cómo reducir la rotación con correos de incorporación" |
| **Autoridad** | Muestra experiencia, resultados, credenciales | "Transformación de cliente: 12 semanas" | "Alcanzamos $50K MRR — aquí está lo que funcionó" |
| **Conexión** | Construye confianza a través de personalidad e historia | "Por qué me convertí en entrenador después del agotamiento" | "El peor error que envié y qué me enseñó" |
| **Promoción** | Impulsa ventas, registros o conversiones | "Se abren espacios para coaching 1:1" | "Prueba nuestro plan gratuito — sin tarjeta de crédito" |
| **Comunidad** | Involucra a la audiencia | "¿Cuál es tu mayor lucha en el gimnasio?" | "Poll: ¿Qué característica deberíamos construir después?" |

**PREDETERMINADO: 4 pilares** — Educación, Autoridad, Conexión, Promoción. Añade Comunidad solo si la estrategia del usuario depende de engagement de audiencia.

---

## Frecuencias de Publicación Comunes

| Cronograma | Publicaciones/Semana | Mejor Para | Total Mensual |
|----------|-----------|----------|---------------|
| Ligero | 3 | Emprendedores individuales con tiempo limitado, B2B solo LinkedIn | 12-13 |
| Estándar | 5 | Mayoría de creadores, coaches, consultantes | 21-22 |
| Activo | 7 | Creadores de tiempo completo, cuentas de marca | 30 |
| Agresivo | 10-14 | Creadores multi-plataforma, agencias | 42-60 |

**PREDETERMINADO: 5 publicaciones/semana (Estándar)** — cubre días laborales, deja fines de semana libres para crear por lotes.

---

## Workflow Principal

TODO CALENDARIO COMIENZA CON PILARES DE CONTENIDO — NUNCA GENERES IDEAS DE PUBLICACIÓN SIN ESTABLECER PILARES PRIMERO.

### Paso 1: Entender

Recopila estas entradas del usuario antes de generar algo:

1. **Negocio/nicho** — qué hacen y a quién sirven
2. **Pilares de contenido** — sus 3-5 temas principales (ofrece la tabla del marco si no están seguros)
3. **Plataformas objetivo** — en cuáles publican
4. **Frecuencia de publicación** — cuántas publicaciones por semana (ofrece tabla de frecuencia si no está seguro)
5. **Audiencia** — a quién intentan llegar (demografía, pain points, objetivos)
6. **Eventos próximos** — lanzamientos de producto, ventas, vacaciones o hitos en los próximos 30 días
7. **Voz de marca** — descriptores de tono (profesional, casual, ingenioso, motivacional, directo)

**Si el usuario proporciona artículos 1-3, procede con predeterminados para artículos 4-7.** Solo pregunta sobre detalles críticos faltantes.

**PUNTO DE CONTROL: No proceedas al Paso 2 hasta que tengas al mínimo: negocio/nicho, plataformas y pilares de contenido proporcionados por el usuario o asignados por defecto.**

---

### Paso 2: Generar

Construye 30 días de ideas de contenido asignadas a pilares, plataformas, tipos de publicación y fechas.

1. **Asigna distribución de pilares** en la frecuencia de publicación:

   Para 5 publicaciones/semana con 4 pilares, la división predeterminada es:
   - Educación: 2x/semana (40%)
   - Autoridad: 1x/semana (20%)
   - Conexión: 1x/semana (20%)
   - Promoción: 1x/semana (20%)

   Educación siempre obtiene la mayor parte. Promoción nunca excedera 25%.

2. **Asigna tipos de publicación a plataformas** — asigna tipos que coincidan con las fortalezas de cada plataforma
3. **Genera 30 días de ideas de publicación** con estos campos:
   - Fecha (Día 1 a Día 30)
   - Plataforma
   - Pilar de Contenido
   - Tipo de Publicación
   - Idea de Epígrafe
   - Estado (predeterminado: "Idea")

---

### Paso 3: Presentar

Muestra el calendario completo al usuario para aprobación antes de crear algo en Notion o Canva.

Presenta una tabla de resumen mostrando los primeros 7 días en detalle y pide aprobación para proceder.

**PUNTO DE CONTROL: No proceedas al Paso 4 hasta que el usuario apruebe la dirección del calendario.**

---

### Paso 4: Actuar

Crea la base de datos de Notion y plantillas de inicio de Canva.

#### 4A: Crear la Base de Datos de Notion

1. **Busca contexto de espacio de trabajo existente** — verifica si el usuario tiene una página o base de datos relacionada con contenido
2. **Crea la base de datos** con estas propiedades:
   - Título de Publicación (Título)
   - Fecha (Fecha)
   - Plataforma (Seleccionar)
   - Pilar (Seleccionar)
   - Tipo de Publicación (Seleccionar)
   - Estado (Seleccionar: Idea, Borrador, Listo, Programado, Publicado)
   - Enlace de Canva (URL)
   - Notas (Texto enriquecido)

3. **Llena la base de datos** agregando todos los 30 días de contenido como entradas individuales
4. **Confirma la base de datos** mostrando al usuario el enlace y detalles

#### 4B: Crear Plantillas de Inicio de Canva

Genera una plantilla gráfica de inicio por pilar de contenido.

1. **Verifica marca kit** — carga colores, fuentes y logo de marca del usuario
2. **Crea una carpeta de Canva** con el nombre: `Calendario de Contenido — [Mes Año]`
3. **Genera una plantilla por pilar** con direcciones de prompt personalizadas:
   - Educación: Diseño limpio con formato de lista numerada o tips
   - Autoridad: Titular audaz con espacio para métrica o cita de testimonial
   - Conexión: Diseño casual estilo historia con espacio para foto personal
   - Promoción: Diseño enfocado en CTA con elemento de urgencia
   - Comunidad: Diseño centrado en pregunta con espacio de respuesta

4. **Obtén miniaturas para cada plantilla**
5. **Mueve todas las plantillas a la carpeta**
6. **Entrega el paquete completo**

---

## Ejemplo 1: Coach de Fitness — Instagram + LinkedIn, 5 Publicaciones/Semana

**Usuario dice:** "Soy coach de fitness especializado en entrenamiento de fuerza para profesionales ocupados. Publico en Instagram y LinkedIn. Quiero 5 publicaciones por semana. Tengo un desafío de 6 semanas que comienza el 15."

**Paso 1 — Entender:**
- Negocio: Coaching de fitness, entrenamiento de fuerza para profesionales ocupados
- Pilares: Educación (tips de entrenamiento), Autoridad (resultados de clientes), Conexión (historia personal), Promoción (ofertas de coaching)
- Plataformas: Instagram, LinkedIn
- Frecuencia: 5/semana
- Audiencia: Profesionales 28-45 con tiempo de gimnasio limitado
- Evento próximo: Lanzamiento de desafío de 6 semanas el 15
- Voz: Motivacional, directo, sin relleno

**Paso 2 — Generar (muestra semana 1):**

| Día | Plataforma | Pilar | Tipo de Publicación | Idea de Epígrafe |
|-----|----------|--------|-----------|--------------|
| Lun | Instagram | Educación | Carrusel | 5 ejercicios compuestos que reemplazan una sesión de 60 min |
| Mar | LinkedIn | Autoridad | Publicación de texto | Mi cliente perdió 4% de grasa corporal en 8 semanas |
| Mié | Instagram | Conexión | Video corto | Cómo se ve realmente mi rutina de 5 AM |
| Jue | LinkedIn | Educación | Carrusel | La dosis efectiva mínima para fuerza |
| Vie | Instagram | Promoción | Imagen | Desafío de 6 semanas comienza el 15 — 12 espacios quedan |

---

## Anti-Patrones

- **NO** generes ideas de publicación sin establecer pilares de contenido primero
- **NO** programes más de 25% contenido promocional — la audiencia se desactiva
- **NO** asignes el mismo tipo de publicación a la misma plataforma 3+ días seguidos
- **NO** crees plantillas de Canva antes de que el usuario apruebe el calendario
- **NO** dejes la propiedad Enlace de Canva vacía sin decir al usuario cómo llenarla
- **NO** asumas días de publicación — pregunta al usuario o usa predeterminado de días laborales

---

## Recuperación y Solución de Problemas

- **Falla creación de base de datos Notion:** Fallback es generar el calendario de 30 días como tabla markdown para importación manual
- **Falla generación parcial de página de Notion:** Anota qué entradas se crearon exitosamente y reintenta las fallidas
- **Falla generación de diseño de Canva:** Simplifica el prompt, reintenta. Si falla de nuevo, proporciona especificaciones de plantilla al usuario
- **No hay marca kit en Canva:** Pregunta por colores primarios (hex), secundarios y preferencia de fuente
- **Usuario sin pilares de contenido:** Presenta tabla del Marco de Pilar de Contenido y recomienda los 4 predeterminados
