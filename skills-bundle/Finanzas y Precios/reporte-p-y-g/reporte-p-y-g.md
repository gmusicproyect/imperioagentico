---
name: "Reporte P&L (Pérdidas y Ganancias)"
description: "Genera estados de P&L (pérdidas y ganancias) mensuales o trimestrales a partir de datos de transacciones con desglose de ingresos, categorías de gastos y análisis de márgenes. Usa esta habilidad cuando un trabajador independiente o propietario de pequeño negocio necesite entender si realmente son rentables, quiera un reporte P&G formateado o necesite revisar desempeño financiero durante un período."
allowed-tools: Read Write Bash(ls:*) Bash(python3:*)
metadata:
  author: Imperio Digital
  version: "1.0"
---

# Reporte de Pérdidas y Ganancias

## Cuándo usar esta habilidad

- El usuario quiere saber si su negocio es rentable
- El usuario necesita un estado de pérdidas y ganancias mensual o trimestral
- El usuario tiene datos de transacciones (CSV, hoja de cálculo o entradas manuales) y quiere organizarlos
- El usuario está preparándose para temporada de impuestos y necesita un resumen financiero
- El usuario quiere comparar ingresos y gastos entre períodos

## Principio Central

UN REPORTE P&G DEBE DECIR LA VERDAD — CATEGORIZA CADA DÓLAR, NO OCULTES NADA Y MUESTRA EL MARGEN REAL.

## Descargo de Responsabilidad Financiero

**IMPORTANTE: Los reportes financieros generados por esta habilidad son solo para propósitos informativos y de planificación. No constituyen asesoramiento contable ni estados financieros auditados. Siempre consulta con un contador calificado o CPA para reportes financieros oficiales, presentaciones fiscales y cumplimiento. La precisión depende completamente de los datos proporcionados por el usuario.**

## Workflow

### Fase 1: Recopila Datos Financieros

1. Determina el período de reporte (mes o trimestre)
2. Recopila datos de ingresos — pide al usuario uno de estos:
   - Archivo CSV o hoja de cálculo con transacciones
   - Lista manual de fuentes de ingresos y montos
   - Resumen de banco/procesador de pagos (Stripe, PayPal, Square)
3. Recopila datos de gastos — mismos formatos que arriba
4. Confirma el tipo de negocio (servicio, e-commerce, productos digitales, híbrido) para establecer categorías apropiadas

### Fase 2: Categoriza Transacciones

5. Ordena todos los ingresos en estas categorías estándar:

| Categoría de Ingresos | Ejemplos |
|----------------------|----------|
| Ventas de Productos | Bienes físicos, descargas digitales |
| Ingresos por Servicios | Consultoría, trabajo freelance, coaching |
| Ingresos Recurrentes | Suscripciones, membresías, retenciones |
| Afiliado/Comisión | Honorarios por referencia, pagos de afiliados |
| Otros Ingresos | Intereses, reembolsos recibidos, misc |

6. Ordena todos los gastos en estas categorías estándar:

| Categoría de Gastos | Ejemplos |
|---------------------|----------|
| Costo de Bienes Vendidos (COGS) | Materiales, manufactura, cumplimiento, cuotas de plataforma |
| Marketing y Publicidad | Anuncios, patrocinios, creación de contenido |
| Software y Herramientas | Suscripciones SaaS, hosting, dominios |
| Contratista y Freelancer | Mano de obra outsourced, VA, diseñadores |
| Oficina y Operaciones | Renta, servicios, suministros, internet |
| Servicios Profesionales | Legal, contabilidad, bookkeeping |
| Viajes y Comidas | Viaje de negocio, comidas de cliente |
| Seguros | Responsabilidad empresarial, E&O, salud (si gasto empresarial) |
| Educación y Capacitación | Cursos, conferencias, libros |
| Misceláneos | Cualquier cosa que no encaje arriba |

7. **PUNTO DE CONTROL: Si alguna transacción es ambigua, pide al usuario aclaración antes de proceder. No adivines categorías para montos mayores a $500.**

### Fase 3: Genera el Reporte P&G

8. Construye el reporte usando este formato:

```
ESTADO DE PÉRDIDAS Y GANANCIAS
[Nombre del Negocio]
Período: [Fecha de Inicio] — [Fecha de Fin]

═══════════════════════════════════════════════════
INGRESOS
───────────────────────────────────────────────────
Ventas de Productos                    $XX,XXX.XX
Ingresos por Servicios                 $XX,XXX.XX
Ingresos Recurrentes                   $XX,XXX.XX
Afiliado/Comisión                      $XX,XXX.XX
Otros Ingresos                         $XX,XXX.XX
───────────────────────────────────────────────────
INGRESOS TOTALES                       $XX,XXX.XX

═══════════════════════════════════════════════════
COSTO DE BIENES VENDIDOS (COGS)
───────────────────────────────────────────────────
[COGS Detallado]                       $XX,XXX.XX
───────────────────────────────────────────────────
COGS TOTAL                             $XX,XXX.XX

═══════════════════════════════════════════════════
GANANCIA BRUTA                         $XX,XXX.XX
MARGEN BRUTO                                XX.X%

═══════════════════════════════════════════════════
GASTOS OPERATIVOS
───────────────────────────────────────────────────
Marketing y Publicidad                  $X,XXX.XX
Software y Herramientas                 $X,XXX.XX
Contratista y Freelancer                $X,XXX.XX
Oficina y Operaciones                   $X,XXX.XX
Servicios Profesionales                 $X,XXX.XX
Viajes y Comidas                        $X,XXX.XX
Seguros                                 $X,XXX.XX
Educación y Capacitación                $X,XXX.XX
Misceláneos                             $X,XXX.XX
───────────────────────────────────────────────────
GASTOS OPERATIVOS TOTALES              $XX,XXX.XX

═══════════════════════════════════════════════════
GANANCIA (PÉRDIDA) NETA                $XX,XXX.XX
MARGEN NETO                                 XX.X%
═══════════════════════════════════════════════════
```

### Fase 4: Añade Análisis

9. Debajo del reporte, incluye:
   - **Top 3 categorías de gastos** por monto en dólares
   - **Evaluación de margen bruto**: Arriba de 50% es saludable para servicios, arriba de 30% para productos físicos
   - **Evaluación de margen neto**: Arriba de 20% es fuerte, 10-20% es aceptable, abajo de 10% necesita atención
   - **Tendencia mes a mes o trimestre a trimestre** si hay datos del período anterior disponibles
   - **Una recomendación accionable** basada en los números

### Fase 5: Entrega

10. Saca el reporte P&G formateado
11. Saca el resumen de análisis
12. Guarda a archivo si el usuario lo solicita

## Ejemplo 1: Diseñador Freelance — P&G Mensual

**Datos de entrada proporcionados por usuario:** "Ingresos de enero: 3 proyectos de cliente en $2,500, $4,000 y $1,800. Vendí 12 plantillas Canva en $29 cada una. Gastos: Adobe Creative Cloud $55, Figma $15, hosting Webflow $29, contraté VA por 20 horas en $25/hora, Facebook ads $350, espacio co-working $200, seguro empresarial $89, compré curso Skillshare por $45."

```
ESTADO DE PÉRDIDAS Y GANANCIAS
Ava Park Design Studio
Período: 1 de Enero — 31 de Enero, 2026

═══════════════════════════════════════════════════
INGRESOS
───────────────────────────────────────────────────
Ingresos por Servicios (3 proyectos)  $8,300.00
Ventas de Productos (12 plantillas)     $348.00
───────────────────────────────────────────────────
INGRESOS TOTALES                      $8,648.00

═══════════════════════════════════════════════════
COSTO DE BIENES VENDIDOS (COGS)
───────────────────────────────────────────────────
Canva Pro (hosting de plantilla)         $13.00
───────────────────────────────────────────────────
COGS TOTAL                                $13.00

═══════════════════════════════════════════════════
GANANCIA BRUTA                        $8,635.00
MARGEN BRUTO                              99.8%

═══════════════════════════════════════════════════
GASTOS OPERATIVOS
───────────────────────────────────────────────────
Marketing y Publicidad                  $350.00
Software y Herramientas                  $99.00
  - Adobe Creative Cloud     $55.00
  - Figma                    $15.00
  - Webflow                  $29.00
Contratista y Freelancer                $500.00
  - Asistente Virtual (20hrs x $25)
Oficina y Operaciones                   $200.00
  - Espacio co-working
Seguros                                  $89.00
Educación y Capacitación                 $45.00
  - Curso Skillshare
───────────────────────────────────────────────────
GASTOS OPERATIVOS TOTALES             $1,283.00

═══════════════════════════════════════════════════
GANANCIA NETA                         $7,352.00
MARGEN NETO                                85.0%
═══════════════════════════════════════════════════
```

**Análisis:**
- **Top 3 gastos:** Contratista ($500), Marketing ($350), Oficina ($200)
- **Margen bruto: 99.8%** — Excepcional. Típico para negocios de servicio con COGS mínimo.
- **Margen neto: 85.0%** — Muy fuerte. Bien arriba del benchmark del 20% para negocios saludables.
- **Recomendación:** El gasto de marketing ($350) generó $8,648 en ingresos. Si esos anuncios de Facebook están impulsando consultas de clientes, considera aumentar presupuesto de anuncios a $500-$700 para probar si ingresos escalan proporcionalmente.

## Anti-patrones

- **NO** incluyas gastos personales en un reporte empresarial P&G
- **NO** adivines categorías para transacciones ambiguas mayores a $500
- **NO** incluyas depreciación o gastos no en efectivo a menos que el usuario específicamente los solicite
- **NO** calcules responsabilidad fiscal — este reporte es para P&L solamente
- **NO** mezcles períodos (enero-febrero) con reportes etiquetados como mensuales

## Recuperación

- **Usuario tiene datos incompletos:** Construye P&L con lo que tienen y etiqueta campos faltantes como "No proporcionado"
- **Usuario no está seguro de categorías:** Presenta la tabla de categorías, haz tu mejor suposición, marca para revisión
- **Usuario quiere "formatos diferentes":** Los márgenes y totales son consistentes; puedes cambiar diseño pero mantén datos iguales
