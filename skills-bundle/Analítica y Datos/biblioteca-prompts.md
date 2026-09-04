---
name: biblioteca-prompts
description: "Organiza y documenta bibliotecas de prompts reutilizables con categorías, variables y puntuación de calidad. Utiliza cuando construyas una colección estructurada de prompts de IA para tu negocio."
allowed-tools: Read Write Glob
metadata:
  author: Imperio Digital
  version: "1.0"
---

# Biblioteca de Prompts

## Cuándo Usar Este Skill

Utiliza este skill cuando necesites:
- Construir una biblioteca organizada de prompts de IA reutilizables para tareas de negocio
- Documentar prompts con variables, ejemplos e instrucciones de uso
- Crear un sistema de puntuación de calidad para efectividad de prompts
- Estandarizar el uso de prompts en un equipo o workflow

**NO** utilices este skill para escribir prompts individuales, tutoriales de ingeniería de prompts o comparaciones de herramientas de IA. Esto es para organizar y documentar una colección de prompts.

---

## Principio Fundamental

UNA BIBLIOTECA DE PROMPTS ES UN ACTIVO DE NEGOCIO — CADA PROMPT DEBERÍA DOCUMENTARSE, PROBARSE Y VERSIONARSE PARA QUE CUALQUIERA PUEDA USARLO Y OBTENER RESULTADOS CONSISTENTES.

---

## Fase 1: Brief

### Entradas Requeridas

| Entrada | Qué Preguntar | Por Defecto |
|---------|--------------|------------|
| **Tipo de negocio** | "¿Qué hace tu negocio?" | Sin valor por defecto — debe proporcionarse |
| **Herramientas de IA utilizadas** | "¿Qué herramientas de IA usas? Claude, ChatGPT, Gemini, otro?" | Claude |
| **Casos de uso clave** | "¿Para qué usas IA más? Contenido, email, investigación, análisis?" | Sin valor por defecto — lista al menos 5 |
| **Uso por equipo** | "¿Será esta biblioteca usada solo por ti o compartida con un equipo?" | Uso solo |
| **Prompts actuales** | "¿Tienes prompts que ya reutilizas regularmente?" | Algunos informales |
| **Preferencia de almacenamiento** | "¿Dónde debería vivir la biblioteca? Notion, Google Docs, archivos markdown?" | Archivos markdown |

**PUNTO DE CONTROL:** Confirma el brief antes de diseñar la estructura de la biblioteca.

---

## Fase 2: Diseñar la Biblioteca

### Estructura de Categorías

Organiza prompts por función de negocio:

```
biblioteca-prompts/
├── contenido/
│   ├── draft-blog-post.md
│   ├── caption-redes-sociales.md
│   └── newsletter-email.md
├── marketing/
│   ├── copy-anuncio.md
│   ├── copy-pagina-destino.md
│   └── esquema-lead-magnet.md
├── operaciones/
│   ├── resumen-reunion.md
│   ├── documentacion-proceso.md
│   └── brief-proyecto.md
├── finanzas/
│   ├── recordatorio-factura.md
│   └── reporte-gastos.md
├── cliente/
│   ├── respuesta-soporte.md
│   ├── respuesta-resena.md
│   └── email-onboarding.md
└── investigacion/
    ├── analisis-competidor.md
    └── investigacion-mercado.md
```

### Plantilla de Tarjeta de Prompt

Cada prompt en la biblioteca usa este formato:

```
# [Nombre del Prompt]

**Categoría:** [Función de negocio]
**Herramienta IA:** [Claude / ChatGPT / Cualquiera]
**Versión:** [1.0]
**Último probado:** [Fecha]
**Puntuación de calidad:** [1-5]

## Propósito
[Una oración: qué produce este prompt]

## Variables
- {{VARIABLE_1}}: [Descripción, ejemplo]
- {{VARIABLE_2}}: [Descripción, ejemplo]

## Prompt
[El texto completo del prompt con {{VARIABLES}} marcadas]

## Ejemplo de Salida
[Una muestra de cómo se ve una buena salida]

## Consejos
- [Consejo de uso 1]
- [Consejo de uso 2]

## Registro de Cambios
- v1.0 — Versión inicial
```

**PUNTO DE CONTROL:** Confirma la estructura y plantilla antes de poblar la biblioteca.

---

## Fase 3: Poblar

### Reglas de Escritura de Prompts

- **Un prompt, un propósito** — no combines tareas. Un prompt que escribe Y edita Y formatea son tres prompts.
- **Las variables son explícitas** — usa `{{LLAVES_DOBLES}}` para cada entrada que el usuario debe proporcionar. Nunca dejes suposiciones implícitas.
- **Incluye restricciones** — conteo de palabras, tono, formato, qué evitar. Las restricciones mejoran la calidad de salida.
- **Muestra la salida ideal** — incluye un ejemplo de cómo se ve una buena respuesta. Esto establece la barra de calidad.
- **Versiona todo** — cuando mejores un prompt, incrementa la versión y nota qué cambió.

### Rúbrica de Puntuación de Calidad

| Puntuación | Etiqueta | Criterios |
|--------|-------|----------|
| 5 | Listo para producción | Salida consistentemente de alta calidad con edición mínima necesaria |
| 4 | Confiable | Buena salida 80%+ del tiempo, ocasional edición ligera |
| 3 | Usable | Produce un punto de inicio sólido pero requiere refinamiento humano |
| 2 | Necesita trabajo | Resultados inconsistentes, prompt necesita mejora |
| 1 | Experimental | Sin probar o no confiable, mantén para iteración |

### Proceso de Iteración de Prompts

1. Escribe el prompt inicial (v1.0)
2. Prueba con 3 entradas diferentes
3. Puntúa las salidas
4. Identifica debilidades (demasiado largo, tono equivocado, elementos faltantes)
5. Revisa el prompt (v1.1)
6. Reprueba y repuntúa
7. Repite hasta que la puntuación alcance 4+

---

## Fase 4: Pulir

### 1. Mantenimiento de Biblioteca

- **Revisión mensual:** Prueba los 10 prompts más usados con versiones actuales de modelo IA
- **Auditoría trimestral:** Archiva prompts no usados en 90 días, añade nuevos para necesidades emergentes
- **Control de versión:** Nunca sobrescribas — siempre crea una nueva versión y nota cambios
- **Seguimiento de uso:** Nota qué prompts se usan más y cuáles producen los mejores resultados

### 2. Guía de Compartir de Equipo (si aplica)

- Almacena en una ubicación compartida (Notion, carpeta compartida, repo)
- Crea una guía de inicio rápido: cómo encontrar prompts, cómo usar variables, cómo presentar nuevos prompts
- Designa un bibliotecario de prompts (o rota el rol)
- Configura un mecanismo de feedback: "Este prompt funcionó / no funcionó porque..."

### 3. Checklist de Calidad

```
## Checklist de Biblioteca de Prompts

- [ ] Categorías cubren todas las funciones principales de negocio
- [ ] Cada prompt usa la plantilla de tarjeta estándar
- [ ] Todas las variables están marcadas con {{LLAVES_DOBLES}} y descritas
- [ ] Cada prompt incluye al menos un ejemplo de salida
- [ ] Las puntuaciones de calidad se asignan y están actualizadas
- [ ] Los prompts están versionados con registros de cambios
- [ ] La biblioteca está organizada en una estructura searchable
- [ ] La cadencia de revisión mensual está programada
- [ ] Los prompts principales se prueban con versiones actuales de modelo IA
- [ ] El proceso de archivo para prompts sin usar existe
```

---

## Ejemplo

**Tarjeta de prompt:**
```
# Caption para Redes Sociales

**Categoría:** Contenido
**Herramienta IA:** Claude
**Versión:** 1.2
**Último probado:** 2026-02-15
**Puntuación de calidad:** 4

## Propósito
Escribe un caption para redes sociales para Instagram o LinkedIn de un tema y mensaje clave.

## Variables
- {{PLATAFORMA}}: Instagram o LinkedIn
- {{TEMA}}: El asunto del post
- {{MENSAJE_CLAVE}}: El punto que quieres hacer
- {{TONO}}: casual, profesional, motivacional, ingenioso
- {{CTA}}: Qué quieres que haga el lector

## Prompt
Escribe un caption para {{PLATAFORMA}} sobre {{TEMA}}.

Mensaje clave: {{MENSAJE_CLAVE}}
Tono: {{TONO}}
Incluye un llamado a la acción: {{CTA}}

Requisitos:
- Bajo 150 palabras para Instagram, bajo 200 para LinkedIn
- Abre con un hook (pregunta, declaración audaz o hecho sorprendente)
- Usa saltos de línea para legibilidad
- Termina con el CTA
- Sin hashtags en el cuerpo (los añadiré por separado)

## Ejemplo de Salida
"La mayoría de solopreneurs gastan 6 horas a la semana en facturación.

Seis. Horas.

Eso es un día de trabajo completo cada mes en papeleo en lugar de ingresos.

Lo reduje a 45 minutos automatizando tres cosas:
→ Generación de factura desde finalización de proyecto
→ Recordatorios de pago automáticos
→ Categorización de gastos automática

Las herramientas cuestan $30/mes en total. El ahorro de tiempo vale $1,200.

Deja un 🔥 si quieres la configuración exacta."

## Registro de Cambios
- v1.2 — Añadió restricción "sin hashtags", mejoró instrucción de hook
- v1.1 — Añadió límites de conteo de palabras específicos de plataforma
- v1.0 — Versión inicial
```

---

## Anti-Patrones

- **Acumular prompts sin probar** — una biblioteca de 50 prompts sin probar es un cajón de basura. Prueba y puntúa antes de añadir.
- **Sin variables** — detalles hardcodeados hacen prompts de una sola vez. Extrae cada elemento cambiable en una variable.
- **Sin ejemplos** — sin una salida de muestra, la calidad es subjetiva. Siempre muestra cómo se ve lo bueno.
- **Nunca actualizar** — los modelos de IA cambian. Un prompt que funcionó hace 6 meses puede no funcionar tan bien hoy. Revisa regularmente.
- **Complicar demasiado** — un prompt que requiere 15 variables es demasiado complejo. Divídelo en múltiples prompts más simples.

---

## Recuperación

- **Demasiados prompts para organizar:** Comienza categorizando los 10 que usas más. Archiva todo lo demás y añade según sea necesario.
- **Los prompts producen resultados inconsistentes:** Añade más restricciones (conteo de palabras, formato, tono, ejemplos). Las restricciones reducen varianza.
- **Los miembros del equipo no usan la biblioteca:** La biblioteca es demasiado difícil de acceder o buscar. Simplifica la estructura y crea una guía de inicio rápido.
- **Las puntuaciones de calidad son todas bajas:** Los prompts pueden ser demasiado amplios. Estrecha el propósito de cada prompt a una salida específica.