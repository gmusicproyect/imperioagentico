# Bono: Meta Ads 2.0 — Matías y el MCP Oficial de Meta (97 Herramientas + Higgsfield)

> *"Le pagaba \$2.000 al mes a un media buyer. Caro Guzmán le pagaba \$1.500 a una agencia que entraba a su cuenta dos veces por semana. Hoy ambos corremos nuestras propias campañas desde la terminal con costos por lead récord (\$0.10 - \$0.20 USD). Meta Ads 2.0 reemplaza el método manual 1.0 (que requería crear apps en developers.facebook.com y tokens temporales con riesgo de restricción de cuentas) gracias al nuevo **MCP Oficial lanzado y aprobado por Meta**."*

---

## 🏗️ La Arquitectura de 3 Piezas: Cerebro, Manos y Fábrica

El 95% de los usuarios comete el error de conectar el MCP únicamente para pedir un reporte de métricas y abandonar la sesión. Eso es solo la punta del iceberg. Un sistema de Paid Media agéntico de alto rendimiento se compone de tres capas articuladas:

```
┌───────────────────────────────────────────────────────────┐
│                     1. EL CEREBRO                         │
│                      Claude Code                          │
│   • Conoce tu negocio, tu audiencia y tu línea editorial  │
│   • Registra en CLAUDE.md qué ángulos ya se quemaron      │
│   • Define presupuestos y toma decisiones estratégicas    │
└─────────────────────────────┬─────────────────────────────┘
                              │
              ┌───────────────┴───────────────┐
              ▼                               ▼
┌───────────────────────────┐   ┌───────────────────────────┐
│        2. LAS MANOS       │   │        3. LA FÁBRICA      │
│     Meta Ads MCP Oficial  │   │       Higgsfield MCP      │
│   • 97 herramientas en vivo│   │   • Generación de imágenes│
│   • Crea, pausa y edita   │   │     1:1 ultra-personalizadas│
│   • Modifica presupuestos │   │   • Variaciones por país  │
│   • Audita y mata lo malo │   │   • Video cinematográfico │
└───────────────────────────┘   └───────────────────────────┘
```

> **La regla de oro:** Con una pieza tienes un chatbot. Con dos, un asistente. Con las tres, **una fábrica autónoma de marketing**.

---

## 🎛️ Las 97 Herramientas del MCP Oficial (Agrupadas en 8 Familias)

El servidor MCP oficial de Meta expone 97 funciones operativas agrupadas en 8 áreas de gestión:

| Familia | Capacidades operativas del agente |
|---------|-----------------------------------|
| **1. Cuentas y Páginas** | Lectura de cuentas publicitarias, páginas de Facebook e Instagram vinculadas. |
| **2. Reportes e Insights** | Análisis granular de CPA, CPC, ROAS, impresiones y desglose por país/edad. |
| **3. Creación de Anuncios** | Creación completa de campañas CBO/ABO, adsets, creativos y anuncios. |
| **4. Gestión y Control** | Activar, pausar, editar presupuestos diarios y matar adsets ineficientes. |
| **5. Audiencias** | Creación y administración de públicos personalizados y lookalikes. |
| **6. Experimentos** | Configuración de tests A/B automáticos y comparativas estadísticas. |
| **7. Píxel y Catálogo** | Monitoreo de eventos del píxel de conversión y catálogos de e-commerce. |
| **8. Ads Library** | Espionaje de anuncios activos de cualquier competidor en la biblioteca de Meta. |

---

## 🚀 Setup en 3 Pasos (Sin Apps de Facebook ni Tokens a Mano)

Ya no es necesario ingresar a `developers.facebook.com` ni redactar políticas de privacidad para evitar restricciones de cuenta.

### Paso 1 — Conectar el MCP Oficial en Claude Code
1. Abre Claude Code y ve a: **Configuración** → **Conectores** → **Agregar conector personalizado**.
2. Asigna el nombre: `metaads`.
3. Pega la URL oficial del MCP de Meta. *(Cuidado: no utilices repositorios comunitarios de terceros en GitHub; asegúrate de conectar el servidor oficial de Meta).*
4. Cierra Claude Code por completo (**Cmd+Q** en Mac o cerrar la ventana en Windows) y vuelve a abrirlo para inicializar los conectores.

### Paso 2 — Configurar los Permisos de Seguridad
Dentro de la configuración del conector `metaads`, calibra la autonomía del agente:
- **Herramientas de lectura y análisis:** `Permitir siempre`.
- **Creación de ads y campañas:** `Permitir siempre`.
- **Eliminación y destrucción de campañas:** `Requiere aprobación` *(nunca otorgues borrado automático)*.

### Paso 3 — Verificar la Conexión
Envía este prompt de diagnóstico inicial:
```
Te conecté a Meta MCP. Verifica tu conexión y dime cuánto está mi costo por lead hoy en la campaña de signups.
```
Compara el valor reportado por Claude contra tu Ads Manager. Si coinciden con precisión, el agente está calibrado.

---

## ⚡ El One Prompt Setup: Campaña Multipaís con Modismos Locales

Este prompt coordina el **Cerebro** (Claude Code), las **Manos** (Meta MCP) y la **Fábrica** (Higgsfield MCP) para lanzar una campaña completa:

```markdown
Revisa mis mejores países por CPA de los últimos 60 días.

Con los 5 mejores arma una campaña de conversión para {TU OFERTA},
un conjunto de anuncios por país, con el copy en español nativo de cada mercado.

Genera 5 imágenes para estos anuncios mediante Higgsfield MCP, una por país,
mismo concepto visual, con el texto en pantalla adaptado al modismo local:
- Chile: español chileno (ej. "cachái", "no sigáis solo")
- México: modismos locales (ej. "no manches", "órale")
- Argentina: modismos locales (ej. "che", "posta")
- Colombia: expresiones colombianas (ej. "parce", "hágale pues")
- Ecuador: modismos locales (ej. "pana")

Presupuesto: {X} USD al día total (CBO). Formato de imágenes: 1:1.

Cuando lo tengas listo, muéstrame los gráficos finales, te los apruebo
y recién ahí subes la estructura a la cuenta.
REGLA OBLIGATORIA: Deja la campaña y todos los adsets en estado APAGADO (paused).
```

---

## 🕵️ Espionaje de Competencia (Meta Ads Library + Browser)

El agente puede auditar a tus principales competidores en vivo mediante el MCP de Meta y navegación web:
1. Inspecciona cientos de anuncios activos de marcas de referencia (ej. Alex Hormozi / Vantage).
2. Agrupa los anuncios por patrones de gancho (*urgencia, confrontación, antiventa, fundador como cuello de botella*).
3. Entrega una **auditoría ejecutiva en HTML interactivo** desglosando los 3 mejores ángulos para modelar en tu oferta semanal.

---

## ⚠️ La Limitación que te Ahorra una Tarde

> [!WARNING]
> **El MCP oficial de Meta aún no permite subir archivos de video directamente.**
> Puede subir imágenes sin restricciones y puede editar videos que ya hayan sido subidos previamente en tu biblioteca de anuncios, pero la carga de archivos de video nuevos debe realizarse de forma manual en el Ads Manager.

---

## 📁 Apéndice: Método Legacy 1.0 (Node.js Direct API)

Para entornos donde no se disponga de la interfaz de conectores MCP, el proyecto conserva la suite CLI nativa en Node.js ESM (`src/api.js`, `src/campaigns.js`, `src/cli.js`) conectada mediante token de Graph API v21.0. Ambos métodos conviven, siendo el MCP 2.0 el estándar recomendado por velocidad y seguridad.
