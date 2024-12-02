---
title: Distance Sensors
nav_order: 1
parent: Sumo
layout: default
---

# Distance Sensors

<br><br>

## Purpose

<table>
  <tr>
    <th>Learning:</th>
    <td style="width:100%">Read values from IR distance sensors</td>
  </tr>
  <tr>
    <th>Robot:</th>
    <td style="width:100%">Detect objects at different distances</td>
  </tr>
</table>
<br><br>

## Walkthrough

1. Install the IR sensors following the [IR LED installation guide](https://learn.parallax.com/tutorials/robot/sumobot-wx/ir-sumobot-wx-opponent-detection-and-tracking/install-front-ir-leds-and) up to the part that says "Installation"
2. Download and run the test program from the [IR testing guide](https://learn.parallax.com/tutorials/robot/sumobot-wx/ir-sumobot-wx-opponent-detection-and-tracking/terminal-ir-distance)
3. Use a white piece of paper to verify the sensors read:
   - 8 when no object is detected
   - 0-2 for very close objects

<br><br>

## Sandbox

2. Move the paper closer and farther while watching the terminal numbers
3. Try different materials (white paper, black paper, shiny metal, a human hand?)
4. Find the maximum distance your sensor can detect each material

<br><br>

## Exercises

<!-- prettier-ignore-start -->
### 1. Distance Chart
{: .d-inline-block}
Approaching
{: .label .label-green }

Create a simple chart showing what sensor values (0-8) you get at these distances:
- 1 inch
- 6 inches
- 12 inches
- 24 inches

Make the chart for two different materials.

### 2. Sweet Spot
{: .d-inline-block}
Proficient
{: .label .label-blue }

Find the "sweet spot" distance where your SumoBot can reliably detect another SumoBot.

### 3. Sensor Optimization
{: .d-inline-block}
Distinguished
{: .label .label-red }

Experiment with different IR LED angles and positions to maximize detection:
1. Test 3 different LED angles (pointing straight, angled up, angled out)
3. Recommend the optimal LED positioning for a sumo match
4. Explain the tradeoffs between different positions

<!-- prettier-ignore-end -->
