## Maximum Coverage Problem

Universe set $U$ where $|U| = n$.
$m$ subsets $S_{1}, \dots, S_{n} \subseteq U$.
Positive integer $k \leq m$. 

Pick $k$ sets from $S_{1}, \dots, S_{n}$ s.t. maximum coverage is achieved. 

### Greedy Approximation

Choose subset which introduces the most new elements. Repeat until $k$ subsets chosen. 

For an input instance $I$, let $\text{OPT}(I)$ be number of elements covered by optimal solution and $\text{GREEDY}(I)$ be number of elements covered by greedy solution.

**Thm 1:** $\text{GREEDY}(I) \geq (1 - \frac{1}{e}) \times \text{OPT}(I)$

### Main Approach 

$\forall t \in [1,k]$, we have $c_{t} \geq \frac{u_{t-1}}{k}$ where $c_{t}$ is the number of newly covered elements at 