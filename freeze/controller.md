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
1. Copy the code below, and paste it under `# Begin Project Code`
1. Download the code and take your robot for a test drive

```python
while True:
    left = controller.axis3.position()
    right = controller.axis2.position()

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

1. Try adding `* 0.5` after each `position()`
1. Download and test drive. Notice how it's different.
1. Update the code to look like below.

```python
# Begin Project Code

left_current = 0
right_current = 0
smoothing = 0.8

while True:
    left_target = controller.axis3.position() * 0.5
    right_target = controller.axis2.position() * 0.5

    left_current = left_current * smoothing + target_speed * (1-smoothing)
    right_current =

    # Set motor speeds using the smoothed values
    drivetrain.set_drive_velocity(left_current, right_current)
    wait(20)

```

1. Finish the `right_current = ` line.
1. Optionally, add this above the `wait(20)` command.

```python
    brain.screen.clear_screen()
    brain.screen.print("Left: {:.1f}".format(left_current))
    brain.screen.print("Right: {:.1f}".format(right_current))
```

1. Download and test drive

{: .important-title }

> Checkpoint Question
>
> Tinker with the `smoothing` value within the range 0.0 - 1.0. What does it do? (write your answer on your Daily Tracker)

<br>
<br>
<br>

## 4️⃣ Advanced Work

Add this just above `left_target = ...`

```python
    if controller.buttonR1.pressing():
        speed_mult = 1.0
    elif controller.buttonR2.pressing():
        speed_mult = 0.25
    else:
        speed_mult = 0.5
```

And add this just before setting the drive velocity:

```python
    left_current *= speed_mult
    right_current *= speed_mult
```

Download and test drive.

{: .important-title }

> Checkpoint Question
>
> Ask Smith to watch you drive and stamp your Daily Tracker.
