---
name: comunicado-prensa
description: "Escribe comunicados de prensa profesionales siguiendo estilo AP con titular, línea de ubicación, párrafo introductorio, cuerpo, párrafo informativo y secciones de contacto de medios. Usa cuando un usuario está lanzando un producto, anunciando un hito, haciendo una contratación, formando una asociación, o tiene cualquier evento con valor noticiable para compartir con medios."
allowed-tools: Read Write Glob
metadata:
  author: Imperio Digital
  version: "1.0"
---

# Comunicado de Prensa

## Cuándo Usar Esta Skill

Usa esta skill cuando necesites:
- Anunciar lanzamiento de producto, liberación de característica o expansión de servicio a medios
- Compartir ronda de financiación, hito de ingresos o logro de compañía con la prensa
- Publicizar contratación nueva, promoción o nombramiento de junta asesora
- Anunciar asociación, adquisición o alianza estratégica
- Promover evento, gran apertura o iniciativa comunitaria
- Distribuir premio, certificación o reconocimiento de industria

**NO USES** esta skill para publicaciones de blog, anuncios de redes sociales, memorándums internos o copia de marketing. Esta es para comunicados de prensa estructurados destinados solo a periodistas y distribución de medios.

---

## Principio Fundamental

UN COMUNICADO DE PRENSA ES UN DOCUMENTO NOTICIOSO, NO UN ANUNCIO. CADA ORACIÓN DEBE REPORTAR HECHOS QUE UN PERIODISTA PUEDA VERIFICAR Y PUBLICAR SIN REESCRIBIR.

---

## Fase 1: Resumen Inicial

Antes de escribir una sola palabra, reúne la información que forma el comunicado completo. Sin resumen, sin borrador.

### Información Requerida

Pide al usuario cada uno de estos. Agrúpalos en dos rondas para evitar abrumar la conversación.

**Ronda 1 -- Las Noticias (pregunta todo a la vez):**

| Entrada | Qué Preguntar | Predeterminado |
|---------|---------------|--------|
| **Las noticias** | "¿Cuál es el anuncio? Una oración." | Sin predeterminado -- debe proporcionarse |
| **Tipo de lanzamiento** | "¿Cuál categoría: Lanzamiento de Producto, Financiación/Hito, Asociación, Contratación/Promoción, Evento o Premio?" | Inferido de las noticias |
| **Quién está involucrado** | "Nombre de compañía, personas clave y sus títulos." | Sin predeterminado -- debe proporcionarse |
| **Cronograma** | "¿Esto es para lanzamiento inmediato, o hay fecha de embargo?" | Para Lanzamiento Inmediato |
| **Atribución de cita** | "¿Quién debería ser citado en el comunicado? Nombre, título, compañía." | Fundador o CEO de compañía |

**Ronda 2 -- Contexto y Distribución (pregunta después de responder Ronda 1):**

| Entrada | Qué Preguntar | Predeterminado |
|---------|---------------|--------|
| **Por qué importa** | "¿Por qué debería un periodista importarle? ¿Cuál es el impacto en clientes, industria o comunidad?" | Sin predeterminado -- presiona por esto |
| **Detalles de apoyo** | "¿Algún número, fecha, característica, precio o información de disponibilidad a incluir?" | Incluye lo que el usuario proporciona |
| **Párrafo informativo de compañía** | "¿Tienes un párrafo 'Acerca de [Compañía]' existente? Si no, dame descripción de 2-3 oraciones: qué hace la compañía, a quién sirve y dónde está basada." | Genera desde info del usuario |
| **Contacto de medios** | "Nombre, correo electrónico y número de teléfono para el contacto de medios." | Sin predeterminado -- debe proporcionarse |
| **Medios objetivo** | "¿Qué medios u tipos de periodista estás buscando? (Publicaciones de industria, periódicos locales, blogs de tecnología nacional, etc.)" | Medios de industria general y locales |

### Plantilla de Resumen Inicial

Presenta esto al usuario antes de proceder:

```
## Resumen de Comunicado de Prensa

**Tipo de lanzamiento:** Lanzamiento de Producto
**Embargo:** PARA LANZAMIENTO INMEDIATO
**Las noticias:** Greenline Analytics lanza herramienta de pronóstico de inventario potenciada por IA para minoristas independientes
**Compañía:** Greenline Analytics, Denver, CO
**Persona clave:** Jordan Reeves, Fundador y CEO
**Atribución de cita:** Jordan Reeves + una cita de cliente (Maria Santos, Propietaria, The Corner Pantry)
**Por qué importa:** Los minoristas independientes pierden un promedio del 8% de ingresos por exceso de existencias y desabastecimiento -- esta herramienta reduce eso en 60% a punto de precio que tiendas pequeñas pueden permitirse ($49/mes)
**Detalles de apoyo:** Disponible a partir del 15 de marzo, se integra con Shopify y Square, 200 usuarios beta, prueba gratuita de 30 días
**Párrafo informativo:** Se genera desde info de compañía
**Contacto de medios:** Jordan Reeves, press@greenlineanalytics.com, (720) 555-0198
**Medios objetivo:** Publicaciones de industria minorista, periódicos de negocios de Denver, blogs de SaaS/startups
```

**PUNTO DE CONTROL: No procedes a Fase 2 hasta que el usuario confirme el resumen. Como mínimo, debes tener: las noticias, una persona citable con su título, información de compañía y contacto de medios.**

---

## Fase 2: Escribir

Con un resumen aprobado, escribe el comunicado de prensa siguiendo esta estructura exacta. Cada sección es requerida a menos que se indique como opcional.

### Estructura de Comunicado de Prensa

```
**PARA LANZAMIENTO INMEDIATO**
(o: **EMBARGADO HASTA [Fecha], [Hora] [Zona Horaria]**)

# [Titular]

## [Subtítulo -- opcional]

**[CIUDAD, ESTADO]** -- [Párrafo introductorio: quién, qué, cuándo, dónde, por qué
en 2-3 oraciones. Las noticias van aquí.]

[Párrafo del cuerpo 1: detalles de apoyo, contexto, problema de mercado]

"[Cita del portavoz principal -- prospectivo, vinculado al
impacto en clientes o mercado]," dijo [Nombre Completo],
[Título] de [Compañía].

[Párrafo del cuerpo 2: detalles adicionales -- características, precio,
disponibilidad, asociaciones]

"[Segunda cita -- opcional -- de socio, cliente o miembro de equipo
proporcionando validación externa]," dijo [Nombre Completo],
[Título] de [Compañía/Organización].

[Párrafo de cierre: disponibilidad, llamada a acción, dónde aprender más]

### Acerca de [Nombre de Compañía]

[Párrafo informativo: 2-4 oraciones. Qué hace la compañía, a quién sirve,
cuándo fue fundada, dónde está headquartered. Termina con URL de sitio web.]

### Contacto de Medios

[Nombre Completo]
[Título]
[Compañía]
[Correo Electrónico]
[Teléfono]

###
```

### Reglas de Escritura Sección por Sección

**Línea de Lanzamiento:**
- "PARA LANZAMIENTO INMEDIATO" en negrita, todas las mayúsculas -- esto es estándar y no negociable
- Si embargado, incluye fecha exacta, hora y zona horaria: "EMBARGADO HASTA 10 de marzo de 2025, 9:00 AM ET"

**Titular:**
- Comienza con verbo de acción (Lanza, Anuncia, Asegura, Expande, Nombra, Se Asocia)
- Contiene nombre de compañía
- Menos de 80 caracteres
- Mayúsculas de Título (estilo AP: capitaliza palabras con 4+ letras, todos los verbos, primera y última palabra)
- Sin puntos al final

**Subtítulo (opcional):**
- Agrega contexto que el titular no puede encajar
- Caso de oración
- Menos de 120 caracteres
- Usa cuando el titular solo no transmite lo suficiente para que un periodista decida si leer más

**Línea de ubicación:**
- Formato: CIUDAD, ESTADO (abreviado por AP: Calif., Colo., N.Y.) seguido de un guión em
- Usa la ciudad de headquarters de compañía a menos que las noticias sean específicas de ubicación (por ejemplo, apertura de tienda en ciudad diferente)

**Párrafo Introductorio:**
- Responde quién, qué, cuándo, dónde y por qué en 2-3 oraciones
- El hecho más importante va en la primera oración
- Nombre de compañía, nombre de producto y las noticias principales deben aparecer aquí
- Sin adjetivos como "líder" o "innovador" -- solo los hechos

**Párrafo del Cuerpo 1:**
- Contexto: por qué esto importa a la audiencia objetivo
- Problema de mercado o trasfondo de industria (1-2 oraciones con punto de datos si disponible)
- Cómo el anuncio aborda ese problema

**Cita Principal:**
- Atribuida a la persona más senior relevante (fundador, CEO, presidente)
- Prospectivo: qué significa esto para clientes, mercado o misión de compañía
- Debe sonar como algo que una persona realmente diría en voz alta
- Formato: "Texto de cita," dijo Nombre Completo, Título de Compañía.
- Usa "dijo" -- no "afirmó," "compartió," "expresó" o "señaló"

**Párrafo del Cuerpo 2:**
- Detalles específicos: características, precio, fechas de disponibilidad, especificaciones técnicas, nombres de socios
- Si lanzamiento de producto, aquí es donde listas 2-4 características clave como puntos de bala
- Si anuncio de financiación, aquí es donde nombras inversores e intención de uso de fondos

**Segunda Cita (opcional):**
- Usa cuando validación externa fortalece el anuncio
- Mejores fuentes: cliente, socio, inversor o figura de industria
- Debe agregar una perspectiva que la cita principal no cubre

**Párrafo de Cierre:**
- Dónde encontrar más información (URL de sitio web, landing page)
- Fecha de disponibilidad o cómo registrarse / asistir / aplicar
- Sin información nueva -- esto es el cierre

**Párrafo Informativo ("Acerca de [Compañía]"):**
- 2-4 oraciones, tiempo presente
- Qué hace la compañía (producto/servicio principal)
- A quién sirve (target market)
- Dónde está headquartered
- Termina con URL de sitio web de compañía
- Sin superlativos ("el líder," "el mejor," "de clase mundial")

**Contacto de Medios:**
- Nombre completo, título, compañía, correo electrónico, teléfono -- cada uno en su propia línea
- Esto es para periodistas, no clientes

**Marcador de Final:**
- Tres almohadillas centradas: ###
- Este es el marcador de final de comunicado de prensa universal

### Referencia Rápida de Estilo AP

Sigue estas reglas en todo el comunicado:

| Regla | Correcto | Incorrecto |
|------|---------|-----------|
| Mayúsculas de Título | Mayúsculas de Título | mayúsculas de título |
| Coma de Oxford | rojo, blanco y azul | rojo, blanco, y azul |
| Números bajo 10 | deletreados: "cinco ubicaciones" | 5 ubicaciones |
| Números 10+ | numerales: "12 empleados" | doce empleados |
| Porcentaje | 8% (numeral + símbolo) | ocho por ciento |
| Fechas | 15 de marzo (sin "º" o "º") | Marzo 15º |
| Estados | abreviados en línea de ubicación: Colo. | Colorado (en línea de ubicación) |
| Títulos antes de nombres | CEO Jordan Reeves | Jordan Reeves, el CEO |
| Títulos después de nombres | Jordan Reeves, fundador y CEO | Jordan Reeves, Fundador y CEO |
| Referencia de compañía | primera mención: nombre completo; después: nombre corto | nombre completo cada vez |

### Objetivo de Longitud

**400-600 palabras total.** La mayoría de periodistas dejan de leer después de 400 palabras. Cada palabra debe ganarse su lugar. Si el comunicado excede 600 palabras, corta detalles de apoyo antes de cortar citas o el párrafo introductorio.

---

## Fase 3: Revisar

Después de escribir el borrador, léelo de nuevo y verifica que cada sección requerida esté presente.

### Lista de Verificación de Revisión

1. PARA LANZAMIENTO INMEDIATO (o aviso de embargo) aparece arriba
2. Titular comienza con verbo de acción, contiene nombre de compañía, bajo 80 caracteres
3. Formato de línea de ubicación es correcto (CIUDAD, ESTADO -- )
4. Párrafo introductorio responde quién, qué, cuándo, dónde, por qué
5. Al menos una cita atribuida usando "dijo"
6. Párrafo informativo existe con descripción de compañía y URL
7. Contacto de medios incluye nombre, correo electrónico y teléfono
8. Marcador de final (###) está presente
9. Recuento de palabras total es 400-600
10. Sin superlativos de marketing ("revolucionario," "que cambia el juego," "de clase mundial")

---

## Fase 4: Entregar

Después de aprobación del usuario, completa estos pasos:

**Paso 1:** Determina la ruta de salida.

Nombre de archivo predeterminado: `[nombre-compañía]-[palabra-clave-tema]-comunicado-prensa.md`

**Paso 2:** Escribe el archivo usando la herramienta Write.

**Paso 3:** Confirma entrega. Reporta: "Tu comunicado de prensa ha sido guardado."

**Paso 4:** Sugiere próximos pasos: "¿Te gustaría que escriba un correo de lanzamiento para enviar a periodistas junto con este comunicado?"

---

## Anti-Patrones

**NUNCA hagas esto al escribir un comunicado de prensa:**

- **NO USES superlativos de marketing.** "Revolucionario," "que cambia el juego," "de clase mundial" son palabras publicitarias, no noticiosas. Los periodistas eliminan comunicados que leen como anuncios.
- **NO ENTIERRES las noticias.** El anuncio debe aparecer en la primera oración del párrafo introductorio.
- **NO ESCRIBAS citas que ningún humano diría.** "Estamos emocionados de apalancar capacidades sinérgicas para interrumpir el paradigma" no suena natural.
- **NO SALTES el párrafo informativo.** Los periodistas lo usan para verificar tu descripción de compañía.
- **NO SALTES el contacto de medios.** Un comunicado sin contacto es un callejón sin salida.
- **NO USES signos de exclamación.** Los comunicados de prensa son documentos fácticos.
- **NO INCLUYAS coma de Oxford.** El estilo AP omite la coma serial: "rojo, blanco y azul."
- **NO EXCEDAS 600 palabras.** Los periodistas tienen límites de atención.
- **NO USES primera persona.** Los comunicados se escriben en tercera persona.
- **NO ENVÍES sin corregir nombres y títulos.** Los errores matan credibilidad con periodistas.

---

## Recuperación

- **Usuario no puede articular las noticias:** Pregunta "¿Qué cambió?" o "Si escribiera una oración sobre tu compañía mañana, ¿qué diría?"
- **Sin persona citable:** La cita no necesita ser elaborada por la persona -- escríbela y pide aprobación.
- **Sin párrafo informativo:** Pregunta qué hace la compañía, a quién sirve y dónde está basada en 2-3 oraciones.
- **Anuncio no tiene hook noticioso:** Sugiere conectarlo a algo específico (lanzamiento, número, hito, contratación).
