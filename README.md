# Owl Ferris Sweep

This is a custom-made minimalist keyboard that I have built that aims to provide the following features:
- Ergonomic keymap that allows the user to not move their hands or stretch to reach positions
- Aggressive pinky stagger, to promote a neutral hand position
- Aggressive (50 degree) tenting angle to put the wrist in a much more neutral position than any commercial keyboard allows (and also much more aggressive than almost all custom keboards I came across during my research)
- Modular build - circuit board, base, key switches, and microcontroller can all be cheaply swapped around and iterated on as necessary without needing to build a brand new keyboard.



Here is the finished product without the base. Full image with both, and with base attached, coming soon. 

<img src="https://user-images.githubusercontent.com/9446419/156084562-7c997dc5-48c9-49e0-af60-a174a4595a0c.jpg" width="300">


## Background
This is a fork of the [Ferris Sweep project](https://github.com/davidphilipbarr/Sweep), which is itself a fork of [Ferris by Pierre Chevalier](https://github.com/pierrechevalier83/ferris) that uses a daughter board like a promicro, elite-c, bit-c, etc. instead of using onboard components.

The main difference I've made here is that I've pulled the Sweep 2.1 version of the board, I've deleted the old silkscreen artwork, and I've added in some owl artwork.

<img src="https://user-images.githubusercontent.com/9446419/143318466-0a3d0682-bb64-4945-b8ab-bbbacb69f23f.png" width="400"> <img src="https://user-images.githubusercontent.com/9446419/143318504-2994da0f-68e2-45f8-aefe-fd5e40d8b8bf.png" width="400">

The QMK keymap and configuration is heavily based on [Ben Vallack's 34 key Ferris Sweep layout](https://github.com/benvallack/34-QMK-Ferris-Sweep), with some light modifications.  My motivation to build this keyboard was heavily inspired by Ben Vallack's [Ferris Sweep](https://www.youtube.com/watch?v=JqpBKuEVinw) build, as well as his videos on various keyboard layouts for 40% keyboards. Build instructions for a similar version of this keyboard can be found [here](https://www.youtube.com/watch?v=fBPu7AyDtkM_).

## Base design
I designed a base that has a tenting angle of 50 degrees. The base is the exact same for each side (the are just mirrored), and is designed to be 3D printed and then attached to the circuit board via 4x M2 heat set inserts inserted into the base and then attached to four M2 screw sized holes on the PCB.

<img src="https://user-images.githubusercontent.com/9446419/153913472-b125c9d9-91c1-4504-bf43-197d8bf727ab.png" width="400">

Here is a study I did where I took a Kinesis Freestyle Pro, propped up to a tenting angle of 50 degrees. You can see the finished product next to the Kinesis, and the advantages of the newly designed keyboard should be clear. When aggressively tenting, a smaller keyboard creates a much smaller desktop footprint than a large keyboard such as the Kinesis.

TODO: INSERT COMPARISON AGAINST TENTED KINESIS KEYBOARD

## Keymap
This keyboard uses the QMK project for the keboard's firmware. I wrote a custom keymap, however there is a default keymap that can be used for any Ferris or Ferris-offshoot keyboards included in the QMK project by default.

The procedure for re-flashing the keyboard with new firmware (which must be done any time the QMK keymap is changed) is to put the keyboard into a reset state and then use the QMK flash command.
1) Connect the keyboard to your PC.
2) Press the reset button (which is mapped to the keyboard's Layer 2 bottom-left most pinkey key) OR simply short the master Arduino's reset and ground pins together as shown in this diagram
<img src="https://user-images.githubusercontent.com/9446419/159301616-7d147aae-19a7-4722-9c3e-0f31a73177a2.png" width="200">
3) In a terminal on the connected PC, run the command `qmk flash`

TODO: QMK keymap incoming

## PCB Build 

### BOM
Each side of the keyboard contains the following:
- 1x Elite-C controller
- 17x Kailh Silver Low Profile Choc Switches 	
- 17x MBK Choc keycaps
- 1x TRRS jack 
- 1x custom 3D printed base
- 4x M2 heat set inserts
- 4x M2 screws

### Assembly Materials
- Adjustable soldering iron
- Solder & flux
- Small screwdriver

Flashed the Elite-C arduino clones with QMK firmware, and then soldered it onto the board. Soldered on the TRRS jack. Then soldered in each individual Choc key switches and snapped on the keycaps. 

Once the base was printed I aligned the circuit board on the 3D printed base, and marked where the four holes are for the M2 screws. Pushed the heat set inserts into the base where the markings were, and then attached the circuit board to the base via the four M2 screws.


