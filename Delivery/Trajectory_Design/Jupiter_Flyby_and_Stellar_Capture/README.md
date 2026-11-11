# Jupiter Flyby Precision and Stellar Capture

**Rocks2Space — Delivery / Trajectory Design**  
*Research stub — November 2026*

## Research question

Can a spacecraft navigate precisely through a Jupiter gravity assist, then coast without active guidance for an interstellar journey, with a useful probability of entering a specified stellar system and—separately—of being gravitationally captured?

The purpose of this study is to quantify whether **precise initial navigation** can substitute for long-lived onboard autonomy. The answer may differ sharply for flythrough and permanent-capture objectives.

## Scope

### 1. Jupiter encounter geometry and control

Develop a three-dimensional patched-conic baseline and then higher-fidelity numerical model. Define incoming state, encounter timing, B-plane aim point, periapsis limits, gravitational parameter and ephemeris uncertainty, maneuver execution errors, and outbound heliocentric state. Derive sensitivities of outbound speed and direction to each input.

A starting idealized expression is `delta = 2 atan(mu_J / (b * v_infinity^2))`. This is not a complete navigation model.

### 2. Interstellar propagation and target motion

Propagate uncertainty in position and velocity over representative flight times and distances. Include stellar proper motion and radial velocity, uncertainty in target ephemerides, relevant gravitational perturbations, and model uncertainty. Define encounter regions explicitly (e.g., within 100 AU, 10 AU, or 1 AU of the star). Estimate probabilities using reproducible Monte Carlo or other validated methods.

### 3. Flythrough versus capture

For an isolated star, an incoming positive-energy hyperbolic orbit cannot become permanently bound through gravity alone. Analyze alternatives separately:

- Planetary three-body energy exchange;
- Binary-star interactions;
- Dissipative capture by gas or atmosphere, where physically relevant;
- Propulsive or sail-based braking;
- Temporary versus long-term capture.

Do not equate close approach, gravitational focusing, or temporary capture with permanent binding. Estimate capture probability only for stated distributions of arrival speed, direction, impact parameter, and destination-system geometry.

### 4. End-to-end success metrics

Track distinct conditional outcomes: entry into a stellar-system region; temporary binding; long-term binding; encounter with a selected planet; survivable deposition. For statistical dispersal, retain a separate benchmark of **incremental viable outbound material**, rather than assigning a grand success probability to each rock.

### 5. Architecture and technology comparison

Compare:

1. Passive initially guided probe with Jupiter assist;
2. Passive ensemble with varied initial trajectories;
3. Probe with limited midcourse correction;
4. Fully autonomous navigation and braking.

Measure mass, propulsion requirements, energy, cost, reliability, travel time, encounter and capture probability, and sensitivity to target-system assumptions.

## Initial modeling deliverables

- A validated Jupiter-flyby trajectory and sensitivity calculation;
- An uncertainty budget and destination-plane miss-distance distribution;
- A target-star ephemeris and encounter model;
- A capture/flythrough simulation with explicit energy diagnostics;
- A reproducible architecture comparison with uncertainty ranges.

## Open questions

- Which navigation errors dominate after a Jupiter encounter?
- What target-state knowledge is needed at departure for journeys lasting thousands of years?
- At what distances and times does passive aiming cease to be competitive?
- Can a giant planet in a destination system enable useful capture probabilities without active arrival guidance?
- How much does reducing arrival hyperbolic excess speed improve capture opportunities?
- When is a flythrough useful even if capture is improbable?
- What are the near-term spin-offs for precision thrusters, orbit determination, and autonomous navigation?

## Starting references

- NASA, *Basics of Space Flight*. https://science.nasa.gov/learn/basics-of-space-flight/
- NASA, *Voyager: Planetary Voyage*. https://science.nasa.gov/mission/voyager/planetary-voyage/
- *Interstellar Probe* mission concept studies (Jupiter assists, mission navigation and outbound trajectories; identify and cite the specific technical report in the full study).
- Napier (2004), *A Mechanism for Interstellar Panspermia*. https://doi.org/10.1111/j.1365-2966.2004.07287.x
- Wallis & Wickramasinghe (2004), *Interstellar Transfer of Planetary Microbiota*. https://doi.org/10.1111/j.1365-2966.2004.07355.x

*Status: Research plan only. No numerical encounter or capture probabilities have yet been established.*
