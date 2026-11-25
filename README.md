# Super Star Trek Classic

A C port of the classic Super Star Trek game, (c) 1996 Chris Nystrom.

It is ported from the BASIC program in *BASIC Computer Games*, edited by David Ahl (Creative Computing / Workman Publishing, 1978).

The project page is at https://nystrom.family/chris/startrek/. An earlier
page is at https://nystrom.family/chris/old/startrek.html.

## Build

The code is 1990s K&R-era C. Modern compilers need C89 mode:

```sh
gcc -std=c89 -o startrek startrek.c -lm
./startrek
```

Tested with gcc 14.2 on Linux.

## License

Free to redistribute and modify in any way you wish; see the header in `startrek.c`. *Star Trek* is a trademark of Paramount.
