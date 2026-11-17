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
- NIST Physical Reference Data: https://physics.nist.gov/
- NASA Astrobiology: https://science.nasa.gov/astrobiology/
- Related Rocks2Space framework: [The Panspermia Spectrum](../Panspermia_Spectrum/README.md) and [The Sea Turtle Strategy](../../Delivery/Sea_Turtle_Strategy/README.md).

**Status:** conceptual feasibility paper. Isotope power calculations are explicitly illustrative and require decay-branch, energy-deposition, mineral-chemistry, and thermal-model verification before being treated as design inputs.
