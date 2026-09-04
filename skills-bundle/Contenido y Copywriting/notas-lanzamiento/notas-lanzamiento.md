---
name: notas-lanzamiento
description: "Escribe notas de lanzamiento amigables para el usuario con cambios categorizados, guías de migración y problemas conocidos. Úsalo cuando comuniques actualizaciones de software a usuarios e interesados."
allowed-tools: Read Write Glob
metadata:
  author: Imperio Digital
  version: "1.0"
---

# Notas de Lanzamiento

## Cuándo Usar Esta Habilidad

Usa esta habilidad cuando necesites:
- Escribir notas de lanzamiento para una actualización de software o nueva versión
- Comunicar cambios importantes con guías de migración
- Documentar problemas conocidos y soluciones alternativas para un lanzamiento
- Crear notas de lanzamiento que sirvan a audiencias técnicas y no técnicas

**NO** uses esta habilidad para registros de cambios de productos (entradas continuas y más cortas), anuncios de características (orientados a marketing), o análisis posteriores internos de ingeniería. Esto es para notas de lanzamiento formales vinculadas a una versión o actualización específica.

---

## Principio Fundamental

LAS NOTAS DE LANZAMIENTO SIRVEN A DOS AUDIENCIAS SIMULTÁNEAMENTE — USUARIOS QUE QUIEREN SABER QUÉ CAMBIÓ Y DESARROLLADORES QUE NECESITAN SABER QUÉ SE ROMPIÓ. ESCRIBE PARA AMBOS.

---

## Fase 1: Análisis Inicial

### Entradas Requeridas

| Entrada | Qué Preguntar | Predeterminado |
|-------|------------|---------|
| **Número de versión** | "¿Cuál es el identificador de versión o lanzamiento?" | No hay predeterminado — debe proporcionarse |
| **Fecha de lanzamiento** | "¿Cuándo se lanza este lanzamiento?" | Hoy |
| **Lista de cambios** | "Lista todos los cambios — características, mejoras, correcciones, cambios importantes." | No hay predeterminado — debe proporcionarse |
| **Cambios importantes** | "¿Hay algún cambio importante que requiera acción del usuario?" | Ninguno |
| **Problemas conocidos** | "¿Hay algún problema conocido incluido en este lanzamiento?" | Ninguno |
| **Audiencia** | "¿Son los lectores desarrolladores técnicos, usuarios finales o ambos?" | Ambos |

**PUNTO DE CONTROL: Confirma el análisis inicial antes de escribir.**

---

## Fase 2: Categorizar Cambios

Ordena cada cambio en una de estas categorías:

- **Aspectos Destacados** — Características principales o cambios que merecen ser destacados al inicio
- **Nuevas Características** — Capacidades que no existían antes
- **Mejoras** — Enhancements a funcionalidad existente
- **Correcciones de Errores** — Problemas resueltos en este lanzamiento
- **Cambios Importantes** — Cambios que requieren acción del usuario o actualizaciones de código
- **Deprecaciones** — Características siendo eliminadas (con cronograma)
- **Problemas Conocidos** — Problemas incluidos en este lanzamiento (con soluciones alternativas)

Presenta la lista categorizada para confirmación.

**PUNTO DE CONTROL: Confirma la categorización antes de escribir las notas completas.**

---

## Fase 3: Escritura

### Formato de Notas de Lanzamiento

```
# Notas de Lanzamiento — v[X.Y.Z]
**Fecha de Lanzamiento:** [Fecha]

## Aspectos Destacados

[Resumen de 1-2 párrafos de los cambios más importantes en este lanzamiento. Escribe para alguien ojeando — debería entender el impacto en 30 segundos.]

## Nuevas Características

- **[Nombre de característica]** — [Qué hace y cómo acceder. 1-2 oraciones.]

## Mejoras

- **[Área mejorada]** — [Qué cambió y el beneficio del usuario. 1 oración.]

## Correcciones de Errores

- **[Descripción del problema]** — [Qué estaba roto y confirmación de que está resuelto. 1 oración.]

## Cambios Importantes

### [Título del cambio]
**Impacto:** [Quién está afectado y cómo]
**Acción requerida:** [Exactamente qué deben hacer los usuarios]
**Guía de migración:** [Instrucciones paso a paso]
**Límite de tiempo:** [Cuándo el comportamiento antiguo deja de funcionar]

## Deprecaciones

- **[Nombre de característica]** — Deprecada a partir de este lanzamiento. Será eliminada en v[X.Y.Z]. Usa [alternativa] en su lugar.

## Problemas Conocidos

- **[Descripción del problema]** — [Solución alternativa si está disponible. Corrección esperada en v[X.Y.Z].]
```

### Reglas de Escritura

- **La sección de aspectos destacados es obligatoria** — incluso para lanzamientos pequeños, resume los cambios clave en 2-3 oraciones
- **Lenguaje orientado al usuario** — traduce cambios técnicos a impacto del usuario
- **Descripciones específicas de correcciones de errores** — "Corregido fallo de inicio de sesión en Safari 17" no "Corregido error de autenticación"
- **Los cambios importantes reciben tratamiento completo** — declaración de impacto, acción requerida, pasos de migración y límite de tiempo
- **Los problemas conocidos incluyen soluciones alternativas** — nunca lista un problema conocido sin una solución alternativa o fecha de corrección esperada

---

## Fase 4: Pulido

### 1. Guía de Migración (si existen cambios importantes)

Escribe una guía de migración paso a paso:
- Ejemplos de código antes/después
- Cambios de configuración requeridos
- Cronograma para compatibilidad hacia atrás
- Contacto de soporte para problemas de migración

### 2. Plan de Distribución

| Canal | Formato | Audiencia |
|---------|--------|----------|
| Notificación en la aplicación | Resumen de aspectos destacados + enlace | Todos los usuarios |
| Email | Notas completas de lanzamiento | Usuarios registrados |
| Sitio de documentación | Notas completas con guías de migración | Desarrolladores |
| Blog | Solo aspectos destacados con enfoque en características | Prospectos y público |
| Redes sociales | Una línea sobre el cambio más importante | Audiencia general |

### 3. Lista de Verificación de Calidad

```
## Lista de Verificación de Notas de Lanzamiento

- [ ] El número de versión y la fecha están claramente indicados
- [ ] La sección de aspectos destacados resume cambios clave en 2-3 oraciones
- [ ] Todos los cambios están categorizados (Nuevo, Mejorado, Corregido, Importante, Deprecado)
- [ ] Los cambios importantes incluyen impacto, acción requerida y pasos de migración
- [ ] Las correcciones de errores describen específicamente qué estaba roto
- [ ] Los problemas conocidos incluyen soluciones alternativas o cronogramas de corrección
- [ ] El lenguaje es comprensible para usuarios no técnicos
- [ ] Sin jerga interna, números de ticket o referencias de código en notas orientadas al usuario
- [ ] El plan de distribución cubre todos los canales relevantes
- [ ] La cronología de deprecación es específica (número de versión y fecha)
```

---

## Ejemplo

**Versión:** v2.4.0
**Fecha de lanzamiento:** 27 de febrero de 2026

**Extracto de aspectos destacados:**
"La versión 2.4.0 introduce facturas recurrentes y un panel rediseñado. Las facturas recurrentes te permiten programar facturación automática en cualquier cadencia — configúralo una vez y las facturas se envían por sí solas. El nuevo panel carga 60% más rápido y muestra tus métricas más importantes de un vistazo."

**Extracto de cambio importante:**
```
### Puntos finales de API v1 Deprecados

**Impacto:** Todos los usuarios que hacen llamadas API a puntos finales api.example.com/v1/.
**Acción requerida:** Actualiza tus llamadas API para usar puntos finales /v2/ antes del 30 de abril de 2026.
**Guía de migración:**
1. Reemplaza /v1/ con /v2/ en todas las URLs de puntos finales
2. Actualiza el formato del encabezado de Autorización (ver documentos)
3. Prueba con el ambiente sandbox
4. Cambia llamadas de producción antes del 30 de abril

**Límite de tiempo:** 30 de abril de 2026. Después de esta fecha, los puntos finales /v1/ devolverán 410 Gone.
```

---

## Anti-Patrones

- **Volcar mensajes de commit de git** — "Corregido #4521" y "Refactorizado servicio de usuario" no son notas de lanzamiento. Traduce a impacto del usuario.
- **Ocultar cambios importantes** — enterrarlos al final garantiza usuarios enojados. Encabeza con cambios importantes o destácalos prominentemente.
- **Sin guía de migración** — decir a los usuarios que algo se rompió sin decirles cómo arreglarlo es peor que no decirles nada.
- **Omitir problemas conocidos** — los usuarios los encontrarán de todas formas. Documentarlos proactivamente construye confianza.
- **Relleno de marketing** — las notas de lanzamiento no son publicaciones de blog. Sé factual, específico y conciso.

---

## Recuperación

- **Lanzamiento pequeño con pocos cambios:** Escribe una nota breve. Incluso "Correcciones de errores y mejoras de desempeño" es mejor que el silencio, pero agrega especificidades.
- **Cambio importante principal con migración compleja:** Crea un documento de guía de migración dedicado. Enlaza desde las notas de lanzamiento.
- **Problema conocido sin solución alternativa:** Declara el problema, reconoce el impacto y proporciona un cronograma para la corrección. Ofrece contacto de soporte directo.
- **Lanzamiento fue revertido:** Publica una nota explicando la reversión, qué fue afectado y cuándo se espera el relanzamiento.
