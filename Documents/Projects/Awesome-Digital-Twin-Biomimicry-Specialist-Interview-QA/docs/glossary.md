# Glossary: Digital Twin Biomimicry Terminology

## Terms A–M

**ALE (Arbitrary Lagrangian-Eulerian)** – FSI mesh formulation allowing fluid mesh to move independently of both fluid material and solid boundary, maintaining mesh quality during large structural deformations.

**ASME V&V 40** – Standard framework for verification and validation of computational models in medical device contexts; establishes risk-proportionate validation rigor requirements.

**BESO (Bi-Directional Evolutionary Structural Optimization)** – Topology optimization method iteratively adding material where stresses are high and removing where stresses are low.

**Biphasic model** – Continuum model representing biological tissue as two interpenetrating phases (solid matrix + interstitial fluid); essential for cartilage, bone, and other fluid-saturated tissues.

**Coarse-grained MD** – Molecular dynamics method grouping atoms into "beads" with effective interactions, enabling simulation of larger systems/longer timescales than all-atom MD.

**Digital twin** – A computational model maintaining persistent bidirectional real-time synchronization with its physical counterpart, tracking a specific physical instance's state over its operational lifetime.

**Domain decomposition** – HPC parallelization strategy partitioning a simulation domain across multiple processors with inter-partition boundary communication via MPI.

**EnKF (Ensemble Kalman Filter)** – Data assimilation algorithm representing state probability distribution as an ensemble of model realizations; handles nonlinear systems and high-dimensional states.

**FEA (Finite Element Analysis)** – Numerical method for solving PDEs over complex geometries by discretizing the domain into finite elements with polynomial approximation functions.

**FSI (Fluid-Structure Interaction)** – Computational simulation of coupled fluid dynamics and structural mechanics when strong mutual interaction exists between fluid and deforming structure.

**HGO (Holzapfel-Gasser-Ogden) model** – Fiber-reinforced hyperelastic constitutive model widely used for arterial wall simulation, capturing anisotropy from collagen fiber architecture.

**Homogenization** – Scale-bridging method simulating a representative volume element at fine scale to extract effective macroscale constitutive properties.

**Hyperelastic model** – Large-deformation elastic constitutive model derived from a strain energy density function; used for biological soft tissues under quasi-static loading.

---

## Terms N–Z

**Particle filter (Sequential Monte Carlo)** – Data assimilation method representing state distribution as weighted particles; handles non-Gaussian distributions but suffers weight degeneracy in high dimensions.

**PINN (Physics-Informed Neural Network)** – Neural network trained with physics residual loss terms enforcing governing PDEs; enables state inference in unobservable biological regions.

**QLV (Quasi-Linear Viscoelasticity)** – Constitutive model framework (Fung) for time-dependent biological soft tissue mechanics combining elastic and viscous response terms.

**Representative Volume Element (RVE)** – A material volume element large enough to statistically represent the heterogeneous microstructure but small enough relative to macro-scale structures.

**SIMP (Solid Isotropic Material with Penalization)** – The most widely-used topology optimization method; uses penalized density design variables to find optimal binary (solid/void) material distribution.

**Topology optimization** – Computational method determining the optimal material distribution within a design domain to minimize a structural objective subject to constraints.

**Wolff's Law** – The biological principle that trabecular bone architecture aligns with the principal stress directions, continuously remodeling to maintain this alignment throughout life.

---

## Abbreviations Reference

| Abbr | Full Form |
|------|-----------|
| ALE | Arbitrary Lagrangian-Eulerian |
| CFD | Computational Fluid Dynamics |
| COU | Context of Use |
| DIC | Digital Image Correlation |
| EnKF | Ensemble Kalman Filter |
| FEA | Finite Element Analysis |
| FFR | Fractional Flow Reserve |
| FSI | Fluid-Structure Interaction |
| GNN | Graph Neural Network |
| HGO | Holzapfel-Gasser-Ogden |
| HPC | High-Performance Computing |
| MD | Molecular Dynamics |
| MPI | Message Passing Interface |
| PINN | Physics-Informed Neural Network |
| QLV | Quasi-Linear Viscoelasticity |
| RVE | Representative Volume Element |
| SIMP | Solid Isotropic Material with Penalization |
| UQ | Uncertainty Quantification |

---

**Note:** This glossary is not exhaustive. Refer to topic files and primary sources for authoritative definitions.
