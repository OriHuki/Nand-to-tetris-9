# Super Basketball (NBA Challenge)

A dynamic basketball arcade game implemented in **Jack language** for the **Nand2Tetris** course (Project 9).

## About The Game

**Super Basketball** is a skill-based arcade game where the player steps into the shoes of an NBA player for one day. You have 60 seconds to score as many points as possible from random positions on the court. The game features a custom physics engine, accurate scoring zones, and a shooting mechanic that requires precision and timing.

## How to Play

### Controls

- **Arrow Keys (Left/Right)**: Move the player/ball across the court
- **Space (First Press)**: Lock your position on the court
- **Space (Second Press)**: Lock the power meter and take the shot

### Objective

You have **60 seconds** on the clock.
1. The ball appears at a random position.
2. Move to your preferred spot.
3. Time your shot power correctly using the moving bar.
4. Score!

### Scoring System

The game calculates points based on distance from the basket:
- **3 Points**: Long-range shots (Left side of the court)
- **2 Points**: Mid-range shots
- **1 Point**: Layups/Close shots (Near the basket)

## Features

- **Physics Engine**: Implements gravity, velocity, and realistic ball trajectory.
- **Collision System**:
    - Ball bounces off the floor and walls.
    - **Solid Backboard**: The ball interacts realistically with the backboard (cannot pass through it from behind).
- **Smart Scoring**: Uses a "Swish" algorithm to detect if the ball passes *down* through the hoop.
- **Clean UI**: Minimalist court design focused on gameplay, with a dynamic HUD showing Score, Time, and Shot Value.

## Project Structure

| File | Description |
|------|-------------|
| `Main.jack` | Entry point. Initializes and runs the game instance. |
| `BasketGame.jack` | **Game Manager**: Handles the game loop, UI (HUD), state machine (Position -> Power -> Shoot), and background rendering. |
| `Ball.jack` | **Physics Engine**: Handles movement, gravity, collision detection (walls, floor, backboard), and drawing/erasing the ball. |

## Building and Running

This project is designed for the **Nand2Tetris** software suite:

1. Compile the directory containing the `.jack` files using the **Jack Compiler**
2. Open the **VM Emulator**
3. Load the compiled folder
4. Set "Animate" to **No Animation** (for best performance) or Fast
5. Run the program

## Technical Notes

- **Resolution**: 512x256 pixels (Standard Hack platform)
- **RNG**: Implements a Linear Congruential Generator (LCG) for random ball placement, seeded by user input time.
- **Graphics**: Uses optimized drawing methods to prevent flickering (manual double-buffering logic).

## Author

**Created by:** Ori Hukima, Liel Uzan, Tzipora Feuchtwanger
Developed as part of the Nand2Tetris course (Project 9).