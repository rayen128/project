# Fade

Instead of turning the LED on and off abruptly, we’re going to make the LED fade slowly in and out. For this we can use the function `analogWrite()`. This function does not write a binary value `HIGH` or `LOW` to the pin, but a value between 0 and 255. Which allows us to write an “analog” value to the pin. If we would replace the line

    digitalWrite(13, HIGH);

with

    analogWrite(13, 20);

in the 'blink' program, we can see the LED blink all the same but at a much lower intensity. Note that `analogWrite(13, 0)` corresponds to `digitalWrite(13, LOW)` and `analogWrite(13, 255)` corresponds to `digitalWrite(13, HIGH)`.

> Note: the function is called `analogWrite`, but the output is not really analog. It is a PWM output. \[[More information](index.php?dir=30+Background&file=30+PWM)\]

## Exercise

Write a program that lets a LED fade in and out slowly. Tip: you might need a `for` loop.
