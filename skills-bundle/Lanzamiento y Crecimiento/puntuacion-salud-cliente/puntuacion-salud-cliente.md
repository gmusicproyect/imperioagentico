---
name: puntuacion-salud-cliente
description: "Diseña modelos de puntuación de salud de cliente con métricas de compromiso, indicadores de riesgo y disparadores de intervención para prevenir rotación de forma proactiva."
allowed-tools: Read Write Glob
metadata:
  author: Imperio Digital
  version: "1.0"
---

# Puntuación de Salud de Cliente

## Cuándo Usar Esta Competencia

Usa esta competencia cuando necesites:
- Construir un modelo de puntuación que identifique clientes en riesgo antes de que se vayan
- Definir métricas de compromiso e indicadores de riesgo para cuentas de cliente
- Crear disparadores de intervención y guías de reproducción para diferentes niveles de salud
- Priorizar esfuerzos de customer success basado en datos de salud objetivo

## Principio Fundamental

LA SALUD DE CLIENTE ES UN INDICADOR ADELANTADO — PARA CUANDO UN CLIENTE TE DICE QUE SE VA, LA DECISIÓN SE TOMÓ HACE SEMANAS. UNA PUNTUACIÓN DE SALUD TE DA ESAS SEMANAS ATRÁS.

## Fase 1: Define Señales de Salud

Identifica lo que se ven clientes saludables vs. poco saludables.

### Entradas Requeridas

| Entrada | Qué Preguntar | Predeterminado |
|---------|-------------|--------------|
| **Modelo de negocio** | "¿Suscripción, basado en proyecto, retainer, o producto?" | Suscripción |
| **Perfil de cliente saludable** | "Describe tu cliente más comprometido y feliz. ¿Qué hacen?" | Sin predeterminado |
| **Señales de rotación** | "Piensa en clientes que se fueron. ¿Qué hicieron (o dejaron de hacer) antes de irse?" | Sin predeterminado |
| **Datos disponibles** | "¿Qué datos de cliente rastreas? (frecuencia de login, uso, tickets de soporte, historial de pago)" | Básico — compromiso de correo, pago |
| **Conteo de clientes** | "¿Cuántos clientes activos tienes?" | Bajo 50 |

**PUNTO DE CONTROL: Confirma señales de salud antes de construir el modelo de puntuación.**

## Fase 2: Construye Modelo de Puntuación

Crea una puntuación de salud ponderada de 0-100.

### Componentes de Puntuación de Salud

```
## Modelo de Puntuación de Salud de Cliente

**Rango de puntuación:** 0-100
**Saludable:** 70-100
**En riesgo:** 40-69
**Crítico:** 0-39

### Componentes de Puntuación

| Componente | Peso | Métrica | Puntuación |
|-----------|------|---------|---------|
| Compromiso | 30% | [Frecuencia de uso, tasa de login, adopción de característica] | 0-30 puntos |
| Relación | 25% | [Capacidad de respuesta de comunicación, asistencia a reunión, participación en feedback] | 0-25 puntos |
| Financiero | 25% | [Pago a tiempo, ingresos de expansión, duración de contrato] | 0-25 puntos |
| Satisfacción | 20% | [NPS, CSAT, sentimiento de ticket de soporte] | 0-20 puntos |
```

## Fase 3: Guías de Intervención

Define acciones para cada zona de salud.

```
## Acciones de Zona de Salud

### Saludable (70-100) — Nutre y Expande
**Frecuencia de verificación:** Mensual
**Acciones:**
- Envía contenido de valor agregado y tips
- Identifica oportunidades de ampliación o referencia
- Solicita testimoniales o casos de estudio
- Invita a junta asesora o programas beta

### En Riesgo (40-69) — Compromete y Recupera
**Frecuencia de verificación:** Quincenalmente
**Acciones:**
- Contacto personal del propietario de cuenta (no automatizado)
- Identifica declive específico — qué componente bajó?
- Ofrece capacitación, soporte o sesión de estrategia
- Aborda problemas no resueltos inmediatamente

### Crítico (0-39) — Salva o Prepara
**Frecuencia de verificación:** Semanalmente
**Acciones:**
- Escala al propietario del negocio
- Llamada directa o reunión de video (no correo)
- Pregunta explícitamente: "¿Qué necesitaría cambiar para que esto funcione?"
- Ofrece concesión si es apropiada (descuento, crédito de servicio, etc.)
- Si no se puede recuperar, realiza entrevista de salida para aprender
```

## Fase 4: Operacionaliza

Haz la puntuación de salud parte del ritmo regular del negocio.

### Cadencia de Puntuación

- **Mensual:** Actualiza todas las puntuaciones de salud de cliente
- **Semanal:** Revisa cualquier cliente marcado como Crítico
- **Trimestral:** Analiza tendencias — ¿está mejorando o decayendo la salud general?

## Anti-Patrones

- Puntuación sin acción — una puntuación de salud es inútil si nadie actúa en ella. Cada zona necesita una guía de reproducción definida
- Modelo demasiado complicado — comienza con 3-4 componentes. Agregar 10 métricas hace la puntuación difícil de mantener e interpretar
- Puntuación solo en sentimiento — la puntuación debe basarse en comportamiento observable y medible, no "creo que son felices"
- Ignorar clientes saludables — puntuaciones altas de salud necesitan atención también. Los promotores descuidados se vuelven pasivos
- Modelo estático — el comportamiento de cliente cambia. Recalibra el modelo trimestralmente
