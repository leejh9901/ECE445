# Notebook
## Week 4 (2/7/2022 – 2/13/2022)
### 2/8/2022 (Tue)


## Week 5 (2/14/2022 – 2/20/2022)
### 2/16/2022 (Wed)
We sent an email to our project sponsor Kenny regarding our inquiries of the project and the design in general. 
After receiving Kenny's reply, we finalized on some of the aspects of the design:
1. Kenny presented a paper explaining that a separate ground plane can poetentially be unnecessary, but does have higher noise than if we had one. In the scope of our project, we decided to include the ground plane in order to eliminate potential noise issues. 
2. Our design will include three patches and a hub. One patch for the reference ground plane and the other two for the positive terminal of the voltage measurement. The hub will contain all the voltage processing, analog to digital conversion, and wireless transmission. 
3. We plan to replace the previous suction system by using clipping ECG patches, which enhances replaceability.
4. Retractable wires will be used in order to eliminate potential wire issues. 


### 2/17/2022 (Thur)
#### \<Weekly meeting with TA Notes\>
#### Logistics
- Better to finish the design document draft before Design Document Check
- Proposal should be graded by this weekend.
- Anything related to PCB -> go talk to the TA, Evan


#### Design Document
1. Have the high level requirements be perfect
2. More feedback during the design document check
3. Verification for every subsystem —> talked about it during lectures
4. Self-explanatory
5. Visual aid: zoom it and provide more details
6. You can definitely change the products you use later, but make sure that the verifications and requirements are stable.
7. Be consistent with the format, spacing, and citation (IEEE), etc.
8. Make sure to cite the last semester’s project
9. Grading is pretty harsh.


<div style="page-break-after: always"></div>


## Week 6 (2/21/2022 – 2/27/2022)
### 2/21/2022 (Mon)
PUT SOMETHING YOU FOUND OR DECIDED WHILE WORKING ON DESIGN DOCUMENT

Data Transmission Module
* Requirements
    1. Successfully transfer the data to the data visualization module
    2. Calcuate the minimum required transmission rate. Ensure the product is at least that transmission rate.

Data Visualization Module
* Requirements
    1. Display three graphs, each graph representing the data of each lead.




### 2/22/2022 (Tue)
#### DESIGN DOCUMENT CHECK
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


#### Requirement and Verification
1. The number —> is it coming from the datasheet?
    - double check that it’s not from data sheet —> no need to verify if it’s from data sheet
    - amplified correctly?
        - where is it coming from
        - maybe combine with the next one

2. Add some tolerances in these so you have rooms
3. Table capture ???


#### Tolerance analysis	
1. Put more equations
    - how you actually calculated the values you’re using
2. ADC
    - from data sheet ?
        - if so, cite it
3. Do some analysis with the frequencies




### 2/24/2022 (Thur)
#### \<Weekly meeting with TA Notes\>

1. Data transmission subsystem calculation (in the desing document) looks fine.
    - You can incorporate that with Tolerance Analysis (if you want)
    - That is something instructors/graders expect to see in Tolerance Analysis

2. Design Review is a formal presentation
    - Be on time
    - Be professional
    - etc.

3. Cite everything in the design document
    - IEEE format
    

Final R & V for Data transmissino module for Design Document 1

Here's an image of a drag racer in action:

![R & V (Data Transmission Module)](./R_andV_1_Data_Transmission_Module.png)

Move along.



<div style="page-break-after: always"></div>

## Week 7 (2/28/2022 – 3/6/2022)






<div style="page-break-after: always"></div>

## Week 8 (3/7/2022 – 3/13/2022)






<div style="page-break-after: always"></div>

## Week 9 (3/14/2022 – 3/20/2022)





<div style="page-break-after: always"></div>

## Week 10 (3/21/2022 – 3/27/2022)



<div style="page-break-after: always"></div>

## Week 11 (3/28/2022 – 4/3/2022)




<div style="page-break-after: always"></div>

## Week 12 (4/4/2022 – 4/10/2022)



<div style="page-break-after: always"></div>

## Week 13 (4/11/2022 – 4/17/2022)




<div style="page-break-after: always"></div>

## Week 14 (4/18/2022 – 4/24/2022)




<div style="page-break-after: always"></div>

## Week 15 (4/25/2022 – 5/1/2022)









