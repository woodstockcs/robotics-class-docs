---
title: Distance Sensors
nav_order: 1
parent: Sumo
layout: default
---

# Distance Sensors

<br><br>

# Purpose

<table>
  <tr>
    <th>Learning:</th>
    <td style="width:100%">how to read values from IR distance sensors</td>
  </tr>
  <tr>
    <th>Making Sumo:</th>
    <td style="width:100%">install sensors to detect other robots</td>
  </tr>
</table>
<br><br>

# Sandbox

Today you will install infrared light ("IR") sensors on your robot.

Explore IR a bit online. Browse these links.

- [robonyx short](https://www.youtube.com/shorts/epcZA5XsS20)
- [off-road vehicles](https://www.superbrightleds.com/blog/how-do-led-infrared-lights-work.html)
- [parts you'll install in your robot](https://learn.parallax.com/sites/default/files/content/Sumo/ir/ir-parts-front.png)
- [diagram of IR in your robot](https://learn.parallax.com/sites/default/files/content/Sumo/ir/ir-led-reflection-beams-falloff-explanation.png)

{: .note-title}

> Write in your sprint notes...
>
> a few things you notice or wonder about IR.

<br><br>

# Walkthrough

1. Install the IR sensors following the [IR LED installation guide](https://learn.parallax.com/tutorials/robot/sumobot-wx/ir-sumobot-wx-opponent-detection-and-tracking/install-front-ir-leds-and).
2. Download and run the test program from the [IR testing guide](https://learn.parallax.com/tutorials/robot/sumobot-wx/ir-sumobot-wx-opponent-detection-and-tracking/terminal-ir-distance). Make use of the Troubleshooting section at the bottom of that page.
3. Grab a white piece of paper and move it closer and farther while watching the terminal numbers. Verify the sensors read:
   - 8 when no object is detected
   - 0-2 for very close objects

{: .note-title}

> Take a picture...
>
> of the installed sensors, then check the box in your sprint notes.
>
> **Note**: Hang on to this picture. You'll use this again soon in the assessment.

<br><br>

# Exercises

<!-- prettier-ignore-start -->
### Distance Chart
{: .d-inline-block}
Approaching
{: .label .label-green }

What sensor values (0-8) do you get at these distances:
- 1 inch
- 6 inches
- 12 inches
- 24 inches

{: .note-title}

> Write in your sprint notes...
>
> those 4 sensor values.

<br><br>

### Reliable Detection
{: .d-inline-block}
Proficient
{: .label .label-blue }

Grab another SumoBot and find the maximum distance where your SumoBot can _reliably_ detect it.

{: .note-title}

> Write in your sprint notes...
>
> how many inches away that is.

<br><br>

### Sensor Optimization
{: .d-inline-block}
Distinguished
{: .label .label-red }

Experiment with different IR LED angles and positions to maximize detection:
1. Test 3 different LED angles (pointing straight, angled up, angled out)
1. Determine the optimal LED positioning for a sumo match

{: .note-title}

> Write in your sprint notes...
>
> What did you determine, and why is that optimal?

<br><br>

<!-- prettier-ignore-end -->
