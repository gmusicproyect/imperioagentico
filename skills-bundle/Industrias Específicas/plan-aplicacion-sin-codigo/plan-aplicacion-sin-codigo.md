---
name: plan-aplicacion-sin-codigo
description: "Planifica compilaciones de aplicaciones sin código con selección de herramientas, mapeo de características y diseño de flujo de usuario. Usar cuando se construyen aplicaciones o herramientas sin escribir código."
allowed-tools: Read Write Glob
metadata:
  author: Imperio Digital
  version: "1.0"
---

# Plan de Aplicación Sin Código

## Cuándo Usar Esta Habilidad

Usa esta habilidad cuando necesites:
- Planificar una compilación de aplicación sin código desde concepto hasta lanzamiento
- Seleccionar las herramientas sin código correctas para tu caso de uso específico
- Mapear características y flujos de usuario antes de construir
- Crear un plan de compilación por fases con hitos

**NO** uses esta habilidad para desarrollo de software personalizado, tutoriales de herramientas sin código, o proyectos solo de sitios web (usa enfoques de diseño web estándar). Esto es para aplicaciones funcionales construidas con plataformas sin código.

---

## Principio Fundamental

SIN CÓDIGO ES UNA HERRAMIENTA DE CONSTRUCCIÓN, NO UN ATAJO — PLANIFICA LA APLICACIÓN ANTES DE TOCAR EL CONSTRUCTOR. UN PLAN CLARO PREVIENE LA FALLA SIN CÓDIGO MÁS COMÚN: CONSTRUIRTE HACIA UNA ESQUINA.

---

## Fase 1: Resumen

### Información Requerida

| Información | Qué Preguntar | Predeterminado |
|-------|------------|---------|
| **Concepto de aplicación** | "¿Qué hace la aplicación en una oración?" | Sin predeterminado — debe proporcionarse |
| **Usuario objetivo** | "¿Quién usará esta aplicación? Describe el usuario principal." | Sin predeterminado — debe proporcionarse |
| **Problema central** | "¿Qué problema resuelve esto para el usuario?" | Sin predeterminado — debe proporcionarse |
| **Características clave** | "Enumera las 5 principales características que la aplicación debe tener al lanzamiento." | Sin predeterminado — debe proporcionarse |
| **Experiencia sin código** | "¿Has construido con herramientas sin código antes? ¿Cuáles?" | Principiante |
| **Presupuesto** | "¿Cuál es tu presupuesto mensual para herramientas y hosting?" | Menos de $50/mes |
| **Cronograma** | "¿Cuándo necesitas esto en vivo?" | 4-6 semanas |

**PUNTO DE CONTROL: Confirma el resumen antes de seleccionar herramientas o diseñar flujos.**

---

## Fase 2: Diseña

### Mapa de Prioridad de Características

Categoriza características en fases de lanzamiento:

| Característica | Prioridad | Fase |
|---------|----------|-------|
| [Característica 1] | Imprescindible | MVP (v1) |
| [Característica 2] | Imprescindible | MVP (v1) |
| [Característica 3] | Imprescindible | MVP (v1) |
| [Característica 4] | Agradable | v2 |
| [Característica 5] | Agradable | v2 |
| [Característica 6] | Futuro | v3+ |

**Regla:** MVP incluye solo las características requeridas para que un usuario realice la tarea central. Todo lo demás es v2 o posterior.

### Diagramas de Flujo de Usuario

Mapea el viaje de usuario principal:

```
## Flujo de Usuario Principal

[Página de Inicio]
  → [Registrarse / Iniciar Sesión]
    → [Dashboard / Inicio]
      → [Acción Principal 1]
        → [Resultado / Confirmación]
      → [Acción Principal 2]
        → [Resultado / Confirmación]
    → [Configuración / Perfil]
    → [Cerrar Sesión]
```

Para cada pantalla, anota:
- Qué ve el usuario
- Qué acciones puede tomar
- Dónde lleva cada acción
- Qué datos se crean o se muestran

### Modelo de Datos

Define la estructura de datos:

```
## Modelo de Datos

**Usuarios**
- Nombre, email, contraseña, rol, fecha_creada

**[Entidad Principal]**
- [Campo 1]: [tipo]
- [Campo 2]: [tipo]
- [Campo 3]: [tipo]
- Relaciones: pertenece_a [Usuario]

**[Entidad Secundaria]**
- [Campo 1]: [tipo]
- Relaciones: pertenece_a [Entidad Principal]
```

**PUNTO DE CONTROL: Confirma características, flujo de usuario y modelo de datos antes de seleccionar herramientas.**

---

## Fase 3: Plan de Compilación

### Selección de Herramienta Sin Código

| Caso de Uso | Herramientas Recomendadas | Mejor Para |
|----------|------------------|----------|
| **Aplicación web con base de datos** | Bubble, Softr, Glide | Aplicaciones web completas |
| **Aplicación móvil** | Adalo, FlutterFlow, Glide | Experiencia móvil nativa |
| **Herramienta interna** | Retool, Notion, Airtable | Dashboards de equipo, paneles de admin |
| **Mercado** | Sharetribe, Bubble | Plataformas de dos lados |
| **Sitio de directorio o listado** | Softr + Airtable | Listados simples y búsqueda |
| **Flujo basado en formulario** | Tally + Airtable + Zapier | Recolección y procesamiento de datos |
| **Página de inicio con características de aplicación** | Carrd + Airtable + Zapier | MVP ligero |

### Stack de Herramienta Recomendado

```
## Stack de Herramientas para [Nombre de Aplicación]

**Frontend:** [Herramienta] — $[X]/mes
**Base de Datos:** [Herramienta] — $[X]/mes
**Autenticación:** [Incorporada / Auth0 / Firebase]
**Pagos:** Stripe — por transacción
**Automatización:** Zapier / Make — $[X]/mes
**Almacenamiento de archivos:** [Herramienta] — $[X]/mes
**Costo mensual total:** $[X]
```

### Cronograma de Compilación

| Semana | Hito | Entregable |
|------|-----------|-------------|
| 1 | Configuración y modelo de datos | Estructura de base de datos, autenticación de usuario, navegación básica |
| 2 | Característica principal 1 | Acción de usuario principal funcionando de extremo a extremo |
| 3 | Características principales 2-3 | Características restantes de MVP |
| 4 | Pulir y probar | Limpieza de UI, capacidad de respuesta móvil, correcciones de errores |
| 5 | Prueba beta | 5-10 usuarios probando la aplicación |
| 6 | Lanzamiento | Lanzamiento público con bucle de comentarios |

---

## Fase 4: Pulir

### 1. Prueba Previa al Lanzamiento

```
## Lista de Verificación de Prueba

- [ ] Todos los flujos de usuario funcionan de extremo a extremo (registrarse → acción principal → resultado)
- [ ] Los datos se guardan y se muestran correctamente
- [ ] La autenticación funciona (login, logout, restablecimiento de contraseña)
- [ ] Capacidad de respuesta móvil (prueba en teléfono y tableta)
- [ ] Casos extremos manejados (estados vacíos, errores, entradas largas)
- [ ] El procesamiento de pagos funciona con transacciones de prueba (si aplica)
- [ ] Tiempo de carga de página menor a 3 segundos
- [ ] 5 usuarios reales han probado y proporcionado comentarios
```

### 2. Consideraciones de Escalabilidad

- **Límites de usuario:** Verifica los límites de plan de la herramienta sin código (filas, usuarios, llamadas API)
- **Rendimiento:** Prueba con volumen de datos realista (100+ registros)
- **Copia de seguridad:** Exporta datos regularmente — nunca confíes solo en la plataforma sin código
- **Estrategia de salida:** ¿Puedes exportar tus datos si necesitas migrar más tarde?

### 3. Lista de Verificación de Calidad

```
## Lista de Verificación de Plan de Aplicación Sin Código

- [ ] Concepto de aplicación descrito en una oración
- [ ] Usuario objetivo y problema claramente definidos
- [ ] Características priorizadas en MVP vs. fases futuras
- [ ] Flujo de usuario principal mapeado pantalla por pantalla
- [ ] Modelo de datos definido con entidades y relaciones
- [ ] Herramientas sin código seleccionadas con estimaciones de costos
- [ ] Cronograma de compilación dividido en hitos semanales
- [ ] Lista de verificación de prueba preparada para previa al lanzamiento
- [ ] Se entienden los límites de escalabilidad de herramientas elegidas
- [ ] Plan de exportación y copia de seguridad de datos documentado
```

---

## Ejemplo

**Aplicación:** Rastreador de proyectos de cliente para freelancers
**Stack de herramientas:** Softr (frontend) + Airtable (base de datos) + Stripe (pagos)
**Costo mensual:** $49 (Softr Pro) + $20 (Airtable Plus) = $69/mes

**Flujo de usuario:**
```
Cliente recibe link → Ve dashboard del proyecto → Ve entregables y cronograma
Freelancer inicia sesión → Crea proyecto → Añade hitos → Rastrea tiempo → Genera factura
```

**Modelo de datos:**
- Clientes: nombre, email, empresa
- Proyectos: nombre, cliente (vinculado), estado, fecha_inicio, fecha_fin
- Hitos: proyecto (vinculado), nombre, fecha_vencimiento, estado
- Entradas de tiempo: proyecto (vinculado), fecha, horas, descripción

---

## Anti-Patrones

- **Construir sin un plan** — saltar al constructor y descubrirlo sobre la marcha crea código espagueti que es imposible de mantener.
- **Demasiadas características en v1** — el MVP debe hacer UNA cosa bien. Añade características después de confirmar que las personas usan la principal.
- **Ignorar modelo de datos** — la estructura de la base de datos es la fundación. Hacerlo mal significa reconstruir todo más tarde.
- **Elegir herramientas basadas en hype** — elige basado en tu caso de uso específico, no en lo que es tendencia en las redes sociales.
- **Sin plan de salida** — si tu plataforma sin código se cierra, ¿puedes obtener tus datos? Siempre verifica la portabilidad de datos.

---

## Recuperación

- **Golpea una limitación de herramienta a mitad de compilación:** Verifica si la limitación es un límite de plan (actualiza) o una limitación de plataforma (puede ser necesario cambiar herramientas). Cambiar herramientas es más fácil en semanas 1-2 que en semana 5.
- **La compilación toma más tiempo del planeado:** Corta características de v1. Envía la versión mínima viable y añade características en v2.
- **Los usuarios no entienden la aplicación:** La UX es demasiado compleja. Simplifica el flujo principal y añade una secuencia de tutorial u onboarding.
- **Necesitas código personalizado después de todo:** Muchas herramientas sin código permiten fragmentos de código personalizado. Úsalos para el 10% que sin código no puede manejar antes de reconstruir completamente.
