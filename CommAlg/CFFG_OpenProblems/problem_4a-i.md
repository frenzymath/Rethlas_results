# lemma lem:noncoherent-ufd-char2

## statement
There exists a commutative ring \(A\) such that:

1. \(A\) is a UFD, hence a G-GCD domain and a finite conductor ring.
2. \(A\) has characteristic \(2\).
3. \(A\) is not coherent.

## proof
We use the following external result.

Complete cited statement:

`paper_id`: Glaz-2000-zero-divisors  
`theorem_id`: Example 9  
`arXiv id`: none

Example 9 in the extracted text `downloads/4a-ii/Glaz-2000-zero-divisors.txt` states:

> Let \(F\) be the field
> \[
> F=\mathbf Z_2(\{a_i\},\{b_i\}),
> \]
> where \(\mathbf Z_2\) is the prime field of characteristic \(2\), and \(\{a_i\}\) and \(\{b_i\}\) are infinitely many variables over \(\mathbf Z_2\). Let
> \[
> S=F[x,y]_{(x,y)},
> \]
> where \(x\) and \(y\) are indeterminates over \(F\). Set \(p_i=a_i x+b_i y\), and define an automorphism \(g\) of \(S\) by
> \[
> g(x)=x,\qquad g(y)=y,\qquad g(a_i)=a_i+y p_{i+1},\qquad g(b_i)=b_i+x p_{i+1}
> \]
> for all \(i\). Let \(G=\langle g\rangle\), then \(o(G)=2\), but \(2\) is not a unit in \(S\). Let
> \[
> R_0=S^G.
> \]
> Then \(R_0\) is a local Krull domain of Krull dimension \(2\). \(R_0\) is not a coherent ring, but \(R_0\) is a UFD.

Set \(A:=R_0\). Since \(A\) is a UFD, it is a GCD domain, hence a G-GCD domain, and therefore a finite conductor ring. By construction \(A\) has characteristic \(2\), and Example 9 says \(A\) is not coherent.

# lemma lem:syzygy-obstruction-in-char2-group-ring

## statement
Let \(A\) be a domain of characteristic \(2\). Let \(a_1,\dots,a_m\in A\), and let
\[
\varphi:A^m\to A,\qquad \varphi(x_1,\dots,x_m)=\sum_{i=1}^m a_i x_i.
\]
Let \(K=\ker(\varphi)\). Put
\[
G=(C_2)^m,\qquad B=A[G].
\]
Then there exists an element \(f\in B\) such that:

1. \(\operatorname{Ann}_B(f)\) is a graded ideal of \(B\).
2. One homogeneous component of \(\operatorname{Ann}_B(f)\) is naturally isomorphic to \(K\).

In particular, if \(K\) is not finitely generated as an \(A\)-module, then \(\operatorname{Ann}_B(f)\) is not finitely generated as an ideal of \(B\), and therefore \(B\) is not a finite conductor ring.

## proof
Let \(g_1,\dots,g_m\) be the standard generators of \(G=(C_2)^m\), and define
\[
\varepsilon_i:=g_i+1\in B.
\]
Since \(\operatorname{char}(A)=2\), we have
\[
\varepsilon_i^2=(g_i+1)^2=g_i^2+2g_i+1=1+0+1=0.
\]
Also the \(\varepsilon_i\) commute, because \(G\) is abelian.

For each subset \(S\subseteq \{1,\dots,m\}\), write
\[
\varepsilon_S:=\prod_{i\in S}\varepsilon_i,
\]
with \(\varepsilon_\varnothing=1\). The family \(\{\varepsilon_S\}_S\) is an \(A\)-basis of \(B\): indeed, from \(g_i=1+\varepsilon_i\) one gets
\[
g_S:=\prod_{i\in S}g_i=\prod_{i\in S}(1+\varepsilon_i)=\sum_{T\subseteq S}\varepsilon_T,
\]
so the change-of-basis matrix from \(\{g_S\}\) to \(\{\varepsilon_S\}\) is triangular with diagonal entries \(1\).

Hence \(B\) is graded by total degree in the \(\varepsilon_i\):
\[
B=\bigoplus_{r=0}^m B_r,\qquad B_r=\bigoplus_{|S|=r}A\varepsilon_S.
\]
Now define
\[
f:=\sum_{i=1}^m a_i\varepsilon_i\in B_1.
\]

Because multiplication by \(f\) raises degree by \(1\), if \(x=\sum_{r=0}^m x_r\) with \(x_r\in B_r\) and \(fx=0\), then
\[
0=fx=\sum_{r=0}^m f x_r,
\]
where \(f x_r\in B_{r+1}\). Since the grading is direct, each \(f x_r=0\). Therefore
\[
\operatorname{Ann}_B(f)=\bigoplus_{r=0}^m \bigl(\operatorname{Ann}_B(f)\cap B_r\bigr),
\]
so \(\operatorname{Ann}_B(f)\) is graded.

Next define
\[
w:=\varepsilon_1\cdots \varepsilon_m\in B_m,
\qquad
v_i:=\prod_{j\neq i}\varepsilon_j\in B_{m-1}.
\]
Then \(\{v_1,\dots,v_m\}\) is an \(A\)-basis of \(B_{m-1}\), and:

- \(\varepsilon_i v_i=w\),
- \(\varepsilon_j v_i=0\) for \(j\neq i\), because \(v_i\) already contains the factor \(\varepsilon_j\), so \(\varepsilon_j v_i\) contains \(\varepsilon_j^2=0\).

Thus for \(x_1,\dots,x_m\in A\),
\[
f\left(\sum_{i=1}^m x_i v_i\right)
=
\sum_{i=1}^m a_i\varepsilon_i\left(\sum_{j=1}^m x_j v_j\right)
=
\left(\sum_{i=1}^m a_i x_i\right)w.
\]
Therefore the degree-\((m-1)\) piece of \(\operatorname{Ann}_B(f)\) is exactly
\[
\left\{\sum_{i=1}^m x_i v_i:\sum_{i=1}^m a_i x_i=0\right\},
\]
which is naturally isomorphic to \(K=\ker(\varphi)\).

Finally, if \(\operatorname{Ann}_B(f)\) were finitely generated as an ideal of \(B\), then it would be finitely generated as an \(A\)-module as well, because \(B\) is a finite free \(A\)-module. Since \(\operatorname{Ann}_B(f)\) is graded, each homogeneous component is the image of \(\operatorname{Ann}_B(f)\) under the corresponding degree projection, hence each component would be finitely generated as an \(A\)-module. In particular, the degree-\((m-1)\) component would be finitely generated, so \(K\) would be finitely generated. This proves the last assertion.

# lemma lem:bad-ideal-in-noncoherent-domain

## statement
Let \(A\) be a noncoherent domain. Then there exists a finitely generated ideal
\[
I=(a_1,\dots,a_m)\subseteq A
\]
such that, if
\[
\varphi:A^m\to A,\qquad \varphi(x_1,\dots,x_m)=\sum_{i=1}^m a_i x_i,
\]
then \(K=\ker(\varphi)\) is not finitely generated as an \(A\)-module.

## proof
Since \(A\) is a domain, all annihilator ideals \((0:c)\) are zero, hence finitely generated. Therefore failure of coherence means that some finitely generated ideal of \(A\) is not finitely presented. Choose such an ideal
\[
I=(a_1,\dots,a_m).
\]
Let \(\psi:A^m\to I\) be the surjective \(A\)-module map sending the \(i\)-th standard basis vector to \(a_i\). Then \(\varphi:A^m\to A\) has image \(I\), and \(\ker(\varphi)=\ker(\psi)\). Hence
\[
0\longrightarrow K\longrightarrow A^m\stackrel{\psi}{\longrightarrow} I\longrightarrow 0
\]
is exact. Since \(I\) is not finitely presented and \(A^m\) is a finitely generated free \(A\)-module, \(K\) cannot be finitely generated.

# theorem thm:target

## statement
A ring \(R\) is a \emph{finite conductor ring} if \(aR\cap bR\) and \((0 : c)\) are finitely generated ideals of \(R\) for all elements \(a, b\), and \(c\) in \(R\). A ring \(R\) is a \emph{quasi coherent ring} if \(a_1 R\cap \ldots \cap a_n R\) and \((0 : c)\) are finitely generated ideals of \(R\) for all elements \(a_1, \ldots, a_n\) and \(c\) in \(R\). Examples of both classes of rings include all coherent rings, UFDs, GCD domains, G-GCD domains (that is, domains in which the intersection of two invertible ideals is an invertible ideal), and the still more general G-GCD rings (that is, rings in which principal ideals are projective and the intersection of two finitely generated flat ideals is a finitely generated flat ideal). For more information on these classes of rings see references [64, 65]. Let \(G\) be a multiplicative abelian group and let \(RG\) be the group ring of \(G\) over \(R\). In the group ring setting where \(R\) is a domain, characterizations of group rings as UFDs and GCD domains were obtained in [61, Theorems 6.1, 6.4, and 7.17]. In the case where \(R\) is a ring with zero divisors, however, the behavior of the finite conductor and quasi coherent properties has been only partially described. Specifically, in the general ring setting, both properties descend from \(RG\) to \(R\) [65, Proposition 3.2], and the question of ascent from \(R\) to \(RG\) reduces to the situation where \(G\) is finitely generated [65, Proposition 3.1]. This, however, does not solve the problem of ascent for either property. Even in the case where \(R\) is a G-GCD ring and \(G\) is an infinite cyclic group, ascent is unknown.

[61] R. Gilmer and T. Parker, Divisibility properties in semigroup rings, Mich. Math. J. 21 (1974), 65-86.

[64] S. Glaz, Finite conductor rings, Proc. Amer. Math. Soc. 129 (2000), 2833-2843.

[65] S. Glaz, Finite conductor rings with zero divisors, Non-Noetherian Commutative Ring Theory, MAIA 520, Kluwer Acad. Publ., Dordrecht, 2000, 251-270.

Assume that \(R\) is a G-GCD ring and \(G\) is a finitely generated abelian group. Does the finite conductor property ascend from \(R\) to \(RG\)?

## proof
No.

Let \(A\) be the local noncoherent UFD of characteristic \(2\) supplied by Lemma `lem:noncoherent-ufd-char2`. By Lemma `lem:bad-ideal-in-noncoherent-domain`, there exists a finitely generated ideal
\[
I=(a_1,\dots,a_m)\subseteq A
\]
such that, for the map
\[
\varphi:A^m\to A,\qquad \varphi(x_1,\dots,x_m)=\sum_{i=1}^m a_i x_i,
\]
the kernel
\[
K:=\ker(\varphi)
\]
is not finitely generated as an \(A\)-module.

Now set
\[
H=(C_2)^m,\qquad B:=A[H].
\]
Then \(H\) is a finite abelian group, hence a finitely generated abelian group. By Lemma `lem:syzygy-obstruction-in-char2-group-ring`, there exists an element
\[
f\in B
\]
such that one homogeneous component of \(\operatorname{Ann}_B(f)\) is naturally isomorphic to \(K\). Since \(K\) is not finitely generated, \(\operatorname{Ann}_B(f)\) is not finitely generated. Therefore \(B=A[H]\) is not a finite conductor ring.

On the other hand, \(A\) is a UFD, hence a G-GCD domain and in particular a finite conductor ring. Thus \(A\) satisfies the hypothesis of the problem, but \(A[H]\) does not satisfy the conclusion.

Therefore the finite conductor property does **not** ascend in general from a G-GCD ring \(R\) to the group ring \(RG\), even when \(G\) is a finite abelian group.
