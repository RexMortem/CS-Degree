*From Lecture 6*

For any two $a,b \in \mathbb{R}$ (though many objects follow the triangle inequality):
- **(i) Triangle Inequality:** $|a + b| \leq |a| + |b|$
- **(ii) Reverse Triangle Inequality:** $|a - b| \geq ||a| - |b||$

> [!NOTE]- Geometric Intuition with Vectors
> For vectors, the triangle inequality has a pretty intuitive geometric proof: you can imagine $|OB| = |OA| + |AB|$ where $O, A, B$ are points of a triangle. Obviously the direct path $OB$ will be shorter (or equal if the triangle is "flattened") than the path represented by $OA$ and $AB$. 
> 

>[!success]- Proof of Triangle Inequality
>First, note that whenever we have something of the form $-x \leq y \leq x$, we can say $|y| \leq x$. You can prove it by cases if you want.
>
>Now consider:
>$-|a| \leq a \leq |a|$ and $-|b| \leq b \leq |b|$. Adding these together:
>
>$-|a| - |b| \leq a + b \leq |a| + |b|$
>$\equiv -(|a| + |b|) \leq a + b \leq |a| + |b|$
>$\equiv |a + b| \leq |a| + |b|$.
>

> [!success]- Proof of Reverse Triangle Inequality
> Proof of Reverse Triangle Inequality
> 
> Sub into triangle inequality $(a - b) + b$ in place of $a + b$:
> 
> $|a + b| \leq |a| + |b|$
> $\equiv |(a-b) + b| \leq |a-b| + |b|$
> $\equiv |a| \leq |a-b| + |b|$
> $\equiv |a| - |b| \leq |a-b|$.
> From the same derivation but swapping $a$ and $b$ (so subbing in with $(b - a) + a$), we get:
> 
> $|b| - |a| \leq |b-a| = |a-b|$.
> 
> So we have two quantities ($|a| - |b|$, $|b| - |a|$) that are smaller than or equal to $|a-b|$. Therefore:
> 
> $|a-b| \geq \text{min}(|a| - |b|, -(|a| - |b|))$
> $\equiv |a-b| \geq ||a| - |b||$.
> 
