# platform-shooter for 3DS

**English** | [Español](#español)

> 🗺️ **[Roadmap](ROADMAP.md)**: what's coming next · lo que viene

Native Nintendo 3DS port of **platform-shooter**, a platform game by
**jmgamer1199**, first made with GameMaker in 2017. Written in C for the
3DS, it does not emulate anything. It plays exactly like the PSP version,
uses both screens and the touch screen, and runs at 60 FPS. It is made and
tested on an **Old 3DS XL**, one of the models with the least power, so it
should work on every 3DS and 2DS, and on the Azahar emulator.

> **Bugs and ideas.** If you find a bug or a problem, or you have an idea
> for the game, write it in [Issues](../../issues) > *New issue*, and
> choose **Bug** (the title starts with [bug]), **Idea** ([idea]) or
> **Other** ([other]). The form asks for what is needed, like your 3DS
> model (or emulator) and the version of the game.

> **Alpha version.** The icon, the banner of the HOME Menu and the button
> symbols are provisional. This repository only has the files to play (no
> source code).

> **Homebrew.** platform-shooter is unofficial homebrew: a free game, not
> made, licensed or endorsed by Nintendo. Nintendo 3DS is a trademark of
> Nintendo. On a real 3DS it needs custom firmware (CFW, for example
> Luma3DS).

## Download

Go to [Releases](../../releases) and download
`platform-shooter-3ds-<version>.zip`.

## Install

**Real 3DS or 2DS** (with custom firmware and FBI):

1. Unzip the file. You get two folders: `3ds` and `cias`.
2. Copy both to the root of the SD card (if they are already there, let
   them merge). The game's files end up in `sdmc:/3ds/platform-shooter/`
   and the installer in `sdmc:/cias/platform-shooter.cia`.
3. On the 3DS, open FBI > *SD* > *cias* > `platform-shooter.cia` >
   *Install CIA*. The game appears in the HOME Menu.

To update, do the same with the new version: it installs over the old one
and keeps your options, packs and logs.

**Azahar emulator** (free, Windows, Android, Mac, Linux):
[azahar-emu.org](https://azahar-emu.org/)

copy the `3ds/platform-shooter` folder to `3ds/` on Azahar's SD card (the
`sdmc` folder inside Azahar's user folder) and open
`3ds/platform-shooter/platform-shooter.3dsx` from Azahar. (That .3dsx is for
the emulator; on a real 3DS it also shows up in the Homebrew Launcher.)

## Controls

The buttons are the PSP version's, in the same places: B jumps (the PSP's
✕), A is the PSP's ○, X talks (△) and Y is □. In the menus and in the
conversations, as usual on Nintendo, A accepts and B goes back.

| Button | In the game | In the menus |
|---|---|---|
| D-pad | move | choose (hold to keep moving) |
| B | jump | back |
| A | | accept |
| R | shoot (from level 6, hold for 3 shots per second) | lower a pack's priority |
| L | | raise a pack's priority |
| X | talk to a character (in the packs' levels) | details and warnings of a pack |
| Start | pause | |
| Touch screen | | the menus' buttons and the packs and controls lists |

In a conversation, A goes on or chooses an answer and B ends it.
Jump, shoot, talk and pause can go on other buttons, and the Circle Pad
can move too: OPTIONS > CONTROLS.

## The two screens

- **Menus:** the top screen shows the menu (on the title screen, the
  game's name with its yellow phrase) and the bottom screen its buttons,
  to touch with the stylus or to choose with the buttons. The lists of
  packs and controls are on the bottom screen too: the first touch
  chooses a row, a touch on the chosen one uses it.
- **Pause:** the top screen shows the level, blurred, with "Pause" in the
  middle; the bottom screen, the pause's buttons.
- **Levels:** the game on the top screen (the whole picture of the PSP
  version, a little smaller), and on the bottom screen the FPS, the memory
  and the position of the player, for bug reports.

## What's in it

- The 5 original levels and a new level 6 with enemies that shoot.
- English, Spanish, French, German, Italian, Dutch and Portuguese (more
  languages can be added as text files).
- **Resource packs**: change any picture (PNG) or sound (WAV) of the game,
  add music (OGG), change the levels or add new ones (simple text files),
  several packs at once with priorities. Packs use the same format on
  every port of the game: a pack made for the PSP works on the 3DS, and
  the game tells you what is wrong in a pack.
- In the packs, **levels drawn as a map** with letters (no coordinates),
  **new enemies** built from pieces (how they move, shoot, split, phases
  for bosses...) and separate pictures for the ground, the platforms and
  the walls. The game itself doesn't come with new levels or enemies:
  these are for the packs.
- **Characters (NPCs) and dialogs** in the packs: people and signs to talk
  to, with conversations in each language and answers to choose.
- **Big levels** in the packs, up to 100 squares wide and 60 tall, with a
  camera that follows the player and backgrounds that move slower than
  the level. All the texts of a pack (levels and conversations) in its
  `texts/` folder, in each language.
- **Two sample packs**, off at first: *0.6.0: The temple* (switches, colour
  blocks, keys and doors, 3 levels) and *0.6.0: The fortress* (coins, extra
  lives and health bars, 3 levels). Each one has its own enemies, a
  character to talk to, a material, music and levels. They are **made
  with AI (Claude Opus 5.5), only to show what packs can do**: they are
  not part of the original game. Turn one on in OPTIONS > TEXTURE PACKS
  and press PLAY.
- A pack can say if it is a **mod** (it changes the game: only from the
  main menu) or just a **texture pack** (also from the pause).
- **Rules** in the packs: change the life, the jump, the gravity, the
  speeds and the fire rate to make an easy mode, a moon mode...
- **Options**: the volume of the sounds and the music, the buttons of
  your choice for jumping, shooting, talking and pausing, and moving with
  the Circle Pad. The menus' buttons are one picture that packs can
  change.
- The game starts in the console's language if it has it; language,
  packs and options are remembered.
- A **log** of everything that happens (`data/cache/log.txt`, in the
  game's folder), written on its own: send it with your bug reports.

How to make packs, levels and rules, add languages or change the font:
`MODDING.txt` inside the game folder.

## The original game and what was made with AI (Claude Opus 5.5)

**From the original game**, made by jmgamer1199 in 2017 with GameMaker:
all the 2017 pictures (the player, the enemies, the wheel, the flag, the
walls, the bullets and the backgrounds, including the drawings of the
player shooting, which the original didn't use), the sounds, levels 1 to 5,
and how the game plays: movement, jumps, enemies, collisions and menus.
Since 0.6.0, several of those pictures have been replaced by Nebura Noctis's
pixel art; the backgrounds of levels 2 to 6 and the walls are still the
original ones. The ground and the platforms use, for now, the original wall
picture.

**Pixel art** by [Nebura Noctis](https://deluxe-torte-5e3896.netlify.app/):
since 0.6.0, the game's own look. The player (standing and shooting), the
walking enemy, the wheel, the flag, the bullet, the menu button, the
level 1 background, the black menu background and the grass of the ground.

**Made with Claude (Opus 5.5) for the PSP port**, directed by jmgamer1199,
and used as it is on the 3DS:
- the game rewritten in C from the original GameMaker code, plus its tools
  and tests;
- level 6 and the shooting;
- the texture packs, the levels in files and drawn as maps, the enemies
  of the packs (built from pieces), the characters (NPCs) and dialogs of
  the packs, the rules and the warnings;
- the languages and their texts (menus, tutorials and title screen
  phrases), the debug mode and the 60 FPS drawing;
- the icon of the template pack and the new buttons drawn on the menus
  (the gear and TEXTURE PACKS). The menu backgrounds are the original
  ones, with their painted text removed;
- the sample packs (sample_temple and sample_fortress): their
  levels, characters, enemies, texts, pictures, sounds and music.

**Made with Claude (Opus 5.5) for the 3DS port**, directed by jmgamer1199:
- all the 3DS's own code: the drawing on both screens, the touch screen,
  the buttons, the sound, the files on the SD card, and its tools and
  tests;
- the provisional pictures: the icon and banner of the HOME Menu and the
  3DS button symbols;
- these documents.

**From others**: the Lilita One font (Juan Montoreano, SIL Open Font
License) and the free software in `THIRD_PARTY_LICENSES.txt`.

## License

platform-shooter © 2017-2026 jmgamer1199, licensed under
[CC BY-NC 4.0](https://creativecommons.org/licenses/by-nc/4.0/) (see
`LICENSE`): you can play it, share it and change it (packs, levels,
translations...), as long as you give credit to jmgamer1199 and say what
you changed, and you can't sell it or use it for commercial purposes.

The third party software and the font keep their own licenses:
`THIRD_PARTY_LICENSES.txt` and `font/LICENSE.txt` inside the game folder.

---

## Español

Port nativo para Nintendo 3DS de **platform-shooter**, un juego de
plataformas de **jmgamer1199**, hecho originalmente con GameMaker en 2017.
Está escrito en C para la 3DS y no emula nada. Se juega exactamente igual
que la versión de PSP, usa las dos pantallas y la pantalla táctil, y va a
60 FPS. Está hecho y probado en una **Old 3DS XL**, uno de los modelos con
menos potencia, así que debería funcionar en cualquier 3DS y 2DS, y en el
emulador Azahar.

> **Fallos e ideas.** Si encuentras un fallo o un problema, o tienes una
> idea para el juego, escríbelo en [Issues](../../issues) > *New issue*, y
> elige **Bug** (el título empieza por [bug]), **Idea** ([idea]) u
> **Other** ([other]). El formulario pide lo necesario, como tu modelo de
> 3DS (o emulador) y la versión del juego.

> **Versión alfa.** El icono, el banner del menú HOME y los símbolos de los
> botones son provisionales. Este repositorio solo tiene los archivos para
> jugar (no el código fuente).

> **Homebrew.** platform-shooter es homebrew no oficial: un juego gratuito,
> que no está hecho, licenciado ni respaldado por Nintendo. Nintendo 3DS es
> una marca de Nintendo. En una 3DS real necesita firmware personalizado
> (CFW, por ejemplo Luma3DS).

### Descargar

Entra en [Releases](../../releases) y descarga
`platform-shooter-3ds-<versión>.zip`.

### Instalar

**3DS o 2DS real** (con firmware personalizado y FBI):

1. Descomprime el archivo. Salen dos carpetas: `3ds` y `cias`.
2. Copia las dos carpetas en la raíz de la tarjeta SD (si ya están, deja
   que se fusionen). Los archivos del juego quedan en `sdmc:/3ds/platform-shooter/`
   y el instalador en `sdmc:/cias/platform-shooter.cia`.
3. En la 3DS, abre FBI > *SD* > *cias* > `platform-shooter.cia` >
   *Install CIA*. El juego aparece en el menú HOME.

Para actualizar, haz lo mismo con la versión nueva: se instala encima de
la anterior y conserva tus opciones, paquetes y registros.

**Emulador Azahar** (gratis, Windows, Android, Mac, Linux):
[azahar-emu.org](https://azahar-emu.org/)

copia la carpeta `3ds/platform-shooter` en `3ds/` de la tarjeta SD de
Azahar (la carpeta `sdmc` dentro de la carpeta de usuario de Azahar) y abre
`3ds/platform-shooter/platform-shooter.3dsx` desde Azahar. (Ese .3dsx es para
el emulador; en una 3DS real también sale en el Homebrew Launcher.)

### Controles

Los botones son los de la versión de PSP, en el mismo sitio: B salta (el
✕ de la PSP), A es el ○ de la PSP, X habla (△) e Y es el □. En los menús y
en las conversaciones, como es habitual en Nintendo, A acepta y B vuelve.

| Botón | En el juego | En los menús |
|---|---|---|
| Cruz de control | moverse | elegir (mantén para seguir moviendo) |
| B | saltar | atrás |
| A | | aceptar |
| R | disparar (desde el nivel 6; mantenlo para 3 disparos por segundo) | bajar la prioridad de un paquete |
| L | | subir la prioridad de un paquete |
| X | hablar con un personaje (en los niveles de los paquetes) | detalles y avisos de un paquete |
| Start | pausa | |
| Pantalla táctil | | los botones de los menús y las listas de paquetes y de controles |

En una conversación, A continúa o elige una respuesta y B la termina.
Saltar, disparar, hablar y pausa pueden ir en otros botones, y el botón
deslizante (Circle Pad) también puede mover: OPCIONES > CONTROLES.

### Las dos pantallas

- **Menús:** la pantalla de arriba enseña el menú (en la pantalla de
  inicio, el nombre del juego con su frase amarilla) y la de abajo sus
  botones, para tocarlos con el lápiz táctil o elegirlos con los botones. Las
  listas de paquetes y de controles también están en la pantalla de
  abajo: el primer toque elige una fila y un toque sobre la elegida la
  usa.
- **Pausa:** la pantalla de arriba enseña el nivel, borroso, con "Pausa"
  en medio; la de abajo, los botones de la pausa.
- **Niveles:** el juego en la pantalla de arriba (la imagen entera de la
  versión de PSP, un poco más pequeña) y en la de abajo los FPS, la memoria
  y la posición del jugador, para los avisos de fallos.

### Qué trae

- Los 5 niveles originales y un nivel 6 nuevo con enemigos que disparan.
- Inglés, español, francés, alemán, italiano, neerlandés y portugués (se
  pueden añadir más idiomas con archivos de texto).
- **Paquetes de recursos**: cambia cualquier dibujo (PNG) o sonido (WAV)
  del juego, añade música (OGG), cambia los niveles o añade otros nuevos
  (archivos de texto sencillos), varios paquetes a la vez con prioridades.
  Los paquetes usan el mismo formato en todos los ports del juego: un
  paquete hecho para la PSP funciona en la 3DS, y el juego te dice qué
  tiene mal un paquete.
- En los paquetes, **niveles dibujados como un mapa** con letras (sin
  coordenadas), **enemigos nuevos** montados con piezas (cómo se mueven,
  disparan, se dividen, fases para jefes...) y dibujos distintos para el
  suelo, las plataformas y las paredes. El juego en sí no trae niveles ni
  enemigos nuevos: son para los paquetes.
- **Personajes (NPC) y diálogos** en los paquetes: gente y carteles con los
  que hablar, con conversaciones en cada idioma y respuestas para elegir.
- **Niveles grandes** en los paquetes, de hasta 100 casillas de ancho y 60
  de alto, con una cámara que sigue al jugador y fondos que se mueven más
  despacio que el nivel. Todos los textos de un paquete (niveles y
  conversaciones) en su carpeta `texts/`, en cada idioma.
- **Dos paquetes de ejemplo**, desactivados al principio: *0.6.0: El
  templo* (interruptores, bloques de colores, llaves y puertas, 3 niveles)
  y *0.6.0: La fortaleza* (monedas, vidas extra y barras de vida, 3
  niveles). Cada uno trae sus enemigos, un personaje con el que hablar, un
  material, música y sus propios niveles. Están **hechos con IA (Claude
  Opus 5.5), solo para enseñar lo que pueden hacer los paquetes**: no son
  parte del juego original. Activa uno en OPCIONES > PAQUETES DE TEXTURAS
  y pulsa JUGAR.
- Un paquete puede decir si es un **mod** (cambia el juego: solo desde el
  menú principal) o solo un **paquete de texturas** (también desde la
  pausa).
- **Reglas** en los paquetes: cambia la vida, el salto, la gravedad, las
  velocidades y la cadencia de disparo para hacer un modo fácil, un modo
  luna...
- **Opciones**: el volumen de los sonidos y de la música, los botones que
  quieras para saltar, disparar, hablar y pausar, y moverte con el botón
  deslizante. Los botones de los menús son un solo dibujo que los paquetes
  pueden cambiar.
- El juego empieza en el idioma de la consola si lo tiene; el idioma, los
  paquetes y las opciones se recuerdan.
- Un **registro (log)** de todo lo que pasa (`data/cache/log.txt`, en la
  carpeta del juego), que se escribe solo: mándalo con tus avisos de
  fallos.

Cómo hacer paquetes, niveles y reglas, añadir idiomas o cambiar la fuente:
`MODDING.txt` en la carpeta del juego.

### El juego original y lo que se ha hecho con IA (Claude Opus 5.5)

**Del juego original**, hecho por jmgamer1199 en 2017 con GameMaker: todos
los dibujos de 2017 (el jugador, los enemigos, la rueda, la bandera, las
paredes, las balas y los fondos, también los del jugador disparando, que el
original no usaba), los sonidos, los niveles 1 a 5, y cómo se juega:
movimiento, saltos, enemigos, colisiones y menús. Desde la 0.6.0, varios de
esos dibujos se han sustituido por el pixel art de Nebura Noctis; los
fondos de los niveles 2 a 6 y las paredes siguen siendo los originales. El
suelo y las plataformas usan, de momento, el dibujo de pared original.

**Pixel art** de [Nebura Noctis](https://deluxe-torte-5e3896.netlify.app/):
desde la 0.6.0, el aspecto propio del juego. El jugador (quieto y
disparando), el enemigo que camina, la rueda, la bandera, la bala, el botón
de los menús, el fondo del nivel 1, el fondo negro de los menús y el césped
del suelo.

**Hecho con Claude (Opus 5.5) para el port de PSP**, bajo la dirección de
jmgamer1199, y usado tal cual en la 3DS:
- el juego reescrito en C a partir del código original de GameMaker, y sus
  herramientas y pruebas;
- el nivel 6 y el disparo;
- los paquetes de texturas, los niveles en archivos y dibujados como
  mapa, los enemigos de los paquetes (montados con piezas), los
  personajes (NPC) y diálogos de los paquetes, las reglas y los avisos;
- los idiomas y sus textos (menús, tutoriales y frases de la pantalla de
  inicio), el modo debug y el dibujado a 60 FPS;
- el icono del paquete plantilla y los botones nuevos dibujados en los
  menús (el engranaje y PAQUETES DE TEXTURAS). Los fondos de los menús son
  los originales, con su texto pintado borrado;
- los paquetes de ejemplo (sample_temple y sample_fortress): sus
  niveles, personajes, enemigos, textos, dibujos, sonidos y música.

**Hecho con Claude (Opus 5.5) para el port de 3DS**, bajo la dirección de
jmgamer1199:
- todo el código propio de la 3DS: el dibujado en las dos pantallas, la
  pantalla táctil, los botones, el sonido, los archivos de la tarjeta SD,
  y sus herramientas y pruebas;
- los dibujos provisionales: el icono y el banner del menú HOME y los
  símbolos de los botones de la 3DS;
- estos documentos.

**De otros**: la fuente Lilita One (Juan Montoreano, SIL Open Font
License) y el software libre de `THIRD_PARTY_LICENSES.txt`.

### Licencia

platform-shooter © 2017-2026 jmgamer1199, con licencia
[CC BY-NC 4.0](https://creativecommons.org/licenses/by-nc/4.0/deed.es) (ver
`LICENSE`): puedes jugarlo, compartirlo y cambiarlo (paquetes, niveles,
traducciones...), siempre que digas que es de jmgamer1199 y qué cambiaste,
y no puedes venderlo ni usarlo con fines comerciales.

El software de terceros y la fuente mantienen sus propias licencias:
`THIRD_PARTY_LICENSES.txt` y `font/LICENSE.txt` dentro de la carpeta del
juego.
