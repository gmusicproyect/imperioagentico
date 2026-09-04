---
name: calculadora-precios
description: "Construye modelos de precios, tablas de comparación, y calculadoras de tarifa para servicios, productos y suscripciones con análisis de margen de ganancia y posicionamiento competitivo. Usa cuando necesites establecer precios para tus ofertas."
allowed-tools: Read Write Glob
metadata:
  author: Imperio Digital
  version: "1.0"
---

# Calculadora de Precios

## Cuándo Usar Este Skill

Usa este skill cuando:
- Necesites establecer precios para un servicio, producto o suscripción
- Un freelancer quiera calcular su tarifa horaria, proyecto o retainer
- Estés construyendo paquetes de precios en tiers (Bueno / Mejor / Mejor)
- Necesites análisis de margen de ganancia en precios actuales o planificados
- Un fundador SaaS necesite estructurar tiers de suscripción con matrices de características
- Un usuario dice "cuánto debo cobrar" o "ayúdame a precio esto"

**NO** uses este skill para:
- Escribir propuestas o facturas (usa skills de propuesta o factura)
- Pronóstico financiero o modelado P&L (esto calcula precios, no planes comerciales)
- Consejo de inversión o fiscal (consulta un profesional financiero)

---

## Principio Fundamental

CADA CÁLCULO DE PRECIOS COMIENZA CON LOS COSTOS DEL USUARIO Y OBJETIVOS DE INGRESOS -- NUNCA ESTABLECES UN PRECIO SIN ENTENDER QUÉ NECESITA CUBRIR.

---

## Workflow Básico

### Paso 1: Recopila Información

**Para freelancers/servicios:** (1) ¿Qué ofereces? (2) ¿Costos fijos mensuales? (3) ¿Objetivo de ingresos anuales? (4) ¿Horas por semana disponibles? (5) ¿Ratio facturable? (Default: 60% solo, 70% con sistemas) (6) ¿Rango de precios competidor? (7) ¿Cliente objetivo?

**Para productos/SaaS:** (1) ¿Cuál es el producto? (2) ¿Costo por unidad/usuario? (3) ¿Costos fijos mensuales? (4) ¿Objetivo de MRR o ingresos anuales? (5) ¿Precios competidores? (6) ¿CAC? (7) ¿Cliente objetivo?

Si el usuario proporciona artículos 1-3, procede con defaults para el resto y sígnala.

### Paso 2: Calcula

Ejecuta el modelo apropiado. **Muestra toda la matemática de forma transparente** para que el usuario pueda verificar y recalcular.

**Freelance por hora:** Ingresos anuales + gastos + reserva fiscal (30%) + buffer de ganancia (10%) = ingresos totales necesarios. Divide entre (horas/semana x ratio facturable x 48 semanas de trabajo) = tasa horaria mínima.

**Basado en proyecto:** Horas estimadas x tarifa horaria + buffer de complejidad (15-25%) = tarifa de proyecto.

**Paquetes en tiers:** Tier base a 1x, medio a 2x, superior a 3-3.5x. Aplica precios charm a al menos el tier objetivo.

**Suscripción:** Calcula precio mínimo de objetivo de margen (costo / (1 - margen%)). Calcula CAC payback (CAC / precio = meses). Calcula LTV (precio / tasa churn mensual). Verifica relación LTV:CAC es al menos 3:1. Establece descuento anual a 2 meses gratis (16.7% descuento).

**PUNTO DE CONTROL: Presenta todos los cálculos al usuario antes de construir el documento de precios.** Pregunta: "¿Esta matemática coincide con tus expectativas? ¿Hay costos que deba ajustar?"

### Paso 3: Presenta el Documento de Precios

Construye un documento con: (1) Resumen de Precios con nombres de tier y precios, (2) Qué Se Incluye (tabla de comparación), (3) Análisis de Margen de Ganancia, (4) Posicionamiento Competitivo (budget / mid-market / premium), (5) Psicología Aplicada, (6) Fórmulas para Recálculo.

**Siempre marca un tier como "MÁS POPULAR" o "Recomendado."** Default al tier medio.

**PUNTO DE CONTROL: Presenta el documento de precios completo para revisión antes de guardar.**

### Paso 4: Entrega

1. Guarda como `pricing-[nombre-oferta].md` en el directorio de trabajo (o ruta especificada por usuario)
2. Confirma: "Tu modelo de precios ha sido guardado a [ruta]. Incluye [X] tiers, margen promedio [X]%, y fórmulas de recálculo."
3. Ofrece: "¿Te gustaría una página de precios que enfrente al cliente o una propuesta usando estas tarifas?"

---

## Framework de Tier de Precios

| Tier | Multiplicador | Propósito | Psicología |
|------|-----------|---------|----------|
| **Iniciador / Básico** | 1x | Barrera baja, atrae compradores sensibles al precio | Hace tier medio verse como mejor oferta |
| **Profesional / Crecimiento** | 2x | El tier que quieres que la mayoría de clientes elija | Etiquetado "MÁS POPULAR" -- empujón de social proof |
| **Premium / Escala** | 3-3.5x | Captura clientes con alta disposición a pagar | Ancla tier medio como razonable |

**CRÍTICO: El tier Profesional debe ser el valor obvio.** La brecha Iniciador-Profesional debe sentirse pequeña. La brecha Profesional-Premium debe sentirse grande. Este es el efecto señuelo.

---

## Anti-Patrones

- **NO establezas precios basados solamente en precios competidores.** Comienza con tus propios costos e objetivos de ingresos. Los competidores son referencia, no fórmula.
- **NO crees más de 4 tiers de precios.** Tres es ideal. Más causa parálisis de decisión.
- **NO ocultes el tier recomendado.** Siempre etiqueta un tier "MÁS POPULAR." Sin un empujón, los clientes default al más barato.
- **NO precies por debajo del costo sin una estrategia documentada.** Precios de líder de pérdida requieren ruta de upsell clara y límite de tiempo.
- **NO uses números redondos para todo.** Precios charm ($4,997 vs $5,000) aumentan conversiones. Excepción: marcas ultra-premium.
- **NO presentes precios sin mostrar qué se incluye.** Precios sin contexto desencadenan shock de pegatina.
- **NO confundas markup con margen.** 50% markup en $100 = $150. 50% margen en $100 = $200. Clarifica cuál significa el usuario.
- **NO omitas el buffer de ganancia.** Siempre incluye 10-15% encima de objetivos de ingresos.
- **NO ignores posición de mercado.** Freelancers nuevos no pueden cobrar tarifas de agencia sin portafolio. Veteranos no deben estar muy baratos.
- **NO establezas precios de suscripción sin análisis LTV y CAC.** $10/mes suena bien hasta que CAC es $200 y churn es 10%.

---

## Recuperación

### El Usuario No Conoce Sus Costos
1. Camina a través de rangos típicos de freelancer ($350-$2,300/mes: software $100-$500, seguros $100-$300, marketing $0-$500, educación $50-$200, equipo $100-$300, espacio de trabajo $0-$500)
2. Usa punto medio ($1,325/mes) como default, sígnala claramente
3. Incluye fórmula para que recalcule con números reales después

### El Usuario Está Severamente Subpreciando
1. Muestra la matemática: "A $50/hora con tus gastos, neto $18/hora después de impuestos -- bajo salario mínimo"
2. Muestra cuál debería ser la tasa basada en sus objetivos
3. Sugiere un plan de transición: nuevos clientes con nuevas tarifas inmediatamente, aviso de 30 días a clientes existentes, tasa completa dentro de 3-5 meses
4. **Sígnala claramente pero respeta la decisión final del usuario**

### Datos de Competidor No Disponibles
1. Usa benchmarks de industria: diseño $75-$250/hr, dev $100-$300/hr, marketing $100-$350/hr, coaching $150-$500/hr, writing $50-$200/hr, SaaS B2B $15-$500/mo, SaaS B2C $5-$50/mo
2. Sígnala como rangos amplios de industria, recomienda encuestar 3-5 pares
3. Procede con punto medio de rango relevante

### Múltiples Servicios para Precio
1. Precio cada servicio independientemente usando la misma tasa base
2. Construye paquetes de bundle a 10-20% descuento de precios individuales
3. Mantén máximo 3 tiers por servicio -- nunca 3 servicios x 3 tiers = 9 opciones

### El Usuario Rechaza Precios Después de 3 Intentos
1. Diagnostica: "¿Es el total muy alto, o el valor no está claro suficientemente?"
2. Si muy alto: reduce alcance, no margen. Remueve deliverable de valor más bajo.
3. Si valor poco claro: reencuadra con lenguaje de precio-a-valor
4. Si desacuerdo persiste: entrega con advertencia de margen y sugiere revisitar después del primer trimestre

### Escritura de Archivo Falla
1. Reporta error, presenta documento de precios como texto formateado en chat
2. Ofrece ruta de archivo diferente. **Si 3 intentos fallan, para y presenta en chat.**

---

## Lista de Verificación Pre-Entrega

**NO OMITAS NINGÚN ARTÍCULO.**

| Verificación | Qué Verificar |
|-------|----------------|
| Matemática correcta | Cada fórmula produce el resultado indicado; márgenes coinciden; totales se suman |
| Costos contabilizados | Costos fijos, costos variables, impuestos, y buffer de ganancia todos incluidos |
| Objetivo de ingresos alcanzable | Precios generan suficientes ingresos para alcanzar objetivo indicado |
| Tiers lógicos | Cada tier agrega valor claro; sin confusión de superposición |
| Tier Recomendado Marcado | Un tier etiquetado "MÁS POPULAR" o "Recomendado" |
| Psicología Aplicada | Al menos una táctica usada y documentada |
| Posición Competitiva Indicada | Usuario sabe si budget, mid-market, o premium |
| Fórmulas Incluidas | Usuario puede recalcular cuando cambien costos |
| Sin Texto Placeholder | Cada número es real; sin `[TBD]` queda |
| Margen Arriba de 30% | Si bajo, sígnala explícitamente con recomendación |
| Archivo Guardado | Herramienta de escritura confirmó exitoso |
| Próximos Pasos Ofrecidos | Usuario sabe qué hacer después (página de ventas, propuesta, etc.) |
