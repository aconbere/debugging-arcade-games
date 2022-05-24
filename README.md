How to get started repairing your arcade cabinet:

## General Theory

Most arcade systems are composed of three major systems.

1. Power
2. Board
3. Monitor

When we're starting fresh with a game, we want to move through each of these systems, in this order.

## First Steps

Before you begin it's best to have a Service Manual for your game, and if you can find it, for the monitor installed in the cabinet. You can often find these on KLOV but otherwise they might just required some digging around the internet. It's important to remember that these machines were designed to be service in the field by relatively inexperienced operators. The service manuals are often filled with information on how to debug and fix common errors.

## Power

In most arcade machines you'll find one of two kinds of power supplies: Linear or switching.

For both linear and switching power supplies it's important to verify that the power supply is still functioning correctly and within spec. Failures in the power supply can result in large downstream failures of the board or monitor and can cause irreperable damage.

Needed Parts:
* A Service Manual for the machine (or power supply documentation)
* Multimeter

* Ensure the machine is unplugged
* Disconnect the board and monitor from power
* Do a visual inspection:
    - Look for signs of heat damage
    - Water damage
    - Broken or cracked wires
* Test all fuses
* Plug in the machine
* With a multimetter validate the power supply test points read within spec

Note:
* For many power supplies you may get slightly out of spec readings when the supply isn't loaded.

## Board

When power has been verified to be good you can move onto testing the board.

Needed Parts:
* A service manual for the board
* A multimeter

Step 1:
* Ensure the machine is unplugged
* Reconnect the board to power
* Reconnect the board to the monitor and audio
* Plug the machine back in

- If you don't get video output: go to step 2.
- If you get video output go to Step 7:

Step 2:
* If you can't hear audio go to step 3
* If you can hear audio go to step 6:

Step 3:

Without audio or video your job just got harder, but it's still not impossible. First you want to ensure that power is infact getting to your board. Most systems will run on +5v but may have several other voltages that are delivered to the board for various sub systems (audio, vector processing, etc). Often times aboard may have a power LED to help test this but even with the power LED we want to get a good multimeter reading to ensure the quality of the power. To test this most arcade boards will have several test points labeld on the board (a ring and a label with the correct voltage). If you don't see anything like this refer to your service manual to see if there's any notes.

* If you board is not getting good power go to step 4:
* If you board has good power go to Step 5.

Step 4:

If your board isn't getting power, but you've validated clean power from the power supply in the previous section, then there are several possibilities:

* Check the wiring from the power supply to the board. Are there any broken or frayed wires?
* Use your multimeter to check connectivity between the board connector and the power supply
* Use your multimeter to ensure that wires carrying power (+5v etc) aren't shorted to ground.
* Use your multimeter to ensure that the board connections for power and GND aren't shorted.

If none of these have found the fault move on to Step 5;

Step 5:

Well this is bad, your board is getting clean power, but you don't have audio or video out. That means there's an error on the board itself, but this still isn't the end! It's just the end of what I can help with. At this point the debugging is machine dependant. You'll want the board manuals and schematics if possible. As examples of the kinds of issues I've repaired: A capicitor in the power rail was broken off and causing +5v to be open, a crystal had broken off and was causing the CPU to have no clock, a logic chip had failed that was preventing the CPU from initializing correctly. When fixing these kinds of errors it usually involves hunting around with a logic probe, an oscilloscope, and a multimeter to trace out the operation of the machine one chip at a time.

Step 6:

If your machine boots up and you have audio but no video, you have a machine that is what we call "playing blind". This is good news because it means the board is running in some capacity! From this point you should look up how to run a self test in the service manual to diagnose any other potential issues. But otherwise should continue to the Monitor section.

Step 7:

If your machine boots up and you're getting video is the video:

* Roughly correct but missing colors or distored or wobbly? If so go to the Monitor Section.
* Missing sprites, oddly garblged, totally incomprehensible? If so go to Step 8.

Step 8:

You potentially have bugs in the board that are impacting the boards ability to output valid video signals.

## Monitor

.. TODO
