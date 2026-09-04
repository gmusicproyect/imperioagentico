---
name: revision-trimestral
description: "Crea documentos de revisión empresarial trimestral con análisis de métricas, seguimiento de objetivos y ajustes estratégicos. Úsalo cuando realices revisiones de desempeño empresarial de fin de trimestre."
allowed-tools: Read Write Glob
metadata:
  author: Imperio Digital
  version: "1.0"
---

# Revisión Trimestral

## Cuándo usar esta habilidad

Usa esta habilidad cuando necesites:
- Conducir una revisión empresarial trimestral estructurada
- Analizar desempeño contra objetivos y OKRs
- Identificar qué funcionó, qué no y qué ajustar
- Establecer prioridades y objetivos para el próximo trimestre

**NO** uses esta habilidad para check-ins semanales, planificación anual o reportes solo financieros. Esto es para revisiones empresariales integrales trimestrales.

---

## Principio Central

UNA REVISIÓN TRIMESTRAL NO ES UNA TARJETA DE CALIFICACIÓN — ES UNA RECALIBRACIÓN ESTRATÉGICA. EL OBJETIVO ES DECIDIR QUÉ HACER DESPUÉS, NO SOLO DOCUMENTAR QUÉ PASÓ.

---

## Fase 1: Recopila Datos

### Entradas Requeridas

| Entrada | Qué Preguntar | Predeterminado |
|---------|--------------|----------------|
| **Trimestre** | "¿Cuál trimestre estás revisando? (Q1, Q2, Q3, Q4 + año)" | Trimestre anterior |
| **Objetivos establecidos para este trimestre** | "¿Cuáles fueron tus objetivos u OKRs para este trimestre?" | Sin predeterminado — debe proporcionarse |
| **Métricas clave** | "¿Cuáles son tus métricas de negocio core? (ingresos, clientes, crecimiento, etc.)" | Ingresos, clientes, ganancia |
| **Ingresos este trimestre** | "¿Cuál fue ingresos totales este trimestre?" | Sin predeterminado — debe proporcionarse |
| **Mayores victorias** | "¿Cuáles fueron los top 3 logros este trimestre?" | Sin predeterminado — debe proporcionarse |
| **Mayores desafíos** | "¿Cuáles fueron los top 3 desafíos o fracasos?" | Sin predeterminado — debe proporcionarse |

**PUNTO DE CONTROL: No continúes sin objetivos trimestrales y resultados reales.**

---

## Fase 2: Revisión de Desempeño

```
## Revisión Empresarial Trimestral: [Q# Año]

### Tarjeta de Puntuación de Objetivo
| Objetivo | Objetivo | Real | Estado | Notas |
|----------|---------|------|--------|-------|
| [Objetivo 1] | [Objetivo] | [Real] | Logrado / Perdido / Parcial | [Contexto] |
| [Objetivo 2] | [Objetivo] | [Real] | Logrado / Perdido / Parcial | |
| [Objetivo 3] | [Objetivo] | [Real] | Logrado / Perdido / Parcial | |

**Objetivos logrados:** [X] de [X] ([X]%)

### Resumen Financiero
| Métrica | Este Trimestre | Trimestre Pasado | Cambio TT | YTD |
|---------|----------|----------|----------|-----|
| Ingresos | $[X] | $[X] | +/-[X]% | $[X] |
| Gastos | $[X] | $[X] | +/-[X]% | $[X] |
| Ganancia neta | $[X] | $[X] | +/-[X]% | $[X] |
| Margen de ganancia | [X]% | [X]% | +/-[X]% | [X]% |
| Clientes | [X] | [X] | +/-[X]% | |
| [Métrica clave] | [X] | [X] | +/-[X]% | |

### Desglose Mensual
| | Mes 1 | Mes 2 | Mes 3 | Total Trimestre |
|--|---------|---------|---------|--------------|
| Ingresos | $[X] | $[X] | $[X] | $[X] |
| Gastos | $[X] | $[X] | $[X] | $[X] |
| Ganancia neta | $[X] | $[X] | $[X] | $[X] |
```

---

## Fase 3: Análisis

### Qué Funcionó

```
## Logros e Insights

### Top 3 Logros
1. **[Logro]** — [Qué pasó, impacto cuantificado, por qué funcionó]
2. **[Logro]** — [Descripción e impacto]
3. **[Logro]** — [Descripción e impacto]

### Insights Clave
- [Insight sobre clientes, mercado u operaciones aprendido este trimestre]
- [Insight]
```

### Qué No Funcionó

```
## Desafíos y Lecciones

### Top 3 Desafíos
1. **[Desafío]** — [Qué pasó, impacto, causa raíz]
2. **[Desafío]** — [Descripción y causa raíz]
3. **[Desafío]** — [Descripción y causa raíz]

### Lecciones Aprendidas
- [Lección — ¿qué harás diferente?]
- [Lección]
```

### Preguntas Estratégicas

```
## Evaluación Estratégica

### Preguntas a Responder
1. ¿Estamos enfocados en las prioridades correctas?
2. ¿Qué deberíamos INICIAR el próximo trimestre?
3. ¿Qué deberíamos DETENER el próximo trimestre?
4. ¿Qué deberíamos CONTINUAR el próximo trimestre?
5. ¿Es nuestra estrategia actual aún la correcta dado lo que aprendimos?
```

---

## Fase 4: Plan del Próximo Trimestre

```
## Prioridades de [Próximo Trimestre]

### Top 3 Objetivos
| Objetivo | Objetivo | Métrica | Propietario | Fecha Límite |
|----------|---------|--------|------------|-------------|
| [Objetivo 1] | [Objetivo específico] | [Cómo medido] | [Quién] | [Fecha] |
| [Objetivo 2] | [Objetivo específico] | [Cómo medido] | [Quién] | [Fecha] |
| [Objetivo 3] | [Objetivo específico] | [Cómo medido] | [Quién] | [Fecha] |

### Iniciativas Clave
1. **[Iniciativa]** — [Qué, por qué, impacto esperado]
2. **[Iniciativa]** — [Qué, por qué, impacto esperado]
3. **[Iniciativa]** — [Qué, por qué, impacto esperado]

### Cambios de Asignación de Recursos
- [Cualquier cambio de presupuesto, nuevas contrataciones, cambios de herramienta o mejoras de proceso]

### Riesgos a Monitorear
- [Riesgo 1] — Mitigación: [Plan]
- [Riesgo 2] — Mitigación: [Plan]
```

---

## Ejemplo: Q4 Revisión de Consultor Solo

**Objetivos:** 1) Lograr $45K ingresos (Real: $42K — 93%), 2) Lanzar coaching grupal (Hecho — 8 inscritos), 3) Reducir concentración de cliente abajo de 40% (Perdido — cliente top aún 48%).

**Logro clave:** Coaching grupal lanzado e inmediatamente rentable en $2,400/mes recurrentes.
**Desafío clave:** Sobre-dependencia de un cliente crea riesgo. Plan para Q1: añadir 2 clientes nuevos para reducir concentración a 35%.

---

## Anti-patrones

- **Saltarse la revisión enteramente** — el trimestre termina y saltas al próximo sin reflexión. Dedica 2-3 horas a esto.
- **Solo números, sin narrativa** — métricas sin interpretación son solo datos. Explica qué impulsó los números.
- **Establecer los mismos objetivos después de perderlos** — si perdiste un objetivo, analiza por qué. Ajusta el objetivo, cambia el enfoque o remuévelo.
- **Demasiados objetivos** — máximo 3-5 objetivos por trimestre. Más que eso diluye el foco.
- **Sin mecanismo de responsabilidad** — escribe la revisión y comparte con alguien (asesor, mastermind, socio) para responsabilidad.

---

## Recuperación

- **No se establecieron objetivos el trimestre pasado:** Usa esta revisión para establecer una línea base. Establece 3 objetivos para el próximo trimestre y comprométete a revisarlos.
- **Trimestre terrible (todo perdido):** Enfócate en causas raíz, no síntomas. Un trimestre malo es un punto de datos. Dos trimestres malos es un patrón que necesita cambio estratégico.
- **Sin seguimiento financiero:** Usa extractos bancarios para reconstruir ingresos y gastos. Configura seguimiento apropiado para próximo trimestre.
- **Fundador solo sin nadie para revisar con:** Escribe la revisión de todas formas. El acto de documentar fuerza claridad. Comparte con mentor, asesor o grupo mastermind.

---

## Preguntas Frecuentes y Detalles Adicionales

### ¿Cuál es la diferencia entre una revisión trimestral y una anual?

Una revisión trimestral es más táctica y enfocada en recalibración. Una revisión anual es más estratégica y enfocada en dirección de largo plazo. Las revisiones trimestrales mantienen el barco en curso; las revisiones anuales deciden si cambiar de curso.

### ¿Cuánto tiempo debería tomar?

Planifica 2-3 horas. Recopilación de datos y reunión de números (30-45 min), escritura del análisis y narrativa (45-60 min), revisión estratégica y planificación (45-60 min).

### ¿A quién debería compartir esto?

Si eres un fundador solo, comparte con un asesor de negocios, mentor o grupo mastermind. Si tienes un equipo, facilita una sesión de revisión trimestral con los líderes clave. La revisión escrita es el documento de base; la discusión es donde ocurre el pensamiento estratégico real.

### ¿Qué hacer si no tengo métricas claras?

Comienza con lo que tienes: ingresos (desde extractos bancarios), clientes (desde lista de clientes activos), gastos (desde tarjeta de crédito o cuenta). El acto de recopilar es el primer paso. Construye sistema de seguimiento apropiado para próximo trimestre.

### ¿Y si perdí la mayoría de mis objetivos?

Esto es información valiosa. No es fallo; es feedback. Analiza por qué ocurrió: ¿objetivos poco realistas, ejecución débil, cambios del mercado o prioridades cambiantes? Una vez que entiendes el por qué, puedes ajustar los objetivos o el enfoque para Q próximo.

### ¿Debería hacer esto solo o con mi equipo?

Ambos. Si tienes equipo, comienza solo (recópila datos, piensa a través de desafíos), luego facilita sesión de revisión con equipo. Traen perspectivas que perdiste. La revisión escrita es tu síntesis; la discusión es donde todos aprenden.
