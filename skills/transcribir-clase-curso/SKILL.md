# SKILL: Transcribir y estructurar clase del curso Claude Code

> Guarda este archivo en `/skills/transcribir-clase-curso/SKILL.md`
> Instrucción para cualquier agente (Antigravity, Claude Code, etc.) que transcriba una clase nueva del curso y la agregue al repo `imperioagentico`.

---

## Cuándo usar este skill

Cuando hay una clase nueva (grabación, audio, video o notas sueltas) del curso "Claude Code — Imperio Digital" que hay que convertir en un archivo Markdown consistente con las clases ya existentes en `curso-claude-code/clases/`.

---

## Prerequisitos

- [ ] Contenido fuente de la clase (transcripción cruda, notas o grabación)
- [ ] Número de clase correspondiente (el siguiente disponible en `curso-claude-code/clases/`)
- [ ] Acceso de escritura al repo `imperioagentico`

---

## Pasos

### Paso 1 — Extraer la idea central

Lee o escucha el material fuente completo. Identifica en 2-4 frases cuál es el concepto único que esa clase enseña. Todo lo demás en el archivo sirve a esa idea, no al revés.

### Paso 2 — Definir el nombre de archivo

Formato: `clase-NN-slug.md`
- `NN`: número de clase con dos dígitos (`17`, `18`...)
- `slug`: 1-3 palabras clave del tema, minúsculas, sin tildes, separadas por guiones (ej: `clase-17-antigravity.md`)

### Paso 3 — Escribir el archivo con esta estructura exacta

```markdown
# Clase NN — [Título corto y descriptivo]

**Tags:** `Tag1` `Tag2` `Tag3` (2 a 4 tags, sustantivos concretos)
**Conecta con:** Clase X · Clase Y (1-3 clases relacionadas por tema)

---

## Idea central

[1 párrafo de 2-4 frases. La idea única de la clase, sin rodeos.]

---

## [Sección de contenido 1 — nombre descriptivo, no genérico]

[Tabla, lista o bloque de código: tablas para comparaciones,
código para configuración/comandos/prompts de ejemplo,
listas para pasos o conceptos enumerados.]

---

## [Sección de contenido 2 si aplica]

...

---

## 🎯 Ejercicio práctico

**Ejercicio 1:** [Consigna concreta y acotada que el alumno ejecuta en Claude Code usando SOLO lo visto en esta clase y anteriores — nunca algo que dependa de una clase futura. Debe tomar 15-30 min y tener un resultado verificable: el alumno sabe si le funcionó o no.]

**Ejercicio 2 (opcional, más avanzado):** [Extiende el ejercicio 1 o lo conecta con una clase anterior relacionada.]

*Si el tema de la clase aporta una pieza al proyecto final del alumno (ej. su propio CLAUDE.md, un skill, un agente), decir explícitamente qué pieza es: "Este ejercicio te deja listo el/la [componente] de tu proyecto."*

---

## 💡 Tip

[Un solo consejo accionable y específico, aplicable la próxima vez que se use lo enseñado.]

---

## ⚠️ Error común

[Un error real y específico, no una advertencia vaga: qué se hace mal + qué pasa como consecuencia.]
```

**Reglas de formato:**
- `---` separa cada sección de nivel `##` — nunca se omite
- Máximo 70-110 líneas por archivo (el ejercicio práctico suma largo respecto a las clases 01-16). Si se pasa mucho de eso, está cubriendo dos temas y debería dividirse en dos clases
- Tablas de máximo 5-6 filas — más que eso, es una lista o hay que resumir
- Sin relleno: cada línea aporta información nueva, no repite lo de arriba con otras palabras
- Tono directo, español neutro, sin muletillas ni "en este video vamos a..."
- El **Ejercicio práctico es obligatorio** y no es opcional como el Tip o el Error común: es la parte que convierte la clase en aprendizaje activo, no solo lectura
- El ejercicio nunca requiere una herramienta o concepto que no se haya visto todavía en el curso — solo usa lo ya explicado hasta esa clase
- No inventar contenido que no esté en la fuente. Si algo no quedó claro, marcar `[PENDIENTE: confirmar con Juan]` en vez de rellenar con una suposición

### Paso 4 — Actualizar los índices

En el mismo commit que crea la clase:
1. `curso-claude-code/README.md` → agregar la fila a la tabla de "Archivos"
2. `README.md` (raíz) → agregar la fila a la tabla del módulo y actualizar el conteo si ya no son 16 clases
3. Si la clase nueva reemplaza al resumen final como última clase, actualizar `clase-16-resumen.md` (o la que sea el cierre) para que el mapa la incluya

---

## Outputs esperados

- 1 archivo `clase-NN-slug.md` en `curso-claude-code/clases/`, con la estructura exacta de arriba **incluyendo el ejercicio práctico**
- Los 2 índices (README raíz y README del módulo) actualizados con la fila nueva
- Sin secciones extra fuera de la estructura (nada de "Introducción" o "Conclusión")
- El alumno puede leer la clase y, en la misma sesión, hacer el ejercicio sin salir a buscar información externa

---

## Errores comunes

| Error | Causa probable | Solución |
|-------|---------------|---------|
| Archivo de 200+ líneas | Se transcribió todo literal en vez de sintetizar | Volver al Paso 1: encontrar la idea central y cortar lo que no la sirve |
| Tags genéricos (`Curso`, `Clase`) | No se identificaron los conceptos específicos | Usar sustantivos concretos del contenido (ej: `MCP`, `Skills`) |
| Falta el Ejercicio práctico | Se trató como sección opcional igual que el Tip | Es obligatoria — sin ella la clase es solo teoría y no cumple el propósito del repo |
| Ejercicio teórico ("explica con tus palabras...") en vez de accionable | Es más fácil escribir una pregunta que un ejercicio ejecutable | El ejercicio debe hacerse EN Claude Code, con un resultado que se pueda verificar (un archivo creado, un comando que corrió, un output concreto) |
| Ejercicio requiere algo de una clase futura | No se revisó el orden del curso antes de escribir el ejercicio | Solo usar herramientas/conceptos ya cubiertos hasta esa clase |
| Índices no actualizados | Se creó el archivo pero no se tocó el README | Repetir el Paso 4 antes de dar la tarea por terminada |

---

## Variaciones

**Variación A — Clase de bono (no del curso principal):** usa la estructura de `bonos/[nombre]/README.md` en vez de esta (más larga, permite subsecciones de instalación/costos/errores).

**Variación B — Fuente es solo audio sin transcripción:** primero generar la transcripción cruda en un archivo temporal, y recién ahí aplicar este skill sobre ese texto — no sintetizar directo desde el audio.

---

## Notas adicionales

El valor del repo `imperioagentico` está en que cada clase sea escaneable en 30 segundos y consistente con las demás — no en que sea exhaustiva. Prioriza síntesis sobre cobertura.

---

*Creado: 2026-09-02 · Última actualización: 2026-09-02*
