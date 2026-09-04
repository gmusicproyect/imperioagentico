---
name: rastreador-recaudacion
description: "Crea rastreadores de pipeline de recaudación con etapas de inversionistas, cálculos de valuación y comparaciones de propuestas de términos. Úsalo cuando estés gestionando un proceso de recaudación activo."
allowed-tools: Read Write Glob
metadata:
  author: Imperio Digital
  version: "1.0"
---

# Rastreador de Recaudación

## Cuándo usar esta habilidad

Usa esta habilidad cuando necesites:
- Organizar y rastrear un pipeline de recaudación activo
- Comparar propuestas de términos y ofertas de inversión
- Calcular dilución y escenarios de valuación
- Crear un proceso estructurado de recaudación con cronogramas e hitos

**NO** uses esta habilidad para escribir pitch decks, construir modelos financieros o gestionar relaciones con inversionistas post-levantamiento. Esto es para rastrear el proceso de recaudación en sí.

---

## Principio Central

LA RECAUDACIÓN ES UN PROCESO DE VENTAS — RASTRÉALO COMO UN PIPELINE CON ETAPAS, TASAS DE CONVERSIÓN Y PLAZOS PARA MANTENER IMPULSO Y APALANCAMIENTO.

---

## Fase 1: Parámetros de Recaudación

### Entradas Requeridas

| Entrada | Qué Preguntar | Predeterminado |
|---------|--------------|----------------|
| **Monto de recaudación** | "¿Cuánto estás recaudando?" | Sin predeterminado — debe proporcionarse |
| **Tipo de ronda** | "¿Qué tipo de ronda? (pre-seed, seed, Series A, bridge, SAFE)" | Seed |
| **Rango de valuación** | "¿Cuál es tu valuación pre-money objetivo?" | Sin predeterminado — debe discutirse |
| **Instrumento** | "¿SAFE, pagaré convertible o ronda con precio?" | SAFE |
| **Cronograma** | "¿Cuándo necesitas cerrar?" | 3 meses |
| **Inversionistas actuales en pipeline** | "¿Cuántos inversionistas has contactado o planeas contactar?" | Se construirá lista |

**PUNTO DE CONTROL: No continúes sin monto de recaudación y tipo de ronda.**

---

## Fase 2: Rastreador de Pipeline

### Pipeline de Inversionistas

```
## Pipeline de Recaudación: [Tipo de Ronda] — $[Monto]

### Resumen de Pipeline
| Etapa | Cantidad | % del Pipeline |
|-------|----------|----------------|
| Lista de objetivos | [X] | [X]% |
| Outreach enviado | [X] | [X]% |
| Primera reunión | [X] | [X]% |
| Seguimiento / due diligence | [X] | [X]% |
| Propuesta de términos / verbal | [X] | [X]% |
| Comprometido | [X] | [X]% |
| Rechazado | [X] | [X]% |

### Pipeline Detallado
| Inversionista | Tipo | Tamaño de Check | Etapa | Último Contacto | Próximo Paso | Notas |
|-----------|------|-----------------|-------|----------------|-------------|-------|
| [Nombre] | [VC/Angel/Fondo] | $[X] | [Etapa] | [Fecha] | [Acción] | |
| [Nombre] | [VC/Angel/Fondo] | $[X] | [Etapa] | [Fecha] | [Acción] | |

### Etapas del Pipeline
1. **Objetivo** — Identificado, investigando encaje
2. **Outreach** — Email/introducción enviada, esperando respuesta
3. **Primera Reunión** — Llamada introductoria o reunión programada/completada
4. **Seguimiento** — Segunda reunión, due diligence o reunión con socio
5. **Propuesta de Términos** — Propuesta de términos recibida o compromiso verbal
6. **Comprometido** — Documentos firmados, fondos en transferencia
7. **Rechazado** — Declinó o se puso frío
```

---

## Fase 3: Comparación de Propuestas de Términos y Dilución

### Comparación de Propuestas de Términos

```
## Comparación de Propuestas de Términos

| Término | Inversionista A | Inversionista B | Inversionista C |
|--------|-----------------|-----------------|-----------------|
| Monto de inversión | $[X] | $[X] | $[X] |
| Instrumento | [SAFE/Pagaré/Precio] | | |
| Valuación pre-money | $[X] | $[X] | $[X] |
| Tope de valuación (si SAFE) | $[X] | $[X] | $[X] |
| Tasa de descuento | [X]% | [X]% | [X]% |
| Derechos pro-rata | [Sí/No] | | |
| Puesto de junta | [Sí/No] | | |
| Derechos de información | [Sí/No] | | |
| Preferencia de liquidación | [X]x | | |
| Anti-dilución | [Amplia/Estrecha/Ninguna] | | |
| Vesting de fundador | [Términos] | | |
| **Amigabilidad con fundador** | **[1-10]** | **[1-10]** | **[1-10]** |
```

### Calculadora de Dilución

```
## Escenarios de Dilución

### Tabla de Capitalización Actual
| Accionista | Acciones | % de Propiedad |
|-----------|----------|----------------|
| Fundador(es) | [X] | [X]% |
| Inversionistas existentes | [X] | [X]% |
| Pool de opciones | [X] | [X]% |
| **Total** | **[X]** | **100%** |

### Tabla de Capitalización Post-Ronda (en valuación $[X]M)
| Accionista | Acciones | % de Propiedad | Dilución |
|-----------|----------|----------------|----------|
| Fundador(es) | [X] | [X]% | -[X]% |
| Inversionistas existentes | [X] | [X]% | -[X]% |
| Nuevos inversionistas | [X] | [X]% | Nuevo |
| Pool de opciones | [X] | [X]% | |
| **Total** | **[X]** | **100%** | |
```

---

## Fase 4: Gestión del Proceso

### Cronograma de Recaudación

```
## Cronograma de Recaudación

| Semana | Hito | Objetivo |
|--------|------|----------|
| Semana 1-2 | Construir lista de objetivos, intros cálidas | [X] inversionistas contactados |
| Semana 3-4 | Primeras reuniones | [X] reuniones completadas |
| Semana 5-6 | Seguimientos, reuniones con socios | [X] en due diligence |
| Semana 7-8 | Propuestas de términos esperadas | [X] propuestas de términos |
| Semana 9-10 | Negociar y cerrar | Compromisos firmados |
| Semana 11-12 | Transferencias de fondos, cierre legal | Dinero en banco |
```

### Lista de Verificación de Revisión Semanal

```
- [ ] Pipeline actualizado con últimas etapas y fechas
- [ ] Seguimientos enviados en 48 horas de cada reunión
- [ ] Nuevas intros solicitadas desde red existente
- [ ] Actualización de inversionista enviada a inversionistas comprometidos
- [ ] Documentos listos para cualquier inversionista entrando en due diligence
```

---

## Ejemplo: $500K Pre-Seed SAFE

**Pipeline:** 40 inversionistas objetivo, 25 outreach enviado, 12 primeras reuniones, 4 en due diligence, 2 compromisos verbales ($150K + $100K). Necesita $250K más del pipeline restante.

**Valuación:** $5M cap SAFE. En conversión: fundadores retienen 88% post-ronda (12% a inversionistas, incluyendo refresco de pool de opciones a 10%).

---

## Anti-patrones

- **Recaudación sin un pipeline** — spray-and-pray desperdicia tiempo. Construye una lista objetivo de 30-50 inversionistas que invierten en tu etapa, sector y tamaño de check.
- **Detener outreach después de primera propuesta de términos** — el mejor apalancamiento es múltiples propuestas de términos. Mantén el pipeline activo hasta que firmes.
- **No rastrear seguimientos** — los inversionistas se mueven lentamente. Si no das seguimiento en 48 horas, pierdes impulso.
- **Aceptar la primera propuesta de términos sin comparación** — a menos que los términos sean excepcionales, espera 2-3 opciones. Cada término es negociable.
- **Compartir tabla de capitalización con cada inversionista** — comparte tabla de capitalización solo durante due diligence con inversionistas serios. Protege esta información.

---

## Recuperación

- **Sin intros cálidas:** Cold email con un hook de una línea fuerte (métrica de tracción + solicitud). Espera 10-15% tasa de respuesta. Aumenta volumen.
- **Todos los inversionistas rechazando:** Reevalúa — ¿es timing, valuación, tracción o pitch? Obtén feedback de inversionistas que rechazaron.
- **Recaudación tomando más tiempo que planeado:** Acorta el cronograma creando urgencia (interés de otro inversionista, plazo de cierre). Considera financing de puente de angels.
- **Sobreasuscrito (demasiado interés):** Aumenta el tamaño de ronda, eleva el tope de valuación o selecciona inversionistas que traen valor estratégico más allá del capital.
