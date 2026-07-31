# lemma lem:finite-field-characteristic-count

## statement

Let \(E\) be a set of projective points spanning an \(n\)-dimensional
\(\mathbb F_q\)-space \(X\), and let \(M(E)\) be its vector matroid. If
\(Q=q^m\), then

\[
 \chi_{M(E)}(Q)
 =\#\{\phi:X\longrightarrow\mathbb F_Q:
          \phi(x)\ne0\text{ for every }x\in E\}.                 \tag{1}
\]

Moreover, if

\[
 I_h(Q)=\prod_{j=0}^{h-1}(Q-q^j),
\]

then, for every \(n\geq0\),

\[
 Q^n=\sum_{h=0}^n {n\brack h}_q I_h(Q).                          \tag{2}
\]

## proof

The subset expansion of the characteristic polynomial is

\[
 \chi_{M(E)}(Q)=\sum_{A\subseteq E}(-1)^{|A|}Q^{n-r(A)}.
\]

Inclusion--exclusion gives the same expression for the number of linear
maps \(X\to\mathbb F_Q\) which vanish on none of the points of \(E\),
because the maps vanishing on a fixed \(A\) form a space of cardinality
\(Q^{n-r(A)}\). This proves (1).

For (2), count all linear maps from an \(n\)-space to \(\mathbb F_Q\) by
the codimension \(h\) of their kernel. There are \({n\brack h}_q\) choices
for the kernel and \(I_h(Q)\) injective maps from the resulting
\(h\)-dimensional quotient to \(\mathbb F_Q\).

# lemma lem:projective-deletion-convolution

## statement

Let \(V\) be an \(r\)-dimensional \(\mathbb F_q\)-space, let \(D\) be any
set of points of \(PG(V)\), and put

\[
 M=PG(V)\setminus D,
 \qquad
 C_D(t)=\sum_{\substack{A\leq V\\PG(A)\subseteq D}}t^{\dim A}.   \tag{3}
\]

The zero subspace is included in this sum. For a flat \(F\) of \(M\), put
\(U=\operatorname{span}F\), and define \(D_U\subseteq PG(V/U)\) as follows:
a quotient point \(B/U\), where \(\dim(B/U)=1\), belongs to \(D_U\) if and
only if

\[
 PG(B)\setminus PG(U)\subseteq D.                                \tag{4}
\]

Then

\[
 t^rC_D(t^{-1})
 =\sum_{F\in L(M)}\chi_{M|F}(t)C_{D_U}(t).                       \tag{5}
\]

## proof

First note the flat and contraction descriptions implicit in the statement.
For a subspace \(U\leq V\), the surviving points in \(PG(U)\) form a flat
of \(M\) precisely when they span \(U\); every flat arises uniquely this
way, with \(U=\operatorname{span}F\). In the contraction by this flat, a
point of \(PG(V/U)\) is represented unless every point in its fiber outside
\(PG(U)\) was deleted. Consequently the simplification of \(M/F\) is

\[
 PG(V/U)\setminus D_U.                                           \tag{6}
\]

Parallel simplification does not change the ranked lattice of flats, hence
does not change the characteristic polynomials of its intervals or its
Kazhdan--Lusztig polynomial.

We prove (5) by evaluating both sides at the infinitely many integers
\(Q=q^m\). By Lemma lem:finite-field-characteristic-count,
\(\chi_{M|F}(Q)\) counts the maps
\(\phi:U\to\mathbb F_Q\) which are nonzero on every surviving point of
\(PG(U)\). A subspace \(\bar A\leq V/U\) counted by \(C_{D_U}(Q)\) has the
form \(\bar A=B/U\), where

\[
 PG(B)\setminus PG(U)\subseteq D.                                \tag{7}
\]

Its weight \(Q^{\dim(B/U)}\) is the number of extensions of \(\phi\) to a
linear map \(\psi:B\to\mathbb F_Q\). Thus the right side of (5), evaluated
at \(Q\), counts triples \((U,B,\psi)\) with (7), with \(U\) spanned by its
surviving points, and with \(\psi\) nonzero on those points.

Equivalently, it counts pairs

\[
 (B,\psi),\qquad B\leq V,\quad
 \psi:B\to\mathbb F_Q,\quad
 \psi(x)\ne0\text{ for every }x\in PG(B)\setminus D.             \tag{8}
\]

Indeed, a pair (8) determines the unique subspace

\[
 U=\operatorname{span}(PG(B)\setminus D).
\]

This \(U\) gives a flat of \(M\), all the points of
\(PG(B)\setminus PG(U)\) are deleted, and restriction of \(\psi\) gives
the required \(\phi\). Conversely every triple above plainly gives (8).

Now classify the pairs (8) by \(A=\ker\psi\). Their defining condition is
equivalent to \(PG(A)\subseteq D\). For a fixed such \(A\), with
\(a=\dim A\), choose \(h=\dim(B/A)\). There are
\({r-a\brack h}_q\) choices for \(B/A\) and \(I_h(Q)\) choices for the
induced injection \(B/A\to\mathbb F_Q\). Equation (2) therefore gives

\[
 \sum_{h\geq0}{r-a\brack h}_q I_h(Q)=Q^{r-a}.
\]

Summing over \(A\) shows that the right side of (5) is

\[
 \sum_{\substack{A\leq V\\PG(A)\subseteq D}}Q^{r-\dim A}
 =Q^rC_D(Q^{-1}),
\]

which is its left side. Equality at infinitely many \(Q\) proves the
polynomial identity.

# lemma lem:projective-deletion-degree-criterion

## statement

Use the notation of Lemma lem:projective-deletion-convolution, and assume
that the surviving points span \(V\), so that \(\operatorname{rk}M=r\).
Suppose that for every flat \(F\) with \(U=\operatorname{span}F\) and
\(\dim U<r\),

\[
 \deg C_{D_U}<\frac{r-\dim U}{2}.                                \tag{9}
\]

Then

\[
 P_M(t)=C_D(t).                                                   \tag{10}
\]

## proof

If \(U\subseteq B\) are spans of flats, quotienting first by \(U\) and then
by \(B/U\) gives the same deleted point set as quotienting directly by
\(B\):

\[
 (D_U)_{B/U}=D_B.                                                 \tag{11}
\]

Indeed, a direction modulo \(B\) is absent after the two quotients exactly
when every original projective point in its fiber outside \(PG(B)\) lies
in \(D\), which is the defining condition for membership in \(D_B\).
Also, the flats above \(F_U\) are precisely the flats of \(M/F_U\).
Thus hypothesis (9) is inherited by every contraction.

We prove (10), simultaneously for all these contractions, by induction on
their rank. Since the surviving points span \(V\), their images span every
quotient \(V/U\); because \(F_U\) spans \(U\), this gives

\[
 \operatorname{rk}(M/F_U)=r-\dim U.                              \tag{12}
\]

The rank-zero case is \(U=V\), where \(D_V\) is empty in the zero-dimensional
quotient and \(C_{D_V}=1\), as required by the defining normalization.
Now fix \(U\) and suppose the assertion is known for every proper
contraction above it. By (6), those contractions have polynomials
\(C_{D_B}\). Apply identity (5) in the quotient \(V/U\), and compare it
with the defining recursion for \(P_{M/F_U}\). By (12), the reciprocal
exponents in the two identities are equal, and all nonempty-flat terms
agree by induction. Hence

\[
 H(t)=P_{M/F_U}(t)-C_{D_U}(t)
\]

satisfies

\[
 t^{r-\dim U}H(t^{-1})=H(t).
\]

Both summands defining \(H\) have degree less than
\((r-\dim U)/2\), by the KL degree axiom and (9). The degrees on the two
sides of the displayed reciprocal identity are therefore disjoint unless
\(H=0\). Taking \(U=0\) proves (10).

# theorem thm:explicit-counterexample

## statement

There is a simple binary matroid \(M\) of rank \(7\) on \(114\) points for
which

\[
 P_M(t)=1+13t+7t^2+t^3,                                          \tag{13}
\]

and this polynomial has two nonreal zeros.

## proof

Let \(V=\mathbb F_2^7\) with basis \(e_1,\ldots,e_7\), and put

\[
 W_0=\langle e_1,e_2,e_3\rangle.
\]

Because the field is binary, we identify a nonzero vector with its
projective point. Define

\[
\begin{aligned}
 S=\{&e_4,\ e_4+e_5,\ e_4+e_6,\ e_4+e_7,\\
     &e_4+e_5+e_6,\ e_4+e_5+e_7\},\\
 D={}&(W_0\setminus\{0\})\cup S,
\end{aligned}                                                     \tag{14}
\]

and let \(M=PG(6,2)\setminus D\). The surviving points span \(V\): for
example \(e_5,e_6,e_7\) survive, as do \(e_1+e_5,e_2+e_5,e_3+e_5\), and
\(e_4+e_6+e_7\); these vectors span all seven basis vectors. Thus \(M\)
has rank \(7\). It is simple because it is a restriction of a projective
geometry, and it has \(2^7-1-13=114\) points.

We first count the subspaces \(A\) with \(PG(A)\subseteq D\). There is one
zero subspace and there are \(13\) one-dimensional subspaces. The sum of
two distinct vectors of \(S\) is a nonzero vector in
\(\langle e_5,e_6,e_7\rangle\), so it is not in \(D\). The sum of a vector
of \(S\) and a nonzero vector of \(W_0\) has both a nonzero
\(W_0\)-component and a nonzero \(e_4\)-component, and is likewise not in
\(D\). Hence no subspace of dimension at least two which contains a point
of \(S\) is contained in \(D\). The remaining contained subspaces lie in
\(W_0\). There are

\[
 {3\brack2}_2=7
\]

two-dimensional subspaces of \(W_0\), exactly one three-dimensional
subspace \(W_0\), and none of larger dimension. Consequently

\[
 C_D(t)=1+13t+7t^2+t^3.                                          \tag{15}
\]

It remains to verify the degree hypothesis (9). Let \(U\) be the span of
any flat, put \(k=\dim U<7\), and suppose that an \(h\)-dimensional
subspace \(\bar A\leq V/U\) is counted by \(C_{D_U}\). If \(B\) is its
preimage in \(V\), then (4) gives

\[
 PG(B)\setminus PG(U)\subseteq D.
\]

The left side contains

\[
 (2^{k+h}-1)-(2^k-1)=2^k(2^h-1)                                \tag{16}
\]

points, whereas \(|D|=13\). If \(h\geq(7-k)/2\), the least possible
integer \(h\) and the corresponding lower bound in (16) are

\[
\begin{array}{c|rrrrrrr}
 k&0&1&2&3&4&5&6\\ \hline
 \lceil(7-k)/2\rceil&4&3&3&2&2&1&1\\
 2^k(2^h-1)&15&14&28&24&48&32&64 .
\end{array}
\]

Every entry in the last row exceeds \(13\), a contradiction. Therefore
\(\deg C_{D_U}<(7-k)/2\) for every flat span \(U\). Lemma
lem:projective-deletion-degree-criterion and (15) now prove (13).

Finally, the discriminant of \(t^3+7t^2+13t+1\) is

\[
 7^2\,13^2-4\,13^3-4\,7^3-27+18\cdot7\cdot13=-268.              \tag{17}
\]

A real cubic with negative discriminant has one real root and a nonreal
conjugate pair. Thus \(P_M\) does not have all of its zeros on the negative
real axis.

# target

## statement

For each matroid \(M\), define its Kazhdan--Lusztig polynomial \(P_M(t)\in\mathbb Z[t]\) as the unique family satisfying: \(P_M(t)=1\) when \(\operatorname{rk}M=0\); \(\deg P_M<\operatorname{rk}(M)/2\) when \(\operatorname{rk}M>0\); and \(t^{\operatorname{rk}M}P_M(t^{-1})=\sum_{F\in L(M)}\chi_{M|F}(t)P_{M/F}(t)\), where \(L(M)\) is the lattice of flats, \(M|F\) and \(M/F\) are restriction and contraction, and \(\chi\) is the characteristic polynomial. Prove or disprove that all zeros of \(P_M(t)\) lie on the negative real axis.

## proof

The assertion is false. The explicit rank-\(7\) binary matroid in Theorem
thm:explicit-counterexample has

\[
 P_M(t)=1+13t+7t^2+t^3
\]

with discriminant \(-268\), so it has two nonreal zeros.
