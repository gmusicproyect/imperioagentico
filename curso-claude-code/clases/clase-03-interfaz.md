# Clase 03 — Interfaz de Claude Code & configuración clave

**Tags:** `Interfaz` `Modelos`
**Conecta con:** Clase 06 · Clase 07

---

## Idea central

La interfaz de Claude Code tiene configuraciones que impactan directamente la calidad del trabajo. El modelo y el nivel de razonamiento son las dos variables más importantes.

---

## Configuración recomendada

| Ajuste | Valor recomendado | Por qué |
|--------|------------------|---------|
| Modelo | **Opus** (por defecto) | Mejor razonamiento para tareas complejas |
| Razonamiento | **Alto** | Más pasos internos = mejores resultados |
| Modo | **Automático** | Claude decide cuándo usar herramientas |

---

## Elementos de la interfaz

- **Pestaña Code** → acceso principal a la terminal agéntica
- **Proyectos** → carpetas con contexto persistente (CLAUDE.md)
- **Historial** → conversaciones anteriores por proyecto
- **Herramientas** → toggle de permisos por sesión

---

## 🎯 Ejercicio práctico

**Ejercicio 1:** Abre la interfaz de Claude Code, vincula la carpeta de tu proyecto y configura el modelo en Opus con nivel de razonamiento "Alto". Envíale un prompt solicitando un plan de 3 pasos para organizar tu proyecto y observa en la interfaz cómo se muestran los bloques de pensamiento y razonamiento antes de la respuesta.

**Ejercicio 2 (avanzado):** Revisa la sección de historial para inspeccionar la sesión recién creada, comprueba el panel de herramientas activas y abre una nueva sesión paralela dentro del mismo proyecto comprobando que la configuración se mantiene.

*Este ejercicio deja calibrada la interfaz de Claude Code con los parámetros de razonamiento requeridos para tareas agénticas.*

---

## ⚠️ Error común

Dejar el razonamiento en "bajo" por ahorrar tokens. Para tareas agénticas complejas, el razonamiento alto es la diferencia entre un resultado correcto y uno a medias.
