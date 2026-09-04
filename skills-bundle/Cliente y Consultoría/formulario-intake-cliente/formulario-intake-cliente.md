---
name: formulario-intake-cliente
description: "Crea formularios de intake de cliente y cuestionarios que recopilan información esencial del proyecto de manera eficiente."
allowed-tools: Read Write Glob
metadata:
  author: Imperio Digital
  version: "1.0"
---

# Formulario de Intake de Cliente

## Cuándo Usar Este Skill

Usa este skill cuando necesites:
- Crear un formulario de intake que capture información esencial del proyecto antes del kickoff
- Diseñar cuestionarios para onboarding de nuevos clientes de manera eficiente
- Reducir tiempo de llamadas de descubrimiento recopilando detalles clave por adelantado
- Estandarizar recopilación de información en todos los nuevos engagement

**NO USES** este skill para encuestas de cliente, formularios de feedback o formularios de generación de leads. Esto es para intake de proveedor de servicios — recopilar lo que necesitas para comenzar a trabajar.

---

## Principio Fundamental

UN FORMULARIO DE INTAKE EXCELENTE HACE LAS PREGUNTAS CORRECTAS EN EL ORDEN CORRECTO — REEMPLAZA UNA LLAMADA DE DESCUBRIMIENTO DE 60 MINUTOS CON UN FORMULARIO DE 10 MINUTOS QUE TE DA MEJOR INFORMACIÓN.

---

## Fase 1: Requisitos de Formulario

### Información Requerida

| Información | Qué Preguntar | Valor por Defecto |
|-------|------------|---------|
| **Tipo de servicio** | "¿Qué servicio entregarás después de recopilar esta info?" | Sin valor por defecto — debe proporcionarse |
| **Información crítica** | "¿Qué debes saber antes de comenzar a trabajar?" | Sin valor por defecto — debe proporcionarse |
| **Tipo de cliente** | "¿Quién completa esto — dueños de negocio, gerentes de marketing, individuos?" | Dueños de negocio |
| **Objetivo de longitud del formulario** | "¿Cuánto debe tomar esto en completar?" | 10-15 minutos |
| **Método de entrega** | "¿Dónde vivirá este formulario — Google Forms, Typeform, PDF, email?" | Google Forms o Typeform |

**PUNTO DE CONTROL: Confirma tipo de servicio e información crítica antes de diseñar el formulario.**

---

## Fase 2: Estructura del Formulario

### Marco de Secciones

Organiza preguntas en secciones lógicas:

```
## Formulario de Intake de Cliente — [Nombre de Servicio]

### Sección 1: Sobre Ti
- Nombre de negocio
- Tu nombre y rol
- URL del sitio web
- Industria/nicho

### Sección 2: Tus Objetivos
- ¿Cuál es el objetivo principal de este proyecto?
- ¿Qué éxito se ve para ti?
- ¿Hay una fecha de plazo o lanzamiento?

### Sección 3: Situación Actual
- ¿Qué has intentado antes?
- ¿Qué está funcionando bien que deberíamos mantener?
- ¿Qué NO está funcionando que sugirió este proyecto?

### Sección 4: Específicos del Proyecto
- [Preguntas específicas del servicio — ver plantillas abajo]
- [Preguntas que definen alcance]
- [Preguntas de preferencia o estilo]

### Sección 5: Logística
- Rango de presupuesto (proporciona niveles, no abierto)
- Preferencia de cronograma
- Método de comunicación preferido
- ¿Cómo nos encontraste?
```

### Reglas de Diseño de Preguntas

1. **Usa preguntas cerradas para hechos** — opción múltiple, dropdowns, sí/no
2. **Usa preguntas abiertas para contexto** — limita a 3-5 por formulario
3. **Proporciona ejemplos** — "Describe tu audiencia objetivo (ej. mujeres 25-40 que compran skincare en línea)"
4. **Haz campos críticos requeridos** — mantén campos opcionales para info agradable
5. **Agrupa preguntas relacionadas** — no saltes entre temas aleatoriamente

---

## Fase 3: Plantillas Específicas de Servicio

### Intake de Diseño/Branding

- ¿Tienes pautas de marca existentes? (opción de upload)
- Comparte 3 sitios web o marcas cuyo estilo de diseño admiras
- ¿Qué colores, fuentes o imaginería deberíamos usar o evitar?
- ¿Quién es tu audiencia objetivo?
- ¿Dónde se usará este diseño — web, impreso, redes sociales?

### Intake de Copywriting/Contenido

- ¿Cuál es el propósito de este contenido — vender, informar, educar, entretener?
- Describe tu voz de marca en 3 adjetivos
- ¿Quién está leyendo esto? ¿Qué les importa?
- ¿Hay palabras clave o frases específicas a incluir?
- Comparte ejemplos de contenido que te gusta (URLs o uploads)

### Intake de Consultoría/Estrategia

- ¿Cuál es el mayor desafío que enfrenta tu negocio ahora?
- ¿Cuál es tu ingresos y tamaño de equipo?
- ¿Qué ya has intentado para resolver este problema?
- ¿Qué recursos (presupuesto, equipo, tiempo) están disponibles para implementación?
- ¿Qué haría este engagement un éxito en tus ojos?

### Intake de Desarrollo Web

- ¿En qué plataforma funciona tu sitio?
- ¿Qué features o funcionalidad necesitas?
- ¿Tienes contenido listo (copia, imágenes, videos)?
- ¿Cuántas páginas incluye el proyecto?
- ¿Necesitas ecommerce, booking o funcionalidad de membresía?

---

## Fase 4: Optimización de Formulario

### Consejos de Tasa de Completación

- Mantén formularios bajo 15 preguntas para mejores tasas de completación
- Usa barras de progreso para mostrar cuánto falta
- Auto-guarda respuestas para que los clientes puedan volver después
- Envía recordatorio si el formulario no se completa en 48 horas
- Agradéceles inmediatamente al envío con confirmación y próximos pasos

### Workflow Post-Envío

1. Formulario enviado — dispara email de confirmación automático
2. Revisa respuestas dentro de 24 horas
3. Señala respuestas faltantes o poco claras para seguimiento
4. Programa llamada de kickoff solo después de que el formulario es revisado
5. Referencia respuestas del formulario durante kickoff para mostrar que te preparaste

### Lista de Verificación de Formulario

- [ ] Cada pregunta sirve un propósito específico — sin relleno
- [ ] Campos requeridos limitados a información verdaderamente esencial
- [ ] Preguntas abiertas incluyen respuestas de ejemplo
- [ ] Pregunta de presupuesto usa rangos, no texto abierto
- [ ] Opción de upload de archivo incluida para assets y referencias
- [ ] Mensaje de confirmación incluye próximos pasos y cronograma
- [ ] El formulario es amigable con móviles

---

## Anti-Patrones

- **Demasiadas preguntas abiertas** — 10 cuadros de texto garantizan respuestas cortas e inútiles. Usa prompts específicos y guiados.
- **Sin pregunta de presupuesto** — preguntar sobre presupuesto temprano ahorra tiempo a todos. Usa rangos para que los clientes se sientan cómodos.
- **Preguntando info que no usarás** — cada pregunta debe conectar a una decisión que tomes durante el proyecto.
- **Sin confirmación o próximos pasos** — enviar un formulario al vacío hace que los clientes se preocupen. Cuéntales qué sucede después.
- **Duplicando la discovery call** — si aún haces las mismas preguntas en la llamada, el formulario no está funcionando.

---

## Recuperación

- **Cliente salta el formulario:** Hazlo prerequisito — "Revisaré tus respuestas antes de nuestra llamada de kickoff." Sin formulario, sin llamada.
- **Las respuestas son vagas o inútiles:** Haz seguimiento con 2-3 preguntas aclaratorias dirigidas. No reenvíes el formulario completo.
- **Cliente se queja de la longitud del formulario:** Acórta a lo absolutamente esencial y recopila el resto durante la llamada de kickoff.
- **Limitaciones de herramienta de formulario:** Usa un Google Form simple o incluso un email bien formateado con preguntas numeradas. La herramienta importa menos que las preguntas.
- **Diferentes clientes necesitan diferentes formularios:** Crea 2-3 variaciones por tipo de servicio en lugar de un formulario de talla única.
