# theorem fixed_sqrt3_threshold_degree_estimate

## statement
There is a universal constant \(C_0\) such that every continuous map
\(g:\mathbb S^1\to\mathbb S^1\) satisfies
\[
|\deg g|
\le
C_0
\int_{\{(x,y)\in\mathbb S^1\times\mathbb S^1:\ |g(x)-g(y)|\ge \sqrt3\}}
\frac{dx\,dy}{|x-y|^2}.
\]

## proof
This is the fixed-threshold degree estimate at the optimal threshold \(\sqrt3\).
The external result used here is:

- paper_id: `Brezis-2023-favorite-open-problems`
- theorem_id: `Theorem 5.2`
- arXiv id: none
- local_pdf_path: `downloads/brezis_favorite_open_problems_2023.pdf`
- local_text_path: `downloads/brezis_favorite_open_problems_2023.txt`
- complete cited statement: there exists a universal constant \(C\) such that, for every \(f\in C(\mathbb S^1;\mathbb S^1)\),
  \[
  |\deg f|
  \le
  C
  \int_{\{(x,y): |f(x)-f(y)|>\sqrt3\}}
  \frac{dx\,dy}{|x-y|^2}.
  \]
  The source states that \(\sqrt3\) is the optimal threshold for this fixed-threshold estimate.

The theorem is stated there with a strict inequality \(>\sqrt3\) in the threshold set. This immediately implies the displayed version with \(\ge\sqrt3\), since the set \(\{|g(x)-g(y)|>\sqrt3\}\) is contained in \(\{|g(x)-g(y)|\ge\sqrt3\}\).

The notation and hypotheses match the present setting: the domain and target are the unit circle with Euclidean chordal distance, \(dx\,dy\) is arclength product measure, and \(\deg g\) is the usual topological degree.

# lemma power_threshold_inclusion

## statement
Let \(0<\delta\le\sqrt3\), and put
\[
\alpha=2\arcsin(\delta/2),\qquad \alpha_0=2\pi/3.
\]
Choose
\[
n=\left\lfloor \frac{\alpha_0}{\alpha}\right\rfloor .
\]
Then \(n\ge1\), \(n\alpha\le\alpha_0\), and
\[
\frac1n\le \frac{2\alpha}{\alpha_0}\le C_1\delta
\]
for a universal constant \(C_1\). Moreover, for any \(a,b\in\mathbb S^1\),
\[
|a^n-b^n|\ge\sqrt3\quad\Longrightarrow\quad |a-b|\ge\delta .
\]

## proof
Since \(0<\delta\le\sqrt3\), the corresponding angular threshold satisfies
\[
0<\alpha=2\arcsin(\delta/2)\le 2\arcsin(\sqrt3/2)=2\pi/3=\alpha_0,
\]
so \(n\ge1\) and \(n\alpha\le\alpha_0\).

If \(\alpha_0/\alpha<2\), then \(n=1\), hence
\[
\frac1n=1<\frac{2\alpha}{\alpha_0}.
\]
If \(\alpha_0/\alpha\ge2\), then
\[
n=\left\lfloor \frac{\alpha_0}{\alpha}\right\rfloor
\ge \frac12\,\frac{\alpha_0}{\alpha},
\]
and again \(1/n\le 2\alpha/\alpha_0\).
Finally,
\[
\alpha=2\arcsin(\delta/2)\le \frac{2\pi}{3\sqrt3}\,\delta
\]
on \(0<\delta\le\sqrt3\), so \(1/n\le C_1\delta\) for a universal \(C_1\).

For the separation implication, let \(\theta\in[0,\pi]\) be the angular distance between
\(a\) and \(b\). Then \(|a-b|=2\sin(\theta/2)\). If \(|a-b|<\delta\), then \(\theta<\alpha\). Hence
\[
n\theta<n\alpha\le\alpha_0<\pi.
\]
The angular distance between \(a^n\) and \(b^n\) is then exactly \(n\theta\), and therefore
\[
|a^n-b^n|=2\sin(n\theta/2)<2\sin(\alpha_0/2)=\sqrt3.
\]
Taking the contrapositive gives the claim.

# lemma power_energy_comparison

## statement
Let \(f:\mathbb S^1\to\mathbb S^1\) be continuous and let \(n\) be as in the previous lemma. Define \(g:\mathbb S^1\to\mathbb S^1\) by
\[
g(x)=f(x)^n.
\]
Then
\[
\deg g=n\deg f
\]
and
\[
\int_{\{|g(x)-g(y)|\ge\sqrt3\}}\frac{dx\,dy}{|x-y|^2}
\le
I_\delta(f).
\]

## proof
The degree identity follows because \(g=P_n\circ f\), where \(P_n:\mathbb S^1\to\mathbb S^1\), \(P_n(z)=z^n\), has degree \(n\). Thus
\[
\deg g=\deg(P_n)\deg f=n\deg f.
\]

By the power-threshold inclusion, the set
\[
\{(x,y): |g(x)-g(y)|\ge\sqrt3\}
\]
is contained in
\[
\{(x,y): |f(x)-f(y)|\ge\delta\}.
\]
The kernels are identical, so integration over the smaller set gives the stated energy comparison.

# theorem

## statement
For a continuous map \(f:\mathbb{S}^1\to\mathbb{S}^1\) and \(0<\delta\le\sqrt3\), define \(I_\delta(f)=\int_{\{(x,y)\in\mathbb{S}^1\times\mathbb{S}^1:\ |f(x)-f(y)|\ge\delta\}}\frac{dx\,dy}{|x-y|^2}\). Does there exist a universal constant \(c\) such that \(|\deg f|\le c\delta I_\delta(f)\) for every continuous \(f:\mathbb{S}^1\to\mathbb{S}^1\) and every \(0<\delta\le\sqrt3\)?

## proof
Yes.

Let \(0<\delta\le\sqrt3\), set \(\alpha=2\arcsin(\delta/2)\), and choose
\[
n=\left\lfloor\frac{2\pi/3}{\alpha}\right\rfloor .
\]
Let \(g=f^n\). By the fixed \(\sqrt3\)-threshold degree estimate and the power-energy comparison,
\[
n|\deg f|
=|\deg g|
\le
C_0
\int_{\{|g(x)-g(y)|\ge\sqrt3\}}\frac{dx\,dy}{|x-y|^2}
\le
C_0 I_\delta(f).
\]
Therefore
\[
|\deg f|\le \frac{C_0}{n}I_\delta(f).
\]
The power-threshold lemma gives \(1/n\le C_1\delta\). Hence
\[
|\deg f|\le C_0C_1\,\delta\, I_\delta(f).
\]
Thus the desired estimate holds with the universal constant \(c=C_0C_1\).
