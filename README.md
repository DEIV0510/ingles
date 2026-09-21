# De Burst a Crept

Videojuego de estudio para aprender los 10 verbos irregulares en pasado del quiz de inglés.

| Verbo | Pasado | Significado |
|---|---|---|
| burst | burst | reventar, estallar |
| buy | bought | comprar |
| cast | cast | lanzar, arrojar |
| catch | caught | atrapar, agarrar |
| come | came | venir, llegar |
| cost | cost | costar |
| cut | cut | cortar |
| choose | chose | elegir, escoger |
| cling | clung | aferrarse |
| creep | crept | moverse sigilosamente |

## Cómo se juega

Un mapa de misión espacial con 10 planetas + un jefe final. Cada planeta es un minijuego distinto:

- **Meteoritos** — dispara la respuesta correcta antes de que el meteorito llegue al suelo.
- **Revienta globos** — completa la frase reventando el globo con el pasado correcto.
- **Memoria** — encuentra cada verbo con su pasado en un tablero de cartas.
- **Deletrea** — arma la palabra letra por letra, sin ver la respuesta.
- **Verdadero o falso** — decide rápido si el pasado mostrado es correcto.
- **Jefe final (El Profesor del Vacío)** — escribes tú mismo, sin pistas ni opciones, como el quiz real.

Tiene vidas (corazones), racha de combo, puntaje, 3 estrellas por nivel, rango por XP, logros, sonidos sintetizados (sin archivos externos) y confeti. El progreso se guarda en el navegador de cada persona (localStorage).

También hay pestañas de **Verbodex** (los 10 verbos por tipo, tabla y la historia de la pizza) y **Arcade** (práctica libre sin bloqueos, incluye repetir al jefe cuando quieras).

## Cómo usarla

Abre `index.html` en el navegador (mejor en Chrome). Es un solo archivo, sin instalación ni conexión a internet.

## Cambiar los verbos

Los datos están al inicio del `<script>` de `index.html`: `VERBS` (verbo, pasado, significado, frases y errores típicos), `TYPES` (los 4 patrones de memoria), `STORY` (el cuento) y `LEVELS` (qué verbos y qué minijuego tiene cada planeta del mapa).
