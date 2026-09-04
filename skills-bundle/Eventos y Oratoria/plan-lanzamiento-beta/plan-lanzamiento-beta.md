---
name: plan-lanzamiento-beta
description: "Planifica lanzamientos beta con reclutamiento de usuarios, recopilación de comentarios, reporte de bugs y ciclos de iteración. Úsalo cuando te prepares para lanzar un producto o característica en beta."
allowed-tools: Read Write Glob
metadata:
  author: Imperio Digital
  version: "1.0"
---

# Launch Plan Beta

## Cuándo Usar Este Skill

Usa este skill cuando necesites:
- Planificar un lanzamiento beta estructurado para un nuevo producto o característica principal
- Diseñar reclutamiento de usuarios y criterios de selección para probadores beta
- Construir sistemas de recopilación de comentarios y reporte de bugs
- Definir criterios de éxito para graduarse de beta a disponibilidad general

**NO** uses este skill para lanzamientos de producto completo, planes de prueba alfa/interna o planes de prueba QA. Esto es solo para planificación de lanzamiento beta externo.

---

## Principio Fundamental

UN BETA NO ES UN LANZAMIENTO SUAVE — ES UN PERÍODO DE APRENDIZAJE ESTRUCTURADO CON OBJETIVOS DEFINIDOS, USUARIOS SELECCIONADOS Y CRITERIOS DE SALIDA CLAROS.

---

## Fase 1: Brief

### Inputs Requeridos

| Input | Qué Preguntar | Predeterminado |
|-------|------------|---------|
| **Producto/característica** | "¿Qué estás lanzando en beta?" | Sin predeterminado — debe proporcionarse |
| **Objetivos beta** | "¿Qué necesitas aprender de este beta? ¿Validar demanda, encontrar bugs, probar UX?" | Validar workflow central e identificar bugs críticos |
| **Tamaño beta objetivo** | "¿Cuántos usuarios beta deseas?" | 20-50 usuarios |
| **Duración beta** | "¿Cuánto tiempo debe ejecutarse el beta?" | 4 semanas |
| **Usuario beta ideal** | "Describe tu probador beta ideal — rol, comodidad tecnológica, caso de uso." | Adoptante temprano, tolerante con bugs, dispuesto a dar comentarios |
| **Riesgos conocidos** | "¿Qué te preocupa más?" | Funcionalidad central rompiéndose bajo uso real |

**PUNTO DE CONTROL:** Confirma el brief antes de construir el plan.

---

## Fase 2: Plan

### Cronograma Beta

```
## Cronograma Beta

**Semana -2 a -1: Pre-Lanzamiento**
- Finalizar criterios beta y métricas de éxito
- Construir sistema de recopilación de comentarios
- Reclutar y seleccionar usuarios beta
- Preparar materiales de bienvenida

**Semana 1: Lanzamiento Controlado**
- Incorporar primera cohort (50% del total)
- Monitoreo diario de problemas críticos
- Primer check-in de comentarios (Día 3)

**Semana 2: Expandir**
- Incorporar usuarios beta restantes
- Primera iteración basada en comentarios de Semana 1
- Encuesta de comentarios estructurada

**Semana 3-4: Iterar y Evaluar**
- Enviar correcciones y mejoras
- Encuesta de comentarios final
- Evaluar contra criterios de éxito
- Decisión: enviar, extender o pivotear
```

### Criterios de Éxito

Define criterios de salida medibles:

| Métrica | Objetivo | Medición |
|--------|--------|-------------|
| Bugs críticos | 0 sin resolver | Rastreador de bugs |
| Tasa de finalización de tareas | 80%+ | Prueba de usuario |
| Puntuación NPS | 30+ | Encuesta |
| Uso activo | 60%+ de usuarios beta comprometidos semanalmente | Analytics |
| Sentimiento de comentarios | Principalmente positivo | Revisión cualitativa |

**PUNTO DE CONTROL:** Confirma cronograma y criterios de éxito antes de diseñar sistemas de reclutamiento y comentarios.

---

## Fase 3: Ejecutar

### Reclutamiento de Usuarios Beta

**Campos del formulario de solicitud:**
- Nombre y correo electrónico
- Rol y tamaño de empresa
- Workflow actual para el problema que el producto resuelve
- Por qué deseas unirte al beta
- Disponibilidad para comentarios (encuesta, llamada, asincrónico)

**Criterios de selección:**
- Representa el perfil de cliente objetivo
- Tiene el problema que el producto resuelve
- Dispuesto a comprometerse con el cronograma de comentarios
- Mezcla de usuarios con conocimiento técnico y usuarios promedio

**Canales de reclutamiento:**
- Anuncio de lista de correo electrónico
- Post en redes sociales
- Base de clientes existente
- Post en comunidad o foro

### Sistema de Recopilación de Comentarios

**Comentarios estructurados:**
- Encuesta semanal (máximo 5 preguntas, tarda menos de 3 minutos)
- Encuesta de fin de beta (10 preguntas, completa)
- Opcional: llamada de comentarios de 15 minutos con 5-10 usuarios

**Comentarios no estructurados:**
- Widget de comentarios en la aplicación (captura de pantalla + texto)
- Canal dedicado de Slack o hilo de correo electrónico
- Formulario de reporte de bugs (pasos para reproducir, comportamiento esperado vs. real)

**Plantilla de Reporte de Bugs:**
```
**Qué sucedió:**
**Qué esperabas:**
**Pasos para reproducir:**
1.
2.
3.
**Captura de pantalla (si aplica):**
**Dispositivo/navegador:**
```

### Plan de Comunicación

- **Email de bienvenida:** Qué esperar, cómo reportar problemas, cronograma de comentarios
- **Actualización semanal:** Qué se corrigió, en qué se está trabajando, qué probar a continuación
- **Email de agradecimiento:** Apreciación de fin de beta, qué viene después, oferta de acceso temprano o descuento

---

## Fase 4: Pulir

### 1. Marco de Decisión Beta-a-Lanzamiento

```
## Criterios Ir/No-Ir

**Enviar a GA si:**
- [ ] Todos los bugs críticos resueltos
- [ ] Tasa de finalización de tareas superior a 80%
- [ ] NPS es 30 o superior
- [ ] Sin pérdida de datos o problemas de seguridad
- [ ] Flujo de incorporación funciona sin asistencia

**Extender beta si:**
- [ ] 1-2 problemas críticos permanecen pero son solucionables en 1-2 semanas
- [ ] Uso es fuerte pero comentarios revelan confusión de UX
- [ ] Necesita más datos para validar un supuesto clave

**Pivotar o eliminar si:**
- [ ] Propuesta de valor central no es validada
- [ ] Usuarios beta no están usando el producto a pesar de recordatorios
- [ ] Limitación técnica crítica no puede resolverse
```

### 2. Apreciación de Usuario Beta

- Acceso temprano al producto completo
- Precios de usuario fundador o descuento de por vida
- Reconocimiento público (con permiso) en materiales de lanzamiento
- Acceso prioritario a futuros betas

### 3. Lista de Verificación de Calidad

```
## Lista de Verificación de Lanzamiento Beta

- [ ] Criterios de éxito definidos con objetivos medibles
- [ ] Formulario de solicitud de usuario beta está vivo
- [ ] Criterios de selección documentados
- [ ] Sistema de recopilación de comentarios configurado (encuesta, widget, formulario de bugs)
- [ ] Email de bienvenida redactado y programado
- [ ] Plantilla de actualización semanal creada
- [ ] Plantilla de reporte de bugs proporcionada a todos los usuarios beta
- [ ] Marco de decisión ir/no-ir acordado
- [ ] Plan de apreciación beta definido
- [ ] Cronograma tiene inicio claro, puntos de control y fecha de finalización
```

---

## Ejemplo

**Producto:** Tomador de notas de reunión impulsado por IA para solopreneurs
**Tamaño beta:** 30 usuarios, 4 semanas

**Fragmento de email de bienvenida:**
"Eres una de 30 personas probando MeetingMind antes que nadie. Durante las próximas 4 semanas, úsalo en tus reuniones reales. Las cosas se romperán — ese es el punto. Reporta bugs con el botón rojo en la esquina inferior derecha. Cada viernes, recibirás una encuesta de 3 preguntas. Tu comentario forma directamente lo que enviamos."

**Encuesta semanal:**
1. ¿Cuántas reuniones usaste MeetingMind esta semana? (número)
2. ¿Algo se rompió o se sintió confuso? (texto)
3. En una escala de 1-10, ¿qué tan útil fue MeetingMind esta semana? (escala)

---

## Anti-Patrones

- **Demasiados usuarios beta** — 200 usuarios beta para un fundador solo significa 200 fuentes de comentarios que no puedes procesar. Comienza con 20-50.
- **Sin criterios de éxito** — sin criterios de salida, beta se ejecuta indefinidamente. Define qué "hecho" significa de antemano.
- **Ignorar comentarios** — recopilar comentarios sin actuar sobre ellos destruye la confianza del usuario beta. Cierra el bucle cada semana.
- **Sin cadencia de comunicación** — usuarios beta que no escuchan nada asumen que el producto está muerto. Las actualizaciones semanales son obligatorias.
- **Tratar beta como marketing gratuito** — beta es para aprender, no para crecer. Optimiza para calidad de comentarios, no conteo de usuarios.

---

## Recuperación

- **Registros beta bajos:** Reduce la barrera. Elimina el formulario de solicitud e invita directamente desde tu lista de correo electrónico o seguidores sociales.
- **Usuarios beta no proporcionando comentarios:** Acorta encuestas a 2 preguntas. Ofrece un pequeño incentivo (tarjeta de regalo, prueba extendida).
- **Demasiados bugs para manejar:** Triage sin piedad. Corrige crítico (pérdida de datos, bloqueos) primero. Reconoce problemas no críticos y cronométralos.
- **Beta necesita extender:** Comunica de manera transparente. Dile a los usuarios por qué, qué cambió y el nuevo cronograma.
