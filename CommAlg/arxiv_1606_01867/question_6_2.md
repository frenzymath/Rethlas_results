# lemma lem:primitive-point-01456

## statement
For the degree sequence
\[
d=(0,1,4,5,6),
\]
the primitive integral point on the corresponding pure Boij--Soderberg ray has nonzero Betti numbers
\[
\beta_{0,0}=1,\qquad \beta_{1,1}=2,\qquad \beta_{2,4}=5,\qquad \beta_{3,5}=6,\qquad \beta_{4,6}=2.
\]

## proof
Let
\[
\beta=(\beta_0,\beta_1,\beta_2,\beta_3,\beta_4)
\]
be the coefficients of a pure table on this ray, so the only nonzero entries are
\[
\beta_{0,0}=\beta_0,\ \beta_{1,1}=\beta_1,\ \beta_{2,4}=\beta_2,\ \beta_{3,5}=\beta_3,\ \beta_{4,6}=\beta_4.
\]
For a codimension-$4$ pure resolution, the Herzog--Kuhl equations are
\[
\sum_{i=0}^4 (-1)^i \beta_i d_i^m=0 \qquad (m=0,1,2,3).
\]
After normalizing by $\beta_0=1$, these become
\[
1-\beta_1+\beta_2-\beta_3+\beta_4=0,
\]
\[
-\beta_1+4\beta_2-5\beta_3+6\beta_4=0,
\]
\[
-\beta_1+16\beta_2-25\beta_3+36\beta_4=0,
\]
\[
-\beta_1+64\beta_2-125\beta_3+216\beta_4=0.
\]
Subtracting the second equation from the third and the third from the fourth gives
\[
6\beta_2-10\beta_3+15\beta_4=0,
\qquad
12\beta_2-25\beta_3+45\beta_4=0.
\]
Subtracting twice the first of these from the second yields
\[
-5\beta_3+15\beta_4=0,
\]
so $\beta_3=3\beta_4$. Plugging back in gives
\[
6\beta_2-30\beta_4+15\beta_4=0,
\]
hence $2\beta_2=5\beta_4$. Using the second Herzog--Kuhl equation then gives
\[
\beta_1=4\beta_2-5\beta_3+6\beta_4=\beta_4.
\]
Finally, the first equation becomes
\[
1-\beta_4+\frac52\beta_4-3\beta_4+\beta_4=0,
\]
so $\beta_4=2$. Therefore
\[
(\beta_0,\beta_1,\beta_2,\beta_3,\beta_4)=(1,2,5,6,2).
\]
This vector is already integral, so it is the primitive integral point on the ray.


# lemma lem:pbw-hilbert-series

## statement
Let
\[
\mathfrak g=\bigoplus_{i\ge 1}\mathfrak g_i
\]
be a finite-dimensional positively graded Lie algebra, and write
\[
h_i=\dim_k \mathfrak g_i.
\]
Then the graded Hilbert series of the universal enveloping algebra is
\[
H_{U(\mathfrak g)}(t)=\prod_{i\ge 1}(1-t^i)^{-h_i}.
\]
Consequently, if a finite-length graded $U(\mathfrak g)$-module $M$ has a pure resolution with nonzero Betti numbers $\beta_i$ in degrees $d_i$, then
\[
p_M(t):=\sum_i (-1)^i \beta_i t^{d_i}
\]
is divisible by
\[
\prod_{i\ge 1}(1-t^i)^{h_i}.
\]

## proof
Choose a homogeneous basis of $\mathfrak g$ consisting of $h_i$ basis vectors in degree $i$.
By the Poincare--Birkhoff--Witt theorem, the ordered monomials in these basis vectors form a graded $k$-basis of $U(\mathfrak g)$. Therefore each degree-$i$ basis vector contributes a factor $(1-t^i)^{-1}$ to the Hilbert series, and multiplying over all basis vectors gives
\[
H_{U(\mathfrak g)}(t)=\prod_{i\ge 1}(1-t^i)^{-h_i}.
\]

Now let
\[
0\leftarrow M\leftarrow \bigoplus_i U(\mathfrak g)(-d_i)^{\beta_i}\leftarrow \cdots
\]
be a graded free resolution of $M$. Taking alternating sums of Hilbert series gives
\[
H_M(t)=p_M(t)\,H_{U(\mathfrak g)}(t).
\]
Since $M$ has finite length, $H_M(t)$ is a polynomial. Thus the denominator
\[
\prod_{i\ge 1}(1-t^i)^{h_i}
\]
must divide $p_M(t)$.


# theorem thm:bs-6-2

## statement
Let $k$ be a field. A standard graded polynomial ring in $n$ variables is $U(k^n)$ where $k^n$ is the abelian Lie algebra of dimension $n$ concentrated in degree 1. Non-realizable integral points in the Boij--S\"oderberg cone over the polynomial ring may be realizable over $U(\mathfrak{g})$ for a $\mathbb{Z}_{>0}$-graded Lie algebra $\mathfrak{g}$. Note that a finite-dimensional $\mathbb{Z}_{>0}$-graded Lie algebra is necessarily nilpotent.

[Source: D. Erman and S. V. Sam, Questions about Boij--S\"oderberg theory, arXiv:1606.01867, 2016.]

For every degree sequence $(d_0, \ldots, d_n)$, and every integral point on the corresponding ray in the Boij--S\"oderberg cone, does there exist an $n$-dimensional $\mathbb{Z}_{>0}$-graded Lie algebra $\mathfrak{g}$ generated in degree 1, and a finite length module over $U(\mathfrak{g})$ whose Betti table is that integral point?

## proof
The answer is **no**.

We give a counterexample with
\[
n=4,\qquad d=(0,1,4,5,6).
\]
By Lemma `lem:primitive-point-01456`, the primitive integral point on this pure ray is
\[
\beta=(1,2,5,6,2).
\]
So the alternating Betti polynomial is
\[
p(t)=1-2t+5t^4-6t^5+2t^6.
\]
A direct factorization gives
\[
p(t)=(1-t)^4(2t^2+2t+1).
\]

Assume, for contradiction, that there exists a $4$-dimensional positively graded Lie algebra
\[
\mathfrak g=\bigoplus_{i\ge 1}\mathfrak g_i
\]
generated in degree $1$, together with a finite-length graded $U(\mathfrak g)$-module $M$ having this Betti table. Write
\[
h_i=\dim_k \mathfrak g_i.
\]
By Lemma `lem:pbw-hilbert-series`, the polynomial $p(t)$ must be divisible by
\[
\prod_{i\ge 1}(1-t^i)^{h_i}.
\]
Since $\sum_{i\ge 1} h_i=\dim \mathfrak g=4$, we may divide by $(1-t)^4$ and conclude that
\[
q(t):=2t^2+2t+1
\]
must be divisible by
\[
\prod_{i\ge 2}(1+t+\cdots+t^{i-1})^{h_i}.
\]

We now show that this is impossible unless every $h_i$ with $i\ge 2$ is zero.

First, $q(-1)=1$, so $1+t$ does not divide $q(t)$.

Second, modulo $1+t+t^2$ we have $t^2+t=-1$, so
\[
q(t)=2t^2+2t+1=2(t^2+t)+1=2(-1)+1=-1.
\]
Hence the remainder of $q(t)$ upon division by $1+t+t^2$ is the nonzero constant $-1$, so $1+t+t^2$ does not divide $q(t)$ over any field.

Finally, $\deg q=2$, so no polynomial $1+t+\cdots+t^{i-1}$ with $i\ge 4$ can divide $q(t)$.

Therefore $h_i=0$ for all $i\ge 2$. Hence $\mathfrak g$ is concentrated in degree $1$, so
\[
[\mathfrak g,\mathfrak g]\subseteq \mathfrak g_2=0,
\]
and $\mathfrak g$ is abelian. Consequently,
\[
U(\mathfrak g)\cong k[x_1,x_2,x_3,x_4].
\]

So $M$ would be a finite-length graded module over the polynomial ring
\[
S:=k[x_1,x_2,x_3,x_4]
\]
with Betti table $\beta=(1,2,5,6,2)$.

But $\beta_0=1$, so $M$ is cyclic:
\[
M\cong S/I
\]
for some homogeneous ideal $I$.
Also $\beta_1=2$, so $I$ is minimally generated by two homogeneous elements.
By Krull's height theorem,
\[
\operatorname{ht}(I)\le 2.
\]
Hence
\[
\dim(S/I)\ge 4-2=2,
\]
so $S/I$ cannot have finite length.
This contradicts the assumption on $M$.

Thus no such pair $(\mathfrak g,M)$ exists for the degree sequence $(0,1,4,5,6)$ and the integral point $(1,2,5,6,2)$ on its pure ray. Therefore the statement in Question 6.2 is false.
