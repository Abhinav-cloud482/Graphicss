# Graphics

## Description
The script uses turtle graphics to draw a continuous spiral with vibrant colors. It utilizes the HSV color space (via colorsys) to smoothly transition colors as the turtle draws. The pattern consists of overlapping circular arcs creating a mesmerizing hypnotic effect.

## Getting Started

Prerequisites

- Python 3.x installed on your system.

- No external dependencies required — uses only built-in Python modules (turtle, colorsys).

Running the Script

- Clone the repository or copy the code.

 - Run the script :

python turtle_spiral.py

The turtle window will open, and the drawing will begin automatically.

## Code Overview

import turtle
import colorsys

t = turtle.Turtle()
s = turtle.Screen().bgcolor('black')
t.speed(0)

n = 70      # Number of distinct colors
h = 0       # Initial hue

for i in range(360):
    c = colorsys.hsv_to_rgb(h, 1, 0.8)
    h += 1/n
    t.color(c)
    t.left(1)
    t.forward(1)
    for j in range(2):
        t.left(2)
        t.circle(100)

colorsys.hsv_to_rgb() is used to generate a smooth rainbow gradient.

The turtle draws slight left turns and circular arcs repeatedly to create a spiral.

## Example Output

![Graphics](https://github.com/user-attachments/assets/74cfbf2e-6fa2-4824-9231-1eca82c48b04)

## License
This project is open-source and free to use under the MIT License.

## Inspiration
Inspired by generative art and the power of simple loops and color theory to create complex visuals.

