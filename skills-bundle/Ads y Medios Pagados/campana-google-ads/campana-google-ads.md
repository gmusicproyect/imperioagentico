---
name: campana-google-ads
description: "Planifica campañas de Google Ads con grupos de palabras clave, variaciones de ad copy, recomendaciones de landing page y estrategia de pujas. Úsalo cuando ejecutes publicidad en búsqueda pagada."
allowed-tools: Read Write Glob
metadata:
  author: Imperio Digital
  version: "1.0"
---

# Campaña de Google Ads

## Cuándo Usar Este Skill

Usa este skill cuando necesites:
- Planificar una campaña de Google Search Ads desde investigación de palabras clave hasta lanzamiento
- Organizar grupos de palabras clave en ad groups con ad copy coincidente
- Escribir ad copy que maximice quality score y click-through rate
- Diseñar una estrategia de pujas y presupuesto para búsqueda pagada rentable

**NO USES** este skill para Google Display ads, YouTube ads o SEO. Esto es específicamente para Google Search Ads (pago por clic).

---

## Principio Fundamental

LAS GANANCIAS DE GOOGLE ADS VIENEN DE LA ALINEACIÓN PALABRA CLAVE-AD-LANDING PAGE — CUANDO LA QUERY DE BÚSQUEDA, EL AD COPY Y LA PÁGINA TODOS DICEN LO MISMO, EL QUALITY SCORE SUBE Y EL COSTO POR CLIC BAJA.

---

## Fase 1: Brief de Campaña

### Inputs Requeridos

| Input | Qué Preguntar | Default |
|-------|---------------|---------|
| **Negocio/producto** | "¿Qué estás anunciando?" | Sin default — debe ser proporcionado |
| **Objetivo** | "¿Qué acción deben tomar? (comprar, llamar, registrarse, reservar)" | Sin default — debe ser proporcionado |
| **Presupuesto mensual** | "¿Cuál es tu presupuesto mensual de Google Ads?" | $500-1,000/mes |
| **Ubicación destino** | "¿Dónde están tus clientes?" | Estados Unidos |
| **Landing page(s)** | "¿Dónde envían los ads a la gente?" | Sin default — debe ser proporcionado |
| **Experiencia previa de Google Ads** | "¿Has ejecutado Google Ads antes? ¿Tienes datos?" | Ninguno |
| **Competidores** | "¿Quién más está pujando en tus palabras clave?" | Conciencia general |

**PUNTO DE CONTROL: Confirma el brief antes de construir la campaña.**

---

## Fase 2: Estrategia de Palabras Clave

### Organización de Palabras Clave

```
## Grupos de Palabras Clave

**Ad Group 1: [Tema — e.g., "Software de Email Marketing"]**
Palabras clave:
- [email marketing software] — Coincidencia exacta
- [best email marketing platform] — Coincidencia exacta
- "email marketing tool for small business" — Coincidencia de frase
- email marketing solution — Modificador de coincidencia amplia

CPC estimado: $[X]
Volumen de búsqueda mensual: [X]
Intención: Comercial (listo para comparar/comprar)

**Ad Group 2: [Tema — e.g., "Email Automation"]**
Palabras clave:
- [email automation tool] — Coincidencia exacta
- [automated email marketing] — Coincidencia exacta
...

**Palabras Clave Negativas (nivel de campaña):**
- free
- tutorial
- how to (a menos que apuntes a intención informativa)
- jobs
- salary
- [nombres de competidores] (a menos que dirijas targeting a competidores)
```

### Estrategia de Tipo de Coincidencia

```
## Reglas de Tipo de Coincidencia

**Coincidencia exacta [palabra clave]:** Mayor intención, mayor control, menor volumen
- Usa para: palabras clave comerciales principales
- Presupuesto: 60% del total

**Coincidencia de frase "palabra clave":** Control moderado, captura variaciones
- Usa para: palabras clave secundarias y frases más largas
- Presupuesto: 30% del total

**Coincidencia amplia palabra clave:** Mayor alcance, requiere pujas inteligentes
- Usa para: descubrimiento (con gestión inteligente de palabras clave negativas)
- Presupuesto: 10% del total (solo pruebas)
```

**PUNTO DE CONTROL: Aprueba grupos de palabras clave y tipos de coincidencia antes de escribir ads.**

---

## Fase 3: Escribe Ad Copy

### Responsive Search Ads (RSA)

Para cada ad group, escribe:
- 15 headlines (30 caracteres cada una)
- 4 descripciones (90 caracteres cada una)

### Estrategia de Headlines

```
## Headlines para Ad Group 1: [Tema]

**Enfocados en palabra clave (3-4):**
1. "Software de Email Marketing" (26 chars)
2. "Mejor Herramienta de Email Marketing" (27 chars)
3. "#1 Plataforma de Email Marketing" (29 chars)

**Enfocados en beneficio (3-4):**
4. "Envía Emails Que Convierten" (26 chars)
5. "Crece Tu Lista 3x Más Rápido" (26 chars)
6. "Ahorra 10 Horas Por Semana" (23 chars)

**Social proof (2-3):**
7. "Confiado por 50,000+ Usuarios" (26 chars)
8. "4.8 Estrellas en G2" (17 chars)

**Enfocados en CTA (2-3):**
9. "Comienza Tu Prueba Gratis Hoy" (29 chars)
10. "Prueba Gratis por 14 Días" (22 chars)

**Urgencia/oferta (2-3):**
11. "50% de Descuento Primeros 3 Meses" (24 chars)
12. "Precio Limitado de Lanzamiento" (27 chars)
```

### Estrategia de Descripciones

```
## Descripciones

1. "Comienza a enviar emails profesionales en minutos. Sin habilidades de diseño necesarias. Prueba gratis de 14 días." (90 chars)
2. "Únete a 50,000 empresas que usan [Brand] para crecer ingresos con email. Planes desde $29/mes." (87 chars)
3. "Editor de arrastrar y soltar, automatización, análisis. Todo lo que necesitas en una plataforma." (83 chars)
4. "Cancela cuando quieras. Sin contratos. Comienza a crecer tu negocio con email marketing hoy." (86 chars)
```

### Extensiones de Ad

```
## Extensiones a Configurar

**Extensiones de sitelink (4-6):**
- Precios / Planes
- Características
- Testimonios / Casos de Estudio
- Prueba Gratis
- Acerca de Nosotros

**Extensiones de callout (4-6):**
- Prueba Gratis Disponible
- Sin Tarjeta de Crédito Requerida
- Soporte 24/7
- Cancela En Cualquier Momento

**Fragmento estructurado:**
- Tipos: Plantillas, Automatización, Análisis, Integraciones, Reportes
```

---

## Fase 4: Pulido

### 1. Estrategia de Pujas

```
## Recomendación de Estrategia de Pujas

**Nuevas campañas (sin datos de conversión):**
- Comienza con CPC Manual o Maximizar Clics
- Establece pujas CPC máximo basadas en matemática de CPA objetivo
- CPA objetivo = [valor del cliente] × [margen de ganancia objetivo]

**Después de 30+ conversiones:**
- Cambia a Target CPA o Maximizar Conversiones
- Establece target CPA basado en datos de desempeño real

**Budget pacing:**
- Presupuesto diario = presupuesto mensual / 30.4
- Monitorea gasto diario vs. resultados
- Ajusta pujas semanalmente basándote en desempeño
```

### 2. Checklist de Alineación de Landing Page

- [ ] Headline coincide con tema de grupo de palabras clave
- [ ] CTA coincide con acción prometida en el ad
- [ ] Página carga en bajo 3 segundos
- [ ] Optimizada para móvil
- [ ] Formulario está above the fold (para lead gen)
- [ ] Número de teléfono visible (si objetivo es llamada)

### 3. Cronograma de Optimización

- Diario: verifica pacing de gasto, pausa perdedores obvios
- Semanal: revisa reporte de search terms, añade palabras clave negativas
- Bi-semanal: pausa palabras clave con bajo desempeño, ajusta pujas
- Mensual: revisión completa de desempeño, nuevas pruebas de ad copy, reasignación de presupuesto

---

## Anti-Patrones

- **Ejecutar toda coincidencia amplia sin negativas** — la coincidencia amplia gastará tu presupuesto en búsquedas irrelevantes sin gestión agresiva de palabras clave negativas.
- **Un ad group con 50 palabras clave** — palabras clave con diferente intención necesitan diferentes ads. Mantén 5-15 palabras clave estrechamente temáticas por ad group.
- **Enviar todos los ads a la homepage** — cada ad group debe vincular a la página de landing más relevante. La homepage raramente es la mejor opción.
- **Ignorar quality score** — quality scores bajos significan CPCs más altos. Mejora relevancia palabra clave-ad-landing page para bajar costos.
- **Establecer y olvidar** — Google Ads requiere optimización semanal. Las campañas abandonadas desperdician dinero.
- **Sin tracking de conversión** — sin tracking no puedes optimizar para lo que importa. Configura tracking de conversión antes de lanzar.

---

## Recuperación

- **Sin datos de conversión aún:** Comienza con Maximizar Clics para reunir datos. Cambia a pujas basadas en conversiones después de 30+ conversiones.
- **CPC alto comiendo el presupuesto:** Enfócate en palabras clave long-tail de coincidencia exacta con menor competencia. Añade más palabras clave negativas.
- **Quality score bajo (bajo 5):** Mejora relevancia de ad (coincide ad copy con palabras clave), experiencia de landing page, y CTR esperado.
- **Gastando presupuesto sin conversiones:** Verifica configuración de tracking de conversión. Luego revisa tasa de conversión de landing page. El problema a menudo es la página, no los ads.
- **Nicho muy competitivo:** Apunta a palabras clave long-tail, usa targeting geográfico para reducir competencia, y asegura que tu landing page convierte arriba del promedio.
