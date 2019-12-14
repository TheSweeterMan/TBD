# Build Instructions
### System diagram
![Image of SystemDiagram](https://thesweeterman.github.io/TBD/SD.PNG)

### Bill of Materials/Budget
[DS18B20=$5.85](https://www.creatroninc.com/product/ds18b20-temperature-sensor-55-to-125c/?search_query=Ds18B20&results=3)

[Raspberry PI 4 Model B(4GB=$88.75)](https://www.creatroninc.com/product/raspberry-pi-4-model-b-4gb/?search_query=raspberry+pi&results=59)

[6 PIN RECEPTACLE SOCKET=$0.44](https://www.creatroninc.com/product/6-pin-receptacle-socket/?search_query=SOCKET&results=231)

[3 PIN RECEPTACLE SOCKET=$0.40](https://www.creatroninc.com/product/3-pin-receptacle-socket/?search_query=SOCKET&results=231)

[3" (M-F) JUMPER WIRE(10 PACK)=$2.34](https://www.creatroninc.com/product/3-m-f-jumper-wire-10-pack/?search_query=CONJU&results=11)

[22AWG HOOKUP WIRE - RED=$4.75](https://www.creatroninc.com/product/22awg-hookup-wire-red/?search_query=HOOKUP+WIRE&results=23)

[Capri Tools Wire Strippper and cutter=$18.99](https://www.amazon.ca/Capri-Tools-CP20013-Professional-Stripper/dp/B01018D07K/ref=sr_1_5?crid=2Z2XTP5GSBVST&keywords=wire+stripper&qid=1576270031&sprefix=wire+%2Caps%2C163&sr=8-5)

[HALF SIZE BREADBOARD - WHITE=$5.95](https://www.creatroninc.com/product/half-size-breadboard-white/?search_query=Half+size+breadboard&results=4)

[Safety Glasses=$30.45)](https://www.amazon.ca/3M-SecureFit-Protection-Glasses-Anti-fog/dp/B0197YJQGI/ref=sr_1_1_sspa?crid=116HJL57V8J66&keywords=safety+glasses&qid=1576270662&sprefix=safet%2Caps%2C171&sr=8-1-spons&psc=1&spLa=ZW5jcnlwdGVkUXVhbGlmaWVyPUExTk5YME9UU0UwTVo5JmVuY3J5cHRlZElkPUEwMzc4MjE3MklRMzFQMFlWT0RYRSZlbmNyeXB0ZWRBZElkPUEwMjUzNjk4MkZWUjRIWVNPODkzRSZ3aWRnZXROYW1lPXNwX2F0ZiZhY3Rpb249Y2xpY2tSZWRpcmVjdCZkb05vdExvZ0NsaWNrPXRydWU=)

[Total=$157.91](https://github.com/TheSweeterMan/TBD/blob/master/BuildBudget.PNG?raw=true)

### Time Commitment

Materials- 30 minutes

Mechanical Assembly- 30 minutes 

PCB- 1 day

Soldering - 1 hour

Power up- 30 minutes

Unit Testing- 5 minutes

Total- 1 day 2 hours 35 minutes

### Mechanical Assembly

Requires:

Bread board, male to male jumper wires, DS18B20 temperature sensor, 4.7k resistor, and Raspberry pi

Step 1:

Place Bread board on table and insert sensor into breadboard.


![Image of sensor](https://thesweeterman.github.io/TBD/PowerUp/step1.PNG)

Step 2:

Insert a 4.7k resistor into the vdd pin and data pin of the sensor.

![Image of SolderingPart1](https://thesweeterman.github.io/TBD/PowerUp/step2.PNG)



Step 3:
Connect your vdd pin to the power supply on your raspberry pi.

![Image of SolderingPart1](https://thesweeterman.github.io/TBD/PowerUp/step3.PNG)

Step 4:
Connect the 1 wired data pin to gpio4.

![Image of SolderingPart1](https://thesweeterman.github.io/TBD/PowerUp/step4.PNG)

Step 5:

Connect the gnd pin to gnd pin on the raspberry pi.

![Image of SolderingPart1](https://thesweeterman.github.io/TBD/PowerUp/step5.PNG)

### Case

Use the link provided below to create your own lazer cut raspberry pi case.

[Raspberry pi case](https://github.com/TheSweeterMan/TBD/blob/master/Raspberry_Pi_model_B%2B_or_Pi2_model_B_case.zip)

### PCB / Soldering

Requires:

PCB Board, 4.7K resistor, wires, 3 pin socket, and 6 pin socket. 

![Image of PCB](https://thesweeterman.github.io/TBD/PCB.PNG)

TOP:

Step 1

Insert the 3 pin stocket into the leftside, where the 3 holes align.

![Image of SolderingPart1](https://thesweeterman.github.io/TBD/Soldering/step1.PNG)

Step 2

Insert 4.7k resistor into the middle holes

![Image of SolderingPart1](https://thesweeterman.github.io/TBD/Soldering/step2.PNG)

step 3

Insert 3 stripped wires into the via's on the middle right of the pcb

![Image of SolderingPart1](https://thesweeterman.github.io/TBD/Soldering/step3.PNG)

Step 4

Solder the 3 stripped wires into the via.

![Image of SolderingPart1](https://thesweeterman.github.io/TBD/Soldering/step4.PNG)




Bottom:

Step 5

Flip PCB board over on to back and insert the 6 pin in the first raspberry pi slot on the pcb. Also, solder the 3 pin holes.

![Image of SolderingPart1](https://thesweeterman.github.io/TBD/Soldering/step5.PNG)

Step 6

Solder wires that acquire soldering.

![Image of SolderingPart1](https://thesweeterman.github.io/TBD/Soldering/step6.PNG)

  Top:
  
Step 7
Flip back to the top of the pcb board and solder the 6 pin stocket holes 

![Image of SolderingPart1](https://thesweeterman.github.io/TBD/Soldering/step7.PNG)


### Power Up

Step 1:

Power up your Raspberry pi and go to Terminal.

![Image of SolderingPart1](https://thesweeterman.github.io/TBD/MechanicalAssembly/Step1.PNG)

step2:

Type in the command sudo nano /boot/config.txt. This command should bring you to the config.txt file, and when your in this file scroll all way down and type in dtoverlay=w1-gpio at the bottom line. Then save and leave the file.

![Image of SolderingPart1](https://thesweeterman.github.io/TBD/MechanicalAssembly/step2.PNG)

![Image of SolderingPart1](https://thesweeterman.github.io/TBD/MechanicalAssembly/step2.5.PNG)


step3:

Type in the command sudo reboot to reboot the raspberry pi and save config.txt changes.

![Image of SolderingPart1](https://thesweeterman.github.io/TBD/MechanicalAssembly/step3.PNG)

step4: 

Once The raspberry pi is rebooted open back up the terminal and type in the command sudo modeprobe w1-gpio

![Image of SolderingPart1](https://thesweeterman.github.io/TBD/MechanicalAssembly/step4.PNG)

step5:

Then type in the command sudo modprobe w1-therm

![Image of SolderingPart1](https://thesweeterman.github.io/TBD/MechanicalAssembly/step5.PNG)

Step 6:

Then type in the command cd /sys/bus/w1/sevices

![Image of SolderingPart1](https://thesweeterman.github.io/TBD/MechanicalAssembly/step6.PNG)

Step7:

This command should bring you to new directory and once your in this directory type in the command ls.

![Image of SolderingPart1](https://thesweeterman.github.io/TBD/MechanicalAssembly/step7.PNG)

Step 8:

Ten you will have change the directory by typing in the command cd address.

![Image of SolderingPart1](https://thesweeterman.github.io/TBD/MechanicalAssembly/step8.PNG)

Step 9: 

After the directory is changed, type in the command cat w1_slave to show the raw temperature

![Image of SolderingPart1](https://thesweeterman.github.io/TBD/MechanicalAssembly/step9.PNG)

step 10:

Type in cd to get back to the root directory. After use the command sudo nano temp.py and use the code provided below to get temperature reads.

[Temperature Code](https://github.com/TheSweeterMan/TBD/blob/master/PowerUp/Code)


![Image of SolderingPart1](https://thesweeterman.github.io/TBD/MechanicalAssembly/step10.PNG)

Step11:

Finally, use the command sudo python temp.py to run your code and get readings.

![Image of running](https://thesweeterman.github.io/TBD/MechanicalAssembly/step11.PNG)


![Image of PCB](https://thesweeterman.github.io/TBD/PowerUp.PNG)

### Unit Testing

Run the code and sqeeze on the sensor to see if you have the proper readings.

### Production Testing

Get every 50th DS18B20 tempeature sensor in the production line and use a premade circuit to test the product.
