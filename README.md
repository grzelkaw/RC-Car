# RC-Car
Remote Control car using two ESP32 microcontrollers. First ESP32 is used to handle car. Second ESP32 is used as controller. Communication between both board is via Wi-Fi.

![image alt](https://github.com/grzelkaw/RC-Car/blob/main/screenshots/4.jpg?raw=true)

# Components
<h3>Car</h3>
<p>- ESP32 DEV MODULE</p>
<p>- 4 DC MOTORS</p>
<p>- SG90 servomotor</p>
<p>- OV7670 camera</p>
<p>- L293D H Bridge
<p>- 4.7Ω resistors</p>

<h3>Controller</h3>
<p>- ESP32 DEV MODULE</p>
<p>- TFT 2.4″ OLED screen </p>
<p>- Analog Joystick</p>
<p>- 2 Tact Switches</p>

# Car
<h3>Chassis</h3>
<p>Whole body of car is made from LEGO Technic bricks. In center there is empty space for powerbank which works as power supply. 
DC Motors are mounted via zip tie to LEGO bricks.
Steering system is also made from LEGO and is controlled by SG90 servomotor.
Most of the parts are taken from LEGO 42035 set.
</p>

![image alt](https://github.com/grzelkaw/RC-Car/blob/main/screenshots/1.jpg?raw=true)

<h3>Power supply</h3>
<p>In center of car is laying 10000mAh power bank with two USB-A outputs. 
Both USB ports can give up to 2A, but for 3.5A MAX on total. 
First USB port is used only to power 4 DC MOTORS and SG90 servomechanism.
Second USB port is used directly to power ESP32 board. Then ESP32 provides 3.3V output to power everyother component like camera.
</p>

![image alt](https://github.com/grzelkaw/RC-Car/blob/main/screenshots/2.jpg?raw=true)

<h3>Electronics</h3>
<p>
Car's microcontroller is connected to the same Wi-Fi network as controller's microcontroller.
ESP32 send signals received from second ESP32 to H Bridge to controll DC MOTORS. 
If we set PIN X as high and PIN X as low then car will go forward, otherwise will go backwards. 
PIN X sends PWM signal to H Bridge to controll speed of the motors. 
PIN X sends PWM signal to controll servomotor enabling turning right or left.
OV7670 camera sends video to local HTML page via Wi-Fi. 
</p>

# Controller
<h3>Case</h3>
<p>Base of controller is basicly two connected small breadboards.</p>

<h3>Power supply</h3>
<p>ESP32 is powered by micro-USB cable. Then board is powering every component so screen and analog joystick.</p>

<h3>Electronics</h3>
<p>
Microcontroller' joystick is connected to PIN X for vertical signal and PIN X for horizontal signal. 
Vertical movement sends PWM signal to change speed of DC Motors.
Horizontal movement sends PWM signal to change servomotor position allowing to turn wheels.
Tact Switch buttons are connected with internal pull-up resisotrs with PIN X and PIN X.
PIN X button send signal to move the car forward and PIN X button sends signal to move the card backwards.
ESP32 receive video signal from HTML page and then displays image on TFT screen.
</p>

![image alt](https://github.com/grzelkaw/RC-Car/blob/main/screenshots/3.jpg?raw=true)

# Circuit diagram
<h3>Car</h3>

![image alt](https://github.com/grzelkaw/RC-Car/blob/main/screenshots/5.png?raw=true)

<h3>Controller</h3>

![image alt](https://github.com/grzelkaw/RC-Car/blob/main/screenshots/6.png?raw=true)

# Code
<p>Programm was written in Arduino IDE. I used OV7670 camera library made by X to handle camera functionality.</p>

<h3>Car</h3>
<p>
TODO CODE DESCRIPTION
</p>

<h3>Controller</h3>
<p>
TODO CODE DESCRIPTION
</p>

