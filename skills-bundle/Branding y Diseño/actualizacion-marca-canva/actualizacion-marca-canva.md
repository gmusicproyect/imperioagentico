---
name: actualizacion-marca-canva
description: "Actualiza textos e imágenes en masa a través de diseños Canva existentes cuando cambian elementos de marca, buscando diseños afectados y aplicando operaciones de búsqueda y reemplazo en todos los archivos confirmados. Úsalo cuando hayas actualizado tus colores de marca, fuentes, tagline, logo o información de contacto y necesites propagar esos cambios a través de múltiples diseños Canva."
allowed-tools: Read Write Glob mcp__claude_ai_Canva__search-designs mcp__claude_ai_Canva__get-design mcp__claude_ai_Canva__get-design-content mcp__claude_ai_Canva__start-editing-transaction mcp__claude_ai_Canva__perform-editing-operations mcp__claude_ai_Canva__commit-editing-transaction mcp__claude_ai_Canva__cancel-editing-transaction mcp__claude_ai_Canva__get-design-thumbnail mcp__claude_ai_Canva__list-brand-kits
metadata:
  author: Imperio Digital
  version: "1.0"
---

# Actualización de Marca en Canva

## Cuándo Usar Este Skill

Usa este skill cuando necesites:
- Propagar un nuevo tagline, slogan o declaración de marca a través de diseños Canva existentes
- Reemplazar un número de teléfono, dirección de email o URL de sitio web antiguos a través de materiales de marketing
- Actualizar referencias de colores de marca o fuentes incrustadas en elementos de texto de diseño
- Cambiar una URL de logo o activo de imagen a través de múltiples diseños después de un rebrand
- Encontrar cada diseño que contiene información de marca desactualizada y actualizarlos en masa

**NO** uses este skill para:
- Crear diseños completamente nuevos desde cero (usa social-media-graphics u habilidades similares)
- Actualizar el Kit de Marca de Canva en sí mismo (haz eso directamente en la configuración de Canva)
- Rediseñar diseños, reestructurar contenido o cambiar conceptos visuales
- Editar un solo diseño (simplemente ábrelo en Canva manualmente)

---

## Referencia Rápida: Tipos de Cambios de Marca Comunes

| Tipo de Cambio | Ejemplo de Valor Antiguo | Ejemplo de Valor Nuevo | Estrategia de Búsqueda |
|-------------|-------------------|-------------------|-----------------|
| Tagline | "Construye Mejor" | "Envía Más Rápido" | Busca contenido de diseño para el texto antiguo exacto |
| URL de Sitio Web | www.sitioviejo.com | www.situonuevo.com | Busca cadena de dominio |
| Número de Teléfono | (555) 123-4567 | (555) 987-6543 | Busca número antiguo con/sin formato |
| Dirección de Email | hola@empresavieja.com | hola@empresanueva.com | Busca cadena de email antiguo |
| Nombre de Empresa | Empresa Vieja Inc. | Empresa Nueva Inc. | Busca nombre de empresa antiguo |
| Código de Color Hex | #FF6B35 | #2D5BFF | Busca elementos de texto que hagan referencia al hex antiguo |
| Dirección Callejera | 123 Calle Principal | 456 Avenida Roble | Busca dirección callejera antigua |

---

## Workflow Principal

TODA ACTUALIZACIÓN DE MARCA COMIENZA CON UNA LISTA DE CAMBIOS COMPLETA ANTES DE TOCAR CUALQUIER DISEÑO -- NUNCA EDITES DISEÑOS SIN SABER TODOS LOS CAMBIOS POR ADELANTADO.

### Paso 1: Comprende los Cambios

Recopila cada cambio de marca del usuario antes de buscar diseños.

1. Pide al usuario que enumere todos los elementos que cambiaron, en pares explícitos de antiguo a nuevo
2. Confirma cada par con el usuario antes de proceder
3. Agrupa cambios por tipo para búsqueda eficiente

**Plantilla para presentar si el usuario hace una solicitud vaga:**

```
Actualizaré tus diseños Canva. Necesito los valores exactos de antiguo a nuevo para cada cambio:

1. ¿Qué texto cambió? (tagline antiguo -> tagline nuevo, URL antigua -> URL nueva, etc.)
2. ¿Algún cambio de información de contacto? (teléfono, email, dirección)
3. ¿Algún cambio visual? (colores, URL de imagen de logo)
4. ¿Cuántos diseños crees que están afectados? (una estimación aproximada me ayuda a buscar)
```

**Construye un manifiesto de cambios como este:**

```
Actualización de Marca — Manifiesto de Cambios
================================
Cambio 1: Tagline
  ANTIGUO: "Construye Mejor"
  NUEVO: "Envía Más Rápido"

Cambio 2: URL de Sitio Web
  ANTIGUO: www.acmecorp.com
  NUEVO: www.acme.io

Cambio 3: Número de Teléfono
  ANTIGUO: (555) 123-4567
  NUEVO: (555) 987-6543

Total de cambios: 3
```

**NO PROCEDAS AL PASO 2 HASTA QUE EL USUARIO CONFIRME QUE EL MANIFIESTO DE CAMBIOS ESTÁ COMPLETO Y CORRECTO.**

### Paso 2: Busca Diseños Afectados

Encuentra cada diseño que contiene cualquiera de los valores antiguos del manifiesto de cambios.

1. Llama a `search-designs` con palabras clave de cada valor antiguo:
   - Para taglines: busca las palabras clave (ej.: "Construye Mejor")
   - Para URLs: busca el dominio (ej.: "acmecorp")
   - Para teléfono/email: busca la cadena completa y coincidencias parciales
   - Para nombres de empresa: busca el nombre antiguo

2. Para cada diseño devuelto por búsqueda, llama a `get-design-content` para inspeccionar los elementos de texto reales

3. Verifica cada elemento de texto en el contenido del diseño contra cada valor antiguo en el manifiesto de cambios

4. Construye una lista de diseños afectados con especificidades:

```
Escaneando diseños en busca de valores de marca antiguos...

Búsqueda: "Construye Mejor" — 23 diseños devueltos
  Verificando contenido... 15 contienen el tagline en elementos de texto

Búsqueda: "acmecorp" — 18 diseños devueltos
  Verificando contenido... 12 contienen la URL antigua en elementos de texto

Búsqueda: "(555) 123-4567" — 9 diseños devueltos
  Verificando contenido... 8 contienen el número de teléfono antiguo
```

5. Deduplica la lista — un solo diseño puede coincidir con múltiples cambios

**SI LA BÚSQUEDA DEVUELVE DEMASIADOS RESULTADOS:**
- Reduce la búsqueda agregando palabras de contexto (ej.: "Construye Mejor tagline" en lugar de solo "Construye")
- Filtra por tipo de diseño si el usuario especifica (posts sociales, presentaciones, volantes)
- Procesa en lotes de 20 diseños a la vez

**SI LA BÚSQUEDA NO DEVUELVE RESULTADOS:**
- Intenta frases alternativas o cadenas parciales
- Pregunta al usuario si el valor antiguo se deletrea diferente en algunos diseños
- Intenta buscar solo el nombre de marca para encontrar todos los diseños de marca, luego inspecciona contenido manualmente
- **Después de 3 estrategias de búsqueda fallidas, informa al usuario:** "No se encontraron diseños que contengan esos valores. Por favor, verifica que el texto antiguo sea exactamente como aparece en tus diseños Canva."

### Paso 3: Presenta Diseños Afectados para Confirmación

Muestra al usuario exactamente qué diseños se modificarán y qué cambios aplican a cada uno.

1. Llama a `get-design-thumbnail` para cada diseño afectado para proporcionar contexto visual

2. Presenta la lista completa agrupada por diseño:

```
DISEÑOS AFECTADOS — REVISAR ANTES DE ACTUALIZAR
==========================================

1. "Post de Instagram de Venta de Verano" (dsg_abc123)
   [miniatura mostrada]
   Cambios a aplicar:
     - Tagline: "Construye Mejor" -> "Envía Más Rápido"
     - URL: www.acmecorp.com -> www.acme.io

2. "Presentación de Descripción General de la Empresa" (dsg_def456)
   [miniatura mostrada]
   Cambios a aplicar:
     - Tagline: "Construye Mejor" -> "Envía Más Rápido"
     - Teléfono: (555) 123-4567 -> (555) 987-6543
     - URL: www.acmecorp.com -> www.acme.io

3. "Plantilla de Tarjeta de Presentación" (dsg_ghi789)
   [miniatura mostrada]
   Cambios a aplicar:
     - Teléfono: (555) 123-4567 -> (555) 987-6543
     - URL: www.acmecorp.com -> www.acme.io

... (12 diseños más)

==========================================
Total: 15 diseños, 34 reemplazos de texto individuales

Confirma: ¿Actualizar todos los 15 diseños? O dime cuáles saltar.
```

3. **Espera confirmación del usuario** antes de editar cualquier cosa
4. Si el usuario quiere saltar diseños específicos, elimínalos del lote
5. Si el usuario identifica diseños que deberían estar afectados pero faltan, ejecuta búsquedas adicionales

**NO EDITES NINGÚN DISEÑO HASTA QUE EL USUARIO CONFIRME EXPLÍCITAMENTE LA LISTA.**

### Paso 4: Aplica Cambios a través de Transacciones de Edición

Procesa cada diseño confirmado usando el workflow de transacción de edición de Canva.

**Para cada diseño en la lista confirmada:**

1. Llama a `start-editing-transaction` para el ID del diseño
2. Llama a `perform-editing-operations` con todos los reemplazos de texto para ese diseño:
   - Reemplaza cada valor antiguo con el valor nuevo en cada elemento de texto donde aparece
   - Aplica todos los cambios para el diseño en una sola llamada `perform-editing-operations` cuando sea posible
3. Llama a `commit-editing-transaction` para guardar los cambios

4. Llama a `get-design-thumbnail` para verificar la actualización visualmente

5. Registra el resultado:

```
[1/15] "Post de Instagram de Venta de Verano" (dsg_abc123)
  - Reemplazó "Construye Mejor" con "Envía Más Rápido" — 1 elemento de texto actualizado
  - Reemplazó "www.acmecorp.com" con "www.acme.io" — 1 elemento de texto actualizado
  ESTADO: Confirmado exitosamente
```

**Procesa diseños secuencialmente — una transacción a la vez.** No inicies una nueva transacción antes de que la anterior se confirme o cancele.

6. Después de procesar todos los diseños, presenta el resumen final:

```
ACTUALIZACIÓN DE MARCA COMPLETA
======================
Diseños actualizados: 15 de 15 exitosos
Total de reemplazos realizados: 34

Desglose por cambio:
  "Construye Mejor" -> "Envía Más Rápido"       — actualizado en 15 diseños
  www.acmecorp.com -> www.acme.io        — actualizado en 12 diseños
  (555) 123-4567 -> (555) 987-6543       — actualizado en 8 diseños

Todos los diseños guardados. Los cambios están en vivo en tu cuenta de Canva.
```

---

## Ejemplo 1: La Empresa Cambia Tagline a Través de Gráficos Sociales

**Solicitud del usuario:** "Acabamos de cambiar nuestro tagline de 'Construye Mejor' a 'Envía Más Rápido'. Necesito actualizar todos nuestros gráficos de redes sociales en Canva — creo que hay alrededor de 15 de ellos."

**Ejecución paso a paso:**

1. **Manifiesto de cambios:**
   ```
   Actualización de Marca — Manifiesto de Cambios
   ================================
   Cambio 1: Tagline
     ANTIGUO: "Construye Mejor"
     NUEVO: "Envía Más Rápido"

   Total de cambios: 1
   ```
   El usuario confirma.

2. **Búsqueda:** Llama a `search-designs` con consulta "Construye Mejor". Devuelve 23 resultados. Llama a `get-design-content` en cada uno. 15 diseños contienen "Construye Mejor" en elementos de texto.

3. **Presenta:** Muestra los 15 diseños con miniaturas y el cambio de tagline anotado para cada uno. El usuario confirma los 15.

4. **Aplica:** Para cada uno de los 15 diseños:
   - `start-editing-transaction` con ID de diseño
   - `perform-editing-operations` — reemplaza "Construye Mejor" con "Envía Más Rápido"
   - `commit-editing-transaction`
   - `get-design-thumbnail` para verificar

   **Resultado:**

   ```
   ACTUALIZACIÓN DE MARCA COMPLETA
   ======================
   Diseños actualizados: 15 de 15 exitosos
   Total de reemplazos realizados: 15

   Diseños actualizados:
     [1]  Post de Instagram — Campaña Q1
     [2]  Post de Instagram — Lanzamiento de Producto
     [3]  Historia de Instagram — Consejos Semanales
     [4]  Foto de Portada de Facebook
     [5]  Post de Facebook — Acerca de Nosotros
     [6]  Encabezado de X/Twitter
     [7]  Post de X/Twitter — Bienvenido
     [8]  Pancarta de LinkedIn
     [9]  Post de LinkedIn — Contratación
     [10] Pin de Pinterest — Descripción General de Marca
     [11] Miniatura de YouTube — Episodio 12
     [12] Miniatura de YouTube — Episodio 13
     [13] Gráfico de Encabezado de Email
     [14] Pancarta de Boletín
     [15] Pancarta de Héroe de Sitio Web

   El tagline "Envía Más Rápido" ahora está en vivo en los 15 diseños.
   ```

---

## Ejemplo 2: Actualizar Número de Teléfono y Sitio Web a Través de Materiales de Marketing

**Solicitud del usuario:** "Nos mudamos de oficina y cambiamos nuestro número de teléfono. El número antiguo era (312) 555-0142, el nuevo es (773) 555-0198. También nuestro sitio web cambió de www.greenleafco.com a www.greenleaf.io. ¿Puedes actualizar todo en Canva?"

**Ejecución paso a paso:**

1. **Manifiesto de cambios:**
   ```
   Actualización de Marca — Manifiesto de Cambios
   ================================
   Cambio 1: Número de Teléfono
     ANTIGUO: (312) 555-0142
     NUEVO: (773) 555-0198

   Cambio 2: URL de Sitio Web
     ANTIGUO: www.greenleafco.com
     NUEVO: www.greenleaf.io

   Total de cambios: 2
   ```
   El usuario confirma.

2. **Búsqueda:**
   - `search-designs` con consulta "(312) 555-0142" — 6 resultados. Verificación de contenido: 5 contienen el número de teléfono.
   - `search-designs` con consulta "greenleafco" — 14 resultados. Verificación de contenido: 8 contienen la URL.
   - Total deduplificado: 10 diseños únicos (3 diseños tienen tanto teléfono como URL).

3. **Presenta:** Muestra 10 diseños con miniaturas. Para cada uno, enumera qué cambios aplican:

   ```
   DISEÑOS AFECTADOS — REVISAR ANTES DE ACTUALIZAR
   ==========================================

   1. "Tarjeta de Presentación — Frente" (dsg_bc001)
      [miniatura mostrada]
      Cambios: teléfono + URL

   2. "Tarjeta de Presentación — Reverso" (dsg_bc002)
      [miniatura mostrada]
      Cambios: teléfono + URL

   3. "Folleto Tríptico — Página 3" (dsg_br003)
      [miniatura mostrada]
      Cambios: teléfono + URL

   4. "Pancarta de Firma de Email" (dsg_es004)
      [miniatura mostrada]
      Cambios: teléfono + URL (bloque de contacto, sin teléfono)
      ** Nota: contiene URL pero teléfono no encontrado en este diseño

   5. "Pancarta de Exposición Comercial" (dsg_ts005)
      [miniatura mostrada]
      Cambios: solo teléfono

   ... (5 diseños más)

   ==========================================
   Total: 10 diseños, 13 reemplazos de texto individuales

   ¿Confirma: Actualizar todos los 10 diseños?
   ```

   El usuario confirma pero dice: "Salta la pancarta de exposición comercial, no la estamos usando más."
   Elimina el diseño 5 del lote. Procediendo con 9 diseños.

4. **Aplica:** Para cada uno de los 9 diseños:
   - Inicia transacción, realiza reemplazos, confirma, verifica miniatura

   **Resultado:**

   ```
   ACTUALIZACIÓN DE MARCA COMPLETA
   ======================
   Diseños actualizados: 9 de 9 exitosos
   Saltado: 1 (Pancarta de Exposición Comercial — usuario solicitó saltar)
   Total de reemplazos realizados: 12

   Desglose:
     (312) 555-0142 -> (773) 555-0198  — actualizado en 4 diseños
     www.greenleafco.com -> www.greenleaf.io — actualizado en 8 diseños

   Todos los diseños guardados. Los cambios están en vivo en tu cuenta de Canva.
   ```

---

## Lista de Verificación Previa a la Actualización

Ejecuta esta lista de verificación antes de confirmar cualquier edición. **NO SALTES NINGÚN ELEMENTO.**

| Verificación | Qué Verificar | Cómo |
|-------|----------------|-----|
| Manifiesto de cambios confirmado | El usuario revisó y aprobó todos los pares de antiguo a nuevo | Confirmación explícita del usuario en el Paso 1 |
| Todos los valores antiguos buscados | Se buscó cada valor antiguo, no solo el primero | Verifica que se ejecutó cada búsqueda |
| Contenido inspeccionado | Se llamó a `get-design-content` en cada resultado de búsqueda | Confirma registros de verificación de contenido |
| Diseños deduplicados | Ningún diseño aparece dos veces en la lista afectada | Verifica IDs de diseño duplicados |
| Miniaturas mostradas | El usuario vio una vista previa de miniatura para cada diseño afectado | Confirma que se mostraron miniaturas |
| Usuario aprobó lista | El usuario confirmó explícitamente qué diseños actualizar | Debe ocurrir en el Paso 3 |
| Cambios por diseño enumerados | Cada diseño muestra exactamente qué reemplazos aplican | Verifica en la lista presentada |
| Transacciones secuenciales | Solo una transacción de edición está abierta a la vez | Procesa un diseño, confirma, luego siguiente |

```
Lista de Verificación Previa a la Actualización:
  [x] Manifiesto de cambios confirmado por usuario
  [x] Todos los valores antiguos buscados
  [x] Contenido de diseño inspeccionado para cada resultado
  [x] Lista de diseños afectados deduplicada
  [x] Miniaturas mostradas para todos los diseños afectados
  [x] Usuario aprobó la lista final
  [x] Lista de cambios por diseño precisa
  [x] Procesamiento de transacción secuencial
```

---

## Recuperación y Solución de Problemas

### La Transacción de Edición Falla a Mitad de Diseño

Si `perform-editing-operations` o `commit-editing-transaction` devuelve un error:

1. Llama a `cancel-editing-transaction` para abortar limpiamente la transacción fallida
2. Registra el diseño como fallido — no reintentar inmediatamente
3. Continúa procesando los diseños restantes
4. Después de que se completa el lote, reintenta cada diseño fallido individualmente
5. **Si un diseño falla dos veces:** "El diseño '[nombre]' (dsg_xxx) no pudo actualizarse. El diseño puede estar bloqueado, corrupto o utilizar un tipo de elemento no soportado. Ábrelo en Canva para actualizar manualmente. Cambios necesarios: [enumera los reemplazos específicos]."

### El Diseño Está Bloqueado o es de Solo Lectura

Si `start-editing-transaction` devuelve un error de permiso o bloqueo:

1. Informa al usuario: "El diseño '[nombre]' está actualmente bloqueado. Puede estar abierto en otra sesión o compartido con permisos restringidos."
2. Salta el diseño y continúa con el resto del lote
3. Después de que se completa el lote, pide al usuario cerrar el diseño en Canva y reintentar

### La Búsqueda Encuentra Diseños que el Usuario No Reconoce

Si la lista de diseños afectados incluye elementos inesperados:

1. Muestra la miniatura y el nombre del diseño — deja que el usuario decida
2. El usuario puede tener diseños antiguos o archivados que olvidó
3. **Predeterminado: inclúyelos en la actualización a menos que el usuario los excluya explícitamente** — los diseños desactualizados con información de marca incorrecta son exactamente lo que esta habilidad arregla

### La Coincidencia de Texto Parcial Crea Reemplazos No Intencionados

Si el valor antiguo es una palabra común o subcadena que podría coincidir con texto no intencionado:

1. Antes de editar, muestra los elementos de texto exactos que cambiarán y su contexto circundante
2. Ejemplo: reemplazar "Ir" (nombre de empresa antiguo) podría coincidir con "Ve a nuestro sitio web" — señálalo al usuario
3. **Usa coincidencia exacta y sensible a mayúsculas** al realizar reemplazos
4. Si un reemplazo es muy amplio, pide al usuario una cadena de búsqueda más específica

### El Usuario Quiere Deshacer Cambios

Si el usuario se da cuenta de que un cambio fue incorrecto después de que se confirmen ediciones:

1. Canva tiene historial de versiones integrado — instruye al usuario restaurar versiones anteriores
2. Alternativamente, ejecuta la habilidad nuevamente con los valores invertidos (intercambia antiguo y nuevo)
3. **Esta habilidad no mantiene su propio historial de deshacer** — confía en el versionado de Canva

---

## Anti-Patrones

- **NO** edites diseños sin confirmación del usuario de la lista afectada — ediciones accidentales en 20+ diseños son difíciles de deshacer
- **NO** abras múltiples transacciones de edición simultáneamente — una a la vez, confirma antes de iniciar la siguiente
- **NO** saltes el paso de inspección de contenido — los resultados de búsqueda pueden incluir diseños que mencionan la palabra clave pero no contienen el elemento de marca real
- **NO** asuidas formato — si el número de teléfono antiguo aparece como "(555) 123-4567" en algunos diseños y "555-123-4567" en otros, busca ambos formatos
- **NO** procedas con un manifiesto de cambios parcial — si el usuario menciona "algunas cosas cambiaron," presiona por la lista completa antes de buscar
- **NO** reemplaces texto ciegamente — siempre verifica que la coincidencia sea el elemento de marca intentado, no parte de contenido relacionado
