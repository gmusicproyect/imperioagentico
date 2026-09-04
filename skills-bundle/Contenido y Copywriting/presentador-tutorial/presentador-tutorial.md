---
name: presentador-tutorial
description: "Crea tutoriales paso a paso con marcadores de captura de pantalla, fragmentos de código y secciones de solución de problemas. Úsalo cuando necesites escribir una guía de cómo hacer, documentación de ayuda, tutorial de incorporación o tutorial educativo."
allowed-tools: Read Grep Glob Bash Write Edit
metadata:
  author: Imperio Digital
  version: "1.0"
---

# Presentador de Tutoriales

## Cuándo Usar Esta Habilidad

Usa esta habilidad cuando:
- Necesites una guía de cómo hacer para tu producto o herramienta
- Quieras crear documentación de ayuda o artículo de base de conocimientos
- Estés construyendo un tutorial de incorporación para nuevos clientes
- Necesites un tutorial técnico con ejemplos de código
- Quieras documentar un proceso con referencias visuales claras
- Se te pida contenido educativo con instrucciones paso a paso

## Principio Fundamental

CADA PASO DEBE PASAR LA PRUEBA "¿PUEDO HACER ESTO AHORA MISMO?" — SI UN LECTOR NO PUEDE TOMAR ACCIÓN INMEDIATA DE UN PASO, EL PASO ES DEMASIADO VAGO.

## Workflow

### Fase 1: Define el Alcance del Tutorial

1. Identifica el tema del tutorial y nivel de habilidad del lector objetivo (principiante, intermedio, avanzado)
2. Define el único resultado que el lector logrará al final
3. Lista los requisitos previos que el lector necesita antes de comenzar
4. Estima el tiempo de finalización para el tutorial completo

Pregunta al usuario:
- ¿Qué está tratando de lograr el lector?
- ¿Qué ya saben al llegar?
- ¿Qué herramienta/plataforma/idioma está involucrado?

### Fase 2: Esquema los Pasos

5. Divide el proceso en 5-12 pasos principales
6. Ordena los pasos cronológicamente
7. Identifica dónde las capturas de pantalla o visuals ayudarían
8. Nota cualquier punto de decisión donde el lector podría tomar caminos diferentes

### Fase 3: Escribe Cada Paso

9. Escribe cada paso usando esta estructura:
   - **Título del paso** como encabezado (verbo de acción + objeto)
   - Una oración explicando POR QUÉ importa este paso
   - Sub-pasos numerados con rutas UI exactas o comandos
   - Marcador de captura de pantalla donde se necesita confirmación visual
   - Resultado esperado después de completar el paso
   - Llamada de error común si es aplicable

10. Para fragmentos de código, siempre incluye:
    - El bloque de código completo (no fragmentos)
    - Identificador de idioma en la valla de código
    - Comentarios en línea explicando líneas no obvias
    - Resultado esperado o salida

### Fase 4: Agrega Solución de Problemas

11. Crea una sección "Solución de Problemas" al final cubriendo:
    - 3-5 errores más comunes o puntos de confusión
    - Mensajes de error exactos que el lector podría ver
    - Pasos para solucionar cada problema
    - Ruta de escalada "Si esto no funciona"

12. Agrega una sección "Qué Sigue" enlazando a tutoriales lógicos o recursos de seguimiento

### Fase 5: Formato y Pulido

13. Agrega un título, tiempo estimado, nivel de dificultad y requisitos previos en la parte superior
14. Asegúrate de que cada marcador de captura de pantalla tiene una etiqueta descriptiva
15. Agrega contraseñas callout de consejo/advertencia/nota usando formato de cita de bloque
16. Revisa jerga — reemplaza o define cualquier término que un principiante no conocería

## Formato de Salida

```markdown
# Cómo [Lograr Resultado Específico]

**Dificultad:** Principiante | Intermedio | Avanzado
**Tiempo:** X minutos
**Requisitos Previos:** [Lista qué se necesita]

---

## Paso 1: [Verbo de Acción] + [Objeto]

Por qué importa: [una oración].

1. Ve a **Configuración > Cuenta > Claves API**
2. Haz clic en **Generar Nueva Clave**
3. Nombra tu clave `production-api`

[CAPTURA DE PANTALLA: Panel de Claves API mostrando botón Generar Nueva Clave]

**Resultado esperado:** Ves una nueva clave comenzando con `sk-` en tu lista de claves.

> **Error común:** No copies el ID de clave — copia el valor de clave completo que comienza con `sk-`.
```

## Ejemplo: Tutorial de Configuración de Integración API

```markdown
# Cómo Conectar Tu Aplicación a Nuestra API

**Dificultad:** Intermedio
**Tiempo:** 10 minutos
**Requisitos Previos:** Cuenta activa, JavaScript básico

## Paso 1: Genera tu Clave API

Por qué importa: Tu clave API autentica todas tus solicitudes a nuestro servicio.

1. Inicia sesión en tu panel de control
2. Ve a **Desarrollador > Claves API**
3. Haz clic en **Nueva Clave**
4. Nombra la clave (p. ej., "producción")

[CAPTURA DE PANTALLA: Panel mostrando nueva clave generada]

**Resultado esperado:** Ves una clave de 32 caracteres en formato `sk-xxxx`.

> **Consejo:** Copia toda la clave ahora — no podrás verla de nuevo.
```

## Anti-Patrones

- **Demasiado asunción de conocimiento** — explica cada término técnico o vincúlalo a referencias
- **Pasos incompletos** — cada paso debe permitir al lector progresar sin adivinar
- **Sin capturas de pantalla** — los tutoriales visuales sin imágenes son frustrantes
- **Sin sección de solución de problemas** — los lectores se quedan atrapados y se van
- **Sin resultado esperado** — los lectores no saben si completaron el paso correctamente

## Recuperación

- **El usuario no tiene las imágenes capturadas:** Incluye marcadores detallados para que las capturen durante la filmación
- **El proceso tiene muchas variaciones:** Nota "Si estás en [plataforma/versión], salta al Paso X"
- **El tutorial se está haciendo demasiado largo:** Divide en "Parte 1" y "Parte 2" o vincula a tutoriales de seguimiento
- **Muchos términos técnicos:** Crea un glosario vinculado al principio

## Checklist de Calidad de Tutorial

```
## Tutorial Checklist

- [ ] Alcance está claramente definido — un resultado específico al final
- [ ] Requisitos previos están listados (qué necesita saber el lector antes)
- [ ] Cada paso tiene título con verbo de acción
- [ ] Cada paso explica por qué importa (contexto del usuario)
- [ ] Los pasos son cronológicos y nunca se saltan hacia adelante
- [ ] Cada paso incluye resultado esperado
- [ ] Las capturas de pantalla están marcadas con descripciones claras
- [ ] Los fragmentos de código tienen comentarios en línea
- [ ] La sección de solución de problemas cubre errores comunes
- [ ] El "Qué Sigue" vincula a recursos o tutoriales relacionados
- [ ] No hay jerga sin definir o está simplificada
```

## Métricas de Éxito

Un tutorial exitoso tiene:
- Tasa de finalización alta (lectores completando todos los pasos)
- Bajo número de preguntas de soporte sobre pasos básicos
- Comentarios positivos sobre claridad
- Bajo rebote (lectores que no abandonan a mitad del tutorial)

Si los tutoriales tienden a abandonarse en un paso específico, ese paso probablemente necesita aclaración o división en pasos más pequeños.
