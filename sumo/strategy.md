---
title: Strategy
nav_order: 3
parent: Sumo
layout: default
---

# Strategy

<br><br>

## Purpose

<table>
  <tr>
    <th>Learning:</th>
    <td style="width:100%">how robot code makes decisions</td>
  </tr>
  <tr>
    <th>Making Sumo:</th>
    <td style="width:100%">improve robot's behavior</td>
  </tr>
</table>
<br><br>

## Sandbox

Skip around a couple minutes of these videos from Sumo competitions:
- [Cooper Union](https://www.youtube.com/watch?v=QCqxOzKNFks)
- [Pro](https://www.youtube.com/watch?v=mS-L2fpV1Is)

{: .note-title}

> Write in your sprint notes...
>
> what successful strategies did you notice?

<br><br>

## Walkthrough

1. Open your IR navigation program from yesterday
2. Right-click the "IR Front Navigator" block 
3. Select "Expand Block"
4. Look at the if/else statements:
   - Both sensors see opponent → charge forward
   - Left sensor only → turn left
   - Right sensor only → turn right
   - No detection → move forward

{: .note-title}

> Check the box in your sprint notes when you've done the steps above.

<br><br>

## Exercises

<!-- prettier-ignore-start -->
### Detection Distance
{: .d-inline-block}
Approaching
{: .label .label-green }

Change when your robot reacts to opponents:
1. Find the number 7 in your code
2. Try changing it to 5
3. Test if this works better or worse

{: .note-title}

> Write in your sprint notes...
>
> what number worked best for your robot.

<br><br>

### Turn Speed
{: .d-inline-block}
Proficient
{: .label .label-blue }

Adjust how fast your robot turns:
1. Find the servo speed numbers in the code
2. Try different speeds between -100 and 100
3. Test which speeds work best

{: .note-title}

> Write in your sprint notes...
>
> what speeds you chose.

<br><br>

### Search Mode
{: .d-inline-block}
Distinguished
{: .label .label-red }

Make your robot search when it can't find anything:
1. Find the else section (when no opponent is seen)
2. Instead of going straight, make it:
   - Spin in place, or
   - Drive in a circle

{: .note-title}

> Take a video...
>
> of your robot's new search behavior.

<!-- prettier-ignore-end -->
