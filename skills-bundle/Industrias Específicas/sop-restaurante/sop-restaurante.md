---
name: sop-restaurante
description: "Construye SOPs de restaurantes para operaciones de cocina, servicio de frente de casa, seguridad alimentaria y procedimientos de apertura/cierre. Usa cuando estandarices las operaciones del restaurante."
allowed-tools: Read Write Glob
metadata:
  author: Imperio Digital
  version: "1.0"
---

# SOP de Restaurante

## Cuándo Usar Este Skill

Usa este skill cuando necesites:
- Crear procedimientos operativos estándar para operaciones de restaurante
- Documentar workflows de cocina, estándares de servicio y procedimientos de seguridad
- Construir manuales listos para entrenamiento para nuevo personal
- Estandarizar procedimientos de apertura, cierre y cambio de turno

**NO** uses este skill para diseño de menú, marketing de restaurante o planificación empresarial. Esto es para SOPs operacionales que el personal sigue diariamente.

---

## Principio Fundamental

UN SOP ELIMINA LA ADIVINANZA — SI UN NUEVO EMPLEADO NO PUEDE SEGUIR EL PROCEDIMIENTO SIN HACER PREGUNTAS, EL SOP NO ES LO SUFICIENTEMENTE CLARO. ESCRIBE PARA LA PERSONA MÁS NUEVA DEL EQUIPO.

---

## Fase 1: Resumen

### Información Requerida

| Entrada | Qué Preguntar | Predeterminado |
|---------|--------------|--------|
| **Tipo de restaurante** | "¿Qué tipo de restaurante? Casual rápido, servicio completo, comida fina, café?" | Sin predeterminado — debe proporcionarse |
| **SOPs necesarios** | "¿Qué áreas necesitan SOPs? ¿Cocina, FOH, seguridad alimentaria, apertura/cierre, todo?" | Todas las áreas |
| **Tamaño del equipo** | "¿Cuántos empleados de personal?" | Menos de 15 |
| **Documentación actual** | "¿Tienes procedimientos escritos hoy?" | Nada formal |
| **Pain points** | "¿Dónde suceden la mayoría de los errores?" | Comida inconsistente, problemas de servicio |
| **Requisitos de departamento de salud** | "¿Algún código de salud específico o requisitos de inspección a cumplir?" | Códigos de salud locales estándar |

**PUNTO DE CONTROL: Confirma el resumen antes de escribir SOPs.**

---

## Fase 2: Estructura

### Categorías de SOP

```
SOPs de Restaurante
├── Procedimientos de Apertura
├── Procedimientos de Cierre
├── Operaciones de Cocina
│   ├── Estándares de Prep de Alimentos
│   ├── Procedimientos de Cocción
│   ├── Estándares de Plating
│   └── Limpieza de Cocina
├── Frente de Casa
│   ├── Bienvenida y Asiento de Clientes
│   ├── Toma de Pedido
│   ├── Servicio de Alimentos
│   ├── Procesamiento de Pagos
│   └── Reset de Mesa
├── Seguridad Alimentaria
│   ├── Monitoreo de Temperatura
│   ├── Almacenamiento de Alimentos (FIFO)
│   ├── Manejo de Alérgenos
│   ├── Protocolo de Lavado de Manos
│   └── Limpieza y Sanitización
├── Gestión de Turno
│   ├── Procedimientos de Cambio de Turno
│   ├── Cronogramas de Descanso
│   └── Manejo de Efectivo
└── Procedimientos de Emergencia
    ├── Quejas de Clientes
    ├── Falla de Equipos
    └── Incidentes de Salud/Seguridad
```

### Plantilla de Documento SOP

```
## [Título de SOP]

**Departamento:** Cocina / FOH / Gestión
**Última actualización:** [Fecha]
**Aplica a:** [Qué roles]

### Propósito
[Una frase: por qué existe este procedimiento]

### Procedimiento
1. [Paso 1]
2. [Paso 2]
3. [Paso 3]
...

### Estándar de Calidad
[Qué se ve "hecho correctamente"]

### Errores Comunes
- [Error 1] → [Cómo evitar]
- [Error 2] → [Cómo evitar]
```

**PUNTO DE CONTROL: Confirma qué SOPs crear y en qué orden antes de escribir.**

---

## Fase 3: Escribir

### Procedimientos de Apertura

```
## SOP de Apertura de Restaurante

**Aplica a:** Gerente de apertura, personal de cocina de apertura, servidores de apertura

### Gerente (llega 60 min antes de abrir)
1. Desactiva el sistema de seguridad y enciende las luces
2. Verifica buzones de voz y email para reservaciones o cancelaciones
3. Camina por el restaurante: revisa pisos, baños y comedor
4. Verifica que el sistema POS funcione y que el efectivo inicial sea correcto
5. Revisa las reservaciones del día, eventos y artículos de "86" (no disponibles)
6. Briefing al personal en reunión previa a la apertura (10 min antes de abrir)

### Cocina (llega 60 min antes de abrir)
1. Enciende todos los equipos (hornos, parrillas, freidoras, baño maría)
2. Revisa temperaturas de la cámara frigorífica (debe ser 40°F o menos)
3. Tira la lista de prep y comienza el prep matutino
4. Configura todas las estaciones con mise en place
5. Verifica que todas las salsas, aderezos y guarniciones sean frescas
6. Confirma que el inventario de respaldo sea accesible

### Frente de Casa (llega 30 min antes de abrir)
1. Configura todas las mesas (cubertería, servilletas, vasos, condimentos)
2. Verifica que los baños estén surtidos y limpios
3. Llena estaciones de agua, cubetas de hielo y café
4. Enciende la música y ajusta la iluminación
5. Revisa especiales y lista de "86"
6. Abre la puerta frontal en la hora de apertura
```

### SOPs de Seguridad Alimentaria

```
## Seguridad Alimentaria: Monitoreo de Temperatura

**Aplica a:** Todo el personal de cocina
**Frecuencia:** Cada 2 horas durante el servicio

### Procedimiento
1. Usa un termómetro calibrado (calibración con baño de hielo al inicio del turno)
2. Revisa y registra temperaturas para:
   - Cámara frigorífica (debe ser 40°F o menos)
   - Congelador (debe ser 0°F o menos)
   - Artículos en caliente (debe ser 135°F o más)
   - Artículos en frío (debe ser 41°F o menos)
3. Registra en la hoja de registro de temperatura
4. Si alguna temperatura está fuera del rango:
   - CALIENTE: Recalienta a 165°F dentro de 2 horas o descarta
   - FRÍO: Mueve a unidad funcional inmediatamente, descarta si está arriba de 41°F por 4+ horas
5. Reporta problemas de equipos al gerente inmediatamente

### Estándar de Calidad
El registro de temperatura está completo sin espacios. Todas las lecturas dentro del rango seguro.
```

### SOP de Servicio de Frente de Casa

```
## Estándares de Servicio al Cliente

**Aplica a:** Todo el personal de servidores y anfitriones

### Bienvenida (dentro de 30 segundos de asiento)
1. Acércate a la mesa con una sonrisa
2. Preséntate por tu nombre
3. Ofrece agua e informa sobre especiales
4. Pregunta si han estado aquí antes (si sí, bienvenido; si no, orientación breve)

### Toma de Pedido
1. Comienza con bebidas
2. Sugiere un aperitivo
3. Toma pedidos de plato principal, confirma modificaciones y alérgenos
4. Repite el pedido completo a la mesa
5. Ingresa pedido en POS inmediatamente (no hagas lotes de pedidos)

### Entrega de Alimentos
1. Entrega comida dentro de 2 minutos de que se platea en cocina
2. Anuncia cada plato por nombre conforme lo colocas
3. Confirma que la mesa tiene todo lo que necesita
4. Regresa dentro de 2 minutos de los primeros bocados

### Pago
1. Presenta la cuenta cuando se solicita (nunca antes)
2. Procesa el pago dentro de 3 minutos
3. Agradece al huésped por su nombre e invítalo a volver
```

---

## Fase 4: Pulir

### 1. Integración de Entrenamiento

- Imprime SOPs en formato de referencia rápida laminado para cada estación
- Usa SOPs durante el entrenamiento de nuevos empleados (lee, sombra, practica, solo)
- Prueba a nuevos empleados en SOPs de seguridad alimentaria antes de trabajar sin supervisión
- Revisa SOPs en reuniones mensuales de personal

### 2. Cronograma de Auditoría

| Área de SOP | Frecuencia de Auditoría | Quién Audita |
|----------|----------------|-----------|
| Registros de seguridad alimentaria | Diariamente | Gerente de turno |
| Listas de verificación de apertura/cierre | Diariamente | Gerente de apertura/cierre |
| Estándares de servicio | Semanalmente (revisión aleatoria de mesa) | Gerente |
| Limpieza profunda | Mensualmente | Gerente + equipo |
| Revisión completa de SOP | Trimestralmente | Propietario/operador |

### 3. Lista de Verificación de Calidad

```
## Lista de Verificación de SOP de Restaurante

- [ ] Procedimientos de apertura documentados para gerente, cocina y FOH
- [ ] Procedimientos de cierre documentados con pasos de limpieza y cierre de caja
- [ ] SOPs de seguridad alimentaria cubren temperatura, almacenamiento, alérgenos y lavado de manos
- [ ] Estándares de servicio definen bienvenida, pedido, entrega y pago
- [ ] Cada SOP tiene una declaración de propósito y estándar de calidad
- [ ] Errores comunes listados con pasos de prevención
- [ ] SOPs están escritos para el miembro del equipo más nuevo (claro, específico)
- [ ] Versiones de referencia rápida disponibles en cada estación
- [ ] El plan de entrenamiento referencia explícitamente los SOPs
- [ ] Se establece cronograma de auditoría para revisiones diarias, semanales y mensuales
```

---

## Ejemplo

**Fragmento de SOP de cierre de cocina:**
```
## Procedimiento de Cierre de Cocina

1. Apaga todos los equipos de cocción (parrillas, freidoras, hornos)
2. Cubre y fecha todos los artículos de prep, almacena en cámara frigorífica (FIFO)
3. Limpia todas las superficies de cocción con desengrasante
4. Barre y trapea pisos de cocina
5. Vacía toda la basura y reemplaza bolsas
6. Sanitiza todas las tablas de corte y superficies de prep
7. Revisa temperaturas de cámara frigorífica y registra en hoja de cierre
8. Apaga campanas de extracción y luces de cocina
9. Notifica al gerente de cierre que la cocina está completa

**Estándar de calidad:** Un gerente inspecciona la cocina antes de que el personal de cierre se vaya. Cada superficie debe pasar una revisión visual y de contacto para limpieza.
```

---

## Anti-Patrones

- **SOPs que nadie lee** — si están enterrados en una carpeta en la oficina, no se seguirán. Colócalos en las estaciones.
- **Demasiado por SOP** — un procedimiento de apertura de 3 páginas se salta. Mantén cada SOP a una página o menos.
- **Instrucciones vagas** — "Limpia la cocina" no es un SOP. "Limpia todas las superficies de acero inoxidable con desengrasante, enjuaga y sanitiza" lo es.
- **Sin responsabilidad** — SOPs sin listas de verificación y auditorías son sugerencias. Construye firmas y revisiones.
- **Establecer y olvidar** — las operaciones cambian, los menús cambian, las regulaciones cambian. Revisa SOPs trimestralmente.

---

## Recuperación

- **El personal resiste a seguir SOPs:** Involucra al personal en escribir los procedimientos. El personal que ayuda a crear los SOPs es más probable que los siga.
- **Los SOPs están desactualizados:** Programa una revisión trimestral de SOP. Asigna una categoría de SOP a cada gerente para actualizaciones.
- **La inspección de salud encuentra problemas:** Actualiza el SOP de seguridad alimentaria relevante inmediatamente. Reentena a todo el personal dentro de 48 horas.
- **El personal nuevo comete errores repetidos:** El SOP es poco claro. Reescribe la sección causando errores y añade el error a la sección "Errores Comunes".
