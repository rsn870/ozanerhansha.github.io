---
layout: post
title: First Order RL Circuits
date: 2018-05-29
tags: physics
---
LR circuits are... this post will mainly concern **first order** LR circuits, taht is lr circuits consisting of  x y in series

#### equivalent first order LR(details)
in situations where we have resistors in parallel or series before a set of inductors in parallel or series we can consider it equivalent to an first order lr circuit by finign the equivalent reisitstanec and inductance blah blah




### Current while Charging
When connected to a source of emf $\mathcal{E}$, the current $I(t)$ through an LR circuit as a function of time is given by the following:

$$I(t)=\frac{\mathcal{E}}{R}\left(1-e^{-Rt/L}\right)$$

<details><summary><h4 class="inline">Proof</h4></summary>
A real world example of a first order linear differential equation with constant coefficients can be found in considering the current of an RL circuit, which is given by Kirchhoff's loop law:

$$\mathcal{E}-IR-L\dfrac{\mathrm{d}I}{\mathrm{d}t}=0$$

*Where emf $\mathcal{E}$ and current $I$ are functions of time $t$, and resistance $R$ and inductance $L$ are constants.*

Rearranging the terms and isolating the derivative, we can put it in a more familiar form:

$$\frac{R}{L}I+\dfrac{\mathrm{d}I}{\mathrm{d}t}=\frac{\mathcal{E}}{L}$$

We can solve this the same way we solve any first order linear differential equation. First we find the integrating factor:

$$e^{\int R/L\;\mathrm{d}t}=e^{Rt/L}$$

Multiplying the equation by the integrating factor:
$$\frac{R}{L}e^{Rt/L}I+e^{Rt/L}\dfrac{\mathrm{d}I}{\mathrm{d}t}=\frac{\mathcal{E}}{L}e^{Rt/L}$$

Integrating both sides (recognizing the product rule):
$$\int \left(\frac{R}{L}e^{Rt/L}I+e^{Rt/L}\dfrac{\mathrm{d}I}{\mathrm{d}t}\right)\;\mathrm{d}t=\int\left(\frac{\mathcal{E}}{L}e^{Rt/L}\right)\;\mathrm{d}t$$

$$\begin{align}
Ie^{Rt/L}&=\frac{L}{R}\cdot\frac{\mathcal{E}}{L}e^{Rt/L}+C\\
&=\frac{\mathcal{E}}{R}e^{Rt/L}+C
\end{align}$$

Solving for $I$ we find:

$$I=\frac{\frac{\mathcal{E}}{R}e^{Rt/L}+C}{e^{Rt/L}}$$

Assuming the current $I$ is $0$ at $t=0$, we can solve for $C$:

$$\begin{align}
0&=\frac{\frac{\mathcal{E}}{R}e^{R(0)/L}+C}{e^{R(0)/L}}\\
&=\frac{\frac{\mathcal{E}}{R}e^{0}+C}{e^{0}}\\
&={\frac{\mathcal{E}}{R}+C}\\
\rightarrow C&=-\frac{\mathcal{E}}{R}
\end{align}$$

Plugging this back into the equation and doing some more manipulations we find:

$$\begin{align}
I&=\frac{\frac{\mathcal{E}}{R}e^{Rt/L}-\frac{\mathcal{E}}{R}}{e^{Rt/L}}\\
&=\frac{\mathcal{E}}{R}\frac{e^{Rt/L}-1}{e^{Rt/L}}\\
&=\frac{\mathcal{E}}{R}\left(1-\frac{1}{e^{Rt/L}}\right)\\
&=\frac{\mathcal{E}}{R}\left(1-e^{-Rt/L}\right)\\
\end{align}$$

And so, we can conclude that the current $I(t)$ in an RL circuit as a function of time is given by:

$$\boxed{I(t)=\frac{\mathcal{E}}{R}\left(1-e^{-Rt/L}\right)}$$
</details>

<details><summary><h4 class="inline">Proof</h4></summary>
Notice that as time increases the current asymptotes, specifically:

$$\begin{align}
\lim_{t\rightarrow\infty}{I(t)}&=\lim_{t\rightarrow\infty}\frac{\mathcal{E}}{R}\left(1-e^{-Rt/L}\right)\\
&=\lim_{t\rightarrow\infty}\frac{\mathcal{E}}{R}\left(1-\frac{1}{e^{Rt/L}}\right)\\
&=\frac{\mathcal{E}}{R}\left(1-0\right)\\
&=\frac{\mathcal{E}}{R}
\end{align}$$

The current in an RL circuit after it has been fully charged and the source of emf has been removed is given by Kirchhoff's loop law:

$$-IR-L\dfrac{\mathrm{d}I}{\mathrm{d}t}=0$$

We can rearrange the first order homogeneous linear differential equation above as so:

$$\frac{\mathrm{d}I\big/\mathrm{d}t}{I}=-\frac{R}{L}$$

Integrating both sides with respect to $t$ and noticing the derivative of $\ln$ on the left hand side:

$$\int\left(\frac{\mathrm{d}I\big/\mathrm{d}t}{I}\right)dt=-\int\left(\frac{R}{L}\right)\ \mathrm{d}t$$

$$\ln |I|=-\frac{R}{L}t+C$$

Exponentiating both sides with $e$ we find:

$$I=e^{-Rt/L+C}$$

Remembering that at $t=0$ the current is at its peak (i.e $I=\frac{\mathcal{E}}{R}$), we can solve for $C$:

$$\begin{align}
\frac{\mathcal{E}}{R}&=e^{-R(0)/L+C}\\
&=e^C\\
\rightarrow C&=\ln\frac{\mathcal{E}}{R}
\end{align}$$

Plugging this back into our equation for $I$ and doing some manipulations we find:

$$\begin{align}
I&=e^{-Rt/L+\ln\mathcal{E}/R}\\
&=e^{-Rt/L}e^{\ln\mathcal{E}/R}\\
&=e^{-Rt/L}\frac{\mathcal{E}}{R}\\
\end{align}$$

Thus we can conclude that the current $I(t)$ as a function of time though a discharging RL circuit is given by:

$$\boxed{I(t)=\frac{\mathcal{E}}{R}e^{-Rt/L}}$$
</details>
