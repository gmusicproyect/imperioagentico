---
name: ciclo-retroalimentacion-producto
description: "Diseña ciclos de feedback de producto conectando la opinión del cliente con las decisiones de producto con transparencia y comunicación. Usa cuando necesites sistematizar cómo la feedback impulsa tu roadmap."
allowed-tools: Read Write Glob
metadata:
  author: Imperio Digital
  version: "1.0"
---

# Ciclo de Feedback de Producto

## Cuándo Usar Este Skill

Usa este skill cuando necesites:
- Diseñar un sistema que conecte la feedback del cliente con las decisiones de producto
- Construir transparencia sobre cómo las opiniones de los usuarios dan forma a la roadmap
- Crear flujos de comunicación que cierren el ciclo con los clientes
- Establecer un proceso repetible para recolectar, priorizar y actuar sobre la feedback

**NO** uses este skill para dashboards de solicitud de funcionalidades (usa sistema-solicitud-caracteristicas), planes de investigación de usuario o diseño de encuestas NPS. Esto es para el ciclo completo de feedback-a-decisión.

---

## Principio Fundamental

UN CICLO DE RETROALIMENTACIÓN SOLO ES UN CICLO SI LA INFORMACIÓN REGRESA AL CLIENTE — RECOLECTAR RETROALIMENTACIÓN SIN CERRAR EL CICLO ENTRENA A LOS USUARIOS A DEJAR DE COMPARTIR.

---

## Fase 1: Brief

### Información Requerida

| Dato | Qué Preguntar | Valor por Defecto |
|------|--------------|-------------------|
| **Producto** | "¿Para qué producto es este ciclo de feedback?" | Sin valor por defecto — debe proporcionarse |
| **Volumen de feedback** | "¿Cuántas piezas de feedback recibes mensualmente?" | Menos de 100 |
| **Proceso actual** | "¿Cómo manejas la feedback hoy?" | Ad hoc / sin sistema |
| **Tomadores de decisión** | "¿Quién decide qué se construye?" | Fundador solo |
| **Brecha de comunicación** | "¿Los clientes saben cuándo su feedback influye una decisión?" | No |

**PUNTO DE CONTROL: Confirma el brief antes de diseñar el ciclo.**

---

## Fase 2: Diseñar el Ciclo

### El Ciclo de Feedback en Cuatro Etapas

```
RECOLECTAR → ANALIZAR → ACTUAR → COMUNICAR
   ↑                                         |
   └─────────────────────────────────────────┘
```

**Etapa 1: Recolectar** — Reúne feedback de todos los canales en un solo sistema
**Etapa 2: Analizar** — Etiqueta, categoriza e identifica patrones
**Etapa 3: Actuar** — Prioriza y decide qué construir, mejorar o ignorar
**Etapa 4: Comunicar** — Dile a los clientes qué pasó con su feedback

### Mapa de Canales de Recolección

| Canal | Tipo | Método de Captura |
|-------|------|------------------|
| Widget en la app | Reactivo | Auto-registrado al sistema central |
| Tickets de soporte | Reactivo | Equipo de CS etiqueta ítems de feedback |
| Encuestas NPS/CSAT | Proactivo | Programadas trimestralmente |
| Entrevistas de usuario | Proactivo | Mensual con 3-5 usuarios |
| Redes sociales | Reactivo | Captura manual, revisión semanal |
| Llamadas de ventas | Reactivo | Notas del CRM etiquetadas como feedback |
| Sitios de reseñas | Reactivo | Monitoreo semanal |

**PUNTO DE CONTROL: Confirma el diseño del ciclo y los canales antes de construir el sistema.**

---

## Fase 3: Construir el Sistema

### Taxonomía de Etiquetado

Cada pieza de feedback se etiqueta con:
- **Categoría:** Área funcional (facturación, onboarding, reportes, etc.)
- **Tipo:** Bug, solicitud de funcionalidad, problema de UX, elogio, queja
- **Sentimiento:** Positivo, neutral, negativo
- **Impacto:** Riesgo de ingresos, riesgo de retención, oportunidad de crecimiento
- **Fuente:** Canal de donde provino

### Cadencia de Análisis

| Frecuencia | Actividad |
|-----------|----------|
| Diaria | Triaje de feedback entrante (etiquetar y categorizar) |
| Semanal | Revisión de patrones y temas emergentes |
| Mensual | Sesión de priorización — decidir sobre qué actuar |
| Trimestral | Análisis de tendencias y alineación con roadmap |

### Marco de Decisión

Para cada tema de feedback, responde:
1. ¿Cuántos usuarios mencionaron esto? (Volumen)
2. ¿Cómo impacta los ingresos o la retención? (Impacto al negocio)
3. ¿Qué tan difícil es abordarlo? (Esfuerzo)
4. ¿Se alinea con la visión del producto? (Ajuste estratégico)

Puntúa y prioriza usando una matriz simple:
- **Alto volumen + alto impacto + bajo esfuerzo** = Hacer ahora
- **Alto volumen + alto impacto + alto esfuerzo** = Planear para el próximo trimestre
- **Bajo volumen + bajo impacto** = Reconocer y diferir
- **Conflicto con la visión** = Rechazar con explicación

### Plantillas de Comunicación

**Feedback recibida:**
"Gracias por compartir esto. Lo hemos registrado y será revisado en nuestra próxima sesión de priorización."

**Feedback en desarrollo:**
"Pediste [funcionalidad]. La estamos construyendo ahora y esperamos lanzarla para [plazo]. Te avisaremos cuando esté en vivo."

**Feedback implementada:**
"Pediste, lo construimos. [Funcionalidad] ya está en vivo. Pruébala aquí: [link]. Gracias por ayudarnos a mejorar [Producto]."

**Feedback rechazada:**
"Revisamos tu sugerencia para [funcionalidad]. Después de una consideración cuidadosa, decidimos no implementarla porque [razón]. Apreciamos que compartas y te animamos a seguir enviando ideas."

---

## Fase 4: Pulir

### 1. Prácticas de Transparencia

- Publica un resumen mensual de "Lo que escuchamos" (blog o email)
- Muestra una roadmap pública con etiquetas de "Inspirado por tu feedback"
- Etiqueta las entradas del changelog que vinieron de feedback de usuarios
- Comparte estadísticas agregadas de feedback: "Revisamos 147 piezas de feedback este mes"

### 2. Métricas de Salud del Ciclo

```
## Métricas de Salud del Ciclo

- **Tasa de recolección:** Piezas de feedback por mes (tendencia ascendente = bueno)
- **Tiempo de respuesta:** Tiempo promedio para reconocer la feedback
- **Tasa de cierre:** % de ítems de feedback con un estado final (construido, rechazado, diferido)
- **Tasa de acción:** % de feedback que influenció una decisión de producto
- **Satisfacción del cliente con el proceso de feedback:** Encuesta anual
```

### 3. Checklist de Calidad

```
## Checklist del Ciclo de Feedback

- [ ] Todos los canales de feedback alimentan un sistema central
- [ ] La taxonomía de etiquetado está documentada y se aplica consistentemente
- [ ] La revisión semanal de patrones está en el calendario
- [ ] La sesión mensual de priorización está agendada
- [ ] Existen plantillas de comunicación para recibida, en desarrollo, implementada y rechazada
- [ ] Los clientes reciben respuesta sobre su feedback dentro de un día hábil
- [ ] Existe un mecanismo de transparencia pública (roadmap, blog, etiquetas de changelog)
- [ ] Las métricas de salud del ciclo se rastrean mensualmente
- [ ] La feedback rechazada incluye una razón (nunca solo silencio)
- [ ] La feedback implementada se celebra y se atribuye
```

---

## Ejemplo

**Extracto de email mensual "Lo que Escuchamos":**
"Este mes, revisamos 83 piezas de feedback de 47 usuarios únicos. El tema principal fue personalización de facturas — 12 de ustedes pidieron personal brandizada en las facturas. Lo estamos agregando al lanzamiento de marzo. El segundo ítem más solicitado fue acciones masivas en el panel. Eso ahora está en nuestro plan del Q2. Tres solicitudes de integración con Xero fueron rechazadas por ahora — nos estamos enfocando en profundizar QuickBooks antes de agregar nuevas integraciones."

---

## Anti-Patrones

- **Recolectar sin responder** — la forma más rápida de matar la feedback es ignorarla. Reconoce todo, aunque sea brevemente.
- **Construir todo lo solicitado** — la feedback informa decisiones; no las toma. Todavía necesitas dirección estratégica.
- **Sesgo de canal único** — si solo lees tickets de soporte, solo escuchas a usuarios frustrados. Diversifica los canales de recolección.
- **Sin ruta de rechazo** — no decir nada sobre solicitudes rechazadas es peor que decir no. Siempre cierra el ciclo.
- **Acumular feedback** — sentarse sobre meses de feedback sin revisar crea un backlog que se vuelve inútil. Procesa semanalmente.

---

## Recuperación

- **Abrumado por el volumen de feedback:** Automatiza el etiquetado donde sea posible. Enfoca la revisión semanal en los 10 temas principales, no en cada ítem individual.
- **Los usuarios no dan feedback:** Hazlo más fácil — reduce el formulario a un campo. Solicita proactivamente durante interacciones de soporte.
- **La feedback es mayormente quejas:** Solicita activamente feedback positiva también. Pregunta qué aman los usuarios, no solo qué está roto.
- **El equipo ignora los datos de feedback:** Vincula los temas de feedback a métricas de ingresos y retención. El impacto al negocio obtiene atención.
