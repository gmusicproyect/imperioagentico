---
name: handout-taller
description: "Crea materiales de handout de taller con ejercicios, hojas de referencia, plantillas y acciones post-taller."
allowed-tools: Read Write Glob
author: Imperio Digital
version: "1.0"
---

# Handout de Taller

## Cuándo Usar Este Skill

Usa este skill cuando necesites:
- Crear materiales de handout para un taller en vivo o virtual
- Construir hojas de trabajo de ejercicio, hojas de referencia y plantillas para participantes
- Diseñar planes de acción post-taller que extiendan el aprendizaje más allá de la sesión
- Producir documentos complementarios imprimibles o digitales para eventos de capacitación

**NO** uses este skill para materiales de curso completo, decks de diapositivas o libros de trabajo independientes. Es para materiales de handout complementarios que acompañan un taller en vivo.

---

## Principio Fundamental

UN HANDOUT DE TALLER NO ES UNA TRANSCRIPCIÓN DE TU CHARLA — ES LA HERRAMIENTA QUE LOS PARTICIPANTES USAN DURANTE LA SESIÓN Y LA REFERENCIA QUE GUARDAN DESPUÉS, CONTENIENDO SOLO LO QUE NECESITAN PARA HACER LOS EJERCICIOS E IMPLEMENTAR EL APRENDIZAJE.

---

## Fase 1: Resumen

### Entradas Requeridas

| Entrada | Qué Preguntar | Predeterminado |
|---------|--------------|--------|
| **Tema del taller** | "¿De qué trata el taller?" | Sin predeterminado — debe proporcionarse |
| **Duración del taller** | "¿Cuánto dura la sesión?" | 90 minutos |
| **Ejercicios clave** | "¿Qué actividades prácticas harán los participantes durante el taller?" | Sin predeterminado — debe proporcionarse |
| **Audiencia** | "¿Quién asiste y qué ya saben?" | Solopreneurs, nivel principiante |
| **Formato** | "¿PDF imprimible, digital rellenable o ambos?" | PDF digital rellenable |

**PUNTO DE CONTROL: Confirma el resumen antes de proceder.**

---

## Fase 2: Estructura

### Arquitectura del Handout

```
1. Página de portada — título del taller, fecha, nombre del facilitador, logo
2. Descripción general de agenda — flujo de sesión con timing
3. Conceptos clave — definiciones y frameworks de referencia (una página máx)
4. Hojas de trabajo de ejercicio — una por actividad práctica
5. Plantillas — herramientas de relleno que los participantes usan durante o después
6. Lista de recursos — herramientas recomendadas, libros, enlaces
7. Plan de acción — pasos de implementación post-taller
8. Página de notas — espacio en blanco para notas personales
```

### Diseño de Hoja de Trabajo de Ejercicio

Cada ejercicio obtiene su propia página:

```
## Ejercicio [N]: [Título]
**Tiempo:** [X minutos]
**Objetivo:** [Qué los participantes producirán]

### Instrucciones
1. [Paso 1]
2. [Paso 2]
3. [Paso 3]

### Espacio de Trabajo
[Área de relleno con indicaciones, cajas o líneas]

### Ejemplo
[Ejemplo completado mostrando cómo se ve buen output]
```

**PUNTO DE CONTROL: Presenta la estructura del handout para aprobación.**

---

## Fase 3: Escribe

### Reglas de Contenido

- **El espacio en blanco es esencial** — los handouts necesitan espacio para escribir, no texto de pared a pared
- **Las instrucciones deben pararse solas** — un participante que se distrajo durante 30 segundos debe poder leer el handout y ponerse al día
- **Un ejercicio por página** — nunca dividas un ejercicio entre páginas
- **El contenido de referencia es mínimo** — solo incluye lo necesitado durante la sesión, no todo lo que sabes
- **Las plantillas están pre-formateadas** — proporciona estructura (encabezados, etiquetas, cajas) no páginas en blanco

### Página de Conceptos Clave

Limita a 5-8 conceptos máximo:

```
| Concepto | Definición | Cuándo Usar |
|---------|-----------|-------------|
| [Término] | [Una oración] | [Contexto] |
```

### Plan de Acción Post-Taller

```
## Tu Plan de Acción de 7 Días

**Hoy:** [Una acción inmediata a tomar mientras la motivación es alta]
**Esta semana:**
- [ ] [Acción 1 — específica y medible]
- [ ] [Acción 2]
- [ ] [Acción 3]
**Este mes:** [Meta de implementación más grande]
**¿Necesitas ayuda?** [Info de contacto o enlace de comunidad]
```

---

## Fase 4: Pulida

### 1. Verificación Lista para Impresión

```
- [ ] Todas las páginas funcionan en blanco y negro (sin elementos dependientes de color)
- [ ] Tamaño de fuente es 11pt mínimo para cuerpo, 14pt para encabezados
- [ ] Los márgenes son al menos 0.75 pulgadas para encuadernación o perforación
- [ ] Las hojas de trabajo de ejercicio tienen espacio de relleno adecuado
- [ ] El conteo de páginas es razonable (objetivo: 8-15 páginas para taller de 90 min)
```

### 2. Optimización Digital

- Campos de formulario rellenable para todas las áreas de ejercicio
- Enlaces clickables en sección de recursos
- Secciones marcadas para navegación fácil
- Tamaño de archivo bajo 5MB para distribución fácil por email

### 3. Notas del Facilitador

Proporciona una versión separada del facilitador con:
- Pistas de timing para cada ejercicio
- Respuestas o outputs de ejemplo para ejercicios
- Preguntas comunes del participante y respuestas
- Scripts de transición entre secciones

---

## Ejemplo 1: Taller "Construye Tu Calendario de Contenido" (2 horas)

```
Contenido del handout:
- Hoja de trabajo de lluvia de ideas de pilar de contenido
- Plantilla de calendario mensual (cuadrícula rellenable)
- Hoja de referencia de fórmula de headline
- Guía de publicación específica de plataforma (una página)
- Plan de acción de 30 días
```

## Ejemplo 2: Taller "Precio Tus Servicios" (90 min)

```
Contenido del handout:
- Hoja de trabajo de cálculo de costos
- Plantilla de investigación de competencia
- Referencia de fórmula de precios basado en valor
- Plantilla de script de presentación de precio
- Lista de verificación de implementación
```

---

## Anti-Patrones

- **Sobrecarga de información** — empacar todo lo que sabes en el handout abruma a los participantes. Cura despiadadamente.
- **Sin espacio de relleno** — un handout sin espacio para escribir es un folleto, no una herramienta de trabajo.
- **Ejercicios sin ejemplos** — los participantes se congelen cuando no saben cómo se ve "hecho".
- **Sin items de acción post-taller** — el valor del handout cae a cero si va a un cajón después de la sesión.
- **Fuentes tiny para caber más contenido** — si necesitas encoger la fuente, necesitas cortar contenido en su lugar.
- **Diseños dependientes de color** — muchos participantes imprimen en blanco y negro. Diseña acorde.

---

## Recuperación

- **El usuario no tiene ejercicios definidos:** Pregunta "¿Qué deberían los participantes haber creado cuando se vayan?" Trabaja hacia atrás desde el deliverable para diseñar 2-3 ejercicios.
- **El taller es demasiado corto para un handout completo:** Crea una hoja de referencia de una página más un email de acción post-taller en su lugar.
- **El usuario quiere incluir todo de la charla:** Limita a conceptos que los participantes necesitan referenciar durante ejercicios. Todo lo demás puede ir en follow-up email.
- **Audiencia solo digital:** Salta el formateo de impresión. Usa una página de Notion o Google Doc con elementos interactivos en su lugar.
