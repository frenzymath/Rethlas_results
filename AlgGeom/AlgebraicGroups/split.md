+++
title = "blueprint_verified"
date = 2026-04-28
weight = 1
[extra]
math = true
+++

# lemma lem:move_to_split_maximal_torus

## statement
Let $F$ be a field, let $G$ be a split connected reductive $F$-group, and fix a split maximal torus $T\subset G$. Then every $F$-defined cocharacter
$$
\lambda:\mathbb G_ m\to G
$$
is $G(F)$-conjugate to a cocharacter with image in $T$.

## proof
Let $S=\lambda(\mathbb G_ m)$. Since $\lambda$ is an $F$-morphism from $\mathbb G_ m$, the image $S$ is an $F$-split torus in $G$. Choose a maximal $F$-split torus $S_ {\max}\subset G$ containing $S$.

Now use the following cited result.

Complete cited statement: Théorème 3.1.3 (Borel--Tits) in *Grassmanniennes affines tordues sur les entiers* says: "Tous les tores déployés maximaux de $G$ sont conjugués par $G(k)$."  
paper_id: *Grassmanniennes affines tordues sur les entiers*  
theorem_id: Théorème 3.1.3  
arXiv id: 1912.11918

Applying that statement with $F$ in place of $k$, there exists $g\in G(F)$ such that
$$
gS_ {\max}g^{-1}=T.
$$
Since $S\subset S_ {\max}$, we get $gSg^{-1}\subset T$. Equivalently, the cocharacter
$$
\operatorname{Int}(g)\circ\lambda:\mathbb G_ m\to G
$$
factors through $T$. Hence $\lambda$ is $G(F)$-conjugate to a cocharacter of $T$.

# lemma lem:conjugate_in_torus_implies_rationally_conjugate

## statement
Let $F$ be a field, let $G$ be a split connected reductive $F$-group, let $T\subset G$ be a split maximal torus, and let $W=N_ G(T)/T$ be the Weyl group. If
$$
\lambda,\mu\in \mathbb X_ \ast(T)
$$
become $G(\Omega)$-conjugate for some field extension $\Omega/F$, then $\lambda$ and $\mu$ are already $G(F)$-conjugate.

## proof
Assume that $\mu=\operatorname{Int}(h)\circ\lambda$ for some $h\in G(\Omega)$. Then $\lambda$ and $\mu$ are also $G(\overline{\Omega})$-conjugate.

We first convert this conjugacy into a Weyl-group relation. The needed external result is:

Complete cited statement: Lemma 4.20 in *Non-semi-stable loci in Hecke stacks and Fargues' conjecture* says: "Given two cocharacters $\mu,\mu'\in X_ \ast(T)$ which are $G$-conjugate, then there exists an element $w$ of the absolute Weyl group of $T$ in $G$ such that $w\cdot \mu=\mu'$."  
paper_id: *Non-semi-stable loci in Hecke stacks and Fargues' conjecture*  
theorem_id: Lemma 4.20  
arXiv id: 1608.07446

Since $T$ is $F$-split, its absolute Weyl group over $\overline{\Omega}$ is canonically the same finite Weyl group
$$
W=N_ G(T)/T.
$$
Applying the cited lemma over $\overline{\Omega}$, we obtain $w\in W$ such that
$$
\mu=w\cdot\lambda.
$$

Because $G$ is split, every Weyl-group element has an $F$-rational representative. More precisely, we use:

Complete cited statement: Corollary 5.1.11 in Brian Conrad's *Reductive group schemes* says: "Let $(G,T,M)$ be a split reductive group over a nonempty scheme $S$. Fix linked trivializations $X_ a\in W(\mathfrak g_ a)^\times(S)$ for all $a\in \Phi$ (so $X_ {-a}$ is dual to $X_ a$). The natural map $N_ G(T)(S)\to W_ G(T)(S)$ is surjective, with $n_ a$ mapping to the reflection $s_ a$."  
paper_id: *Reductive group schemes*  
theorem_id: Corollary 5.1.11  
arXiv id:

Applying this with $S=\operatorname{Spec}(F)$, the map
$$
N_ G(T)(F)\to W(F)=W
$$
is surjective. Choose $n_ w\in N_ G(T)(F)$ lifting $w$. Then
$$
\operatorname{Int}(n_ w)\circ\lambda=w\cdot\lambda=\mu.
$$
Therefore $\lambda$ and $\mu$ are $G(F)$-conjugate.

# theorem thm:main

## statement
Let $G$ be a split connected reductive group over a field $k$. Let $K$ be an algebraic field extension of $k$. Let $\mathbb{X}_ \ast(G):=\mathrm{Hom}_ {\text{group}}(\mathbb{G}_ m,G)$. Let $G_ K$ be the base change of $G$ to $K$. Prove that $\mathbb{X}_ \ast(G)/G(k)\rightarrow\mathbb{X}_ \ast(G_ K)/G(K)$ is injective.

## proof
Fix a split maximal torus $T\subset G$. We must show that if two $k$-defined cocharacters of $G$ become conjugate under $G(K)$, then they were already conjugate under $G(k)$.

Take $\lambda,\mu\in \mathbb X_ \ast(G)$ whose images in $\mathbb X_ \ast(G_ K)/G(K)$ are equal. By definition of the quotient, there exists $g\in G(K)$ such that
$$
\mu=\operatorname{Int}(g)\circ \lambda
$$
as cocharacters $ \mathbb G_ {m,K}\to G_ K$.

By Lemma `lem:move_to_split_maximal_torus` over the field $k$, there exist $g_ 1,g_ 2\in G(k)$ such that
$$
\lambda_ 1:=\operatorname{Int}(g_ 1)\circ\lambda,\qquad
\mu_ 1:=\operatorname{Int}(g_ 2)\circ\mu
$$
both lie in $\mathbb X_ \ast(T)$. Since $\mu=\operatorname{Int}(g)\circ\lambda$, we have
$$
\mu_ 1=\operatorname{Int}(g_ 2gg_ 1^{-1})\circ \lambda_ 1,
$$
and $g_ 2gg_ 1^{-1}\in G(K)$. Thus $\lambda_ 1$ and $\mu_ 1$ are $G(K)$-conjugate.

Now apply Lemma `lem:conjugate_in_torus_implies_rationally_conjugate` with $F=k$ and $\Omega=K$. It follows that $\lambda_ 1$ and $\mu_ 1$ are already $G(k)$-conjugate. Therefore $\lambda$ and $\mu$ are $G(k)$-conjugate as well.

So two cocharacters of $G$ that map to the same class in $\mathbb X_ \ast(G_ K)/G(K)$ already define the same class in $\mathbb X_ \ast(G)/G(k)$. This proves that
$$
\mathbb X_ \ast(G)/G(k)\longrightarrow \mathbb X_ \ast(G_ K)/G(K)
$$
is injective.