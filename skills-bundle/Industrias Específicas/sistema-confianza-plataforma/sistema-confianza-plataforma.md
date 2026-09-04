---
name: sistema-confianza-plataforma
description: "Diseña sistemas de confianza y seguridad con políticas de revisión, resolución de disputas, y medidas de prevención de fraude. Usar cuando se construye infraestructura de confianza para plataformas de mercado."
allowed-tools: Read Write Glob
metadata:
  author: Imperio Digital
  version: "1.0"
---

# Sistema de Confianza de Plataforma

## Cuándo Usar Esta Habilidad

Usa esta habilidad cuando necesites:
- Diseñar un sistema de confianza y seguridad para una plataforma de mercado
- Crear políticas de revisión y calificación que construyan confianza
- Crear workflows de resolución de disputas para conflictos comprador-vendedor
- Implementar medidas de prevención de fraude y disparadores de detección

**NO** uses esta habilidad para configuración de procesamiento de pagos, cumplimiento legal (consulta un abogado), o ticketing de servicio al cliente. Esto es para diseño de infraestructura de confianza.

---

## Principio Fundamental

LA CONFIANZA ES LA MONEDA DE LOS MERCADOS — SIN ELLA, LOS COMPRADORES NO PAGARÁN Y LOS VENDEDORES NO LISTARÁN. CONSTRUYE CONFIANZA EN CADA PUNTO DE CONTACTO DE TRANSACCIÓN.

---

## Fase 1: Resumen

### Información Requerida

| Información | Qué Preguntar | Predeterminado |
|-------|------------|---------|
| **Tipo de plataforma** | "¿Qué conecta tu mercado? Productos, servicios, alquileres?" | Sin predeterminado — debe proporcionarse |
| **Valor de transacción** | "¿Cuál es el valor de transacción promedio?" | Menos de $500 |
| **Problemas actuales** | "¿Qué problemas de confianza enfrentas? Fraude, disputas, reseñas falsas?" | Diseño desde cero |
| **Tolerancia de riesgo** | "¿Qué tan estricta debe ser verificación y moderación?" | Moderada — balancea confianza con facilidad de uso |
| **Tamaño del equipo de moderación** | "¿Quién maneja disputas y moderación?" | Fundador en solitario |

**PUNTO DE CONTROL: Confirma el resumen antes de diseñar el sistema.**

---

## Fase 2: Diseña Arquitectura de Confianza

### Tres Pilares de Confianza de Plataforma

**1. Prevención** — Detiene actores malos antes de que transaccionen
**2. Detección** — Identifica problemas mientras suceden
**3. Resolución** — Maneja disputas justa y rápidamente

### Capa de Prevención

| Mecanismo | Descripción |
|-----------|-------------|
| **Verificación de identidad** | Requiere ID o verificación de negocio para vendedores |
| **Completitud de perfil** | Señales de mayor confianza para perfiles completos (foto, bio, credenciales) |
| **Verificación de pago** | Método de pago verificado antes de transaccionar |
| **Moderación de contenido** | Revisa listados antes de que vayan en vivo (o spot-check) |
| **Límites de usuario nuevo** | Limita volumen de transacción o listados para cuentas nuevas |

### Capa de Detección

| Señal | Acción |
|--------|--------|
| Múltiples cuentas desde mismo IP/dispositivo | Reporta para revisión |
| Pico repentino en listados o transacciones | Suspensión automatizada |
| Reportes de comprador dentro de las primeras 24 horas | Revisión de prioridad |
| Mensajería contiene links de pago fuera de plataforma | Bloqueo de mensaje automático |
| Patrones de revisión sugieren manipulación | Reporta e investiga |

### Capa de Resolución

Ver Fase 3 para flujo de resolución de disputas detallado.

**PUNTO DE CONTROL: Confirma el enfoque de tres pilares antes de escribir políticas.**

---

## Fase 3: Escribe Políticas de Confianza

### Sistema de Revisión y Calificación

**Elegibilidad de revisión:** Solo usuarios que completaron una transacción pueden dejar revisión
**Ventana de revisión:** 14 días después de completación de transacción
**Formato de revisión:** Calificación de estrellas (1-5) + revisión escrita (mínimo 20 caracteres)
**Respuesta:** Los vendedores pueden responder públicamente (una respuesta por revisión)

**Criterios de eliminación de revisión:**
- Contiene discurso de odio, amenazas, o información personal
- El revisor no completó una transacción
- La revisión es sobre la plataforma, no el vendedor/producto
- Se prueba que es fraudulenta o incentivada

**Las revisiones NO se eliminan por:**
- Ser negativas
- Contener crítica que el vendedor no está de acuerdo
- Calificaciones bajas

### Flujo de Resolución de Disputas

```
1. El comprador o vendedor abre una disputa
   ↓
2. Ambas partes proporcionan su versión (ventana de 48 horas cada una)
   ↓
3. La plataforma revisa evidencia (mensajes, registros de transacción, fotos)
   ↓
4. Decisión emitida dentro de 5 días hábiles
   ↓
5a. Se emite reembolso (parcial o completo)
5b. Disputa resuelta a favor del vendedor
5c. Oferta de compromiso
   ↓
6. Opción de apelación (una por disputa, revisada por miembro de equipo diferente)
```

**Evidencia aceptada:** Capturas de pantalla, mensajes en plataforma, fotos, números de rastreo, contratos

### Medidas de Prevención de Fraude

- **Monitoreo de transacción:** Reporta transacciones 3x por encima del promedio de categoría
- **Límites de velocidad de cuenta:** Nuevos vendedores limitados a 5 transacciones en primeros 14 días
- **Suspensiones de pago:** Pagos de vendedor por primera vez suspendidos por 7 días
- **Advertencia de comunicación fuera de plataforma:** Mensaje automatizado cuando usuarios comparten emails o números de teléfono
- **Rastreo de contracargo:** Vendedores con 3+ contracargos en 90 días enfrentan revisión de cuenta

---

## Fase 4: Pulir

### 1. Insignias de Confianza y Señales

Diseña indicadores de confianza visibles:
- **Insignia Verificada** — Completó verificación de identidad o negocio
- **Insignia Top Rated** — Promedio 4.8+ con 10+ reseñas
- **Insignia Quick Responder** — Responde dentro de 4 horas en promedio
- **Insignia Establecida** — Activo en plataforma durante 6+ meses
- **Icono de Protección del Comprador** — Mostrado en todas las transacciones

### 2. Dashboard de Métricas de Confianza

```
## Métricas de Salud de Confianza

- **Tasa de disputa:** % de transacciones que resultan en disputa (meta: menos de 2%)
- **Tiempo de resolución:** Promedio de días para resolver una disputa (meta: menos de 5)
- **Tasa de detección de fraude:** % de cuentas reportadas confirmadas como fraudulentas
- **Autenticidad de revisión:** % de reseñas verificadas como genuinas
- **Tasa de transacción repetida:** Proxy para confianza (mayor = más confianza)
- **Tasa de contracargo:** % de transacciones que resultan en contracargos (meta: menos de 0.5%)
```

### 3. Lista de Verificación de Calidad

```
## Lista de Verificación del Sistema de Confianza

- [ ] Proceso de verificación de identidad definido para vendedores
- [ ] Sistema de revisión permite solo participantes de transacción verificada
- [ ] Criterios de eliminación de revisión documentados y justos
- [ ] Flujo de resolución de disputas tiene pasos claros y cronogramas
- [ ] Señales de detección de fraude definidas y automatizadas donde es posible
- [ ] Límites de transacción de usuario nuevo están en su lugar
- [ ] Insignias de confianza definidas y criterios documentados
- [ ] Política de suspensión de pago documentada para vendedores nuevos
- [ ] Monitoreo de comunicación fuera de plataforma está activo
- [ ] Métricas de confianza se rastreen y revisen mensualmente
```

---

## Ejemplo

**Plataforma:** Mercado de servicios freelance

**Plantilla de respuesta de revisión para vendedores:**
"Agradezco tu feedback, [Nombre]. Aprecio que compartas tu experiencia. [Aborda punto específico]. He [mejora hecha desde entonces]. Espero entregar trabajo excelente para clientes futuros."

**Mensaje de resolución de disputas:**
"Hemos revisado ambos lados de esta disputa. Con base en el alcance del proyecto acordado en mensajes y los entregables proporcionados, hemos decidido emitir un reembolso del 50% al comprador. El vendedor entregó el trabajo central, pero las revisiones clave descritas en el acuerdo original no se completaron. Ambas partes pueden apelar dentro de 7 días."

---

## Anti-Patrones

- **Sin moderación de revisión** — las reseñas falsas destruyen la credibilidad del mercado. Monitorea y aplica políticas.
- **Resolución de disputas opaca** — si los usuarios no pueden ver el proceso, asumen que es injusto. Documenta y comunica cada paso.
- **Sobre-verificación** — requerir 5 documentos para listar un artículo mata el suministro. Verifica lo que importa para confianza, no burocracia.
- **Siempre favorecer compradores** — las políticas de siempre-reembolso atraen compradores fraudulentos y alejan vendedores. Sé justo con ambos lados.
- **Ignorar transacciones fuera de plataforma** — los usuarios que transacciona fuera de plataforma evitan honorarios y tus protecciones. Detecta y desalienta.

---

## Recuperación

- **Pico en disputas:** Identifica el patrón (vendedor específico, categoría, o comportamiento de comprador). Cierra verificación o estándares de listados en áreas afectadas.
- **Anillo de reseña falsa detectado:** Elimina todas las reseñas conectadas, suspende cuentas involucradas, y notifica vendedores/compradores afectados.
- **El vendedor se siente tratado injustamente en disputa:** Ofrece el proceso de apelación. Haz que una persona diferente revise. La transparencia previene escalación.
- **Sin recursos para moderación manual:** Prioriza detección automatizada y enfoca revisión manual solo en transacciones de alto riesgo.
