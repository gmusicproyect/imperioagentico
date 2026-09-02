# Clase 10 — Agentes & Subagentes

**Tags:** `Agentes` `Ultra` `Orquestación` `Paralelismo`
**Conecta con:** Clase 09 · Clase 11 · Clase 14

---

## Idea central

Claude Code puede orquestar múltiples agentes en paralelo. Un agente principal (orquestador) divide el trabajo y delega subtareas a agentes especializados que corren simultáneamente, reduciendo el tiempo total de ejecución.

---

## Arquitectura de agentes

```
Ultra (Orquestador)
├── Subagente A → tarea específica A
├── Subagente B → tarea específica B
└── Subagente C → tarea específica C
         ↓
   Consolida resultados
```

---

## Cuándo usar subagentes

| Escenario | ¿Usar subagentes? |
|-----------|------------------|
| Tarea lineal de 5 pasos | No — un solo agente |
| Analizar 50 leads en paralelo | Sí |
| Crear contenido para 3 plataformas a la vez | Sí |
| Ejecutar tests en múltiples entornos | Sí |

---

## Roles típicos en una arquitectura de agentes

- **Orquestador (Ultra):** divide el trabajo, asigna tareas, consolida
- **Especialista de datos:** extrae y procesa información
- **Especialista de acción:** ejecuta en servicios externos (GHL, Meta, etc.)
- **Especialista de reporte:** formatea y entrega resultados

---

## 💡 Tip

El orquestador funciona mejor con instrucciones de alto nivel. No le digas *cómo* hacer las cosas — dile *qué* resultado esperas y deja que divida el trabajo él solo.

---

## ⚠️ Error común

Crear subagentes para tareas que son naturalmente secuenciales (donde el paso 2 depende del resultado del paso 1). El paralelismo solo ayuda cuando las tareas son independientes entre sí.
