# Prompts para copiar

Prompts del curso, listos para pegar en Claude con tu bóveda conectada. Cambia los nombres entre `[[ ]]` por los tuyos. En todos, Claude propone y tú apruebas.

Una buena petición lleva cuatro partes: contexto (qué notas leer), tarea (un verbo), formato (cómo quieres verlo) y límites (qué no debe tocar o inventar).

## Pedir algo bien

Así no:

```
Resume mis notas.
```

Así sí:

```
Lee [[Evento de aniversario]] y mis notas de 10 Diario de esta semana. Resume qué avanzó, qué está bloqueado y qué depende de mí, en 5 viñetas. No inventes fechas.
```

## De reunión a resumen y acuerdos

Pega la transcripción (de Zoom, Meet, Teams, una grabación transcrita o tus notas a mano) y usa este prompt. Avisa a los demás antes de grabar. Si la transcripción es larga, guárdala primero en `00 Inbox` y pide que la lea desde ahí.

```
Te paso la transcripción de la reunión de hoy con [[Ana López]] y [[Luis Pérez]].
1. Resume en 5 líneas qué se habló.
2. Acuerdos: quién · qué · para cuándo.
3. Decisiones tomadas y por qué.
4. Pendientes míos y de otros. Marca cuáles van a 50 Tareas.
Si algo no está claro, escribe [por confirmar].
Propón qué va en 10 Diario, en cada Persona y en el Proyecto.
Para cada Persona, propón actualizar ultimo_contacto con la fecha de la reunión (YYYY-MM-DD) y agrega la fuente, por ejemplo "reunión 2026-11-10".
En el Proyecto, propón una entrada en la sección Bitácora útil y actualizar ultima_actualizacion.
Espera mi OK para guardar.
```

## Procesar un chat de WhatsApp

Exporta el chat sin archivos, mueve el `.txt` a `00 Inbox` y pide:

```
Lee el chat exportado en 00 Inbox, solo desde el 1 de noviembre. Extrae acuerdos (quién, qué, cuándo) y preguntas sin responder.
```

Un chat contiene mensajes de otras personas. Antes de guardar algo, pregúntate si alguien se sentiría incómodo de que quede en tu bóveda o lo lea una IA.

## Procesar un audio o nota de voz

```
Esto es lo que pensé manejando. Sepáralo en ideas, pendientes y decisiones, y propón a qué nota va cada cosa.
```

## Resumir

```
Te adjunto el reglamento interno. Crea en 60 Recursos una nota con las 10 reglas que me afectan como coordinadora, con su número de página.
```

```
Antes de mi llamada con [[Ana López]]: resume la última conversación, los acuerdos abiertos y qué no debo olvidar.
```

## Buscar y relacionar

```
¿Qué he escrito sobre la sede del evento en el último mes? Cita la nota y la fecha de cada cosa.
```

```
¿Qué ideas del Inbox se relacionan con mis proyectos activos? Propón a cuál enlazar cada una.
```

Pide siempre que cite la nota de donde sacó cada dato: así verificas en un clic.

## Revisión diaria (10 minutos)

```
Haz mi revisión diaria. Lee mi nota de ayer en 10 Diario, el Inbox, 50 Tareas y los proyectos con estado: activo.
1. Propón mi Top 3 de hoy y por qué.
2. Dime qué NO debería hacer hoy.
3. Acuerdos y tareas que vencen esta semana.
4. Clasifica cada línea del Inbox: acción · contexto · evidencia · decisión · ruido.
Crea la nota de hoy con la plantilla Diaria cuando yo apruebe.
```

## Revisión semanal (30 minutos, cada viernes)

```
Haz mi revisión semanal con 10 Diario de esta semana, 00 Inbox, 20 Personas, 30 Proyectos y 50 Tareas.
1. Proyectos sin siguiente acción: ¿seguir, pausar o archivar?
2. Personas con pendiente o sin contacto en 30 días.
3. Acuerdos abiertos: quién · qué · cuándo. Tareas vencidas o bloqueadas.
4. Decisiones de la semana y su porqué.
5. Propón mi Top 3 de la próxima semana.
Usa la plantilla Revisión semanal. No cambies nada sin mostrarme la lista.
```

## Acuerdos

Un acuerdo se escribe en una línea:

```
- [ ] [[Luis Pérez]] · manda el contrato · 2026-11-14 · fuente: llamada 2026-11-10
```

Frases que delatan un acuerdo: "te lo mando", "lo reviso", "quedamos en...", "nos vemos el...", "vence el...", "yo me encargo".

```
Busca en 20 Personas todos los acuerdos sin marcar, ordénalos por fecha y dime cuáles vencieron.
```

## Con conectores

Los prompts que leen correo, calendario y chats están en [conexiones.md](conexiones.md).
