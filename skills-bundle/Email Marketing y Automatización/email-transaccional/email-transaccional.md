---
name: email-transaccional
description: "Diseña emails transaccionales (confirmación, recibos, resets) que construyen confianza."
allowed-tools: Read Write Glob
metadata:
  author: Imperio Digital
  version: "1.0"
---

# Email Transaccional

## Cuándo Usar Este Skill

Usa este skill cuando necesites:
- Confirmación de compra
- Recibos de pago
- Password reset
- Cambios de cuenta
- Shipping updates

---

## Principio FUNDAMENTAL

UN EMAIL TRANSACCIONAL DEBE SER CLARO PRIMERO, HERMOSO SEGUNDO — CLARIDAD > DISEÑO.

---

## Tipos Principales

### Confirmación de Compra
- Número de orden
- Items + precio
- Total
- Próximos pasos

### Recibo de Pago
- Información de pago
- Confirmación de transaction
- Cómo obtener help

### Password Reset
- Link (con expiración)
- Instrucciones
- Support si no te la pediste

### Shipping Notification
- Tracking number
- Expected delivery
- Return/exchange info

### Account Change
- Qué cambió
- Cuándo
- Cómo revert

---

## Template Email Confirmación

```
Subject: Order confirmation #[order-id]

Hi [Name],

Thanks for your order.

Order details:
- Order #[id]
- Date: [date]
- Items: [list]
- Total: $[amount]

What's next:
- Confirmation sent to [email]
- Ships by [date]
- Tracking: [link when available]

Questions? [support link]

— Team
```

---

## Design Rules

- **Clear subject line** — "Order confirmed #123" (not "YAY!")
- **Order number prominent** — top of email
- **Plain English** — no jargon
- **All important info above fold**
- **Simple table format** — items + prices
- **Clear CTA** — "Track your order"
- **Support contact** — phone + email + chat

---

## Anti-Patrones

- **Ambiguous** — "Your account" (which one?)
- **Sin contexto** — email aparece de nada
- **Links rotos** — tracking number no funciona
- **Sin expiración en reset links** — security risk
- **Too designed** — hard to find info importante

---

## Compliance

- **Include:** Company name, address, contact
- **Clear:** What happened, cuando, qué hacer next
- **Accessible:** Mobile-friendly, alt text on images
- **Secure:** Use HTTPS, no passwords in email

---

## Checklist

- [ ] Subject línea clara
- [ ] Confirmación de acción
- [ ] Datos importantes visibles
- [ ] Próximos pasos claros
- [ ] Support contact included
- [ ] Mobile optimizado
- [ ] Compliant con regulations
