+++
title = "blueprint_verified"
date = 2026-05-02
weight = 4
[extra]
math = true
+++

# lemma lem:split_unipotent_h1

## statement
Let $k$ be a field and let $U$ be a $k$-split smooth connected unipotent $k$-group. Then
$$
H^1(k,U)=1
$$
for nonabelian fppf cohomology. Consequently, if
$$
1\to U\to E\xrightarrow{\pi} Q\to 1
$$
is an exact sequence of smooth affine $k$-groups, then the map
$$
E(k)\to Q(k)
$$
is surjective.

## proof
Since $U$ is $k$-split, it has a composition series by smooth connected normal
$k$-subgroups whose successive quotients are $k$-isomorphic to $\mathbf G_ a$.
Induction on the length of such a series, using the exact sequence in nonabelian
fppf cohomology and $H^1(k,\mathbf G_ a)=0$, gives $H^1(k,U)=1$.

For the consequence, the fiber over any $q\in Q(k)$ is a left $U$-torsor over
$\operatorname{Spec} k$. Its cohomology class is trivial, so the fiber has a
$k$-point. Hence $E(k)\to Q(k)$ is surjective.

# lemma lem:split_unipotent_reduction

## statement
Let $G$ be a smooth connected affine $k$-group, let
$$
U=R_ {us,k}(G)
$$
be its maximal $k$-split smooth connected unipotent normal $k$-subgroup, and put
$$
\overline G=G/U.
$$
Assume that for every algebraic extension $K/k$ the natural map
$$
\mathbb X_ \ast(\overline G)/\overline G(k)\to
\mathbb X_ \ast(\overline G_ K)/\overline G(K)
$$
is injective. Then for every algebraic extension $K/k$ the natural map
$$
\mathbb X_ \ast(G)/G(k)\to \mathbb X_ \ast(G_ K)/G(K)
$$
is injective.

## proof
Let $\pi:G\to \overline G$ be the quotient map, and let
$\lambda,\mu\in \mathbb X_ \ast(G)$ become $G(K)$-conjugate. Then
$\overline\lambda=\pi\circ\lambda$ and
$\overline\mu=\pi\circ\mu$ become $\overline G(K)$-conjugate. By the assumed
injectivity for $\overline G$, there is $\overline g\in \overline G(k)$ such that
$$
\overline\mu=\operatorname{Int}(\overline g)\circ\overline\lambda.
$$
By Lemma `lem:split_unipotent_h1`, $G(k)\to\overline G(k)$ is surjective, so
choose $g\in G(k)$ lifting $\overline g$. Replacing $\lambda$ by
$\operatorname{Int}(g)\circ\lambda$, we reduce to the case
$$
\pi\circ\lambda=\pi\circ\mu=:\nu:\mathbf G_ m\to\overline G.
$$

Form the pullback $k$-group
$$
E:=\mathbf G_ m\times_ {\nu,\overline G,\pi}G.
$$
Then $E$ is smooth connected affine and fits into an exact sequence
$$
1\to U\to E\xrightarrow{q}\mathbf G_ m\to 1.
$$
The two cocharacters $\lambda$ and $\mu$ are the same thing as two
$k$-homomorphic sections
$$
s_ \lambda(t)=(t,\lambda(t)),\qquad s_ \mu(t)=(t,\mu(t))
$$
of $q$.

We use the following cited result.

Complete cited statement: Theorem 4.2.9 in *Structure and classification of pseudo-reductive groups* states: “Any two maximal split $k$-tori in a smooth connected affine $k$-group $G$ are conjugate under $G(k)$.”

paper_id: Structure and classification of pseudo-reductive groups  
theorem_id: Theorem 4.2.9  
arXiv id:

The images $s_ \lambda(\mathbf G_ m)$ and $s_ \mu(\mathbf G_ m)$ are split
one-dimensional $k$-tori in $E$. They are maximal split $k$-tori: a split torus
in $E$ maps injectively to $\mathbf G_ m$, because the kernel $U$ is unipotent
and contains no nontrivial torus. By the cited theorem, there is $e\in E(k)$ such that
$$
e\\,s_ \lambda(\mathbf G_ m)\\,e^{-1}=s_ \mu(\mathbf G_ m).
$$
Let $a=q(e)\in k^\times=\mathbf G_ m(k)$. Since $s_ \mu(a)$ centralizes
$s_ \mu(\mathbf G_ m)$, the element
$$
u:=s_ \mu(a)^{-1}e
$$
lies in $U(k)$ and still carries $s_ \lambda(\mathbf G_ m)$ onto
$s_ \mu(\mathbf G_ m)$. Moreover $q\circ\operatorname{Int}(u)\circ s_ \lambda=q\circ s_ \lambda$.
The restriction $q|_ {s_ \mu(\mathbf G_ m)}$ is an isomorphism onto $\mathbf G_ m$,
so the only section of $q$ with image $s_ \mu(\mathbf G_ m)$ is $s_ \mu$. Thus
$$
s_ \mu=\operatorname{Int}(u)\circ s_ \lambda,
$$
and hence $\mu=\operatorname{Int}(u)\circ\lambda$. Therefore $\lambda$ and
$\mu$ are $G(k)$-conjugate.

# lemma lem:geometric_normalizer_conjugacy

## statement
Let $F$ be an algebraically closed field, let $H$ be a smooth connected affine
$F$-group, and let $T\subset H$ be a maximal torus. If
$\lambda,\mu\in X_ \ast(T)$ are $H(F)$-conjugate, then they are conjugate by an
element of $N_ H(T)(F)$.

## proof
Choose $g\in H(F)$ such that $\mu=\operatorname{Int}(g)\circ\lambda$. Let
$$
C=Z_ H(\mu(\mathbf G_ m))^\circ.
$$
The standard torus-centralizer theorem says that the centralizer of a torus in a
smooth affine group is smooth; hence $C$ is a smooth connected affine $F$-group.
Both $T$ and $gTg^{-1}$ contain $\mu(\mathbf G_ m)$, so they are contained in
$C$. They are maximal tori of $C$, since any larger torus in $C$ would be a
larger torus in $H$.

Over the algebraically closed field $F$, maximal tori are maximal split tori. Applying
Theorem 4.2.9 from *Structure and classification of pseudo-reductive groups* to the
smooth connected affine group $C$, choose $c\in C(F)$ with
$$
c\\,gTg^{-1}c^{-1}=T.
$$
Then $n:=cg\in N_ H(T)(F)$, and because $c$ centralizes $\mu(\mathbf G_ m)$,
$$
\operatorname{Int}(n)\circ\lambda
=\operatorname{Int}(c)\circ\mu
=\mu.
$$
Thus $\lambda$ and $\mu$ are $N_ H(T)(F)$-conjugate.

# lemma lem:wound_relative_dominant_representatives

## statement
Let $H$ be a smooth connected affine $k$-group such that $R_ {u,k}(H)$ is
$k$-wound. Let $S\subset H$ be a maximal split $k$-torus, and let $P$ be a
minimal pseudo-parabolic $k$-subgroup containing $S$. Let
$$
{}^k\Phi=\Phi(H/R_ {u,k}(H),S)
$$
be the relative root system with positive system ${}^k\Phi^+=\Phi(P/R_ {u,k}(H),S)$,
and set
$$
C=\\{\nu\in X_ \ast(S)\mid \langle a,\nu\rangle\ge 0
\text{ for all }a\in{}^k\Phi^+\\}.
$$
Then:

1. every element of $X_ \ast(S)$ is $N_ H(S)(k)$-conjugate to a unique element of $C$;
2. if $\lambda,\mu\in X_ \ast(S)$ become $H(K)$-conjugate over an algebraic
extension $K/k$, then they have the same unique representative in $C$. In
particular, $\lambda$ and $\mu$ are $N_ H(S)(k)$-conjugate.

## proof
We use the following cited results.

Complete cited statement: Proposition 5.3.1 in *Structure and classification of pseudo-reductive groups* states that if $S$ is a maximal split $k$-torus in a smooth connected affine $k$-group $G$, then
$$
W(G,S):=N_ G(S)/Z_ G(S)
$$
is a constant finite étale $k$-group and the inclusion
$$
N_ G(S)(k)/Z_ G(S)(k)\hookrightarrow W(G,S)(k)
$$
is an equality.

paper_id: Structure and classification of pseudo-reductive groups  
theorem_id: Proposition 5.3.1  
arXiv id:

Complete cited statement: Theorem 5.3.2(i) in *Structure and classification of pseudo-reductive groups* states that for a smooth connected affine $k$-group $G$, a maximal split $k$-torus $S$, and a minimal pseudo-parabolic $k$-subgroup $P$ containing $S$, the set
$$
{}^k\Phi=\Phi(G/R_ {u,k}(G),S)
$$
is a root system in its $\mathbf Q$-span in $X(S)_ \mathbf Q$, the subset
$$
\Phi(P/R_ {u,k}(G),S)
$$
is a positive system of roots, and the natural map
$$
N_ G(S)(k)/Z_ G(S)(k)\to W({}^k\Phi)
$$
is an isomorphism.

paper_id: Structure and classification of pseudo-reductive groups  
theorem_id: Theorem 5.3.2(i)  
arXiv id:

Complete cited statement: Theorem 5.3.2(iv) in *Structure and classification of pseudo-reductive groups* states that if $R_ {u,k}(G)$ is $k$-wound, then the root system $\Phi(G,S)$ consists of the nontrivial $S$-weights on $\operatorname{Lie}(G)$.

paper_id: Structure and classification of pseudo-reductive groups  
theorem_id: Theorem 5.3.2(iv)  
arXiv id:

By Theorem 5.3.2(i), $N_ H(S)(k)/Z_ H(S)(k)$ is identified with the Weyl group
of the root system ${}^k\Phi$. The usual root-system argument shows that each Weyl
orbit on $X_ \ast(S)$ has a unique representative in the closed dominant chamber
$C$. Proposition 5.3.1 realizes these Weyl elements by $k$-points of $N_ H(S)$.
This proves part (1).

For part (2), let $\lambda^+,\mu^+\in C$ be the unique representatives of
$\lambda$ and $\mu$ from part (1). Since the conjugations from $\lambda$ to
$\lambda^+$ and from $\mu$ to $\mu^+$ are already defined over $k$, the
cocharacters $\lambda^+$ and $\mu^+$ are still $H(K)$-conjugate. Replacing
$\lambda,\mu$ by $\lambda^+,\mu^+$, we may assume from now on that
$$
\lambda,\mu\in C.
$$

Let $k_ s$ be a separable closure of $k$. Choose a maximal $k_ s$-split torus
$$
T\subset H_ {k_ s}
$$
containing $S_ {k_ s}$. Choose a minimal pseudo-parabolic $k_ s$-subgroup
$$
B\subset P_ {k_ s}
$$
containing $T$. Let
$$
\Phi_ {\mathrm{abs}}=\Phi(H_ {k_ s}/R_ {u,k_ s}(H_ {k_ s}),T)
$$
be the corresponding absolute root system, with positive system
$\Phi_ {\mathrm{abs}}^+=\Phi(B/R_ {u,k_ s}(H_ {k_ s}),T)$.

For $\nu\in X_ \ast(S)\subset X_ \ast(T)$ and $\alpha\in\Phi_ {\mathrm{abs}}$,
$$
\langle \alpha,\nu\rangle=\langle \alpha|_ S,\nu\rangle.
$$
By Theorem 5.3.2(iv), because the $k$-wound property of $R_ {u,k}(H)$ is preserved
under separable extension, the relative and absolute roots are exactly the nontrivial
weights of $S$ and $T$ on the corresponding Lie algebras. Since $B\subset P_ {k_ s}$,
every $\alpha\in\Phi_ {\mathrm{abs}}^+$ restricts either to $0$ or to an element of
${}^k\Phi^+$, and every element of ${}^k\Phi^+$ arises as the nonzero restriction
of some element of $\Phi_ {\mathrm{abs}}^+$. Hence, for cocharacters in $X_ \ast(S)$,
dominance for ${}^k\Phi^+$ is equivalent to dominance for
$\Phi_ {\mathrm{abs}}^+$. Thus $\lambda$ and $\mu$ are also
$\Phi_ {\mathrm{abs}}^+$-dominant.

Let $\Omega$ be an algebraic closure containing both $K$ and $k_ s$. Since
$\lambda$ and $\mu$ are $H(K)$-conjugate, they are $H(\Omega)$-conjugate.
The torus $T_ \Omega$ is a maximal torus of $H_ \Omega$. By Lemma
`lem:geometric_normalizer_conjugacy`, $\lambda$ and $\mu$ are conjugate by an
element of $N_ {H_ \Omega}(T_ \Omega)(\Omega)$.

By Proposition 5.3.1 applied over $k_ s$ to the maximal split torus $T$, the finite
étale group $N_ {H_ {k_ s}}(T)/Z_ {H_ {k_ s}}(T)$ is constant; therefore purely inseparable
extension from $k_ s$ to $\Omega$ adds no new Weyl elements. By Theorem 5.3.2(i),
this Weyl group is $W(\Phi_ {\mathrm{abs}})$. Thus $\lambda$ and $\mu$ lie in the
same $W(\Phi_ {\mathrm{abs}})$-orbit.

Every Weyl-group orbit in a root system has a unique element in the closed dominant
chamber. Since both $\lambda$ and $\mu$ are $\Phi_ {\mathrm{abs}}^+$-dominant, we get
$$
\lambda=\mu.
$$
Undoing the initial $N_ H(S)(k)$-conjugations to dominant representatives proves that
$\lambda$ and $\mu$ have the same unique representative in $C$, and hence are
$N_ H(S)(k)$-conjugate.

# lemma lem:wound_unipotent_case

## statement
Let $H$ be a smooth connected affine $k$-group such that $R_ {u,k}(H)$ is
$k$-wound. For every algebraic extension $K/k$, the natural map
$$
\mathbb X_ \ast(H)/H(k)\to\mathbb X_ \ast(H_ K)/H(K)
$$
is injective.

## proof
Let $\lambda,\mu\in\mathbb X_ \ast(H)$ become $H(K)$-conjugate. We use again
Theorem 4.2.9 from *Structure and classification of pseudo-reductive groups*: any
two maximal split $k$-tori in a smooth connected affine $k$-group are conjugate
under $k$-rational points.

Choose a maximal split $k$-torus $S\subset H$. Since the image of any
$k$-cocharacter is a split $k$-torus, Theorem 4.2.9 lets us conjugate $\lambda$
and $\mu$, separately by elements of $H(k)$, so that both lie in $X_ \ast(S)$.
These conjugated cocharacters are still $H(K)$-conjugate.

Choose a minimal pseudo-parabolic $k$-subgroup $P$ containing $S$. Applying
Lemma `lem:wound_relative_dominant_representatives` to $H,S,P$, the two
cocharacters in $X_ \ast(S)$ are $N_ H(S)(k)$-conjugate. Hence the original
$\lambda$ and $\mu$ are $H(k)$-conjugate.

# theorem thm:main

## statement
Let $G$ be a (not necessarily reductive) smooth connected affine group over a  (not necessarily perfect) field $k$. Let $K$ be an algebraic field extension of $k$. Let $\mathbb{X}_ \ast(G):=\mathrm{Hom}_ {k\text{-groups}}(\mathbb{G}_ m,G)$ $k$-homomorphisms. Let $G_ K$ be the base change of $G$ to $K$. Prove (or disprove with a counterexample) that $\mathbb{X}_ \ast(G)/G(k)\rightarrow\mathbb{X}_ \ast(G_ K)/G(K)$ is injective. (You can take for granted that this statement is true if $k$ is a perfect field.)

## proof
We prove that the displayed map is injective; hence there is no counterexample.

Let
$$
U=R_ {us,k}(G)
$$
be the maximal $k$-split smooth connected unipotent normal $k$-subgroup of $G$,
and set $\overline G=G/U$.

We use the following cited result.

Complete cited statement: Corollary 3.12 in *The structure of solvable groups over fields* states that for any smooth connected affine $k$-group $G$,
$$
R_ {us,k}(G)=R_ {u,k}(G)_ {\mathrm{split}}.
$$
In particular,
$$
R_ {u,k}(G)/R_ {us,k}(G)
$$
is $k$-wound.

paper_id: The structure of solvable groups over fields  
theorem_id: Corollary 3.12  
arXiv id:

Applying this result to $G$, the unipotent radical of $\overline G$ is
$$
R_ {u,k}(\overline G)=R_ {u,k}(G)/R_ {us,k}(G),
$$
which is $k$-wound. Therefore Lemma `lem:wound_unipotent_case` proves injectivity
for $\overline G$.

Finally Lemma `lem:split_unipotent_reduction` lifts injectivity from $\overline G$
to $G$. Thus, if two $k$-homomorphisms
$$
\mathbf G_ m\to G
$$
become conjugate by an element of $G(K)$, then they were already conjugate by an
element of $G(k)$. Equivalently,
$$
\mathbb X_ \ast(G)/G(k)\to \mathbb X_ \ast(G_ K)/G(K)
$$
is injective.