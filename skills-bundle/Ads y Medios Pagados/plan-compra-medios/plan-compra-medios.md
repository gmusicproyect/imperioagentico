---
name: plan-compra-medios
description: "Planifica presupuestos de medios pagados en canales con estrategia de asignación, ROAS esperado, y roadmap de pruebas. Úsalo cuando manejes gasto en ad en múltiples plataformas."
allowed-tools: Read Write Glob
metadata:
  author: Imperio Digital
  version: "1.0"
---

# Plan de Compra de Medios

## Cuándo Usar Este Skill

Usa este skill cuando necesites:
- Asignar presupuesto publicitario en múltiples canales pagados
- Construir estrategia de compra de medios con ROAS esperado y KPI targets
- Crear roadmap de pruebas para canales y campañas nuevas
- Planear gasto mensual y trimestral con hitos de desempeño

---

## Principio Fundamental

CADA DÓLAR DE GASTO EN AD DEBE TENER UN TRABAJO — BIEN PRUEBAS UN CANAL NUEVO, ESCALA UNO PROBADO, O RETARGETEA AUDIENCIAS WARM, SIN PRESUPUESTO DEBE SER GASTADO SIN RESULTADO ESPERADO CLARO Y PLAN DE MEDICIÓN.

---

## Fase 1: Brief

### Inputs Requeridos

| Input | Qué Preguntar | Default |
|-------|---------------|---------|
| **Presupuesto mensual total** | "¿Cuál es tu presupuesto mensual total de publicidad?" | Sin default — debe ser proporcionado |
| **Modelo de negocio** | "¿Cómo haces dinero? (e-commerce, servicios, SaaS, productos info)" | Sin default — debe ser proporcionado |
| **AOV / Tamaño de trato** | "¿Cuál es el valor promedio de venta?" | Sin default — debe ser proporcionado |
| **Target CPA** | "¿Cuánto puedes permitirte gastar para adquirir un cliente?" | Derivado de márgenes |
| **Canales actuales** | "¿Dónde estás publicitando ahora? ¿Qué resultados?" | Ninguno / comenzando desde cero |
| **Customer LTV** | "¿Cuál es lo que vale un cliente durante su vida?" | Valor de compra única |
| **Objetivos** | "¿Cuáles son tus objetivos mensuales de ingresos o leads de ads?" | Sin default — debe ser proporcionado |

---

## Fase 2: Estrategia de Canales

### Framework de Asignación de Presupuesto

```
## Asignación de Presupuesto: $[X]/mes

**Canales Probados (60-70% del presupuesto):**
- [Canal 1]: $[X]/mes ([X]% del presupuesto)
- [Canal 2]: $[X]/mes ([X]% del presupuesto)

**Canales de Prueba (15-20% del presupuesto):**
- [Canal 3]: $[X]/mes ([X]% del presupuesto)

**Retargeting (15-20% del presupuesto):**
- Retargeting Meta: $[X]/mes
- Retargeting Google: $[X]/mes

**Reserva (5-10%):**
- $[X]/mes set aside
```

---

## Fase 3: Roadmap del Plan de Medios

### Plan Mensual de Medios

**Mes 1: Fundación**
- Objetivo: Establecer desempeño baseline en canales primarios
- Presupuesto: $[X]
- Criterio de éxito: ROAS positivo en al menos una campaña

**Mes 2: Optimiza y Prueba**
- Objetivo: Escala ganadores, mata perdedores, prueba un canal nuevo
- Acciones: Escala 30% en campañas que alcanzan target CPA, pausa con 2x+ target CPA, prueba nuevo canal con $[X]

**Mes 3: Escala**
- Objetivo: Dobla abajo en canales probados, expande audiencias
- Presupuesto: $[X] (aumenta si Mes 2 fue rentable)

---

## Anti-Patrones

- **Esparcir presupuesto demasiado fino** — $100/mes en 5 canales significa ninguno obtiene suficientes datos para optimizar
- **Sin presupuesto de pruebas** — gastar 100% en canales probados significa nunca descubres qué más funciona
- **Escalar demasiado rápido** — duplicar presupuesto durante la noche resetea el aprendizaje del algoritmo
- **Sin target CPA** — gastar sin objetivo CPA definido lo hace imposible saber si ads funcionan
- **Ignorar atribución** — entiende cómo mides resultados

---

## Recuperación

- **Presupuesto muy pequeño (bajo $500/mes):** Elige UN canal. Meta para B2C, Google Search para B2B alto-intención
- **Gastando sin tracking de ROAS:** Configura tracking de conversión inmediatamente
- **Todos los canales no rentables:** Verifica oferta y landing page antes de culpar ads
- **Sin datos históricos:** Comienza con benchmarks de industria, ajusta basándote en datos reales dentro de 30 días
