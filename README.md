% 西尾 真 / Shin Nishio's profile

I am **Shin Nishio**, a project assistant professor in [Prof. Takahiko Satoh's Group](https://sites.google.com/view/satoh-quantum-lab/) in **Keio University** in Japan 🇯🇵.　I am also a research associate funded by Overseas Research Fellowships of JSPS (海外学振) in [Prof. Dan Browne's Group](https://www.homepages.ucl.ac.uk/~ucapdeb/) in **University College London (UCL)** in UK 🇬🇧. I am physically based in London. 

My interests are: quantum information processing, system software/middleware for quantum computing, fault-tolerant quantum computation,  quantum programming language, quantum error correction codes

* email: parton (at) sfc.wide.ad.jp
* [Google Scholar](https://scholar.google.com/citations?user=gZNt8twAAAAJ&hl=ja)
* ORCiD [0000-0003-2659-5930](https://orcid.org/0000-0003-2659-5930)
* GitHub: [parton-quark](https://github.com/parton-quark)
* Twitter: [\@shin_tsujido](https://twitter.com/shin_tsujido)

## Selected Research Projects
<details><summary> Efficient Quantum Communication with Quantum Multiplexing </summary><div>

**Quantum multiplexing** uses multiple degrees of freedom (DoFs), or multiple modes within a single DoF to encode higher dimensional quantum information onto a single photon. Applying quantum multiplexing to quantum information–processing systems can drastically reduce resource requirements—for example, lowering the gate count of encoding circuits for quantum error-correcting codes (QECCs) [[Physical Review A 107, 032620](https://doi.org/10.1103/PhysRevA.107.032620)] and reducing the number of photons required for QECC-based quantum communication [[Quantum 9, 1613](https://arxiv.org/abs/2406.08832)]. We also analyzed how multiplexing affects error models, showing that it can induce correlated errors. To mitigate this, we showed that permuting physical-qubit assignments to leverage randomness and maximizing the code distance within a single photon are effective.

Efficient implementation of multiple controlled-X gate on a multiplexed photon.
![multiplexing](https://parton-quark.github.io/figures/multiplexed_gate.png)

Quantum communication with multiplexed photons.
![multiplexing](https://parton-quark.github.io/figures/multiplexing_flow.png)
</div></details>

<details><summary> Multiprogramming system for fault-tolerant quatnum computers </summary><div>

**Multiprogramming** achieves high-throughput computing by running multiple programs in parallel. We formally defined multiprogramming for fault-tolerant quantum computing and, for the first time, posed the corresponding online scheduling problem—think like 3D Tetris—for realizing it. Increasing throughput can substantially reduce the cost per program [[arxiv[quant-ph] 2505.06741](https://arxiv.org/abs/2505.06741)]. 
![QM](https://parton-quark.github.io/figures/multiprogramming.png)
</div></details>

<details><summary> Formal Programming Language for Distributed Quantum Computing </summary><div>

A formal programming language specifies the semantics of programs. One representative approach is **operational semantics**, which specifies how a machine executes atomic operations. Based on such semantics, one can design **type systems** that allow users to verify properties (e.g., safety) before execution. We introduced **InQuIR**, the first formal programming language for distributed quantum computing [[arXiv[quant-ph] 2302.00267](https://arxiv.org/abs/2302.00267)]. It also enables fair comparisons of compiler performance.

Type system can proof whether given code can be resulted in **Dead Lock**.
![DeadLock](https://parton-quark.github.io/figures/InQuIR.png)
</div></details>

<details><summary> Compilation and Circuit optimization for Quantum Computing </summary><div>

**Compilation** and circuit optimization are crucial for harnessing the full potential of quantum computers. We proposed a compiler for noisy intermediate-scale quantum (NISQ) devices that takes qubit quality into account so users obtain higher-fidelity results [[ACM Journal on Emerging Technologies in Computing Systems Vol. 16, No. 3](https://dl.acm.org/doi/abs/10.1145/3386162)]. We also formulated the circuit-optimization problem for **defect-braiding-based surface-code fault-tolerant quantum computing** and proved its **computational complexity** [[IEEE Transactions on Quantum Engineering vol. 4, pp. 1-7, 2023](https://doi.org/10.1109/TQE.2023.3251358)].

Error aware compilation for NISQ devices.
![EA](https://parton-quark.github.io/figures/mapping.png)

Defect braiding circuit.
![DB](https://parton-quark.github.io/figures/3d_braiding_circuit.png)
</div></details>

## News
<div class="news-container">
  <iframe src="news.html" title="News" loading="lazy"></iframe>
</div>

## Table of Contents
- [Papers](#papers)
- [Presentations](#presentations)
  - [Invited Talks](#invited-talks)
  - [International Conferences](#international-conferences)
  - [Domestic Conferences, Symposiums and Workshops](#domestic-conferences-symposiums-and-workshops)
- [Professional Background](#professional-background)
  - [Education](#education)
  - [Professional Experience](#professional-experience)
- [Fundings](#fundings)
- [Awards](#awards)
- [Hobby](#hobby)

# Papers
<!-- <details><summary> Categories </summary><div> -->
<span style="background-color:#f6cdcb; color:#99211a; padding:2px 6px; border-radius:4px; font-size:0.85em;">QEC</span> Quantum Error Correction and Fault-tolerant Quantum Computing<br>
<span style="background-color:#e0f7fa; color:#006064; padding:2px 6px; border-radius:4px; font-size:0.85em;">QI</span> Quantum Information<br>
<span style="background-color:#f7caf5; color:#c21fba; padding:2px 6px; border-radius:4px; font-size:0.85em;">SYS</span> System Software and Programming Languages<br>
<span style="background-color:#c4c8ee; color:#6360e1; padding:2px 6px; border-radius:4px; font-size:0.85em;">QML</span> Quantum Machine Learning
<!-- </div></details> -->

### 20. Qubit Loss Inference with Stabilizer Codes without Leakage Detection Units <span style="background-color:#f6cdcb; color:#99211a; padding:2px 6px; border-radius:4px; font-size:0.85em;">QEC</span> <span style="background-color:#f7caf5; color:#c21fba; padding:2px 6px; border-radius:4px; font-size:0.85em;">SYS</span>
<details><summary>Abstract</summary><div>
Qubit loss occurs when the physical carrier of a qubit leaves the computational system without directly revealing the event's location. Such errors are a major obstacle to fault-tolerant quantum computation on platforms including photonic, neutral-atom, and trapped-ion systems. Loss locations are commonly identified using additional hardware operations such as leakage-detection units (LDUs), which introduce space-time overhead and may themselves become a source of error.

We investigate whether qubit loss on stabilizer codes can instead be inferred from syndrome data obtained through standard repeated stabilizer measurements. Under a non-entangling model for gates involving a lost qubit, we derive a sufficient condition for loss detectability in general stabilizer codes. The condition is based on the emergence of anticommutation between stabilizer checks after their support on the lost qubits is removed. By using that condition, we formulate the exact loss-inference problem using the observed set of non-deterministic checks together with its maximum-likelihood formulation. We then relax the problem to the minimum set cover problem with a greedy heuristic algorithm.
We evaluate the resulting inference and loss-correction protocols on the rotated surface code via circuit-level noise simulations for trapped-ion and neutral-atom platforms. On both platforms, inference-based and adaptive protocols reduce the logical error rate relative to a noisy-LDU baseline in the low-to-moderate loss-rate regime relevant to near-term hardware, while requiring fewer space-time overheads.
</div></details>

- **Shin Nishio**, Takeaki Uno, Fumiyoshi Kobayashi, Takahiko Satoh, and Dan E. Browne
- preprint: [arxiv[quant-ph] 2607.29603](https://arxiv.org/abs/2607.29603)

### 19. Anticipating Decoder Side-channel Attacks in Fault-tolerant Quantum Computers <span style="background-color:#f6cdcb; color:#99211a; padding:2px 6px; border-radius:4px; font-size:0.85em;">QEC</span> <span style="background-color:#f7caf5; color:#c21fba; padding:2px 6px; border-radius:4px; font-size:0.85em;">SYS</span>
<details><summary>Abstract</summary><div>
As quantum computing emerges as an applied technology, there is a growing need to protect quantum computers against information security attacks. This work identifies a new class of side-channel attacks against fault-tolerant quantum computers, in which the syndrome data that is sent to the decoder system is used to infer which computation (logical circuit) is taking place on the quantum computer. Our work introduces the concept of gate fingerprints, which describes those patterns present in syndrome data that indicate which logical operation took place on the quantum computer. We show different effects by which logical operations produce gate fingerprints by focusing on Clifford+T computation in the surface code. We then explore how gate fingerprint information can be used to make inferences about the circuits or algorithms run on a quantum computer. Our findings indicate that decoder systems can be a vector for side-channel attacks and thus to prevent this, decoder systems should either be secured or built by a trusted party.
</div></details>

- Shashvat Shukla, Dan E. Browne, **Shin Nishio**
- Accepted for publication in the proceedings of IEEE International Conference on Quantum Computing and Engineering (QCE2026, IEEE Quantum Week).
- preprint: [arXiv[quant-ph] 2607.12174 ](https://arxiv.org/abs/2607.12174)

### 18. Treewidth-Aware Gate Cut Selection for Reducing Transpilation Overhead on Superconducting Quantum Devices <span style="background-color:#f7caf5; color:#c21fba; padding:2px 6px; border-radius:4px; font-size:0.85em;">SYS</span>
<details><summary>Abstract</summary><div>
On superconducting quantum devices with sparse qubit connectivity, transpilation of long-range two-qubit interactions inserts additional SWAP gates, increasing hardware cost and execution error. Gate cutting via quasi-probability decomposition (QPD) can remove a selected two-qubit gate and thereby reduce routing overhead, but its sampling cost makes cut placement critical. We propose TW2S, a graph-only two-stage gate-cut selection method that operates on the circuit interaction graph without backend-specific transpilation at selection time. Stage 1 analyzes a min-fill elimination trace and scores edges by their contribution to a treewidth upper bound. Stage 2 ranks the resulting candidates by edge betweenness centrality with a degree penalty to identify routing bottlenecks. Across grid, Watts-Strogatz, barbell, and stochastic block model benchmarks transpiled to IBM's FakeSherbrooke backend, TW2S consistently outperforms random cut selection when the interaction graph contains identifiable sparse cuts. The advantage is governed not by absolute graph density but by moderate community structure and accessible inter-community edges. We further derive a mean-squared-error breakeven condition showing that, under a shared total shot budget, QPD is beneficial only when the ECR reduction is large enough and the signal strength is sufficient. Under an expanded per-subcircuit budget the signal-strength requirement is substantially relaxed. In noisy simulations of the J1-J2 transverse-field Ising model, TW2S achieves ΔECR = 47 for n = 8, compared with approximately 9 for random selection, and yields lower estimation error than the uncut baseline in the tested strong-signal regime, with larger gains at increased shot budgets. These results position graph-structural cut selection as a practical compiler-side tool for turning circuit cutting into a targeted routing-reduction strategy.
</div></details>

- Hana Ebi, **Shin Nishio**, Takahiko Satoh
- preprint: [arXiv[quant-ph] 2605.29723 ](https://arxiv.org/abs/2605.29723)

### 17. QuBridge: Layer-wise Fidelity Decomposition in Quantum Computation Pipeline <span style="background-color:#f7caf5; color:#c21fba; padding:2px 6px; border-radius:4px; font-size:0.85em;">SYS</span>
<details><summary>Abstract</summary><div>
Running a quantum circuit on current hardware involves a sequence of engineering decisions, each with tunable parameters and distinct error characteristics. Existing tools optimize each decision in isolation, leaving practitioners unable to determine how much each decision contributes to final output quality. We present QuBridge, a pipeline analysis tool that decomposes quantum computation into three decision layers and measures each layer's fidelity contribution through progressive ablation and isolation experiments. Applied to quantum teleportation under IBM-calibrated noise models, the framework surfaces three phenomena that end-to-end measurement obscures. Qubit selection narrows the worst-case fidelity band from 11.8% to under 2% with downstream layers held fixed, without changing the peak. Per-gate pulse-shape assignment adds a +0.9% residual gain whose attributed magnitude depends on upstream layout. Error-detection encoding is not uniformly advantageous, and its conditional benefit emerges for input states whose dominant error channel is detectable by the chosen code. QuBridge operates on cached calibration data without requiring live hardware access.
</div></details>

- Kisho Sotokawa, Hideaki Kawaguchi, **Shin Nishio**, Takahiko Satoh
- preprint: [arXiv[quant-ph] 2605.11529 ](https://arxiv.org/abs/2605.11529)


### 16. Digital Annealer-Assisted Accuracy-First Quantum Circuit Transpilation with Integrated QUBO Mapping and Routing <span style="background-color:#f7caf5; color:#c21fba; padding:2px 6px; border-radius:4px; font-size:0.85em;">SYS</span>
<details><summary>Abstract</summary><div>
In the Noisy Intermediate-Scale Quantum (NISQ) era, limited qubit counts and high gate error rates directly constrain circuit fidelity, making the minimization of CNOT gate counts crucial. While conventional compilers prioritize heuristic efficiency, there is a compelling need for "accuracy-first" transpilation that prioritizes gate reduction over compilation latency. We propose a framework leveraging the Digital Annealer (DA) via two complementary strategies: (1) Hybrid, which uses DA-driven global initial mapping combined with high-speed heuristic routing by Qiskit, and (2) Full DA, which solves mapping and routing as separate DA-assisted QUBO subproblems within an iterative workflow. Benchmarks demonstrate that our Hybrid approach achieves an average CNOT reduction of 13.7 % (up to 57.4 %) compared to Qiskit's highest optimization level, with the largest gains on structured circuits such as GHZ and ASP where the initial layout is decisive. The Full DA approach matches Hybrid on structured circuits and outperforms ISAAQ by 23.1 % on average (maximum 90.8 %), but degrades on circuits with random or concentrated connectivity - exposing a trade-off between QUBO size and solution quality when the entire circuit is encoded in a single annealing pass. Although these global optimizations incur higher computational overhead than pure heuristics, our results indicate that for high-precision workflows where gate noise is the primary bottleneck, DA-assisted global initial placement provides a practical "time-for-quality" trade-off for enhancing the utility of near-term quantum hardware.
</div></details>

- Kazuma Watanabe, Hideaki Kawaguchi, **Shin Nishio**, Takahiko satoh
- Accepted for publication in the proceedings of IEEE International Conference on Quantum Computing and Engineering (QCE2026, IEEE Quantum Week).
- preprint: [arXiv[quant-ph] 2605.11500 ](https://arxiv.org/abs/2605.11500)

### 15. Efficient Preparation of Graph States using the Quotient-Augmented Strong Split Tree <span style="background-color:#e0f7fa; color:#006064; padding:2px 6px; border-radius:4px; font-size:0.85em;">QI</span> <span style="background-color:#f7caf5; color:#c21fba; padding:2px 6px; border-radius:4px; font-size:0.85em;">SYS</span>
<details><summary>Abstract</summary><div>
Graph states are a key resource for measurement-based quantum computation and quantum networking, but state-preparation costs limit their practical use. Graph states related by local complement (LC) operations are equivalent up to single-qubit Clifford gates; one may reduce entangling resources by preparing a favorable LC-equivalent representative. However, exhaustive optimization over the LC orbit is not scalable. We address this problem using the split decomposition and its quotient-augmented strong split tree (QASST). For several families of distance-hereditary (DH) graphs, we use the QASST to characterize LC orbits and identify representatives with reduced controlled-Z count or preparation circuit depth. We also introduce a split-fuse construction for arbitrary DH graph states, achieving linear scaling with respect to entangling gates, time steps, and auxiliary qubits. Beyond the DH setting, we discuss a generalized divide-and-conquer split-fuse strategy and a simple greedy heuristic for generic graphs based on triangle enumeration. Together, these methods outperform direct implementations on sufficiently large graphs, providing a scalable alternative to brute-force optimization.
</div></details>

- Nicholas Connolly, **Shin Nishio**, Dan E. Browne, Willian John Munro, Kae Nemoto
- preprint: [arXiv[quant-ph] 2603.23892](https://arxiv.org/abs/2603.23892)


### 14. Local Equivalence Classes of Distance-Hereditary Graphs using Split Decompositions <span style="background-color:#e0f7fa; color:#006064; padding:2px 6px; border-radius:4px; font-size:0.85em;">QI</span>
<details><summary>Abstract</summary><div>
Local complement is a graph operation formalized by Bouchet which replaces the neighborhood of a chosen vertex with its edge-complement. This operation induces an equivalence relation on graphs; determining the size of the resulting equivalence classes is a challenging problem in general. Bouchet obtained formulas only for paths and cycles, and brute-force methods are limited to very small graphs. In this work, we extend these results by deriving explicit formulas for several broad families of distance-hereditary graphs, including complete multipartite graphs, clique-stars, and repeater graphs. Our approach uses a technique known as split decomposition to establish upper bounds on equivalence class sizes, and we prove these bounds are tight through a combinatorial enumeration of the graphs' decomposed structure up to symmetry.
</div></details>

- Nicholas Connolly, **Shin Nishio**, Kae Nemoto
- Accepted for publication in Journal of Physics A: Mathematical and Theoretical.
- preprint: [arxiv[math.CO] 2602.23825](https://arxiv.org/abs/2602.23825)


### 13. Telemetry-Based Server Selection in the Quantum Internet via Cross-Layer Runtime Estimation <span style="background-color:#f7caf5; color:#c21fba; padding:2px 6px; border-radius:4px; font-size:0.85em;">SYS</span>
<details><summary>Abstract</summary><div>
The Quantum Internet will allow clients to delegate quantum workloads to remote servers over heterogeneous networks, but choosing the server that minimizes end-to-end execution time is difficult because server processing, feedforward classical communication, and entanglement distribution can overlap in protocol-dependent ways and shift the runtime bottleneck. We propose Tmax, a lightweight runtime score that sums coarse telemetry from multiple layers to obtain a conservative ranking for online server selection without calibrating weights for each deployment. Using NetSquid discrete-event simulations of a modified parameter-blind VQE (PB-VQE) workload, we evaluate Tmax on pools of 10,000 heterogeneous candidates (selecting among up to 100 per decision) across crossover and bottleneck-dominated regimes, including temporal jitter scenarios and jobs with multiple shots. Tmax achieves single-digit mean regret normalized by the oracle (below 10%) in both regimes and remains in the single-digit range under classical communication latency jitter for multi-shot jobs, while performance degrades for single-shot jobs under severe jitter. To connect performance to deployment planning, we derive an operating map based on requirements relating distance and entanglement rate requirements to protocol level counts, quantify how simple multiuser contention shifts the crossover, and use Sobol global sensitivity analysis to identify regime-dependent bottlenecks. These findings suggest that simple cross-layer telemetry can enable practical server selection while providing actionable provisioning guidance for emerging Quantum Internet services.
</div></details>

- Masaki Nagai, Hideaki Kawaguchi, **Shin Nishio**, Takahiko Satoh
- preprint: [arxiv[quant-ph] 2602.21007](https://arxiv.org/abs/2602.21007)

### 12. RuleSet Generation Framework for Application Layer Integration in Quantum Internet <span style="background-color:#f7caf5; color:#c21fba; padding:2px 6px; border-radius:4px; font-size:0.85em;">SYS</span>
<details><summary>Abstract</summary><div>
Layered architectures for the Quantum Internet have been proposed, inspired by that of the classical Internet, which has demonstrated high maintainability even in large-scale systems. While lower layers in the Quantum Internet, such as entanglement generation and distribution, have been extensively studied, the application layer - responsible for translating user requests into executable quantum-network operations - remains largely unexplored. A significant challenge is translating application-level requests into the concrete instructions executable at lower layers. In this work, we introduce a RuleSet-based framework that explicitly incorporates the application layer into the layered architecture of the Quantum Internet. Our framework builds on a RuleSet-based protocol, clarifying communication procedures, organizing application request information, and introducing new Rules for application execution by embedding application specifications into RuleSets. To evaluate feasibility, we constructed state machines from the generated RuleSets. This approach enables a transparent integration from the application layer down to the physical layer, thereby lowering barriers to deploying new applications on the Quantum Internet.
</div></details>

- Rei Kawano, **Shin Nishio**, Hideaki Kawaguchi, Shota Nagayama, Takahiko Satoh
- Accepted for publication in IEEE Transactions of Quantum Engineering.
- preprint: [arxiv[quant-ph] 2512.07475](https://arxiv.org/abs/2512.07475)

### 11. Dense packing of the surface code: code deformation procedures and hook-error-avoiding gate scheduling <span style="background-color:#f6cdcb; color:#99211a; padding:2px 6px; border-radius:4px; font-size:0.85em;">QEC</span>
<details><summary>Abstract</summary><div>
The surface code is one of the leading quantum error correction codes for realizing large-scale fault-tolerant quantum computing (FTQC).
One major challenge in realizing surface-code-based FTQC is the extremely large number of qubits required. To mitigate this problem, fusing multiple codewords of the surface code into a densely packed configuration has been proposed. It is known that by using dense packing, the number of physical qubits required per logical qubit can be reduced to approximately three-fourths compared to simply placing surface-code patches side by side.
Despite its potential, concrete deformation procedures and quantitative error-rate analyses have remained largely unexplored.
In this work, we present a detailed code-deformation procedure that transforms multiple standard surface code patches into a densely packed, connected configuration, along with a conceptual microarchitecture to utilize this dense packing. We also propose a CNOT gate-scheduling for stabilizer measurement circuits that suppresses hook errors in the densely packed surface code. 
We performed circuit-level Monte Carlo noise simulation of densely packed surface codes using this gate scheduling.
The numerical results demonstrate that as the code distance of the densely packed surface code increases and the physical error rate decreases, the logical error rate of the densely packed surface code becomes lower than that of the standard surface code.
Furthermore, we find that only when employing hook-error-avoiding syndrome extraction can the densely packed surface code achieve a lower logical error rate than the standard surface code, while simultaneously reducing the space overhead.
</div></details>

- Kohei Fujiu, Shota Nagayama, **Shin Nishio**, Hideaki Kawaguchi, Takahiko Satoh
- Physical Review A [113, 042412](https://doi.org/10.1103/7lm4-3bnh)
- preprint: [arxiv[quant-ph] 2511.06758](https://arxiv.org/abs/2511.06758)


### 10. Online Job Scheduler for Fault-tolerant Quantum Multiprogramming <span style="background-color:#f6cdcb; color:#99211a; padding:2px 6px; border-radius:4px; font-size:0.85em;">QEC</span> <span style="background-color:#f7caf5; color:#c21fba; padding:2px 6px; border-radius:4px; font-size:0.85em;">SYS</span>  
<details><summary>Abstract</summary><div>
Fault-tolerant quantum computers are expected to be offered as cloud services due to their significant resource and infrastructure requirements. Quantum multiprogramming, which runs multiple quantum jobs in parallel, is a promising approach to maximize the utilization of such systems. A key challenge in this setting is the need for an online scheduler capable of handling jobs submitted dynamically while other programs are already running.

In this study, we formulate the online job scheduling problem for fault-tolerant quantum computing systems based on lattice surgery and propose an efficient scheduler to address it. To meet the responsiveness required in an online environment, our scheduler approximates lattice surgery programs, originally represented as polycubes, by using simpler cuboid representations. This approximation enables efficient scheduling while improving overall throughput. In addition, we incorporate a defragmentation mechanism into the scheduling process, demonstrating that it can further enhance QPU utilization.
</div></details>

- **Shin Nishio**, Ryo Wakizaka, Daisuke Sakuma, Yosuke Ueno, Yasunari Suzuki
- Proceedings of [2025 IEEE International Conference on Quantum Computing and Engineering](https://doi.org/10.1109/QCE65121.2025.00090) (IEEE QCE 2025)
- preprint: [arxiv[quant-ph] 2505.06741](https://arxiv.org/abs/2505.06741)


### 9. Quantitative Evaluation of Quantum/Classical Neural Network Using a Game Solver Metric <span style="background-color:#c4c8ee; color:#6360e1; padding:2px 6px; border-radius:4px; font-size:0.85em;">QML</span>
<details><summary>Abstract</summary><div>
To evaluate the performance of quantum computing systems relative to classical counterparts and explore the potential for quantum advantage, we propose a game-solving benchmark based on Elo ratings in the game of tic-tac-toe. We compare classical convolutional neural networks (CNNs), quantum convolutional neural networks (QCNNs), and hybrid classical-quantum models by assessing their performance against a random-move agent in automated matches. Additionally, we implement a QCNN integrated with quantum communication and evaluate its performance to quantify the overhead introduced by noisy quantum channels. Our results show that the classical-quantum hybrid model achieves Elo ratings comparable to those of classical CNNs, while the standalone QCNN underperforms under current hardware constraints. The communication overhead was found to be modest. These findings demonstrate the viability of using game-based benchmarks for evaluating quantum computing systems and suggest that quantum communication can be incorporated with limited impact on performance, providing a foundation for future hybrid quantum applications.
</div></details>

* Suzukaze Kamei, Hideaki Kawaguchi, **Shin Nishio**, Tatakahiko Satoh
* Accepted for publication in IEEE Access.
* preprint: [arxiv[quant-ph] 2503.21514](https://arxiv.org/abs/2503.21514)

### 8. Use of faulty states in cat-code error correction <span style="background-color:#f6cdcb; color:#99211a; padding:2px 6px; border-radius:4px; font-size:0.85em;">QEC</span> 
<details><summary>Abstract</summary><div>
Bosonic codes have seen a resurgence in interest for applications as varied as fault-tolerant quantum architectures, quantum enhanced sensing, and entanglement distribution. Cat codes have been proposed as low-level elements in larger architectures, and the theory of rotationally symmetric codes more generally has been significantly expanded in the recent literature. The fault-tolerant preparation and maintenance of cat-code states as a standalone quantum error correction scheme remains, however, limited by the need for robust state preparation and strong intermode interactions. In this work, we consider the teleportation-based correction circuit for cat-code quantum error correction. We show that the class of acceptable ancillary states is broader than is typically acknowledged, and exploit this to propose the use of many-component bridge states, which, though not themselves in the cat-code space, are nonetheless capable of syndrome extraction in the regime where nonlinear interactions are a limiting factor.
</div></details>

* Michael Hanks, Soovin Lee, Nicolo Lo Piparo, **Shin Nishio**, William J. Munro, Kae Nemoto, M.S. Kim
* Physical Review A [113, 042621](https://doi.org/10.1103/vb9n-g6gx)
* preprint: [arXiv[quant-ph] 2412.15134](https://arxiv.org/abs/2412.15134)

### 7. Multiplexed Quantum Communication with Surface and Hypergraph Product Codes <span style="background-color:#f6cdcb; color:#99211a; padding:2px 6px; border-radius:4px; font-size:0.85em;">QEC</span>
<details><summary>Abstract</summary><div>
Connecting multiple processors via quantum interconnect technologies could help to overcome issues of scalability in single-processor quantum computers. Transmission via these interconnects can be performed more efficiently using quantum multiplexing, where information is encoded in high-dimensional photonic degrees of freedom. We explore the effects of multiplexing on logical error rates in surface codes and hypergraph product codes. We show that, although multiplexing makes loss errors more damaging, assigning qubits to photons in an intelligent manner can minimize these effects, and the ability to encode higher-distance codes in a smaller number of photons can result in overall lower logical error rates. This multiplexing technique can also be adapted to quantum communication and multimode quantum memory with high-dimensional qudit systems.
</div></details>

* **Shin Nishio**, Nicholas Connolly, Nicolò Lo Piparo, William John Munro, Thomas Rowan Scruby, Kae Nemoto
* Quantum [9, 1613 (2025).](https://quantum-journal.org/papers/q-2025-01-28-1613/)
* preprint: [arXiv[quant-ph] 2406.08832](https://arxiv.org/abs/2406.08832)

### 6. Equilibration of Non-interacting Photons and Quantum Signatures of Chaos <span style="background-color:#e0f7fa; color:#006064; padding:2px 6px; border-radius:4px; font-size:0.85em;">QI</span>
formerly titled: Photonic quantum signatures of chaos and boson sampling
<details><summary>Abstract</summary><div>
Boson sampling is a paradigmatic example of a task that can be performed by a quantum photonic computer yet is hard for digital classical computers. In a typical boson sampling experiment, the scattering amplitude is determined by the permanent of a submatrix of a unitary drawn from an ensemble of random matrices. Random matrix theory plays a very important role in quite diverse fields while at the same time being intimately related to quantum signatures of chaos. Within this framework, a chaotic quantum system exhibits level statistics characteristic of ensembles of random matrices. Such quantum signatures are encoded in the unitary evolution and so in this work we combine the dynamics of chaotic systems with boson sampling. One of the key results of our work is that we demonstrate the intimate relation between out-of-time-order correlators and boson sampling. We show that the unitary dynamics of a Floquet system may be exploited to perform sampling tasks with identical particles using single-mode phase shifters and multiport beamsplitters. At the end of our paper propose a photonic implementation of the multiparticle kicked rotor, which provides a concrete example of our general approach.
</div></details>

* V. M. Bastidas, H. Nourse, A. Sakurai, A. Hayashi, **S. Nishio**, Kae Nemoto, W. J. Munro
* Physical Review B [112, 134304](https://doi.org/10.1103/tmw1-vry7)
* preprint: [arXiv[quant-ph] 2307.13200](https://arxiv.org/abs/2307.13200)
 

### 5. Hardness of braided quantum circuit optimization in the surface code <span style="background-color:#f6cdcb; color:#99211a; padding:2px 6px; border-radius:4px; font-size:0.85em;">QEC</span>
<details><summary>Abstract</summary><div>
Large-scale quantum information processing requires the use of quantum error correcting codes to mitigate the effects of noise in quantum devices. Topological error-correcting codes, such as surface codes, are promising candidates as they can be implemented using only local interactions in a two-dimensional array of physical qubits. Procedures such as defect braiding and lattice surgery can then be used to realize a fault-tolerant universal set of gates on the logical space of such topological codes. However, error correction also introduces a significant overhead in computation time, the number of physical qubits, and the number of physical gates. While optimizing fault-tolerant circuits to minimize this overhead is critical, the computational complexity of such optimization problems remains unknown. This ambiguity leaves room for doubt surrounding the most effective methods for compiling fault-tolerant circuits for a large-scale quantum computer. In this paper, we show that the optimization of a special subset of braided quantum circuits is NP-hard by a polynomial-time reduction of the optimization problem into a specific problem called Planar Rectilinear 3SAT.
</div></details>

* Kunihiro Wasa, **Shin Nishio**, Koki Suetsugu, Michael Hanks, Ashley Stephens, Yu Yokoi, Kae Nemoto
* IEEE Transactions on Quantum Engineering [vol. 4, pp. 1-7, 2023](https://doi.org/10.1109/TQE.2023.3251358)
* preprint: [arXiv[quant-ph] 2302.00273](https://arxiv.org/abs/2302.00273)

### 4. InQuIR: Intermediate Representation for Interconnected Quantum Computers <span style="background-color:#f7caf5; color:#c21fba; padding:2px 6px; border-radius:4px; font-size:0.85em;">SYS</span> 
<details><summary>Abstract</summary><div>
Various physical constraints limit the number of qubits that can be implemented in a single quantum processor, and thus it is necessary to connect multiple quantum processors via quantum interconnects. While several compiler implementations for interconnected quantum computers have been proposed, there is no suitable representation as their compilation target. The lack of such representation impairs the reusability of compiled programs and makes it difficult to reason formally about the complicated behavior of distributed quantum programs. We propose InQuIR, an intermediate representation that can express communication and computation on distributed quantum systems. InQuIR has formal semantics that allows us to describe precisely the behaviors of distributed quantum programs. We give examples written in InQuIR to illustrate the problems arising in distributed programs, such as deadlock. We present a roadmap for static verification using type systems to deal with such a problem. We also provide software tools for InQuIR and evaluate the computational costs of quantum circuits under various conditions. Our tools are available at this [URL](https://github.com/team-InQuIR/InQuIR).
</div></details>

* **Shin Nishio**, Ryo Wakizaka
* preprint: [arXiv[quant-ph] 2302.00267](https://arxiv.org/abs/2302.00267)

### 3. Impact of the form of weighted networks on the quantum extreme reservoir computation <span style="background-color:#c4c8ee; color:#6360e1; padding:2px 6px; border-radius:4px; font-size:0.85em;">QML</span>
<details><summary>Abstract</summary><div>
The quantum extreme reservoir computation (QERC) is a versatile quantum neural network model that combines the concepts of extreme machine learning with quantum reservoir computation. Key to QERC is the generation of a complex quantum reservoir (feature space) that does not need to be optimized for different problem instances. Originally, a periodically driven system Hamiltonian dynamics was employed as the quantum feature map. In this work we capture how the quantum feature map is generated as the number of time-steps of the dynamics increases by a method to characterize unitary matrices in the form of weighted networks. Furthermore, to identify the key properties of the feature map that has sufficiently grown, we evaluate it with various weighted network models that could be used for the quantum reservoir in image classification situations. At last, we show how a simple Hamiltonian model based on a disordered discrete time crystal with its simple implementation route provides nearly optimal performance while removing the necessity of programming of the quantum processor gate by gate.
</div></details>

* Aoi Hayashi, Akitada Sakurai, **Shin Nishio**, William J Munro, Kae Nemoto
* Physical Review A [108, 042609](https://journals.aps.org/pra/abstract/10.1103/PhysRevA.108.042609)
* preprint: [arXiv[quant-ph] 2211.07841](https://arxiv.org/abs/2211.07841)

### 2. Resource Reduction in Multiplexed High-Dimensional Quantum Reed-Solomon Codes <span style="background-color:#f6cdcb; color:#99211a; padding:2px 6px; border-radius:4px; font-size:0.85em;">QEC</span>
<details><summary>Abstract</summary><div>
Quantum communication technologies will play an important role in quantum information processing in the near future as we network devices together. However, their implementation is still a challenging task due to both loss and gate errors. Quantum error correction codes are one important technique to address this issue. In particular, the Quantum Reed-Solomon codes are known to be quite efficient for quantum communication tasks. The high degree of physical resources required, however, makes such a code difficult to use in practice. A recent technique called quantum multiplexing has been shown to reduce resources by using multiple degrees of freedom of a photon. In this work, we propose a method to decompose multi-controlled gates using fewer CX gates via this quantum multiplexing technique. We show that our method can significantly reduce the required number of CX gates needed in the encoding circuits for the quantum Reed-Solomon code. Our approach is also applicable to many other quantum error correction codes and quantum algorithms, including Grovers and quantum walks.
</div></details>

* **Shin Nishio**, Nicolò Lo Piparo, Michael Hanks, William John Munro, Kae Nemoto
* Physical Review A [107, 032620](https://doi.org/10.1103/PhysRevA.107.032620)
* preprint: [arXiv[quant-ph] 2206.03712](https://arxiv.org/abs/2206.03712)

### 1. Extracting Success from IBM's 20-Qubit Machines Using Error-Aware Compilation <span style="background-color:#f7caf5; color:#c21fba; padding:2px 6px; border-radius:4px; font-size:0.85em;">SYS</span> 
<details><summary>Abstract</summary><div>
NISQ (Noisy, Intermediate-Scale Quantum) computing requires error mitigation to achieve meaningful computation. Our compilation tool development focuses on the fact that the error rates of individual qubits are not equal, with a goal of maximizing the success probability of real-world subroutines such as an adder circuit. We begin by establishing a metric for choosing among possible paths and circuit alternatives for executing gates between variables placed far apart within the processor and test our approach on two IBM 20-qubit systems named Tokyo and Poughkeepsie. We find that a single-number metric describing the fidelity of individual gates is a useful but imperfect guide.
Our compiler uses this subsystem and maps complete circuits onto the machine using a beam search-based heuristic that will scale as processor and program sizes grow. To evaluate the whole compilation process, we compiled and executed adder circuits, then calculated the Kullback–Leibler divergence (KL-divergence, a measure of the distance between two probability distributions). For a circuit within the capabilities of the hardware, our compilation increases estimated success probability and reduce KL-divergence relative to an error-oblivious placement.
</div></details>

* **Shin Nishio**, Yulu Pan, Takahiko Satoh, Hideharu Amano, Rodney Van Meter
* ACM Journal on Emerging Technologies in Computing Systems [Vol. 16, No. 3](https://dl.acm.org/doi/abs/10.1145/3386162)
* preprint: [arXiv[quant-ph] 1903.10963](https://arxiv.org/abs/1903.10963)


# Presentations
##  Invited Talks
### Detecting Qubit Loss without Leakage Detection Units
* **Shin Nishio** and **Dan Browne**
* [QEC Workshop @ UCL](https://ucl-qec-workshop.sessionize.com/speaker/7f504513-5b2a-4213-b9b9-e34fc489c038)
* University College London, UK (7 May 2026)

### Online Job Scheduler for Fault-Tolerant Quantum Multiprogramming
* **Shin Nishio** 
* [Q-LEAP Workshop: Towards Building a Large-Scale Quantum Computer](https://sites.google.com/nii.ac.jp/q-leap-workshop-2026/)
* National Institute of Informatics, Tokyo, Japan (19 Feburary 2026)


### Toward Scalable Multicore Fault-Tolerant Quantum Computers using Quantum Multiplexing
* [Abstract PDF](https://parton-quark.github.io/abstract/2025_07_31_quantuminnovation_abstract.pdf), [Slides PDF](https://parton-quark.github.io/slides/2025_07_31_QuantumInnovation.pdf)
* **Shin Nishio**
* [Quantum Innovation 2025](https://www.qi2025.jp/index.html) The International Symposium on Quantum Science, Technology and Innovation
* Congress Square Grand Green Osaka, Osaka Japan

### A computer system perspective of large-scale quantum computers
<details><summary>Abstract</summary><div>
As the execution speed of the atomic operations of quantum computation in many physical systems is slower than that in classical computation, large-scale quantum computation is required to achieve a computational advantage. Fault-tolerant quantum computation, one of the frameworks for realizing large-scale quantum computation, introduces spatial overhead, including a large number of physical qubits, and temporal overhead, including logical gates and magic state distillation. In addition to these, costs related to classical computational resources for a system software are non-negligible. In this talk, we will give an overview of the system software configuration required for large-scale quantum computers. Then, we will discuss the results and prospects of resource optimization in distributed quantum computing systems with quantum interconnects, a promising approach for scaling up quantum computers. As a further developmental topic, we deal with formal language for distributed quantum computing; we show a method for detecting deadlocks in quantum programs with a type system.
</div></details>

* [Slides PDF](https://parton-quark.github.io/slides/2024_08_31_AQIS2024_satellite_WS_for_FTQC_public.pdf)
* **Shin Nishio**
* [AQIS2024 Satellite Workshop on Fault-Tolerant Quantum Computing](https://teruo41.github.io/aqis2024sw/)
* Sapporo L-Plaza, Kita 8-jo Nishi 3-chome, Kita-ku, Sapporo, Hokkaido, 060-0808 Japan

### Quantum Error Correction and Quantum Multiplexing
* **Shin Nishio**
* 2024 YITP Quantum Error Correction Workshop
* Yukawa Institute for Theoretical Physics, Kyoto, Japan, 18 - 29 March 2024

## International Conferences
### Detecting Qubit Loss without Leakage Detection Units via Repeated Stabilizer Measurements
- Shin Nishio and Dan E. Browne
- poster
- the 8th edition of the International Quantum Error Correction conference, Santa Barbara June 11 2026.


### Quantum Process Tomography Analysis of Thermal Noise in Mølmer-Sørensen Gates for Quantum Error Correction
- Author(s): HIRAI Noah*; KUDO Isamu; MIYANISHI Koichiro; **NISHIO Shin**; SATOH Takahiko; TAKAHASHI Hiroki; TAKEOKA Masahiro; TANJI Kazufumi Affiliation(s): Department of Electronics and Electrical Engineering, Keio University
- poster
- Asian Conference on Trapped Ions 2026, National University of Singapore April 20-22 2026.

### Transport-Aware Syndrome Measurement Circuit Compiler for 1D QCCD Architecture 
- Author(s): ISHIKAWA Eitaro*; **NISHIO Shin**; MIYANISHI Koichiro; TANJI Kazufumi; KUDO Isamu; TAKEOKA Masahiro; TAKAHASHI Hiroki; SATOH Takahiko 
Affiliation(s): Department of Information Engineering, Faculty of Science and Technology, Keio University
- poster
- Asian Conference on Trapped Ions 2026, National University of Singapore April 20-22 2026.

### Online Job Scheduler for Fault-tolerant Quantum Multiprogramming 
- [YouTube Video](https://youtu.be/Yb2j4pQ-rQs)
- Ryo Wakizaka, <u>**Shin Nishio**</u>, Daisuke Sakuma, Yosuke Ueno, Yasunari Suzuki
- Technical paper in [IEEE International Conference on Quantum Computing and Engineering (QCE2025, also known as IEEE Quantum Week 2025)](https://qce.quantum.ieee.org/2025/) Alberquerque, New Mexico, US, Aug 31 - Sep 5 2025
- To be appear in the proceedings of 2025 IEEE International Conference on Quantum Computing and Engineering (QCE)

### Online Job Scheduler for Fault-tolerant Quantum Multiprogramming
- **Shin Nishio**, Ryo Wakizaka, Daisuke Sakuma, Yosuke Ueno, Yasunari Suzuki
- [Seeking Quantum Advantage (SEEQA2025)](https://conference.seeqa.org/) Merton and Corpus Christi Colleges, Oxford, August 25 – 29, 2025.

### Online Job Scheduler for Fault-tolerant Quantum Multiprogramming
- [Poster PDF](https://parton-quark.github.io/poster/QCTiP2025_OnlineScheduler.pdf)
- **Shin Nishio**, Ryo Wakizaka, Daisuke Sakuma, Yosuke Ueno, Yasunari Suzuki
- [Quantum Computing Theory in Practice 2025(QCTiP2025)](https://qctip2025.com/) Berlin, 23-25 April 2025

### Surface Code Communication with Quantum Multiplexing
* **Shin Nishio**, Nicholas Connolly, Nicolò Lo Piparo, William John Munro, Thomas Rowan Scruby, Kae Nemoto
* 19th International Conference on Theory of Quantum Computation, Communication and Cryptography (TQC2024)
* Okinawa Institute of Science and Technology, Okinawa, Japan

### Resource-Aware Deadlock Freedom for Distributed Quantum Programs
* Ryo Wakizaka and **Shin Nishio**
* 6th International Workshop on Quantum Compilation, 11-12 September 2024 Berlin, Germany

### Multiplexed Quantum Communication with Surface and Hypergraph Product Codes
* **Shin Nishio**, Nicholas Connolly, Nicolò Lo Piparo, William Munro, Thomas Scruby and
Kae Nemoto
* 24th Asian Quantum Information Science Conference Sapporo, Japan (Aug. 26-30, 2024)

### An Efficient Erasure Decoder and Quantum Multiplexing using Hypergraph Product Codes
* Nicholas Connolly, **Shin Nishio**, Vivien Londe, Nicolò Lo Piparo, William J. Munro,
Thomas R. Scruby, Anthony Leverrier, Nicolas Delfosse and Kae Nemoto
* 24th Asian Quantum Information Science Conference Sapporo, Japan (Aug. 26-30, 2024)

### Operations on graph states and flows
*	**Shin Nishio**, Dan Browne and Kae Nemoto
* [The international conference on Quantum Information Processing 2024](https://qip2024.tw/) (QIP2024)
* Taipei International Convention Center (TICC), Taipei, Taiwan (January 13-19, 2024)

### Surface Code Communication with Quantum Multiplexing
* [Poster PDF](https://parton-quark.github.io/poster/QEC2023_QM_surface.pdf)
* **Shin Nishio**, Thomas Scruby, Nicolo Lo Piparo, William Munro and Kae Nemoto
* [6th International Conference on Quantum Error Correction, Sydney](https://quantum.sydney.edu.au/qec23/) (QEC23)
* Doltone House, Darling Island and Doltone House, Jones Bay Wharf, Sydney (30 October to 3 November 2023) Peer-reviewed 査読あり

### Computational complexity of optimizing defect braiding quantum circuits by reordering qubits
* [Poster PDF](https://parton-quark.github.io/poster/QIP2023_dbcircuit.pdf)
* Kunihiro Wasa, **Shin Nishio**(presentator), Koki Suetsugu, Michael Hanks, Ashley Stephens, Yu Yokoi and Kae Nemoto
* [26th Conference on Quantum Information Processing](http://qip2023.ugent.be/) (QIP2023)
* Ghent University UFO, Gent, Belgium (February 6th - 10th, 2023) Peer-reviewed 査読あり

### Reducing the resources needed to implement quantum error correction codes using quantum multiplexing
* **Shin Nishio**, Nicolò Lo Piparo, Michael Hanks, William John Munro, Kae Nemoto
* [The 15th Pacific Rim Conference on Lasers and Electro-Optics](https://www.cleopr2022.org/) (CLEO Pacific Rim, CLEO-PR 2022) Peer-reviewed 査読あり
* Sapporo Convention Center, Hokkaido, JAPAN (31 July - 5 August 2022)

### Bridging the gap between theory and implementation via system software construction for quantum computing
<details><summary>Abstract</summary><div>

In recent years, the development of quantum computers has accelerated, and the number of qubits implemented on a quantum processor is rapidly increasing. In order to handle such processors, there is a growing trend to implement system software and language processing systems for quantum computers. This has revealed the practical resources required to implement quantum algorithms and quantum communication protocols that have been proposed theoretically, as well as efficient ways to handle quantum circuits. Furthermore, quantum programming contests are now being held using quantum programming SDKs such as Qiskit, enabling a deeper understanding of quantum computation through small-scale implementations of algorithms. In addition, by describing various quantum applications as concrete code, it has become clear what functions a language processor for quantum computers should have and even what kind of computational difficulties it may face. In this presentation, in addition to results and issues related to language processing systems for quantum computers, I will introduce InQuIR, an intermediate representation for distributed quantum computation[1].<br>[1] Shin Nishio and Ryo Wakizaka. (2022). InQuIR: Intermediate Representation for Interconnected Quantum Computers. In The 4th International Workshop on Quantum Resource Estimation (QRE2022).
</div></details>

* [Nano Korea 2022 Satellite Session II  ‘IBM Quantum Young Scientist’](https://www.nanokorea-sympo.or.kr/)

### InQuIR: Intermediate Representation for Interconnected Quantum Compters
<details><summary>Abstract</summary><div>

Various physical constraints limit the number of qubits that can be implemented in a single quantum processor, and thus it is necessary to connect multiple quantum processors via quantum interconnects. While several compiler implementations for interconnected quantum computers have been proposed, there is no suitable programming language as their compilation target. We propose InQuIR, an intermediate language that can express communication and computation on distributed systems. InQuIR allows various compilation strategies to be evaluated under the same configuration and enhances the reusability of programs. Furthermore, InQuIR facilitates the introduction of static program analysis, such as type systems, to verify that a given program does not have specific program errors and bugs. We also discuss the challenges inherent in quantum programs running on distributed systems, such as failure of communication because of qubit memory exhaustion.<br>
Index Terms: Quantum Interconnect, Quantum Computer Cluster, Distributed Quantum Computation, Quantum Programming Language
</div></details>

* **Shin Nishio** and Ryo Wakizaka
* [Quantum Resource Estimation](https://www.quantumresource.org/) (QRE2022)
* New York, USA co-located with International Symposium on Computer Architecture (ISCA) (18 June 2022) Peer-reviewed 査読あり

### Hardness of braided quantum circuit optimization in the surface code
<details><summary>Abstract</summary><div>

Large-scale quantum information processing requires using error-correcting codes to achieve fault-tolerant quantum computation (FTQC).
However, FTQC has significant resource requirements.
Optimization of FTQC circuits is therefore an important problem, but its computational complexity in common FTQC models, specifically for braided surface code quantum computation, remains unknown.
This ambiguity leaves room for doubt surrounding the most efficient circuits and compilation methods.
In this paper, we show that the optimization of a special subset of braided quantum circuits is NP-hard and that as a result so too is the problem of braided circuit optimization more generally.<br>
Keywords: Fault-tolerant quantum computation, Quantum circuit optimization, Surface code, Braiding Circuits, Computational Complexity, NP-complete, Planar rectilinear 3SAT
</div></details>

* Kunihiro Wasa, **Shin Nishio**, Koki Suetsugu, Michael Hanks, Ashley Stephens, Yu Yokoi, and Kae Nemoto
* [Quantum Resource Estimation](https://www.quantumresource.org/) (QRE2022)
* New York, USA co-located with International Symposium on Computer Architecture (ISCA) (18 June 2022) Peer-reviewed 査読あり

### Resource Reduction in Multiplexed High-Dimensional Quantum Reed-Solomon Codes
* **Shin Nishio**, Nicolò Lo Piparo, Michael Hanks, William Munro and Kae Nemoto
* [21st Asian Quantum Information Science Conference](http://aqis-conf.org/2021/) (AQIS2021)
* Fully virtual conference, hosted by University of Tokyo, Japan, September 1 – September 4, 2021, Peer-reviewed 査読あり

### Compilation Process for Multi-Controlled Gates in Qiskit
* [Poster PDF](https://parton-quark.github.io/poster/FQST2020_compilation.pdf)
* **Shin Nishio**, Takahiko Satoh, and Rodney Van Meter
* [International Workshop for Young Researchers on the Future of Quantum Science and Technology](https://fqst2020.wordpress.com/) (FQST2020)
* National Institute of Informatics, Tokyo, Japan (February 3rd - 6th, 2020) Peer-reviewed 査読あり

### High Fidelity Qubit Mapping for IBM Q
* **Shin Nishio**, Yulu Pan, Takahiko Satoh, and Rodney Van Meter
* [2nd International Workshop on Quantum Compilation](https://msoeken.github.io/iwqc18.html) (IWQC2018)
* Hilton San Diego Resort & Spa, San Diego, USA co-located with ICCAD (8 November 2018) Peer-reviewed 査読あり

### High Fidelity Qubit Mapping for IBM Q
* **Shin Nishio**, Takahiko Satoh and Rodney Van Meter,
* [18th Asian Quantum Information Science Conference](http://aqis-conf.org/2018/) (AQIS2018)
* Nagoya University, Nagoya, Japan(9 September 2018) Peer-reviewed 査読あり

### An Automated Tool for Mapping Program Variables to Qubits on the IBM Q Topologies
* **Shin Nishio**, Takahiko Satoh and Rodney Van Meter,
* [International Conference on challenges in Quantum Information Science](https://qis1.ex.nii.ac.jp/workshop/CQIS2018/) (CQIS2018)
* National Institute for Informatics, Tokyo, Japan(9 April 2018) Peer-reviewed 査読あり

## Domestic Conferences, Symposiums and Workshops
### 量子エラー訂正のための量子プロセストモグラフィーを用いた、Mølmer-Sørensenゲートにおけるノイズの数値解析	
- 平井希空・丹治和史（慶大）・宮西孝一郎（Qubitcore）・工藤　勇・**西尾　真**・佐藤貴彦（慶大）・高橋優樹（OIST）・武岡正裕（慶大）
- [講演抄録](https://ken.ieice.org/ken/paper/202605297cvX/)
- 第54回量子情報技術研究会 (QIT54) 2026年5月27日(水)〜2026年5月29日(金) シンフォニアテクノロジー響ホール伊勢（伊勢市観光文化会館）

### フォールトトレラント量子マルチプログラミングのためのオンラインスケジューラ
* **西尾 真**
* Quantum Internet Task Force 研究会 2025年6月11日 オンライン

### Online Job Scheduler for Fault-tolerant Quantum Multiprogramming
* Nishio Shin (SOKENDAI)・Wakizaka Ryo (Kyoto University)・Sakuma Daisuke (Keio University)・Ueno Yosuke (RIKEN)・Suzuki Yasunari (NTT)
* [情報処理学会第198回ハイパフォーマンスコンピューティング・第14回量子ソフトウェア合同研究発表会](https://www.ipsj.or.jp/kenkyukai/event/hpc198qs14.html)
* [研究報告](https://ipsj.ixsq.nii.ac.jp/records/2001303) 西尾,真, 脇坂,遼, 佐久間,大輔, 上野,洋典, 鈴木,泰成, 2025, フォールトトレラント量子マルチプログラミングのためのオンラインスケジューラ: 情報処理学会, 1–7 p. 
* 2025年3月17日(月) - 3月19日(水)、北海道大学 学術交流会館 小講堂／オンライン

### Panel session for AQIS2024 Satellite Workshop on Fault-Tolerant Quantum Computing
* [Program](https://teruo41.github.io/aqis2024sw/program.html)
* Panelists: Warit Asavanant (The University of Tokyo), Shin Nishio (Okinawa Institute of Science and Technology), Thinh Le (University of Technology Sydney), Ting-Chun Lin (University of California San Diego), Yosuke Ueno (RIKEN)
* Moderator: Akihito Soeda (National Institute of Informatics, Research Organization of Information and Systems)
  
### 量子ビット順序変更による Defect Braiding 量子回路最適化の計算量
* [Poster PDF](https://parton-quark.github.io/poster/QEd_Summer_School_DBQC.pdf)
* Kunihiro Wasa, <u>**Shin Nishio**</u>, Koki Suetsugu, Michael Hanks, Ashley Stephens, Yu Yokoi, and Kae Nemoto.
* 量子教育プログラムオンラインコース・サマースクール [QEd Summer School 2022](https://www.sqei.c.u-tokyo.ac.jp/qed/) / Quantum EDucation For Future Technologies
* 光・量子飛躍フラッグシッププログラム(Q-LEAP) 人材育成プログラム　/ Moonshot Research and Development Program
* 沖縄科学技術大学院大学・リザンシーパークホテル谷茶ベイ, September 23rd-30th, 2022

### InQuIR: Intermediate Representation for Interconncted Quantum Computers
* <u>脇坂遼</u>、**西尾真**
* 量子教育プログラムオンラインコース・サマースクール [QEd Summer School 2022](https://www.sqei.c.u-tokyo.ac.jp/qed/) / Quantum EDucation For Future Technologies
* 光・量子飛躍フラッグシッププログラム(Q-LEAP) 人材育成プログラム　/ MOONSHOT Research and Development Program
* 沖縄科学技術大学院大学・リザンシーパークホテル谷茶ベイ, September 23rd-30th, 2022

### 量子ニューラルネットワークにおける量子特徴マップの解析
* <u>林碧惟</u>、櫻井 彰忠、**⻄尾 真**、William J. Munro、根本 香絵
* 量子教育プログラムオンラインコース・サマースクール [QEd Summer School 2022](https://www.sqei.c.u-tokyo.ac.jp/qed/) / Quantum EDucation For Future Technologies
* 光・量子飛躍フラッグシッププログラム(Q-LEAP) 人材育成プログラム　/ MOONSHOT Research and Development Program
* 沖縄科学技術大学院大学・リザンシーパークホテル谷茶ベイ, September 23rd-30th, 2022

### 量子多重通信路を用いた高次元量子Reed-Solomon符号のリソース削減
* **西尾 真**
* Quantum Internet Task Force [第二回 Student Session](https://qitf.org/news/20210928-2nd-student-session/)
* fully virtual, October 1st, 2021

### 量子多重通信路上の量子Reed-Solomon符号
* **西尾 真**
* Q-LEAP人材育成プログラム 量子技術高等教育拠点 [第一回量子技術 Workshop](https://qacademy.jp/workshop/)
* fully virtual, March 25th, 2021

### High Fidelity Qubit Mapping for IBMQ (poster) **最優秀ポスター賞**
* **西尾 真**
* [WIDEプロジェクト 2018年12月研究会](https://www.wide.ad.jp/News/2018/20181223.html)
* Tokyo University, December 22-23, 2018

### NISQプロセッサ上量子ビットへのプログラム変数配置自動化と高フィデリティ化
* **西尾 真** (慶應義塾大学 バンミーター研究室)
* [物性研短期研究会 量子情報・物性の新潮流 -量子技術が生み出す多様な物性と情報処理技術-](http://www.qi.t.u-tokyo.ac.jp/workshop/NQuIC2018/access.html)
* 東京大学物性研究所, 2018年7月31日〜8月3日

### An Automated Tool for Mapping Program Variables to Qubits on the IBM Q Topologies (poster)
* **西尾 真**
* [第24回 量子情報関西 Student Chapter](https://sites.google.com/site/qikansai/past/24meeting)
* Kyoto University, May 15th, 2018


# Professional Background

## Education
* 聖光学院中学校高等学校 / Seiko Gakuin (Junior/Senior) High School (April 2010 - March 2016)
* Bachelor of Arts.(April 2016 - March 2020) 学士(総合政策学)
  * 慶應義塾大学総合政策学部 Keio University Faculty of Policy Management, Japan
  * Major area of study: Quantum Information Processing
  * [Advancing Quantum Architecture (AQUA)](https://aqua.sfc.wide.ad.jp/home.html) Group in [RG(so called Murai-ken)](https://rg.sfc.keio.ac.jp/)
  * Thesis: [Controlled Gate Compilation for IBMQ](https://aqua.sfc.wide.ad.jp/publications/parton_bthesis.pdf), supervised by Prof.Takahiko Satoh, Prof.Rondney Van Meter and Prof.Jun Murai
* Doctor of Philosophy (5 year course, April 2020 - March 2025) 博士(情報学)
  * 国立情報学研究所 情報学プリンシプル研究系 / 総合研究大学院大学 複合科学研究科 情報学専攻 情報基礎科学分野 
    * NII (National Institute of Informatics) /  SOKENDAI (The Graduate University for Advanced Studies), Japan
    * supervised by Prof. Takeaki Uno and Prof. Kae Nemoto
  * Visiting Researcher at University College London, supervised by Prof. Dan Browne from September 2023 - December 2023
  * 沖縄科学技術大学院大学（OIST）特別研究生、ティーチングフェローシップ
    * OIST (Okinawa Institute of Science and Technology Graduate University) as a special research student (SRS) and teaching fellowship
    * [Quantum Information Science and Technology Unit](https://groups.oist.jp/qist). Supervised by Prof. Kae Nemoto and Prof. Takeaki Uno.
  * Dissertation: [Resource Reduction for Distributed Fault-tolerant Quantum Computing](https://ir.soken.ac.jp/records/2000314) (分散フォールトトレラント量子計算のリソース削減)

## professional experience
|Period|Place|Job title|description|
|----------|-----------------------|-----------------------|---------------------------------------|
|April 2025 - **Current**|[慶應義塾大学]((https://www.keio.ac.jp/jp/)) [Keio University](https://www.keio.ac.jp/en/)|Project Assistant Professor (特任助教)|[Takahiko Satoh's Group](https://sites.google.com/view/satoh-quantum-lab/) in Graduate School of Science and Technology.|
|April 2025 - **Current**|[University College London](https://www.ucl.ac.uk/physics-astronomy/)|Research Associate|[Prof. Dan Browne's Group](https://sites.google.com/site/danbrowneucl/group) in Department of Physics and Astronomy.|
|April 2025 - **Current**|[日本学術振興会(JSPS) Japan Society for the Promotion of Science](https://www.jsps.go.jp/)|Overseas Research Fellowship 海外特別研究員|[海外特別研究員制度](https://www.jsps.go.jp/j-ab/)、書面審査区分：情報学　小区分：計算機システム関連|
|April 2022 - March 2025|[日本学術振興会(JSPS) Japan Society for the Promotion of Science](https://www.jsps.go.jp/)|Research Fellowship for Young Scientists 特別研究員 DC1|[特別研究員制度](https://www.jsps.go.jp/j-pd/index.html)、書面審査区分：情報学　小区分：計算機システム関連 「[量子インターコネクトを用いた量子クラスタ計算のシステムソフトウェア構築](https://kaken.nii.ac.jp/grant/KAKENHI-PROJECT-22KJ1436/)」　受入研究者：宇野　毅明 教授(総合研究大学院大学 複合科学研究科 情報学専攻) Grant Number JP22J20882|
|April 2022 - March 2025|[沖縄科学技術大学院大学(OIST)Okinawa Institute of Science and Technology Graduate University](https://www.oist.jp/)|Teaching Fellowship|[Quantum Information Science and Technology Unit](https://groups.oist.jp/qist), led by Prof. Kae Nemoto|
|September 2023 - December 2023|[日本学術振興会(JSPS) Japan Society for the Promotion of Science](https://www.jsps.go.jp/)|Overseas Challenge Program for Young Researchers 若手研究者海外挑戦プログラム|[若手研究者海外挑戦プログラム制度](https://www.jsps.go.jp/j-abc/)、書面審査区分：情報学　小区分：情報学基礎論関連「フォールトトレラント量子計算のための3直交符号の探索」[報告書](https://www.jsps.go.jp/j-abc/abc_list/R5.html) 派遣先: Department of physics and astronomy, University College London|
|September 2023 - December 2023| [University College London (UCL)](https://www.ucl.ac.uk/) | Visiting Researcher | Supervised by Prof. Dan Browne.|
|April 2020 - March 2022|[国立情報学研究所(NII) National Institute of Informatics](https://www.nii.ac.jp/)|Research Assistant|--|
|July 2020 - December 2020|[IBM東京基礎研究所 IBM Research - Tokyo](https://research.ibm.com/jp-ja/labs/tokyo/)|Research And Development Intern|[IBM Quantum Challenge 2020](https://github.com/qiskit-community/IBMQuantumChallenge2020) Problems Design and Judge.|
|November 2018 - March 2020|[独立行政法人情報処理推進機構 IPA (Information-technology Promotion Agency, JAPAN)](https://www.ipa.go.jp/index-e.html), 経済産業省(Ministry of Economy, Trade and Industry, Japan)|Mitou Target 2018 / 2018年度未踏ターゲット事業（ゲート式量子コンピュータ部門） Exploratory IT Human Resources Project (MITOU TARGET Program)|Adopted project: "Implementation and improvement of machine learning tools using quantum computers", **Shin Nishio**, Ryosuke Sato, Yasuhiro Okura「量子コンピュータを用いた機械学習ツールの実装と改良」, **西尾 真**, 佐藤 綾祐, 大倉 康寛|
|May 2018 – March 2022|[Keio University Quantum Computing Center](https://quantum.keio.ac.jp/)|Development assistance for quantum computer interface, Q-LEAP Network-based research center for quantum information processing|(1)[IBM Quantum Challenge 2019](https://ibmquantum.angelhack.com/) Problems Design and Judge. (2)Qiskit Camp Asia’s 1st Place hackathon champions: [Design a Pulse Programming Language](https://github.com/SaraM92/qiskit-terra), Thomas Alexander, Anastasia Marchenkova, Sara Metwalli, **Shin Nishio**, Maika Takita, Ryo Wakizaka (3) Qiskit-community-tutorial ["Implementation of Quantum Walks on Cycle Graph"](https://github.com/qiskit-community/qiskit-community-tutorials/blob/master/terra/qis_adv/quantum_walk.ipynb), Jordan Kemp, **Shin Nishio**, Ryosuke Satoh, Desiree Vogt-Lee, and Tanisha Bassan|
|April 2017 – March 2020|[Keio University SFC Media Center AV/Fab space](http://www.sfc.lib.keio.ac.jp/eng/general/fabspace_eng.html)|AV / Fab Consultant Student Vice President / AV・Fabコンサルタント 副代表|Fab Space is a glass-windowed corner near the 1st floor entrance of the Media Center, and can be seen from the outside. This is where 3D Printers, 3D Scanners, Cutting Machines, Laser Cutter, and Sewing Machines (regular and embroidery) are located, and users can experience digitalized craftwork. AV Counter or Fab Space staff is available to answer any inquiries.|
|2017|[Link-U inc.](https://www.link-u.co.jp/)|Application development, part time job|--|

* Lecture material preparation support
  
|year|semester|Institute|subject number|class|teacher|description|
|----|--------|---------|-----|------------|-------|---------------|
|2025|Spring|Keio University|FST-IC-35333-211-60|量子コンピューティング1A|Associate Professor Takahiko Satoh|[Lecture page](https://gslbs.keio.jp/pub-syllabus/detail?ttblyr=2025&entno=13046&lang=jp), [Jupyter notebook](https://github.com/parton-quark/QuantumComputing1A)|
|2025|Spring|Keio University|FST-IC-35333-211-60|量子コンピューティング1B|Associate Professor Takahiko Satoh|[Lecture page](https://gslbs.keio.jp/pub-syllabus/detail?ttblyr=2025&entno=13065&lang=jp)|
|2022|--|The University of Tokyo|35603-1091|物理学特別講義Ｂ|Prof. Kae Nemoto|量子計算における量子誤り訂正の基礎と実装|

* Student Assistant (Teaching Assistant) at Keio University

|year|semester|subject number|class|teacher|description|
|----|------------|-----|----------------|-------|----------------------|
|2018|春学期 spring|14270|線形の理論 LINEAR ALGEBRA(GIGA)|佐藤　貴彦特任助教 Project Research Associate Takahiko Satoh|For students who follow the school rules of 2007, content is the same as "LINEAR ALGEBRA DS1 (GIGA/GG/GI)"(simultaneous holding).|
|2018|春学期 spring|B3104|線形代数 LINEAR ALGEBRA DS1 (GIGA/GG/GI)|佐藤　貴彦特任助教 Project Research Associate Takahiko Satoh|[Some of the material / programs I wrote](https://github.com/parton-quark/LinearAlgebra-2018F-2019F)|
|2018|秋学期 autumn|14330|不確実性と情報 INFORMATION AND UNCERTAINTY(GIGA)|佐藤　貴彦特任助教 Project Research Associate Takahiko Satoh|For students who follow the school rules of 2007, content is the same as "PROBABILITY DS1 (GIGA/GG/GI)"(simultaneous holding).|
|2018|秋学期 autumn|B3102|確率 PROBABILITY DS1 (GIGA/GG/GI)|佐藤　貴彦特任助教 Project Research Associate Takahiko Satoh|---|
|2017|春学期 spring|32140|地域と社会（欧州・ＣＩＳ）REGION AND SOCIETY(EUROPE AND CIS COUNTRIES)|横手　慎二教授 Prof. Shinji Yokote|For students who follow the school rules of 2007, content is the same as "REGION AND SOCIETY(EUROPE AND CIS COUNTRIES)"(simultaneous holding).|
|2017|春学期 spring|C1102|地域と社会（欧州・ＣＩＳ）REGION AND SOCIETY(EUROPE AND CIS COUNTRIES)|横手　慎二教授 Prof. Shinji Yokote|---|

### Co-Supervision
- 格子手術に基づく二次元アーキテクチャ向け誤り耐性ブラインド量子計算プロトコル 藤生 剛平（修士論文）[PDF](https://drive.google.com/file/d/1973Q3dOb2uPZRnV5hGkI8bHho1D9upx_/view)
- ユニバーサル量子計算に向けたクリフォード階層スタビライザ符号の誤り訂正閾値解析 芳賀 一玖（卒業論文）[PDF](https://drive.google.com/file/d/1lw7xbS_vYrlTyOqBAMse9NYfKkyXTqsj/view?usp=sharing)
- 1次元QCCDアーキテクチャにおける量子回路実行時間評価のためのコンパイラ設計 石川 英太郎（卒業論文）[PDF](https://drive.google.com/file/d/12O5cPUJH6W-EcRrzAJZ_iOuNJ3epk3dc/view?usp=sharing)

# Fundings
### Overseas Research Fellowship (海外学振), 8 million yen per year (April 2025 - March 2027)
- Japan Society for the Promotion of Science (JSPS)
- **Shin Nishio**, Low-overhead fault-tolerant quantum computation with circuit-centric dynamical codes.

### Overseas Challenge Program for Young Researchers (若手研究者海外挑戦プログラム), 1.4 million yen (September 2023 - December 2024)
- Japan Society for the Promotion of Science (JSPS)
-  **Shin Nishio**, An exploration of triorthogonal codes for fault-tolerant quantum computing ([フォールトトレラント量子計算のための3直交符号の探索](https://www.jsps.go.jp/j-abc/abc_list/R5.html))
-  Host institute: University College London
-  Host researcher: Prof. Dan Browne

### Research Fellowship for Young Scientists (学振DC1), 3.4 million yen(April 2022 - March 2025)
- Japan Society for the Promotion of Science (JSPS)
- **Shin Nishio**, System software construction of quantum computer clusters with quantum interconnect
- [Grant Number JP22KJ1436](https://kaken.nii.ac.jp/en/grant/KAKENHI-PROJECT-22KJ1436/)

### Exploratory IT Human Resources Project (Mitou target, 未踏ターゲット事業 2018), 6.8 million yen (November 2018 - March 2020)
- Information-technology Promotion Agency (IPA) and Ministry of Economy, Trade and Industry (METI)
- [Exploratory IT Human Resources Project](https://www.ipa.go.jp/jinzai/target/index.html)
- Adopted project: **Shin Nishio**(representative), Ryosuke Satoh, Yasuhiro Okura, [“Implementation and improvement of machine learning tools using quantum computers”](https://www.ipa.go.jp/jinzai/target/2018/seika2.html)


# Awards
* 情報処理学会 第198回HPC・第14回量子ソフトウェア合同研究発表会　[学生奨励賞](https://www.ipsj.or.jp/award/qs-award2.html)
  * Student Encouragement Award of 14th symposium of SIG on Quantum Software, the Information Processing Society of Japan.
  * **Nishio Shin**,	Online Job Scheduler for Fault-tolerant Quantum Multiprogramming
* National Institute of Informatics Inose Outstanding Student Award (March 24th 2025). 
  * 猪瀬優秀学生賞: 2025年度に国立情報学研究所における指導で博士号を取得した学生の中で最も優秀な学生に贈られる賞を受賞しました!!
* [LOQCathon 2.0](https://www.linkedin.com/posts/quandela_replay-loqcathon-20-highlights-activity-7135624694388465664-98Lu?utm_source=li_share&utm_content=feedcontent&utm_medium=g_dt_web&utm_campaign=copy) 3rd place hackathon champions. Team 6: Shadow VQE, Mentor: Benjamin Stott, Members: Eduardo Beattie, Maria Gragera Garces, **Shin Nishio**, Lia Yeh, Hafsa Zeroual.
* [QEd Summer School 2022](https://www.sqei.c.u-tokyo.ac.jp/qed/) Best Poster: "InQuIR: Intermediate Representation for Interconncted Quantum Computers" Ryo Wakizaka, **Shin Nishio**
* [QEd Summer School 2022](https://www.sqei.c.u-tokyo.ac.jp/qed/) Best Group Presentation: 「高階量子計算による反転操作を用いた系統誤差の訂正」"Correction of systematic errors using inversion operations with higher-order quantum computation"  Team M (Aoi Hayashi, Haruka Komiyama, **Shin Nishio**, Tomohiro Yamaji)
* [Qiskit Camp Asia 2019](https://medium.com/qiskit/recap-2019-qiskit-camp-asia-26e02dfbd51e) the 1st Place hackathon champions
* [WIDEプロジェクト 2018年12月研究会 最優秀ポスター賞 High Fidelity Qubit Mapping for IBMQ](https://www.wide.ad.jp/News/2018/20181223.html) **西尾 真** (慶應義塾大学)
* [2016年度 能代宇宙イベント](http://unisec.jp/archives/1842) CanSat(模擬人工衛星)競技 ミッションの部 タイプエス賞第2位およびUNISON賞 [慶應義塾大学宇宙科学総合研究会(LYNCS)](https://lyncs-keio.net/) SNSミッションチーム
* 2016年第24回衛星設計コンテスト 設計の部: 全天周宇宙映像収集衛星「Sachika」 地球電磁気・地球惑星圏学会賞

# Hobby
* Annict: [ehdnifnaoneva](https://annict.jp/@ehdnifnaoneva)
* Playstation Network: [kshatriya-zeon](https://my.playstation.com/profile/kshatriya-zeon)
## 競プロ Programming contest
* [IBM Quantum Challenge](https://ibmquantum.angelhack.com/)
    * IBMQ/Qiskit's first competitive programming contest in 2019
    * Problems Design and Judges: Takahiko Satoh, **Shin Nishio**, and Atsushi Matsuo
    * Planning and Translation: Yuri Kobayashi
    * Sponsored by: IBM
    * Co-organized by: Keio University Quantum Computing Center
    * Powerd by AngelHack

* [IBM Quantum Challenge 2020 fall](https://github.com/qiskit-community/IBMQuantumChallenge2020)
    * Problems Design and Judges: Takahiko Satoh, **Shin Nishio**, and Atsushi Matsuo

## Hackathon
* [Qiskit Camp 2019](https://medium.com/qiskit/recap-of-qiskit-camp-2019-4d95f07dd179)
    *  Deliverable is in Qiskit-community-tutorial ["Implementation of Quantum Walks on Cycle Graph"](https://github.com/Qiskit/qiskit-community-tutorials/blob/master/terra/qis_adv/quantum_walk.ipynb)
    *  Jordan Kemp (University of Chicago), **Shin Nishio** (Keio University), Ryosuke Satoh (Keio University), Desiree Vogt-Lee (University of Queensland), and Tanisha Bassan (The Knowledge Society)
* [Qiskit Camp Asia 2019](https://qiskit.org/events/asia/)
    * Our team won the 1st Place hackathon champions: [Design a Pulse Programming Language](https://github.com/SaraM92/qiskit-terra/blob/master/qiskit/qasm/Pulse%20Programming%20Language%20Documentation.md)
        * Thomas Alexander, Anastasia Marchenkova,  Sara Metwalli, **Shin Nishio**, Maika Takita, Ryo Wakizaka
* [LOQCathon 2.0](https://www.linkedin.com/posts/quandela_replay-loqcathon-20-highlights-activity-7135624694388465664-98Lu?utm_source=li_share&utm_content=feedcontent&utm_medium=g_dt_web&utm_campaign=copy)
    * [YouTube](https://youtu.be/jyhFlXNskz8?si=plYoGKAA1RCItdMB)
    * Team 6: Shadow VQE (Mentor: Benjamin Stott, Members: Eduardo Beattie, Maria Gragera Garces, **Shin Nishio**, Lia Yeh, Hafsa Zeroual)
    * Our team won the 3rd Place hackathon champions!
    * Paris, Sorbonne Université, 15 - 17 November 2023
    * Event Host: Pierre-Emmanuel Emeriau, Organized by Quandela

## 所属(過去のものを含む)のウェブサイト
- (学部)[慶應義塾大学 SFC Advancing Quantum Architecture Group (Van Meter研)](https://aqua.sfc.wide.ad.jp/)
- (インターン) [IBM東京基礎研究所](https://research.ibm.com/labs/tokyo)
- (博士)
  - [総合研究大学院大学 先端学術院 情報学コース](https://www.nii.ac.jp/graduate/) 在籍時には複合科学研究科情報学専攻。
  - [Global Research Center for Quantum Information Science in the National Institute of Informatics 2004-2020](https://qis1.ex.nii.ac.jp/quantumCenter/index.html)
  - [OIST Quantum Architecture Unit (根本研)](https://www.oist.jp/research/research-units/qist) 
- (特任助教)[慶應義塾大学理工学部 佐藤貴彦研究室](https://sites.google.com/view/satoh-quantum-lab)
- (ポスドク)[UCL QASTAL Group (Prof.Dan Browne group)](https://www.homepages.ucl.ac.uk/~ucapdeb/)

## 参考になるwebサイト
- [松尾豊 論文の書き方](https://ymatsuo.com/information/how-to-write-paper-en/)
- [Rodney Van Meter "Abstracts for Systems Papers"](https://rdvlivefromtokyo.blogspot.com/2011/04/abstracts-for-systems-papers.html): 英語論文の要旨の書き方
- William Strunk Jr. and E.B. White "The Elements of Style" 英語ライティングの短い教科書。
- [ACM Computing Classification System](https://dl.acm.org/ccs): ACMによる計算機の分野の分類
- [IEEE Thesaurus and IEEE Taxonomy Access](https://www.ieee.org/publications/services/thesaurus-thank-you): IEEEによる分野の分類
- [「審査区分表」の見直し案](https://www.mext.go.jp/a_menu/shinkou/hojyo/1385136_00007.htm): 日本学術振興会/科研費の審査区分に量子情報分野が追加されることが検討されています。「中区分91：量子情報およびその関連分野（新設区分）以下小区分： 91010 量子情報ハードウェア関連（新設区分）, 91020 量子情報システム関連（新設区分）、91030 量子情報基礎理論・応用関連（新設区分）」 これらの制度変更によって日本の量子情報分野が活性化することを期待しています。
- [Doctoral Students Funding Calendar](https://kn1cht.github.io/doctor-funding-calendar/): 日本の博士課程支援プログラム(生活費・研究費)がまとまっている個人サイト。
- [How to use latexdiff on Overleaf](https://ja.overleaf.com/learn/latex/Articles/How_to_use_latexdiff_on_Overleaf)

## その他
### Astronomy
* 慶應義塾大学文化団体連盟所属団体 宇宙科学総合研究会 [LYNCS](https://lyncs-keio.net/)(Laboratory of sYNnthetic Cosmic Science, リンクス)18年度代表/ 2018 representative

I take astrophotographies on weekends.


### [Satellite](https://lyncs-keio.net/advance/)
* 2016年第24回衛星設計コンテスト 設計の部: 全天周宇宙映像収集衛星「Sachika」 地球電磁気・地球惑星圏学会賞受賞\
  西尾は模型製作を担当。

* 2017年第25回衛星設計コンテスト アイデアの部「光格子時計測位衛星 ツキアカリ」応募(代表)。
* Cansat

### Camera
* Camera
  * Nikon D7200
  * Nikon D7100 (IR filter modificated)
* Equatorial Mount
  * Vixen SXD2 Kyoei limited edition with Starbook 10
    * SXG-HAL130 tripod
  * Skymemo S
* Telescope
  * Redcat 51

### Robot-SciFi (including games, novels, and so on)
* Yoshiyuki Tomino's anime
* All Anime of Gundam Series(especially ∀, Reconguista in G, and Victory)
* Full Matal Panic!
* Code Geass
* ARMORED CORE (1,3,SL,LR,4,FA,5,VD,6)
* Muv-Luv Alternative
* Getter Robot
* MACROSS (Zero, F)

### Favorite Video Games
* Gundam EXVS series
* Metal Gear Solid Series
* 十三機兵防衛圏
* FROM SOFTWARE 
  * (In order of preference) Armored Core Series > Dark Souls > King's Field > Sekiro > Demon's souls > Déraciné > Bloodborne > Dark Souls 2 > Dark Souls 3 > ELDEN RING (I prefer structured games than just open world) 
* STAR WARS Jedi: Fallen Order
* Battle Field V
* 戦場のヴァルキュリア4
* Civilization
* Hearts of Iron, Crusader Kings
* 信長の野望
* Drag on Dragoon and Nier series
* Pokemon
* GNOSIA
* レイジングループ

### 最近みたもの
- 閃光のハサウェイ
- グノーシア
- 天国大魔境
- 機動戦士Gundam GQuuuuuuX
- 劇場版 鬼滅の刃 無限城編

### プロ野球
東京ヤクルトスワローズを応援しています。