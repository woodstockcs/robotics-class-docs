---
title: Controller
layout: home
nav_order: 1
parent: Freeze Tag
---

# Controller

## 1️⃣ Get started

1. Get your a controller and a brain
1. Turn them both on
1. Connect controller to brain
1. Go to [codeexp.vex.com](codeexp.vex.com)
1. Click File > New Text Project > Python > EXP Brain.
1. Connect the brain (wait for the green brain icon)

{: .important-title }

> Checkpoint Question
>
> Imagine a tank driving forward. It doesn't have a steering system like a car. How does it turn left? (write your answer on your Daily Tracker)

<br>
<br>
<br>
## 2️⃣ Basic Task

1. In VEX Code, add a Controller device.
1. Put this code under `# Begin Project Code`
1. Update the code to look like below.
1. Download the code and take your robot for a test drive

```python
while True:
    # Get joystick positions (-100 to 100)
    left = controller.axis3.position()
    right = controller.axis2.position()

    # Set motor speeds
    drivetrain.set_drive_velocity(left, right)
    wait(20)
```

{: .important-title }

> Checkpoint Question
>
> Ask Smith to watch you drive and stamp your Daily Tracker.

<br>
<br>
<br>

## 3️⃣ Main Challenge

1. Set base speed to 50% by adding `* 0.5` after each `position()`
1. Download and test drive. Notice how it's different.
1. Update the code to look like below.
1. Download and test drive.

```python
# Variables for tracking current speeds (put outside loop)
left_current = 0
right_current = 0

# How smooth the acceleration is
smoothing = 0.8

while True:
    # Get joystick positions and apply 50% speed limit
    left_target = controller.axis3.position() * 0.5
    right_target = controller.axis2.position() * 0.5

    # Smooth acceleration formula:
    # new_speed = current_speed * smoothing + target_speed * (1-smoothing)
    left_current = left_current * smoothing + left_target * (1-smoothing)
    right_current = right_current * smoothing + right_target * (1-smoothing)

    # Set motor speeds using the smoothed values
    drivetrain.set_drive_velocity(left_current, right_current)

    # Optional: Display current speeds on brain
    brain.screen.clear_screen()
    brain.screen.print("Left: {:.1f}".format(left_current))
    brain.screen.print("Right: {:.1f}".format(right_current))

    wait(20)

```

{: .important-title }

> Checkpoint Question
>
> Tinker with the `smoothing` value within the range 0.0 - 1.0. What does it do? (write your answer on your Daily Tracker)

<br>
<br>
<br>

## 4️⃣ Advanced Work

Make these updates. Download and test drive. Try to figure out what it does.

```
    # Add this at the top of the loop (inside)
    if controller.buttonR1.pressing():
        speed_mult = 1.0
    elif controller.buttonR2.pressing():
        speed_mult = 0.25
    else:
        speed_mult = 0.5

    ...
    # Add this before setting the drive velocity
    left_current *= speed_mult
    right_current *= speed_mult

```

{: .important-title }

> Checkpoint Question
>
> Ask Smith to watch you drive and stamp your Daily Tracker.
