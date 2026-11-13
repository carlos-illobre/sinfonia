# Glosario

Cada concepto, en sus tres idiomas: cómo se dice en la vista simple, cómo se dice en la vista de
teoría y cómo se nombra en el código. Cada concepto tiene una sola fila; una palabra nueva se
agrega acá antes de usarla (constitución, principios III y X).

En el código se escriben en `camelCase` (variables, funciones) o `PascalCase` (tipos).

**Estado:** propuesta, junto con el [idioma simple](simple-language.md).

## La altura

| Vista simple | Vista de teoría | Qué es | En el código |
|---|---|---|---|
| Escalón | Grado (de la escala) | La altura de un sonido dentro del clima, del 1 al 7 | `degree` |
| Piso | Octava | Los siete escalones, repetidos más agudos o más graves | `octave` |
| Casa | Tónica | El escalón 1, donde la melodía descansa | `tonic` |
| Clima | Modo (o escala) | Cuáles son los siete escalones; le da el carácter a la canción | `mode` |
| Correr (la canción) | Transportar; tonalidad | Toda la canción más aguda o más grave, sin cambiar su dibujo | `transpose`, `key` |
| Detalle fino | (no tiene: es lo que la vista simple no sabe decir) | Lo hecho en la vista de teoría que no entra en el idioma simple | `fineDetail` |
| — | Nota (do, re, mi…) | Un sonido con su altura absoluta | `pitch` |
| — | Alteración (sostenido, bemol) | Un sonido entre dos escalones | `accidental` |

### Los climas

| Vista simple | Vista de teoría | En el código |
|---|---|---|
| Alegre | Mayor (jónico) | `major` |
| Triste | Menor natural (eólico) | `minor` |
| Misterioso | Dórico | `dorian` |
| Aventura | Mixolidio | `mixolydian` |
| Soñador | Lidio | `lydian` |
| Oscuro | Frigio | `phrygian` |

## El tiempo

| Vista simple | Vista de teoría | Qué es | En el código |
|---|---|---|---|
| Pulso | Tiempo | El latido de la canción | `beat` |
| Velocidad | Tempo (pulsos por minuto) | Cuántos pulsos entran en un minuto | `tempo` |
| Casillero | Subdivisión (semicorchea, de arranque) | La parte más chica de la grilla | `step` |
| Vuelta | Compás | El grupo de pulsos que se repite | `bar` |
| Pulsos por vuelta | Cifra de compás | Cuántos pulsos tiene cada vuelta | `timeSignature` |
| Bloque | Nota (en la partitura) | Un sonido puesto en la grilla | `note` |
| Largo | Duración (figura) | Cuántos casilleros dura un bloque | `duration` |
| Hueco | Silencio | Un lugar donde no suena nada | `rest` |
| Fuerza | Dinámica (intensidad) | Qué tan fuerte suena un bloque | `velocity` |
| Balanceo | Swing | Los casilleros pares llegan un poco tarde | `swing` |

## Lo que acompaña

| Vista simple | Vista de teoría | Qué es | En el código |
|---|---|---|---|
| Fondo | Acorde (por su grado: I, ii, iii, IV, V, vi) | Lo que suena debajo de la melodía | `chord` |
| Camino | Progresión | Una seguidilla de fondos | `progression` |
| Apoya | Nota del acorde | Un bloque que está en un escalón del fondo | `chordTone` |
| Tira | Nota extraña al acorde (de paso, tensión) | Un bloque que no está en un escalón del fondo | `nonChordTone` |
| Manera de tocar (el fondo) | Patrón de acompañamiento (bloque, arpegio, rasgueo) | Cómo se tocan los sonidos de un fondo | `accompanimentPattern` |

## La canción

| Vista simple | Vista de teoría | Qué es | En el código |
|---|---|---|---|
| Canción | Canción | Todo lo que se guarda junto | `song` |
| Capa | Pista | Un instrumento con lo que toca | `track` |
| Papel | (rol de la pista) | Para qué está la capa: melodía, fondo, bajo o ritmo | `role` |
| Instrumento | Instrumento | Con qué sonido toca una capa | `instrument` |
| Golpe | Golpe de percusión | Un sonido de la capa de ritmo | `drumHit` |
| Golpe grave | Bombo | | `kick` |
| Golpe seco | Redoblante | | `snare` |
| Brillo (golpe) | Platillo (hi-hat) | | `hiHat` |
| Ritmo listo | Patrón de batería | Una grilla de golpes ya armada | `drumPattern` |
| Parte | Sección | Un tramo de la canción que se puede repetir y mover | `section` |

## Los efectos

| Vista simple | Vista de teoría | En el código |
|---|---|---|
| Espacio | Reverberación | `reverb` |
| Eco | Delay | `delay` |
| Brillo | Filtro (y ecualización) | `filter` |
| Grosor | Chorus | `chorus` |
| Aspereza | Distorsión | `distortion` |
| Vaivén | Trémolo y vibrato | `tremolo`, `vibrato` |
| Lado | Paneo | `pan` |
| Volumen | Volumen (ganancia) | `gain` |

## La aplicación

| Castellano | Qué es | En el código |
|---|---|---|
| Vista simple | La manera de ver la canción en idioma simple | `simpleView` |
| Vista de teoría | La manera de ver la canción con las palabras de la teoría musical | `theoryView` |
| Puente | Mostrar, a pedido, cómo se llama en la teoría algo de la vista simple | `bridge` |
| Grilla | Donde se ponen los bloques: escalones hacia arriba, tiempo hacia la derecha | `grid` |
