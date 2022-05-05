# Halim Worklog Notebook

[[_TOC_]]

## 2022-02-16 - Discussion with Kenny
Objective: Discuss with our project sponsor, Kenny, with project details and outline key aspects related to our design
Progress: We sent an email to our project sponsor Kenny regarding our inquiries of the project and the design in general. After receiving Kenny's reply, we had set up a zoom meeting to discuss some things regarding the design. After the session, we finalized on some of the aspects of the design:

Kenny presented a paper explaining that a separate ground plane can poetentially be unnecessary, but does have higher noise than if we had one. In the scope of our project, we decided to include the ground plane in order to eliminate potential noise issues.
Our design will include three patches and a hub. One patch for the reference ground plane and the other two for the positive terminal of the voltage measurement. The hub will contain all the voltage processing, analog to digital conversion, and wireless transmission.
We plan to replace the previous suction system by using clipping ECG patches, which enhances replaceability.
Retractable wires will be used in order to eliminate potential wire issues.

## 2022-02-22 - DESIGN DOCUMENT CHECK
Objective: Receive feedback on our draft design document.
Progress:
#### \<General Feedback\>
#### Tolerance analysis
1. The most important point in our project
2. How modifications will change the results
3. Specific component, not a module
4. Equations should be in separate lines from text
#### Requirement and Verification
1. Lines start in the same page
#### Block diagram
1. You don’t put specific chips on block diagram
#### \<Our Design Document Feeback\>
#### High-level Requirements
1. Add tolerance
	- what if cut off freq is not within the bound
	- if 200Hz is coming from somewhere, put citation (like [3])
#### Block diagram
1. Some of the lines are hard to distinguish
    - e.g., between power and ground 
2. Show what’s 3.3V and 5V
3. Label transmission as bluetooth
4. Data
    - analog or digital ? —> label them
    - if have different data protocols
5. No need to label all the ground
6. Lines a bit confusing
    - from the top
7. Arrow between 9b and 5.5
    - invisible (too small)


## 2022-02-28 - DESIGN DOCUMENT improvement
Objective: Improve the design document based on the feedback provided
Progress: Here is the updated version of our block diagram:

<img width="1041" alt="스크린샷 2022-05-04 오후 3 12 14" src="https://user-images.githubusercontent.com/33310400/167015643-7e07ad4b-5b88-485d-bf4a-48489f3957cb.png">

I deleted the unnecessary ground arrows as given in the feedback, and made the lines much clearer for easier comprehensiveness. 


## 2022-03-08 - PCB round 1 deisgn, and feedback
Objective: Design first round of PCB design and receive feedback
Progress: Here is round 1 PCB design of our device:

<img width="847" alt="스크린샷 2022-05-05 오후 2 59 38" src="https://user-images.githubusercontent.com/33310400/167015881-0d1de266-722d-4d9a-bf41-04ec114af23b.png">

It contains bridge connectors for the battery, power switch, voltage regulator, SEN-12650 chips, and the ESP32 chip. As we were not fully confident with the choice of our microprocessor, it is likely that this design will not function properly in terms of wireless transmission, but it does provide a good start. I believe that I can make the PCB smaller than this current design, such that the device is much more compact in size. 



## 2022-03-15 - Testing LEAD I, III signal with a dev board (SEN-12650)
Objective: Check if the board is able to produce a correct ECG signal
Progress: Ye and I visited the lab to test whether we were able to obtain an ECG signal using the SEN-12650 board. This board contains the AD8232 chip with a biasing configuration listed in its datasheet. 
<img width="450" alt="스크린샷 2022-05-05 오후 2 32 17" src="https://user-images.githubusercontent.com/33310400/167011687-ac4d86a2-d7e7-448c-b17a-248034d30c17.png">

Connecting the V_s, ground, and the electrode patches to the body (Right Arm (RA, positive node), Left Arm(LA, negative node), and Right Leg (RL, ground node)), we were able to see the ECG signal shown above. This corresponds to Lead I signal of the ECG. Now switching to having LA, LL, RA, we were able to obtain the Lead III signal. 

## 2022-03-23 - Ordering Necessary Components
Objective: Order all necessary components through my.medicine purchasing portal
Progress: Since our project was sponsored by Kenny from the medical school, we had plenty of funding available compared to other groups. 
Here are what I ordered:
#### \<Mouser\>
1. 9V battery snaps - for mounting the battery
2. 9V batteries
3. AD8232 - Heart Rate Monitor Front End
4. Anti-vandal switch
5. Resistors : 360k, 100k, 10M, 180k, 1M
6. Capacitors : 1u, 0.22u, 3.3n, 0.022u, 
#### \<Sparkfun\>
1. 3.5mm TRRS Audio Jack - for SMD
2. Voltage Regulator - 3.3V - COM-00526
#### \<Digikey\>
1. Electrode pad sensor cable in 3 - for wire connection to the ECG patches
2. 10uF capacitors

Since we had sufficient funding, resistors and capacitos were picked by considering a high voltage rating (more stable). 
I would expect them to arrive in a week, though some parts might take longer. 

## 2022-03-30 - PCB round 2 design
Objective: Design second round of PCB design
Progress: Here is round 2 PCB design of our device:

<img width="790" alt="스크린샷 2022-05-05 오후 3 03 29" src="https://user-images.githubusercontent.com/33310400/167016429-19c5985c-49fc-43c9-ae21-a2cf36050c8f.png">

Based on the successes and failures from PCB round 1, this design is implemented in the hope of creating more space in the enclosure. Test points are added for debugging purposes. One main challenge here is to solder the AD8232 chip on it. It is a QFN packaging, which is a type that does not have legs. It would require heatguns to solder them. I will try soldering them next week. 


## 2022-03-31 - Ordering the plastic enclosure
Objective: Order the plastic enclosure to match our PCB design
Progress: Consideirng the size of our PCB, an enclosure with 76.20mm x 76.20mm x 38.10mm was chosen. It contained screws that can be fixed after successfully installing all the necesasry comopnents inside.
Here are what I ordered:
#### \<Polycase\>
1. TS-3315P Plastic Electronics Enclosure - x2 (in case one breaks apart)


## 2022-04-06 - Soldering components to PCB
Objective: Solder components on PCB to test funtionalities of subsystems
Progress: Battery connection and the voltage regulator was soldered to test whether the output of the voltage regulator was able to produce 3.3V. It indeed is able to produce a steady voltage around 3.29V with an error in only millivolts. 
Onto soldering the AD8232 chip, I referred to youtube tutorials on how to solder QFN packaging chips. Upon wasting about 6 chips and 3 boards, I believed that I had soldered them correctly. After soldering the resistors and capacitors on, I connected everything and tested for the signal on the oscciloscope. However, I was not able to see any output signal. I used proves to test each node of the AD8232 chip. The input voltage, input signal nodes were working, but I could not see any outputs. The verified nodes might have even been not connected to the chip itself, as the probe was thicker than the width of each leg. It was 4 hours of soldering with no outcome. Ye and I discussed about this issue and decided to use SEN12650 board for our device. 
Using the SEN-12650 would guarantee us to produce the correct signal, but far from our initial objective. However, we are able to justify this. When we ordered our resistors and capacitors, we intentionally ordered them in 1206 packaging, which comes in a larger size such that it is easier to solder. However, for the SEN-12650 board, the resistors and capacitors were in 0805 packaging, and are aligned very nicely. 

![12650-02](https://user-images.githubusercontent.com/33310400/167017796-38ec19a3-313e-42be-8b1c-af890d0559c6.jpg)

Therefore we were able to justify our decision by claiming that this board ultimately can be more ideal as its entire setup is compact in size. We decided to use a hot air machine to desolder the audiojack portion, which would significantly reduce the space that this board takes. 




## 2022-04-08 - Ordering replacement parts required
Objective: Order necessary components that changed after the testing of final product
Progress: Upon checking the arrived PCB, I realized that I ordered the wrong packing for the 3.5mm audio jack connector. 

![스크린샷 2022-05-05 오후 2 48 20](https://user-images.githubusercontent.com/33310400/167014227-5a3cc730-8071-49d4-ad11-9d0a0aef446e.png)

The connector on the top was what I had ordered, but the connector packaging did not fit the layout printed in our PCB (left). Hence I had to reorder the audio connector that fits this type of packaging. I learned about different packasing styles and realized that I need to be more considerate about packaging standards when considering putting parts together.
Furthermore, upon testing the functionality of the anti-vandal switch that I had ordered, I realized that this is the type of switch that only turns on when I am pressing and holding the button. This is far from ideal since we want the switch to be hands-free. This was a OFF-(ON) type specified in Mouser, and the type that we should look for is OFF-ON-OFF. A rocker switch, though doesn't have a LED indicator, is a perfect fit given our compact size. I decided to add a small LED that is separate from the switch that tells us whether the device is On or OFF. 

Here are what I ordered:
#### \<Mouser\>
1. Rocker Switch - RA12131100
2. Phone Connectors (SMD) - SJ-3523-SMT-TR



## 2022-04-22 - Mounting PCB with the enclosure in the Machine Shop
Objective: Visit Machine Shop to drill holes in appropriate places of our device enclosure
Progress:

I visited the Machine Shop to follow up on our details of the design with the desired placements. We discussed placements for the battery case, LED, rocker switch, input circular hole for the ECG wire, hole for the three signal wires to be checked with the osciilscope (signal 1, signal 2, ground), and hole for a USB connection with the microprocessor. As I explained my requirements, they suggested me some solutions, which were a tremenderous help. What they suggested was:
1. Cut out the corners of the PCB to be able to mount the PCB at the bottom of the enclosure
2. Place the battery on the top of the device so that a user won't need to open the enclosure every time when battery needs to be replaced
Here is a picture of the 
