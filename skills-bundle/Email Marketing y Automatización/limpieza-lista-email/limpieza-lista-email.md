---
name: limpieza-lista-email
description: "Diseña procesos de limpieza de lista de email para eliminar inactivos, direcciones invalidas y direcciones de rebote. Úsalo cuando baje tu tasa de entrega o cresca list fatigue."
allowed-tools: Read Write Glob
metadata:
  author: Imperio Digital
  version: "1.0"
---

# Limpieza de Lista de Email

## Cuándo Usar Este Skill

Usa este skill cuando necesites:
- Identificar suscriptores inactivos en tu lista
- Eliminar direcciones inválidas o que rebotan
- Implementar re-engagement antes de eliminar
- Mejorar entregabilidad eliminando contactos problemáticos

**NO** uses este skill para segmentación general o targeting de audiencia. Esto es especialmente para limpiar y mantener lista saludable.

---

## Principio Fundamental

UNA LISTA MÁS PEQUEÑA DE PERSONAS COMPROMETIDAS SUPERA UNA LISTA GRANDE DE PERSONAS DORMIDAS — SIEMPRE.

---

## Fase 1: Auditar tu Lista

### Métricas a Revisar

- Tasa de apertura: <3% es inactivo
- Tasa de clic: <0.5% es muerto
- Bounce rate: >3% es problema
- Unsubscribe rate: >0.5% es problema
- Queja de spam: >0.1% es red flag

### Segmenta tu Lista

- **Activos:** Abrieron o clickearon últimos 90 días
- **Dormidos:** Sin engagement últimos 6 meses
- **Inválidos:** Hard bounces o spam reports
- **Riesgosos:** Soft bounce mayor a 5 intentos

---

## Fase 2: Plan de Re-engagement

Para suscriptores dormidos:

**Email 1:** "¿Todavía aquí?"
- Sencillo, preguntar si siguen interesados
- CTA: "Confirma que quieres estar en esta lista"
- Sin descuento o incentivo

**Email 2:** (5 días después)
- Oferta especial (descuento, contenido gratis)
- "Última oportunidad para quedarse en lista"
- Enlace confirmar suscripción

**Email 3:** (3 días después)
- Final - "Eliminándote en 3 días si no responder"
- Muy claro
- Enlace confirmar suscripción

### Decisión Post Re-engagement

- Confirmó = Quedarse en lista y enviar contenido
- No respondió = Eliminar suave (mover a otro lista)
- Hard bounce = Eliminar inmediatamente

---

## Fase 3: Limpieza Automática

Implementa esto cada trimestre:

- Eliminar hard bounces
- Eliminar 3+ spam reports
- Ejecutar re-engagement en inactivos
- Validar nuevas direcciones al sign-up

---

## Métricas de Éxito

Después de limpieza:
- Open rate debería SUBIR 20-30%
- Click rate debería SUBIR 30-50%
- Bounce rate debería BAJAR <2%

---

## Anti-Patrones

- **Eliminar sin re-engagement** — algunos dormidos pueden reactivarse
- **Mantener inactivos para números** — mata entregabilidad
- **Elminar demasiado agresivo** — personas se van de vacaciones y vuelven
- **Sin validación de new signups** — previene problemas de bounce

---

## Recuperación

- **Bounce rate alto:** Valida emails en signup, verifica formato
- **Muchos inactivos:** Tu contenido no es relevante, reexamina estrategia
- **Re-engagement baja:** Tu offer no es atractivo, intenta algo diferente
