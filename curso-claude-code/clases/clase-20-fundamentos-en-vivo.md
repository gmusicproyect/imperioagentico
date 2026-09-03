# Clase 20 — Masterclass de Fundamentos: del mito al primer proyecto en vivo

**Tags:** `Fundamentos` `Ecosistema` `Cowork` `VSCode` `Antigravity` `CLAUDE.md`
**Conecta con:** Clase 01 · Clase 02 · Clase 03 · Clase 04 · Clase 11

---

## Idea central

Claude Code no es una herramienta exclusiva para programadores ni un simple chatbot de ventana: es un entorno de ejecución bidireccional en lenguaje natural capaz de reemplazar al desarrollador intermediario. Conectando un modelo de razonamiento profundo con el sistema de archivos local y la terminal, permite a cualquier usuario conceptualizar, iterar y desplegar aplicaciones completas en minutos, siempre que se comprenda la diferencia entre Chat, Cowork y Code, se mantenga un contexto limpio (`CLAUDE.md` bajo 200 líneas) y se elija el entorno de desarrollo adecuado.

---

## Desmitificando Claude Code: el fin de la barrera técnica

Uno de los mayores frenos de entrada es la palabra *Code*, que provoca parálisis por análisis en perfiles no técnicos:
- **No requiere programar:** La interacción se realiza íntegramente en español natural. El usuario define el objetivo de negocio (*qué lograr*) y Claude Code se encarga de la sintaxis, las dependencias y la ejecución (*cómo lograrlo*).
- **Comunicación bidireccional:** A diferencia de copiar y pegar código entre un navegador y un editor, Claude Code lee directamente los archivos, propone modificaciones, corre pruebas y ejecuta scripts de despliegue en un entorno controlado y aislado.

---

## Las 3 herramientas del ecosistema: Chat vs Cowork vs Claude Code

Anthropic ofrece tres niveles de interacción según el tipo de tarea:

| Herramienta | Dónde opera | Capacidades clave | Limitación principal | Caso de uso ideal |
|-------------|-------------|-------------------|----------------------|-------------------|
| **Claude Chat** | Web / App móvil | Diálogo conversacional, análisis de texto, conectores MCP (Notion, Google Drive) | Sin acceso a archivos locales ni terminal | Brainstorming, redacción, consultas rápidas |
| **Claude Cowork** | App de escritorio | Acceso a carpetas del computador, edición de documentos, clasificación por lotes (facturas, Excel), multitasking | **No ejecuta terminal** ni comandos de sistema | Tareas administrativas, organización de archivos |
| **Claude Code** | Terminal / IDE | Lectura/escritura de archivos + **ejecución completa de comandos de terminal** | Requiere suscripción Pro/Max | Desarrollo de software, landing pages, automatizaciones |

---

## Modelos y economía operacional: Sonnet vs Opus

Claude Code consume un volumen significativo de tokens operacionales durante sus ciclos de lectura e inspección:
- **Claude Sonnet:** Es el modelo de cabecera para el 80% del trabajo. Es ágil, altamente competente en código y sustancialmente más económico. Ideal para desarrollo iterativo y scaffolding rápido.
- **Claude Opus:** Incorpora una capa superior de razonamiento abstracto (*deep thinking*). Se reserva para arquitectura compleja, refactorizaciones estructurales o resolución de bugs elusivos.
- **Pricing:** El uso de Claude Code requiere plan **Pro ($20/mes)** o **Max ($100–$200/mes)**. La capa gratuita no tiene acceso al CLI.

---

## Dónde correr Claude Code: Terminal vs IDEs vs VPS

Existen tres entornos principales para operar:

1. **Terminal pura:** Interfaz en línea de comandos rápida y minimalista. Permite arrastrar imágenes y archivos directamente sobre la consola.
2. **Entornos de desarrollo integrados (IDEs):**
   - **VS Code:** El estándar de la industria. Permite visualizar el árbol de archivos a la izquierda y la terminal con Claude Code a la derecha.
   - **Google Antigravity:** Un *fork* especializado de VS Code optimizado para agentes de IA. Ambos corren la misma extensión oficial de Claude Code y comparten idéntica lógica.
3. **Servidor Privado Virtual (VPS):** Útil para agentes que corren 24/7 sin interfaz gráfica, aunque para desarrollo interactivo se recomienda conectar VS Code de forma remota vía SSH o usar una máquina local dedicada (ej. Mac Mini).

---

## Modos de ejecución y control de autonomía

Dentro de Claude Code se pueden alternar distintos modos según la confianza en la tarea:
- **Ask before changes (Preguntar antes de cambios):** Solicita aprobación explícita antes de tocar cada archivo. Recomendado para entender el paso a paso en proyectos nuevos.
- **Edit automatically:** Aplica cambios automáticamente en los archivos de la carpeta asignada.
- **Plan mode (Modo planeación):** El agente hace preguntas de diseño, evalúa opciones técnicas y elabora la estrategia sin ejecutar código ni consumir cambios en disco.
- **Bypass permissions (`allow dangerously to skip permissions`):** Modo de máxima autonomía para prototipado ultrarrápido sin interrupciones constantes de confirmación.

---

## Caso práctico en vivo: Landing page de "Malik Studios"

Demostración del ciclo completo de desarrollo en menos de 5 minutos:

1. **Prompt inicial en lenguaje natural:**
   *"Crea una landing page moderna para Malik Studios, una agencia de recepcionistas virtuales con IA para clínicas estéticas y dentales. El único Call to Action debe ser un agendamiento a una llamada de demo enlazada a Calendly. Lánzala sin pedirme permisos innecesarios."*
2. **Razonamiento y Scaffolding:** Claude crea la estructura HTML/CSS en la carpeta aislada, redacta el copy enfocado en objeciones y pain points de clínicas, y enlaza el botón al formulario.
3. **Iteración estética:** Modificación de paleta en segundos (*"cambia el acento dorado por un naranja estilo Nvidia"*).
4. **Deploy:** Consulta de opciones para publicar en vivo vía Netlify o Vercel sin salir de la sesión.

---

## Contexto inmutable: El comando `/init` y la regla de `CLAUDE.md`

El principio fundamental del desarrollo agéntico es **GIGO (Garbage In, Garbage Out)**: si entregas contexto ruidoso, recibirás código defectuoso.

```
[ Proyecto ]
├── /init            → Escanea los archivos existentes y genera el contexto inicial
└── CLAUDE.md        → Contexto persistente (System Prompt local)
```

- **El rol de `CLAUDE.md`:** Se antepone de manera invisible en cada interacción. No se pierde cuando la ventana de contexto se compacta.
- **Regla de las 200 líneas:** Un `CLAUDE.md` debe mantenerse siempre por debajo de **200 líneas**. Si es demasiado extenso, devora la ventana de contexto y diluye la atención del modelo.

---

## Automatización visual continua con `/loop`

La función `/loop` permite ejecutar ciclos de auto-evaluación y mejora periódica sin intervención humana:
- **Ejemplo visual:** Proporcionar una captura de pantalla del diseño objetivo y programar un loop:
  `"/loop cada 5 minutos: audita la página web contra la imagen de referencia, identifica discrepancias visuales y ajusta el CSS hasta que sean indistinguibles."`
- Claude inspecciona, edita, valida en el navegador y repite hasta converger con el objetivo.

---

## Q&A de arquitectura: Claude Code vs Cursor vs OpenClaw

| Herramienta | Naturaleza | Arquitectura de contexto | Mejor caso de uso |
|-------------|------------|--------------------------|-------------------|
| **Cursor** | IDE con autocompletado IA | Enfocado en el archivo/pestaña activa | Asistencia de código línea por línea para programadores |
| **OpenClaw** | Asistente personal 24/7 | Un solo contexto global (vía Telegram/WhatsApp) | Automatizaciones continuas de negocio, alertas, calendario |
| **Claude Code** | Agente de terminal modular | Contexto segmentado por carpeta de proyecto (`CLAUDE.md`) | Construcción de productos completos, pipelines y software |

---

## 🎯 Ejercicio práctico

**Ejercicio 1:** Abre una terminal o VS Code en una carpeta vacía llamada `agencia-demo`. Ejecuta `/init` para inicializar el proyecto, crea un `CLAUDE.md` de menos de 50 líneas definiendo el rol de un diseñador web enfocado en conversión, y pídele en un solo prompt que genere una landing page funcional en un archivo `index.html` con un botón de agendamiento.

**Ejercicio 2 (avanzado):** Abre el archivo en tu navegador, toma una captura de pantalla, guárdala en la carpeta del proyecto y pídele a Claude Code: *"Analiza esta imagen y ajusta el contraste y la tipografía para maximizar legibilidad en pantallas móviles"*. Verifica que aplique los cambios directamente en el código.

*Este ejercicio te deja dominado el ciclo completo de inicialización, control de contexto y refinamiento visual iterativo con Claude Code.*

---

## 💡 Tip

Cuando inicies un proyecto grande, comienza siempre en **Plan Mode**. Permite que Claude te formule 5 a 10 preguntas sobre la arquitectura antes de escribir una sola línea de código; ahorrarás miles de tokens evitando rehacer interfaces mal especificadas.

---

## ⚠️ Error común

Sobrecargar `CLAUDE.md` con manuales completos o documentación externa cruda. Trata a `CLAUDE.md` como una lista de reglas ejecutivas (estilo de código, comandos de test y restricciones clave); si necesitas documentar procesos largos, usa archivos independientes en `/skills/`.
