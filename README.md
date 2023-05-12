# Cyclone_Game
Cyclone Game


The aim of this project was to re-create a popular arcade game known as the Cyclone. The goal of the game is to stop the LED at a certain point. The catch is that the LED is cycling very fast. Making it harder for the user to react. Furthermore, an offset was added to ensure that the LED is not always aligned to a normal cycle. This offset can be seen in the WaveGen image above.

Supplying the circuit with a 3.3V supply will first cause all the LED’s to illuminate. The current wave output we have set here is going to pass in ‘0’ to the registers of the 74HC164 causing the LED’s to turn off one by one due to the right shifting of registers discussed above. Then the pattern generator will shift ‘1’ into the 74CH164 causing the LED’s to turn on one by one.

You may notice that in general there are 8 high inputs provided by the DIO 1 for every low/high input provided by the DIO 0. However, this will not be the case all the time because the frequencies are not aligned properly. This is done intentionally to provide a small offset which accumulates over time which will either introduce either an extra ‘0’ or an extra ‘1’. This was part of your design requirements as the client does not want the game to be easy to beat

COMPONENTS USED
NAME	DESCRIPTION
74HC164	8 bit serial-in parallel-out shift register
Analog Discovery 2	USB oscilloscope, logic analyzer, and multi-function instrument allowing users to work with various circuits
Push Button Switch	Switch with a push button mechanism
Multiple LEDs	LEDs used to visualize the game
Assorted Resistors	Used for multiple case scenarios
3.3V Power Supply	Power supply to power circuit
