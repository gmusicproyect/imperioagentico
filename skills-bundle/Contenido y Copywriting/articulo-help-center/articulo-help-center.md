---
name: articulo-help-center
description: "Escribe artículos del centro de ayuda con instrucciones paso a paso, marcadores de posición de captura de pantalla y secciones de solución de problemas para autoservicio del cliente."
allowed-tools: Read Write Glob
metadata:
  author: Imperio Digital
  version: "1.0"
---

# Artículo del Centro de Ayuda

## Cuándo Usar Esta Skill

Usa esta skill cuando necesites:
- Escribir un artículo de centro de ayuda o base de conocimientos orientado al cliente
- Crear instrucciones paso a paso con marcadores de posición de captura de pantalla
- Construir guías de solución de problemas para problemas comunes del cliente
- Reducir el volumen de tickets de soporte habilitando el autoservicio

**NO USES** esta skill para procedimientos operativos internos (usa knowledge-base-builder), publicaciones de blog o plantillas de respuesta de soporte. Esta es para documentación de autoservicio orientada al cliente.

---

## Principio Fundamental

UN ARTÍCULO DEL CENTRO DE AYUDA DEBE RESPONDER LA PREGUNTA DEL CLIENTE SIN NECESIDAD DE QUE SE COMUNIQUE CON EL SOPORTE — SI AÚN NECESITAN ENVIARTE UN CORREO DESPUÉS DE LEERLO, EL ARTÍCULO FALLÓ.

---

## Fase 1: Resumen del Artículo

Define qué cubrirá el artículo y para quién.

### Información Requerida

| Entrada | Qué Preguntar | Predeterminado |
|---------|---------------|--------|
| **Tema** | "¿Qué pregunta o tarea aborda este artículo?" | Sin predeterminado |
| **Audiencia** | "¿Cuál es el nivel de habilidad técnica del cliente?" | Amigable para principiantes |
| **Tipo de artículo** | "¿Es esto un instruccional, guía de solución de problemas, FAQ o explicador conceptual?" | Instruccional |
| **Artículos relacionados** | "¿Hay algún artículo relacionado para enlazar?" | Ninguno |
| **Errores comunes** | "¿Qué es lo que los clientes suelen hacer mal con esto?" | Sin predeterminado |

**PUNTO DE CONTROL: Confirma el resumen del artículo antes de escribir.**

---

## Fase 2: Escribir Artículo

Crea el artículo siguiendo las mejores prácticas del centro de ayuda.

### Plantilla de Artículo Instruccional

```
# Cómo [Nombre de la Tarea]

**Última actualización:** [Fecha]
**Se aplica a:** [Nivel de plan / versión de producto / rol de usuario]
**Tiempo requerido:** [X minutos]

## Descripción General

[1-2 oraciones: qué cubre este artículo y el resultado final]

## Antes de Comenzar

- [Requisito previo 1 — qué necesita el cliente antes de comenzar]
- [Requisito previo 2]

## Pasos

### Paso 1: [Acción]

[1-2 oraciones de instrucción]

[Captura de pantalla: Descripción de lo que el cliente debe ver]

### Paso 2: [Acción]

[1-2 oraciones de instrucción]

[Captura de pantalla: Descripción de lo que el cliente debe ver]

### Paso 3: [Acción]

[1-2 oraciones de instrucción]

**Resultado:** [Lo que el cliente debe ver cuando completa este paso]

## Solución de Problemas

### [Problema común 1]

**Síntoma:** [Lo que ve el cliente]
**Causa:** [Por qué sucede]
**Solución:** [Solución paso a paso]

### [Problema común 2]

**Síntoma:** [Lo que ve el cliente]
**Solución:** [Solución]

## Artículos Relacionados

- [Título del artículo y enlace]
- [Título del artículo y enlace]

## ¿Aún Necesitas Ayuda?

Si estos pasos no resolvieron tu problema, [enlace de contacto con soporte] e incluye:
- [Información a incluir: captura de pantalla, mensajes de error, detalles de cuenta]
```

### Plantilla de Guía de Solución de Problemas

```
# Solución de Problemas: [Nombre del Problema]

## Soluciones Rápidas

Intenta estas primero (la mayoría de los problemas se resuelven aquí):

1. [Solución rápida 1 — ej., "Borra el caché del navegador y actualiza"]
2. [Solución rápida 2 — ej., "Cierra sesión e inicia de nuevo"]
3. [Solución rápida 3]

## Soluciones Detalladas

### Si ves [Error/Síntoma A]

**Causa:** [Explicación]
**Solución:**
1. [Paso]
2. [Paso]

### Si ves [Error/Síntoma B]

**Causa:** [Explicación]
**Solución:**
1. [Paso]
2. [Paso]

## ¿Aún No Funciona?

Contacta con soporte en [enlace] con:
- Qué estabas intentando hacer
- El mensaje de error exacto (captura de pantalla preferida)
- Tu tipo de navegador y dispositivo
```

**PUNTO DE CONTROL: Presenta el borrador del artículo para revisión.**

---

## Fase 3: Optimizar

Mejora el artículo para descubribilidad y usabilidad.

### Optimización de SEO y Búsqueda

- **Título:** Usa las palabras exactas que buscarían los clientes
- **Meta descripción:** Resume la respuesta en 1 oración
- **Etiquetas/categorías:** Añade etiquetas relevantes para búsqueda interna

### Lista de Verificación de Legibilidad

```
- [ ] El título coincide con lo que un cliente escribiría en una barra de búsqueda
- [ ] Los pasos están numerados y cada paso tiene UNA acción
- [ ] Las capturas de pantalla (o marcadores de posición) muestran lo que el cliente debe ver
- [ ] Sin jerga — si es necesario un término técnico, defínelo
- [ ] El artículo está bajo 500 palabras (los artículos más largos deben dividirse)
- [ ] La sección de solución de problemas cubre los 2-3 problemas principales
- [ ] La sección "¿Aún necesitas ayuda?" incluye una ruta de contacto clara
- [ ] Los artículos relacionados están enlazados para exploración más profunda
```

### Reglas de Escritura

- Usa lenguaje "tú": "Haz clic en el botón Configuración" no "El usuario debe hacer clic en Configuración"
- Una acción por paso — nunca combines dos acciones en un paso
- Enfatiza el elemento clickeable: "Haz clic en **Guardar Cambios**"
- Usa tiempo presente: "La página muestra..." no "La página mostrará..."
- Incluye el aspecto del éxito: "Debes ver un mensaje de confirmación en verde"

---

## Fase 4: Mantener

Mantén los artículos precisos y relevantes.

### Disparadores de Mantenimiento

Actualiza el artículo cuando:
- La interfaz de usuario del producto cambia
- Una nueva característica afecta el workflow
- Los tickets de soporte hacen referencia a este artículo con confusión
- Las capturas de pantalla se vuelven obsoletas

### Métricas de Rendimiento

```
| Métrica | Objetivo | Actual |
|--------|--------|---------|
| Vistas de artículo por mes | Tendencia al alza | — |
| Tickets de soporte en este tema | Tendencia a la baja | — |
| Calificación de utilidad del artículo | 80%+ positivo | — |
| Tiempo promedio en el artículo | 1-3 minutos | — |
```

---

## Anti-Patrones

- **Pared de texto sin pasos** — los clientes escanean, no leen párrafos. Usa pasos numerados y encabezados.
- **Asumir conocimiento** — "Navega a la configuración de API" asume que el cliente sabe qué es una API y dónde encontrarla.
- **Capturas de pantalla obsoletas** — nada erosiona la confianza más rápido que instrucciones que no coinciden con lo que ve el cliente.
- **Enterrar la respuesta** — pon la solución más común primero. No hagas que los clientes lean 500 palabras para encontrar una solución de 1 oración.
- **Sin vía de escape** — cada artículo necesita un "¿Aún necesitas ayuda? Contáctanos" al final.

---

## Recuperación

- **Los clientes aún contactan con soporte sobre un tema documentado:** El artículo es difícil de encontrar, difícil de entender o carece de un escenario común. Revisa y revisa.
- **El usuario no tiene capturas de pantalla aún:** Usa marcadores de posición de descripción: `[Captura de pantalla: La página de Configuración con la pestaña "Facturación" resaltada]`. Añade capturas de pantalla reales después.
- **El artículo es demasiado largo:** Divide en múltiples artículos. Un instruccional y una guía de solución de problemas son mejores como dos artículos que uno mega-artículo.
- **El usuario no sabe qué documentar primero:** Comienza con los 5 temas principales de tickets de soporte. Cada uno se convierte en un artículo.
- **El centro de ayuda no recibe tráfico:** Enlaza artículos relevantes en correos de incorporación, respuestas de soporte e interfaz de usuario del producto.
