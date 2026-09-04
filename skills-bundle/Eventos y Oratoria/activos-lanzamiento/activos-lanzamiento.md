---
name: activos-lanzamiento
description: "Construye un paquete completo de lanzamiento de producto o servicio con una lista de verificación estructurada en Notion y activos visuales coordinados en Canva, incluyendo gráficos para redes sociales, imágenes de anuncio y encabezados de email. Úsalo cuando un usuario se prepara para lanzar un producto, curso, servicio o campaña y necesita que se creen tanto la lista de verificación de planificación como los activos visuales juntos."
allowed-tools: Read Write Glob mcp__claude_ai_Notion__notion-create-pages mcp__claude_ai_Notion__notion-search mcp__claude_ai_Canva__generate-design mcp__claude_ai_Canva__generate-design-structured mcp__claude_ai_Canva__resize-design mcp__claude_ai_Canva__export-design mcp__claude_ai_Canva__get-export-formats mcp__claude_ai_Canva__list-brand-kits mcp__claude_ai_Canva__create-folder mcp__claude_ai_Canva__move-item-to-folder mcp__claude_ai_Canva__get-design-thumbnail
metadata:
  author: Imperio Digital
  version: "1.0"
---

# Activos de Lanzamiento

## Cuándo Usar Este Skill

Usa este skill cuando necesites:
- Preparar un paquete completo de lanzamiento para un producto, curso, servicio o campaña
- Construir una lista de verificación estructurada de lanzamiento en Notion con tareas previas al lanzamiento, del día del lanzamiento y posteriores
- Generar activos visuales coordinados (gráfico de anuncio, conjunto para redes sociales, encabezado de email) en Canva
- Asegurar que nada se escape el día del lanzamiento combinando planificación y activos en un único workflow

**NO** uses este skill para:
- Creación continua de contenido en redes sociales (usa social-media-graphics o content-repurpose en su lugar)
- Construir un CRM o pipeline de clientes (usa client-crm en su lugar)
- Crear un calendario de contenido sin activos visuales (usa content-calendar en su lugar)
- Diseñar logos, identidad de marca completa o materiales impresos

---

## Referencia Rápida: Dimensiones de Activos

| Activo | Ancho | Alto | Relación de Aspecto | Propósito |
|-------|-------|--------|--------------|---------|
| Gráfico de Anuncio | 1080 | 1080 | 1:1 | Imagen principal, publicación Instagram |
| Publicación Facebook | 1200 | 630 | 1.91:1 | Anuncio en feed de Facebook |
| Publicación X/Twitter | 1600 | 900 | 16:9 | Imagen de cronología X/Twitter |
| Publicación LinkedIn | 1200 | 627 | 1.91:1 | Anuncio en feed de LinkedIn |
| Encabezado de Email | 600 | 200 | 3:1 | Banner superior para email de lanzamiento |

## Referencia Rápida: Secciones de Lista de Verificación de Lanzamiento

| Fase | Tareas | Timing |
|-------|-------|--------|
| Previo al Lanzamiento | 8 tareas | 7-14 días antes del lanzamiento |
| Día del Lanzamiento | 6 tareas | Día del lanzamiento |
| Posterior al Lanzamiento | 5 tareas | 1-7 días después del lanzamiento |

---

## Workflow Principal

TODO PAQUETE DE LANZAMIENTO COMIENZA CON UN BRIEF COMPLETO ANTES DE QUE SE CREE CUALQUIER PÁGINA EN NOTION O DISEÑO EN CANVA -- NUNCA CONSTRUYAS ACTIVOS SIN CONOCER EL PRODUCTO, AUDIENCIA Y MENSAJE CLAVE.

### Fase 1: Brief de Lanzamiento

Recopila todos los detalles del lanzamiento del usuario antes de construir nada.

1. **Nombre del producto/servicio** -- qué se está lanzando
2. **Fecha de lanzamiento** -- cuándo entra en vivo
3. **Audiencia objetivo** -- para quién es esto (datos demográficos, puntos débiles, intereses)
4. **Mensaje clave** -- el titular o propuesta de valor única para el lanzamiento
5. **CTA (call to action)** -- qué debe hacer la audiencia (inscribirse, comprar, unirse, matricularse)
6. **Plataformas** -- qué plataformas sociales son el objetivo (predeterminado: Instagram, Facebook, X/Twitter, LinkedIn)
7. **Kit de marca** -- usar kit de marca existente en Canva o especificar colores/fuentes
8. **Página padre de Notion** -- dónde crear la lista de verificación de lanzamiento

Si el usuario proporciona los elementos 1-5, procede con los valores predeterminados para los elementos 6-8. Pregunta solo sobre detalles críticos faltantes.

**Plantilla de brief para solicitudes vagas:**

```
Voy a construir tu paquete completo de lanzamiento. Respuestas rápidas necesarias:

1. ¿Qué estás lanzando? (nombre del producto/servicio)
2. ¿Cuándo es el día del lanzamiento?
3. ¿Para quién es? (audiencia objetivo)
4. ¿Cuál es el mensaje clave o titular?
5. ¿Qué deben hacer las personas? (CTA: comprar, inscribirse, matricularse, etc.)
6. ¿Qué plataformas? (predeterminado: Instagram, Facebook, X/Twitter, LinkedIn)
7. ¿Usar tu kit de marca de Canva? (S/N)
8. ¿Qué página de Notion debería albergar la lista de verificación?
```

**PUNTO DE CONTROL: No procedes a la Fase 2 hasta que tengas confirmados los elementos 1-5.** Los elementos 6-8 pueden usar valores predeterminados.

### Fase 2: Construir Lista de Verificación de Lanzamiento en Notion

Crea una página de lista de verificación de lanzamiento estructurada en Notion con bloques de tareas organizados por fase.

#### Paso 1: Localizar la Página Padre de Notion

1. Llama a `notion-search` con el nombre de página o palabras clave que proporcionó el usuario
2. Identifica la página padre correcta de los resultados de búsqueda
3. Confirma el ID de página con el usuario si existen múltiples coincidencias

```
Página de Notion encontrada: "Marketing Hub"
ID de Página: abc12345-def6-7890-ghij-klmnopqrstuv

Voy a crear la lista de verificación de lanzamiento bajo esta página. ¿Correcto?
```

**SI LA PÁGINA NO SE ENCUENTRA:**
- Pide el título exacto de la página
- Intenta `notion-search` de nuevo con una palabra clave más corta
- **Después de 3 búsquedas fallidas:** "No puedo encontrar esa página. Por favor verifica que existe y que la integración de Notion tiene acceso. Revisa Configuración > Conexiones en Notion."

#### Paso 2: Crear la Página de Lista de Verificación de Lanzamiento

Llama a `notion-create-pages` para crear una página bajo la página padre con la siguiente estructura. Usa el nombre del producto/servicio y la fecha de lanzamiento en el título.

**Título de la página:** `{Nombre del Producto} Lista de Verificación de Lanzamiento — {Fecha de Lanzamiento}`

**Contenido de la página (bloques de tareas organizados por sección):**

```
# Lista de Verificación de Lanzamiento {Nombre del Producto}

Fecha de Lanzamiento: {fecha}
Audiencia Objetivo: {audiencia}
Mensaje Clave: {titular}
CTA: {call to action}

---

## Previo al Lanzamiento (7-14 Días Antes)

- [ ] Finalizar la página del producto/servicio o copia de página de ventas
- [ ] Escribir y programar email de anuncio de lanzamiento
- [ ] Crear y programar publicaciones en redes sociales para todas las plataformas
- [ ] Preparar documento de FAQ o manejo de objeciones
- [ ] Configurar flujo de pago/checkout y probarlo de extremo a extremo
- [ ] Informar a miembros del equipo, socios o afiliados
- [ ] Programar publicaciones del día de lanzamiento en programador de redes sociales
- [ ] Revisar todos los activos visuales para consistencia de marca

## Día del Lanzamiento

- [ ] Publicar página del producto/servicio o ponerla en vivo
- [ ] Enviar email de anuncio de lanzamiento
- [ ] Publicar anuncio en todas las plataformas sociales
- [ ] Notificar a socios, afiliados y colaboradores
- [ ] Monitorear comentarios, DMs y respuestas de email — responder dentro de 1 hora
- [ ] Rastrear métricas tempranas (vistas de página, inscripciones, ventas)

## Posterior al Lanzamiento (1-7 Días Después)

- [ ] Enviar follow-up email a no abiertos (48 horas después del lanzamiento)
- [ ] Compartir social proof (testimonios, resultados tempranos, hitos)
- [ ] Participar con comentarios y preguntas en todas las plataformas
- [ ] Compilar reporte de métricas de lanzamiento (tráfico, conversiones, ingresos)
- [ ] Documentar lecciones aprendidas para el siguiente lanzamiento
```

Presenta la lista de verificación completada al usuario:

```
Lista de verificación de lanzamiento creada en Notion:

  Página: "{Nombre del Producto} Lista de Verificación de Lanzamiento — {Fecha de Lanzamiento}"
  Ubicación: Bajo "{Nombre de Página Padre}"
  Secciones: Previo al Lanzamiento (8 tareas), Día del Lanzamiento (6 tareas), Posterior al Lanzamiento (5 tareas)
  Total: 19 tareas accionables con casillas de verificación

Listo para generar tus activos visuales ahora.
```

**PUNTO DE CONTROL: Confirma que la lista de verificación se creó correctamente antes de proceder a la Fase 3.** Si la creación en Notion falla, resuélvelo antes de pasar a Canva.

### Fase 3: Generar Activos Visuales en Canva

Crea todos los elementos visuales de lanzamiento a partir de un único diseño principal, luego redimensiona y genera variantes específicas para cada plataforma.

#### Paso 1: Cargar Kit de Marca

1. Llama a `list-brand-kits` para recuperar kits de marca disponibles
2. Presenta nombres de kit de marca al usuario si existen múltiples
3. Toma nota de colores de marca, fuentes y referencias de logo para indicaciones de generación

```
Kit de marca cargado: "Mi Marca"
- Principal: #2D5BFF
- Secundario: #FF6B35
- Fuente: Montserrat Bold / Open Sans Regular
- Logo: Disponible
```

**SI NO EXISTE KIT DE MARCA:**
- Pide al usuario color principal, color secundario y preferencia de fuente
- Procede sin kit de marca — integra códigos hexadecimales de color y estilo de fuente directamente en indicaciones de generación
- Informa al usuario: "Puedes crear un kit de marca en Canva para consistencia futura."

#### Paso 2: Generar el Gráfico de Anuncio (Diseño Principal)

El gráfico de anuncio es el diseño principal. **Predeterminado: Publicación Instagram (1080x1080)** porque el cuadrado se recorta limpiamente a otros formatos.

1. Construye la indicación de generación incorporando:
   - Nombre del producto/servicio y mensaje clave como texto de titular
   - Texto de CTA como subtítulo
   - Colores de marca, fuentes y estilo del kit de marca
   - Tono visual apropiado para lanzamiento (emocionante, profesional, audaz)
   - Composición cuadrada (1:1) con texto y elementos focales centrados

2. Llama a `generate-design` con la indicación compuesta

3. Llama a `get-design-thumbnail` para previsualizar el diseño principal

4. Presenta al usuario:

```
Gráfico de anuncio generado: "{Nombre del Producto} Lanzamiento"
ID de Diseño: dsg_hero123
Previsualización: [miniatura mostrada]

¿Esto se ve bien, o te gustaría ajustes antes de que cree el resto del conjunto?
```

5. **Espera la aprobación del usuario antes de proceder**

**SI EL DISEÑO PRINCIPAL NO ALCANZA LA META:**
- Pregunta qué elemento específico necesita cambio (disposición, colores, colocación de texto, imágenes)
- Regenera con una indicación ajustada
- Si 2 regeneraciones aún no alcanzan, pide al usuario describir qué imaginan o proporcionar una imagen de referencia
- **Si 3 intentos fallan:** "Déjame intentar un enfoque diferente con `generate-design-structured` para más control de disposición."

#### Paso 3: Generar el Conjunto de Redes Sociales

Una vez que el diseño principal está aprobado, crea variantes específicas para cada plataforma.

1. **Redimensionar para Facebook (1200x630):**
   - Llama a `resize-design` con ID de diseño principal y dimensiones objetivo
   - Llama a `get-design-thumbnail` para verificar que titular y CTA sean visibles
   - Recorte ancho — asegura que el texto no se corte en los bordes

2. **Redimensionar para X/Twitter (1600x900):**
   - Llama a `resize-design` con ID de diseño principal y dimensiones objetivo
   - Llama a `get-design-thumbnail` para verificar
   - Formato ancho — verifica que el texto permanezca centrado

3. **Redimensionar para LinkedIn (1200x627):**
   - Llama a `resize-design` con ID de diseño principal y dimensiones objetivo
   - Llama a `get-design-thumbnail` para verificar
   - Casi idéntico a Facebook — confirma disposición limpia

**SI UN REDIMENSIONAMIENTO RECORTA TEXTO O ELEMENTOS CLAVE:**
- No entregues la versión recortada
- Llama a `generate-design` para esa dimensión de plataforma específica usando el mismo brief creativo
- Ajusta la indicación: "Centra el texto horizontalmente, mantén en el tercio medio verticalmente"
- Verifica la variante regenerada con `get-design-thumbnail`

#### Paso 4: Generar el Encabezado de Email

El encabezado de email tiene una relación de aspecto única (600x200) que no se redimensiona bien a partir del cuadrado principal. **Genera esto como un diseño separado.**

1. Llama a `generate-design` con una indicación personalizada para encabezado de email:
   - Dimensiones 600x200, relación de aspecto 3:1
   - Nombre del producto y mensaje clave en forma concisa
   - Colores y fuentes de marca que coincidan con el gráfico de anuncio
   - Disposición mínima — el texto debe ser legible a pequeño tamaño
   - Sin detalles finos que se pierdan a 200px de altura

2. Llama a `get-design-thumbnail` para verificar legibilidad

```
Encabezado de email generado: "{Nombre del Producto} - Banner de Email"
ID de Diseño: dsg_email456
Previsualización: [miniatura mostrada]

Texto legible a ancho de email. Colores de marca coinciden con el conjunto de anuncio.
```

#### Paso 5: Exportar Todos los Activos

1. Llama a `get-export-formats` para confirmar formatos disponibles

2. Exporta cada diseño como PNG (predeterminado):
   - Gráfico de anuncio (1080x1080)
   - Publicación Facebook (1200x630)
   - Publicación X/Twitter (1600x900)
   - Publicación LinkedIn (1200x627)
   - Encabezado de email (600x200)

3. Recopila todas las URLs de descarga de exportación

**CONVENCIÓN DE NOMBRES DE ARCHIVO:** `{product-name}-{asset-type}.png`
- Todo minúsculas, solo guiones, sin espacios
- Ejemplos: `email-mastery-announcement.png`, `email-mastery-facebook.png`, `email-mastery-email-header.png`

#### Paso 6: Organizar en Carpeta de Canva

1. Llama a `create-folder` con nombre: `{Nombre del Producto} — Activos de Lanzamiento`

2. Llama a `move-item-to-folder` para cada diseño colocarlo en la carpeta

3. Confirma la organización:

```
Todos los diseños organizados en carpeta de Canva: "{Nombre del Producto} — Activos de Lanzamiento"

Contenidos:
  - Gráfico de Anuncio (1080x1080)
  - Publicación Facebook (1200x630)
  - Publicación X/Twitter (1600x900)
  - Publicación LinkedIn (1200x627)
  - Encabezado de Email (600x200)
```

### Fase 4: Entregar el Paquete Completo

Presenta el paquete completo de lanzamiento con tanto la lista de verificación de Notion como todos los activos de Canva en un único resumen.

```
PAQUETE DE LANZAMIENTO COMPLETO: {Nombre del Producto}

Notion: "{Nombre del Producto} Lista de Verificación de Lanzamiento — {Fecha de Lanzamiento}" bajo "{Página Padre}"
        19 tareas (8 previas al lanzamiento, 6 día del lanzamiento, 5 posteriores)

Canva:  "{Nombre del Producto} — Activos de Lanzamiento" (PNG, {kit de marca o colores})
  Anuncio (1080x1080)   — [URL de exportación]
  Facebook (1200x630)   — [URL de exportación]
  X/Twitter (1600x900)  — [URL de exportación]
  LinkedIn (1200x627)   — [URL de exportación]
  Encabezado de Email (600x200) — [URL de exportación]

Próximos Pasos:
1. Revisa la lista de verificación en Notion — ajusta fechas/propietarios
2. Descarga activos o accede desde tu carpeta de Canva
3. Sube gráficos a tu programador de redes sociales
4. Añade encabezado de email a tu plantilla de email de lanzamiento
5. Comienza a trabajar en tareas previas al lanzamiento
```

---

## Ejemplo 1: Lanzamiento de Curso Online

**Solicitud del usuario:** "Estoy lanzando un curso online llamado 'Freelance Mastery' el 15 de marzo. Es para freelancers que quieren conseguir clientes mejor pagados. Mensaje clave: 'Deja de Cobra Poco. Comienza a Ganar lo Que Vales.' El CTA es 'Inscríbete ahora.' Mi página de Notion es 'Course Launches' y tengo un kit de marca de Canva."

**Ejecución:**

1. **Brief:** Producto: Freelance Mastery. Lanzamiento: 15 de marzo. Audiencia: freelancers. Mensaje: "Deja de Cobra Poco. Comienza a Ganar lo Que Vales." CTA: "Inscríbete ahora." Kit de marca: sí. Página padre de Notion: "Course Launches."

2. **Lista de verificación de Notion:** `notion-search` encuentra "Course Launches" (`pg_courses789`). Creada "Freelance Mastery Lista de Verificación de Lanzamiento — 15 de marzo" con 19 tareas (8 previas, 6 día de lanzamiento, 5 posteriores).

3. **Kit de marca:** `list-brand-kits` devuelve "Freelance Pro" — azul marino (#1A3A5C), oro (#E8A838), Poppins Bold / Inter Regular.

4. **Diseño principal:** `generate-design` con indicación incluyendo titular, colores de marca y estilo "profesional, aspiracional" a 1080x1080. Miniatura previsualized. Usuario aprueba.

5. **Conjunto social:** Diseño principal redimensionado para Facebook (1200x630), X/Twitter (1600x900), LinkedIn (1200x627). Todas las miniaturas verificadas — texto visible, sin recortes.

6. **Encabezado de email:** Generado por separado a 600x200 con titular condensado. Verificado legible.

7. **Exportado** todos los 5 como PNG: `freelance-mastery-announcement.png`, `freelance-mastery-facebook.png`, `freelance-mastery-twitter.png`, `freelance-mastery-linkedin.png`, `freelance-mastery-email-header.png`

8. **Organizado** en carpeta de Canva: "Freelance Mastery — Activos de Lanzamiento"

**Entregado:**

```
PAQUETE DE LANZAMIENTO COMPLETO: Freelance Mastery

Notion: "Freelance Mastery Lista de Verificación de Lanzamiento — 15 de marzo" (19 tareas)
Canva:  "Freelance Mastery — Activos de Lanzamiento" (5 diseños, PNG, kit de marca "Freelance Pro")

  Anuncio (1080x1080) | Facebook (1200x630) | X/Twitter (1600x900)
  LinkedIn (1200x627) | Encabezado de Email (600x200)

Próximo: Revisa lista de verificación, descarga activos, programa publicaciones para 15 de marzo.
```

---

## Ejemplo 2: Lanzamiento de Nueva Oferta de Servicio

**Solicitud del usuario:** "Soy coach empresarial añadiendo una nueva oferta VIP Day. La lanzo el próximo viernes. La audiencia son empresarios establecidos que quieren sesiones de estrategia intensivas 1-on-1. Mensaje: 'Un Día. Claridad Total.' CTA: 'Reserva tu VIP Day.' La página de Notion es 'Services'. Sin kit de marca pero mis colores son coral y carbón."

**Ejecución:**

1. **Brief:** Producto: VIP Day (servicio de coaching). Lanzamiento: próximo viernes. Audiencia: empresarios establecidos. Mensaje: "Un Día. Claridad Total." CTA: "Reserva tu VIP Day." Sin kit de marca — coral (#FF6F61) + carbón (#36454F). Página padre de Notion: "Services."

2. **Lista de verificación de Notion:** `notion-search` encuentra "Services" (`pg_services456`). Creada "VIP Day Lista de Verificación de Lanzamiento — {fecha}" con 19 tareas.

3. **Sin kit de marca:** `list-brand-kits` devuelve vacío. Usando colores manuales: coral (#FF6F61), carbón (#36454F). Fuente predeterminada a Playfair Display Bold / Lato Regular. Usuario informado sobre crear kit de marca para uso futuro.

4. **Diseño principal:** Generado a 1080x1080 con estilo elegante y mínimo. Usuario solicita "más coral" — regenerado con fondo coral y texto en carbón. Aprobado en segundo intento.

5. **Conjunto social:** Facebook y LinkedIn redimensionados limpiamente. Redimensionamiento de X/Twitter recortó titular — regenerado nativamente a 1600x900 con texto en tercio medio. Todos verificados.

6. **Encabezado de email:** Generado por separado a 600x200. Verificado legible.

7. **Exportado** todos los 5 como PNG: `vip-day-announcement.png`, `vip-day-facebook.png`, `vip-day-twitter.png`, `vip-day-linkedin.png`, `vip-day-email-header.png`

8. **Organizado** en carpeta de Canva: "VIP Day — Activos de Lanzamiento"

**Entregado:**

```
PAQUETE DE LANZAMIENTO COMPLETO: VIP Day

Notion: "VIP Day Lista de Verificación de Lanzamiento — {fecha}" (19 tareas)
Canva:  "VIP Day — Activos de Lanzamiento" (5 diseños, PNG, coral + carbón)

  Anuncio (1080x1080) | Facebook (1200x630) | X/Twitter (1600x900)*
  LinkedIn (1200x627) | Encabezado de Email (600x200)
  * X/Twitter regenerado nativamente debido a problema de recorte

Próximo: Revisa lista de verificación, descarga activos, programa publicaciones para día de lanzamiento.
```

---

## Lista de Verificación Previa a Entrega

Ejecuta esto antes de entregar. **NO SALTES NINGÚN ELEMENTO.**

```
Lista de Verificación Previa a Entrega:
  [ ] Lista de verificación de Notion creada bajo página padre correcta
  [ ] Las 3 secciones presentes (previo al lanzamiento, día del lanzamiento, posterior)
  [ ] 19 tareas con casillas de verificación
  [ ] Fecha de lanzamiento en título de página
  [ ] Diseño principal aprobado por usuario antes de redimensionar
  [ ] Los 5 activos visuales generados (anuncio, FB, X, LinkedIn, encabezado de email)
  [ ] Colores de marca coinciden con kit o valores especificados por usuario
  [ ] Texto legible en todos los activos a tamaño móvil
  [ ] Texto no recortado en ninguna variante redimensionada
  [ ] Estilo visual consistente en todos los 5 activos
  [ ] Nombres de archivo siguen convención {product-name}-{asset-type}.png
  [ ] Todos los diseños organizados en una carpeta de Canva
  [ ] Formato de exportación confirmado (PNG predeterminado)
```

---

## Recuperación y Solución de Problemas

### Página de Notion No Encontrada

1. Pide el título exacto de la página
2. Intenta `notion-search` con palabra clave más corta (p.ej., "Marketing" en lugar de "Marketing Hub Dashboard")
3. Pide al usuario confirmar que la página se comparte con la integración de Notion
4. **Después de 3 búsquedas fallidas:** "No puedo ubicar esa página. Verifica Configuración > Conexiones en Notion y confirma que la integración tiene acceso."

### Falla en Creación de Página de Notion

1. Verifica el ID de página padre buscando de nuevo
2. Reintenta una vez con los mismos parámetros
3. **Si falla de nuevo:** "La creación de página falló. Por favor verifica que la integración de Notion tiene acceso 'Can edit'. Ve a la página > menú tres-puntos > Conexiones."
4. **Alternativa:** Proporciona la lista de verificación completa como texto markdown formateado que el usuario puede pegar en Notion manualmente

### Kit de Marca No Encontrado

1. Informa al usuario: "No se encontraron kits de marca en tu cuenta de Canva."
2. Pide color principal (código hexadecimal o nombre), color secundario y preferencia de fuente
3. Procede con valores manuales integrados en la indicación de generación
4. Sugiere: "Puedes crear un kit de marca en Canva para acelerar futuros lanzamientos."

### El Redimensionamiento Recorta Texto o Elementos Clave

1. No entregues la versión recortada
2. Llama a `generate-design` para esa dimensión específica de plataforma usando el mismo brief creativo
3. Ajusta la indicación para el relación de aspecto objetivo:
   - Formatos anchos (Facebook, X/Twitter, LinkedIn): "Centra el texto horizontalmente, mantén en tercio medio verticalmente"
   - Encabezado de email: "Condensa el texto para ajustar relación 3:1, prioriza legibilidad"
4. Verifica la variante regenerada con `get-design-thumbnail`

### Falla en Generación de Diseño

1. Simplifica la indicación — elimina instrucciones de disposición complejas, mantén solo titular + colores + estilo
2. Reintenta una vez con la indicación simplificada
3. Si falla de nuevo, intenta `generate-design-structured` como alternativa
4. **Si 3 intentos fallan:** "La generación de diseño de Canva no está disponible en este momento. Aquí están las especificaciones para cada activo para que puedas crearlos manualmente: [proporciona dimensiones, colores, texto para los 5 activos]."

### Falla en Exportación

1. Verifica el ID de diseño llamando a `get-design-thumbnail`
2. Intenta exportar como JPG en lugar de PNG
3. **Si ambos fallan:** proporciona los IDs de diseño y nombre de carpeta de Canva para que el usuario exporte manualmente desde su cuenta de Canva

### Falla Parcial (Notion Funciona, Canva Falla — o Viceversa)

1. **Notion funciona, Canva falla:** Entrega la lista de verificación de Notion y proporciona especificaciones de diseño completas (dimensiones, colores, texto, notas de disposición) para los 5 activos para que el usuario los cree manualmente en Canva
2. **Canva funciona, Notion falla:** Entrega los activos de Canva y proporciona la lista de verificación completa como markdown formateado para que el usuario la pegue en Notion manualmente
3. **NUNCA saltes una mitad del paquete sin informar al usuario** — siempre entrega lo que funcionó y proporciona un camino claro para la parte que falló

---

## Anti-Patrones

- **NO** saltes el brief de lanzamiento — generar activos sin nombre de producto confirmado, mensaje clave y audiencia produce resultados genéricos y desalignados con marca
- **NO** crees activos de Canva antes de confirmar la lista de verificación de Notion — la lista de verificación fundamenta todo el launch plan y puede revelar detalles que afecten los elementos visuales
- **NO** generes cada variante de plataforma social desde cero — comienza con el gráfico de anuncio principal y redimensiona, solo regenera nativamente cuando el redimensionamiento recorta mal
- **NO** saltes la verificación de kit de marca — adivinar colores de marca produce activos inconsistentes que el usuario tendrá que rehacer
- **NO** exportes antes de que el usuario apruebe el diseño principal — redimensionar y exportar 5 activos desde un diseño principal no aprobado desperdicia tiempo
- **NO** dejes diseños dispersos en Canva — siempre organiza todos los activos de lanzamiento en una carpeta único etiquetada
- **NO** entregues los activos de Canva sin la lista de verificación de Notion (o viceversa) — este skill produce un paquete completo de lanzamiento, no una pieza de él
- **NO** uses JPG como exportación predeterminada — siempre predeterminado a PNG para gráficos de lanzamiento
- **NO** hagas demasiado denso ningún diseño con texto — los gráficos de lanzamiento necesitan una jerarquía visual clara con un máximo de un titular y una CTA
