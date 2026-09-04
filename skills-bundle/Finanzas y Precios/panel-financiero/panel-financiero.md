---
name: panel-financiero
description: "Crea una estructura de panel de seguimiento de KPI financieros con ingresos, gastos, márgenes, pista de despegue y análisis de tendencias. Usa esta habilidad cuando el dueño del negocio quiera una vista única de su salud financiera, necesite configurar seguimiento de KPI o quiera monitorear métricas financieras consistentemente."
allowed-tools: Read Write Bash(ls)
---

# Panel Financiero

## Cuándo usar esta habilidad

- El usuario quiere un panel financiero de vista única para su negocio
- El usuario necesita rastrear ingresos, gastos y márgenes en el tiempo
- El usuario quiere configurar seguimiento de KPI para salud financiera
- El usuario está creciendo y necesita visibilidad en tasa de quemado o pista de despegue
- El usuario quiere comparar desempeño financiero entre meses o trimestres

## Principio Central

UN PANEL QUE RASTREA TODO RASTREA NADA — LIMITA A 8-12 KPIS QUE DIRECTAMENTE RESPONDEN "¿ESTOY GANANDO DINERO Y SEGUIRÉ GANANDO DINERO?"

## Descargo de Responsabilidad Financiero

**IMPORTANTE: Este panel es solo para propósitos de seguimiento y planificación interna. No constituye reportes financieros auditados. Siempre consulta a un contador calificado para estados financieros oficiales, presentaciones fiscales y cumplimiento. La precisión depende de los datos ingresados por el usuario.**

## Workflow

### Fase 1: Define el Modelo de Negocio

1. Confirma el tipo de negocio para seleccionar KPIs relevantes:
   - **Negocio de servicios** (freelancer, consultor, agencia): Enfócate en ingresos por cliente, tasa de utilización, margen de proyecto
   - **E-commerce**: Enfócate en AOV, COGS, margen bruto, costo de adquisición de cliente
   - **Productos digitales/SaaS**: Enfócate en MRR, churn, LTV, CAC
   - **Híbrido**: Combina métricas relevantes de arriba
2. Determina frecuencia de seguimiento: mensual (predeterminado) o semanal
3. Identifica fuentes de datos (cuenta bancaria, Stripe, PayPal, QuickBooks, hoja de cálculo)

### Fase 2: Selecciona KPIs

4. Elige 8-12 KPIs de la lista maestra abajo. Las selecciones predeterminadas están marcadas.

**KPIs de Ingresos:**

| KPI | Fórmula | Predeterminado Para |
|-----|---------|---------------------|
| Ingresos Totales | Suma de todos los ingresos | Todos los negocios |
| Ingresos Recurrentes Mensuales (MRR) | Suscripciones/retenciones recurrentes | SaaS, membresías |
| Ingresos por Fuente | Ingresos desglosados por canal/producto | Todos los negocios |
| Valor Promedio de Pedido (AOV) | Ingresos / Número de pedidos | E-commerce |
| Ingresos por Cliente | Ingresos / Clientes activos | Negocios de servicios |

**KPIs de Rentabilidad:**

| KPI | Fórmula | Predeterminado Para |
|-----|---------|---------------------|
| Ganancia Bruta | Ingresos - COGS | Todos los negocios |
| Margen Bruto % | (Ganancia Bruta / Ingresos) x 100 | Todos los negocios |
| Ganancia Neta | Ingresos - Todos los Gastos | Todos los negocios |
| Margen Neto % | (Ganancia Neta / Ingresos) x 100 | Todos los negocios |
| Razón de Gastos Operativos | Gastos Operativos / Ingresos | Todos los negocios |

**KPIs de Crecimiento y Salud:**

| KPI | Fórmula | Predeterminado Para |
|-----|---------|---------------------|
| Crecimiento Mes a Mes | (Este Mes - Mes Pasado) / Mes Pasado x 100 | Todos los negocios |
| Pista de Despegue de Caja | Caja en Mano / Tasa Mensual de Quemado | Startups, negocios nuevos |
| Costo de Adquisición de Cliente (CAC) | Gasto de Marketing / Nuevos Clientes | E-commerce, SaaS |
| Valor de Vida del Cliente (LTV) | Ingresos Promedio por Cliente x Retención Promedio (meses) | SaaS, membresías |
| Envejecimiento de Cuentas por Cobrar | Facturas pendientes por días vencidos | Negocios de servicios |

### Fase 3: Construye la Estructura del Panel

5. Crea el diseño del panel con estas secciones:

```
╔══════════════════════════════════════════════════════════╗
║              PANEL FINANCIERO — [MES AÑO]              ║
║              [Nombre del Negocio]                       ║
╠══════════════════════════════════════════════════════════╣
║                                                         ║
║  PANORAMA (Números de línea superior)                   ║
║  ┌──────────┐ ┌──────────┐ ┌──────────┐ ┌──────────┐  ║
║  │ Ingresos │ │ Gastos   │ │Ganancia  │ │Margen    │  ║
║  │          │ │          │ │ Neta     │ │ Neto     │  ║
║  │ $XX,XXX  │ │ $XX,XXX  │ │ $X,XXX  │ │  XX.X%   │  ║
║  │ ▲ +12%   │ │ ▲ +5%    │ │ ▲ +22%  │ │ ▲ +3.1pp │  ║
║  └──────────┘ └──────────┘ └──────────┘ └──────────┘  ║
║                                                         ║
║  DESGLOSE DE INGRESOS                                  ║
║  [Ingresos por fuente — gráfico de barras o tabla]     ║
║                                                         ║
║  DESGLOSE DE GASTOS                                    ║
║  [Top 5 categorías de gastos — gráfico de barras]      ║
║                                                         ║
║  TENDENCIA (Últimos 6 meses)                           ║
║  [Ingresos, Gastos, Ganancia Neta en el tiempo]        ║
║                                                         ║
║  INDICADORES DE SALUD                                  ║
║  [CAC, LTV, Pista de Despegue, Envejecimiento AR]      ║
║                                                         ║
╚══════════════════════════════════════════════════════════╝
```

6. Para cada KPI, define:
   - Umbrales verde/amarillo/rojo (qué es saludable, advertencia, crítico)
   - Fuente de datos (dónde viene el número)
   - Frecuencia de actualización

### Fase 4: Poblado con Datos

7. Si el usuario proporciona datos financieros, puebla el panel con números reales
8. Calcula todas las métricas derivadas (márgenes, ratios, tasas de crecimiento)
9. Marca cualquier KPI en zona roja con comentario específico

### Fase 5: Entrega

10. Saca la estructura completa del panel
11. Saca una plantilla de recopilación de datos (qué rastrear y dónde ingresar)
12. Proporciona definiciones de umbrales para que el usuario sepa qué significa verde/amarillo/rojo

## Ejemplo 1: Panel de Redactor Freelance

**Contexto:** Redactor independiente ganando $6,000-$9,000/mes de clientes con retención y proyectos únicos. Quiere rastrear si el negocio es saludable.

**KPIs Seleccionados (8):** Ingresos Totales, Ingresos por Cliente, Margen Bruto, Ganancia Neta, Margen Neto, Crecimiento MM, Razón de Gasto Operativo, Cuentas por Cobrar

```
╔══════════════════════════════════════════════════════════╗
║         PANEL FINANCIERO — ENERO 2026                  ║
║         Cole Bradley Redacción                         ║
╠══════════════════════════════════════════════════════════╣
║                                                         ║
║  PANORAMA                                               ║
║  ┌──────────┐ ┌──────────┐ ┌──────────┐ ┌──────────┐  ║
║  │ Ingresos │ │ Gastos   │ │Ganancia  │ │Margen    │  ║
║  │          │ │          │ │ Neta     │ │ Neto     │  ║
║  │ $8,200   │ │ $1,340   │ │ $6,860  │ │  83.7%   │  ║
║  │ ▲ +8.6%  │ │ ▼ -2.1%  │ │ ▲ +11.4%│ │ ▲ +2.1pp │  ║
║  │ 🟢 BUENO │ │ 🟢 BUENO │ │ 🟢 BUENO│ │ 🟢 BUENO │  ║
║  └──────────┘ └──────────┘ └──────────┘ └──────────┘  ║
║                                                         ║
║  DESGLOSE DE INGRESOS                                  ║
║  Clientes con Retención (3)        $6,000    73.2%     ║
║    - Greenline Marketing           $2,500              ║
║    - FreshPress Juicery            $2,000              ║
║    - Oakmont Financial             $1,500              ║
║  Proyectos Únicos (2)              $2,200    26.8%     ║
║    - Copia web (Bloom Yoga)        $1,400              ║
║    - Secuencia de email (autor)      $800              ║
║                                                         ║
║  Ingresos por Cliente: $1,640                          ║
║                                                         ║
║  DESGLOSE DE GASTOS                                    ║
║  Software & Herramientas  $144    10.7%                ║
║    Jasper AI $49, Grammarly $30, ConvertKit $29,       ║
║    Google Workspace $12, Notion $8, Zoom $16           ║
║  Marketing                $450    33.6%                ║
║    LinkedIn ads $300, hosting del portafolio $50,      ║
║    evento de networking $100                            ║
║  Contratista              $400    29.9%                ║
║    VA (16 hrs x $25)                                   ║
║  Servicios Profesionales  $150    11.2%                ║
║    Contador                                            ║
║  Oficina & Operaciones    $145    10.8%                ║
║    Co-working $120, suministros $25                    ║
║  Educación                 $51     3.8%                ║
║    Suscripción a newsletter                            ║
║                                                         ║
║  TENDENCIA (Últimos 6 meses)                           ║
║  Ago   $5,800  ████████████                            ║
║  Sep   $6,400  █████████████                           ║
║  Oct   $7,100  ██████████████                          ║
║  Nov   $7,550  ███████████████                         ║
║  Dic   $7,550  ███████████████                         ║
║  Ene   $8,200  ████████████████                        ║
║  Crecimiento MM: +8.6% (promedio 6-mo: +7.2%)         ║
║                                                         ║
║  INDICADORES DE SALUD                                  ║
║  Razón de Gasto Operativo: 16.3% 🟢 (objetivo: <30%)  ║
║  Cuentas por Cobrar: $1,400 🟡                         ║
║    - Bloom Yoga: $1,400 pendiente (22 días)            ║
║    - Todas las retenciones: pagadas al día             ║
║                                                         ║
╚══════════════════════════════════════════════════════════╝
```

**Definiciones de Umbral:**

| KPI | Verde | Amarillo | Rojo |
|-----|-------|----------|------|
| Margen Neto | >60% | 40-60% | <40% |
| Crecimiento MM | >5% | 0-5% | Negativo |
| Razón OpEx | <30% | 30-50% | >50% |
| Envejecimiento AR | <30 días | 30-60 días | >60 días |

**Elemento de acción:** Haz seguimiento con Bloom Yoga en la factura de $1,400 pendiente — aproximándose al umbral de 30 días.

## Ejemplo 2: Panel de Marca de E-Commerce de Cuidado de la Piel

**Contexto:** Pequeña marca de cuidado de la piel vendiendo a través de Shopify, $15K-$22K/mes de ingresos, 3 líneas de productos.

**KPIs Seleccionados (10):** Ingresos Totales, AOV, Ganancia Bruta, Margen Bruto, Ganancia Neta, Margen Neto, Crecimiento MM, CAC, Ingresos por Línea de Producto, Pista de Caja

```
╔══════════════════════════════════════════════════════════╗
║         PANEL FINANCIERO — ENERO 2026                  ║
║         GlowRoot Botanicals                            ║
╠══════════════════════════════════════════════════════════╣
║                                                         ║
║  PANORAMA                                               ║
║  ┌──────────┐ ┌──────────┐ ┌──────────┐ ┌──────────┐  ║
║  │ Ingresos │ │Margen    │ │Ganancia  │ │   AOV    │  ║
║  │          │ │ Bruto    │ │ Neta     │ │          │  ║
║  │ $19,400  │ │  68.2%   │ │ $7,180  │ │  $54.20  │  ║
║  │ ▲ +6.0%  │ │ ▼ -1.3pp │ │ ▲ +4.2% │ │ ▲ +$2.40 │  ║
║  │ 🟢 BUENO │ │ 🟢 BUENO │ │ 🟢 BUENO│ │ 🟢 BUENO │  ║
║  └──────────┘ └──────────┘ └──────────┘ └──────────┘  ║
║                                                         ║
║  INGRESOS POR LÍNEA DE PRODUCTO                        ║
║  Sueros                  $9,800     50.5%   ▲ +12%    ║
║  Limpiadores             $5,600     28.9%   ▼ -3%     ║
║  Hidratantes             $4,000     20.6%   ▲ +8%     ║
║                                                         ║
║  RESUMEN DE GASTOS                                     ║
║  COGS                    $6,168     31.8%              ║
║  Marketing               $3,200     16.5%              ║
║  Cumplimiento            $1,450      7.5%              ║
║  Software                  $372      1.9%              ║
║  Contratistas              $600      3.1%              ║
║  Otra Opex                 $430      2.2%              ║
║  Gastos Totales        $12,220     63.0%               ║
║                                                         ║
║  MÉTRICAS DE CRECIMIENTO                               ║
║  Nuevos Clientes: 142    CAC: $22.54                   ║
║  Clientes Repetidores: 86  Tasa de Repetición: 37.7%  ║
║  Tendencia CAC: $22.54 🟢 (objetivo: <$30)            ║
║                                                         ║
║  TENDENCIA (Últimos 6 meses)                           ║
║  Ago   $14,200  ████████████                           ║
║  Sep   $15,800  █████████████                          ║
║  Oct   $17,600  ██████████████                         ║
║  Nov   $21,300  █████████████████                      ║
║  Dic   $18,300  ███████████████                        ║
║  Ene   $19,400  ████████████████                       ║
║                                                         ║
║  POSICIÓN DE CAJA                                      ║
║  Caja en mano: $28,500                                 ║
║  Quemado mensual: $12,220                              ║
║  Pista de Despegue: 2.3 meses (sin ingresos) 🟡        ║
║  Nota: Pista es conservadora — asume sin ingresos      ║
║                                                         ║
╚══════════════════════════════════════════════════════════╝
```

**Definiciones de Umbral para E-Commerce:**

| KPI | Verde | Amarillo | Rojo |
|-----|-------|----------|------|
| Margen Bruto | >50% | 30-50% | <30% |
| Margen Neto | >20% | 10-20% | <10% |
| CAC | <$30 | $30-$50 | >$50 |
| Pista de Caja | >3 meses | 1-3 meses | <1 mes |
| AOV | >$45 | $30-$45 | <$30 |

**Plantilla de Recopilación de Datos:**

Rastrea estos números semanalmente, compila mensualmente:
1. **Ingresos**: Exporta desde Shopify Admin > Analytics > Sales by product
2. **COGS**: Rastrea costos por unidad en una hoja de cálculo, multiplica por unidades vendidas
3. **Gasto de marketing**: Suma de dashboards de plataformas de anuncios (Meta, Google) + cualquier otro costo de promoción
4. **Clientes nuevos vs. repetidores**: Shopify Admin > Customers > filtra por "First order this month"
5. **Caja en mano**: Saldo de cuenta corriente comercial del último día del mes

## Recuperación y Respuesta Alternativa

- Si el usuario no tiene datos históricos, configura la estructura del panel con campos vacíos y ayúdalo a comenzar a rastrear desde el mes actual
- Si el usuario usa múltiples procesadores de pagos, ayúdalo a consolidar listando todas las fuentes y sugiriendo un proceso de reconciliación mensual
- Si un KPI está en zona roja, proporciona una acción específica para abordarlo (no una lista de 10 opciones)
- Si el usuario encuentra el panel completo abrumador, comienza con solo el panorama de 4 métricas (Ingresos, Gastos, Ganancia Neta, Margen Neto) y añade KPIs con el tiempo

## Restricciones

- **Siempre incluye el descargo de responsabilidad financiero**
- Limita a 12 KPIs máximo — más que eso reduce usabilidad
- No incluyas métricas de vanidad (seguidores sociales, visitas web) en un panel financiero
- No calcules ni estimes responsabilidad fiscal
- El cálculo de pista de caja asume ingresos cero como peor caso — siempre nota esto
- Los umbrales son pautas, no reglas — varían por industria y etapa de negocio
- No recomiendes software específico de contabilidad a menos que el usuario lo solicite
- Todos los datos financieros deben venir del usuario — no estimes ni fabriques números
