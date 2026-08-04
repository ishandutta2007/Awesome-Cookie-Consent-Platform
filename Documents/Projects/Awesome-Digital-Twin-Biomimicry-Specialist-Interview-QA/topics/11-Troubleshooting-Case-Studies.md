# Topic 11: Troubleshooting & Case Studies

## Overview
Diagnosing simulation failures, model-experiment mismatches, and structured problem-solving for common digital twin biomimicry engineering scenarios.

---

### Q1: A patient-specific cardiac FEA model shows excellent agreement with echocardiographic geometry data but substantially overpredicts peak ventricular wall stress compared to indirect clinical indicators (biomarker levels, symptoms) suggesting the stress should be lower. How do you diagnose this discrepancy?

**A:**
**Systematic diagnostic approach:**

1. **Distinguish between model geometry being correct and model mechanics being correct — these are independent:** The fact that the FEA geometry matches echocardiographic geometry does not mean the model's mechanical behavior is correct. A geometrically-matched model can still have: incorrect material stiffness (affecting strain-stress relationship), incorrect boundary conditions (incorrect representation of pericardial constraint, adjacent tissue interaction, or residual stress state), incorrect active contractile force model (incorrect calcium transient model, cross-bridge kinetics, or myofiber orientation field), or incorrect loading conditions (incorrect representation of preload/afterload, intraventricular pressure boundary conditions). Geometry validation and mechanical validation are completely independent — solving Q1 requires focusing on the mechanical model components that affect stress predictions without affecting geometry.

2. **Identify the most likely mechanical candidates for stress overprediction:**
   - **Material stiffness over-specification (most common):** If myocardial passive stiffness parameters are set to published "average" values rather than patient-specific values, and this patient has a stiffer-than-average myocardium (e.g., due to fibrosis from prior MI), the model may use an appropriate average stiffness but this patient's actual tissue is stiffer — paradoxically, for a passive-stiffness dominated model under diastolic loading, stiffer tissue can produce higher wall stress for the same pressure loading. However, for systolic stress, stiffer passive material generally reduces active stress requirements.
   - **Residual stress state incorrect:** Biological tissues are not stress-free at any observable configuration (unlike a machined engineering component). Setting the FEA reference configuration to the measured end-diastolic geometry (zero stress assumed) may substantially misrepresent the actual stress state, introducing systematic stress errors that compound with applied loading.
   - **Active contraction model parameters:** If the active contractile force model is parameterized with published average values rather than patient-specific contractility, and this patient's contractility is higher or lower than average, the computed systolic stress will be correspondingly over- or under-estimated.
   - **Boundary conditions at the base/valves:** How the model constrains the cardiac base (where the valve annuli attach to the fibrous skeleton) substantially affects wall stress distribution — over-constraining the base artificially elevates wall stress; under-constraining allows unrealistic rigid-body motion.

3. **Prioritize investigation by clinical-biological plausibility:**
   Request additional clinical data that can help distinguish these candidates: end-diastolic pressure (for passive stiffness validation), ejection fraction trajectory (for contractility assessment), prior imaging (for residual stress reference configuration estimation). Sensitivity analysis (Topic 08) quantifying how much each uncertain parameter affects the stress prediction guides which parameters warrant most urgent clinical measurement for targeted recalibration.

4. **If clinical-data-supported diagnosis identifies the root cause, update parameter estimate and verify discrepancy is resolved:**
   After recalibration, verify not only that the stress prediction is reduced but that the updated model still correctly predicts the echocardiographic geometry (confirming the recalibration hasn't traded one validation domain for another) and is consistent with other available clinical indicators — a consistent multi-indicator validation, not just resolution of the single discrepancy.

### Q2: Case study — A fluid-structure interaction model of a fish tail fin during swimming predicts thrust force 40% higher than direct force measurement in a flow tank experiment with a physical tail model. How do you systematically investigate this large discrepancy?

**A:**
**Systematic investigation:**

1. **First verify whether the physical experiment and computational model are actually modelling the same thing:**
   - **Geometry match:** Is the physical tail model geometry identical to the FSI model geometry? Any manufacturing deviation from CAD (especially at thin trailing edge sections where FSI is most sensitive) can produce substantial thrust differences.
   - **Material properties match:** Is the physical tail model material actually represented by the FSI model's constitutive model? Physical tail models often use silicone or hydrogel materials with viscoelastic properties that simple hyperelastic FSI models may not capture.
   - **Boundary conditions match:** Is the fin root constraint in the experiment (clamped, pinned, or prescribed motion) identical to the FSI model's boundary condition? Root constraint stiffness strongly affects tail deformation and thrust production.
   - **Flow conditions match:** Flow tank experimental conditions (turbulence intensity, flow uniformity, wall proximity effects from finite tank dimensions) may not match the FSI model's assumed idealized incoming uniform flow — flow tank walls and tunnel turbulence can substantially affect measured thrust.

2. **If experiment-model configuration match is confirmed, check FSI-specific numerical issues:**
   - **Added-mass instability:** For flexible structures in fluid with density comparable to structure (aquatic tail: water density ~1000 kg/m³, silicone/fish tissue ~1050 kg/m³), loose FSI coupling can suffer added-mass instability producing nonphysical amplitude amplification — verify FSI coupling strategy (tight vs. loose) and check if solution is artificially oscillating.
   - **Mesh resolution in wake:** If the downstream wake mesh is too coarse, numerical diffusion can artificially smear the shed vortex structures that carry momentum — run mesh convergence study specifically focused on thrust prediction (not just wall stress or near-body pressure, which may converge at coarser mesh than far-field wake quantities).
   - **Turbulence model appropriateness:** If Reynolds number is in the transitional or turbulent regime and an inappropriate turbulence model (or no turbulence model) is used, flow separation prediction can be substantially wrong, affecting thrust prediction.

3. **If numerical issues are resolved, consider fundamental constitutive model mismatch:**
   - **Viscoelastic vs. hyperelastic for tail material:** Viscoelastic materials (which silicone and fish tissue both are) dissipate energy during oscillation — a purely hyperelastic FSI model loses no energy to material damping, potentially overpredicting thrust by not accounting for energy loss to material hysteresis. Physical testing of the tail material's complex modulus under dynamic loading conditions matching the swimming frequency would characterize this.

4. **Quantify each investigated factor's contribution and report:**
   Rather than stopping when a plausible explanation is identified, systematically quantify each investigated factor's contribution to the discrepancy — enabling a complete "discrepancy budget" accounting for the full 40% difference across identified sources, which is more scientifically rigorous and more useful for informing model improvements than a single identified "most likely" cause.

### Q3–Q13: (Representative additional topics)
- Diagnosing mesh-dependent FEA results and mesh convergence study design
- Root-causing data assimilation divergence in biological digital twin updating
- Investigating topology optimization convergence failure and checkerboard patterns
- Diagnosing unexpected material property variations across a patient cohort
- Troubleshooting multi-scale coupling instabilities (MD-FEA boundary artifacts)
- Investigating HPC parallel simulation results that diverge from serial results (floating-point non-associativity, load imbalance artifacts)
- Root-causing surrogate model accuracy degradation outside training distribution
- Investigating PINN training failure (loss landscape pathologies, competing loss terms)
- Diagnosing sensitivity to constitutive model parameter values in soft tissue FEA
- Handling cases where experimental data and simulation predictions are fundamentally irreconcilable (model structural inadequacy)

---

## Summary
Rigorous troubleshooting of digital twin biomimicry model failures requires systematic isolation of geometry/material/boundary condition/numerical/physics candidates — always verifying that the computational model and physical experiment are actually representing the same system before attributing discrepancies to deeper modeling issues, and building comprehensive discrepancy budgets that account for all identified sources rather than stopping at the first plausible explanation.
