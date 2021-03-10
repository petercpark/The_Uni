# How to Build Your Own Uni
## Step 1: Buy a PCB
Go to [StenoKeyboard.com](https://www.stenokeyboards.com/) and buy yourself a PCB. Cool. You are done with this step.

## Step 2: Buy the other parts
You need to buy these components:
* Pro Micro (or Pro Micro compatible Elite C)
* 28 PCB Mount* Switches (Mx, Alps, or Choc; they all work!)
* 28 [Keycaps](https://www.stenokeyboards.com/) (You can also buy keycaps from other vendors)
* 5 Rubber Feet
* Solder and Soldering Iron
* USB Cable to connect your Uni to the computer

*PCB mount switches have two additional plastic legs that makes it easier for the switches to stay on the PCB while you solder. Plate mount can work, but it will be harder.

## Step 3: Solder the Pro-Micro
* Make sure to position the Pro-Micro on the side of the board WITHOUT diodes.
* It is also extremely important that you solder the pro micro on so that the smooth of the pro micro is facing up so that the footprints match up.
* The long pins face the pro micro while the short pins face the pcb.
* I first solder the long side of the pins to the Pro Micro, and then solder the short side of the pins onto the Uni PCB from the bottom.

Picture of me soldering the Pro Micro

![Me soldering Pro Micro To The Uni PCB](https://github.com/petercpark/The_Uni/blob/main/Pics/soldering-pro-micro.jpg?raw=true)

Here is how the arduino should look on the board

![Pro Micro soldered on backwards on the top of the PCB](https://github.com/petercpark/The_Uni/blob/main/Pics/pro-micro-on-uni.jpg?raw=true)

## Step 4: Solder the Switches
* Place the switches on the board
* Flip the board over to solder
* Be careful to not let the switches slip off the pcb or else you will be left with some crooked keys.

## Step 5: Place the Keycaps and Rubber Feet
* Place your keycap of choice.
* Rubber feet go here:

![Rubber Feet Placement](https://github.com/petercpark/The_Uni/blob/main/Pics/rubber-feet.jpg?raw=true)

## Step 6: Flash it with QMK Toolbox
* Download the [firmware](https://github.com/petercpark/The_Uni/releases/tag/v1.0.0) (the_uni_default.hex)
* Download [QMK Toolbox](https://github.com/qmk/qmk_toolbox/releases) (qmk_toolbox.exe)
* Open up QMK Toolbox
* Select the_uni_default.hex file that you downloaded
* Make sure it says ATMega32U4 at the top right
* Check Auto-Flash
* Next, plug in the keyboard to your computer and using a piece of conductive metal such as a tweezer, connect GND to RST on the back of the keyboard. Wait for it to load up and you have succesfully flashed the keyboard.

![QMK Toolbox configuration](https://github.com/petercpark/The_Uni/blob/main/Pics/qmk-toolbox-setup.jpg?raw=true)

## Step 7: Hook it up with Plover (applies to those of you who bought the fully assembled version as well)
* Make sure that the Uni is plugged in to your computer.
* Open Plover and go to "Configure"
* Click "Machine" and under the drop down select "Gemini PR"
* Click "Scan"
* Click on the drop down that says "Port" and select the "COM[insert_number]" option that shows up.
* Click "Apply" and then "OK"
* Click the drop down on machine and select Gemini PR if it is not already selected and then click the refresh icon.
* Click "Enable" on the Output and you are good to go!
* If it does not work, then go back to "Configure" and try selecting a different "COM[insert_number]"
Now you should be able to use the Uni for steno and use your keyboard normally without having to toggle Plover on and off.
