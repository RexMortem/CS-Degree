Refer to [[Probability|CS130]] for probability recap.

> [!note]- Warmup Problem with Bayes
> ```
> You are back from holiday on an exotic island, and your doctor has bad news and good news. The bad news is that you've been diagnosed with a disease and the test is 99% accurate. The good news is that the disease is very rare (1 in 10,000 get it).
> 
> Should you be worried?
> ```

> [!success]- Warmup Problem Solution
> 
> $P(d|p) = \frac{P(p|d)P(d)}{P(p)} = \frac{0.99 \times 0.0001}{P(p)}$
> 
> We can calculate $P(p)$ as the sum of the cases of whether a person has it or not:
> 
> $P(p) = (0.0001 \times 0.99) + (0.9999 \times 0.01)$
> 
> $\frac{0.99 \times 0.0001}{(0.0001 \times 0.99) + (0.9999 \times 0.01)} \approx 0.0098$
> 
> Posterior probability is very small.

## Conditional Independence

Recall that $P(A \cap B) = P(A|B)P(B)$ and $P(A \cap B) = P(B|A)P(A)$ from Bayes' derivation.

We can use this to break down a large conjunction.

***Example:*** $P(\text{Toothache}, \text{Catch}, \text{Cavity})$
$\equiv P(\text{Toothache}|\text{Catch}, \text{Cavity}) \times P(\text{Catch}, \text{Cavity})$
$\equiv P(\text{Toothache}|\text{Catch}, \text{Cavity}) \times P(\text{Catch}|\text{Cavity}) \times P(\text{Cavity})$


In most cases, using conditional independence reduces a problem size of the representation of the joint distribution from exponential to linear.