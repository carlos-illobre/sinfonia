# Constitución de Sinfonia

Lo que no se negocia. Todo capítulo, diseño, tarea y línea de código se revisa contra este
documento; si algo lo contradice, se cambia ese algo o se cambia la constitución con la
aprobación de Carlos.

**Estado:** propuesta. Vale cuando Carlos la apruebe (tarea T001 del [plan](roadmap.md)).

## Principios

### I. La documentación manda y no depende del código

Lo fijo son las reglas; el código puede rehacerse en cualquier momento. La documentación tiene
que alcanzar para que alguien que nunca vio el código construya de nuevo una aplicación que
cumpla todas las reglas, funcionales y no funcionales.

- **El orden de autoridad.** Ante una diferencia, manda lo de más arriba y se corrige lo de abajo:
  1. Las reglas (`docs/chapters/`).
  2. Las maquetas aprobadas, en cómo se ve, cómo se usa y cómo suena.
  3. El diseño técnico (`docs/technical/`).
  4. Las pruebas, que se escriben desde los escenarios y antes que el código.
  5. El código, que se escribe para pasar las pruebas ya armadas.

  Una prueba nunca se cambia para que pase el código; si una prueba está mal, se corrige contra
  la regla.
- **La documentación principal está en `docs/`, fuera de `src/`.** Si se borra `src/`, no se
  pierde ninguna regla ni ningún diseño. Dentro de `src/` puede haber documentación que ayude a
  entender el código, nunca una regla que no esté también en `docs/`.
- **Los capítulos (`docs/chapters/`) dicen qué tiene que pasar y nunca cómo está hecho:** no
  nombran archivos, bibliotecas ni componentes, y no dicen si algo está construido. El diseño
  técnico de cada módulo vive en `docs/technical/modules/`.
- **No se escribe código de un módulo sin sus reglas, sus pantallas y su diseño técnico
  aprobados por Carlos.**
- **Ningún cambio queda solo en el código.**
- **El estado no se escribe a mano:** sale de las pruebas, que nombran el escenario que cubren.

### II. La vara es tararear

Quien no sabe nada de música tiene que poder armar, en su primer minuto y sin leer nada, una
melodía que suene bien. Una pantalla que hace eso más difícil que tararear y grabarse con el
celular está mal, aunque sea más completa.

- **Nunca hay silencio ni pantalla vacía:** una canción nueva ya suena, y el estado vacío dice
  qué tocar.
- **Todo lo que se toca, suena en el momento:** poner, mover o cambiar algo se escucha sin
  apretar «reproducir». Entre el toque y el sonido pasan menos de 50 ms.
- **Se puede cambiar todo mientras suena,** sin que la música se corte ni salte.
- **Deshacer siempre.** Nada se pierde por probar; por eso no hay ventanas de confirmación,
  salvo para lo que no se puede recuperar.
- **Los errores van en el lugar, en castellano, y dicen qué hacer.**
- Se aprende sin manual: cada pantalla se explica sola.

### III. Una canción, dos idiomas

Hay una sola canción y dos maneras de verla: la **vista simple**, para quien no sabe teoría
musical, y la **vista de teoría**, para quien sabe. No son dos aplicaciones ni dos formatos.

- **Se cambia de vista en cualquier momento, también mientras suena, y no se pierde nada.** Lo
  que se hizo en una se ve y se puede seguir en la otra.
- **La vista simple no usa ninguna palabra de la teoría musical:** ni nota, ni acorde, ni escala,
  ni compás, ni pentagrama, ni nombres de notas. Usa solo las del
  [idioma simple](simple-language.md).
- **Cada palabra del idioma simple tiene un solo equivalente en la teoría,** el del
  [glosario](glossary.md). Una palabra nueva se agrega ahí antes de usarla.
- **La vista de teoría puede más que la simple, nunca al revés.** Lo que la vista simple no sabe
  decir (lo que se hizo en la de teoría y no entra en el idioma simple), lo muestra marcado como
  «detalle fino», lo hace sonar igual y no lo rompe ni lo borra al editar alrededor.
- **El puente:** en la vista simple, cada cosa puede mostrar a pedido cómo se llama en la teoría.
  Quien quiere aprender, aprende; a quien no quiere, nunca se le aparece.
- **La funcionalidad que no depende del idioma es la misma en las dos vistas:** instrumentos,
  efectos, guardar, exportar.

### IV. En la vista simple, nada suena mal

La vista simple ofrece solo lo que combina: los sonidos del clima elegido, los fondos que le
corresponden, los golpes sobre el pulso. No hace falta saber por qué. Lo que tensa se muestra
como tensión, no como error, y nunca se prohíbe: se puede salir de la baranda a propósito, y
ahí avisa.

### V. Suena igual a como se ve, siempre

- **La misma canción suena igual cada vez,** en la aplicación y en lo que se exporta.
- **El tiempo lo lleva el reloj del audio, nunca un temporizador:** el pulso no se atrasa ni se
  adelanta aunque la pantalla esté ocupada.
- **Lo que se ve es lo que suena:** no hay nada que suene y no esté a la vista en alguna de las
  dos vistas, ni nada a la vista que no suene, salvo lo que está silenciado, que lo dice.

### VI. La canción es de quien la hizo

- **Sin cuenta y sin servidor:** la aplicación entera corre en el dispositivo, y las canciones se
  guardan ahí. Abierta una vez, anda sin internet.
- **Se guarda sola,** siempre. No existe «perdí lo que hice».
- **Se puede llevar:** toda canción sale como audio, como MIDI y como archivo de Sinfonia, y el
  formato del archivo está documentado en `docs/technical/`.
- **El micrófono se usa solo cuando la persona lo pide,** y lo que entra no sale del dispositivo.
- **Es pública y gratis:** una página de GitHub Pages que cualquiera abre y usa, sin registrarse.
  La infraestructura no cuesta nada.
- **La música la hace la persona.** No hay inteligencia artificial ni nada que componga: la
  aplicación ofrece cosas listas para elegir (caminos, ritmos, instrumentos) y saca del medio lo
  que no combina, pero cada sonido lo pone alguien.
- **Solo instrumentos y efectos.** No hay voz grabada ni letra. Los instrumentos son todos
  sintetizados: no se usan sonidos grabados.

### VII. Una sola aplicación para el celular y la computadora

La funcionalidad es exactamente la misma en los dos; cambia solo la disposición. Hay una sola
versión de cada pantalla, en HTML semántico, y el CSS la acomoda a cada ancho. En el celular se
usa con los dedos y sin desplazarse al costado, salvo a lo largo de la canción; en la
computadora, todo se puede hacer con el teclado y el mouse nunca es la única forma.

- **El color nunca es la única señal:** lo que se distingue por color se distingue también por
  número, forma o posición.
- **Si el sistema pide no animar, manda el sistema,** salvo lo que marca por dónde va la música.

### VIII. Primero la prueba, y «hecho» solo con evidencia

- Cada escenario de un capítulo tiene una prueba que lo nombra (`melody-E05`), escrita antes que
  el código.
- **Las pruebas usan el módulo como lo usa el resto de la aplicación:** por su fachada y por lo
  que ve, toca y escucha la persona. No prueban cómo está hecho por dentro.
- **La música se prueba sin parlantes.** Todo lo musical (qué suena, cuándo, a qué altura, con
  qué fuerza, con qué efecto) es una lista de eventos que sale de funciones sin navegador, y las
  pruebas comparan esa lista. Lo único que no se prueba así es lo que habla con el audio del
  dispositivo, en una lista corta con su ADR.
- **Pruebas unitarias rápidas:** todas juntas en menos de 30 segundos.
- **Cobertura del 100 % de líneas y ramas,** con esa única excepción.
- **Lo que una unitaria no puede probar, se prueba en un navegador de verdad:** que suene (que
  salga señal, a tiempo y sin cortes) y que el toque llegue.
- **La prueba de oído es de Carlos:** ningún módulo se cierra sin que lo haya escuchado.

### IX. Seguro por defecto

Ni secretos ni música ajena entran en el repositorio: todo sonido, muestra o fuente que se sume
tiene una licencia que lo permite, anotada donde está. Un archivo de canción que viene de afuera
se valida entero antes de abrirlo y nunca ejecuta nada. La aplicación no carga código de otros
sitios mientras se usa. El diseño técnico de cada módulo tiene su sección «Seguridad».

### X. Cada idioma en su lugar

- **Código en inglés, con las palabras de la teoría musical** (`note`, `chord`, `scale`,
  `tempo`): son las que entiende cualquier programador y cualquier biblioteca. También en inglés
  los nombres de archivos y carpetas de la documentación.
- **Castellano en todo lo demás:** el contenido de la documentación, los comentarios, los
  commits, los mensajes de error y los textos de la aplicación.
- **Tres columnas en el [glosario](glossary.md):** cómo se dice en la vista simple, cómo se dice
  en la vista de teoría y cómo se dice en el código. Cada concepto tiene una sola fila.
- **La vara de una palabra del idioma simple es Carlos:** si no la entiende sin que se la
  expliquen, la palabra está mal y se cambia.

### XI. La documentación describe el presente

- **Lo que decide Carlos se escribe donde corresponde,** como estado actual: una regla, en el
  capítulo que toca; cómo se trabaja, en esta constitución; una decisión técnica, en su ADR. Si
  cambia, se reescribe el texto: no se agregan enmiendas ni se guardan versiones viejas.
- **Sin fechas ni historia.** Cuándo y por qué cambió algo está en los commits, y cada commit
  explica el porqué.
- **El porqué que sigue valiendo sí se escribe:** un ADR dice las opciones descartadas y por qué;
  un capítulo puede decir qué no se hace y por qué, para que nadie lo vuelva a proponer.

### XII. Cómo se escribe el código

En este orden, y ante un empate se mira la siguiente:

1. **Simple:** los nombres de carpetas, archivos, tipos, funciones y variables funcionan como el
   índice de un libro. Baja complejidad, funciones cortas, un archivo por responsabilidad. Los
   comentarios dicen el porqué, no el qué.
2. **Rápido, sobre todo en el audio:** nada reserva memoria ni espera al disco o a la red
   mientras suena; lo que va a sonar se prepara antes. Cada módulo se baja recién cuando se abre,
   y los sonidos de un instrumento, recién cuando se elige.
3. **Sin repetir:** la lógica está una sola vez y cada lugar la usa. Las dos vistas comparten
   toda la lógica; lo único propio de cada una es cómo muestra y cómo nombra.
4. **Menos líneas y declarativo:** entre dos soluciones iguales en lo anterior, la de menos
   líneas. Nunca a costa de que se entienda.

Además:

- **Organizado por funcionalidad, no por capa técnica.** Un módulo tiene el mismo nombre en el
  capítulo, en el diseño técnico y en el código.
- **Tres capas que no se mezclan:** la música (qué es una canción y qué se le puede hacer, sin
  navegador ni audio), el sonido (convertir la canción en audio) y las vistas. La música no
  importa nada de las otras dos, y ninguna vista habla con el audio sin pasar por el sonido.
- **Carpetas chicas, agrupadas por concepto:** como mucho 20 archivos por carpeta, sin contar las
  pruebas.
- **Cada archivo se explica solo:** empieza con un comentario que dice de qué se encarga y por
  qué existe.
- **Los tiempos y los topes, con nombre y en un solo lugar:** cada módulo tiene los suyos en su
  `settings.ts`, y cada uno dice de qué regla sale.
- **Patrones solo donde sacan acoplamiento real**, de esta lista: fachada por módulo, estrategia
  donde hay variantes (los instrumentos, los efectos, las dos vistas), comando para todo cambio a
  la canción (así se deshace y se rehace), máquina de estados para cada proceso con pasos, y
  eventos para que un módulo reaccione a otro sin conocerlo. Un patrón fuera de la lista necesita
  un ADR.
- **Los límites se controlan con herramientas** en `pnpm check`, no con la buena voluntad.

## Restricciones técnicas

- **Cada tecnología elegida tiene su ADR**, con las opciones, sus pros y contras, y el porqué.
  Sumar una tecnología nueva (lenguaje, biblioteca de peso, servicio) necesita su ADR antes de
  usarla.
- **Una sola aplicación web, toda en TypeScript, sin servidor propio,** publicada en GitHub Pages
  (principio VI).
- **Equipo de referencia:** un celular Android de gama media y una notebook vieja. Si ahí suena
  sin cortes, está bien.

## Cómo se trabaja

**Todo se sube directo a `main`**, sin ramas ni pull requests. En una sesión en la nube que
arranca en una rama `claude/…`, se sube igual a `main` (`git push origin HEAD:main`).

### Los capítulos

Cada módulo es un capítulo en `docs/chapters/`, con un número fijo:

| Archivo | Qué tiene |
|---|---|
| `summary.md` | Una página para entrar rápido: cada regla en una línea, lo que más pesa y lo que falta decidir. Es lo primero que se lee |
| `rules.md` | Las reglas vigentes, con sus escenarios numerados (`E01`, `E02`…) en forma *dado / cuando / entonces*, incluidos los de error y de borde. Cada regla dice cómo se ve y cómo se llama en la vista simple y en la de teoría |
| `screens.md` | Qué se tiene que poder hacer en cada pantalla, en cada vista, y qué maqueta de `docs/design/mockups/` vale |
| `composer-review.md` | La opinión vigente del compositor sobre el alcance, las maquetas y el módulo programado. No es una regla: lo que Carlos acepta pasa a `rules.md` |

`rules.md` tiene siempre lo vigente: cada cambio lo actualiza en el mismo commit. No hay otro
documento de requerimientos: una regla está en un solo lugar.

### Los nueve pasos de un módulo

**Antes del paso 1, el alcance.** El agente le lista a Carlos todo lo que abarca el módulo, para
que evalúe si se divide. Junto con la lista va la opinión del compositor (abajo) sobre cada
herramienta. Se empieza recién con la respuesta de Carlos.

**El compositor (agente `composer`).** Carlos no sabe música, así que no puede juzgar solo si una
herramienta le sirve a alguien que compone. El compositor mira como músico, con el contexto
limpio, y dice qué aporta, qué estorba, qué limita, qué falta y qué sobra, para quien no sabe
teoría y para quien sabe. Interviene tres veces en cada módulo: sobre el alcance, sobre las
maquetas y sobre el módulo programado. **Propone y no decide:** lo que Carlos acepta entra a las
reglas del módulo; una herramienta nueva que no entra en el módulo va a «Herramientas propuestas»
del [plan](roadmap.md), donde Carlos decide si se hace y cuándo; lo que descarta se anota en el
capítulo con el porqué, para que nadie lo vuelva a proponer. El compositor no escucha: lo que
depende del oído lo deja como una prueba para Carlos, y la opinión de músicos de verdad llega en
la etapa de pruebas reales.

Los hace el mismo agente en la misma sesión, en este orden; el código se escribe recién en el
sexto. Solo las revisiones las hace un subagente con el contexto limpio, porque quien diseñó o
programó no puede revisarse.

| Paso | Rol | Qué hace | Deja | Aprueba Carlos |
|---|---|---|---|---|
| 1 | Analista | Le pregunta a Carlos **todo** lo que haga falta para cubrir la funcionalidad completa: cada caso, cada borde, cada error. Las preguntas van en idioma simple, con un ejemplo que se pueda escuchar cuando la pregunta es sobre cómo suena algo: Carlos no tiene por qué saber teoría para decidir. Toda regla que define Carlos la cuestiona: le ofrece las alternativas mejores que encuentre y las desventajas de aplicarla tal cual. Propone las palabras nuevas del idioma simple, con su equivalente en la teoría. Las preguntas van todas juntas, en tandas, hasta que no quede nada sin respuesta | `rules.md` y `summary.md`, con los escenarios, y las filas nuevas del glosario | Sí |
| 2 | Director de arte (skill `art-director`) | Tres versiones muy distintas de cada pantalla, una por vez y en el orden en que se usan, **funcionando y sonando**, en el visor de maquetas. Primero la vista simple, después la de teoría de la misma pantalla. Carlos elige una antes de pasar a la siguiente. Sin restricciones: puede romper las reglas y el marco para un diseño mejor, diciendo qué rompe | `docs/design/mockups/<pantalla>/`, `screens.md` y, del compositor, que intenta componer algo con cada una de las tres, cuál le sirve más a quien compone y por qué | Sí: las ve, las escucha y da sus comentarios, con la opinión del compositor a la vista |
| 2b | Maquetador (agente `mockup-builder`) | Construye la maqueta final: la variante elegida, lo que Carlos quiera de las otras y sus comentarios, ajustada a las reglas aprobadas. Nunca modifica lo del director | `docs/design/mockups/<pantalla>/final/` | Sí: la evalúa; si pide cambios, vuelve el maquetador |
| 3 | Arquitecto | Qué le agrega el módulo a la canción y a su archivo, sus comandos, sus eventos, cómo suena (qué pasa en el audio), la sección «Seguridad», las **metas de performance** (milisegundos entre el toque y el sonido, uso del procesador mientras suena, bytes que se bajan) y las tareas con sus dependencias; un ADR si hay una decisión técnica | `docs/technical/modules/<module>.md` | — |
| 4 | Revisor del diseño (agente `design-reviewer`) y revisor de teoría musical (agente `music-reviewer`), por separado | El primero busca puntos débiles y mejoras al diseño técnico, contra la constitución. El segundo lo mira como un músico: que cada palabra del idioma simple tenga un equivalente correcto en la teoría, que lo que la vista simple deja hacer suene bien de verdad, y que la vista de teoría no tenga errores que un músico notaría | `docs/technical/modules/<module>-design-review.md` y `<module>-music-review.md` | — |
| 5 | Arquitecto | Corrige el diseño con lo que encontraron los dos revisores y se lo presenta a Carlos | El diseño final | Sí |
| 6 | Desarrollador | Primero las pruebas: una por escenario y las que miden las metas de performance, todas fallando. Después el código que las hace pasar, con cobertura total; `pnpm check` en verde | Pruebas y código | — |
| 7 | Revisor del código (agente `code-reviewer`) y revisor de teoría musical (agente `music-reviewer`), por separado | El primero compara el código con las reglas, las pantallas y el diseño. El segundo comprueba que lo que suena sea lo que dicen las reglas. Lo que encuentran se arregla | `docs/technical/modules/<module>-code-review.md` y la sección del código de `<module>-music-review.md` | — |
| 8 | Compositor (agente `composer`) y Carlos | El compositor usa el módulo programado para componer algo corto, dice si cumple lo que prometía y le deja a Carlos una lista de qué probar y qué escuchar. Carlos lo prueba y lo escucha en el ambiente de pruebas, en la vista simple; los ajustes vuelven al paso que corresponda | La sección del módulo programado de `composer-review.md` | Sí: cierra el módulo |
| 9 | Redactor | El manual del módulo, en idioma simple, con capturas y con ejemplos que se escuchan | `docs/manual/` | — |

La sección «Seguridad» del diseño contesta siempre: qué entra de afuera y cómo se valida
(archivos, enlaces, el micrófono), qué se guarda en el dispositivo y qué licencia tiene cada
sonido que se suma.

### Qué tamaño tiene un pedido

Los cambios a un módulo ya cerrado no pasan por los nueve pasos. Antes de tocar nada se decide el
tamaño y se le dice a Carlos en una línea:

| Tamaño | Cuándo | Qué hace falta antes del código |
|---|---|---|
| Arreglo | El código no cumple lo que la documentación ya dice | Nada más que anotar la tarea |
| Ajuste | Un color, un texto, un sonido que se cambia por otro parecido | El documento actualizado; el pedido vale como aprobación |
| Cambio de regla | Una regla nueva o distinta en un capítulo que existe | Pasos 1 y 3 a 5, solo en lo que cambia |
| Cambio de interfaz | Una pantalla que cambia de un modo que Carlos tiene que ver o escuchar | Paso 2 |
| Funcionalidad nueva | Algo que no existe, que toca más de un capítulo o lleva más de un día | Los nueve pasos |

Ante la duda, vale el más grande.

### Trabajo en paralelo

Varias sesiones pueden trabajar a la vez en módulos distintos:

- **Se toma la tarea antes de empezar:** la sesión cambia el estado del módulo en el
  [plan](roadmap.md) a «En curso: paso N», hace commit y sube, antes de tocar nada más.
- **Solo se toma un módulo libre cuyos módulos previos estén cerrados.**
- **El código común y los documentos del proyecto tienen un dueño por vez:** cambiarlos es una
  tarea propia del plan, que se toma igual que un módulo.
- **En los archivos compartidos cada módulo toca solo lo suyo:** en el glosario, sus filas.
- **Carlos atiende una cosa por vez:** cada sesión le dice en qué módulo y en qué paso está, al
  principio de cada mensaje.

### Antes de subir

`pnpm check` corre los tipos, los límites de tamaño y complejidad, qué puede importar a qué (las
tres capas del principio XII), las pruebas con su cobertura, las dependencias con fallas
conocidas, los secretos, que los enlaces de la documentación funcionen y que ningún texto de la
vista simple use una palabra de la teoría (principio III). No se sube nada que no lo pase. Si
solo cambian archivos `.md`, alcanza con los enlaces y los secretos. Nace con el primer módulo
(tarea T005).

## Cómo se cambia

Se cambia con la aprobación de Carlos, en el mismo commit que explica por qué.
