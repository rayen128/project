# Hello, world! Hello, world! Hello, w…

You might want to be able to do some debugging. Remember how useful `prinft` in C could be for that? Bad news, no `printf` for Arduino. One reason might be that the Arduino does not have a screen to print to. You can, however, send signals over the USB-connection to your computer. For this we need to setup a serial connection. This can be done by adding the line

    Serial.begin(9600);

to the setup function. This starts a connection with your PC at 9600 baud (don’t worry about the connection speed, 9600 is almost always fine).

Now you can send messages to your computer using the command

    Serial.print("Hello!");

or

    Serial.println("Hello!");

The later prints a new-line at the end of the text.

Where do these messages wind up? They’re sent over a virtual tty-modem to your computer. You can display these messages using the _Serial monitor_ in the Arduino IDE:

![Serial monitor](images/serial.png "300px")

## Exercise

Write a program that displays the text “Hello, world!” endlessly (until the Arduino is turned off):

    Hello, world!
    Hello, world!
    Hello, world!
    Hello, world!
    ...

Make sure there is a pause of at least 200 milliseconds between every “Hello, world!”.
