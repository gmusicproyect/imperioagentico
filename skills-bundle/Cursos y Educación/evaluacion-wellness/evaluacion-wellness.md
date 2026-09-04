---
name: evaluacion-wellness
description: "Construye evaluaciones de intake de wellness con historial de salud, establecimiento de metas y cuestionarios de evaluación de estilo de vida."
allowed-tools: Read Write Glob
author: Imperio Digital
version: "1.0"
---

# Evaluación de Wellness

## Cuándo Usar Este Skill

Usa este skill cuando necesites:
- Crear una evaluación de intake de wellness para nuevos clientes de coaching o entrenamiento
- Construir cuestionarios de historial de salud que informen el diseño del programa
- Diseñar frameworks de establecimiento de metas para compromisos de wellness
- Evaluar factores de estilo de vida que afecten resultados del cliente

**NO** uses este skill para formularios de intake médico, evaluaciones clínicas o cuestionarios diagnósticos. Es para coaches de wellness, entrenadores personales y coaches de salud operando dentro de su alcance de práctica.

---

## Principio Fundamental

UNA EVALUACIÓN DE WELLNESS NO ES UN EXAMEN MÉDICO — ES UNA HERRAMIENTA PARA ENTENDER DÓNDE ESTÁ TU CLIENTE, DÓNDE QUIEREN IR Y QUÉ FACTORES DE ESTILO DE VIDA AYUDARÁN O IMPEDIRÁN SU PROGRESO.

---

## Fase 1: Alcance de Evaluación

### Entradas Requeridas

| Entrada | Qué Preguntar | Predeterminado |
|---------|--------------|--------|
| **Tipo de servicio** | "¿Qué servicio proporcionarás — entrenamiento personal, coaching de salud, coaching de nutrición?" | Coaching de salud |
| **Población de clientes** | "¿Quiénes son tus clientes típicos?" | Adultos 30-55, wellness general |
| **Alcance de práctica** | "¿Cuáles son tus credenciales y qué estás calificado para evaluar?" | Sin predeterminado — debe proporcionarse |
| **Profundidad de evaluación** | "¿Cuán detallado — screening rápido o intake comprensivo?" | Intake comprensivo |
| **Evaluaciones de seguimiento** | "¿Reevaluarás periódicamente?" | Sí — cada 8-12 semanas |

**PUNTO DE CONTROL: Confirma alcance de práctica antes de diseñar la evaluación. Solo incluye secciones que estés calificado para evaluar.**

---

## Fase 2: Secciones de Evaluación

### Sección 1: Información Personal

```
## Información del Cliente

Nombre: _______________
Fecha: _______________
Fecha de nacimiento: _______________
Email: _______________
Teléfono: _______________
Contacto de emergencia: _______________
Teléfono de emergencia: _______________
```

### Sección 2: Historial de Salud

```
## Historial de Salud

**Condiciones médicas actuales (marca todas que apliquen):**
[ ] Enfermedad cardíaca o condición cardiovascular
[ ] Presión arterial alta
[ ] Diabetes (Tipo 1 / Tipo 2)
[ ] Asma o condición respiratoria
[ ] Problemas de articulación u óseos (artritis, osteoporosis)
[ ] Dolor de espalda o condiciones de columna
[ ] Condición de tiroides
[ ] Ansiedad o depresión
[ ] Condición autoinmune
[ ] Ninguno de los anteriores
[ ] Otro: _______________

**Medicamentos actuales:**
_______________

**Alergias (alimento, medicamento, ambiental):**
_______________

**Cirugías o lesiones pasadas:**
_______________

**¿Actualmente estás bajo cuidado de un médico para alguna condición?** Sí / No
Si es sí, ¿tu médico te ha dado luz verde para [ejercicio / cambios dietéticos]? Sí / No / Aún no

**Para mujeres: ¿Estás embarazada o planeando quedarte embarazada?** Sí / No / N/A

**¿Tienes alguna limitación física que afecte movimiento o ejercicio?**
_______________
```

### Sección 3: Evaluación de Estilo de Vida

```
## Estilo de Vida Actual

**Sueño:**
- Horas promedio por noche: ___
- Calidad de sueño (1-5, 5 = excelente): ___
- ¿Tienes problemas conciliando o manteniéndote dormido? Sí / No

**Estrés:**
- Nivel de estrés actual (1-10, 10 = extremadamente estresado): ___
- Top 3 fuentes de estrés: _______________
- ¿Cómo manejas actualmente el estrés? _______________

**Nutrición (día típico):**
- Desayuno: _______________
- Almuerzo: _______________
- Cena: _______________
- Snacks: _______________
- Consumo de agua (vasos por día): ___
- Alcohol (bebidas por semana): ___
- Cafeína (tazas por día): ___

**Actividad Física:**
- Frecuencia de ejercicio actual: ___ días/semana
- Tipos de ejercicio: _______________
- Nivel de actividad en el trabajo: Sedentario / Ligeramente activo / Activo / Muy activo

**Hábitos:**
- ¿Fumas? Sí / No / Antiguo
- Tiempo de pantalla (horas por día fuera del trabajo): ___
```

### Sección 4: Metas y Motivación

```
## Tus Metas

**Meta principal:**
_______________

**¿Por qué es importante esta meta para ti ahora?**
_______________

**¿Qué has intentado antes para lograr esta meta?**
_______________

**¿Qué funcionó? ¿Qué no?**
_______________

**En una escala de 1-10, ¿qué tan listo estás para hacer cambios?** ___

**En una escala de 1-10, ¿qué tan confiado estás que puedes tener éxito?** ___

**¿Cuál es el obstáculo más grande que anticipas?**
_______________

**¿Cómo sabrás que has tenido éxito? ¿Cómo se verá y se sentirá el éxito?**
_______________

**Timeline: ¿Cuándo quieres lograr esta meta?**
_______________
```

---

## Fase 3: Evaluación y Resumen

### Plantilla de Resumen de Evaluación

```
## Resumen de Evaluación de Wellness — [Nombre del Cliente]

**Fecha:** [Fecha]
**Evaluado por:** [Tu nombre]

### Hallazgos Clave

**Consideraciones de salud:**
- [Cualquier condición o medicamento que afecte programación]
- [¿Se necesita referencia? Sí/No — a quién]

**Fortalezas de estilo de vida:**
- [Qué ya están haciendo bien]

**Áreas de estilo de vida para mejorar:**
- [Brechas de sueño, estrés, nutrición o actividad]

**Alineación de meta:**
- Meta principal: [Meta]
- Nivel de disposición: [X/10]
- Nivel de confianza: [X/10]
- Timeline: [Timeline declarado — ¿realista? Sí/No]

### Áreas de Enfoque Recomendadas (Orden de Prioridad)

1. [Área de enfoque 1] — [Por qué y paso de acción inicial]
2. [Área de enfoque 2] — [Por qué y paso de acción inicial]
3. [Área de enfoque 3] — [Por qué y paso de acción inicial]

### Referidas Necesitadas
- [ ] Autorización médica del médico
- [ ] Dietista registrado para [preocupación específica]
- [ ] Profesional de salud mental para [preocupación específica]
- [ ] Fisioterapeuta para [preocupación específica]
- [X] Ninguna necesitada en este momento
```

### Plan de Reevaluación

Programa reevaluaciones en intervalos regulares:
- **Verificación de 4 semanas:** Revisión de progreso rápido, adherencia a hábitos, ajusta según sea necesario
- **Reevaluación de 8-12 semanas:** Comparación de evaluación completa, mide progreso hacia metas
- **Continuo:** Verificaciones mensuales breves entre evaluaciones completas

---

## Fase 4: Implementación

### Opciones de Entrega

| Formato | Mejor Para |
|--------|----------|
| Formulario de papel | Consultas presenciales |
| Google Form | Clientes remotos, recopilación automatizada |
| PDF rellenable | Intake basado en email |
| Software de gestión de práctica | Gestión integrada de clientes (Practice Better, TrueCoach) |

### Lista de Verificación de Evaluación

- [ ] Todas las secciones son apropiadas para tu alcance de práctica
- [ ] Sección de historial de salud cubre condiciones relevantes a tu servicio
- [ ] Consentimiento y descargo de responsabilidad están incluidos (ve skill de descargo de responsabilidad de salud)
- [ ] Se identifican disparadores de referencia (cuándo referir a profesional médico)
- [ ] La evaluación se almacena de forma segura y confidencial
- [ ] El cronograma de reevaluación se comunica al cliente
- [ ] El resumen se revisa con el cliente, no solo se archiva

---

## Anti-Patrones

- **Hacer preguntas médicas más allá de tu alcance** — si no eres médico, no diagnostiques. Recopila historial y refiere cuando sea apropiado.
- **Recopilar datos y nunca usarlos** — cada pregunta debe informar tu programación. Elimina preguntas que no cambien lo que haces.
- **Saltarse el historial de salud** — comenzar un programa de fitness o nutrición sin conocer condiciones médicas es imprudente.
- **No seguir banderas rojas** — si un cliente reporta dolor en el pecho durante ejercicio o una condición no manejada, refiere a médico antes de continuar.
- **Una evaluación y listo** — el seguimiento de progreso requiere reevaluación. Constrúyelo en tu proceso.

---

## Recuperación

- **El cliente no revela una condición:** Incluye una cláusula que el cliente es responsable de revelar toda información de salud relevante y actualizarte si su estado cambia.
- **Bandera roja en historial de salud:** Pausa programación y requiere autorización médica. No diseñes programas alrededor de condiciones que no estés calificado para manejar.
- **El cliente es resistente a la evaluación:** Explica que la evaluación asegura su seguridad y te ayuda a diseñar el programa más efectivo para ellos.
- **La evaluación es demasiado larga:** Recorta a secciones esenciales solamente. Una evaluación de 30 minutos que se completa vence una de 60 minutos que se abandona.
- **Las metas del cliente son poco realistas:** Ten una conversación honesta. Ajusta la timeline o reenmarca la meta para ser lograble y medible.
