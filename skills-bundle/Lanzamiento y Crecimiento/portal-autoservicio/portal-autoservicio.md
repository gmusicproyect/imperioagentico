---
name: portal-autoservicio
description: "Diseña estructuras de portales de autoservicio con base de conocimiento, ticketing, gestión de cuentas y bibliotecas de recursos para la independencia del cliente."
allowed-tools: Read Write Glob
metadata:
  author: Imperio Digital
  version: "1.0"
---

# Portal de Autoservicio

## Cuándo Usar Este Skill

Usa este skill cuando necesites:
- Diseñar la estructura y arquitectura de contenido de un portal de autoservicio para clientes
- Planificar secciones de base de conocimiento, ticketing, gestión de cuentas y biblioteca de recursos
- Reducir el volumen de soporte habilitando a los clientes a ayudarse a sí mismos
- Crear una arquitectura de información del portal antes de construir o configurar una plataforma

**NO** uses este skill para construir el portal técnicamente, seleccionar plataformas de software o escribir artículos de ayuda individuales. Esto es para diseñar la estructura y experiencia de usuario del portal.

---

## Principio Fundamental

UN PORTAL DE AUTOSERVICIO TIENE ÉXITO CUANDO LOS CLIENTES LO PREFIEREN SOBRE CONTACTAR SOPORTE — ESO SIGNIFICA RESPUESTAS RÁPIDAS, NAVEGACIÓN FÁCIL Y UN CAMINO CLARO A UN HUMANO CUANDO EL AUTOSERVICIO NO ES SUFICIENTE.

---

## Fase 1: Evaluación de Necesidades

Entiende qué necesitan los clientes del autoservicio.

### Información Requerida

| Dato | Qué Preguntar | Predeterminado |
|------|---------------|----------------|
| **Tipo de negocio** | "¿Qué producto o servicio ofreces?" | Sin predeterminado |
| **Volumen de soporte** | "¿Cuántas solicitudes de soporte manejas por mes?" | 20-50 |
| **Principales necesidades de autoservicio** | "¿Qué preguntan los clientes que podrían responder por sí mismos?" | Sin predeterminado |
| **Herramientas actuales** | "¿Qué recursos de autoservicio existen hoy? (página de FAQ, docs de ayuda)" | Mínimo o ninguno |
| **Plataforma** | "¿Dónde vivirá el portal? (Notion, Zendesk, sitio personalizado, WordPress)" | Por decidir |
| **Nivel técnico del cliente** | "¿Qué tan cómodos están tus clientes con el autoservicio?" | Moderado |

**PUNTO DE CONTROL: Confirma las necesidades antes de diseñar la estructura del portal.**

---

## Fase 2: Arquitectura de Información

Diseña la estructura y navegación del portal.

### Secciones del Portal

```
## Estructura del Portal de Autoservicio

### 1. Base de Conocimiento
   - Primeros Pasos
     - [Guía de configuración]
     - [Tutorial de inicio rápido]
     - [Checklist de primeros pasos]
   - Guías Cómo Hacer
     - [Categoría 1: guías]
     - [Categoría 2: guías]
   - Solución de Problemas
     - [Problemas comunes]
     - [Mensajes de error]
   - Preguntas Frecuentes
     - [Preguntas de facturación]
     - [Preguntas de cuenta]
     - [Preguntas de producto]

### 2. Gestión de Cuenta
   - Ver/actualizar información de cuenta
   - Historial de facturación y facturas
   - Gestión de suscripción
   - Restablecimiento de contraseña

### 3. Soporte
   - Enviar un ticket de soporte
   - Verificar estado del ticket
   - Chat en vivo (durante horario laboral)
   - Información de contacto de emergencia

### 4. Recursos
   - Video tutoriales
   - Plantillas y descargas
   - Guías de mejores prácticas
   - Notas de versión / Qué hay de nuevo

### 5. Comunidad (opcional)
   - Foro de discusión
   - Solicitudes de funciones
   - Tips de otros clientes
```

### Diseño de Navegación

```
## Layout de Página Principal del Portal

**Barra de búsqueda** (prominente, parte superior de la página)
"Busca respuestas..."

**Enlaces rápidos** (4-6 acciones más comunes)
[ Primeros Pasos ] [ Enviar Ticket ] [ Facturación ] [ Cuenta ]

**Artículos populares** (auto-poblados por conteo de vistas)
1. [Artículo más visto]
2. [Segundo más visto]
3. [Tercero más visto]

**Categorías** (tarjetas visuales o iconos)
[ Base de Conocimiento ] [ Guías ] [ Solución de Problemas ] [ Recursos ]

**¿Aún necesitas ayuda?** (siempre visible)
Botón [Contactar Soporte]
```

**PUNTO DE CONTROL: Presenta la arquitectura de información para revisión.**

---

## Fase 3: Plan de Contenido

Planifica el contenido necesario para poblar el portal.

### Inventario de Contenido

```
## Plan de Contenido del Portal

| Sección | Artículo/Página | Prioridad | Estado | Responsable |
|---------|----------------|-----------|--------|-------------|
| Primeros Pasos | Guía de configuración | ALTA | Por escribir | [Nombre] |
| Primeros Pasos | Inicio rápido | ALTA | Por escribir | [Nombre] |
| Solución de Problemas | [Problema común 1] | ALTA | Por escribir | [Nombre] |
| FAQ | Preguntas de facturación | MEDIA | Por escribir | [Nombre] |
| Recursos | [Plantilla 1] | BAJA | Por crear | [Nombre] |
```

### Orden de Prioridad de Contenido

1. **Esenciales de lanzamiento (Mes 1):** Guía de primeros pasos, top 5 respuestas FAQ, formulario de ticket de soporte
2. **Contenido central (Mes 2):** Guías de solución de problemas comunes, instrucciones de gestión de cuenta
3. **Expansión (Mes 3+):** Video tutoriales, plantillas, mejores prácticas, funciones de comunidad

### Optimización de Búsqueda

- Titula cada artículo con las palabras exactas que los clientes usan para describir el problema
- Agrega etiquetas y palabras clave que coincidan con consultas de búsqueda comunes
- Incluye sinónimos (ej., "iniciar sesión" y "login" deben encontrar el mismo artículo)
- Muestra artículos populares en la página principal

---

## Fase 4: Medición

Rastrea el rendimiento del portal e itera.

### Métricas de Éxito

```
## Métricas del Portal

| Métrica | Objetivo | Actual |
|---------|----------|--------|
| Tasa de resolución por autoservicio | 60%+ de problemas | — |
| Tasa de éxito de búsqueda (encontró lo que necesitaba) | 80%+ | — |
| Reducción de tickets de soporte | [X]% de disminución desde línea base | — |
| Satisfacción del portal (encuesta post-visita) | 4+/5 | — |
| Términos más buscados sin resultados | 0 | — |
```

### Revisión Mensual del Portal

1. ¿Cuáles son los términos de búsqueda principales? ¿Existen artículos para todos ellos?
2. ¿Qué artículos tienen muchas vistas pero baja calificación de utilidad? (Necesitan reescritura)
3. ¿Qué tickets de soporte podrían haber sido autoservicio? (Brecha de contenido)
4. ¿Los clientes están encontrando el portal? (Verificar fuentes de tráfico)

### Mejora Continua

- Agrega nuevos artículos para cada pregunta de soporte hecha 3+ veces
- Actualiza artículos cuando cambios de producto afecten las instrucciones
- Elimina o archiva contenido desactualizado trimestralmente
- Prueba la experiencia de búsqueda mensualmente — ¿puedes encontrar respuestas en menos de 60 segundos?

---

## Anti-Patrones

- **Difícil de encontrar** — si los clientes no pueden encontrar el portal, no existe. Enlázalo desde cada email de soporte, interfaz del producto y pie de página del sitio web.
- **Sin búsqueda** — los clientes no van a navegar categorías. La búsqueda debe funcionar y funcionar bien.
- **Contenido desactualizado** — artículos obsoletos erosionan la confianza en todo el portal. Asigna dueños de artículos y fechas de revisión.
- **Sin camino a un humano** — autoservicio sin escape a soporte crea frustración. Siempre proporciona una opción de contacto.
- **Lanzar vacío** — un portal con 3 artículos parece abandonado. Lanza con al menos 10-15 artículos centrales.

---

## Recuperación

- **Los clientes aún contactan soporte por problemas documentados:** El portal es difícil de encontrar o los artículos son difíciles de entender. Audita tanto la descubribilidad como la legibilidad.
- **Bajo tráfico del portal:** Agrega enlaces del portal en auto-respuestas de soporte, emails de onboarding y UI del producto. Los clientes necesitan ser entrenados a verificar autoservicio primero.
- **El usuario no puede crear suficiente contenido:** Comienza con respuestas estilo FAQ (cortas, directas). Las guías completas pueden venir después.
- **La búsqueda devuelve resultados irrelevantes:** Mejora títulos de artículos, agrega etiquetas y crea artículos para búsquedas comunes que actualmente no devuelven nada.
- **El usuario no tiene presupuesto para plataforma de portal:** Una página de Notion bien organizada o un Google Site es un portal gratuito viable para pequeños negocios.
