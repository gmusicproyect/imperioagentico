---
name: mapa-ruta-producto
description: "Crea roadmaps de producto en Notion con milestones, prioridades de features, timelines de release y tracking de estado. Úsalo cuando necesites planificar desarrollo de producto, comunicar un roadmap a stakeholders o priorizar features para releases próximos."
allowed-tools: Read Write Glob
metadata:
  author: "Imperio Digital"
  version: "1.0"
---

# Mapa de Ruta de Producto

## Cuándo Usar Este Skill

Usa este skill cuando necesites:
- Construir una base de datos de roadmap de producto en Notion para planificar features, milestones y releases
- Priorizar un backlog de ideas de features usando ICE scoring o MoSCoW
- Comunicar un timeline de desarrollo a stakeholders, inversores o miembros del equipo
- Reemplazar un proceso de planificación de productos basado en spreadsheet, Trello o whiteboard

**NO** uses este skill para:
- Gestión de tareas de proyecto con to-dos diarios (usa project-tracker en su lugar)
- Tracking de bugs o gestión de issues (esquema y workflow diferentes)
- Gestión de portfolio empresarial entre docenas de productos (demasiado complejo para una sola base de datos)

---

## Referencia Rápida

| Feature | Detalles |
|---------|---------|
| Propiedades | 12 fields por registro de feature |
| Priorización | ICE scoring (defecto) o framework MoSCoW |
| Etapas de estado | 6 (Backlog > Planned > In Progress > Testing > Shipped > Deferred) |
| Timeframes | 4 horizontes (Now, Next, Later, Icebox) |
| Vistas de base de datos | 4 vistas filtradas |
| Seeding | Importación en bulk desde lista de features o brief de producto |

## Esquema de Base de Datos

| Propiedad | Tipo | Opciones/Defecto |
|----------|------|-----------------|
| Nombre de Feature | Title | Requerido |
| Descripción | Rich text | Vacío |
| Prioridad | Select | Must Have (rojo), Should Have (naranja), Could Have (amarillo), Won't Have (gris) |
| Estado | Select | Backlog (gris), Planned (azul), In Progress (púrpura), Testing (naranja), Shipped (verde), Deferred (rojo) |
| Quarter/Phase | Select | Now (verde), Next (azul), Later (amarillo), Icebox (gris) |
| Effort | Select | XS (gris), Small (verde), Medium (amarillo), Large (naranja), XL (rojo) |
| Impact | Number | Escala 1-10 |
| Confidence | Number | Escala 1-10 |
| Ease | Number | Escala 1-10 |
| Owner | Rich text | Vacío |
| Category | Select | Core (azul), Growth (verde), Monetization (púrpura), Infrastructure (gris), UX/Design (rosa), Integrations (naranja) |
| Dependencies | Rich text | Vacío |

### Flujo de Estado

| Estado | Significado | Acción |
|--------|---------|--------|
| Backlog | Idea capturada, sin timeline | Score con ICE, asigna prioridad |
| Planned | Comprometido para un quarter | Asigna owner, refina descripción |
| In Progress | Activamente siendo construido | Owner proporciona actualizaciones de progreso |
| Testing | Construido, bajo QA o beta | Testers proporciona feedback dentro de 5 días |
| Shipped | Live y disponible para usuarios | Marca release date en Description |
| Deferred | Intencionalmente pospuesto | Log razón, revisita próximo quarter |

### Dimensionamiento de Effort

XS = menos de 1 día | Small = 1-3 días | Medium = 1-2 semanas | Large = 3-4 semanas | XL = 5+ semanas

---

## Framework de ICE Scoring

MÉTODO DE PRIORIZACIÓN POR DEFECTO. Usa ICE a menos que el usuario explícitamente requiera solo MoSCoW.

**ICE Score = (Impact x Confidence x Ease) / 10**

| Dimensión | Pregunta | Escala |
|-----------|----------|-------|
| Impact | ¿Cuánto mueve la aguja en revenue, retention o satisfaction? | 1 (mínimo) a 10 (transformativo) |
| Confidence | ¿Cuán seguros estamos de que esto entregará el impacto esperado? | 1 (puro guess) a 10 (validado con datos) |
| Ease | ¿Cuán fácil es implementar esto con recursos actuales? | 1 (esfuerzo masivo) a 10 (trivial de ship) |

| Rango ICE | Acción |
|-----------|--------|
| 50-100 | Prioriza inmediatamente; move a Now |
| 25-49 | Planea para quarter Next |
| 10-24 | Keep en Later; refina scope |
| 1-9 | Move a Icebox; revisita cuando datos mejoren |

**Reglas de scoring:**
- Score Impact en **business outcomes**, no feature coolness. Un fix de billing que reduce churn supera una animación flashy.
- Score Confidence en **evidencia.** Customer interviews = 8-10, gut feeling = 2-3, competitor tiene = 5-6.
- Score Ease **relativo al tamaño del equipo.** Solo dev rate una feature de 2-semanas como 3; equipo de 5-personas la rata 7.
- **NUNCA des a cada feature los mismos scores.** Si todas las features score 5/5/5, el framework proporciona cero signal.

---

## Workflow Core

CADA ROADMAP DE PRODUCTO COMIENZA RECOLECTANDO DETALLES DE PRODUCTO Y CREANDO LA BASE DE DATOS CON EL ESQUEMA COMPLETO DE 12 PROPIEDADES ANTES DE AGREGAR CUALQUIER FEATURE -- NUNCA AGREGUES PÁGINAS A UNA BASE DE DATOS QUE ESTÁ FALTANDO PROPIEDADES.

### Fase 1: Recopila Detalles de Producto

1. **Nombre de producto** -- cómo se llama el producto
2. **Tipo de producto** -- SaaS, mobile app, web app, online course, physical product, marketplace
3. **Etapa actual** -- idea, MVP, beta, launched, scaling
4. **Página padre en Notion** -- dónde debe vivir el roadmap (nombre de página o URL)
5. **Lista de features** -- features conocidas, ideas o items de backlog a importar
6. **Tamaño del equipo** -- solo, small team (2-5), o team (6+); afecta Ease scoring
7. **Cadencia de release** -- semanal, biweekly, mensual, trimestral o milestone-based
8. **Audiencia de stakeholder** -- quién leerá esto (team, investors, customers, board)
9. **Categorías custom** -- áreas de producto más allá de los 6 defaults

Si el usuario proporciona solo items 1, 4 y 5, procede con todos los defaults.

### Fase 2: Prioriza Features con ICE Scoring

1. Score cada feature con Impact, Confidence, Ease (1-10 cada)
2. Calcula ICE Score: (I x C x E) / 10
3. Asigna MoSCoW Priority: ICE 50+ = Must Have, 25-49 = Should Have, 10-24 = Could Have, bajo 10 = Won't Have
4. Asigna Quarter/Phase: Must Have -> Now, Should Have -> Now/Next, Could Have -> Next/Later, Won't Have -> Icebox
5. Presenta lista scored para aprobación del usuario

### Fase 3: Analiza y Ejecuta

Crea el database en Notion, populate con features scored, y proporciona guía de uso para quarterly reviews, weekly check-ins y adiciones de nuevas ideas.

---

## Anti-Patrones

- **NO** crees la base de datos sin el esquema completo de 12-properties -- agregar properties después de que existan páginas causa alignment issues
- **NO** saltes ICE scoring -- la priorización es el core value de un roadmap, no la lista misma
- **NO** uses fechas que impliquen compromisos a menos que el usuario confirme deadlines -- usa horizontes relativos (Now, Next, Later), no fechas de calendario
- **NO** agregues más de 20 features sin agrupar en categorías -- listas sin categorizar son backlog dumps, no roadmaps
- **NO** asignes todas las features a "Now" -- si todo es Now, nada está priorizado
- **NO** des a cada feature los mismos ICE scores -- scores idénticos derrotan el framework
- **NO** saltes confirmación de página padre -- crear bajo la página equivocada es difícil de deshacer

---

## Recuperación y Troubleshooting

### Sin datos para basar proyecciones
Comienza con benchmarks de industria y tu tasa actual de adquisición. Modela desde la realidad, no desde deseos.

### Negocio sin ingresos
Construye el modelo alrededor del punto de equilibrio primero. ¿Cuántos clientes a qué precio cubre costos?

### Múltiples productos, modelo complejo
Enfócate en el stream de ingresos principal primero. Agrega streams secundarios después de que el modelo principal sea sólido.

### Usuario quiere números garantizados
Explica que los modelos son estimaciones basadas en supuestos. El valor está en entender las palancas, no en predecir números exactos.
