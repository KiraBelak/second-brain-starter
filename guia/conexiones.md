# Conectar Claude con tu bóveda, tu correo, tu calendario y tus chats

Esta guía te lleva paso a paso para que Claude lea tu bóveda de Obsidian y, si quieres, también Gmail, Google Calendar, Beeper y Monologue. Todo es opcional: empieza por la bóveda y agrega lo demás cuando lo necesites.

## Elige tu camino

| | Camino A: Cowork (app) | Camino B: Claude Code (terminal) |
| --- | --- | --- |
| Para quién | Prefieres una app con ventanas y botones | Te sientes cómoda con la terminal |
| Bóveda | Das acceso a la carpeta de la bóveda | Servidor MCP de Obsidian o abrir Claude Code dentro de la carpeta |
| Gmail y Calendar | Ajustes › Conectores | Los mismos conectores de claude.ai |
| Beeper y Monologue | Según lo que ofrezca tu app | `claude mcp add` |

Si dudas, empieza por el camino A. Los conectores de Gmail y Google Calendar se activan una sola vez en tu cuenta de claude.ai y funcionan en los dos caminos.

## 1. Obsidian MCP (camino B)

Un servidor MCP deja que Claude Code busque y lea notas de tu bóveda por propiedades, nombres y enlaces. Usa el binario `obsidian-mcp` de lstpsche.

1. Entra a https://github.com/lstpsche/obsidian-mcp/releases y descarga el binario que corresponde a tu sistema (Mac con chip Apple, Mac Intel, etc.).
2. Crea la carpeta de destino y mueve el binario ahí:

   ```
   mkdir -p ~/.local/bin
   mv ~/Downloads/obsidian-mcp ~/.local/bin/obsidian-mcp
   ```

   Ajusta el nombre del archivo si el descargado se llama distinto.
3. Dale permiso de ejecución:

   ```
   chmod +x ~/.local/bin/obsidian-mcp
   ```

4. Regístralo en Claude Code. Cambia `TU_USUARIO` por tu usuario y revisa que la ruta de la bóveda sea la tuya (el espacio va escapado con `\`):

   ```
   claude mcp add obsidian -e OBSIDIAN_VAULT_PATH=/Users/TU_USUARIO/Documents/Second\ brain -- /Users/TU_USUARIO/.local/bin/obsidian-mcp
   ```

5. Verifica:

   ```
   claude mcp list
   ```

   Debe aparecer `obsidian` como conectado.

Usa siempre rutas absolutas, completas, desde `/Users/...`.

### Si algo falla

- **La ruta lleva `~`.** En `claude mcp add` el `~` no siempre se expande. Escribe `/Users/TU_USUARIO/...` completo.
- **El binario no se ejecuta.** Falta el `chmod +x`. Repite el paso 3.
- **La ruta de la bóveda tiene espacios.** Escápalos con `\` (como en `Second\ brain`) o ponla entre comillas.
- **Una nota no aparece en las búsquedas.** Revisa sus propiedades: si el YAML entre las dos líneas `---` está roto (una comilla sin cerrar, una sangría mal puesta), la nota queda fuera del índice. Corrige el YAML y vuelve a buscar.
- **Cambiaste algo y no se nota.** Cierra y abre Claude Code para que relea la configuración.

## 2. Gmail y Google Calendar

Se conectan con los conectores de claude.ai, sin binarios ni terminal.

1. Entra a claude.ai, ve a Ajustes › Conectores.
2. Busca Gmail y pulsa Conectar. Inicia sesión con tu cuenta de Google y acepta los permisos.
3. Repite con Google Calendar.

La misma cuenta de claude.ai sirve en Cowork y en Claude Code: lo que conectes una vez aparece en los dos. En Claude Code puedes comprobarlo con `claude mcp list`.

Prompt para probar:

```
Lee mis correos y mi calendario de esta semana con [[Ana López]]. Dime qué quedó pendiente, qué reuniones hay y qué acuerdos aparecen (quién, qué, para cuándo). Propón dónde va cada cosa y espera mi OK para guardar.
```

## 3. Beeper Desktop

Beeper junta tus chats (WhatsApp, Telegram y otros) en una sola app. Su API local permite que Claude los lea.

1. Abre Beeper Desktop y ve a Settings › Developer › Desktop API.
2. Activa la API y genera un token. Cópialo.
3. Conéctalo en Claude Code (cambia `TU_TOKEN`):

   ```
   claude mcp add --transport http beeper http://127.0.0.1:23373/v0/mcp --header "Authorization: Bearer TU_TOKEN"
   ```

4. Verifica con `claude mcp list`.

Reglas importantes:

- Beeper Desktop debe estar abierto mientras Claude lo usa. Si lo cierras, la conexión falla.
- El token da acceso a todos tus chats. No lo guardes en la bóveda, no lo pegues en notas ni lo compartas.
- Úsalo solo para leer. Claude nunca debe enviar mensajes (la herramienta `send_message` existe, pero no se usa).

Prompt para probar:

```
Revisa mis chats de hoy en Beeper. Dime qué acuerdos, preguntas sin responder y pendientes hay, con quién y para cuándo. Propón dónde va cada cosa y espera mi OK. Nunca envíes mensajes.
```

## 4. Monologue

Monologue guarda tus notas de voz y sus transcripciones.

1. Conéctalo:

   ```
   claude mcp add --transport http monologue https://api.monologue.to/mcp
   ```

2. La primera vez se abre el navegador para que inicies sesión (OAuth) y autorices el acceso.
3. Verifica con `claude mcp list`.

## Prompt todo en uno: la revisión diaria

Cuando tengas correo, calendario y chats conectados:

```
Revisa mis correos, chats y calendario de hoy; saca acuerdos, pendientes y propón dónde van. Espera mi OK.
```

Claude te devuelve una propuesta. Tú decides qué se guarda y dónde.

## Privacidad

- Los chats y correos contienen mensajes de otras personas. Antes de guardar algo en tu bóveda, pregúntate si esa persona estaría cómoda con que quede ahí o lo lea una IA.
- Pide a Claude que te pregunte antes de guardar. Por eso todos los prompts terminan con "espera mi OK".
- Guarda el acuerdo, la fecha y la fuente, no la conversación completa.
- Nada sensible en la bóveda: contraseñas, tokens, números de tarjeta, datos médicos o de terceros que no te corresponda guardar.
- Los tokens (como el de Beeper) viven en la configuración de Claude, nunca en una nota.
- Con conectores solo se lee. Nunca se envían mensajes ni correos desde Claude.
