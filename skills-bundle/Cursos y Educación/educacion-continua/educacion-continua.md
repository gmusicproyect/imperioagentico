---
name: educacion-continua
description: "Planifica ofertas de educación continua con requisitos de crédito, catálogos de cursos y sistemas de seguimiento de finalización."
allowed-tools: Read Write Glob
author: Imperio Digital
version: "1.0"
---

# Educación Continua

## Cuándo Usar Este Skill

Usa este skill cuando necesites:
- Planificar un programa de educación continua con requisitos de crédito estructurados
- Construir un catálogo de cursos con categorías, requisitos previos y valores de crédito
- Diseñar sistemas de seguimiento de finalización para desarrollo profesional
- Crear una oferta de CE para vender a profesionales que necesitan credenciales continuas

**NO** uses este skill para cursos únicos, programas de grado o aprendizaje informal. Es para educación continua estructurada con seguimiento de crédito y elementos de cumplimiento.

---

## Principio Fundamental

LA EDUCACIÓN CONTINUA DEBE EQUILIBRAR REQUISITOS DE CUMPLIMIENTO CON DESARROLLO GENUINO DE HABILIDADES — LOS MEJORES PROGRAMAS DE CE HACEN A LOS PROFESIONALES MEJOR EN SUS TRABAJOS, NO SOLO MARCAR UNA CASILLA.

---

## Fase 1: Resumen

### Entradas Requeridas

| Entrada | Qué Preguntar | Predeterminado |
|---------|--------------|--------|
| **Profesión o industria** | "¿Qué profesión o industria necesita estos créditos de CE?" | Sin predeterminado — debe proporcionarse |
| **Requisitos de crédito** | "¿Cuántos créditos se requieren por ciclo y cuál es la duración del ciclo?" | 20 créditos por año |
| **Organismo de acreditación** | "¿Hay un organismo que debe aprobar los cursos?" | Auto-certificado (sin cuerpo externo) |
| **Formato de entrega** | "¿Online, presencial o híbrido?" | Online autorritmado |
| **Modelo de ingresos** | "¿Suscripción, por curso o incluido en membresía?" | Compra por curso |

**PUNTO DE CONTROL: Confirma el resumen antes de proceder.**

---

## Fase 2: Arquitectura del Programa

### Estructura de Crédito

```
## Sistema de Crédito
**Total requerido:** [X] créditos por [duración del ciclo]
**Categorías de crédito:**
- Núcleo/obligatorio: [X créditos mínimo]
- Electivo: [X créditos]
- Ética/cumplimiento: [X créditos si aplica]

**Cálculo de crédito:**
- 1 crédito = 1 hora de contenido instructivo
- Eventos en vivo: [multiplicador si aplica]
- Autorritmado: [requisitos de finalización]
```

### Estructura del Catálogo de Cursos

```
## Categorías de Catálogo
1. [Categoría 1] — [X cursos, Y créditos totales]
2. [Categoría 2] — [X cursos, Y créditos totales]
3. [Categoría 3] — [X cursos, Y créditos totales]

## Formato de Listado de Cursos
| Título del Curso | Categoría | Créditos | Formato | Requisitos Previos | Precio |
|-------------|----------|---------|--------|--------------|-------|
```

### Requisitos de Finalización

Define qué significa "completar" un curso:
- Tasa de aprobación de evaluación (ej. 80% en post-test)
- Tiempo mínimo gastado (sin pasar rápido video)
- Requisitos de asistencia para sesiones en vivo
- Generación de certificado al completar

**PUNTO DE CONTROL: Presenta la arquitectura del programa para aprobación.**

---

## Fase 3: Construye

### Catálogo de Cursos

Crea 15-25 listados de cursos en todas las categorías:

```
## [Título del Curso]
**Categoría:** [Nombre de categoría]
**Créditos:** [Número]
**Duración:** [Tiempo]
**Formato:** [Autorritmado / En vivo / Híbrido]
**Descripción:** [2-3 oraciones]
**Objetivos de aprendizaje:** [3-5 puntos de viñeta]
**Requisitos previos:** [Ninguno o cursos específicos]
**Evaluación:** [Quiz, proyecto o basado en asistencia]
```

### Sistema de Seguimiento

```
## Requisitos de Panel del Estudiante
- Balance de crédito (ganados vs. requeridos)
- Historial de finalización con fechas y certificados
- Próximas fechas límite (expiración del ciclo)
- Recomendaciones de cursos basado en requisitos restantes
- Exportación de transcripción (PDF)
```

### Documentación de Cumplimiento

- Plantilla de certificado de finalización (incluye nombre, curso, créditos, fecha, número de ID)
- Formato de transcripción para reportar a organismos de acreditación
- Política de retención de registros (cuánto tiempo se guardan los registros)
- Pista de auditoría para verificación de crédito

---

## Fase 4: Pulida

### 1. Launch Plan

```
## Lista de Verificación de Lanzamiento de Programa CE
- [ ] Catálogo de cursos finalizado con al menos 1.5x los créditos requeridos disponibles
- [ ] Sistema de seguimiento configurado y probado
- [ ] Plantilla de certificado creada
- [ ] Sistema de precios y pago listo
- [ ] Materiales de marketing para profesionales objetivo
- [ ] Documento de preguntas frecuentes abordando preguntas comunes de cumplimiento
- [ ] Proceso de apoyo para disputas de crédito o problemas técnicos
```

### 2. Plan de Crecimiento

- Agrega 5-10 cursos nuevos por trimestre
- Retira cursos obsoletos anualmente
- Encuesta a completadores para solicitudes de temas
- Rastrear cursos más y menos populares para guiar creación

### 3. Métricas de Calidad

```
## Rastrear Trimestral
- Tasas de finalización de cursos (objetivo: 80%+)
- Tasas de aprobación de evaluación (objetivo: 85%+)
- Puntuaciones de satisfacción del estudiante (objetivo: 4.2+/5)
- Tasa de cumplimiento de crédito (% de estudiantes cumpliendo requisitos a tiempo)
- Ingresos por estudiante
```

---

## Ejemplo 1: Programa CE para Profesional de Marketing

```
Categorías: Marketing Digital (8 créditos), Analítica (4 créditos), Estrategia (4 créditos), Ética (4 créditos)
Cursos de muestra: "Ética de IA en Marketing" (2 créditos), "Google Analytics Avanzado" (3 créditos)
Ciclo: 20 créditos por año calendario
```

## Ejemplo 2: Programa CE para Asesor Financiero

```
Categorías: Regulatorio (10 créditos), Conocimiento de Producto (5 créditos), Ética (5 créditos), Electivo (10 créditos)
Ciclo: 30 créditos por período de 2 años
Requisito: Al menos 5 créditos de instrucción en vivo
```

---

## Anti-Patrones

- **Cultura de marcar casillas** — diseñar cursos que sean fáciles de pasar pero no enseñen nada destruye la reputación del programa.
- **Variedad de cursos insuficiente** — si los estudiantes deben tomar los mismos cursos cada ciclo, se desenganchan. Ofrece 2x los créditos requeridos en opciones.
- **Sin recordatorios de fecha límite** — los profesionales procrastinan. Envía recordatorios en 75%, 50% y 25% del ciclo restante.
- **Seguimiento manual** — el seguimiento basado en hoja de cálculo falla a escala. Construye o usa un LMS apropiado con seguimiento de crédito.
- **Ignorar móvil** — muchos profesionales completan CE en su teléfono durante tiempo libre. Asegura compatibilidad móvil.

---

## Recuperación

- **No existe organismo de acreditación:** Crea una certificación interna con estándares claros. Comercializa la credencial basado en calidad del curso y reconocimiento de la industria.
- **Usuario inseguro cuántos créditos requerir:** Investiga programas comparables en la industria. Usa 20 créditos por año como punto de partida razonable.
- **No hay suficiente contenido para catálogo completo:** Lanza con 10 cursos cubriendo categorías obligatorias. Agrega electivos trimestralmente.
- **Estudiantes no completando a tiempo:** Implementa período de gracia con opciones de finalización tardía. Agrega recordatorios automatizados comenzando 90 días antes de deadline.
