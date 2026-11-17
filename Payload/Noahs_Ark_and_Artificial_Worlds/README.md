# From Noah's Ark to Artificial Worlds: Engineering Interstellar Biospheres

**Rocks2Space — speculative systems-engineering research framework, November 2026**  
*How much of a world must travel with its organisms—and when does the vehicle become a permanent home?*

## Abstract

The [Panspermia Spectrum](../Panspermia_Spectrum/README.md) ranges from a single microbial founder to a full biological Noah's Ark. At the upper end, the problem changes character. Preserving a broad biological library is difficult; keeping interacting ecosystems alive for centuries or millennia requires life support, energy, maintenance, ecological control and industrial capability. A sufficiently autonomous ark may become a **worldship**: not simply a vessel to a habitable planet, but a lasting artificial world whose inhabitants need not arrive anywhere.

This paper separates four architectures, identifies the capabilities each demands, derives first-order scaling relations, and proposes falsifiable research milestones. It treats fictional worldships as inspiration, **not engineering evidence**. No currently demonstrated system is a self-sufficient, indefinitely operating artificial biosphere. The distinction between biological preservation, viable delivery, ecological establishment and autonomous habitation must remain explicit.

## 1. The change of question

For a small panspermia payload, the central question is whether protected organisms can survive transport and establish themselves in a compatible environment. A full ark adds the problem of preserving diverse lineages, developmental stages, symbionts, food webs and ecological functions. A living ark adds a harder requirement: keeping those functions operating **during** transit.

At the far end, the ship itself provides habitable conditions. The destination may be optional. The architecture is no longer optimized solely for delivery; it is optimized for **continuity of a biosphere**.

The two goals must be compared separately:

1. **Biosphere transport:** preserve and deliver life to a destination, possibly with reconstruction infrastructure.
2. **Biosphere habitation:** sustain a viable ecosystem within the spacecraft for an open-ended duration, with repair and renewal.

A vehicle can be excellent at one and poor at the other. A frozen archive might transport more genetic diversity per kilogram than a living habitat. A functioning worldship might preserve ecological relationships that an archive cannot, but at enormous mass and energy cost.

## 2. Four architectures along the spectrum

| Architecture | What travels | Main dependence | Success condition |
| --- | --- | --- | --- |
| **Frozen ark** | Seeds, spores, gametes, embryos, tissue, genomes, microbial cultures, reconstruction instructions | Long-term preservation; revival/reconstruction machinery and receiving habitat | A useful portion of the biological library can be restored |
| **Living ark** | Metabolically active communities, plants, fungi, microbes, possibly animals | Stable bioregenerative life support, controlled environment, continuous energy | Ecosystem functions persist through transit |
| **Worldship** | Living ecosystems plus habitat, maintenance, manufacturing and potentially a resident society | Durable infrastructure, industrial renewal, ecological and institutional resilience | Habitable conditions persist across many generations |
| **Independent artificial world** | A sufficiently self-maintaining biosphere and its supporting industry | Long-term autonomy, resources, replacement capability, heat rejection | Habitation remains viable without a destination or routine external supply |

These are overlapping design regions, not a predetermined ladder. An ark may combine dormant archives with a small active ecosystem; a worldship may still carry extensive frozen reserves.

**Noah's Ark is not simply a species count.** An inventory of species omits microbiomes, population-level genetic variation, pollination, soil ecology, nutrient cycling, pathogens, life stages, developmental dependencies, and ecological assembly. A viable ecosystem cannot be inferred from a collection of specimens.

## 3. Capability requirements

### 3.1 Biological archives and reconstruction

- Preservation and monitoring of viability across seeds, spores, embryos, gametes, cell cultures and microbial consortia.
- Genomic integrity, epigenetic and developmental competence, reproductive diversity and population bottleneck management.
- Cryogenic or other low-temperature storage, with power and refrigeration requirements explicitly modeled.
- Revival, artificial gestation or cultivation where necessary; **stored DNA alone does not reconstruct an organism**.
- Redundancy across compartments and independent failure modes.

Research metric: **fraction of required biological functions recoverable after a specified duration**, not simply fraction of samples still chemically intact.

### 3.2 Ecological closure

Track elemental inventories and fluxes for carbon, nitrogen, phosphorus, sulfur, oxygen, hydrogen and trace nutrients. Photosynthesis or chemosynthesis must be balanced against respiration, decomposition, waste processing and population dynamics. Water recycling does not imply mineral or ecological closure.

A simplified inventory for resource i is

\[
\frac{dM_i}{dt}=I_i-L_i+R_i-C_i,
\]

where imports \(I_i\), irrecoverable losses \(L_i\), regeneration \(R_i\) and consumption \(C_i\) are **defined consistently** for the chosen system boundary. In a truly closed physical system, internal recycling and consumption cancel when all reservoirs are counted; apparent depletion can instead arise from inaccessible chemical forms or leakage.

Research metric: stable habitat function under perturbation, with measured loss and recovery rates.

### 3.3 Energy and heat rejection

Energy sources may include sunlight near stars, stored chemical or nuclear energy, or long-duration generation systems. No option should be assumed to last indefinitely without fuel, spare parts or replenishment.

At thermal steady state, waste heat must be rejected. For an ideal radiator,

\[
P_{\rm rad}=\epsilon\sigma A(T_{\rm rad}^4-T_{\rm bg}^4).
\]

At 300 K, emissivity 0.9, and a negligible background, ideal radiative flux is approximately **413 W/m²**. Rejecting **1 GW** at this temperature would require at least **2.42 million m²** of effective radiating area, before geometry, mutual irradiation, radiator mass and degradation. Hotter radiators reduce area but complicate heat transport.

This is an **engineering lower-bound illustration**, not a worldship power estimate.

### 3.4 Gravity and habitat geometry

For rotation-generated centripetal acceleration,

\[
a_g=\omega^2r,\qquad
T=\frac{2\pi}{\omega}=2\pi\sqrt{\frac{r}{a_g}}.
\]

At radius \(r=1000\) m and \(a_g=9.81\) m/s², the period is approximately **63.4 s**, or **0.946 rpm**. At 100 m, the same acceleration requires ~3.0 rpm. Human comfort and organism-specific biological requirements are not established solely by these equations; rotation also creates Coriolis effects and structural stresses.

Assess whether full Earth gravity is necessary for each biological and industrial function. Habitats may use distinct gravity zones rather than one universal value.

### 3.5 Radiation, structure and pressure integrity

Long-term radiation protection, micrometeoroid impacts, pressure containment, corrosion, fatigue, seal degradation and thermal cycling must be considered jointly. Shielding can be massive but may also serve as thermal mass, water reserve or structural material. A habitat's radiation protection is not equivalent to that of a small dormant rock; inhabited areas have different dose and maintenance constraints.

### 3.6 Maintenance and autonomous industry

A vessel cannot be self-sufficient if it recycles air but depends on externally supplied pumps, bearings, semiconductor devices, pharmaceuticals, catalysts, tools or pressure seals. Model a **dependency graph** of replacement parts, raw materials, machine tools, metrology, chemical processing, electronics, software, and skilled labor or autonomous systems.

An especially important question is whether the system can manufacture **the machines needed to maintain its manufacturing capability**. Complete industrial closure is much more demanding than life-support closure.

### 3.7 Ecological and social resilience

Closed ecosystems can experience nutrient imbalances, disease, trophic collapse, genetic drift and unwanted evolutionary change. If intelligent inhabitants are present, governance, education, knowledge preservation, conflict resolution and consent are central to sustainability; a worldship is not merely a mechanical container for a population.

Do not assume an ecosystem becomes stable simply by increasing its species count or habitat volume. Model disturbances and recovery.

## 4. First-order calculations

### 4.1 Total mass budget

\[
M_{\rm total}=M_{\rm structure}+M_{\rm shielding}+M_{\rm habitat}
+M_{\rm inventory}+M_{\rm industry}+M_{\rm propulsion}
+M_{\rm reserves}.
\]

These categories must avoid double counting: water may be both shielding and inventory; regolith may be both radiation shielding and feedstock.

For a thin cylindrical pressure shell of radius r, internal pressure p and allowable stress \(\sigma_{\rm allow}\), a first screening approximation is

\[
t\sim\frac{pr}{\sigma_{\rm allow}},
\]

subject to structural geometry, rotation, safety factors, buckling, fatigue and damage tolerance. This alone cannot size a rotating habitat.

### 4.2 Closure losses compound

If a resource loses a fixed fraction \(\lambda\) of its *remaining* stock annually, with no replenishment,

\[
M(t)=M_0(1-\lambda)^t\approx M_0e^{-\lambda t}.
\]

For \(\lambda=10^{-5}\) per year (**0.001% annually**), after 100,000 years the remaining fraction is approximately \(e^{-1}=36.8\%\): **63.2% depleted**. This illustrates why apparently excellent recycling may still require replenishment over extreme durations.

But **constant fractional loss is only one model**. Fixed absolute leakage, episodic catastrophic loss, recoverable storage and ecological sequestration produce different outcomes. The appropriate model depends on the resource and system boundary.

### 4.3 Energy over time

If average net power demand is P and duration is t, energy required is \(E=Pt\). For a continuous 1 MW demand over 100,000 Julian years,

\[
E\approx3.16\times10^{18}\ {\rm J}.
\]

This does not imply energy must all be stored at departure; generation and fuel replenishment may be possible. The important distinction is between **energy supply** and **power-system durability**.

### 4.4 Propulsion mass penalty

For idealized reaction propulsion,

\[
\frac{m_0}{m_f}=\exp\left(\frac{\Delta v}{v_e}\right).
\]

At total mission \(\Delta v=10\) km/s and exhaust velocity \(v_e=30\) km/s, the ideal mass ratio is ~1.40. At \(\Delta v=100\) km/s, it is ~28.0. These are ideal rocket-equation examples, **not feasible worldship propulsion designs**; real propulsion needs tanks, engines, energy, thrust-time, shielding and reliability budgets.

For a habitat-sized mass, modest speed changes can require immense total energy and reaction mass. A permanent artificial world may be more practical as a stationary or slowly moving habitat than as a fast interstellar vessel.

## 5. The transition: when does the ship become a world?

There is no sharp physical threshold, but three useful tests are:

**Habitat test:** Can organisms live and reproduce within it for many generations without waiting for arrival?

**Renewal test:** Can the system maintain and replace the infrastructure needed to keep its habitats functioning?

**Destination-independence test:** Would its biosphere remain viable if the planned destination proved unreachable or unsuitable?

A ship that passes all three has become, functionally, an **artificial world**. Its original transport mission may remain historically important, but arrival is no longer essential to continued habitation.

This creates a design tension. Propulsion rewards low mass; permanent habitation rewards redundancy, inventories, shielding, and industrial depth. The best *transport vessel* need not be the best *permanent dwelling*.

## 6. A parent world: combining ark and Sea Turtle strategies

A worldship might function as a **parent ecosystem** that manufactures and disperses many smaller biological archives or protected rocks. This connects the [Sea Turtle Strategy](../../Delivery/Sea_Turtle_Strategy/README.md) with the upper end of the Panspermia Spectrum.

It also separates roles:
- A large habitat maintains biological and technological capabilities.
- Small daughter payloads are optimized for cruise and atmospheric/impact survival.
- Navigation and destination selection are evaluated separately.
- Any eventual biological deployment requires independent planetary-protection review and authorization.

This is a conceptual architecture, not evidence that an autonomous seed-producing worldship can be built.

## 7. The Rocks2Space equation for an ark

The homepage's Drake-like framework still applies, but the probabilities are **architecture-conditional**:

\[
\mathbb{E}[N_{\rm established}\mid A]
=N_{\rm launched}(A)\prod_i
P(E_i\mid E_1,\ldots,E_{i-1},A).
\]

Here \(A\) describes the whole architecture, including biological inventory, habitat size, preservation mode, navigation, destination and time horizon. The chain rule avoids assuming independent stages.

For a **worldship as destination**, however, the outcome metric changes. Rather than counting biological establishments on another planet, measure the probability of **continued autonomous habitation through time T**, the number of functioning descendant habitats, or total sustained viable biosphere-years. Comparing these metrics as though they were identical would be misleading.

## 8. Research program: from achievable experiments to speculative architecture

| Horizon | Testable work | Evidence required |
| --- | --- | --- |
| Near term | Biological archives; cryostorage and revival; seed and microbial consortia preservation | Measured post-storage viability and function |
| Near term | Small closed-ecosystem experiments and nutrient inventories | Longitudinal mass balance, perturbation recovery, failure analysis |
| Medium term | Regenerative habitat subsystem demonstrations | Long-duration performance with controlled external resupply |
| Medium term | Autonomous repair and manufacturing dependency mapping | Demonstrated replacement chains and measured import dependence |
| Long term | Integrated habitat/ecology/industry simulation | Reproducible sensitivity analysis, uncertainty and independent review |
| Speculative | Generational worldship and autonomous artificial-world design | No claim of feasibility without evidence for full-system closure and renewal |

Priority unknowns include the minimum viable ecological complexity; degradation of dormant libraries; stability of closed nutrient cycles; scalable radiation shielding; autonomy of manufacturing; the true mass of industrial closure; and failure recovery over centuries or longer.

### Suggested modeling outputs

1. Mass and power budgets by architecture.
2. Elemental and biological inventory trajectories over time.
3. Replacement-part dependency graph and external import requirement.
4. Reliability model with common-cause failures and repair capacity.
5. Ecosystem perturbation and recovery simulations.
6. Trade-off map of **delivery efficiency versus autonomous habitability**.
7. Sensitivity to mission duration, habitat scale, species/function inventory, and available external resources.

## 9. Science fiction as a source of questions

The large-scale technological habitats and long-lived civilizations imagined by authors such as **Alastair Reynolds** and **Neal Asher** help expose assumptions about longevity, ecology, artificial environments and the meaning of a destination. They are useful prompts for thought experiments, not technical citations or proof of feasibility. A future literature review should distinguish particular fictional examples from engineering studies and avoid attributing a specific design to an author without a checked source.

## 10. Conclusion

At one end of panspermia, a rock transports a few organisms and relies on a world to receive them. At the other, a constructed habitat transports so much ecological and industrial capability that **it becomes a world in its own right**.

The defining question is not simply how many species fit aboard. It is:

> **How much of the biosphere's supporting world must travel with it—and at what point does the vessel no longer need to arrive?**

This shift expands Rocks2Space from delivery mechanics into preservation, closed ecosystems, autonomous manufacturing, long-duration engineering and the creation of permanent artificial habitats. These fields have independent scientific value even if interstellar worldships remain speculative.

## Connections

- [The Panspermia Spectrum](../Panspermia_Spectrum/README.md)
- [The Living Rock](../Living_Rock_Radiolytic_Ecosystems/README.md)
- [The Sea Turtle Strategy](../../Delivery/Sea_Turtle_Strategy/README.md)
- [Interstellar Braking and Capture](../../Delivery/Braking_and_Capture/README.md)
- [Atmospheric Entry and Impact Survival](../../Delivery/Atmospheric_Entry_and_Impact_Survival/README.md)
- [Extreme-Longevity and Radiation-Hardened Systems](../../Impact/Technology_Spinoffs/Extreme_Longevity_and_Radiation_Hardened_Systems/README.md)

**Status:** conceptual research framework with illustrative physical calculations. It does not demonstrate feasibility or advocate biological release.
