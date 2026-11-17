# The Living Rock: Radioisotope-Powered Microbial Survival During Interstellar Transit

**Rocks2Space — Payload research concept, November 2026**  
*Speculative feasibility study; not a demonstrated biological delivery method*

## Abstract

The default panspermia payload is a dormant organism shielded inside a rock. A different architecture—the **living rock**—would preserve a tiny, intermittently metabolizing microbial ecosystem during an interstellar voyage. Natural radionuclides embedded in minerals could continuously deposit energy, radiolyze water, and create hydrogen and oxidants. Some terrestrial subsurface organisms exploit related chemical disequilibria. Could that support repair and survival over 1–100 million years?

The energy source is physically credible; the self-sustaining ecosystem is **not established**. A million-year half-life is not required: isotopes with billion-year half-lives provide nearly constant, but generally very low, power. The hard questions are usable chemical-energy yield, access to liquid or biologically active water, redox balance, radiation damage, nutrient recycling, and the minimum maintenance power of a real microbial community.

This paper treats the concept as a research hypothesis, not an authorization to release biological material.

## 1. Dormant rock versus living rock

| Property | Dormant rock | Living rock |
| --- | --- | --- |
| Survival mechanism | Slow degradation in cold, dry dormancy | Occasional metabolism, repair, and possibly turnover |
| Water | Often favors dryness | Requires accessible water for radiolysis and biological chemistry |
| Energy source | Stored biological reserves; no continuous power assumed | Natural radionuclides, potentially supplemented by external radiation |
| Main risk | Unrepaired molecular damage | Failure of thermal, aqueous, chemical, and ecological balance |
| Evidence | Short-duration space experiments and terrestrial analogues | Terrestrial deep subsurface radiolytic ecosystems, not interstellar tests |
| System complexity | Lower | Higher, with more failure modes |

A hybrid is plausible: mostly dormant spores in a mineral matrix with rare, localized periods of repair or microbial activity. This must not be confused with evidence that repair can proceed in a frozen, desiccated rock.

## 2. Terrestrial precedent: radiolysis-supported life

Ionizing radiation can split water, creating H2, oxidants, and radicals. Mineral surfaces and chemical reactions can then mediate redox processes. In some deep continental subsurface environments, microbial communities draw energy from hydrogen and other chemical products associated with water–rock reactions, including radiolysis. The classic case of a deep, isolated ecosystem dominated by *Candidatus Desulforudis audaxviator* illustrates a largely independent subsurface energy economy.

This is **not** proof that microbes consume radioactivity directly or that a closed, isolated rock can run indefinitely. The geological setting provides water, minerals, reactive surfaces, and a large thermal and chemical environment that a meter-scale interstellar rock may lack.

Some melanized fungi have been studied for responses to ionizing radiation. Claims that such organisms can directly use radiation as a substantial long-term power supply should be kept separate from the better-grounded mechanism of **radiolysis-derived chemical substrates**.

## 3. Candidate long-lived radionuclides

| Nuclide | Approximate half-life | Possible role | Limitation |
| --- | ---: | --- | --- |
| Potassium-40 | 1.25 billion years | Widespread in potassium-bearing minerals; beta and electron-capture decays | Modest specific activity and energy deposition in natural rock |
| Uranium-238 | 4.47 billion years | Alpha-rich decay chain can efficiently deposit energy locally | Concentration, daughter equilibrium, radiation damage, and geochemistry matter |
| Thorium-232 | 14.0 billion years | Very long-lived alpha-decay chain | Low activity per gram of parent; daughters and mineral distribution matter |
| Uranium-235 | 704 million years | Additional natural decay-chain contribution | Low natural abundance; not a practical reason to assume a concentrated source |

After 10 Myr, the remaining parent fractions are approximately 99.45% for K-40, 99.85% for U-238, and 99.95% for Th-232. **Persistence of the source is not the problem; low available power is.**

These nuclides should be studied as naturally occurring mineral constituents. No enriched isotope or engineered high-activity source is assumed.

### 3.1 What about potassium-40 specifically?

Natural potassium contains a small fraction of K-40, yielding about **31 radioactive decays per second per gram of natural potassium**. A rock with **2% potassium by mass** therefore has roughly **620 K-40 decays per second per kilogram of rock**.

For an illustrative **0.5 MeV of locally absorbed energy per decay** (a simplifying effective deposition assumption; actual deposition depends on decay branch, escaping photons, and geometry):

\[
P_{\mathrm{K40}}\approx620\ {\rm s}^{-1}\times0.5\ {\rm MeV}\times1.602\times10^{-13}\ {\rm J/MeV}
\approx5.0\times10^{-11}\ {\rm W/kg}.
\]

That is **0.05 nanowatts per kilogram**, or approximately **1.6 millijoules per kilogram per year**. Over 1 Myr the integrated deposited energy is about **1.6 kilojoules per kilogram**, before any conversion losses.

This is not a universal value for rocks: potassium abundance, branching, daughter chemistry, and absorption change the result. It is an order-of-magnitude baseline.

**Crucial:** this tiny power is far too small to heat an ordinary small rock into a liquid-water habitat in deep space. A rock would need a separate thermal argument, not merely a radiolysis argument.

### 3.2 Uranium and thorium

For a parent isotope, the approximate activity is

\[
A=\frac{\ln2}{t_{1/2}}\frac{m}{M}N_A.
\]

A concentration of **1 ppm U-238** corresponds to approximately **12.4 decays/s per kilogram of bulk rock** from the U-238 parent alone. Its ~4.2 MeV alpha emission deposits roughly **8 picowatts/kg** if locally absorbed, excluding decay-chain daughters. Daughter products in secular equilibrium can materially increase the deposited energy; in an open or disturbed mineral, equilibrium cannot simply be assumed.

Thorium-232 must be evaluated with the same daughter-chain and mineral-distribution care. The energy that reaches **water-bearing pore spaces**, rather than dry mineral, is more relevant than total bulk-rock heat production.

## 4. Energy is not the same as metabolic fuel

A living rock needs a complete chain:

1. Radioactive decay deposits energy in or near water.
2. Radiolysis creates H2 and oxidizing products.
3. Chemical reactions keep some products separated rather than allowing immediate recombination.
4. Microbes access an electron donor and compatible acceptor.
5. The resulting usable free energy exceeds maintenance, repair, and nutrient-processing costs.
6. The cycle remains viable as reactants, minerals, and microbial populations change.

Define

\[
P_{\rm bio}=\eta_{\rm deposition}\eta_{\rm radiolysis}\eta_{\rm accessible}\eta_{\rm metabolism}P_{\rm decay},
\]

where the efficiencies are **unknown, geometry- and chemistry-dependent**, and the product is an accounting device rather than a measured yield. Bulk radioactive power is only an upper bound on usable biological power.

A simple annual energy comparison for the 2% K rock is:

| Fraction of deposited energy becoming usable metabolism | Usable energy per kg rock per year |
| --- | ---: |
| 100% (unphysical upper bound) | ~1.6 mJ |
| 10% (hypothetical) | ~0.16 mJ |
| 1% (hypothetical) | ~0.016 mJ |
| 0.01% (hypothetical) | ~0.00016 mJ |

These percentages are **sensitivity assumptions, not experimentally established efficiencies**. The decisive metric is usable energy **per viable cell per unit time**, coupled to an empirically grounded maintenance requirement.

## 5. The water and thermal problem

Liquid water is the largest architectural challenge. A passive small rock in interstellar space loses heat by radiation. The natural decay power of ordinary K-, U-, and Th-bearing minerals is many orders of magnitude too small to keep a centimeter- or meter-scale rock warm against that loss.

Possible environments worth *modeling*, without presuming feasibility:
- Microscopic brines or interfacial water with low-temperature activity, subject to freezing-point and water-activity constraints.
- A substantially larger insulated parent body with radiogenic heat, though mass and transport economics change dramatically.
- A mostly frozen rock with **intermittent** episodes of warming and repair, provided a physically justified heat source and schedule exist.
- An aqueous pore system maintained by conditions other than decay heat; in this case radioactivity is an energy input, not the sole life-support mechanism.

A hydrated rock at low temperature does not necessarily contain *liquid*, metabolically accessible water. Ice can be radiolyzed, but production of trapped chemicals is not equivalent to sustained microbial metabolism.

## 5A. Water retention over million-year voyages: size, temperature and sealing

**The critical distinction is evaporation versus escape.** Water that evaporates or sublimates into a sealed internal pore remains in the rock; only transport through connected pores, fractures, or a breached shell causes net loss to space. Water retention and biologically accessible *liquid* water are separate requirements.

### 5A.1 Exposed ice: a deliberately pessimistic limiting case

For an exposed water-ice surface in vacuum, the Hertz–Knudsen mass flux (assuming sublimation coefficient 1 and negligible ambient water vapor) is

\[
j(T)=P_{\rm ice}(T)\sqrt{\frac{M_{\rm H_2O}}{2\pi R_gT}},
\]

where \(j\) is kg m^-2 s^-1, \(P_{\rm ice}\) is saturation vapor pressure over ice, \(M_{\rm H_2O}=0.018015\) kg/mol and \(R_g=8.314\) J mol^-1 K^-1. For the illustrative values below, use the Murphy–Koop (2005) vapor-pressure fit, which is empirical over a stated temperature range; **80 K is an extreme extrapolation outside its validated range** and should not be treated as a measured prediction.

| Fixed surface temperature | Approximate exposed-ice loss per square meter over 1 Myr |
| --- | ---: |
| 80 K (extrapolated) | 2.3 × 10^-10 kg |
| 100 K (extrapolated) | 6.4 × 10^-4 kg |
| 120 K | 13.3 kg |
| 150 K | 2.9 × 10^5 kg |

This is an *integrated constant-temperature free-sublimation flux*, not a measured rate for an actual interstellar rock. The low-temperature fit extrapolations should eventually be replaced by laboratory-constrained vapor-pressure models. In reality, sublimation consumes latent heat and cools the surface; sunlight, cosmic background radiation, internal heating, rotation and changing heliocentric distance determine temperature.

### 5A.2 Rock radius and an illustrative water budget

For a spherical rock with radius \(a\), bulk density \(\rho=3000\) kg/m^3, and initially accessible water mass fraction \(w=0.10\), total water inventory divided by exposed surface area is

\[
\frac{M_w}{A}=\frac{w\rho a}{3}=100a\quad{\rm kg/m^2}
\]

for \(a\) in meters. The *inventory divided by constant initial sublimation rate* gives the following **notional depletion times**:

| Rock radius | Initial water inventory | At 100 K | At 120 K | At 150 K |
| --- | ---: | ---: | ---: | ---: |
| 1 cm | 0.126 kg | ~1.6 billion yr | ~75,000 yr | ~3.4 yr |
| 10 cm | 126 kg | ~16 billion yr | ~750,000 yr | ~34 yr |
| 1 m | 1.26 × 10^6 kg | ~157 billion yr | ~7.5 million yr | ~342 yr |
| 10 m | 1.26 × 10^9 kg | ~1.57 trillion yr | ~75 million yr | ~3,420 yr |

**Correction to interpretation:** the water inventory scales with rock volume and can be far larger than one might intuitively expect. A 1 m-radius sphere at 3000 kg/m^3 weighs ~12,600 kg, so its 10% water inventory is **~1,260 kg**, not 1.26 million kg. Likewise a 10 cm sphere contains ~1.26 kg water, and a 10 m sphere ~1.26 million kg water. The table's depletion times use the **correct** mass-per-area relation \(100a\) kg/m^2, independent of these illustrative inventory labels. See the corrected table immediately below.

| Radius | Correct bulk rock mass | Correct water mass at 10% |
| --- | ---: | ---: |
| 1 cm | 0.0126 kg | 0.00126 kg |
| 10 cm | 12.6 kg | 1.26 kg |
| 1 m | 12,600 kg | 1,260 kg |
| 10 m | 12.6 million kg | 1.26 million kg |

These times are **upper-level bookkeeping comparisons**, not physically accurate drying curves: an exposed ice front retreats, a dry crust forms, temperature and available ice area change, and most water in a mineral-bearing rock is not exposed at the surface. The 100 K and 120 K cases demonstrate the extreme sensitivity to temperature; at 150 K a freely exposed inventory disappears quickly even in large bodies.

### 5A.3 Connected pores: a moving sublimation front

When ice lies beneath a dry porous mantle, the limiting rate may be transport through pore throats rather than surface sublimation. A first approximation uses Fickian diffusion of water vapor:

\[
\dot M\simeq 4\pi D_{\rm eff}\frac{M_{\rm H_2O}}{R_gT}
\frac{r_i a}{a-r_i}\left[P_{\rm ice}(T_i)-P_{\rm ext}\right],
\]

where \(a\) is outer radius, \(r_i\) is the retreating ice-front radius, and \(D_{\rm eff}\) is the effective vapor diffusion coefficient. This is the steady-state spherical-shell solution for constant \(D_{\rm eff}\), constant temperature, and boundary pressures; it is **not** valid as \(r_i\to a\), where the mantle vanishes and the sublimation boundary condition must be used. In vacuum, pore transport may be in the Knudsen regime, requiring pore-size-dependent diffusivity; cracks can dominate the leakage pathway.

A practical model should solve mass and heat transport together, moving the ice front inward and updating pore geometry, pressure, vapor pressure, and the latent-heat sink. **Porosity alone is insufficient:** connectivity, tortuosity, pore radius, sealing minerals, and fracture history determine whether water can escape.

### 5A.4 Sealed inclusions and mineral-bound water

Three distinct inventories should be tracked:

1. **Free or pore ice** — can sublimate if connected to vacuum.
2. **Sealed fluid or ice inclusions** — potentially retained until fracture, permeability change, or diffusion through the mineral shell.
3. **Structurally bound water / hydroxyl** — may remain in minerals but is not automatically available for microbial metabolism or water radiolysis in a biologically useful environment.

For a genuinely sealed inclusion, net evaporative mass loss to space is approximately zero until leakage occurs. This does **not** mean the inclusion is liquid, metabolically active, or immune to radiation chemistry. Internal vapor pressure, freezing expansion, impacts, thermal cycling, and accumulated damage can compromise the seal.

### 5A.5 Thermal constraints and the rock-size trade-off

For a sphere with volumetric radiogenic heating \(q\) W/m^3 and thermal conductivity \(k\), the center-to-surface temperature difference under a steady uniform-heating model is

\[
\Delta T_{c-s}=\frac{qa^2}{6k}.
\]

For a 2%-potassium rock with K-40 power ~5 × 10^-11 W/kg and density 3000 kg/m^3, \(q\sim1.5\times10^{-7}\) W/m^3. With \(k=2\) W m^-1 K^-1:

- \(a=0.01\) m: \(\Delta T\sim1.3\times10^{-12}\) K;
- \(a=0.1\) m: \(\Delta T\sim1.3\times10^{-10}\) K;
- \(a=1\) m: \(\Delta T\sim1.3\times10^{-8}\) K;
- \(a=10\) m: \(\Delta T\sim1.3\times10^{-6}\) K.

These negligible internal gradients show that **K-40 in ordinary rocks cannot maintain a warm core at these sizes**. A full calculation must also determine surface equilibrium from absorbed starlight, thermal infrared radiation, background radiation, and any other heat source; the rock does not automatically remain at a chosen 100 K or 120 K for its entire journey.

### 5A.6 What to simulate next

Use radii **1 cm, 10 cm, 1 m, 10 m**, water fractions **1%, 10%**, and a temperature history covering solar-system departure, deep interstellar coast, and stellar-system arrival. Compare:
- bare ice, porous mantle, fractured rock, sealed mineral inclusions;
- pore-size and tortuosity distributions; Knudsen versus continuum transport;
- radiative/conductive heat balance and sublimation cooling;
- retained water *mass* versus accessible *liquid-water fraction*;
- radiation-induced chemistry, fracture probability, and mineral hydration changes;
- 0.1, 1, 10, and 100 Myr voyage durations.

Report water retained, likelihood of containment failure, and biological activity feasibility **separately**. The leading hypothesis is that **cold and sealing may preserve water for a very long time, but the same cold conditions inhibit active repair**. This tension may favor a hybrid dormant/intermittently active architecture only if a defensible intermittent heating mechanism is identified.

## 6. Closed-system chemistry and ecology

A radiolytic ecosystem must manage:
- **Redox balance:** hydrogen is useful only if appropriate electron acceptors remain available and are not rapidly recombined.
- **Nutrients:** carbon, nitrogen, phosphorus, sulfur, trace metals, and micronutrients must remain biologically accessible.
- **Waste and toxicity:** peroxide, radicals, and accumulated byproducts can injure cells or alter minerals.
- **Population structure:** a sparse maintenance community may be more plausible than an actively growing dense culture.
- **Mineral interfaces:** radionuclide location relative to pores controls local radiolysis and dose.
- **Evolution and failure:** mutation, population bottlenecks, viral interactions, and ecological collapse become relevant over million-year intervals.

A geological ecosystem exchanges matter and energy with its surroundings. A sealed rock has a stricter mass balance; it cannot indefinitely assume replenished reactants.

## 7. Radiation: fuel and hazard

The same decays that generate useful radiolysis also cause DNA lesions, oxidative damage, and changes to proteins and membranes. Alpha particles deposit energy over short distances; beta and gamma contributions have different ranges. Shielding against galactic cosmic rays does not remove **internal** radionuclide exposure.

An optimum may exist between:
- too little radiolytic production to sustain repair, and
- too much local dose or radical production to preserve viable cells.

That optimum cannot be inferred from isotope half-life alone.

## 8. First-order feasibility tests

The first calculations should be falsifiable rather than optimistic:

**Test A — thermal equilibrium:** Given rock radius, emissivity, mineral composition, and environment, calculate whether any pore region can sustain biologically accessible liquid water. Use radiative heat balance and conductive transport. For ordinary small rocks with natural radioactivity, expect a negative result unless an additional mechanism is identified.

**Test B — deposited dose map:** For realistic mineral grains and pores, estimate alpha, beta, gamma, and cosmic-ray energy deposition as a function of depth. Distinguish energy deposited in rock from energy deposited in water.

**Test C — radiolysis chemistry:** Estimate H2 production, oxidant availability, recombination, mineral reactions, and free-energy flux over 1–100 Myr.

**Test D — maintenance budget:** Compare the usable power to empirically measured maintenance and repair costs for selected low-energy microbial communities, with uncertainty spanning orders of magnitude.

**Test E — ecological stability:** Model nutrient closure, biomass turnover, DNA repair, and probability of extinction. A tiny energy budget does not guarantee a stable community.

**Test F — compare with dormancy:** Under identical rock mass and environment, compare the fraction of viable organisms at arrival for dormant, intermittently active, and continuously active hypotheses.

## 9. A deliberately skeptical baseline

The following conclusions should anchor future analysis:

- **Physically supported:** long-lived natural isotopes continuously deposit energy for millions of years.
- **Terrestrially supported:** radiolysis-derived chemicals can help sustain deep subsurface microbial life.
- **Plausible but unverified:** a sufficiently suitable isolated mineral-water microenvironment could use some of this energy for microbial maintenance.
- **Major unresolved obstacle:** maintaining biologically accessible water in a passive small rock during cold interstellar transit.
- **Not demonstrated:** a sealed living rock surviving a million-year voyage, repairing itself throughout, or establishing life after arrival.

The concept may be most useful as a **limiting-case comparison**: can any plausible continuous-maintenance system outperform dry dormancy, after accounting for the mass and failure risks of keeping it alive?

## 10. Research value along the way

Even if interstellar living rocks prove infeasible, the investigation could improve understanding of ultra-low-energy microbial maintenance, radiation-driven water chemistry, subsurface habitability, geological biosignatures, and long-duration preservation. Initial experiments should use inert mineral-water systems and appropriately contained laboratory microbes, not extraterrestrial release.

## 11. References and verification starting points

- Lin et al. (2006), *Long-Term Sustainability of a High-Energy, Low-Diversity Crustal Biome*, **Science** 314, 479–482. https://doi.org/10.1126/science.1127376
- Chivian et al. (2008), *Environmental Genomics Reveals a Single-Species Ecosystem Deep Within Earth*, **Science** 322, 275–278. https://doi.org/10.1126/science.1155495
- Dzaugis et al. (2016), *A quantitative model of water radiolysis and chemical production rates near radionuclide-containing solids*, **Radiation Physics and Chemistry** (radiolysis modeling; bibliographic details to verify in literature review).
- IAEA LiveChart of Nuclides, half-lives and decay branches: https://www-nds.iaea.org/relnsd/vcharthtml/VChartHTML.html
- Murphy & Koop (2005), *Review of the vapour pressures of ice and supercooled water for atmospheric applications*, **Quarterly Journal of the Royal Meteorological Society** 131, 1539–1565. https://doi.org/10.1256/qj.04.94
- NIST Physical Reference Data: https://physics.nist.gov/
- NASA Astrobiology: https://science.nasa.gov/astrobiology/
- Related Rocks2Space framework: [The Panspermia Spectrum](../Panspermia_Spectrum/README.md) and [The Sea Turtle Strategy](../../Delivery/Sea_Turtle_Strategy/README.md).

**Status:** expanded conceptual feasibility paper with a first-order water-retention and thermal model. Isotope power calculations are explicitly illustrative and require decay-branch, energy-deposition, mineral-chemistry, and thermal-model verification before being treated as design inputs.
