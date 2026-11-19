# Quantum Exercise: Unit 1 (Expanded Model Answers)

**Quantum Mechanics Foundations** | Marks: 2 / 5 / 10 | Answers are written at exam length: 2-mark answers are brief, 5-mark answers are half to three-quarters of a page, and 10-mark answers are a full page.

---

## Q1 (2 marks each)

**(a) Superposition principle.** A quantum system can exist in a linear combination of its basis states. If |psi1> and |psi2> are two possible states, then |psi> = alpha|psi1> + beta|psi2> is also a valid state, provided the normalisation |alpha|^2 + |beta|^2 = 1 holds. A measurement returns one outcome, with probability given by the squared magnitude of each coefficient.

**(b) Wave-particle duality.** Matter and light display wave behaviour (interference, diffraction) and particle behaviour (localised detection). Which behaviour appears depends on the experimental arrangement, not on the object itself.

**(c) Heisenberg's Uncertainty Principle.** The product of the uncertainties in position and momentum cannot be smaller than hbar/2:

```latex
\Delta x \, \Delta p \ge \frac{\hbar}{2}
```

**(d) Quantization of energy.** A bound system can only take discrete energies E\_n. Example: for hydrogen, E\_n = -13.6/n^2 eV.

**(e) Two quantum systems in nature.** An electron bound in an atom, and a photon (a quantum of light).

---

## Q2 (5 marks each)

**(a) Transition from classical to quantum physics.**

Classical physics explained a wide range of phenomena, but it failed in three well-known cases, and each failure forced the introduction of quantum ideas.

First, blackbody radiation. Classical Rayleigh-Jeans theory predicted that the energy density of radiation grows without limit at short wavelengths, the so-called ultraviolet catastrophe. Planck resolved this in 1900 by proposing that energy is exchanged only in discrete packets, E = h nu, where h is Planck's constant and nu is the frequency.

Second, the photoelectric effect. Electrons are ejected from a metal only when the light frequency exceeds a threshold, and their maximum kinetic energy depends on frequency, not on intensity. Einstein explained this in 1905 with photons: K\_max = h nu - phi, where phi is the work function.

Third, atomic stability. Rutherford's planetary atom, under classical electrodynamics, should radiate energy and spiral into the nucleus within a fraction of a second. Bohr's 1913 model, with quantized orbits, explained both stability and the discrete spectral lines of hydrogen.

Example for the answer: the photoelectric effect is the clearest case, because a classical wave model predicts that a dim, intense light should eventually eject electrons, while the experiment shows that no electrons are emitted below threshold regardless of intensity.

**(b) Wave-particle duality with an example.**

Wave-particle duality states that every particle has an associated wave. The de Broglie wavelength is

```latex
\lambda = \frac{h}{p}
```

The double-slit experiment with electrons illustrates it. Electrons are fired one at a time at a screen with two slits. Each electron is detected as a single localised spot on the detector, which shows particle behaviour. Over many electrons, however, the spots build up an interference pattern of bright and dark fringes, which only waves can produce. The electron seems to pass through both slits as a wave, yet arrives as a particle.

Numerical support: an electron accelerated through 100 V has a wavelength of about 0.123 nm, comparable to atomic spacing in a crystal. This is why crystals diffract electrons, as shown in the Davisson-Germer experiment.

---

## Q3 (10 marks): Fundamental principles of quantum mechanics

Three principles are central to quantum mechanics: superposition, entanglement and the uncertainty principle. Each is a departure from classical intuition, and together they form the basis of quantum computing and quantum communication.

**1. Superposition.** A quantum state can be a combination of basis states. For a qubit,

```latex
|\psi\rangle = \frac{1}{\sqrt{2}}\left(|0\rangle + |1\rangle\right)
```

the system is not in state 0 or state 1 but in both at once, in the sense that both amplitudes contribute to interference. The state has a definite value only after measurement, which gives 0 or 1, each with probability 1/2. Superposition is the source of the parallelism exploited by quantum algorithms: a single circuit acts on all basis states at once. Its limitation is that measurement returns only one result, so an algorithm must use interference to make the desired answer more likely.

**2. Entanglement.** Two or more particles can share a joint state that cannot be written as a product of individual states. The Bell state

```latex
|\Phi^+\rangle = \frac{1}{\sqrt{2}}\left(|00\rangle + |11\rangle\right)
```

is the standard example. Neither qubit has a definite value on its own: each is in a maximally mixed state if considered alone. Yet the two outcomes are perfectly correlated. If the first qubit is measured as 0, the second is certain to be 0 as well. Entanglement is not a hidden variable: Bell inequalities show that these correlations cannot be explained by pre-existing local values. Entanglement does not allow signalling, because each party's individual outcomes are random, and the correlation can only be seen when the two sets of results are compared.

**3. The uncertainty principle.** Certain pairs of observables, such as position and momentum, are complementary. The uncertainty relation

```latex
\Delta x \, \Delta p \ge \frac{\hbar}{2}
```

means a state cannot have sharp values of both at once. This is not merely a limitation of measurement; it is a property of the state. A particle localised in a narrow region must have a wide spread of momenta. In quantum computing, the analogous principle appears between complementary bases: a qubit prepared as an eigenstate of Z has completely uncertain outcomes for X, and vice versa. This is the basis of quantum key distribution.

**Significance.** Superposition gives quantum computers their parallelism. Entanglement provides the non-classical correlations used in teleportation, superdense coding and quantum key distribution. Uncertainty, together with the no-cloning theorem, guarantees that an eavesdropper cannot learn quantum information without disturbing it. Together these principles explain why quantum systems can do tasks that classical systems cannot, while still obeying the rules of probability.

---

## Q4 (5 marks each)

**(a) Quantum states and the effect of measurement.**

A quantum state is represented by a normalised vector |psi> in a Hilbert space. All information the theory can give about the system is contained in this vector. An observable, such as spin along the z-axis, corresponds to a Hermitian operator whose eigenstates |n> form a complete basis. Expanding the state in this basis,

```latex
|\psi\rangle = \sum_n c_n |n\rangle
```

measuring the observable yields the outcome n with probability

```latex
P(n) = |\langle n|\psi\rangle|^2 = |c_n|^2
```

After the measurement, the state collapses to |n>. Repeating the measurement immediately gives the same outcome. Example: for the state (|0> + |1>)/sqrt(2), a z-measurement gives 0 or 1 with probability 1/2. If the result is 0, the state after measurement is |0>, and the original superposition is gone. Measurement therefore changes the state, which distinguishes it from a classical observation that only reveals an existing value.

**(b) Comparison of classical and quantum mechanics.**

Classical mechanics is deterministic: given the position and momentum at one time, the trajectory is fixed by Newton's laws. Observables such as position always have definite values. Measurement reveals these values, and in principle the disturbance can be made arbitrarily small.

Quantum mechanics is probabilistic. The state is a vector in a Hilbert space that evolves deterministically under the Schrodinger equation, but measurement outcomes are random and given by the Born rule. Observables are Hermitian operators, and they need not have definite values before measurement. Measurement changes the state, and the disturbance cannot be avoided.

The two theories agree in the correspondence limit: when quantum numbers are large and action is large compared with hbar, quantum predictions converge to classical ones.

---

## Q5 (5 marks each)

**(a) Quantization in atoms, using the hydrogen atom.**

Bohr's model of hydrogen assumes that the electron's angular momentum is quantized, L = n hbar. Combining this with the Coulomb force gives orbit radii r\_n = n^2 a\_0, where a\_0 is about 0.053 nm, and energy levels

```latex
E_n = -\frac{13.6}{n^2}\ \text{eV}
```

When an electron drops from level n\_2 to n\_1, it emits a photon whose wavelength obeys the Rydberg formula

```latex
\frac{1}{\lambda} = R\left(\frac{1}{n_1^2} - \frac{1}{n_2^2}\right)
```

This gives the discrete spectral lines of hydrogen, which classical physics could not explain. The importance of quantization is that it accounts for the stability of atoms, the discrete spectra used in spectroscopy and astronomy, and the chemical properties of elements, all of which depend on the allowed energy levels.

**(b) Strategic importance of quantum technologies.**

In science, quantum technologies enable atomic clocks, which define the second and underpin GPS timing, and quantum simulation, which allows chemistry and materials to be modelled more accurately. In defence, quantum key distribution offers communication whose security rests on physics, not on computational difficulty. Quantum sensing provides navigation without GPS, which matters where satellite signals can be jammed. Shor's algorithm, if run on a sufficiently large quantum computer, would break the RSA and elliptic-curve systems that protect most current communications. Nations therefore regard quantum capability as a question of security as well as research, which explains the scale of public investment.

---

## Q6 (5 marks each)

**(a) Quantum communication and its applications.**

Quantum communication sends information encoded in quantum states, usually the polarisation or time-bin of single photons, through a channel such as an optical fibre or free-space link. The two main methods are quantum key distribution, which generates shared secret keys, and quantum teleportation, which transfers a quantum state using a pre-shared entangled pair and classical communication.

QKD protocols such as BB84 use the no-cloning theorem and the disturbance caused by measurement: any eavesdropper who measures the photons introduces detectable errors in the sifted key. Applications include secure banking links, protection of government and military communication, and the planned quantum internet, which would connect quantum computers and sensors through networks of entangled nodes. Satellite-based QKD has already been demonstrated over distances of over 1000 km.

**(b) Quantum sensing and its applications.**

Quantum sensing uses quantum systems, such as atoms, ions, spins or superconducting circuits, as extremely sensitive detectors of physical quantities. Their energy levels shift with small changes in magnetic field, gravitational acceleration, time or rotation, and these shifts can be read out precisely.

Applications include atomic clocks, which provide timing for telecom networks and satellite navigation; nitrogen-vacancy magnetometers, which measure weak magnetic fields for medical imaging and geological survey; quantum gravimeters, which detect density variations underground for resource exploration; and inertial sensors, which allow navigation without GPS. Because these sensors need no external reference signal, they are useful where satellite navigation is unavailable or can be jammed.

---

## Q7 (10 marks): Scientific, strategic and technological significance of quantum mechanics

Quantum mechanics is the most successful physical theory ever formulated. Its significance can be grouped into three areas: scientific understanding, technological development and strategic power.

**Scientific significance.** Quantum mechanics explains the structure of atoms and molecules, the nature of chemical bonds, the properties of solids, and the behaviour of light. It accounts for the periodic table, the stability of matter, the colour of materials and the conduction of electricity in metals and semiconductors. It unified phenomena that classical physics treated separately, from spectroscopy to thermodynamics of solids. It also raised deep questions about measurement, randomness and the nature of reality, which remain active areas of research.

**Technological significance.** Many everyday technologies depend on quantum effects. The transistor, which underpins all modern electronics, relies on the quantum behaviour of electrons in semiconductors. Lasers depend on stimulated emission between quantized energy levels. Magnetic resonance imaging uses nuclear spin, a quantum property. Light-emitting diodes, solar cells, and flash memory all rely on quantum band structure. Current research extends these benefits into quantum computing, quantum communication and quantum sensing, which exploit superposition, entanglement and coherence directly rather than through their averaged effects.

**Strategic significance.** Quantum technology now carries strategic weight. Quantum computers running Shor's algorithm would threaten the public-key cryptography protecting financial systems, government communication and critical infrastructure. This creates the risk of harvest-now-decrypt-later attacks, in which encrypted data is stored today for decryption later. Quantum sensing offers navigation and detection capabilities that are hard to jam or spoof. Quantum communication offers security grounded in physics. Because of these applications, countries invest heavily, export controls on quantum components have been introduced, and the field is treated as part of national security policy.

**Summary.** Quantum mechanics gives both an explanation of nature and the tools that shape modern technology and security. Its significance is therefore scientific, technological and strategic at once.

---

## Q8 (10 marks): Classical mechanics vs quantum mechanics

Classical and quantum mechanics differ in their basic assumptions about the world, and the differences show in four areas: determinism, observables, measurement and mathematical framework.

**Determinism.** Classical mechanics is deterministic. Given the initial positions and momenta of all particles, Newton's laws (or their Lagrangian and Hamiltonian equivalents) determine the state at any later time. Randomness in classical physics arises only from ignorance of initial conditions, as in statistical mechanics. Quantum mechanics is also deterministic between measurements, because the state evolves according to the Schrodinger equation. However, the outcome of a measurement is not determined by the state. The Born rule gives only probabilities, and Bell tests show that these probabilities cannot be attributed to pre-existing hidden values. Randomness is therefore intrinsic in quantum theory.

**Observables.** In classical mechanics, every observable such as position, momentum or energy has a definite value at every moment, and a complete description of the system is a point in phase space. In quantum mechanics, observables are represented by Hermitian operators acting on a Hilbert space. The possible results of measuring an observable are its eigenvalues, and a system need not possess a definite value of that observable before measurement. Complementary observables, such as position and momentum, cannot both have definite values, as the uncertainty principle states.

**Measurement.** In classical mechanics, measurement reveals a property that the system already has, and the disturbance caused by the measuring device can in principle be made negligible. In quantum mechanics, measurement is an interaction that changes the state. The outcome is random, drawn with probability given by the squared amplitude, and afterwards the state is the eigenstate associated with that outcome. Repeated measurements give the same result, but any measurement of a complementary observable destroys the earlier information. The role of the measuring apparatus, and whether it must involve an observer, remains a question of interpretation.

**Mathematical framework.** Classical mechanics uses differential equations for positions and momenta, defined on phase space, with Newton's laws, the Lagrangian or the Hamiltonian as its formulation. Quantum mechanics uses a complex vector space, the Hilbert space, in which states are vectors and observables are operators. Dynamics are unitary: the Schrodinger equation preserves the norm of the state. Amplitudes are complex, and interference arises from their addition. The mathematics of quantum mechanics therefore differs at the most basic level, from real-valued trajectories to complex-valued amplitudes.

**Correspondence.** The two theories agree in the limit of large quantum numbers and large actions. In that regime, the probability distribution of quantum outcomes becomes sharply peaked around the classical value, so classical mechanics is recovered as an approximation. This explains why classical physics works for everyday objects while quantum effects dominate at atomic scales.

---

## Q9 (10 marks): Global efforts in quantum research

Quantum research is now a major area of public and private investment worldwide. Four regions show distinct strategies: India, the United States, the European Union and China.

**India.** In April 2023 the Union Cabinet approved the National Quantum Mission with an outlay of about Rs 6,003 crore for the period 2023 to 2031. It aims to develop quantum computers with a target of intermediate-scale machines, secure quantum communication over long distances, quantum sensing and metrology, and quantum materials and devices. Implementation is through hubs at institutions such as IITs and IISc, with the aim of building domestic capability and a skilled workforce.

**United States.** The National Quantum Initiative Act of 2018 established a coordinated federal programme across agencies, including the Department of Energy, the National Science Foundation and NIST. Its focus is on research centres, workforce development and standards. Industry plays a leading role: companies such as IBM, Google, Microsoft and several startups develop hardware and software, and the country is strong in venture funding and in the commercial ecosystem.

**European Union.** The Quantum Flagship, launched in 2018, is a ten-year programme with about one billion euros committed. It funds collaborative research across quantum computing, communication, sensing and simulation, and emphasises networks of universities and companies. The EU also works on common standards and on the quantum internet concept, and member states run national programmes in parallel.

**China.** Quantum research in China is state-led, with large investment in dedicated research centres. The Micius satellite, launched in 2016, demonstrated satellite-based quantum key distribution over long distances, and China has since developed a national quantum communication backbone that links cities. It has also made advances in quantum computing with superconducting and photonic systems.

**Comparison.** The United States leads in industry-driven quantum computing and venture investment. The European Union emphasises collaboration, shared infrastructure and standards. China leads in quantum communication infrastructure and invests heavily through state programmes. India's approach is a national mission that aims to build capability across all four pillars, with emphasis on skills and domestic manufacturing. Each approach reflects the country's strengths, and the most rapid progress comes where academic research, industry and public funding work together.

---

## Q10 (10 marks): Working principle of quantum computers and their difference from classical computers

**How a classical computer works.** A classical computer stores information in bits, each of which is either 0 or 1. Logic gates such as AND, OR and NOT transform bits, and circuits combine gates to compute functions. A register of n bits holds one of 2^n possible strings at any moment. The computer's state is a definite string, and its operations are deterministic and generally irreversible.

**How a quantum computer works.** A quantum computer stores information in qubits, each of which can be in a superposition of 0 and 1. The state of n qubits is a vector with 2^n complex amplitudes, so the computer holds a superposition over all 2^n strings. Its operations are unitary gates, which act on all amplitudes at once. Entanglement links qubits so that operations on one affect the joint state. Interference then plays the key role. Amplitudes from different computational paths add or cancel, so the algorithm is designed to amplify the amplitude of correct answers and suppress wrong ones. The final step is a measurement, which returns one outcome with probability given by the squared amplitude. A good algorithm makes the desired answer highly probable.

**Differences.**

First, the unit of information differs. A bit has a definite value. A qubit has complex amplitudes that describe a state on the Bloch sphere, and it can be in a superposition.

Second, the state space differs. An n-bit register is in one of 2^n states at a time. An n-qubit register can be in any superposition of those 2^n states, so the description grows exponentially with n. This is the source of both the power and the difficulty of simulating quantum systems.

Third, the gates differ. Classical gates such as AND are generally irreversible, since the input cannot be recovered from the output. Quantum gates are unitary matrices, so they are always reversible. The Toffoli gate is a reversible version of AND when the target starts at 0.

Fourth, the output differs. A classical computation gives a definite output that can be read and copied. A quantum computation gives a random outcome that must be repeated to estimate a probability, and the quantum state cannot be copied.

Fifth, the speed-up is problem-specific. Quantum computers do not run every program faster. They give advantages for particular problems, such as factoring large integers with Shor's algorithm and searching unstructured databases with Grover's algorithm, where interference can be arranged to reveal the answer.

**Limitations.** Qubits decohere, so computations must be short or corrected. Current hardware is noisy and small, and the advantage for practical problems remains to be demonstrated.

---

## Q11 (10 marks): Photons, atoms and electrons as quantum systems

A quantum system is one whose behaviour is governed by discrete energy levels, superposition and measurement that changes the state. Photons, atoms and electrons all meet these criteria, and each is used in quantum technology in a different way. The choice of system depends on how well it can be isolated, controlled and read out.

**Photons.** A photon is a quantum of the electromagnetic field. Its polarisation (horizontal or vertical) can serve as a qubit, with |H> = |0> and |V> = |1>. Photons travel at the speed of light, interact weakly with their environment, and so keep their quantum information for long distances. For this reason they are the natural carriers for quantum communication, as in BB84 key distribution and satellite links. Their weak interaction is also a drawback, since two-photon gates are difficult to make deterministic. Photonic quantum computing uses linear optics, beam splitters and single-photon sources, with measurement-based or fusion-based schemes to create entanglement.

**Atoms.** Atoms have discrete energy levels, which are the basis of the Bohr model and of atomic spectroscopy. Two chosen levels of a trapped atomic ion form a qubit. The ion is confined by electromagnetic fields, and lasers drive transitions between its levels to implement gates. Trapped-ion systems achieve very high gate fidelity and long coherence times, though they run slowly. Neutral atoms held in optical tweezers can be arranged in arrays and entangled through Rydberg interactions. Atoms also serve as precise clocks and sensors because their transition frequencies are extremely stable.

**Electrons.** An electron has spin-1/2, which is a two-level system. Spin-up and spin-down can serve as |0> and |1>. Electron spins in semiconductor quantum dots are being developed as qubits, because they can be controlled with electric and magnetic fields and fabricated with semiconductor processes. The electron also shows wave-particle duality, as seen in electron diffraction. Its spin is sensitive to magnetic noise, which is a major source of decoherence in solid-state devices.

**Why all three are quantum systems.** Each has discrete, measurable states, can be placed in superposition, and can become entangled with other systems. Each can also be isolated from its environment for some period, which is what allows coherent operations. The trade-offs differ: photons travel well but are hard to entangle, atoms are stable and precise but slow, and electrons are compact and scalable but noisy. Practical quantum computers combine these strengths, for example by using photons to connect atomic or solid-state processors.

---

*End of Unit 1 expanded answers. Say the word and I will do Unit 2 next, then Units 3 to 5, in the same format.*
