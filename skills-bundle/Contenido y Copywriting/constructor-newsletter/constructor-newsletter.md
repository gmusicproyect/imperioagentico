---
name: constructor-newsletter
description: "Construye newsletters profesionales con estructura, templates y CTA claros. Usa cuando necesites crear newsletters regulares para tu audiencia."
allowed-tools: Read Write Glob
metadata:
  author: Imperio Digital
  version: "1.0"
---

# Constructor de Newsletter

## Cuándo Usar Esta Skill

Usa esta skill cuando necesites:
- Crear una estructura y plantilla de newsletter reutilizable
- Diseñar secciones recurrentes que mantengan la consistencia
- Establecer un formato que sea fácil de escribir y leer
- Desarrollar un workflow para producción de newsletter

**NO USES** esta skill para escribir el contenido de una sola newsletter. Esto es para crear el framework y template.

---

## Principio Fundamental

UNA NEWSLETTER EXITOSA TIENE UN FORMATO PREDECIBLE Y CONSISTENTE — EL LECTOR SABE QUÉ ESPERAR Y CUÁNDO ESPERAR CADA SECCIÓN.

---

## Fase 1: Definir Estructura

### Componentes Clave

Toda newsletter tiene estos elementos:

1. **Línea de asunto** — Atractivo, específico, bajo 50 caracteres
2. **Preheader** — Texto que aparece después del asunto (50-100 caracteres)
3. **Saludo personal** — Crea conexión inmediata
4. **Sección principal** — El contenido que importa
5. **Secciones secundarias** — Contenido de apoyo, anuncios
6. **CTA principal** — Una acción clara
7. **Footer** — Información de contacto, desuscripción, redes sociales

### Plantilla de Estructura

```
## Línea de Asunto
[Personalization] + [Beneficio] + [Número/dato si aplica]

## Preheader
[Continúa la línea de asunto con 40-60 caracteres adicionales]

## Cuerpo

### Saludo
Hola [Nombre/Audiencia],

### Sección principal
[Hook - captura atención]
[Contenido principal - 2-4 párrafos]
[Beneficio - por qué esto importa]

### Secciones secundarias
[Recurso/noticia/anuncio]
[CTA secundario - opcional]

### CTA Principal
[Botón claro con acción específica]

### Footer
[Detalles de contacto]
[Enlace de desuscripción]
[Redes sociales]
```

---

## Fase 2: Desarrollar Secciones Recurrentes

Define qué aparecerá en cada newsletter:

```
**Sección 1: [Nombre]**
- Contenido: [tipo]
- Largo: [X palabras]
- Frecuencia: Cada edición / Alternada / Ocasional
- Responsable: [quién escribe esto]

**Sección 2: [Nombre]**
...
```

### Opciones de Secciones Comunes

- **Espacio de pensamiento** — Editorial corto del autor
- **Contenido principal** — Artículo featured
- **Recursos** — Enlaces curados o herramientas
- **Historias** — Casos de éxito o testimonios
- **Noticias de industria** — Resumen de actualizaciones
- **Encuesta/pregunta** — Engagement directo
- **Anuncio/promoción** — Producto o evento
- **Recomendación personal** — Libro, recurso, etc.

---

## Fase 3: Crear Especificación de Email

Define dimensiones técnicas:

```
## Especificaciones Técnicas

- **Ancho** — 600px máximo (para outlook)
- **Fuentes** — Sans-serif para cuerpo, serif o sans para títulos
- **Colores** — Máximo 3 primarios + 1 acento
- **Imágenes** — Cargar fallback de texto (algunos clientes no cargan imágenes)
- **Botones** — Mínimo 44px altura, texto descriptivo
- **Mobile** — Todo debe ser legible en 375px ancho
```

---

## Fase 4: Crear Checklist de Producción

```
## Checklist de Cada Newsletter

**Antes de escribir:**
- [ ] Tema/tema principal identificado
- [ ] Secciones recurrentes incluidas
- [ ] Largo estimado vs. presupuesto de tiempo
- [ ] Imágenes/recursos identificados

**Mientras escribes:**
- [ ] Línea de asunto bajo 50 caracteres
- [ ] Preheader complementa la línea de asunto
- [ ] Saludo personalizado
- [ ] Sección principal tiene hook claro
- [ ] CTA principal es singular y claro
- [ ] Todos los enlaces funcionan
- [ ] Sin errores de ortografía/gramática

**Antes de enviar:**
- [ ] Se ve bien en móvil
- [ ] Se ve bien en desktop
- [ ] Imágenes cargan correctamente
- [ ] Enlaces funcionan
- [ ] Enlace de desuscripción presente
- [ ] Información de contacto correcta
```

---

## Ejemplo de Plantilla Completamente Desarrollada

```
**LÍNEA DE ASUNTO:**
[Nombre], el error que cometía con mi newsletter (y cómo lo arreglé)

**PREHEADER:**
El cambio que hizo que mis tasas de apertura subieran 28%

**CUERPO:**

Hola [Nombre],

Pasé tres años escribiendo newsletters que la gente no leía.

No era el contenido. Era el formato.

Descubrí que mi audiencia queraba:
1. Una idea clara en los primeros párrafos
2. Párrafos cortos y respirables
3. Un CTA obvio, sin múltiples opciones

Cambié tres cosas:
- Eliminé secciones que "pensé" que los lectores querían (pero no leían)
- Cambié a párrafos de máximo 3 líneas
- Cambié a un único botón de CTA en lugar de 3

Resultado: tasas de apertura subieron 28%. Las tasas de clic subieron 15%.

La moraleja: conoce tu formato. Hazlo consistente. Hazlo escaneable.

[BOTÓN CTA] Leer mi guía completa de newsletter

---

Sección de recurso:
Esta semana recomiendo: [Libro/Artículo/Herramienta]

---

[Información de contacto]
[Enlace de desuscripción]
[Redes sociales]
```

---

## Anti-Patrones

- Demasiadas secciones — 3-4 es el máximo
- Demasiados CTAs — uno principal, máximo uno secundario
- Párrafos de muro de texto — mantén máximo 3 líneas
- Sin línea de asunto clara — el lector no sabe de qué se trata
- Cambiar formato constantemente — consistencia es clave
- Ignorar datos — revisa tasas de apertura, clic, desuscripción cada mes
