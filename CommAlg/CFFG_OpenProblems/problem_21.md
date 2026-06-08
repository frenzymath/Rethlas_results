# definition def:counterexample-domain

## statement
Let
\[
k=\mathbf F_2,\qquad A=k[t],\qquad S=A\setminus\bigl((t)\cup(t+1)\bigr),
\]
and set
\[
T=S^{-1}A,\qquad N_0=tT,\qquad N_1=(t+1)T,\qquad m=t(t+1),\qquad M=mT=N_0N_1.
\]
Define
\[
D:=k+M=\{a+u:\ a\in \mathbf F_2,\ u\in M\}\subset T.
\]
Let
\[
\theta_2:\operatorname{Int}(D)\otimes_D \operatorname{Int}(D)\longrightarrow \operatorname{Int}(D^2)
\]
be the canonical \(D\)-algebra homomorphism. Under the usual identification of
\(\operatorname{Int}(D^2)\) with a subring of \(\operatorname{Frac}(D)[X,Y]\), the image of
\(\theta_2\) is the set of finite sums \(\sum_i f_i(X)h_i(Y)\) with
\(f_i,h_i\in \operatorname{Int}(D)\).

## proof
This is only notation.

# lemma lem:basic-structure

## statement
For the domain \(D\) of Definition `def:counterexample-domain`, the following hold.

1. \(T\) is a semilocal PID with maximal ideals \(N_0\) and \(N_1\).
2. \(M=N_0\cap N_1=N_0N_1=mT\).
3. \(D\) is a local integral domain with maximal ideal \(M\).
4. \(N_0\cap D=N_1\cap D=M\).
5. If \(v_0\) and \(v_1\) denote the discrete valuations of the DVRs \(T_{N_0}\) and
   \(T_{N_1}\), normalized by \(v_0(t)=1\) and \(v_1(t+1)=1\), then for every \(n\ge 1\)
   the element
   \[
   u_n:=t(t+1)^{n+1}=m(t+1)^n
   \]
   lies in \(M\setminus M^2\).

## proof
Since \(A=\mathbf F_2[t]\) is a PID and \(T=S^{-1}A\) is obtained by inverting all
elements outside \((t)\cup(t+1)\), the maximal ideals of \(T\) are exactly
\[
N_0=tT,\qquad N_1=(t+1)T,
\]
and \(T\) is semilocal and principal. This proves (1).

The ideals \(N_0\) and \(N_1\) are comaximal, so
\[
N_0\cap N_1=N_0N_1=t(t+1)T=mT=M.
\]
Thus (2) holds.

Because \(D\subset T\) and \(T\) is a domain, \(D\) is a domain. Also,
\[
D/M\cong \mathbf F_2,
\]
so \(M\) is maximal in \(D\). If \(x=a+u\in D\setminus M\), then \(a=1\) and
\(x=1+u\) with \(u\in M\subset N_0\cap N_1\), hence \(1+u\) is a unit in the semilocal
ring \(T\). Its inverse lies in \(1+M\subset D\). Therefore \(D\) is local with maximal
ideal \(M\). This proves (3).

Now let \(x=a+u\in D\) with \(a\in \mathbf F_2\) and \(u\in M\). Modulo \(N_0\), the
class of \(x\) is \(a\), because \(u\in M\subset N_0\); hence \(x\in N_0\) iff \(a=0\), i.e.
iff \(x\in M\). Thus \(N_0\cap D=M\). The same argument gives \(N_1\cap D=M\), so
(4) holds.

Finally, for \(u_n=t(t+1)^{n+1}\) we have
\[
v_0(u_n)=1+0=1,
\]
because \(t+1\) is a unit in \(T_{N_0}\). Since every element of
\[
M^2=(mT)^2=m^2T
\]
has \(v_0\)-value at least \(2\), it follows that \(u_n\in M\setminus M^2\). This proves
(5).

# lemma lem:difference-criterion

## statement
Let \(H\subset \operatorname{Int}(D)\) be a finite set. Then there exists an integer
\(n\ge 1\) such that, with
\[
u_n=t(t+1)^{n+1}=m(t+1)^n\in M\setminus M^2,
\]
one has
\[
h(u_n)-h(0)\in M
\]
for every \(h\in H\).

## proof
Fix \(h\in H\), and write
\[
h(X)=\sum_{r=0}^{d_h} c_{h,r}X^r
\]
with \(c_{h,r}\in \operatorname{Frac}(D)=\operatorname{Frac}(T)\). Since \(H\) is finite, we may
choose an integer \(n\ge 1\) such that
\[
v_1(c_{h,r})\ge -(n-1)
\]
for every \(h\in H\) and every \(r\ge 1\). Let
\[
u_n=t(t+1)^{n+1}=m(t+1)^n.
\]
By Lemma `lem:basic-structure`, \(u_n\in M\setminus M^2\).

For every \(r\ge 1\),
\[
v_1(c_{h,r}u_n^r)\ge -(n-1)+r(n+1)\ge 2.
\]
Therefore
\[
h(u_n)-h(0)=\sum_{r\ge 1} c_{h,r}u_n^r\in N_1.
\]
But \(h(u_n),h(0)\in D\), because \(h\in \operatorname{Int}(D)\) and \(u_n,0\in D\). Hence
\[
h(u_n)-h(0)\in N_1\cap D=M
\]
by Lemma `lem:basic-structure`. This holds for every \(h\in H\).

# lemma lem:construct-g

## statement
Define
\[
q(X):=\frac{X^2+X}{m}\in \operatorname{Frac}(D)[X],
\qquad
g(X):=q(X)^2+q(X)\in \operatorname{Frac}(D)[X].
\]
Then:

1. \(g\in \operatorname{Int}(D)\), in fact \(g(D)\subset M\).
2. For every \(n\ge 1\), if \(u_n=t(t+1)^{n+1}=m(t+1)^n\), then
   \[
   g(u_n^2)\notin M^2.
   \]

## proof
Let \(x\in D\). Since \(D=\mathbf F_2+M\), the residue class of \(x\) modulo \(M\) lies in
\(\mathbf F_2\). Hence \(x^2+x\in M=mT\), so \(q(x)\in T\).

Now let \(y\in T\). Modulo \(N_0\) and \(N_1\), the image of \(y\) lies in the residue
field \(\mathbf F_2\), so
\[
y^2+y\equiv 0 \pmod{N_0},
\qquad
y^2+y\equiv 0 \pmod{N_1}.
\]
Therefore
\[
y^2+y\in N_0\cap N_1=M.
\]
Applying this to \(y=q(x)\in T\), we get
\[
g(x)=q(x)^2+q(x)\in M\subset D.
\]
Thus \(g(D)\subset M\), so \(g\in \operatorname{Int}(D)\). This proves (1).

For (2), write \(u_n=mw\) with \(w=(t+1)^n\). Then
\[
u_n^2=m^2w^2
\]
and
\[
q(u_n^2)
=\frac{u_n^4+u_n^2}{m}
=\frac{m^4w^4+m^2w^2}{m}
=mw^2+m^3w^4.
\]
Hence \(q(u_n^2)\in M\). Moreover, since \(w\) is a unit in \(T_{N_0}\),
\[
v_0\!\bigl(q(u_n^2)\bigr)=1,
\]
because the first summand has \(v_0\)-value \(1\) and the second has \(v_0\)-value at
least \(3\). Thus
\[
q(u_n^2)\in M\setminus M^2.
\]
Since \(q(u_n^2)^2\in M^2\), we have
\[
g(u_n^2)=q(u_n^2)^2+q(u_n^2)\equiv q(u_n^2)\pmod{M^2}.
\]
Therefore \(g(u_n^2)\notin M^2\).

# proposition prop:gxy-not-in-image

## statement
Let
\[
P(X,Y):=g(XY)\in \operatorname{Int}(D^2).
\]
Then \(P(X,Y)\notin \operatorname{im}(\theta_2)\).

## proof
Since \(g\in \operatorname{Int}(D)\) by Lemma `lem:construct-g`, and \(XY\) maps \(D^2\)
into \(D\), the polynomial \(P(X,Y)=g(XY)\) lies in \(\operatorname{Int}(D^2)\).

Assume for contradiction that \(P\in \operatorname{im}(\theta_2)\). Then
\[
P(X,Y)=\sum_{i=1}^r f_i(X)h_i(Y)
\]
for some \(f_i,h_i\in \operatorname{Int}(D)\).

Apply Lemma `lem:difference-criterion` to the finite set
\[
H=\{f_1,\dots,f_r,h_1,\dots,h_r\}.
\]
Choose \(n\ge 1\) as in that lemma, and set
\[
u:=u_n=t(t+1)^{n+1}.
\]
Then
\[
f_i(u)-f_i(0)\in M,\qquad h_i(u)-h_i(0)\in M
\]
for all \(i\). Then
\[
\begin{aligned}
&P(u,u)-P(u,0)-P(0,u)+P(0,0)\\
&=\sum_{i=1}^r\bigl(f_i(u)-f_i(0)\bigr)\bigl(h_i(u)-h_i(0)\bigr)\in M^2.
\end{aligned}
\]

On the other hand, \(g(0)=0\), so
\[
P(u,0)=g(0)=0,\qquad P(0,u)=g(0)=0,\qquad P(0,0)=g(0)=0.
\]
Hence
\[
P(u,u)-P(u,0)-P(0,u)+P(0,0)=g(u^2).
\]
By Lemma `lem:construct-g`, \(g(u^2)\notin M^2\). This contradiction shows that
\[
P(X,Y)\notin \operatorname{im}(\theta_2).
\]

# theorem thm:main

## statement
Let $D$ be an integral domain. This is the case if the canonical $D$-algebra homomorphism $\operatorname{Int}(D)^{\otimes_D n} \to \operatorname{Int}(D^n)$ is an isomorphism for all $n$ [36].

[36] J. Elliott, Birings and plethories of integer-valued polynomials, Third International Meeting on Integer-Valued Polynomials (2010), Actes des Rencontres du CIRM 2 (2) (2010), 53-58.

Does $\operatorname{Int}(D)$ always have a unique structure of a $D$-$D$-biring such that the inclusion $D[X] \to \operatorname{Int}(D)$ is a homomorphism of $D$-$D$-birings?

## proof
The answer is **no**.

Take the explicit domain \(D=\mathbf F_2+M\subset T\) from Definition
`def:counterexample-domain`, where
\[
T=\mathbf F_2[t]_{\mathbf F_2[t]\setminus((t)\cup(t+1))},
\qquad
M=t(t+1)T.
\]

We first show that \(D\) is not weakly polynomially composite. By Proposition
`prop:gxy-not-in-image`, the image of
\[
\theta_2:\operatorname{Int}(D)\otimes_D \operatorname{Int}(D)\to \operatorname{Int}(D^2)
\]
does **not** contain \(g(XY)\), where \(g\in \operatorname{Int}(D)\) is the polynomial
constructed in Lemma `lem:construct-g`.

But \(XY\in \operatorname{im}(\theta_2)\), because it is the image of \(X\otimes X\). If
\(\operatorname{im}(\theta_2)\) were weakly polynomially complete over \(D\), then, since
\(g\in \operatorname{Int}(D)\) and \(XY\in \operatorname{im}(\theta_2)\), we would have
\(g(XY)\in \operatorname{im}(\theta_2)\), contrary to Proposition `prop:gxy-not-in-image`.
Thus \(\operatorname{im}(\theta_2)\) is not WPC. By the terminology introduced in
Elliott's paper, a domain is weakly polynomially composite precisely when these
images \(\operatorname{im}(\theta_X)\) are WPC for all sets \(X\). Therefore \(D\) is not
weakly polynomially composite.

Now invoke the following external result:

**Cited external theorem.**
Paper id: `arXiv:1109.3848`.
Theorem id: `Theorem 12(1)`.
arXiv id: `1109.3848`.
Complete statement:

> Let \(D\) be an integral domain. If the domain \(\operatorname{Int}(D)\) has a
> \(D\)-\(D\)-biring structure such that the inclusion
> \(D[X]\to \operatorname{Int}(D)\) is a homomorphism of \(D\)-\(D\)-birings, then
> \(D\) is weakly polynomially composite.

Since our explicit domain \(D\) is **not** weakly polynomially composite, the cited
theorem implies that \(\operatorname{Int}(D)\) cannot have a \(D\)-\(D\)-biring structure
for which \(D[X]\to \operatorname{Int}(D)\) is a homomorphism of \(D\)-\(D\)-birings.

Therefore \(\operatorname{Int}(D)\) does **not** always admit such a structure.
