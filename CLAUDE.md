# CLAUDE.md

## Qué es esta carpeta

Es el second brain del alumno: una bóveda de Obsidian con notas en markdown. Léela antes de responder cualquier cosa sobre su trabajo, sus personas o sus proyectos.

## Reglas de escritura

- Trabaja solo con archivos markdown (`.md`) y bases (`.base`). Nunca edites `.obsidian/`.
- Antes de crear una nota, busca si ya existe una sobre lo mismo. Actualiza la existente en vez de duplicar.
- Toda nota lleva sus propiedades al inicio y al menos un [[wikilink]].
- Si no sabes dónde va algo, pregunta. No lo adivines.
- Una nota por entidad. El archivo se llama como la persona, el proyecto o la tarea.
- Nunca borres una captura. Cuando ya la procesaste, muévela a `00 Inbox/procesado/`.

## Buscar antes de contestar

- Busca en la bóveda antes de contestar de memoria: propiedades, nombres y enlaces.
- Si no encuentras nada, dilo. No inventes datos ni fechas.
- Si una propiedad está vacía, es que no hay evidencia. No la rellenes por deducción.

## Propiedades

Van entre dos líneas de tres guiones al inicio de la nota. Nombres sin acentos ni ñ, fechas siempre como `YYYY-MM-DD`, y `estado` de una lista corta.

| Tipo | Propiedades |
| --- | --- |
| Persona | `tipo`, `estado` (activa, pausada, archivada), `ultima_revision`, `ultimo_contacto`, `siguiente_accion`, `fuente`, `area`, `organizacion`, `rol` |
| Proyecto | `tipo`, `estado` (activo, pausado, cerrado), `ultima_revision`, `ultima_actualizacion`, `responsable`, `siguiente_accion`, `responsable_siguiente`, `fuente`, `fuente_oficial`, `area`, `fecha_cierre` |
| Tarea | `tipo`, `estado` (pendiente, en curso, bloqueada, hecha), `proyecto`, `responsable`, `fecha_limite`, `siguiente_accion`, `fuente` |
| Decisión | `tipo`, `estado` (abierta, tomada, descartada), `responsable`, `fecha_limite`, `proyecto`, `fuente` |
| Área | `tipo`, `estado` (activa, referencia), `revision`, `ultima_revision` |

- `siguiente_accion` es una sola acción que empieza con verbo, y solo se llena si hay evidencia en la bóveda. Vacío es válido.
- `ultimo_contacto` es la última interacción real, no la última vez que alguien revisó la nota (eso es `ultima_revision`).
- `ultima_actualizacion` es el último cambio real del proyecto.
- `responsable_siguiente` es `yo`, `esperando` (nombra a la persona en `siguiente_accion`) o `ninguno`.
- `fuente` es texto corto y verificable, por ejemplo "llamada 2026-11-10".
- Una nota sin propiedades queda fuera de las búsquedas y de las vistas.

## Enlaces

- Los proyectos enlazan a sus personas clave y a su área. Las personas enlazan a sus proyectos.
- Una tarea siempre enlaza a su proyecto o a su persona: una tarea suelta se pierde.
- Enlaza con `[[Nombre]]`, sin ruta, como se llama el archivo.

## Dónde va cada cosa

La primera pregunta que se responda con sí te dice la carpeta.

| Pregunta | Va en |
| --- | --- |
| ¿Todavía no sé qué es ni dónde vive? | 00 Inbox |
| ¿Es sobre una persona y lo que hablamos? | 20 Personas |
| ¿Tiene entregable y puede terminarse? | 30 Proyectos |
| ¿Es una responsabilidad que no termina? | 40 Áreas |
| ¿Es un compromiso con fecha, un bloqueo o algo que depende de mí? | 50 Tareas |
| ¿Lo voy a consultar, pero no me pide acción? | 60 Recursos |
| ¿Ya terminó o dejó de importar? | 90 Archivo |

Si no cambia ninguna acción, decisión ni relación, es ruido y no se guarda. Si dudas, la nota se queda en el Inbox hasta la siguiente revisión.

Una tarea se crea solo cuando pasa la prueba: compromiso, bloqueo o fecha límite. Si no pasa, se queda como contexto en su proyecto o persona.

Una decisión abierta necesita responsable, fecha límite y el lugar donde se resuelve. Se escribe con la plantilla `Decisión`, junto al proyecto al que pertenece.

Las notas diarias viven en `10 Diario`, las revisiones y sus vistas en `70 Revisiones`, las plantillas en `80 Plantillas` y los adjuntos en `85 Adjuntos`.

## Al empezar

1. Lee `Inicio.md`.
2. Lee el diario de hoy en `10 Diario`, si existe (se llama `YYYY-MM-DD.md`).
3. Revisa `00 Inbox`.
4. Si te piden una revisión, abre `70 Revisiones/Tablero.md`.
