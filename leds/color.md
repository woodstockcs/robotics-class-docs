---
title: Colors
nav_order: 1
parent: LEDs
layout: default
---

# Colors

<br><br>

# Purpose

<table>
<tr>
<th>Learning:</th>
<td style="width:100%">how to control LED strip colors</td>
</tr>
<tr>
<th>Making:</th>
<td style="width:100%">light patterns with multiple colors</td>
</tr>
</table>

<br><br>

# Sandbox

You have a strip of 10 special LEDs called NeoPixels. Each one can be any color you want!

Take a few minutes to explore colors:

- [HTML Color Picker](https://www.w3schools.com/colors/colors_picker.asp)
- [RGB Color Mixer](https://www.w3schools.com/colors/colors_rgb.asp)
- [Color Psychology](https://www.canva.com/colors/color-meanings/)

{: .note-title}

> Write in your sprint notes...
>
> What's your favorite color? Find its RGB values.

<br><br>

# Walkthrough

1.  Go to [makecode.microbit.org](https://makecode.microbit.org).
1.  Sign in with your school google account.
1.  Create a new project named `LED starter`.
1.  Add the NeoPixel extension:
    - Click the gear icon ⚙️ in the top right
    - Choose "Extensions"
    - Search for and add "NeoPixel"
1.  Build this starter code in blocks.

    ```
        on start
        └─ set strip to NeoPixel at pin P0 with 10 leds as RGB
        └─ set strip brightness 50
        └─ show color Red
        └─ show strip
    ```

1.  Press the `Download` button and follow the instructions.
1.  Now let's change one light. Update your code so it looks like this:

    ```
        on start
        └─ set strip to NeoPixel at pin P0 with 10 leds as RGB
        └─ set strip brightness 50
        └─ show color Red
        └─ set pixel color at 4 to White
        └─ show strip
    ```

1.  Download again.

{: .note-title}

> Take a picture...
>
> of your LED strip glowing red with one white LED, then check the box in your sprint notes.

<br><br>

# Exercises

<!-- prettier-ignore-start -->

### Three Colors
{: .d-inline-block}
Approaching
{: .label .label-green }

1. Click the Home button, then create a new project called `Three Colors`.
1. Make your strip show these colors in order:
   - First 2 LEDs: Red
   - Next 3 LEDs: Green  
   - Rest of the LEDs: Blue

Optional: try it with the `range` block.

{: .note-title}
> Write in your sprint notes...
>
> What block did you use to set different sections of LEDs?

<br><br>

### Custom Colors
{: .d-inline-block}
Proficient
{: .label .label-blue }

1. Click the Home button, then create a new project called `Custom Colors`.
1. Create an alternating pattern using 2 different custom RGB colors (not the built-in color options). 

Hint: in `... more`, use the `red...green...blue...` block.

{: .note-title}
> Write in your sprint notes...
>
> What RGB values did you use?

<br><br>

### Color Story
{: .d-inline-block}
Distinguished
{: .label .label-red }

1. Click the Home button, then create a new project called `Color Story`.
1. Create a light pattern that tells a simple story or represents an emotion using at least 4 different colors. Examples:
    - Sunset colors fading from yellow to orange to red to purple
    - Holiday theme with red and green alternating
    - Ocean depths going from light to dark blue

Hint: Maybe use this [color mixer](https://www.w3schools.com/colors/colors_mixer.asp)?

{: .note-title}
> Write in your sprint notes...
>
> What story/emotion did you choose?

<br><br>

<!-- prettier-ignore-end -->
