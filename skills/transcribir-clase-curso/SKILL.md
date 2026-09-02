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

## 💡 Tip

[Un solo consejo accionable y específico, aplicable la próxima vez que se use lo enseñado.]

---

## ⚠️ Error común

[Un error real y específico, no una advertencia vaga: qué se hace mal + qué pasa como consecuencia.]
```

**Reglas de formato:**
- `---` separa cada sección de nivel `##` — nunca se omite
- Máximo 60-90 líneas por archivo. Si es más largo, está cubriendo dos temas y debería dividirse en dos clases
- Tablas de máximo 5-6 filas — más que eso, es una lista o hay que resumir
- Sin relleno: cada línea aporta información nueva, no repite lo de arriba con otras palabras
- Tono directo, español neutro, sin muletillas ni "en este video vamos a..."
- No inventar contenido que no esté en la fuente. Si algo no quedó claro, marcar `[PENDIENTE: confirmar con Juan]` en vez de rellenar con una suposición

### Paso 4 — Actualizar los índices

En el mismo commit que crea la clase:
1. `curso-claude-code/README.md` → agregar la fila a la tabla de "Archivos"
2. `README.md` (raíz) → agregar la fila a la tabla del módulo y actualizar el conteo si ya no son 16 clases
3. Si la clase nueva reemplaza al resumen final como última clase, actualizar `clase-16-resumen.md` (o la que sea el cierre) para que el mapa la incluya

---

## Outputs esperados

- 1 archivo `clase-NN-slug.md` en `curso-claude-code/clases/`, con la estructura exacta de arriba
- Los 2 índices (README raíz y README del módulo) actualizados con la fila nueva
- Sin secciones extra fuera de la estructura (nada de "Introducción" o "Conclusión")

---

## Errores comunes

| Error | Causa probable | Solución |
|-------|---------------|---------|
| Archivo de 200+ líneas | Se transcribió todo literal en vez de sintetizar | Volver al Paso 1: encontrar la idea central y cortar lo que no la sirve |
| Tags genéricos (`Curso`, `Clase`) | No se identificaron los conceptos específicos | Usar sustantivos concretos del contenido (ej: `MCP`, `Skills`) |
| Falta el Tip o el Error común | Se copió la transcripción sin sintetizar | Son obligatorios; si no hay un error común real, se omite la sección — nunca se rellena inventado |
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
