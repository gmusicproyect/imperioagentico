# SKILL: Handoff de Claude Design a Claude Code

> Guarda este archivo en `/skills/handoff-claude-design/SKILL.md`
> Referencia en tu CLAUDE.md: `- /skills/handoff-claude-design/SKILL.md → para importar y convertir diseños de Claude Design en código funcional`

---

## Cuándo usar este skill

Cuando el usuario tenga una interfaz, prototipo o landing page generada en Claude Design (`claude.ai/design`) y necesite exportarla, integrarla en un proyecto local con Claude Code, conectar APIs externas y levantarla como aplicación funcional en `localhost` o producción.

---

## Prerequisitos

- [ ] Proyecto diseñado en Claude Design con ID/comando de exportación o archivo ZIP descargado
- [ ] Directorio de trabajo local abierto en Claude Code
- [ ] Node.js y npm instalados localmente
- [ ] Credenciales de APIs requeridas (ej. ElevenLabs, OpenRouter, Supabase) preparadas para archivo `.env`

---

## Pasos

### Paso 1 — Obtener el comando o paquete de exportación

1. En la interfaz de Claude Design, hacer clic en **Exportar**.
2. Seleccionar la opción de exportación a Claude Code para copiar el comando directo (`fetch this design, implement...`), o descargar el archivo ZIP del proyecto completo.

### Paso 2 — Ejecutar el handoff en Claude Code

1. Abrir la carpeta de destino en Claude Code.
2. Ejecutar el comando de handoff de forma limpia (sin instrucciones adicionales pegadas en el mismo bloque):

```
fetch this design, implement [nombre-del-proyecto]
```

3. Si la llamada devuelve error de red o autenticación (ej. 404), recurrir a la alternativa manual: descomprimir el ZIP en la carpeta del proyecto y pedirle a Claude Code:
   *"Lee los archivos de diseño descomprimidos en este directorio y genera el scaffolding del proyecto."*

### Paso 3 — Configurar variables de entorno y dependencias

1. Crear un archivo `.env` en la raíz del proyecto para alojar las claves requeridas (nunca hardcodearlas en el código fuente).
2. Crear o actualizar `.gitignore` asegurando que `.env` quede excluido del control de versiones.
3. Solicitar a Claude Code la instalación de dependencias necesarias (`npm install`).

### Paso 4 — Conectar la lógica de negocio y APIs

1. Reemplazar los datos mockeados del prototipo por llamadas reales a endpoints o servicios externos (ej. generación de audio con ElevenLabs o consultas a LLMs).
2. Asegurar manejo de errores y estados de carga (loading spinners, fallbacks).

### Paso 5 — Ejecutar en servidor local y verificar

1. Levantar el servidor de desarrollo (`npm run dev` o script correspondiente).
2. Abrir `http://localhost:[puerto]` y validar:
   - Navegación e interactividad completas.
   - Responsividad en vista móvil y desktop.
   - Ejecución exitosa de las llamadas a API sin fugas de credenciales en consola.

---

## Outputs esperados

- Proyecto frontend estructurado y funcional en la carpeta local.
- Archivo `.env` configurado con claves protegidas.
- Servidor local corriendo y accesible en el navegador.

---

## Errores comunes

| Error | Causa probable | Solución |
|-------|---------------|---------|
| Error 404 en fetch | URL requiere autenticación web de sesión | Descargar el ZIP desde Claude Design y procesar localmente |
| Claves API expuestas en cliente | Credenciales insertadas directo en código frontend | Mover las llamadas a funciones de servidor o backend proxy |
| Estilos desalineados | Faltan tokens de diseño o fuentes externas | Verificar que la carpeta de assets e importaciones CSS se hayan transferido completas |

---

## Variaciones

**Variación A — Despliegue a producción:** Tras verificar en `localhost`, configurar proyecto en Vercel o Netlify vinculando el repositorio de GitHub y cargando las variables de entorno en el panel de despliegue.

**Variación B — Prototipo estático HTML:** Si el proyecto no requiere frameworks como React o Next.js, Claude Code puede servir el diseño directamente con un servidor estático local (`npx serve .`).

---

## Notas adicionales

Claude Design actúa como la capa de diseño de alta fidelidad (UI/UX), mientras que Claude Code actúa como el desarrollador fullstack responsable de la arquitectura de datos, llamadas asíncronas y despliegue.

---

*Creado: 2026-09-02*
