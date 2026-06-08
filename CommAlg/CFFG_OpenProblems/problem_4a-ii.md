# lemma lem:char2_noncoherent_ufd

## statement
There exists a commutative ring $A$ such that:
\[
\text{$A$ is a UFD, $\operatorname{char}(A)=2$, and $A$ is not coherent.}
\]
In particular, $A$ is a G-GCD ring and hence a quasi coherent ring.

## proof
We use the following external result.

Complete cited statement:

Let
\[
F=\mathbf Z_2(\{a_i\},\{b_i\}), \qquad S=F[x,y]_{(x,y)},
\]
and define the order-$2$ automorphism $g$ of $S$ by
\[
g(x)=x,\qquad g(y)=y,\qquad g(a_i)=a_i+yp_{i+1},\qquad g(b_i)=b_i+xp_{i+1},
\]
where $p_i=a_ix+b_iy$. Then the fixed ring
\[
R_0=S^{\langle g\rangle}
\]
is a local Krull domain of Krull dimension $2$, is not coherent, and is a UFD.

paper_id: `OpenAlex:W76112031`
theorem_id: `Example 9`
arXiv id: not available

Set $A:=R_0$. Then $A$ is a UFD of characteristic $2$ and is not coherent. Since every UFD is a GCD domain, $A$ is a G-GCD ring. Glaz's paper also states that G-GCD rings are quasi coherent.
We now justify the G-GCD claim. Let $I$ be a nonzero invertible fractional ideal of the UFD $A$. Since $A$ is a GCD domain, any finitely generated ideal $J=(a_1,\dots,a_n)$ has principal $v$-closure $J_v=dA$, where $d$ is a greatest common divisor of $a_1,\dots,a_n$. Indeed,
\[
J^{-1}=\bigcap_{i=1}^n a_i^{-1}A=d^{-1}\bigcap_{i=1}^n b_i^{-1}A=d^{-1}A
\]
after writing $a_i=db_i$ with $\gcd(b_1,\dots,b_n)=1$, because then $\bigcap b_i^{-1}A=A$: if $x\in\bigcap b_i^{-1}A$, write $x=c/e$ with $\gcd(c,e)=1$; then $xb_i\in A$ for all $i$, so $e\mid b_i$ for all $i$, hence $e$ divides $\gcd(b_1,\dots,b_n)=1$, and therefore $x\in A$. Hence
\[
J_v=(J^{-1})^{-1}=dA.
\]
Now an invertible ideal is finitely generated and divisorial, so $I=I_v$, and therefore $I$ is principal. Thus every nonzero invertible fractional ideal of $A$ is principal. The intersection of two invertible ideals is therefore the intersection of two principal ideals, which is principal in a GCD domain, hence invertible. So $A$ is a G-GCD domain, and therefore a G-GCD ring.

# lemma lem:annihilator_component

## statement
Let $A$ be a domain of characteristic $2$, let $a_1,\dots,a_m\in A$, and define
\[
\varphi:A^m\to A,\qquad \varphi(x_1,\dots,x_m)=\sum_{i=1}^m a_i x_i.
\]
Let $K=\ker(\varphi)$, let $G=(C_2)^m$, let $B=A[G]$, and set
\[
\varepsilon_i=g_i+1,\qquad f=\sum_{i=1}^m a_i\varepsilon_i.
\]
Then the degree-$(m-1)$ homogeneous component of $\operatorname{Ann}_B(f)$ is naturally isomorphic to $K$.

Consequently, if $K$ is not finitely generated over $A$, then $\operatorname{Ann}_B(f)$ is not finitely generated as an ideal of $B$.

## proof
Since $\operatorname{char}(A)=2$ and $g_i^2=1$, we have $\varepsilon_i^2=0$. Also the $\varepsilon_i$ commute. The monomials
\[
\varepsilon_S:=\prod_{i\in S}\varepsilon_i \qquad (S\subseteq\{1,\dots,m\})
\]
form an $A$-basis of $B$, because
\[
\prod_{i\in S} g_i=\prod_{i\in S}(1+\varepsilon_i)=\sum_{T\subseteq S}\varepsilon_T.
\]
Hence
\[
B=\bigoplus_{r=0}^m B_r
\]
where $B_r$ is the free $A$-module spanned by the $\varepsilon_S$ with $|S|=r$.

Define
\[
w:=\varepsilon_1\cdots\varepsilon_m,\qquad v_i:=\prod_{j\neq i}\varepsilon_j.
\]
Then $\{v_1,\dots,v_m\}$ is an $A$-basis of $B_{m-1}$, and
\[
\varepsilon_i v_i=w,\qquad \varepsilon_j v_i=0 \text{ for } j\neq i.
\]
Therefore, for $x_1,\dots,x_m\in A$,
\[
f\Bigl(\sum_{i=1}^m x_i v_i\Bigr)=\Bigl(\sum_{i=1}^m a_i x_i\Bigr)w.
\]
So the degree-$(m-1)$ part of $\operatorname{Ann}_B(f)$ is exactly
\[
\left\{\sum_{i=1}^m x_i v_i:\sum_{i=1}^m a_i x_i=0\right\},
\]
which is naturally isomorphic to $K$.

We also need that $\operatorname{Ann}_B(f)$ is graded. Since $f\in B_1$, multiplication by $f$ raises degree by $1$. If $x=\sum_{r=0}^m x_r$ with $x_r\in B_r$ and $fx=0$, then
\[
0=fx=\sum_{r=0}^m fx_r
\]
with $fx_r\in B_{r+1}$. As the grading is direct, each $fx_r=0$, so every homogeneous component of $x$ lies in $\operatorname{Ann}_B(f)$. Hence $\operatorname{Ann}_B(f)$ is a graded ideal.

Now $B$ is a finite free $A$-module. Hence any finitely generated ideal of $B$ is finitely generated as an $A$-module. If $\operatorname{Ann}_B(f)$ were finitely generated as an ideal of $B$, then it would be a finitely generated $A$-module. Since it is graded, its degree-$(m-1)$ part is the image of $\operatorname{Ann}_B(f)$ under the $A$-linear projection
\[
\operatorname{Ann}_B(f)\to B_{m-1},
\]
so that component would also be finitely generated over $A$. Therefore $K$ would be finitely generated. This proves the consequence.

# theorem thm:4a-ii

## statement
A ring $R$ is a \emph{finite conductor ring} if $aR\cap bR$ and $(0 : c)$ are finitely generated ideals of $R$ for all elements $a, b$, and $c$ in $R$. A ring $R$ is a \emph{quasi coherent ring} if $a_1 R\cap \ldots \cap a_n R$ and $(0 : c)$ are finitely generated ideals of $R$ for all elements $a_1, \ldots, a_n$ and $c$ in $R$. Examples of both classes of rings include all coherent rings, UFDs, GCD domains, G-GCD domains (that is, domains in which the intersection of two invertible ideals is an invertible ideal), and the still more general G-GCD rings (that is, rings in which principal ideals are projective and the intersection of two finitely generated flat ideals is a finitely generated flat ideal). For more information on these classes of rings see references [64, 65]. Let $G$ be a multiplicative abelian group and let $RG$ be the group ring of $G$ over $R$. In the group ring setting where $R$ is a domain, characterizations of group rings as UFDs and GCD domains were obtained in [61, Theorems 6.1, 6.4, and 7.17]. In the case where $R$ is a ring with zero divisors, however, the behavior of the finite conductor and quasi coherent properties has been only partially described. Specifically, in the general ring setting, both properties descend from $RG$ to $R$ [65, Proposition 3.2], and the question of ascent from $R$ to $RG$ reduces to the situation where $G$ is finitely generated [65, Proposition 3.1]. This, however, does not solve the problem of ascent for either property. Even in the case where $R$ is a G-GCD ring and $G$ is an infinite cyclic group, ascent is unknown.

[61] R. Gilmer and T. Parker, Divisibility properties in semigroup rings, Mich. Math. J. 21 (1974), 65-86.

[64] S. Glaz, Finite conductor rings, Proc. Amer. Math. Soc. 129 (2000), 2833-2843.

[65] S. Glaz, Finite conductor rings with zero divisors, Non-Noetherian Commutative Ring Theory, MAIA 520, Kluwer Acad. Publ., Dordrecht, 2000, 251-270.

Assume that $R$ is a G-GCD ring and $G$ is a finitely generated abelian group. Does the quasi coherent property ascend from $R$ to $RG$?

## proof
No.

Let $A$ be the ring from Lemma `lem:char2_noncoherent_ufd`. Since $A$ is not coherent, there exists a finitely generated ideal
\[
I=(a_1,\dots,a_m)\subseteq A
\]
whose syzygy module
\[
K:=\ker\!\bigl(A^m\to A,\ (x_1,\dots,x_m)\mapsto \sum_{i=1}^m a_i x_i\bigr)
\]
is not finitely generated.

Set
\[
G=(C_2)^m,\qquad B=A[G].
\]
Then $G$ is a finite abelian group, hence a finitely generated abelian group. By Lemma `lem:annihilator_component`, there exists $f\in B$ such that $\operatorname{Ann}_B(f)$ has degree-$(m-1)$ homogeneous component isomorphic to $K$. Since $K$ is not finitely generated, $\operatorname{Ann}_B(f)$ is not finitely generated.

Therefore $B$ is not a finite conductor ring. But every quasi coherent ring is a finite conductor ring by definition. Hence $B$ is not quasi coherent.

Thus $A$ is a G-GCD ring, $G$ is a finitely generated abelian group, and $A[G]$ is not quasi coherent. So the quasi coherent property does not ascend from $R$ to $RG$ in general.
