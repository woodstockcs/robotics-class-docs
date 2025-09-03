---
title: Day 1 - Robot Controller
layout: default
nav_order: 1
parent: Freeze Tag Challenge
---

# Day 1: Robot Controller Programming
{: .no_toc }

Learn to control your robot using a wireless controller. Today you'll implement tank-style driving with smooth movement and variable speed control.

## Table of Contents
{: .no_toc .text-delta }

1. TOC
{:toc}

---

## Learning Objectives

By the end of this lesson, you will be able to:
- Implement tank-style robot control
- Program smooth movement using interpolation
- Add variable speed controls
- Understand real-time control systems

---

## Setup Your Development Environment

### Hardware Preparation
1. Get your controller and robot brain
2. Turn both devices on
3. Connect controller to brain (wait for connection indicator)

### Software Setup
4. Navigate to [codeexp.vex.com](https://codeexp.vex.com)
5. Click **File > New Text Project > Python > EXP Brain**
6. Connect the brain (wait for the green brain icon)

---

## Understanding Tank Drive

{: .important }
**Think About This**: Imagine a tank driving forward. It doesn't have a steering system like a car. How does it turn left? 

*Write your answer in your daily tracker before continuing.*

### Tank Drive Principles
- **Left stick** controls left side motors
- **Right stick** controls right side motors  
- **Forward motion**: Both sticks forward
- **Turning**: One side faster than the other
- **Pivot turning**: One side forward, one backward

---

## Basic Tank Drive Implementation

### Step 1: Basic Controller Input

1. In VEX Code, add a **Controller** device
2. Copy this code under `# Begin Project Code`:

```python
while True:
    left = controller.axis3.position()
    right = controller.axis2.position()

    drivetrain.set_drive_velocity(left, right)
    wait(20)
```

3. Download and test your robot

{: .important }
**Checkpoint**: Have your instructor watch you drive and get approval in your daily tracker.

---

## Adding Speed Control

### Step 2: Reduce Maximum Speed

1. Modify your code to reduce speed by adding `* 0.5`:

```python
while True:
    left = controller.axis3.position() * 0.5
    right = controller.axis2.position() * 0.5

    drivetrain.set_drive_velocity(left, right)
    wait(20)
```

2. Download and test - notice how the reduced speed affects control

---

## Smooth Movement Control

### Step 3: Implement Movement Smoothing

Sudden speed changes can make robots hard to control. Let's add smoothing:

```python
# Begin Project Code

left_current = 0
right_current = 0
smoothing = 0.8

while True:
    left_target = controller.axis3.position() * 0.5
    right_target = controller.axis2.position() * 0.5

    left_current = left_current * smoothing + left_target * (1-smoothing)
    right_current = right_current * smoothing + right_target * (1-smoothing)

    # Set motor speeds using the smoothed values
    drivetrain.set_drive_velocity(left_current, right_current)
    wait(20)
```

{: .note }
**Your Task**: Complete the `right_current` calculation line following the pattern from `left_current`.

### Optional: Add Debug Display

Add this code above `wait(20)` to see the smoothed values:

```python
    brain.screen.clear_screen()
    brain.screen.print("Left: {:.1f}".format(left_current))
    brain.screen.print("Right: {:.1f}".format(right_current))
```

{: .important }
**Experiment**: Try different `smoothing` values between 0.0 and 1.0. What effect does this have on robot control? Record your observations.

---

## Variable Speed System

### Step 4: Multi-Speed Control

Add speed selection using controller buttons:

```python
# Add this above left_target = ...
if controller.buttonR1.pressing():
    speed_mult = 1.0      # Fast speed
elif controller.buttonR2.pressing():
    speed_mult = 0.25     # Slow speed  
else:
    speed_mult = 0.5      # Normal speed
```

```python
# Add this before setting drive velocity
left_current *= speed_mult
right_current *= speed_mult
```

### Complete Control Scheme

| Control | Function |
|:--|:--|
| **Left Stick** | Left side motors |
| **Right Stick** | Right side motors |
| **R1 Button** | Fast speed (100%) |
| **R2 Button** | Slow speed (25%) |
| **Default** | Normal speed (50%) |

{: .important }
**Final Checkpoint**: Demonstrate all three speed modes to your instructor for approval.

---

## Understanding the Code

### Key Programming Concepts

1. **Real-time Loop**: The `while True` loop runs continuously
2. **Interpolation**: Smoothing creates gradual transitions
3. **State Management**: Variables track current vs. target values
4. **Input Processing**: Controller values become motor commands

### Performance Considerations

- **Update Rate**: `wait(20)` means 50 updates per second
- **Smoothing Factor**: Higher values = more smoothing, slower response
- **Speed Multipliers**: Allow fine control for different situations

---

## Next Steps

This foundational control system will be essential for:
- **Autonomous navigation** - Converting sensor input to movement
- **Competition strategy** - Precise maneuvering in tight spaces
- **Advanced behaviors** - Building complex robot actions

Tomorrow we'll add autonomous features to make your robot play freeze tag independently!
