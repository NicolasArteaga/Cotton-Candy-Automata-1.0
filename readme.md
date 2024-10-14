# Cotton Candy Automata 1.0

### **Project Overview**

The Cotton Candy Automata project involves developing a robotic system for the automated production of cotton candy.

In summary, this project required approximately 360 hours and included a proposal phase, the definition of primary objectives, optimization of variables for cotton candy production, and an iterative development and testing process, culminating in the final testing phase.

### Process

The workflow consists of the following stages: sugar filling, machine activation, stick placement, cotton candy creation, and serving. These are organized into four phases.

In the first phase (sugar filling and machine activation), the robotic arm grips the sugar holder funnel for 0.5 seconds, deposits 8 grams of sugar into the spoon, serves it to the machine, and returns the spoon to its original position. The machine and heating buttons are then activated.

In the second phase (stick placement), the arm retrieves a stick, positions it at the center of the rotary head, and waits for the necessary idle time.

During the third phase (cotton candy creation), the arm moves in a circular motion with a radius of 13 cm and vertically along a 10 cm range, just as the sugar begins to melt. This phase continues until all the sugar is consumed, with consumption parameters determined by environment temperature, the amount of sugar used, and the cooldown time from the previous batch.

In the final phase (serving), the completed cotton candy is placed in a designated vase, and the heating element is turned off. The robotic arm remains idle for the cooldown period before powering off the machine and returning to its starting position.

The software files for this project can be accessed at [https://cpee.org/hub/?stage=development&dir=Teaching.dir/Prak.dir/TUM-Prak-24-SS.dir/](https://cpee.org/hub/?stage=development&dir=Teaching.dir/Prak.dir/TUM-Prak-24-SS.dir/) (Cottonbot.xml for the CPEE environment), and in the robot’s memory under /NicolasArteagaCottonbot/cottonbot.urp.

- The standard parameters defined at the start of the workflow are:
    - spin time: 1 spin, 3.75s
    - always: 25 spins, 93.75s
    - normal(2-3): 60s wait time
    - cold start: 101.25s wait time
    - hot start(4-7)): 50s wait time
    - cooldown: 90s cold spinning time
    - radius: 0.13 m = 13 cm (no contact) or 0.145 m (occasional contact with plastic)
    - height diff: 0.05m=5cm from center or 10cm total
    - sugar amount: 0.5s = 8g (change to sleep(in6) if parametized with variable in6)

### Technical Details

The automaton consists of seven 3D-printed components, which can be found in the folder “3D Models,” as well as a cotton candy machine (including base, rotary head, aluminum cover, plastic cover, and cable), a food-safe spoon, and a sugar holder. The only additional materials required for each cotton candy are standard 30 x 0.4 x 0.4 cm wooden sticks and refined white sugar.

Below is an image of the Cotton Candy Automata components needed for the start of the automaton:

![1265DCC4-AC2C-450D-AB3D-72E29104FCF6_1_201_a.heic](Cotton%20Candy%20Automata%201%200%2011f3835bc17f80b28492dd993cb6950e/1265DCC4-AC2C-450D-AB3D-72E29104FCF6_1_201_a.heic)

### Future Work

Future developments for this project will focus on improving key elements, such as measuring the rotary head’s temperature with an external sensor to enhance workflow efficiency, designing a sensor that identifies which stick can be used next, and determining the maximum number of cotton candy units that can be produced before the machine requires cleaning, in order to reduce errors in production.