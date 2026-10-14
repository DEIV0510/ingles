# De Hit a Lean

Videojuego de estudio para aprender 10 verbos irregulares en pasado del quiz de inglés.

| Verbo | Pasado | Participio | Significado |
|---|---|---|---|
| hit | hit | hit | golpear |
| hold | held | held | sostener, agarrar |
| hurt | hurt | hurt | lastimar, doler |
| keep | kept | kept | guardar, mantener |
| know | knew | known | saber, conocer |
| kneel | knelt (o kneeled) | knelt / kneeled | arrodillarse |
| knit | knit (o knitted) | knit / knitted | tejer |
| lay | laid | laid | poner, colocar |
| lead | led | led | guiar, liderar |
| lean | leant (o leaned) | leant / leaned | apoyarse, inclinarse |

El quiz solo pide el **pasado simple** (columna "Pasado"). El participio queda de referencia en el Verbodex. La tabla del profe solo traía verbo y pasado; el participio y el significado se agregaron para el Verbodex.

Tres verbos no cambian (**hit, hurt, knit**) y tres tienen una forma regular también válida (**kneeled, knitted, leaned**): el jefe final las acepta pero avisa que la lista pide la principal.

## Cómo se juega

Un mapa de misión espacial con 10 planetas + un jefe final. Cada planeta es un minijuego distinto:

- **Meteoritos** — dispara la respuesta correcta antes de que el meteorito llegue al suelo.
- **Revienta globos** — completa la frase reventando el globo con el pasado correcto.
- **Memoria** — encuentra cada verbo con su pasado en un tablero de cartas.
- **Deletrea** — arma la palabra letra por letra, sin ver la respuesta.
- **Verdadero o falso** — decide rápido si el pasado mostrado es correcto.
- **Jefe final (El Profesor del Vacío)** — escribes tú mismo, sin pistas ni opciones, como el quiz real. Tiene una vida por verbo.

Tiene vidas (corazones), racha de combo, puntaje, 3 estrellas por nivel, rango por XP, logros, sonidos sintetizados (sin archivos externos) y confeti. El progreso se guarda en el navegador de cada persona (localStorage). **Cada lista nueva de verbos empieza un mapa nuevo** (estrellas, dominados y logros desde cero); el XP y el sonido se conservan.

También hay pestañas de **Verbodex** (los verbos por tipo, tabla con las 4 columnas y la historia de la bufanda del perro) y **Arcade** (práctica libre sin bloqueos, incluye repetir al jefe cuando quieras).

## Pestaña «Did?»: negativo e interrogativo (Misión 2)

Los mismos 10 verbos, pero en **negativa** (*She didn't hold…*) y en **pregunta** (*Did she hold…?*). La idea que se practica: con *did / didn't* el verbo **vuelve a su forma normal** (didn't hold, no ~~didn't held~~).

- **Lección interactiva** «El truco de did»: eliges un verbo y ves la frase afirmativa, la negativa y la pregunta con cada palabra coloreada por su función.
- **Tabla de referencia** con los 10 verbos en las tres formas (con audio), y un cuadro «Negativo y pregunta» en la ficha de cada verbo.
- **Mapa de 9 niveles** (con su propio jefe: *El Profesor del Vacío II*) y 5 juegos:
  - **Memoria** — une cada pasado con su negativa (*held* ↔ *didn't hold*).
  - **Completa** — globos con el verbo en forma normal (la trampa: el pasado).
  - **¿Bien o mal?** — decide si la frase está bien escrita; te explica el error.
  - **Arma la frase** — toca las palabras en orden para armar la negativa o la pregunta.
  - **Transforma** (jefe) — escribes tú la negativa o la pregunta de una frase afirmativa. Acepta *did not* y *didn't*, mayúsculas y sin signo final; te dice si pusiste el verbo en pasado, copiaste la afirmativa o usaste *do/does*.
- Los aciertos de esta misión **no** suben el «dominado» del pasado (eso mide lo que pide el quiz) ni activan el logro «Sin ayuda». Tiene 3 logros propios.

## Cómo usarla

Abre `index.html` en el navegador (mejor en Chrome). Es un solo archivo, sin instalación ni conexión a internet.

## Cambiar los verbos

Los datos están al inicio del `<script>` de `index.html`: `VERBS` (verbo, pasado, participio, significado, 10 frases y errores típicos — `altPast`/`altPart` para verbos con dos formas válidas, como *knelt/kneeled*, y `notes` para avisos propios de una respuesta equivocada, como *lent* en lean), `TYPES` (los patrones de memoria), `STORY` (el cuento, un verbo por línea), `LEVELS` (qué verbos y qué minijuego tiene cada planeta del mapa), `LEVELS_Q` (lo mismo para la Misión 2) y `FORM_ROWS` (5 frases por verbo para negativo/pregunta: solo se escribe el sujeto, el resto y las 3 traducciones; el inglés de las tres formas se arma solo). Además hay que cambiar el `<title>` de la página. Todo lo demás (logo, contadores, jefes, textos) sale solo de esos datos. El progreso guardado se reinicia solo al cambiar los verbos (firma `LIST_SIG` = ids de la lista).

Si un verbo no cambia entre base y pasado (como *hit*, *hurt* y *knit*), el generador de opciones y de trampas ya lo detecta: no repite fichas, no genera una trampa imposible y, donde la frase "mal" saldría igual a la buena, usa la forma con -ed.
