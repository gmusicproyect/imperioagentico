---
name: centro-ayuda-plataforma
description: "Estructura centros de ayuda de plataformas con secciones separadas para compradores/vendedores, tutoriales en video y escalación de contacto. Usa cuando construyas soporte de autoservicio para plataformas de mercado."
allowed-tools: Read Write Glob
metadata:
  author: Imperio Digital
  version: "1.0"
---

# Centro de Ayuda de Plataforma

## Cuándo Usar Este Skill

Usa este skill cuando necesites:
- Estructurar un centro de ayuda para un mercado con audiencias de compradores y vendedores
- Escribir artículos de ayuda que reduzcan el volumen de tickets de soporte
- Diseñar una ruta de escalación de contacto del autoservicio al soporte humano
- Organizar preguntas frecuentes, tutoriales y guías de solución de problemas por tipo de usuario

**NO** uses este skill para selección de software de base de conocimientos, diseño de chatbots o documentación interna. Esto es para la estructura y contenido del centro de ayuda de cara al público.

---

## Principio Fundamental

UN CENTRO DE AYUDA EXISTE PARA RESPONDER PREGUNTAS ANTES DE QUE SE CONVIERTAN EN TICKETS DE SOPORTE — CADA ARTÍCULO DEBE SER ENCONTRABLE EN MENOS DE 30 SEGUNDOS Y RESPONDER EN MENOS DE 2 MINUTOS.

---

## Fase 1: Resumen

### Información Requerida

| Entrada | Qué Preguntar | Predeterminado |
|---------|--------------|--------|
| **Tipo de plataforma** | "¿Qué conecta tu mercado?" | Sin predeterminado — debe proporcionarse |
| **Preguntas de soporte principales** | "¿Cuáles son las 10 preguntas más comunes de compradores y vendedores?" | Sin predeterminado — debe proporcionarse |
| **Volumen de soporte actual** | "¿Cuántos tickets de soporte por semana?" | Menos de 50 |
| **Canales de soporte** | "¿Cómo llegan los usuarios al soporte actualmente? ¿Correo, chat, teléfono?" | Solo correo electrónico |
| **Herramienta de centro de ayuda** | "¿Qué plataforma alojará el centro de ayuda?" | Notion, Zendesk o página independiente |

**PUNTO DE CONTROL: Confirma el resumen antes de estructurar el centro de ayuda.**

---

## Fase 2: Estructura

### Arquitectura de Información

```
Inicio del Centro de Ayuda
├── Para Compradores
│   ├── Comenzando
│   ├── Navegación y Búsqueda
│   ├── Realizar un Pedido
│   ├── Pagos y Reembolsos
│   ├── Reseñas y Calificaciones
│   └── Cuenta y Configuración
├── Para Vendedores
│   ├── Comenzando
│   ├── Crear Listados
│   ├── Gestionar Pedidos
│   ├── Pagos y Transferencias
│   ├── Reseñas y Calificaciones
│   └── Cuenta y Configuración
├── Confianza y Seguridad
│   ├── Nuestra Garantía
│   ├── Reportar un Problema
│   ├── Resolución de Disputas
│   └── Directrices de la Comunidad
└── Contáctanos
    ├── Enviar una Solicitud
    └── Chat en Vivo (si está disponible)
```

### Matriz de Prioridad de Artículos

Clasifica artículos por impacto:

| Prioridad | Criterios | Acción |
|----------|----------|--------|
| P1 | Top 10 preguntas por volumen de tickets | Escribir primero |
| P2 | Preguntas de incorporación y activación | Escribir segundo |
| P3 | Casos límite y temas avanzados | Escribir tercero |
| P4 | Contenido de referencia opcional | Escribir según sea necesario |

**PUNTO DE CONTROL: Confirma la estructura y lista de prioridades antes de escribir artículos.**

---

## Fase 3: Escribir

### Plantilla de Artículo

```
## [Título del Artículo — formulado como pregunta]

**Aplicable a:** Compradores / Vendedores / Ambos

[Respuesta de 1-2 frases a la pregunta — el resumen ejecutivo.]

### Paso a paso

1. [Paso con referencia específica de UI]
2. [Paso con referencia específica de UI]
3. [Paso con referencia específica de UI]

### Captura de Pantalla
[CAPTURA: descripción de qué capturar]

### Problemas Comunes
- **[Problema]:** [Solución]
- **[Problema]:** [Solución]

### ¿Aún necesitas ayuda?
[Contacta a nuestro equipo de soporte →](enlace)
```

### Reglas de Escritura

- **El título es una pregunta** — coincide con cómo piensan y buscan los usuarios ("¿Cómo obtengo un reembolso?" no "Política de Reembolso")
- **Respuesta primero, detalles después** — las primeras 1-2 frases deben responder directamente la pregunta
- **Formato paso a paso** — usa listas numeradas para procesos, viñetas para opciones
- **Referencias específicas de UI** — "Haz clic en el icono de engranaje en la esquina superior derecha" no "Ve a configuración"
- **Capturas de pantalla para cada proceso** — notas de marcador de posición si las capturas no están listas: `[CAPTURA: página de configuración con icono de engranaje marcado]`
- **Vincula a artículos relacionados** — al final, sugiere 2-3 artículos relacionados

### Tipos de Contenido

| Tipo | Cuándo Usar | Formato |
|------|-------------|--------|
| **Artículo instructivo** | Preguntas de proceso | Pasos numerados + capturas |
| **Guía de solución de problemas** | Preguntas "No funciona" | Problema → posibles causas → soluciones |
| **Entrada de FAQ** | Respuestas rápidas de hechos | Pregunta + respuesta de 1-3 frases |
| **Tutorial en video** | Procesos complejos de múltiples pasos | Screencast de 60-120 segundos |

---

## Fase 4: Pulir

### 1. Ruta de Escalación de Contacto

```
El usuario tiene una pregunta
    ↓
Buscar en el centro de ayuda (autoservicio)
    ↓
No se encontró respuesta → Sugerir artículos relacionados
    ↓
Aún sin respuesta → Formulario de contacto con selección de categoría
    ↓
Ticket creado → Respuesta automática con tiempo estimado de respuesta
    ↓
Soporte humano responde dentro de [X] horas
```

### 2. Métricas del Centro de Ayuda

```
## Métricas del Centro de Ayuda

- **Tasa de éxito de búsqueda:** % de búsquedas que resultan en un clic de artículo
- **Tasa de contacto:** % de visitantes del centro de ayuda que envían un ticket (más bajo = mejor)
- **Búsquedas principales sin resultados:** Palabras clave que buscan los usuarios sin resultados
- **Utilidad del artículo:** "¿Fue útil?" sí/no al final de cada artículo
- **Tasa de desviación de tickets:** % reducción en tickets después de la publicación del artículo
- **Tiempo de resolución:** Tiempo promedio para resolver tickets que se escalan más allá del autoservicio
```

### 3. Lista de Verificación de Calidad

```
## Lista de Verificación del Centro de Ayuda

- [ ] Secciones separadas para compradores y vendedores con navegación clara
- [ ] Las 10 preguntas principales (por volumen de tickets) tienen artículos dedicados
- [ ] Todos los títulos de artículos están formulados como preguntas
- [ ] Cada artículo responde la pregunta en las primeras 2 frases
- [ ] Los artículos paso a paso incluyen capturas (o marcadores de posición)
- [ ] La ruta de escalación de contacto es clara y accesible
- [ ] La funcionalidad de búsqueda funciona en todos los artículos
- [ ] La feedback "¿Fue útil?" está en cada artículo
- [ ] Artículos relacionados vinculados al final de cada página
- [ ] El enlace del centro de ayuda es accesible desde cada página de la plataforma
```

---

## Ejemplo

**Plataforma:** Mercado de servicios freelance

**Artículo del comprador:**
```
## ¿Cómo obtengo un reembolso?

Puedes solicitar un reembolso si el trabajo entregado no coincide con lo acordado en tu resumen del proyecto.

### Pasos para solicitar un reembolso

1. Ve a **Mis Pedidos** en tu panel
2. Haz clic en el pedido en cuestión
3. Haz clic en **Solicitar Reembolso** (disponible durante 14 días después de la entrega)
4. Selecciona tu razón y añade detalles
5. Haz clic en **Enviar** — el vendedor tiene 48 horas para responder

### Qué sucede después
- Si el vendedor acepta, tu reembolso se procesa dentro de 3-5 días hábiles
- Si el vendedor rechaza, nuestro equipo revisa el caso y decide dentro de 5 días hábiles

### ¿Aún necesitas ayuda?
[Contacta a soporte →](enlace) | Relacionado: [¿Cómo funciona la protección del comprador?](enlace)
```

---

## Anti-Patrones

- **Centro de ayuda único para ambos lados** — compradores y vendedores tienen preguntas diferentes y vocabulario diferente. Separa las secciones.
- **Artículos largos** — si un artículo tarda más de 2 minutos en leer, divídelo en múltiples artículos.
- **Sin función de búsqueda** — si los usuarios no pueden buscar, te escribirán al soporte. La búsqueda es obligatoria.
- **Ocultar la opción de contacto** — el autoservicio es el objetivo, pero ocultar el soporte humano frustra a los usuarios que genuinamente lo necesitan.
- **Contenido obsoleto** — capturas de pantalla e procesos desactualizados crean más confusión que ningún artículo. Revisa trimestralmente.

---

## Recuperación

- **Sin datos sobre preguntas comunes:** Revisa los últimos 50 correos de soporte. Agrupa por tema. Los 10 temas principales son tus primeros artículos.
- **Demasiados artículos necesarios a la vez:** Comienza con las 5 preguntas principales para cada lado (10 total). Añade 2-3 por semana.
- **Los usuarios aún contactan a soporte para preguntas que tienen artículos:** Los artículos son difíciles de encontrar o difíciles de entender. Mejora la búsqueda y reescribe usando lenguaje más simple.
- **El centro de ayuda no recibe tráfico:** Vincula desde correos transaccionales, tooltips en la aplicación y la respuesta automática de soporte. Hazlo visible en todas partes.
