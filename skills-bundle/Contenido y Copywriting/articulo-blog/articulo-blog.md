---
name: articulo-blog
description: "Escribe artículos de blog optimizados para SEO de forma larga con aprobación de esquema, meta descripciones, sugerencias de enlaces internos, briefs de imagen destacada y una lista de verificación de SEO pre-publicación. Utiliza esta skill cuando un usuario necesita un artículo de blog para su sitio web, quiere ranking para palabras clave específicas o necesita piezas de marketing de contenido que impulsen tráfico orgánico."
allowed-tools: Read Write Glob
metadata:
  author: Imperio Digital
  version: "1.0"
---

# Artículo de Blog

## Cuándo Usar Este Skill

Usa esta skill cuando necesites:
- Escribir un artículo de blog de forma larga optimizado para rankings de motores de búsqueda
- Crear un artículo de marketing de contenido diseñado para impulsar tráfico orgánico
- Producir un listicle, guía cómo-hacer o pieza de liderazgo de pensamiento para un sitio web
- Generar un paquete completo de blog (esquema, post, meta descripción, brief de imagen, lista de verificación SEO)

**NO** uses esta skill para copias de redes sociales cortas, newsletters de email, copias de landing page o contenido que no vive en un blog. Esto es para artículos de blog de forma larga optimizados para SEO únicamente.

---

## Principio Fundamental

TODO ARTÍCULO DE BLOG DEBE RESPONDER UNA INTENCIÓN DE BÚSQUEDA ESPECÍFICA MEJOR QUE CUALQUIER COSA ACTUALMENTE EN LA PÁGINA UNO -- ESCRIBIENDO PARA HUMANOS PRIMERO Y MOTORES DE BÚSQUEDA SEGUNDO.

---

## Fase 1: Brief

Antes de escribir cualquier cosa, recopila los cinco inputs que dan forma al post completo. Sin brief, sin esquema.

### Inputs Requeridos

Pregunta al usuario por cada uno de estos. Si no proporcionan uno, usa el predeterminado.

| Input | Qué Preguntar | Predeterminado |
|-------|------------|---------|
| **Palabra clave objetivo** | "¿Para qué palabra clave o frase debería este post tener ranking?" | Sin predeterminado -- debe ser proporcionado |
| **Audiencia** | "¿Quién está leyendo esto? Rol, nivel de experiencia, qué les importa." | Emprendedores y dueños de pequeños negocios |
| **Ángulo / perspectiva única** | "¿Qué hace tu toma sobre esto diferente? ¿Una experiencia personal, datos propios, vista contraria?" | Perspectiva de practicante de primera mano |
| **Objetivo de cantidad de palabras** | "¿Cuán largo debería ser este post?" | 1,500-2,000 palabras |
| **Enlaces internos** | "Comparte URLs o títulos de posts existentes en tu sitio que debería enlazar." | Ninguno -- salta enlaces internos si no se proporciona |

### Plantilla de Brief

Presenta esto al usuario antes de pasar a Fase 2:

```
## Brief de Artículo de Blog

**Palabra clave objetivo:** sistema de repurposing de contenido
**Palabras clave secundarias:** repurposar contenido, workflow de repurposing, repurposar posts de blog
**Intención de búsqueda:** How-to (lector quiere un sistema paso a paso que pueda implementar)
**Audiencia:** Creadores de contenido solo publicando 1-2 veces por semana que quieren más alcance sin más escritura
**Ángulo:** Autor construyó un sistema que convierte un post de blog en 8 piezas en 4 plataformas en menos de 2 horas
**Cantidad de palabras:** 2,000 palabras
**Enlaces internos a incluir:**
- /blog/guia-programacion-redes-sociales
- /blog/consejos-newsletter-email
```

**PUNTO DE CONTROL:** No procede a Fase 2 hasta que usuario confirme o ajuste el brief.

---

## Fase 2: Esquema

Construye una estructura de heading completa con puntos clave bajo cada sección. El esquema ES el blueprint -- todo en Fase 3 lo sigue exactamente.

### Reglas de Esquema

1. **H1** contiene la palabra clave objetivo, escrito para humanos (no keyword-stuffed)
2. **H2s** cubren las secciones mayores -- apunta para 4-7 H2s dependiendo de cantidad de palabras
3. **H3s** desglosan secciones H2 complejas -- usa solo cuando una sección cubre 2+ sub-tópicos distintos
4. **Puntos clave** bajo cada heading -- 2-4 bullet points describiendo qué cubrirá esa sección
5. **Cantidad de palabras estimada** próximo a cada H2 para que usuario vea balance en secciones

### Formato de Esquema

Usa esta estructura para todo esquema:

```
**H1:** [Título con palabra clave objetivo]

**H2: [Título de Sección]** (~[cantidad de palabras] palabras)
- [Punto clave 1]
- [Punto clave 2]
- [Punto clave 3]

**H2: [Título de Sección]** (~[cantidad de palabras] palabras)
  **H3: [Sub-tópico]**
  - [Punto clave]
  **H3: [Sub-tópico]**
  - [Punto clave]
```

Ver Ejemplo 1 y Ejemplo 2 abajo para ejemplos de esquema completo.

**PUNTO DE CONTROL:** Presenta el esquema y espera aprobación del usuario. No escribas el post completo hasta que usuario diga que el esquema es bueno. Si usuario solicita cambios, revisa el esquema y preséntalo de nuevo.

---

## Fase 3: Escribe

Con un esquema aprobado, escribe el post completo. Sigue estas reglas SEO y estructurales para cada sección.

### Estructura del Post

Todo post de blog sigue esta arquitectura:

**1. Hook de Intro (primeras 100-150 palabras)**
- Abre con un pain point específico, estadística sorprendente o afirmación audaz -- no "En el mundo digital actual..."
- Establece qué el lector aprenderá y por qué importa para ellos
- Incluye la palabra clave objetivo naturalmente dentro de las primeras 100 palabras
- Termina la intro con una transición a la primera sección de cuerpo

**2. Secciones de Cuerpo (mayor parte de cantidad de palabras)**
- Sigue el esquema aprobado heading por heading
- Usa párrafos cortos (máximo 2-4 oraciones)
- Incluye al menos uno por sección H2: un ejemplo concreto, un punto de datos, una cita directa o una instrucción paso a paso
- Usa listas de bullets y listas numeradas para romper paredes de texto
- Coloca enlaces internos donde agregan valor genuino (no forzado)

**3. Conclusión + CTA (final 100-150 palabras)**
- Resume el aprendizaje clave único en una oración
- Dile al lector qué hacer AHORA (no "considera" o "piensa en")
- CTA coincide con la meta del negocio: suscribirse, descargar, reservar llamada, probar el método, leer siguiente post

### Elementos SEO a Tejer

Mientras escribes, incrusta estos elementos naturalmente:

| Elemento | Regla |
|---------|------|
| **Palabra clave objetivo en H1** | Debe aparecer en H1 exactamente una vez |
| **Palabra clave en primeras 100 palabras** | Colócala naturalmente en párrafo de apertura |
| **Palabra clave en al menos 1 H2** | Úsala o una variante cercana en una subheading |
| **Densidad de palabra clave** | 0.5-1.5% del recuento total de palabras -- nunca la forces |
| **Palabras clave secundarias** | Esparce 2-3 términos relacionados durante el cuerpo |
| **Enlaces internos** | Coloca enlaces proporcionados por usuario donde son relevantes contextualmente, usando texto de anclaje descriptivo (no "haz clic aquí") |
| **Sugerencias de alt text** | Para cualquier referencia de imagen, incluye alt text sugerido en brackets: [Alt: descripción incluyendo palabra clave si es natural] |

### Meta Descripción

Escribe una meta descripción inmediatamente después del cuerpo del post:

- **Duración:** 150-160 caracteres (límite duro)
- **Estructura:** [Beneficio u hook] + [Lo que el post cubre] + [CTA implícita o explícita]
- **Incluye la palabra clave objetivo** naturalmente
- **Escribe para el clic** -- este es el ad copy que aparece en resultados de búsqueda

Ejemplo:
```
**Meta descripción (155 caracteres):** Aprende a construir un sistema de repurposing de contenido que convierte un post de blog en 8 piezas listas para plataforma. Marco paso a paso dentro.
```

### Colocaciones de Enlaces Internos

Si usuario proporcionó enlaces internos en Fase 1, muestra dónde cada uno fue colocado:

```
## Enlaces Internos Colocados

1. /blog/guia-programacion-redes-sociales -- enlazado en sección "Herramientas Que Hacen Repurposing Más Rápido", texto de anclaje: "guía de programación de redes sociales"
2. /blog/consejos-newsletter-email -- enlazado en H3 "Newsletter de Email", texto de anclaje: "escribir newsletters de email que conviertan"
```

Si usuario no proporcionó enlaces internos, sugiere 3-5 ideas de tópico para posts que podrían escribir e interenlazar con este artículo (ver Ejemplo 2 para una muestra).

---

## Fase 4: Pulir

Después que el post completo está escrito, entrega tres elementos finales.

### 1. Brief de Imagen Destacada

Proporciona un brief creativo para la imagen destacada del blog (para un diseñador o herramienta de imagen AI):

```
## Brief de Imagen Destacada

**Concepto:** [Descripción visual vinculada al tópico del post]
**Estilo:** Diseño flat minimalista, 2-3 colores de marca, fondo blanco
**Dimensiones:** 1200x630px (optimizado para compartición social y Open Graph)
**Overlay de texto (opcional):** [Título corto o ninguno]
**Alt text:** [Alt text descriptivo incluyendo palabra clave objetivo si es natural]
```

Ver Ejemplo 1 y Ejemplo 2 para briefs de imagen destacada completos.

### 2. Lista de Verificación de Pre-Publicación SEO

Presenta esta lista de verificación. Todo item debe pasar antes de que el post esté listo.

```
## Lista de Verificación de Pre-Publicación SEO

### Optimización de Palabras Clave
- [ ] Palabra clave objetivo aparece en H1
- [ ] Palabra clave objetivo aparece en primeras 100 palabras
- [ ] Palabra clave objetivo aparece en al menos un H2
- [ ] Densidad de palabra clave está entre 0.5% y 1.5%
- [ ] 2-3 palabras clave secundarias se usan naturalmente en el cuerpo
- [ ] Meta descripción incluye palabra clave objetivo

### Estructura y Legibilidad
- [ ] La jerarquía H1 > H2 > H3 es correcta (sin niveles saltados)
- [ ] Ningún H2 o H3 está huérfano (todo heading tiene contenido de cuerpo bajo)
- [ ] Párrafos son máximo 2-4 oraciones
- [ ] Al menos una lista (bullet o numerada) por 500 palabras
- [ ] Intro engancha al lector en primeras 2 oraciones (sin aperturas "En el mundo digital actual...")

### Meta y Técnico
- [ ] Meta descripción tiene 150-160 caracteres
- [ ] Meta descripción incluye un beneficio y CTA implícita
- [ ] Todas las imágenes tienen sugerencias de alt text
- [ ] Enlaces internos usan texto de anclaje descriptivo (no "haz clic aquí" o "leer más")
- [ ] Sin enlaces rotos o de placeholder

### Calidad de Contenido
- [ ] Toda afirmación está respaldada por un ejemplo específico, punto de datos o paso accionable
- [ ] El post responde la intención de búsqueda establecida en el brief
- [ ] La conclusión tiene un CTA claro y único
- [ ] Cantidad de palabras cumple objetivo del brief (+/- 10%)
```

### 3. Verificación de Legibilidad

Proporciona una breve evaluación cubriendo: nivel de lectura estimado (apunta a grado 8), duración promedio de oración, porcentaje de voz pasiva (apunta a bajo 5%), y si alguna sección única excede 600 palabras (recomienda dividir si así).

---

## Ejemplo 1: "Cómo Construir un Sistema de Repurposing de Contenido" (2,000 palabras)

**Brief:**
- Palabra clave objetivo: sistema de repurposing de contenido
- Audiencia: Creadores de contenido solo que publican semanalmente
- Ángulo: Sistema personal del autor que produce 8 piezas desde 1 post en menos de 2 horas
- Cantidad de palabras: 2,000
- Enlaces internos: /blog/guia-programacion-redes-sociales, /blog/consejos-newsletter-email

**Extracto de esquema:**

```
H1: Cómo Construir un Sistema de Repurposing de Contenido Que Te Ahorre 10 Horas a la Semana
H2: Por Qué La Mayoría del Contenido Muere Después de Un Post (~200 palabras)
H2: El Marco de Repurposing de 4 Pasos (~500 palabras)
H2: Desglose Plataforma por Plataforma (~600 palabras)
  H3: Threads de Twitter/X
  H3: Posts de LinkedIn
  H3: Newsletter de Email
  H3: Video de Forma Corta
H2: Herramientas Que Hacen Repurposing Más Rápido (~300 palabras)
H2: Errores Comunes Que Matan Tus Resultados de Repurposing (~200 palabras)
H2: Tu Primer Sprint de Repurposing -- Comienza Esta Semana (~200 palabras)
```

**Meta descripción:**
```
Aprende a construir un sistema de repurposing de contenido que convierte un post de blog en 8 piezas listas para plataforma. Marco paso a paso dentro.
```

**Brief de imagen destacada:**
```
Concepto: Icono de post de blog único ramificándose en 8 iconos de formato (thread, post, email, video, carousel, story, nota de podcast, infografía)
Estilo: Diseño flat minimalista, colores de marca en blanco
Dimensiones: 1200x630px
Alt text: Sistema de repurposing de contenido -- convierte un post de blog en 8 piezas de contenido
```

---

## Ejemplo 2: "5 Errores de Factura Que Cometen Freelancers" (listicle de 1,500 palabras)

**Brief:**
- Palabra clave objetivo: errores de factura de freelancers
- Audiencia: Freelancers y solopreneurs que envían facturas manualmente
- Ángulo: Errores reales que el autor cometió (o vio que clientes cometían) que cuestan dinero
- Cantidad de palabras: 1,500
- Enlaces internos: ninguno proporcionado

**Extracto de esquema:**

```
H1: 5 Errores de Factura Que Cometen Freelancers (Y Cómo Arreglar Cada Uno)
H2: Error 1 -- No Incluir Términos de Pago (~250 palabras)
H2: Error 2 -- Enviar Facturas Tarde (~250 palabras)
H2: Error 3 -- Usar Descripciones de Línea Vagas (~250 palabras)
H2: Error 4 -- Olvidar Cobrar por Revisiones (~250 palabras)
H2: Error 5 -- No Hacer Seguimiento en Facturas Vencidas (~250 palabras)
H2: La Auditoría de Factura de 60 Segundos (~150 palabras)
```

**Meta descripción:**
```
Evita estos 5 errores de factura que cuestan a freelancers miles en pagos atrasados y revenue perdido. Arregla cada uno con una plantilla simple.
```

**Brief de imagen destacada:**
```
Concepto: Documento de factura estilizado con 5 marcas rojo "X" tachadas, reemplazadas por checkmarks verdes -- representando errores siendo arreglados
Estilo: Ilustración de línea limpia, colores de énfasis rojo y verde en blanco
Dimensiones: 1200x630px
Alt text: 5 errores de factura de freelancers -- errores de facturación comunes y cómo arreglarlos
```

**Oportunidades de enlaces internos sugeridos:**
```
1. "Cómo Establecer Tus Tarifas de Freelancer" -- enlaza desde Error 3 (descripciones de línea vagas)
2. "Las Mejores Herramientas de Facturación para Solopreneurs" -- enlaza desde sección Auditoría de Factura
3. "Plantilla de Términos de Pago de Freelancer" -- enlaza desde Error 1 (términos de pago)
```

---

## Anti-Patrones

**NUNCA hagas estas cosas cuando escribas un post de blog:**

- **Keyword stuffing** -- forzar la palabra clave en cada párrafo o exceder densidad 1.5%. Los lectores notan y motores de búsqueda castigan.
- **Contenido delgado** -- entregando 500 palabras cuando prometiste 1,500. Cada sección necesita ejemplos, datos o pasos accionables.
- **Saltarse la puerta de esquema** -- escribir el post completo sin aprobación lleva a mayores reescrituras. Siempre obtén estructura aprobada primero.
- **Intros genéricos** -- "En el mundo digital actual..." desperdicia el bienes raíces más valioso del post. Engancha con específicos.
- **Párrafos de pared de texto** -- cualquier cosa sobre 4 oraciones obtiene skimmed. Divídelo.
- **Meta descripciones de clickbait** -- no prometas "secretos" o "hacks" que el post no entrega.
- **Texto de anclaje "haz clic aquí"** -- enlaces internos deben usar texto de anclaje descriptivo.
- **Headings huérfanos** -- un H2 o H3 sin contenido de cuerpo bajo daña señales de estructura.
- **CTAs múltiples en conclusión** -- un CTA, no tres.

---

## Recuperación

- **Sin palabra clave objetivo:** Pregunta qué pregunta su cliente ideal tipea en Google. Si aún no pueden identificar una, sugiere 3 ideas de palabras clave basadas en su negocio y elige una juntos.
- **Sin enlaces internos:** Salta enlaces internos. Proporciona 3-5 tópicos de posts sugeridos para construir un cluster de contenido alrededor de la palabra clave objetivo.
- **Esquema rechazado dos veces:** Pregunta qué específicamente se siente mal -- ángulo, profundidad, estructura o desajuste de audiencia. Aísla el issue antes de reescribir.
- **Cantidad de palabras bajo 800:** Advierte que posts bajo 800 palabras raramente tienen ranking. Recomienda mínimo 1,200. Si insisten, procede pero nota en evaluación de legibilidad.
- **Cantidad de palabras sobre 3,000:** Confirma que necesitan esa profundidad. Sugiere dividir en serie de 2 partes si esquema excede 7 secciones H2.
- **Palabra clave pero sin ángulo:** Sugiere 3 ángulos (experiencia personal, impulsado por datos, toma contraria). Predeterminado a perspectiva de practicante.
- **Si 3 revisiones de esquema fallan:** Detén y reevalúa. Pide al usuario que comparta un post de blog que admire para que puedas reverse-engineer estructura y tono.

---

## Entrega y Output de Archivo

Cuando el post está completo, presenta los entregables en este orden:

1. **Post de blog completo** (H1 a través de conclusión + CTA)
2. **Meta descripción**
3. **Colocaciones de enlaces internos** (u oportunidades sugeridas)
4. **Brief de imagen destacada**
5. **Lista de verificación de pre-publicación SEO** (con items checkeados/no checkeados)
6. **Evaluación de legibilidad**

Si usuario proporciona ruta de archivo o pide guardar, escribe el post completo a un archivo:

```
blog/
└── [slug-de-h1].md
```

Incluye la meta descripción, brief de imagen y lista de verificación como secciones en el fondo del archivo, separadas por divisores `---`.
