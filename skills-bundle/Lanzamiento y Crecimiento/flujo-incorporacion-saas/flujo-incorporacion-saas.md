---
name: flujo-incorporacion-saas
description: "Diseña flujos de incorporación de usuarios SaaS con hitos de activación, secuencias de tooltips y métricas de éxito. Usa cuando construyas o mejores experiencias de incorporación de nuevos usuarios."
allowed-tools: Read Write Glob
metadata:
  author: Imperio Digital
  version: "1.0"
---

# Flujo de Onboarding SaaS

## Cuándo Usar Este Skill

Usa este skill cuando necesites:
- Diseñar un flujo de incorporación de nuevos usuarios para un producto SaaS
- Mejorar las tasas de activación reestructurando la experiencia del usuario por primera vez
- Definir hitos de activación y medir el éxito de la incorporación
- Crear secuencias de tooltips, emails de bienvenida e indicadores de progreso

**NO** uses este skill para documentación de soporte al cliente, tutoriales de funciones para usuarios existentes o guiones de demos de venta. Esto es solo para flujos de activación de nuevos usuarios.

---

## Principio Fundamental

LA INCORPORACIÓN TERMINA CUANDO EL USUARIO EXPERIMENTA EL VALOR CENTRAL DEL PRODUCTO — CADA PASO ANTES DE ESE MOMENTO DEBE REDUCIR LA FRICCIÓN Y ACELERAR EL TIEMPO HASTA EL VALOR.

---

## Fase 1: Brief

### Información Requerida

| Dato | Qué Preguntar | Predeterminado |
|------|---------------|----------------|
| **Descripción del producto** | "¿Qué hace tu producto SaaS en una oración?" | Sin predeterminado — debe proporcionarse |
| **Momento de valor central** | "¿Cuál es el momento 'ajá' — la acción donde los usuarios sienten el valor por primera vez?" | Sin predeterminado — debe proporcionarse |
| **Tasa actual registro-a-activación** | "¿Qué porcentaje de registros llega a tu momento de valor central?" | Desconocido — establecer línea base |
| **Tipo de incorporación** | "¿Product-led (autoservicio), asistido por ventas o híbrido?" | Product-led |
| **Persona del usuario** | "¿Quién es tu usuario principal? Rol, nivel técnico, nivel de urgencia." | Dueño de pequeño negocio, habilidades técnicas moderadas |
| **Pain points actuales** | "¿Dónde se caen o atascan los usuarios actualmente?" | Desconocido — diseñar desde cero |

**PUNTO DE CONTROL: Confirma el brief antes de mapear el flujo.**

---

## Fase 2: Mapear el Flujo

### Marco de Hitos de Activación

Define 3-5 hitos entre el registro y el momento de valor central:

```
## Hitos de Activación

1. **Registro Completo** — Cuenta creada, email verificado
2. **Configuración del Perfil** — Ajustes esenciales configurados (nombre, empresa, preferencias)
3. **Primera Acción** — El usuario realiza la acción principal del producto una vez
4. **Valor Central** — El usuario experimenta el momento "ajá" por primera vez
5. **Ciclo de Hábito** — El usuario regresa y repite la acción central dentro de 7 días
```

### Mapa del Flujo

Para cada hito, define:
- **Disparador:** Qué inicia este paso
- **Acción:** Qué necesita hacer el usuario
- **Elemento UI:** Tooltip, modal, checklist o email
- **Plan alternativo:** Qué pasa si el usuario no completa este paso en 24/48/72 horas

Presenta el mapa del flujo como un documento estructurado.

**PUNTO DE CONTROL: Confirma los hitos y el flujo antes de escribir el copy detallado.**

---

## Fase 3: Escribir

Redacta todo el copy y secuencias de incorporación:

### Elementos In-App

- **Modal de bienvenida:** 1 oración de bienvenida, 1 oración de qué hacer primero, 1 botón CTA
- **Checklist de progreso:** 3-5 ítems visibles en una barra lateral o widget del dashboard
- **Tooltips:** Máximo 2 oraciones cada uno. Apuntar al elemento UI específico. Incluir botón de "Entendido".
- **Estados vacíos:** Para cada pantalla en blanco que vea el usuario, escribe copy de placeholder útil con un CTA

### Secuencia de Email

Diseña una secuencia de 5 emails de incorporación:

| Email | Momento | Enfoque del Asunto | CTA |
|-------|---------|-------------------|-----|
| Bienvenida | Inmediatamente | Confirmar registro, establecer expectativas | Completar perfil |
| Victoria Rápida | Día 1 | Guiar a la primera acción | Hacer [acción central] |
| Historia de Valor | Día 3 | Historia de éxito de cliente | Regresar al producto |
| Verificación de Progreso | Día 5 | Reconocer progreso o re-enganchar | Completar siguiente hito |
| Empujón de Activación | Día 7 | Último empujón hacia el momento de valor central | [Acción específica] |

### Reglas de Copy

- **Orientado a la acción:** Cada pieza de copy le dice al usuario exactamente qué hacer después
- **Beneficio primero:** Explica POR QUÉ antes del CÓMO
- **Corto:** Tooltips menos de 20 palabras, modales menos de 50, emails menos de 150
- **Sin jerga:** Usa el lenguaje del usuario, no términos internos del producto

---

## Fase 4: Pulir

### 1. Dashboard de Métricas

Define las métricas para rastrear el éxito de la incorporación:

```
## Métricas de Onboarding

- **Tasa Registro-a-Activación:** % de registros que llegan al momento de valor central
- **Tiempo hasta el Valor:** Mediana de tiempo desde registro hasta primer momento de valor central
- **Tasas de Completación de Hitos:** % que completa cada hito
- **Puntos de Abandono:** Dónde los usuarios abandonan el flujo
- **Retención Día 7:** % de usuarios que regresan dentro de la primera semana
- **Engagement de Email:** Tasas de apertura y clic para cada email de incorporación
```

### 2. Sugerencias de Test A/B

Proporciona 3 hipótesis testeables:
- Testear eliminar un paso de incorporación para ver si la activación mejora
- Testear reordenar hitos (victoria rápida primero vs. perfil primero)
- Testear formato de tooltip vs. checklist para guía in-app

### 3. Lista de Verificación de Calidad

```
## Lista de Verificación del Flujo de Onboarding

- [ ] El momento de valor central está claramente definido y es medible
- [ ] 3-5 hitos conectan el registro con la activación
- [ ] Cada paso tiene un CTA claro (el usuario siempre sabe qué hacer después)
- [ ] Existen emails alternativos para usuarios que se estancan en cada hito
- [ ] Los estados vacíos tienen copy útil, no pantallas en blanco
- [ ] Los tooltips tienen menos de 20 palabras cada uno
- [ ] El email de bienvenida se envía inmediatamente (no horas después)
- [ ] El indicador de progreso es visible durante toda la incorporación
- [ ] Ningún paso requiere más de 2 minutos para completar
- [ ] La métrica de retención Día 7 está definida y es rastreable
```

---

## Ejemplo

**Producto:** Herramienta de gestión de proyectos para freelancers
**Momento de valor central:** El usuario crea su primer proyecto y agrega una tarea

**Modal de bienvenida:**
"Bienvenido a TaskFlow. Vamos a configurar tu primer proyecto en menos de 2 minutos — verás exactamente cómo TaskFlow mantiene organizado tu trabajo freelance. [Crear Mi Primer Proyecto]"

**Tooltip (en página de creación de proyecto):**
"Nombra tu proyecto con el nombre de tu cliente o proyecto. Puedes renombrarlo cuando quieras. [Entendido]"

---

## Anti-Patrones

- **Demasiados pasos antes del valor** — si la activación requiere 8 pasos, los usuarios no terminarán. Reduce a 3-5.
- **Pedir información que no necesitas aún** — posterga los campos del perfil que no son esenciales para el primer momento de valor.
- **Sin plan alternativo para usuarios estancados** — si alguien no completa el paso 2, necesita un empujón. Diseña el camino de rescate.
- **Sobrecarga de tooltips** — más de 3 tooltips seguidos se siente como un tutorial, no una guía. Espácialos.
- **Email de bienvenida genérico** — "¡Bienvenido a [Producto]!" sin siguiente paso desperdicia tu mejor ventana de engagement.

---

## Recuperación

- **No existen datos de activación:** Comienza con lo cualitativo — entrevista a 5 registros recientes sobre su primera experiencia. Usa su lenguaje en el flujo.
- **El momento de valor central no está claro:** Busca la acción más correlacionada con la retención. Si no estás seguro, elige la acción que los clientes que pagan hacen más.
- **El producto es complejo:** Divide la incorporación en "inicio rápido" (3 pasos hasta el primer valor) y "configuración avanzada" (configuración más profunda opcional).
- **El usuario abandona en el registro:** Simplifica a registro solo con email. Posterga todo lo demás al post-login.
