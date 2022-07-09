# Inference HMM
Hidden Markov Models (HMMs) define a Markov chain on hidden variables $h_{1:T}$ that are observed indirectly through the visible variables $v_{1:T}$ 

**Inference tasks**:
* **Filtering**: Inferring the present  $p(h_{t}|v_{1:T})$
* **Prediction**: Inferring the future $p(h_{t}|v_{1:s})\quad t>s$
* **Smoothing**: Inferring the past  $p(h_{t}|v_{1:u})\quad t>u$
* **Likelihood**
* **Most likely Hidden path**: Viterbi alignment $\underset{h_{1:T}}{argmax}\  p(h_{1:T}|v_{1:T})$ 

## Filtering
Inferring the present  $p(h_{t}|v_{1:T})$. 

$$
\begin{align*}
p(h_{t},v_{1:t})&=
\sum\limits_{h_{t-1}}
p(h_{t}, h_{t-1}, v_{1:t}, v_{t})\\
&=\sum\limits_{h_{t-1}}
p(v_{t}|h_{t})
p(h_{t}|h_{t-1})
p(h_{t-1},v_{1:t-1})
\end{align*}
$$

