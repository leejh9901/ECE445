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

## 2022-03-22 - Testing LEAD I signal with a dev board (SEN-12650)
Objective: Check if the board is able to produce a correct ECG signal
Progress: Ye and I visited the lab to test whether we were able to obtain an ECG signal using the SEN-12650 board. This board contains the AD8232 chip with a biasing configuration listed in its datasheet. 
<img width="450" alt="스크린샷 2022-05-05 오후 2 32 17" src="https://user-images.githubusercontent.com/33310400/167011687-ac4d86a2-d7e7-448c-b17a-248034d30c17.png">





## 2022-04-22 - Mounting PCB with the enclosure in the Machine Shop
Objective: Visit Machine Shop to drill holes in appropriate places of our device enclosure
Progress:

I visited the Machine Shop to follow up on our details of the design with the desired placements. We discussed placements for the battery case, LED, rocker switch, input circular hole for the ECG wire, hole for the three signal wires to be checked with the osciilscope (signal 1, signal 2, ground), and hole for a USB connection with the microprocessor. As I explained my requirements, they suggested me some solutions, which were a tremenderous help. What they suggested was:
1. Cut out the corners of the PCB to be able to mount the PCB at the bottom of the enclosure
2. Place the battery on the top of the device so that a user won't need to open the enclosure every time when battery needs to be replaced
Here is a picture of the 
