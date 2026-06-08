# lemma lem:landesman-litt-trace-vanishing-cover

## statement
There exists a smooth proper connected complex curve \(X\) of genus \(2\), a finite etale connected cover
\[
\pi:Y\to X,
\]
and a nonzero section
\[
\lambda\in H^0(Y,\pi^*K_X)=H^0(Y,K_Y)
\]
such that the trace-product map
\[
H^0(Y,K_Y)\longrightarrow H^0(X,K_X^2),\qquad
\alpha\longmapsto \operatorname{Tr}_{Y/X}(\lambda\alpha)
\]
is the zero map.

## proof
We use the following result of Landesman and Litt.

External result used in this proof:

- paper_id: `Landesman-Litt-Prills-Problem`
- title: *Prill's Problem*
- arXiv id: `2209.12958v2`
- theorem_id: Theorem 1.2, Proposition 2.3, Proposition 2.4
- complete cited statement: Theorem 1.2 says that if \(X\) is any smooth proper connected curve of genus \(2\) over \(\mathbb C\), then there is a finite etale cover \(\pi:Y\to X\) which is Prill exceptional. Proposition 2.4 constructs such a degree \(36\) etale cover in a versal genus-\(2\) family whose relative Jacobian has an isotrivial isogeny factor. Proposition 2.3 proves, in that setup, that there is a nonzero element
  \[
  \lambda\in H^0(Y,K_Y)=H^0(X,\pi_*K_Y)
  \]
  such that the nonzero \(\mathcal O_X\)-linear map
  \[
  q_\lambda:\pi_*K_Y\longrightarrow K_X^2,\qquad
  \alpha\longmapsto \operatorname{Tr}_{Y/X}(\lambda\alpha),
  \]
  induces the zero map on global sections.

Here "Prill exceptional" means that \(h^0(Y,\mathcal O_Y(\pi^{-1}(x)))\ge 2\) for every \(x\in X\). In Proposition 2.3, this property is obtained from the infinitesimal variation of Hodge structure: an isotrivial isogeny factor of the Jacobian gives a nonzero flat Hodge substructure, hence a nonzero kernel vector \(\lambda\) for the induced infinitesimal period map. Landesman and Litt identify that infinitesimal period map with the trace-product operator \(q_\lambda\).

Because \(\pi\) is etale, \(K_Y\simeq \pi^*K_X\). Thus the section \(\lambda\) supplied by Proposition 2.3 is also a nonzero section of \(\pi^*K_X\), and the induced map on global sections is exactly
\[
\alpha\longmapsto \operatorname{Tr}_{Y/X}(\lambda\alpha).
\]
This proves the lemma.

# lemma lem:pushforward-etale-semistable

## statement
Let \(\pi:Y\to X\) be a finite etale morphism of smooth proper connected curves over an algebraically closed field. Then \(\pi_*\mathcal O_Y\) is a semistable vector bundle of degree \(0\) on \(X\).

## proof
Let \(d=\deg\pi\). Since \(\pi\) is etale,
\[
g(Y)-1=d(g(X)-1),
\]
and hence
\[
\chi(Y,\mathcal O_Y)=d\chi(X,\mathcal O_X).
\]
For a rank \(d\) bundle \(V\) on \(X\),
\[
\chi(X,V)=\deg(V)+d\chi(X,\mathcal O_X).
\]
Applying this to \(V=\pi_*\mathcal O_Y\) and using
\(\chi(X,\pi_*\mathcal O_Y)=\chi(Y,\mathcal O_Y)\), we get
\[
\deg(\pi_*\mathcal O_Y)=0.
\]

It remains to show semistability. Let \(r:Z\to X\) be a finite etale Galois cover dominating \(\pi\). Then
\[
r^*\pi_*\mathcal O_Y\simeq \mathcal O_Z^{\oplus d},
\]
because \(Y\times_X Z\) is a disjoint union of \(d\) copies of \(Z\). If \(F\subset \pi_*\mathcal O_Y\) were a subbundle of positive degree, then \(r^*F\subset \mathcal O_Z^{\oplus d}\) would also have positive degree. But the trivial bundle \(\mathcal O_Z^{\oplus d}\) is semistable of degree \(0\), so it has no positive-degree subbundle. Therefore every subbundle of \(\pi_*\mathcal O_Y\) has degree at most \(0\), and \(\pi_*\mathcal O_Y\) is semistable of degree \(0\).

# lemma lem:trace-vanishing-gives-quasi-independent-higgs

## statement
Let \(X\) be a smooth proper connected curve over an algebraically closed field of characteristic \(0\), let \(K_X=\Omega^1_X\), let \(\pi:Y\to X\) be a finite etale connected cover, and let
\[
0\neq\lambda\in H^0(Y,\pi^*K_X).
\]
Assume that
\[
H^0(Y,K_Y)\longrightarrow H^0(X,K_X^2),\qquad
\alpha\longmapsto \operatorname{Tr}_{Y/X}(\lambda\alpha)
\]
is the zero map. Put
\[
\mathcal H=\pi_*\mathcal O_Y
\]
and let \(\theta:\mathcal H\to\mathcal H\otimes K_X\) be multiplication by \(\lambda\). Then \((\mathcal H,\theta)\) is a quasi-independent semistable Higgs bundle, and \(\theta\) is not nilpotent.

## proof
The Higgs field is well-defined because
\[
\pi_*\pi^*K_X\simeq \pi_*\mathcal O_Y\otimes K_X.
\]
On a curve, the integrability condition \(\theta\wedge\theta=0\) is automatic.

Let
\[
\mathcal E=\{f\in \underline{\operatorname{End}}_{\mathcal O_X}(\mathcal H):f\theta=\theta f\}
\]
be the endomorphism sheaf of the Higgs bundle. The algebra \(\pi_*\mathcal O_Y\) acts on itself by multiplication, so there is an injective morphism of sheaves
\[
i:\pi_*\mathcal O_Y\hookrightarrow \mathcal E,
\]
because multiplication operators commute with multiplication by \(\lambda\).

The Higgs field induces a map
\[
\varphi_\theta:K_X^{-1}=T_X\longrightarrow \mathcal E.
\]
Under the inclusion \(i\), this map factors as
\[
K_X^{-1}\xrightarrow{u_\lambda}\pi_*\mathcal O_Y\xrightarrow{i}\mathcal E,
\]
where \(u_\lambda\) is the morphism obtained by contracting the section
\(\lambda\in H^0(Y,\pi^*K_X)\) with vector fields on \(X\).

We claim that \(H^1(u_\lambda)=0\). By Serre duality and finite duality, the dual of
\[
H^1(X,K_X^{-1})\xrightarrow{H^1(u_\lambda)}H^1(X,\pi_*\mathcal O_Y)
=H^1(Y,\mathcal O_Y)
\]
is
\[
H^0(Y,K_Y)=H^0(X,\pi_*K_Y)\longrightarrow H^0(X,K_X^2),
\qquad
\alpha\longmapsto \operatorname{Tr}_{Y/X}(\lambda\alpha).
\]
This dual map is zero by hypothesis, hence \(H^1(u_\lambda)=0\). Therefore
\[
H^1(\varphi_\theta)=H^1(i)\circ H^1(u_\lambda)=0,
\]
so \((\mathcal H,\theta)\) is quasi-independent.

By Lemma \(\mathrm{lem:pushforward-etale-semistable}\), the underlying vector bundle \(\mathcal H=\pi_*\mathcal O_Y\) is semistable of degree \(0\). Hence every \(\theta\)-invariant subbundle has slope at most \(0=\mu(\mathcal H)\), so the Higgs bundle is semistable.

Finally, \(\theta\) is not nilpotent. Since \(\lambda\neq0\), on a nonempty open subset of \(X\) we may choose a local generator \(\omega\) of \(K_X\) and write
\[
\lambda=a\,\pi^*\omega
\]
with \(0\neq a\in \mathcal O_Y(\pi^{-1}U)\). Let \(\partial\) be the dual local vector field on \(U\). Then \(\theta(\partial)\) is multiplication by \(a\) on \(\pi_*\mathcal O_Y|_U\). At the generic point of \(Y\), \(a\) is a nonzero element of the function field \(C(Y)\), so multiplication by \(a\) is not nilpotent. Thus \(\theta(\partial)\) is not nilpotent on \(U\), and the Higgs field is not nilpotent.

# theorem

## statement
Definition: Let C be an algebraically closed field of characteristic 0, and let \(X / C\) be a proper smooth variety over C. Let (H, θ) be a Higgs bundle over X, and let E denote the endomorphism sheaf of (H, θ). That is,  
\[
\mathcal {E} = \{f \in \underline {{E n d}} _ {\mathcal {O} _ {X}} (\mathcal {H}): f \mathrm{commuteswith} \theta \}.
\]
Then, \(( { \mathcal { H } } , \theta )\) is called quasi-independent if the homomorphism \(H ^ { 1 } ( X , T _ { X / C } ) \to H ^ { 1 } ( X , { \mathcal { E } } )\) induced by θ vanishes. 

Let X be a proper smooth curve over C of genus \(g \geq 2 .\) . Is every quasi-independent semi-stable Higgs bundle (H, θ) nilpotent (i.e., for any open subset \(U \subseteq X\) and \(\partial \in T _ { X / C } ( U )\) , θ(∂) is nilpotent)?

## proof
No.

Take \(C=\mathbb C\) and let \(X\) be any smooth proper connected complex curve of genus \(2\). By Lemma \(\mathrm{lem:landesman-litt-trace-vanishing-cover}\), there is a finite etale connected cover
\[
\pi:Y\to X
\]
and a nonzero section
\[
\lambda\in H^0(Y,\pi^*K_X)
\]
such that
\[
H^0(Y,K_Y)\longrightarrow H^0(X,K_X^2),\qquad
\alpha\longmapsto \operatorname{Tr}_{Y/X}(\lambda\alpha)
\]
is the zero map.

Now put
\[
\mathcal H=\pi_*\mathcal O_Y
\]
and let \(\theta\) be multiplication by \(\lambda\). Lemma \(\mathrm{lem:trace-vanishing-gives-quasi-independent-higgs}\) shows that \((\mathcal H,\theta)\) is a quasi-independent semistable Higgs bundle and that \(\theta\) is not nilpotent.

Thus there exists a quasi-independent semistable Higgs bundle on a smooth proper curve of genus \(2\) over an algebraically closed field of characteristic \(0\) which is not nilpotent. Therefore the proposed assertion is false.
