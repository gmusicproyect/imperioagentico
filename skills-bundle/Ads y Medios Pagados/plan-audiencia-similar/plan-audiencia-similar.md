---
name: plan-audiencia-similar
description: "Diseña estrategias de audiencia similar con selección de audiencia de origen, tiers de porcentaje y framework de pruebas. Úsalo cuando planees targeting pagado en ad para encontrar clientes nuevos similares a tus mejores existentes."
allowed-tools: Read Write Glob
metadata:
  author: Imperio Digital
  version: "1.0"
---

# Plan de Audiencia Similar

## Cuándo Usar Este Skill

Usa este skill cuando necesites:
- Construir una estrategia de audiencia similar para Facebook, Google u otras plataformas de ad
- Seleccionar las mejores audiencias de origen de tus datos de clientes existentes
- Planificar tiers de porcentaje y secuencias de pruebas para expansión de audiencia similar
- Crear un plan de rollout estructurado para escalar gasto en ad con lookalikes

**NO USES** este skill para targeting basado en intereses, configuración de retargeting, o construcción de audiencia orgánica. Esto es específicamente para estrategias de audiencia similar/lookalike en plataformas pagadas.

---

## Principio Fundamental

LA CALIDAD DE UNA AUDIENCIA SIMILAR SOLO ES TAN BUENA COMO LA AUDIENCIA DE ORIGEN — COMIENZA CON TUS CLIENTES DE MAYOR VALOR, NO TU LISTA MÁS GRANDE.

---

## Fase 1: Auditoría de Origen

Antes de construir lookalikes, identifica y evalúa audiencias de origen disponibles.

### Inputs Requeridos

| Input | Qué Preguntar | Default |
|-------|---------------|---------|
| **Plataforma de ad** | "¿Qué plataforma? (Meta, Google, TikTok, LinkedIn)" | Meta (Facebook/Instagram) |
| **Datos de cliente disponibles** | "¿Qué listas de clientes o datos de pixel tienes? (listas de email, compradores, leads, visitantes de sitio)" | Sin default — debe ser proporcionado |
| **AOV / LTV promedio** | "¿Cuál es el valor de cliente promedio o lifetime value?" | Desconocido |
| **Presupuesto mensual de ad** | "¿Cuál es tu presupuesto mensual de gasto en ad?" | $2,000/mes |
| **Objetivos geográficos** | "¿Qué países o regiones diriges?" | Estados Unidos |

**PUNTO DE CONTROL: No procedas hasta que el usuario confirme sus fuentes de datos disponibles y plataforma.**

---

## Fase 2: Estrategia de Audiencia de Origen

Clasifica y recomienda audiencias de origen basándote en señales de calidad.

### Jerarquía de Audiencia de Origen (Mejor a Débil)

1. **Top 25% de clientes por LTV** — mayor valor, señal más clara
2. **Todos los compradores** — compradores probados, señal fuerte
3. **Compradores repetidos** — señal de lealtad, pool más pequeño pero potente
4. **Leads de alta intención** — reservaron llamadas, iniciaron checkout, pidieron demos
5. **Suscriptores de email (engaged)** — abrieron/clickearon en últimos 90 días
6. **Todos los suscriptores de email** — señal más débil, pool más grande
7. **Visitantes de sitio (páginas clave)** — página de precios, páginas de producto
8. **Todos los visitantes de sitio** — señal más débil, pool más grande

### Requisitos de Tamaño Mínimo de Origen

| Plataforma | Mínimo de Origen | Origen Recomendado |
|----------|-----------------|-------------------|
| Meta | 100 personas | 1,000-5,000 |
| Google | 100 personas | 1,000+ |
| TikTok | 100 personas | 1,000+ |
| LinkedIn | 300 personas | 1,000+ |

Presenta audiencias de origen recomendadas con lógica antes de proceder.

**PUNTO DE CONTROL: Confirma selecciones de audiencia de origen con el usuario.**

---

## Fase 3: Plan de Construcción de Lookalike

Diseña la estrategia lookalike por tiers con framework de pruebas.

### Estrategia de Tier de Porcentaje

```
## Tiers de Lookalike

### Tier 1: Precisión (1-2%)
- Coincidencia más cercana con audiencia de origen
- Tasa de conversión esperada más alta
- Menor alcance, CPM más alto
- Usa para: Pruebas iniciales, presupuestos limitados

### Tier 2: Balanceado (3-5%)
- Buen match con alcance más amplio
- Potencial fuerte de conversión con escala
- Usa para: Escalar después de validación de Tier 1

### Tier 3: Expansión (6-10%)
- Mayor alcance, señal más débil
- Tasa de conversión más baja pero CPM más bajo
- Usa para: Conciencia top-of-funnel, presupuestos grandes
```

---

## Anti-Patrones

- **Usar "todos los visitantes de sitio" como origen primario** — demasiado amplio, señal débil. Comienza con compradores o acciones de alta intención.
- **Pruebar todos los tiers simultáneamente** — quema presupuesto sin aprender. Prueba secuencialmente.
- **Ignorar freshness de audiencia de origen** — una lista de email de 3 años produce lookalikes peores que una lista de comprador de 90 días.
- **Saltear exclusiones** — siempre excluye clientes existentes y pools de retargeting activos.
- **Asumir un origen funciona para todo** — productos diferentes pueden necesitar diferentes audiencias de origen.

---

## Recuperación

- **Audiencia de origen muy pequeña:** Si está bajo mínimos de plataforma, combina audiencias relacionadas. Nota el tradeoff de calidad.
- **Sin datos de comprador:** Usa la señal de mayor intención disponible — suscriptores engaged o visitantes de página clave.
- **Múltiples productos/servicios:** Crea audiencias de origen separadas por línea de producto. No mezcles tipos de clientes no relacionados.
- **Sin datos de cliente existente:** Este skill requiere algunos datos. Ejecuta campañas de targeting por intereses primero para construir audiencia pixel de 500+ convertidos.
