# Clase 17 — Media Buyer Agent en producción: personalización y research de competencia

**Tags:** `Meta MCP` `Personalización` `Competencia` `Browser`
**Conecta con:** Clase 14 · Clase 10 · Clase 07

---

## Idea central

Combinando el MCP de Meta con Claude Browser, Claude Code ejecuta el flujo completo de un media buyer: sube creativos como borrador para aprobación, lanza campañas hiper-personalizadas por país y hace research de competencia leyendo anuncios reales de la industria. Lo que antes exigía contratar a alguien por $1.000/mes ahora lo arma y opera una sola persona.

---

## Flujo seguro de publicación

| Paso | Detalle |
|------|---------|
| Sube como borrador | Nunca publicado directo — queda pendiente de tu aprobación |
| Presupuesto explícito | Se define en el prompt (ej. $50/día), nunca a criterio del agente |
| URL de destino | El agente la pide antes de confirmar la creación del creativo |
| Verificación manual | Entra al Ads Manager y confirma — que el agente diga "subido" no significa que se subió bien |

**Limitación actual:** el MCP de Meta no sube archivos de video (solo imágenes), aunque sí puede editar videos que ya están subidos en la cuenta.

---

## Personalización real por país

Un mismo anuncio ganador se convierte en variaciones específicas por mercado, cambiando idioma, modismos y creatividad para que resuene local — no una traducción literal:

```
Toma el anuncio ganador (ad #1) y crea 5 variaciones.
Crea además una campaña nueva dirigida solo a Chile, Argentina y España:
- Chile → español chileno
- Argentina → español argentino (modismos como "quilombo")
- España → español de España
El texto y el gráfico de cada una deben sentirse hechos para ese país,
no traducidos. Preséntalas como borrador con $50/día cada una.
```

---

## Research de competencia (Meta Ad Library + Browser)

```
1. Meta MCP busca en la Ad Library los anuncios activos de [marca de referencia]
2. Claude Browser abre cada anuncio para ver el creativo y la landing real
3. Se agrupan los anuncios por ángulo/gancho repetido
```

De 697 anuncios de un solo negocio, este proceso los redujo a 4 ángulos core. La lógica: si una marca ya gastó millones probando, no hay que reinventar — se adapta ese ángulo probado al propio negocio.

---

## Qué puede y qué no puede hacer el MCP de Meta

| Puede | No puede |
|-------|----------|
| Analizar insights y detectar anomalías | Subir archivos de video |
| Encontrar oportunidades de campaña | Cambiar métodos de pago |
| Investigar competencia (Ad Library) | Cualquier acción fuera de publicidad |

---

## 🎯 Ejercicio práctico

**Ejercicio 1:** Con un negocio propio o ficticio, pide a Claude Code que use el MCP de Meta (Ad Library) para buscar los anuncios de un referente exitoso del mismo rubro, abra 3 con Claude Browser y te devuelva una tabla con el ángulo/gancho de cada uno.

**Ejercicio 2 (avanzado):** Toma uno de esos ángulos y pide 3 variaciones de copy personalizadas para 3 países distintos, cada una en el tono y modismos locales — sin traducir literal.

*Este ejercicio deja lista la fase de research de competencia de tu propio agente media buyer.*

---

## 💡 Tip

Pide siempre subir en modo borrador con presupuesto explícito en el mismo prompt — nunca dejes que el agente decida el presupuesto o publique directo.

---

## ⚠️ Error común

Confiar en que el agente subió algo bien solo porque lo confirmó en texto. Puede fallar en silencio (URL mal formada, creativo rechazado) y reportarlo como éxito — siempre se verifica en el Ads Manager.
