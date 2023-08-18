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
