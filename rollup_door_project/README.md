# Rollup Door PLC Project

## Overview

This project simulates an industrial rollup door control system using ladder logic programmed in Allen-Bradley RSLogix Micro Starter Lite.

The system allows an operator to open and close a rollup door using pushbuttons while incorporating proper interlocking and safety behavior to prevent conflicting outputs.

This project was completed as part of the PLC Training Academy course:

> "The Complete PLC Programming Course - 10 Day PLC Programmer" by Robert Simons

---

## Objectives

The purpose of this project was to learn:

* Ladder logic fundamentals
* Seal-in (latching) circuits
* Motor control logic
* Normally Open (NO) and Normally Closed (NC) instructions
* PLC troubleshooting and scan-cycle behavior
* Real-world industrial control structure

---

## System Description

The rollup door operates in two directions:

* OPEN direction
* CLOSE direction

The PLC monitors pushbutton inputs and energizes the correct output while preventing both outputs from turning on simultaneously.

The system includes:

* Open pushbutton
* Close pushbutton
* Stop behavior
* Interlocking logic
* Seal-in circuits to maintain operation after button release

---

## Inputs and Outputs

| Address | Description             |
| ------- | ----------------------- |
| I:0/0   | Open Pushbutton         |
| I:0/1   | Close Pushbutton        |
| I:0/2   | Stop Pushbutton         |
| O:0/0   | Door Open Motor Output  |
| O:0/1   | Door Close Motor Output |

---

## PLC Concepts Used

### Seal-In Circuits

Seal-in logic was used so the motor output remains energized after the operator releases the pushbutton.

### Interlocking

Interlocking logic prevents the OPEN and CLOSE outputs from energizing at the same time.

### Normally Open / Normally Closed Instructions

Both NO and NC instructions were used to create safe and reliable control behavior.

### Ladder Logic Troubleshooting

The project required testing rung conditions and verifying correct scan-cycle operation during simulation.

---

## Program Behavior

### Opening Sequence

1. Operator presses OPEN pushbutton
2. OPEN output energizes
3. Seal-in circuit maintains output
4. Door continues opening until stopped

### Closing Sequence

1. Operator presses CLOSE pushbutton
2. CLOSE output energizes
3. Seal-in circuit maintains output
4. Door continues closing until stopped

### Safety Logic

* OPEN and CLOSE outputs cannot energize simultaneously
* Stop command removes motor output
* Interlocking prevents conflicting motion commands

---

## Software Used

* Allen-Bradley RSLogix Micro Starter Lite
* RSLinx Classic
* RSLogix Emulate 500

---

## Files Included

* `RollupDoor.RSS` → RSLogix ladder logic project
* `/screenshots` → Program screenshots and simulation images

---

## Skills Demonstrated

* PLC programming fundamentals
* Ladder diagram development
* Industrial motor control logic
* PLC troubleshooting
* Program documentation
* Commented rung organization
* Boolean logic implementation

---

## What I Learned

This project helped reinforce the relationship between relay logic and PLC ladder diagrams. I gained practical experience designing seal-in circuits, implementing motor interlocks, and debugging ladder logic behavior using RSLogix simulation tools.

I also improved my understanding of how PLC scan cycles affect program execution and output behavior.

---

## Future Improvements

Potential future improvements include:

* Adding limit switches for automatic stop positions
* Adding timers for motion delays
* Implementing fault/alarm conditions
* Integrating HMI controls
* Adding safety sensors

---

## Screenshots

Add screenshots here.

Example:

```md
![Main Ladder Logic](roolup_door.png)
```

---

## Author

Computer Science student transitioning into Controls Engineering and Industrial Automation.

Focus areas:

* PLC Programming
* Industrial Automation
* Allen-Bradley Systems
* Ladder Logic
* HMI Development
