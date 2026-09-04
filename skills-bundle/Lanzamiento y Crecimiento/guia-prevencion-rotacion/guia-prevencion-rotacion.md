---
name: guia-prevencion-rotacion
description: "Crea guías de prevención de rotación con indicadores de alerta temprana, secuencias de intervención y estrategias de oferta de salvaguarda. Usa cuando reduces rotación de clientes en negocios de suscripción."
allowed-tools: Read Write Glob
metadata:
  author: Imperio Digital
  version: "1.0"
---

# Guía de Prevención de Rotación

## Cuándo Usar Esta Competencia

Usa esta competencia cuando necesites:
- Construir una estrategia sistemática de prevención de rotación para un negocio de suscripción
- Identificar señales de advertencia temprana que predicen cancelación de clientes
- Diseñar secuencias de intervención para salvar cuentas en riesgo
- Crear ofertas de salvaguarda y guías de reproducción para equipos de soporte

## Principio Fundamental

LA PREVENCIÓN DE ROTACIÓN COMIENZA 60 DÍAS ANTES DEL CLIC DE CANCELACIÓN — PARA CUANDO UN CLIENTE PIDE CANCELAR, YA HAS PERDIDO LA MAYORÍA DE LA BATALLA.

## Fase 1: Resumen Ejecutivo

### Entradas Requeridas

| Entrada | Qué Preguntar | Predeterminado |
|---------|-------------|--------------|
| **Tipo de producto** | "¿Cuál es tu producto de suscripción?" | Sin predeterminado — debe proporcionarse |
| **Tasa de rotación actual** | "¿Cuál es tu tasa de rotación mensual?" | Desconocida — estima de datos disponibles |
| **Ciclo de facturación** | "¿Mensual, anual, o ambos?" | Mensual |
| **Razones principales de cancelación** | "¿Por qué dicen que se van los clientes? Top 3 razones." | Sin predeterminado — entrada crítica |
| **Segmentos de clientes** | "¿Tienes diferentes niveles de cliente o segmentos?" | Nivel único |
| **Esfuerzos de retención actuales** | "¿Qué haces actualmente para prevenir rotación?" | Nada sistemático |

**PUNTO DE CONTROL: Confirma el resumen antes de construir la guía.**

## Fase 2: Plan

### Sistema de Advertencia Temprana

Define 5-8 señales de comportamiento que predicen rotación:

```
## Indicadores de Alerta Temprana

| Señal | Nivel de Riesgo | Ventana de Detección |
|-------|---------------|-------------------|
| Frecuencia de login baja 50%+ | Alto | 14 días |
| Uso de característica clave se detiene | Alto | 7 días |
| Tickets de soporte aumentan 3x | Medio | 30 días |
| Fallo de pago (sin actualización) | Alto | Inmediato |
| Asientos de equipo disminuyen | Medio | Ciclo de facturación |
| Consulta de degradación | Alto | Inmediato |
| Puntuación NPS cae bajo 6 | Medio | Ciclo de encuesta |
| Sin login 14+ días | Crítico | 14 días |
```

### Modelo de Puntuación de Riesgo

Crea un marco de puntuación simple:
- **Verde (0-2 señales):** Saludable — compromiso estándar
- **Amarillo (3-4 señales):** En riesgo — dispara contacto proactivo
- **Rojo (5+ señales):** Alto riesgo — intervención inmediata

**PUNTO DE CONTROL: Confirma indicadores y niveles de riesgo antes de diseñar intervenciones.**

## Fase 3: Escribe

### Guía de Intervención

Para cada nivel de riesgo, define la respuesta:

**Amarillo — Compromiso Proactivo:**
- Correo automatizado: "Notamos que no usaste [característica] recientemente. Aquí un consejo rápido..."
- Mensaje en-app destacando características subutilizadas
- Verificación de cliente success (si cuenta de alto valor)

**Rojo — Retención Activa:**
- Correo personal de fundador o líder CS
- Ofrece llamada de estrategia de 15 minutos
- Comparte historia de éxito de cliente relevante a su caso de uso
- Presenta una oferta de salvaguarda (mira menú de Oferta de Salvaguarda abajo)

**Página de Cancelación — Último Recurso:**
- Encuesta de salida (requerida, 3 preguntas máximo)
- Oferta de salvaguarda basada en razón declarada
- Opción de degradación en lugar de cancelación completa
- Opción de pausa de suscripción (30/60/90 días)

### Menú de Oferta de Salvaguarda

Diseña ofertas emparejadas a razones de cancelación:

| Razón | Oferta de Salvaguarda | Términos |
|------|---------------------|---------|
| Demasiado caro | Descuento (20-30% por 3 meses) | Una vez, no renovable |
| No la uso suficiente | Llamada de estrategia gratis + guía de uso | Dentro de 7 días |
| Característica faltante | Vista previa de roadmap + acceso beta | ETA de característica requerida |
| Cambio a competidor | Iguala precio de competidor o característica | Caso por caso |
| Negocio cerrando | Pausa de suscripción | Hasta 90 días |

## Fase 4: Pulimiento

### Marco de Métricas

```
## Métricas de Prevención de Rotación

- **Tasa de rotación mensual:** Rastrea tendencia mes-a-mes
- **Tasa de salvaguarda:** % de cuentas en riesgo retenidas después de intervención
- **Tasa de respuesta de intervención:** % de usuarios en riesgo que responden a contacto
- **Tasa de aceptación de oferta de salvaguarda:** % que aceptan una oferta de retención
- **Tiempo hasta señal de rotación:** Días promedio entre primera señal de advertencia y cancelación
- **Tasa de reactivación:** % de cuentas pausadas que se reanudan
```

### Anti-Patrones

- Descuentas para todos — ofertas de salvaguarda solo para clientes sensibles a precio. Los que no usan necesitan valor, no descuentos
- Ignorar señales de advertencia — esperar hasta cancelación es demasiado tarde. Intervén en amarillo, no rojo
- Correos genéricos "Te echamos de menos" — menciona comportamiento específico o características. Los correos genéricos se sienten automatizados e impersonales
- Sin encuesta de salida — si no sabes por qué se van, no puedes arreglarlo. Siempre recopila la razón
- Ofertas de salvaguarda ilimitadas — un descuento por cliente, con términos claros. De lo contrario entrenas clientes a amenazar cancelación para descuentos
