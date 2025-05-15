# FireAlarm_LM358P

Firealarm using Thermistor for the sensor and LM358P for Comparator. 

How it works:
Thermistor and 10K Resistor are being series connected so it could be a Voltage divider for our LM358P Comparator. Remember Thermistor are variable resistor who are changing it value based on the temperature around the resistor. So in order to make a tresh hold and make the comprator works we will use another variable resistor but the one where we could set it manually the Potensiometer (set constant parameter for comparator that couldnt change because of the envioremental state or we could just use voltage divider for this offset, it works both way anyway).


Technical Side / How comparator works and why we use it.


LM358P are dual comparator who are comparing between two input and the outcome are different when the the +/- are higher. in order to active or we could send a voltage to the buzzer and led that indicated there's a fire. We have to make sure the output from the LM358P are Positive Voltage. So how we gonna make sure that the output are Positive Voltage when the fire are occure and the system are beeping correctly?
in order to know how we are gonna check the schematic of our system first 

![image](https://github.com/user-attachments/assets/c5d7e611-b0c2-4ad9-8241-941967b61991)

here's the schematic you could see that LM358 have 4 input 2 positive input and 2 negative input and there's a VCC and Ground. So in order for the output are positive voltage we HAVE TO make the positive input are higher than negative input so we could output the positive side of lm358 which in case of this we use 5V.

So how it gonna works?


well i already explained that we use a thermistor and potensiometer for the input of LM358P so when you turn on the system what you want to do first are to set the offset first using the potensiometer until the buzzer stop beeping. why? Buzzer being beeping or turn on meaning that our output for the lm358P are high (in this context 5V since im using 5V power supply to the lm358p positive side) in order the system works we have to make sure that input from the potensiometer are lower than thermistor. So when the thermistor are detecting some fire meaning that the resistance of thermistor are changing and making the voltage of the voltage divider changing so eventually the output of LM358P will be positive. 


Advice for further development or someone who want to make it again.

-Adding a Pipe / DC Motor system so that it will automaticlly sprinkle a water for the room.

-Considering using PTC instead of NTC for better voltage dividing in the LM358P input side.
