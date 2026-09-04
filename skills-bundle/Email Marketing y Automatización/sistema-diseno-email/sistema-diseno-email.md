---
name: sistema-diseno-email
description: "Diseña sistemas de plantilla de email con estándares de encabezado/pie, estilos de botón, directrices de imagen, reglas responsivas y layouts específicos de tipo. Úsalo cuando estandarices comunicaciones de email."
allowed-tools: Read Write Glob
metadata:
  author: Imperio Digital
  version: "1.0"
---

# Sistema de Diseño de Email

## Cuándo Usar Este Skill

Usa este skill cuando necesites:
- Crear un conjunto de plantillas de email marcadas para diferentes casos de uso
- Estandarizar diseño de email en comunicaciones de marketing, transaccionales e internas
- Definir reglas de diseño responsivo para móvil y desktop
- Briefear a un desarrollador o plataforma de email sobre requisitos de plantilla

**NO** uses este skill para escribir copias de email, estrategia de email marketing, u optimización de entregabilidad de email. Esto es para diseño visual y estructural de plantilla de email.

---

## Principio Fundamental

EL DISEÑO DE EMAIL DEBE FUNCIONAR EN EL PEOR CASO — UN TELÉFONO DE 5 AÑOS, OUTLOOK 2016, Y DARK MODE SIMULTÁNEAMENTE. DISEÑA PARA RESTRICCIONES, NO IDEALES.

---

## Fase 1: Resumen

### Entradas Requeridas

| Entrada | Qué Preguntar | Por Defecto |
|-------|------------|---------|
| **Tipos de email** | "¿Qué tipos de emails envías? (boletín, promocional, transaccional, onboarding, anuncio)" | Boletín y transaccional |
| **Plataforma** | "¿Qué herramienta de email? (Mailchimp, ConvertKit, Klaviyo, SendGrid, custom)" | Mailchimp |
| **Directrices de marca** | "¿Colores de marca, fonts, y logo?" | Debe ser proporcionado |
| **Problemas actuales** | "¿Qué está mal con tus emails actuales? (inconsistentes, feos en móvil, bajos clics)" | Diseño inconsistente |
| **Audiencia** | "¿Quién recibe estos emails? (clientes, suscriptores, equipo interno)" | Clientes y suscriptores |

---

## Fase 2: Arquitectura de Sistema

### Plantillas Base a Diseñar

1. **Plantilla de Boletín** — contenido editorial + promoción
2. **Plantilla Transaccional** — confirmación, envío, receipt
3. **Plantilla Transaccional de Onboarding** — bienvenida, educación
4. **Plantilla Promocional** — venta, flash, especial
5. **Plantilla de Anuncio** — noticia importante, cambio

### Estándares de Diseño

- **Ancho de contenido:** 600px máximo (mejor para Outlook)
- **Márgenes:** 20px izquierda/derecha mínimo
- **Tipo:** Sans-serif para cuerpo (Arial, Helvetica, -apple-system)
- **Tamaño de tipo:** 14-16px base
- **Altura de línea:** 1.5 mínimo para legibilidad
- **Colores:** Máximo 3 colores primarios
- **Botones:** 44px altura mínimo, padding 10px/20px

### Reglas Responsivas

- **Mobile:** Stack de una sola columna
- **Márgenes:** Reducir a 15px en móvil
- **Tipo:** 12px mínimo, nunca zoom needed
- **Imágenes:** 100% width con max-width
- **CTAs:** Full-width buttons en móvil

---

## Fase 3: Componentes Estándar

### Encabezado

```
- Logo (100px alt height)
- Navegación opcional (máximo 5 links)
- Fondo: Color de marca o blanco
```

### Pie

```
- Enlace unsubscribe (legalmente requerido)
- Información de contacto
- Redes sociales opcionales
- Dirección de empresa
```

### Botones de CTA

```
- Padding: 10px 20px
- Radio de borde: 4px
- Color: Contraste 4.5:1 con fondo
- Hover state definido
- Móvil: Full-width
```

---

## Anti-Patrones

- **Imágenes de texto** — no accesible, no seleccionable
- **Fondos oscuros** — rompen en dark mode
- **Sin enlace unsubscribe** — requerimiento legal y reduce spam reports
- **Demasiados colores** — confunde y se siente desordenado
- **Tablas anidadas profundas** — rompen fácilmente

---

## Checklist de Implementación

- [ ] Plantillas base creadas para cada tipo
- [ ] Testeado en Outlook, Gmail, Apple Mail, móvil
- [ ] Guía de estilo documentada para usuarios
- [ ] Código fuente y templates descargables
- [ ] Documentación de componentes reutilizables
