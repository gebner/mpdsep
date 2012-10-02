mpd sound effect player
=======================

`mpdsep` reads a file called `effects.txt` from the current directory and
allows the user to play a sound file with a single keystroke.

Format of effects.txt
---------------------

Each line in `effects.txt` describes a single sound effect.  For example:

    w "Hilarious laughing" laughtrack o

`w` is the keystroke that will trigger the effect, "Hilarious laughing" is
shown in the on-screen legend, `laughtrack` is the search term used to find the
sound track, and `o` means that the track will be played once (for repeating on
a loop use `r`).  `mpdsep` uses the first result of `mpc search any $query`, a
filename is also fine.

As shown in the example, spaces can be escaped using double quotes.

Usage
-----

If you start `mpdsep` with the example `effects.txt`, you will see the following:

    $ ./mpdsep 
    (w) Hilarious laughing    

Press the indicated key to play a sound effect.  Pressing space will stop the
effect immediately.
