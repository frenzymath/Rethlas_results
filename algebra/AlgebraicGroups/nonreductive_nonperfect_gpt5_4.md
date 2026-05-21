+++
title = "blueprint"
date = 2026-04-29
weight = 3
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

We prove $H^1(k,U)=1$ by induction on $r$. The case $r=0$ is trivial. For the induction step, choose an exact sequence
$$
1\to U_ 1\to U\to \mathbf G_ a\to 1.
$$
The standard exact sequence in nonabelian fppf cohomology gives
$$
H^1(k,U_ 1)\to H^1(k,U)\to H^1(k,\mathbf G_ a).
$$
By induction $H^1(k,U_ 1)=1$, and by additive Hilbert 90 we have
$$
H^1(k,\mathbf G_ a)=0.
$$
Hence $H^1(k,U)=1$.

For the surjectivity statement, let $q\in Q(k)$. The fiber $\pi^{-1}(q)$ is a left $U$-torsor over $\operatorname{Spec}(k)$. Since $H^1(k,U)=1$, that torsor is trivial, so it has a $k$-point. Therefore $q$ lifts to an element of $E(k)$.

# lemma lem:reduction_by_split_unipotent_radical

## statement
Let $G$ be a smooth connected affine $k$-group, let
$$
U:=R_ {us,k}(G)
$$
be the maximal $k$-split smooth connected unipotent normal $k$-subgroup, and write
$$
\pi:G\to \overline G:=G/U.
$$
Assume that for every algebraic extension $K/k$ the natural map
$$
\mathbb X_ \ast(\overline G)/\overline G(k)\to \mathbb X_ \ast(\overline G_ K)/\overline G(K)
$$
is injective. Then for every algebraic extension $K/k$ the natural map
$$
\mathbb X_ \ast(G)/G(k)\to \mathbb X_ \ast(G_ K)/G(K)
$$
is injective.

## proof
Let $K/k$ be algebraic, and let $\lambda,\mu\in \mathbb X_ \ast(G)$ become $G(K)$-conjugate. Their images
$$
\overline\lambda:=\pi\circ \lambda,\qquad \overline\mu:=\pi\circ \mu
$$
become $\overline G(K)$-conjugate. By injectivity for $\overline G$, there exists $\overline g\in \overline G(k)$ such that
$$
\overline\mu=\operatorname{Int}(\overline g)\circ \overline\lambda.
$$
By Lemma `lem:split_unipotent_h1`, the map $G(k)\to \overline G(k)$ is surjective, so choose $g\in G(k)$ lifting $\overline g$. Replacing $\lambda$ by $\operatorname{Int}(g)\circ\lambda$, we reduce to the case
$$
\overline\lambda=\overline\mu=:\nu.
$$

Let
$$
E:=\pi^{-1}(\nu(\mathbf G_ m))\subset G.
$$
Then
$$
1\to U\to E\xrightarrow{\pi} \nu(\mathbf G_ m)\simeq \mathbf G_ m\to 1
$$
is exact, and both $\lambda$ and $\mu$ are $k$-sections of $\pi$.

Because $U$ is unipotent, every $k$-split torus in $E$ maps injectively into $\nu(\mathbf G_ m)$, so every $k$-split torus in $E$ has dimension at most $1$. Hence $\lambda(\mathbf G_ m)$ and $\mu(\mathbf G_ m)$ are maximal split $k$-tori of $E$.

We use the following cited result.

Complete cited statement: Theorem 4.2.9 in *Structure and classification of pseudo-reductive groups* states: “Any two maximal split $k$-tori in a smooth connected affine $k$-group $G$ are conjugate under $G(k)$.”

paper_id: Structure and classification of pseudo-reductive groups  
theorem_id: Theorem 4.2.9  
arXiv id:

Applying this to $E$, there exists $e\in E(k)$ such that
$$
e\lambda(\mathbf G_ m)e^{-1}=\mu(\mathbf G_ m).
$$
Since $\pi(e)\in \nu(\mathbf G_ m)(k)=\mu(\mathbf G_ m)(k)$, choose $t\in \mathbf G_ m(k)$ such that
$$
\mu(t)=\pi(e).
$$
Then
$$
u:=\mu(t)^{-1}e\in U(k),
$$
and $u$ still conjugates $\lambda(\mathbf G_ m)$ onto $\mu(\mathbf G_ m)$ because $\mu(t)$ centralizes $\mu(\mathbf G_ m)$.

Finally, $\operatorname{Int}(u)\circ\lambda$ and $\mu$ are both sections of $\pi:E\to \nu(\mathbf G_ m)$ with the same image torus $\mu(\mathbf G_ m)$. Since $\pi|_ {\mu(\mathbf G_ m)}:\mu(\mathbf G_ m)\to \nu(\mathbf G_ m)$ is an isomorphism, there is only one such section. Therefore
$$
\mu=\operatorname{Int}(u)\circ\lambda.
$$
So $\lambda$ and $\mu$ are $G(k)$-conjugate.

# lemma lem:reduction_by_central_split_torus

## statement
Let $G$ be a smooth connected affine $k$-group, let
$$
1\to Z\to G\xrightarrow{\pi} \overline G\to 1
$$
be an exact sequence with $Z$ a central split $k$-torus, and assume that for every algebraic extension $K/k$ the natural map
$$
\mathbb X_ \ast(\overline G)/\overline G(k)\to \mathbb X_ \ast(\overline G_ K)/\overline G(K)
$$
is injective. Then for every algebraic extension $K/k$ the natural map
$$
\mathbb X_ \ast(G)/G(k)\to \mathbb X_ \ast(G_ K)/G(K)
$$
is injective.

## proof
Let $K/k$ be algebraic and let $\lambda,\mu\in \mathbb X_ \ast(G)$ become $G(K)$-conjugate. Their images $\overline\lambda,\overline\mu\in \mathbb X_ \ast(\overline G)$ become $\overline G(K)$-conjugate. By injectivity for $\overline G$, there exists $\overline g\in \overline G(k)$ such that
$$
\overline\mu=\operatorname{Int}(\overline g)\circ \overline\lambda.
$$

Since $Z\simeq \mathbf G_ m^n$ is split, $H^1(k,Z)=1$ by Hilbert 90, so $G(k)\to \overline G(k)$ is surjective. Choose $g\in G(k)$ lifting $\overline g$. Replacing $\lambda$ by $\operatorname{Int}(g)\circ\lambda$, we reduce to the case
$$
\overline\lambda=\overline\mu=:\nu.
$$

Let
$$
M:=\pi^{-1}(\nu(\mathbf G_ m)).
$$
Then
$$
1\to Z\to M\to \nu(\mathbf G_ m)\simeq \mathbf G_ m\to 1
$$
is an exact sequence of tori. Because both kernel and quotient are split, $M$ is itself a split $k$-torus: on character lattices we get a short exact sequence of free abelian groups, hence a split exact sequence. In particular, $M$ is commutative.

Choose $h\in G(K)$ such that
$$
\mu=\operatorname{Int}(h)\circ\lambda.
$$
Since $\pi\circ\lambda=\pi\circ\mu=\nu$, the element $\pi(h)$ centralizes $\nu(\mathbf G_ m)$. Hence $h$ normalizes $M_ K$, and conjugation by $h$ induces an automorphism of the split torus $M_ K$.

This automorphism acts trivially on the quotient $\nu(\mathbf G_ m)_ K$, because $\pi(h)$ centralizes that torus, and it acts trivially on the kernel $Z_ K$, because $Z$ is central in $G$. Therefore the induced automorphism of the split torus $M_ K$ is the identity: on character lattices it acts trivially on the quotient lattice and on the sublattice coming from $Z$, so it is trivial on all of $X^\ast(M_ K)$.

Thus conjugation by $h$ is trivial on $M_ K$, and hence
$$
\lambda_ K=\mu_ K.
$$
By faithful flat descent for morphisms, $\lambda=\mu$. So $\lambda$ and $\mu$ are already $G(k)$-conjugate.

# lemma lem:wound_radical_centralizes_split_tori

## statement
Let $H$ be a smooth connected affine $k$-group with
$$
R_ {us,k}(H)=1,\qquad
R_ {s,k}(H)=1.
$$
Let $R:=R_ k(H)$ be the $k$-radical of $H$, so $R$ is a smooth connected solvable normal $k$-subgroup. Then every split $k$-torus $S\subset H$ centralizes $R$.

## proof
We first show that the solvable group $R$ has no nontrivial split smooth connected normal $k$-subgroup. Indeed, let
$$
N\subset R
$$
be such a subgroup. By the split solvable structure theorem, quoted below, $N$ is a semi-direct product of a split torus against a split unipotent normal subgroup $U=R_ {u,k}(N)$. Since $N$ is normal in $R$ and $R$ is normal in $H$, the subgroup $N$ is normal in $H$, so $U$ is a split smooth connected unipotent normal $k$-subgroup of $H$. Hence
$$
U\subset R_ {us,k}(H)=1.
$$
Thus $N$ is a split torus. But a normal torus in a connected affine group is central, so
$$
N\subset R_ {s,k}(H)=1.
$$
Therefore $N=1$.

We use the following cited result.

Complete cited statement: Theorem 5.4 in *The structure of solvable groups over fields* states that for any solvable smooth connected affine $k$-group $G$, the quotient $G/G_ {\mathrm{split}}$ is a central extension of a $k$-wound unipotent group by a $k$-wound torus, where $G_ {\mathrm{split}}$ is the maximal $k$-split smooth connected normal $k$-subgroup of $G$. In particular, if $G_ {\mathrm{split}}=1$ then $G$ itself is a central extension
$$
1\to T_ w\to G\to U_ w\to 1
$$
with $T_ w$ a $k$-wound torus and $U_ w$ a $k$-wound unipotent group.

paper_id: The structure of solvable groups over fields  
theorem_id: Theorem 5.4  
arXiv id:

Applying this to $R$, the vanishing just proved shows that $R_ {\mathrm{split}}=1$, so $R$ is $k$-wound.

Now let
$$
G:=SR\subset H
$$
be the smooth connected solvable $k$-subgroup generated by $S$ and $R$. Let $G_ {\mathrm{split}}\subset G$ be its maximal split smooth connected normal $k$-subgroup from Theorem 5.4.

Because the inclusion
$$
S\hookrightarrow G
$$
is a homomorphism from a split smooth connected affine $k$-group into $G$, the finality assertion in Theorem 5.4 forces this inclusion to factor through
$$
G_ {\mathrm{split}}\hookrightarrow G.
$$
Hence
$$
S\subset G_ {\mathrm{split}}.
$$

On the other hand,
$$
G_ {\mathrm{split}}\cap R
$$
is a split smooth connected normal $k$-subgroup of the $k$-wound solvable group $R$, so it is trivial. Therefore the projection
$$
G\to G/R\simeq S
$$
restricts to an injective homomorphism $G_ {\mathrm{split}}\to S$. Since the image contains $S$, we obtain
$$
G_ {\mathrm{split}}=S.
$$

Thus $S$ is a normal torus in the connected group $G$. The conjugation action
$$
G\to \underline{\mathrm{Aut}}(S)
$$
factors through an étale $k$-group, so it is trivial on the connected group $G$. Hence $S$ is central in $G$, and therefore $S$ centralizes $R$.

# lemma lem:pseudo_reductive_fixed_torus

## statement
Let $Q$ be a pseudo-reductive $k$-group, let
$$
S\subset Q
$$
be a maximal split $k$-torus, and let $K/k$ be an algebraic extension. If
$$
\lambda,\mu\in X_ \ast(S)
$$
become $Q(K)$-conjugate, then they have the same unique representative in the closed dominant chamber for the relative root system $\Phi(Q,S)$. In particular, they are $N_ Q(S)(k)$-conjugate.

## proof
Choose a minimal pseudo-parabolic $k$-subgroup
$$
P_ 0\subset Q
$$
containing $S$. We use the following cited results.

Complete cited statement: Theorem 5.3.2(i) in *Structure and classification of pseudo-reductive groups* states that for a smooth connected affine $k$-group $G$, a maximal split $k$-torus $S$, and a minimal pseudo-parabolic $k$-subgroup $P$ containing $S$, the set $\Phi(G/R_ {u,k}(G),S)$ is a root system in $X(S)_ \mathbf Q$, the roots coming from $P$ form a positive system, and the natural map
$$
N_ G(S)(k)/Z_ G(S)(k)\to W(\Phi(G/R_ {u,k}(G),S))
$$
is an isomorphism.

paper_id: Structure and classification of pseudo-reductive groups  
theorem_id: Theorem 5.3.2(i)  
arXiv id:

Since $Q$ is pseudo-reductive, $R_ {u,k}(Q)=1$, so Theorem 5.3.2(i) gives a root system
$$
{}^k\Phi:=\Phi(Q,S)
$$
in $X(S)_ \mathbf Q$, with positive system ${}^k\Phi^+$ determined by $P_ 0$, and identifies
$$
N_ Q(S)(k)/Z_ Q(S)(k)
$$
with the Weyl group $W({}^k\Phi)$.

Let
$$
C=\\{\nu\in X_ \ast(S)\mid \langle \beta,\nu\rangle\ge 0\text{ for all }\beta\in {}^k\Phi^+\\}
$$
be the closed dominant chamber. By root-system combinatorics, each $W({}^k\Phi)$-orbit in $X_ \ast(S)$ meets $C$ in exactly one point.

Hence every $\nu\in X_ \ast(S)$ is $N_ Q(S)(k)$-conjugate to a unique element of $C$. It therefore remains to show that $\lambda$ and $\mu$ have the same representative in $C$.

Let $k_ s$ be a separable closure of $k$. Then $Q_ {k_ s}$ is pseudo-split pseudo-reductive. Choose a split maximal $k_ s$-torus
$$
T\subset (P_ 0)_ {k_ s}
$$
containing $S_ {k_ s}$, and choose a minimal pseudo-parabolic $k_ s$-subgroup
$$
B\subset (P_ 0)_ {k_ s}
$$
containing $T$. Let
$$
\Phi_ {\mathrm{abs}}:=\Phi(Q_ {k_ s},T)
$$
be the absolute root system, with positive system $\Phi_ {\mathrm{abs}}^+$ determined by $B$.

We use one further cited result.

Complete cited statement: Theorem 5.3.2(iv) in *Structure and classification of pseudo-reductive groups* states that if $G$ is a smooth connected affine $k$-group with $R_ {u,k}(G)$ $k$-wound, then the root system $\Phi(G,S)$ consists of the nontrivial $S$-weights on $\operatorname{Lie}(G)$.

paper_id: Structure and classification of pseudo-reductive groups  
theorem_id: Theorem 5.3.2(iv)  
arXiv id:

For $\nu\in X_ \ast(S)\subset X_ \ast(T)$ and $\alpha\in \Phi_ {\mathrm{abs}}$, one has
$$
\langle \alpha,\nu\rangle=\langle \alpha|_ S,\nu\rangle.
$$
Since $Q$ is pseudo-reductive, $R_ {u,k}(Q)=1$ is certainly $k$-wound, so Theorem 5.3.2(iv) identifies the relative roots with the nontrivial $S$-weights on $\operatorname{Lie}(Q)$. The positive relative roots are the $S$-weights occurring in $\operatorname{Lie}(P_ 0)$. On the other hand, the absolute positive roots are exactly the nontrivial $T$-weights occurring in $\operatorname{Lie}(B)\subset \operatorname{Lie}((P_ 0)_ {k_ s})$. Therefore every root in $\Phi_ {\mathrm{abs}}^+$ restricts either to $0$ or to an element of ${}^k\Phi^+$, and every element of ${}^k\Phi^+$ arises as the nonzero restriction of some root in $\Phi_ {\mathrm{abs}}^+$. Hence a cocharacter $\nu\in X_ \ast(S)$ lies in $C$ if and only if it is dominant for $\Phi_ {\mathrm{abs}}^+$.

Let $\lambda^+,\mu^+\in C$ be the unique representatives of $\lambda$ and $\mu$ in $C$. Since the relative Weyl action is realized by $N_ Q(S)(k)\subset Q(k)$, the pairs $(\lambda,\lambda^+)$ and $(\mu,\mu^+)$ are already $Q(k)$-conjugate. Thus $\lambda^+$ and $\mu^+$ remain $Q(K)$-conjugate, and hence $Q(\overline k)$-conjugate. We claim that they are in the same orbit under the absolute Weyl group $W(\Phi_ {\mathrm{abs}})$. Let $g\in Q(\overline k)$ satisfy
$$
\mu^+=\operatorname{Int}(g)\circ\lambda^+.
$$
Let
$$
H:=Z_ {Q_ {\overline k}}(\mu^+)^\circ.
$$
Since both $T_ {\overline k}$ and $gT_ {\overline k}g^{-1}$ contain the image of $\mu^+$, they lie in $H$. They are maximal tori of $H$, because any larger torus in $H$ would be a torus in $Q_ {\overline k}$ properly containing $T_ {\overline k}$. By Theorem 4.2.9 applied over the algebraically closed field $\overline k$, any two maximal tori in the smooth connected affine group $H$ are conjugate. So there exists
$$
c\in H(\overline k)
$$
such that
$$
c g T_ {\overline k} g^{-1} c^{-1}=T_ {\overline k}.
$$
Thus
$$
n:=cg\in N_ Q(T)(\overline k)
$$
and still
$$
\mu^+=\operatorname{Int}(n)\circ\lambda^+.
$$
Applying Theorem 5.3.2(i) over the separably closed field $k_ s$ to the maximal split torus $T\subset Q_ {k_ s}$, the quotient $N_ Q(T)/Z_ Q(T)$ is the constant Weyl group $W(\Phi_ {\mathrm{abs}})$. Hence $\lambda$ and $\mu$ lie in the same $W(\Phi_ {\mathrm{abs}})$-orbit.
Hence $\lambda^+$ and $\mu^+$ lie in the same $W(\Phi_ {\mathrm{abs}})$-orbit.

Every absolute Weyl-group orbit in $X_ \ast(T)$ has a unique $\Phi_ {\mathrm{abs}}^+$-dominant element. Since $\lambda^+,\mu^+\in C$, the equivalence between relative and absolute dominance on $X_ \ast(S)$ shows that both $\lambda^+$ and $\mu^+$ are $\Phi_ {\mathrm{abs}}^+$-dominant. Therefore
$$
\lambda^+=\mu^+.
$$
So $\lambda$ and $\mu$ have the same unique representative in $C$, and in particular they are $N_ Q(S)(k)$-conjugate.

# theorem thm:main

## statement
Let $G$ be a (not necessarily reductive) smooth connected affine group over a  (not necessarily perfect) field $k$. Let $K$ be an algebraic field extension of $k$. Let $\mathbb{X}_ \ast(G):=\mathrm{Hom}_ {k\text{-groups}}(\mathbb{G}_ m,G)$ $k$-homomorphisms. Let $G_ K$ be the base change of $G$ to $K$. Prove (or disprove with a counterexample) that $\mathbb{X}_ \ast(G)/G(k)\rightarrow\mathbb{X}_ \ast(G_ K)/G(K)$ is injective. (You can take for granted that this statement is true if $k$ is a perfect field.)

## proof
We prove that the map is injective for every smooth connected affine $k$-group $G$, so there is no counterexample.

Let
$$
\lambda,\mu\in \mathbb X_ \ast(G)
$$
and assume that they become $G(K)$-conjugate.

### Step 1: remove the split unipotent radical

Let
$$
U:=R_ {us,k}(G).
$$
By Lemma `lem:reduction_by_split_unipotent_radical`, it is enough to prove the theorem for
$$
G_ 1:=G/U.
$$
So from now on we replace $G$ by $G_ 1$ and assume
$$
R_ {us,k}(G)=1.
$$

### Step 2: remove the central split-torus part of the solvable radical

We use the following cited result.

Complete cited statement: Corollary 5.12 in *The structure of solvable groups over fields* states: for any smooth connected affine $k$-group $G$, if $R_ {us,k}(G)=1$ then $R_ {s,k}(G)$ is the maximal central $k$-split torus in $G$.

paper_id: The structure of solvable groups over fields  
theorem_id: Corollary 5.12  
arXiv id:

So
$$
Z:=R_ {s,k}(G)
$$
is a central split $k$-torus. By Lemma `lem:reduction_by_central_split_torus`, it is enough to prove the theorem for
$$
G_ 2:=G/Z.
$$
Thus we may replace $G$ by $G_ 2$ and assume
$$
R_ {us,k}(G)=R_ {s,k}(G)=1.
$$

### Step 3: pass from the wound solvable radical to the pseudo-reductive quotient

Let
$$
R:=R_ k(G)
$$
be the $k$-radical. Because
$$
R_ {us,k}(G)=R_ {s,k}(G)=1,
$$
the argument in Lemma `lem:wound_radical_centralizes_split_tori` shows that $R$ has no nontrivial split smooth connected normal $k$-subgroup. Hence Theorem 5.4 implies that $R$ is $k$-wound. Let
$$
Q:=G/R.
$$
Then $Q$ is pseudo-reductive.

Fix a maximal split $k$-torus
$$
S\subset G.
$$
By Lemma `lem:wound_radical_centralizes_split_tori`, the torus $S$ centralizes $R$. Hence the quotient map $G\to Q$ identifies $S$ with a maximal split $k$-torus of $Q$.

We now use the following cited result.

Complete cited statement: Theorem 4.2.9 in *Structure and classification of pseudo-reductive groups* states: “Any two maximal split $k$-tori in a smooth connected affine $k$-group $G$ are conjugate under $G(k)$.”

paper_id: Structure and classification of pseudo-reductive groups  
theorem_id: Theorem 4.2.9  
arXiv id:

Applying this to $G$, after conjugating $\lambda$ and $\mu$ by suitable elements of $G(k)$, we may assume
$$
\lambda,\mu\in X_ \ast(S).
$$
Since $R$ centralizes $S$, the images
$$
\overline\lambda,\overline\mu\in X_ \ast(S)\subset X_ \ast(Q)
$$
are still $Q(K)$-conjugate.

By Lemma `lem:pseudo_reductive_fixed_torus`, $\overline\lambda$ and $\overline\mu$ are $N_ Q(S)(k)$-conjugate. Equivalently, they lie in the same orbit under the Weyl group
$$
N_ Q(S)(k)/Z_ Q(S)(k).
$$

We next use the following cited result.

Complete cited statement: Proposition 5.3.1 in *Structure and classification of pseudo-reductive groups* states that for a maximal split $k$-torus $S$ in a smooth connected affine $k$-group $G$, the quotient $N_ G(S)/Z_ G(S)$ is constant and the natural map
$$
N_ G(S)(k)/Z_ G(S)(k)\to (N_ G(S)/Z_ G(S))(k)
$$
is an equality.

paper_id: Structure and classification of pseudo-reductive groups  
theorem_id: Proposition 5.3.1  
arXiv id:

Because $R$ centralizes $S$, the natural map
$$
N_ G(S)/Z_ G(S)\to N_ Q(S)/Z_ Q(S)
$$
is an isomorphism. So the Weyl element carrying $\overline\lambda$ to $\overline\mu$ is represented by some
$$
n\in N_ G(S)(k).
$$
Again because $R$ centralizes $S$, the action of $n$ on $S$ is the same before and after passage to $Q$. Hence
$$
\mu=\operatorname{Int}(n)\circ \lambda.
$$
So $\lambda$ and $\mu$ are $G(k)$-conjugate.

We have proved that whenever two $k$-defined cocharacters of $G$ become conjugate under $G(K)$, they were already conjugate under $G(k)$. Equivalently,
$$
\mathbb X_ \ast(G)/G(k)\longrightarrow \mathbb X_ \ast(G_ K)/G(K)
$$
is injective.