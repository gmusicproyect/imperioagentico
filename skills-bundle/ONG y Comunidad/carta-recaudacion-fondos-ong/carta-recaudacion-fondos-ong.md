---
name: carta-recaudacion-fondos-ong
description: "Escribe cartas de apelación de recaudación de fondos con narrativas, datos de impacto, solicitudes de donación y secuencias de seguimiento."
allowed-tools: Read Write Glob
metadata:
  author: Imperio Digital
  version: "1.0"
---

# Carta de Recaudación de Fondos para ONG

## Cuándo Usar Este Skill

Usa este skill cuando necesites:
- Escribir una carta de apelación de recaudación de fondos para una ONG u organización basada en causa
- Crear emails de solicitud de donantes o correo directo con narrativa y datos de impacto
- Construir una secuencia de recaudación de fondos de múltiples contactos con solicitudes escalonadas
- Redactar apelaciones de fin de año, emergencia o específicas de campaña

**NO** uses este skill para solicitudes de subvenciones, propuestas de patrocinio o cartas de ventas con fines de lucro. Esto es para comunicaciones de recaudación de fondos dirigidas a donantes.

---

## Principio Fundamental

LOS DONANTES DONAN A PERSONAS, NO A ORGANIZACIONES — CADA CARTA DE RECAUDACIÓN DE FONDOS DEBE CONTAR LA HISTORIA DE UNA PERSONA, MOSTRAR EL IMPACTO ESPECÍFICO DE UN REGALO Y HACER QUE DONAR SEA EL SIGUIENTE PASO OBVIO.

---

## Fase 1: Resumen

### Información Requerida

| Entrada | Qué Preguntar | Predeterminado |
|---------|--------------|--------|
| **Organización y misión** | "¿Cuál es la organización y qué hace?" | Sin predeterminado — debe proporcionarse |
| **Tipo de campaña** | "¿Es fin de año, emergencia, específico de proyecto o fondo general?" | Apelación de fondo general |
| **Cantidad de la solicitud** | "¿Qué cantidad de donación estás buscando?" | Escalonado: $25, $50, $100, $250 |
| **Historia de beneficiario** | "¿Puedes compartir una historia específica de alguien a quien tu organización ha ayudado?" | Sin predeterminado — debe proporcionarse |
| **Métricas de impacto** | "¿Qué logra una donación? ($50 = X, $100 = Y)" | Sin predeterminado — debe proporcionarse |
| **Audiencia** | "¿Quién recibe esto? (donantes actuales, donantes anteriores, prospectos)" | Donantes actuales |

**PUNTO DE CONTROL: Confirma el resumen antes de escribir.**

---

## Fase 2: Estructura

### Arquitectura de Carta

```
1. GANCHO — Una historia que crea conexión emocional (2-3 párrafos)
2. PROBLEMA — La necesidad más amplia que representa esta historia (1-2 párrafos)
3. SOLUCIÓN — Cómo la organización lo aborda (1-2 párrafos)
4. IMPACTO — Qué logra una donación específica (escalera de impacto)
5. SOLICITUD — Solicitud clara y específica con opciones de donación
6. URGENCIA — Por qué ahora es importante (plazo, regalo igualado, necesidad inmediata)
7. CIERRE — Gratitud y visión del futuro que ayudan a crear
8. P.D. — Reafirma el punto más convincente (sección más leída después de la apertura)
```

### Escalera de Impacto

```
$25 — [Impacto específico y tangible]
$50 — [Impacto específico y tangible]
$100 — [Impacto específico y tangible]
$250 — [Impacto específico y tangible]
$___  — Cualquier cantidad hace una diferencia porque [razón]
```

**PUNTO DE CONTROL: Presenta la estructura y escalera de impacto para aprobación.**

---

## Fase 3: Escribir

### Reglas de Escritura

- **Una historia, una persona** — no generalices. Nómbrala (o usa un nombre representativo con divulgación).
- **Muestra, no digas** — "María caminó 3 millas a la fuente de agua más cercana" vence a "Muchas personas carecen de acceso a agua."
- **Segunda persona durante** — "Tu regalo de $50" no "Una donación de $50."
- **Párrafos cortos** — 1-3 frases. El espacio en blanco es tu amigo.
- **Voz activa** — "Puedes cambiar la vida de María hoy" no "Las vidas pueden ser cambiadas."
- **Una solicitud clara** — no pidas que donen Y se ofrezcan como voluntarios Y compartan Y asistan.

### Plantilla de Carta

```
Estimado/a [Nombre / Amigo/a],

[Hook: Abre con la historia del beneficiario — un momento específico, no un resumen]

[Problema: Conecta esta historia al problema más amplio que tu organización aborda]

[Solución: Muestra qué está haciendo tu organización y cómo funciona]

[Impacto: Aquí es lo que TU regalo hace posible:]
- $25 proporciona [resultado específico]
- $50 proporciona [resultado específico]
- $100 proporciona [resultado específico]

[Solicitud: ¿Harás una donación de $[cantidad sugerida] hoy?]

[Urgencia: Plazo, oportunidad de regalo igualado o necesidad inmediata]

[Cierre: Gracias + visión del futuro que su regalo ayuda a crear]

Con gratitud,
[Firma]
[Título, Organización]

P.D. [Reafirma el elemento más poderoso — la historia, el regalo igualado o el plazo]
```

### Secuencia de Seguimiento

```
## Secuencia de Seguimiento de 3 Emails

**Email 1 (Día 3):** Recordatorio con un ángulo diferente de la misma historia
**Email 2 (Día 7):** Social proof — "X donantes ya han dado, aquí está lo que hemos recaudado"
**Email 3 (Día 14 o plazo):** Última oportunidad — enfoque de urgencia con countdown
```

---

## Fase 4: Pulir

### 1. Revisión Emocional

Revisa la carta para:
- ¿La apertura crea una respuesta emocional dentro de las primeras 3 frases?
- ¿El impacto es específico suficientemente que un donante puede visualizar exactamente qué hace su regalo?
- ¿El P.D. se mantiene por sí solo como una razón convincente para donar?
- ¿La culpa está ausente? (La recaudación de fondos efectiva inspira, no avergüenza.)

### 2. Revisión Técnica

```
- [ ] El nombre del donante está personalizado (o "Amigo/a" como alternativa)
- [ ] La cantidad de la solicitud coincide con el segmento de audiencia (no pidas $25 a donantes de $1,000)
- [ ] El enlace de donación o mecanismo de respuesta es claro y prominente
- [ ] Las afirmaciones de impacto son precisas y verificables
- [ ] La historia tiene permiso de ser compartida (o está anonimizada)
- [ ] La carta es menos de 2 páginas (correo directo) o menos de 500 palabras (email)
```

### 3. Sugerencias de Prueba A/B

Recomienda probar:
- Línea de asunto (email) o teaser de sobre (correo)
- Historia de apertura vs. apertura con la solicitud
- Cantidad de solicitud única vs. cantidades escalonadas
- Con lenguaje de regalo igualado vs. sin él

---

## Ejemplo 1: Apelación de Fin de Año

```
Hook: "El enero pasado, Deshawn entró a nuestro taller con $47 en su cuenta bancaria y una idea de negocio en una servilleta."
Impacto: "$100 financia un emprendedor a través de nuestro programa de 6 semanas"
Urgencia: "Todos los regalos antes del 31 de diciembre están igualados dólar por dólar"
P.D.: "El negocio de Deshawn ahora gana $4,000/mes. Tu regalo de fin de año crea el próximo Deshawn."
```

## Ejemplo 2: Apelación de Emergencia

```
Hook: "Cuando la tormenta golpeó el martes pasado, 200 familias lo perdieron todo en 6 horas."
Impacto: "$50 proporciona suministros de emergencia para una familia durante una semana"
Urgencia: "Las familias necesitan ayuda AHORA — cada hora cuenta"
P.D.: "200 familias. $50 cada una. Tú puedes ser la razón por la que una familia duerme segura esta noche."
```

---

## Anti-Patrones

- **Estadísticas sin historias** — "Servimos a 10,000 personas" es olvidable. La historia de una persona es inolvidable.
- **Apelaciones basadas en culpa** — "¿Cómo puedes ignorar este sufrimiento?" aleja a los donantes. Inspira acción, no avergüenza inacción.
- **Enterrar la solicitud** — la solicitud de donación debe ser inconfundible, no escondida en el párrafo 6.
- **Impacto vago** — "Tu regalo hace una diferencia" no significa nada. "Tu $50 alimenta a una familia durante una semana" lo significa todo.
- **Sin P.D.** — el post scriptum es la segunda parte más leída de cualquier carta. Nunca la omitas.
- **Pedir a todos por la misma cantidad** — segmenta tu lista. Un donante por primera vez obtiene una solicitud diferente a un donante anual de $500.

---

## Recuperación

- **Sin historia de beneficiario disponible:** Usa una historia compuesta basada en experiencias reales (divulga que es representativa). O cuenta la historia de un voluntario o miembro del personal.
- **El usuario no puede cuantificar el impacto:** Trabaja hacia atrás desde el presupuesto. Si el programa cuesta $50,000 y sirve a 100 personas, cada persona cuesta $500 servir. Divide eso en incrementos amigables para donantes.
- **La audiencia son donantes anteriores:** Usa lenguaje "Te extrañamos" y muestra qué ha cambiado desde que dieron por última vez. Ofrece una cantidad de re-entrada más baja.
- **La organización es nueva sin historial:** Enfócate en la visión y la historia de fundación. Pide "donantes fundadores" que crean en la misión antes de que la prueba exista.
