# Google_Quantum_Deep_Learning_Training
Most of my Studies on https://quantumai.google/education

---

## Key sources in context

The sources behind the notebooks in this repository, written as a compact annotated bibliography. Each one is tied to the file it supports. None is used to claim a quantum advantage. <sup>[E1](#en1)</sup>

**How to read each entry.** The *caption*, *metadata*, *descriptors*, *tags* and *labels* form the catalog card. The *abstract*, *gloss*, *commentary* (with its *elucidation* and *exposition*), *exegesis* and *critique* are the reading. *Marginalia* point to files in this repository, *scholia* compare the sources with each other, and each entry has one *footnote*. The anchors (`#b11`, `#b11-fn`) are the *markup*. Code comments, docstrings, directives and decorators in this repository are listed after the entries.

**Sources:** [B31](#b31) · [B22](#b22) · [B18](#b18) · [B28](#b28) · [B19](#b19) · [B24](#b24) · [B38](#b38) · [B27](#b27) · [B23](#b23) · [B21](#b21) <sup>[E2](#en2)</sup>

<a id="b31"></a>

### B31 · Educational Resources

> **Caption.** Google Quantum AI's live learning hub.

**Metadata.** Google Quantum AI (2026). *Web page, accessed 10 November 2026*. Web page. [quantumai.google/resources](https://quantumai.google/resources). Verified 10 Nov 2026.<br>
**Descriptors.** Curriculum · Gate-model computing · **Tags.** `google-quantum-ai` `tutorials` · **Labels.** `evidence:curriculum` `role:curriculum` `type:web-page` `status:verified`

- **Abstract.** Hub for Google Quantum AI tutorials and learning material on Cirq, qsim, OpenFermion and quantum basics.
- **Gloss.** *qsim*: Google's high-performance state-vector simulator.
- **Commentary.** The live home of the Google Quantum AI study material. *Elucidation:* The address at the top of this README (quantumai.google/education) now returns "not found". This is its current replacement. *Exposition:* Tutorial-first learning path from circuits to simulators to applications.
- **Exegesis.** A living web page; content can change without notice, and it is not research evidence.<sup>[1](#b31-fn)</sup>
- **Critique.** Vendor curriculum and a living page, so links rot (the old /education address already returns 404). Good for orientation; pair with B22 for depth and with B18's docs for current APIs.
- **Marginalia.**
  - `README.md`: The first line still points to the old /education address and is left unchanged; use quantumai.google/resources instead.
  - `copy_of_basics.ipynb`: Its 'View on QuantumAI' button links into this hub.
- **Scholia.** [B18](#b18): The Cirq docs are part of this hub. [B22](#b22): Textbook depth behind the tutorials.
- **Footnote.** <a id="b31-fn"></a>¹ Checked 10 Nov 2026: /resources returns 200 and /education returns 404.
- **In context.** The curriculum source for every notebook here.

<a id="b22"></a>

### B22 · Quantum Computation and Quantum Information

> **Caption.** The standard textbook; the notation every course assumes.

**Metadata.** Michael A. Nielsen, Isaac L. Chuang (2010). *Cambridge University Press, 10th anniversary edition*. Book. DOI: [10.1017/CBO9780511976667](https://doi.org/10.1017/CBO9780511976667). Verified 10 Nov 2026.<br>
**Descriptors.** Gate-model computing · Curriculum · **Tags.** `textbook` `dirac-notation` `error-correction` · **Labels.** `evidence:book` `role:foundation` `type:book` `status:verified`

- **Abstract.** The standard textbook on qubits, gates, quantum algorithms, noise, error correction and quantum information theory.
- **Gloss.** *Density matrix*: Representation of mixed quantum states, needed to describe noise. *Universal gate set*: A finite set of gates that approximates any unitary.
- **Commentary.** The textbook whose notation the tutorials assume. *Elucidation:* When `copy_of_basics.ipynb` writes gates, moments and measurements, Nielsen and Chuang give the underlying definitions. *Exposition:* Builds from linear algebra and postulates to circuits, algorithms (Shor, Grover), noise channels and codes.
- **Exegesis.** A textbook; its 2010 edition predates NISQ-era practice (B23) and modern QML, and it does not cover annealing.<sup>[1](#b22-fn)</sup>
- **Critique.** The 10th-anniversary edition adds a new introduction but keeps the 2000 text, so error correction and algorithms stop around 2000. There is nothing on annealing, variational methods or QML. Dense for self-study without exercises worked in a group.
- **Marginalia.**
  - `copy_of_basics.ipynb`: 'Create a circuit to generate a Bell State' is the textbook's first entangling example.
  - `Copy_of_hello_many_worlds.ipynb`: 'Calculate a state vector with a=0.5 and b=-0.5' uses the textbook's state-vector notation.
- **Scholia.** [B23](#b23): How the outlook changed for noisy hardware. [B18](#b18): The software that implements these gates.
- **Footnote.** <a id="b22-fn"></a>¹ 10th anniversary edition (2010). Crossref dates the online release to 2012.
- **In context.** The reference text behind both notebooks.

<a id="b18"></a>

### B18 · Cirq

> **Caption.** Google's circuit framework under TFQ and OpenFermion.

**Metadata.** Cirq Developers (2026). *Zenodo software record (concept DOI)*. Software. DOI: [10.5281/zenodo.4062499](https://doi.org/10.5281/zenodo.4062499). Verified 10 Nov 2026.<br>
**Descriptors.** Software toolchain · Gate-model computing · **Tags.** `cirq` `gridqubit` `sycamore-gate` `simulation` · **Labels.** `evidence:software` `role:tool` `type:software` `status:verified`

- **Abstract.** Open-source Python framework for writing, simulating and running quantum circuits on near-term devices, with device-aware qubit and gate models.
- **Gloss.** *GridQubit*: A qubit addressed by (row, column) on a 2D device layout. *Moment*: A time slice of simultaneous operations.
- **Commentary.** The circuit framework used in both notebooks. *Elucidation:* `copy_of_basics.ipynb` builds `cirq.GridQubit(5, 6)` and Sycamore gates, so its qubits follow a real device layout. *Exposition:* Circuits are lists of Moments of Operations on Qubits; simulators and devices accept the same object.
- **Exegesis.** The concept DOI cites the *software*, always resolving to the newest version. It does not pin a version; cite a version DOI for reproducibility.<sup>[1](#b18-fn)</sup>
- **Critique.** Device support evolves; tutorial copies age.
- **Marginalia.**
  - `copy_of_basics.ipynb`: A copy of the official 'Cirq basics' tutorial, with its Apache-2.0 header kept.
  - `Copy_of_hello_many_worlds.ipynb`: 'Create two qubits' and the parameterised circuits are Cirq objects.
- **Scholia.** [B19](#b19): TFQ wraps these circuits as tensors. [B28](#b28): Where the Sycamore gate comes from.
- **Footnote.** <a id="b18-fn"></a>¹ The concept DOI always resolves to the newest release. Cite a version DOI if you need reproducibility.
- **In context.** The framework behind `copy_of_basics.ipynb`.

<a id="b28"></a>

### B28 · Quantum supremacy using a programmable superconducting processor

> **Caption.** Sycamore's random-circuit milestone and how it was tested.

**Metadata.** Frank Arute, Kunal Arya, Ryan Babbush, et al. (2019). *Nature 574(7779): 505–510*. Journal article. DOI: [10.1038/s41586-019-1666-5](https://doi.org/10.1038/s41586-019-1666-5). Verified 10 Nov 2026.<br>
**Descriptors.** Gate-model computing · Benchmarking · **Tags.** `sycamore` `random-circuit-sampling` `milestone` · **Labels.** `evidence:peer-reviewed` `role:hardware-context` `type:journal-article` `status:verified`

- **Abstract.** Reports sampling from random circuits on the 53-qubit Sycamore processor and argues the task would take classical supercomputers far longer at the time.
- **Gloss.** *Cross-entropy benchmarking*: Fidelity estimate comparing sampled bitstrings with ideal probabilities.
- **Commentary.** The Sycamore experiment. *Elucidation:* It explains the 'Sycamore gate, which is supported on Google hardware' used in `copy_of_basics.ipynb`. *Exposition:* Run deep random circuits, sample bitstrings, estimate fidelity with XEB, and compare with classical simulation cost estimates.
- **Exegesis.** Claims a *specific sampling task* beyond practical classical simulation *as estimated in 2019*. It makes no claim about useful applications.<sup>[1](#b28-fn)</sup>
- **Critique.** Improved tensor-network simulations later narrowed the classical cost estimate substantially.
- **Marginalia.**
  - `copy_of_basics.ipynb`: Operations built with the Sycamore gate on GridQubits mirror this processor.
- **Scholia.** [B18](#b18): The software side of the same hardware. [B23](#b23): The NISQ framing of what this result means.
- **Footnote.** <a id="b28-fn"></a>¹ 53 working qubits in the 2019 experiment.
- **In context.** Hardware context for the GridQubit and Sycamore-gate cells.

<a id="b19"></a>

### B19 · TensorFlow Quantum: A Software Framework for Quantum Machine Learning

> **Caption.** Cirq circuits as Keras layers: hybrid quantum-classical ML.

**Metadata.** Michael Broughton, Guillaume Verdon, Trevor McCourt, et al. (2020). *arXiv:2003.02989*. Preprint. [arxiv.org/abs/2003.02989](https://arxiv.org/abs/2003.02989). Verified 10 Nov 2026.<br>
**Descriptors.** Software toolchain · Quantum machine learning · **Tags.** `tfq` `keras` `pqc` `hello-many-worlds` · **Labels.** `evidence:preprint` `role:tool` `type:preprint` `status:verified`

- **Abstract.** Describes TensorFlow Quantum's design for representing circuits as tensors, differentiating parameterised circuits, and combining them with classical Keras models, with example applications.
- **Gloss.** *PQC*: Parameterised quantum circuit, the trainable layer. *Parameter shift*: A rule for exact gradients of circuit expectation values.
- **Commentary.** The software spine of `Copy_of_hello_many_worlds.ipynb`. *Elucidation:* The notebook turns Cirq circuits into tensors and trains a hybrid model that corrects a simulated miscalibration: a PQC controlled by a classical network. *Exposition:* Encode data into circuits, apply a PQC, measure expectation values, and back-propagate through them alongside classical layers.
- **Exegesis.** A software paper: it shows *what can be built*, not that quantum layers improve accuracy.<sup>[1](#b19-fn)</sup>
- **Critique.** TFQ releases can lag current TensorFlow versions; check compatibility before running a copied notebook.
- **Marginalia.**
  - `Copy_of_hello_many_worlds.ipynb`: 'TFQ layer for classically controlled circuits' and 'The full Keras model is built from our layers' are the paper's design in code.
  - `Copy_of_hello_many_worlds.ipynb`: 'Update package resources to account for version changes': copied notebooks need dependency care.
- **Scholia.** [B24](#b24): The model family it implements. [B27](#b27): Why such models can stall as they grow.
- **Footnote.** <a id="b19-fn"></a>¹ Tutorial: tensorflow.org/quantum/tutorials/hello_many_worlds.
- **In context.** The library behind `Copy_of_hello_many_worlds.ipynb`.

<a id="b24"></a>

### B24 · Classification with Quantum Neural Networks on Near Term Processors

> **Caption.** Parameterised circuits as binary classifiers.

**Metadata.** Edward Farhi, Hartmut Neven (2018). *arXiv:1802.06002*. Preprint. [arxiv.org/abs/1802.06002](https://arxiv.org/abs/1802.06002). Verified 10 Nov 2026.<br>
**Descriptors.** Quantum machine learning · Variational algorithms · **Tags.** `qnn` `binary-classification` `mnist` · **Labels.** `evidence:preprint` `role:foundation` `type:preprint` `status:verified`

- **Abstract.** Proposes a quantum neural network in which a parameterised circuit acts on an input state and a measured readout qubit gives the class label; tested in simulation, including downsampled MNIST.
- **Gloss.** *Readout qubit*: The qubit measured to produce the prediction.
- **Commentary.** Parameterised circuits used as classifiers. *Elucidation:* It is the model family the hello-many-worlds notebook works up to: trainable circuit parameters fed by a classical controller. *Exposition:* Encode input as a quantum state, apply trainable unitaries, measure a Pauli on the readout qubit, minimise a loss over parameters.
- **Exegesis.** Shows *the model can learn small tasks in simulation*. It does not show an advantage over classical networks.<sup>[1](#b24-fn)</sup>
- **Critique.** Simulated, small-scale; trainability caveats arrived soon after (B27).
- **Marginalia.**
  - `Copy_of_hello_many_worlds.ipynb`: 'Parameters that the classical NN will feed values into' is the QNN parameter vector.
- **Scholia.** [B27](#b27): The counterweight from the same lab, the same year. [B38](#b38): Where QNNs sit among variational algorithms.
- **Footnote.** <a id="b24-fn"></a>¹ TFQ's MNIST tutorial cites this approach.
- **In context.** The model idea behind sections 1.1 and 2 of the notebook.

<a id="b38"></a>

### B38 · Variational quantum algorithms

> **Caption.** The review of VQAs: QAOA, VQE, QNNs and their obstacles.

**Metadata.** M. Cerezo, Andrew Arrasmith, Ryan Babbush, et al. (2021). *Nature Reviews Physics 3(9): 625–644*. Journal article. DOI: [10.1038/s42254-021-00348-9](https://doi.org/10.1038/s42254-021-00348-9). Verified 10 Nov 2026.<br>
**Descriptors.** Variational algorithms · Trainability · Quantum machine learning · **Tags.** `vqe` `qaoa` `ansatz` `error-mitigation` · **Labels.** `evidence:peer-reviewed` `role:foundation` `type:journal-article` `status:verified`

- **Abstract.** Reviews variational quantum algorithms: cost functions, ansatz design, optimisers, applications from chemistry to optimization and ML, and challenges including barren plateaus, noise and error mitigation.
- **Gloss.** *Ansatz*: The parameterised circuit template. *Error mitigation*: Post-processing that reduces noise bias without full error correction.
- **Commentary.** The review that ties QNNs, QAOA and VQE into one family. *Elucidation:* It shows that the notebook's training loop is a variational quantum algorithm: the circuit evaluates a cost and a classical optimizer updates the parameters. *Exposition:* A quantum circuit evaluates a cost; a classical optimiser updates parameters; the loop repeats. Everything hinges on cost design and trainability.
- **Exegesis.** The review presents VQAs as *leading candidates* for near-term advantage. It does not report a demonstrated practical advantage.<sup>[1](#b38-fn)</sup>
- **Critique.** A 2021 snapshot; trainability theory has advanced since.
- **Marginalia.**
  - `Copy_of_hello_many_worlds.ipynb`: The `model.fit` call is the classical half of a VQA loop.
- **Scholia.** [B24](#b24): One member of the family. [B27](#b27): The main obstacle this review discusses.
- **Footnote.** <a id="b38-fn"></a>¹ Crossref lists 11 authors.
- **In context.** A map for what to study after the notebook.

<a id="b27"></a>

### B27 · Barren plateaus in quantum neural network training landscapes

> **Caption.** Gradients that vanish exponentially: the QML counterweight.

**Metadata.** Jarrod R. McClean, Sergio Boixo, Vadim N. Smelyanskiy, et al. (2018). *Nature Communications 9: 4812*. Journal article. DOI: [10.1038/s41467-018-07090-4](https://doi.org/10.1038/s41467-018-07090-4). Verified 10 Nov 2026.<br>
**Descriptors.** Trainability · Quantum machine learning · **Tags.** `barren-plateau` `counterevidence` `random-circuits` · **Labels.** `evidence:peer-reviewed` `role:caution` `type:journal-article` `status:verified` `claim:counterweight`

- **Abstract.** Shows that for sufficiently random parameterised circuits, gradient variance decays exponentially in qubit number, making gradient-based training impractical at scale.
- **Gloss.** *Barren plateau*: A flat loss landscape where gradients are exponentially small. *2-design*: A circuit ensemble that mimics random unitaries up to second moments.
- **Commentary.** Vanishing gradients: the main caution for scaling up trainable circuits. *Elucidation:* The one- and two-qubit circuits in the notebook train easily. This paper explains why that ease may not survive many qubits and deep random circuits. *Exposition:* Random deep circuits concentrate expectation values; derivatives concentrate around zero, so the optimiser sees noise.
- **Exegesis.** Applies to *circuits that form approximate 2-designs*. It does not say all QNNs are untrainable; structured or shallow circuits may escape.<sup>[1](#b27-fn)</sup>
- **Critique.** Follow-ups (e.g., B38's summary) refine conditions: cost locality, depth and noise all matter.
- **Marginalia.**
  - `Copy_of_hello_many_worlds.ipynb`: Small examples train well; do not extrapolate the loss curves to larger circuits.
- **Scholia.** [B24](#b24): The model it limits. [B38](#b38): Its follow-ups, summarised.
- **Footnote.** <a id="b27-fn"></a>¹ An early draft DOI for this paper was wrong. The one shown here was verified on Crossref.
- **In context.** The caution beside every training cell.

<a id="b23"></a>

### B23 · Quantum Computing in the NISQ era and beyond

> **Caption.** The essay that named NISQ and set expectations.

**Metadata.** John Preskill (2018). *Quantum 2: 79*. Journal article. DOI: [10.22331/q-2018-08-06-79](https://doi.org/10.22331/q-2018-08-06-79). Verified 10 Nov 2026.<br>
**Descriptors.** Gate-model computing · Benchmarking · **Tags.** `nisq` `perspective` `expectations` · **Labels.** `evidence:peer-reviewed` `role:caution` `type:journal-article` `status:verified` `claim:counterweight`

- **Abstract.** An influential perspective defining noisy intermediate-scale quantum devices and assessing what they might achieve before full error correction, including optimization and ML, with deliberate caution.
- **Gloss.** *NISQ*: Noisy intermediate-scale quantum: tens to hundreds (now thousands) of qubits without full error correction.
- **Commentary.** The essay that named NISQ. *Elucidation:* The hello-many-worlds introduction uses 'Noisy Intermediate Scale Quantum'. That is why the notebook models qubit miscalibration. *Exposition:* Noise limits circuit depth; useful near-term advantage is possible but must be demonstrated, and error correction remains the long-run route.
- **Exegesis.** Preskill says NISQ devices *may* be useful and are worth exploring; he explicitly does not promise near-term transformative applications.<sup>[1](#b23-fn)</sup>
- **Critique.** A perspective, not data; the qubit-count range has since shifted.
- **Marginalia.**
  - `Copy_of_hello_many_worlds.ipynb`: 'This input is the simulated miscalibration that the model will learn to correct' is NISQ noise, made concrete.
- **Scholia.** [B28](#b28): A NISQ-era milestone. [B38](#b38): The algorithms NISQ invites.
- **Footnote.** <a id="b23-fn"></a>¹ Based on a keynote Preskill gave in December 2017.
- **In context.** The framing for what these notebooks do and do not show.

<a id="b21"></a>

### B21 · The Fermionic Quantum Emulator

> **Caption.** Symmetry-aware emulation of fermionic circuits.

**Metadata.** Nicholas C. Rubin, Klaas Gunst, Alec White, et al. (2021). *arXiv:2104.13944*. Preprint. [arxiv.org/abs/2104.13944](https://arxiv.org/abs/2104.13944). Verified 10 Nov 2026.<br>
**Descriptors.** Software toolchain · Quantum chemistry · **Tags.** `fqe` `emulator` `particle-number-symmetry` · **Labels.** `evidence:preprint` `role:tool` `type:preprint` `status:verified`

- **Abstract.** Presents FQE, an emulator that simulates fermionic quantum circuits efficiently by working in symmetry sectors such as fixed particle number and spin.
- **Gloss.** *Symmetry sector*: Subspace with fixed conserved quantities; restricting to it shrinks the state vector.
- **Commentary.** A symmetry-aware emulator for fermionic circuits. *Elucidation:* `docs/fqe/guide/introduction.ipynb` is copied from this project's documentation. *Exposition:* Store wavefunctions only in the relevant symmetry blocks and apply fermionic operators directly, avoiding the full 2ⁿ qubit space.
- **Exegesis.** Claims *efficiency gains for symmetry-preserving circuits*; not a general-purpose simulator.<sup>[1](#b21-fn)</sup>
- **Critique.** Preprint. Speedups are reported against general-purpose simulators on the authors' own benchmarks, and they shrink for circuits that break particle-number or spin symmetry. Re-run before reusing any timing figure.
- **Marginalia.**
  - `docs/fqe/guide/introduction.ipynb`: Copied FQE guide, with its `#@title` license cell kept.
- **Scholia.** [B18](#b18): FQE plugs into the Cirq and OpenFermion stack. [B38](#b38): Chemistry VQAs are a main use case.
- **Footnote.** <a id="b21-fn"></a>¹ Code: github.com/quantumlib/OpenFermion-FQE.
- **In context.** The source of the `docs/fqe/` material.

### Code annotations in this repository

Where the four code-annotation elements appear in this repository's own files.<sup>[E3](#en3)</sup>

| Element | Example in this repository |
| --- | --- |
| Code comment | `copy_of_basics.ipynb`: `# Create some qubits.`, `# Create a circuit to generate a Bell State:`; `Copy_of_hello_many_worlds.ipynb`: `# The classical neural network layers.` |
| Docstring | None in the copied cells; the tutorials explain code in Markdown cells instead |
| Directive | `#@title Licensed under the Apache License…` in `Copy_of_hello_many_worlds.ipynb` and `docs/fqe/guide/introduction.ipynb` is a Colab form directive (Colab hides the cell behind a title) |
| Decorator | None used in these notebooks |

<a id="excursus"></a>

### Excursus: Two notebooks, one stack

The two notebooks climb one ladder. `copy_of_basics.ipynb` teaches the bottom rung: qubits on a device grid, gates such as the Sycamore gate, moments, simulation ([B18](#b18), [B22](#b22), [B28](#b28)). `Copy_of_hello_many_worlds.ipynb` adds learning. Circuits become tensors, a classical network chooses circuit parameters, and Keras trains the pair to undo a simulated miscalibration ([B19](#b19), [B24](#b24)). That loop is a variational quantum algorithm in miniature ([B38](#b38)), and the miscalibration is the NISQ problem in miniature ([B23](#b23)). What the notebooks do not show matters as much. They run on a simulator, with one or two qubits, where gradients are healthy. At scale, barren plateaus ([B27](#b27)) and noise change the picture, so these notebooks are study material, not evidence that quantum models learn better.

### Endnotes

1. <a id="en1"></a>**Verification.** Every source was checked on 10 November 2026 (America/New_York). DOIs were resolved at doi.org and matched against Crossref; preprints were checked on arXiv, the patent on Google Patents, and documentation and course pages on the live page.
2. <a id="en2"></a>**Numbering.** B-numbers are stable identifiers shared across David Merwin's annotated bibliographies, so a source keeps the same number in every repository. Gaps in the numbering are expected.
3. <a id="en3"></a>**Scope.** Sources are cited for background and method. None is used to claim a quantum advantage. The code-annotation table describes files as they are; no code was changed.

### P.S.

P.S. Both notebooks are copies of official tutorials, kept with their licence headers. Their study value is in re-running them, and what they show is how the tools work.
