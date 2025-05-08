# HP Prime Projectile Motion Solver

This is a simple projectile motion calculator written in HP PPL for the HP Prime calculator, originally created by me in high school physics class.

## Features

- User input for:
  - Initial velocity (m/s)
  - Launch angle (degrees)
  - Launch height & final height (m)
  - Gravitational acceleration
- Calculates:
  - Time of flight
  - Final X position
- Outputs results in a friendly MSGBOX format

## File

- `Projectile Motion.hpprgm` – Source code file compatible with the HP Prime calculator.
- `Projectile_Motion.md` - Text version of the code because github doesnt preview hpprgm files!

## How it Works

Uses standard kinematic equations assuming no air resistance. Solves a quadratic equation to calculate time of flight and uses that to compute horizontal distance traveled.
