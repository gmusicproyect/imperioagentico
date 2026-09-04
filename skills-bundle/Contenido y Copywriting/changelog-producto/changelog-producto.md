---
name: changelog-producto
description: "Crea formatos de changelog de producto con notas de versión, categorización (nuevo, mejorado, reparado) y lenguaje amigable para usuarios. Usa cuando documentes actualizaciones de producto para usuarios."
allowed-tools: Read Write Glob
metadata:
  author: Imperio Digital
  version: "1.0"
---

# Changelog de Producto

## Cuándo Usar Esta Skill

Usa esta skill cuando necesites:
- Crear un formato de changelog y plantilla para actualizaciones de producto continuas
- Escribir notas de versión amigables para usuarios para un lanzamiento de producto
- Categorizar cambios en nuevas características, mejoras y correcciones de errores
- Establecer una cadencia y estilo de changelog consistente

**NO USES** esta skill para notas de lanzamiento internas (orientadas a ingeniería), anuncios de características (orientados al marketing) o documentación técnica de API. Esto es para changelogs de producto orientados al usuario.

---

## Principio Fundamental

UN CHANGELOG CONSTRUYE CONFIANZA DEL USUARIO MOSTRANDO MEJORA CONTINUA — ESCRIBE CADA ENTRADA PARA QUE UN USUARIO NO TÉCNICO ENTIENDA QUÉ CAMBIÓ Y POR QUÉ IMPORTA PARA ELLOS.

---

## Fase 1: Resumen Inicial

### Información Requerida

| Entrada | Qué Preguntar | Predeterminado |
|---------|---------------|--------|
| **Nombre de producto** | "¿Para qué producto es este changelog?" | Sin predeterminado — debe proporcionarse |
| **Frecuencia de actualización** | "¿Con qué frecuencia envías actualizaciones? ¿Semanalmente, quincenalmente, mensualmente?" | Quincenalmente |
| **Audiencia** | "¿Leen los lectores del changelog contenido técnico o no técnico?" | Usuarios comerciales no técnicos |
| **Cambios actuales** | "Lista los cambios en esta actualización — características, mejoras y correcciones." | Sin predeterminado — debe proporcionarse |
| **Numeración de versión** | "¿Usas números de versión, fechas o ambos?" | Basado en fecha (ej., 15 de Enero de 2026) |
| **Distribución** | "¿Dónde vive el changelog? ¿En la app, blog, correo, página dedicada?" | Página de changelog dedicada |

**PUNTO DE CONTROL: Confirma el resumen antes de escribir.**

---

## Fase 2: Estructura

### Sistema de Categorización

Todo cambio entra en una de estas categorías:

- **Nuevo** — Características o capacidades que no existían antes
- **Mejorado** — Mejoras a características existentes (rendimiento, UX, funcionalidad expandida)
- **Reparado** — Correcciones de errores y resoluciones de problemas
- **Eliminado** (usar con moderación) — Características deprecadas con guía de migración

### Formato de Entrada

Cada entrada de changelog sigue esta estructura:

```
### [Fecha o Versión]

**Nuevo**
- **[Nombre de característica]** — [Qué hace y por qué importa en una oración]

**Mejorado**
- **[Nombre de característica]** — [Qué cambió y el beneficio del usuario]

**Reparado**
- **[Descripción del problema]** — [Qué estaba roto y confirmación de que está resuelto]
```

**PUNTO DE CONTROL: Confirma el sistema de categorización y formato antes de escribir entradas.**

---

## Fase 3: Escribir

### Reglas de Escritura

- **Comienza con el beneficio, no con el cambio técnico.** "Las facturas ahora se envían 3x más rápido" supera a "Procesamiento optimizado de cola de facturas."
- **Una oración por entrada.** Si necesita más, merece un anuncio de característica.
- **Usa voz activa.** "Ahora puedes exportar a PDF" no "Se ha añadido exportación a PDF."
- **Sé específico sobre correcciones.** "Reparado: Los correos con adjuntos mayores de 5MB no se podían enviar" no "Corrección de error de correo."
- **Agrupa cambios relacionados.** Si 3 correcciones se relacionan con la misma característica, enuméralas bajo un subtítulo.

### Guía de Tono

- Conversacional pero profesional
- Celebratorio para características grandes ("Hemos estado trabajando en esto durante meses...")
- Práctico para correcciones (reconoce, confirma reparado, continúa)
- Sin disculpas por errores — solo repara y declara claramente

### Guía de Largo de Entrada

| Categoría | Largo | Nivel de Detalle |
|----------|--------|-------------|
| Característica nueva importante | 2-3 oraciones | Beneficio + cómo acceder |
| Mejora menor | 1 oración | Qué cambió + beneficio |
| Corrección de error | 1 oración | Qué estaba roto + resuelto |
| Deprecación | 2-3 oraciones | Qué, cuándo, ruta de migración |

---

## Fase 4: Pulir

### 1. Plantilla de Página de Changelog

Proporciona un diseño de página recomendado:
- Nombre de producto e encabezado "Changelog" o "Novedades"
- Filtro/búsqueda por categoría (Nuevo, Mejorado, Reparado)
- Opción de suscripción (correo o RSS)
- Archivo con meses expandibles o paginación
- Enlace a roadmap o dashboard de solicitud de características

### 2. Plan de Distribución

- **En-app:** Notificación de insignia en enlace de changelog cuando existan nuevas entradas
- **Correo:** Resumen mensual de cambios para suscriptores
- **Redes sociales:** Características principales destacadas en una publicación dedicada
- **Blog:** Artículo completo solo para lanzamientos importantes

### 3. Lista de Verificación de Calidad

```
## Lista de Verificación de Calidad de Changelog

- [ ] Cada entrada comienza con un beneficio, no una descripción técnica
- [ ] Los cambios están categorizados como Nuevo, Mejorado o Reparado
- [ ] Cada entrada es una oración (características importantes pueden usar 2-3)
- [ ] Voz activa utilizada en toda
- [ ] Las correcciones de errores describen específicamente qué estaba roto
- [ ] Sin jerga — legible por usuarios no técnicos
- [ ] Se incluye número de fecha o versión
- [ ] Las características deprecadas incluyen guía de migración
- [ ] Existe opción de suscripción/notificación para la página de changelog
```

---

## Ejemplo

```
### 15 de Febrero de 2026

**Nuevo**
- **Facturas recurrentes** — Establece cualquier factura para enviarse automáticamente en un cronograma (semanal, mensual o personalizado). Encuéntralo bajo Configuración de Factura.
- **Portal de cliente** — Tus clientes ahora pueden ver todas sus facturas e historial de pagos en un solo lugar. Comparte el enlace desde cualquier perfil de cliente.

**Mejorado**
- **Velocidad de carga del panel** — El panel ahora carga 60% más rápido, especialmente para cuentas con 500+ facturas.
- **Exportaciones CSV** — Las exportaciones ahora incluyen columnas de estado de pago y fecha por defecto.

**Reparado**
- **Cálculo de impuesto en artículos con descuento** — Los impuestos se calculaban antes del descuento, resultando en sobrecargos. Ahora calcula correctamente en el monto con descuento.
- **Notificaciones de correo** — Algunos usuarios no recibían correos de confirmación de pago. Resuelto para todas las cuentas.
```

---

## Anti-Patrones

- **Jerga técnica** — "Refactorizado el manejador de webhook" no significa nada para usuarios. Traduce a impacto.
- **Descripciones vagas de correcciones** — "Reparado un error" no dice nada a los usuarios. Sé específico sobre qué estaba roto.
- **Omitir actualizaciones** — los changelogs inconsistentes erosionan la confianza. Envía en tu cadencia establecida, incluso si es una actualización pequeña.
- **Relleno de marketing en changelogs** — guarda la exageración para anuncios de características. Los changelogs deben ser factuales y escaneables.
- **Sin categorización** — una lista plana de cambios es difícil de escanear. Siempre categoriza.

---

## Recuperación

- **Muy pocos cambios en este ciclo:** Combina con el siguiente ciclo, o envía una actualización breve notando mejoras y trabajo de fondo.
- **Se incluye cambio de ruptura:** Abre con el cambio de ruptura, explica qué deben hacer los usuarios y proporciona un enlace a guía de migración.
- **Error reportado por usuario es reparado:** Considera nombrar la corrección de una forma que reconozca el reporte: "Reparado (¡gracias por reportar!): [descripción]."
- **Aún no existe changelog:** Crea una entrada de lanzamiento retroactiva resumiendo las capacidades actuales del producto, luego comienza actualizaciones regulares.
