# Super Star Trek Classic

Version 1.2

A C port of the classic Super Star Trek game, (c) 1996 Chris Nystrom.

It is ported from the BASIC program in *BASIC Computer Games*, edited by David Ahl (Creative Computing / Workman Publishing, 1978).

The project page is at https://nystrom.family/chris/startrek/. An earlier
page is at https://nystrom.family/chris/old/startrek.html.
All of Chris's code: https://nystrom.family/chris/code/

## Build

```sh
gcc -o startrek startrek.c -lm
./startrek
```

Version 1.2 builds with gcc and clang in their default modes as well as
`-std=c89`. Tested with gcc 14.2 and clang 19 on Linux.

A Windows .exe can be built with MinGW-w64:

```sh
x86_64-w64-mingw32-gcc startrek.c -o startrek.exe -lm
```

## Changes in 1.2

- Input is read safely. Very long lines no longer overflow a buffer, and
  the game exits cleanly at end of input instead of looping forever.
- Typing "nan" (or anything else that is not a number) as a course no
  longer crashes the game or is taken as a valid course. Courses must be
  1 to 9, as in the original BASIC.
- After moving, the ship sits on a whole sector again, so torpedoes fly
  along the row or column shown on the scan.
- Starting a new game after "aye" resets the Klingon and starbase counts,
  so the new game can be won.
- Starbases offer repairs whenever you are docked, not only when Damage
  Control is broken.
- Repairs during travel, Klingon hit damage to devices, distance in hit
  calculations, and starbase repair time now follow the original BASIC.
- Bouncing off the edge of the galaxy no longer resets the current
  quadrant's Klingons.
- Shields can be set to all available energy.
- Smaller fixes: safe printing of text, the instructions file is closed
  after reading, and the code compiles with modern C compilers.

## Version 1.1

The original 1996 code (version 1.1) is preserved in the git history at
tag `v1.1`:

```sh
git checkout v1.1
```

## License

Free to redistribute and modify in any way you wish; see the header in `startrek.c`. *Star Trek* is a trademark of Paramount.

See `LICENSE`.
