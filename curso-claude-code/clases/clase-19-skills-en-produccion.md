# Clase 19 — Skills en producción: de prompts aislados a sistemas operativos

**Tags:** `Skills` `MCPs` `Automatización` `Producción` `Meta-Skills`
**Conecta con:** Clase 05 · Clase 04 · Clase 06

---

## Idea central

Los Skills de Anthropic no son "prompts bonitos" ni simples instrucciones de sistema: son procedimientos estándar operativos (SOPs) que Claude carga dinámicamente solo cuando los necesita. A diferencia de los prompts estáticos que saturan la ventana de contexto, los skills actúan como empleados especializados que ya conocen los procesos de tu negocio. Al combinarlos con conectores MCP, transforman a Claude de un asistente conversacional en un sistema operativo agéntico capaz de ejecutar flujos completos de producción.

---

## Prompts tradicionales vs Custom Instructions vs Skills

| Dimensión | Prompts tradicionales | Custom Instructions / Proyectos | Claude Skills |
|-----------|----------------------|---------------------------------|---------------|
| **Carga de contexto** | Se copia todo en cada mensaje (alto consumo de tokens) | Permanente en el proyecto (consume tokens en cada turno) | **Bajo demanda:** Se invoca solo cuando la tarea lo requiere |
| **Persistencia** | Efímera (se pierde al cerrar el chat) | Limitada a la configuración del proyecto | **Total:** Modular, versionable en Git y reutilizable |
| **Complejidad** | Bloques de texto plano | Instrucciones generales | **Avanzada:** Soporta templates, scripts y múltiples archivos |
| **Compartibilidad** | Copiar y pegar manualmente | Aislado a una cuenta | **Portable:** Importable en 1 clic o vía archivo `.md` |

---

## Skills vs MCPs: La sinergia operativa

Una confusión común es asumir que los Skills reemplazan a los conectores MCP. En la práctica, son dos capas complementarias de la misma arquitectura:

```
[ Herramientas & Datos Externos ] 
              │
         (Protocolo MCP) ──→ "El puerto físico / USBC" (conecta Notion, Apollo, Mercury, terminal)
              │
       [ Claude Code ]
              │
       (Claude Skills)  ──→ "El manual de procedimientos / SOP" (enseña cómo y cuándo operar)
              │
    [ Output de Producción ]
```

- **Usa MCPs** cuando necesites conectar a Claude con el mundo exterior (APIs, bases de datos, sistemas de archivos).
- **Usa Skills** cuando necesites que Claude ejecute un proceso estructurado con consistencia y criterio predefinido.

---

## Las 3 formas de incorporar Skills

1. **Crear con Claude (Modo conversacional):** Pedirle directamente al modelo que elabore la estructura del skill a partir de tus requerimientos.
2. **Redacción directa de instrucciones:** Crear manualmente el archivo `SKILL.md` definiendo el trigger de activación, los prerequisitos y los pasos operativos.
3. **Importar paquetes preconstruidos:** Descargar habilidades creadas por la comunidad desde plataformas como `skillsmp.com` o repositorios de GitHub y arrastrarlas a la interfaz.

---

## 3 Skills reales en entornos de producción

### 1. YouTube Creator (De audio a Content OS)
- **El dolor:** Planificar 5 videos de YouTube tomaba 2 días completos de investigación, diseño de hooks, estructura, b-roll y metadatos.
- **La solución con Skill:** El usuario envía un audio informal de 10 minutos con sus ideas. El skill estructura automáticamente: hook, timestamps, b-roll sugerido, guión por bloques, descripción y etiquetas.
- **Conexión MCP:** Al terminar, interactúa vía MCP con **Notion** para registrar la página completa en el *Content OS* de la empresa sin tocar una sola pestaña.

### 2. Frontend Design (Eliminar el "AI Slop")
- **El dolor:** Los constructores de código por IA suelen generar interfaces genéricas, sobrecargadas y visualmente deficientes ("AI slop").
- **La solución con Skill:** Define directrices estrictas de espaciado, jerarquía tipográfica, microinteracciones y tokens de diseño.
- **Integración:** Al combinarse con herramientas de desarrollo como **Claude Code** o **Antigravity**, el código frontend producido adopta estándares profesionales de desarrollo de software listos para producción.

### 3. Pedro el Prospectador (Outbound B2B automatizado)
- **El dolor:** Prospectar clientes en frío exige extraer datos, redactar emails personalizados uno a uno y configurar secuencias de seguimiento.
- **La solución con Skill:** Opera como un agente de prospección. A partir de una instrucción como *"Prospecta 100 restaurantes en Chile"*, genera filtros para Apollo, redacta correos personalizados siguiendo la fórmula *Observación + Conexión + Propuesta de valor*, y programa automáticamente la campaña y los follow-ups conectándose con **Instantly**.

---

## Meta-Skill: Creación sistemática con Skill Creator

Un **Skill Creator** es una meta-habilidad cuyo propósito exclusivo es diseñar, documentar y probar nuevas habilidades. 

### Caso práctico: "Mi Contador" (Mercury Bank + Reporte HTML)
1. **Conexión:** Se conecta la cuenta bancaria de la empresa (Mercury) mediante un conector MCP.
2. **Trigger y proceso:** Al preguntar *"¿Cómo estuvieron mis finanzas en noviembre?"*, el skill extrae las transacciones brutas del mes seleccionado.
3. **Clasificación:** Agrupa automáticamente los egresos por centro de costos (Educación, Infraestructura, Viajes, Operaciones).
4. **Output profesional:** En lugar de una respuesta en texto plano, compila y sirve un reporte HTML estilizado en el navegador con métricas clave, balance consolidado e insights de optimización financiera.

---

## Criterio humano e iteración con sistema SMART

Los skills no sustituyen el criterio del operador: automatizan la fricción mecánica para que el humano pueda concentrarse en la evaluación cualitativa. Las mejores habilidades no surgen perfectas al primer intento; se perfeccionan mediante iteraciones sucesivas ajustando las reglas negativas (qué *no* hacer) y agregando ejemplos de salidas deseadas (few-shot).

---

## 🎯 Ejercicio práctico

**Ejercicio 1:** Elige una tarea que hayas realizado manualmente más de 2 veces esta semana (por ejemplo: generar un hilo de Twitter/X a partir de un artículo, analizar un pull request, o clasificar tickets de soporte). Redacta su `SKILL.md` definiendo con precisión el cuándo usarlo, 3 pasos secuenciales obligatorios y un formato de salida específico.

**Ejercicio 2 (avanzado):** Configura tu nuevo skill en Claude Code o en la sección de habilidades de la aplicación. Ejecuta la tarea usando una instrucción en lenguaje natural sin mencionar explícitamente el nombre del archivo. Verifica que el modelo identifique el contexto, aplique el procedimiento documentado y entregue el resultado exacto sin desvíos.

*Al completar este ejercicio habrás construido tu primer SOP agéntico reutilizable, liberando ancho de banda mental en tus flujos diarios.*

---

## 💡 Tip

Aplica la regla de oro: **crea un skill inmediatamente después de haber ejecutado un proceso con éxito 2 veces**. Intentar documentar flujos hipotéticos genera skills rígidos; documentar lo que ya funcionó en la práctica crea herramientas infalibles.

---

## ⚠️ Error común

Crear skills genéricos ("asistente-de-marketing", "ayudante-general"). Los skills efectivos son atómicos y específicos para un objetivo claro ("redactar-guion-youtube", "auditar-accesibilidad-web"). Si un skill intenta abarcar demasiadas responsabilidades, diluye la precisión de las instrucciones.
