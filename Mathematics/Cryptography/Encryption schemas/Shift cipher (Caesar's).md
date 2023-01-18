The main idea is to shift the letters of the alphabet forward a number of times. More formal:

* $KeyGen$: choose a uniform random key $k\in\{0,\ldots,25\}$
  
* $Enc_k(m1,\ldots,m_{\mathit{l}}) = c_{1}\dots c_{l}$, where $c_{i}= [(m_i+k)\mod 26]$    
  
* $Dec_k(c_{1},\ldots,c_{l})=m_{1},\ldots,m_{l}$, where $m_{i}=[(c_{i}-k)\mod 26]$

This kind of cipher is easily broken by brute-force with actual technology