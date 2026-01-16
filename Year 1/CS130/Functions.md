- Make surjectivity and injectivity mapping to function properties a separate header (as there are uses for surjections/injections not directly related to their inverse)

Functions are a special case of relations where each element in the first set is mapped to *exactly one* element of the second set. 
- If an element in the first set does not map, then ***existence*** is violated
- If an element in the first set maps to 2+ elements, then ***uniqueness*** is violated

So a relation $R \subseteq X \times Y$ if $\forall x \in X. \; \exists! y \in Y. \; xRy.$

### Key Properties

We will introduce *surjectivity* and *injectivity*, which are essentially the two properties required for the **inverse** relation to be a valid function.
Think about the constraint for a function ($\forall x \in X. \; \exists! y \in Y. \; xRy.$) and what this means must be true for its inverse. 

A function is ***injective*** if "no 2+ x are mapped to the same y" (i.e. each $y \in Y$ is mapped to by one $x \in X$ or not mapped to).

$\forall a, b \in X. \; (a=b) \implies f(a) \neq f(b).$ 



As all elements in the domain ($X$) map to an element in the codomain ($Y$), and no two elements are mapped to the same y, then $|X| \leq |Y|$.

A function is ***surjective*** if "no y is not mapped to". 

$\forall y \in Y. \; \exists x \in X.\; f(x) = y.$

Since every $y \in Y$ is mapped to, the size of $|X|$ must be equal to greater than $|Y|$. 

**Intuition:** which of (injectivity, surjectivity) map to (existence, uniqueness)?

## How Surjectivity, Injectivity maps to Existence, Uniqueness
## Bijections

A function is ***bijective*** if it's both surjective and injective. 
