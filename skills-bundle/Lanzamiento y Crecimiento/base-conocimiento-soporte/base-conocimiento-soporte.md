---
name: base-conocimiento-soporte
description: "Construye una base de conocimiento completa de soporte al cliente con FAQs por niveles, plantillas de respuestas predefinidas, árboles de decisión para resolución de problemas y protocolos de escalamiento. Usa cuando un usuario necesite sistematizar el soporte al cliente, reducir tiempos de respuesta, capacitar personal de soporte o dejar de responder las mismas preguntas repetidamente."
allowed-tools: Read Write Glob
metadata:
  author: Imperio Digital
  version: "1.0"
---

# Base de Conocimiento de Soporte

## Cuándo Usar Este Skill

Usa este skill cuando necesites:
- Construir una base de conocimiento de soporte al cliente desde cero para tu negocio
- Sistematizar respuestas a preguntas que te hacen una y otra vez
- Capacitar a un VA, nuevo empleado de soporte o miembro del equipo que necesita manejar consultas de clientes
- Reducir tu tiempo personal de respuesta creando recursos de autoservicio
- Crear reglas de escalamiento para que solo te involucren cuando realmente se necesita tu intervención

**NO** uses este skill para crear copy de marketing, FAQs de ventas o contenido de centro de ayuda público diseñado para SEO. Esto construye un sistema operativo interno de soporte.

## Cómo Funciona

CADA RESPUESTA DE SOPORTE DEBE SONAR COMO UN HUMANO REAL QUE CONOCE EL NEGOCIO — NUNCA COMO UN BOT LEYENDO UN GUION.

---

### Fase 1: Recopilar — Recolectar Escenarios de Soporte

Reúne cada pregunta, queja y escenario de soporte que maneja el negocio.

1. **Pregunta al usuario su tipo de negocio y oferta principal** (producto, servicio, curso, coaching, SaaS, etc.)
2. **Solicita sus 10-20 preguntas más comunes de clientes** — si no puede listarlas, estimula con estas categorías:
   - Preguntas pre-compra (precios, características, cómo funciona)
   - Problemas de cuenta y acceso (login, contraseña, facturación)
   - Problemas con el producto o servicio (defectos, bugs, problemas de envío)
   - Solicitudes de reembolso y cancelación
   - Preguntas de uso y cómo hacerlo
   - Quejas y feedback negativa
3. **Pide material de soporte existente** — hilos de email, capturas de pantalla de DMs, documentos de ayuda, páginas de Notion, o cualquier archivo que tengan. Léelos con `Read` o `Glob` si proporcionan rutas de archivo.
4. **Identifica los canales de soporte** que usan (email, DM, chat en vivo, teléfono, herramienta de helpdesk)
5. **Pregunta sobre sus pain points actuales** — qué toma más tiempo, qué se escala innecesariamente, qué se cae entre las grietas

Presenta un resumen al usuario:

```
## Panorama de Soporte

**Negocio:** Tienda e-commerce de velas artesanales
**Canales:** Email, Instagram DM, mensajes de Etsy
**Volumen:** ~40 consultas/semana

**Problemas Principales Identificados:**
1. "¿Dónde está mi pedido?" — 35% de todas las consultas
2. "¿Puedo cambiar/cancelar mi pedido?" — 15%
3. "Llegó dañado" — 12%
4. "¿Ofrecen aromas personalizados?" — 10%
5. "¿Cómo uso la suscripción?" — 8%
6. "Quiero un reembolso" — 7%
7. "Consulta mayorista" — 5%
8. "Otro" — 8%

**Pain Points:**
- La dueña responde personalmente cada DM y email
- Sin plantillas — cada respuesta escrita desde cero
- El proceso de artículos dañados es inconsistente
- Sin reglas claras de escalamiento para el VA
```

**PUNTO DE CONTROL: No procedas hasta que el usuario confirme que el panorama de soporte es preciso y completo.**

---

### Fase 2: Organizar — Clasificar por Niveles

Ordena cada problema identificado en uno de cuatro niveles basados en complejidad y quién debe manejarlo.

1. **Asigna cada problema a un nivel:**

| Nivel | Qué Cubre | Quién lo Maneja | Respuesta Objetivo |
|-------|-----------|-----------------|-------------------|
| Nivel 1 | Autoservicio / FAQ | Cliente (sin personal necesario) | Instantánea |
| Nivel 2 | Respuestas predefinidas | VA o personal de soporte | Menos de 2 horas |
| Nivel 3 | Árboles de resolución | Personal de soporte capacitado | Menos de 24 horas |
| Nivel 4 | Escalamiento | Dueño del negocio | Menos de 48 horas |

2. **Aplica la regla 80/20** — Nivel 1 y Nivel 2 deben manejar al menos el 80% de las consultas. Si no lo hacen, re-examina si algunos problemas de Nivel 3 pueden simplificarse en plantillas de Nivel 2.

3. **Presenta el mapa de niveles al usuario:**

```
## Mapa de Niveles

### Nivel 1 — FAQ de Autoservicio (los clientes se responden solos)
- ¿Dónde está mi pedido? → link de página de rastreo
- ¿Cuáles son los tiempos de envío? → política de envío
- ¿Envían internacionalmente? → política de envío
- ¿Cuál es su política de devolución? → página de devoluciones

### Nivel 2 — Respuestas Predefinidas (VA envía con personalización menor)
- ¿Puedo cambiar/cancelar mi pedido?
- ¿Ofrecen aromas personalizados?
- ¿Cómo uso la suscripción?
- Preguntas generales sobre productos

### Nivel 3 — Árboles de Resolución (VA sigue árbol de decisión)
- Artículo llegó dañado → foto requerida → flujo de reemplazo o reembolso
- Artículo incorrecto recibido → verificar pedido → flujo de reenvío
- Problema de facturación de suscripción → verificar estado de pago → reintentar o cancelar

### Nivel 4 — Escalamiento al Dueño
- Solicitudes de reembolso mayores a $75
- Amenazas legales o contracargos
- Consultas mayoristas/asociaciones
- Quejas publicadas públicamente en redes sociales
- Cualquier cosa sin resolver después de 2 intercambios entre soporte y cliente
```

**PUNTO DE CONTROL: El usuario debe aprobar las asignaciones de niveles antes de comenzar a escribir.**

---

### Fase 3: Escribir — Crear Todo el Contenido de la Base de Conocimiento

Desarrolla el contenido completo para cada nivel. Trabaja en orden.

#### Paso 1: Escribir Entradas FAQ de Nivel 1

Para cada entrada FAQ, escribe:
- **Pregunta** como la formularía el cliente (conversacional, no formal)
- **Respuesta corta** (1-3 oraciones, directa)
- **Respuesta detallada** (si es necesario, con links o pasos)

Formato:

```markdown
### ¿Dónde está mi pedido?

**Respuesta rápida:** Puedes rastrear tu pedido en cualquier momento usando el link de rastreo en tu email de confirmación de envío.

**Detalles:** Después de hacer tu pedido, recibirás un email de confirmación dentro de 1 hora. Una vez que tu pedido se envíe (1-2 días hábiles para artículos en stock), recibirás un segundo email con un número de rastreo y link. Si no recibiste ninguno de los emails, revisa tu carpeta de spam primero, luego contáctanos a soporte@ejemplo.com.
```

Escribe 8-15 entradas FAQ dependiendo del negocio. **Cada respuesta debe incluir un siguiente paso específico** — nunca termines con "contáctanos" como única opción.

#### Paso 2: Escribir Plantillas de Respuesta Predefinida de Nivel 2

Para cada respuesta predefinida, escribe:
- **Disparador** — la situación que requiere esta plantilla
- **Nota de tono** — una línea de guía (ej., "cálido y comprensivo" o "amigable pero firme")
- **Plantilla** con `{variables}` para puntos de personalización
- **Cuándo NO usar** — casos límite donde esta plantilla es incorrecta

Formato:

```markdown
### Solicitud de Cambio/Cancelación de Pedido

**Disparador:** El cliente quiere modificar o cancelar un pedido que aún no se ha enviado.
**Tono:** Servicial, sin fricción — hazlo fácil.

**Plantilla:**
Hola {nombre},

¡Gracias por escribirnos! Revisé tu pedido #{numero_pedido} y aún no se ha enviado, así que absolutamente podemos {cambiar/cancelar}lo para ti.

{Si cambio: Esto es lo que actualicé: [describir cambio]. Tu nuevo total es {monto}. Todo lo demás sigue igual.}

{Si cancelación: He cancelado el pedido y tu reembolso de {monto} llegará a tu cuenta dentro de 3-5 días hábiles.}

¡Avísame si hay algo más en lo que pueda ayudarte!

{firma}

**NO usar cuando:** El pedido ya se envió. Cambia a la plantilla "Pedido Ya Enviado".
```

Escribe 6-12 plantillas de respuesta predefinida. **Cada plantilla debe incluir al menos una variable de personalización** — nada de bloques genéricos para copiar y pegar.

#### Paso 3: Escribir Árboles de Decisión de Resolución de Nivel 3

Para cada escenario de resolución, escribe un árbol de decisión claro de si/entonces que un agente de soporte pueda seguir sin adivinar.

Formato:

```markdown
### Resolución de Artículo Dañado

**Comienza aquí:** El cliente reporta un artículo dañado o defectuoso.

1. Pide al cliente que envíe 1-2 fotos del daño.
   - **Si se reciben fotos y el daño se confirma** → ve al paso 2
   - **Si las fotos no son claras** → responde: "Gracias por enviarlo. ¿Podrías tomar una foto más con buena iluminación mostrando el área dañada? Eso me ayuda a resolverlo más rápido para ti."
   - **Si el cliente se niega a enviar fotos** → ve al paso 4

2. Verifica el valor del pedido.
   - **Si el valor del pedido es menor a $50** → envía reemplazo inmediatamente, sin devolución requerida. Usa la plantilla "Reemplazo Gratuito".
   - **Si el valor del pedido es $50-$150** → ofrece opción: reemplazo o reembolso completo. Usa la plantilla "Opciones de Resolución por Daño".
   - **Si el valor del pedido es mayor a $150** → escala al dueño (Nivel 4).

3. Procesa la resolución.
   - Registra el problema en el rastreador de soporte con: número de pedido, descripción del daño, links de fotos, resolución elegida.
   - Envía confirmación al cliente usando la plantilla apropiada.
   - Marca al proveedor/lote de producción si este es el tercer reporte de daño del mismo producto en 30 días.

4. Excepción sin foto.
   - Si el cliente es comprador recurrente (3+ pedidos) → confía en él y ofrece reemplazo.
   - Si el cliente es comprador primerizo → explica que las fotos son necesarias para seguimiento de calidad y ofrece ayuda para tomar una. Si aún se niega después de un seguimiento, escala al dueño.
```

Escribe 3-6 árboles de decisión. **Cada rama debe terminar con una acción específica** — sin callejones sin salida.

#### Paso 4: Escribir Protocolo de Escalamiento de Nivel 4

Define exactamente cuándo y cómo los problemas llegan al dueño del negocio.

```markdown
## Protocolo de Escalamiento

### Cuándo Escalar
- Solicitudes de reembolso que exceden {umbral_monto definido por el usuario}
- Lenguaje legal, amenazas de contracargo o menciones de abogado
- Quejas públicas en redes sociales o plataformas de reseñas
- El cliente solicita "hablar con el dueño/gerente"
- Cualquier problema sin resolver después de 2 intercambios entre soporte y cliente
- Consultas mayoristas, de asociación o de medios

### Cómo Escalar
1. Escribe un resumen breve: nombre del cliente, número de pedido (si aplica), problema, qué se ha intentado hasta ahora.
2. Reenvía el hilo completo de conversación — no resumas las palabras del cliente, inclúyelas textualmente.
3. Marca como URGENTE si involucra: amenazas legales, quejas públicas o pedidos mayores a {umbral_alto_valor}.
4. Tiempo de respuesta esperado del dueño: 24 horas (URGENTE: 4 horas).

### Qué Decirle al Cliente
Usa esta plantilla mientras se escala:

"Hola {nombre}, quiero asegurarme de que esto reciba la atención que merece, así que he contactado a {nombre_dueño} quien te dará seguimiento personalmente dentro de {plazo}. Gracias por tu paciencia."

**NUNCA** digas "Solo soy la persona de soporte" o "No puedo ayudarte con eso." Siempre enmarca el escalamiento como conseguirles mejor/más rápida ayuda.
```

**PUNTO DE CONTROL: Presenta el borrador completo de los cuatro niveles al usuario. Obtén aprobación o solicitudes de revisión antes de entregar los archivos finales.**

---

### Fase 4: Entregar — Organizar en Archivos Estructurados

Escribe la base de conocimiento en archivos organizados que el usuario pueda consultar, compartir con su personal o cargar en una herramienta de helpdesk.

1. **Crea la estructura de directorios:**

```
base-conocimiento-soporte/
├── README.md                              # Resumen, tabla de niveles, referencia rápida
├── nivel-1-faq/
│   └── faq.md                             # Todas las entradas FAQ
├── nivel-2-plantillas/
│   └── respuestas-predefinidas.md         # Todas las plantillas de respuesta
├── nivel-3-resolucion/
│   └── arboles-de-decision.md             # Todos los árboles de resolución
├── nivel-4-escalamiento/
│   └── protocolo-escalamiento.md          # Reglas y plantillas de escalamiento
└── guia-soporte.md                        # Versión completa en un solo archivo para onboarding rápido
```

2. **Escribe el README.md** con:
   - Nombre del negocio y lista de canales de soporte
   - Tabla resumen de niveles (copia de la Fase 2)
   - Links de referencia rápida a cada archivo
   - Fecha de última actualización

3. **Escribe guia-soporte.md** como un documento combinado con los cuatro niveles — este es el archivo "entrégale esto a un nuevo empleado en su primer día".

4. **Confirma todos los archivos escritos** y proporciona un resumen:

```
## Base de Conocimiento Completa

**Archivos creados:**
- base-conocimiento-soporte/README.md — resumen y referencia rápida
- base-conocimiento-soporte/nivel-1-faq/faq.md — 12 entradas FAQ
- base-conocimiento-soporte/nivel-2-plantillas/respuestas-predefinidas.md — 8 plantillas de respuesta
- base-conocimiento-soporte/nivel-3-resolucion/arboles-de-decision.md — 4 árboles de decisión
- base-conocimiento-soporte/nivel-4-escalamiento/protocolo-escalamiento.md — reglas de escalamiento
- base-conocimiento-soporte/guia-soporte.md — guía completa en un archivo para onboarding

**Cobertura:** Nivel 1 + Nivel 2 manejan un estimado del 82% de las consultas.
**Siguiente paso:** Revisa cada archivo y personaliza las {variables} con los detalles reales de tu negocio.
```

---

## Ejemplo Concreto 1: Tienda E-Commerce (Velas Artesanales)

**El usuario dice:** "Vendo velas artesanales en Etsy y mi propia tienda Shopify. Recibo como 40 mensajes por semana y respondo personalmente cada uno. Estoy contratando un VA el próximo mes y necesito un sistema de soporte."

**Salida de Fase 1 (extracto):**
```
## Panorama de Soporte

**Negocio:** Tienda de velas de soya artesanales (Etsy + Shopify)
**Canales:** Mensajes de Etsy, email de Shopify, Instagram DM
**Volumen:** ~40 consultas/semana

**Problemas Principales:**
1. ¿Dónde está mi pedido? / solicitud de rastreo — 35%
2. Cambio o cancelación de pedido — 15%
3. Artículo dañado al llegar — 12%
4. Preguntas de aromas personalizados o pedidos al por mayor — 10%
5. Gestión de suscripción — 8%
6. Solicitudes de reembolso — 7%
7. Consultas mayoristas — 5%
8. Cuidado de velas / tiempo de quemado — 5%
9. Envoltura de regalo / empaque especial — 3%
```

**Salida de Fase 4 (extracto de respuestas-predefinidas.md):**
```markdown
### Consulta de Aroma Personalizado

**Disparador:** El cliente pregunta si hacen aromas personalizados o pueden modificar una vela existente.
**Tono:** Entusiasta pero honesto sobre lo que es posible.

Hola {nombre},

¡Me encanta que estés interesado/a en un aroma personalizado! Así funciona:

Ofrezco mezclas personalizadas para pedidos de 6 o más velas. Eliges hasta 3 notas de fragancia de nuestro menú de aromas (te envío el link), y yo creo una combinación personalizada solo para ti. El tiempo de entrega es de 7-10 días hábiles ya que cada lote se vierte a mano.

Para velas individuales, no puedo hacer mezclas personalizadas completas, pero estoy encantado/a de recomendarte la opción más cercana de nuestra colección actual si me cuentas qué vibra buscas.

¿Quieres que te envíe el menú de aromas?

{firma}

**NO usar cuando:** El cliente pregunta sobre aromas personalizados al por mayor (50+ unidades). Escala al dueño.
```

---

## Ejemplo Concreto 2: SaaS / Negocio de Coaching Online

**El usuario dice:** "Manejo un programa de coaching online con un sitio de membresía. Los miembros pagan mensualmente. Mis mayores dolores de cabeza son problemas de login, gente que quiere cancelar, y preguntas sobre qué incluye su plan."

**Salida de Fase 1 (extracto):**
```
## Panorama de Soporte

**Negocio:** Membresía de coaching online (3 niveles: Starter, Pro, Elite)
**Canales:** Email (soporte@), widget de chat en la app, DMs del grupo de Facebook
**Volumen:** ~60 consultas/semana

**Problemas Principales:**
1. No puedo iniciar sesión / el reseteo de contraseña no funciona — 25%
2. ¿Qué incluye mi plan? / preguntas de upgrade — 20%
3. Solicitudes de cancelación y reembolso — 15%
4. Errores de facturación o cobros dobles — 10%
5. Cómo acceder a un módulo específico del curso — 10%
6. Problemas técnicos con reproducción de video — 8%
7. Solicitudes de coaching 1-a-1 (solo Elite) — 7%
8. Normas de comunidad / publicaciones reportadas — 5%
```

**Salida de Fase 3 (extracto de arboles-de-decision.md):**
```markdown
### Resolución de Problemas de Login / Acceso

**Comienza aquí:** El miembro reporta que no puede iniciar sesión o acceder al contenido.

1. Pregunta qué dirección de email está usando para iniciar sesión.
   - **Si proporciona un email** → verifica si coincide con el email de membresía en archivo.
     - **Coincidencia encontrada** → ve al paso 2
     - **Sin coincidencia** → responde: "Parece que tu membresía está bajo un email diferente. Intenta iniciar sesión con {email_correcto}. Si no funciona, avísame y lo resuelvo."
   - **Si no está seguro de qué email** → busca por nombre en la base de datos de miembros.
     - **Encontrado** → proporciona su email (enmascarado: j***n@gmail.com) y pide que intente de nuevo.
     - **No encontrado** → pide el email usado en la compra y revisa registros del procesador de pago.

2. Confirma el estado de su suscripción.
   - **Activa** → envía link de reseteo de contraseña manualmente. Responde: "Acabo de enviarte un reseteo de contraseña fresco a {email}. Revisa tu bandeja de entrada (y carpeta de spam). El link expira en 1 hora."
   - **Expirada/cancelada** → responde: "Parece que tu membresía terminó el {fecha}. ¿Te gustaría reactivarla? Puedo enviarte un link directo."
   - **Pago fallido** → responde: "Tu último pago del {fecha} no se procesó. ¿Quieres actualizar tu tarjeta en archivo? Aquí está el link: {link_facturacion}"

3. Si el reseteo de contraseña no funciona después de 2 intentos:
   - Limpia su sesión manualmente en el panel de administración.
   - Envía una nueva contraseña temporal por email.
   - **Si sigue sin acceso** → escala al dueño con nota: "Posible problema del lado de la plataforma, el reseteo manual falló dos veces."
```

---

## Anti-Patrones

- **NO** uses lenguaje robótico corporativo. Escribe "Encantado de ayudarte" no "Su consulta ha sido recibida y será procesada conforme al procedimiento establecido." Los clientes notan la diferencia.
- **NO** crees plantillas de talla única. Una solicitud de reembolso de un cliente leal recurrente y una solicitud de reembolso de un comprador primerizo en el primer día requieren tonos y políticas diferentes. Construye lógica de bifurcación.
- **NO** omitas casos límite en los árboles de decisión. Si una rama puede ocurrir, documéntala. Cada "¿y si...?" que un agente de soporte pueda preguntar debe tener respuesta en el árbol.
- **NO** entierres la respuesta detrás de cortesías innecesarias. El cliente quiere la respuesta primero, luego la calidez. Lidera con la resolución: "Tu reembolso ha sido procesado" no "Muchas gracias por comunicarte con nosotros hoy, realmente apreciamos tu paciencia y comprensión..."
- **NO** escribas respuestas FAQ que solo digan "contáctanos." Cada entrada FAQ debe intentar responder la pregunta directamente. "Contáctanos" es solo el respaldo después de la respuesta.
- **NO** crees plantillas con cero variables de personalización. Si una respuesta puede enviarse a cualquier cliente sin cambiar una sola palabra, se sentirá como spam.

---

## Recuperación

- **El usuario no puede identificar sus preguntas principales:** Pídele que reenvíe o pegue sus últimos 10-15 mensajes de clientes. Extrae patrones de las conversaciones crudas en su lugar.
- **El usuario no tiene material de soporte existente:** Comienza desde su página de producto/servicio y genera preguntas probables basadas en lo que un cliente necesitaría saber antes de comprar, durante la entrega y después de usar el producto.
- **El árbol de decisión se vuelve demasiado complejo (más de 5 ramas de profundidad):** Divídelo en dos árboles separados. Un árbol debe manejar el camino común, y un segundo árbol maneja el camino de casos límite.
- **El usuario quiere soportar un canal no cubierto:** Pregunta por las restricciones del canal (longitud de respuesta, formato, si se soportan adjuntos) y adapta las plantillas en consecuencia.
- **Si 3 intentos de recopilar requisitos fallan** (el usuario no está seguro, da respuestas vagas o sigue cambiando el alcance): Detente y re-evalúa. Sugiere al usuario que pase una semana registrando cada consulta de cliente en una hoja de cálculo simple antes de construir la base de conocimiento. Proporciona una plantilla de registro:

```
| Fecha | Canal | Pregunta del Cliente (textual) | Categoría | Tiempo para Resolver | Resuelto Por |
|-------|-------|-------------------------------|-----------|---------------------|-------------|
```

Esto da datos reales para construir en lugar de adivinar.
