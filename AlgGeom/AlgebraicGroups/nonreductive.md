+++
title = "blueprint"
date = 2026-04-28
weight = 2
[extra]
math = true
+++

# lemma lem:split_unipotent_h1

## statement
Let $k$ be a field and let $U$ be a smooth connected $k$-split unipotent group. Then
$$
H^1(k,U)=1
$$
for nonabelian fppf cohomology. In particular, if
$$
1\to U\to E\xrightarrow{\pi} Q\to 1
$$
is an exact sequence of smooth affine $k$-groups, then the map
$$
E(k)\to Q(k)
$$
is surjective.

## proof
Since $U$ is $k$-split, there is a composition series by smooth connected normal $k$-subgroups
$$
1=U_ r\subset U_ {r-1}\subset \cdots \subset U_ 1\subset U_ 0=U
$$
such that each quotient $U_ i/U_ {i+1}$ is $k$-isomorphic to $\mathbf G_ a$.

We prove $H^1(k,U)=1$ by induction on $r$. The case $r=0$ is trivial. For the induction step, choose a short exact sequence
$$
1\to U_ 1\to U\to \mathbf G_ a\to 1.
$$
The quotient $U/U_ 1\simeq \mathbf G_ a$ is commutative, so the standard exact sequence in nonabelian fppf cohomology gives
$$
H^1(k,U_ 1)\to H^1(k,U)\to H^1(k,\mathbf G_ a).
$$
By induction $H^1(k,U_ 1)=1$, and by Hilbert 90 for the additive group we have
$$
H^1(k,\mathbf G_ a)=0.
$$
Hence $H^1(k,U)=1$.

For the surjectivity statement, let $q\in Q(k)$. The fiber $\pi^{-1}(q)$ is a left $U$-torsor over $\operatorname{Spec}(k)$. Since $H^1(k,U)=1$, that torsor is trivial, so it has a $k$-point. Therefore $q$ lifts to an element of $E(k)$.

# lemma lem:sections_of_split_unipotent_extension_are_conjugate

## statement
Let $k$ be a perfect field, let $U$ be a smooth connected unipotent $k$-group, let $S$ be a $k$-split torus, and let
$$
1\to U\to E\xrightarrow{\pi} S\to 1
$$
be an exact sequence of smooth connected affine $k$-groups. Then any two $k$-group sections
$$
s_ 1,s_ 2:S\to E
$$
of $\pi$ are conjugate by an element of $U(k)$.

## proof
Because $k$ is perfect and $U$ is smooth connected unipotent, $U$ is $k$-split. We will use this repeatedly.

Set
$$
T_ i=s_ i(S)\subset E \qquad (i=1,2).
$$
Each $T_ i$ is a $k$-split torus and $\pi|_ {T_ i}:T_ i\to S$ is an isomorphism.

We first work over $\overline{k}$. Since $U_ {\overline{k}}$ is unipotent, it contains no nontrivial torus. Therefore any torus $T\subset E_ {\overline{k}}$ has trivial intersection with $U_ {\overline{k}}$, so the map
$$
T\to E_ {\overline{k}}/U_ {\overline{k}}\simeq S_ {\overline{k}}
$$
is injective. Hence
$$
\dim T\le \dim S.
$$
Because each $T_ i$ has dimension $\dim S$, both $T_ {1,\overline{k}}$ and $T_ {2,\overline{k}}$ are maximal tori of $E_ {\overline{k}}$.

Now use the standard structure theorem for connected solvable linear algebraic groups over an algebraically closed field:

Complete cited statement: Theorem 10.6(4) in Borel's *Linear Algebraic Groups* says that if $B$ is a connected solvable linear algebraic group over an algebraically closed field and $T\subset B$ is a maximal torus, then $B=T\ltimes R_ u(B)$. In particular, any two maximal tori of $B$ are conjugate by $R_ u(B)$.

paper_id: Borel, *Linear Algebraic Groups*  
theorem_id: Theorem 10.6(4)  
arXiv id:

Applying this to the connected solvable $\overline{k}$-group $E_ {\overline{k}}$, whose unipotent radical is $U_ {\overline{k}}$, we get some
$$
\overline{u}\in U(\overline{k})
$$
such that
$$
\overline{u}T_ 1\overline{u}^{-1}=T_ 2.
$$

Let
$$
C:=C_ U(T_ 1).
$$
We need to descend $\overline{u}$ to a $k$-point. First observe that $C$ is smooth and connected. Indeed, we use the following cited fact.

Complete cited statement: In Brian Conrad's *Reductive groups over fields* (proof of Theorem 2.1.3), it is shown more generally that if $S$ is a torus in a smooth connected affine group $G$, and $H\subset G$ is a smooth connected subgroup normalized by $S$, then $Z_ G(S)\cap H$ is smooth and connected. In particular, torus centralizers in smooth connected affine groups are smooth and connected.

paper_id: Brian Conrad, *Reductive groups over fields*  
theorem_id: Theorem 2.1.3, proof  
arXiv id:

Apply this with $G=E$, $S=T_ 1$, and $H=U$. Thus $C$ is a smooth connected unipotent $k$-group. Since $k$ is perfect, $C$ is $k$-split.

For $\sigma\in \operatorname{Gal}(\overline{k}/k)$, the equality
$$
\sigma(T_ i)=T_ i
$$
implies
$$
\sigma(\overline{u})T_ 1\sigma(\overline{u})^{-1}=T_ 2=\overline{u}T_ 1\overline{u}^{-1}.
$$
Hence
$$
\overline{u}^{-1}\sigma(\overline{u})\in C(\overline{k}).
$$
So $\sigma\mapsto \overline{u}^{-1}\sigma(\overline{u})$ is a $1$-cocycle with values in $C$. By Lemma `lem:split_unipotent_h1`, $H^1(k,C)=1$. Therefore there exists
$$
c\in C(\overline{k})
$$
such that
$$
\overline{u}^{-1}\sigma(\overline{u})=c^{-1}\sigma(c)
\qquad\text{for all }\sigma.
$$
Then
$$
u:=\overline{u}c^{-1}
$$
is Galois-fixed, so $u\in U(k)$. Since $c$ centralizes $T_ 1$, we still have
$$
uT_ 1u^{-1}=T_ 2.
$$

Finally, $\operatorname{Int}(u)\circ s_ 1$ and $s_ 2$ are both $k$-group sections of $\pi$ whose image is the same torus $T_ 2$. Because $\pi|_ {T_ 2}:T_ 2\to S$ is an isomorphism, there is only one section with image $T_ 2$, namely $(\pi|_ {T_ 2})^{-1}$. Hence
$$
s_ 2=\operatorname{Int}(u)\circ s_ 1.
$$
So $s_ 1$ and $s_ 2$ are $U(k)$-conjugate.

# theorem thm:main

## statement
Let $G$ be a (not necessarily reductive) smooth connected affine group over a perfect field $k$. Let $K$ be an algebraic field extension of $k$. Let $\mathbb{X}_ \ast(G):=\mathrm{Hom}_ {k\text{-groups}}(\mathbb{G}_ m,G)$ $k$-homomorphisms. Let $G_ K$ be the base change of $G$ to $K$. Prove that $\mathbb{X}_ \ast(G)/G(k)\rightarrow\mathbb{X}_ \ast(G_ K)/G(K)$ is injective. (You can take for granted that this statement is true if $G$ is connected reductive over a field $k$.)

## proof
Let
$$
U:=R_ u(G)
$$
be the unipotent radical of $G$, and let
$$
\pi:G\to H:=G/U
$$
be the quotient map. Since $k$ is perfect and $G$ is smooth connected affine, $U$ is a smooth connected unipotent $k$-subgroup. We use the following cited result.

Complete cited statement: Exercise 5.5.10 in Brian Conrad's *Reductive group schemes* records that if $k$ is perfect, then every smooth connected unipotent group over $k$ is split; equivalently, it admits a composition series with successive quotients $k$-isomorphic to $\mathbf G_ a$. The exercise cites Borel, *Linear Algebraic Groups*, Corollary 15.5(ii), and SGA3, XVII, 4.1.3.

paper_id: Brian Conrad, *Reductive group schemes*  
theorem_id: Exercise 5.5.10 (citing Borel 15.5(ii) and SGA3 XVII 4.1.3)  
arXiv id:

Thus $U$ is $k$-split. The quotient $H=G/U$ is a connected reductive $k$-group.

Take
$$
\lambda,\mu\in \mathbb X_ \ast(G)
$$
whose images in
$$
\mathbb X_ \ast(G_ K)/G(K)
$$
coincide. Then there exists $g\in G(K)$ such that
$$
\mu=\operatorname{Int}(g)\circ\lambda
$$
as cocharacters $\mathbf G_ m\to G$.

Projecting to $H_ K$, we obtain
$$
\pi\circ\mu=\operatorname{Int}(\pi(g))\circ (\pi\circ\lambda).
$$
So the cocharacters
$$
\overline{\lambda}:=\pi\circ\lambda,\qquad \overline{\mu}:=\pi\circ\mu
$$
of $H$ become $H(K)$-conjugate. By the reductive case, which we are allowed to assume, there exists
$$
\overline{h}\in H(k)
$$
such that
$$
\overline{\mu}=\operatorname{Int}(\overline{h})\circ \overline{\lambda}.
$$

By Lemma `lem:split_unipotent_h1`, the map
$$
G(k)\to H(k)
$$
is surjective because $U$ is $k$-split unipotent. Choose $h\in G(k)$ lifting $\overline{h}$. Replacing $\lambda$ by $\operatorname{Int}(h)\circ \lambda$, which does not change its class in $\mathbb X_ \ast(G)/G(k)$, we reduce to the case
$$
\overline{\lambda}=\overline{\mu}=:\nu.
$$

If $\nu$ is trivial then $\lambda$ and $\mu$ both land in $U$. But a unipotent group contains no nontrivial torus, so the only cocharacter $\mathbf G_ m\to U$ is the trivial one. Hence $\lambda=\mu$, and we are done.

Assume now that $\nu$ is nontrivial. Its image
$$
S:=\nu(\mathbf G_ m)\subset H
$$
is a $k$-split torus isomorphic to $\mathbf G_ m$. Let
$$
E:=\pi^{-1}(S)\subset G.
$$
Then $E$ is a smooth connected affine $k$-subgroup of $G$, its unipotent radical is still $U$, and there is an exact sequence
$$
1\to U\to E\xrightarrow{\pi} S\to 1.
$$
Indeed, $U$ is a smooth connected unipotent normal subgroup of $E$, and any smooth connected unipotent normal subgroup of $E$ maps trivially to the torus $S$, so must be contained in $U$.
The cocharacters $\lambda,\mu:\mathbf G_ m\to G$ both land in $E$, and each is a $k$-section of $\pi:E\to S$ because $\pi\circ\lambda=\pi\circ\mu=\nu$, which identifies $\mathbf G_ m$ with $S$.

Lemma `lem:sections_of_split_unipotent_extension_are_conjugate` therefore applies to the exact sequence
$$
1\to U\to E\to S\to 1.
$$
It yields an element
$$
u\in U(k)\subset G(k)
$$
such that
$$
\mu=\operatorname{Int}(u)\circ\lambda.
$$
Thus $\lambda$ and $\mu$ are $G(k)$-conjugate.

We have proved that whenever two $k$-defined cocharacters of $G$ become conjugate under $G(K)$, they were already conjugate under $G(k)$. Equivalently, the natural map
$$
\mathbb X_ \ast(G)/G(k)\longrightarrow \mathbb X_ \ast(G_ K)/G(K)
$$
is injective.