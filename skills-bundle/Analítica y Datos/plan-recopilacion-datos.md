---
name: plan-recopilacion-datos
description: "Planifica estrategias de recopilación de datos con requisitos de seguimiento, compliance de privacidad, recomendaciones de almacenamiento y pasos de implementación. Utiliza cuando estés construyendo tu infraestructura de datos empresariales."
allowed-tools: Read Write Glob
metadata:
  author: Imperio Digital
  version: "1.0"
---

# Plan de Recopilación de Datos

## Cuándo Usar Este Skill

Utiliza este skill cuando necesites:
- Planificar qué datos recopilar en tus operaciones comerciales
- Diseñar implementaciones de seguimiento para web, producto o marketing
- Asegurar que la recopilación de datos cumple con regulaciones de privacidad
- Crear un plan de arquitectura de datos para un negocio en crecimiento

**NO** utilices este skill para análisis de datos, construcción de dashboards o ingeniería de bases de datos. Esto es para planificar qué recopilar, por qué y cómo.

---

## Principio Fundamental

RECOPILA DATOS CON PROPÓSITO — CADA PUNTO DE DATOS DEBE RESPONDER UNA PREGUNTA DE NEGOCIO O IMPULSAR UNA DECISIÓN. RECOPILAR "POR SI ACASO" CREA RESPONSABILIDAD SIN VALOR.

---

## Fase 1: Brief

### Entradas Requeridas

| Entrada | Qué Preguntar | Por Defecto |
|---------|--------------|------------|
| **Tipo de negocio** | "¿Qué hace tu negocio?" | Debe proporcionarse |
| **Decisiones clave** | "¿Para qué decisiones te gustaría tener mejores datos?" | Debe proporcionarse |
| **Datos actuales** | "¿Qué datos recopila ya? ¿Dónde están almacenados?" | Mínimo — comenzando desde cero |
| **Canales** | "¿Dónde interactúas con clientes? (sitio web, app, email, redes sociales, presencial)" | Sitio web y email |
| **Requisitos de privacidad** | "¿Dónde están tus clientes? (afecta GDPR, CCPA, etc.)" | Clientes con sede en EE.UU. |
| **Recursos técnicos** | "¿Tienes un desarrollador o implementarás sin código?" | Autoimplementación sin código |

**PUNTO DE CONTROL:** Confirma el brief antes de continuar.

---

## Fase 2: Diseño

### Marco de Recopilación de Datos

Organiza por función empresarial:

1. **Datos de marketing** — fuentes de tráfico, desempeño de campañas, gasto en publicidad, conversiones
2. **Datos de producto/sitio web** — comportamiento del usuario, uso de funciones, métricas de engagement
3. **Datos de ventas** — leads, etapas del pipeline, tasas de cierre, valores de transacciones
4. **Datos de clientes** — perfiles, preferencias, historial de compras, interacciones de soporte
5. **Datos financieros** — ingresos, costos, márgenes, flujo de efectivo
6. **Datos operacionales** — tiempos de cumplimiento, tasas de error, utilización de capacidad

### Matriz de Prioridad de Datos

Para cada punto de datos, evalúa:
- **Valor:** ¿Cuánto mejora esta data las decisiones? (Alto/Medio/Bajo)
- **Esfuerzo:** ¿Qué tan difícil es recopilar? (Alto/Medio/Bajo)
- **Riesgo de privacidad:** ¿Implica datos personales? (Sí/No)

Comienza con datos de alto valor, bajo esfuerzo y bajo riesgo.

**PUNTO DE CONTROL:** Presenta el plan priorizado de recopilación de datos y espera aprobación.

---

## Fase 3: Construir

### Entregables

**1. Inventario de Recopilación de Datos**
| Punto de Datos | Fuente | Método de Recopilación | Almacenamiento | Frecuencia | Nivel de Privacidad |
|---|---|---|---|---|---|
| Vistas de página | Sitio web | GA4 | Google | Tiempo real | Bajo |
| Registros de email | Formularios | Zapier → CRM | CRM | Tiempo real | Medio |
| Ingresos | Stripe | Sincronización API | Hoja de cálculo | Diario | Alto |

**2. Guía de Implementación**
- Configuración paso a paso para cada herramienta de recopilación de datos
- Conexiones de integración (qué se alimenta en qué)
- Procedimientos de prueba para verificar que los datos fluyen

**3. Checklist de Cumplimiento de Privacidad**
- [ ] Política de privacidad actualizada para reflejar la recopilación de datos
- [ ] Banner de consentimiento de cookies implementado (si es necesario)
- [ ] Registros de procesamiento de datos documentados
- [ ] Períodos de retención de datos definidos
- [ ] Proceso de eliminación de datos de usuarios establecido
- [ ] Compartir datos con terceros divulgado

**4. Reglas de Calidad de Datos**
- Convenciones de nombres para eventos y campos
- Reglas de validación para entrada de datos
- Estrategia de deduplicación para registros de clientes
- Cronograma de auditoría regular (verificación mensual de calidad de datos)

---

## Fase 4: Pulir

### Diagrama del Data Stack

Crea un mapa simple mostrando: fuentes de datos → herramientas de recopilación → almacenamiento → herramientas de reporte.

### Roadmap de Implementación de 90 Días

- Mes 1: Seguimiento principal (analítica de sitio web, CRM básico)
- Mes 2: Atribución de marketing (UTMs, seguimiento de conversiones)
- Mes 3: Enriquecimiento de datos de clientes (seguimiento de comportamiento, segmentación)

---

## Ejemplo 1: Negocio de E-commerce

**Datos prioritarios:** Fuentes de tráfico, eventos de conversión, AOV, churn rate de carrito, historial de compras del cliente, engagement de email. Herramientas: GA4, analítica de Shopify, Klaviyo.

## Ejemplo 2: Negocio de Servicios

**Datos prioritarios:** Fuentes de leads, reservas de consulta, tasa de cierre, rentabilidad del proyecto, puntuaciones de satisfacción del cliente. Herramientas: GA4, CRM (HubSpot gratis), Google Sheets para finanzas.

---

## Anti-Patrones

- **Recopilar todo** — más datos significan más riesgo de privacidad, más costo de almacenamiento y más ruido. Sé selectivo.
- **Sin considerar privacidad** — recopilar datos personales sin consentimiento adecuado y documentación es un riesgo legal y financiero.
- **Silos de datos** — datos de clientes en 5 herramientas que no se comunican entre sí hace que el análisis sea imposible. Planifica integraciones desde el principio.
- **Sin convenciones de nombres** — `email_signup`, `EmailSignup`, `email-signup` y `signup_email` en diferentes herramientas crea caos. Estandariza.
- **Recopilar sin revisar** — datos que nadie consulta es peor que ningún dato porque crea una falsa sensación de estar basado en datos.

---

## Recuperación

- **Usuario abrumado por opciones:** Comienza con 3 puntos de datos que responden directamente su pregunta comercial más importante. Expande después.
- **Preocupaciones de privacidad paralizan la acción:** Enfócate en datos agregados, no personales primero (vistas de página, tasas de conversión). Añade recopilación de datos personales solo con mecanismos de consentimiento adecuados.
- **Sin capacidad técnica:** Recomienda herramientas sin código (Zapier, Google Forms, analítica nativa de plataforma). La mayoría de la recopilación de datos esencial requiere cero código.
- **Datos ya dispersos:** Comienza con un inventario de datos existentes y crea un plan de consolidación antes de agregar nueva recopilación.