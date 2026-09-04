---
name: planificador-conferencia
description: "Planifica conferencias de múltiples días con pistas, gestión de speakers, logística, patrocinio y diseño de experiencia de asistentes."
allowed-tools: Read Write Glob
metadata:
  author: Imperio Digital
  version: "1.0"
---

# Planificador de Conferencia

## Cuándo Usar Este Skill

Usa este skill cuando necesites:
- Planificar una conferencia de múltiples días con múltiples pistas y speakers
- Gestionar logística incluyendo venue, catering, AV y flujo de asistentes
- Crear procesos de gestión de speakers y sistemas de curación de contenido
- Diseñar la experiencia completa de asistentes desde registro hasta seguimiento post-evento

**NO** uses este skill para workshops individuales, webinars o pequeños meetups. Esto es para conferencias con 100+ asistentes, múltiples sesiones y logística compleja.

---

## Principio Fundamental

UNA CONFERENCIA NO ES UNA COLECCIÓN DE CHARLAS — ES UNA EXPERIENCIA CURADA DONDE CONTENIDO, NETWORKING Y LOGÍSTICA TRABAJAN JUNTOS PARA CREAR VALOR QUE NO PUEDE SER REPLICADO VIENDO GRABACIONES.

---

## Fase 1: Brief

### Inputs Requeridos

| Input | Qué Preguntar | Predeterminado |
|-------|------------|---------|
| **Tema de conferencia** | "¿De qué trata la conferencia?" | Sin predeterminado — debe proporcionarse |
| **Duración** | "¿Cuántos días?" | 2 días |
| **Asistencia esperada** | "¿Cuántos asistentes?" | 200-300 |
| **Formato** | "¿In-person, virtual o híbrido?" | In-person |
| **Presupuesto** | "¿Cuál es el presupuesto total?" | $50,000 |
| **Modelo de ingresos** | "¿Ventas de entradas, patrocinios o ambos?" | Ambos |
| **Rango de fechas** | "¿Cuándo es el evento?" | Sin predeterminado — debe proporcionarse |

**PUNTO DE CONTROL:** Confirma el brief antes de proceder.

---

## Fase 2: Arquitectura

### Estructura de Conferencia

```
## Día 1
**Mañana:** Keynote de apertura (60 min) → Sesiones de breakout Track A/B (2 x 45 min)
**Almuerzo:** Almuerzo patrocinado + networking (90 min)
**Tarde:** Sesiones de breakout Track A/B (2 x 45 min) → Discusión en panel (60 min)
**Noche:** Recepción de networking (2 horas)

## Día 2
**Mañana:** Keynote (60 min) → Sesiones de breakout Track A/B (2 x 45 min)
**Almuerzo:** Discusiones en mesa redonda (90 min)
**Tarde:** Sesiones de workshop (90 min) → Keynote de cierre (45 min)
**Cierre:** Resumen + próximos pasos (15 min)
```

### Diseño de Pista

```
| Pista | Enfoque | Audiencia | Sesiones |
|-------|-------|----------|----------|
| Pista A | [Tema] | [Principiante/Intermedio] | [X sesiones] |
| Pista B | [Tema] | [Intermedio/Avanzado] | [X sesiones] |
```

### Plan de Speakers

```
## Objetivos de Speakers
- Keynotes: [2-3 nombres o descripciones de perfil]
- Speakers de breakout: [8-12 speakers necesarios]
- Panelistas: [4-6 por panel]
- Facilitadores de workshop: [2-4]

## Paquete de Speaker
- Compensación: [Tarifa, viaje, hotel, entrada gratuita]
- Requisitos: [Plazo de diapositivas, bio, foto de perfil, necesidades de AV]
- Cronograma de comunicación: [Alcance → confirmar → preparar → evento]
```

**PUNTO DE CONTROL:** Presenta la arquitectura de conferencia para aprobación.

---

## Fase 3: Construir

### Documento Maestra de Planificación

**1. Venue y Logística**
```
## Requisitos de Venue
- Escenario principal: [capacidad, necesidades de AV]
- Salas de breakout: [número, capacidad cada una]
- Área de networking: [requisitos de espacio]
- Área de patrocinador: [espacio de booth/mesa]
- Área de registro: [estaciones de check-in]
- Catering: [comidas, descansos, acomodaciones dietéticas]
```

**2. Cronograma (Trabajando Hacia Atrás)**
```
6 meses antes: Venue reservado, tema finalizado, alcance de speakers comienza
4 meses antes: Speakers confirmados, ventas de patrocinio abren, entradas early bird se lanzan
3 meses antes: Cronograma publicado, aumento de marketing
2 meses antes: Materiales de patrocinador vencidos, AV confirmado, voluntarios reclutados
1 mes antes: Cronograma final, comunicaciones de asistentes, borrador de run-of-show
2 semanas antes: Confirmación logística final, llamadas de preparación de speakers
1 semana antes: Materiales impresos, señalización, bolsas de swag preparadas
Día anterior: Caminata de venue, tech check, briefing de equipo
```

**3. Plantilla de Presupuesto**
```
| Categoría | Estimado | Real | Notas |
|----------|----------|--------|-------|
| Venue | $[X] | | |
| Catering | $[X] | | |
| AV/Tech | $[X] | | |
| Tarifas/viajes de speakers | $[X] | | |
| Marketing | $[X] | | |
| Impresión/señalización | $[X] | | |
| Swag/materiales | $[X] | | |
| Personal/voluntarios | $[X] | | |
| Contingencia (10%) | $[X] | | |
| **Total** | **$[X]** | | |
```

**4. Mapa de Experiencia de Asistente**
```
Registro → Email de bienvenida → Descarga de app de evento → Check-in Día 1 →
Sesión de bienvenida → Pistas de contenido → Actividades de networking → Contenido Día 2 →
Sesión de cierre → Email de agradecimiento → Acceso a grabaciones → Encuesta de feedback →
Oferta early bird del próximo año
```

---

## Fase 4: Pulir

### 1. Lista de Verificación Pre-Evento

```
## 1 Semana Antes
- [ ] Todos los speakers confirmados y preparados
- [ ] AV probado en venue
- [ ] Equipo de voluntarios briefed y asignado
- [ ] Comunicaciones de asistentes enviadas (cronograma, logística, estacionamiento)
- [ ] Señalización y materiales impresos
- [ ] Plan de emergencia en lugar (médico, clima, fallo técnico)
- [ ] Documento de run-of-show finalizado y distribuido
```

### 2. Operaciones del Día del Evento

```
## Asignaciones de Equipo del Día del Evento
- Registro: [X personas]
- Gestión de escenario: [X personas]
- Enlace de speaker: [1 persona por pista]
- Tech de AV: [1-2 personas]
- Soporte de patrocinador: [1 persona]
- Soporte de asistente: [X personas]
- Fotografía/redes sociales: [1-2 personas]
```

### 3. Plan Post-Evento

```
## Cronograma Post-Evento
Día 1: Email de agradecimiento a todos los asistentes
Día 3: Agradecimiento a speaker + procesamiento de pago
Día 5: Distribución de encuesta de asistentes
Semana 2: Edición y distribución de grabaciones
Semana 3: Reportes de impacto de patrocinador entregados
Semana 4: Debrief de equipo y lecciones aprendidas
Mes 2: Anuncio early bird para el próximo año
```

---

## Ejemplo 1: Conferencia Empresarial de 200 Personas (2 Días)

```
Tema: "Escalar Sin un Equipo" — herramientas y estrategias para solopreneurs
Pistas: Sistemas & Automatización, Marketing & Ventas
Keynotes: 2 (apertura y cierre cada día)
Breakouts: 8 sesiones en 2 pistas
Presupuesto: $45,000 (compensado por $20K patrocinio + $30K ventas de entradas)
```

## Ejemplo 2: Cumbre de Industria de 500 Personas (3 Días)

```
Tema: "El Futuro de [Industria]" — tendencias, tecnología y transformación
Pistas: Estrategia, Tecnología, Liderazgo
Keynotes: 3 (uno por día)
Breakouts: 18 sesiones, 3 workshops, 2 paneles
Presupuesto: $120,000 (fuertemente patrocinado, precios de entradas premium)
```

---

## Anti-Patrones

- **Demasiadas sesiones** — calidad sobre cantidad. Los asistentes no pueden asistir a todo, así que cura sin piedad.
- **Sin tiempo de networking** — sesiones espalda con espalda sin descansos previenen las conexiones que hacen valiosas las conferencias.
- **Ignorar el viaje del asistente** — si alguien no puede descubrir dónde ir, qué asistir o cómo conectar, la experiencia falla.
- **Presupuestar poco en AV** — el audio malo arruina cada sesión. Invierte en AV profesional o no hagas in-person.
- **Sin presupuesto de contingencia** — algo irá mal. Presupuesta 10-15% para sorpresas.
- **Comenzar planificación demasiado tarde** — una conferencia de 200 personas necesita mínimo 4-6 meses de tiempo de anticipación.

---

## Recuperación

- **El presupuesto es demasiado pequeño para la visión:** Reduce la asistencia, reduce a 1 día o aumenta objetivos de patrocinio. Haz menos cosas bien.
- **No puedes llenar slots de speakers:** Abre una CFP (call for proposals) a tu comunidad. Los speakers de pares a menudo son más relacionables que celebridades.
- **Ventas de entradas son lentas:** Agrega urgencia (plazo early bird), aumenta promoción, ofrece descuentos de grupo o da a registrados existentes un incentivo de referencia.
- **Venue se cae:** Ten un venue de backup identificado desde el inicio. Para emergencias, pivota a virtual con 30+ días de aviso.
