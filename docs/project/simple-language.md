# El idioma simple

La manera de hacer música de la vista simple: qué ve, qué toca y qué palabras lee quien no sabe
teoría musical. Las reglas de cada parte están en su capítulo; acá está la idea completa y por
qué es así. Cada palabra, con su equivalente en la teoría, está en el [glosario](glossary.md).

**Estado:** propuesta. Vale cuando Carlos la pruebe y la apruebe (tareas T002 y T003 del
[plan](roadmap.md)).

## La idea

La teoría musical no se puede sacar: es lo que hace que algo suene bien. Lo que sí se puede es
**no pedirle a la persona que la sepa**. La teoría es difícil por tres razones, y el idioma
simple ataca las tres:

| Por qué cuesta la teoría | Qué hace el idioma simple |
|---|---|
| **Hay que elegir entre demasiado.** De los 12 sonidos posibles, en una canción se usan 7, y cuáles 7 depende de reglas | La aplicación elige esos 7 por la persona. Solo se ve lo que combina: no hay tecla equivocada |
| **Los nombres no dicen nada.** «Fa sostenido», «corchea», «subdominante» hay que memorizarlos | Cada cosa se llama por lo que se percibe: más alto o más bajo, más largo o más corto, descansa o tira |
| **Se escribe en un código.** El pentagrama hay que aprender a leerlo | Se dibuja: la altura es arriba y abajo, el tiempo es izquierda y derecha, el largo es el ancho |

La persona decide lo que ya sabe decidir sin estudiar (si sube o baja, si es alegre o triste, si
va rápido o lento, si algo le gusta) y la aplicación resuelve lo demás.

## Las siete piezas

### 1. La escalera: la altura

Los sonidos disponibles son los **escalones** de una escalera. Hay siete, numerados del 1 al 7,
cada uno con su color y su forma. Después del 7 viene otra vez el 1, un **piso** más arriba: el
mismo sonido, más agudo.

El escalón 1 es la **casa**: donde la melodía descansa. Una melodía que termina en casa suena
terminada; una que termina en otro escalón queda en el aire. Es la única «regla» que hace falta
conocer, y se aprende escuchando.

No hay sonidos entre escalones: por eso nada desafina.

### 2. El clima: el carácter

El **clima** decide cuáles son los siete escalones, y con eso, a qué suena todo: alegre, triste,
misterioso, de aventura, soñador. Se elige con una palabra y se escucha en el momento.

Cambiar el clima no borra nada: la melodía conserva su dibujo (los mismos escalones) y cambia
de carácter. La misma melodía, alegre o triste, con un toque.

Aparte del clima, toda la canción se puede **correr** más aguda o más grave, para que quede
cómoda para cantarla.

### 3. La grilla: el tiempo

El tiempo es una grilla que se lee de izquierda a derecha.

- El **pulso** es el latido de la canción, el que se marca con el pie.
- La **velocidad** es cuántos pulsos entran en un minuto.
- Cada pulso se parte en **casilleros** (cuatro, de arranque).
- Los pulsos se agrupan en **vueltas** (de cuatro pulsos, de arranque): el ciclo que se repite.

Un sonido es un bloque en la grilla: en qué fila está es su escalón, dónde empieza es cuándo
suena y su ancho es su **largo**. Donde no hay bloque hay un **hueco**. Cada bloque tiene su
**fuerza**: más fuerte o más suave.

### 4. El fondo: lo que acompaña

Debajo de la melodía suena un **fondo**, que cambia de vuelta en vuelta (o cada medio). En cada
lugar se elige uno entre seis, y cada fondo tiene el número y el color del escalón sobre el que
está armado: el fondo 1 es la casa.

Una seguidilla de fondos es un **camino**. Hay caminos listos, con nombre, que son los que usan
miles de canciones; se elige uno y ya suena a canción.

La grilla pinta cada vuelta con el color de su fondo, y con eso se ve algo que en la teoría lleva
años escuchar: un bloque de la melodía que está en un escalón del fondo **apoya** (suena firme);
uno que no, **tira** (pide moverse). Ninguno de los dos está mal: la gracia de una melodía es
tirar y volver a apoyar.

### 5. Las capas y los papeles: quién toca qué

Una canción tiene **capas**, y cada capa tiene un instrumento y un **papel**:

| Papel | Qué hace |
|---|---|
| Melodía | Lo que se canta |
| Fondo | Toca los fondos del camino, con una manera de tocarlos que se elige (todo junto, de a uno, rasgueado) |
| Bajo | Lo más grave; de arranque sigue solo al fondo |
| Ritmo | Los **golpes**: grave, seco y brillo, en su propia grilla, con ritmos listos |

Con solo elegir un camino y un ritmo listos, el fondo, el bajo y el ritmo ya suenan, y la
persona se dedica a la melodía.

### 6. Las partes: la forma

La canción se arma con **partes** (inicio, estrofa, estribillo, puente, final) que se ordenan y
se repiten como bloques.

### 7. Los efectos: cómo suena

Cada efecto se llama por lo que se escucha y tiene una sola perilla, de «nada» a «mucho»:

| Efecto | Qué se escucha |
|---|---|
| Espacio | El sonido en un cuarto, en una sala o en una catedral |
| Eco | El sonido se repite, cada vez más lejos |
| Brillo | Más opaco o más brillante |
| Grosor | Suena como varios a la vez |
| Aspereza | Sucio, rasgado |
| Vaivén | El sonido tiembla o se mece |
| Lado | Más a la izquierda o más a la derecha |

## Cómo entra una melodía

Tocar la grilla es la manera de base. Hay otras dos que no piden saber nada, y cada una es un
módulo del plan:

- **Dibujar:** se traza una línea con el dedo, como un cerro, y la aplicación la convierte en
  bloques sobre los escalones y los casilleros.
- **Tararear:** se canta o se silba al micrófono, y la aplicación lo anota en la grilla, corregido
  al escalón más cercano.

## Qué se pierde, y cómo se resuelve

- **Los sonidos fuera del clima.** Hay música que usa sonidos entre escalones. La vista simple no
  los ofrece; la de teoría, sí. Si una canción los tiene, la vista simple los muestra como
  «detalle fino»: suenan igual y no se rompen.
- **Ritmos fuera de la grilla** (tres sonidos donde entran dos, por ejemplo) y **cambiar de clima
  a mitad de la canción:** solo en la vista de teoría, y la simple los muestra igual, como
  detalle fino.
- **El pentagrama:** no existe en la vista simple. En la de teoría es un módulo del final del
  plan.
- **Las palabras son una apuesta.** «Clima», «fondo», «tira» pueden no decirle nada a quien las
  lee por primera vez. Por eso la vara es Carlos (constitución, principio X) y por eso el idioma
  se prueba con una maqueta que suena antes de escribir ningún capítulo (T002).

## Qué no es

- **No es un generador de canciones.** No hay inteligencia artificial ni nada que componga: la
  persona pone cada sonido, y la aplicación le saca del medio lo que no combina.
- **No es una teoría paralela.** Cada palabra tiene su equivalente exacto, y quien aprende acá
  puede pasar a la vista de teoría y encontrarse con lo mismo, con otro nombre.

## De dónde sale

Ninguna pieza es un invento: la escalera numerada es como se enseña música a los chicos y como
anotan los músicos de sesión; los colores por altura vienen de los métodos para quien no lee
partituras; la grilla es la de cualquier programa de música; los caminos listos son las
progresiones más usadas de la música popular. Lo propio de Sinfonia es juntarlas en un solo
idioma, sin una sola palabra de teoría, y con la vista de teoría al lado para la misma canción.
