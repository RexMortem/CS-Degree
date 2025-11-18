
First set of a symbol $X$ is the set of terminals that can appear at the start of a string derived from $X$.

Follow set of a symbol $X$ is the set of terminals that can immediately follow $X$. 

## Finding First(X)

Cases where you add to First(X):
- $X \rightarrow \alpha Y$ is present: we add $\alpha$ to First(X)
- 
## Finding Follow(X)

Cases where you add to Follow(X):
- $X$ shows up in a production before a terminal i.e. in $A \rightarrow Xa$, you add $a$ to Follow(X)
- $X$ shows up in a production before a non-terminal i.e. in $A \rightarrow XB$, you should add First(B) to Follow(X)
- $X$ shows up at the end of a production i.e. $A \rightarrow BX$: you should add Follow(A) to Follow(X) since all the terminals that can follow $A$ can follow $X$
- If $X$ is the start symbol then it should just be $\{\$\}$ where $\$$ is the special symbol denoting the end of a string
