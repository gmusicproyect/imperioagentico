---
name: sop-gestion-propiedad
description: "Construye SOPs gestión propiedad para solicitudes mantenimiento, inspecciones, recopilación alquiler y comunicación inquilino."
allowed-tools: Read Write Glob
metadata:
  author: Imperio Digital
  version: "1.0"
---

# SOP Gestión Propiedad

## Cuándo Usar Este Skill

Usa este skill cuando necesites:
- Crear procedimientos operativos estándar gestión propiedades alquiler
- Sistematizar solicitudes mantenimiento, inspecciones y recopilación alquiler
- Construir plantillas comunicación inquilino situaciones comunes
- Documentar procesos gestión propiedad consistente a escala

**NO USES** este skill para análisis adquisición propiedad, gestión construcción o documentos gobernanza HOA. Esto es para operaciones gestión propiedad alquiler día-a-día.

---

## Principio Fundamental

PROCESOS CONSISTENTES GESTIÓN PROPIEDAD PROTEGEN INVERSIÓN, MANTIENEN INQUILINOS FELICES Y REDUCEN EMERGENCIAS — DOCUMENTAR CADA PROCEDIMIENTO ASEGURA NADA CAE A TRAVÉS GRIETAS.

---

## Fase 1: Alcance SOP

### Entradas Requeridas

| Entrada | Qué Preguntar | Predeterminado |
|-------|------------|---------|
| **Número propiedades** | "¿Cuántas unidades alquiler gestionas?" | 1-5 unidades |
| **Tipos propiedad** | "¿Single-family, multi-family, o mixta?" | Single-family |
| **Auto-gestionado o equipo** | "¿Gestionas solo o con equipo/VA?" | Auto-gestionado |
| **Puntos dolor actuales** | "¿Qué tareas gestión propiedad causan problemas?" | Coordinación mantenimiento y recopilación alquiler |
| **Herramientas usadas** | "¿Qué software usas — Buildium, AppFolio, hojas cálculo?" | Hojas cálculo y email |

**PUNTO DE CONTROL:** Confirma alcance y puntos dolor antes construir SOPs.

---

## Fase 2: SOPs Núcleo

### SOP 1: Recopilación Alquiler

```
## SOP Recopilación Alquiler

**Alquiler vence:** 1º mes
**Período gracia:** [3-5] días
**Tarifa morosidad:** $[cantidad] o [X]% alquiler mensual

### Proceso:
1. Alquiler vence 1º — sin acción si se recibe tiempo
2. Día 2: Sin recibir, envía recordatorio amable vía texto/email
3. Día [período gracia + 1]: Aplica tarifa morosidad, envía aviso formal morosidad
4. Día 10: Llamada para discutir plan pago si es necesario
5. Día 15: Envía aviso pagar-o-desocupar (consulta requisitos locales)
6. Día 30+: Comienza procedimientos desalojo sin pago o arreglo

### Plantilla Recordatorio:
"Hola [Nombre], recordatorio amable que alquiler de $[cantidad] venció
[fecha]. Envía pago lo antes posible. Déjame saber si tienes preguntas."

### Plantilla Aviso Morosidad:
"Estimado [Nombre], al [fecha], tu pago alquiler de $[cantidad] no se recibió.
Tarifa morosidad de $[cantidad] aplicada por tu acuerdo arrendamiento.
Cantidad total vencida: $[alquiler + tarifa morosidad]. Envía pago antes [fecha]."
```

### SOP 2: Solicitudes Mantenimiento

```
## SOP Solicitudes Mantenimiento

### Recibimiento Solicitudes:
- Inquilinos envían solicitudes vía [email/portal/texto]
- Todas solicitudes registradas con fecha, descripción unidad
- Reconocimiento recibido dentro [4] horas

### Niveles Prioridad:
| Prioridad | Tiempo Respuesta | Ejemplos |
|----------|--------------|---------|
| Emergencia | Dentro 2 horas | Fuga agua, sin calor invierno, olor gas, lockout |
| Urgente | Dentro 24 horas | Electrodoméstico roto, AC falla verano, problema plomería |
| Rutina | Dentro 3-5 días | Reparaciones cosméticas, problemas fixture menores |
| Programado | Próximo ciclo inspección | Mejoras no urgentes, pintura |

### Proceso:
1. Recibe y registra solicitud
2. Evalúa nivel prioridad
3. Contacta inquilino con cronograma estimado
4. Envía vendor o programa visita personal
5. Completa reparación documenta (fotos, factura, notas)
6. Seguimiento inquilino confirma resolución
7. Archiva documentación actualiza log mantenimiento
```

---

## Fase 3: Comunicación Inquilino

### Plantillas Comunicación

**Aviso Renovación Arrendamiento (60-90 días antes vencimiento):**
```
Estimado [Nombre], tu arrendamiento en [dirección] vence [fecha]. Nos gustaría
ofrecer renovación a $[alquiler nuevo]/mes por [término]. Confírma antes [fecha]
si deseas renovar. Si planeas mudarte, proporciona [30/60] días aviso escrito.
```

**Finalización Mantenimiento:**
```
Hola [Nombre], [tipo reparación] en tu unidad completado al [fecha].
Déjame saber si problema completamente resuelto o si notas problemas adicionales.
Gracias paciencia.
```

**Aviso Violación Arrendamiento:**
```
Estimado [Nombre], durante inspección reciente/observación, identificamos
[violación específica] en [dirección]. Por Sección [X] tu acuerdo arrendamiento,
[describe requisito]. Favor [acción correctiva] dentro [X] días. Preguntas, contáctanos.
```

---

## Anti-Patrones

- **Sin documentación** — acuerdos verbales y gestión basada memoria crean responsabilidad legal y caos operacional.
- **Enforcement inconsistente** — aplicar reglas diferentemente entre inquilinos invita denuncias vivienda justa.
- **Ignorar solicitudes mantenimiento** — reparaciones atrasadas escalan problemas caros y rotación inquilino.
- **Sin plan emergencia** — no saber quién llamar 2 AM fuga agua cuesta tiempo dinero.
- **Saltarse inspecciones** — problemas pequeños atrapados temprano previenen gastos mayores después.

---

## Recuperación

- **Heredaste propiedad mal gestionada:** Realiza inspección completa, documenta condiciones actuales introduce SOPs próximo ciclo arrendamiento.
- **Inquilino rechaza acceso inspección:** Referencia cláusula arrendamiento permitiendo inspecciones con aviso apropiado. Documenta rechazo escrito.
- **Pagadores crónicos atrasados:** Enforcement tarifas morosidad consistentemente. Ofrece configuración auto-pago. Si continúa, considera no-renovación vencimiento arrendamiento.
- **Problemas calidad vendor:** Construye roster 2-3 vendors por especialidad. Obtén múltiples cotizaciones, verifica referencias antes agregar lista.
- **Escalando más self-gestión:** Transición software gestión propiedad considera contratar VA o gestión propiedad profesional superas 10 unidades.
