Welcome! My first PCB design had some challenges. It was not my first time soldering in general, but
it was my first time having to solder an entire PCB. I found that part quite easy, especially with
enough flux. I personally prefer lead-less solder, even though it requires a higher temperature.

The first challenge was when I first assembled everything together, it didn't work. I used a lot of
time testing the entire circuit with a continuity test, and then later simple voltage tests to see
where it's going wrong. I still couldn't find anything, and then had to use the "dead-bug" technique,
of taking the IC, flipping it, gluing it to a breadboard, and individually attaching wires to it to
test every part of it. Interestingly, I found that the problem was that the comparator was a pull,
meaning when the (+) voltage was higher than the (-) voltage, the output pin completed a circuit
instead of sending +5V as I thought it would.

Originally, I thought that I'd have to redesign the circuit and wait a couple more weeks for another
PCB, but I got an idea. I ended up physically shifting all of the LEDs so that only one of the pads
were touching, and stringing a copper wire around, touching all of the "floating" pads of the LEDs,
which was connected to the positive voltage terminal of the USB port.

This created a circuit where voltage was being sent through the LEDs, but if the comparator was not
"on", then the circuit was never completed, meaning no current would flow through the LED - thus it
didn't turn on. Then, when the comparator turned on, the circuit was completed, and the current was
still limited by the resistor so that the LED wouldn't burn up.

What I thought was the simplest project I could think of, turned out not so simple. I'm glad that
it happened, as it taught me how to design, assemble, dissasemble, analyze, test, fix, and reassemble
a circuit when a complete redesign wasn't an option. True engineering!

I wanted to redesign this circuit anyway, as the number of resistors in the circuit made it so that
the first couple of LEDs wouldn't turn on until the fourth LED voltage level was met. I wanted to
use USB-C and PD technology to push around 30V through the circuit, and upgrading the resistors to
compensate.
