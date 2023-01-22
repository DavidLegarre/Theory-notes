tags: [[Efficient Algorithms|efficient]]

## Procedure

Given a sorted array $A=\{A_{0},\ldots,A_{n-1}\}$, and target value $T$, then binary search follows:

1. Let $L\gets0$ and $R\gets n-1$
2. If $L>R$, the search terminates as unsuccessful
3. Let $m\gets \lfloor \frac{L+R}{2}\rfloor$
4. IF $A_{m}<T$, set $L\gets m+1$ and go to step 2
5. If $A_{m}>T$, set $R\gets m-1$ and go to step 2
6. If $A_{m}=T$, the search is done; return $m$

![[Pasted image 20230119194425.png]]

## Performance

$$
\begin{align*}
\text{Worst-case performance:}&\quad O(\log n)\\
\text{Best-case performance:}&\quad O(1)\\
\text{Average performance:}&\quad O(\log n)
\end{align*}
$$
