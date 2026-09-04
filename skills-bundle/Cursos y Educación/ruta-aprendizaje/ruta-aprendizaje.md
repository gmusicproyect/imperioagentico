---
name: ruta-aprendizaje
description: "Mapea rutas de aprendizaje con habilidades de requisito previo, evaluaciones de hito y secuencias de recursos recomendados."
allowed-tools: Read Write Glob
author: Imperio Digital
version: "1.0"
---

# Ruta de Aprendizaje

## Cuándo Usar Este Skill

Usa este skill cuando necesites:
- Mapear una ruta de aprendizaje estructurada para una habilidad o dominio de conocimiento
- Secuenciar temas de requisitos previos para que los estudiantes construyan conocimiento en el orden correcto
- Diseñar evaluaciones de hito que confirmen que están listos antes de avanzar
- Curar recomendaciones de recursos para cada etapa de la ruta

**NO** uses este skill para planes de lección individuales (usa lección-plan), páginas de ventas de curso o planificación de títulos académicos. Es para mapear el viaje completo desde "no sé nada" a "puedo hacerlo con confianza" en un área de habilidad específica.

---

## Principio Fundamental

UNA RUTA DE APRENDIZAJE ES UN MAPA, NO UN MANDATO — MUESTRA LA RUTA MÁS EFICIENTE DESDE "NO SÉ NADA" A "PUEDO HACER ESTO CON CONFIANZA" MIENTRAS PERMITE A LOS ESTUDIANTES MOVERSE A SU PROPIO RITMO.

---

## Fase 1: Definición de la Ruta

### Entradas Requeridas

| Entrada | Qué Preguntar | Predeterminado |
|---------|--------------|--------|
| **Habilidad o dominio** | "¿Qué habilidad o tema cubre esta ruta de aprendizaje?" | Sin predeterminado — debe proporcionarse |
| **Estudiante objetivo** | "¿Para quién es esto — principiantes absolutos, que cambian carrera, profesionales mejorando habilidades?" | Principiantes absolutos |
| **Meta final** | "¿Qué debe poder hacer el estudiante al final de esta ruta?" | Sin predeterminado — debe proporcionarse |
| **Duración estimada** | "¿Cuánto debería tomar la ruta completa?" | 3-6 meses a 5-10 horas/semana |
| **Formato de recursos** | "¿Son los recursos gratuitos, de pago, tu propio contenido o curados de fuentes externas?" | Mezcla de gratuitos y de pago recomendado |

**PUNTO DE CONTROL: Confirma la habilidad, estudiante objetivo y meta final antes de mapear la ruta.**

---

## Fase 2: Arquitectura de la Ruta

### Diseño de Etapa

Organiza la ruta en 3-5 etapas:

```
## [Título de Ruta de Aprendizaje]

### Etapa 1: Fundación (Semanas 1-4)
**Meta:** [Qué el estudiante puede hacer después de completar esta etapa]
**Requisitos previos:** Ninguno
**Hito:** [Cómo prueban que están listos para avanzar]

### Etapa 2: Habilidades Centrales (Semanas 5-10)
**Meta:** [Qué el estudiante puede hacer después de completar esta etapa]
**Requisitos previos:** Hito de Etapa 1 pasado
**Hito:** [Evaluación o proyecto]

### Etapa 3: Aplicación (Semanas 11-16)
**Meta:** [Qué el estudiante puede hacer después de completar esta etapa]
**Requisitos previos:** Hito de Etapa 2 pasado
**Hito:** [Proyecto en el mundo real o pieza de portafolio]

### Etapa 4: Maestría (Semanas 17-24)
**Meta:** [Qué el estudiante puede hacer después de completar esta etapa]
**Requisitos previos:** Hito de Etapa 3 pasado
**Hito:** [Proyecto capstone, certificación o demostración]
```

### Plantilla de Detalle de Etapa

Para cada etapa, proporciona:

```
## Etapa [X]: [Nombre de Etapa]

### Objetivos de Aprendizaje
Al final de esta etapa, podrás:
1. [Objetivo 1 — específico y medible]
2. [Objetivo 2]
3. [Objetivo 3]

### Temas Cubiertos
| Tema | Descripción | Horas Estimadas |
|------|-------------|----------------|
| [Tema 1] | [Descripción breve] | [X] horas |
| [Tema 2] | [Descripción breve] | [X] horas |
| [Tema 3] | [Descripción breve] | [X] horas |

### Recursos Recomendados
| Recurso | Tipo | Costo | Notas |
|---------|------|-------|-------|
| [Recurso 1] | [Libro / Curso / Video / Artículo] | [Gratuito / $X] | [Por qué este recurso] |
| [Recurso 2] | [Tipo] | [Costo] | [Notas] |
| [Recurso 3] | [Tipo] | [Costo] | [Notas] |

### Actividades Prácticas
- [Actividad 1 — práctica práctica aplicando el tema]
- [Actividad 2]
- [Actividad 3]

### Evaluación de Hito
**Formato:** [Quiz / Proyecto / Demostración de habilidad]
**Criterios de aprobación:** [Qué califica como "listo para avanzar"]
**Si no apruebas:** [Qué revisar antes de reintentar]
```

---

## Fase 3: Mapeo de Requisitos Previos

### Gráfico de Dependencia

Mapea qué temas dependen de cuáles:

```
## Mapa de Requisitos Previos

[Tema A] → Sin requisitos previos (comienza aquí)
[Tema B] → Requiere Tema A
[Tema C] → Requiere Tema A
[Tema D] → Requiere Temas B + C
[Tema E] → Requiere Tema D
[Capstone] → Requiere todos los temas
```

### Indicadores de Nivel de Habilidad

Ayuda a los estudiantes a autoevaluar dónde comenzar:

```
## ¿Dónde Deberías Comenzar?

**Comienza en Etapa 1 si:**
- Nunca has [hecho esta habilidad] antes
- No puedes definir [término clave 1] o [término clave 2]
- No tienes experiencia práctica en esta área

**Comienza en Etapa 2 si:**
- Entiendes los conceptos básicos pero no los has aplicado
- Puedes [habilidad básica] pero luchas con [habilidad intermedia]
- Has completado un curso o tutorial para principiantes

**Comienza en Etapa 3 si:**
- Has estado practicando durante [X] meses
- Puedes [habilidad intermedia] independientemente
- Quieres refinar tu enfoque y construir un portafolio

**Comienza en Etapa 4 si:**
- Tienes [X] meses/años de experiencia
- Quieres dominar técnicas avanzadas o especializarte
- Te estás preparando para [certificación / cambio de carrera]
```

---

## Fase 4: Entrega de la Ruta

### Seguimiento de Progreso

```
## Rastreador de Progreso de Ruta de Aprendizaje

| Etapa | Tema | Estado | Hito | Fecha de Finalización |
|-------|-------|--------|-----------|---------------|
| 1 | [Tema 1] | ☐ No iniciado / ◐ En progreso / ☑ Completo | | |
| 1 | [Tema 2] | ☐ / ◐ / ☑ | | |
| 1 | Hito 1 | ☐ / ◐ / ☑ | [Pasar/Fallar] | |
| 2 | [Tema 3] | ☐ / ◐ / ☑ | | |
```

### Inversión de Tiempo Estimada

```
## Compromiso de Tiempo

| Etapa | Duración | Horas/Semana | Horas Totales |
|-------|----------|-----------|-------------|
| Fundación | 4 semanas | 5-8 horas | 20-32 horas |
| Habilidades Centrales | 6 semanas | 8-10 horas | 48-60 horas |
| Aplicación | 6 semanas | 10-12 horas | 60-72 horas |
| Maestría | 8 semanas | 8-10 horas | 64-80 horas |
| **Total** | **24 semanas** | | **192-244 horas** |
```

### Lista de Verificación de Ruta de Aprendizaje

- [ ] Meta final clara definida — qué el estudiante puede HACER, no solo saber
- [ ] 3-5 etapas con dificultad progresiva
- [ ] Cada etapa tiene objetivos de aprendizaje medibles
- [ ] Requisitos previos y dependencias están mapeados
- [ ] Recursos recomendados para cada tema (mezcla de gratuitos y de pago)
- [ ] Actividades prácticas incluidas en cada etapa
- [ ] Las evaluaciones de hito cierran el avance entre etapas
- [ ] Guía de autoevaluación ayuda a estudiantes encontrar su punto de inicio
- [ ] Estimaciones de tiempo son realistas para el estudiante objetivo

---

## Anti-Patrones

- **Sin estado final claro** — "aprender marketing" no es una ruta de aprendizaje. "Poder planificar y ejecutar una campaña de anuncios pagados que genere leads" es.
- **Solo teoría, sin práctica** — si cada etapa es lectura y visionado, el estudiante nunca construye habilidad real.
- **Sin hitos** — sin checkpoints, los estudiantes se estancan o avanzan sin preparación.
- **Sobrecarga de recursos** — recomendar 20 libros y 10 cursos por etapa paraliza al estudiante. Cura despiadadamente.
- **Estructura solo lineal** — algunos temas pueden aprenderse en paralelo. Muestra cuáles son secuenciales y cuáles son flexibles.
- **Sin guía "comienza aquí"** — los estudiantes experimentados no deben sentarse en conceptos básicos que ya conocen.

---

## Recuperación

- **Estudiante atascado en una etapa:** Desglosa el hito en sub-metas más pequeñas. Identifica el concepto específico causando dificultad y proporciona recursos dirigidos.
- **Los recursos se vuelven obsoletos:** Revisa y actualiza recursos recomendados trimestralmente. Reemplaza contenido deprecated o discontinuado.
- **La ruta es demasiado larga:** Ofrece una versión "carril rápido" que cubre solo lo esencial para estudiantes que necesitan ser productivos rápidamente.
- **El estudiante salta etapas y lucha:** Redirige al auto-evaluación. Recomienda completar la etapa de requisitos previos antes de continuar.
- **Múltiples secuencias válidas de aprendizaje:** Ofrece una "ruta recomendada" y una "ruta alternativa" para estudiantes con diferentes puntos de partida o prioridades.
