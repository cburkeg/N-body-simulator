# N-body simulator

You can see this repo deployed as a [static site on GitHub Pages](https://cburkeg.github.io/N-body-simulator/index.html) - check it out!

This a JavaScript-based simulation that models gravitational interactions between multiple bodies in a 2D space. The simulation visualizes the movement of bodies over time, demonstrating the effects of gravitational forces in a simple and interactive manner.

I built this before Dev Academy had properly started, so the simulation is very crude and simplistic at the moment. There are no collisions between bodies at present, so the bodies tend to get arbitrarily close to one another before flying off at extreme angles due to very high forces. I will fix this at the first opportunity.

## Overview of Simulation

The simulation first undergoes an initial setup by:
- initialising body objects with default values for position, velocity, force, acceleration, radius, and mass; and
- randomising the initial positions of the bodies within a specified boundary of the canvas.

The main simulation loop works by:
- incrementing the step counter (to keep track of how much time has elapsed),
- checking if the simulation has reached the step limit to see if it should be concluded,
- updating the positions of the bodies based on their velocities,
- calculating the distances between all pairs of bodies,
- calculating the direction vectors from each body to every other body,
- calculating the gravitational forces between bodies based on their masses and distances,
- updating the accelerations of the bodies based on the forces acting on them,
- updating the velocities of the bodies based on their accelerations, and
- drawing the bodies on the canvas based on their updated positions.

## Known Issues

I plan to fix the following issues ASAP:
- The simulation does not include collisions, so bodies interact unphysically as their distance approaches 0.
- The position of the bodies on the canvas does not update smoothly with each tick of the simulation. 
