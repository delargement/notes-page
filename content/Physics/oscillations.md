+++
title = "Oscillations"
author = ["root"]
draft = false
+++

## Linear differential equations {#linear-differential-equations}

For a relationship such as \\(\ddot{x} = ax\\), one can write down:

(note)
\\(a = -\omega^2\\)

If a is negative

\\[
x(t) = Ae^{i\omega t} + Be^{-i\omega t}
\\]


## SHM {#shm}

Hooke's law

\\[
\ddot{x} + \omega^2 x = 0
\\]

Note:

If you are given initial position and velocity, \\(x\_0\\) and \\(v\_0\\), then \\(x(t) = C\cos{\omega t} + D\sin{\omega t}\\) works best as \\(C = x\_0\\) and \\(D = v\_0/\omega\\)


## Damped harmonic motion {#damped-harmonic-motion}

Given a damping force of the form (including the restitution force from the string):

\\[
F = -b\dot{x} - kx
\\]

gives an implicit F = ma equation of:

\\[
\ddot{x} +2\gamma \dot{x} + \omega^2 x = 0
\\]

where \\(\gamma = b/2m\\) and omega is the same as before.

We place the restriction that:

-   \\(\gamma > 0\\)
-   \\(\omega^2 > 0\\)

And defining \\(\Omega^2 = \gamma^2 - \omega^2\\):

\begin{equation}
x(t) = e^{-\gamma t}(Ae^{\Omega t} + Be^{-\Omega t})
\end{equation}

which is the solution to the above homogenous differential equation


### Underdamping {#underdamping}

If \\(\Omega^2 < 0\\), then \\(\gamma < \omega\\) and \\(\Omega\\) is imaginary. We will define the real \\(\tilde{\omega} = i\Omega = \sqrt{\omega^2 - \gamma^2}\\).

Equation (1) then gives

\begin{align\*}
x(t) & = e^{-\gamma t}(Ae^{i\tilde{\omega}t} + Be^{-i\tilde{\omega}t}) \\\\
     & = e^{-\gamma t}C \cos(\tilde{\omega} t + \phi)  \\\\
\end{align\*}

The constants are related by \\(A + B = C \cos\phi\\), \\(A-B=iC\sin\phi\\), and in a physical problem, A\* = B. The \\(e^{-\gamma t}\\) factor describes the envelope of the motion but not necessarily the curve that passes throught the extremes.


### Overdamping {#overdamping}

Opposite of overdamping

\begin{align\*}
x(t) & = e^{-\gamma t}(Ae^{i\Omega t} + Be^{-i\Omega t}) \\\\
     & = Ae^{-(\gamma - \Omega)t} + Be^{-(\gamma + \Omega)t}
\end{align\*}

If \\(\gamma\\) is only slightly larger than \\(\omega\\) (\\(\Omega \approx 0^+\\)), then we'd have exponential decay according to the  'e' coefficient. If \\(\gamma >> \omega\\), then \\(\gamma \approx \Omega\\) and the first term on the right-most side dominates as it has the less negative exponent. We could approxmiate \\(\Omega \approx \gamma(1-\omega^2/2\gamma^2)\\). and the behavior goes like \\(e^{-\omega^2 t/2\gamma}\\)


### Critical damping {#critical-damping}

(Note that we can't use the solution to the diff eq derived above because they're identical. The second unique solution is \\(te^{-\gamma t}\\))

When \\(\Omega = 0\\) (\\(\gamma = \omega\\)),

\\[
x(t) = e^{-\gamma t}(A+Bt)
\\]

Motion converges to zero in the quickest way


## Driven motion {#driven-motion}

\\[
\ddot{x} + 2 \gamma \dot{x} + ax = C\_0e^{i\omega\_0 t}
\\]

We guess that the solution is of the form \\(Ae^{i\omega\_0 t}\\)

Solution:

\\[
x(t) =\left(\frac{C\_0}{-\omega\_0^2 + 2 i \gamma \omega\_0 + a}\right)e^{i\omega\_0 t}
\\] + the earlier solution to the homogenous equation


### Example: {#example}

Take a spring with spring constant, k, a drag force \\(F\_f = -bv\\), and is also subject to a driving force \\(F\_d(t) = F\_d \cos\omega\_d t\\)

<span class="underline">Solution</span>

The force is:
\\(F(x,\dot{x},t) = -b\dot{x} - kx + F\_d\cos{\omega\_d t}\\). So F = ma gives:

\begin{align\*}
\ddot{x} + 2\gamma\dot{x} + \omega^2x & = F\cos{\omega\_d t} \\\\
                                      & = \frac{F}{2} (e^{i\omega\_d t} + e^{-i\omega\_d t})
\end{align\*}

where \\(2\gamma = b/m\\), \\(\omega^2 = k/m\\), and \\(F =F\_d/m\\).

The particular to this equation is obtained similar to as above:

\begin{align\*}
x(t) & = \left(\frac{F/2}{-\omega^2\_d + 2 i \gamma \omega\_d + \omega^2}\right)e^{i\omega\_d t} \\\\
       & + \left(\frac{F/2}{-\omega^2\_d - 2 i \gamma \omega\_d + \omega^2}\right)e^{-i\omega\_d t} \\\\
       & + e^{- \gamma t}\left(Ae^{\sqrt{\gamma^2 - \omega^2} t} + Be^{-\sqrt{\gamma^2 - \omega^2  } t}\right) \\\\
\end{align\*}

By rationalising the denominators and applying Euler's identity:

\begin{align\*}
x(t) & = \left(\frac{F(\omega^2 - \omega\_d^2)}{(\omega^2 - \omega^2\_d)^2 + 4\gamma^2\omega\_d^2}\right)\cos\omega\_d t\\\\
       & + \left(\frac{2F\gamma \omega\_d}{(\omega^2 - \omega\_d^2)^2 + 4\gamma^2\omega^2\_d}\right)\sin\omega\_d t\\\\
       & + e^{- \gamma t}\left(Ae^{\sqrt{\gamma^2 - \omega^2} t} + Be^{-\sqrt{\gamma^2 - \omega^2 } t}\right) \\\\
\end{align\*}

We may draw a right angled triangle with \\(\omega^2 - \omega\_d^2\\) as adjacent, \\(2\gamma\omega\_d\\) as opposite and R as their hypotenuse and define \\(\phi\\) as the corresponding angle to derive:

\\[
x\_p(t) = \frac{F}{R}cos(\omega\_d t - \phi)
\\]