# SKILL: Sincronizar clases existentes con el template vigente

> Guarda este archivo en `/skills/sincronizar-estructura-clases/SKILL.md`
> Se usa cada vez que el template de `skills/transcribir-clase-curso/SKILL.md` cambia
> y las clases ya publicadas quedan desactualizadas respecto a esa estructura.

---

## Cuándo usar este skill

Cuando `skills/transcribir-clase-curso/SKILL.md` agrega o cambia una sección obligatoria (ej. se agregó `## 🎯 Ejercicio práctico`) y hay clases en `curso-claude-code/clases/` que fueron escritas antes de ese cambio y no la tienen.

---

## Prerequisitos

- [ ] Leer `skills/transcribir-clase-curso/SKILL.md` completo — es la fuente de verdad de la estructura
- [ ] Listar qué clases existentes NO cumplen el template actual (comparar sección por sección, no por longitud)
- [ ] Acceso de escritura al repo `imperioagentico`

---

## Pasos

### Paso 1 — Auditar antes de tocar nada

Para cada clase en `curso-claude-code/clases/`, revisar si tiene TODAS las secciones obligatorias del template vigente en el orden correcto. Anotar solo lo que falta o está mal — no marcar como "falla" una clase que ya cumple.

### Paso 2 — Editar SOLO lo que falta

Regla dura: **no reescribir contenido que ya está bien.** Si a una clase le falta el Ejercicio práctico, se agrega esa sección nueva en su lugar (entre el último bloque de contenido y el Tip) y no se toca el resto del archivo. Idea central, tablas, Tip y Error común existentes se dejan intactos salvo que tengan un error real.

### Paso 3 — El ejercicio nuevo respeta las reglas del template

- Accionable en Claude Code, no una pregunta teórica
- Usa solo lo enseñado hasta esa clase (nunca algo de una clase posterior)
- 15-30 minutos, con resultado verificable
- Si aplica, indicar qué pieza del proyecto del alumno deja lista

### Paso 4 — No commitear ni hacer push

Dejar los archivos modificados en el working tree del repo local, sin commit. La revisión final y el commit/push los hace Claude (Juan lo pidió así explícitamente: la responsabilidad de aprobar el resultado final es de Claude, no de Antigravity).

### Paso 5 — Reportar en texto plano, no repegar los archivos completos

Al terminar, listar en 1 línea por clase: qué se agregó o cambió. No repetir el contenido completo de cada archivo en la respuesta — el archivo ya quedó escrito en el repo, repetirlo en el chat es gasto de tokens innecesario.

---

## Outputs esperados

- Cada clase en `curso-claude-code/clases/` cumple el template vigente completo
- Ningún contenido previo válido fue reescrito o resumido de nuevo
- Un listado corto (no el contenido) de qué cambió por archivo, para que Claude revise con `git diff`

---

## Errores comunes

| Error | Causa probable | Solución |
|-------|---------------|---------|
| Se reescribió una clase completa | Se trató como "generar de nuevo" en vez de "parchar lo que falta" | Solo tocar la(s) sección(es) ausente(s) |
| Ejercicio genérico igual en varias clases | Se copió una plantilla sin adaptar al tema específico | Cada ejercicio usa el concepto único de esa clase |
| Se hizo commit o push | No se respetó el Paso 4 | Dejar cambios sin commitear; Claude revisa y decide |
| Se repegó el archivo completo en el chat | No se respetó el Paso 5 | Reportar solo el resumen de cambios, el archivo ya está en el repo |

---

## Notas adicionales

Este skill existe para que el costo de mantener el repo consistente lo absorba la ejecución (Antigravity), no la revisión (Claude). Claude solo necesita ver el diff final, no regenerar contenido que ya estaba bien escrito.

---

*Creado: 2026-09-02*
