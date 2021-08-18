# Painless Prototyping BYO PCB Kit

## Intro

If you're reading this, you probably picked up a BYO Keyboard kit from MakerspaceCT. These boards were designed by [Painless Prototyping](https://painlessprototyping.com/) to use Adafruit's Itsy Bitsy M0 Express. In order to keep costs down, we've packaged the boards with Pro Micro microcontrollers powered by the Atmega32u4. The functionality is the same, but it requires aligning the pins correctly.

## Kit Contents
The kit includes the following:
* PCB
* Pro Micro clone
* Gateron PCB-mount Switches (Red) (6x)
* Diodes (THT) (6x)
* MicroUSB Cable (not included)

## Assembly
Assembling this board will take someone with solid soldering skills 5-10 minutes, and will take a beginner an estimated 15-30 minutes. We've provided some notes below that we recommend you read carefully.

### Diodes

Diodes are polarized, meaning they only work if installed in the correct orientation. Each diode has a black ring around one end. That right should be aligned with the thicker end of the foodprint silkscreened ontot he PCB.

### Switches

Line up the pins with the holes, make sure they're pushed all the way in, and solder.

### Pro Micro

The Itsy Bitsy shipped with the kit has two more pins on each side, so placement of the Pro Micro is important. Ensure you leave the two pins at the bottom of each side unused (as pictured).

![pro micro placement](img/promicro_placement.jpg?raw=true "Pro Micro Placement")


### Case

You'll probably want some sort of case so the solder joints on the bottom of the board don't scratch up your desk. This is left as an exercise for the reader, but check out [painlessprototyping/byo_keyboard_cases](https://github.com/painlessprototyping/byo_keyboard_cases) for files to start with.

### Flash and Test

The easiest way to flash this board will be to flash one of the `.hex` files in this repository onto your keypad with [QMK Toolbox](https://github.com/qmk/qmk_toolbox). To put the board into DFU-mode (Device Firmware Upadate), use a jumper wire (or a paper clip) to short the ground `GND` and reset `RST` pins together briefly. Immediately, press the `Flash` button in QMK toolbox and wait as the flash completes. Of the two `.hex` files included, one sets the buttons to the numbers 1, 2, 3, 4, 5, and 6, and the other sets the buttons to F13, F14, F15, F16, F18, and F18.

Want to set your own layout? The structure you'll need to get custom QMK firmware working is [here](https://github.com/spanpeak51/6keyj)

# Thanks

Special thanks to [spanpeak51](github.com/spanpeak51) for his help in test assembly and QMK development at MakerspaceCT.

To all you who read these notes: greetings, good luck, and happy making! May this lead you down one rabbit hole or another. Have fun!
