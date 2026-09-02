# SKILL: Servidor Local 24/7 con Control Remoto en Claude Code

> Guarda este archivo en `/skills/servidor-local-control-remoto/SKILL.md`
> Referencia en tu CLAUDE.md: `- /skills/servidor-local-control-remoto/SKILL.md → para configurar y operar una máquina local 24/7 accesible desde el celular vía Remote Control`

---

## Cuándo usar este skill

Cuando el usuario desee configurar y operar una máquina local (como un Mac Mini M4, PC o laptop) como servidor agéntico 24/7 para lanzar tareas, leer archivos, ejecutar comandos y acceder a MCPs locales en tiempo real desde el celular o tablet vía Remote Control, evitando costos de infraestructura VPS.

---

## Prerequisitos

- [ ] Claude Code CLI versión 2.1.51 o superior instalado
- [ ] Suscripción activa a Claude Pro o Max
- [ ] Computadora host conectada a corriente y red con suspensión de pantalla/disco desactivada
- [ ] Dispositivo móvil (iOS o Android) con la app oficial de Claude y la misma cuenta iniciada
- [ ] Servidores MCP requeridos configurados en el proyecto local

---

## Pasos

### Paso 1 — Calibrar la máquina local para operación 24/7

Para que el servidor responda sin interrupciones:
1. En macOS: ir a *Ajustes del Sistema → Pantalla de bloqueo* y configurar "Desactivar la pantalla al estar inactivo" manteniendo activo "Impedir que el equipo entre en reposo automáticamente al estar conectado".
2. En Windows/Linux: deshabilitar la suspensión del sistema y configurar que la tarjeta de red no se desactive para ahorrar energía.

### Paso 2 — Verificar entorno y servidores MCP

Antes de habilitar el control remoto, comprobar en la terminal del proyecto:

```bash
# Verificar versión compatible
claude --version

# Iniciar Claude Code y verificar herramientas y MCPs disponibles
claude
> /mcp
```

### Paso 3 — Iniciar la sesión con Remote Control nombrado

Lanzar la sesión asignando un nombre explícito para distinguirla en la app móvil:

```bash
# Desde la terminal al iniciar:
claude --remote-control --name "servidor-principal"

# O si ya estás en una sesión activa de Claude Code:
/remote-control --name "servidor-principal"
```

*Nota:* Se generará un enlace web único (`claude.ai/code/...`) y un código QR en pantalla.

### Paso 4 — Emparejar con el dispositivo móvil

1. Abrir la app de Claude en el celular y acceder a la sección **Code**.
2. Localizar la sesión activa identificada con el nombre asignado y un punto verde indicador de enlace local 🟢 (o escanear el código QR).
3. Confirmar que la sesión cargue el historial completo del proyecto.

### Paso 5 — Validar la sincronización bidireccional

1. Enviar una solicitud de prueba desde el móvil:
   `"Lista los archivos del directorio actual y confirma qué servidores MCP tienes activos."`
2. Verificar en la pantalla del computador anfitrión que la terminal replique el mensaje y ejecute los comandos en tiempo real sin desincronizaciones ni creación de ramas divergentes.

### Paso 6 — Protocolo ante pérdidas de conexión

Si el computador o el teléfono pierden señal temporalmente:
- No cerrar la sesión en el celular: el cliente mantiene intentos de reconexión continua.
- Al restablecerse la red, la sesión recupera el hilo automáticamente sin perder el contexto ni los comandos intermedios.

---

## Outputs esperados

- Servidor local accesible desde cualquier ubicación geográfica vía móvil.
- Acceso remoto directo al filesystem, scripts y servidores MCP de la máquina física.
- Historial sincronizado en tiempo real entre la terminal física y la interfaz del teléfono.

---

## Errores comunes

| Error | Causa probable | Solución |
|-------|---------------|---------|
| Comando no reconocido | CLI inferior a v2.1.51 | Ejecutar `npm install -g @anthropic-ai/claude-code@latest` |
| Se ingresó como texto en el chat | Escribir "inicia remote control" al agente en lugar de usar el comando | Usar el comando de barra `/remote-control` o el flag `--remote-control` |
| Sesión se desconecta al cerrar la tapa | Computadora laptop entra en reposo | Usar utilidades tipo *Caffeine* / *Amphetamine* o mantener la laptop conectada a monitor externo |
| Acceso denegado a herramientas | Modo de permisos esperando confirmación manual en pantalla | Configurar modo auto-accept en flujos probados antes de salir |

---

## Variaciones

**Variación A — Combinación con Rutinas y Cron:** Dejar el servidor local ejecutando rutinas matutinas o loops de trabajo (framework DAME) y supervisar el avance periódicamente desde el móvil.

**Variación B — Entorno mixto con OpenClaw:** Si se tienen flujos de mensajería (Telegram/WhatsApp), utilizar OpenClaw en paralelo con Claude Code en la misma máquina local compartiendo repositorios de trabajo.

---

## Notas adicionales

Un Mac Mini M4 operando como servidor agéntico continuo consume entre 5W y 15W en reposo/carga moderada, lo que equivale a un costo eléctrico mensual de aprox. $2 a $2.5 USD en Chile ($2.000–$2.500 CLP), brindando mayor privacidad, potencia de procesamiento y memoria que un VPS de gama de entrada.

---

*Creado: 2026-09-02*
