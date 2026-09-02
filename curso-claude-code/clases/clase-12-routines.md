# Clase 12 — Routines, N8N & VPS

**Tags:** `Routines` `N8N` `VPS` `Infraestructura`
**Conecta con:** Clase 11 · Clase 05 · Bono Ads

---

## Idea central

Las Routines son automatizaciones programadas que corren Claude Code de forma autónoma — sin que tengas que iniciar la sesión manualmente. Para workflows más complejos o de alto volumen, N8N + VPS es la infraestructura que las sostiene 24/7.

---

## Routines vs N8N

| | Routines (Claude Code nativo) | N8N + VPS |
|--|-------------------------------|-----------|
| Configuración | Simple, desde la interfaz | Requiere setup de servidor |
| Triggers | Horario (cron) | Horario + webhooks + eventos |
| Volumen | Bajo-medio | Alto |
| Costo | Incluido en el plan | VPS ~$5-20/mes |
| Cuándo usarlo | Tareas diarias simples | Pipelines de producción |

---

## Configurar una Routine básica

```
"Todos los días a las 8am:
1. Extrae las métricas de mis ads activos en Meta
2. Compara con los últimos 7 días
3. Si algún ad tiene CPA > $50, mándame un mensaje en Telegram
4. Guarda el reporte en Google Drive"
```

---

## Arquitectura VPS para producción

```
VPS (Ubuntu)
├── N8N          → orquesta los workflows
├── Claude Code  → ejecuta tareas agénticas
└── Cron jobs    → dispara N8N en horarios definidos
```

---

## Servicios de VPS recomendados

- DigitalOcean Droplet (~$6/mes para empezar)
- Hetzner (más barato, Europa)
- Railway (más fácil, buen tier gratis)

---

## 💡 Tip

Empieza con Routines nativas para validar el workflow. Migra a VPS solo cuando necesites más volumen, más triggers, o que corra mientras tienes la laptop apagada.
