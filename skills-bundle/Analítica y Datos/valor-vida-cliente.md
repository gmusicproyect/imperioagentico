---
name: "LTV (Valor Vida Cliente)"
description: "Calcula el LTV (valor de vida del cliente) con segmentación, modelos de predicción y recomendaciones de inversión en retención. Utiliza cuando determines cuánto vale un cliente en el tiempo."
allowed-tools: Read Write Glob
metadata:
  author: Imperio Digital
  version: "1.0"
---

# Valor de Vida del Cliente

## Cuándo Usar Este Skill

Utiliza este skill cuando necesites:
- Calcular el valor de vida del cliente (CLV/LTV) para tu negocio
- Segmentar clientes por valor para priorizar esfuerzos de retención
- Determinar cuánto gastar en adquisición de clientes (relación CAC:LTV)
- Construir un modelo CLV para pronóstico y presupuesto

**NO** utilices este skill para pronóstico de ingresos a corto plazo, análisis de rentabilidad de cliente individual o auditoría financiera. Esto es para modelado CLV y toma de decisiones estratégicas.

---

## Principio Fundamental

CLV ES LA MÉTRICA ÚNICA MÁS IMPORTANTE PARA EL CRECIMIENTO SOSTENIBLE — TE DICE CUÁNTO PUEDES PERMITIRTE GASTAR PARA ADQUIRIR Y RETENER UN CLIENTE.

---

## Fase 1: Brief

### Entradas Requeridas

| Entrada | Qué Preguntar | Por Defecto |
|---------|--------------|------------|
| **Modelo de negocio** | "¿Suscripción, compra única, compra repetida o híbrido?" | Debe proporcionarse |
| **Valor promedio de pedido** | "¿Qué gasta un cliente por transacción?" | Debe proporcionarse |
| **Frecuencia de compra** | "¿Con qué frecuencia compra un cliente? (mensual, trimestral, anual)" | Debe proporcionarse |
| **Vida útil del cliente** | "¿Cuánto tiempo permanece un cliente típico? (meses o años)" | Estimado de churn |
| **Tasa de churn** | "¿Qué porcentaje de clientes se van cada mes/año?" | Estimado de datos |
| **Margen bruto** | "¿Cuál es tu porcentaje de margen bruto?" | 60-70% para digital |
| **Segmentos** | "¿Algún segmento de cliente para analizar por separado? (nivel de plan, canal, geografía)" | General primero |

**PUNTO DE CONTROL:** Confirma entradas antes de calcular.

---

## Fase 2: Calcular

### Fórmulas de CLV

**CLV Simple (buen punto de inicio):**
`CLV = Valor Promedio de Pedido x Frecuencia de Compra x Vida Útil del Cliente`

**CLV Ajustado por Margen:**
`CLV = (AOV x Frecuencia x Vida Útil) x % Margen Bruto`

**CLV de Suscripción:**
`CLV = (Ingresos Mensuales por Cliente / Tasa Churn Mensual) x % Margen Bruto`

### Relación CAC:LTV

- **Saludable:** LTV es 3x+ CAC
- **Advertencia:** LTV es 1-3x CAC (el crecimiento es costoso)
- **Peligro:** LTV está por debajo de CAC (perdiendo dinero en cada cliente)

**PUNTO DE CONTROL:** Presenta el cálculo CLV línea base y confirma precisión antes de segmentar.

---

## Fase 3: Construir

### Entregables

**1. Hoja de Trabajo de Cálculo CLV**
- Fórmula con todas las entradas claramente documentadas
- Número CLV general con ajuste de margen
- Relación CAC:LTV con interpretación
- Período de recuperación: meses para recuperar costo de adquisición

**2. Análisis CLV Segmentado**
- CLV por segmento de cliente (nivel de plan, canal de adquisición, cohort)
- Perfil de segmento de alto valor: ¿cómo se ven tus mejores clientes?
- Segmento de bajo valor: ¿hay clientes costando más de lo que generan?

**3. Análisis de Sensibilidad**
- Cómo cambia CLV si el churn mejora 5%, 10%, 20%
- Cómo cambia CLV si AOV aumenta 10%, 20%
- ¿Cuál palanca tiene el mayor impacto en CLV?

**4. Recomendaciones Estratégicas**
- Inversión en retención: cuánto gastar manteniendo clientes basado en CLV
- Presupuesto de adquisición: CAC máximo basado en relación LTV objetivo
- Oportunidades de ingresos de expansión: potencial de upsell por segmento

---

## Fase 4: Pulir

### Métricas de Dashboard CLV

Rastrea mensualmente:
- CLV promedio (general y por segmento)
- Tendencia de relación CAC:LTV
- Tendencia de tasa de churn (el mayor conductor de CLV)
- Tendencia de ingresos por cliente

### Revisión Trimestral

Recalcula CLV trimestralmente a medida que las entradas cambian. Actualiza presupuestos de adquisición y retención en consecuencia.

---

## Ejemplo 1: Suscripción SaaS ($49/mes, 5% churn mensual)

**CLV:** $49 / 0.05 = $980 bruto, $686 ajustado por margen (70% margen)
**Objetivo CAC saludable:** Bajo $229 (relación 3:1)
**Palanca clave:** Reducir churn de 5% a 4% aumenta CLV 25% a $857

## Ejemplo 2: E-commerce (AOV $75, 3 compras/año, vida útil 2.5 años)

**CLV:** $75 x 3 x 2.5 = $562 bruto, $281 ajustado por margen (50% margen)
**Objetivo CAC saludable:** Bajo $94 (relación 3:1)
**Palanca clave:** Aumentar frecuencia de 3 a 4 compras/año aumenta CLV 33%

---

## Anti-Patrones

- **Usar ingresos en lugar de margen** — CLV basado en ingresos sobrestima valor. Siempre ajusta por margen bruto.
- **Ignorar churn** — asumir que los clientes permanecen para siempre infla CLV a números sin sentido.
- **CLV de una sola talla para todos** — tus mejores clientes pueden valer 10x tus peores. Segmenta o pierde el insight.
- **Cálculo estático** — CLV cambia a medida que tu producto, precios y retención mejoran. Recalcula regularmente.
- **CLV sin contexto CAC** — CLV solo es una métrica de vanidad. La relación al costo de adquisición es lo que importa.

---

## Recuperación

- **Sin datos de churn:** Estima de tendencias de ingresos o cambios de cantidad de clientes. Incluso una estimación aproximada es mejor que ignorar churn.
- **Demasiado pronto para datos confiables:** Calcula basado en datos de 3 meses y etiquétalo "proyectado." Revisa trimestralmente a medida que se acumulan datos.
- **CLV es más bajo que CAC:** Este es un hallazgo crítico. Prioriza: reducir CAC, mejorar retención, aumentar AOV o subir precios.
- **Usuario inseguro de margen bruto:** Usa valores por defecto de industria (SaaS: 70-80%, e-commerce: 30-50%, servicios: 50-70%) y refina después.