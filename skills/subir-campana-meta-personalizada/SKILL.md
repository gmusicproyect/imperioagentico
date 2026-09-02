# SKILL: Subir campaña a Meta (simple o personalizada por país)

> Guarda este archivo en `/skills/subir-campana-meta-personalizada/SKILL.md`
> Referencia en tu CLAUDE.md: `- /skills/subir-campana-meta-personalizada/SKILL.md → para subir creativos y campañas a Meta`

---

## Cuándo usar este skill

Cuando el usuario pide subir o crear una campaña en Meta Ads con creativos ya generados — ya sea una campaña simple o una versión hiper-personalizada por país/mercado — y quiere dejarla lista para aprobar, no publicada.

---

## Prerequisitos

- [ ] MCP de Meta conectado y verificado con `/mcp`
- [ ] Creativos (imágenes) ya generados y ubicados en la carpeta del proyecto
- [ ] URL de destino de la campaña
- [ ] Presupuesto diario definido por el usuario

---

## Pasos

### Paso 1 — Confirmar inputs obligatorios
Si el prompt no trae presupuesto diario y URL de destino, pedirlos antes de continuar. Nunca asumir un valor por defecto.

### Paso 2 — Seleccionar creativos
Confirmar exactamente qué imágenes se suben (ej. "sube la 1, 5 y 8"), no asumir "todas".

### Paso 3 — Si es personalizado por país
Para cada país objetivo: adaptar copy y creatividad al idioma/modismo local — nunca traducir literal. El texto debe sentirse escrito para ese mercado, no traducido desde otro.

```
Ejemplo de instrucción:
"Crea una campaña por país: Chile (español chileno),
Argentina (español argentino, modismos locales), España (español de España).
Cada una con su propio copy y creativo adaptado, $[X]/día."
```

### Paso 4 — Subir como borrador
Crear la(s) campaña(s) en estado **unpublished** (sin publicar) con el presupuesto indicado. Nunca publicar directo sin aprobación humana.

### Paso 5 — Verificar la subida
No confiar en que el agente reporte "subido" como confirmación suficiente. Pedir que liste la campaña vía MCP, o entrar manualmente al Ads Manager y confirmar que existe con los datos correctos.

### Paso 6 — Reportar al usuario
Resumen breve: qué se subió, en qué campaña(s), con qué presupuesto, y que está pendiente de aprobación manual.

---

## Outputs esperados

- Campaña(s) creada(s) en Meta en estado borrador (no publicadas)
- 1 campaña por país cuando se pide personalización, cada una con copy/creativo propio, no una traducción del original
- Confirmación **verificada** (no solo reportada) de que la subida fue exitosa

---

## Errores comunes

| Error | Causa probable | Solución |
|-------|---------------|---------|
| Presupuesto no definido | Se asumió un valor por defecto | Preguntar siempre por el presupuesto antes de crear la campaña |
| Campaña publicada directo | No se especificó "borrador" en el prompt | Pedir explícitamente "sin publicar, para mi aprobación" |
| Copy traducido literal en vez de adaptado | Se tradujo palabra por palabra en vez de reescribir | Pedir modismos y tono local específicos por país |
| Video no sube | El MCP de Meta no soporta subida de archivos de video | Subir como imagen, o editar un video que ya esté en la cuenta |
| Se da por hecho que subió bien | No se verificó en el Ads Manager | Repetir el Paso 5 siempre, incluso si el agente confirma éxito |

---

## Variaciones

**Variación A — Campaña única (no personalizada):** saltar el Paso 3, usar el mismo copy/creativo para toda la audiencia.

**Variación B — Basada en un anuncio ganador:** antes del Paso 4, pedir que genere N variaciones (copy y/o creativo) del anuncio con mejor performance histórico, y subir esas variaciones como una campaña de testeo.

---

## Notas adicionales

Este skill reemplaza el trabajo manual de un media buyer editando campaña por campaña dentro del Ads Manager (buscar texto, reemplazar, duplicar sets, repetir por país). La clave no es el MCP en sí — es la dirección creativa: personalización real por mercado, no una traducción automática.

---

*Creado: 2026-09-02*
