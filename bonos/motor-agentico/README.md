# Bono: Motor Agéntico v2.0 — Cabina Local de Control, ROI y Auditoría Agéntica

El **Motor Agéntico v2.0** no es un parche: es la transformación del dashboard en una verdadera **cabina de mando** para tu operación con IA. Corre 100% en tu computadora (`http://localhost:8081`), lee tu actividad real de Claude Code y asistentes conectados (Hermes, OpenClaw, Codex), y sintetiza tu desempeño en un solo indicador clave (**tu Operator Score de 0 a 100**), además de medir tu racha activa, tu ROI real frente a tarifas API, la salud de tu memoria en un grafo interactivo 2.5D y la automejora matutina de **"El Sueño"**.

---

## 🛡️ Las 3 Reglas de Oro del Motor Agéntico

1. **100% Local:** Tus datos nunca salen de tu máquina. Cero nube, cero telemetría, cero fuga de credenciales o de código propietario.
2. **Solo Lectura:** El Motor observa, parsea y audita logs y transcripts de tus sesiones; **nunca escribe en `~/.claude`, en Obsidian ni en tus repositorios**.
3. **Completamente Honesto:** No inventa métricas ni proyecta números inflados. Si un proyecto o herramienta aún no tiene datos registrados, el Motor lo declara explícitamente vacío.

---

## 🎛️ Novedades de la Versión 2.0: La Cabina del Operador

| Funcionalidad v2 | Qué resuelve | Dónde se visualiza |
|-------------------|--------------|-------------------|
| **Operator Score (0–100)** | Un solo número que califica la eficiencia y madurez de tu operación agéntica (deja de adivinar si le estás sacando provecho a tu stack) | Círculo central en la capa **Vista** |
| **Racha Activa (Streak)** | Conteo de días seguidos abriendo y operando el Motor; consolida el hábito de auditar y gobernar tus agentes | Header y widget central |
| **Grafo de Memoria 2.5D** | Visualizador tridimensional interactivo de workspaces, archivos (Obsidian / Claude local) y vectores de decisión. Permite rotar, inclinar, hacer hover e inspeccionar detalles | Capa **Memoria** |
| **Agentes con Vida Propia** | Estado en vivo de asistentes locales con **chat integrado para interactuar con Hermes sin salir del dashboard** y monitoreo de OpenClaw | Capa **Agentes** |
| **Compartir tu ROI (`/share`)** | Pantalla lista y formateada para compartir públicamente tu multiplicador de ROI real en un solo clic | Ruta `/share` |
| **Soporte Windows + macOS** | Compatibilidad multiplataforma completa (`launchd` en Mac, Programador de Tareas en Windows) | Instalador universal |

---

## 🗂️ Organización en Capas Especializadas

A diferencia de la v1 (que presentaba un único muro continuo de datos), la v2 distribuye la operación en pantallas dedicadas:

```
MOTOR AGÉNTICO v2
├── [VISTA]       → Cabina central: Operator Score (0-100), gasto IA, ROI, racha, turnos y alertas
├── [COSTO]       → Desglose financiero: suscripciones ($20 Pro / $200 Max) vs costo API acumulado
├── [MEMORIA]     → Grafo 2.5D: 850+ archivos indexados, nodos de Obsidian y detección de memoria rancia
├── [SUEÑO]       → Auditoría matutina (7:00 AM) a pantalla completa con 4 prescripciones accionables
├── [AGENTES]     → Asistentes en vivo: chat interactivo con Hermes y monitoreo de OpenClaw
├── [SKILLS]      → Mapa de comandos /<skill>, conteo de usos y tiempo ahorrado en dinero ($)
├── [ACTIVIDAD]   → Línea de tiempo de turnos y sesiones ejecutadas por día
└── [PROYECTOS]   → Workspaces detectados en tu máquina local
```

---

## 🎯 Las 4 Preguntas Críticas que Responde la Cabina

| Pregunta | Respuesta en el Dashboard | Métrica / Capa |
|----------|---------------------------|----------------|
| **1. ¿Cuánto estás gastando de verdad?** | Suma consolidada de suscripciones fijas y consumo acumulado por modelo | **Gasto IA - Mes** ($200 USD) en Capa Costo |
| **2. ¿Cuánto te está rindiendo en dinero? (ROI)** | Comparativa de lo pagado en suscripción vs tarifas de API públicas | **Tu ROI Real** (ej. 3.3x, 15x, 40x) en Capa Vista |
| **3. ¿Qué sabe la IA de tus proyectos?** | Relaciones entre notas, workspaces y porcentaje de **salud de memoria** | **Grafo 2.5D** (Núcleo, Workspaces, Archivos) en Capa Memoria |
| **4. ¿Qué está haciendo ahora mismo?** | Estado de asistentes conectados y cron jobs activos | **Agentes** (Hermes Chat + OpenClaw) en Capa Agentes |

---

## ⚙️ Arquitectura y Stack Interno

- **Runtime:** [Bun](https://bun.sh) (motor ultrarrápido en JavaScript/TypeScript; arranca en milisegundos sin dependencias pesadas de Node).
- **Frontend:** React + Vite + Tailwind CSS (interfaz estilo HUD aeroespacial, modo oscuro con acentos dorados imperiales).
- **Grafo 2.5D:** Motor Canvas/WebGL optimizado para rotación, inclinación y filtrado de cientos de nodos sin lag.
- **Agregador de Datos:** Parser local de transcripts (`~/.claude/projects/`, logs JSONL de sesiones, vaults de Obsidian y canales de agentes).
- **Programador del Sueño:** `launchd` nativo en macOS y Programador de Tareas (*Task Scheduler*) en Windows para ejecutar la auditoría a las 7:00 AM.

---

## 🚀 Instalación Guiada por IA en 3 Minutos (`INSTALAR.md`)

Tú no tienes que programar ni configurar rutas; tu propio agente de código realiza la instalación desatendida.

### Paso 1 — Descarga y descompresión
Descarga `motor-agentico-v2.x.x.zip` desde el Classroom de Imperio Digital y descomprímelo:
- **En Mac:** Doble clic sobre el archivo `.zip`.
- **En Windows:** Clic derecho → *"Extraer todo..."*.

### Paso 2 — Delegar la instalación a Claude Code
1. Abre tu terminal o IDE con Claude Code dentro de la carpeta descomprimida.
2. Arrastra el archivo **`INSTALAR.md`** al chat.
3. Escribe una sola palabra:
   ```
   instalalo
   ```
4. Presiona Enter.

### Qué hace el agente en segundo plano:
1. Verifica Bun en el sistema y lo instala automáticamente si no existe.
2. Descarga e instala los paquetes necesarios (~300 MB).
3. Corre el escaneo inicial de tus transcripts locales para poblar tus primeros datos históricos.
4. Programa la rutina matutina de **"El Sueño"** a las 7:00 AM.
5. Inicia el servidor local y abre automáticamente la cabina en:
   ```
   http://localhost:8081
   ```

---

## 🧭 Onboarding y Calibración del Núcleo (90 Segundos)

- **Si ya usabas Claude Code:** Entras directo a la cabina con tus números históricos ya calculados. Un aviso dorado superior te permite abrir la *Calibración del núcleo* cuando desees.
- **Si partes desde cero:** El asistente de 7 pasos te solicita tu nombre, foto, herramientas activas, rutas de Obsidian/Notion y tu **tarifa por hora ($/hora)**, indispensable para calcular cuánto dinero te ahorran tus skills.

---

## 🌙 La Capa "El Sueño": Automejora Matutina a las 7:00 AM

Cada mañana a las 7:00 AM (o manualmente con `bun run dream`), El Sueño audita tus últimas 24 horas y deja 4 prescripciones accionables en el dashboard:
1. **Empaquetador de Skills:** Identifica tareas repetitivas en tus sesiones y propone convertirlas en un `/skills/[nombre]/SKILL.md`.
2. **Calibración de Modelos:** Detecta si usaste Opus para tareas mecánicas que Haiku o Sonnet resolvían por un 90% menos de costo.
3. **Salud de Memoria:** Alerta si tus archivos de contexto (`CLAUDE.md`, perfiles de usuario o notas clave) llevan más de 10 a 50 días sin actualizarse.
4. **Estimación de Ahorro:** Cuantifica el tiempo y los dólares ganados en la semana.

---

## 🔄 Cómo Actualizar de v1 a v2 (Sin Perder Datos)

Tu progreso (tu Operator Score, tu racha de días activos, tu nombre, tu foto y tu configuración) vive en el `localStorage` de tu navegador atado a `http://localhost:8081`.

1. Descarga el archivo `motor-agentico-v2.x.x.zip`.
2. Reemplaza los archivos de la carpeta del Motor.
3. Arrastra el nuevo `INSTALAR.md` a Claude Code y escribe:
   ```
   actualiza el Motor a la v2
   ```
4. **Reglas de oro para conservar tu racha:** No cambies el puerto (`8081`) y no borres los datos del sitio `localhost:8081` en tu navegador.

---

## 🛠️ Cómo Construir tu Propio Odómetro Básico (Prompt Gratuito)

Para quienes no forman parte de Imperio, este prompt genera un odómetro básico local en Claude Code:

```
Lee mis transcripts de Claude Code ubicados en la carpeta de configuración (~/.claude/projects/ o logs locales).
Calcula el costo de cada sesión según las tarifas oficiales de Anthropic (Opus, Sonnet, Haiku).
Móntame una página web local ligera en React/HTML que muestre:
1. Gasto acumulado por modelo y por día.
2. Comparativa del consumo API vs mi suscripción mensual ($20 Pro / $200 Max) para ver mi ROI.
3. Un Operator Score preliminar (0 a 100) basado en frecuencia de skills y horas ahorradas.
4. Lista de archivos de contexto que llevan más de 15 días sin modificarse.
Otorga permisos estrictamente de SOLO LECTURA, sin modificar ningún archivo de las sesiones originales.
```

---

## 🛠️ Troubleshooting y Desinstalación

| Problema | Causa | Solución |
|----------|-------|----------|
| La instalación se traba en paquetes | Conexión lenta o interrupción | Arrastra `INSTALAR.md` y escribe: *"la instalación falló en el paso 2, arréglalo"* |
| La racha se reinició a 1 día | Se borraron los datos de navegación o se usó modo incógnito | Operar siempre en el navegador habitual en `http://localhost:8081` |
| Error en el programador de tareas | Permisos insuficientes en Windows | Ejecutar la terminal como Administrador y repetir el comando de activación del Sueño |
| Desinstalar por completo | Retiro del sistema | Arrastra `INSTALAR.md` y dile: *"desinstala el Motor"*; el script limpiará los cron jobs y dependencias |
