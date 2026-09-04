---
name: plan-retiro-producto
description: "Crea planes de comunicación de retiro de producto con notificación de cliente, procedimientos de retorno y estrategias de gestión de reputación."
allowed-tools: Read Write Glob
metadata:
  author: Imperio Digital
  version: "1.0"
---

# Plan de Retiro de Producto

## Cuándo Usar Este Skill

Usa este skill cuando necesites:
- Redactar un plan de comunicación para retiro de producto o problema de seguridad
- Crear plantillas de notificación al cliente para productos defectuosos o peligrosos
- Construir procedimientos de retorno y reembolso para artículos retirados
- Planificar gestión de reputación durante y después de evento de retiro

**NO USES** este skill para devoluciones rutinarias de producto, reclamaciones de garantía o discontinuaciones voluntarias de producto. Esto es para retiros relacionados con seguridad o calidad que requieren comunicación estructurada.

---

## Principio Fundamental

LA VELOCIDAD Y TRANSPARENCIA GANAN CONFIANZA DURANTE UN RETIRO — CADA HORA DE RETRASO O AMBIGÜEDAD COMPONE DAÑO REPUTACIONAL Y RIESGO LEGAL.

---

## Fase 1: Evaluación de Retiro

Reúne hechos antes de redactar cualquier comunicación.

### Entradas Requeridas

| Entrada | Qué Preguntar | Predeterminado |
|-------|------------|---------|
| **Producto afectado** | "¿Qué producto se retira? Incluye SKU, lote o rango de fechas." | Sin predeterminado — debe proporcionarse |
| **Descripción del problema** | "¿Cuál es el defecto o preocupación de seguridad?" | Sin predeterminado — debe proporcionarse |
| **Nivel de severidad** | "¿Es peligro de seguridad, defecto de calidad o problema de cumplimiento regulatorio?" | Defecto de calidad |
| **Unidades vendidas** | "¿Cuántas unidades se afectan y a través de qué canales?" | Desconocido — planifica para notificación amplia |
| **Estado actual** | "¿Ha habido lesiones o quejas presentadas? ¿Contacto regulatorio?" | No se conocen lesiones ni quejas |

### Resumen de Evaluación

```
## Evaluación de Retiro

**Producto:** Taza de viaje cerámica — Modelo TM-200, manufacturado marzo-mayo 2024
**Problema:** Grietas finas en asa que pueden causar rotura durante uso con líquidos calientes
**Severidad:** Peligro de seguridad — riesgo de quemaduras
**Unidades afectadas:** ~2,400 unidades vendidas vía sitio web y 3 socios retail
**Incidentes conocidos:** 2 quejas de clientes, sin lesiones reportadas
**Estado regulatorio:** Sin contacto CPSC aún — retiro voluntario recomendado
```

**PUNTO DE CONTROL:** Confirma todos los hechos con el usuario antes de redactar comunicaciones. Avisos de retiro inexactos crean responsabilidad legal.

---

## Fase 2: Plan de Comunicación

### Secuencia de Notificación

Construye comunicaciones en este orden:

1. **Alerta interna** (Día 0) — notifica equipo, pausa ventas, retira inventario
2. **Notificación de socio retail** (Día 0-1) — alerta distribuidores y minoristas para retirar producto
3. **Notificación de cliente** (Día 1-2) — email, banner de sitio web, post en redes sociales
4. **Presentación regulatoria** (si es requerida) — reporte CPSC, aviso FDA, o agencia relevante
5. **Comunicado de prensa** (si es necesario) — comunicado preparado para consultas de medios

### Plantilla de Notificación del Cliente

```
Asunto: Aviso Importante de Seguridad — [Nombre de Producto] Retiro

Estimado [Nombre del Cliente],

Estamos retirando voluntariamente [Nombre de Producto] ([detalles modelo/lote]) debido a [descripción breve y clara del problema].

**Lo que debes hacer:**
1. Detén el uso del producto inmediatamente
2. [Instrucciones específicas de retorno]
3. [Cómo recibir reembolso/reemplazo]

**Cómo devolver:**
- [Método de retorno — etiqueta prepago, ubicación de entrega o recogida]
- [Cronograma para procesar reembolso/reemplazo]

Nos disculpamos sinceramente por cualquier inconveniente. Tu seguridad es nuestra prioridad principal.

¿Preguntas? Contáctanos en [email] o [teléfono] — nuestro equipo está disponible [horas].

[Nombre de Empresa]
```

### Comunicaciones Específicas por Canal

- **Email** — notificación directa a todos los clientes que compraron el producto afectado
- **Sitio web** — banner en página principal + página dedicada de retiro con FAQ
- **Redes sociales** — anuncio breve enlazando a página de retiro
- **Señalización en tienda** — si se vende a través de socios retail

---

## Fase 3: Procedimientos de Retorno y Resolución

### Proceso de Retorno

Define el proceso paso a paso:

1. El cliente contacta al soporte o visita página de retiro
2. Verifica compra (número de orden, foto de producto o comprobante de compra)
3. Proporciona etiqueta de retorno prepago o instrucciones de disposición
4. Procesa reembolso o envía reemplazo dentro de [X] días hábiles
5. Confirma resolución con follow-up email

### Opciones de Resolución

Ofrece al menos dos opciones:
- **Reembolso completo** — sin preguntas, procesado a método de pago original
- **Reemplazo** — producto corregido enviado gratis, con opción expedita
- **Crédito tienda + bonificación** — 110-120% del precio de compra como crédito (incentiva retención)

### Script del Equipo de Soporte

Prepara puntos clave para servicio al cliente:
- Reconoce el problema sin esquivarlo
- Explica exactamente qué salió mal en lenguaje simple
- Camina a través de pasos de retorno/reembolso claramente
- No especules sobre causas más allá de la declaración oficial
- Camino de escalada para clientes enojados o reportes de lesiones

---

## Fase 4: Gestión de Reputación

### Acciones Inmediatas

- Publica un post de blog transparente o carta del fundador explicando el problema y arreglo
- Responde a cada comentario en redes sociales y reseña sobre el retiro dentro de 4 horas
- Actualiza listados de producto para reflejar estado de retiro

### Cronograma de Recuperación

| Período de Tiempo | Acción |
|-----------|--------|
| Semana 1 | Ejecuta retiro, maneja devoluciones, monitorea sentimiento |
| Semanas 2-3 | Comparte detrás de cámaras del arreglo de calidad con clientes |
| Mes 2 | Relanza producto corregido con historia de aseguramiento de calidad |
| Mes 3 | Seguimiento con clientes afectados — oferta de lealtad o vista previa exclusiva |

### Monitoreo

- Rastrea tasa de finalización de retiro (objetivo: 80%+ de unidades afectadas devueltas o contabilizadas)
- Monitorea menciones de marca y sentimiento diariamente durante 30 días
- Documenta todo para protección legal

---

## Anti-Patrones

- **Minimizar el problema** — lenguaje vago como "por abundancia de precaución" cuando hay riesgo real de seguridad erosiona confianza.
- **Notificación lenta** — esperar días para notificar clientes después de descubrir el problema multiplica pasivos.
- **Hacer devoluciones difíciles** — requerir recibos, empaque original o formas complejas reduce cumplimiento e incrementa enojo.
- **Silencio después del retiro** — no hacer seguimiento da la impresión de que estás ocultando.
- **Culpar proveedores públicamente** — maneja responsabilidad de cadena de suministro internamente, no en comunicaciones de cliente.
- **Sin página de retiro dedicada** — enviar clientes a página de soporte genérica crea confusión.

---

## Recuperación

- **Número desconocido de unidades afectadas:** Usa registros de compra y estima conservadoramente. Sobre-comunica en lugar de sub-notificar.
- **Sin lista de email de cliente:** Usa redes sociales, banners de sitio web, redes de socios retail y alcance a prensa para llegar a compradores.
- **Incertidumbre regulatoria:** Cuando dudes, consulta abogado de responsabilidad de producto. Erra en el lado de reportar voluntariamente.
- **Reacción negativa en redes sociales:** Responde con empatía y hechos. No elimines comentarios negativos — abórdales públicamente.
- **Problema repetido después del arreglo:** Escala procedimientos de control de calidad y considera auditoría de terceros antes de relanzar.
