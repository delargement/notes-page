+++
title = "Thermodynamics"
author = ["root"]
draft = false
+++

## Boring {#boring}

\\[
T\_F = \frac{9}{5}T\_C +32
\\]


### Thermal expansion {#thermal-expansion}

\\[
\Delta L = L \alpha \Delta T
\\]

\\[
\Delta V = V \beta \Delta T
\\]


## First law of thermodynamics {#first-law-of-thermodynamics}

Work done by a gas

\\[
W = \int \dd W = \int\_{v\_i}^{v\_f} p \dd{V}
\\]

First law of thermodynamics

\\[
dE\_{int} = dQ-dW
\\]

where W is the work done by the system


### Special cases {#special-cases}


#### Adiabatic process {#adiabatic-process}

\\[
\Delta E\_{int} = -W
\\]

when Q=0 (occurs rapidly or is very well insulated)


#### Constant-volume processes {#constant-volume-processes}

\\[
\Delta E\_{int} = Q
\\]


#### Cyclical process {#cyclical-process}

\\[
Q=W
\\]

No change in internal energy


#### Free expansions {#free-expansions}

\\[
\Delta E\_{int} = 0
\\]

Q=W=0

Adiabatic processes


## Heat transfer {#heat-transfer}


### Conduction {#conduction}

\\[
P\_{cond} = \frac{Q}{t} = kA\frac{T\_H-T\_C}{L}
\\]

where P is the conduction rate, k is the thermal conductivity, and T is temperature of the hot and cold reservoirs.
A and L is the area surface area and length of the conducting slab

R-value (Thermal Resistance) is defined as \\(\frac{L}{k}\\) for a material of specified thickness

For a conduction slab made up of multiple slabs:

\\[
P\_{cond} = \frac{A(T\_H-T\_C)}{\sum (L/k)}
\\]

assuming thermal conduction is in the steady state (all energy absorbed is conducted away)

Greater the thermal conductivity, the smaller the temperature difference between reservoirs


### Convection {#convection}

Trivial


### Radiation {#radiation}

\\[
P\_{rad} = \sigma \epsilon A T^4
\\]

where \\(\sigma = 5.6704 \times 10^{-8} W/m^2 \cdot K^4\\) (Stefan-Boltzmann constant),
\\(\epsilon\\) represents the emissivity of the object's surface, which is a value from 0-1.

A surface with a maximum emissivity of 1.0 is a blackbody radiator.

\\[
P\_{abs} = \sigma \epsilon A T\_{env}^4
\\]

A blackbody would absorb all the radiated energy it intercepts

Thus:

\\[
P\_{net} = P\_{abs} - P\_{rad}
\\]