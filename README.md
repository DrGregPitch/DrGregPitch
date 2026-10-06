Physical-organic chemist (PhD) building computational chemistry tools and machine-learning models.

**[glass](https://github.com/DrGregPitch/glass)** · [chemistryconsole.glass](https://chemistryconsole.glass)
A live web console for chemical identity, structure, and spectra. It cross-checks names against SMILES with OPSIN, numbers structures with IUPAC locants, and predicts ¹H/¹³C NMR (nmrshiftdb2 HOSE codes), IR and UV–Vis. Vibrational normal modes and electronic structure come from GFN2-xTB; NMR shielding and frontier-orbital surfaces from PySCF at Hartree–Fock. Every method states its own scope and typical error.

**[MLIP1](https://github.com/DrGregPitch/MLIP1)**
Active-learning fine-tuning of a MACE interatomic potential against real DFT (PBE0/def2-SVP). A committee picks which configurations to label; on out-of-distribution configurations this lowers worst-case (p90) force error 24–55% versus random at the same labeling budget, winning all six paired restarts at every budget. Relabelling with DFT also showed that MACE-OFF, which carries no short-range repulsive term, saturates on compressed geometries — so the force filter built on its predictions had never once fired.

**[SMPro1](https://github.com/DrGregPitch/SMPro1)**
Evaluation for drug-discovery models: scaffold and cluster splits for property prediction, cold drug/target/both splits for binding affinity, and ligand-only / protein-only baselines to separate memorization from real signal.

**[polytools](https://github.com/DrGregPitch/polytools)**
Polymer property prediction, from linear baselines up to a message-passing GNN, with calibrated uncertainty on non-random splits. The point is honest evaluation: on a real polymer dataset the same gradient-boosting model that scores R² 0.94 on a random split collapses to a negative R² when asked to extrapolate beyond the training range — the gap a single random-split score hides.

**[formulate](https://github.com/DrGregPitch/formulate)**
Active learning for formulation: a surrogate and acquisition loop that reaches within 10% of the best measured conductivity in ~10–13 experiments where random screening needs ~30, across 6,949 literature-measured conductivities (median over 20 restarts). Uses polytools as the surrogate and copolybench as the oracle.

**[copolybench](https://github.com/DrGregPitch/copolybench)**
A benchmark for when copolymer sequence matters, not just composition. Composition-only features stay flat across a 130 °C range driven by blockiness; first-order sequence statistics cut that error about 40% (and ~5% on a held-out comonomer-pair split).

pitch.gregory@gmail.com
