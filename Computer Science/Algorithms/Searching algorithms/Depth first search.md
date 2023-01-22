tags:

## Procedure

The algorithm starts at the root node (selecting some arbitrary node as the root node in the case of a graph) and explores as far as possible along each branch before backtracking. Extra memory, usually a [[stack]], is needed to keep track of the nodes discovered so far along a specified branch which helps in backtracking to the graph

![[Pasted image 20230119200524.png]]

Recursive implementation in pseudocode
```
procedure DFS(G, v) is
    label v as discovered
    for all directed edges from v to w that are in G.adjacentEdges(v) do
        if vertex w is not labeled as discovered then
            recursively call DFS(G, w)
```

## Performance

$$
\begin{align*}
\text{Worst-case performance:}&\quad O()\\
\text{Best-case performance:}&\quad O()\\
\text{Average performance:}&\quad O()
\end{align*}
$$