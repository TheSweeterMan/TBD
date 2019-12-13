# Build Instructions
### Introduction using a system diagram
![Image of SystemDiagram](https://thesweeterman.github.io/TBD/SD.PNG)

### Bill of Materials/Budget
[DS18B20=$5.85](https://www.creatroninc.com/product/ds18b20-temperature-sensor-55-to-125c/?search_query=Ds18B20&results=3)
[Raspberry PI 4 Model B(4GB=$88.75)](https://www.creatroninc.com/product/ds18b20-temperature-sensor-55-to-125c/?search_query=Ds18b20&results=3)

[6 PIN RECEPTACLE SOCKET=$0.44](https://www.creatroninc.com/product/6-pin-receptacle-socket/?search_query=SOCKET&results=231)

[3 PIN RECEPTACLE SOCKET=$0.40](https://www.creatroninc.com/product/3-pin-receptacle-socket/?search_query=SOCKET&results=231)

[3" (M-F) JUMPER WIRE(10 PACK)=$2.34](https://www.creatroninc.com/product/3-m-f-jumper-wire-10-pack/?search_query=CONJU&results=11)

[22AWG HOOKUP WIRE - RED=$4.75](https://www.creatroninc.com/product/22awg-hookup-wire-red/?search_query=HOOKUP+WIRE&results=23)

[Capri Tools Wire Strippper and cutter=$18.99](https://www.amazon.ca/Capri-Tools-CP20013-Professional-Stripper/dp/B01018D07K/ref=sr_1_5?crid=2Z2XTP5GSBVST&keywords=wire+stripper&qid=1576270031&sprefix=wire+%2Caps%2C163&sr=8-5)

[HALF SIZE BREADBOARD - WHITE=$5.95](https://www.creatroninc.com/product/half-size-breadboard-white/?search_query=Half+size+breadboard&results=4)
[Safety Glasses=$30.45)](https://www.amazon.ca/3M-SecureFit-Protection-Glasses-Anti-fog/dp/B0197YJQGI/ref=sr_1_1_sspa?crid=116HJL57V8J66&keywords=safety+glasses&qid=1576270662&sprefix=safet%2Caps%2C171&sr=8-1-spons&psc=1&spLa=ZW5jcnlwdGVkUXVhbGlmaWVyPUExTk5YME9UU0UwTVo5JmVuY3J5cHRlZElkPUEwMzc4MjE3MklRMzFQMFlWT0RYRSZlbmNyeXB0ZWRBZElkPUEwMjUzNjk4MkZWUjRIWVNPODkzRSZ3aWRnZXROYW1lPXNwX2F0ZiZhY3Rpb249Y2xpY2tSZWRpcmVjdCZkb05vdExvZ0NsaWNrPXRydWU=)

[Total=$151.97](https://thesweeterman.github.io/TBD/BuildBudget.PNG)

### Time Commitment
### Mechanical Assembly
Requires: 
Bread board, male to male jumper wires, DS18B20 temperature sensor, , and Raspberry pi

[Youtube tutorial](https://www.youtube.com/watch?v=aEnS0-Jy2vE&t=87s)

### PCB / Soldering
Requires:
PCB Board
![Image of PCB](https://thesweeterman.github.io/TBD/PCB.PNG)
TOP:
Step 1:
Insert THE 3 pin stocket into the leftside, where the 3 holes align.
Step 2:
Insert 4.7k resistor into the middle holes
step 3:
Insert 3 stripped wires into the via's on the middle right of the pcb
Step 4:
Solder the 3 stripped wires into the via.
step 5:
flip PCB board over and go to step 6
![Image of SolderingPart1](https://thesweeterman.github.io/TBD/SolderingPart1.PNG)
BOTTOM:
Step 7:
Solder the 3 pin stocket holes 
Step 8:
Solder the 4.7k resistor holes
Step 9: 

Solder the the 3 stripped wires on the bottom side this time.

Step 10:
Insert the 6 pin socket into pcb board
Top:

Step 11: 

flip the pcb board back to the top and solder in the 6 pin socket.
![Image of SolderingPart2](https://thesweeterman.github.io/TBD/SolderingPart2.PNG)

### Power Up
Step 1:
Power up your Raspberry pi and go to Terminal.
![Image of SolderingPart1](https://thesweeterman.github.io/TBD/Mechanical Assembly/Step1.PNG)
step2:
Type in the command sudo nano /boot/config.txt. This command should bring you to the config.txt file, and when your in this file scroll all way down and type in dtoverlay=w1-gpio at the bottom line. Then save and leave the file.
![Image of SolderingPart1](https://thesweeterman.github.io/TBD/Mechanical Assembly/step2.PNG)
step3:
Type in the command sudo reboot to reboot the raspberry pi and save config.txt changes.
![Image of SolderingPart1](https://thesweeterman.github.io/TBD/Mechanical Assembly/Step1.PNG
step4: 
once The raspberry pi is rebooted open back up the terminal and type in the command sudo modeprobe w1-gpio
![Image of SolderingPart1](https://thesweeterman.github.io/TBD/Mechanical Assembly/step1.PNG)
step5:
then type in the command sudo modprobe w1-therm
![Image of SolderingPart1](https://thesweeterman.github.io/TBD/Mechanical Assembly/step5.PNG)
Step 6:
Then type in the command cd /sys/bus/w1/sevices
![Image of SolderingPart1](https://thesweeterman.github.io/TBD/Mechanical Assembly/Step1.PNG)
Step7:
this command should bring you to new directory and once your in this directory type in the command ls.
![Image of SolderingPart1](https://thesweeterman.github.io/TBD/Mechanical Assembly/Step1.PNG)
Step 8:
Ten you will have change the directory by typing in the command cd address.
![Image of SolderingPart1](https://thesweeterman.github.io/TBD/Mechanical Assembly/Step1.PNG)
Step 9: 
After the directory is changed, type in the command cat w1_slave to show the raw temperature
![Image of SolderingPart1](https://thesweeterman.github.io/TBD/Mechanical Assembly/Step1.PNG)
step 10:
type in cd to get back to the root directory. 
![Image of SolderingPart1](https://thesweeterman.github.io/TBD/Mechanical Assembly/Step1.PNG)
![Image of SolderingPart1](https://thesweeterman.github.io/TBD/Mechanical Assembly/Step1.PNG)


![Image of PCB](https://thesweeterman.github.io/TBD/PowerUp.PNG)

### Unit Testing

### Production Testing
Get every 50th DS18B20 tempeature sensor in the production line and use a premade circuit to test the product.
