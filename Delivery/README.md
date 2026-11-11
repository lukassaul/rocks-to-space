# Delivery Architectures: From Natural Dispersal to Autonomous Interstellar Navigation

**Rocks2Space — Delivery**  
*Broad technical overview — November 2026*

## 1. Purpose and organizing principle

The Delivery program asks how material might escape a source system, traverse interstellar space, encounter a destination system, and—where possible—be retained or deposited in a suitable environment. It evaluates **complete mission architectures**, not propulsion methods in isolation.

The comparison spans natural impact ejecta, deliberately released passive material, rideshare-launched probes, precisely targeted Jupiter-assist trajectories, and autonomous vessels. Increasing control can improve targeting but adds cost, mass, energy demands, and long-term reliability requirements. A sophisticated vehicle is not necessarily the best architecture per unit of cost or launched mass.

All proposed biological applications remain subject to planetary protection, ecological ethics, and international governance. No demonstrated space-survival experiment establishes that deliberate extraterrestrial inoculation would be safe or justified.

## 2. Architecture comparison

| Architecture | Departure | Cruise control | Arrival outcome | Primary measure |
| --- | --- | --- | --- | --- |
| Natural impact ejecta | Asteroid/comet impacts and subsequent fragmentation | None | Statistical flythrough, rare encounters or capture | Total viable outbound material and its distribution |
| Engineered passive dispersal | Dedicated or shared launches of many particles/capsules | None | Statistical distribution | Incremental viable-material flux per cost |
| Piggybacked passive payload | Secondary payload on a compatible launch | None or brief early corrections | Flythrough or chance gravitational interactions | Viable material added to outbound tail per launch opportunity |
| Initially guided Jupiter-assist probe | Controlled launch, navigation, precise giant-planet flyby | Long passive coast | Targeted stellar-system encounter; capture uncertain | Encounter probability and passive capture probability |
| Autonomous navigating vessel | Controlled launch, possible assists and propulsion | Onboard sensing and corrections | Guided encounter, potential braking/deposition | End-to-end delivery probability and lifetime reliability |

These categories overlap: rideshare is an acquisition/departure strategy and can support either statistical dispersal or a targeted probe. Architecture comparisons must therefore specify combinations of launch access, navigation, propulsion, and arrival mechanism.

## 3. Natural ejecta and the viable-material tail

Impact ejecta provide a physically motivated baseline for dispersal. Some rocks escape planetary gravity; subsequent collisions and radiation forces can redistribute smaller fragments. The key papers by **Napier (2004)** and **Wallis and Wickramasinghe (2004)** modeled pathways for potentially life-bearing material to leave the Solar System and interact with other environments. Their estimates are model-dependent; they do not constitute measurements of viable organisms in interstellar space.

Napier discussed fragmentation and radiation-pressure removal of small particles, with an illustrative estimate of roughly 10^20 potentially life-bearing particles per million years under the model. Wallis and Wickramasinghe estimated an order of several tonnes per year of potentially fertile material escaping under their assumptions. These quantities should not be interpreted as directly measured viable biomass.

For the **randomly dispersed architecture**, the appropriate first benchmark is **the total viable-material tail**, not the chance that one particular rock will establish life somewhere. A meaningful comparison asks whether an intervention increases the mass or count of biologically viable material moving outward, in what sizes and velocity directions, and for how long it remains viable.

A useful bookkeeping model is:

**Viable outbound inventory = released material × viable fraction after release × survival fraction through a defined boundary.**

The boundary must be stated (for example, heliocentric escape, 100 AU, or another defined surface), and survival should be reported with uncertainty. Material mass alone is insufficient: size distribution, shielding, organism type, ejection speed, and survival time also matter. Ideally, report the **differential viable flux** by size, speed, direction, and time, rather than compressing everything into one number.

An engineered contribution could be evaluated by **incremental viable outbound mass or viable units per dollar, per launch, or per kilogram of available secondary-payload capacity**. That does not establish capture or establishment elsewhere. It is a transparent intermediate metric for statistical dispersal.

## 4. Engineered passive dispersal

A deliberately manufactured passive payload might use protected particles, capsules, or aggregates launched onto outbound trajectories. It may improve on natural ejecta through controlled preparation, shielding, size distributions, and departure conditions.

Its advantage is minimal dependence on systems surviving the cruise. Its limitations are weak destination control and uncertain arrival or capture. The architecture should be compared using outbound viable-material inventory and uncertainty, with destination encounter rates modeled separately where possible.

For any biological material, research must first address containment, launch approvals, planetary protection, and the possibility of unwanted contamination. Near-term demonstrations can use inert tracers, simulated payloads, or nonviable biological analogues.

## 5. Piggybacking and rideshare opportunities

**Piggybacking on existing launches** deserves its own evaluation because launch cost and available trajectories may dominate the economics of small payloads. Opportunities include secondary spacecraft accommodations, ESPA-class interfaces, hosted payloads, and missions carrying additional small probes.

Rideshare imposes constraints: the primary mission determines much of the schedule and trajectory; secondary payloads face mass, volume, separation, safety, integration, and regulatory requirements. A rideshare to Earth orbit is not equivalent to injection onto a Jupiter-transfer or solar-escape trajectory. Additional propulsion or gravity assists may be required.

Two distinct piggyback strategies should be compared:

1. **Statistical dispersal:** use available excess capacity to increase the total outbound inventory of viable material (or, for early demonstrations, inert analogues). The performance benchmark is the *incremental viable-material tail* rather than the success probability of a chosen particle.
2. **Targeted piggyback probe:** use a compatible launch opportunity as the first leg of a planned trajectory, followed by correction maneuvers, gravity assists, or propulsion. Here the benchmark includes the probability of reaching a specified region of a destination stellar system.

An important literature and market-research program should examine NASA's rideshare guidance, the Small Spacecraft Technology State of the Art reports, ESPA interfaces, smallsat propulsion, and trajectory-flexible missions such as ESCAPADE. The latter illustrates adaptation to a constrained launch opportunity, not a general guarantee that arbitrary rideshares can reach Jupiter.

Research questions include: how often do missions offer compatible escape energy and geometry; how much secondary mass is available; what propulsion must the secondary carry; and what incremental outbound inventory or target-encounter probability is achievable per dollar?

## 6. Initially guided trajectories and Jupiter flybys

A middle architecture uses active navigation early, establishes an accurately directed outbound trajectory, and then coasts for a very long time without relying on active systems.

A **Jupiter gravity assist** can rotate the spacecraft's planet-relative velocity vector and alter its heliocentric energy and direction through exchange with Jupiter's orbital motion. Its usefulness depends on incoming speed, encounter geometry, periapsis constraints, and the desired outbound trajectory. It is not unlimited free propulsion.

For an idealized hyperbolic flyby, the turning angle can be expressed as:

`delta = 2 atan(mu_J / (b * v_infinity^2))`

where `mu_J` is Jupiter's gravitational parameter, `b` the asymptotic impact parameter, and `v_infinity` the incoming Jupiter-relative excess speed.

The central issue is **outbound-state uncertainty**. A small angular departure error `dtheta` creates a lateral error of approximately `D * dtheta` over travel distance `D`, before accounting for gravity, target motion, and other uncertainties. Precise Jupiter navigation is only one part of the uncertainty budget; the destination star's future position and velocity must also be predicted.

The engineering question is whether the departure accuracy and uncertainty model can make a long passive coast competitive with a vessel that remains operational for navigation on arrival.

See [Jupiter Flyby Precision and Stellar Capture](Trajectory_Design/Jupiter_Flyby_and_Stellar_Capture/README.md) for the dedicated research stub.

## 7. Propulsion and precision control

Architectures may combine chemical propulsion, electric propulsion, solar sails, beamed-light sails, nuclear concepts, and gravity assists. These differ in thrust, specific impulse, power, infrastructure, achievable velocity, and technology readiness.

For passive-targeted missions, **precision impulse delivery** may matter as much as maximum speed: small errors in burn magnitude, direction, timing, or flyby geometry can grow into enormous miss distances over interstellar travel times. Propulsion comparison should therefore include minimum controllable impulse, calibration, navigation observability, and uncertainty—not only theoretical performance.

## 8. Flythrough versus gravitational capture

**Reaching a stellar system is not the same as becoming gravitationally bound to it.** A body arriving with positive hyperbolic excess energy cannot be permanently captured by an isolated star through a purely conservative two-body encounter. Stellar gravity bends and focuses its trajectory, but the object departs again.

Capture requires an energy-exchange or dissipation mechanism, potentially including:

- A carefully timed gravitational interaction with an orbiting planet or binary companion;
- Atmospheric or gas drag in a suitable environment;
- Onboard braking propulsion;
- A sufficiently effective sail or other environmental braking mechanism.

Three-body capture is possible in principle but depends strongly on encounter geometry, planetary phase, incoming speed, and the definition of *permanent* rather than temporary capture. No useful capture probability should be asserted without specifying a destination-system model and performing simulations.

A rigorous architecture comparison must distinguish **stellar-system encounter**, **temporary capture**, **long-term bound orbit**, **planetary encounter**, and **actual deposition**. A passive flythrough might still be scientifically interesting, but it is not equivalent to a captured delivery.

## 9. Autonomous navigating vessels

At the opposite end of the spectrum, autonomous craft could use onboard observations and propulsion to correct course and possibly brake at arrival. This reduces dependence on departure accuracy and long-range ephemeris forecasts, but introduces severe lifetime requirements for sensors, power, computing, attitude control, propulsion, and fault recovery.

Spacecraft autonomy and optical navigation have precedents within the Solar System; autonomous interstellar arrival and biological deposition do not. The survival of navigation and braking systems over centuries or millennia is a substantially higher engineering bar than maintaining a passive payload.

## 10. Quantitative comparison framework

Architecture selection should be driven by clearly defined outcomes and common assumptions.

For **statistical dispersal**, report:

- Total released mass and viable fraction;
- Viable outbound mass or organism count crossing a stated boundary;
- Distribution by particle size, shielding, speed, and direction;
- Survival estimates over specified durations;
- Incremental viable tail per launch opportunity, cost, or secondary-payload mass.

For **targeted missions**, report:

- Distribution of departure state and predicted destination state;
- Probability of entering a specified stellar-system region;
- Conditional probability of capture given encounter;
- Conditional probability of the defined delivery outcome;
- Mission cost, payload mass, travel time, and operational reliability.

The probability of a defined targeted success can be factored as:

`P(success) = P(encounter) * P(capture | encounter) * P(delivery | capture)`

This factorization applies only where capture is part of the chosen success definition; a flythrough mission requires a different outcome model. **Do not use the targeted per-object success metric to dismiss statistical dispersal**, and do not treat increased outbound viable material as proof of successful settlement.

For mixed strategies, compare expected outcomes under an explicit objective function and retain separate intermediate measures where direct comparison is not meaningful.

## 11. Dual-benefit research opportunities

Delivery research can yield independently useful technologies:

- **Propulsion and precision drives:** efficient microthrusters, repeatable small impulses, compact power and propulsion, satellite maneuvering;
- **Navigation and estimation:** optical navigation, improved ephemerides, uncertainty propagation, trajectory optimization, automated mission design;
- **Autonomy:** fault-tolerant computers, long-lived sensors, low-power operation, onboard decision-making and health monitoring;
- **Launch integration:** rideshare interfaces, standardized small probes, flexible mission planning, lower-cost scientific access to space;
- **Modeling:** robust Monte Carlo simulation, risk analysis, and verification of rare-event probabilities.

These benefits should be pursued even if interstellar biological delivery proves impractical or ethically impermissible.

## 12. Research priorities

1. Establish a defensible baseline for the Solar System's natural outbound *potentially viable* material distribution, with survival uncertainty clearly separated from total ejecta mass.
2. Survey rideshare opportunities and compare the marginal cost of adding passive outbound material or nonbiological test payloads.
3. Quantify Jupiter-flyby targeting accuracy, uncertainty propagation, and the effect of destination-star motion.
4. Model stellar-system flythrough, temporary capture, permanent capture, and delivery as distinct outcomes.
5. Compare passive, statistically dispersed, initially guided, and autonomous architectures using common costs and explicit objectives.

## 13. Conclusion

The strongest initial framework is **architecture comparison**, not a contest among propulsion technologies. Natural ejecta and passive piggyback dispersal should first be assessed by their contribution to the *total viable-material tail*. Jupiter-assist probes should be assessed by their ability to reach specified stellar-system regions after long passive coasts. Autonomous vessels should be assessed by their end-to-end capabilities and extraordinary long-duration reliability requirements.

The most important unresolved distinction is between **arriving in a stellar system and being gravitationally captured there**. That issue, alongside Jupiter departure precision, warrants a dedicated technical study.

---

## Selected references and starting points

1. Napier, W. M. (2004). A Mechanism for Interstellar Panspermia. *Monthly Notices of the Royal Astronomical Society*. https://doi.org/10.1111/j.1365-2966.2004.07287.x
2. Wallis, M. K., & Wickramasinghe, N. C. (2004). Interstellar Transfer of Planetary Microbiota. *Monthly Notices of the Royal Astronomical Society*. https://doi.org/10.1111/j.1365-2966.2004.07355.x
3. NASA, *Basics of Space Flight* (trajectories, gravity assists and navigation). https://science.nasa.gov/learn/basics-of-space-flight/
4. NASA, *Voyager: Planetary Voyage* (gravity-assist mission history). https://science.nasa.gov/mission/voyager/planetary-voyage/
5. NASA, *Small Spacecraft Technology State of the Art* (small spacecraft and integration; consult current edition). https://www.nasa.gov/smallsat-institute/sst-soa/
6. NASA, *SMD Rideshare 101* (secondary payload opportunities and constraints; verify current program guidance).
7. Johns Hopkins Applied Physics Laboratory and partners, *Interstellar Probe* mission concept studies (Jupiter-assist and outbound-trajectory design; verify specific study edition).

*Status: Conceptual architecture review. Numerical delivery and capture probabilities require dedicated modeling; cited engineering resources are research starting points, not validated performance inputs.*
