## Members
Jack Leddy, Computer Engineering Student
jackleddy@vt.edu

## Mentor
MENTOR NAME HERE

## Current Status
IN PROGRESS

## Project Overview

The goal of this project is to create a 2.5 axis cnc controlled plotter with the ability to tool change. A plotter is a device that holds a pen and follows G-Code instructions to draw. My current design implements an x-y gantry with a servo actuated z axis. 

*video example, maybe*

Future iterations may expand to lazer engraving, simple lazer cutting, or wood cnc routing.  

## Educational Value Added

Building this CNC plotter has immense educational value through integrating design, mechanics, electronics, controls, and software into a single system. 

I have a controls engineering internship lined up for summer 2026, and a lot of the machines I will be working on are 3 axis gantrys. This project will serve as a window into the full stack design process, alongside giving me a machine to practice with. I plan to use this plotter not just for making interesting art, but also to learn ladder logic position control and simulated PLC software.

Skills and concepts that have been applied up to this point:
- Translating vague goals and constraints into a workable architecture which is iteratively designed and edited into a completed first draft
- CAD in Fusion
- Understanding and working around mechanical constraints
- Designing a motor control system
- Electronic and mechanical parts selection based on goals and specs

## Tasks

<!-- Your Text Here. You may work with your mentor on this later when they are assigned -->

## Design Decisions

<!-- Your Text Here. You may work with your mentor on this later when they are assigned -->
1. Frame
Originally I was planning on not having the aluminum extrusion frame and just attatching the linear rails to 3D printed parts which would be bolted to the mdf board, but this seemed like it would not be rigid enough for fast, precise movement. A more robust frame also allows for more future upgrades, like the lazer engraver. If the design were changed to have a screw-driven z axis sat on the x axis, the machine may even be retrofit to work as a subtractive cnc machine with a router. 

2. Motors
NEMA 17 stepper motors were chosen for their low cost, small profile, and relatively good performance. Their step size is small enough for the level of precision I am aiming for, but it is hard to know if they will be strong enough for this application. I'm mostly worried that the torque will decrease as speed increases. The current design has a ~60mm length NEMA 17 for the x axis and ~48mm length stepper for the y axis. 
A mg90s micro servo (ideally metal gears) will be used to raise and lower the end effector. Another stepper is likely not needed for the z axis, as only up/down states must be reachable. 

3. X Axis
I was torn over how to drive the x axis. The main options were (1) two x motors, one for each side, (2) one x motor with a mechanical linkage between the sides, and (3) one x motor and only drive the single side. The dual motor option seemed complex to control because another driver would be needed, and dealing with desynchronization would be troublesome. The best balance looked to be mechanically linking the sides, probaby with the x motor driving an axle that runs perpendicular to the x axis and connects to the belts on both sides, however I am unsure whether even this will be necessary. For now, I have decided to only drive one side of the x axis, because the y axis is relatively short and the racking/torsion forces might not be an issue. If racking is an issue, the upgrade will not be a challenge, as room has been left for the axle and drive belt on the other side of the x axis.

4. Belts vs Lead Screw
Screws are more rigid than belts, but this is a simple plotter and the tool shouldn't be seeing much force, so belts will be strong enough. Belts are also generally faster at translational movement as compared to screws.

5. Size
Originally, I designed the machine to be about 1.5x bigger along each axis, but this seemed redundant and akward. The final design has a drawimg area for A2 paper, about 600x420 mm. Shorter axes means more strength and less expensive materials, alongside 3D printed joints receiving less force.

6. Electronics
For the control and power delivery, I made relatively standard decisions based on the specs I had already designed. An Arduino Uno with hobbiest CNC shield and 2 stepper drivers rated at 2.2 A each handle the motor control including firmware for G-code streaming. I will test the machine using grbl, an open source firmware that converts G-code to CNC motor control signals, but I plan to write my own eventually. For power delivery I will use a DC power supply sized for stepper peak current, alongside the arduino and stepper needs. 

## Design Misc

<!-- Your Text Here. You may work with your mentor on this later when they are assigned -->

## Steps for Documenting Your Design Process

<!-- Your Text Here. You may work with your mentor on this later when they are assigned -->
- Maintain a work log on this git repo
- Store CAD and control files here
- Pictures and videos

## BOM + Component Cost

<!-- Your Text Here. You may work with your mentor on this later when they are assigned -->

## Timeline

<!-- Your Text Here. You may work with your mentor on this later when they are assigned -->

## Useful Links

<!-- Your Text Here. You may work with your mentor on this later when they are assigned -->

## Log

<!-- Your Text Here. You may work with your mentor on this later when they are assigned -->
