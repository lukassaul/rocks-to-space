# The Sea Turtle Strategy: Statistical Interstellar Dispersal

**Rocks2Space — Delivery / Passive Dispersal**  
*Back-of-the-envelope research paper — November 2026*

## Abstract

A minimalist alternative to guided interstellar delivery is to release very large numbers of independent rocks or inert analogue capsules onto escaping trajectories, without navigation, onboard electronics, arrival propulsion, or destination selection. Like the sea turtle reproductive strategy, the architecture accepts a low probability of success for any one unit and asks whether the aggregate number of trials makes some favorable outcomes plausible. This paper builds a transparent order-of-magnitude model of encounter frequency, gravitational focusing, physical survival, and biological viability. **It does not demonstrate that a viable organism could survive interstellar transit or establish itself on another world.**

The principal finding is that random dispersal is exceptionally inefficient at reaching a particular stellar system, but can be studied statistically against an entire population of potential destinations. Under an illustrative uniform field-star density of 0.1 pc^-3, isotropic motion at 10 km/s, and 100,000 years of travel, the probability of passing within 100 AU of *any* star is approximately 8.9 x 10^-8 per rock, including point-mass gravitational focusing for a solar-mass star. That is roughly one such encounter per 11 million independent rocks, **not** one successful biological delivery per 11 million rocks.

## 1. What the sea turtle analogy means

The strategy is **fecundity over precision**: many inexpensive units, negligible onboard complexity, no expectation that any individual unit succeeds. The analogue breaks down in several ways: turtles have a nearby reproductive habitat and natural selection acting over generations; interstellar rocks face very small target cross-sections, unknown survival times, and no demonstrated interstellar biological establishment. The analogy is a useful architecture metaphor, not biological evidence.

Compare against the Delivery program's guided trajectories and capture analysis:
- [Delivery overview](../README.md)
- [Interstellar Braking and Capture](../Braking_and_Capture/README.md)
- [Gravity-Assist Navigation for a Long Quiet Interstellar Flight](../Trajectory_Design/Gravity_Assist_Precision/README.md)

## 2. Define outcomes and denominators

Track separately:
1. **Escape:** rock crosses a stated boundary on a positive-energy solar-system trajectory.
2. **Physical survival:** the carrier remains sufficiently intact for the specified interval.
3. **Biological survival:** a specified organism or dormant biological unit remains viable (not established for interstellar times).
4. **Stellar encounter:** passage within a chosen radius R of any star.
5. **Capture:** bound orbit after three-body or dissipative interaction; an isolated star cannot capture a positive-energy incoming object through two-body gravity.
6. **Deposition:** impact or other transfer to a planetary environment.
7. **Establishment:** sustained reproduction and ecological persistence.

A headline probability must state which of these events it measures and whether the denominator is **all released**, **all escaping**, **all physically intact**, or **all arriving within R**.

## 3. Minimal homogeneous-field model

Assume:
- field stars form a spatially uniform Poisson population with number density n (stars per pc^3);
- the rock follows a straight path of length L = vT relative to the stellar population;
- every star is represented by the same encounter radius R;
- stellar motion is absorbed into an effective relative speed v; no stellar clustering or Galactic-orbit correlations;
- rare encounters can be counted independently to first approximation.

The geometric encounter optical depth is

\[
\tau_{\rm geom}=n\pi R^2 L,\qquad P_{\rm geom}(\geq1)=1-e^{-\tau_{\rm geom}}.
\]

For gravitational focusing by a star of mass M, the cross-section at relative speed v_infinity is

\[
\sigma(R,v_\infty)=\pi R^2\left(1+\frac{2GM}{Rv_\infty^2}\right).
\]

Then \(\tau=n\sigma L\), and \(P=1-e^{-\tau}\). This formula describes **encounter with the star's R-sphere**, not capture, impact, or biological success.

For a realistic velocity distribution and stellar mass function, replace the single speed and mass with a rate integral over \(n(M) f(\mathbf v_\star)\sigma(R,v_{\rm rel})v_{\rm rel}\). Stellar motion means rock speed relative to the Sun is **not automatically** its speed relative to every encountered star.

### 3.1 Baseline assumptions

- \(n=0.1\,\mathrm{pc}^{-3}\) — illustrative local-order stellar density, not a measured value for a chosen trajectory or all stellar populations.
- \(v_{\rm rel}=10\,\mathrm{km/s}\) — illustrative effective relative speed; real stellar velocity dispersion may make it much higher.
- \(T=100{,}000\) Julian years.
- \(L\approx1.0227\) pc (~3.34 light-years).
- \(M=M_\odot\), with gravitational focusing applied at the selected R.

### 3.2 Encounter estimates per escaped rock

| Encounter radius R | Geometric probability | With solar-mass gravitational focusing at 10 km/s | Approx. rocks per expected encounter |
|---|---:|---:|---:|
| 1 AU | 7.55 x 10^-12 | 1.35 x 10^-9 | 740 million |
| 10 AU | 7.55 x 10^-10 | 1.41 x 10^-8 | 71 million |
| 100 AU | 7.55 x 10^-8 | 8.89 x 10^-8 | 11 million |
| 1,000 AU | 7.55 x 10^-6 | 7.69 x 10^-6 | 130,000 |

These numbers are **model illustrations**. At 1 AU, the strong focusing correction greatly increases the cross-section for low-speed arrivals, but still does not imply collision with a planet. The 1 AU sphere is a *periapsis threshold around the star*.

For independent rare trials, N rocks have probability \(P_{\ge1}=1-(1-p)^N\approx1-e^{-Np}\) of at least one such encounter. For R=100 AU, p=8.89 x 10^-8:

| Escaping rocks N | Probability of >=1 passage within 100 AU of any star |
|---|---:|
| 1 million | ~8.5% |
| 10 million | ~59% |
| 100 million | ~99.986% |
| 1 billion | effectively 100% |

**This is a count of encounters, not a count of successful deliveries.** Large ensembles may also be correlated if fragments share similar launch directions and velocities; the independent-trial model can overstate the effective sample size.

### 3.3 The 100,000-year distance limit

At 10 km/s, a rock travels ~3.34 light-years in 100 kyr. Reaching a destination 4.2 light-years away at constant 10 km/s takes ~126,000 years, *before accounting for relative motion and gravitational trajectories*. A slower rock may need hundreds of thousands or millions of years. A fast rock travels farther but generally encounters a given star with weaker gravitational focusing.

### 3.4 Why this is not a target-star probability

The homogeneous-field calculation asks for an encounter with **any star along the path**. A specific target at distance d requires the departure direction to intersect its future position, and the result is roughly the angular cross-section of that target, not n sigma L. For isotropic rays from a point source, ignoring focusing and target motion:

\[
p_{\rm specific}\approx\frac{\pi R^2}{4\pi d^2}=\frac{R^2}{4d^2}\quad(R\ll d).
\]

For d=4.2 ly (~265,700 AU) and R=100 AU, p_specific ~3.54 x 10^-8 for a static target. This is **conditional on the rock reaching that distance and on a static-target geometry**; proper motion and the star's trajectory must be incorporated for an actual launch.

## 4. Physical and biological survival

There is no credible single numerical percentage for biological survival over 100 kyr without specifying the organism, state (e.g., spores), rock dimensions, shielding, temperature, radiation environment, launch and arrival heating, and viable-cell criterion.

A bookkeeping decomposition is

\[
p_{\rm total}=p_{\rm escape}\,p_{\rm intact|escape}\,p_{\rm viable|intact}\,p_{\rm encounter|viable}\,p_{\rm capture/deposit|encounter}\,p_{\rm establish|deposit}.
\]

This product is a **chain of conditional probabilities**, not a claim that events are independent. In reality, rock size and speed couple several factors.

### 4.1 Sensitivity rather than invented biological success rates

Suppose p_encounter=8.89 x 10^-8 (100 AU baseline). Let q denote the *combined conditional fraction* that (a) remains physically and biologically viable and (b) achieves the desired downstream outcome after an encounter. Then \(p_{\rm success}=p_{\rm encounter}q\), where q is unknown.

| Assumed q (scenario only) | Success per escaped rock | Escaped rocks for one expected success |
|---|---:|---:|
| 1 | 8.89 x 10^-8 | 11 million |
| 10^-3 | 8.89 x 10^-11 | 11 billion |
| 10^-6 | 8.89 x 10^-14 | 11 trillion |
| 10^-9 | 8.89 x 10^-17 | 11 quadrillion |
| 0 | 0 | No finite number succeeds |

**None of these q values is empirically established.** They are deliberately varied to show that downstream survival/deposition dominates the final estimate. A 100 AU flythrough is not an adequate proxy for biological success.

### 4.2 Time-dependent viability

If viable fraction decays according to an illustrative hazard \(\lambda\), then \(S(T)=e^{-\lambda T}\). This is a *toy model*, not an established spore lifetime law. For half-life H, \(S(T)=2^{-T/H}\). Radiation and aging may produce non-exponential or heterogeneous survival, and shielding may make rock size critical.

A physically meaningful survival model should account for:
- escape shock and thermal exposure;
- desiccation, vacuum, cryogenic temperature and chemical stability;
- galactic cosmic rays, secondary particles and accumulated dose as a function of depth;
- microfractures, erosion, and interstellar dust collisions;
- heating and impact survival at destination;
- viability assay and biological replication after arrival.

A rock can remain intact while all organisms inside are nonviable.

## 5. How many rocks can be launched?

Define total outbound mass M_out, rock mass m, and escape fraction f_escape:

\[
N_{\rm escaped}=\frac{M_{\rm out}}{m}f_{\rm escape}.
\]

For spherical rock of radius a and bulk density rho, \(m=4\pi\rho a^3/3\). At rho=3,000 kg/m^3:
- radius 1 mm: mass ~0.0126 g; one tonne corresponds to ~79.6 million rocks;
- radius 1 cm: mass ~12.6 g; one tonne corresponds to ~79,600 rocks;
- radius 10 cm: mass ~12.6 kg; one tonne corresponds to ~80 rocks.

**Critical trade-off:** smaller particles yield more trials per unit mass, but may provide less radiation shielding and greater vulnerability to heating, erosion, and radiation pressure. Larger rocks protect better but reduce the number of trials. Also, a swarm released from one vehicle may share nearly the same trajectory: fragment count does not imply independent directional coverage.

For the 100 AU baseline, one tonne of independent 1 mm-radius rocks would yield ~7.1 expected stellar encounters in the illustrative 100 kyr field model **if every rock escaped and dispersed into statistically independent trajectories**. The same tonne in 1 cm-radius rocks yields ~0.007 expected encounters. Neither figure is a viability or capture prediction.

## 6. Directionality, natural ejecta and launch energetics

Random dispersal must be defined precisely:
- isotropic release from the source;
- isotropic *asymptotic solar-system escape directions*;
- a common outward cone or correlated debris stream;
- repeated launch epochs while stars move through the Galaxy.

Rocks released from Earth are not automatically solar-system escapees. Earth's orbital velocity, launch energy, gravitational assists, and solar gravity shape the final asymptotes. Isotropic launch directions at a local surface do not map trivially to isotropic outbound directions.

A deliberately engineered dispersal architecture must include energy and cost of achieving escape, release-system reliability, and the possibility of secondary fragmentation. Compare with natural impact ejecta and existing outbound missions, using **incremental viable outbound inventory per cost** as the first-stage benchmark.

## 7. What happens after stellar encounter?

An isolated star cannot capture a positive-energy incoming rock by conservative two-body gravity. Long-term capture requires a planet, binary companion, dissipative interaction, or another energy-exchange mechanism. Even captured rocks may later be ejected. Planetary collision and biological establishment are separate, potentially much rarer outcomes.

The capture fraction must be estimated with target-system N-body models conditional on incoming velocity, impact parameter, direction, and orbital phases. Do not multiply a geometric Hill-sphere area ratio by the 100 AU penetration fraction and call it a capture probability.

## 8. Model limitations and uncertainty budget

The simple n sigma L model ignores stellar clustering, Galactic disk geometry, the Sun's orbit, relative velocity distributions, mass spectra, binaries, gravitational interactions, and correlations among ejecta. It is most useful as a **dimensional benchmark**.

The biological model lacks demonstrated survival rates for multi-kyr to 100-kyr exposure. Even a very large launched population may produce no established life if any required conditional stage has probability zero.

For a rigorous next version, perform Monte Carlo experiments with:
1. realistic stellar density and 6D velocity distributions (e.g., Gaia-informed local populations);
2. an explicit escape-direction and speed distribution;
3. an evolving rock size/viability model;
4. gravitationally focused close approaches;
5. planetary-system capture/deposition simulations;
6. confidence intervals and sensitivity plots.

## 9. Research literature and technical starting points

### Natural transfer and panspermia
- Napier (2004), *A Mechanism for Interstellar Panspermia*. https://doi.org/10.1111/j.1365-2966.2004.07287.x
- Wallis & Wickramasinghe (2004), *Interstellar Transfer of Planetary Microbiota*. https://doi.org/10.1111/j.1365-2966.2004.07355.x
- Mileikowsky et al. (2000), *Natural Transfer of Viable Microbes in Space: 1. From Mars to Earth and Earth to Mars*. https://doi.org/10.1006/icar.2000.6316
- Horneck et al. (2010), *Space Microbiology*. https://doi.org/10.1128/MMBR.00016-09

### Capture and encounter physics
- Napier, Adams & Batygin (2021), *On the Capture of Interstellar Objects by Our Solar System*. https://doi.org/10.3847/PSJ/abe76e
- Hands & Dehnen (2020), *Capture of interstellar objects: a source of long-period comets*. https://doi.org/10.1093/mnrasl/slz186
- Dehnen & Hands (2022), *Capture of interstellar objects – I. The capture cross-section*. https://doi.org/10.1093/mnras/stab3670
- Dehnen, Hands & Schönrich (2022), *Capture of interstellar objects – II. By the Solar system*. https://doi.org/10.1093/mnras/stab3666

### Empirical and computational resources
- ESA Gaia archive: https://gea.esac.esa.int/archive/
- NASA JPL Horizons: https://ssd.jpl.nasa.gov/horizons/
- REBOUND N-body integrator: https://rebound.readthedocs.io/
- NASA astrobiology and space biology resources: https://science.nasa.gov/astrobiology/

References are starting points for verification and deeper literature review; the numerical table is derived from stated assumptions, not copied from a cited paper.

## 10. Research priorities and near-term value

1. **Validate the geometric model** against a synthetic uniform-star Monte Carlo.
2. **Quantify direction correlation** for plausible fragment-release mechanisms.
3. **Build a mass/size/shielding trade study** using inert rocks and nonviable analogues.
4. **Replace homogeneous stars** with a Gaia-informed moving stellar population.
5. **Link encounters to capture and deposition**, retaining explicit conditional denominators.
6. **Assess terrestrial spin-offs** in ruggedized archival materials, low-cost dispersal physics, autonomous passive tracking, and radiation/aging studies.

Any biological deployment would require planetary-protection and ecological review; this paper advocates theoretical modeling and inert-analogue research, not unapproved biological release.

## Conclusion

The sea turtle strategy exchanges **precision for numbers**. Under a toy 100 kyr, 10 km/s, 0.1 stars/pc^3 model, one rock has a ~9-in-100-million chance of passing within 100 AU of some star, assuming a solar-mass target and fixed relative speed. Huge ensembles can make *stellar encounters* plausible, but biological success remains unconstrained because viability, capture, deposition, and establishment probabilities are unknown.

The key design question is not merely “How many rocks?” It is **“How much independently dispersed, adequately shielded, viable material can be sent onto true escape trajectories per unit cost—and what fraction reaches meaningful environments?”**
