# The Last Hundred Kilometers: Atmospheric Entry, Impact, and Biological Survival

**Rocks2Space — Delivery research paper, November 2026**  
*First-order physics, evidence review, parameter-space design and simulation specification*

## Executive summary

A rock may survive a million-year interstellar voyage yet fail in the last minutes of delivery. Atmospheric entry is not uniformly destructive: it deposits heat in the surface and can ablate or fragment the carrier, **but atmospheric drag can reduce impact speed by orders of magnitude**. The same carrier that protects spores from cosmic rays may be too large to decelerate safely. Conversely, a small particle may land gently but provide inadequate cruise shielding.

**Primary output:** probability or fraction of initially viable payload that reaches a defined receiving environment alive, conditional on a stated distribution of incoming rock size, speed, angle, structure, atmospheric properties, and biological location. Distinguish physical landing, biological survival, and subsequent ecological establishment.

This document proposes a multi-fidelity model and gives reproducible *screening* calculations, not validated survival fractions. Biological deployment remains subject to planetary protection and governance; near-term studies should use inert or contained analogues.

## 1. The complete arrival sequence

1. **Approach:** stellar-relative hyperbolic excess speed, gravitational focusing, planetary encounter geometry.
2. **Atmospheric interface:** planet-relative entry speed and flight-path angle.
3. **Hypersonic entry:** bow shock, radiation/convection, drag, ablation, rotation, internal conduction.
4. **Mechanical breakup:** dynamic pressure, flaws, porosity, thermal stress, fragmentation and fragment interactions.
5. **Dark flight:** deceleration to subsonic/transonic speeds, cooling, wind drift, terminal velocity.
6. **Impact/deposition:** ground, regolith, ocean, ice, atmosphere, or aerial breakup.
7. **Biological outcome:** viable material released into a compatible habitat, not merely present in a recovered meteorite.

**Do not confuse:** entry speed with impact speed; bow-shock gas temperature with interior rock temperature; acceleration with shock pressure; survival of one spore with successful ecological establishment.

## 2. Planetary speed sets the initial hurdle

Ignoring atmosphere and planetary rotation, speed at atmospheric radius r is approximately

\[
v_{\rm entry}=\sqrt{v_{\infty,p}^2+v_{\rm esc}(r)^2},
\]

where \(v_{\infty,p}\) is planet-relative hyperbolic excess speed, **not** speed relative to the destination star. Relative velocity depends on the planet's orbital motion and encounter geometry. A rock arriving at 10 km/s stellar-relative can approach a planet at a substantially different speed.

Illustrative Earth-like entries: 11.2, 15, 30, 60 and 72 km/s. The ~11.2 km/s lower bound applies to unbound approach to Earth from infinity in an Earth-centered two-body model; objects already bound in Earth orbit, or entering other planets, have different minima. Include much slower (0.1–10 km/s) planet-relative arrivals in capture/aerobraking scenarios, and speeds above 72 km/s for interstellar populations not constrained to ordinary bound heliocentric meteoroid orbits.

At fixed mass, kinetic energy scales as \(v^2\); energy per kg is 63, 113, 450, 1800 MJ/kg for 11.2, 15, 30 and 60 km/s respectively. **Most of that energy is not deposited into the surviving rock interior:** it goes into atmosphere, shock layer, radiation, ablated mass and fragments.

## 3. Parameters to vary — avoid a narrow grid

| Category | Baseline range | Important extensions |
| --- | --- | --- |
| Initial radius | 1 mm, 1 cm, 10 cm, 1 m, 10 m | micrometeoroids; 100 m–km bodies; layered carriers |
| Entry speed | 11.2, 15, 30, 60 km/s (Earth case) | planet-bound slow arrivals; >72 km/s unbound interstellar |
| Entry angle below horizontal | 5°, 15°, 30°, 60°, 90° | grazing skip-out, multiple passes, near-horizontal long heating |
| Atmospheric column | 0, 0.01, 0.1, 1, 10, 100 × Earth | CO2, H2, N2, steam, high-altitude density profile |
| Surface gravity | 0.1, 0.38, 1, 2, 3 g | varying scale height and escape speed independently |
| Density | 300, 1000, 3000, 8000 kg/m³ | icy, porous, stony, iron-rich, composite |
| Strength | 0.01–100 MPa | flaw distributions, layered/anisotropic rock, rubble pile |
| Thermal diffusivity | 10^-8–10^-5 m²/s | porosity, ice, glass, metal, anisotropy |
| Heat/ablation | uncertain coefficients | radiative heating, melting, vaporization, spallation |
| Rotation | stable orientation to fast tumble | localized hot spots, asymmetric shielding |
| Biological depth | surface to center | clustered spores, pores, sealed inclusions |
| Receiving surface | rock, loose soil, water, ice, deep ocean | aerial release, lake, hydrothermal zone, subsurface |
| Biology | spores, vegetative microbes, fungi, consortia | viability response to time-temperature-dose-shock |

A complete simulation should sample distributions, not assume that all rocks of one size are identical.

## 4. First-order entry mechanics

For a sphere of radius a, bulk density \(\rho_m\), drag coefficient \(C_D\), mass \(m=4\pi\rho_m a^3/3\), and projected area \(A=\pi a^2\), define the ballistic coefficient

\[
\beta=\frac{m}{C_D A}=\frac{4\rho_m a}{3C_D}.
\]

Drag and dynamic pressure:

\[
F_D=\frac12 C_D\rho_{\rm air}v^2A,\qquad
q_{\rm dyn}=\frac12\rho_{\rm air}v^2,\qquad
\left|\frac{dv}{dt}\right|_{\rm drag}=\frac{q_{\rm dyn}}{\beta}.
\]

For a constant-angle, constant-mass, nonfragmenting body in an exponential atmosphere, integrating drag approximately gives

\[
v_{\rm out}\approx v_{\rm in}\exp\left[-\frac{\Sigma}{2\beta\sin\gamma}\right],
\]

where \(\Sigma=\int\rho_{\rm air}\,dh\) is vertical atmospheric mass column and \(\gamma\) is entry angle below horizontal. **This is a screening expression only:** gravity, ablation, fragmentation, changing \(C_D\), curvature, and surface interception are neglected. It is especially unreliable for shallow skipping trajectories and large changes in speed.

At \(\rho_m=3000\) kg/m³ and \(C_D=1\):

| Radius | Mass | Ballistic coefficient |
| --- | ---: | ---: |
| 1 mm | 0.0126 g | 4 kg/m² |
| 1 cm | 12.6 g | 40 kg/m² |
| 10 cm | 12.6 kg | 400 kg/m² |
| 1 m | 12,600 kg | 4,000 kg/m² |
| 10 m | 12.6 million kg | 40,000 kg/m² |

Earth's total vertical atmospheric column is about 10,300 kg/m². This comparison suggests small rocks can experience substantial deceleration, while large bodies penetrate much more deeply; **it does not predict survival**, because ablation and fragmentation strongly alter the effective ballistic coefficient.

### 4.1 Terminal velocity (late dark-flight limit)

For approximately constant near-surface air density, \(v_t=\sqrt{2mg/(\rho_{\rm air}C_DA)}\). With \(\rho_{\rm air}=1.2\) kg/m³, \(g=9.81\) m/s², \(C_D=1\), \(\rho_m=3000\) kg/m³:

| Radius | Idealized terminal velocity |
| --- | ---: |
| 1 mm | ~8.1 m/s |
| 1 cm | ~25.6 m/s |
| 10 cm | ~80.9 m/s |
| 1 m | ~256 m/s |
| 10 m | ~809 m/s |

This is **not** an impact-speed prediction for every case. A fragment needs sufficient altitude/time after slowing to approach terminal speed; large objects may retain hypervelocity and generate craters. Real shapes, orientation, density and winds matter.

## 5. Heating is a transient depth problem

The rock interior evolves according to

\[
\rho_m c_p\frac{\partial T}{\partial t}=\nabla\cdot(k\nabla T)+Q,
\qquad \alpha=\frac{k}{\rho_m c_p}.
\]

A useful *scale*, not a sterilization depth, is \(\ell\sim\sqrt{\alpha t}\). With \(\alpha=10^{-6}\) m²/s:

| Intense heating duration | \(\sqrt{\alpha t}\) |
| --- | ---: |
| 1 s | 1 mm |
| 10 s | 3.2 mm |
| 30 s | 5.5 mm |
| 100 s | 10 mm |
| 1000 s | 32 mm |

**A surface heat pulse does not instantaneously heat the center of a 10 cm rock.** However, the actual temperature at depth depends on boundary heat flux, ablation recession, phase changes, cracks, pre-entry temperature, and subsequent thermal soak. A 5 mm diffusion scale is **not** proof that organisms deeper than 5 mm survive.

Use coupled transient heat conduction with a receding surface, convective and radiative shock-layer flux, reradiation, latent heat, and phase changes. Compare with real meteorite thermal histories and measured fusion crust thickness where available.

### 5.1 Biological thermal dose

Replace an arbitrary peak-temperature cutoff with a dose-response model incorporating time and temperature, for example a calibrated survival integral or organism-specific D-value/z-value framework. Separate:
- desiccated bacterial endospores;
- fungal spores;
- vegetative bacteria and archaea;
- biofilms, mineral-bound and hydrated consortia.

**Do not extrapolate short laboratory exposures linearly to multi-minute, heterogeneous meteor entry.** A microbe in an aqueous inclusion may suffer boiling/pressure failure even when dry spores survive nearby.

## 6. Ablation, fragmentation and the protection paradox

A simplified single-body ablation law is

\[
\frac{dm}{dt}\approx-\frac{C_H\rho_{\rm air}v^3 A}{2Q^*},
\]

with heat-transfer coefficient \(C_H\) and effective ablation enthalpy \(Q^*\). These parameters are highly uncertain and regime-dependent; shock-layer radiation can matter at high speeds. Track mass, radius, heat balance, and momentum consistently.

Mechanical breakup is often screened when \(q_{\rm dyn}\) approaches an effective failure strength \(S\), but real fragmentation depends on internal cracks, strain rates, thermal gradients, porosity and stress history. Use a probabilistic strength distribution, not one universal threshold.

**Potentially beneficial fragmentation:** a large carrier shields organisms during interstellar cruise; atmospheric breakup produces smaller fragments that slow and land more gently. But breakup may expose organisms, multiply hot surfaces, and occur too low for fragments to decelerate. There is no guarantee of a beneficial fragmentation altitude.

Explore deliberate *passive* layering or weak interfaces in models, but do not assume controlled fragmentation can be engineered reliably over million-year cruises.

## 7. Landing and impact: distinct receiving environments

**Rock or hard ground:** stopping distance is short, with severe local shocks possible even after dark flight. Shock pressure cannot be inferred from speed alone; target impedance, geometry, porosity, obliquity and material failure matter.

**Loose soil/regolith:** penetration may extend stopping distance and moderate some loads, but compressive shock and frictional heating remain.

**Water/ocean:** liquid water can be an attractive habitat but water impact at high speed can be destructive; slower, small fragments may enter water more gently. Account for pressure, cavitation, depth, salt, thermal shock and whether organisms remain accessible.

**Ice/snow:** may cushion some slow impacts, but impact heating, fracture, burial and long-term accessibility are separate.

**Airless body:** no atmospheric deceleration or aerothermal heating; high-speed surface impact becomes the dominant obstacle. A bound, low-relative-speed arrival is fundamentally different from an unbound hypervelocity arrival.

**Dense atmosphere:** greater deceleration may help small bodies, but longer heating, intense pressure, or high-temperature environments may defeat biology.

**Atmospheric or aerial deposition:** microscopic particles or fragments might be deposited without a single hard impact; include survival in aerosols, residence time, radiation and subsequent settling.

## 8. Evidence: what experiments do and do not establish

- **ALH84001:** paleomagnetic evidence has been interpreted as indicating that portions of this Martian meteorite avoided heating above ~40 °C since before ejection. It is an existence proof for a relatively cool interior history, not proof of surviving organisms or a universal entry-temperature bound. Weiss et al. (2000), *A Low Temperature Transfer of ALH84001 from Mars to Earth*. https://doi.org/10.1126/science.290.5492.791
- **Shock recovery:** Horneck et al. (2008) found viable windows for some rock-associated microorganisms in experimental ejection shocks; tolerance differs greatly among organisms and shock protocols. https://doi.org/10.1089/ast.2007.0134
- **Granite spallation:** bacterial spores recovered from lightly shocked spall fragments had survival of order 10^-5 under that specific experiment; the nominal impact-site shock was much higher than the fragment shock. https://pubmed.ncbi.nlm.nih.gov/19778276/
- **Sounding-rocket entry analogue:** spores were recovered from artificial meteorite samples after entry up to ~1.2 km/s, substantially slower than typical Earth-arriving natural meteoroids. https://pubmed.ncbi.nlm.nih.gov/16379527/
- **Tardigrade impact:** experimental tolerance was much lower than some microbial spore results; no universal biological shock threshold exists. https://pmc.ncbi.nlm.nih.gov/articles/PMC8262385/
- **Meteor modeling:** coupled flow/material-response models use transient radial conduction and ablation. https://doi.org/10.1093/MNRAS/STZ3559
- **Entry dynamics:** observationally inferred meteor velocity and mass-loss models help calibrate drag/ablation. https://doi.org/10.1029/2024JE008382

These observations are constraints for validation, **not plug-in probabilities** for an untested million-year interstellar carrier.

## 9. A quantitative survival accounting framework

For an incoming rock with state vector \(x\), define the **fraction of initially viable biological units surviving arrival**:

\[
f_{\rm viable}(x)=
\frac{\int_{\rm payload} n_0(\mathbf r)\,S_{\rm thermal}(\mathbf r,x)\,
S_{\rm shock}(\mathbf r,x)\,S_{\rm chemical}(\mathbf r,x)\,
I_{\rm deposited}(\mathbf r,x)\,dV}
{\int_{\rm payload}n_0(\mathbf r)\,dV}.
\]

Here \(I_{\rm deposited}\) is an indicator or conditional probability for arrival in the specified receiving environment. The product form is a **modeling approximation**; coupled injuries and correlations require joint response models. If cruise viability is the starting denominator, include cruise survival separately and avoid counting it twice.

For a population of incoming rocks with distribution \(p(x)\),

\[
\bar f_{\rm viable}=\int f_{\rm viable}(x)p(x)\,dx.
\]

Report also:
- \(P(\text{at least one viable unit delivered})\);
- mass fraction of surviving carrier;
- viable units per kilogram launched and per kilogram arriving;
- distribution over destination habitats;
- conditional uncertainty bands, especially where no biological calibration exists.

Do not equate landing with successful establishment.

## 10. Parameter sweep and staged simulation

**Stage 0 — unit tests:** reproduce ballistic coefficient, terminal-speed and diffusion-length tables; confirm dimensional consistency and conservation laws.

**Stage 1 — analytic screening:** atmospheric column versus ballistic coefficient; thermal diffusion timescale versus flight duration; pressure versus strength. Reject only cases that violate robust bounds, not cases whose uncertain coefficients could reverse the result.

**Stage 2 — 1D coupled entry:** integrate mass, velocity, angle, temperature profile and radius through atmospheric entry. Include gravity, density profile, changing area, ablation and reradiation.

**Stage 3 — fragmentation ensemble:** Monte Carlo over strength, flaws, breakup altitude, size distribution and individual fragment trajectories. Recompute heating and deceleration for each fragment.

**Stage 4 — impact/deposition:** link terminal state to material-specific impact models for land, water, ice and airless surfaces; include obliquity and fragment burial.

**Stage 5 — biology:** apply experimental thermal and shock dose-response curves to the modeled spatial histories, with uncertainty and separate organism classes.

**Stage 6 — full architecture:** connect arrival to cruise shielding, rock mass, launch cost, and probability of stellar/planetary encounter. Optimize **viable units delivered per unit initial mass/cost**, not merely meteorite survival.

### Required comparison cases

- 1 mm–10 m stony, icy, porous and metallic bodies.
- Earth, Mars, Venus-like, Titan-like, and airless targets, using *actual* atmospheric compositions and profiles in later runs.
- Vertical, shallow and grazing approaches.
- Low-velocity capture/planet-bound arrivals versus fast unbound arrivals.
- Single coherent rock versus controlled/accidental fragmentation.
- Dry spores versus hydrated microbial pockets and mixed payloads.
- Soil, rock, ice, ocean and atmospheric deposition.

### Numerical validation gates

1. Convergence with timestep and spatial mesh.
2. Energy/mass conservation and physically consistent heating/ablation.
3. Benchmark recovered meteorite fall and dark-flight trajectories.
4. Compare calculated thermal histories with meteoritic evidence.
5. Compare biological predictions with **held-out** shock/thermal survival experiments.
6. Propagate uncertainty; report which unknown parameters control the answer.

## 11. Preliminary program-level hypotheses

1. **An intermediate carrier size may dominate.** Larger rocks protect during cruise but may fail to decelerate; smaller ones land gently but shield poorly.
2. **Fragmentation timing may matter more than initial radius.** Early breakup can improve deceleration but increase heating and exposure.
3. **Atmosphere is not simply a hazard.** The same gas that ablates the surface can prevent a much worse high-speed impact.
4. **Low-speed arrival pathways may be disproportionately valuable.** A rare captured rock that impacts gently could outperform many fast direct impacts, depending on capture and delivery probabilities.
5. **Habitat matters.** A viable spore in sterile desert regolith is not equivalent to a viable spore reaching liquid water or a suitable subsurface niche.
6. **Biology must shape materials design.** The optimum rock size, porosity, and internal distribution cannot be chosen from mechanics alone.

These are **hypotheses to test**, not established rankings.

## 12. Next concrete calculation

Build an open, reproducible Earth-atmosphere baseline integrating 1D drag/ablation/thermal diffusion for 1 mm–10 m bodies and 11.2–60 km/s entries, with explicit angle and material sweeps. Then add stochastic fragmentation and a **bounded** microbial survival model. Publish intermediate trajectories, peak temperatures by depth, remaining mass, terminal speeds, and uncertainty envelopes **before** reporting any biological survival percentage.

The paper's most important question is:

> **Which incoming rock architectures maximize the number of biologically viable units deposited into potentially habitable environments, rather than merely surviving atmospheric entry?**

## Related Rocks2Space work

- [Delivery overview](../README.md)
- [Interstellar Braking and Capture](../Braking_and_Capture/README.md)
- [The Sea Turtle Strategy](../Sea_Turtle_Strategy/README.md)
- [The Living Rock](../../Payload/Living_Rock_Radiolytic_Ecosystems/README.md)

**Status:** research framework with first-order calculations; a validated entry/impact survival model remains to be built.
