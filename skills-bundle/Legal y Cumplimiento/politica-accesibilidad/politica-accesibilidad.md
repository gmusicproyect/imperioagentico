---
name: politica-accesibilidad
description: "Redacta políticas de accesibilidad web con compromisos de cumplimiento WCAG y procedimientos de acomodación. Usa cuando crees una declaración de accesibilidad para tu sitio web."
allowed-tools: Read Write Glob
metadata:
  author: Imperio Digital
  version: "1.0"
---

# Política de Accesibilidad

## Cuándo Usar Este Skill

Usa este skill cuando necesites:
- Escribir una declaración o política de accesibilidad web
- Documentar tus compromisos de cumplimiento WCAG
- Crear procedimientos para solicitudes de acomodación
- Esbozar tu enfoque de accesibilidad digital

**NO USES** este skill para auditorías de accesibilidad técnica, remediación WCAG, o consultoría de cumplimiento ADA. Esto es para el documento de política en sí.

---

## Principio Fundamental

UNA POLÍTICA DE ACCESIBILIDAD DEMUESTRA TU COMPROMISO CON LA INCLUSIÓN — LE DICE A LOS USUARIOS CON DISCAPACIDADES QUÉ ESPERAR Y CÓMO OBTENER AYUDA CUANDO ALGO NO FUNCIONA.

---

## Fase 1: Información Requerida

### Información Requerida

| Entrada | Qué Preguntar | Por Defecto |
|---------|---------------|------------|
| **URL del sitio web** | "¿Para qué sitio web es esta política?" | Sin defecto — debe proporcionarse |
| **Nombre del negocio** | "¿Cuál es tu nombre de negocio?" | Sin defecto — debe proporcionarse |
| **Objetivo WCAG** | "¿Qué nivel WCAG buscas? (A, AA, AAA)" | WCAG 2.1 Level AA |
| **Limitaciones conocidas** | "¿Hay problemas de accesibilidad conocidos?" | Ninguno identificado |
| **Contacto de accesibilidad** | "¿Quién gestiona solicitudes de accesibilidad? (nombre, email, teléfono)" | Sin defecto — debe proporcionarse |

**PUNTO DE CONTROL:** No procedas sin nombre del negocio, sitio web e información de contacto.

---

## Fase 2: Documento de Política

```
## Declaración de Accesibilidad

**[Nombre del Negocio]** se compromete a garantizar accesibilidad digital
para personas con discapacidades. Continuamente trabajamos para mejorar
la experiencia del usuario para todos y aplicamos estándares de
accesibilidad relevantes.

### Estado de Conformidad

Nos propusimos cumplir con las Pautas de Accesibilidad de Contenido Web
(WCAG) 2.1 en el Nivel [AA]. Estas pautas explican cómo hacer contenido
web más accesible para personas con discapacidades, incluyendo aquellas
con discapacidades visuales, auditivas, físicas, del habla, cognitivas,
lingüísticas, de aprendizaje y neurológicas.

### Medidas Que Tomamos

[Nombre del Negocio] toma las siguientes medidas para garantizar
accesibilidad:

- Incluir accesibilidad como parte de nuestro proceso de diseño y desarrollo
- Proporcionar capacitación continua en conciencia de accesibilidad a nuestro equipo
- Usar herramientas de prueba automatizadas y manuales para evaluar accesibilidad
- Buscar comentarios de usuarios sobre accesibilidad de nuestras propiedades digitales
- Revisar y actualizar nuestras prácticas de accesibilidad regularmente

### Especificaciones Técnicas

Este sitio web se basa en las siguientes tecnologías para conformidad
con WCAG 2.1:
- HTML
- CSS
- JavaScript
- WAI-ARIA

Estas tecnologías se emplean para accesibilidad con las tecnologías de asistencia y
agentes de usuario que utilizan nuestros usuarios.

### Limitaciones Conocidas

Aunque nos esforzamos por accesibilidad completa, algunas áreas de nuestro sitio
web pueden no ser completamente accesibles aún:

[Enumera limitaciones conocidas, p. ej.:]
- [El contenido de terceros (videos incrustados, feeds de redes sociales) puede no
  cumplir completamente con estándares de accesibilidad]
- [Los documentos PDF más antiguos pueden no ser completamente accesibles — estamos
  trabajando en remediar esto]
- [Algunos elementos interactivos se están actualizando para mejorar compatibilidad
  con lectores de pantalla]

Estamos trabajando activamente para resolver estos problemas. Si encuentras una
barrera, por favor contáctanos.

### Comentarios y Solicitudes de Acomodación

Agradecemos tus comentarios sobre la accesibilidad de [sitio web/negocio].
Si encuentras barreras de accesibilidad o necesitas acomodaciones,
por favor contáctanos:

- **Email:** [correo de accesibilidad]
- **Teléfono:** [número de teléfono]
- **Dirección postal:** [dirección]

Nos proponemos responder a comentarios de accesibilidad dentro de [2-5] días hábiles.

### Compatibilidad

Nuestro sitio web está diseñado para ser compatible con las siguientes
tecnologías de asistencia:
- Lectores de pantalla (JAWS, NVDA, VoiceOver)
- Software de ampliación de pantalla
- Software de reconocimiento de voz
- Navegación solo con teclado

### Evaluación y Revisión de Cumplimiento

La accesibilidad de este sitio web fue evaluada por última vez el [fecha] usando:
- [Herramientas de prueba automatizadas usadas, p. ej., axe, WAVE, Lighthouse]
- [Prueba manual, p. ej., navegación con teclado, prueba de lector de pantalla]
- [Auditoría de terceros, si aplica]

Revisamos nuestras prácticas de accesibilidad [anualmente / semestralmente].

### Aplicación

Si no estás satisfecho con nuestra respuesta a tu preocupación de accesibilidad,
puedes escalar contactando [autoridad apropiada o resolución alternativa de disputas].

---

Esta declaración fue actualizada por última vez el [fecha].
```

---

## Fase 3: Lista de Verificación de Implementación

```
## Lista de Verificación de Implementación de Accesibilidad

### Contenido
- [ ] Todas las imágenes tienen texto alternativo descriptivo
- [ ] Los videos tienen subtítulos y/o transcripciones
- [ ] El color no es el único medio para transmitir información
- [ ] El texto tiene suficiente contraste de color (4.5:1 mínimo para texto normal)
- [ ] El contenido es legible y funcional al 200% de zoom
- [ ] Los enlaces son descriptivos (no "haz clic aquí")

### Navegación
- [ ] Todos los elementos interactivos son accesibles con teclado
- [ ] Los indicadores de enfoque son visibles
- [ ] Se proporciona un enlace para saltar la navegación
- [ ] La estructura de la página usa jerarquía de encabezados apropiada (H1, H2, H3)
- [ ] Se usan puntos de referencia ARIA apropiadamente

### Formularios
- [ ] Todos los campos de formulario tienen etiquetas asociadas
- [ ] Los mensajes de error son claros y asociados con el campo relevante
- [ ] Los campos obligatorios están claramente indicados
- [ ] Se proporcionan instrucciones de formulario antes del formulario

### General
- [ ] Declaración de accesibilidad publicada y vinculada desde el pie de página
- [ ] La información de contacto para comentarios de accesibilidad es clara
- [ ] El equipo está capacitado en crear contenido accesible
- [ ] Se programan auditorías de accesibilidad regulares
```

---

## Fase 4: Entrega

Publica la declaración de accesibilidad en una página dedicada (p. ej., /accesibilidad) y vincula desde el pie de página del sitio web.

---

## Ejemplo: Tienda de E-commerce

**Fragmento de declaración:** "ShopBright se compromete con cumplimiento WCAG 2.1 Nivel AA. Nuestro proceso de compra soporta navegación con teclado y lectores de pantalla. Las imágenes de productos incluyen texto alternativo descriptivo. Limitación conocida: algunos videos de productos proporcionados por vendedores carecen de subtítulos — estamos trabajando con vendedores para agregarlos. Contacta a accessibility@shopbright.com para solicitudes de acomodación."

---

## Anti-Patrones

- **Promesas vacías** — afirmar que cumples con WCAG AA cuando tu sitio no ha sido probado es engañoso y legalmente riesgoso
- **Sin información de contacto** — la parte más importante de una declaración de accesibilidad es cómo los usuarios pueden reportar problemas y obtener ayuda
- **Configurar y olvidar** — la accesibilidad requiere atención continua mientras cambia el contenido y las características
- **Política sin acción** — publicar una declaración sin probar y arreglar realmente problemas de accesibilidad proporciona falsa comodidad
- **Ignorar contenido de terceros** — videos incrustados, feeds sociales y widgets también deben ser accesibles o ser divulgados como limitaciones

---

## Recuperación

- **No se ha realizado prueba de accesibilidad:** Ejecuta un escaneo automatizado gratuito (WAVE, axe, Lighthouse) para identificar problemas mayores. Arregla primero elementos críticos (navegación con teclado, texto alternativo, contraste de color).
- **Recibió una carta de demanda ADA:** Consulta a un abogado inmediatamente. Inicia remediación y documenta tus esfuerzos.
- **Las herramientas de terceros no son accesibles:** Contacta a vendedores sobre accesibilidad. Si no pueden cumplir, considera alternativas o divulga como limitación conocida.
- **Presupuesto limitado para accesibilidad:** Enfócate en elementos de mayor impacto: navegación con teclado, texto alternativo, estructura de encabezados y contraste de color. Estos abordan las barreras más comunes.
