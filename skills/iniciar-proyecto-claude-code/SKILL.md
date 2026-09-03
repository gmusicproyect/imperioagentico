# SKILL: Inicialización y Scaffolding de Proyectos en Claude Code

> Guarda este archivo en `/skills/iniciar-proyecto-claude-code/SKILL.md`
> Referencia en tu CLAUDE.md: `- /skills/iniciar-proyecto-claude-code/SKILL.md → para inicializar nuevos proyectos con contexto limpio y buenas prácticas`

---

## Cuándo usar este skill

Cuando el usuario comience un nuevo proyecto, repositorio o carpeta de trabajo en Claude Code y requiera establecer la arquitectura inicial de contexto (`/init`, `CLAUDE.md`), calibrar el modelo adecuado (Sonnet vs Opus) y definir el modo de permisos para prototipar o construir software sin desperdiciar tokens.

---

## Prerequisitos

- [ ] Claude Code CLI instalado y autenticado (requiere plan Pro o Max)
- [ ] Editor configurado (VS Code, Google Antigravity o terminal pura)
- [ ] Directorio local dedicado para el proyecto

---

## Pasos

### Paso 1 — Crear el directorio y abrir el entorno

1. Crear una carpeta con nombre descriptivo en kebab-case (ej. `agencia-landing`, `crm-automations`).
2. Abrir la carpeta en tu IDE preferido (VS Code / Antigravity) o navegar desde la terminal:
   ```bash
   mkdir mi-nuevo-proyecto && cd mi-nuevo-proyecto
   claude
   ```

### Paso 2 — Ejecutar el comando de escaneo inicial

Si el proyecto ya cuenta con archivos existentes o dependencias previas:
```bash
/init
```
*Función:* Claude Code inspecciona el árbol de archivos, detecta el stack tecnológico y elabora un mapa mental del repositorio, optimizando el consumo de tokens para todas las sesiones futuras.

### Paso 3 — Configurar un `CLAUDE.md` de alta eficiencia (<200 líneas)

Crear el archivo `CLAUDE.md` en la raíz del proyecto aplicando el principio GIGO (Garbage In, Garbage Out):
1. **Regla de oro:** Mantener el archivo estrictamente por debajo de **200 líneas**.
2. **Estructura mínima obligatoria:**
   - **Propósito del proyecto:** 1–2 líneas sobre qué resuelve el sistema.
   - **Comandos habituales:** Comandos para compilar, correr servidor local y ejecutar tests (`npm run dev`, `pytest`, etc.).
   - **Estándares y restricciones:** Guías estilísticas, dependencias prohibidas y reglas negativas explícitas.
   - **Referencias a skills:** Enlaces hacia `/skills/[nombre]/SKILL.md` para tareas complejas.

### Paso 4 — Seleccionar el modelo y esfuerzo de razonamiento

1. Para el 80% de tareas (desarrollo frontend, scripts, endpoints, scaffolding): seleccionar **Claude Sonnet** para maximizar velocidad y reducir gasto operacional de tokens.
2. Para arquitectura compleja, esquemas de bases de datos o depuración profunda: alternar a **Claude Opus** mediante `/model`.
3. Ajustar el nivel de razonamiento (*thinking effort*) en nivel medio o alto según la complejidad.

### Paso 5 — Iniciar en Plan Mode antes de escribir código

Para proyectos nuevos de mediana o alta envergadura:
1. Activar el **Plan Mode** en la interfaz o solicitarlo en el prompt:
   *"Actúa en modo planeación. No modifiques archivos aún; hazme las preguntas necesarias sobre requerimientos y arquitectura antes de ejecutar."*
2. Responder a las preguntas de alineación técnica.
3. Una vez aprobado el plan, conmutar al modo de edición automática (*Edit automatically* o *Bypass permissions* para prototipado rápido).

### Paso 6 — Ejecución del prompt semilla y verificación

1. Enviar el prompt de especificación inicial incluyendo objetivo de negocio, usuario final y restricciones clave.
2. Comprobar que Claude Code genere los archivos dentro del directorio aislado sin desbordar permisos.
3. Probar la aplicación en local (`localhost`) o abrir los archivos en el navegador para validar la primera versión funcional.

---

## Outputs esperados

- Directorio del proyecto inicializado con contexto ordenado.
- Archivo `CLAUDE.md` conciso y enfocado (<200 líneas).
- Primer entregable funcional generado e inspeccionado en local.

---

## Errores comunes

| Error | Causa probable | Solución |
|-------|---------------|---------|
| `CLAUDE.md` gigante que satura la sesión | Copiar manuales extensos o librerías enteras en el archivo | Extraer procesos detallados a carpetas independientes en `/skills/` |
| Claude ejecuta código incorrecto al inicio | Falta de alineación en requerimientos | Iniciar siempre en Plan Mode para resolver dudas arquitectónicas |
| Proyecto mezcla múltiples propósitos | Agrupar varias aplicaciones no relacionadas en una sola carpeta | Crear proyectos independientes con su propio `CLAUDE.md` |
| Consumo excesivo de tokens en tareas simples | Usar Opus permanentemente en tareas de baja complejidad | Mantener Sonnet como modelo por defecto para desarrollo iterativo |

---

## Variaciones

**Variación A — Prototipado ultrarrápido (Hackathon / MVP):** Activar la opción `allow dangerously to skip permissions` en la configuración para que Claude genere HTML/CSS/JS y levante el servidor sin pedir confirmaciones manuales constantes.

**Variación B — Agente corporativo con múltiples subproyectos:** Crear subcarpetas con un `CLAUDE.md` raíz que orqueste las reglas generales y `CLAUDE.md` locales en cada módulo específico.

---

## Notas adicionales

El éxito de una sesión en Claude Code depende del contexto inicial. Una inversión de 3 minutos en configurar adecuadamente `/init` y un `CLAUDE.md` limpio previene horas de correcciones por código desalineado.

---

*Creado: 2026-09-03*
