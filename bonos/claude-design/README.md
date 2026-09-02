# Bono: Claude Design — Del Prototipo UI al Handoff en Claude Code

Claude Design (`claude.ai/design`) es el entorno visual de Anthropic impulsado por Claude Opus 4.7 que unifica prototipado, sistemas de diseño y frontend interactivo en una sola herramienta, reemplazando flujos dispersos entre Figma, Canva, v0 y Lovable. Su verdadero potencial se desbloquea al realizar el handoff hacia Claude Code para conectar APIs, lógica de backend y levantar la app en producción.

---

## Stack del flujo

| Componente | Herramienta | Rol en el pipeline |
|------------|-------------|--------------------|
| **Diseño y Prototipado** | Claude Design (Opus 4.7) | Creación de UI responsiva, tokens de diseño y layouts interactivos |
| **Ingeniería y Backend** | Claude Code | Descarga de componentes, scaffolding, conexión a APIs y servidor local |
| **Voz y Audio IA** | ElevenLabs API | Generación de voz sintética dinámica para la experiencia de usuario |
| **Modelos y Razonamiento** | OpenRouter / Anthropic API | Inferencia de LLMs para generación de contenido en tiempo real |
| **Producción** | Supabase + Vercel / Netlify | Autenticación, persistencia de usuarios y despliegue público |

---

## Qué es Claude Design y cómo funciona por dentro

A diferencia de los generadores de interfaces genéricos ("AI slop"), Claude Design crea código interactivo y responsivo con criterio estético:

- **Entrevista guiada:** Claude formula preguntas interactivas de opción múltiple (paleta, estilo de iconos, pantallas clave, onboarding) para alinear la visión antes de escribir código.
- **Edición multimodal y directa:** Permite adjuntar logos o brand assets arrastrándolos al canvas, anotar cambios visuales con la herramienta de dibujo/edit y solicitar fallbacks inmediatos a versiones anteriores.
- **Tokens y componentes:** Genera una estructura modular limpia (assets, componentes, estilos globales) preparada para desarrollo.

---

## Design Systems: consistencia multimarca

Claude Design permite crear y gestionar múltiples **Design Systems** independientes:
- Cada Design System almacena los lineamientos de una empresa o cliente (tipografías, logotipos, paletas de color y reglas de espaciado).
- Al iniciar un nuevo proyecto, se selecciona el Design System correspondiente para garantizar fidelidad de marca sin alucinaciones visuales.
- Ideal para agencias o freelancers que operan varias marcas simultáneamente.

---

## Frontend vs Backend en 60 segundos

- **Frontend (Claude Design):** Es la capa visual interactiva (lo que el usuario ve y toca: botones, navegación, animaciones, estilos).
- **Backend (Claude Code):** Es la capa funcional oculta (llamadas a APIs externas, autenticación con Supabase, cobros con Stripe, persistencia en base de datos).
- **La sinergia:** Diseñas la UI en minutos en Claude Design y usas Claude Code como el ingeniero fullstack que le da vida con código funcional.

---

## El flujo de Handoff a Claude Code

```
1. En Claude Design: Exportar → "Copy command" (o descargar ZIP)
2. Comando generado: fetch this design, implement [nombre-proyecto]
3. En Claude Code (directorio local):
   → Pegar el comando limpio de handoff
   → Claude Code descarga assets, HTML/React y scaffolding
4. Configuración de variables de entorno (.env):
   → ELEVENLABS_API_KEY
   → OPENROUTER_API_KEY / ANTHROPIC_API_KEY
5. Ejecución:
   → npm install / npm run dev
   → Abrir http://localhost:3000
```

---

## Pasos para llevar tu app a producción

1. **Autenticación (Supabase):** Implementa login y registro de usuarios para proteger tus endpoints y evitar que terceros consuman tus créditos de API.
2. **Límites y Pagos (Stripe):** Integra pasarela de pago para monetizar o cobrar créditos por uso.
3. **Despliegue (Vercel / Netlify):** Sube el repositorio a GitHub y conecta con Vercel para hosting global automático con HTTPS.

---

## Errores comunes

| Error | Causa probable | Solución |
|-------|---------------|---------|
| Error 404 al hacer fetch | Se agregó texto explicativo al comando o URL privada expirada | Copiar y ejecutar el comando de exportación limpio sin texto adicional, o usar la descarga en ZIP |
| API Keys quemadas en código | Pasar credenciales en el chat público | Guardar siempre las API keys en un archivo `.env` excluido por `.gitignore` |
| UI rota en pantallas móviles | Prompt inicial no especificó mobile-first | Solicitar explícitamente desde el primer mensaje layout responsivo para smartphones |
| Intentar crear backend en Design | Claude Design está enfocado en UI/UX | Resolver lógica compleja, webhooks y bases de datos en Claude Code |

---

## Tips

- Activa el modo **mock por defecto** en Claude Design para iterar el flujo visual sin gastar saldo en llamadas reales a APIs de voz o LLMs.
- Si el handoff directo por CLI falla por permisos de red o sesión web, descarga el archivo ZIP desde Claude Design, descomprímelo en tu carpeta y dile a Claude Code: `Implementa este proyecto a partir de los archivos locales`.
