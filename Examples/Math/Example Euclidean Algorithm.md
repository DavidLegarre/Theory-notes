# Example of the EEA

Connects to: [[Algorithms]], [[Euclidean Algorithm]], [[Modular arithmetic]]

The Extended Euclidean Algorithm (EEA) is an efficient [[Algorithms|algorithm]]   
![[Pasted image 20220604223542.png]]

Display the columns as shown in the image, with the residues in the first column and the quotients in the last. The two other columns will express the values of the inverse of the other and always, x for the first and y for the second. The $\gcd$ of both numbers will be the residue above $0$.

``` ad-summary
title: Algorithm

1. Start by building 4 columns $r,x,y,q$ where in $r$ we will store the initial
   values, in the image 36 and 25 (the bigger one must always be on top). Then 
   in column $x$ we will put a $1$ for the row with the bigger number and a $0$ 
   on the other, and viceversa for column $y$. Leave $q$ column empty for now
   
2. Divide $r_{1}$ by $r_{2}$ and set the quotient in the column (in the image is
   the first one on the "*q*" column) and the remainder on the $r$ column of 
   the next row also. 
   
3. To calculate the new values of $x$ and $y$ at row $i$. 
$$
\begin{align*}
x_{i} &= x_{i-2}-x_{i-1}·q_{i}\\
y_{i} &= y_{i-2}-y_{i-1}·q_{i}\\
\end{align*}   
$$

4. Repeat steps $2$ and $3$ until the new remainder $r$ is $0$, then the previous
   remainder will be the gcd, and the $x$ and $y$ will be their respective inverses
```
