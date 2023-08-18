**Schroeder-Bernstein Theorem**   
If $A \preceq B$ and $B \preceq A$ then $A \sim B$, i.e. if there exists injections $f: A \to B$ and $g: B \to A$, then there exists a bijection $h: A \to B$   

**Lemma**   
If $h: A \to B$ is an injection and $C \subseteq A$, then $h[A \setminus C] = h[A] \setminus h[C]$   

**Proof of Lemma**   
We will show the nontrivial direction, that is, given $f: A \to B$ is an injection and $C \subseteq A$, then $f[A] \setminus f[C] \subseteq f[A \setminus C]$

Let $x \in f[A] \setminus f[C]$   
$\Rightarrow x \in f[A]$ and $x \notin f[C]$
$\Rightarrow \exists x \in C$ such that $f(a) = x$ and there is no $x \in C$ such that $f(c) = x$   
$\Rightarrow \exists x \in A \setminus C$ such that $f(a \setminus c) = x$   
Hence, $x \in f[A \setminus C]$   

**Proof**   
Since $A \preceq B$ and $B \preceq A$, there exist injections $f: A \to B$ and $g: B \to A$.   
Define the function $C = g[B]$ This is the image of $B$ from the function $g$   
Then clearly, we have that $B \sim C$, and it is enough to show that $A \sim C$   

Define the function $h = g \circ f$, then we have $h: A \to A$ is an injection.

Define $A$ and $C$ inductively, as follows   
$A_{0} = A$,   
$A_{n+1} = h[A_{n}]$,   
$C_{0} = C$,   
$C_{n+1} = h[C_{n}]$   

Also, let us define the function $k: A \to C$ by   
$$
k(x) = 
\begin{cases} 
  h(x) &\text{if } x \in A_{n} \setminus C_{n} for some n \in \omega   
  x &\text{otherwise }
\end{cases}
$$
