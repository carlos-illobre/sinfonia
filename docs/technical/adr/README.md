# Decisiones técnicas (ADR)

Una decisión técnica que afecta a más de un módulo, con las opciones consideradas y el porqué.
Cada ADR describe la decisión vigente; si cambia, se reescribe, y la historia está en los commits.
Cada tecnología elegida tiene su ADR (constitución, «Restricciones técnicas»).

Ninguno está escrito todavía: se escriben en la tarea T004 del [plan](../../project/roadmap.md),
cada uno con sus opciones, pros y contras. La columna «Se propone» es el punto de partida, no una
decisión.

| ADR | Qué decide | Se propone | Estado |
|---|---|---|---|
| ADR-001 | Una sola aplicación, sin servidor, con las canciones en el dispositivo | Una PWA estática; las canciones en IndexedDB | Por escribir |
| ADR-002 | Cómo se guarda una canción para que las dos vistas sean la misma canción, y el formato del archivo de Sinfonia | Un archivo de texto propio, de líneas, no JSON: una línea por vuelta, con su minuto y segundo, dentro de cada capa y cada parte (constitución, principio VI). Cada sonido se guarda como escalón más un ajuste fino, relativo al clima y a la tonalidad; la altura absoluta se calcula. Así cambiar de clima conserva el dibujo y la vista de teoría puede poner cualquier nota | Por escribir |
| ADR-003 | El motor de sonido y quién lleva el tiempo | Web Audio, con el reloj del audio y lo que va a sonar programado por adelantado; a evaluar Tone.js contra un motor propio chico | Por escribir |
| ADR-004 | TypeScript, pnpm y las bibliotecas de la aplicación | Lo mismo que Ferrebress: Preact, Vite, CSS común y piezas propias | Por escribir |
| ADR-005 | Cómo se prueba la música sin parlantes | La canción se convierte en una lista de eventos con funciones puras, y las pruebas comparan la lista; el audio de verdad, en pocas pruebas en un navegador con audio sin tiempo real | Por escribir |
| ADR-006 | Qué controla `pnpm check` | Lo de Ferrebress, más el control de las tres capas y el de las palabras de la vista simple | Por escribir |
| ADR-007 | Dónde se publica | GitHub Pages, pública (decidido por Carlos); falta resolver dónde va el ambiente de pruebas | Por escribir |
| ADR-008 | Deshacer y rehacer | Todo cambio a la canción es un comando que se puede revertir | Por escribir |

Con su módulo: cómo se sintetizan los instrumentos, de qué colección salen los grabados (con su licencia, su
peso y cómo se bajan de a uno), reconocer lo que se tararea, y el pentagrama.
