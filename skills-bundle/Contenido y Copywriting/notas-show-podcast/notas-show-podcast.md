---
name: notas-show-podcast
description: "Transforma transcripciones de podcast o video en notas de episodio estructuradas con timestamps, puntos clave, enlaces de recursos, biografías de invitados, citas destacadas y descripciones de episodios optimizadas para SEO. Úsalo cuando tengas una transcripción o resumen de grabación y necesites notas pulidas para tu página de episodios de podcast."
allowed-tools: Read Write Glob Grep
metadata:
  author: Imperio Digital
  version: "1.0"
---

# Notas de Episodios de Podcast

## Cuándo Usar Esta Habilidad

Usa esta habilidad cuando necesites:
- Convertir una transcripción bruta de podcast o video en notas listas para publicar
- Generar timestamps, puntos clave y citas destacadas de una conversación grabada
- Escribir una descripción de episodio optimizada para SEO para Apple Podcasts, Spotify o YouTube
- Extraer biografías de invitados y enlaces de recursos mencionados durante un episodio

**NO** uses esta habilidad para:
- Escribir un guión de podcast antes de grabar (usa una habilidad de video-script en su lugar)
- Editar transcripciones brutas para legibilidad (esto produce notas, no transcripciones limpias)
- Crear clips de redes sociales o activos promocionales de episodios (usa una habilidad de repurposing-contenido)

---

## Cómo Funciona

CADA CONJUNTO DE NOTAS DEBE DERIVARSE DE LA TRANSCRIPCIÓN ACTUAL -- NUNCA INVENTES TIMESTAMPS, CITAS O AFIRMACIONES QUE NO ESTÉN EN EL MATERIAL FUENTE.

---

### Paso 1: Entender -- Lee y Analiza la Transcripción

1. **Obtén la transcripción.** Acepta rutas de archivo (`.txt`, `.md`, `.srt`, `.vtt`), texto pegado o notas de grabación. Lee archivos con `Read` o `Glob`.
2. **Pide contexto del episodio** si no se proporciona: número de episodio, nombre de serie, nombre y título del invitado, audiencia objetivo, enlaces específicos para incluir.
3. **Identifica elementos centrales:** tema del episodio, identidad del invitado, 3-5 temas clave, formato del episodio (entrevista, solo, panel).
4. **Presenta la descripción general para confirmación:**

```
## Descripción General del Episodio

**Formato:** Entrevista
**Tema:** Cómo construir un motor de referencia sin anuncios pagados
**Invitado:** Sarah Chen, fundadora de GrowthLoop
**Temas Clave:**
1. Por qué los referidos superan el alcance frío
2. La secuencia de solicitud de referencia de 3 emails
3. Construir incentivos de referencia que se sientan genuinos
4. Seguimiento de referencia de baja tecnología

¿Procedo a extraer timestamps y notas? ¿Está confirmado?
```

**PUNTO DE CONTROL: No procedas hasta que el usuario confirme que la descripción general es precisa.**

---

### Paso 2: Extraer -- Extrae Datos Estructurados de la Transcripción

#### Timestamps
- Usa códigos de tiempo existentes de SRT/VTT/timestamps en línea cuando estén disponibles
- Si no existen timestamps, estima a partir del conteo de palabras a 150 palabras por minuto y marca como `[aprox]`
- Formato: `[MM:SS]` bajo 1 hora, `[HH:MM:SS]` sobre 1 hora
- Marca: introducción, cada cambio de tema principal, historias notables/tangentes, cierre/CTA

#### Puntos Clave (3-7)
- Cada uno debe ser una declaración independiente, completa y viable
- Representa insights distintos del episodio (sin duplicados)

#### Citas Destacadas (2-4)
- Palabras exactas de la transcripción -- nunca parafraseadas
- Menos de 280 caracteres (compartibles en redes sociales)
- Atribuidas al orador correcto

#### Recursos Mencionados
- Nombre exactamente como se declaró; agrega URL si es bien conocida o se declaró en la transcripción
- Marca URLs desconocidas como `[URL requerida]`

#### Biografía del Invitado (solo episodios de entrevista)
- 2-3 oraciones de lo que se dijo en el episodio
- Incluye nombre, rol, una credencial y dónde encontrarlos
- **NUNCA fabrique credenciales o identificadores sociales.** Marca brechas como `[confirmar con invitado]`.

---

### Paso 3: Presentar -- Borrador de Notas para Aprobación

Ensambla en esta plantilla y presenta para revisión:

```markdown
# [Número de Episodio]: [Título del Episodio]

## Invitado
**[Nombre del Invitado]** -- [Título, Empresa]
[Biografía de 2-3 oraciones]

## Resumen del Episodio
[2-3 oraciones: qué cubre, para quién es, promesa principal al oyente]

## Timestamps
- [00:00] Introducción y bienvenida del invitado
- [02:15] [Descripción del tema]
- [08:42] [Descripción del tema]
- [15:30] [Descripción del tema]

## Puntos Clave
1. [Punto clave viable]
2. [Punto clave viable]
3. [Punto clave viable]

## Citas Destacadas
> "[Cita directa]" -- [Nombre del Orador]

## Recursos Mencionados
- [Nombre del Recurso](URL) -- breve descripción
- [Nombre del Recurso] [URL requerida] -- breve descripción

## Descripción del Episodio SEO
[150-250 palabras optimizadas para directorios de podcast. Incluye tema, nombre del invitado,
3-5 palabras clave buscables y un llamado a la acción.]
```

Pregunta: "¿Son precisos los timestamps? ¿Puntos clave para agregar o eliminar? ¿Citas correctas? ¿Recursos faltantes? ¿Necesita cambios la biografía del invitado? ¿La descripción SEO está bien?"

**PUNTO DE CONTROL: No escribas el archivo final hasta que el usuario apruebe o se apliquen revisiones.**

---

### Paso 4: Entregar -- Escribe Notas Finales a Archivo

1. **Pide la ruta de salida** si no se especifica. Predeterminado: `notas-show/ep-[número]-[slug].md`
2. **Escribe el archivo** con `Write`.
3. **Confirma la entrega:**

```
Notas escritas a: notas-show/ep-042-motor-referencia.md

Contenidos:
  - Biografía del invitado, resumen del episodio
  - 7 timestamps, 5 puntos clave, 2 citas destacadas
  - 4 recursos (1 necesita URL)
  - Descripción SEO (187 palabras)

Próximos pasos:
  - Agrega cualquier URL faltante
  - Copia la descripción SEO a tu plataforma de hosting de podcast
  - Usa citas destacadas para promoción en redes sociales
```

---

## Patrones Comunes

| Tipo de Transcripción | Ajuste |
|----------------|------------|
| Archivo de subtítulos SRT/VTT | Reconstruye oraciones completas; usa timestamps proporcionados directamente |
| Exportación Otter.ai / Descript | Mapea etiquetas de orador a nombres; usa timestamps en línea |
| Notas manuales (sin transcripción) | Marca timestamps como `[timestamp requerido]`; trabaja a partir de notas |
| Transcripción bruta sin editar | Ignora palabras de relleno; extrae citas limpias; marca secciones poco claras |
| Episodio en solitario | Omite biografía del invitado; enfócate en timestamps y puntos clave |
| Panel / múltiples invitados | Lista todos los invitados con biografías; atribuye citas cuidadosamente |

---

## Ejemplo 1: Episodio de Entrevista con Experto en Marketing

**Usuario dice:** "Aquí está la transcripción del episodio 42 de The Growth Lab. Entrevisté a Sarah Chen de GrowthLoop sobre motores de referencia. El archivo está en transcripts/ep42.txt."

**Paso 1:** Lee el archivo. Presenta descripción general identificando formato de entrevista, invitado como Sarah Chen (Fundadora, GrowthLoop), y 4 temas clave sobre estrategias de referencia. Obtén confirmación.

**Entrega del Paso 3 (extracto):**

```markdown
# Episodio 42: Construyendo un Motor de Referencia que Reemplaza Anuncios Pagados

## Invitado
**Sarah Chen** -- Fundadora y CEO, GrowthLoop
Sarah escaló su práctica de consultoría a $500K/año enteramente a través de referidos
y ha ayudado a 200+ negocios de servicios a sistematizar su proceso de referencia.

## Timestamps
- [00:00] Bienvenida y trasfondo de Sarah
- [03:12] Por qué los referidos superan la adquisición pagada para negocios de servicios
- [09:45] La secuencia de solicitud de referencia de 3 emails (desglose completo)
- [18:20] Estructuras de incentivo que no se sienten transaccionales
- [25:08] Seguimiento de baja tecnología: hojas de cálculo vs. etiquetas de CRM
- [32:15] Errores principales en programas de referencia
- [38:40] Ronda de fuego y dónde encontrar a Sarah

## Puntos Clave
1. Solicita referidos dentro de 48 horas de entregar un resultado -- el entusiasmo
   alcanza su punto máximo justo después de una victoria.
2. El email de "presentación cálida" supera a los enlaces de referencia porque da
   control al que refiere.
3. Los incentivos no monetarios superan los premios en efectivo para referidos B2B de alto valor.

## Citas Destacadas
> "Deja de preguntar '¿Conoces a alguien que necesite esto?' Empieza a preguntar
> '¿Quién tuvo el mismo problema que tuviste hace seis meses?'" -- Sarah Chen
```

**Paso 4:** Escribe a `notas-show/ep-042-motor-referencia.md` después de la aprobación.

---

## Ejemplo 2: Episodio en Solitario sobre Sistemas de Negocio

**Usuario dice:** "Acabo de grabar un episodio en solitario sobre los 5 sistemas que cada emprendedor necesita. Sin invitado. La transcripción está pegada abajo."

**Paso 1:** Identifica formato en solitario, 5 temas clave (captura de clientes potenciales, incorporación, producción de contenido, seguimiento financiero, revisión semanal). Confirma con usuario.

**Entrega del Paso 3 (extracto):**

```markdown
# Episodio 58: 5 Sistemas que Todo Emprendedor Necesita para Dejar de Trabajar en el Caos

## Resumen del Episodio
Ejecutar un negocio de una persona sin sistemas significa que eres el cuello de botella
para todo. Este episodio cubre 5 sistemas fundamentales y cómo construir cada uno en menos
de un día usando herramientas gratuitas.

## Timestamps
- [00:00] Por qué los emprendedores se ahogan sin sistemas
- [02:30] Sistema 1: Captura de clientes potenciales
- [08:15] Sistema 2: Onboarding de clientes
- [14:40] Sistema 3: Producción de contenido
- [21:05] Sistema 4: Seguimiento financiero
- [26:50] Sistema 5: Revisión semanal
- [32:10] Cómo elegir qué sistema construir primero

## Puntos Clave
1. Construye captura de clientes potenciales primero -- sin ingresos sin clientes potenciales
   entrando en tu pipeline de forma consistente.
2. Agrupa la producción de contenido en un día por semana. La creación diaria mata el
   trabajo profundo.
3. La revisión semanal mantiene todos los otros sistemas en funcionamiento. Omítela y todo
   se degrada en dos semanas.

## Citas Destacadas
> "Si tu proceso de onboarding vive en tu cabeza, no tienes un proceso.
> Tienes una memoria y las memorias fallan." -- Anfitrión
```

**Paso 4:** Escribe a `notas-show/ep-058-sistemas-emprendedor.md` después de la aprobación.

---

## Recuperación

**La transcripción es muy desordenada o incoherente:**
1. Extrae de secciones legibles, marca áreas problemáticas con timestamps aproximados
2. Pide al usuario que clarifique secciones poco claras de memoria
3. Si más del 50% no es usable: "Esta transcripción necesita limpieza primero. Ejecútala a través de Descript u Otter.ai para una versión más limpia."

**Sin timestamps en la transcripción:**
1. Estima a partir del conteo de palabras a 150 palabras por minuto
2. Marca todos los timestamps como `[aprox]` para que el usuario verifique contra su grabación
3. O déjalos como `[timestamp requerido]` para que el usuario rellene

**La información del invitado es incompleta o vaga:**
1. Redacta lo que puedas de la transcripción
2. Marca brechas: "Biografía del invitado incompleta -- falta [empresa / título / sitio web]. Por favor confirma con tu invitado."
3. **NUNCA fabriques credenciales, títulos o identificadores sociales**

**El usuario quiere un formato específico de plataforma:**
1. Pregunta por la plataforma (WordPress, Buzzsprout, Transistor, etc.)
2. Solicita un ejemplo de sus notas existentes y coincide con esa estructura
3. Adapta la plantilla de markdown para que se ajuste (HTML, shortcodes, campos de plataforma)

**Si 3 intentos de aclaración de requisitos fallan:**
Detente y proporciona una plantilla en blanco que el usuario pueda rellenar manualmente:

```
# Episodio [Número]: [Título]
## Invitado: [Nombre] -- [Título, Empresa]
## Resumen: [2-3 oraciones]
## Timestamps: [Rellena a partir de tu grabación]
## Puntos Clave: [3-7 viñetas]
## Recursos: [Lista con enlaces]
## Citas Destacadas: [2-4 citas directas]
## Descripción SEO: [150-250 palabras]
```
