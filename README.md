## ibmethod2d 
---
### A MATLAB-based 2D Immersed Boundary Navier-Stokes fluid solver.

This package provides MATLAB files that implement the Cartesian grid
Immersed Boundary (IB) method of C. S. Peskin, as described in "_The
Immersed Boundary Method_", Acta Numerica 11:479-517, 2002.  The
solver assumes periodic boundary conditions on a square domain.

Note, the solver does not handle wrapping of IB structures across
periodic boundaries. In any simulations you must make sure that the
immersed structure stays away from the domain boundaries.

Please notify the author of any bugs, and contribute any improvements
or bug fixes back to the original author.

**License:** MIT Expat License. This code is free to use for any
purposes, provided any publications resulting from the use of this
code reference the original code/author.

**Author:**  Samuel Isaacson (isaacson@math.bu.edu)

**Disclaimer:**
This code is provided as is. The author takes no responsibility for
its results or effects.

**Files:**
* ibDriver.m
 + Defines simulation paramters.
 + Implements the overall IB method.
* fluidDriver.m 
 + Defines simulation parameters when running just the NS solver.
 + Runs just the fluid solver (no IBs).
* fluidSolver.m
 + Solves the Navier-Stokes equations with periodic boundary
conditions on a square Cartesian grid.
* D02DPeriodic.m
 + Cartesian grid centered difference operator.
* D02DPeriodicFT.m
 + Discrete Fourier Transform of centered difference operator.
* lap2DPeriodic.m
 + Cartesian grid discrete Laplacian.
* lap2DPeriodicFT.m
 + Discrete Fourier Transform of the discrete Laplacian.
* advanceBoundary.m
 + Advects the IB with the local fluid velocity.
* calcLagrangianForce.m
 + Calculates the elastic force at each Lagrangian point.
* spreadForce.m
 + Spreads forces from Lagrangian points to Eulerian points.
* evalDelta.m
 + Evaluates the discrete delta function at grid locations.
* evalPhi.m
 + Evaulates the unscaled discrete delta function. 
