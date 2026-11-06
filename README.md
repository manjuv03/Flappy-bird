# Flappy Bird

**An Arcade Game in Python with Pygame**

## Overview

A remake of Flappy Bird. The bird moves forward on its own, and the player taps **Space** to flap and fly through the gaps between pipes. The game covers the basics of 2D game programming: a game loop, gravity, sprite animation, collision detection, scoring and sound.

## Repository layout

| Path | Content |
| --- | --- |
| `main.py` | The whole game |
| `resources/images/` | Background, floor, pipe, three bird frames and the start screen |
| `resources/sounds/` | Flap, hit, point, die and swoosh sound effects |
| `resources/fonts/` | The 04B_19 pixel font |

## How to run

1. Install Python 3.9 or later and Pygame: `pip install pygame`
2. From the repository folder, run `python main.py`

On macOS or Linux, file names are case-sensitive: rename `resources/fonts/04B_19.TTF` to `04B_19.ttf`, or change the two font paths in `main.py` to match.

## Controls

| Key | Action |
| --- | --- |
| Space | Flap; after a game over, start again |
| Esc | Quit |

## How it works

| Part | Content |
| --- | --- |
| Window | 480 × 640 pixels at 60 frames per second |
| Physics | Gravity adds 0.25 to the bird's speed every frame; a flap sets it to −10 |
| Pipes | A new pair every 1.2 seconds at one of 5 heights, with a 300-pixel gap, moving left 5 pixels per frame |
| Animation | The bird cycles through 3 wing frames every 200 ms and tilts with its speed |
| Collision | The game ends if the bird hits a pipe, the floor or flies too high |
| Score | Rises with time survived; the high score is kept until you quit |
