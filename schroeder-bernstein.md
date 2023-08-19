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

**Proof of Theorem**   
Since $A \preceq B$ and $B \preceq A$, there exist injections $f: A \to B$ and $g: B \to A$.   
Define the function $C = g[B]$ This is the image of $B$ from the function $g$   
Then clearly, we have that $B \sim C$, and it is enough to show that $A \sim C$   

Define the function $h = g \circ f$, then we have $h: A \to A$ is an injection.

Define $A$ and $C$ inductively, as follows   
$A_{0} = A$,   
$A_{n+1} = h[A_{n}]$,   
$C_{0} = C$,   
$C_{n+1} = h[C_{n}]$   

Also, let us define the function $k: A \to C$ by cases

-If $x \in A_{n} \setminus C_{n}$ for some $n \in \omega$, $k(x) = h(x)$   
-Otherwise, $k(x) = x$   

Now, we must show that $k: A \to C$ is a bijection.

*Claim 1*

$k: A \to C$ is an injection

*Proof of Claim 1*

Suppose $a \neq a' \in A.$  There are three cases to consider.   
*Case 1*   
Suppose there exist (not necessarily distinct) $n,m \in \omega$ such that $a \in A_{n} \setminus C_{n}$ and $a' \in A_{m} \setminus C_{m}$.  Then,   
$k(a) = h(a) \neq h(a') = k(a')$, since $h$ is an injection    

*Case 2*   
Suppose $a, a' \notin A_{n} \setminus C_{n}$ for all $n \in \omega$   
Then $k(a) = a \neq a' = k(a')$      

*Case 3*   
Suppose $a \in A_{n} \setminus C_{n}$ and $a' \notin A_{m} \setminus C_{m}$ for all $m$,   
Then $k(a) = h(a) \in h[A_{n} \setminus C_{n}] = h[A_{n}] \setminus h[A_{n}] \setminus h[C_{n}]$ (by our lemma),
and this is equivalent to $A_{n+1} \setminus C_{n+1}$   
Since $a' \notin A_{n+1} \setminus C_{n+1}$, we obtain $k(a') = a' \neq h(a) = k(a)$   

*Claim 2*   
$k: A \to C$ is a surjection   

*Proof of Claim 2*   
Let $c \in C$, then there are two cases to consider.   

*Case 1*   
Suppose $c \notin A_{n} \setminus C_{n}$ for all $n \in \omega$.  Then $k(c) = c$   

*Case 2*   
Suppose that $c \in A_{n} \setminus C_{n}$.  Since $c \notin A_{0} \setminus C_{0} = A \setminus C$, it follows that $n=m+1$ for some $m \in \omega$.   
Thus, $c \in A_{m+1} \setminus C_{m+1}$   
$\Rightarrow h[A_{m}] \setminus h[C_{m}]$   
$\Rightarrow h[A_{m} \setminus C_{m}]$   
Thus, there exists $a \in A_{m} \setminus C_{m}$ such that $k(a) = h(a) = c$

Thus, our proof is concluded.
