---
name: optimizador-meta-tags
description: Optimiza title tags y meta descripciones para un lote de páginas con conteos de caracteres y optimización de CTR. Usa cuando mejores la apariencia de tu sitio en búsquedas.
allowed-tools: Read Write Glob
author: Imperio Digital
version: "1.0"
---

# Optimizador de Meta Tags

## Cuándo Usar Este Skill

Usa este skill cuando necesites:
- Optimizar title tags y meta descripciones en múltiples páginas
- Mejorar tasas de clics desde páginas de resultados de motores de búsqueda
- Auditar meta tags existentes por longitud, inclusión de palabras clave y efectividad
- Escribir meta tags por lotes para páginas nuevas o poco optimizadas

**NO** uses este skill para optimización de contenido en página, auditorías de SEO técnico o schema markup. Esto es específicamente para title tags y meta descripciones.

---

## Principio Fundamental

LOS TITLE TAGS Y META DESCRIPCIONES SON TU COPY DE ANUNCIO EN RESULTADOS DE BÚSQUEDA — DEBEN INCLUIR LA PALABRA CLAVE OBJETIVO, CABER EN LOS LÍMITES DE CARACTERES Y HACER QUE LOS BUSCADORES ELIJAN TU RESULTADO SOBRE LOS OTROS.

---

## Fase 1: Briefing

### Información Requerida

| Input | Qué Preguntar | Por Defecto |
|-------|------------|---------|
| **Páginas a optimizar** | "Lista las páginas (URLs o títulos) que necesitan optimización de meta tags." | Sin defecto — debe proporcionarse |
| **Palabras clave objetivo** | "¿Qué palabra clave debería apuntar cada página?" | Sin defecto — debe proporcionarse |
| **Nombre de marca** | "¿Cuál es tu nombre de marca para formateo de title tag?" | Nombre de negocio |
| **Preferencia de formato de título** | "¿Añades tu nombre de marca a los title tags?" | Sí — "Título de Página | Nombre de Marca" |
| **Meta tags actuales** | "¿Puedes compartir los title tags y meta descripciones existentes?" | Auditaremos si se proporcionan URLs |

**PUNTO DE CONTROL: Confirma la lista de páginas y palabras clave antes de optimizar.**

---

## Fase 2: Auditoría de Meta Tags

### Evaluación del Estado Actual

Para cada página, evalúa:

```
## Auditoría de Meta Tags

| Página | Title Actual | Caracteres | Descripción Actual | Caracteres | Problemas |
|------|--------------|-------|--------------------|----|--------|
| [Página 1] | [Título] | [X] | [Descripción] | [X] | [Problemas] |
```

### Problemas Comunes a Señalar

- Título sobre 60 caracteres (se trunca)
- Título bajo 30 caracteres (pierde potencial de ranking)
- Meta descripción sobre 160 caracteres (se trunca)
- Meta descripción bajo 120 caracteres (desperdicia espacio de SERP)
- Palabra clave objetivo faltante en título
- Palabra clave objetivo faltante en descripción
- Títulos duplicados en múltiples páginas
- Descripciones genéricas ("Bienvenido a nuestro sitio web")
- Sin CTA o beneficio en descripción

**PUNTO DE CONTROL: Presenta la auditoría antes de escribir versiones optimizadas.**

---

## Fase 3: Escribir Meta Tags Optimizados

### Reglas de Title Tag

- **Longitud:** 50-60 caracteres (límite duro: 60 para evitar truncamiento)
- **Ubicación de palabra clave:** Palabra clave objetivo lo más cerca del principio posible
- **Nombre de marca:** Añade al final con separador de tubería (| Marca)
- **Formato:** [Frase de Palabra Clave Primaria] — [Beneficio o Modificador] | Marca
- **Unicidad:** Cada página obtiene un title tag único

### Reglas de Meta Descripción

- **Longitud:** 150-160 caracteres (límite duro: 160)
- **Inclusión de palabra clave:** Palabra clave objetivo aparece naturalmente (Google la resalta)
- **Estructura:** [Hook/beneficio] + [Lo que cubre la página] + [CTA o propuesta de valor]
- **Palabras de acción:** Usa "Aprende," "Descubre," "Obtén," "Encuentra" — no lenguaje pasivo
- **Sin comillas o caracteres especiales** que podrían causar truncamiento

### Formato de Output

```
## Meta Tags Optimizados

### Página: [Nombre de Página/URL]
**Palabra clave objetivo:** [palabra clave]

**Title tag (XX caracteres):**
[Título tag optimizado aquí]

**Meta descripción (XXX caracteres):**
[Meta descripción optimizada aquí]

**Notas:** [Cualquier recomendación específica]
```

---

## Fase 4: Pulir

### 1. Lista de Verificación de Implementación

- [ ] Todos los title tags bajo 60 caracteres
- [ ] Todas las meta descripciones entre 150-160 caracteres
- [ ] Cada página tiene un título y descripción únicos
- [ ] Palabra clave objetivo presente en cada título
- [ ] Palabra clave objetivo presente en cada descripción
- [ ] Sin meta tags duplicados en el sitio
- [ ] Nombre de marca consistentemente formateado

### 2. Consejos de Optimización de CTR

- Usa números cuando sea posible ("7 Formas de..." o "Ahorrar $500")
- Usa año actual para contenido sensible al tiempo ("Guía 2026")
- Prueba adiciones entre paréntesis: (Plantilla Gratuita) (Paso a Paso) (Con Ejemplos)
- Analiza datos de CTR de Search Console mensualmente — impresiones altas + bajo CTR = reescribe los meta tags

### 3. Proceso Continuo

- Revisa meta tags para las top 20 páginas mensualmente
- Actualiza title tags cuando cambian objetivos
- Refresca descripciones estacionalmente o cuando cambian ofertas
- Verifica Google Search Console para páginas con altas impresiones pero bajo CTR

---

## Anti-Patrones

- **Keyword stuffing en títulos** — "Marketing por Email Email Herramientas Email Software" es ilegible y daña rankings.
- **Misma meta descripción en cada página** — descripciones duplicadas son tratadas como descripciones faltantes por Google.
- **Escribir para motores de búsqueda, no humanos** — la meta descripción debe hacer que un humano quiera hacer clic, no solo contener palabras clave.
- **Ignorar truncamiento móvil** — SERPs móviles muestran menos caracteres. Coloca las palabras más importantes al frente.
- **Establecer y olvidar** — los meta tags deberían ser revisados y actualizados mientras las estrategias de palabras clave evolucionan.

---

## Recuperación

- **Cientos de páginas a optimizar:** Prioriza por tráfico e impresiones. Comienza con las top 20 páginas en Google Search Console.
- **Sin palabras clave objetivo definidas:** Ejecuta primero investigación de palabras clave. Cada página necesita una palabra clave primaria antes de que los meta tags puedan optimizarse.
- **Google reescribe tus meta tags:** Google a veces genera sus propios snippets. Asegúrate de que tus tags reflejen precisamente el contenido de la página — esto reduce reescrituras.
- **CMS no soporta meta tags personalizados:** Recomienda Yoast SEO (WordPress) u plugins similares que añaden campos de meta tags a cada página.
