---
name: flujo-cancelacion-saas
description: "Diseña flujos de cancelación con ofertas de retención, recolección de feedback y disparadores de secuencias de recuperación. Usa cuando construyas u optimices experiencias de cancelación de suscripciones."
allowed-tools: Read Write Glob
metadata:
  author: Imperio Digital
  version: "1.0"
---

# Flujo de Cancelación SaaS

## Cuándo Usar Este Skill

Usa este skill cuando necesites:
- Diseñar un flujo de cancelación que retenga usuarios sin ser manipulativo
- Construir ofertas de retención vinculadas a razones específicas de cancelación
- Crear una encuesta de salida que produzca datos accionables
- Configurar disparadores de email de recuperación para cuentas canceladas

**NO** uses este skill para prevención de churn (intervenciones pre-cancelación), cambios de precios o guiones de soporte al cliente. Esto es para el UX y mensajería del flujo de cancelación.

---

## Principio Fundamental

UN FLUJO DE CANCELACIÓN RESPETA LA DECISIÓN DEL USUARIO MIENTRAS OFRECE ALTERNATIVAS GENUINAS — LOS DARK PATTERNS DESTRUYEN LA CONFIANZA Y GENERAN CONTRACARGOS. HAZLO FÁCIL DE IRSE Y QUE VALGA LA PENA QUEDARSE.

---

## Fase 1: Brief

### Información Requerida

| Dato | Qué Preguntar | Predeterminado |
|------|---------------|----------------|
| **Producto y precios** | "¿Cuál es el producto y cuánto cuestan los planes?" | Sin predeterminado — debe proporcionarse |
| **Tasa de cancelación actual** | "¿Qué porcentaje de usuarios cancela por mes?" | Desconocido |
| **Principales razones de cancelación** | "¿Por qué cancelan los usuarios? Lista las 3-5 razones principales." | Sin predeterminado — debe proporcionarse |
| **Flujo actual** | "¿Cuál es el proceso de cancelación hoy?" | Email a soporte para cancelar |
| **Presupuesto de retención** | "¿Estás dispuesto a ofrecer descuentos o créditos para salvar cuentas?" | Sí, dentro de límites |
| **Proveedor de facturación** | "¿Qué gestiona tu facturación? Stripe, Paddle, ¿personalizado?" | Stripe |

**PUNTO DE CONTROL: Confirma el brief antes de diseñar el flujo.**

---

## Fase 2: Diseñar el Flujo

### Pasos del Flujo de Cancelación

```
1. El usuario hace clic en "Cancelar Suscripción"
   ↓
2. Encuesta de Salida (obligatoria, 1 pregunta)
   ↓
3. Oferta de Retención Personalizada (basada en respuesta de encuesta)
   ↓
4a. El usuario acepta la oferta → La suscripción continúa
4b. El usuario rechaza → Página de confirmación
   ↓
5. Confirmación + qué pierde + cuándo termina el acceso
   ↓
6. Secuencia de recuperación activada (Día 3, 7, 30)
```

### Diseño de Encuesta de Salida

Una pregunta principal con 5-7 opciones:

```
"Lamentamos verte partir. ¿Cuál es la razón principal por la que cancelas?"

○ Demasiado caro
○ No lo uso suficiente
○ Le falta una función que necesito
○ Cambiando a otra herramienta
○ El negocio está cerrando/pausando
○ Tuve una mala experiencia
○ Otro: [campo de texto]
```

**Reglas:**
- Una sola pregunta (la tasa de completación cae con cada pregunta adicional)
- Obligatoria antes de continuar (pero no ocultes el botón de cancelar)
- Campo de texto opcional para elaborar
- Sin lenguaje que genere culpa

**PUNTO DE CONTROL: Confirma el flujo y la encuesta antes de escribir ofertas y copy.**

---

## Fase 3: Escribir

### Ofertas de Retención por Razón

| Razón | Oferta | Copy |
|-------|--------|------|
| Demasiado caro | 30% de descuento por 3 meses | "Nos encantaría que te quedes. ¿Qué tal 30% de descuento los próximos 3 meses mientras evalúas el ROI?" |
| No lo uso suficiente | Llamada estratégica gratuita | "Déjanos ayudarte a obtener más valor. Agenda una llamada de configuración gratuita de 15 minutos y optimizaremos tu cuenta." |
| Le falta una función | Vista previa del roadmap + cronograma | "Esa función está en nuestro roadmap para [mes]. ¿Quieres quedarte y ser el primero en probarla?" |
| Cambiando a otra herramienta | Comparación de funciones | "Antes de irte — así nos comparamos en [diferenciador clave]. ¿Una [mejora específica] cambiaría tu decisión?" |
| Negocio cerrando | Opción de pausa (90 días) | "Lo entendemos. Puedes pausar tu suscripción hasta 90 días y retomar donde lo dejaste." |
| Mala experiencia | Escalamiento al fundador | "Lamento tu experiencia. ¿Puedo conectarte con [nombre del fundador] directamente para solucionarlo?" |

### Copy de Página de Confirmación

```
## Tu suscripción ha sido cancelada

**Qué pasa ahora:**
- Tienes acceso hasta [fecha de fin del ciclo de facturación]
- Tus datos se guardarán por 90 días
- Puedes reactivar en cualquier momento desde la configuración de tu cuenta

**A qué perderás acceso:**
- [Función clave 1]
- [Función clave 2]
- [Función clave 3]

Nos encantaría tenerte de vuelta. Si algo cambia, tu cuenta está a un clic de distancia.
```

### Secuencia de Emails de Recuperación

| Email | Momento | Asunto | Enfoque |
|-------|---------|--------|---------|
| 1 | Día 3 | "Tu cuenta sigue aquí" | Reconocer la partida, sin presión |
| 2 | Día 7 | "Esto es lo que te estás perdiendo" | Destacar nuevas funciones o mejoras |
| 3 | Día 30 | "Regresa — [oferta especial]" | Oferta de descuento o crédito |

---

## Fase 4: Pulir

### 1. Métricas a Rastrear

```
## Métricas del Flujo de Cancelación

- **Tasa de salvamento:** % de usuarios que inician cancelación pero aceptan una oferta de retención
- **Tasa de completación de encuesta de salida:** % que responde la pregunta de la encuesta
- **Principales razones de cancelación:** Rankeadas por frecuencia
- **Tasa de conversión de recuperación:** % que reactiva dentro de 30/60/90 días
- **Tiempo para cancelar:** Segundos desde clic en "Cancelar" hasta confirmación (mantener bajo 60)
- **Tasa de contracargos:** Debería disminuir con un flujo transparente
```

### 2. Cumplimiento Legal y UX

- El botón de cancelar debe ser encontrable en máximo 2 clics desde configuración de cuenta
- Sin opciones de cancelar ocultas o en gris
- Sin requerir llamadas telefónicas o emails para cancelar
- Email de confirmación enviado inmediatamente después de la cancelación
- Política de retención de datos claramente indicada
- Cumplir con regulaciones aplicables (FTC, protección al consumidor de la UE)

### 3. Lista de Verificación de Calidad

```
## Lista de Verificación del Flujo de Cancelación

- [ ] La opción de cancelar es encontrable en máximo 2 clics
- [ ] La encuesta de salida es 1 pregunta con 5-7 opciones
- [ ] Las ofertas de retención están vinculadas a razones específicas de cancelación
- [ ] Las ofertas tienen términos y límites claros (no descuentos ilimitados)
- [ ] La página de confirmación muestra qué pierde el usuario y cuándo termina el acceso
- [ ] La política de retención de datos está indicada en la página de confirmación
- [ ] El email de confirmación se envía inmediatamente
- [ ] La secuencia de recuperación se activa con la cancelación (Día 3, 7, 30)
- [ ] El tiempo para completar la cancelación es menor a 60 segundos
- [ ] Sin dark patterns (botones ocultos, culpabilización, llamadas obligatorias)
```

---

## Ejemplo

**Producto:** SaaS de gestión de proyectos, $29/mes

**Oferta de retención (demasiado caro):**
"Te escuchamos — $29/mes es una inversión. Podemos ofrecerte 3 meses a $19/mes mientras evalúas si el ahorro de tiempo justifica el costo. Son $30 de vuelta a tu bolsillo. [Aceptar Oferta] [No gracias, cancelar]"

**Email de recuperación (Día 30):**
```
Asunto: Hemos hecho algunos cambios desde que te fuiste

Hola [Nombre],

Desde que cancelaste, hemos lanzado:
- [Nueva función 1]
- [Mejora relevante a su razón de cancelación]

Regresa y pruébalo gratis por 7 días — sin compromiso, sin tarjeta de crédito.

[Reactivar Mi Cuenta]
```

---

## Anti-Patrones

- **Dark patterns** — ocultar el botón de cancelar, requerir llamadas o agregar pasos innecesarios. Los usuarios harán contracargo e irán enojados.
- **Misma oferta para cada razón** — un descuento no ayuda a alguien cuyo negocio está cerrando. Vincula la oferta a la razón.
- **Sin encuesta de salida** — las cancelaciones sin datos son oportunidades de aprendizaje desperdiciadas.
- **Copy que genera culpa** — "¿Estás seguro de que quieres abandonar tu progreso?" es manipulativo. Sé respetuoso.
- **Sin secuencia de recuperación** — 20-30% de los que cancelan son recuperables dentro de 90 días. El silencio después de la cancelación deja dinero en la mesa.

---

## Recuperación

- **No puedes ofrecer descuentos:** Ofrece un downgrade de plan, pausa de funciones o prueba extendida en su lugar.
- **Sin datos sobre por qué cancelan los usuarios:** Implementa la encuesta de salida inmediatamente. Incluso 2 semanas de datos revelan patrones.
- **Los usuarios se quejan de que el flujo es muy largo:** Reduce pasos. Encuesta + una oferta + confirmación es el máximo. Si toma más de 60 segundos, simplifica.
- **Alta tasa de contracargos:** Tu flujo de cancelación es muy difícil de encontrar o completar. Arregla el UX inmediatamente.
