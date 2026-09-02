# SKILL: Procesar una transcripción nueva (instrucción maestra para Google/Antigravity)

> Guarda este archivo en `/skills/procesar-transcripcion/SKILL.md`
> Esta es la instrucción de referencia fija para CUALQUIER transcripción nueva que Juan entregue.
> No hace falta pedir una instrucción distinta cada vez — basta con decir "aplica el flujo estándar" y adjuntar la transcripción.

---

## Cuándo usar este skill

Siempre que llegue una transcripción cruda (grabación, audio, notas) de cualquier tema del curso — clase nueva, profundización de una clase existente, o una herramienta/integración específica — para integrarla al repo `imperioagentico`.

---

## Prerequisitos

- [ ] Transcripción cruda del contenido
- [ ] Acceso de lectura a `curso-claude-code/clases/`, `bonos/` y `skills/` para no duplicar algo que ya existe
- [ ] Acceso de escritura al repo local (sin permiso de commit/push — ver Paso 3)

---

## Pasos

### Paso 0 — Clasificar el contenido antes de escribir nada

| Categoría | Cuándo aplica | Qué hacer |
|-----------|---------------|-----------|
| **Clase nueva** | El tema no tiene ningún archivo relacionado en `curso-claude-code/clases/` | Crear `clase-NN` con el siguiente número disponible, usando `skills/transcribir-clase-curso/SKILL.md` |
| **Profundización de una clase existente** | El tema ya tiene una clase (ej. Obsidian = clase-13, Skills = clase-05) y el contenido nuevo es un caso práctico o avanzado de lo mismo | Crear una clase nueva con el siguiente número disponible, cross-linkeada en `Conecta con` con la clase original (igual que se hizo con clase-17 sobre clase-14). **Nunca sobreescribir la clase original.** |
| **Bono / herramienta específica** (ej. Higgsfield, Graphify, Control Remoto) | Es una integración o herramienta puntual, no un concepto transversal del curso | Crear `bonos/[nombre]/README.md` siguiendo el formato largo ya usado en los bonos existentes (Stack, Instalación, Casos de uso, Errores comunes) — no el formato corto de clase |
| **Workflow repetible detectado dentro de la transcripción** | El contenido describe un proceso que se va a ejecutar más de una vez (como pasó con "sube las imágenes" → skill de Meta) | Además de la clase/bono, extraer un `SKILL.md` nuevo en `/skills/[nombre-del-proceso]/` usando `recursos/plantillas/skill-template.md` |

Si hay duda entre dos categorías, preferir la más específica (bono sobre clase) y dejarlo anotado en el reporte del Paso 4 para que Claude lo confirme.

### Paso 1 — Aplicar la estructura correspondiente

- Clase o extensión → `skills/transcribir-clase-curso/SKILL.md` (estructura exacta, límites de largo, Ejercicio práctico obligatorio)
- Bono → estructura de los `bonos/*/README.md` existentes
- Skill extraído → `recursos/plantillas/skill-template.md`

### Paso 2 — Actualizar índices

En el mismo lote de cambios:
- `curso-claude-code/README.md` y `README.md` (raíz) si se creó/extendió una clase
- `bonos/README.md` si se creó un bono nuevo
- El `Conecta con` de la clase original si es una profundización

### Paso 3 — No commitear ni hacer push

Dejar todos los archivos nuevos/modificados en el working tree del repo local, sin commit. La responsabilidad de revisar, corregir y aprobar el resultado final antes de subirlo a GitHub es de Claude, no de Google.

### Paso 4 — Reportar en texto plano, sin repegar contenido

Al terminar, reportar en 1-2 líneas por archivo: nombre, categoría (clase / extensión / bono / skill), y de qué trata. Nunca repegar el contenido completo de los archivos en el chat — ya quedaron escritos en el repo; Claude los revisa directamente ahí.

---

## Outputs esperados

- Archivos nuevos o modificados en el repo, ya clasificados correctamente (clase, bono o skill)
- Índices actualizados en el mismo lote
- Un reporte corto (no el contenido) listo para que Claude revise con `git diff`
- Cero commits, cero pushes

---

## Errores comunes

| Error | Causa probable | Solución |
|-------|---------------|---------|
| Se creó una clase cuando debía ser un bono (o viceversa) | No se revisó si el tema es transversal o una herramienta puntual | Aplicar la tabla del Paso 0 antes de escribir |
| Se sobreescribió una clase existente en vez de crear una extensión | No se buscó primero si el tema ya tenía archivo | Siempre revisar `curso-claude-code/clases/` antes de decidir el nombre del archivo |
| Se hizo commit/push | No se respetó el Paso 3 | Dejar los cambios sin commitear siempre |
| Se repegó el archivo completo en el reporte | No se respetó el Paso 4 | Reportar solo el resumen |

---

## Notas adicionales

Este skill reemplaza tener que pedirle a Claude una instrucción distinta cada vez. Es el punto de entrada único: cualquier transcripción nueva, de cualquier tema, sigue este mismo flujo de clasificación → estructura → índices → entrega sin commit.

---

*Creado: 2026-09-02*
