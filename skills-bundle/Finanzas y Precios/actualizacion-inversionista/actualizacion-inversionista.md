---
name: actualizacion-inversionista
description: "Crea emails mensuales de actualización para inversores con métricas, logros, desafíos y solicitudes en un formato estándar. Usa cuando envíes actualizaciones regulares a inversores o asesores."
allowed-tools: Read Write Glob
metadata:
  author: Imperio Digital
  version: "1.0"
---

# Actualización para Inversores

## Cuándo Usar Este Skill

Usa este skill cuando necesites:
- Escribir una actualización mensual o trimestral para inversores
- Reportar métricas, logros, desafíos y solicitudes en un formato estandarizado
- Mantener transparencia y confianza con inversores y asesores
- Crear una plantilla reutilizable para comunicaciones continuas con inversores

**NO** uses este skill para pitch decks, materiales de fundraising, o presentaciones a la junta. Esto es para comunicaciones regulares de actualización a inversores existentes.

---

## Principio Fundamental

LAS ACTUALIZACIONES PARA INVERSORES CONSTRUYEN CONFIANZA A TRAVÉS DE CONSISTENCIA Y TRANSPARENCIA — COMPARTE TANTO LOGROS COMO DESAFÍOS, Y SIEMPRE INCLUYE UNA SOLICITUD ESPECÍFICA.

---

## Fase 1: Información de Actualización

### Información Requerida

| Entrada | Qué Preguntar | Por Defecto |
|---------|---------------|------------|
| **Período de reporte** | "¿Para qué mes/trimestre es esta actualización?" | Mes anterior |
| **Métricas clave** | "¿Cuáles son tus métricas principales? (MRR, usuarios, ingresos, tasa de crecimiento)" | No hay predeterminado — debe proporcionarse |
| **Logros principales** | "¿Cuáles fueron los 2-3 principales logros este período?" | No hay predeterminado — debe proporcionarse |
| **Desafíos** | "¿Cuáles son los mayores desafíos o riesgos en este momento?" | No hay predeterminado — debe proporcionarse |
| **Solicitudes** | "¿Qué ayuda necesitas de los inversores? (presentaciones, consejo, contratación)" | No hay predeterminado — al menos una solicitud |
| **Posición de caja** | "¿Cuál es tu saldo de caja actual y runway?" | No hay predeterminado — debe proporcionarse |

**PUNTO DE CONTROL: No procedas sin métricas, logros, desafíos y posición de caja.**

---

## Fase 2: Estructura de Actualización

### Formato Estándar de Actualización para Inversores

```
Asunto: [Nombre de Empresa] — Actualización [Mes Año]

---

Hola [inversores/equipo],

[Resumen de 1-2 frases del mes — la versión del titular]

## Métricas Clave

| Métrica | Este Mes | Mes Anterior | Cambio MoM |
|---------|----------|-------------|-----------|
| MRR/Ingresos | $[X] | $[X] | +/-[X]% |
| Clientes/Usuarios | [X] | [X] | +/-[X]% |
| [Métrica Clave 3] | [X] | [X] | +/-[X]% |
| Saldo de Caja | $[X] | $[X] | |
| Runway | [X] meses | [X] meses | |

## Logros

1. **[Logro 1]** — [Descripción de 2-3 frases con impacto específico]
2. **[Logro 2]** — [Descripción de 2-3 frases]
3. **[Logro 3]** — [Descripción de 2-3 frases]

## Desafíos

1. **[Desafío 1]** — [Qué es + qué estás haciendo al respecto]
2. **[Desafío 2]** — [Qué es + qué estás haciendo al respecto]

## Actualización de Producto/Negocio

[2-3 frases sobre qué se lanzó, qué está en progreso, o qué decisiones estratégicas se tomaron este mes]

## Solicitudes

Podría usar tu ayuda con:
1. **[Solicitud específica]** — [Contexto sobre por qué y qué se vería como un buen resultado]
2. **[Solicitud específica]** — [Contexto]

## Qué Viene

[2-3 puntos viñeta sobre prioridades para el próximo mes]

---

Gracias por tu apoyo continuo.

[Tu nombre]
[Empresa]
```

---

## Fase 3: Directrices de Tono y Contenido

### Qué Incluir

- **Métricas:** Siempre incluye las mismas métricas cada mes para trendabilidad
- **Contexto:** Los números sin contexto son inútiles. "$50K MRR" no significa nada — "$50K MRR, arriba 15% de $43.5K, impulsado por acuerdo enterprise" significa todo.
- **Honestidad sobre desafíos:** Los inversores respetan a los fundadores que identifican problemas temprano. Ocultar malas noticias erosiona la confianza.
- **Solicitudes específicas:** "¿Puedes presentarme a..." es mejor que "buscando conexiones". Facilita que los inversores te ayuden.

### Tono

- Confiado pero honesto — no spin, no doom
- Basado en datos — afirmaciones respaldadas por números
- Conciso — apunta a máximo 500 palabras. Los inversores leen docenas de actualizaciones.
- Profesional pero personal — firma calurosamente, reconoce su apoyo

---

## Fase 4: Entrega

### Lista de Verificación Final

```
- [ ] Todas las métricas son exactas y coinciden con registros financieros
- [ ] Las métricas son consistentes con actualizaciones previas (mismo formato, mismos KPIs)
- [ ] Al menos 1 solicitud específica y accionable
- [ ] Posición de caja y runway son actuales
- [ ] La sección de desafíos es honesta e incluye planes de mitigación
- [ ] El email tiene menos de 500 palabras
- [ ] Enviado dentro de la primera semana del nuevo mes
```

### Notas de Entrega

- Envía como email de texto plano (no adjunto PDF)
- BCC a inversores si no se conocen entre sí, CC si sí se conocen
- Almacena una copia en tus registros para referencia
- Rastrear qué inversores responden — los inversores comprometidos son tu mejor recurso

---

## Ejemplo: Actualización Mensual SaaS Startup

**Asunto:** Acme AI — Actualización Enero 2026

**Resumen:** "Enero fue nuestro mejor mes hasta ahora — $32K MRR (arriba 22%), conseguimos nuestro primer cliente enterprise, y lanzamos la integración API que estaba bloqueando 3 acuerdos."

**Métricas:** MRR $32K (+22%), clientes 145 (+18), NRR 112%, caja $180K, runway 8 meses.

**Logro:** "Cerré un acuerdo enterprise de $2,400/mes con [Empresa] — nuestro primer cliente sobre $1K MRR. Esto valida el tier de precio enterprise que lanzamos en diciembre."

**Desafío:** "El churn subió a 4.2% de 3.1%. Causa raíz: fricción de onboarding para usuarios no técnicos. Estamos lanzando un asistente de configuración guiada para el 15 de febrero."

**Solicitud:** "Buscando una presentación a un candidato de Head of Sales con experiencia SaaS. Si alguien en tu red está explorando, me encantaría una presentación."

---

## Anti-Patrones

- **Omitir meses cuando las cosas van mal** — el silencio señala problemas. Los peores meses necesitan actualizaciones más.
- **Solo logros, sin desafíos** — los inversores ven a través del spin. Incluye al menos un desafío honesto.
- **Cambiar métricas cada mes** — elige 3-5 métricas centrales y reporta idénticamente cada mes para visibilidad de tendencias.
- **Sin solicitud** — los inversores quieren ayudar. Si nunca pides, asumen que no te necesitan.
- **Narrativas largas** — mantén bajo 500 palabras. Guarda los análisis profundos para juntas de junta.

---

## Recuperación

- **Mes vergonzoso (ingresos abajo, churn arriba):** Lidera con qué pasó, qué aprendiste, y qué estás haciendo al respecto. Los inversores respaldan a los fundadores que responden a la adversidad.
- **Sin inversores aún (enviando a asesores):** El mismo formato funciona. Los asesores aprecian actualizaciones estructuradas y solicitudes claras.
- **Primera actualización jamás:** Envía un email introductorio explicando que enviarás actualizaciones mensuales y qué esperar. Incluye una breve descripción general de la empresa.
- **Atrasado en actualizaciones:** Envía una actualización de "recuperación" cubriendo el período faltante. Reconoce la brecha. Reanuda la cadencia mensual inmediatamente.
