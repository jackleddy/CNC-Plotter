## Members
Jack Leddy, Computer Engineering Student
jackleddy@vt.edu

## Mentor
MENTOR NAME HERE

## Current Status
IN PROGRESS

## Project Overview

The goal of this project is to create a 2.5 axis cnc controlled plotter with the ability to tool change. A plotter is a device that holds a pen and follows G-Code instructions to draw, and my current design implements an x-y gantry with a servo actuated z axis. 

*video, maybe*

This machine may also be upgraded to a lazer engraver or cutter in future iterations. 

## Educational Value Added

Building this CNC plotter has immense educational value through integrating design, mechanics, electronics, controls, and software into a single project. 

I translated vague goals and constraints into a workable architecture which was iteratively designed into a completed first draft. Sdd

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

5. Size

6. Control 

7. Electronics

## Design Misc

<!-- Your Text Here. You may work with your mentor on this later when they are assigned -->

## Steps for Documenting Your Design Process

<!-- Your Text Here. You may work with your mentor on this later when they are assigned -->

## BOM + Component Cost

<!-- Your Text Here. You may work with your mentor on this later when they are assigned -->

## Timeline

<!-- Your Text Here. You may work with your mentor on this later when they are assigned -->

## Useful Links

<!-- Your Text Here. You may work with your mentor on this later when they are assigned -->

## Log

<!-- Your Text Here. You may work with your mentor on this later when they are assigned -->
