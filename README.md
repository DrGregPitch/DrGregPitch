### Honest machine learning for chemistry, from a physical chemist.

I'm a physical-organic chemist (PhD) building ML that reports the number which survives an honest test, not the one a random split flatters. Chemical datasets are dense with near-duplicate analogues, so a random test set almost always has a close cousin in training — the model interpolates and the score is inflated. The thread through every project below is the same discipline: a molecular property is a free energy over a geometry — a polymer's glass transition, a drug's binding ΔG, the energy a simulation puts on a set of atoms — so the same honest evaluation applies everywhere. Each repo ships a reported baseline, non-random out-of-distribution evaluation, calibrated uncertainty, and one-command reproduction with green CI.

#### Polymers — three repositories that each stand alone and compose into one system

**[polytools](https://github.com/DrGregPitch/polytools)** — *Polymer property prediction, done honestly.*
The *same* model on the *same* Tg data goes from 48 to 126 °C RMSE when only the train/test split changes — the gap a single random-split score hides. A model ladder from linear baselines to a directed message-passing GNN, calibrated uncertainty, a mechanistic error analysis, and a clickable demo.

**[copolybench](https://github.com/DrGregPitch/copolybench)** — *When does copolymer sequence matter?*
The composition-weighted encoding most work defaults to is blind to sequence by construction: it predicts a flat line across a 130 °C swing driven purely by blockiness. A controlled benchmark that measures exactly what that costs — first-order sequence statistics cut error 60%.

**[formulate](https://github.com/DrGregPitch/formulate)** — *Active learning for formulation.*
A surrogate-plus-acquisition loop that chooses which experiment to run next under a budget: it reaches the best formulation in ~16 experiments where random screening needs more than 60. Reuses `polytools` as its surrogate and `copolybench` as its oracle.

#### Small molecules & atomistic simulation — the same discipline, beyond polymers

**[SMPro1](https://github.com/DrGregPitch/SMPro1)** — *Small molecule–protein: leakage measured, not assumed.*
Drug-discovery models look excellent on a random split and fail on the next chemical series a project wants to make. This measures the drop instead of hiding it: property prediction under scaffold and cluster splits, and binding affinity under cold drug / target / both splits with single-sided memorization baselines — because pKd is a free energy and a drug–target pair can leak through either side.

**[MLIP1](https://github.com/DrGregPitch/MLIP1)** — *Active learning for interatomic potentials.*
A committee of fine-tuned [MACE](https://github.com/ACEsuit/mace) foundation models picks which configurations to label with an expensive reference. On the out-of-distribution regime a real molecular-dynamics run actually visits, that cuts worst-case force error 35–62% versus random selection at equal labeling budget — the loop NVIDIA's ALCHEMI is built on, reproduced faithfully on a laptop.

*Five projects, one discipline: measure what the model actually knows.*

#### Tools

**[glass](https://github.com/DrGregPitch/glass)** — *A chemistry web console, live at [chemistryconsole.glass](https://chemistryconsole.glass).*
Verified name↔SMILES cross-checking with IUPAC locant numbering, journal-style depiction, and predicted ¹H/¹³C NMR, IR and UV–Vis spectra with GFN2-xTB vibrational normal modes — the working end of the same chemistry.

<sub>📫 pitch.gregory@gmail.com</sub>
