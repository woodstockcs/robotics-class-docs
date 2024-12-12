---
title: Charge
nav_order: 2
parent: Sumo
layout: default
---

# Charge

<br><br>

## Purpose

<table>
  <tr>
    <th>Learning:</th>
    <td style="width:100%">how to program autonomous navigation</td>
  </tr>
  <tr>
    <th>Making Sumo:</th>
    <td style="width:100%">make robot detect and charge at opponents</td>
  </tr>
</table>
<br><br>

## Sandbox

Before we program our robot to chase things, let's explore how robots navigate in the real world. Find short clips online of these robots moving in their environments:

- Robot vacuum navigation
- Boston Dynamics robot
- Self-driving car

{: .note-title}

> Write in your sprint notes...
>
> what patterns you notice in how these robots navigate their environments.

<br><br>

## Walkthrough

1. Download the [SumoBot-Front-IR-Nav program](https://learn.parallax.com/sites/default/files/content/Sumo/ir/SumoBot-Front-IR-Nav.svg)
2. Open it in BlocklyProp Solo
3. If your IR sensors don't reach 8 when there's no object:
   - Right-click the IR Front Navigator block
   - Select "Expand Block"
   - Change the 7s to one less than your max reading
4. Load the program and test that your robot:
   - Still avoids ring borders
   - Turns toward objects it detects
   - Pushes detected objects

{: .note-title}

> Take a video...
>
> of your robot successfully detecting and charging at an object.

<br><br>

## Exercises

<!-- prettier-ignore-start -->
### Navigation Test
{: .d-inline-block}
Approaching
{: .label .label-green }

Place a paper cylinder 6 inches in front of your robot at these angles:
- Directly in front
- 45° to the left
- 45° to the right

{: .note-title}
> Write in your sprint notes...
>
> Record if the robot successfully detected and charged each time.

<br><br>

### Response Time
{: .d-inline-block}
Proficient
{: .label .label-blue }

Measure how long it takes your robot to:
1. Notice an object that suddenly appears 6 inches away at an angle
2. Begin turning toward it
3. Make contact with it

Try to optimize these times.

{: .note-title}
> Write in your sprint notes...
>
> what's something you did to improve the response time?

<br><br>

### Navigation Strategy
{: .d-inline-block}
Distinguished
{: .label .label-red }

Design and test on of these different navigation strategies:
1. Run away when opponent detected
2. Spiral search pattern
3. Random walk with occasional spins

Make sure you save your strategy in a place you can get it back!

{: .note-title}
> Write in your sprint notes...
>
> a name for your strategy

<!-- prettier-ignore-end -->
