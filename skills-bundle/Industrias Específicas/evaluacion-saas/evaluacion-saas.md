---
name: evaluacion-saas
description: "Evalúa herramientas SaaS para adopción empresarial con comparación de características, análisis de precios, y planificación de migración. Usar cuando se elige entre opciones de software para tu negocio."
allowed-tools: Read Write Glob
metadata:
  author: Imperio Digital
  version: "1.0"
---

# Evaluación de SaaS

## Cuándo Usar Esta Habilidad

Usa esta habilidad cuando necesites:
- Evaluar y comparar herramientas SaaS para una necesidad empresarial específica
- Crear un marco de decisión estructurado para selección de software
- Analizar precios, características, y requisitos de migración
- Documentar una decisión de selección de herramienta para referencia futura

**NO** uses esta habilidad para auditorías de stack completo (usa tool-stack-audit), construcción de software, o negociaciones de contratos de vendedor. Esto es para evaluar opciones de herramienta SaaS individual.

---

## Principio Fundamental

LA MEJOR HERRAMIENTA NO ES LA QUE TIENE LA MAYORÍA DE CARACTERÍSTICAS — ES LA QUE RESUELVE TU PROBLEMA ESPECÍFICO A UN PRECIO QUE PUEDES SOSTENER, CON LA FRICCIÓN MÍNIMA PARA ADOPTAR.

---

## Fase 1: Resumen

### Información Requerida

| Información | Qué Preguntar | Predeterminado |
|-------|------------|---------|
| **Problema a resolver** | "¿Qué problema específico intenta resolver con esta herramienta?" | Sin predeterminado — debe proporcionarse |
| **Características imprescindibles** | "¿Qué características son absolutamente requeridas? No negociables." | Sin predeterminado — lista 3-5 |
| **Características agradables** | "¿Qué características serían excelentes pero puedes vivir sin ellas?" | Sin especificar |
| **Presupuesto** | "¿Cuál es tu presupuesto mensual para esta herramienta?" | Menos de $50/mes |
| **Opciones siendo consideradas** | "¿Qué herramientas estás evaluando? Lista 2-5 opciones." | Sin predeterminado — investiga si es necesario |
| **Solución actual** | "¿Qué usas ahora, si es que algo?" | Proceso manual o hojas de cálculo |
| **Necesidades de integración** | "¿Con qué otras herramientas necesita conectar esto?" | Sin especificar |

**PUNTO DE CONTROL: Confirma el resumen antes de comenzar la evaluación.**

---

## Fase 2: Investiga y Compara

### Matriz de Comparación

| Criterios | [Herramienta A] | [Herramienta B] | [Herramienta C] |
|----------|----------|----------|----------|
| **Precio mensual** | | | |
| **Precio anual** | | | |
| **Nivel gratuito/prueba** | | | |
| **Imprescindible 1** | Sí/No/Parcial | | |
| **Imprescindible 2** | Sí/No/Parcial | | |
| **Imprescindible 3** | Sí/No/Parcial | | |
| **Agradable 1** | Sí/No | | |
| **Agradable 2** | Sí/No | | |
| **Integraciones** | | | |
| **Aplicación móvil** | Sí/No | | |
| **Acceso a API** | Sí/No | | |
| **Calidad de soporte** | | | |
| **Exportación de datos** | Sí/No | | |

### Puntuación Ponderada

Asigna pesos a cada criterio:

| Criterio | Peso | Herramienta A | Herramienta B | Herramienta C |
|----------|--------|--------|--------|--------|
| Características imprescindibles | 40% | /10 | /10 | /10 |
| Precio/valor | 25% | /10 | /10 | /10 |
| Facilidad de uso | 15% | /10 | /10 | /10 |
| Integraciones | 10% | /10 | /10 | /10 |
| Soporte y confiabilidad | 10% | /10 | /10 | /10 |
| **Total ponderado** | 100% | /10 | /10 | /10 |

### Análisis de Costo Oculto

Verifica costos más allá del precio de suscripción:
- Cuotas de configuración u onboarding
- Precios por usuario (¿cómo escala el costo con crecimiento del equipo?)
- Límites de almacenamiento de datos y cargos por exceso
- Características de complemento que deberían incluirse
- Diferencia de precios anual vs. mensual
- Requisitos de duración de contrato

**PUNTO DE CONTROL: Presenta la comparación y puntuaciones antes de hacer recomendación.**

---

## Fase 3: Recomienda

### Formato de Recomendación

```
## Recomendación: [Nombre de Herramienta]

**Por qué gana esta herramienta:**
1. [Razón principal — vinculada a características imprescindibles]
2. [Razón secundaria — vinculada a precio o integración]
3. [Razón terciaria — vinculada a facilidad de uso o soporte]

**Compromisos a aceptar:**
- [Qué esta herramienta no hace tan bien como competidores]
- [Brecha de característica que puedes vivir sin ella]

**Plan recomendado:** [Nombre de plan] en $[X]/mes
**Costo total del primer año:** $[X] (incluyendo cuotas de configuración)

**Opción de respaldo:** [Nombre de herramienta] — elige esto si [condición específica]
```

### Plan de Prueba

Antes de comprometerse, prueba la herramienta recomendada:

```
## Lista de Verificación de Prueba (7-14 días)

- [ ] Registrarse para prueba gratuita
- [ ] Completar onboarding e instalación inicial
- [ ] Realizar tus 3 casos de uso principales
- [ ] Probar integración con [herramienta conectada]
- [ ] Probar importación de datos de solución actual
- [ ] Evaluar experiencia móvil (si es relevante)
- [ ] Contactar soporte con pregunta de prueba (mide tiempo de respuesta)
- [ ] Exportar datos para confirmar que puedes irte si es necesario
```

---

## Fase 4: Pulir

### 1. Plan de Migración

```
## Plan de Migración: [Solución Antigua] → [Nueva Herramienta]

**Cronograma:** [X] semanas

**Semana 1: Configuración**
- Crear cuenta en plan recomendado
- Configurar preferencias y configuración
- Configurar integraciones

**Semana 2: Migración de Datos**
- Exportar datos de solución antigua
- Importar en nueva herramienta
- Verificar precisión de datos

**Semana 3: Transición**
- Ejecutar ambas herramientas en paralelo
- Entrenar tu equipo en nuevos workflows
- Resolver cualquier problema

**Semana 4: Cutover**
- Desactivar herramienta antigua
- Cancelar suscripción antigua (verifica ciclo de facturación)
- Confirmar que todos los workflows se ejecutan en herramienta nueva
```

### 2. Documentación de Decisión

Guarda la evaluación para referencia futura:

```
## Registro de Decisión: Selección de Herramienta [Categoría]

**Fecha:** [Fecha]
**Decisión:** Seleccionado [Herramienta] para [propósito]
**Alternativas consideradas:** [Listar]
**Factores clave:** [Top 3 razones]
**Costo:** $[X]/mes en [Plan]
**Fecha de revisión:** [6 meses a partir de ahora — reevalúa]
```

### 3. Lista de Verificación de Calidad

```
## Lista de Verificación de Evaluación de SaaS

- [ ] Problema a resolver está claramente definido
- [ ] Características imprescindibles listadas (mínimo 3-5)
- [ ] Al menos 3 herramientas comparadas lado a lado
- [ ] Matriz de comparación incluye características, precios, e integraciones
- [ ] Puntuación ponderada aplicada con justificación
- [ ] Costos ocultos identificados (configuración, excesos, escalado)
- [ ] Recomendación incluye compromisos y opción de respaldo
- [ ] Plan de prueba documentado y seguido
- [ ] Plan de migración creado para cambiar herramientas
- [ ] Decisión documentada para referencia futura
```

---

## Ejemplo

**Problema:** Necesito una herramienta de gestión de proyectos para trabajo con clientes
**Presupuesto:** $20/mes
**Imprescindibles:** Vistas orientadas al cliente, asignaciones de tareas, adjuntos de archivos

**Extracto de recomendación:**
"Selecciona Notion ($10/mes, plan Plus). Cubre todos los imprescindibles: páginas de clientes compartidas, bases de datos de tareas con asignaciones, y adjuntos de archivos. Obtiene la puntuación más alta en facilidad de uso y precio, aunque Asana gana en reportes de proyecto avanzados. Como administras menos de 10 proyectos activos, la simplicidad de Notion es un mejor ajuste que la complejidad de Asana. Reevalúa en 6 meses si el volumen de proyecto excede 20."

---

## Anti-Patrones

- **Fijación en características** — elegir la herramienta con la mayoría de características en lugar del mejor ajuste. Usarás 20% de características — enfócate en las correctas 20%.
- **Ignorar costos de salida** — si no puedes exportar tus datos, estás encerrado. Siempre verifica portabilidad de datos antes de comprometerte.
- **Saltar la prueba** — reseñas y comparaciones no son sustitutos de prueba práctica. Siempre ejecuta una prueba con tu workflow real.
- **El más barato gana** — la opción más barata que no resuelve el problema cuesta más que la herramienta correcta al precio correcto.
- **Parálisis de análisis** — comparar 10 herramientas durante 3 meses es peor que elegir una herramienta suficientemente buena y comenzar. Establece un plazo de decisión.

---

## Recuperación

- **No puedo decidir entre dos herramientas:** Ejecuta una prueba de 1 semana con cada una usando el mismo escenario de prueba. La experiencia práctica generalmente rompe el empate.
- **Herramienta recomendada está fuera de presupuesto:** Verifica si la facturación anual reduce el costo. Si aún está fuera, evalúa cuáles características imprescindibles puedes comprometer en.
- **Herramienta seleccionada pero no adoptada:** El problema generalmente es fricción de onboarding, no la herramienta. Dedica una sesión enfocada a configuración y migración.
- **La herramienta no funciona después de 30 días:** Remítete a la evaluación. Si la opción de respaldo aborda los problemas, cambia temprano antes de que más datos se acumule.
