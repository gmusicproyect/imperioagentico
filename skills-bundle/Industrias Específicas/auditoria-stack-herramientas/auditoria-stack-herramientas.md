---
name: auditoria-stack-herramientas
description: "Audita pilas de tecnología empresarial para redundancia, optimización de costos y oportunidades de integración. Usar cuando se revisa y optimiza el gasto de software empresarial."
allowed-tools: Read Write Glob
metadata:
  author: Imperio Digital
  version: "1.0"
---

# Auditoría de Stack de Herramientas

## Cuándo Usar Esta Habilidad

Usa esta habilidad cuando necesites:
- Auditar tu stack de software empresarial para identificar redundancia y desperdicio
- Identificar ahorros de costos consolidando o reemplazando herramientas
- Evaluar oportunidades de integración entre herramientas existentes
- Crear una recomendación de stack racionalizado y optimizado

**NO** uses esta habilidad para elegir una sola herramienta (usa saas-evaluation), construir workflows de automatización, o auditorías de infraestructura técnica. Esto es para revisión y optimización de stack de software empresarial.

---

## Principio Fundamental

CADA HERRAMIENTA EN TU STACK DEBE GANAR SU ASIENTO — SI NO PUEDES NOMBRAR EL PROBLEMA ESPECÍFICO QUE RESUELVE Y EL TIEMPO O DINERO QUE AHORRA, ES CANDIDATA PARA ELIMINACIÓN.

---

## Fase 1: Resumen

### Información Requerida

| Información | Qué Preguntar | Predeterminado |
|-------|------------|---------|
| **Tipo de negocio** | "¿Qué hace tu negocio?" | Sin predeterminado — debe proporcionarse |
| **Herramientas actuales** | "Enumera cada herramienta o software pagado que usas para negocios." | Sin predeterminado — debe proporcionarse |
| **Gasto mensual** | "¿Cuál es tu gasto total mensual en software?" | Desconocido — lo calcularemos |
| **Pain points** | "¿Qué te frustra de tus herramientas actuales?" | Superposición, costo, complejidad |
| **Herramientas imprescindibles** | "¿Hay herramientas innegociables? ¿Cuáles y por qué?" | Ninguna especificada |
| **Meta presupuestaria** | "¿Tienes una meta de gasto mensual que te gustaría alcanzar?" | Reducir 20-30% |

**PUNTO DE CONTROL: Confirma la lista de herramientas y objetivos antes de comenzar la auditoría.**

---

## Fase 2: Inventario y Evaluación

### Plantilla de Inventario de Herramientas

Para cada herramienta, documenta:

| Campo | Detalles |
|-------|---------|
| **Nombre de herramienta** | |
| **Categoría** | (comunicación, gestión de proyectos, marketing, finanzas, etc.) |
| **Costo mensual** | |
| **Costo anual** | |
| **Nivel de plan** | (gratuito, básico, pro, empresa) |
| **Uso principal** | (para qué la usas) |
| **Frecuencia de uso** | (diario, semanal, mensual, raramente) |
| **Integraciones** | (qué otras herramientas conecta) |
| **Usuarios** | (cuántas personas la usan) |
| **Fin de contrato** | (¿cuándo puedes cancelar?) |

### Puntuación de Evaluación

Califica cada herramienta en:

| Criterio | Puntuación 1-5 |
|-----------|-----------|
| **Esencial** — ¿Se rompería tu negocio sin esta herramienta? | |
| **Utilizada** — ¿Usas más del 50% de sus características? | |
| **Valor** — ¿El costo se justifica por el tiempo/dinero ahorrado? | |
| **Integrada** — ¿Se conecta con tus otras herramientas? | |

**Umbrales de acción:**
- Puntuación 16-20: Mantener — esencial, bien utilizada
- Puntuación 11-15: Optimizar — puede estar en el nivel incorrecto o subutilizada
- Puntuación 6-10: Reemplazar — existe una alternativa mejor o más barata
- Puntuación 1-5: Eliminar — no gana su asiento

**PUNTO DE CONTROL: Presenta el inventario calificado y obtén confirmación antes de hacer recomendaciones.**

---

## Fase 3: Recomendar

### Acciones de Optimización

Para cada herramienta, recomienda una acción:

| Acción | Cuándo Aplicar |
|--------|---------------|
| **Mantener** | Esencial, bien utilizada, buen valor |
| **Bajar de nivel** | Usando menos de lo que el plan proporciona |
| **Consolidar** | Dos herramientas hacen el mismo trabajo — elige la mejor |
| **Reemplazar** | Existe una alternativa mejor o más barata |
| **Eliminar** | No se usa lo suficiente para justificar el costo |
| **Integrar** | Conectar con otras herramientas para aumentar valor |

### Oportunidades de Consolidación

Identifica herramientas con funcionalidad superpuesta:

```
## Análisis de Superposición

**Comunicación:** Slack + Teams + email → Consolidar en uno + email
**Gestión de Proyectos:** Trello + Asana + Notion → Elige uno
**Email Marketing:** Mailchimp + ConvertKit → Elige uno
**Diseño:** Canva + Adobe → Evalúa uso, elige uno
**Almacenamiento:** Google Drive + Dropbox → Consolidar en uno
```

### Recomendaciones de Reemplazo

Para cada herramienta marcada para reemplazo:
- **Herramienta actual:** [Nombre] — $[costo]/mes
- **Reemplazo recomendado:** [Nombre] — $[costo]/mes
- **Ahorros:** $[X]/mes
- **Esfuerzo de migración:** [Bajo/Medio/Alto]
- **Compensación clave:** [Qué ganas vs. qué pierdes]

---

## Fase 4: Pulir

### 1. Resumen de Ahorros

```
## Resumen de Optimización de Stack

**Gasto mensual actual:** $[X]
**Gasto mensual optimizado:** $[Y]
**Ahorros mensuales:** $[X-Y]
**Ahorros anuales:** $[X-Y x 12]

### Cambios
| Herramienta | Acción | Antes | Después | Ahorros |
|------|--------|--------|-------|---------|
| [Herramienta 1] | Eliminar | $29/mes | $0 | $29/mes |
| [Herramienta 2] | Bajar de nivel | $49/mes | $19/mes | $30/mes |
| [Herramienta 3] | Reemplazar | $39/mes | $15/mes | $24/mes |
| **Total** | | **$[X]** | **$[Y]** | **$[Z]/mes** |
```

### 2. Plan de Migración

Para herramientas que se reemplazan o eliminan:
- Exporta todos los datos antes de cancelar
- Anota fechas de fin de contrato y requisitos de cancelación
- Secuencia cambios para evitar interrupciones en el workflow
- Permite 1-2 semanas de superposición durante transiciones

### 3. Lista de Verificación de Calidad

```
## Lista de Verificación de Auditoría de Stack de Herramientas

- [ ] Todas las herramientas pagadas inventariadas con costos y categorías
- [ ] Cada herramienta calificada en esencial, utilizada, valor, e integrada
- [ ] Herramientas superpuestas identificadas con recomendaciones de consolidación
- [ ] Herramientas de reemplazo investigadas con comparaciones de costos
- [ ] Ahorros mensuales y anuales totales calculados
- [ ] Plan de migración incluye exportación de datos y cronograma
- [ ] Fechas de fin de contrato verificadas para ventanas de cancelación
- [ ] Herramientas imprescindibles confirmadas con usuario
- [ ] Oportunidades de integración entre herramientas restantes identificadas
- [ ] Stack optimizado documentado para referencia
```

---

## Ejemplo

**Negocio:** Consultor de marketing independiente, $487/mes en herramientas

**Hallazgo de auditoría:**
"Estás pagando por Trello ($10/mes), Asana ($11/mes) y Notion ($10/mes). Los tres son herramientas de gestión de proyectos. Consolida en Notion — cubre gestión de proyectos, notas y portales de clientes. Ahorros: $21/mes."

**Resumen:**
"Gasto actual: $487/mes. Después de eliminar 3 herramientas no utilizadas, bajar de nivel 2 planes y consolidar 2 herramientas superpuestas: $312/mes. Ahorros anuales: $2,100."

---

## Anti-Patrones

- **Eliminar herramientas sin plan de reemplazo** — eliminar una herramienta antes de confirmar que el workflow puede sobrevivir sin ella causa caos.
- **Optimizar solo en costo** — una herramienta de $49/mes que ahorra 10 horas/mes vale $490 a $49/hora. No la elimines para ahorrar $49.
- **Ignorar contratos anuales** — algunas herramientas cobran tarifas de cancelación o tienen compromisos anuales. Verifica antes de recomendar eliminaciones.
- **Demasiados cambios a la vez** — migra una herramienta a la vez. Cambiar 5 herramientas en una semana garantiza confusión.
- **Olvidar herramientas gratuitas** — las herramientas gratuitas aún tienen costos (tiempo de gestión, complejidad de integración, fragmentación de datos). Inclúyelas en la auditoría.

---

## Recuperación

- **Usuario no puede enumerar todas sus herramientas:** Revisa extractos bancarios y de tarjeta de crédito para cargos de software recurrentes. Revisa marcadores del navegador e inicios de sesión de aplicaciones.
- **Usuario se opone a eliminar una herramienta:** Pídale que rastree el uso real durante 2 semanas. Los datos a menudo cambian de opinión cuando los sentimientos no lo hacen.
- **La migración rompe un workflow:** Revierte temporalmente a la herramienta antigua. Diagnostica qué se rompió y repáralo antes de migrar de nuevo.
- **Los ahorros son mínimos:** El stack puede estar ya optimizado. Enfócate en mejoras de integración y optimización de workflow en lugar de cortes de costos.
