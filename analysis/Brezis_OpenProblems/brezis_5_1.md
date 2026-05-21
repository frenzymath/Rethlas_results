# lemma lem:hhalf-degree

## statement
There is a universal constant \(C_0\) such that every
\(g\in H^{1/2}(\mathbb S^1;\mathbb S^1)\) satisfies
\[
 |\deg g|\le C_0
 \int_{\mathbb S^1}\int_{\mathbb S^1}
 \frac{|g(x)-g(y)|^2}{|x-y|^2}\,dx\,dy .
\]
Moreover, for every \(S^1\)-valued VMO map \(f\) and every integer \(k\ge1\),
\[
\deg(f^k)=k\,\deg f .
\]

## proof
We recall the standard \(p=2\) degree estimate for circle-valued maps. In
Bourgain--Brezis--Mironescu, "Lifting, Degree, and Distributional Jacobian
Revisited" (paper_id: `BBM_CPAM_2005_lifting_degree_distributional_jacobian`,
theorem_id: Corollary 0.5 and formula (0.7), arXiv id: not applicable), the
following complete statement is recorded: for \(1<p<\infty\) and
\(g\in W^{1/p,p}(\mathbb S^1;\mathbb S^1)\),
\[
|\deg g|\le C_p |g|_{W^{1/p,p}}^p.
\]
In the special case \(p=2\), formula (0.7) states
\[
\deg g=\frac{1}{2i\pi}\langle \overline g,\dot g\rangle_{H^{1/2},H^{-1/2}},
\]
and therefore
\[
|\deg g|\le C_0 |g|_{H^{1/2}}^2.
\]
With the chordal kernel on \(\mathbb S^1\), the \(H^{1/2}\) seminorm is
equivalent to
\[
\int_{\mathbb S^1}\int_{\mathbb S^1}
\frac{|g(x)-g(y)|^2}{|x-y|^2}\,dx\,dy,
\]
which gives the asserted estimate.

The same degree theory is the VMO degree; it is compatible with composition by
the degree \(k\) map \(z\mapsto z^k\) on \(\mathbb S^1\). Hence
\(\deg(f^k)=k\deg f\). This follows first for smooth maps from the ordinary
winding number and then passes to VMO maps by the continuity of the VMO degree.

# lemma lem:weighted-powers

## statement
There is a universal constant \(C_1\) such that for every \(1<p\le 3/2\) one can
choose positive weights
\[
a_k=\frac{k^{-p-1}}{\sum_{j=1}^\infty j^{-p}},\qquad k\ge1,
\]
for which
\[
\sum_{k=1}^\infty a_k k=1
\]
and, for every \(z,w\in\mathbb S^1\),
\[
\sum_{k=1}^\infty a_k |z^k-w^k|^2
\le C_1 (p-1)|z-w|^p .
\]

## proof
The normalization gives
\[
\sum_{k=1}^\infty a_k k
=\frac{\sum_{k=1}^\infty k^{-p}}{\sum_{j=1}^\infty j^{-p}}
=1.
\]
Also
\[
\sum_{j=1}^\infty j^{-p}\ge \int_1^\infty t^{-p}\,dt=\frac1{p-1},
\]
so the reciprocal of the denominator is at most \(p-1\).

Put \(\rho=|z-w|\). Since \(|z|=|w|=1\),
\[
|z^k-w^k|\le k|z-w|=k\rho
\quad\text{and}\quad
|z^k-w^k|\le 2.
\]
Thus
\[
\sum_{k=1}^\infty k^{-p-1}|z^k-w^k|^2
\le
\sum_{k=1}^\infty k^{-p-1}\min\{k^2\rho^2,4\}.
\]
If \(\rho\ge1\), the right hand side is bounded by a universal constant, hence
by \(C\rho^p\). If \(0<\rho<1\), split the sum at \(K=\lfloor \rho^{-1}\rfloor\).
Then, since \(1<p\le3/2\),
\[
\rho^2\sum_{k\le K} k^{1-p}
\le C\rho^2 K^{2-p}
\le C\rho^p
\]
and
\[
\sum_{k>K} k^{-p-1}\le C K^{-p}\le C\rho^p.
\]
The case \(\rho=0\) is trivial. Multiplying by the reciprocal of
\(\sum_{j=1}^\infty j^{-p}\), which is at most \(p-1\), proves the claim.

# lemma lem:large-p

## statement
There is a universal constant \(C_2\) such that for every \(3/2\le p\le2\) and
every \(f\in W^{1/p,p}(\mathbb S^1;\mathbb S^1)\),
\[
|\deg f|\le C_2(p-1)
\int_{\mathbb S^1}\int_{\mathbb S^1}
\frac{|f(x)-f(y)|^p}{|x-y|^2}\,dx\,dy .
\]

## proof
For \(z,w\in\mathbb S^1\) and \(p\le2\),
\[
|z-w|^2\le 2^{2-p}|z-w|^p.
\]
Therefore \(f\in H^{1/2}(\mathbb S^1;\mathbb S^1)\) and
\[
\int_{\mathbb S^1}\int_{\mathbb S^1}
\frac{|f(x)-f(y)|^2}{|x-y|^2}\,dx\,dy
\le
2^{2-p}
\int_{\mathbb S^1}\int_{\mathbb S^1}
\frac{|f(x)-f(y)|^p}{|x-y|^2}\,dx\,dy .
\]
Applying Lemma \(\mathrm{lem:hhalf-degree}\) and using \(p-1\ge1/2\) gives the
assertion after increasing the universal constant.

# lemma lem:small-p

## statement
There is a universal constant \(C_3\) such that for every \(1<p\le3/2\) and
every \(f\in W^{1/p,p}(\mathbb S^1;\mathbb S^1)\),
\[
|\deg f|\le C_3(p-1)
\int_{\mathbb S^1}\int_{\mathbb S^1}
\frac{|f(x)-f(y)|^p}{|x-y|^2}\,dx\,dy .
\]

## proof
Let \(a_k\) be the weights from Lemma \(\mathrm{lem:weighted-powers}\). For each
\(k\ge1\), Lemma \(\mathrm{lem:weighted-powers}\) and the finiteness of the
\(W^{1/p,p}\) seminorm imply, after integration, that \(f^k\in H^{1/2}\). Hence
Lemma \(\mathrm{lem:hhalf-degree}\) applies to \(f^k\), and
\[
k|\deg f|=|\deg(f^k)|
\le C_0
\int_{\mathbb S^1}\int_{\mathbb S^1}
\frac{|f(x)^k-f(y)^k|^2}{|x-y|^2}\,dx\,dy .
\]
Multiplying by \(a_k\), summing in \(k\), and using
\(\sum_k a_k k=1\), Tonelli's theorem, and Lemma
\(\mathrm{lem:weighted-powers}\), we get
\[
\begin{aligned}
|\deg f|
&\le C_0
\int_{\mathbb S^1}\int_{\mathbb S^1}
\frac{\sum_{k=1}^\infty a_k |f(x)^k-f(y)^k|^2}{|x-y|^2}\,dx\,dy\\
&\le C_0C_1(p-1)
\int_{\mathbb S^1}\int_{\mathbb S^1}
\frac{|f(x)-f(y)|^p}{|x-y|^2}\,dx\,dy .
\end{aligned}
\]
This is the desired estimate.

# theorem

## statement
For maps \(f:\mathbb{S}^1\to\mathbb{S}^1\) in \(W^{1/p,p}(\mathbb{S}^1;\mathbb{S}^1)\), where \(1<p\le2\) and \([f]_{W^{1/p,p}}^p=\int_{\mathbb{S}^1}\int_{\mathbb{S}^1}\frac{|f(x)-f(y)|^p}{|x-y|^2}\,dx\,dy\), does there exist a universal constant \(c\) such that \(|\deg f|\le c(p-1)[f]_{W^{1/p,p}}^p\) for every such \(p\) and every such \(f\)?

## proof
Yes. If \(3/2\le p\le2\), the estimate follows from Lemma
\(\mathrm{lem:large-p}\). If \(1<p\le3/2\), it follows from Lemma
\(\mathrm{lem:small-p}\). Taking
\[
c=\max\{C_2,C_3\}
\]
gives a universal constant valid for every \(1<p\le2\) and every
\(f\in W^{1/p,p}(\mathbb S^1;\mathbb S^1)\).
