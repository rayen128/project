# LED

## Important to know:

1. LED's are directional (they have a positive and negative side). If you connect it the wrong way around, it doesn't do anything.
2. Always connect a LED in series with a resistor! LED's have very little resistance themselves, that means that if you connect them directly to a power source without a series resistor, they are likely to blow up.

## Directionality

The LED typically has a longer and a shorter lead. The shorter lead is the negative side (also called cathode):

![LED direction](LED-direction.png "200px")

## Resistors

A LED requires a resistor (connected in series) to prevent too much current going through it. If you don't do this, you'll likely blow up the LED. Typical resistances for a LED are in the range 100Ω - 2kΩ. The higher the resistance, the lower the intensity of the emitted light. [More information](arduino/bg-resistpr-values)
