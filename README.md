# De Feel a Freeze

Videojuego de estudio para aprender 9 verbos irregulares en pasado del quiz de inglés.

| Verbo | Pasado | Participio | Significado |
|---|---|---|---|
| feel | felt | felt | sentir |
| fight | fought | fought | luchar |
| find | found | found | encontrar |
| flee | fled | fled | huir |
| fly | flew | flown | volar |
| forbid | forbade | forbidden | prohibir |
| forget | forgot | forgotten | olvidar |
| forgive | forgave | forgiven | perdonar |
| freeze | froze | frozen | helar |

El quiz solo pide el **pasado simple** (columna "Pasado"). El participio queda de referencia en el Verbodex.

> La tabla original traía 9 verbos (las anteriores traían 10). Si el profe agrega un décimo, es agregarlo a `VERBS` en `index.html`: el juego se adapta solo a la cantidad.

## Cómo se juega

Un mapa de misión espacial con 10 planetas + un jefe final. Cada planeta es un minijuego distinto:

- **Meteoritos** — dispara la respuesta correcta antes de que el meteorito llegue al suelo.
- **Revienta globos** — completa la frase reventando el globo con el pasado correcto.
- **Memoria** — encuentra cada verbo con su pasado en un tablero de cartas.
- **Deletrea** — arma la palabra letra por letra, sin ver la respuesta.
- **Verdadero o falso** — decide rápido si el pasado mostrado es correcto.
- **Jefe final (El Profesor del Vacío)** — escribes tú mismo, sin pistas ni opciones, como el quiz real. Tiene una vida por verbo.

Tiene vidas (corazones), racha de combo, puntaje, 3 estrellas por nivel, rango por XP, logros, sonidos sintetizados (sin archivos externos) y confeti. El progreso se guarda en el navegador de cada persona (localStorage).

También hay pestañas de **Verbodex** (los verbos por tipo, tabla con las 4 columnas y la historia del dragón de hielo) y **Arcade** (práctica libre sin bloqueos, incluye repetir al jefe cuando quieras).

## Cómo usarla

Abre `index.html` en el navegador (mejor en Chrome). Es un solo archivo, sin instalación ni conexión a internet.

## Cambiar los verbos

Los datos están al inicio del `<script>` de `index.html`: `VERBS` (verbo, pasado, participio, significado, 10 frases y errores típicos — `altPast`/`altPart` para verbos con dos formas válidas), `TYPES` (los patrones de memoria), `STORY` (el cuento, un verbo por línea) y `LEVELS` (qué verbos y qué minijuego tiene cada planeta del mapa). Además hay que cambiar el `<title>` de la página. Todo lo demás (logo, contadores, jefe, textos) sale solo de esos datos.
