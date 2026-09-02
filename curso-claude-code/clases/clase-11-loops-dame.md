# Clase 11 — Loops & Framework DAME

**Tags:** `Loops` `DAME` `Objetivos` `Automatización`
**Conecta con:** Clase 10 · Clase 12

---

## Idea central

Claude Code puede correr en loops continuos orientados a objetivos en lugar de esperar instrucciones una por una. El framework DAME define cómo estructurar estos objetivos para que el agente sepa exactamente cuándo parar.

---

## Framework DAME

| Letra | Concepto | Ejemplo |
|-------|----------|---------|
| **D** | **Destino** | "Conseguir 10 leads calificados" |
| **A** | **Acciones** | "Buscar en LinkedIn, verificar email, guardar en GHL" |
| **M** | **Métrica** | "Lead calificado = empresa +20 empleados, cargo C-level" |
| **E** | **Estado de parada** | "Parar cuando haya 10 leads en GHL con status Verificado" |

---

## Ejemplo de prompt con DAME

```
Destino: 10 leads calificados en mi pipeline de GHL
Acciones: busca en LinkedIn empresas de software en LATAM,
  extrae el email del founder/CEO, verifica que tenga +20 empleados,
  crea el contacto en GHL con tag "prospecto-frío"
Métrica: calificado = empresa de software, LATAM, +20 empleados, contacto es decisor
Estado de parada: cuando haya 10 contactos con tag "prospecto-frío" en GHL
```

---

## Tipos de loops

- **Loop acotado:** corre X veces o hasta alcanzar un objetivo
- **Loop continuo:** corre en background indefinidamente (requiere Routine)
- **Loop condicional:** actúa solo si se cumple una condición

---

## 🎯 Ejercicio práctico

**Ejercicio 1:** Escribe y ejecuta en Claude Code un prompt estructurado con el framework DAME para un loop acotado:
- **Destino:** Generar una lista curada de 5 herramientas o recursos útiles para tu proyecto.
- **Acciones:** Buscar en internet o documentación, extraer nombre y utilidad, y escribir en `herramientas-seleccionadas.md`.
- **Métrica:** Cada entrada debe incluir nombre, URL o comando, y caso de uso específico.
- **Estado de parada:** Detenerse exactamente cuando el archivo contenga 5 herramientas válidas.

**Ejercicio 2 (avanzado):** Revisa la ejecución del agente y verifica que se haya detenido por sí solo al alcanzar el Estado de Parada sin requerir intervención ni quedar en bucle continuo.

*Este ejercicio te deja listo tu primer prompt autónomo con framework DAME y condición de parada verificable.*

---

## 💡 Tip

El Estado de Parada es el elemento más crítico del DAME. Sin una condición de parada clara, el agente puede seguir corriendo indefinidamente o detenerse demasiado pronto.
