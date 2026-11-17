# Interstellar Braking and Capture: Passive Statistics versus Active Engineering

**Rocks2Space — Delivery research draft, November 2026**

> **Terminology:** The physical process is *braking* (reducing speed or orbital energy), not *breaking*. This paper compares passive capture with active braking. Its calculations are first-order illustrations, **not measured capture percentages**.

## Executive summary

A rock arriving from interstellar space with positive hyperbolic excess speed cannot become permanently bound to an isolated star through two-body gravity alone. A planet, companion star, gas, collision, or other energy-exchange/dissipation mechanism is needed. The destination may contain many bodies, but their capture opportunities **cannot simply be added as independent percentages**: geometry, orbital phases, repeated encounters, and ejection are correlated.

For passive delivery, the governing variables are incoming speed relative to the target star, target-system architecture, arrival direction and impact parameter, and the duration for which an object must remain bound. For active delivery, the dominant obstacle may be less the total radiation dose than maintaining a functional system over **100,000 years**, especially power, mechanical deployment, memory integrity, and navigation. Passive structures that require no surviving electronics deserve comparison with actively controlled craft.

## 1. Definitions and outcome ladder

1. **Stellar encounter:** an object enters a specified sphere (for example, 100 AU).
2. **Planetary-region passage:** its trajectory crosses the orbital region of one or more planets.
3. **Temporary capture:** negative instantaneous osculating stellar energy for some interval, followed by possible escape.
4. **Long-term capture:** bound for a specified horizon, such as 1 Myr or 1 Gyr.
5. **Impact/deposition:** collision with a planet, moon, atmosphere, or other relevant target.
6. **Biological establishment:** viable organisms reproduce and persist. This is a separate, unproven step.

A capture percentage must state **its denominator**: all launched objects, all objects passing within 100 AU, all objects crossing the giant-planet region, or all objects experiencing a close planetary encounter. These can differ by many orders of magnitude.

## 2. Passive capture: basic physics

For an incoming test particle at infinity, specific energy relative to a star is

\[
\epsilon_\infty=\frac{v_\infty^2}{2}>0.
\]

A bound Kepler orbit requires negative energy. The minimum required change in specific orbital energy is

\[
\Delta\epsilon < -\frac{v_\infty^2}{2}.
\]

This energy must go somewhere. A gravitational encounter with an orbiting planet can transfer energy and angular momentum to the planet's orbit; the sign depends on encounter geometry. A binary star can provide a larger moving gravitational scatterer. Gas drag or impact dissipates energy. An isolated stationary star provides no net loss of orbital energy.

### 2.1 Energy hurdle by arrival speed

| Stellar-relative excess speed | Minimum specific energy removal |
|---|---:|
| 0.1 km/s | 0.005 MJ/kg |
| 1 km/s | 0.5 MJ/kg |
| 4 km/s | 8 MJ/kg |
| 10 km/s | 50 MJ/kg |
| 20 km/s | 200 MJ/kg |
| 30 km/s | 450 MJ/kg |

These values follow from \(v_\infty^2/2\), and are independent of rock mass. They do **not** represent propulsion requirements for a specific trajectory.

### 2.2 How many incoming trajectories reach the planetary region?

For an isotropic, uniform incident flux with speed \(v_\infty\), stellar gravitational focusing gives a cross-section for periapsis inside radius \(r\):

\[
\sigma_{\rm pass}(<r)=\pi r^2\left(1+\frac{2GM_\star}{rv_\infty^2}\right).
\]

Conditioned on passing within outer reference radius \(R\), the fraction penetrating within \(r\) is approximately

\[
f_{r|R}=\frac{r^2+2GM_\star r/v_\infty^2}{R^2+2GM_\star R/v_\infty^2}.
\]

**Illustrative Sun-like star, reference boundary 100 AU:**

| \(v_\infty\) | Pass within 5.2 AU / pass within 100 AU |
|---|---:|
| 1 km/s | ~4.98% |
| 4 km/s | ~4.49% |
| 10 km/s | ~3.17% |
| 20 km/s | ~1.66% |
| 30 km/s | ~1.08% |

These percentages describe **penetration**, not capture. They assume isotropic trajectories, a point-mass star, and a 100 AU encounter boundary. A directed beam aimed at the planetary region has a different denominator and distribution.

### 2.3 A deliberately optimistic close-encounter geometry bound

Consider a Jupiter-like planet with orbital radius \(a_p=5.2\) AU and Hill radius

\[
r_H\simeq a_p\left(\frac{M_p}{3M_\star}\right)^{1/3}\approx0.36\;\mathrm{AU}.
\]

The planet's Hill sphere is **not** its capture cross-section. A very loose geometric illustration is the area ratio

\[
\left(\frac{r_H}{a_p}\right)^2\approx0.0048\;(0.48\%).
\]

This ratio is **not a valid capture probability**, nor a reliable probability of a Hill-sphere encounter for an isotropic incoming flux: the planet moves along an orbit, incoming trajectories are focused and anisotropic, and the correct encounter measure integrates over orbital phase and incoming phase space. It is included only as a scale comparison showing that a planetary interaction occupies a small portion of the planetary orbital region.

**Do not multiply the 5.2 AU penetration fraction by 0.48% and label the result a capture estimate.** That would compound incompatible geometric assumptions. To compute a defensible capture percentage, use the simulation in Section 3.

### 2.4 Published numerical context

- Napier, Adams & Batygin (2021), *On the Capture of Interstellar Objects by Our Solar System*, simulated approximately **500 million** trajectories to derive capture cross-sections versus incoming speed. https://doi.org/10.3847/PSJ/abe76e
- Hands & Dehnen (2020), *Capture of interstellar objects: a source of long-period comets*, found Solar System capture in their setup to be small and favored \(v_\infty\lesssim4\) km/s. https://doi.org/10.1093/mnrasl/slz186
- Dehnen & Hands (2022), *Capture of interstellar objects – I. The capture cross-section*, derived velocity- and planet-dependent cross-sections, including collisions. https://doi.org/10.1093/mnras/stab3670
- Dehnen, Hands & Schönrich (2022), *Capture of interstellar objects – II. By the Solar system*, found capture dominated by very slow incoming objects (\(<4\) km/s) under their modeled population. https://doi.org/10.1093/mnras/stab3666
- Napier, Adams & Batygin (2021), *On the Fate of Interstellar Objects Captured by Our Solar System*, separately modeled how long captured objects remain bound. https://doi.org/10.3847/PSJ/ac29bb

**Crucial interpretation:** A published *capture rate* (objects/year) depends on the assumed ambient number density and speed distribution. It is **not** the percentage of a purpose-launched stream captured. That percentage requires normalizing the capture cross-section by the stream's actual spatial/velocity distribution at the target.

## 3. Calculating capture fractions for multiple planets

For a defined incoming distribution \(p(\mathbf{x},\mathbf{v},t)\) at a 100 AU boundary, sample \(N\) trajectories, integrate the complete star–planet–particle N-body system, and classify each trajectory at a specified follow-up horizon.

\[
\hat f_{\rm cap}(T)=\frac{N_{\rm bound\ at\ }T}{N_{\rm entering\ boundary}},
\qquad
\hat f_{\rm deposit}(T)=\frac{N_{\rm deposited\ by\ }T}{N_{\rm entering\ boundary}}.
\]

Report a binomial confidence interval **only if trials are independently sampled**; account for weighting or correlations otherwise. With zero captures in \(N\) independent trials, a rough 95% upper bound is \(3/N\), not zero.

**Parameter sweep:**

- Star: 0.2, 1, and 2 solar masses; also binaries.
- Architecture: zero, one, two, four, and eight planets; masses from terrestrial to Jupiter-like; orbital spacings, eccentricities, inclinations, phases.
- Arrival speeds: 0.1, 1, 4, 10, 20, 30 km/s; also physically motivated speed distributions.
- Directions: isotropic flux versus a deliberately targeted stream; varying impact-parameter spreads.
- Follow-up: immediate post-encounter, 10^3, 10^6, and 10^9 years, where computationally feasible.
- Outputs: flythrough, temporary capture, long-term capture, ejection, impact, and survival.

For a **fixed ensemble of initial conditions**, compare each planetary architecture against the same star-only baseline. This isolates the effect of multiple planets without falsely assuming independent capture events. More planets can raise the chance of an energy exchange **and** raise the chance that a newly captured rock is ejected.

An initial publishable deliverable is a table \(f_{\rm cap}(v_\infty,N_p,T)\) with uncertainties and clearly defined denominator. No scientifically defensible numeric capture percentage for multi-planet targets is asserted here without that simulation.

## 4. Active braking: energy and impulse

The simplest idealization is a spacecraft approaching with excess speed \(v_\infty\). At a specified braking point, the impulsive speed reduction to reach a parabolic trajectory is

\[
\Delta v_{\rm min}(r)=\sqrt{v_\infty^2+v_{\rm esc}(r)^2}-v_{\rm esc}(r).
\]

This is a **best-case lower bound** for a perfectly timed retrograde burn at radius \(r\), not a practical mission budget; a durable bound orbit and safe periapsis may require more. For a Sun-like star at 1 AU, \(v_{\rm esc}\approx42.1\) km/s:

| \(v_\infty\) | Minimum impulse at 1 AU to become marginally bound |
|---|---:|
| 1 km/s | ~0.012 km/s |
| 4 km/s | ~0.190 km/s |
| 10 km/s | ~1.17 km/s |
| 20 km/s | ~4.51 km/s |
| 30 km/s | ~9.55 km/s |

This illustrates the **Oberth advantage** of braking deep in a gravity well. However, arriving on a suitable close passage without hitting the star or a planet is itself a demanding navigation problem.

For a propulsive vehicle, the ideal rocket equation is

\[
m_0/m_f=\exp(\Delta v/v_e),
\]

with exhaust speed \(v_e\). For example, a 10 km/s braking maneuver requires mass ratios of ~12.2 for \(v_e=4\) km/s or ~1.65 for \(v_e=20\) km/s, **before** tanks, power, losses, and reliability margins. The active system must retain fuel and execute the maneuver at the correct time.

## 5. Is a 100,000-year active spacecraft practical?

**Not demonstrated.** It is not automatically forbidden by physics, but there is an extraordinary gap between present validated spacecraft lifetimes and a reliable 100,000-year arrival maneuver.

### 5.1 Radiation: separate dose from time

A simple cumulative-dose model is

\[
D=\int_0^T\dot D(t)\,dt.
\]

For \(T=100{,}000\) years, an *illustrative, unverified at-hardware* dose rate of 0.001–0.1 Gy/year would integrate to 100–10,000 Gy. **These are sensitivity assumptions, not an interstellar radiation prediction.** Real dose depends on particle spectrum, shielding geometry, galactic cosmic rays, local interstellar environment, solar/stellar activity, and secondary-particle cascades. Device response depends on ionizing dose, displacement damage, and single-event effects; absorbed dose in Gy is not interchangeable with semiconductor dose qualification in rad(Si).

Radiation also is **not the only or necessarily dominant lifetime limiter**. Long-term material degradation, micrometeoroid impacts, cold welding, seal failures, propellant loss, corrosion, deployment mechanisms, data retention, and autonomous decision-making are critical.

### 5.2 Engineering strategies

| Architecture | What must survive 100 kyr? | Key difficulty | Assessment |
|---|---|---|---|
| Continuously awake probe | Electronics, power, sensors, actuators, thermal control | Continuous failures and energy demand | Least plausible |
| Hibernating probe with timed wake-up | Passive structure, clock/timer, energy store, restart path | 100 kyr timing drift, storage, restart reliability | Highly speculative |
| Passive cruise with external wake trigger | Structure, sensor/trigger, power and propulsion at arrival | Reliable autonomous detection without continuous operation | Speculative |
| Mechanically deployed passive sail | Sail, attachment, structural integrity; possibly no electronics | Deployment and sail survival | Worth screening |
| Magnetic/electric sail | Field generator/conductor or charged structures; plasma coupling | Mass, longevity, uncertain low-density braking | Worth theoretical modeling |
| Purely passive planetary capture | Only rock integrity and orbital geometry | Very low capture fraction at high speed | Best baseline for statistical dispersal |

A **100,000-year calendar lifetime does not necessarily mean 100,000 years of operating electronics**. A vehicle could remain dormant, but an arrival-time trigger, stored energy source, and deployment system still need credible reliability. Radioisotope power sources with ordinary decades-scale half-lives are not viable as straightforward 100 kyr standby supplies. A dormant craft might instead seek to harvest stellar energy on approach, but powering the first detection and deployment remains a bootstrap problem.

### 5.3 Passive braking is a third category

Not all braking is an onboard active maneuver. A sail may use **destination starlight**, or a magnetic sail may exchange momentum with plasma, without a conventional engine firing after cruise. Such concepts shift the lifetime burden from active electronics to long-lived materials and geometry. Feasibility depends on approach speed, sail area-to-mass ratio, target luminosity, plasma conditions, deployment, and whether braking can be achieved without collision.

The relevant comparison is therefore **passive gravitational capture vs passive environmental braking vs active autonomous braking**.

## 6. An illustrative 100 kyr transit

At constant 10 km/s, a payload travels approximately **1.02 light-years per 100,000 years**. A 4.2 light-year trip would take about 400,000 years at this speed, ignoring acceleration and gravitational effects. To travel 4.2 light-years in 100,000 years requires mean speed ~12.6 km/s. Crucially, the *arrival excess speed* relative to the destination star is not necessarily the spacecraft's speed relative to the Sun: stellar relative motion must be included.

## 7. Decision framework for Rocks2Space

Evaluate strategies using:

\[
P_{\rm useful}=P_{\rm encounter}\times P_{\rm capture|encounter}\times P_{\rm retention|capture}\times P_{\rm deposit|retention}\times P_{\rm viability|deposit}.
\]

This is a **conditional probability decomposition**, not an assertion that factors are known or independent. For flythrough deposition, model an alternate pathway rather than forcing deposition to follow long-term capture.

Compare **cost per physically delivered inert analogue**, then separately biological viability and ethical permissibility. A low-probability passive approach can outperform a sophisticated craft in expected outcomes if it permits enormously more independent payloads; that conclusion cannot be drawn without the actual capture fraction and costs.

### Priority research sequence

1. Reproduce published Sun–Jupiter capture cross-sections and definitions.
2. Build the multi-planet N-body experiment with documented distributions and error bars.
3. Compare low-speed (\(<4\) km/s) and ordinary stellar-relative-speed arrivals.
4. Evaluate passive stellar-light and plasma braking with material lifetime constraints.
5. Construct a 100 kyr radiation/materials/power failure-mode budget for dormant active designs.
6. Compare outcomes per unit mass and cost, initially using inert tracers.

## 8. Scientific and ethical boundaries

Capture into a star system is **not** impact on a habitable planet, and impact is **not** biological establishment. Targeting or releasing viable organisms into an extraterrestrial environment raises planetary-protection and governance questions. All near-term tests should use inert or nonviable analogues; no biological release is proposed here.

## 9. References

1. Napier, K. J., Adams, F. C. & Batygin, K. (2021), *On the Capture of Interstellar Objects by Our Solar System*, Planetary Science Journal 2, 53. https://doi.org/10.3847/PSJ/abe76e
2. Hands, T. O. & Dehnen, W. (2020), *Capture of interstellar objects: a source of long-period comets*, MNRAS Letters 493, L59. https://doi.org/10.1093/mnrasl/slz186
3. Dehnen, W. & Hands, T. O. (2022), *Capture of interstellar objects – I. The capture cross-section*, MNRAS 512, 4062. https://doi.org/10.1093/mnras/stab3670
4. Dehnen, W., Hands, T. O. & Schönrich, R. (2022), *Capture of interstellar objects – II. By the Solar system*, MNRAS 512, 4078. https://doi.org/10.1093/mnras/stab3666
5. Napier, K. J., Adams, F. C. & Batygin, K. (2021), *On the Fate of Interstellar Objects Captured by Our Solar System*, Planetary Science Journal 2, 217. https://doi.org/10.3847/PSJ/ac29bb
6. Lingam, M. & Loeb, A. (2018), *Implications of Captured Interstellar Objects for Panspermia and Extraterrestrial Life*. https://doi.org/10.3847/1538-3881/aae09a

**Status:** Scoping paper with analytic sanity checks. The central requested quantity—*the percentage captured by a multi-body target system*—remains a simulation deliverable, not an established result.
