---
name: configuracion-crm-inmobiliario
description: "Configura sistemas CRM inmobiliarios con etapas pipeline, puntuación leads y secuencias seguimiento automatizado."
allowed-tools: Read Write Glob
metadata:
  author: Imperio Digital
  version: "1.0"
---

# Configuración CRM Inmobiliario

## Cuándo Usar Este Skill

Usa este skill cuando necesites:
- Configurar o reestructurar CRM gestión leads inmobiliarios
- Definir etapas pipeline que coincidan viaje comprador y vendedor
- Crear criterios puntuación leads para priorizar esfuerzos seguimiento
- Diseñar secuencias automatizadas para diferentes tipos leads

**NO USES** este skill para selección software CRM, integraciones técnicas o configuración CRM general ventas. Esto es específicamente para configuración CRM inmobiliaria.

---

## Principio Fundamental

TU CRM ES SOLO TAN BUENO COMO TU PROCESO — LA MEJOR HERRAMIENTA DEL MUNDO FALLA SI TUS ETAPAS PIPELINE, SECUENCIAS SEGUIMIENTO Y PUNTUACIÓN LEADS NO COINCIDEN CÓMO TRANSACCIONES INMOBILIARIAS REALMENTE OCURREN.

---

## Fase 1: Requisitos CRM

### Entradas Requeridas

| Entrada | Qué Preguntar | Predeterminado |
|-------|------------|---------|
| **Plataforma CRM** | "¿Qué CRM — Follow Up Boss, KVCore, LionDesk, otro?" | Follow Up Boss |
| **Modelo negocio** | "¿Agente solo, equipo o correduría?" | Agente solo |
| **Fuentes leads** | "¿Dónde vienen leads — Zillow, sitio web, referrals, redes sociales, casas abiertas?" | Mixta — referrals, Zillow, sitio web |
| **Volumen leads mensual** | "¿Cuántos leads nuevos mes?" | 20-50 |
| **Punto dolor actual** | "¿Qué no funciona en proceso seguimiento actual?" | Leads cayendo a través grietas |

**PUNTO DE CONTROL:** Confirma plataforma y fuentes leads antes diseñar sistema.

---

## Fase 2: Diseño Pipeline

### Etapas Pipeline Comprador

```
## Pipeline Comprador

| Etapa | Definición | Acción Requerida |
|-------|-----------|----------------|
| Lead Nuevo | Acaba entrar sistema — sin contacto aún | Haz primer contacto dentro 5 minutos |
| Contactado | Conversación inicial completada | Califica: cronograma, presupuesto, pre-aprobación |
| Calificando | Recopilando requisitos, evaluando preparación | Programa consulta comprador |
| Comprador Activo | Pre-aprobado, buscando activamente | Configura alertas propiedad, programa visualizaciones |
| Visualizando | Visitando propiedades activamente | Seguimiento después cada visualización |
| Oferta Enviada | Oferta escrita y presentada | Monitorea negociaciones, actualiza cliente |
| Bajo Contrato | Oferta aceptada, en escrow | Gestiona inspección, tasación, tareas cierre |
| Cerrado | Transacción completada | Mueve cliente pasado a pipeline nutrición |
| Perdido / Inactivo | No responsivo o eligió agente otro | Agrega secuencia nutrición largo plazo |
```

### Etapas Pipeline Vendedor

```
## Pipeline Vendedor

| Etapa | Definición | Acción Requerida |
|-------|-----------|----------------|
| Lead Nuevo | Consulta vendedor recibida | Haz primer contacto dentro 5 minutos |
| Contactado | Conversación inicial completada | Programa cita listado |
| Cita Listado | Reunión agendada | Prepara CMA y presentación listado |
| Pre-Listado | Preparando listar — staging, fotos, precios | Coordina tareas prep listado |
| Listado Activo | Propiedad mercado | Actualizaciones semanales vendedor, feedback visualización |
| Bajo Contrato | Oferta aceptada, en escrow | Gestiona contingencias y proceso cierre |
| Cerrado | Transacción completada | Mueve cliente pasado a pipeline nutrición |
| Perdido / Inactivo | No listó o eligió agente otro | Agrega secuencia nutrición largo plazo |
```

---

## Fase 3: Puntuación Leads

### Modelo Puntuación Leads

```
## Modelo Puntuación Leads

### Puntuación Cronograma (0-30 puntos)
| Cronograma | Puntos |
|----------|--------|
| Comprando/vendiendo dentro 30 días | 30 |
| Dentro 1-3 meses | 20 |
| Dentro 3-6 meses | 10 |
| 6+ meses o "solo viendo" | 5 |

### Preparación Financiera (0-30 puntos)
| Estado | Puntos |
|--------|--------|
| Pre-aprobado / equity hogar disponible | 30 |
| Hablé lender, no aprobado aún | 15 |
| No contactado lender | 5 |

### Nivel Engagement (0-20 puntos)
| Comportamiento | Puntos |
|----------|--------|
| Respondió seguimiento dentro 24 horas | 10 |
| Asistió visualización o reunión | 10 |
| Abrió emails no respuesta | 3 |
| Sin engagement | 0 |

### Calidad Fuente Lead (0-20 puntos)
| Fuente | Puntos |
|--------|--------|
| Referral personal | 20 |
| Cliente pasado | 20 |
| Consulta sitio web directo | 15 |
| Registro casa abierta | 10 |
| Lead portal Zillow | 5 |
| Lista leads comprados | 3 |

### Niveles Prioridad
| Puntuación | Prioridad | Cadencia Seguimiento |
|-------|----------|------------------|
| 70-100 | Caliente | Contacto diario |
| 40-69 | Tibio | 2-3x semana |
| 20-39 | Nutrición | Semanal |
| 0-19 | Largo plazo | Drip mensual |
```

---

## Fase 4: Secuencias Automatizadas

### Secuencia Respuesta Lead Nuevo

```
## Lead Nuevo — Primeros 7 Días

**Minuto 1:** Auto-texto: "Hola [Nombre], soy [Tu nombre] con [Compañía].
Vi tu interés [propiedad/área]. ¿Cuándo bueno para charlar?"

**Minuto 5:** Intento llamada #1

**Hora 1 (sin respuesta):** Email: Introducción + propuesta valor + CTA

**Día 1 (tarde):** Intento llamada #2

**Día 2:** Texto: "Hola [Nombre], siguiendo. ¿Buscas comprar/vender
[área]? Me encantaría ayudar."

**Día 3:** Intento llamada #3

**Día 5:** Email: Actualización mercado área interés + CTA

**Día 7:** Texto: Alcance final — "No quiero ser molesto, pero estoy
aquí cuando estés listo. Guarda mi número."

**Después Día 7:** Mueve secuencia nutrición sin respuesta.
```

---

## Anti-Patrones

- **Demasiadas etapas pipeline** — complejidad mata adopción. Mantén bajo 10 etapas por pipeline.
- **Sin proceso velocidad-a-lead** — responder leads horas después de minutos dramáticamente reduce conversión.
- **Set it and forget it** — automatización maneja primer toque, pero conversión requiere seguimiento personal.
- **Sin rastreo fuentes leads** — sin rastreo fuente, no puedes calcular ROI gasto marketing.
- **Over-complicar puntuación leads** — comienza simple y refina. Sistema básico caliente/tibio/frío supera modelo 100-puntos no usado.

---

## Recuperación

- **CRM datos desordenados:** Deduplica contactos, actualiza etapas pipeline, tagea todos leads por fuente. Programa limpieza trimestral.
- **Equipo no usa CRM:** Simplifica proceso, demuestra ROI, haz uso CRM no negociable para asignaciones leads.
- **Bajas tasas respuesta secuencias automatizadas:** Prueba mensajería diferente, tiempo, canales. Personaliza primer toque.
- **Demasiados leads seguimiento:** Usa puntuación leads priorizar. Enfócate esfuerzo diario caliente, automatiza nutrición resto.
- **Cambiar plataformas CRM:** Exporta todos contactos con tags y notas. Mapea etapas pipeline viejas a nuevas. Reconstruye secuencias automatización.
