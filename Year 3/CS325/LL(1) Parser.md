
1) Put into proper form
	- Eliminate ambiguity
	- Eliminate left-recursion
	- Perform left-factorisation
	- Add an extra start production rule
2) Calculate FIRST, FOLLOW sets 
	- FIRST for every production
	- FOLLOW for every non-terminal symbol
3) Choose production $N \rightarrow \alpha$ when:

Left-factorisation is to remove ambiguity - the recursive-descent parser does not know which path to take. To remove this non-determinism, you should perform left-factorisation (usually introducing another production rule).