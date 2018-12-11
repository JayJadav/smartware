# Build Instructions for using MAG3110 Magnetometer Sensor on a Raspberry Pi 3B+
####            By Jay Jadav • For Hardware Production Technology CENG 317, Humber College School of Applied Technology

<br />
# MAG3110 Sensor

## Table of Contents
- [Introduction](#Introduction)
- [UML Diagram](#UML-Diagram)
- [Functionality](#Functionality)
- [Build Materials and Budget](#Build-materials-and-Budget)
- [Time Commitment](#time-commitment)
- [Mechanical Assembly](#Mechanical-Assembly)
- [PCB and Soldering](#pcb-and-soldering)
- [Powering Up Device](#powering-up-device)
- [The Software](#the-software)
- [Testing](#testing)
- [Finished Product](#finished-product)
- [Resources](#resources)
<br />

# Introduction
Freescale's MAG3110 is a small, low-power, digital 3-axis magnetometer. The device can be used in conjunction with a 3-axis accelerometer to realize an orientation independent electronic compass that can provide accurate heading information.

![mag3110](https://user-images.githubusercontent.com/43185906/49823957-e2d9c880-fd4e-11e8-8f70-44ee31da6da7.jpg)

You can buy Raspberry Pie from [here]( https://www.raspberrypi.org/products/raspberry-pi-3-model-b-plus/)
and  the MAG3110 sensor from [here]( https://www.sparkfun.com/products/12670).

# UML Diagram 
![uml](https://user-images.githubusercontent.com/43185906/49811569-8ae09900-fd31-11e8-8731-d61196c1b937.png)
# Functionality:
![image](https://user-images.githubusercontent.com/43185906/49824195-8c20be80-fd4f-11e8-9433-6161749a942a.png)

# Build-Materials-and-Budget

A full list of materials along with a detailed view of costs can be downloaded form within this repository.[budget.docx](https://github.com/JayJadav/smartware/files/2621811/budget.docx)

The total cost of producing this project is heavily inflated due to the cost of the soldering kit that was supplied in the lab during
development. Any generic solding iron can be used for this project.

The total cost after removing the soldering kit is: **$398.27 CAD** after HST. This includes all the tools used in completing the project (eg. wirecutters, needlenose pliers, breadboard, etc.)

Notable purchases include: Raspberry Pi 3B+ Kit ($107.29 CAD) and MAG3110 3-axis Magnetometer ($24.76 CAD).

### Raspberry Pi 3b+

![rpi3b](https://user-images.githubusercontent.com/42980862/49776194-078b5d00-fcc9-11e8-8d61-f96a17dfd31c.PNG)

Also known as Rpi 3b+ is the newest as well as fastest pocket sized computer. 

### Features and Specifications:
- 1.4GHz 64-bit quad-core processor
- dual-band wireless LAN
- Bluetooth 4.2/BLE
- Faster Ethernet
- Power-over-Ethernet support 
- 4 USB 2.0 ports
- 5V/2.5A DC power input
- MicroSD for setting up Operating System as well as storing personal data

### MAG3110 

![mag3110](https://user-images.githubusercontent.com/43185906/49823957-e2d9c880-fd4e-11e8-8f70-44ee31da6da7.jpg)

### Features and Specifications:

- 1.95V to 3.6V Supply Voltage
- 7-bit I2C address = 0x0E
- Full Scale Range ±1000 μT
- Sensitivity of 0.10 μT
- Pull Up Resistor Jumper
- 13.3 x 14.5 mm

## Time Commitment
A detailed view of the schedule followed this semster can be downloaded from within this repository [Schedule.zip](https://github.com/JayJadav/smartware/files/2621844/Schedule.zip)

This schedule uses a weekly breakdown that follows the CENG 317 class schedule for the fall semester of 2018. This project could be completed in a more compact time frame if the builder so chooses. The schedule is helpful in outlining the overall flow and the order in which each milestone for the project is completed. Orignally the project was completed over a 15 week semester, however it could more reasonably be completed in 1-2 week(s) dependant on how many of the materials the builder already possesses, access to the facilities necessary in producing the PCB, and shipping times. 
<br />

# Mechanical Assembly

### 1) Steps for setting up Rpi:

a. Setup SD card:

  - **NOOBS** is the recommended as well as easy to install software for initializing Raspberry Pi. 
  - Insert SD card underneath Rpi's micro SD card slot
 
b. Connections:

   - HDMI cable,Ethernet cable,Keyboard,mouse 
   
  **Note** - Switch computer display to HDMI from VGA to initialize raspberry PI
           - Must see red led on rpi and blinking green led. 
           - During the setup, system will ask user to set username,password
      
 c. Setting up files for internet connection:
 
  - Issue the following command: ``` sudo /etc/network/interfaces``` to make changes in wpa_supplicant.conf which looks like:
  
  ```
  network={
	ssid="myWi-Fi@Humber"
	key_mgmt=WPA-EAP
	auth_alg=OPEN
	eap=PEAP
	identity="Username or N-Number"
	password="Password"
	phase1="peaplabel=0"
	phase2="auth=MSCHAPV2"
	priority=999
	proactive_key_caching=1
}
```
**Make sure to reboot!**

   - In order to run program from Putty, turn on ```SSH``` options from ```Interface``` option from Rpi
   - For Sensor readings, enable ```GPIO feature```
              
 
 
 Startup Screen looks like:
 
  
   ![startscreen](https://user-images.githubusercontent.com/42980862/49777295-f1cc6680-fccd-11e8-8aad-ea40f830cb08.PNG)
   
  
  Fresh Screen after setup:
  
![pi-desktop](https://user-images.githubusercontent.com/42980862/49777538-e62d6f80-fcce-11e8-9446-ed2d50d9548e.png)


### In order to get rid of using HDMI, mouse and a keyboard there's an alternative steps:

- Before making any connection to Rpi make sure to perform te steps

    a. Go to ```Network And Sharing Center``` option from control panel and go to your actual Wifi connection to which computer is connected to and then go to ```properties/Sharing``` which looks like:
    
    ![wifi stat](https://user-images.githubusercontent.com/42980862/49777786-f1cd6600-fccf-11e8-9720-2d31cc633486.PNG)
    
    b. Enable the following option:  
    - [x] Allow other network users to connect through this computer's internet connection. 
    And in the dropdown list choose your Ethernet option
    
    ![ethrnt](https://user-images.githubusercontent.com/42980862/49778059-445b5200-fcd1-11e8-9e32-a4653de4528f.PNG)
    
    This will assign IP address to your raspberry Pi.
    
    c. Go to remote desktop connection and go for ```raspberrypi.mashome.net```
    
    ![image](https://user-images.githubusercontent.com/42980862/49778147-ab790680-fcd1-11e8-9469-78ef9798cf00.png)
    
    
   ### 2) Steps for pinout:

1) Solder your sensor

2) Follow the RPI Header reference for your pinout to breadboard

3) Look for the 3V/5V pin from your Rpi and connect it to breadboard (pin no.1)

4) Connect VCC to 3V power supply and GND to common ground (pin no.5 in 2nd Row)

5) Now connect your SCL to I2C clock SCL pin on your RPi(pin no.3 in 2nd Row)

6) Connect SDA to I2C clock SDA pin on your RPI (which is pin no.2 in 2nd Row)

#### Breadboard ####
After following the Pinout this is what the breadboarded sensor will look like 
![image](https://user-images.githubusercontent.com/43185906/49827675-e02fa100-fd57-11e8-9ca3-f8e56ec868c1.png)


Next, to ensure the MAG3110 has been connected properly for I2C communications, the following command should be entered in to the Pi's terminal: ```sudo i2cdetect -y 1```. This will display a simple graphic listing each device connected to the I2C bus and it's corrisponding address. The address the MAG3110 uses is 0x0e.


![whatsapp image 2018-11-26 at 8 55 05 pm](https://user-images.githubusercontent.com/43185906/49053955-582a9280-f1c0-11e8-80eb-0f55d59a4f8a.jpeg)

## PCB and Soldering
The following PCB was designed and used for this project. The Gerber files for the PCB can be found from within this repository.[sensor.zip](https://github.com/JayJadav/smartware/files/2618036/sensor.zip) Included in these files is a save for the application **Fritzing** which was used to produce this design. This file can be opened and used by the same program to add any modifications to the board as the builder should see fit. Such as, their own name and a description. 



To construct the PCB, the prototype lab located at Humber College was used. However, any third party production facility may be used, as the files are universally accepted as an industry standard. The two images below show the PCB constructed from both the top and bottom. A 6 pin header has been soldered to the top of the PCB to connect to the MAG3110 and a 68 pin header has been soldered to the bottom to connect to the GPIO pins on the Pi.
** Top **
![whatsapp image 2018-11-26 at 8 55 06 pm 3](https://user-images.githubusercontent.com/43185906/49054973-084dca80-f1c4-11e8-9900-d0bf9f48963b.jpeg)

** Bottom **

![whatsapp image 2018-11-26 at 8 55 06 pm 5](https://user-images.githubusercontent.com/43185906/49055245-d8eb8d80-f1c4-11e8-9943-502f761685ae.jpeg)




