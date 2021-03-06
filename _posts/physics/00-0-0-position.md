---
layout: post
title: Position
date: 2018-03-15
tags: physics
# classical-mechanics
---
The position of a particle or object in **space** is defined as a point on an n-dimensional [**Cartesian coordinate system**](/cartesian-product/#cartesian-coordinates). This point can equivalently be thought of as a vector.

### Classical Physics
In classical physics, a position or displacement $\vec{x}$ is a 3-dimensional vector with components $\left(x,y,z\right)$.

*Position is used to refer to a specific point in a coordinate space while displacement refers to the distance traveled from an initial point (usually this point is the origin making position and displacement equivalent)*

The magnitude of displacement, or net **distance**, is calculated the same as any other vector:

$$\left|\vec{x}\right|=\sqrt{x^2+y^2+z^2}$$

<!--more-->

#### Displacement Function
An object's position can be described as a function of time, $\vec{x}(t)$. This position function would thus map from time to 3D-space:

$$\vec{x}:\mathbb{R}\rightarrow \mathbb{R}^3$$

Taking the derivative of an object's displacement function with respect to $t$ provides the object's velocity function, $\vec{v}(t)$:

$$\frac{\mathrm{d}}{\mathrm{d}t}\vec{x}(t)=\vec{v}(t)$$

<!-- Click [here]() for a list of the repeated time derivatives of displacement. -->

### Relativity
In relativity, both time and space are combined into a single space-time continuum. As such, we need a more general notion of '*position*' that includes time. This 4-dimensional position (3 spatial dimensions and 1 time) is called 4-position or, more commonly, an **event**.

An event is defined as a 4-dimensional vector with components $\left(t,x,y,z\right)$. Relativity shows that events that occur at the same time in one reference frame, don't necessarily happen at the same time in another. This is known as **relativity of simultaneity**.

*This is only true for space-like separated events where $\|c\Delta t\| \lt \|\Delta x\|$*.

In special relativity the distance between two positions is not invariant in different reference frames. This brings us to the **spacetime interval**. The spacetime interval, $(\Delta s)^2$ between two events stays constant in all reference frames. In special relativity $(\Delta s)^2$ is:

$$(\Delta s)^2=(c\Delta t)^2-(\Delta x)^2-(\Delta y)^2-(\Delta z)^2$$

### Quantum Mechanics
In quantum mechanics, the state of a particle is given (and completely described) by its **wavefunction** $\psi(\mathbf{x}, t)$. With $\mathbf{x}$ being a point in 3-space and $t$ being a point in time. $\psi$ returns a complex valued probability amplitude.

$$\psi:\mathbb{R^4}\rightarrow \mathbb{C}$$

The probability of observing a particle at position $x$ at time $t$ is given by $\left \vert \psi \right \vert^2$. This implies that, in the one dimensional case, at a given time $t$:

$$\int_{-\infty}^{\infty}\left | \psi(x) \right |^2 dx=1$$

Because the particle has to be somewhere in space, the probabilities must sum to 1. We integrate from $-\infty$ to $\infty$ since the particle is a wave spread out over all of space. This means that the particle could possibly be anywhere in the universe, just with an unfathomably low probability. With some vector calculus, this can be extended to the 3D case we see in the real world.
