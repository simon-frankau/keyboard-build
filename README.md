Building a Phantom keyboard
===========================

FIXME: Background and motivation

More details in the sections below.

1. Got customised plate lasered
2. Soldered the Teensy microcontroller to the Phantom PCB
3. Installed diodes
4. Painted plates

Plates
======

Edited original file (sourced from FIXME) in Inkscape. On importing,
scaled up by 25.4 to get appropriate inch sizes. All I did was remove
the plate holes for keys I'm not using (since I'm not adding a
cosmetic top layer), and add a larger surround with screw holes (since
I'm not using the standard cases). Result is "tkl-rim.dxf".

After a few quotes, and recommendations on the web, the plates were
then laser cut by Yorkshire Profiles. This plate was cut with a couple
of others to get the price down a bit. Would still be a lot better in
a big group buy. The finishing was pretty raw (as expected).

My original plan was to leave it raw, but then I decided to go for a
painted surface. Rubbed with fine grades of steel wool, then sprayed
with etching primer and plain white spray paint.

Used Autotek AT000EP500 500ml Etch Primer and Hammerite Smooth White
Metal Paint. Important things I learnt were:

 * If steel wooling with the keyboard on cardboard and a dust sheet,
   don't just clean the bits off the keyboard and get on with
   spraying. The spray can will blow the bits everywhere. Clear off
   the surface too, duh!
 * Make sure you wear a mask if you don't want funny-coloured snot
   (previously learnt sandpapering a painted surface).

The surface coating wasn't absolutely perfect, but it's good enough,
and the bits without the tiny blemishes do look kinda awesome.

PCB
===

Bought from MechanicalKeyboards website.

Microcontroller
===============

Bought in a group buy from Deskthority.

Downloading
-----------

Got the teensy software from
http://www.pjrc.com/teensy/loader_mac.html

Firmware
--------

https://github.com/tmk/tmk_keyboard looks awesome, but needs the tools
to build

Ended up using phantom_ansi_iso.hex from
https://github.com/BathroomEpiphanies/AVR-Keyboard

Testing
-------

Flashed it, and it came up as a keyboard. Once the Teensy was soldered
to the main board, bridging the appropriate pads produced the expected
keystroke. Hurrah!

Diodes etc.
===========

Bought in bulk off ebay. Soldered on, and then the keys tested.

Also installed a couple of 5mm LEDs with 220 ohm resistors for the
locks.

Stabilisers
===========

Bought some plate-mounted Cherry stabilisers. Royal Mail lost them.

Tried sawing off PCB-mounted stabilisers (like you can saw pins off
the PCB-mounted keyswitches to create ones suitable for
plate-mounting). Put them in the board. Looked about right, but when I
stuck a keycap on the alignment was clearly wrong as the keys stuck.

Keys
====

Vintage MX blues taken from my old Cherry keyboard (bought in
1995). Opened them all up, took them apart got the accumulated fluff
out with a loupe, a pointy stick and Rodico.

Afterwards, tested them all for correct switching and correct feel -
the keyboard had had about a decade of constant use, so some of the
switches didn't feel as nice as the others. Since this is a TKL build,
and the original keyboard was full-size, I could take a few out of
circulation.

Keycaps
=======

Taken from my old Cherry keyboard.

FIXME: Need a clean. Need a 1u Cherry profile Windows key - d'oh,
would have been simpler to replace that row and get a new 6.25u space
bar, with easier-to-source modifiers, than deal with this.
