# Google_Quantum_Deep_Learning_Training
Most of my Studies on https://quantumai.google/education

---

## Key sources in context

The sources behind the notebooks in this repository, each tied to the file it supports.

- **B31.** Google Quantum AI. *Educational Resources.* [quantumai.google/resources](https://quantumai.google/resources)  
  *In context:* the live home of the Google Quantum AI study material named above; the older quantumai.google/education address now returns "not found".
- **B18.** Cirq Developers. *Cirq.* Zenodo concept DOI [10.5281/zenodo.4062499](https://doi.org/10.5281/zenodo.4062499); docs at [quantumai.google/cirq](https://quantumai.google/cirq)  
  *In context:* `copy_of_basics.ipynb` is the official "Cirq basics" tutorial: qubits, gates, moments, simulation and parameter sweeps.
- **B19.** Broughton, Michael; Verdon, Guillaume; McCourt, Trevor; et al. "TensorFlow Quantum: A Software Framework for Quantum Machine Learning." arXiv:2003.02989, 2020. [arxiv.org/abs/2003.02989](https://arxiv.org/abs/2003.02989)  
  *In context:* `Copy_of_hello_many_worlds.ipynb` is TFQ's "Hello, many worlds" tutorial, which turns Cirq circuits into tensors and trains a hybrid quantum-classical Keras model.
- **B24.** Farhi, Edward; Neven, Hartmut. "Classification with Quantum Neural Networks on Near Term Processors." arXiv:1802.06002, 2018. [arxiv.org/abs/1802.06002](https://arxiv.org/abs/1802.06002)  
  *In context:* the parameterized-circuit model family that the hello-many-worlds notebook builds on in sections 1.1 and 2.
- **B27.** McClean, Jarrod R.; Boixo, Sergio; Smelyanskiy, Vadim N.; Babbush, Ryan; Neven, Hartmut. "Barren plateaus in quantum neural network training landscapes." *Nature Communications* 9: 4812, 2018. DOI: [10.1038/s41467-018-07090-4](https://doi.org/10.1038/s41467-018-07090-4)  
  *In context:* the main caution for scaling up the trainable circuits in the hello-many-worlds notebook: gradients can vanish as qubit count grows.
- **B23.** Preskill, John. "Quantum Computing in the NISQ era and beyond." *Quantum* 2: 79, 2018. DOI: [10.22331/q-2018-08-06-79](https://doi.org/10.22331/q-2018-08-06-79)  
  *In context:* coined the "Noisy Intermediate Scale Quantum (NISQ)" term used in the hello-many-worlds introduction, and explains why the notebook models qubit miscalibration.
- **B21.** Rubin, Nicholas C.; Gunst, Klaas; White, Alec; Freitag, Leon; et al. "The Fermionic Quantum Emulator." arXiv:2104.13944, 2021. [arxiv.org/abs/2104.13944](https://arxiv.org/abs/2104.13944)  
  *In context:* the paper behind `docs/fqe/guide/introduction.ipynb`, from the OpenFermion-FQE documentation.

The B-numbers (B18, B19, B21, B23, B24, B27, B31) refer to the full annotated bibliography in the private [merwin-flagship-projects](https://github.com/davidmerwin/merwin-flagship-projects/blob/main/bibliography/ANNOTATED_BIBLIOGRAPHY.md) repository, which requires access. Each source is cited for background and method; none is used to claim a quantum advantage.
