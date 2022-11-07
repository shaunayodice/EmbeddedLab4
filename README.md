# Embedded Lab 4

# Overview

This lab disccusses the process of using the clock of the microcontroller to generate a PWM signal. Polling was implemented in the code used to execute this on the MSP430 Microcontroller board.


# Question 1:

In Question 1, the code shown allows for the ability to toggle a Green LED found on the MSP430FR2355 microcontroller. To do so, timer interupt processes will be used. On the MSP430FR2355, the green LED is found on port "P6.6". This means that P6.6 will be an output for the code. A specific timer be chosen in order to be able to have the green LED toggle at 250ms. The timer used for this application will be the auxiliary timer of 250ms represneted by the macro named "WDT_ADLY_250" in the provided code used. In order to enable to interrupt capability, SFRIE1 |= WDTIE will be used as it will use the bitwise or operator in order to turn on the interupt. The LED will then be able to oscillate by using the bitwise XOR operator for the output P6 Bit6 by using the code P6OUT^=BIT6. 


# Question 2:

A) Below is the table that compares the calculated and the measured values for a PWM signal with 10% duty cycle. As the table shows, the calculated and measured values match almost indentical. The duty cycle and the period were provided in the question, but we were able to generate the PWM to have a duty cycle at exactly 10%. 

**Table of Measured VS. Calculated Results**

![image](https://user-images.githubusercontent.com/98931471/200187166-5b34c9f5-a9cb-4189-bb9b-0faf932bbeb0.png)


The image below shows the hand calculations that were used to find the duty cycle, period, and frequency. The period of the signal was provided in the question as well as the duty cycle. Using the given information, we wee able to find the value for both CCR0 and CCR1 as shown in the image below. 

**Hand Calculations to Find CCR1 and CCR0**

![image](https://user-images.githubusercontent.com/98931471/200186997-743eb2c5-161e-45ad-91fc-4f5345dd111f.png)


The image below is the signal from the oscilloscope. In the image, the duty cycle is shown to match the calculated duty cycle. The period shown from the generated signal is at 500.6 ms which was very close to the desired 500 ms period found in the hand calculations. 

**Oscilloscope Reading**

![image](https://user-images.githubusercontent.com/98931471/200151590-2a5a245b-2b1d-46ed-860b-4768dc889c9e.png)


B) UML Diagram

![image](https://user-images.githubusercontent.com/93303476/200198812-e1b56e36-2967-4a26-84a0-435d4d34aa59.png)

C) The code for this portion of the lab can be found in the file named, "Q2"

# Question 3:


A) The image below shows the hand calculations used to find the duty cycle, period, and frequency of the PWM. The duty cycle and the period were provided in the question. Using this information, we found the CCR 0 and CCR 1 freqency values using the formula shown in the image below. 

**Hand Calculations to find CCR0 and CCR1**

![image](https://user-images.githubusercontent.com/98931471/200186985-f4456710-33a0-4f71-8fe6-db83a6244b01.png)


The image below depicts the signal generation on the oscilloscope. Here the duty cycle matched the 20% were were looking to achieve. The period was 250.3 ms which also matched the desired period of 250 ms.

**Oscilloscope Image**

![image](https://user-images.githubusercontent.com/98931471/200151601-c0e14307-012a-4390-aa55-00ff32991f19.png)


B) The table below compares the hand calculation values to the values measured on the oscilloscope. The values found in the hand calculations matched the values collected from the generated PWM signal using the oscilloscope.

**Table of Measured VS. Calculated results**

![image](https://user-images.githubusercontent.com/98931471/200187208-104719a4-b0dc-4f88-9b02-0e2113cd8568.png)


C) The code for this question can be found inside the file labeled, "Q3"

