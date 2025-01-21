<img src="./Pictures/MetaphoricLogo.png">

# Metaphoric - an enhanced Oric clone
Metaphoric is an Oric clone with the memory subsystem based on the OriClone-1 project and some additional features:
* Composite video output (RCA socket)
* TRRS audio-video socket for connecting "jack to 3xRCA" cable
* Footprints for both original AY-3-8912 chips and for (much cheaper) AY-3-8910 chips (or other 40-pin clones)
* Ability to use 7905 or 7805 power regulator and also to power the Metaphoric using an external +5V power supply
* Two joystick ports on the keyboard PCB — one is an IJK „Stingy” port, the other is a cursors+space joystick for games that do not support IJK but are controlled with cursors or make it possible to redefine the keys.
* Easily accessible RESET and NMI buttons on top of the keyboard.
* Easily accessible switches for changing the ROM between Oric-1 and Oric Atmos and for disabling the IJK interface (it may interfere with the operation of printer port and it can also corrupt sound in games that do not support IJK, e.g. Manic Miner)
* Automatic hardware V-sync hack - original Orics did not have any way of checking the vertical sync signal, which made it difficult to write games without flickering sprites, so somebody came up with the idea of connecting video sync signal to tape in using an external cable and synchronizing games/demos in that way. Metaphoric has a transistor that connects sync out to tape in when the tape relay is inactive and disconnects it when the relay is active (to allow loading from tape).

<img src="./Pictures/20250114_101616.jpg" width="512">
<img src="./Pictures/20250114_101747.jpg" width="512">
<img src="./Pictures/20250114_221728.jpg" width="512">
<img src="./Pictures/20250117_132145.jpg" width="512">

# Building the Metaphoric
Note: The main PCB fits in the original Oric-1/Atmos case (the keyboard PCB <i>does not</i>!). If you would like to use the main PCB with the original keyboard and case, do not install J10 (TRRS socket) and J7 (auxiliary connector that supports the additional switches on the keyboard).

Most of the build is pretty self-explanatory, as all the components are described on the PCB. The things to watch for, in no particular order, are as follows:
1. You can omit all the parts in the 'COMPOSITE VIDEO SECTION' if you're only planning to use the RGB output. The file 'RGB_Scart_Tape.pdf' shows how to build a SCART cable, and this is definitely the recommended way of using an Oric, original or cloned.
2. Next to the composite RCA socket there is a header J11. You can put jumper on pins 2-3 to use the nearby TRRS socket as an audio/video video out; there are ready-made 3,5mm jack-3 x RCA cables which you can use to output video and sound. Or you can put a jumper on pins 1-2 to use the TRRS socket as a regular 3,5mm stereo sound out, useful for connecting the Oric to a stereo system or an external speaker. 
3. You can omit all the parts in the "AMPLIFIER SECTION" if you're not going to use the internal speaker. Again, highly recommended to skip these components, they were only added for the sake of completeness, the sound quality is pretty terrible with the internal speaker and sometimes there is no way to turn it off or to control volume.
