# Bono: Control Remoto — Tu Computador Completo en el Celular (Mac Mini 24/7 + MCPs)

Hasta ahora, usar Claude Code requería estar físicamente frente a la terminal o el editor en tu máquina local. Con la actualización de **Remote Control** de Anthropic, puedes controlar tu computador completo desde la app móvil de Claude (iOS y Android) o desde cualquier navegador, leyendo archivos, editando código y ejecutando comandos de terminal en tiempo real mientras estás en el gimnasio, en un café o en el sofá.

---

## Stack de la integración

| Componente | Rol en el sistema | Tipo |
|------------|-------------------|------|
| **Claude Code CLI (v2.1.51+)** | Motor de ejecución local y gestión de procesos | Terminal local / macOS / Linux / Windows |
| **App de Claude (iOS / Android / Web)** | Interfaz de control móvil y visualización remota | App móvil / `claude.ai/code` |
| **Servidor local (Mac Mini M4 / PC)** | Máquina anfitriona corriendo 24/7 | Hardware local |
| **Servidores MCP locales** | Herramientas externas y APIs conectadas | `.mcp.json` en máquina host |

---

## Las 3 ventajas clave de Remote Control

1. **Sincronización simultánea sin bifurcaciones:**
   Puedes tener la sesión abierta en el monitor del computador y en el celular al mismo tiempo. Cada mensaje enviado desde el móvil se refleja en la terminal local y viceversa en tiempo real, resolviendo el problema clásico de los LLMs donde abrir una sesión en dos dispositivos generaba ramas ("forks") divergentes que rompían la memoria.
2. **Resiliencia ante desconexiones:**
   Si pierdes señal de internet o el computador entra temporalmente en suspensión (*sleep*), el sistema mantiene el estado y se reconecta automáticamente en cuanto la máquina anfitriona vuelve a estar online.
3. **Acceso al entorno completo (Filesystem + MCPs):**
   A diferencia de Claude en la web (que corre en un contenedor aislado en la nube), Remote Control es una ventana directa hacia tu máquina física. Tiene acceso a tus carpetas privadas, comandos bash y a todos los servidores MCP configurados localmente (Bases de datos, Meta, GHL, Airtable, etc.).

---

## Arquitectura recomendada: Mac Mini 24/7 vs VPS

Tener un servidor dedicado para correr agentes y control remoto no requiere contratar infraestructura cara en la nube.

```
Mac Mini M4 (debajo del monitor)
├── Corriendo 24/7 con Claude Code en background
├── Conectado a servidores MCP locales y carpetas de proyectos
└── Accesible desde cualquier lugar vía Remote Control en el celular
```

### Comparativa de costos y rendimiento:

| Criterio | Mac Mini M4 local (24/7) | VPS en la nube equivalente |
|----------|--------------------------|----------------------------|
| **Costo mensual** | ~$2.000 – $2.500 CLP/mes (~$2 – $2.5 USD en luz) | ~$20 – $60+ USD/mes |
| **Potencia y RAM** | 16 GB+ memoria unificada, chip Apple Silicon M4 | 8–16 GB vCPU compartida |
| **Privacidad de archivos** | 100% en tu disco local privado | Alojado en servidores de terceros |
| **Acceso a hardware/MCPs** | Directo a scripts, puertos locales y automatizaciones | Requiere configurar túneles, SSH y proxies |

---

## Comparativa: Claude Code Remote Control vs OpenClaw

| Característica | Claude Code Remote Control | OpenClaw |
|----------------|---------------------------|----------|
| **Interfaz móvil** | App oficial de Claude (pestaña Code) o `claude.ai/code` | Mensajería (Telegram, WhatsApp, Slack) |
| **Entorno de ejecución** | Terminal nativa de Claude Code con confirmaciones de permisos | Daemon/agente independiente conectado a APIs |
| **Configuración** | Un solo comando (`/remote-control`) sin setup adicional | Requiere bots de Telegram, tokens y webhooks |
| **Seguridad** | Autenticación cerrada por cuenta de Anthropic | Depende de la seguridad del canal de mensajería |

---

## Cómo activar y operar Remote Control

### 1. Iniciar desde una sesión nueva
```bash
# Iniciar sesión vinculada directamente a Remote Control
claude --remote-control --name "nombre-proyecto"
```

### 2. Iniciar desde una sesión ya abierta en terminal
Dentro de una sesión activa de Claude Code, escribe:
```bash
/remote-control --name "refactor-auth"
```

> ⚠️ **Regla de oro:** El comando se ejecuta como comando de terminal o comando de barra (`/remote-control`), **nunca** como un prompt conversacional en texto libre dentro del chat de Claude.

### 3. Conexión desde el móvil
1. Abre la app de Claude en iOS o Android (o ingresa en el navegador a `claude.ai/code`).
2. Ve a la pestaña **Code**: verás tu sesión local listada con el ícono de una computadora y un indicador verde 🟢.
3. Alternativamente, escanea el código QR que se imprimió en la terminal al lanzar el comando.

---

## Requisitos previos obligatorios

- **Suscripción activa:** Requiere plan **Pro** (~$17/mes) o **Max** de Anthropic (el plan gratuito no incluye Claude Code).
- **Versión del CLI:** Versión `2.1.51` o superior (verificar con `claude --version`).
- **Actualización:** Si el comando no es reconocido, actualizar con:
  ```bash
  npm install -g @anthropic-ai/claude-code@latest
  ```
- **Alimentación y red:** La computadora anfitriona debe permanecer encendida y con conexión a internet activa.

---

## Errores comunes y soluciones

| Error | Causa | Solución |
|-------|-------|---------|
| Claude no reconoce el comando | Se escribió en el chat como texto libre en vez de comando | Usar el prefijo de barra `/remote-control` en terminal activa |
| Sesión no aparece en la app móvil | Cuenta de Claude diferente en móvil y escritorio | Asegurarse de haber iniciado sesión con el mismo email en ambos dispositivos |
| Desconexión prolongada | La máquina entró en reposo profundo (*deep sleep*) | Desactivar la suspensión automática en los ajustes de energía de macOS/Windows |
| Sin permisos de ejecución | Modo de permisos bloquea acciones desatendidas | Configurar auto-accept o pre-aprobar herramientas antes de operar en movimiento |

---

## Tips para operar en producción

- Si dejas el equipo corriendo 24/7, desactiva la suspensión del disco en *Ajustes del Sistema → Pantalla de bloqueo / Economizador*.
- Nombra siempre la sesión con `--name` para identificarla al instante en el selector móvil cuando administres múltiples repositorios.
- Consulta el [Bono Gestión de Sesiones](../gestion-sesiones/) para combinar Remote Control con reanudaciones automáticas (`--continue`) y selectores de historial (`--resume`).
