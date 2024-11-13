# Bike Light

Create a bike light with a button and a LED: If you press the button once, the LED turns on; when you press it a second time, the LED starts blinking; when you press the button a third time, the LED turns off again.

Hm… this might be trickier than it seems. You need to do multiple things at once. Blink a light and check for button input. How to deal with that?

The function 'delay()' is getting in the way. Every time you call 'delay()' you block the Arduino. So you cannot use it for anything, not for checking a button state or anything else. This makes it hard to do multiple things at the same time.

### Part 1: Blink

Make a LED blink, but this time without using the function 'delay()'. Instead you can use the function 'millis()'. This function returns the amount of milliseconds that have passed since the Arduino was turned on.

### Part 2: Button

Write a program that checks a button every 200 milliseconds. Again, do this without using 'delay()'. When the button is pressed, toggle a LED. Make sure that when you keep the button pressed, it does not continue toggling the LED.

### Part 3: Bike Light

Now add a the third mode: blink. So when the button is pressed once, it simply turns the LED on. But when it is pressed a second time, the LED starts blinking. Press the button a third time and the LED turns off again. Again, don't use 'delay()'.
