---
name: plan-prueba-ab-email
description: "Diseña planes de prueba A/B para campañas de email con hipótesis, variables de prueba, tamaños de muestra y métricas de éxito. Úsalo cuando necesites optimización de email impulsada por datos."
allowed-tools: Read Write Glob
metadata:
  author: Imperio Digital
  version: "1.0"
---

# Plan de Prueba A/B de Email

## Cuándo Usar Este Skill

Usa este skill cuando necesites:
- Diseñar un plan de prueba A/B estructurado para campañas de email
- Definir hipótesis claras, variables de prueba y criterios de éxito
- Calcular tamaños de muestra necesarios para resultados estadísticamente significativos
- Construir un roadmap de testing que componga el desempeño de email en el tiempo

**NO** uses este skill para testing de sitio web, testing de creatividad de anuncios, o configuración general de analytics. Esto es para split testing específico de email.

---

## Principio Fundamental

PRUEBA UNA VARIABLE A LA VEZ CON UNA HIPÓTESIS CLARA — UNA PRUEBA SIN UNA PREDICCIÓN ES SOLO VARIACIÓN ALEATORIA.

---

## Fase 1: Resumen de Testing

### Entradas Requeridas

| Entrada | Qué Preguntar | Por Defecto |
|-------|------------|---------|
| **Tipo de email** | "¿Qué email estás probando? (boletín, promoción, nutrición)" | Sin valor por defecto — debe ser proporcionado |
| **Desempeño actual** | "¿Cuáles son tus tasas actuales de apertura y clic?" | Promedio de la industria (20% apertura, 2.5% clic) |
| **Tamaño de lista** | "¿Cuántos suscriptores estarán en esta prueba?" | Sin valor por defecto — debe ser proporcionado |
| **Objetivo de testing** | "¿Qué métrica deseas mejorar más?" | Tasa de apertura |
| **Plataforma de email** | "¿Qué herramienta usas?" | Agnóstica a plataforma |
| **Frecuencia de envío** | "¿Con qué frecuencia envías este tipo de email?" | Semanal |

**PUNTO DE CONTROL: Confirma los inputs antes de diseñar el plan de prueba.**

---

## Fase 2: Diseño de Prueba

### Marco de Hipótesis

Cada prueba comienza con una hipótesis en este formato:

```
SI cambiamos [esta variable]
ENTONCES [esta métrica] será [aumentará/disminuirá]
PORQUE [razonamiento basado en comportamiento de audiencia]
```

Ejemplo:
```
SI cambiamos la línea de asunto de enfocada en beneficio a basada en curiosidad
ENTONCES la tasa de apertura aumentará 5+ puntos porcentuales
PORQUE nuestra audiencia responde a brechas de información más que beneficios establecidos
```

### Variables Probables (Una a la Vez)

**Pruebas de Línea de Asunto:**
- Largo (corto vs. largo)
- Fórmula (curiosidad vs. beneficio vs. urgencia)
- Personalizacion (con nombre vs. sin)
- Emojis (con vs. sin)

**Pruebas de Contenido:**
- Largo de cuerpo (corto vs. medio vs. largo)
- Número de CTAs (uno vs. múltiples)
- Posición de CTA (arriba vs. abajo)
- Tipo de CTA (botón vs. enlace)

**Pruebas de Timing:**
- Día de semana (lunes vs. viernes)
- Hora del día (mañana vs. tarde)

---

## Fase 3: Diseño de Muestra

### Cálculo de Tamaño de Muestra

Para resultados significativos:

```
Tasa de apertura 20%:
- Para detectar 5% de aumento: 1,000-1,500 por variante
- Para detectar 10% de aumento: 300-500 por variante

Tasa de clic 2.5%:
- Para detectar 25% de aumento: 3,000-5,000 por variante
- Para detectar 50% de aumento: 800-1,200 por variante
```

**Regla:** Si tu lista es menor a 10,000, testea el email a todos pero reserva 20% para una variante control.

---

## Fase 4: Ejecución y Análisis

### Checklist de Prueba

- [ ] Hipótesis escrita antes de diseñar variantes
- [ ] Una sola variable diferente entre A y B
- [ ] Muestras aleatorias y distribuidas equitativamente
- [ ] Tamaño de muestra lo suficientemente grande para significancia
- [ ] Fecha de análisis establecida (no mires a mitad de semana)

### Interpretación de Resultados

- **Significancia estadística:** 95% de confianza antes de declarar ganador
- **Diferencia mínima práctica:** 5+ puntos porcentuales en apertura, 25%+ en clics
- **Ganador claro:** Aplica a futuras campañas
- **Sin ganador claro:** Prueba otra variable siguiente

---

## Anti-Patrones

- **Cambiar múltiples variables** — no sabrás qué causó la diferencia
- **Tamaños de muestra muy pequeños** — resultados no confiables
- **Mirar resultados a mitad de prueba** — pueden cambiar por variación aleatoria
- **Ignorar ganadores anteriores** — si una línea de asunto funcionó en marzo, pruébala contra nuevas ideas
- **Sin hipótesis clara** — el testing sin propósito es desperdicio de datos

---

## Recuperación

- **Demasiado tiempo para resultados:** Tu lista es demasiado pequeña o variantes muy similares.
- **Ganador marginal:** A veces no hay diferencia clara. Elige la opción más simple y prueba algo diferente después.
- **La ganadora del mes pasado pierde este mes:** Las audiencias cambian. Re-test cada trimestre.
