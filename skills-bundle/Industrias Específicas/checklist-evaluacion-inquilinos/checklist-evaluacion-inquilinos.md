---
name: checklist-evaluacion-inquilinos
description: "Crea listas de verificación de evaluación de inquilinos con pasos de verificación, preguntas de revisión de referencias y criterios de evaluación."
allowed-tools: Read Write Glob
metadata:
  author: Imperio Digital
  version: "1.0"
---

# Lista de Verificación de Evaluación de Inquilinos

## Cuándo Usar Este Skill

Usa este skill cuando necesites:
- Construir un proceso consistente de evaluación de inquilinos para propiedades de alquiler
- Crear listas de verificación de verificación de ingresos, crédito e historial de alquiler
- Escribir preguntas de verificación de referencias para propietarios anteriores y empleadores
- Diseñar criterios de evaluación que seleccionen inquilinos confiables de manera justa

**NO** uses este skill para evaluación de inquilinos comerciales, selección de compañero de casa o procesos de desalojo de inquilinos. Esto es para evaluación residencial de propietarios de propietarios de posibles inquilinos.

---

## Principio Fundamental

LA EVALUACIÓN CONSISTENTE APLICADA EQUITATIVAMENTE A CADA SOLICITANTE TE PROTEGE LEGALMENTE Y SELECCIONA MEJOR INQUILINOS — NUNCA OMITAS PASOS NI APLIQUES ESTÁNDARES DIFERENTES A DIFERENTES PERSONAS.

---

## Fase 1: Estándares de Evaluación

### Información Requerida

| Entrada | Qué Preguntar | Predeterminado |
|---------|--------------|--------|
| **Tipo de propiedad** | "¿Qué tipo de alquiler — casa unifamiliar, multifamiliar, condominio?" | Alquiler unifamiliar |
| **Renta mensual** | "¿Cuál es la renta mensual?" | Sin predeterminado — debe proporcionarse |
| **Puntuación de crédito mínima** | "¿Qué puntuación de crédito requieres?" | 620 |
| **Requisito de ingresos** | "¿Relación de ingresos a renta?" | 3x renta mensual |
| **Política de mascotas** | "¿Permites mascotas? ¿Restricciones?" | Caso a caso |
| **Estado/jurisdicción** | "¿En qué estado está la propiedad?" | Sin predeterminado — afecta requisitos legales |

**PUNTO DE CONTROL: Confirma estándares de evaluación y requisitos legales locales antes de construir la lista de verificación.**

---

## Fase 2: Lista de Verificación de Solicitud

### Documentos Requeridos

```
## Lista de Verificación de Solicitud de Inquilino

### Verificación de Identidad
- [ ] ID con foto emitida por el gobierno (licencia de conducir, pasaporte)
- [ ] Número de Seguro Social (para verificación de crédito/antecedentes)
- [ ] Formulario de solicitud firmado con autorización de evaluación

### Verificación de Ingresos
- [ ] Últimos 3 talones de pago (o 2 meses de extractos bancarios para trabajadores por cuenta propia)
- [ ] Carta de verificación de empleo u oferta de empleo
- [ ] Declaraciones de impuestos (si es trabajador por cuenta propia — últimos 2 años)
- [ ] Ingresos cumplen con mínimo [3x] renta mensual: $[cantidad]/mes requerida

### Historial de Alquiler
- [ ] Información de contacto para últimos 2-3 propietarios
- [ ] Direcciones de alquiler y fechas para últimos 3-5 años
- [ ] Explicación de brechas en el historial de alquiler

### Crédito y Antecedentes
- [ ] Informe de crédito obtenido (puntuación: mínimo [620])
- [ ] Revisión de antecedentes completada
- [ ] Búsqueda de historial de desalojo completada
- [ ] Búsqueda en registro de delincuentes sexuales (donde sea legalmente requerido/permitido)
```

---

## Fase 3: Procedimientos de Verificación

### Preguntas de Verificación de Propietario

Llama a propietarios anteriores y pregunta:

```
## Revisión de Referencia de Propietario

**Nombre del inquilino:** _______________
**Dirección de propiedad:** _______________
**Nombre del propietario:** _______________
**Fecha de llamada:** _______________

1. ¿Puedes confirmar que [nombre del inquilino] alquiló de ti en [dirección]?
2. ¿Cuáles fueron las fechas del arrendamiento? (De ___ a ___)
3. ¿Cuál era la renta mensual? $___
4. ¿Se pagaba la renta a tiempo de manera consistente? (Sí / Usualmente / No)
5. ¿Hubo violaciones de arrendamiento o quejas? (Sí / No — detalles)
6. ¿Se devolvió el depósito de seguridad en su totalidad? (Sí / Parcial / No — razón)
7. ¿Dieron aviso adecuado de mudanza? (Sí / No)
8. ¿Los rentarías de nuevo? (Sí / No — razón)
9. ¿Cuántos ocupantes vivían en la unidad?
10. ¿Hay daño a la propiedad más allá del desgaste normal?
```

### Verificación de Empleo

```
## Verificación de Empleo

**Nombre del solicitante:** _______________
**Empleador:** _______________
**Contacto:** _______________

1. ¿Puedes confirmar que [nombre] está actualmente empleado con tu empresa?
2. ¿Cuál es su posición/título?
3. ¿Por cuánto tiempo han estado empleados?
4. ¿Su posición es tiempo completo o tiempo parcial?
5. ¿Puedes verificar sus ingresos declarados de $___/mes? (Sí / No / Incapaz de divulgar)
```

### Evaluación de Informe de Crédito

| Factor | Bandera Verde | Bandera Amarilla | Bandera Roja |
|--------|-----------|-------------|----------|
| Puntuación de crédito | 700+ | 620-699 | Debajo de 620 |
| Historial de pagos | Sin pagos atrasados | 1-2 atrasados (30 días) | Cobros o castigos |
| Deuda-ingresos | Debajo de 35% | 35-45% | Arriba de 45% |
| Historial de desalojo | Ninguno | Ninguno pero tenencias cortas | Desalojo anterior |
| Bancarrotas | Ninguno | Descargado 5+ años atrás | Reciente o activo |

---

## Fase 4: Marco de Decisión

### Matriz de Puntuación

```
## Evaluación de Solicitante — [Nombre]

| Criterios | Ponderación | Puntuación (1-5) | Puntuación Ponderada |
|----------|--------|------------|----------------|
| Calificación de ingresos | 25% | [X] | [X] |
| Puntuación de crédito/historial | 25% | [X] | [X] |
| Referencias de alquiler | 25% | [X] | [X] |
| Estabilidad de empleo | 15% | [X] | [X] |
| Completitud de aplicación | 10% | [X] | [X] |
| **Total** | 100% | | **[X/5.0]** |

**Decisión:** Aceptar / Aceptación Condicional / Rechazar
**Condiciones (si aplica):** [Depósito adicional, codeudor, etc.]
```

### Proceso de Rechazo

Si rechazas una solicitud:
- Proporciona un aviso de acción adversa según lo requerido por la Ley de Informes de Crédito Justo
- Establece la razón del rechazo en términos objetivos y no discriminatorios
- Incluye la información de contacto de la oficina de crédito si el crédito fue un factor
- Devuelve las tarifas de solicitud si lo requiere la ley local
- Documenta la razón del rechazo para tus registros

### Cumplimiento de Vivienda Justa

Aplica cada criterio de evaluación de manera idéntica a cada solicitante:
- Misma puntuación de crédito mínima para todos
- Misma relación de ingresos para todos
- Mismo proceso de revisión de referencias para todos
- Documenta todo — tu consistencia es tu protección legal
- Nunca hagas excepciones basadas en características de clase protegida

---

## Anti-Patrones

- **Saltarse revisiones de referencias** — un informe de crédito limpio no te dice cómo el inquilino trató la propiedad anterior. Llama a propietarios anteriores.
- **Estándares inconsistentes** — aplicar criterios diferentes a diferentes solicitantes crea responsabilidad de vivienda justa.
- **Solo revisar el propietario más reciente** — el propietario actual puede dar una buena referencia solo para mover a un inquilino problemático. Revisa 2-3 propietarios atrás.
- **Sin criterios escritos** — los estándares no documentados no pueden defenderse. Escribe tus criterios antes de evaluar a alguien.
- **Apresurarse a llenar una vacancia** — un inquilino malo cuesta más que un mes vacío. Evalúa a fondo cada vez.

---

## Recuperación

- **El solicitante no tiene historial de alquiler:** Acepta otras referencias (empleador, profesional, personal). Considera un depósito más alto o codeudor.
- **No puedes contactar a propietarios anteriores:** Pide al solicitante contactos alternativos. Verifica la propiedad en registros de propiedad. Documenta tus intentos.
- **Puntuación de crédito límite:** Considera el cuadro completo — ingresos estables, referencias fuertes y una explicación razonable pueden compensar una puntuación más baja.
- **El solicitante reclama discriminación:** Revisa tus registros mostrando criterios consistentes aplicados a todos los solicitantes. Consulta a un abogado si se presenta una queja formal.
- **Las leyes locales restringen criterios de evaluación:** Investiga las limitaciones específicas de tu jurisdicción (algunas ciudades restringen revisiones de crédito o evaluación del historial penal).
