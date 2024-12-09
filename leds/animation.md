---
title: Animation
nav_order: 2
parent: LEDs
layout: default
---

# Animation

<br><br>

# Purpose

Today you will learn the code behind LED light shows with multiple colors and movement.

<br><br>

# Sandbox

Let's refresh what we did last time. Build this code:

```
on start
└─ set strip to NeoPixel at pin P0 with 10 leds as RGB
└─ set strip brightness 50
└─ show color Red
└─ set pixel color at 4 to White
└─ show strip
```

Update the code with more Set Pixel Color At... blocks to make every pixel light up a different color

{: .note-title}

> Write in your sprint notes...
>
> What you notice about the number in Set Pixel Color At \_\_\_.

<br><br>

# Walkthrough

1. Open a new project called `LED Patterns`
2. Add the NeoPixel extension
3. Build this code that makes the LEDs change color every second:

```
on start
└─ set strip to NeoPixel at pin P0 with 10 leds as RGB

forever
└─ show color Red
└─ show strip
└─ pause (ms) 1000
└─ show color Blue
└─ show strip
└─ pause (ms) 1000
```

1.  Download and test it on your LED strip.

{: .note-title}

> Take a picture...
>
> of your code.
>
> **Note**: Hang on to this picture. You'll use this again soon in the assessment.

<br><br>

# Exercises

<!-- prettier-ignore-start -->

### Color Timer
{: .d-inline-block}
Approaching
{: .label .label-green }

Create a program that:
1. Shows green for 3 seconds
2. Changes to yellow for 2 seconds
3. Finally changes to red for 1 second
4. Repeats forever

{: .note-title}
> Write in your sprint notes...
>
> How many pause blocks did you use?

<br><br>

### Moving Light
{: .d-inline-block}
Proficient
{: .label .label-blue }

Create a single white light that moves down your strip:
1. Start at position 0
2. Move one position every half second
3. When it reaches the end, start over at position 0

Hint: Use the "set pixel color" and "clear" blocks

{: .note-title}
> Write in your sprint notes...
>
> What happens if you don't clear the strip each time?

<br><br>

### Rainbow Wave
{: .d-inline-block}
Distinguished
{: .label .label-red }

Create a moving rainbow pattern:
1. Use the "show rainbow" block
2. Make it move using the "rotate pixels" block
3. Experiment with different rotation speeds and pause times

Hint: Look at the example code in the NeoPixel extension blocks

{: .note-title}
> Write in your sprint notes...
>
> What rotation and pause values gave you the smoothest animation?

<br><br>

<!-- prettier-ignore-end -->
