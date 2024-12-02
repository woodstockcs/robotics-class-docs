---
title: Wheels
nav_order: 1
parent: Roomba
layout: default
---

# Wheels

<br><br>

## Purpose

<table>
  <tr>
    <th>Learning:</th>
    <td style="width:100%">Control servo motors</td>
  </tr>
  <tr>
    <th>Roomba:</th>
    <td style="width:100%">Make wheels turn and stop</td>
  </tr>
</table>
<br><br>

## Sandbox

Try these things:

1. Set your robot plow-down on a table so wheels don't touch the ground ([shown here](https://learn.parallax.com/sites/default/files/content/Sumo/move/sumobot-face-down-on-table.png)).
1. Set the power switch to different positions (0, 1, 2).
1. Press and release the reset (RST) button ([shown here](https://learn.parallax.com/sites/default/files/content/Sumo/move/sumo-rst-button.png)). <mark>What do you notice so far?</mark>
1. Look at the back of the motors and find the "set screws" under the pieces of tape. ([shown here in yellow](https://learn.parallax.com/sites/default/files/content/Sumo/move/center-servos-sumobot-picture.png))
1. Press reset to get the wheels spinning. While they're spinning, <mark>what happens when you very gently turn these screws?</mark>

<br><br>

## Walkthrough

### Part 1: Getting Started

1. Open the [BlocklyProp Launcher](https://learn.parallax.com/print/book/export/html/2308).
2. Write your [First Program](https://learn.parallax.com/print/book/export/html/2309).
3. [Download your program to the robot](https://learn.parallax.com/print/book/export/html/2310).

### Part 2: Turning the Wheels

4. First, we need to make sure our wheels stay still when we tell them to. Follow the [Servo Centering Program](https://learn.parallax.com/print/book/export/html/2334) instructions to calibrate your wheels.

5. Once your wheels are centered, try the [Speed & Direction Program](https://learn.parallax.com/print/book/export/html/2337) to learn how to make your wheels move at different speeds and directions.

<br><br>

## Exercises

<!-- prettier-ignore-start -->
### 1. Dance Move
{: .d-inline-block}
Approaching
{: .label .label-green }

Make your robot do a "spin move":
- Spin clockwise for 1 second
- Stop for 1 second
- Spin counterclockwise for 1 second
- Stop for 1 second

Hint: To spin, make one wheel go forward and one backward at the same time.

### 2. Stop and Go
{: .d-inline-block}
Proficient
{: .label .label-blue }

Create a program that:
- Drives forward for 2 seconds
- Stops completely for 1 second
- Drives backward for 2 seconds
- Stops completely

Hint: To drive forward, set one wheel to a positive number, and the other to a negative number.

### 3. Speed Control
{: .d-inline-block}
Distinguished
{: .label .label-red }

Create a program that makes your robot drive forward:
- Start very slowly (speed 20)
- Speed up to medium speed (speed 50) after 2 seconds
- Speed up to fast (speed 100) after another 2 seconds
- Stop

<!-- prettier-ignore-end -->
