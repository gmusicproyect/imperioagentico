---
name: medicion-impacto-social
description: "Diseña marcos de medición de impacto social con indicadores, métodos de recopilación de datos y plantillas de reporteo."
allowed-tools: Read Write Glob
metadata:
  author: Imperio Digital
  version: "1.0"
---

# Medición de Impacto Social

## Cuándo Usar Este Skill

Utiliza este skill cuando necesites:
- Diseñar un marco para medir el impacto social de programas o iniciativas
- Definir indicadores, métodos de recopilación de datos y estructuras de reporteo
- Crear un modelo lógico o teoría de cambio para seguimiento de impacto
- Construir plantillas de reporteo que comuniquen impacto a financiadores y stakeholders

**NO** utilices este skill para dashboards de KPI de negocio, cálculos de ROI financiero o medición de satisfacción del cliente. Esto es para medir impacto social, comunitario o ambiental.

---

## Principio Fundamental

MEDIR IMPACTO NO SE TRATA DE PROBAR QUE HICISTE ALGO — SE TRATA DE ENTENDER SI LO QUE HICISTE REALMENTE CAMBIÓ VIDAS, Y USAR ESE ENTENDIMIENTO PARA HACERLO MEJOR.

---

## Fase 1: Brief

### Entradas Requeridas

| Entrada | Qué Preguntar | Por Defecto |
|---------|--------------|------------|
| **Programa o iniciativa** | "¿Para qué programa estás midiendo impacto?" | Sin valor por defecto — debe proporcionarse |
| **Impacto previsto** | "¿Qué cambio estás intentando crear en el mundo?" | Sin valor por defecto — debe proporcionarse |
| **Stakeholders** | "¿Quién necesita ver estas mediciones de impacto? (financiadores, junta directiva, público)" | Financiadores y junta directiva |
| **Seguimiento actual** | "¿Qué datos estás recopilando ya?" | Mínimo o ninguno |
| **Recursos para medición** | "¿Cuánto tiempo y presupuesto puedes dedicar a recopilación de datos?" | Bajo — necesita ser ligero |

**PUNTO DE CONTROL:** Confirma el brief antes de continuar.

---

## Fase 2: Diseño de Marco

### Modelo Lógico

```
## Modelo Lógico: [Nombre del Programa]

**Entradas** → **Actividades** → **Productos** → **Resultados** → **Impacto**

**Entradas:** [Recursos invertidos — personal, dinero, materiales, tiempo]
**Actividades:** [Lo que hace el programa — entrenamientos, servicios, eventos]
**Productos:** [Productos directos — personas servidas, sesiones entregadas, materiales distribuidos]
**Resultados:** [Cambios en participantes — conocimiento ganado, comportamiento cambiado, condiciones mejoradas]
**Impacto:** [Cambio a largo plazo en la comunidad o sistema]
```

### Selección de Indicadores

Para cada resultado, define indicadores medibles:

```
| Resultado | Indicador | Fuente de Datos | Método de Recopilación | Frecuencia |
|---------|-----------|-------------|------------------|-----------|
| [Resultado 1] | [Indicador medible] | [Dónde vienen los datos] | [Encuesta, observación, registros] | [Mensual, trimestral, anual] |
| [Resultado 2] | [Indicador medible] | [Fuente] | [Método] | [Frecuencia] |
```

### Tipos de Indicadores

- **Cuantitativo:** Números, porcentajes, conteos (p. ej., "85% de participantes reportan confianza mejorada")
- **Cualitativo:** Historias, citas, observaciones (p. ej., testimonios de participantes sobre cambios de vida)
- **Adelantado:** Señales tempranas de progreso (p. ej., tasa de asistencia a taller)
- **Rezagado:** Resultados a largo plazo (p. ej., tasa de empleo 6 meses después del programa)

**PUNTO DE CONTROL:** Presenta el modelo lógico e indicadores para aprobación.

---

## Fase 3: Construir

### Herramientas de Recopilación de Datos

Para cada indicador, crea o recomienda una herramienta de recopilación:

**Encuestas:**
```
## Plantilla de Encuesta Pre/Post
Administra al inicio y fin del programa para medir cambio.

1. En una escala de 1-5, ¿cuán confiado estás en [habilidad]? (Pre y Post)
2. ¿Con qué frecuencia [comportamiento deseado]? (Pre y Post)
3. ¿Cuál es tu mayor desafío relacionado con [tema]? (Pre — preguntas abiertas)
4. ¿Qué cambió para ti como resultado de este programa? (Post — preguntas abiertas)
```

**Hojas de Seguimiento:**
```
## Seguimiento de Producto
| Fecha | Actividad | Participantes | Horas | Notas |
|------|----------|-------------|-------|-------|
```

**Guía de Entrevista:**
```
## Entrevista de Beneficiario (15 minutos)
1. ¿Cuál era tu situación antes del programa?
2. ¿Qué aprendiste o ganaste participando?
3. ¿Cómo ha cambiado tu [área específica] desde el programa?
4. ¿Qué le dirías a alguien considerando este programa?
5. ¿Qué podríamos hacer mejor?
```

### Plantilla de Reporteo

```
## Reporte de Impacto: [Período]

### Resumen
[Descripción general de un párrafo del impacto durante el período]

### Productos
| Métrica | Objetivo | Real |
|--------|--------|--------|
| Personas servidas | [X] | [Y] |
| Sesiones entregadas | [X] | [Y] |

### Resultados
| Indicador | Línea Base | Actual | Cambio |
|-----------|----------|---------|--------|
| [Indicador 1] | [X] | [Y] | [+/-Z%] |

### Historias
[1-2 historias de beneficiarios que ilustren los datos]

### Lecciones Aprendidas
[Lo que los datos te dicen sobre cómo mejorar]
```

---

## Fase 4: Pulir

### 1. Calendario de Medición

```
| Cuándo | Qué | Quién |
|------|------|-----|
| Inicio de programa | Pre-encuesta, datos basal | Personal del programa |
| Mensual | Actualización de seguimiento de producto | Personal del programa |
| Trimestral | Revisión de resultados, entrevistas de beneficiarios | Líder de impacto |
| Fin de programa | Post-encuesta, recopilación de datos final | Personal del programa |
| Anualmente | Análisis de impacto anual y reporte | Liderazgo |
```

### 2. Checklist de Calidad de Datos

```
- [ ] Datos basales se recopilan antes de que comience el programa
- [ ] Las encuestas usan preguntas validadas donde sea posible
- [ ] El tamaño de muestra es lo suficientemente grande para sacar conclusiones
- [ ] Los datos se recopilan consistentemente (mismo método, mismo tiempo)
- [ ] Los datos cualitativos complementan datos cuantitativos
- [ ] Los datos se almacenan segura y éticamente
```

### 3. Dimensionamiento Correcto del Marco

Haz coincidir el esfuerzo de medición con la capacidad organizacional:

```
**Ligero (1-2 horas/mes):** Rastrea 3-5 métricas de producto + encuesta anual
**Moderado (4-6 horas/mes):** Productos + encuestas de resultados trimestrales + entrevistas de beneficiarios
**Completo (10+ horas/mes):** Seguimiento de modelo lógico completo + grupos de comparación + datos longitudinales
```

---

## Ejemplo 1: Programa de Mentoría Juvenil

```
Modelo lógico: Mentores capacitados (entrada) → reuniones semanales (actividad) → 100 jóvenes emparejados (producto) → confianza académica mejorada (resultado) → tasa de graduación más alta (impacto)
Indicador clave: Pre/post encuesta en confianza académica (escala 1-5)
Objetivo: 80% de participantes muestran mejora de 1+ punto
```

## Ejemplo 2: Incubadora de Pequeños Negocios

```
Modelo lógico: Currículo de capacitación + mentores (entradas) → programa de 12 semanas (actividad) → 30 negocios lanzados (producto) → ingresos aumentados (resultado) → crecimiento económico comunitario (impacto)
Indicador clave: Cambio promedio de ingresos 6 meses después del programa
Objetivo: 70% de participantes aumentan ingresos 25%+
```

---

## Anti-Patrones

- **Medir solo productos** — contar personas servidas no es impacto. El impacto es si sus vidas realmente cambiaron.
- **Sobre-medir** — recopilar datos que nunca analizas desperdicia el tiempo de todos. Solo mide lo que usarás.
- **Sin línea base** — no puedes probar cambio sin saber dónde comenzaron las personas. Siempre recopila datos previos al programa.
- **Ignorar datos cualitativos** — números dicen qué pasó, historias dicen por qué importa. Necesitas ambos.
- **Sesgo de confirmación** — diseñar mediciones para probar que tu programa funciona en lugar de evaluarlo honestamente.
- **Medición única** — el impacto ocurre con el tiempo. Construye medición de seguimiento a 3, 6 y 12 meses.

---

## Recuperación

- **Sin datos basales para participantes actuales:** Comienza a recopilar ahora para cohorts futuras. Para participantes actuales, usa encuestas retrospectivas ("Pensando en antes del programa...").
- **La organización no tiene capacidad de medición:** Comienza con la opción ligera — 3 métricas de producto y una encuesta anual. Construye desde ahí.
- **Los financiadores quieren métricas específicas que no rastreas:** Sé honesto sobre lo que puedes medir ahora, comprométete a añadir métricas de prioridad de financiador, y proporciona datos cualitativos mientras tanto.
- **El impacto es difícil de atribuir a tu programa:** Reconoce factores externos honestamente. Usa datos de comparación donde sea posible y enfócate en el cambio que puedes reclamar creíblemente.