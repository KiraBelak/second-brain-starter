# Second brain starter

Bóveda de Obsidian para el curso Tu second brain con IA, sesión 01. Es la misma estructura que montamos en clase, ya armada, para que puedas empezar o ponerte al día si te quedó algo pendiente.

## Qué es esto

Una carpeta con once carpetas numeradas, una nota de inicio, tres plantillas y cuatro notas de ejemplo (más una nota diaria y una de área) para ver cómo se ve todo conectado. Los datos son inventados. Bórralos cuando quieras y escribe los tuyos.

## Cómo abrirla en Obsidian

1. Instala Obsidian desde obsidian.md.
2. En esta página de GitHub, pulsa el botón verde Code y elige Download ZIP.
3. Descomprime el archivo y mueve la carpeta a Documentos.
4. En Obsidian elige Open folder as vault y selecciona esa carpeta.

La carpeta `.obsidian` ya viene incluida con los ajustes del curso. Obsidian la lee al abrir la bóveda.

## Qué hay en cada carpeta

- `Inicio.md`: tu panel de mando. Enlaza a lo que quieres mirar primero.
- `00 Inbox`: todo entra aquí primero. Incluye `Inbox.md` con tres capturas de ejemplo y la subcarpeta `procesado/`, donde se mueven las capturas ya procesadas.
- `10 Diario`: notas diarias, nombradas `YYYY-MM-DD`.
- `20 Personas`: relaciones y acuerdos. Una nota por persona.
- `30 Proyectos`: trabajo con entregable y fecha de cierre.
- `40 Áreas`: responsabilidades que se mantienen.
- `50 Tareas`: un compromiso con fecha, un bloqueo o algo que depende de ti. Una nota por tarea.
- `60 Recursos`: material de consulta que no pide acción.
- `70 Revisiones`: notas de tus revisiones periódicas.
- `80 Plantillas`: `Persona.md`, `Proyecto.md` y `Tarea.md`, con las propiedades del curso.
- `85 Adjuntos`: imágenes y archivos.
- `90 Archivo`: lo que ya terminó o dejó de importar.

Los números mantienen siempre el mismo orden y dejan huecos para agregar carpetas sin desordenar; por ejemplo, el 32 queda libre. Cada carpeta trae un `_README.md` o un ejemplo; puedes borrarlos cuando ya no los necesites.

## Ajustes de Obsidian

No tienes que hacerlos a mano: `.obsidian/` ya los trae. Esto es lo que cambia respecto a una bóveda nueva:

1. Notas nuevas caen en `00 Inbox`.
2. Adjuntos nuevos caen en `85 Adjuntos`.
3. Plantillas activo, con la carpeta `80 Plantillas`.
4. Notas diarias con formato `YYYY-MM-DD` en la carpeta `10 Diario`.
5. Bases y Recuperación de archivos activos.

Para verlos, abre Ajustes con el engrane abajo a la izquierda, o con Ctrl/Cmd + coma. Con los complementos principales alcanza para todo el curso. No instales complementos de la comunidad por ahora.

## Para Claude

Si usas Claude con esta carpeta, él lee `CLAUDE.md` al empezar. Ahí están las reglas de la bóveda y la tabla de dónde va cada cosa.

## Dónde va cada cosa

Hazte estas preguntas en este orden. La primera respuesta que sea sí te dice la carpeta.

| Pregunta | Va en |
| --- | --- |
| ¿Todavía no sé qué es ni dónde vive? | 00 Inbox |
| ¿Es sobre una persona y lo que hablamos? | 20 Personas |
| ¿Tiene entregable y puede terminarse? | 30 Proyectos |
| ¿Es una responsabilidad que no termina? | 40 Áreas |
| ¿Es un compromiso con fecha, un bloqueo o algo que depende de mí? | 50 Tareas |
| ¿Lo voy a consultar, pero no me pide acción? | 60 Recursos |
| ¿Ya terminó o dejó de importar? | 90 Archivo |

Si no cambia ninguna acción, decisión ni relación, es ruido y no se guarda. Descartar también es decidir.

Solo los compromisos se convierten en acciones. Un compromiso tiene una acción concreta, alguien responsable y un siguiente paso. Lo demás se guarda como contexto o como evidencia, o se descarta. Si dudas, la nota se queda en el Inbox hasta la siguiente revisión.

Para distinguir proyecto de área, pregúntate si puedes decir "ya terminé". Si puedes, es un proyecto.

## Propiedades de las notas

Las propiedades van entre dos líneas de tres guiones al inicio de la nota. Obsidian las muestra como una tabla editable.

Persona: `tipo`, `estado` (activa, pausada, archivada), `rol`, `organizacion`, `ultimo_contacto`, `siguiente_accion`.

Proyecto: `tipo`, `estado` (activo, pausado, cerrado), `area`, `fecha_cierre`, `siguiente_accion`.

Tarea: `tipo`, `estado` (pendiente, en curso, hecha), `proyecto`, `fecha_limite`, `siguiente_accion`.

Tres reglas: nombres sin acentos ni ñ, fechas siempre como `YYYY-MM-DD`, y `estado` siempre de una lista corta. `siguiente_accion` solo se llena si hay evidencia. Sin propiedades, una nota no aparece en las búsquedas ni en las vistas que haremos más adelante.

## Tus primeros 7 días

1. Día 1: abre la bóveda, revisa que los cinco ajustes estén y borra los ejemplos que no quieras.
2. Día 1: crea la nota de una persona con la plantilla y enlázala a un proyecto tuyo con `[[ ]]`. Abre la persona y mira Enlaces entrantes en el panel derecho.
3. Días 2 al 7: captura al menos tres cosas al día en `00 Inbox/Inbox.md`, con fecha, qué es y de dónde salió.
4. Al final de cada día, procesa el Inbox: cada línea va a una carpeta y la captura se mueve a `00 Inbox/procesado/`. Nada se borra.
5. Para la sesión 02: ten notas de tres personas y dos proyectos, aunque estén casi vacías, y trae las notas o la transcripción de una reunión reciente. Si tiene información sensible, trae otra o anonimízala.

## Licencia

MIT. Consulta el archivo `LICENSE`.
