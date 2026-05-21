+++
title = "blueprint_verified"
date = 2026-04-28
weight = 2
[extra]
math = true
+++

# lemma lem:move_into_fixed_maximal_split_torus

## statement
Let $F$ be a field, let $H$ be a connected reductive $F$-group, and let
$$
S \subset H
$$
be a maximal $F$-split torus. Then every $F$-defined cocharacter
$$
\lambda:\mathbf G_ m \to H
$$
is $H(F)$-conjugate to a cocharacter with image in $S$.

## proof
The image $\lambda(\mathbf G_ m)$ is an $F$-split torus in $H$, so it is contained in some maximal $F$-split torus $S_ \lambda\subset H$.

We use the following cited result.

Complete cited statement: Théorème 3.1.3 in *Grassmanniennes affines tordues sur les entiers* states: “Tous les tores déployés maximaux de $G$ sont conjugués par $G(k)$.”

paper_id: Grassmanniennes affines tordues sur les entiers  
theorem_id: Théorème 3.1.3  
arXiv id: 1912.11918

Applying this with $H$ in place of $G$, there exists $h\in H(F)$ such that
$$
hS_ \lambda h^{-1}=S.
$$
Since $\lambda(\mathbf G_ m)\subset S_ \lambda$, the conjugate cocharacter
$$
h\cdot \lambda := \operatorname{Int}(h)\circ \lambda
$$
has image in $S$. So every $F$-defined cocharacter is $H(F)$-conjugate to one valued in $S$.

# lemma lem:relative_dominant_representatives

## statement
Let $F$ be a field, let $H$ be a connected reductive $F$-group, let
$$
S \subset H
$$
be a maximal $F$-split torus, and let $P_ 0\subset H$ be a minimal parabolic $F$-subgroup containing $S$. Let $\Phi(H,S)^+$ be the corresponding positive system in the relative root system $\Phi(H,S)$, and let
$$
C=\\{\nu\in X_ \ast(S)\mid \langle \beta,\nu\rangle \ge 0\text{ for all }\beta\in \Phi(H,S)^+\\}
$$
be the closed relative dominant chamber. Then:

1. every $\nu\in X_ \ast(S)$ is $N_ H(S)(F)$-conjugate to a unique element of $C$;
2. if $\lambda,\mu\in X_ \ast(S)$ become $H(\Omega)$-conjugate for some algebraic extension $\Omega/F$, then $\lambda$ and $\mu$ have the same unique representative in $C$.

## proof
Choose a maximal $F$-torus $T\subset Z_ H(S)$. Since $Z_ H(S)$ is a Levi $F$-subgroup of $P_ 0$, we have $T\subset P_ 0$. Fix a Borel subgroup
$$
B \subset H_ {\overline F}
$$
containing $T_ {\overline F}$ and contained in $P_ {0,\overline F}$. Let
$$
\Phi_ {\mathrm{abs}}=\Phi(H_ {\overline F},T_ {\overline F})
$$
be the absolute root system, and let $\Phi_ {\mathrm{abs}}^+$ be the positive system defined by $B$.

For $\nu\in X_ \ast(S)\subset X_ \ast(T)$ and $\alpha\in \Phi_ {\mathrm{abs}}$, one has
$$
\langle \alpha,\nu\rangle = \langle \alpha|_ S,\nu\rangle.
$$
Also, by construction of the relative root system, every positive absolute root restricts either to $0$ or to a positive relative root, and every positive relative root arises as the restriction of some positive absolute root. Hence a cocharacter $\nu\in X_ \ast(S)$ is dominant for $\Phi_ {\mathrm{abs}}^+$ if and only if it is dominant for $\Phi(H,S)^+$, i.e. if and only if $\nu\in C$.

For part (1), we use the following cited result.

Complete cited statement: Theorem 11.4.6 in *Reductive groups over fields* states that the natural inclusion $W(\Phi(H,S)) \subset W(H,S)$ is an equality, where $W(H,S)$ is the relative Weyl group attached to $S$.

paper_id: Reductive groups over fields  
theorem_id: Theorem 11.4.6  
arXiv id:

Thus the relative Weyl group $(N_ H(S)/Z_ H(S))(F)$ acts on $X_ \ast(S)$ through the Weyl group of the relative root system. By the standard combinatorics of root systems, every Weyl-group orbit meets the closed dominant chamber $C$ in exactly one point.

To realize those Weyl elements by $F$-rational normalizer elements, we use the following cited result.

Complete cited statement: Lemma 4.1 and Proposition 4.2 in *Math 249B. Relative Bruhat decomposition and relative Weyl group* state that $N_ H(S)/Z_ H(S)$ is a constant finite étale $F$-group and that the natural map
$$
N_ H(S)(F)/Z_ H(S)(F)\to (N_ H(S)/Z_ H(S))(F)
$$
is surjective.

paper_id: Conrad relative Bruhat handout  
theorem_id: Lemma 4.1; Proposition 4.2  
arXiv id:

Therefore every relative Weyl element has an $F$-rational representative in $N_ H(S)(F)$, so every $\nu\in X_ \ast(S)$ is $N_ H(S)(F)$-conjugate to a unique element of $C$.

For part (2), let $\lambda^+,\mu^+\in C$ be the unique relative-dominant representatives of $\lambda$ and $\mu$ given by part (1). Since part (1) realizes the relative Weyl action by elements of $N_ H(S)(F)\subset H(F)$, the pairs $(\lambda,\lambda^+)$ and $(\mu,\mu^+)$ are already $H(F)$-conjugate. Hence $\lambda^+$ and $\mu^+$ are still $H(\Omega)$-conjugate, and therefore $H(\overline F)$-conjugate. Since both are cocharacters of the common maximal torus $T_ {\overline F}$, we may apply the following cited result.

Complete cited statement: Lemma 4.20 in *Non-semi-stable loci in Hecke stacks and Fargues' conjecture* states: “Given two cocharacters $\mu,\mu'\in X_ \ast(T)$ which are $G$-conjugate, then there exists an element $w$ of the absolute Weyl group of $T$ in $G$ such that $w\cdot \mu=\mu'$.”

paper_id: Non-semi-stable loci in Hecke stacks and Fargues' conjecture  
theorem_id: Lemma 4.20  
arXiv id: 1608.07446

So $\lambda^+$ and $\mu^+$ lie in the same orbit under the absolute Weyl group of $T$. But $\lambda^+,\mu^+\in C$, and we already checked that on $X_ \ast(S)$ relative dominance is equivalent to absolute dominance. Thus both $\lambda^+$ and $\mu^+$ are $\Phi_ {\mathrm{abs}}^+$-dominant. Every absolute Weyl orbit in $X_ \ast(T)$ has a unique $\Phi_ {\mathrm{abs}}^+$-dominant element, so $\lambda^+=\mu^+$. Therefore $\lambda$ and $\mu$ have the same unique representative in $C$. This proves part (2).

# theorem thm:main

## statement
Let $G$ be a (not necessarily split) connected reductive group over a field $k$. Let $K$ be an algebraic field extension of $k$. Let $\mathbb{X}_ \ast(G):=\mathrm{Hom}_ {k\text{-groups}}(\mathbb{G}_ m,G)$ $k$-homomorphisms. Let $G_ K$ be the base change of $G$ to $K$. Prove that $\mathbb{X}_ \ast(G)/G(k)\rightarrow\mathbb{X}_ \ast(G_ K)/G(K)$ is injective.

## proof
Fix a maximal $k$-split torus $S\subset G$ and a minimal parabolic $k$-subgroup $P_ 0\subset G$ containing $S$.

Take $\lambda,\mu\in \mathbb X_ \ast(G)$ whose images in
$$
\mathbb X_ \ast(G_ K)/G(K)
$$
coincide. By definition, there exists $g\in G(K)$ such that
$$
\mu=\operatorname{Int}(g)\circ \lambda.
$$

By Lemma `lem:move_into_fixed_maximal_split_torus`, there exist $x,y\in G(k)$ such that
$$
\lambda_ 1:=x\cdot \lambda,\qquad \mu_ 1:=y\cdot \mu
$$
both lie in $X_ \ast(S)$. Since $\mu$ and $\lambda$ are $G(K)$-conjugate, so are $\mu_ 1$ and $\lambda_ 1$.

Now apply Lemma `lem:relative_dominant_representatives` to the connected reductive group $G$, the maximal $k$-split torus $S$, and the minimal parabolic $P_ 0$. Part (2) shows that $\lambda_ 1$ and $\mu_ 1$ have the same unique representative in the closed relative dominant chamber. Then part (1) shows that $\lambda_ 1$ and $\mu_ 1$ are $N_ G(S)(k)$-conjugate, hence $G(k)$-conjugate.

Undoing the conjugations by $x$ and $y$, we conclude that $\lambda$ and $\mu$ are $G(k)$-conjugate. Therefore two $k$-defined cocharacters of $G$ that become conjugate over $K$ were already conjugate over $k$. Equivalently,
$$
\mathbb X_ \ast(G)/G(k)\longrightarrow \mathbb X_ \ast(G_ K)/G(K)
$$
is injective.