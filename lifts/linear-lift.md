---
title: Linear Lift Mechanism
nav_order: 1
parent: Mechanical Systems
layout: default
---

# Linear Lift Mechanism
{: .no_toc }

Learn to build and control linear lift mechanisms. Linear lifts use a straight-line motion to raise and lower loads, making them ideal for simple lifting applications.

## Table of Contents
{: .no_toc .text-delta }

1. TOC
{:toc}

---

## Learning Objectives

By the end of this lesson, you will be able to:
- Understand the principles of linear motion systems
- Build a functional linear lift mechanism
- Calculate mechanical advantage in linear systems
- Program motor control for precise positioning

---

## Mechanism Overview

### How Linear Lifts Work

Linear lifts convert rotational motion (from motors) into straight-line motion using:
- **Lead screws**: Threaded rods that convert rotation to linear motion
- **Rack and pinion**: Gear systems that move loads in straight lines
- **Belt and pulley**: Flexible systems for smooth vertical movement
- **Hydraulic/pneumatic**: Fluid-powered linear actuators

### Applications in Robotics

- **Elevator systems**: Raising robots to different levels
- **Lifting mechanisms**: Picking up and placing objects
- **Camera mounts**: Adjusting sensor height
- **Tool positioning**: Precise linear movement of end effectors

---

## Build Instructions

### Interactive Assembly Guide

<iframe allowfullscreen="allowfullscreen" height="480" src="https://instructions.online/?id=4063-vex-exp-linear-lift" title="Linear Lifts" width="640"></iframe>

### Key Components

1. **Base structure**: Provides stable foundation
2. **Linear guide**: Ensures straight motion without binding
3. **Drive mechanism**: Motor and transmission system
4. **Load platform**: Carries the objects being lifted
5. **Limit switches**: Detect top and bottom positions

---

## Programming Control

### Basic Motor Control

```c
// Pseudocode for linear lift control
void moveUp(int distance) {
    motor.start(UP_DIRECTION);
    delay(calculateTime(distance));
    motor.stop();
}

void moveDown(int distance) {
    motor.start(DOWN_DIRECTION);
    delay(calculateTime(distance));
    motor.stop();
}
```

### Position Feedback

For precise control, add sensors to track position:
- **Encoders**: Count motor rotations
- **Potentiometers**: Measure linear position
- **Limit switches**: Detect end positions

---

## Mechanical Advantage

### Calculating Advantage

Linear lifts can multiply force at the cost of speed:

```
Mechanical Advantage = Input Distance / Output Distance
```

For a lead screw with 4 threads per inch:
- 1 motor revolution = 1/4 inch of lift
- MA = 4:1 (4x force multiplication)

---

## Design Challenges

### Exercise 1: Load Testing
Build your linear lift and test with different weights:
1. Start with light objects (100g)
2. Gradually increase load
3. Find the maximum lifting capacity
4. Record the relationship between load and speed

### Exercise 2: Precision Control
Program precise positioning:
1. Move to exact heights (2", 4", 6")
2. Hold position for 5 seconds
3. Return to starting position
4. Measure accuracy (within ±0.1")

---

## Troubleshooting

### Common Issues

| Problem | Possible Cause | Solution |
|:--|:--|:--|
| Jerky movement | Binding in guide | Check alignment, lubricate |
| Motor stalls | Load too heavy | Reduce weight or add gearing |
| Inconsistent position | Backlash in drive | Adjust tension, add preload |
| Slow movement | Insufficient power | Check battery, motor voltage |

---

## Reference Resources

### Construction Video
[Linear Lift Construction Guide](https://www.youtube.com/watch?v=GwvHStrcXWU&list=PLYZlZ-HVwqm4-iTDcZ4YVJ340yVCvwmbU&index=2) 

{: .note }
**Note**: This video uses slightly different robot parts than we have in class, so adapt the design to match our available components.

### Next Steps
- [Scissor Lift](scissor-lift) - More complex lifting mechanism
- [Telescoping Lift](telescoping-lift) - Compact extending design
