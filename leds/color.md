---
title: Day 1 - Color Control
nav_order: 1
parent: LEDs
layout: default
---

# Day 1: Color Control
{: .no_toc }

Learn how to control LED strip colors programmatically. Today you'll explore the relationship between code and visual output through colorful NeoPixel LEDs.

## Table of Contents
{: .no_toc .text-delta }

1. TOC
{:toc}

---

## Learning Objectives

By the end of this lesson, you will be able to:
- Control individual LED colors in a strip
- Understand RGB color values and mixing
- Create simple color patterns
- Use the MakeCode environment to program microcontrollers

| **Learning Focus** | **Skill Development** |
|:--|:--|
| **Concepts** | How to control LED strip colors |
| **Application** | Creating patterns with multiple colors |
| **Tools** | MakeCode programming environment |

---

## Color Theory Exploration

Before programming, explore how colors work in digital systems:

### Resources
- [HTML Color Picker](https://www.w3schools.com/colors/colors_picker.asp) - Find color codes visually
- [RGB Color Mixer](https://www.w3schools.com/colors/colors_rgb.asp) - Understand color mixing
- [Color Psychology](https://www.canva.com/colors/color-meanings/) - Colors and emotions

{: .note }
**Sprint Notes**: What's your favorite color? Find its RGB values (Red, Green, Blue numbers 0-255).

---

## Programming Walkthrough

### Setup Your Environment

1. Navigate to [makecode.microbit.org](https://makecode.microbit.org)
2. Sign in with your school Google account
3. Create a new project named `LED Color Control`

### Add NeoPixel Support

4. Add the NeoPixel extension:
   - Click the gear icon ⚙️ in the top right
   - Choose "Extensions"  
   - Search for and add "NeoPixel"

### Basic Color Control

5. Build this starter code in blocks:

```
on start
└─ set strip to NeoPixel at pin P0 with 10 leds as RGB
└─ set strip brightness 50
└─ show color Red
└─ show strip
```

6. Press `Download` and transfer to your micro:bit

### Individual LED Control

7. Now control individual LEDs. Update your code:

```
on start
└─ set strip to NeoPixel at pin P0 with 10 leds as RGB
└─ set strip brightness 50
└─ show color Red
└─ set pixel color at 4 to White
└─ show strip
```

8. Download and test again

{: .note }
**Documentation**: Take a picture of your LED strip showing red with one white LED. Save this for your assessment portfolio.

---

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
