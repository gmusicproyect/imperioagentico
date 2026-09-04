---
name: venta-transfronteriza
description: "Planifica estrategias de venta internacional con localización, envíos, aranceles/impuestos y consideraciones de cumplimiento."
allowed-tools: Read Write Glob
metadata:
  author: Imperio Digital
  version: "1.0"
---

# Venta Transfronteriza

## Cuándo Usar Este Skill

Usa este skill cuando necesites:
- Expandir tu negocio de e-commerce a mercados internacionales
- Planificar estrategia de localización para listados de productos, precios y experiencia del cliente
- Navegar logística de envío, aranceles e impuestos para órdenes transfronterizas
- Asegurar cumplimiento con regulaciones de venta internacional

**NO USES** este skill para expansión doméstica, compras mayoristas/de importación, o establecer presencia retail física en el extranjero. Esto es para vendedores en línea que envían productos internacionalmente.

---

## Principio Fundamental

LA VENTA INTERNACIONAL NO ES SOLO AGREGAR PAÍSES A TUS ZONAS DE ENVÍO — REQUIERE PRECIOS LOCALIZADOS, EXPECTATIVAS CLARAS SOBRE ARANCELES Y CONSTRUCCIÓN DE CONFIANZA PARA COMPRADORES QUE NO PUEDEN TOCAR TU PRODUCTO.

---

## Fase 1: Evaluación de Mercado

### Entradas Requeridas

| Entrada | Qué Preguntar | Predeterminado |
|-------|------------|---------|
| **Mercado actual** | "¿Dónde vendes ahora?" | Estados Unidos |
| **Mercados objetivo** | "¿A qué países o regiones quieres vender?" | Sin predeterminado — debe proporcionarse |
| **Categoría de producto** | "¿Qué vendes? ¿Hay artículos restringidos o regulados?" | Sin predeterminado — debe proporcionarse |
| **Valor de orden promedio** | "¿Cuál es tu valor de orden típico?" | $50-100 |
| **Órdenes internacionales actuales** | "¿Ya recibes consultas u órdenes internacionales?" | Ocasionalmente, pero sin enfoque estructurado |

**PUNTO DE CONTROL:** Confirma mercados objetivo y detalles de producto antes de planificar.

---

## Fase 2: Estrategia de Localización

### Localización de Precios

- Muestra precios en moneda local — usa conversión dinámica o fija precios locales
- Cuenta para costos de envío, aranceles e impuestos en el precio mostrado o divúlgalos claramente
- Considera poder adquisitivo — un producto de $50 en EE.UU. puede necesitar posicionamiento diferente en otros mercados
- Redondea precios según convenciones locales (ej. .99 en EE.UU., .00 en algunos mercados europeos)

### Localización de Sitio Web y Listados

| Elemento | Acción |
|---------|--------|
| Idioma | Traduce páginas clave (producto, checkout, FAQ, devoluciones) — no confíes en auto-traducción |
| Medidas | Convierte a sistema métrico para mercados no estadounidenses |
| Formatos de fecha | Usa DD/MM/YYYY para la mayoría de mercados internacionales |
| Métodos de pago | Agrega opciones locales (iDEAL para Países Bajos, Klarna para UE, etc.) |
| Señales de confianza | Muestra insignias de confianza locales, reseñas de compradores locales |

### Prioridades de Entrada a Mercados

Clasifica mercados objetivo por estos criterios:
1. **Demanda existente** — ¿Ya recibes tráfico o consultas de este mercado?
2. **Viabilidad de envío** — ¿Puedes enviar allí de manera confiable y asequible?
3. **Nivel de competencia** — ¿El mercado está desatendido para tu categoría de producto?
4. **Complejidad regulatoria** — ¿Qué tan difícil es el cumplimiento?
5. **Barrera de idioma** — ¿Puedes soportar clientes en su idioma?

---

## Fase 3: Envío y Aranceles

### Opciones de Envío

| Método | Velocidad | Costo | Mejor Para |
|--------|-------|------|----------|
| Correo internacional estándar | 2-4 semanas | Bajo | Artículos de bajo valor, prueba de mercados |
| Envío express internacional (DHL, FedEx, UPS) | 3-7 días | Alto | Artículos de alto valor, experiencia premium |
| Centro de cumplimiento regional | 2-5 días | Medio | Mercados de alto volumen (usa 3PL en el país) |
| Cumplimiento de marketplace (FBA, etc.) | 1-3 días | Medio | Ya vendiendo en ese marketplace |

### Marco de Aranceles y Impuestos

```
## Consideraciones de Aranceles e Impuestos

**DDP vs. DDU:**
- DDP (Entrega con Derechos Pagados) — pagas aranceles por adelantado, cliente sin sorpresas ✓
- DDU (Entrega con Derechos No Pagados) — cliente paga aranceles en la entrega, causa rechazos y quejas ✗

**Umbrales clave (ejemplos — verifica tasas actuales):**
- UE: IVA en todos los bienes, IOSS para artículos bajo €150
- Reino Unido: IVA en todos los bienes, arancel en artículos sobre £135
- Canadá: De minimis $20 CAD (muy bajo — la mayoría de órdenes incurren arancel)
- Australia: GST en todos los bienes vendidos por proveedores extranjeros con ingresos $75K+ AUD

**Códigos HS:** Clasifica productos con códigos del Sistema Armonizado correctos para cálculo preciso de aranceles
```

### Documentación Aduanal

Cada envío internacional necesita:
- Factura comercial con descripción de producto, valor y código HS
- Marcado de país de origen en el producto
- Formulario de declaración aduanal
- Cualquier certificado requerido (FDA, marca CE, etc.)

---

## Fase 4: Cumplimiento y Operaciones

### Lista de Verificación Regulatoria

- [ ] Producto cumple con estándares de seguridad del país destino
- [ ] Etiquetado cumple con requisitos de idioma y contenido local
- [ ] Sin artículos prohibidos o restringidos para mercados objetivo
- [ ] Registro fiscal completado donde sea requerido (IVA, GST, etc.)
- [ ] Política de privacidad cumple con leyes de datos locales (GDPR para UE)
- [ ] Política de devolución cuenta para costos de envío internacional

### Experiencia del Cliente

- Proporciona tiempos de entrega estimados por región en páginas de producto
- Ofrece rastreo de envío para todas las órdenes internacionales
- Crea página de FAQ de envío internacional
- Configura horas de servicio al cliente que se superponen con zonas horarias de mercados objetivo
- Ten un plan para manejar devoluciones de clientes internacionales

### Métricas Clave

| Métrica | Objetivo |
|--------|--------|
| Ingresos internacionales como % del total | 10-30% dentro del primer año |
| Tasa de devolución de orden internacional | Bajo 5% |
| Tasa de problema de despacho aduanal | Bajo 2% de envíos |
| Satisfacción del cliente por mercado | En línea con clasificaciones domésticas |

---

## Anti-Patrones

- **Envío DDU esperando lo mejor** — cargos de arancel sorpresa causan rechazos, devoluciones y clientes enojados. Usa DDP cuando sea posible.
- **Ignorar requisitos de registro fiscal** — muchos países ahora requieren que vendedores extranjeros se registren y recopilen IVA/GST.
- **Auto-traducir todo** — la traducción automática sin revisión crea páginas de producto embarazosas o confusas.
- **Precios iguales globalmente** — no contabilizar envío, aranceles y poder adquisitivo local lleva a precios no competitivos.
- **Sin política de devolución internacional** — los compradores no comprarán si no pueden devolver. Crea un proceso claro de devoluciones internacionales.

---

## Recuperación

- **Aduanas retiene o confisca envíos:** Asegura que códigos HS sean precisos, facturas comerciales completas y productos cumplan. Contacta al transportista para resolución.
- **Tasas de devolución altas de un mercado:** Investiga — puede ser confusión de tamaño, sorpresa de arancel o tiempos de entrega largos. Arregla la causa raíz.
- **Confusión de cumplimiento fiscal:** Consulta especialista en impuestos transfronterizos. Para UE, regístrate en IOSS. Para Reino Unido, regístrate para IVA si superas umbral.
- **Costos de envío demasiado altos:** Negocia tasas de volumen con transportistas, considera cumplimiento regional, o establece valores mínimos de orden para envío internacional.
- **Baja conversión desde tráfico internacional:** Agrega moneda local, métodos de pago y señales de confianza. Destaca reseñas de compradores en ese mercado.
