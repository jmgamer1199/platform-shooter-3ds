# Changelog / Cambios

The 3DS version is the same game as the PSP version. Its versions start at
0.6.2-alpha; what came before is in the PSP version's changelog.

La versión de 3DS es el mismo juego que la de PSP. Sus versiones empiezan
en la 0.6.2-alpha; lo de antes está en los cambios de la versión de PSP.

## 0.6.2-alpha

**English**

The first 3DS version:

- The whole game of the PSP version 0.6.2, written in C for the 3DS
  without emulating anything, and playing exactly the same: the same
  levels, jumps, enemies and packs. A pack made for the PSP works on the
  3DS.
- Made and tested on an Old 3DS XL, at 60 FPS, also in the big levels of
  the packs. It installs in the HOME Menu (.cia) and also plays on the
  Azahar emulator.
- The buttons are the PSP version's, in the same places (B jumps, X
  talks, R shoots). In the menus and in the conversations, A accepts and
  B goes back. The texts show the 3DS's buttons; the controls list shows
  the buttons used in the levels (jump: B). A pack's own pictures of the
  PSP's buttons are not used on the 3DS.
- Both screens: in the menus, the top screen shows the menu (on the title
  screen, the game's name with its yellow phrase) and the bottom screen
  its buttons, which can be touched with the stylus. The packs and
  controls lists can be touched too. The pause shows the level blurred on
  the top screen and its buttons on the bottom one.
- In the levels, the bottom screen shows the FPS, the memory and the
  position of the player, for bug reports.
- The log (`data/cache/log.txt`) also writes down every touch and the
  calls to the SD card that take a long time.

What 0.6.2 brings to the game (also on the PSP):

- The title screen shows the game's name. A pack can change it
  (`GAME_TITLE` in its texts).
- The packs screen remembers the packs it has already checked (in
  `data/cache/`): a pack is only checked again when one of its files
  changes, or with a new version of the game. The screen shows the last
  results straight away while it looks for changes, and "Checking..."
  only appears on a pack that changed.
- The checks of the packs only use the time left over in each frame, so
  the packs screen doesn't go in jerks.
- The music of a pack gets ready in the time the game leaves free, so the
  game doesn't stop when it starts.
- The log says how long each music track took to start.

**Español**

La primera versión para 3DS:

- Todo el juego de la versión 0.6.2 de PSP, escrito en C para la 3DS sin
  emular nada, y que se juega exactamente igual: los mismos niveles,
  saltos, enemigos y paquetes. Un paquete hecho para la PSP funciona en
  la 3DS.
- Hecha y probada en una Old 3DS XL, a 60 FPS, también en los niveles
  grandes de los paquetes. Se instala en el menú HOME (.cia) y también se
  juega en el emulador Azahar.
- Los botones son los de la versión de PSP, en el mismo sitio (B salta, X
  habla, R dispara). En los menús y en las conversaciones, A acepta y B
  vuelve, como es habitual en Nintendo. Los textos enseñan los botones de
  la 3DS; la lista de controles enseña los botones de los niveles (saltar:
  B). La 3DS no usa los dibujos de los botones de la PSP que traiga un
  paquete.
- Las dos pantallas: en los menús, la de arriba enseña el menú (en la
  pantalla de inicio, el nombre del juego con su frase amarilla) y la de
  abajo sus botones, que se pueden tocar con el lápiz. Las listas de
  paquetes y de controles también se pueden tocar. La pausa enseña el
  nivel borroso en la pantalla de arriba y sus botones en la de abajo.
- En los niveles, la pantalla de abajo enseña los FPS, la memoria y la
  posición del jugador, para los avisos de fallos.
- El registro (`data/cache/log.txt`) también apunta cada toque y las
  llamadas a la tarjeta SD que tardan mucho.

Lo que la 0.6.2 trae al juego (también en la PSP):

- La pantalla de inicio enseña el nombre del juego. Un paquete puede
  cambiarlo (`GAME_TITLE` en sus textos).
- La pantalla de paquetes recuerda los paquetes que ya ha comprobado (en
  `data/cache/`): un paquete solo se vuelve a comprobar cuando cambia
  alguno de sus archivos, o con una versión nueva del juego. La pantalla
  muestra enseguida los últimos resultados mientras busca cambios, y
  "Comprobando..." solo aparece en un paquete que ha cambiado.
- La comprobación de los paquetes solo usa el tiempo que sobra en cada
  fotograma, así que la pantalla de paquetes no va a tirones.
- La música de un paquete se prepara en el tiempo que el juego deja
  libre, así que el juego no se para cuando empieza.
- El registro dice cuánto tardó en empezar cada música.
