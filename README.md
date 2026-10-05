Physical-organic chemist (PhD) building computational chemistry tools and machine-learning models.

**[glass](https://github.com/DrGregPitch/glass)** · [chemistryconsole.glass](https://chemistryconsole.glass)
A live web console for chemical identity, structure, and spectra. It cross-checks names against SMILES with OPSIN, numbers structures with IUPAC locants, and predicts ¹H/¹³C NMR (nmrshiftdb2 HOSE codes, held-out ¹³C MAE 2.75 ppm), IR and UV–Vis. Vibrational normal modes and electronic structure come from GFN2-xTB; NMR shielding and frontier-orbital surfaces from PySCF at Hartree–Fock. Every method states its own scope and typical error.

**[MLIP1](https://github.com/DrGregPitch/MLIP1)**
Active-learning fine-tuning of a MACE interatomic potential. A committee picks which configurations to label; on out-of-distribution configurations this lowers worst-case (p90) force error 26–59% versus random at the same labeling budget, winning all six paired restarts at every budget.

**[SMPro1](https://github.com/DrGregPitch/SMPro1)**
Evaluation for drug-discovery models: scaffold and cluster splits for property prediction, cold drug/target/both splits for binding affinity, and ligand-only / protein-only baselines to separate memorization from real signal.

**[polytools](https://github.com/DrGregPitch/polytools)**
Polymer property prediction, from linear baselines up to a message-passing GNN, with calibrated uncertainty. On glass-transition data the same model scores 48 °C RMSE on a random split and 126 °C on a scaffold split.

**[formulate](https://github.com/DrGregPitch/formulate)**
Active learning for formulation: a surrogate and acquisition loop that finds a top-decile solid-polymer electrolyte in ~10–13 experiments where random screening needs 30, on 6,949 literature-measured conductivities (median over 20 restarts). On a controlled synthetic oracle the margin is wider still. Uses polytools as the surrogate and copolybench as the oracle.

**[copolybench](https://github.com/DrGregPitch/copolybench)**
A benchmark for when copolymer sequence matters, not just composition. Composition-only features stay flat across a 130 °C range driven by blockiness; first-order sequence statistics cut that error about 60%.

pitch.gregory@gmail.com
