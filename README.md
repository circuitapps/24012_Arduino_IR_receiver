# 24012 - IR RECEIVER USING ATTINY85 MICROCONTROLLER
---

In this project we are introducing a simple IR receiver circuit and code that will allow you to integrate remote control function to various projects using the ATtiny85 microcontroller.

Following is the circuit diagram of the IR receiver. It is a very simple circuit indeed!

![IR receiver circuit diagram](./AtTiny85_IR_receiver.png)

You can access the AtTiny85 software code using the following link.

![AtTiny85 code folder](./attiny85_24012)

Though the above code showcases an IR remote control function for changing color of an RGB LED in our **<u>[project video][1]</u>**, there are many other things you can do with simple modifications to this basic code.

Description: This code demonstrates how off the shelf remote controllers can be repurposed to control any device using an AtTiny85 microcontroller using this IR receiver code. For the purpose of demonstrating how the IR receiver works, this control application uses an RGB LED as the target device to generate different colors using an IR remote control. However, it can easily be modified to control many other devices such as motors, lamps, MP3 players, and many more!

Though you can use any IR remote controller, we suggest you get a cheap X11TI1 (see purchase link: www.amazon.com/dp/B0CG37L55Z), which will be fully compatible with the code here. 

Following are the button map we have used in this code:
#define LEDS_OFF BUTTON_HASH
#define RED_LED_ON BUTTON_LEFT
#define GREEN_LED_ON BUTTON_OK
#define BLUE_LED_ON BUTTON_RIGHT
#define TEAL_LED_ON BUTTON_UP
#define ORANGE_LED_ON BUTTON_DOWN

Therefore, when you press the left button on IR remote X11TI1, you should see the Red light turn on on the RGB LED. (Be sure to review the circuit diagram in this repository to create the same demo set up we have used for in this project) Use other mapped buttons to experiment with other light functions.
 
If you decide to use an alternative IR remote controller, you will need to first create a table of which button generates which 8-bit code and use that table to allocate your control functions to the buttons of your choice. You can simply connect AtTiny85 (device pin 7) that is programmed to send serial data to a host at 115200 baud to decode any IR transmitter button presses using this code! WE suggest you use TeraTerm as the serial terminal on your computer to perform this.

If you build this project, please share your thoughts and suggestions with the rest of circuitapps community in the comments section of **<u>[our YouTube video][1]</u>**. Also, please feel free to talk about any interesting modifications you make and your experimentations!

## Project Challenges
Though this is a simple project, be careful with the polarity of the leads when connecting the IR receiver to the rest of the circuit. Especially when connecting the +5V and GND as reversing this by mistake can damage the receiver!

## Useful tip

If you have not worked with ATtiny85 before and need support with the basic operation and programming of this device, have a look at this **<u>[excellent reference][2]</u>** that walks you through the entire process step by step. If you get stuck, drop us a message in the comments section of **<u>[our YouTube video][1]</u>**


GOOD LUCK & ENJOY CONTROLLING ELECTRONIC DEVICES FROM THE COMFORT OF YOUR SEAT WITH THIS IR RECEIVER !


[1]: <UPDATE YOUTUBE VIDEO TO PROJECT>

[2]: https://circuitdigest.com/microcontroller-projects/programming-attiny85-microcontroller-ic-using-arduin