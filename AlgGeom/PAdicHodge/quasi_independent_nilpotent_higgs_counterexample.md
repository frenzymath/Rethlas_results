# lemma lem:torsion-augmented-extension

## statement
Let \(X\) be a smooth proper curve over an algebraically closed field, let \(K=\Omega^1_X\), and assume \(g(X)=g\geq 2\). Put
\[
L=K^{-1},\qquad D=\deg K=2g-2,\qquad N=h^1(X,L)=3g-3.
\]
There is a locally free sheaf \(V\) and an exact sequence
\[
0\to L\xrightarrow{i}V\xrightarrow{q}\mathcal O_X^{\oplus N}\oplus T\to 0
\tag{1}
\]
where \(T\) is a torsion sheaf of length \(D\), such that the connecting homomorphism
\[
H^0(X,\mathcal O_X^{\oplus N})\to H^1(X,L)
\]
induced by (1) is an isomorphism. In particular, the induced map
\[
H^1(X,L)\to H^1(X,V)
\]
is zero, and \(\deg V=0\).

## proof
Choose an effective divisor \(\Delta\) of degree \(D\), and set \(T=\mathcal O_\Delta\). The elementary modification
\[
0\to L\to L(\Delta)\to T\to 0
\tag{2}
\]
has locally free middle term.

Since
\[
\operatorname{Ext}^1(\mathcal O_X^{\oplus N}\oplus T,L)
\simeq H^1(X,L)^{\oplus N}\oplus \operatorname{Ext}^1(T,L),
\]
we may choose an extension class whose \(\mathcal O_X^{\oplus N}\)-component gives a prescribed isomorphism
\[
H^0(X,\mathcal O_X^{\oplus N})\simeq H^1(X,L)
\]
as connecting homomorphism, and whose torsion component is the class of (2). Let (1) be the corresponding extension.

The middle term \(V\) is locally free. Indeed, locally on the curve the extension by the free quotient \(\mathcal O_X^{\oplus N}\) splits, while the torsion component is locally the standard sequence
\[
0\to R\xrightarrow{t^m}R\to R/(t^m)\to 0
\]
over a discrete valuation ring. Thus the local middle term is free.

The long exact cohomology sequence of (1) contains
\[
H^0(X,\mathcal O_X^{\oplus N}\oplus T)\to H^1(X,L)\to H^1(X,V).
\]
Because the restriction of the first arrow to \(H^0(X,\mathcal O_X^{\oplus N})\) is an isomorphism, it is surjective. Hence \(H^1(X,L)\to H^1(X,V)\) is zero. Finally
\[
\deg V=\deg L+\operatorname{length}(T)=-(2g-2)+(2g-2)=0.
\]

# lemma lem:V-semistable

## statement
For the vector bundle \(V\) constructed in Lemma \(\mathrm{lem:torsion-augmented-extension}\), every nonzero subbundle \(A\subset V\) has \(\deg A\leq 0\). Hence \(V\) is semistable of degree \(0\).

## proof
Let
\[
0\to L\to V\to \mathcal O_X^{\oplus N}\oplus T\to 0
\]
be the exact sequence from Lemma \(\mathrm{lem:torsion-augmented-extension}\), where \(T\) is torsion. Let \(A\subset V\) be a nonzero subbundle.

First suppose \(A\cap L=0\). Then \(A\) injects into \(\mathcal O_X^{\oplus N}\oplus T\). Since \(A\) is torsion-free, its image has zero intersection with the torsion summand \(T\), and therefore \(A\) injects into \(\mathcal O_X^{\oplus N}\). The trivial bundle is semistable of degree \(0\), so \(\deg A\leq 0\).

Now suppose \(A\cap L\neq 0\). Then \(A\cap L\) is a nonzero subsheaf of the line bundle \(L\), so
\[
\deg(A\cap L)\leq \deg L=-(2g-2)<0.
\]
Let \(B\) be the image of \(A/(A\cap L)\) in \(\mathcal O_X^{\oplus N}\oplus T\). Its torsion subsheaf has length at most \(\operatorname{length}(T)=2g-2\), and its torsion-free quotient injects into \(\mathcal O_X^{\oplus N}\). Therefore
\[
\deg B\leq 2g-2.
\]
Thus
\[
\deg A=\deg(A\cap L)+\deg B\leq -(2g-2)+(2g-2)=0.
\]
Since Lemma \(\mathrm{lem:torsion-augmented-extension}\) gives \(\deg V=0\), this proves that \(V\) is semistable.

# lemma lem:square-zero-degree-zero-higgs

## statement
Let \(V\) and \(i:L=K^{-1}\to V\) be as in Lemma \(\mathrm{lem:torsion-augmented-extension}\). Put
\[
H=V\oplus\mathcal O_X.
\]
Define a Higgs field \(\theta:H\to H\otimes K\) by \(\theta|_V=0\), and on the second summand by
\[
\mathcal O_X=L\otimes K\xrightarrow{i\otimes 1_K}V\otimes K\subset H\otimes K.
\tag{3}
\]
Then \((H,\theta)\) is a semistable Higgs bundle of degree \(0\), and \(\theta\neq 0\) is nilpotent.

## proof
The underlying bundle has degree
\[
\deg H=\deg V+\deg\mathcal O_X=0.
\]
The Higgs field is nonzero because \(i\) is injective. It is square-zero because \(\theta\) vanishes on \(V\) and its image is contained in \(V\otimes K\). Thus \(\theta\) is nilpotent.

It remains to prove Higgs semistability. Let \(S\subset H\) be a nonzero \(\theta\)-invariant subbundle. If \(S\subset V\), then Lemma \(\mathrm{lem:V-semistable}\) gives \(\deg S\leq 0\).

Suppose now that \(S\not\subset V\). Let \(M\subset\mathcal O_X\) be the image of \(S\) under the projection \(H=V\oplus\mathcal O_X\to\mathcal O_X\). Then
\[
M\simeq\mathcal O_X(-Z)
\]
for some effective divisor \(Z\). Put \(A=S\cap V\). Since \(S\) is \(\theta\)-invariant, the image of \(M\) under \(\theta\) must lie in \(S\otimes K\). After tensoring by \(K^{-1}\), this says
\[
L(-Z)=M\otimes K^{-1}\subset A\subset V.
\]
In particular \(A\cap L\neq 0\). The proof of Lemma \(\mathrm{lem:V-semistable}\), in the case where the intersection with \(L\) is nonzero, gives \(\deg A\leq 0\). Also \(\deg M\leq 0\). Since \(S/A\) is a subsheaf of \(M\), we get
\[
\deg S\leq \deg A+\deg M\leq 0.
\]

Thus every nonzero \(\theta\)-invariant subbundle has slope at most \(0=\mu(H)\). Hence \((H,\theta)\) is semistable.

# lemma lem:centralizer-quasi-independent

## statement
Let \((H,\theta)\) be the Higgs bundle constructed in Lemma \(\mathrm{lem:square-zero-degree-zero-higgs}\), and let
\[
\mathcal E=\{f\in \underline{\operatorname{End}}_{\mathcal O_X}(H):f\theta=\theta f\}
\]
be its sheaf of Higgs endomorphisms. Then the morphism
\[
T_X=K^{-1}\to\mathcal E
\]
induced by \(\theta\) gives the zero map
\[
H^1(X,T_X)\to H^1(X,\mathcal E).
\]

## proof
Write \(H=V\oplus\mathcal O_X\). The direct summand
\[
\underline{\operatorname{Hom}}(\mathcal O_X,V)=V
\]
inside \(\underline{\operatorname{End}}(H)\) consists of endomorphisms that vanish on \(V\) and map \(\mathcal O_X\) to \(V\). Every such endomorphism commutes with \(\theta\), because \(\theta|_V=0\) and \(\operatorname{im}\theta\subset V\otimes K\). Moreover, in block-matrix form, the commutation equations impose no condition on this upper-right block. Therefore this copy of \(V\) is a direct summand of \(\mathcal E\).

On a curve, contraction of \(\theta\) with vector fields is the morphism
\[
T_X=K^{-1}\to\mathcal E.
\]
Under the direct-summand projection \(\mathcal E\to V\), this morphism is precisely the inclusion
\[
i:L=K^{-1}\to V
\]
from Lemma \(\mathrm{lem:torsion-augmented-extension}\), and it has no component in the complementary summand. Lemma \(\mathrm{lem:torsion-augmented-extension}\) shows that
\[
H^1(X,L)\to H^1(X,V)
\]
is zero. Since \(V\) is a direct summand of \(\mathcal E\), the whole induced map
\[
H^1(X,T_X)\to H^1(X,\mathcal E)
\]
is zero.

# theorem

## statement
Definition: Let C be an algebraically closed field of characteristic 0, and let \(X / C\) be a proper smooth variety over C. Let (H, θ) be a Higgs bundle over X, and let E denote the endomorphism sheaf of (H, θ). That is,  
\[
\mathcal {E} = \{f \in \underline {{E n d}} _ {\mathcal {O} _ {X}} (\mathcal {H}): f \mathrm{commuteswith} \theta \}.
\]
Then, \(( { \mathcal { H } } , \theta )\) is called quasi-independent if the homomorphism \(H ^ { 1 } ( X , T _ { X / C } ) \to H ^ { 1 } ( X , { \mathcal { E } } )\) induced by θ vanishes. 

Let X be a proper smooth curve over C of genus \(g \geq 2\) . Is every quasi-independent, nilpotent and semi-stable Higgs bundle (H, θ) such that deg (H) = 0 must have \(\theta = 0\) ?

## proof
No. We construct a counterexample on any such curve \(X\).

Let \(K=\Omega^1_{X/C}\), \(L=K^{-1}\), and choose \(V\) and \(i:L\to V\) as in Lemma \(\mathrm{lem:torsion-augmented-extension}\). Put
\[
H=V\oplus\mathcal O_X
\]
and define \(\theta\) by (3). Lemma \(\mathrm{lem:square-zero-degree-zero-higgs}\) shows that \((H,\theta)\) is a semistable Higgs bundle, that
\[
\deg H=0,
\]
and that \(\theta\neq 0\) is nilpotent. Lemma \(\mathrm{lem:centralizer-quasi-independent}\) shows that the induced homomorphism
\[
H^1(X,T_{X/C})\to H^1(X,\mathcal E)
\]
vanishes, so \((H,\theta)\) is quasi-independent.

Thus there exists a quasi-independent, nilpotent, semistable Higgs bundle of degree \(0\) with \(\theta\neq 0\). Therefore the proposed assertion is false.
