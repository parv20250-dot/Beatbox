# Beatbox
Welcome to the land of music and dreams (hopefully not nightmares). Here you see me try my hand at making a drum pad.
<img width="388" height="335" alt="FINAL" src="https://github.com/user-attachments/assets/1449425f-2714-4b47-89b3-f5927518e0eb" />
<img width="446" height="342" alt="back final" src="https://github.com/user-attachments/assets/21901a30-afb5-4a0a-8942-fdbdaab3770b" />
(note: the colour can be selected/altered on the pcb manufacturer's app)

#Basic functioning
The drum pad detects when it is hit using Piezo discs which are basically small discs that can measure changes in pressure or vibration through the piezoelectric effect. When you strike the pad the force flexes the internal ceramic element inside the piezo disc creating an electrical signal. This is used to sense when it is hit and also the intensity of the hit through the vibrations caused on impact.
This information is send to the ESP-32-C3-Supermini which then computes what sound to play and how loud to play it and sends this information or audio data to the Amplifier module. The amplifier module then converts this information/audio data to playable audio and sends it to the speaker resulting in sound being played. 

There is also protective equipment such as resistors and diodes, which can be observed in the schematic below.
<img width="421" height="286" alt="final schematic" src="https://github.com/user-attachments/assets/88073450-250b-4eb9-a3ed-2071b24c2d58" />

LIGHT
The lighting system works mostly separate of the sound system. The WS2812(12 Bit LED ring) is connected to the ESP32-C3-SuperMini. When the Piezo disc detects a hit, the ESP simultaneously sends audio data to the Amplifier module and lighting data to the LED's. The LED rings are connected in series allowing for the lighting information to be passed along the LED rings in order to make the corresponding ring light up. There is a level shifter in between as the LED's require a 5v input whereas the ESP only outputs 3.3V of current. 

POWER
The whole system is powered via USB-C input on the ESP.

SPECIAL EFFECT-
When the Piezo discs are hit in a particular order within a predefined time frame, it plays a special long sound effect and lights up all four LED's.

FIRMWARE-
#todo

Credits-
This project has been inspired by several different drum pad projects online, however, the design, pcb layout and firmware are all my own. This project was made as a part of the Half Life event by Hack Club.


