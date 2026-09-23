# De Deal a Feed

Videojuego de estudio para aprender 10 verbos irregulares en pasado del quiz de inglés.

| Verbo | Pasado | Participio | Significado |
|---|---|---|---|
| deal | dealt | dealt | tratar, lidiar con |
| dig | dug | dug | cavar |
| do (does) | did | done | hacer |
| draw | drew | drawn | dibujar |
| dream | dreamt / dreamed | dreamt / dreamed | soñar |
| drink | drank | drunk | beber |
| drive | drove | driven | conducir |
| eat | ate | eaten | comer |
| fall | fell | fallen | caer |
| feed | fed | fed | alimentar |

El quiz solo pide el **pasado simple** (columna "Pasado"). El participio queda de referencia en el Verbodex, por si el profe lo usa más adelante.

## Cómo se juega

Un mapa de misión espacial con 10 planetas + un jefe final. Cada planeta es un minijuego distinto:

- **Meteoritos** — dispara la respuesta correcta antes de que el meteorito llegue al suelo.
- **Revienta globos** — completa la frase reventando el globo con el pasado correcto.
- **Memoria** — encuentra cada verbo con su pasado en un tablero de cartas.
- **Deletrea** — arma la palabra letra por letra, sin ver la respuesta.
- **Verdadero o falso** — decide rápido si el pasado mostrado es correcto.
- **Jefe final (El Profesor del Vacío)** — escribes tú mismo, sin pistas ni opciones, como el quiz real.

Tiene vidas (corazones), racha de combo, puntaje, 3 estrellas por nivel, rango por XP, logros, sonidos sintetizados (sin archivos externos) y confeti. El progreso se guarda en el navegador de cada persona (localStorage).

También hay pestañas de **Verbodex** (los 10 verbos por tipo, tabla con las 4 columnas y la historia del tesoro) y **Arcade** (práctica libre sin bloqueos, incluye repetir al jefe cuando quieras).

## Cómo usarla

Abre `index.html` en el navegador (mejor en Chrome). Es un solo archivo, sin instalación ni conexión a internet.

## Cambiar los verbos

Los datos están al inicio del `<script>` de `index.html`: `VERBS` (verbo, pasado, participio, significado, frases y errores típicos — `altPast`/`altPart` para verbos con dos formas válidas como dream), `TYPES` (los patrones de memoria), `STORY` (el cuento) y `LEVELS` (qué verbos y qué minijuego tiene cada planeta del mapa).
