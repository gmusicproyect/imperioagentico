---
name: rastreador-gastos
description: "Crea un sistema de seguimiento y categorización de gastos en Notion con registros de transacciones, desglose de categorías, resúmenes mensuales y marcado de deducciones fiscales para freelancers y pequeños negocios. Úsalo cuando necesites rastrear gastos empresariales, reemplazar sistemas de contabilidad basados en hojas de cálculo u organizar recibos y transacciones para la declaración fiscal."
allowed-tools: Read Write Glob mcp__claude_ai_Notion__notion-create-database mcp__claude_ai_Notion__notion-create-pages mcp__claude_ai_Notion__notion-search mcp__claude_ai_Notion__notion-fetch
metadata:
  author: Imperio Digital
  version: "1.0"
---

# Rastreador de Gastos

## Cuándo usar esta habilidad

Usa esta habilidad cuando necesites:
- Construir una base de datos de rastreo de gastos empresariales en Notion desde cero
- Reemplazar una hoja de cálculo, caja de recibos o sistema mental para rastrear gastos
- Categorizar gastos por categorías del Anexo C del IRS para preparación fiscal
- Marcar compras deducibles fiscales para no perder nada al final del año
- Importar transacciones existentes desde una exportación de extracto bancario, CSV o lista manual

**NO** uses esta habilidad para:
- Presupuestos personales o rastreo de gastos domésticos (esto es para gastos empresariales)
- Facturación o cuentas por cobrar (usa una habilidad de plantilla de factura en su lugar)
- Procesamiento de nómina o presentación de impuestos (requiere software dedicado y profesionales)
- Contabilidad completa de doble entrada o plan de cuentas (usa QuickBooks o Wave)

---

## Referencia Rápida: Características del Rastreador de Gastos

| Característica | Detalles |
|---------|---------|
| Propiedades | 12 campos por registro de gasto |
| Categorías de gastos | 15 categorías alineadas con el Anexo C del IRS |
| Métodos de pago | 6 opciones (Efectivo, Tarjeta de Crédito, Débito, Transferencia Bancaria, PayPal, Otro) |
| Marcas de deducción fiscal | Completa, Parcial, Ninguna, Verificar |
| Vistas de base de datos | 5 vistas preconfiguradas filtradas |
| Seeding | Importación masiva desde CSV, extracto bancario o lista manual |

## Referencia Rápida: Esquema de Base de Datos

| Propiedad | Tipo | Propósito | Predeterminado |
|----------|------|---------|---------|
| Nombre de Gasto | Título | Descripción corta de la compra | Requerido |
| Fecha | Fecha | Fecha de la transacción | Requerido |
| Monto | Número (USD) | Cantidad total gastada | Requerido |
| Categoría | Seleccionar | Clasificación del Anexo C del IRS | Ver tabla de categorías |
| Vendedor | Texto enriquecido | Negocio o persona pagada | Vacío |
| Método de Pago | Seleccionar | Cómo se pagó el gasto | Tarjeta de Crédito |
| Deducible Fiscal | Seleccionar | Calificación de deducción | Verificar |
| Recibo | URL | Enlace a imagen de recibo o archivo | Vacío |
| Notas | Texto enriquecido | Contexto, propósito o asociación con cliente | Vacío |
| Cliente/Proyecto | Texto enriquecido | Cliente o proyecto relacionado | Vacío |
| Recurrente | Casilla de verificación | Gasto mensual recurrente | false |
| Etiquetas | Multi-seleccionar | Etiquetas para filtrado | Ver abajo |

### Métodos de Pago

Tarjeta de Crédito, Débito, Efectivo, Transferencia Bancaria, PayPal, Otro

### Etiquetas Predeterminadas

`mensual`, `trimestral`, `anual`, `facturable-cliente`, `reembolsable`, `recibo-pendiente`, `compra-grande`, `suscripción`, `una-sola-vez`

---

## Referencia Rápida: Categorías de Gastos (Alineadas con el Anexo C del IRS)

ESTAS CATEGORÍAS SON SOLO PARA PROPÓSITOS DE SEGUIMIENTO. CONSULTA A UN PROFESIONAL FISCAL PARA LA ELEGIBILIDAD DE DEDUCCIÓN Y CUMPLIMIENTO.

| Categoría | Deducibilidad Típica | Ejemplos |
|----------|----------------------|----------|
| Publicidad | Completa | Google Ads, Facebook Ads, tarjetas de negocio, publicaciones patrocinadas |
| Auto & Transporte | Parcial (solo % comercial) | Gasolina, mantenimiento, peajes, estacionamiento para viajes comerciales |
| Contratistas | Completa (1099 sobre $600) | Diseñadores freelance, asistentes virtuales, subcontratistas |
| Educación | Completa | Cursos en línea, certificaciones, talleres, libros |
| Seguro | Completa | Responsabilidad, E&O, salud (autoempleado), equipo |
| Legal & Profesional | Completa | Honorarios de CPA, consulta legal, coaching empresarial |
| Comidas | Parcial (50%) | Almuerzos con clientes, comidas durante viajes de negocio |
| Gastos de Oficina | Completa | Tinta de impresora, papel, suministros de limpieza, café para oficina |
| Renta & Arrendamiento | Completa | Espacio de coworking, arrendamiento de oficina, alquiler de equipo |
| Software & Suscripciones | Completa | Adobe Creative Cloud, Notion, Slack, Zoom, hosting |
| Suministros | Completa | Materiales de empaque, materias primas, suministros de inventario |
| Impuestos & Licencias | Completa | Licencia comercial, registro estatal, cuotas profesionales |
| Viajes | Completa | Vuelos, hoteles, autos de alquiler, transporte compartido para viajes de negocio |
| Servicios | Parcial (% comercial) | Internet, plan telefónico, electricidad (porción home office) |
| Otro | Varía | Cuotas bancarias, franqueo, costos misceláneos empresariales |

### Marcas de Deducción Fiscal

| Marca | Significado | Acción |
|------|---------|--------|
| Completa | 100% deducible | No se necesita ajuste al momento de impuestos |
| Parcial | Solo un porcentaje es deducible | Registra el % de uso comercial en Notas |
| Ninguna | No deducible | No incluyas en el Anexo C |
| Verificar | Incierto | Marca para revisión con tu contador |

**PREDETERMINADO: Establece Deducible Fiscal a "Verificar" cuando la deducibilidad no es obvia.** Deja que el contador del usuario tome la decisión final.

---

## Workflow Central

TODO RASTREADOR DE GASTOS COMIENZA RECOPILANDO DETALLES EMPRESARIALES Y CREANDO LA BASE DE DATOS CON EL ESQUEMA COMPLETO ANTES DE AGREGAR CUALQUIER TRANSACCIÓN -- NUNCA AGREGUES PÁGINAS A UNA BASE DE DATOS QUE FALTAN PROPIEDADES.

### Paso 1: Recopila Requisitos

1. **Tipo de negocio** -- propietario único, LLC, S-corp, sociedad
2. **Página padre de Notion** -- dónde debe vivir la base de datos de gastos
3. **Año fiscal** -- año calendario (ene-dic) o año fiscal personalizado
4. **Moneda** -- predeterminado USD; confirma o cambia
5. **Categorías personalizadas** -- cualquier adición a los 15 predeterminados
6. **Gastos existentes** -- transacciones para importar (CSV, lista o dictadas)
7. **Situación fiscal** -- cualquier regla de deducción conocida o preferencia del contador

Si el usuario proporciona solo los artículos 1 y 2, procede con todos los predeterminados.

**Plantilla breve para solicitudes vagas:**

```
Construiré tu rastreador de gastos en Notion. Respuestas rápidas necesarias:

1. ¿Qué tipo de entidad empresarial? (propietario único, LLC, S-corp)
2. ¿Cuál página de Notion debería crear el rastreador bajo?
3. ¿Año fiscal? (predeterminado: Enero - Diciembre)
4. ¿Moneda? (predeterminado: USD)
5. ¿Alguna categoría de gasto más allá de los 15 predeterminados?
6. ¿Tienes gastos existentes para importar?
```

### Paso 2: Localiza la Página Padre en Notion

1. Llama a `notion-search` con el nombre de página o palabras clave que el usuario proporcionó
2. Confirma el ID de página con el usuario si existen múltiples coincidencias

**SI LA PÁGINA NO SE ENCUENTRA:** Pide título exacto o URL, reintenta con palabras clave más cortas. **Después de 3 búsquedas fallidas, detente:** "No puedo encontrar esa página. Verifica Configuración > Conexiones en Notion y confirma que la integración tiene acceso."

### Paso 3: Crea la Base de Datos en Notion

1. Llama a `notion-create-database` con el ID de página padre y esquema completo:

**Título de base de datos:** `Gastos Empresariales`

**Propiedades para crear:**

```
Nombre de Gasto        -> título
Fecha                  -> fecha
Monto                  -> número (formato: dólar)
Categoría              -> seleccionar
  opciones: Publicidad (azul), Auto & Transporte (marrón), Contratistas (púrpura),
            Educación (rosa), Seguro (naranja), Legal & Profesional (amarillo),
            Comidas (rojo), Gastos de Oficina (gris), Renta & Arrendamiento (verde),
            Software & Suscripciones (azul), Suministros (naranja),
            Impuestos & Licencias (amarillo), Viajes (rosa), Servicios (gris),
            Otro (predeterminado)
Vendedor               -> texto_enriquecido
Método de Pago         -> seleccionar
  opciones: Tarjeta de Crédito (azul), Débito (verde), Efectivo (amarillo),
            Transferencia Bancaria (púrpura), PayPal (naranja), Otro (gris)
Deducible Fiscal       -> seleccionar
  opciones: Completa (verde), Parcial (amarillo), Ninguna (rojo), Verificar (gris)
Recibo                 -> url
Notas                  -> texto_enriquecido
Cliente/Proyecto       -> texto_enriquecido
Recurrente             -> casilla de verificación
Etiquetas              -> multi_seleccionar
  opciones: mensual (azul), trimestral (púrpura), anual (naranja),
            facturable-cliente (verde), reembolsable (rosa),
            recibo-pendiente (rojo), compra-grande (amarillo),
            suscripción (marrón), una-sola-vez (gris)
```

2. Verifica con `notion-fetch` en el ID de base de datos devuelto
3. Confirma la creación con un resumen de todas las propiedades configuradas

**SI LA CREACIÓN DE BASE DE DATOS FALLA:** Verifica el ID de página padre con `notion-fetch`, reintenta una vez. **Si falla de nuevo:** "Por favor ve a la página padre > menú de tres puntos > Conexiones y asegúrate que la integración tiene acceso 'Puede editar'."

### Paso 4: Sembrar con Gastos Existentes

**OMITE ESTE PASO si el usuario no tiene gastos existentes para importar.**

1. Analiza los datos de gastos del usuario (CSV, extracto bancario, lista de viñetas o lenguaje natural)
2. Mapea cada gasto al esquema:
   - **Nombre de Gasto** -- corto, descriptivo (p. ej., "Adobe Creative Cloud - Enero")
   - **Fecha** -- fecha de transacción de los datos
   - **Monto** -- cantidad en dólares; **NUNCA adivines montos**
   - **Categoría** -- coincide con la categoría del IRS más cercana
   - **Vendedor** -- extrae el nombre del negocio
   - **Método de Pago** -- infiere del contexto, predeterminado a "Tarjeta de Crédito"
   - **Deducible Fiscal** -- establece desde reglas de categoría; predeterminado "Verificar" cuando es incierto
   - **Recurrente** -- marca verdadero para suscripciones y servicios mensuales
   - **Etiquetas** -- infiere del contexto (p. ej., suscripción = `mensual` + `suscripción`)

3. Llama a `notion-create-pages` para agregar gastos en lotes
4. Reporta resultados de siembra con desglose de categoría y totales

**SI LOS DATOS DE GASTOS SON AMBIGUOS:** Presenta la interpretación antes de crear páginas. **SI LA CREACIÓN EN LOTE FALLA PARCIALMENTE:** Reporta éxitos/fracasos, reintenta individualmente, proporciona detalles de entrada manual si los reintentos fallan.

### Paso 5: Configura Vistas y Entrega

**Notion MCP no soporta la creación de vistas de forma programática.** Proporciona instrucciones exactas:

```
VISTAS RECOMENDADAS (crea estas en Notion):

1. TODOS LOS GASTOS (Tabla) — Ordenar: Fecha descendente. Sin filtro.
2. ESTE MES (Tabla) — Filtro: Fecha es "Este mes". Agrupar por: Categoría.
3. POR CATEGORÍA (Tabla) — Agrupar por: Categoría. Ordenar: Monto descendente.
4. DEDUCCIONES FISCALES (Tabla) — Filtro: Deducible Fiscal es "Completa" O "Parcial".
   Agrupar por: Categoría. Ordenar: Fecha ascendente.
5. NECESITA ATENCIÓN (Tabla) — Filtro: Deducible Fiscal es "Verificar" O Etiquetas
   contiene "recibo-pendiente". Ordenar: Fecha ascendente.
```

**GUÍA DE USO (entrega a todo usuario):**

```
AGREGAR UN GASTO (el mismo día de la compra):
1. Haz clic en "+ Nuevo" en "Todos los Gastos"
2. Ingresa Nombre de Gasto, Monto, Fecha, Categoría, Vendedor, Método de Pago
3. Establece Deducible Fiscal: Completa (claramente comercial), Parcial (uso mixto),
   Ninguna (personal), Verificar (incierto — marca para contador)
4. Pega enlace de recibo si está disponible; marca "Recurrente" para suscripciones

REVISIÓN MENSUAL (30 min, fin de mes):
1. Abre "Este Mes" — verifica totales por categoría
2. Abre "Necesita Atención" — resuelve elementos "Verificar", carga recibos faltantes

PREPARACIÓN PARA IMPUESTOS (anualmente):
1. Abre "Deducciones Fiscales" — filtra por año fiscal
2. Agrupa por Categoría para coincidir con artículos del Anexo C
3. Resuelve elementos "Verificar" restantes
4. Comparte base de datos con tu contador a través del compartir de Notion

DEDUCCIONES PARCIALES: Establece a "Parcial", registra % de uso comercial en Notas
(p. ej., "Internet del hogar — 40% uso comercial")
```

**DESCARGO DE RESPONSABILIDAD IMPORTANTE (incluye en cada entrega):**

```
DESCARGO DE RESPONSABILIDAD: Este rastreador de gastos es solo para mantener
registros y propósitos de organización. No constituye asesoramiento fiscal. Consulta
a un profesional fiscal calificado para elegibilidad de deducción, cumplimiento y presentación.
```

---

## Ejemplo 1: Desarrollador Web Freelance

**Solicitud del usuario:** "Soy un desarrollador web freelance, propietario único. Rastrea mis gastos en Notion bajo 'Finanzas Freelance'. Tengo algunos gastos recientes para agregar."

**Ejecución:**

1. **Requisitos:** Propietario único, padre "Finanzas Freelance", año calendario, USD, 8 gastos
2. **Búsqueda:** `notion-search` para "Finanzas Freelance" -> `pg_fin456`. Confirmado.
3. **Crear:** `notion-create-database` con esquema completo -> `db_exp789`
4. **Siembra 8 gastos:**

```
Gastos importados: 8 de 8 exitosos

  SOFTWARE & SUSCRIPCIONES:
    Adobe Creative Cloud - Enero      $54.99   Tarjeta de Crédito   Completa
    GitHub Pro - Enero                $4.00    Tarjeta de Crédito   Completa
    Notion Team Plan - Enero          $10.00   Tarjeta de Crédito   Completa
    AWS Hosting - Enero               $127.43  Tarjeta de Crédito   Completa

  CONTRATISTAS:
    Rediseño de Logo - Sarah Kim Design    $750.00  PayPal        Completa
    Copywriting - Jake Torres              $400.00  Transferencia Bancaria Completa

  GASTOS DE OFICINA:
    Elevador de escritorio de pie                 $189.99  Débito         Completa
    Hub USB-C y cables                           $67.50   Tarjeta de Crédito   Completa

Total: $1,603.91 | Recurrente: $196.42/mes (4 suscripciones) | Todas totalmente deducibles
```

5. **Entregado:** Vistas + guía de uso + descargo de responsabilidad. Próximos pasos: crear vistas, agregar suscripciones de febrero, registrar gastos el mismo día, programar revisión mensual.

---

## Ejemplo 2: Dueño de Tienda de E-Commerce

**Solicitud del usuario:** "Ejecuto una pequeña tienda de e-commerce vendiendo velas hechas a mano. LLC. Mi página de Notion es 'Operaciones Candle Biz'. Tengo alrededor de 10 gastos recientes."

**Ejecución:**

1. **Requisitos:** LLC, padre "Operaciones Candle Biz", año calendario, USD, 10 gastos
2. **Búsqueda:** `notion-search` para "Operaciones Candle Biz" -> `pg_candle321`. Confirmado.
3. **Crear:** `notion-create-database` con esquema completo -> `db_candle654`
4. **Siembra 10 gastos:**

```
Gastos importados: 10 de 10 exitosos

  SUMINISTROS:
    Orden a granel de cera de soya (50 lbs)    $189.00  Tarjeta de Crédito   Completa
    Surtido de aceites fragantes (12 pk)       $84.50   Tarjeta de Crédito   Completa
    Paquete de mechas y etiquetas             $42.00   Débito         Completa
    Frascos de vidrio (caja de 48)             $156.00  Tarjeta de Crédito   Completa

  PUBLICIDAD:
    Anuncios de Instagram - Enero              $250.00  Tarjeta de Crédito   Completa
    Listados Promocionados de Etsy - Enero     $87.30   Débito         Completa
    Anuncios de Facebook - Enero               $150.00  Tarjeta de Crédito   Completa

  VIAJES:
    Alquiler de puesto en feria artesanal - Portland   $175.00  Efectivo          Completa
  AUTO & TRANSPORTE:
    Gasolina y peajes para viaje a Portland    $63.20   Efectivo          Parcial

  SOFTWARE & SUSCRIPCIONES:
    Plan Shopify Basic - Enero                 $39.00   Tarjeta de Crédito   Completa

Total: $1,236.00 | Recurrente: $526.30/mes | Completa (9), Parcial (1)
Consejo: Etiqueta inventario con "una-sola-vez" y gastos publicitarios con "mensual" para separar
costo de bienes de gastos operacionales al momento de impuestos.
```

5. **Entregado:** Vistas + guía de uso + descargo de responsabilidad. Próximos pasos: crear vistas, cargar 2 recibos en efectivo, registrar % de uso comercial para Auto & Transporte, registrar gastos el mismo día.

---

## Lista de Verificación Previa a la Entrega

Ejecuta esto antes de entregar. **NO OMITAS NINGÚN ARTÍCULO.**

| Verificación | Qué Verificar |
|-------|----------------|
| Base de datos existe | `notion-fetch` con ID de base de datos tiene éxito |
| Todas las 12 propiedades | Cada propiedad del esquema configurada |
| Opciones de categoría | Todas las 15 categorías existen como opciones de selección |
| Métodos de pago | Todos los 6 métodos existen como opciones de selección |
| Opciones Deducible Fiscal | Completa, Parcial, Ninguna, Verificar todos presentes |
| Formato de monto | Número formateado como dólar |
| Fecha + Recurrente | Fecha es tipo fecha, Recurrente es casilla de verificación |
| Etiquetas configuradas | Todas las 9 etiquetas predeterminadas existen como opciones multi-seleccionar |
| Gastos sembrados | Todos los gastos proporcionados creados, sin duplicados |
| Montos precisos | Los montos en dólares coinciden exactamente con datos del usuario |
| Descargo entregado | Descargo de responsabilidad fiscal incluido en entrega |
| Vistas + guía de uso | Todas las 5 vistas e instrucciones de operaciones entregadas |
| Página padre correcta | Base de datos bajo página solicitada |

```
Lista de Verificación Previa a la Entrega:
  [x] Base de datos creada y accesible
  [x] Todas las 12 propiedades configuradas
  [x] Opciones de categoría correctas (15 alineadas con IRS)
  [x] Métodos de pago presentes (6)
  [x] Opciones Deducible Fiscal correctas (4)
  [x] Monto formateado como dólar
  [x] Propiedades Fecha y Recurrente configuradas
  [x] Etiquetas configuradas (9 predeterminadas o personalizadas)
  [x] Todos los gastos sembrados, sin duplicados, montos verificados
  [x] Descargo de responsabilidad fiscal entregado
  [x] Instrucciones de vistas y guía de uso entregadas
  [x] Base de datos bajo página padre correcta
```

---

## Recuperación y Solución de Problemas

### Notion Search No Devuelve Resultados

1. Pide título exacto de página (sensible a mayúsculas)
2. Intenta palabra clave más corta (p. ej., "Finanzas" en lugar de "Dashboard Finanzas Empresariales")
3. Confirma que la página es compartida con la integración de Notion
4. **Después de 3 fracasos:** "Verifica Configuración > Conexiones en Notion y confirma acceso de integración."

### La Creación de Base de Datos Falla

1. Verifica ID de página padre con `notion-fetch`
2. Verifica errores de permiso
3. Reintenta una vez
4. **Si aún falla:** "Ve a página padre > menú de tres puntos > Conexiones > asegúrate acceso 'Puede editar'."

### La Siembra de Gastos Falla Parcialmente

1. Reporta qué gastos tuvieron éxito y cuáles fracasaron
2. Reintenta gastos fallidos individualmente
3. Si los reintentos fallan, proporciona detalles para entrada manual

### Límites de Velocidad de API de Notion

1. Pausa 10 segundos entre lotes, reduce a 5 por llamada
2. **NO omitas gastos debido a límites** -- desacelera y reintenta

### El Usuario No Está Seguro Sobre Categorías

1. Presenta la tabla de categorías
2. Mapea a categoría más probable
3. Si es ambiguo, predeterminado a "Otro" con Deducible Fiscal = "Verificar"
4. Agrega Nota: "Categoría incierta -- revisar con contador"

### El Usuario Quiere Modificar el Esquema Después

**Notion MCP no soporta modificar esquemas.** Instruye al usuario: haz clic en "+" para agregar propiedad, haz clic en encabezado de columna > "Editar propiedad" para modificar, o agrega nuevas opciones de categoría a través de "Editar propiedad" en la columna Categoría.

### Importación CSV Grande

1. Analiza encabezados y presenta mapeo para confirmación
2. Procesa en lotes de 10-15 por llamada `notion-create-pages`
3. Reporta progreso después de cada lote
4. **50+ filas:** Advierte que la importación toma varios minutos debido a límites de API

---

## Anti-patrones

- **NO** proporciones asesoramiento fiscal específico -- este es un sistema de seguimiento, no un servicio de asesoramiento fiscal
- **NO** asumas deducibilidad sin marcar -- cuando tengas dudas, establece a "Verificar"
- **NO** mezcles gastos personales y empresariales -- aconseja seguimiento separado
- **NO** adivines o fabriques montos en dólares -- solo registra lo que el usuario proporciona
- **NO** crees la base de datos sin el esquema de propiedades completo
- **NO** omitas el descargo de responsabilidad fiscal -- toda entrega debe incluirlo
- **NO** categorices gastos de auto como 100% deducibles -- casi siempre parcial
- **NO** prometas cumplimiento del IRS -- esto organiza registros, no garantiza auditorías
- **NO** crees vistas de forma programática -- proporciona instrucciones manuales
- **NO** entregues sin la guía de uso -- el rastreador requiere conocimiento de operación diaria
