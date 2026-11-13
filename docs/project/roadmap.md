# Plan del proyecto

Lo previsto, por etapa y por módulo. Cada módulo se construye entero (reglas, pantallas, diseño,
código, pruebas y manual) y se cierra cuando Carlos lo prueba y lo escucha; recién entonces
empieza el siguiente. Este archivo es la fuente de verdad de las tareas: los issues de GitHub no
se usan.

**Estado:** propuesta. Vale cuando Carlos lo apruebe (T001).

## Etapas

| Etapa | Qué pasa | Termina cuando |
|---|---|---|
| 0. La base | Carlos aprueba la constitución, prueba el idioma simple con una maqueta que suena y se eligen las tecnologías | Están cerradas las tareas T001 a T007 |
| a. Desarrollo | Se construyen los módulos, en el orden de abajo. Hay un solo ambiente: pruebas | Están los módulos 01 a 08: una canción completa, con efectos, que se puede guardar y llevar |
| b. Pruebas reales | La usan una persona que no sabe teoría y una que sí, y se corrige lo que reportan. Se construyen los módulos 09 a 11 | No queda nada reportado sin resolver |
| c. Publicación | Primera versión pública, en GitHub Pages | — |

## Tareas de la base

| Tarea | Qué | Depende de | Estado |
|---|---|---|---|
| T001 | Carlos lee la [constitución](constitution.md) y este plan, los cuestiona y los aprueba. Contesta «Lo que falta decidir», abajo | — | Libre |
| T002 | **La prueba del idioma simple.** Una maqueta que suena, sin el resto de la aplicación: la escalera, el clima, la grilla, el fondo con sus colores y un camino listo. Carlos intenta hacer una melodía sin que nadie le explique nada. Lo que no entienda, se cambia | T001 | Libre |
| T003 | El [idioma simple](simple-language.md) y el [glosario](glossary.md), corregidos con lo que salió de T002 y aprobados | T002 | Libre |
| T004 | Los [ADR](../technical/adr/README.md) de la base, cada uno con sus opciones, y `docs/technical/architecture.md` | T001 | Libre |
| T005 | El esqueleto: el repositorio de código, `pnpm check` con todos sus controles y el despliegue al ambiente de pruebas, con una pantalla vacía | T004 | Libre |
| T006 | Los agentes y el skill de los nueve pasos, adaptados de Ferrebress: `art-director` (con maquetas que suenan), `mockup-builder`, `design-reviewer`, `code-reviewer`, y el nuevo `music-reviewer` | T001 | Libre |
| T007 | El lenguaje visual de partida y el visor de maquetas (`docs/design/`) | T002 | Libre |

## Módulos, en orden

El mismo nombre se usa en el capítulo (`docs/chapters/NN-<module>/`), en el diseño técnico
(`docs/technical/modules/<module>.md`) y en el código (`src/modules/<module>/`). Cada módulo
termina en algo que se puede escuchar.

| # | Módulo | Qué cubre | Por qué en este lugar | Depende de | Estado |
|---|---|---|---|---|---|
| 00 | `app` | Las reglas generales: el marco, cambiar de vista, el puente, el detalle fino, deshacer, el teclado, reproducir y parar, las esperas | No se construye solo: cada regla se construye con el primer módulo que la necesita | — | Por escribir |
| 01 | `melody` | En dos etapas. **a. La melodía en la vista simple:** la grilla y la escalera, poner, mover, alargar y borrar bloques, que suene al tocar, reproducir en vuelta, la velocidad, el clima y correr la canción, con un solo instrumento. Con él nace la base: la canción, el motor de sonido y deshacer. **b. La misma melodía en la vista de teoría:** las notas con su nombre, la tonalidad, el modo, el tempo y el compás, y el cambio de vista | Es lo que da nombre a la aplicación. La b va pegada para que las dos vistas existan desde el primer módulo: si la de teoría se deja para después, la canción se diseña solo para la simple | a: T003, T005; b: 01a | Por escribir |
| 02 | `songs` | Mis canciones: se guarda sola, abrir, nombre, copiar, borrar y recuperar lo borrado | En cuanto hay algo que vale la pena no perder | 01a | Por escribir |
| 03 | `instruments` | Elegir el instrumento de una capa, varias capas de melodía, volumen, silenciar y «solo esta» | Pedido de Carlos; cambia más el resultado que cualquier otra cosa | 01a | Por escribir |
| 04 | `rhythm` | La capa de ritmo: la grilla de golpes, los ritmos listos, el balanceo | Con ritmo, una melodía ya parece una canción | 03 | Por escribir |
| 05 | `harmony` | El fondo: elegir el fondo de cada vuelta, los caminos listos, apoya y tira, la manera de tocar el fondo, el bajo que lo sigue. En la vista de teoría, los acordes con su nombre y su grado | Es la pieza más difícil del idioma simple y la que más necesita lo anterior andando | 01b, 03 | Por escribir |
| 06 | `effects` | Los efectos de cada capa y los de toda la canción. Una perilla por efecto en la vista simple; todos los parámetros en la de teoría | Pedido de Carlos; necesita las capas | 03 | Por escribir |
| 07 | `structure` | Las partes: crear, nombrar, repetir, ordenar y copiar | Recién cuando hay con qué llenar una canción entera | 04, 05 | Por escribir |
| 08 | `export` | Llevarse la canción: descargarla como audio, como MIDI y como archivo de Sinfonia, y abrir uno que viene de afuera | Cierra la etapa a: lo hecho sirve fuera de la aplicación | 02, 06, 07 | Por escribir |
| 09 | `draw` | Dibujar la melodía con una línea | Otra manera de entrar una melodía, sobre la grilla ya probada | 01a | Por escribir |
| 10 | `capture` | Tararear o silbar al micrófono, marcar un ritmo golpeando, tocar con el teclado de la computadora o con un teclado MIDI | Es lo más cercano a la vara del principio II, y lo más difícil de hacer bien | 01a, 04 | Por escribir |
| 11 | `score` | El pentagrama en la vista de teoría: ver la canción como partitura y sacarla en PDF | Solo le sirve a quien sabe teoría, y es caro | 05, 07 | Por escribir |

## Lo que no se hace

Decidido por Carlos (constitución, principio VI):

- **Ni servidor ni cuentas.** Todo se genera en el navegador y la canción se descarga como
  archivo.
- **Nada de inteligencia artificial ni de ideas propuestas por la aplicación:** la edición es
  puramente humana. Lo listo para elegir (caminos, ritmos) sí está.
- **Ni voz ni letra:** solo instrumentos y efectos.

## Lo que falta decidir

Preguntas para Carlos (T001). Cada una, con lo que se propone.

1. **¿Solo castellano?** Se propone que sí, por ahora, con los textos separados del código para
   poder traducir después. El idioma simple habría que diseñarlo de nuevo en cada lengua.
2. **¿Instrumentos grabados o sintetizados?** Los sintetizados no pesan nada y suenan a
   electrónica; los grabados (un piano, una guitarra de verdad) suenan mejor y pesan varios MB
   cada uno. Se propone empezar el módulo 01 con uno sintetizado y decidirlo en el 03, con un ADR.
3. **¿Tararear al micrófono (módulo 10)?** No es voz en la canción: el micrófono solo sirve para
   anotar la melodía en la grilla. Si tampoco va, el módulo queda en marcar el ritmo y el teclado.
4. **¿El orden?** Si los efectos importan más que el ritmo o el fondo, el 06 puede ir justo
   después del 03.
5. **¿El nombre de las vistas?** «Vista simple» y «vista de teoría» son nombres de trabajo.
