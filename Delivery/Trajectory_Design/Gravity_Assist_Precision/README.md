# Gravity-Assist Navigation for a Long Quiet Interstellar Flight

**Rocks2Space — Delivery / Trajectory Design — Technical research draft (November 2026)**

**Research objective:** Determine the precision of navigation, gravity-assist targeting, trajectory-correction maneuvers, and destination-star state prediction needed to execute a Jupiter-assisted outbound trajectory followed by a **long, unpowered, uncorrected interstellar coast**.

**Status:** Analytic requirements and literature map; not a validated end-to-end mission solution. Numerical examples are order-of-magnitude and explicitly state assumptions.

## 1. Executive result

For an uncorrected flight of duration \(T\), a small residual transverse velocity error produces \(\Delta r_\perp\approx T\Delta v_\perp\). Over 100,000 Julian years, a 1 mm/s transverse velocity error corresponds to ~0.0211 AU of positional drift. To keep the **spacecraft-only** linear miss contribution below 1 AU, residual transverse velocity error must be below ~47.4 mm/s. At 100 AU, the corresponding tolerance is ~4.74 m/s.

**Correction to avoid a common unit error:** 1 AU / 100,000 years = **0.0474 m/s (47.4 mm/s)**. The scaling is \(\Delta v = \Delta r/T\).

The much larger obstacle may be **predicting the target star's future location**, rather than merely executing a tiny thruster impulse. A target transverse-velocity uncertainty of 1 m/s over 100 kyr corresponds to ~21.1 AU of position uncertainty. This is smaller than a 100 AU encounter radius, but substantial for a 1–10 AU encounter objective. These calculations ignore dynamical correlations, gravitational acceleration, and future improved observations, and are intended to expose requirements.

A Jupiter flyby can produce a large, controllable change in outbound direction and heliocentric energy; it also **amplifies errors** in the inbound aim point. The mission must therefore be optimized as an end-to-end covariance problem, not as a single burn tolerance.

## 2. Define the success event before designing the flyby

Distinguish:

- passing within 1, 10, 100, or 1,000 AU of the **future target-star position**;
- entering a planetary system with specified approach speed and direction;
- passing a selected target planet's orbit;
- becoming temporarily or permanently captured (requires additional energy exchange);
- actual impact or deposition.

Specify an encounter probability (e.g., 50%, 90%, 99%) and uncertainty confidence model. A 100 AU sphere is not a guarantee of capture or planetary encounter.

## 3. Coordinate frames and state representation

Use a consistent inertial frame (e.g., ICRF/BCRS where appropriate), a documented time scale (TDB/TCB conversions), and full six-dimensional state vectors. Separate:

1. spacecraft barycentric state \((\mathbf r_s,\mathbf v_s)\);
2. Jupiter barycentric state and covariance;
3. target-star state \((\mathbf r_\star,\mathbf v_\star)\) and covariance;
4. dynamical-model uncertainties and correlations.

Do not propagate a star's apparent proper motion alone as if it were a complete 3D state: parallax, radial velocity, perspective acceleration, companions, and Galactic dynamics can matter over 100 kyr.

## 4. Patched-conic Jupiter encounter

In Jupiter's instantaneous frame, let incoming hyperbolic excess velocity be \(\mathbf v_{\infty,-}\), with magnitude \(v_\infty\). The impact parameter \(b\) and Jupiter gravitational parameter \(\mu_J\) set the hyperbolic turning angle:

\[
\delta=2\arctan\left(\frac{\mu_J}{b v_\infty^2}\right).
\]

Equivalently, the hyperbolic eccentricity is
\(e=\sqrt{1+(b v_\infty^2/\mu_J)^2}\), and \(\delta=2\arcsin(1/e)\).

At closest approach radius \(r_p\),

\[
b=r_p\sqrt{1+\frac{2\mu_J}{r_p v_\infty^2}}.
\]

For an ideal elastic planetary flyby \(|\mathbf v_{\infty,+}|=|\mathbf v_{\infty,-}|\), but the direction changes. In a heliocentric frame,

\[
\mathbf v_{\odot,+}=\mathbf v_J+\mathbf v_{\infty,+},
\]

so Jupiter's orbital motion changes spacecraft heliocentric energy. The 3D direction of the B-plane offset determines whether the encounter increases or decreases heliocentric energy and where it aims the outbound asymptote.

### 4.1 B-plane targeting

Let \(\hat{\mathbf S}\) follow the incoming asymptotic velocity, with orthogonal \(\hat{\mathbf T}\) and \(\hat{\mathbf R}\) spanning the encounter B-plane. The aim point is \((B\cdot T,B\cdot R)\); the associated linearized time of flight describes along-track timing. Navigation should propagate a **3D B-plane and timing covariance**, not just periapsis altitude.

JPL's technical description of the B-plane, dispersion ellipses, and LTOF is an essential starting source: https://tmo.jpl.nasa.gov/progress_report/42-123/123E.pdf

### 4.2 Flyby sensitivity

For fixed incoming \(v_\infty\), the first-order turn-angle sensitivity to B magnitude is

\[
\frac{\partial\delta}{\partial b}
=-\frac{2\mu_J v_\infty^2}{b^2v_\infty^4+\mu_J^2}.
\]

For speed uncertainty,

\[
\frac{\partial\delta}{\partial v_\infty}
=-\frac{4\mu_J b v_\infty}{b^2v_\infty^4+\mu_J^2}.
\]

These are **scalar planar partial derivatives**, not the full 3D state transition matrix. Outbound state also responds to the B-plane azimuth, incoming velocity direction, encounter epoch, and Jupiter ephemeris.

A small outbound angular error \(\Delta\theta\) leads to an approximate transverse error \(L\Delta\theta\) over distance \(L\). At 4.2 light-years, a 100 AU miss radius subtends ~\(3.77\times10^{-4}\) rad (~78 arcseconds), while 1 AU subtends ~\(3.77\times10^{-6}\) rad (~0.78 arcseconds). This is a **directional** bound, not a complete encounter-probability calculation.

## 5. Burn requirements: what precision actually means

An impulse \(\Delta\mathbf v\) applied at epoch \(t_m\) affects Jupiter's B-plane target and final interstellar state. Define sensitivity matrices from the propagated dynamics:

\[
\Delta\mathbf B\simeq \frac{\partial\mathbf B}{\partial\Delta\mathbf v_m}\Delta\mathbf v_m
+\frac{\partial\mathbf B}{\partial t_m}\Delta t_m+\cdots
\]

and

\[
\Delta\mathbf r_{\rm rel}(T)\simeq
\Phi_{rv}(T,t_m)\Delta\mathbf v_m
+\Phi_{rr}(T,t_m)\Delta\mathbf r_m
-\Delta\mathbf r_\star(T)+\cdots .
\]

For a simple free coast, \(\Phi_{rv}\approx T I\). Around Jupiter, the flyby can make this matrix highly anisotropic and nonlinear.

**Do not confuse** thruster minimum impulse bit, commanded \(\Delta v\), execution repeatability, knowledge of executed \(\Delta v\), pointing error, B-plane error, or residual post-correction velocity covariance. A 1 m/s maneuver with 0.1% execution error leaves a nominal 1 mm/s velocity error, which would drift ~0.021 AU in 100 kyr if not measured and corrected.

### 5.1 Velocity error versus quiet-coast miss distance

Assume exactly 100,000 Julian years, linear free coast, and no target-state error.

| Allowed transverse miss | Max residual transverse velocity error |
|---|---:|
| 1 AU | 47.4 mm/s |
| 10 AU | 0.474 m/s |
| 100 AU | 4.74 m/s |
| 1,000 AU | 47.4 m/s |
| 10,000 AU | 474 m/s |

Equivalently, **1 mm/s** residual error yields ~0.0211 AU drift over 100 kyr; **1 cm/s** yields ~0.211 AU; **1 m/s** yields ~21.1 AU.

The tolerance scales inversely with flight time. A 400 kyr coast demands four times tighter residual transverse velocity knowledge/control for the same miss radius.

### 5.2 Precision in timing

A velocity of 10 km/s moves ~0.0021 AU per 8.7 hours, and ~2.11 AU per year. An error in departure/encounter epoch shifts arrival position, but the actual effect must account for star motion, target approach geometry, and coupled orbital state. Timing is not interchangeable with transverse velocity accuracy.

### 5.3 Practical correction architecture

A credible design includes: initial injection targeting; tracking and orbit determination; an early correction; a late B-plane cleanup; Jupiter flyby; **post-flyby tracking and final correction** while communication and navigation remain feasible; then shutdown and long quiet coast. The last correction may be more decisive than the pre-flyby burn, because it removes actual flyby execution/model errors.

The spacecraft must have a verified state **after** the final correction. An unmeasured final impulse does not establish the required outbound accuracy.

## 6. Target-star prediction may dominate

Gaia EDR3 documents typical proper-motion uncertainties of ~0.02–0.03 mas/year for bright sources, with source-dependent performance. At distance \(d\) pc, the corresponding transverse velocity uncertainty is

\[
\sigma_{v_t}[\mathrm{km/s}]=4.74047\,d[\mathrm{pc}]\,\sigma_\mu[\mathrm{arcsec/yr}].
\]

This is one component of a correlated 6D uncertainty model. At \(d=1.3\) pc and \(\sigma_\mu=0.03\) mas/year, the formal proper-motion-only transverse velocity uncertainty is ~0.185 m/s, corresponding to ~3.90 AU of linear drift in 100 kyr. **Illustrative only**: not a target-specific Gaia measurement, and not a complete predicted star-position uncertainty. Parallax, radial velocity, acceleration, binarity, and Galactic potential matter.

For an illustrative target-state transverse-velocity uncertainty of 1 m/s, the 100 kyr drift is ~21.1 AU; for 0.01 m/s, ~0.211 AU. Better spacecraft burn precision cannot compensate for an unknown target position.

A proper analysis should propagate the full Gaia covariance, available spectroscopic radial velocities, known companions, and a Galactic gravitational model; report 2D/3D encounter probability distributions, not only a nominal miss distance.

## 7. Covariance propagation and Monte Carlo

For state \(\mathbf x\), a first-order covariance estimate is

\[
P_f\approx\Phi P_0\Phi^T+Q,
\]

where \(\Phi\) is the state-transition matrix and \(Q\) represents accumulated model/process uncertainty. At Jupiter, nonlinear mapping and non-Gaussian tails may invalidate a purely linear estimate.

Recommended pipeline:

1. Build patched-conic trajectories and analytic sensitivities.
2. Use JPL SPICE kernels and Horizons for high-fidelity planetary ephemerides, with documented validity ranges.
3. Fit/simulate tracking data (range, Doppler, VLBI/Delta-DOR, optical navigation where available).
4. Model finite-burn thrust magnitude, pointing, calibration, timing, and residuals.
5. Numerically propagate solar-system gravity and relevant nongravitational accelerations.
6. Propagate target-star 6D state under Galactic dynamics and companion perturbations.
7. Sample spacecraft and target-state uncertainty jointly; evaluate miss distances and encounter probabilities.
8. Repeat across flyby geometries, arrival velocities, coast durations, and correction schedules.

A useful output is the **required post-Jupiter outbound-state covariance** for a chosen encounter probability, then the necessary burn/tracking precision to achieve it.

## 8. Mission and flight-dynamics evidence

- **Juno navigation to Jupiter orbit insertion:** actual navigation campaign; Jupiter barycenter ephemeris uncertainty was important late in approach. https://ntrs.nasa.gov/citations/20210007658
- **Galileo gravity-assist maneuver planning:** NASA describes repeated maneuvers and a 0.92 m/s correction ahead of an Earth flyby. https://www.jpl.nasa.gov/news/galileo-third-trajectory-correction-maneuvers/
- **Galileo Earth flyby:** six correction maneuvers, with a final adjustment after a maneuver accurate within 1%. https://www.jpl.nasa.gov/news/galileo-earth-flyby/
- **Galileo Earth–Venus trajectory-correction design:** injection targeting and statistical correction budgets. https://ntrs.nasa.gov/citations/19880063153
- **Galileo navigation and Io gravity assist:** historical account of navigation accuracy and the use of Io's gravity. https://descanso.jpl.nasa.gov/evolution/AAS_08-311.pdf
- **NASA Basics of Space Flight, Navigation:** iterative orbit determination and trajectory corrections. https://science.nasa.gov/learn/basics-of-space-flight/chapter13-1/
- **JPL B-plane aiming coordinates:** definitions, B-plane dispersion ellipses, and linearized time of flight. https://tmo.jpl.nasa.gov/progress_report/42-123/123E.pdf

These are evidence of modern interplanetary navigation techniques, **not** proof of micro-mm/s long-term interstellar departure accuracy.

## 9. Tools and foundational resources

### Authoritative software and data

- NASA/JPL **NAIF SPICE Toolkit**, reference frames, SPK kernels, time conversion, and geometry: https://naif.jpl.nasa.gov/naif/
- JPL **Horizons** ephemeris system and manual: https://ssd.jpl.nasa.gov/horizons/ and https://ssd.jpl.nasa.gov/horizons/manual.html
- NASA **GMAT** open mission analysis and optimization: https://software.nasa.gov/software/GSC-17177-1
- **Orekit** open-source flight dynamics library: https://www.orekit.org/
- **poliastro** open-source astrodynamics package: https://docs.poliastro.space/
- **REBOUND** N-body integrator and variational equations: https://rebound.readthedocs.io/
- ESA **Gaia archive and documentation** for stellar astrometry/covariance: https://gea.esac.esa.int/archive/ and https://gea.esac.esa.int/archive/documentation/GEDR3/

Tool links are a research inventory; current maintenance, licensing, and suitability for each specific calculation must be verified before adoption.

### Books and reference texts

- Bate, Mueller & White, *Fundamentals of Astrodynamics* — two-body conics, orbital transfers.
- Battin, *An Introduction to the Mathematics and Methods of Astrodynamics* — orbit determination and sensitivity.
- Vallado, *Fundamentals of Astrodynamics and Applications* — frames, perturbations, covariance, navigation.
- Prussing & Conway, *Orbital Mechanics* — trajectory design and optimization.
- Wiesel, *Spaceflight Dynamics* — gravity assists and mission design.
- Montenbruck & Gill, *Satellite Orbits* — orbit determination, numerical methods.
- Tapley, Schutz & Born, *Statistical Orbit Determination* — estimation, covariance, measurement modeling.
- Longuski, Guzmán & Prussing, *Optimal Control with Aerospace Applications* — trajectory optimization.
- Conway (ed.), *Spacecraft Trajectory Optimization* — multi-body trajectory optimization.

### Further primary-source retrieval targets

- Voyager 1/2 Jupiter/Saturn encounter navigation reconstructions and B-plane residuals.
- New Horizons Jupiter flyby targeting and post-encounter navigation performance.
- Cassini Venus–Venus–Earth–Jupiter gravity-assist navigation design.
- Juno Earth gravity assist and Jupiter arrival navigation covariance.
- Deep Space Network Doppler, range, and Delta-DOR accuracy and systematic-error budgets.
- Low-thrust trajectory-correction calibration, minimum impulse bit, thrust misalignment, and post-burn reconstruction.
- Stellar radial velocity, proper-motion covariance, astrometric acceleration, binary companions, and Galactic orbit uncertainty over 100 kyr.

These are **search targets**, not claimed reviewed references.

## 10. Concrete next calculation

Define a reference case: a Sun-like source, Jupiter flyby, 100 kyr post-flyby coast, 1/10/100 AU target radii, and a target star with a fully specified 6D state/covariance. Run:

1. A patched-conic grid over Jupiter B-plane radius and azimuth.
2. Finite-difference \(\partial\mathbf v_{\rm out}/\partial(B_T,B_R,t,v_\infty)\).
3. Map outbound velocity covariance into 100 kyr miss covariance.
4. Allocate a fraction of total miss budget to burn error, Jupiter ephemeris, departure-state knowledge, target-star motion, and unmodeled forces.
5. Infer the maximum allowable thrust calibration, pointing error, timing jitter, and tracking uncertainty for each target radius.
6. Validate selected trajectories with full N-body propagation and Monte Carlo.

**Critical research decision:** If target-star position uncertainty exceeds the target encounter radius by orders of magnitude, the mission should prioritize better target astrometry, a broader distributed swarm, a shorter coast, or late corrections **before** investing in sub-mm/s burn precision.

## 11. Connection to capture

A successful stellar encounter is not stellar capture. In a star-only two-body model, a positive-energy arrival remains unbound. The braking/capture paper addresses additional energy-exchange mechanisms: [Interstellar Braking and Capture](../../Braking_and_Capture/README.md). Optimize gravity-assist departure trajectories for both the target **position** and the target **relative arrival speed**, because passive planetary capture is sensitive to arrival speed.

## 12. References and evidence status

This paper combines **derived first-order calculations**, **published navigation documentation**, and **proposed numerical research**. Values derived from the free-coast approximation are not mission performance claims. Before publication, verify bibliographic details for every book and retrieve original navigation reports with measured B-plane residuals and maneuver reconstruction data.
