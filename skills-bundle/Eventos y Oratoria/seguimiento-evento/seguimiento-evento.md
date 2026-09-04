---
name: seguimiento-evento
description: "Crea secuencias de seguimiento post-evento con emails de agradecimiento, distribución de encuestas, entrega de contenido y rutas de nutrición."
allowed-tools: Read Write Glob
metadata:
  author: Imperio Digital
  version: "1.0"
---

# Seguimiento de Evento

## Cuándo Usar Este Skill

Usa este skill cuando necesites:
- Crear una secuencia de follow-up email post-evento para asistentes
- Diseñar procesos de distribución de encuestas y recopilación de comentarios
- Construir sistemas de entrega de contenido para grabaciones, diapositivas y recursos
- Planificar rutas de nutrición que conviertan asistentes en clientes o miembros de comunidad

**NO** uses este skill para marketing pre-evento o comunicaciones del día del evento. Esto es para todo lo que sucede después del evento.

---

## Principio Fundamental

EL EVENTO NO TERMINA CUANDO TERMINA LA ÚLTIMA SESIÓN — TERMINA CUANDO CADA ASISTENTE HA SIDO AGRADECIDO, ENCUESTADO, DADO ACCESO A GRABACIONES Y OFRECIDO UN PRÓXIMO PASO CLARO.

---

## Fase 1: Brief

### Inputs Requeridos

| Input | Qué Preguntar | Predeterminado |
|-------|------------|---------|
| **Nombre y fecha del evento** | "¿Qué evento acaba de ocurrir?" | Sin predeterminado — debe proporcionarse |
| **Conteo de asistentes** | "¿Cuántas personas asistieron?" | Sin predeterminado — debe proporcionarse |
| **Contenido para entregar** | "¿Tienes grabaciones, diapositivas o recursos para compartir?" | Grabaciones + decks de diapositivas |
| **Siguiente oferta** | "¿Qué deseas que los asistentes hagan a continuación? (comprar, unirse, suscribirse, asistir próximo evento)" | Unirse a programa pagado o comunidad |
| **Objetivos de encuesta** | "¿Qué comentarios necesitas?" | Satisfacción general + sugerencias de mejora |
| **Cronograma de seguimiento** | "¿Cuánto tiempo debe ejecutarse la follow-up sequence?" | 14 días |

**PUNTO DE CONTROL:** Confirma el brief antes de construir la secuencia.

---

## Fase 2: Planificar

### Cronograma de Seguimiento

```
## Secuencia Post-Evento

**Día 0 (evento termina):** Email de agradecimiento + conclusiones clave
**Día 1:** Email de encuesta de comentarios
**Día 3:** Email de entrega de grabación/recurso
**Día 5:** Reel destacado — mejores momentos, citas, fotos
**Día 7:** Recordatorio de encuesta (si no se completó)
**Día 10:** Email de nutrición — "Aquí está cómo implementar lo que aprendiste"
**Día 14:** Oferta de siguiente paso — "El siguiente nivel es [programa pagado/próximo evento/comunidad]"
```

### Segmentación de Audiencia

```
| Segmento | Criterios | Enfoque de Seguimiento |
|---------|----------|----------------|
| Asistió en vivo | Mostró up para sesiones | Secuencia completa + trato VIP |
| Registrado pero ausente | Se registró, no asistió | Acceso a grabación + encuadre "te lo perdiste" |
| VIP/premium | Pagó por nivel superior | Seguimiento personal + bonificación exclusiva |
| Speakers/patrocinadores | Partners | Agradecimiento + datos de resultados + conversación de renovación |
```

**PUNTO DE CONTROL:** Presenta el cronograma y segmentos para aprobación.

---

## Fase 3: Escribir

### Email 1: Agradecimiento (Día 0)

```
Asunto: Te presentaste — aquí está lo próximo

[Agradecimiento personal del anfitrión]
[Top 3 conclusiones clave o momentos del evento]
[Qué esperar en los próximos días (grabaciones, recursos, encuesta)]
[Un elemento de acción inmediata: "La #1 cosa a hacer esta semana basado en lo que aprendiste"]
```

### Email 2: Encuesta (Día 1)

```
Asunto: Favor rápido — 2 minutos para hacer el próximo evento aún mejor

[Reconoce su tiempo e input]
[Enlace a encuesta — mantenla bajo 5 minutos]
[Qué harás con los comentarios]
[Opcional: incentivo para completar (entrada de rifa, recurso bonificación)]
```

### Email 3: Entrega de Contenido (Día 3)

```
Asunto: Tus grabaciones y recursos de [Nombre del Evento] están listos

[Enlace de acceso a grabaciones]
[Decks de diapositivas o recursos descargables]
[Orden de visualización recomendado o guía "comienza aquí"]
[Expiración de acceso si aplica]
```

### Email 4: Reel Destacado (Día 5)

```
Asunto: Los mejores momentos de [Nombre del Evento]

[Fotos, citas y estadísticas clave del evento]
[Aviso de compartir en redes sociales — anima a asistentes a compartir su experiencia]
[Enlace de comunidad si aplica]
```

### Email 5: Implementación (Día 10)

```
Asunto: Cómo realmente usar lo que aprendiste en [Nombre del Evento]

[Elige un framework o táctica clave del evento]
[Divídelo en 3 pasos de implementación]
[Ofrece ayuda: recurso, plantilla o soporte de comunidad]
```

### Email 6: Oferta de Siguiente Paso (Día 14)

```
Asunto: ¿Listo para el siguiente nivel?

[Conecta la experiencia del evento a la siguiente oferta]
[Qué es la oferta y para quién es]
[Beneficio específico — qué lograrán]
[CTA con plazo o incentivo para asistentes del evento]
[Precios exclusivos de asistente o bonificación si aplica]
```

---

## Fase 4: Pulir

### 1. Diseño de Encuesta

```
## Encuesta Post-Evento (5 minutos)

1. En general, ¿cómo calificarías el evento? (1-10)
2. ¿Cuál fue la sesión más valiosa o conclusión clave? (Abierta)
3. ¿Qué mejorarías para la próxima vez? (Abierta)
4. ¿Qué tan probable es que asistas de nuevo? (1-10 NPS)
5. ¿Qué tan probable es que recomiendes este evento a un colega? (1-10 NPS)
6. ¿Podemos usar tus comentarios como testimonial? (Sí/No)
7. ¿Qué temas deseas ver en eventos futuros? (Abierta)
```

### 2. Lista de Verificación de Entrega de Contenido

```
- [ ] Las grabaciones están editadas (elimina silencio, problemas técnicos)
- [ ] Los decks de diapositivas se recogen de todos los speakers
- [ ] Los recursos se organizan en un único punto de acceso (Notion, Google Drive o área de miembros)
- [ ] Los enlaces de acceso se prueban y funcionan
- [ ] Las fechas de expiración se establecen y comunican (si aplica)
- [ ] La atribución del speaker se incluye en todos los materiales compartidos
```

### 3. Métricas a Rastrear

```
## Rendimiento de Seguimiento
- Tasa de apertura de email de agradecimiento (objetivo: 60%+)
- Tasa de finalización de encuesta (objetivo: 30%+)
- Tasa de acceso a grabación (objetivo: 50%+)
- Tasa de clics de email de nutrición (objetivo: 5%+)
- Tasa de conversión de oferta de siguiente paso (rastrear contra conteo de asistentes del evento)
- Puntuación NPS de encuesta (objetivo: 50+)
```

---

## Ejemplo 1: Seguimiento de Conferencia Empresarial

```
Día 0: "Gracias por hacer Scale Summit inolvidable" — top 3 momentos + próximos pasos
Día 1: Encuesta con rifa para entrada libre al próximo evento
Día 3: Todas las 12 grabaciones de sesión + diapositivas de speaker
Día 7: "El #1 framework de Scale Summit — cómo implementarlo esta semana"
Día 14: "Alumnos de Scale Summit obtienen 20% descuento en nuestro programa de crecimiento de 12 semanas"
```

## Ejemplo 2: Seguimiento de Summit Virtual

```
Día 0: "El summit es un envoltorio — aquí están tus conclusiones clave"
Día 1: Encuesta de 3 preguntas (mantenla ultra corta para virtual)
Día 2: Oferta de pase VIP — "Obtén acceso de por vida a todas las grabaciones por $47"
Día 5: Reel destacado + etiquetas sociales de speaker
Día 10: Recurso libre relacionado al tema del summit
Día 14: Oferta de membresía de comunidad
```

---

## Anti-Patrones

- **Sin seguimiento en absoluto** — el error más común. El silencio después de un evento desperdicia toda la buena voluntad que construiste.
- **Esperar demasiado tiempo** — el email de agradecimiento debe salir dentro de horas, no días. El momentum desaparece rápido.
- **Venta forzada inmediata** — lanzar tu programa pagado 2 horas después del evento se siente extractivo. Agradece primero, vende después.
- **Sin encuesta** — no puedes mejorar lo que no mides. Siempre recopila comentarios.
- **Emails genéricos** — "Estimado asistente" es perezoso. Usa su nombre y segmenta por tipo de asistencia.
- **Grabaciones nunca entregadas** — si prometiste grabaciones, entrégalas dentro de 72 horas o pierdes confianza.

---

## Recuperación

- **Las grabaciones no están listas:** Envía un email "próximamente" con una fecha de entrega específica. No esperes a que estén las grabaciones para enviar el agradecimiento.
- **Tasa de respuesta de encuesta es baja:** Envía un recordatorio, luego acepta los datos que tienes. Ofrecer un pequeño incentivo (rifa, recurso bonus) ayuda.
- **Los asistentes no responden a nutrición:** Acorta la secuencia. Si no están comprometidos por email 3, pueden no convertirse este ciclo. Agrégalos a tu lista regular.
- **El usuario no recopilió emails de asistentes:** Si fue un evento in-person, usa la lista de registro. Para eventos futuros, haz que la captura de email sea obligatoria en check-in.
