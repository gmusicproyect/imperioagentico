---
name: reporte-subvención
description: "Escribe reportes de progreso y finales de subvención con seguimiento de métricas, actualizaciones narrativas y contabilidad financiera."
allowed-tools: Read Write Glob
metadata:
  author: Imperio Digital
  version: "1.0"
---

# Reporte de Subvención

## Cuándo Usar Este Skill

Utiliza este skill cuando necesites:
- Escribir un reporte de progreso o final para un financiador de subvención
- Rastrear y presentar métricas contra objetivos de subvención
- Crear actualizaciones narrativas con contabilidad financiera para cumplimiento de subvención
- Construir plantillas reutilizables de reporte de subvención para ciclos de financiamiento recurrentes

**NO** utilices este skill para solicitudes de subvención, reportes de impacto para donantes o evaluaciones de programa interno. Esto es para reportes presentados a un financiador de subvención específico para demostrar cómo se utilizaron sus fondos.

---

## Principio Fundamental

UN REPORTE DE SUBVENCIÓN DEBE PROBAR DOS COSAS: HICISTE LO QUE DIJISTE QUE HARÍAS, Y EL DINERO SE GASTÓ EXACTAMENTE COMO SE PROPUSO — LOS FINANCIADORES QUE CONFÍAN EN TU REPORTEO TE FINANCIAN DE NUEVO.

---

## Fase 1: Brief

### Entradas Requeridas

| Entrada | Qué Preguntar | Por Defecto |
|---------|--------------|------------|
| **Nombre del financiador** | "¿A qué financiador estás reportando?" | Sin valor por defecto — debe proporcionarse |
| **Propósito de subvención** | "¿Para qué se otorgó la subvención?" | Sin valor por defecto — debe proporcionarse |
| **Tipo de reporte** | "¿Reporte de progreso o reporte final?" | Reporte de progreso |
| **Período de reporte** | "¿Qué fechas cubre este reporte?" | Sin valor por defecto — debe proporcionarse |
| **Objetivos originales** | "¿Cuáles fueron los objetivos declarados en la propuesta de subvención?" | Sin valor por defecto — debe proporcionarse |
| **Plantilla del financiador** | "¿El financiador tiene un formato requerido o plantilla de reporte?" | Sin formato requerido |

**PUNTO DE CONTROL:** Confirma el brief y recopila todos los datos antes de escribir.

---

## Fase 2: Estructura

### Arquitectura de Reporte

Si no se requiere una plantilla del financiador, usa esta estructura:

```
1. Información de portada — ID de subvención, organización, período de reporte, contacto
2. Resumen ejecutivo — descripción general de 1 párrafo del progreso
3. Objetivos y resultados — cada objetivo con métricas y narrativa
4. Actividades e hitos — qué se hizo durante el período
5. Desafíos y adaptaciones — qué cambió y por qué
6. Reporte financiero — presupuesto vs. gasto real
7. Lecciones aprendidas — insights para trabajo futuro
8. Próximos pasos (reporte de progreso) o Plan de sostenibilidad (reporte final)
9. Apéndice — datos de apoyo, fotos, testimonios
```

### Tabla de Seguimiento de Objetivos

```
| Objetivo | Objetivo | Actual | % Completo | Estado |
|----------|----------|--------|-----------|--------|
| [Objetivo 1] | [Métrica objetivo] | [Real] | [%] | En camino / Atrasado / Completo |
| [Objetivo 2] | [Métrica objetivo] | [Real] | [%] | En camino / Atrasado / Completo |
```

**PUNTO DE CONTROL:** Presenta la estructura y confirma que todos los objetivos se capturan antes de escribir.

---

## Fase 3: Escribir

### Guía Sección por Sección

**Resumen Ejecutivo (100-150 palabras)**
- Propósito de subvención en una oración
- Logros clave este período
- Cualquier desafío o cambio significativo
- Evaluación general del estado

**Objetivos y Resultados**
Para cada objetivo de la propuesta original:

```
## Objetivo [N]: [Declaración de objetivo de propuesta]
**Objetivo:** [Qué se prometió]
**Progreso:** [Qué se logró, con números específicos]
**Evidencia:** [Cómo se midió]
**Narrativa:** [2-3 oraciones explicando el contexto detrás de los números]
```

**Actividades e Hitos**
```
| Actividad | Fecha Planeada | Fecha Real | Estado | Notas |
|----------|-------------|-------------|--------|-------|
| [Actividad 1] | [Fecha] | [Fecha] | Completo / En progreso / Retrasado | [Nota breve] |
```

**Desafíos y Adaptaciones**
- Declara cada desafío directamente — no ocultes problemas
- Explica qué adaptación se hizo
- Nota si la adaptación requirió un cambio al plan original
- Si se realocó presupuesto, explica y justifica

**Reporte Financiero**
```
## Resumen Financiero

| Categoría de Presupuesto | Presupuesto Aprobado | Gastado Este Período | Gastado a Fecha | Restante |
|----------------|----------------|------------------|--------------|-----------|
| Personal | $[X] | $[X] | $[X] | $[X] |
| Suministros | $[X] | $[X] | $[X] | $[X] |
| Viajes | $[X] | $[X] | $[X] | $[X] |
| Otro | $[X] | $[X] | $[X] | $[X] |
| **Total** | **$[X]** | **$[X]** | **$[X]** | **$[X]** |

**Explicaciones de variación:** [Explica cualquier categoría donde el gasto difiera del presupuesto por más de 10%]
```

---

## Fase 4: Pulir

### 1. Verificación de Cumplimiento

```
- [ ] Todos los objetivos originales se aborden (incluso si están atrasados)
- [ ] Las métricas coinciden con el plan de medición en la propuesta
- [ ] El reporte financiero contabiliza cada dólar de fondos de subvención
- [ ] Las variaciones presupuestarias mayores al 10% se explican
- [ ] Cualquier cambio de alcance o cronograma está documentado
- [ ] El reporte coincide con el formato requerido del financiador (si aplica)
- [ ] Se cumplirá la fecha límite de presentación
```

### 2. Verificación de Calidad Narrativa

- Hechos y datos, no opiniones ni lenguaje vago
- Números específicos reemplazan palabras como "muchos", "varios" o "significativo"
- Los desafíos se declaran honestamente, no se ocultan ni minimizan
- El tono es profesional y factual — no defensivo ni promocional

### 3. Paquete de Presentación

```
## Checklist de Presentación
- [ ] Reporte narrativo (Word o PDF)
- [ ] Reporte financiero (Excel o formato coincidente)
- [ ] Documentos de apoyo (fotos, testimonios, datos)
- [ ] Carta de portada (si es requerida)
- [ ] Enviado al contacto correcto en el financiador
- [ ] Copia archivada en registros de subvención de la organización
```

---

## Ejemplo 1: Reporte de Progreso de Subvención de Educación

```
Objetivo: Proporcionar tutoría a 100 estudiantes en 12 meses
Progreso (6 meses): 62 estudiantes inscritos, 45 asistiendo regularmente
Desafío: Inscripción menor a la esperada en áreas rurales
Adaptación: Añadió programa de estipendio de transporte, inscripción aumentó 30%
Presupuesto: 48% gastado en la marca del 50% — en camino
```

## Ejemplo 2: Reporte Final de Subvención de Salud Comunitaria

```
Objetivo: Conducir 500 exámenes de salud en vecindarios desatendidos
Resultado: 547 exámenes completados (109% del objetivo)
Resultado clave: 83 individuos referidos a cuidado continuo, 61 confirmaron seguimiento
Presupuesto: $49,200 de $50,000 gastados — $800 retornados al financiador
Sostenibilidad: Se asoció con 3 clínicas para acceso continuo a exámenes
```

---

## Anti-Patrones

- **Ocultar malas noticias** — los financiadores respetan la honestidad. Problemas no reportados destruyen confianza cuando se descubren después.
- **Métricas vagas** — "Ayudamos a muchas personas" es inaceptable. Usa números exactos de tu sistema de seguimiento.
- **Detalle financiero faltante** — cada dólar debe contabilizarse. Las variaciones sin explicación desencadenan auditorías.
- **Copiar-pegar la propuesta** — el reporte debería describir qué pasó, no qué planeaste hacer.
- **Presentar tarde** — reportes tardíos ponen en peligro financiamiento futuro. Construye un buffer de 1 semana antes de la fecha límite.
- **Ignorar el formato del financiador** — si proporcionan una plantilla, úsala exactamente. No sustituyas tu propio formato.

---

## Recuperación

- **Objetivos no cumplidos:** Reporta honestamente. Explica por qué, qué se aprendió y qué ajustes se hicieron. Los financiadores financian organizaciones de aprendizaje, no perfectas.
- **Registros financieros incompletos:** Reconstruye de extractos bancarios y recibos. Señala cualquier cantidad que no pudo verificarse y explica la brecha.
- **La plantilla del financiador es confusa:** Llama al oficial del programa y pide clarificación. Preferirían responder preguntas a recibir un reporte incorrecto.
- **Múltiples subvenciones con reporteo superpuesto:** Crea una hoja de cálculo de seguimiento maestro que mapee cada gasto y métrica a la subvención correcta. Nunca dobles cuentes.