---
name: estructura-de-comisiones
description: "Diseña estructuras de comisiones de ventas con niveles, aceleradores, disposiciones de recuperación y cronogramas de pago. Utiliza cuando crees o revises planes de compensación para roles de ventas."
allowed-tools: Read Write Glob
author: Imperio Digital
version: "1.0"
---

# Estructura de Comisiones

## Cuándo Usar Esta Habilidad

Utiliza esta habilidad cuando necesites:
- Diseñar un plan de comisión para representantes de ventas o afiliados
- Crear estructuras de comisión escalonadas con aceleradores
- Definir disposiciones de recuperación y cronogramas de pago
- Construir un plan de compensación que alinee incentivos con objetivos empresariales

**NO** uses esta habilidad para planificación de salarios de empleados, tarjetas de tarifas freelance o términos de programas afiliados (usa affiliate-terms). Esto es para diseño de comisión de ventas.

---

## Principio Fundamental

UNA ESTRUCTURA DE COMISIÓN DEBE HACER QUE EL COMPORTAMIENTO DE MAYOR INGRESOS DEL REP SEA IDÉNTICO AL RESULTADO DE MAYOR VALOR DE LA EMPRESA.

---

## Fase 1: Contexto Empresarial

### Entradas Requeridas

| Entrada | Qué Preguntar | Predeterminado |
|---------|---------------|----------------|
| **Modelo de ventas** | "¿Qué estás vendiendo? (SaaS, servicios, productos, única vez, recurrente)" | Sin predeterminado — debe proporcionarse |
| **Tamaño promedio de trato** | "¿Cuál es el valor promedio de venta/contrato?" | Sin predeterminado — debe proporcionarse |
| **Duración del ciclo de ventas** | "¿Cuánto tiempo desde el primer contacto hasta el cierre?" | 30 días |
| **Margen bruto** | "¿Cuál es tu margen bruto en ventas?" | 60% |
| **OTE de destino** | "¿Cuál debe ser la compensación total (base + comisión) que gane un rep?" | $75,000 |
| **División base/variable** | "¿Qué división entre salario base y comisión variable?" | 50/50 |
| **Período de cuota** | "¿Cuotas mensuales o trimestrales?" | Mensualmente |

**PUNTO DE CONTROL: No procedas sin modelo de ventas, tamaño de trato y OTE de destino.**

---

## Fase 2: Diseño de Estructura

### Opciones de Modelo de Comisión

```
## Estructura de Comisión: [Nombre de Empresa]

### Selección de Modelo

| Modelo | Mejor Para | Complejidad |
|--------|-----------|------------|
| Porcentaje plano | Productos simples, etapa temprana | Baja |
| Escalonado (% creciente) | Motivar sobredesempeño | Media |
| Escalonado con aceleradores | Ventas SaaS, empresariales | Alta |
| Participación de ingresos | Ingresos recurrentes, asociaciones | Media |
| Basado en margen bruto | Servicios con márgenes variables | Media |

### Modelo Seleccionado: [Escalonado con Aceleradores]
```

### Tabla de Comisión

```
### Tasas de Comisión

| Cumplimiento de Cuota | Tasa de Comisión | Pago de Ejemplo |
|----------------------|-----------------|-----------------|
| 0-50% de cuota | [X]% (tasa base) | $[X] |
| 51-100% de cuota | [X]% (tasa estándar) | $[X] |
| 101-125% de cuota | [X]% (acelerador 1) | $[X] |
| 126-150% de cuota | [X]% (acelerador 2) | $[X] |
| 150%+ de cuota | [X]% (kicker) | $[X] |

### Cuota
- Cuota mensual: $[X] en [ingresos / reservas / tratos cerrados]
- Cuota trimestral: $[X]
- Cuota anual: $[X]

### Desglose de OTE
| Componente | Cantidad | % de OTE |
|-----------|----------|---------|
| Salario base | $[X]/mes | [50]% |
| Variable de destino (a 100% de cuota) | $[X]/mes | [50]% |
| **OTE Total** | **$[X]/mes** | **100%** |
```

---

## Fase 3: Reglas y Disposiciones

### Clawback y Recuperación

```
### Disposiciones de Clawback

| Escenario | Regla de Clawback |
|-----------|------------------|
| Cliente cancela dentro de [30] días | Clawback de comisión 100% |
| Cliente cancela dentro de [31-90] días | Clawback de comisión 50% |
| Cliente falla en pago | Comisión revertida en contracargo/no pago |
| Venta fraudulenta | Clawback 100% + acción disciplinaria |

### Cronograma de Pago
- Comisión calculada: [Final de cada mes]
- Comisión pagada: [15 del mes siguiente]
- Ventana de clawback: [90 días desde fecha de venta]
- Umbral de pago mínimo: $[50]
```

### Reglas Especiales

```
### Disposiciones Adicionales

**Rampa de rep nuevo:** Rampa de [X] meses con cuota reducida
- Mes 1: [50]% cuota, tasa de comisión completa
- Mes 2: [75]% cuota, tasa de comisión completa
- Mes 3+: Cuota completa

**Tratos en equipo:** Si dos reps colaboran, la comisión se divide [50/50 o basada en contribución].

**Renovaciones:** [X]% comisión en renovaciones de clientes (típicamente más baja que tasa de negocio nuevo).

**Upsells/expansión:** Tratado como [tasa de negocio nuevo / renovación] dependiendo de [criterios].

**Spiffs (bonificaciones):** Bonificación de $[X] por [comportamiento específico — tratos de múltiples años, cuentas estratégicas, ventas de nuevo producto].
```

---

## Fase 4: Documentación

### Documento del Plan de Comisión

```
## Plan de Comisión de Ventas [Empresa] — [Año]

### Resumen del Plan
- Fecha efectiva: [Fecha]
- Período del plan: [Anual / Trimestral]
- Roles elegibles: [Listar]
- Cambios desde plan anterior: [Listar o "Nuevo plan"]

### Estructura de Compensación
[Insertar tablas de Fase 2]

### Reglas y Disposiciones
[Insertar de Fase 3]

### Resolución de Disputas
Las disputas de comisión deben presentarse por escrito dentro de [30] días
del estado de comisión. Resolución dentro de [15] días hábiles.

### Modificaciones del Plan
La empresa se reserva el derecho de modificar el plan con [30] días de notificación.
Los cambios no afectan las comisiones ya ganadas.

### Reconocimiento
Firma del empleado: _______________
Fecha: _______________
```

---

## Ejemplo: Empresa SaaS (ACV $12,000)

**OTE:** $90K ($45K base + $45K variable). Cuota mensual: $40K en nuevo ARR.

| Cumplimiento | Tasa | Pago en $40K |
|-------------|------|-------------|
| 0-75% | 5% | Hasta $1,500 |
| 76-100% | 10% | $1,500-$2,500 |
| 101-125% | 15% | $2,500-$4,375 |
| 125%+ | 20% | $4,375+ sin tope |

A 100% de cuota: $3,750/mes variable = $45K anual. Clawback: 100% si churn en 60 días.

---

## Anti-Patrones

- **Comisiones limitadas** — los topes matan la motivación una vez que un rep alcanza la cuota. Los mejores desempeños dejan de vender. Deja el potencial sin tope.
- **Comisiones en ingresos sin consideración de margen** — los reps descuentarán para cerrar. Vincula comisión a margen o establece umbrales de aprobación de descuento.
- **Sin disposición de clawback** — sin clawbacks, los reps no tienen incentivo para asegurar calidad de trato
- **Cambiar el plan a mitad de período** — destruye confianza. Solo cambia planes en límites de período con notificación anticipada.
- **Estructuras excesivamente complejas** — si un rep no puede calcular su propia comisión en una servilleta, el plan es demasiado complejo.

---

## Recuperación

- **No puede permitirse salario base (fundador individual):** Usa solo comisión con tasas más altas (15-25%). Atrae con potencial de ingresos sin tope y leads proporcionados.
- **Reps jugando con el sistema:** Identifica qué comportamiento se está incentivando que no pretendías. Ajusta la estructura para alinear incentivos.
- **Alto churn en tratos comisionados:** Implementa o extiende ventanas de clawback. Agrega una bonificación de calidad para tratos que se retienen más allá de 6 meses.
- **Transición de un plan a otro:** Honra todos los tratos en el pipeline bajo el plan anterior. Nuevo plan se aplica a nuevas oportunidades solamente.
