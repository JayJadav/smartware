# Week 13 Nov27
**Presentation**

Worked on final Documentation of index.md and presentation during the class hours.

[MAG3110 3-Axis Magnetometer.pptx](https://github.com/JayJadav/smartware/files/2622098/MAG3110.3-Axis.Magnetometer.pptx)

# Week 12 Nov20


#### Progress Report:-####
  This week I worked on the coral draw case . I had to make some changes in the coral draw file . As my Pcb  Board was slightly out of the raspberry pi . So I had to make changes in the width and length of the base as well as top layer but making sure that the hole-points for the raspberry pie and case don't change and are perfectly aligned.
  
 After
 
![whatsapp image 2018-11-26 at 8 55 04 pm 7](https://user-images.githubusercontent.com/43185906/49056831-3da9e680-f1cb-11e8-97d0-8c86cfe8e4aa.jpeg)

![whatsapp image 2018-11-26 at 8 55 04 pm 8](https://user-images.githubusercontent.com/43185906/49056834-413d6d80-f1cb-11e8-9712-6e8c6e88659e.jpeg)

![whatsapp image 2018-11-26 at 8 55 04 pm 4](https://user-images.githubusercontent.com/43185906/49056545-1999d580-f1ca-11e8-9352-f4748defd203.jpeg)

![whatsapp image 2018-11-26 at 8 55 04 pm 6](https://user-images.githubusercontent.com/43185906/49056551-24546a80-f1ca-11e8-9073-52532696ec10.jpeg)

 Before

  ![whatsapp image 2018-11-26 at 8 55 04 pm](https://user-images.githubusercontent.com/43185906/49056115-4220d000-f1c8-11e8-99ce-d594aae61304.jpeg)

![whatsapp image 2018-11-26 at 8 55 04 pm 1](https://user-images.githubusercontent.com/43185906/49056122-4b11a180-f1c8-11e8-9fa9-ddd4a0cbd1b3.jpeg)

The Coral draw file:

[CORAL_CASE.zip](https://github.com/JayJadav/smartware/files/2618218/CORAL_CASE.zip)

This is the picture of the coral  draw case 

![capture](https://user-images.githubusercontent.com/43185906/49056605-5f569e00-f1ca-11e8-9c04-012a5cc33bea.PNG)

# Week 11 Nov13

#### Progress Report:-####
I worked on the Power up . First I had some problem finding the code online because the sensor I ordered was from Sparkfun programmed to  be run on Raspberry Pi 3b+ and all the code available online was of Adafruit and that was also Audrino driver.So this week there was no additional expense to my original budget. 

Intiallly I faced some problem getting the values from the sensor , but by the end of the lab I was able to get the readings from my sensor.

I tried With different metallic as well as electromagnetic devices . As soon as I got them close to the senosr the readings would change.
![whatsapp image 2018-11-26 at 8 55 05 pm 2](https://user-images.githubusercontent.com/43185906/49055855-34b71600-f1c7-11e8-91f5-171996c0d903.jpeg)

 This is the code I used:-
 
 **MAG3110.py**
 [MAG3110.zip](https://github.com/JayJadav/smartware/files/2618144/MAG3110.zip)

# Week 10 Nov06

Got my pcb board and started working on soldering of it and made the use of necessary header pins as well as made sure that I can also get the same ip address once the sensor is soldered.

####PROGRESS REPORT:- ####
So it is week 10 and I got my PCB today from the prototype lab. I was late in getting it because when i went on monday to confirm that wheter my PCB is done but vlad told me that they havn't recieved any email under my name then I showed him the mail I had sent and he replied that it must be stuck in a spam or something like that and told me to re-send it again. So I got it on tuesday and did my soldering in the class.To connect my sensor to PCB I bought header pins for my sensor from the prototype lab. Once soldering was done so I tried to obtain my i2c address by connecting my PCB to the Raspberry and i was successful in doing it. 
So no additional expense was added in my original budget.
![whatsapp image 2018-11-26 at 8 55 05 pm](https://user-images.githubusercontent.com/43185906/49053955-582a9280-f1c0-11e8-80eb-0f55d59a4f8a.jpeg)

I Worked on soldering of the pcb and made sure the sensor is properly compatible with the pcb
![whatsapp image 2018-11-26 at 8 55 06 pm 3](https://user-images.githubusercontent.com/43185906/49054973-084dca80-f1c4-11e8-9900-d0bf9f48963b.jpeg)

**Soldered PCB**

![whatsapp image 2018-11-26 at 8 55 06 pm 5](https://user-images.githubusercontent.com/43185906/49055245-d8eb8d80-f1c4-11e8-9943-502f761685ae.jpeg)

# Week 9  Oct29
Created pcb design, Breadboard as well as schema and exported generated Gerber file to Prototype lab.


THe File I sent for my PCB
**Gerber File**
[sensor.zip](https://github.com/JayJadav/smartware/files/2618036/sensor.zip)

![whatsapp image 2018-10-31 at 12 09 39 pm](https://user-images.githubusercontent.com/43185906/47802103-fdf3fa00-dd05-11e8-9b34-e50ed16d51f0.jpeg)

![whatsapp image 2018-10-31 at 12 09 39 pm 2](https://user-images.githubusercontent.com/43185906/47802088-f6ccec00-dd05-11e8-9973-30492c135280.jpeg)

![whatsapp image 2018-10-31 at 12 09 39 pm 1](https://user-images.githubusercontent.com/43185906/47802072-eddc1a80-dd05-11e8-8b42-f29e63214f07.jpeg)

#### Progress Report:-####
So it is week 09. This week I worked on fritzing to make my pcb design and intially I had problem in making the via connection ,but with the help of the professor I was able to learn it and made the proper Gerber file that I can send to prototype lab. 

# Week8   Oct23 
Worked on breadboarding and soldering. Tested my addrress on RPi and noticed my default address as 0x0E. Later I realised it should suppose to show 0x0e. Worked on pinouts where I connected AD1 to +ve supply and AD0 to SCL and I was able to change my address from 0x05 to 0x0E.

**After** 
*When I changed my address* 
![whatsapp image 2018-11-26 at 8 55 05 pm](https://user-images.githubusercontent.com/43185906/49053955-582a9280-f1c0-11e8-80eb-0f55d59a4f8a.jpeg)

Steps for pinout (Only for sensor that I’m currently holding):

1) Solder your sensor

2) Follow the RPI Header reference for your pinout to breadboard

3) Look for the 3V/5V pin from your Rpi and connect it to breadboard (pin no.1)

4) Connect VCC to 3V power supply and GND to common ground (pin no.5 in 2nd Row)

5) Now connect your SCL to I2C clock SCL pin on your RPi(pin no.3 in 2nd Row)

6) Connect SDA to I2C clock SDA pin on your RPI (which is pin no.2 in 2nd Row)


![whatsapp image 2018-10-31 at 12 05 21 pm](https://user-images.githubusercontent.com/43185906/47801889-82924880-dd05-11e8-990b-06bec037c3d5.jpeg)

![whatsapp image 2018-10-31 at 12 05 21 pm 1](https://user-images.githubusercontent.com/43185906/47801849-67273d80-dd05-11e8-8d55-5040117f2e17.jpeg)


# Week7  Oct16 
This Week I got my sensor as well as Raspberry Pi from sparkfun and also worked on Psuedo code assignment with First year student.

**Parts**

![whatsapp image 2018-11-27 at 5 55 07 pm](https://user-images.githubusercontent.com/43185906/49117110-ae094400-f26d-11e8-947b-9564b7c30fcb.jpeg)

![raspberry_pi_3_b _ 40759296402](https://user-images.githubusercontent.com/43185906/49117134-c4170480-f26d-11e8-96ad-1ea1458842cf.png)


This is the psuedo code:-
[MAG3110 3-Axis Magnetometer-converted (1).pdf](https://github.com/JayJadav/smartware/files/2621191/MAG3110.3-Axis.Magnetometer-converted.1.pdf)

# Week6  Oct09
Worked on UML diagram and was a study day off .

![image](https://user-images.githubusercontent.com/43185906/49100423-e5fa9200-f241-11e8-8e5e-12d6eab21f13.png)

# Week5 Oct05

This is Invoice of The sensor and Raspberry Pi  I Ordered. 
![invoice](https://user-images.githubusercontent.com/43185906/46378746-9c8b2d80-c66a-11e8-9bd2-c2db49c1f30d.PNG)

# Week4 Sept25

Budget
![image](https://user-images.githubusercontent.com/43185906/47387436-5cedb980-d6dd-11e8-90c2-b8bd429985bb.png)

**Budget**
[budget.docx](https://github.com/JayJadav/smartware/files/2621811/budget.docx)

# Week3 Sept18
Schedule
![image](https://user-images.githubusercontent.com/43185906/47387249-c1f4df80-d6dc-11e8-9725-7fe4e579356e.png)

**Schedule**
[Schedule.zip](https://github.com/JayJadav/smartware/files/2621844/Schedule.zip)

# Week2 Sept11

Proposal
![image](https://user-images.githubusercontent.com/43185906/47385882-3e85bf00-d6d9-11e8-973b-cc82fc21dd60.png)

**Proposal**
[ProposalContentStudent.xlsx](https://github.com/JayJadav/smartware/files/2621819/ProposalContentStudent.xlsx)

# Week 1 Sept04
**Blinking LED**
