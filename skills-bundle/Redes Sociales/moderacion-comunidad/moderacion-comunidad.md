---
name: moderacion-comunidad
description: "Crea pautas de moderación de comunidad con reglas, procedimientos de escalamiento y recomendaciones de moderación automatizada. Úsalo al establecer o mejorar moderación para comunidades online."
allowed-tools: Read Write Glob
metadata:
  author: Imperio Digital
  version: "1.0"
---

# Moderación de Comunidad

## Cuándo Usar Este Skill

Usa este skill cuando necesites:
- Escribir reglas de comunidad y pautas de moderación para una comunidad online
- Crear procedimientos de escalamiento para manejar violaciones y conflictos
- Diseñar workflows de moderación automatizada (filtros, auto-respuestas)
- Entrenar moderadores con pautas claras y marcos de decisión

**NO** uses este skill para estrategia comunitaria o planificación de lanzamiento (usa skill de community-launch). Esto es específicamente para sistemas de moderación.

---

## Principio Fundamental

LA BUENA MODERACIÓN ES INVISIBLE — LOS MIEMBROS DEBEN SENTIRSE SEGUROS Y ESCUCHADOS SIN NOTAR LAS REGLAS EN ACCIÓN.

---

## Fase 1: Resumen

### Información Requerida

| Entrada | Qué Preguntar | Por Defecto |
|---------|---------------|------------|
| **Plataforma de comunidad** | "¿Cuál es la plataforma? Discord, Slack, Grupo de Facebook, Circle, Skool?" | Sin defecto — debe proporcionarse |
| **Tamaño de comunidad** | "¿Cuántos miembros?" | Bajo 500 |
| **Tipo de comunidad** | "¿Gratis, de pago, o basada en curso?" | Gratis |
| **Problemas actuales** | "¿Qué problemas de moderación enfrentas?" | Ninguno aún — construyendo proactivamente |
| **Cantidad de moderadores** | "¿Cuántos moderadores (incluyéndote)?" | 1 (solo el fundador) |
| **Tono** | "¿Debe la moderación ser estricta, amistosa, o mínima?" | Amistosa pero firme |

**PUNTO DE CONTROL: Confirma el resumen antes de construir pautas.**

---

## Fase 2: Esquema

```
1. Reglas de Comunidad — estándares claros y ejecutables
2. Categorías de Violación — niveles de severidad y ejemplos
3. Procedimientos de Escalamiento — paso a paso para cada nivel de violación
4. Pautas de Moderador — cómo deben comportarse y decidir los moderadores
5. Moderación Automatizada — filtros, bots y auto-respuestas
6. Proceso de Apelaciones — cómo pueden los miembros impugnar decisiones
```

**PUNTO DE CONTROL: Aprueba el esquema antes de escribir.**

---

## Fase 3: Escribir

### 1. Reglas de Comunidad

```
## Reglas de Comunidad

**Regla 1: Sé Respetuoso**
Desacuerda con ideas, no con personas. Sin ataques personales, insultos u hostigamiento.

**Regla 2: Añade Valor**
Comparte conocimiento, haz preguntas reflexivas, y ayuda a otros. Posts de poco esfuerzo ("lol," "igual") se desalientan.

**Regla 3: Sin Spam o Auto-Promoción**
No dejes enlaces a tus productos, servicios, o contenido sin contexto. Comparte tu trabajo cuando responde genuinamente una pregunta o añade a la discusión.

**Regla 4: Mantente en Tema**
Usa los canales correctos para discusiones correctas. Los posts fuera de tema serán movidos o eliminados.

**Regla 5: Sin Hurgar**
No hagas DM a miembros con propuestas de venta sin solicitar, mensajes de reclutamiento, u ofertas de servicio.

**Regla 6: Protege Privacidad**
No compartas información personal sobre otros miembros. No hagas screenshots de conversaciones privadas sin consentimiento.

**Regla 7: Sigue Términos de Plataforma**
Todas las reglas específicas de plataforma aplican. Las violaciones que rompan TOS de plataforma pueden resultar en eliminación inmediata.
```

### 2. Categorías de Violación

```
## Niveles de Severidad de Violación

| Nivel | Tipo | Ejemplos | Acción |
|-------|------|----------|--------|
| **Bajo** | Fricción de pauta | Post fuera de tema, comentario de poco esfuerzo, auto-promo accidental | Redirección amistosa |
| **Medio** | Violación de regla | Auto-promoción repetida, comentarios despectivos/groseros, ignorar reglas de canal | Advertencia + educación |
| **Alto** | Violación seria | Ataques personales, hostigamiento, discurso de odio, doxxing | Silenciamiento inmediato + revisión |
| **Crítico** | Tolerancia cero | Amenazas, contenido ilegal, hostigamiento sexual, estafas | Ban inmediato |
```

### 3. Procedimientos de Escalamiento

```
## Playbook de Escalamiento

### Violaciones Bajas
1. Responde públicamente con una redirección amistosa: "Hola [Nombre], ¡esto sería un buen ajuste para #[canal-correcto]! ¿Te importaría re-publicar allí?"
2. Si repetido: envía un DM privado explicando la pauta
3. Sin advertencia formal a menos que continúe después del DM

### Violaciones Medias
1. Elimina o edita el contenido
2. Envía un DM privado: "Hola [Nombre], eliminé tu post porque [regla específica]. Aquí está lo que nos gustaría ver en su lugar: [orientación]. Sin resentimientos — solo manteniendo la comunidad valiosa para todos."
3. Log del incidente en el registro de moderación
4. Si segunda ofensa: advertencia formal con consecuencias indicadas

### Violaciones Altas
1. Silencia inmediatamente al miembro (restricción temporal)
2. Elimina el contenido ofensivo
3. Investiga el contexto (¿fue provocado? ¿hay historial?)
4. El moderador senior o fundador decide: advertencia formal, ban temporal, o ban permanente
5. Comunica la decisión vía DM con razonamiento claro

### Violaciones Críticas
1. Ban permanente inmediato — sin advertencias
2. Elimina todo contenido ofensivo
3. Reporta a la plataforma si es requerido (amenazas, actividad ilegal)
4. Notifica a la comunidad solo si el incidente fue público
```

### 4. Pautas de Moderador

```
## Cómo Deben Operar los Moderadores

**Principios:**
- Sé justo y consistente — las mismas reglas aplican a todos
- Asume buena intención primero — la mayoría de violaciones son accidentales
- Sé firme pero amable — enforce reglas sin ser hostil
- Documenta todo — log todas las advertencias y bans
- Nunca moderes cuando estés enojado — calma antes de responder

**Marco de Decisión:**
1. ¿Es esto una violación de regla? → Si no, déjalo.
2. ¿Es esta la primera ofensa? → Si sí, redirección o DM amistoso.
3. ¿Fue intencional o accidental? → Los accidentes reciben más gracia.
4. ¿Está alguien siendo dañado? → Si sí, actúa inmediatamente.
5. En duda, escalona al fundador.

**Lo que los moderadores NUNCA deben hacer:**
- Involucrarse en argumentos públicos con miembros
- Tomar decisiones de moderación basadas en desagrado personal
- Compartir discusiones de moderación fuera del equipo mod
- Moderar sus propios conflictos (escalona a otro mod)
```

### 5. Moderación Automatizada

```
## Recomendaciones de Automatización

| Herramienta/Característica | Lo Que Hace | Plataforma |
|---------------------------|-----------|-----------|
| Filtro de palabra clave | Auto-marca o elimina posts que contienen palabras prohibidas | La mayoría de plataformas |
| Filtro de enlace | Retiene posts con enlaces para revisión de moderador | Discord, Slack |
| Ralentización de nuevo miembro | Restringe posts para nuevos miembros (primeras 24-48 horas) | Discord, algunos foros |
| Auto-bienvenida | Envía mensaje de onboarding a nuevos miembros | La mayoría de plataformas |
| Sistema de reporte | Permite a miembros marcar contenido para revisión de mod | La mayoría de plataformas |

**Filtros de palabra clave recomendados:**
- Insultos y discurso de odio obvios (la plataforma usualmente proporciona defaults)
- Nombres de marca competidora (opcional, depende de comunidad)
- Frases de spam comunes ("DMme para detalles," "revisa mi bio")
```

### 6. Proceso de Apelaciones

```
## Apelaciones de Miembro

Si un miembro cree que una acción de moderación fue injusta:
1. DM a un moderador (no el que tomó la acción, si es posible)
2. Indica qué pasó y por qué están en desacuerdo
3. El equipo mod revisa dentro de 48 horas
4. La decisión se comunica vía DM con razonamiento
5. El fundador tiene la palabra final en apelaciones contestadas

**Las apelaciones NO están disponibles para violaciones críticas (amenazas, contenido ilegal, hostigamiento).**
```

---

## Fase 4: Pulir

### 1. Lista de Verificación de Moderación

```
## Lista de Verificación del Sistema de Moderación

- [ ] Las reglas comunitarias están escritas en lenguaje claro y llano
- [ ] Los niveles de severidad de violación están definidos con ejemplos
- [ ] Los procedimientos de escalamiento son paso a paso para cada nivel
- [ ] Las pautas de moderador incluyen marco de decisión
- [ ] Las herramientas de moderación automatizada están configuradas
- [ ] El proceso de apelaciones está documentado
- [ ] La plantilla de log de moderación está creada
- [ ] Las reglas están publicadas en una ubicación visible y fijada
```

### 2. Plantilla de Log de Moderación

```
| Fecha | Miembro | Violación | Severidad | Acción Tomada | Moderador | Notas |
|------|--------|-----------|----------|---------------|-----------|-------|
```

---

## Ejemplo: Pautas de Moderación para Comunidad de Discord de 200 Personas

```
Reglas: 7 reglas principales (publicadas en #reglas, aceptadas al unirse)
Niveles de severidad: Bajo (redirección), Medio (DM de advertencia), Alto (silenciamiento + revisión), Crítico (ban)
Automatización: Filtro de palabra clave para insultos, retención de enlace para nuevos miembros, auto-bienvenida DM
Moderadores: Fundador + 2 campeones comunitarios
Apelaciones: DM a cualquier mod, ventana de revisión de 48 horas
```

---

## Anti-Patrones

- **Sin reglas publicadas** — los miembros no pueden seguir reglas que no conocen. Fíjalas prominentemente.
- **Enforcement inconsistente** — aplicar reglas diferente basado en quién sea el miembro destruye confianza.
- **Sobre-moderación** — eliminar cada post ligeramente fuera de tema mata la espontaneidad y hace la comunidad sentirse estéril.
- **Argumentos públicos con violadores** — siempre maneja la moderación en DMs. Las confrontaciones públicas escalan.
- **Sin documentación** — sin un log de moderación, los infractores repetidos se escapan y las decisiones son inconsistentes.
- **Burnout de moderador** — una persona moderando una comunidad de 500+ sola se quemará. Recluta ayuda temprano.

---

## Recuperación

- **La comunidad ya es tóxica:** Publica las nuevas reglas, anuncia un nuevo comienzo, y enforce consistentemente desde el primer día. Algunos miembros se irán — está bien.
- **Los moderadores desacuerdan en decisiones:** Crea el marco de decisión de arriba y úsalo como estándar. El fundador tiene palabra final en áreas grises.
- **Reacción de miembro contra decisión de moderación:** Comparte tu razonamiento (en DMs o públicamente si es necesario) calmada y factualmente. Mantente en decisiones justas.
- **Demasiadas violaciones para manejar:** Aumenta la moderación automatizada, recluta más moderadores, y considera si el onboarding de la comunidad atrae los miembros equivocados.
- **Nadie para moderar:** Comienza con herramientas automatizadas y recluta 1-2 miembros activos y confiables como moderadores voluntarios con pautas claras.
