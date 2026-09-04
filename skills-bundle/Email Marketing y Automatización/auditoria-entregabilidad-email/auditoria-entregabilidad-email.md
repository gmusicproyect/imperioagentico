---
name: auditoria-entregabilidad-email
description: "Audita prácticas de email por problemas de entregabilidad incluyendo reputación del remitente, autenticación e higiene de lista. Úsalo cuando los emails caen en spam o las tasas de engagement caen."
allowed-tools: Read Write Glob
metadata:
  author: Imperio Digital
  version: "1.0"
---

# Auditoría de Entregabilidad de Email

## Cuándo Usar Este Skill

Usa este skill cuando necesites:
- Diagnosticar por qué los emails caen en spam o pestañas de promociones
- Auditar autenticación de remitente (SPF, DKIM, DMARC) y reputación del dominio
- Revisar prácticas de higiene de lista e identificar riesgos de entregabilidad
- Construir un plan de acción para mejorar tasas de colocación en bandeja de entrada

**NO** uses este skill para escribir emails, construir secuencias, o estrategia de email. Esta es una auditoría técnica de entregabilidad de email.

---

## Principio Fundamental

EL MEJOR EMAIL DEL MUNDO ES INÚTIL SI NUNCA LLEGA A LA BANDEJA DE ENTRADA — LA ENTREGABILIDAD ES LA FUNDACIÓN EN LA QUE TODA OTRA TÁCTICA DE EMAIL DEPENDE.

---

## Fase 1: Resumen

### Entradas Requeridas

| Entrada | Qué Preguntar | Por Defecto |
|-------|------------|---------|
| **Plataforma de email** | "¿Qué proveedor de servicio de email usas?" | Sin valor por defecto — debe ser proporcionado |
| **Dominio de envío** | "¿Desde qué dominio envías (p.ej., @tunegogio.com)?" | Sin valor por defecto — debe ser proporcionado |
| **Tamaño de lista** | "¿Cuántos suscriptores?" | Sin valor por defecto — debe ser proporcionado |
| **Tasa de apertura promedio** | "¿Cuáles son tus tasas de apertura actual?" | Desconocido — haré benchmark |
| **Problemas conocidos** | "¿Los emails van a spam, promociones, o rebotan?" | Desconocido |
| **Volumen de envío** | "¿Cuántos emails envías por semana/mes?" | Varía |
| **Fuente de lista** | "¿Cómo fueron adquiridos los suscriptores? Opt-in, comprado, importado?" | Opt-in |

**PUNTO DE CONTROL: Confirma el alcance antes de comenzar la auditoría.**

---

## Fase 2: Marco de Auditoría

### Áreas de Auditoría de Entregabilidad

1. **Autenticación de Remitente**
   - SPF (Sender Policy Framework)
   - DKIM (DomainKeys Identified Mail)
   - DMARC (Domain-based Message Authentication)

2. **Reputación del Dominio**
   - Score de reputación de IP
   - Historial de quejas de spam
   - Listas negras públicas

3. **Higiene de Lista**
   - Tasas de bounce (hard bounce vs. soft)
   - Frecuencia de bajas
   - Validación de direcciones de email

4. **Contenido de Email**
   - Spammy words o triggers
   - Enlace quality y ratios de texto/imagen
   - HTML validity

5. **Prácticas de Envío**
   - Warmup de IP (para nuevas IPs)
   - Consistencia de volumen
   - Frecuencia de envío

---

## Fase 3: Plan de Acción

### Quick Wins (Implementar Primero)

- [ ] Verifica SPF/DKIM/DMARC están configurados
- [ ] Usa una dirección "from" reconocible (nombre real, no noreply@)
- [ ] Incluye enlace de unsubscribe visible
- [ ] Elimina direcciones invalidas de lista
- [ ] Monitorea bounce rates

### Optimizaciones a Mediano Plazo

- [ ] Implementa double opt-in
- [ ] Segmenta por engagement
- [ ] Re-engagement para inactivos
- [ ] A/B test de líneas de asunto
- [ ] Monitorea lista negra

---

## Métricas a Rastrear

| Métrica | Objetivo |
|--------|---------|
| Tasa de entrega | 98%+ |
| Tasa de bounce | <3% |
| Tasa de queja spam | <0.3% |
| Tasa de apertura | 15-25% |
| Tasa de clic | 2-5% |

---

## Anti-Patrones

- **Sin SPF/DKIM/DMARC** — setup básico que toma 15 minutos
- **Lista sucia** — contactos inválidos y hard bounces dañan reputación
- **Falta de unsubscribe** — requerido legalmente y reduce reportes de spam
- **Cambios frecuentes de IP** — nuevas IPs deben calentarse
- **Ignorar bounce rates** — bounces altos destrozan reputación rápidamente

---

## Recuperación

- **Dominio en lista negra:** Solicitar delist, investigar causa root, implementar cambios
- **Bajas tasas de entrega:** Revisa SPF/DKIM, implementa warmup de IP
- **Muchas quejas:** Tema selección, frecuencia de envío, o list quality
