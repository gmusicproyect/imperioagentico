---
name: plantilla-boletin-email
description: "Crea plantillas de boletín de email con estructura de contenido, ratios de contenido editorial vs. promocional, y mejores prácticas de diseño."
allowed-tools: Read Write Glob
metadata:
  author: Imperio Digital
  version: "1.0"
---

# Plantilla de Boletín de Email

## Cuándo Usar Este Skill

Usa este skill cuando necesites:
- Diseñar estructura de boletín semanal o mensual
- Equilibrar contenido editorial, social proof, y promoción
- Crear formato reutilizable para múltiples ediciones
- Mejorar readabilidad y engagement en boletín

---

## Principio Fundamental

UN BOLETÍN GRANDE TRATA DE TÚ, UN BOLETÍN GRANDE TRATA DE TU AUDIENCIA.

---

## Estructura Recomendada

### Arriba del Pliegue (Primeras 200px)

```
- Encabezado de marca
- Línea de asunto visual (opcional)
- Intro: 1-2 oraciones conectando con reader
```

### Zona Central (Contenido Principal)

```
- Story 1: Artículo/contenido principal (30-40% espacio)
  + Imagen thumbnail
  + 2-3 párrafos
  + Enlace "Leer más"

- Story 2-3: Historias secundarias (20-30% espacio)
  + Más cortas (1-2 párrafos)
  + Imágenes thumbnail

- Sección de Promoción (10-20% espacio)
  + Limitado a 1 promoción
  + Botón CTA claro
```

### Pie

```
- Unsubscribe link
- Dirección social media
- Información de contacto
```

---

## Ratio de Contenido

**Mejor mezcla:**
- 70% Editorial (contenido útil, insights)
- 20% Social Proof (testimonios, casos de estudio)
- 10% Promocional (ofertas, CTAs)

---

## Mejores Prácticas

- **Línea de asunto:** 40-50 caracteres, específica
- **Preview text:** Continúa la promesa de asunto
- **Colores:** Máximo 3, consistente con marca
- **Fonts:** Sans-serif, 14-16px cuerpo
- **Imágenes:** <1MB total, alt text en todas
- **CTAs:** 2-3 máximo, claro call to action
- **Móvil:** Testeado en 320px, stack vertical

---

## Template HTML Skeleton

```html
<table width="100%" cellpadding="0" cellspacing="0">
  <tr>
    <td width="600">
      <!-- HEADER -->
      <!-- INTRO -->
      <!-- MAIN STORY -->
      <!-- SECONDARY STORIES -->
      <!-- PROMOTION -->
      <!-- FOOTER -->
    </td>
  </tr>
</table>
```

---

## Anti-Patrones

- **Demasiados colores** — confunde, reduce conversión
- **Imágenes enormes** — lento, rompe en móvil
- **Sin alt text** — inaccesible, cae a spam
- **Demasiado promotional** — gente se desuscribe
- **Sin preview text** — pierde 40% del inbox

---

## Checklist

- [ ] Plantilla base en HTML creada
- [ ] Testeada en Outlook, Gmail, Apple, móvil
- [ ] Alt text en todas imágenes
- [ ] CTAs contrastados y clickeables
- [ ] Unsubscribe link visible
- [ ] Documentación para reutilización
