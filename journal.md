---
title: "flip clock"
author: "lola sanchez"
description: "a mock-sort of flip clock that tracks...how many missing assignments i have "
created_at: "2025-05-30"
---

## initial design
- i plan to use two stepper motors attached to a pcb with a wifi board that recieves a number and sets its two digits to that number. it will be all in a case, and the there will be two wheels with digits from 1-10 on them on the stepper motors, with there being a little piece of plastic/metal sticking out in the front that keeps the digits in place. it will look a little like this:
![image](photos/clockExample.png)
every time the missing assignments increase, the motor will turn with just enough force so that the next number flips over. the turning wheels should look like this, but with numbers from 1-10.
![image](photos/wheel.png)
the wheels should have a hole in them that fits snugly on the motor shaft.

## checklist
- [ ] pcb
    - esp32 module with external button to turn on and off and way of sending signal to stepper motor, while also keeping track of what number the clock is on at the moment. (could be done through server? that number needs to be persistent and i have no idea how to store stuff permanently/on disk on a microcontroller. OR could just flip the numbers to 00 everytime its turned off and just get the number from the server to put itself back every time it turns on. hmmmmm). might add some more stuff, like a status light or some other small things if im going through the trouble of getting a pcb anyways
- [ ] case
    - still unsure as to what to do for the case - needs to house the motors and pcb and battery, and most important, needs the thing sticking out in front (frame)
- [ ] finding materials
    - motors
    - material for case? (probably pla filament)
    - microcontroller
    - battery
- [ ] software
    - need some sort of software SOMEWHERE that scrapes my school's assignment website (blackbaud) and gets my assignments and sends over a number to the local pcb.
    - will probably use nest to expose an api. but i need to use chromedriver, or some sort of other headless chrome tool (need to get around google oauth!!) which requires some significant space and computational power, so we will see. i have a working headless chrome tool on my computer with golang specifically for this purpose, that uses a library which promises to be portable and not rely on a locally downloaded chromedriver, i just need to move it to nest - which will probably take some work. preferably i'd run this all locally on the pcb, but raspberry pi 5s are expensive!

# completed on june 1st, whole planning took one hour ish
---

