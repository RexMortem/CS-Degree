
## Dirac Notation


## Quantum States

**Def (Quantum State Vectors):** $\psi = \sum^{d}_{i=1} \alpha_{i} | i > \in \mathbb{C}^{d}$ if $\braket{\psi|\psi} = 1$.

These are **qudit states** and for $d=2$, it is a **qubit**. 

**State Postulate:** State of a (closed) quantum system is described by a quantum state vector.


## Measurements
*how to read out an output from some quantum computation*

OUB.

$p(i) = |\braket{e_{i}|\psi}|^{2}$

Why is this valid prob? Can you show sum to 1? (Parseval)


After observing outcome $i$, the quantum system is in the state $|e_{i}>$.

Plus state in comp basis $\{|0>, |1>\}$ gives perfectly random bit.
Not easy in classical mechanics - impossible?

Hermitian - equal to its complex conjugate c

**Postulate V2:** Measuring a state w.r.t. set of Hermitian orthogonal projections $\{\pi_{i} \delta^{k}_{i=1}\}$

"Dirac delta": $S_{i,j} = 1 \; \text{if}\; i = j \; \text{or}\; 0$

Prob of observing $i \in [k]$ is $p(i) = \braket{\psi|\pi_{i}\psi} = tr[]$

After observing $i$, "post-measurement state conditioned on outcome $i$" is:

$|\psi_{i}> = \frac{\pi_{i}|\psi>}{\sqrt{p(i)}}$

Check this is a valid quantum state
...

What is a "closed" quantum system?
Review of complex inner product mathematics
"trace" of a matrix
LaTeX - how to write all the dirac notation in LaTeX