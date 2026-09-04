---
name: sistema-solicitud-caracteristicas
description: "Diseña sistemas de recolección y priorización de solicitudes de funciones con votación, etiquetado e integración con roadmap. Usa cuando organices la opinión del cliente en decisiones de producto."
allowed-tools: Read Write Glob
metadata:
  author: Imperio Digital
  version: "1.0"
---

# Sistema de Solicitud de Características

## Cuándo Usar Este Skill

Usa este skill cuando necesites:
- Diseñar un sistema para recopilar y organizar solicitudes de funciones de clientes
- Construir un marco de priorización para evaluar solicitudes
- Crear un roadmap público o interno conectado a feedback de usuarios
- Configurar workflows de votación, etiquetado y estados para gestión de funciones

**NO** uses este skill para sistemas de seguimiento de bugs, flujos de soporte al cliente o estrategia de roadmap de producto. Esto es específicamente para el sistema de recolección y priorización de solicitudes de funciones.

---

## Principio Fundamental

UN SISTEMA DE SOLICITUD DE FUNCIONES NO ES UN BUZÓN DE SUGERENCIAS — ES UNA HERRAMIENTA DE TOMA DE DECISIONES QUE CONECTA LA VOZ DEL CLIENTE CON LAS PRIORIDADES DEL PRODUCTO CON TRANSPARENCIA.

---

## Fase 1: Brief

### Información Requerida

| Dato | Qué Preguntar | Predeterminado |
|------|---------------|----------------|
| **Tipo de producto** | "¿Cuál es el producto?" | Sin predeterminado — debe proporcionarse |
| **Volumen de solicitudes** | "¿Cuántas solicitudes de funciones recibes por mes?" | Menos de 50 |
| **Proceso actual** | "¿Cómo gestionas las solicitudes de funciones hoy?" | Email o ad hoc |
| **Público o interno** | "¿Deberían los clientes ver y votar las solicitudes, o es solo interno?" | Dashboard de votación público |
| **Tamaño del equipo** | "¿Quién revisa y prioriza las solicitudes?" | Fundador solo |
| **Herramientas existentes** | "¿Usas alguna herramienta de gestión de proyectos actualmente?" | Ninguna específica |

**PUNTO DE CONTROL: Confirma el brief antes de diseñar el sistema.**

---

## Fase 2: Diseñar el Sistema

### Canales de Recolección

Define dónde entran las solicitudes al sistema:

| Canal | Método de Captura |
|-------|------------------|
| **Widget in-app** | Botón de feedback → envío de formulario |
| **Email** | Bandeja de soporte → etiquetar y reenviar |
| **Tickets de soporte** | Equipo de CS etiqueta solicitudes de funciones |
| **Redes sociales** | Captura manual al sistema |
| **Llamadas de venta** | Nota en CRM → etiqueta de solicitud de función |
| **Dashboard público** | Envío directo del usuario |

### Plantilla de Solicitud

Cada solicitud capturada con estos campos:
- **Título:** Nombre corto y descriptivo
- **Descripción:** Qué quiere el usuario y por qué
- **Caso de uso:** El escenario específico que impulsa la solicitud
- **Info del solicitante:** Nombre, nivel de plan, valor de cuenta
- **Categoría:** Área de función (ej., facturación, reportes, integraciones)
- **Puntuación de prioridad:** Calculada (ver Fase 3)

### Flujo de Estados

```
Enviado → En Revisión → Planificado → En Progreso → Lanzado → Cerrado (No se hará)
```

**PUNTO DE CONTROL: Confirma el diseño del sistema antes de construir el marco de priorización.**

---

## Fase 3: Marco de Priorización

### Modelo de Puntuación (RICE)

| Factor | Descripción | Escala |
|--------|-------------|--------|
| **Alcance (Reach)** | ¿A cuántos usuarios afectará esto? | 1-10 (% de base de usuarios) |
| **Impacto** | ¿Cuánto mejorará su experiencia? | 1-3 (bajo/medio/alto) |
| **Confianza** | ¿Qué tan seguros estamos de que funcionará? | 50-100% |
| **Esfuerzo** | ¿Cuánto trabajo para construir? | 1-10 (días/semanas) |

**Puntuación RICE = (Alcance x Impacto x Confianza) / Esfuerzo**

### Matriz de Decisión

| Rango de Puntuación | Acción |
|---------------------|--------|
| 50+ | Priorizar para el siguiente ciclo |
| 20-49 | Planificar para ciclo futuro |
| 10-19 | Monitorear por votos adicionales |
| Menos de 10 | Reconocer y postergar |

### Reglas del Sistema de Votación

- Un voto por usuario por función
- Permitir a los usuarios agregar contexto con su voto ("Necesito esto porque...")
- Mostrar conteos de votos públicamente para generar engagement
- Clientes de alto valor (enterprise, alto MRR) pueden ponderarse internamente

---

## Fase 4: Pulir

### 1. Plantillas de Comunicación

**Solicitud recibida:**
"¡Gracias por la sugerencia! Hemos registrado tu solicitud para [función]. Puedes rastrear su estado y votar en [enlace]."

**Actualización de estado:**
"Actualización sobre tu solicitud: [función] ha pasado a 'Planificado' — lo estamos apuntando para [plazo]. Te notificaremos cuando se lance."

**Solicitud lanzada:**
"¡Buenas noticias! [función] está disponible. Tú lo pediste, nosotros lo construimos. Pruébalo: [enlace]."

**Solicitud rechazada:**
"Revisamos tu solicitud para [función] y decidimos no avanzar con ella en este momento. La razón: [razón breve]. Apreciamos la feedback y te animamos a seguir compartiendo ideas."

### 2. Integración con Roadmap

- Vincula solicitudes de funciones a ítems del roadmap
- Muestra una página pública de "en qué estamos trabajando" con 3 columnas: Planificado, En Progreso, Lanzado
- Actualiza el dashboard mensualmente como mínimo
- Celebra funciones lanzadas con mensajería "Lo pediste, lo construimos"

### 3. Lista de Verificación de Calidad

```
## Lista de Verificación del Sistema de Solicitudes

- [ ] Canales de recolección definidos (in-app, email, soporte, redes sociales)
- [ ] Plantilla de solicitud captura título, descripción, caso de uso e info del solicitante
- [ ] Flujo de estados tiene etapas claras (Enviado → Lanzado o Cerrado)
- [ ] Marco de priorización usa un modelo de puntuación (RICE o similar)
- [ ] Sistema de votación permite a los usuarios apoyar solicitudes
- [ ] Plantillas de comunicación existen para recibido, planificado, lanzado y rechazado
- [ ] Roadmap público o interno está conectado al sistema
- [ ] Cadencia de revisión mensual establecida para priorización
- [ ] Solicitudes "No se hará" se comunican con una razón
- [ ] Sistema se integra con herramientas de gestión de proyectos existentes
```

---

## Ejemplo

**Producto:** Herramienta SaaS de gestión de proyectos
**Volumen:** 30 solicitudes/mes

**Categorías del dashboard público:**
- Integraciones (Slack, Zapier, etc.)
- Reportes y Analítica
- Gestión de Tareas
- App Móvil
- Facturación y Cuenta

**Ejemplo de tarjeta de solicitud principal:**
```
## Modo Oscuro
Votos: 47 | Estado: Planificado | Categoría: UI/UX

"Agregar una opción de modo oscuro para la app web y móvil."

Comentario del votante principal: "Trabajo hasta tarde y la interfaz blanca es cegadora. Incluso un simple tema oscuro haría una gran diferencia." — Sarah K., Plan Growth
```

---

## Anti-Patrones

- **Construir todo lo que piden los usuarios** — las solicitudes populares no siempre son las prioridades correctas. Usa puntuación para balancear demanda con estrategia.
- **Feedback de agujero negro** — recopilar solicitudes sin actualizar estado destruye la confianza. Cierra el ciclo.
- **Sin camino de rechazo** — nunca decir no significa un backlog infinito. Ten un estado "No se hará" con razón.
- **Dejar que solo el conteo de votos decida** — una función con 100 votos de usuarios gratuitos puede importar menos que una solicitud de tus 5 clientes más grandes.
- **Sobrecomplicar el sistema** — una hoja de cálculo supera a una herramienta compleja que nadie usa. Comienza simple.

---

## Recuperación

- **Abrumado por el volumen de solicitudes:** Procesa por lotes semanalmente en lugar de diariamente. Agrupa solicitudes similares para reducir duplicados.
- **Sin votos en el dashboard:** Aliméntalo con solicitudes conocidas de emails de soporte. Anuncia el dashboard a usuarios existentes.
- **Solicitudes contradictorias:** Documenta las compensaciones. Presenta ambas opciones a un pequeño grupo de usuarios para feedback de desempate.
- **Usuario enojado por solicitud rechazada:** Responde personalmente. Explica el razonamiento y sugiere una solución alternativa si existe.
