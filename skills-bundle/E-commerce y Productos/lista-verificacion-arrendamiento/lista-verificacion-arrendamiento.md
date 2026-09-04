---
name: lista-verificacion-arrendamiento
description: "Crea listas verificación revisión arrendamiento asegurando todos términos esenciales, revelaciones y anexos incluidos."
allowed-tools: Read Write Glob
metadata:
  author: Imperio Digital
  version: "1.0"
---

# Lista de Verificación Arrendamiento

## Cuándo Usar Este Skill

Usa este skill cuando necesites:
- Revisar acuerdo arrendamiento residencial completitud antes firmar
- Asegurar todos términos esenciales, revelaciones y anexos incluidos
- Identificar cláusulas faltantes que podrían crear problemas durante inquilinato
- Crear lista de verificación estandarizada para preparación arrendamiento consistente

**NO USES** este skill para redactar arrendamientos desde cero, revisión arrendamiento comercial o asesoría legal. Esto es lista de verificación completitud — siempre consulta abogado revisión legal.

---

## Principio Fundamental

UN ARRENDAMIENTO COMPLETO PROTEGE TANTO PROPIETARIO COMO INQUILINO — CADA CLÁUSULA FALTANTE ES DISPUTA POTENCIAL ESPERANDO PASAR.

---

## Fase 1: Contexto Arrendamiento

### Entradas Requeridas

| Entrada | Qué Preguntar | Predeterminado |
|-------|------------|---------|
| **Rol** | "¿Eres propietario o inquilino revisando arrendamiento?" | Propietario |
| **Estado** | "¿Qué estado está propiedad?" | Sin predeterminado — ley estatal afecta requisitos |
| **Tipo propiedad** | "¿Single-family, apartamento, condo, duplex?" | Single-family |
| **Tipo arrendamiento** | "¿Plazo fijo o mes-a-mes?" | Plazo fijo 12 meses |
| **Circunstancias especiales** | "¿Términos inusuales — amueblado, servicios incluidos, compañeros, mascotas?" | Standard sin amueblar |

**PUNTO DE CONTROL:** Confirma rol y jurisdicción antes aplicar lista de verificación.

---

## Fase 2: Lista de Verificación Términos Esenciales

### Información Partes y Propiedad

- [ ] Nombres legales completos todos inquilinos (adultos)
- [ ] Nombre legal propietario/compañía gestión y contacto
- [ ] Dirección propiedad completa incluyendo número unidad
- [ ] Fecha inicio arrendamiento fecha final
- [ ] Fecha mudanza (si diferente inicio arrendamiento)

### Términos Financieros

- [ ] Monto alquiler mensual
- [ ] Fecha vencimiento alquiler (típicamente 1º mes)
- [ ] Métodos pago aceptados
- [ ] Período gracia especificado (número días)
- [ ] Monto tarifa morosidad cuándo aplica
- [ ] Monto depósito seguridad
- [ ] Cronograma retorno depósito seguridad y condiciones
- [ ] Cualquier tarifa no reembolsable (solicitud, limpieza, admin)
- [ ] Alquiler prorrateado primer/último mes parcial (si aplica)
- [ ] Términos aumento alquiler y requisitos aviso

### Ocupación y Uso

- [ ] Número máximo ocupantes
- [ ] Política huéspedes y limitaciones
- [ ] Uso permitido (solo residencial)
- [ ] Restricciones negocios hogar
- [ ] Política subarrendamiento y cesión
- [ ] Restricciones horas silencio o ruido

---

## Fase 3: Políticas y Responsabilidades

### Mantenimiento y Reparaciones

- [ ] Responsabilidades mantenimiento propietario definidas
- [ ] Responsabilidades mantenimiento inquilino definidas
- [ ] Procedimiento solicitud mantenimiento (cómo enviar)
- [ ] Contacto mantenimiento emergencia y procedimiento
- [ ] Mantenimiento patio, remoción nieve asignado
- [ ] Responsabilidad inquilino por daño más allá desgaste normal

### Servicios Públicos

- [ ] Qué servicios públicos paga propietario
- [ ] Qué servicios públicos paga inquilino
- [ ] Responsabilidad transferencia servicio público y cronograma
- [ ] Arreglos servicios públicos compartidos (si multi-unidad)

### Mascotas

- [ ] Política mascotas claramente establecida (permitidas/no permitidas)
- [ ] Monto depósito mascotas o tarifa
- [ ] Alquiler mensual mascotas (si aplica)
- [ ] Restricciones raza, tamaño número
- [ ] Responsabilidad daño mascotas

### Seguros

- [ ] Requisito seguro inquilino establecido
- [ ] Monto cobertura mínimo especificado
- [ ] Plazo comprobante seguro
- [ ] Propietario nombrado como parte interesada (si requerida)

---

## Fase 4: Protecciones Legales y Anexos

### Terminación y Renovación

- [ ] Cláusula terminación anticipada y sanciones
- [ ] Opción rescisión arrendamiento o buyout
- [ ] Período aviso mudanza (30/60 días)
- [ ] Términos renovación (renovación auto, conversión mes-a-mes o vencimiento)
- [ ] Derecho propietario terminación y aviso requerido
- [ ] Procedimiento inspección mudanza
- [ ] Documentación condición propiedad (mudanza-entrada/mudanza-salida)

### Revelaciones Requeridas (Verificar por Estado)

- [ ] Revelación pintura base plomo (propiedades pre-1978 — requisito federal)
- [ ] Revelación moho (donde requerida)
- [ ] Revelación chinche cama (donde requerida)
- [ ] Notificación registro delincuente sexual
- [ ] Revelación zona inundable
- [ ] Defectos conocidos o peligros
- [ ] Revelación asbesto (donde requerida)
- [ ] Revelación servicios públicos compartidos (donde requerida)

### Anexos Comunes

- [ ] Reporte condición mudanza-entrada/mudanza-salida
- [ ] Anexo mascotas (si mascotas permitidas)
- [ ] Anexo estacionamiento (espacios asignados, reglas)
- [ ] Anexo política no fumar
- [ ] Anexo prevención moho
- [ ] Apéndice reglas HOA (si aplica)
- [ ] Lista inventario electrodomésticos
- [ ] Inventario llaves/dispositivos acceso

### Firmas y Ejecución

- [ ] Todos inquilinos adultos han firmado
- [ ] Propietario o agente autorizado ha firmado
- [ ] Fecha ejecución
- [ ] Copias proporcionadas todas partes
- [ ] Todos anexos inicialados y adjuntos

---

## Plantilla Resumen Revisión

```
## Resumen Revisión Arrendamiento

**Propiedad:** [Dirección]
**Revisado por:** [Nombre]
**Fecha:** [Fecha]

### Estado: [Completo / Artículos Faltantes / Necesita Revisión Legal]

### Artículos Faltantes o Incompletos:
1. [Artículo] — [Por qué importa]
2. [Artículo] — [Por qué importa]

### Artículos Necesitando Clarificación:
1. [Cláusula] — [Qué no está claro]

### Recomendaciones:
- [Artículo acción 1]
- [Artículo acción 2]
```

---

## Anti-Patrones

- **Usar plantilla genérica online sin personalización estatal** — leyes arrendamiento varían dramáticamente estado e incluso ciudad. Plantillas genéricas pierden disposiciones requeridas locales.
- **Sin reporte condición mudanza-entrada** — sin documentación condición propiedad mudanza-entrada, disputas depósito seguridad son irresolubles.
- **Responsabilidades mantenimiento vagas** — "Inquilino responsable por mantenimiento" sin especificidades lleva desacuerdos.
- **Revelaciones faltantes** — no incluir revelaciones requeridas puede anular disposiciones arrendamiento o crear responsabilidad legal.
- **Sin cláusula terminación anticipada** — vida pasa. Tener proceso buyout claro es mejor que incumplimiento desordenado.

---

## Recuperación

- **Arrendamiento ya firmado con términos faltantes:** Crea anexo cubriendo artículos faltantes. Ambas partes firman.
- **Requisitos específicos estado desconocidos:** Investiga estatutos propietario-inquilino tu estado o consulta abogado inmobiliario local.
- **Inquilino disputa término arrendamiento:** Referencia cláusula específica. Si cláusula genuinamente ambigua, negocia interpretación razonable documenta.
- **Usando plantilla arrendamiento desactualizada:** Revisa actualiza anualmente. Leyes cambian y arrendamiento debe reflejar requisitos actuales.
- **Múltiples propiedades con diferentes versiones arrendamiento:** Estandariza una plantilla por tipo propiedad y jurisdicción. Personaliza solo detalles específicos propiedad.
