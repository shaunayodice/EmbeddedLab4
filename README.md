# Embedded Lab 4


Question 1:
In Question 1, the code shown allows for the ability to toggle a Green LED found on the MSP430FR2355 microcontroller. To do so, timer interupt processes will be used. On the MSP430FR2355, the green LED is found on port "P6.6". This means that P6.6 will be an output for the code. A specific timer be chosen in order to be able to have the green LED toggle at 250ms. The timer used for this application will be the auxiliary timer of 250ms represneted by the macro named "WDT_ADLY_250" in the provided code used. In order to enable to interrupt capability, SFRIE1 |= WDTIE will be used as it will use the bitwise or operator in order to turn on the interupt. The LED will then be able to oscillate by using the bitwise XOR operator for the output P6 Bit6 by using the code P6OUT^=BIT6. 


Question 2:

A) Below is the table that compares the calculated and the measured values for a PWM signal with 10% duty cycle. 

**insert table**

The image below shows the hand calculations that were used to find the duty cycle, period, and frequency. 

**insert image of hand calculations**

The image below is the signal from the oscilloscope. In the image, the frequency is shown to match the calculated frequency.

**Oscilloscope Reading**
![image](https://user-images.githubusercontent.com/98931471/200151590-2a5a245b-2b1d-46ed-860b-4768dc889c9e.png)


B) UML Diagram

C) The code for this portion of the lab can be found in the file named, "Q2"

Question 3:


A) The image below shows the hand calculations used to find the duty cycle, period, and frequency of the PWM. 

**insert image of hand calculations**

The image below depicts the singal generation on the oscilloscope. Here the frequency measured was X.

**Oscilloscope Image**
![image](https://user-images.githubusercontent.com/98931471/200151601-c0e14307-012a-4390-aa55-00ff32991f19.png)


B) The table below compares the hand calculation values to the values measured on the oscilloscope.

**insert table**

C) The code for this question can be found inside the file labeled, "Q3"

