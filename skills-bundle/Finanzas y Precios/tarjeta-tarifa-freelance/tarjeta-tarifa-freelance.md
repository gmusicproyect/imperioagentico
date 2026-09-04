---
name: tarjeta-tarifa-freelance
description: "Calcula tarifas freelance basadas en gastos, ingresos deseados y posicionamiento de mercado con formato de tarjeta de tarifa. Úsalo cuando estableces o actualizas tu precios freelance."
allowed-tools: Read Write Glob
metadata:
  author: Imperio Digital
  version: "1.0"
---

# Tarjeta de Tarifa Freelance

## Cuándo usar esta habilidad

Usa esta habilidad cuando necesites:
- Calcular tarifas por hora, proyecto o retención basadas en tus objetivos de ingresos
- Crear una tarjeta de tarifa profesional para uso frente al cliente
- Evaluar si tus tarifas actuales soportan tus objetivos financieros
- Diseñar una estructura de precios con paquetes y niveles

**NO** uses esta habilidad para negociación de salario de empleado, precios de agencia o estrategia de precios de producto. Esto es específicamente para freelancers e consultores independientes.

---

## Principio Central

TU TARIFA NO ES TU SALARIO POR HORA — DEBE CUBRIR IMPUESTOS, BENEFICIOS, GASTOS GENERALES, TIEMPO NO FACTURABLE Y MARGEN DE GANANCIA ADEMÁS DE TU PAY DESEADO PARA LLEVAR A CASA.

---

## Fase 1: Entradas Financieras

### Entradas Requeridas

| Entrada | Qué Preguntar | Predeterminado |
|---------|--------------|----------------|
| **Ingresos anuales deseados** | "¿Qué quieres llevar a casa después de impuestos y gastos?" | Sin predeterminado — debe proporcionarse |
| **Gastos de negocio anuales** | "¿Cuáles son tus costos de negocio anuales? (software, seguros, equipo)" | $5,000 |
| **Tasa fiscal** | "¿Cuál es tu tasa fiscal estimada? (federal + estado + auto-empleo)" | 30% |
| **Costo de beneficios** | "¿Costo anual de seguro de salud, contribuciones de retiro?" | $8,000 |
| **Horas facturable por semana** | "¿Cuántas horas por semana puedes facturar a clientes? (no horas totales)" | 25 horas |
| **Semanas trabajadas por año** | "¿Cuántas semanas trabajas después de vacaciones y días feriados?" | 46 semanas |
| **Tipo de servicio** | "¿Qué haces? (diseño, redacción, desarrollo, consultoría, marketing)" | Sin predeterminado — debe proporcionarse |

**PUNTO DE CONTROL: No continúes sin ingresos deseados y tipo de servicio.**

---

## Fase 2: Cálculo de Tarifa

### Fórmula de Tarifa por Hora

```
## Cálculo de Tarifa

### Paso 1: Necesidad Anual Verdadera
| Componente | Monto |
|-----------|-------|
| Pay deseado para llevar a casa | $[X] |
| + Reserva de impuestos (30%) | $[X] |
| + Gastos de negocio | $[X] |
| + Beneficios (salud, retiro) | $[X] |
| + Margen de ganancia (10-15%) | $[X] |
| **= Ingresos anuales totales necesarios** | **$[X]** |

### Paso 2: Horas Facturable Disponibles
| Componente | Valor |
|-----------|-------|
| Horas facturable/semana | [X] |
| x Semanas trabajadas/año | [X] |
| **= Horas anuales facturable** | **[X]** |

### Paso 3: Tarifa Hora Mínima
| | |
|--|--|
| Ingresos totales necesarios | $[X] |
| / Horas facturable | [X] |
| **= Tarifa hora mínima** | **$[X]/hr** |
| Tarifa ajustada al mercado | **$[X]/hr** |
```

### Tipos de Tarifa

```
### Tus Opciones de Tarifa

| Tipo de Tarifa | Monto | Cuándo Usar |
|----------|--------|-----------|
| Tarifa hora | $[X]/hr | Tareas pequeñas, llamadas de consultoría, trabajo excedente |
| Tarifa medio día (4 hrs) | $[X] | Workshops, sesiones intensivas |
| Tarifa día completo (8 hrs) | $[X] | Trabajo en sitio, compromiso de día completo |
| Tarifa proyecto | $[X]-$[X] | Entregables de alcance definido |
| Retención mensual | $[X]/mes | Relaciones continuas con clientes |

### Fórmula de Tarifa de Proyecto
Tarifa proyecto = (Horas estimadas x Tarifa hora) x 1.2 buffer de complejidad
```

---

## Fase 3: Diseño de Tarjeta de Tarifa

### Tarjeta de Tarifa Profesional

```
## [Tu Nombre] — Tarjeta de Tarifa [Año]

### Servicios & Precios

**[Categoría de Servicio 1]**
| Servicio | A partir de | Incluye |
|---------|-----------|----------|
| [Servicio A] | $[X] | [Entregables, cronograma] |
| [Servicio B] | $[X] | [Entregables, cronograma] |

**[Categoría de Servicio 2]**
| Servicio | A partir de | Incluye |
|---------|-----------|----------|
| [Servicio C] | $[X] | [Entregables, cronograma] |

### Paquetes de Retención
| Paquete | Horas/Mes | Tarifa | Inversión Mensual |
|---------|------------|------|-------------------|
| [Inicio] | [X] hrs | $[X]/hr | $[X]/mes |
| [Crecimiento] | [X] hrs | $[X]/hr | $[X]/mes |
| [Socio] | [X] hrs | $[X]/hr | $[X]/mes |

Los clientes de retención reciben [programación prioritaria, horas transferibles, tarifa reducida].

### Detalles Adicionales
- **Tarifa de urgencia:** +[25-50]% para entrega en menos de [X] días
- **Revisiones:** [X] rondas incluidas; adicionales a $[X]/hr
- **Términos de pago:** [50% adelantado, 50% a la entrega / Neto 15]
- **Disponibilidad:** Reserva [X] semanas por adelantado
```

---

## Fase 4: Validación de Mercado

### Comparación de Tarifas de Mercado

```
## Posicionamiento de Mercado

| Nivel | Rango de Mercado | Tu Posición |
|-------|-------------|--------------|
| Entrada | $[X]-$[X]/hr | |
| Mid-level | $[X]-$[X]/hr | |
| Senior/Experto | $[X]-$[X]/hr | |
| Premium/Especialista | $[X]+/hr | |

**Tu tarifa:** $[X]/hr — posicionado en [nivel]

### Notas de Posicionamiento
- Si está por debajo del mercado: oportunidad para aumentar tarifas
- Si está en el mercado: diferénciate en calidad, velocidad o especialización
- Si está por encima del mercado: asegúrate que marca y portafolio justifiquen el premium
```

---

## Ejemplo: Desarrollador Web Freelance (Objetivo de $100K)

**Cálculo:** $100K de ingresos + $30K impuestos + $8K beneficios + $5K gastos + $14.3K margen de ganancia = $157,300 necesarios. Con 25 hrs facturable/semana x 46 semanas = 1,150 horas anuales facturable. Tarifa mínima: $137/hr.

**Tarjeta de tarifa:** Hora $150/hr, medio día $550, día completo $1,000, proyecto de sitio web $3,000-8,000, retención mensual $2,400/mes (20 hrs a $120/hr descuento de retención).

---

## Anti-patrones

- **Usar tu salario empleado para establecer tarifas freelance** — los empleados reciben beneficios, PTO y equipo. Los freelancers pagan por todo. Las tarifas freelance deben ser 2-3x el equivalente por hora de un salario.
- **Facturar cada hora trabajada** — administración, marketing, facturación y aprendizaje no son facturables. Trabajas 40 horas pero facturas 25.
- **Correr hacia el fondo** — competir en precio atrae clientes sensibles al precio que son los más difíciles de servir. Compite en valor.
- **Sin tarifa de urgencia** — el trabajo urgente desplaza trabajo planeado. Cobra un premium por él.
- **Solo precios por hora** — los precios de proyecto y retención capturan más valor y proporcionan predictibilidad de ingresos.

---

## Recuperación

- **Tarifa está por debajo del mínimo viable:** Muestra las matemáticas. O aumenta tarifas, reduce gastos, o aumenta horas facturables. Los números no mienten.
- **Miedo de aumentar tarifas:** Aumenta tarifas para clientes nuevos primero. Los clientes existentes reciben 60-90 días de notificación. La mayoría se queda — los que se van no te valoraban.
- **Sin idea de cuáles son las tarifas de mercado:** Investiga en plataformas freelance, encuestas de industria y conversaciones con colegas. Comienza en mid-market y ajusta basado en demanda.
- **Los clientes objetan las tarifas:** El valor es el problema, no el precio. Mejora tu portafolio, agrega testimonios, o reformula precios en términos de ROI para el cliente.
