# Sinfonia

Aplicación web para crear melodías, con una vista simple para quien no sabe teoría musical y una
vista de teoría para quien sabe. **La documentación manda; el código es secundario.**

## Por dónde empezar

1. [docs/project/constitution.md](docs/project/constitution.md): lo que no se negocia, cómo se
   escribe el código y los nueve pasos de un módulo. **Leela antes de tocar nada.**
2. [docs/project/roadmap.md](docs/project/roadmap.md): en qué etapa está el proyecto, qué sigue
   y lo que falta decidir.
3. [docs/project/simple-language.md](docs/project/simple-language.md) y
   [docs/project/glossary.md](docs/project/glossary.md): el idioma simple y cómo se dice cada
   concepto en la vista simple, en la de teoría y en el código. Una palabra que no está, se
   agrega antes de usarla.
4. [docs/chapters/](docs/chapters/README.md): el `summary.md` del capítulo que vas a tocar; el
   `rules.md`, solo en la parte que vas a cambiar.
5. [docs/technical/](docs/technical/adr/README.md): los ADR y el diseño de cada módulo.

## Reglas que no se olvidan

- **Carlos no sabe teoría musical.** Todo lo que se le pregunta o se le muestra va en idioma
  simple, y si la pregunta es sobre cómo suena algo, con un ejemplo que pueda escuchar. Él es la
  vara del idioma simple: si no entiende una palabra sin explicación, la palabra está mal.
- **La vista simple no usa ninguna palabra de la teoría musical.** El código, sí: en inglés y
  con las palabras de la teoría.
- **Idiomas:** el código en inglés, también los nombres de archivos y carpetas de la
  documentación. El contenido de la documentación, los comentarios, los commits y los textos que
  ve la persona, en castellano.
- **Un módulo a la vez, entero,** en los nueve pasos de la constitución. No se programa sin las
  reglas, las pantallas y el diseño técnico aprobados por Carlos.
- **Toda regla que define Carlos se cuestiona:** se le ofrecen las alternativas mejores y las
  desventajas de aplicarla tal cual; decide él.
- **La documentación describe el presente:** sin fechas, sin numerar decisiones y sin historia.
  La historia está en los commits, y cada commit explica el porqué.
- **Antes de empezar un módulo, se le lista a Carlos todo lo que abarca,** para que decida si se
  divide.
- **El analista pregunta todo,** todas las preguntas juntas y en tandas hasta que no quede nada
  sin respuesta.
- **Las pantallas salen del director de arte,** siempre tres versiones, funcionando y sonando.
- **El orden de autoridad:** reglas, maquetas, diseño técnico, pruebas y código. Las pruebas se
  escriben antes que el código y no se cambian para que el código pase.
- **El compositor (agente `composer`) opina antes que Carlos decida** el alcance, las maquetas y
  el cierre de cada módulo: dice si las herramientas le sirven a quien compone y propone
  mejoras y herramientas nuevas. Propone, no decide.
- **Un módulo se cierra cuando Carlos lo escuchó.**
- **Fuera de alcance, decidido:** servidor, cuentas, inteligencia artificial, voz y letra.
- **Todo directo a `main`,** sin ramas ni pull requests. En una sesión en la nube que arranca en
  una rama `claude/…`, se sube igual a `main` (`git push origin HEAD:main`).

## Qué no decide el agente

El alcance, las fechas y las prioridades. Un requerimiento nuevo, o uno que cambia, se le
pregunta a Carlos. Si Carlos no contestó una pregunta, o la respuesta no quedó clara, se le
vuelve a preguntar: nada queda supuesto.
