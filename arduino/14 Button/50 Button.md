# Button

Time for some input. We're going to connect a push button to our Arduino.

## Getting started

### Circuit

First we need to build the circuit. For this we need a resistor (around 10kΩ) and, well, a push button:

![Button](images/Components-Button.jpg "300px")

Connect them like this:

![Push button hookup](images/BB-Button.png "300px")

### Code

The following code prints the state of the push button to the Serial monitor.

    void setup()
    {
      Serial.begin(9600);
      pinMode(2, INPUT);
    }

    void loop()
    {
      int buttonState = digitalRead(2);
      Serial.println(buttonState);
      delay(20);
    }

The button pin is configured as input with `pinMode(2, INPUT)`. The state of the button (HIGH or LOW) is read with the function `digitalRead(2)`.

Copy this sketch and save as `button`. Compile, upload and test this sketch.

> What is printed when you press the button? What is printed when you release it?

## Exercise

Use a button to turn the LED on and off. When the button is pressed, the LED is on, otherwise it is off.
