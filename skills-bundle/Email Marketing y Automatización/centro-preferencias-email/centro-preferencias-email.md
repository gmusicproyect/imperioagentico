---
name: centro-preferencias-email
description: "Diseña centro de preferencias de email que permite a suscriptores controlar frecuencia, temas, y tipo de contenido que reciben."
allowed-tools: Read Write Glob
metadata:
  author: Imperio Digital
  version: "1.0"
---

# Centro de Preferencias de Email

## Cuándo Usar Este Skill

Usa este skill cuando necesites:
- Dar a suscriptores control sobre email que reciben
- Reducir unsubscribes ofreciendo preferencias
- Segmentar por interés sin necesidad de reafiliación
- Cumplir con GDPR/CCPA requiriendo preferencias claras

---

## Principio Fundamental

LAS PERSONAS SE DESUSCRIBEN PORQUE RECIBEN EMAILS EQUIVOCADOS, NO PORQUE ODIABAN TUS EMAILS — DAL  ES CONTROL Y MANTÉN MÁS SUBSCRIBERS.

---

## Estructura del Centro

### Opciones Mínimas

1. **Frecuencia**
   - Diariamente
   - Semanalmente
   - Mensualmente
   - Nunca (sin unsubscribirse)

2. **Temas/Categorías**
   - Selecciona qué contenido interesa
   - Mínimo 3-5 opciones
   - Checkboxes, no dropdowns

3. **Tipo de Contenido**
   - Eduactional
   - Promocional
   - Anuncios de producto
   - Actualizaciones de compañía

### Información Adicional

- Frecuencia de email aproximada
- Política de datos
- Opción de unsubscribe (legalmente requerida)

---

## Mejores Prácticas

- **Simple:** 2-3 opciones máximo, no abrumar
- **Visual:** Checkboxes claros, layout limpio
- **Accesible:** Trabajo en móvil, screenreader amigable
- **Confirmation:** Email de confirmación después cambio
- **Privacy:** HTTPS solo, sin almacenamiento de datos innecesarios
- **Fácil encontrar:** Enlace en pie de emails

---

## Flujo de Usuario

1. Usuario hace clic enlace "Preferencias"
2. Valida email (opcional si logged in)
3. Muestra opciones actuales
4. Usuario cambia preferencias
5. Guardar cambios
6. Confirmación: "Preferencias actualizadas"

---

## Implementación

### URL
`https://tudominio.com/email-preferences?email=user@example.com&token=secure_token`

### Datos a Guardar
- Email
- Preferencias seleccionadas
- Timestamp del cambio
- IP (opcional, para seguridad)

### Sincronización
- Actualizar plataforma de email en tiempo real
- Respetaractualización en próximo envío
- Sin delay

---

## Anti-Patrones

- **Ocultar enlace de preferencias** — obligatorio legalmente
- **Requiere re-opt-in** — eso es unsubscribe disfrazado
- **Demasiadas opciones** — confunde decisión
- **No sincronizar con plataforma** — crea fricción
- **Cambios requieren confirmación extra** — añade pasos

---

## Checklist

- [ ] Mínimo 2 opciones (frecuencia + categoría)
- [ ] Funciona en móvil
- [ ] Enlace en pie de cada email
- [ ] Cambios guardados inmediatamente
- [ ] Confirmación envida por email
- [ ] HTTPS/seguro
- [ ] GDPR compliant
