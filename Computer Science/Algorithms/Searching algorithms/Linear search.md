
Tags: [[Efficient Algorithms|efficient]].

## Basic Algorithm

Given a list $L = \{L_{0},\ldots, L_{n-1}\}$, and  target value $T$ the algorithm follows:
1. Let $i\gets 0$.
2. If $L_{i}=T$, the search terminates successfully; return $i$.
3. Increase $i$ by $1$.
4. If $i<n$, go to step $2$. Otherwise, the search terminates unsuccessfully.

## Complexity 

* Worst-case performance: $O(n)$
* Best-case performance: $O(1)$
* Average performance: $O(n)$
