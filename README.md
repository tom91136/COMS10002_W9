# COMS10002_W9
SDL setup and compile instructions for OSX(macOS)

##Install

Download the latest **development libraries** [here](https://www.libsdl.org/release/SDL2-2.0.5.dmg)

Mount the `.dmg` file and copy `SDL2.framework` to `/Library/Frameworks` if your have sufficient previlidges.
If OSX stops you for permission or security reasons, try copying `SDL2.framework` to `<home>/Library/Frameworks`
instead. Your home directory can be found by typing `cd ~`.

##Compile

Modify references for SDL2 to `-I/Library/Frameworks/SDL2.framework/Headers` and add the flag `-framework SDL2`.

For example, given:

    gcc -std=c99 -Wall -O3 -pedantic sketch.c display.c -lSDL2 -o sketch

You should change it like so:

    gcc -std=c99 -Wall -O3 -pedantic sketch.c display.c -I/Library/Frameworks/SDL2.framework/Headers -framework SDL2 -o sketch

