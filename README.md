# VanguardMacropad
A nine key macropad, featuring an ISO enter key. This supports both MX and Alps switches (or clones of either), and runs QMK. The included firmware is for an Amtel ATmega32U4 based ProMicro, and while you could get it to work with any controler board with the same pins, you may need to rewrite the firmware yourself. USB C-C cables don't work. I don't know why either, beyond that it is a limitation of the ProMicro used. Assembly assumes that you have some experience soldering (nothing difficult though, I was able to do it in about 20 minutes) and some basic knowledge about mechanical keyboards (nothing you can't easily find on YouTube)

# Shopping List
- 1x ProMicro controller (or equivalent)- https://mechboards.co.uk/collections/controllers/products/pro-micro-5v
- 9x 1N4148 diodes- https://mechboards.co.uk/collections/diodes/products/throughhole-diodes
- 9x MX or Alps switches (or their clones)- https://www.serpentkeys.co.uk/collections/switches
- 1x 2U PCB mount stabiliser- https://keebcats.co.uk/products/durock-screw-in-stabilisers-v2-2u
- A set of compatible keycaps (you may want to use blank keycaps, relegendables, or something like GMK Dots that allows you to have keycaps that somewhat represent the macros you use)

# Assembly
- Order the PCBs from JLCPCB (or any other PCB manufacturer) using the production file
- Solder the pins for the ProMicro in first, then the THT Diodes, then the ProMicro, then the switches. Install the stabiliser for the ISO enter key. Install the keycaps.
- Connect the macropad to a computer that has QMK toolbox installed (download here: https://github.com/qmk/qmk_toolbox/releases).
- While Bridging the exposed pads on the back of the macropad (behind the ProMicro), flash the .hex file in the firmware folder to the Macropad. Note that this firmware is sort of just random bits of a numpad by default, you will probably want to change it yourself. This is easier said than done, when I tried to flash the firmware on it took about 10 tries and some witchcraft to get my laptop to realise that the macropad was in COM10 not COM11 but it worked in the end, so I had a moderately useless half numpad until I had set up the firmware I actually wanted.
