---
name: planificador-horario-clases
description: "Planifica horarios de clases/sesiones con asignación de instructores, asignación de espacios y gestión de capacidad de inscripción."
allowed-tools: Read Write Glob
author: Imperio Digital
version: "1.0"
---

# Planificador de Horario de Clases

## Cuándo Usar Este Skill

Usa este skill cuando necesites:
- Planificar un horario semanal de clases o sesiones para un estudio, gimnasio o centro de aprendizaje
- Asignar instructores a franjas horarias mientras gestionas disponibilidad y especialidades
- Asignar espacios o salones basado en tamaño de clase y necesidades de equipo
- Gestionar capacidad de inscripción y listas de espera

**NO** uses este skill para programación de citas individuales, planificación de eventos o programación académica escolar. Es para horarios de clases grupos recurrentes en estudios de fitness, estudios de yoga, centros de aprendizaje o instalaciones similares.

---

## Principio Fundamental

UN HORARIO BIEN DISEÑADO MAXIMIZA LA UTILIZACIÓN DEL ESPACIO Y EL TALENTO DEL INSTRUCTOR MIENTRAS COINCIDE CON LOS TIEMPOS Y CLASES QUE TUS CLIENTES REALMENTE QUIEREN — CONSTRUYE ALREDEDOR DE LA DEMANDA, NO DE LA CONVENIENCIA.

---

## Fase 1: Parámetros del Horario

### Entradas Requeridas

| Entrada | Qué Preguntar | Predeterminado |
|---------|--------------|--------|
| **Tipo de instalación** | "¿Qué tipo de instalación — estudio de fitness, estudio de yoga, centro de aprendizaje, otro?" | Estudio de fitness |
| **Espacios/salas** | "¿Cuántos espacios o salas están disponibles y cuál es su capacidad?" | 1 estudio principal, capacidad 20 |
| **Horas de operación** | "¿Cuáles son tus horas de operación?" | 6 AM - 9 PM entre semana, 8 AM - 2 PM fines de semana |
| **Tipos de clases** | "¿Qué clases ofreces?" | Sin predeterminado — debe proporcionarse |
| **Instructores** | "¿Cuántos instructores, su disponibilidad y especialidades?" | Sin predeterminado — debe proporcionarse |
| **Horas pico de demanda** | "¿Cuándo quieren la mayoría de clientes asistir?" | Madrugada (6-8 AM) y tarde (5-7 PM) entre semana |

**PUNTO DE CONTROL: Confirma espacios, instructores y tipos de clases antes de construir el horario.**

---

## Fase 2: Diseño del Horario

### Plantilla de Cuadrícula de Horario

```
## Horario de Clases Semanal — [Nombre de Instalación]

### Estudio A (Capacidad: 20)

| Hora | Lunes | Martes | Miércoles | Jueves | Viernes | Sábado | Domingo |
|------|--------|---------|-----------|--------|---------|----------|---------|
| 6:00 AM | [Clase] | — | [Clase] | — | [Clase] | — | — |
| 7:00 AM | [Clase] | [Clase] | [Clase] | [Clase] | [Clase] | [Clase] | — |
| 9:00 AM | [Clase] | [Clase] | [Clase] | [Clase] | [Clase] | [Clase] | [Clase] |
| 12:00 PM | [Clase] | — | [Clase] | — | [Clase] | — | — |
| 5:30 PM | [Clase] | [Clase] | [Clase] | [Clase] | [Clase] | — | — |
| 6:30 PM | [Clase] | [Clase] | [Clase] | [Clase] | — | — | — |
```

### Reglas de Programación

1. **Las horas pico obtienen tus clases más populares** — no programes clases de nicho a las 5:30 PM
2. **Tiempo de buffer entre clases** — 15-30 minutos para limpieza, configuración y llegadas tardías
3. **Límites del instructor** — ningún instructor enseña más de 3 clases seguidas
4. **Variedad de clases en el día** — evita programar clases similares en franjas horarias adyacentes
5. **Horarios de fin de semana reflejan demanda** — menos clases, enfoque a media mañana

### Estrategia de Mezcla de Clases

| Franja Horaria | Mejores Tipos de Clase | Audiencia |
|-----------|-----------------|----------|
| Madrugada (6-7 AM) | Alta energía — HIIT, ciclismo, boot camp | Multitud pre-trabajo |
| Media mañana (9-10 AM) | Moderado — yoga, pilates, barre | Padres en casa, jubilados, trabajadores remotos |
| Almuerzo (12-1 PM) | Rápidas — clases express de 45 min | Trabajadores de oficina |
| Post-trabajo (5-7 PM) | Variedad popular — fuerza, cardio, yoga | Multitud post-trabajo |
| Noche (7-8 PM) | Recuperación — yoga, estiramiento, meditación | Buscadores de relajación |
| Mañana de fin de semana | Comunidad — clases más largas, workshops | Horarios flexibles |

---

## Fase 3: Gestión de Instructor y Espacio

### Matriz de Asignación de Instructor

```
## Asignaciones de Instructor

| Instructor | Especialidades | Disponibilidad | Clases Semanales | Máx Clases |
|-----------|-------------|-------------|----------------|------------|
| [Nombre 1] | Yoga, Pilates | L/M/V mañanas, M/J noches | 6 | 8 |
| [Nombre 2] | HIIT, Fuerza | L-V mañanas y noches | 8 | 10 |
| [Nombre 3] | Ciclismo, Cardio | M/J/S | 4 | 6 |
```

### Política de Sub/Cobertura

```
## Política de Sustitución de Instructor

1. El instructor notifica a la gerencia [48] horas antes de ausencia
2. El instructor es responsable de encontrar un sub calificado de la lista aprobada
3. Si no se encuentra sub, la gerencia intenta cubrir o cancela con aviso
4. Aviso de cancelación enviado a clientes inscritos al menos [4] horas antes
5. A los instructores suplentes se les paga [misma tarifa / tarifa plana de suplencia de $X]
```

### Asignación de Espacios (Instalaciones Multi-Espacio)

| Espacio | Capacidad | Equipo | Mejor Para |
|-------|----------|-----------|----------|
| Estudio A | 25 | Espejos, sistema de sonido, tapetes | Fitness grupal, danza, yoga |
| Estudio B | 12 | Bicicletas estáticas, pantallas | Ciclismo, entrenamiento pequeño grupo |
| Espacio al aire libre | 15 | Ninguno (portátil) | Boot camp, clases estacionales |

---

## Fase 4: Inscripción y Capacidad

### Gestión de Capacidad

```
## Configuración de Inscripción

| Clase | Capacidad | Mín para Ejecutar | Límite Lista Espera |
|-------|----------|-----------|---------------|
| Yoga Flow | 20 | 3 | 5 |
| HIIT | 15 | 4 | 5 |
| Ciclismo | 12 | 3 | 3 |
| Boot Camp | 20 | 5 | 5 |
```

### Reglas de Lista de Espera

- Los clientes en lista de espera se notifican automáticamente cuando se abre un lugar
- Los clientes tienen [2] horas para confirmar o pierden su lugar
- Los no asistentes se rastrean — 3 no asistencias en 30 días resulta en restricciones de reserva

### Cadencia de Revisión de Horario

| Frecuencia | Revisión |
|-----------|--------|
| Semanal | Verifica asistencia por clase, aborda clases de baja inscripción |
| Mensual | Revisa rendimiento general del horario, feedback del instructor |
| Trimestral | Ajusta horas de clase, agrega/quita clases basado en tendencias de demanda |
| Estacionalmente | Cuenta para cambios estacionales (caída estival, subida de enero) |

### Métricas Clave

| Métrica | Objetivo |
|--------|--------|
| Tasa promedio de llenado de clase | 70%+ de capacidad |
| Clases canceladas (baja inscripción) | Menos del 5% |
| Tasa de conversión de lista de espera | 60%+ |
| Tasa de no asistencia | Menos del 15% |
| Utilización de instructor | 70-85% de horas disponibles |

---

## Anti-Patrones

- **Programación basada en preferencia del instructor, no demanda** — el horario debe servir primero a los clientes.
- **Sin buffer entre clases** — clases seguidas sin tiempo de transición crean caos.
- **Demasiados tipos de clase** — esparcirse entre 15 tipos de clase diluye la calidad. Enfócate en 5-8 ofertas principales.
- **Ignorar datos de asistencia** — una clase que promedia 2 asistentes debe moverse, cambiarse o cancelarse.
- **Horario estático todo el año** — la demanda cambia estacionalmente. Ajusta en consecuencia.

---

## Recuperación

- **Asistencia constantemente baja para una clase:** Muévela a una franja horaria diferente, prueba con un instructor diferente, o reemplázala con un formato más popular.
- **Agotamiento del instructor:** Reduce su conteo de clases semanal, asegura días de descanso, capacita a otros instructores en sus especialidades.
- **Conflictos de programación entre instructores:** Usa un calendario compartido y confirma disponibilidad antes de publicar el horario.
- **Caída de inscripción estacional:** Ofrece promociones limitadas, agrega temas de clase estacionales, reduce el horario temporalmente en lugar de ejecutar clases vacías.
- **Nuevo tipo de clase no ganando tracción:** Dale 6-8 semanas con promoción activa antes de cancelar. Ofrece precios introductorios para construir una base.
