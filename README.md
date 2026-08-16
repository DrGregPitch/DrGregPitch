### Rigorous, reproducible machine learning for polymers.

Polymers are the underserved corner of ML chemistry. SMILES and the standard cheminformatics stack were built for discrete molecules, and a polymer is a statistical ensemble — so the usual tools run without error and hand back numbers that are quietly wrong. These projects are about doing it honestly instead: each ships with a reported baseline, non-random out-of-distribution evaluation, calibrated uncertainty, and one-command reproduction with green CI.

**[polytools](https://github.com/DrGregPitch/polytools)** — *Polymer property prediction, done honestly.*
The *same* model on the *same* Tg data goes from 48 to 126 °C RMSE when only the train/test split changes — the gap a single random-split score hides. A model ladder from linear baselines to a directed message-passing GNN, calibrated uncertainty, a mechanistic error analysis, and a clickable demo.

**[copolybench](https://github.com/DrGregPitch/copolybench)** — *When does copolymer sequence matter?*
The composition-weighted encoding most work defaults to is blind to sequence by construction: it predicts a flat line across a 130 °C swing driven purely by blockiness. A controlled benchmark that measures exactly what that costs — first-order sequence statistics cut error 60%.

**[formulate](https://github.com/DrGregPitch/formulate)** — *Active learning for formulation.*
A surrogate-plus-acquisition loop that chooses which experiment to run next under a budget: it reaches the best formulation in ~16 experiments where random screening needs more than 60. Reuses `polytools` as its surrogate and `copolybench` as its oracle.

*Three repositories that each stand alone and compose into one system.*

<sub>📫 pitch.gregory@gmail.com</sub>
