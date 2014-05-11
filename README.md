Building a Phantom keyboard
===========================

Back in the mid-90's, I got myself a Cherry keyboard with MX blues. It
was great. I used it a lot. I never took it in to work, though, and at
the start of this year, after my KVM broke, they replaced my cheap and
flimsy rubber dome with something far, far worse. Something that might
have cost 2 quid to make. I looked at it in horror, and decided
something must be done.

I wanted a mechanical keyboard for work, and something based off my
old Cherry seemed perfect. Why not use the Cherry itself?

 * It didn't do USB. It didn't actually do PS/2, either, having an AT
   plug and an adapater
 * It lacks Windows keys, which are convenient
 * Actually, a couple of keys had started to flake out. That
   definitely needs fixing
 * It didn't have a metal plate, which seemed a shame
 * It wasn't tenkeyless and, well, I never use the number pad and do
   use a mouse on the right, so that's a bit sub-optimal

So, I decided to take the old Cherry, and reuse the switches and
keycaps. This project has taken rather longer than I expected (and
been more expensive!), so I should probably have just bought a nice
new mechanical, rather than wait so long, using the horrible work
keyboard, but it's certainly been a fun project.

As I'd never done any custom keyboard stuff before, I just followed a
very simple variation of the Phantom design.

More details in the sections below, but the basic steps ran something
like this:

1. Got customised plate lasered
2. Soldered the Teensy microcontroller to the Phantom PCB
3. Installed diodes
4. Painted plates
5. Installed switches and stabilisers
6. Soldered up the switches
7. Made case

The instructions at
http://deskthority.net/wiki/Phantom_instruction_guide are very good
and should give you everything you need, but I thought I'd just share
my thoughts and experiences.

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

Installing
----------

It's very important to solder the Teensy in correctly. Solder the
Teensy as low onto the main PCB as you can, since the Teensy sticking
out the back is the limiting factor on the the depth of your keyboard,
which you probably want to make quite thin. At the very least, take
any plastic blocks off the headers. Ideally, solder the thing flat
against the main board.

Once soldered in, you need to really trim the soldered connections as
flat as possible on the switch side, since they control how low you
can put the switches that overlap the Teensy. You want as near as
possible to flat.

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

Got some more plate-mounted Cherry stabilisers. These ones arrived,
and did the business. It took a while to work out the best way to
mount them. They are pushed in from the keycap side, having first
passed the metal bar through the cut-out slot from the cap side to the
soldering side.

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

Taken from my old Cherry keyboard. (They're doubleshot. This is not
something I'd realised at first, so I was somewhat surprised after the
first few years that there was really no sign of wear to the
labels...).

They were quite grubby after all their usage, but they quicky cleaned
up when I scrubbed them with water and washing-up liquid, using an old
toothbrush.

FIXME: Modifiers. Need a 1u Cherry profile Windows key - d'oh,
would have been simpler to replace that row and get a new 6.25u space
bar, with easier-to-source modifiers, than deal with this.

Thoughts on the Phantom design
==============================

The Phantom design tries to be a jack of all trades. It covers ISO and
ANSI, plus a few other custom funky things, with 1u and 1.5 Windows
keys. This does lead to a few ugly things - the wide switch hole for
caps lock, the space bar with multiple stabiliser cut-outs, various
bits on the PCB where the holes are a bit ick, etc.

Overall, it does a pretty good job, but if I were to do this again I'd
probably tidy up the plate a little bit more. I'd not try to redo the
PCB though!

On of the more painful bits is quite how thick the keyboard has to be
because of the Teensy and the way it's mounted. As I'm reasonably
confident with my soldering, /if/ I were to produce my own PCB, I
think I'd directly solder a microcontroller to the board, saving the
depth. If I could find an appropriate easy-to-solder SMT
microcontroller, I guess.
