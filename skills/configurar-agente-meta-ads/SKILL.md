# SKILL: Configuración y Operación del Agente Meta Ads (Matías)

> Guarda este archivo en `/skills/configurar-agente-meta-ads/SKILL.md`
> Referencia en tu CLAUDE.md: `- /skills/configurar-agente-meta-ads/SKILL.md → para configurar el agente CLI de Meta Marketing API (Matías) y gestionar campañas publicitarias desde la terminal`

---

## Cuándo usar este skill

Cuando el usuario requiera gestionar, auditar o crear campañas de Meta Ads directamente desde Claude Code sin dashboards de terceros ni intermediarios, utilizando el **MCP Oficial de Meta (Meta Ads 2.0)** o mediante una suite Node.js nativa con la Marketing API v21.0 (Meta Ads 1.0).

---

## Prerequisitos

- [ ] Cuenta de Meta Ads Manager activa y con método de pago verificado
- [ ] Claude Code CLI instalado
- [ ] Servidor MCP oficial de Meta configurado en Conectores
- [ ] (Opcional) Cuenta en [developers.facebook.com](https://developers.facebook.com) si se opta por la suite CLI 1.0

---

## Pasos

### Opción A — Configuración con el MCP Oficial de Meta (Recomendada - Meta Ads 2.0)

1. En Claude Code, acceder a **Configuración** → **Conectores** → **Agregar conector personalizado**.
2. Asignar el nombre `metaads` y pegar la URL del servidor MCP oficial de Meta.
3. Reiniciar la aplicación de terminal (`Cmd+Q` en Mac o reabrir ventana en Windows).
4. **Calibrar permisos de seguridad:**
   - Lectura y analítica: *Permitir siempre*.
   - Creación de campañas y ads: *Permitir siempre*.
   - Eliminación destructiva: *Requiere aprobación manual*.
5. **Verificación de conexión:**
   Enviar el prompt: *"Te conecté a Meta MCP. Verifica tu conexión y dime cuánto está mi costo por lead hoy en la campaña de signups"*.

### Opción B — Configuración Directa vía Node.js CLI (Método Legacy 1.0)

1. Crear app empresarial en [developers.facebook.com](https://developers.facebook.com), publicar con URLs de privacidad válidas y extraer el token de Marketing API desde Graph API Explorer.
2. Desplegar la suite en Node.js con el One Prompt Setup:

```markdown
Tu rol es ser Matías, mi Ad Manager personal de Meta Ads. Tu trabajo es gestionar, analizar, modificar y crear campañas directamente desde la terminal usando la API de Meta — sin que yo tenga que abrir el Ads Manager. Cuando te pida algo, lo ejecutas. Si quiero pausar un adset, lo pausas. Si quiero subir el presupuesto, lo subes. Si quiero una campaña nueva con copies por país, la creas. Operas en español y confirmas cada acción antes de ejecutarla.

Para empezar, crea el proyecto Node.js desde cero. Stack: ESM modules, fetch nativo, dotenv, Meta Marketing API v21.0.
Archivos a crear:
- .env → META_ACCESS_TOKEN y META_API_VERSION=v21.0
- src/api.js → cliente HTTP base con manejo de errores
- src/campaigns.js → listar cuentas, campañas, adsets, ads, insights; pausar/activar; cambiar presupuesto
- src/analyze-countries.js → gasto por país, CPA, ranking de mejor a peor
- src/analyze-ads.js → top performers por compras y por CPA
- src/cli.js → comandos: accounts, campaigns, insights, pause, activate, budget, adsets, ads
- CLAUDE.md → Directivas del agente, reglas de confirmación obligatoria

MI TOKEN: [PEGA_AQUÍ_TU_TOKEN]
```

### Verificar la conexión (tras cualquiera de las dos opciones)

Correr en terminal el comando de verificación:
```bash
node src/cli.js accounts
```
Confirmar que liste el `id` y `name` de la cuenta publicitaria asociada.

### Ejecutar auditorías y optimizaciones por lenguaje natural

1. **Auditar los mejores anuncios:**
   *"Dime cuáles fueron mis mejores anuncios el último mes ordenados por menor CPA."*
2. **Desglose geográfico:**
   *"Analiza el gasto por país y ordéname los mercados de menor a mayor costo por adquisición."*
3. **Pausas y reactivaciones:**
   *"Pausa los conjuntos de anuncios con CPA superior a \$[X] que hayan gastado más de \$[Y]."*
4. **Campañas localizadas:**
   *"Crea una campaña de remarketing para España y Chile con \$5/día cada una, usando expresiones nativas en cada copy."*

---

## Outputs esperados

- Suite Node.js funcional en `src/` conectada directamente a la API oficial de Meta.
- Informes de rendimiento financiero y CPA sin intermediarios SaaS.
- Campañas creadas y adsets modificados en tiempo real bajo confirmación explícita del operador.

---

## Errores comunes

| Error | Causa probable | Solución |
|-------|---------------|---------|
| Token caducado a las 2 horas | Uso de token temporal de Graph API Explorer | Intercambiar por un *Long-Lived User Token* (60 días) en el Access Token Tool de Meta |
| `(#100) Missing permissions` | No se tildaron los scopes de Marketing | Regenerar el token marcando `ads_management` y `ads_read` |
| Cambios aplicados sin aviso | Agente en modo auto-approve descontrolado | Exigir en `CLAUDE.md` confirmación previa antes de cualquier llamada `POST` o `DELETE` |

---

## Notas adicionales

Matías elimina el desfase de comunicación entre el estratega y el ejecutor técnico. El operador mantiene el control absoluto del presupuesto y de la línea editorial.

---

*Creado: 2026-09-03*
