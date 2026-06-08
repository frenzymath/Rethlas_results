# lemma lem:globally-generated-bound

## statement
Let \(A\) be a globally generated coherent sheaf on a smooth projective curve \(X\) over an algebraically closed field. Then
\[
h^0(X,A)\leq \deg(A)+\operatorname{rk}(A).
\]
Here the degree of a torsion sheaf is its length.

## proof
Let \(T\subset A\) be the torsion subsheaf and put \(B=A/T\). Then \(B\) is a globally generated vector bundle, \(h^0(T)=\deg(T)\), and the exact sequence
\[
0\to T\to A\to B\to 0
\]
gives \(h^0(A)\leq h^0(T)+h^0(B)\). It is therefore enough to prove the assertion for globally generated vector bundles.

If \(B\) has rank \(1\), then \(B\) is a globally generated line bundle. A line bundle \(L\) with a nonzero section satisfies \(h^0(L)\leq \deg(L)+1\), for example by induction on \(\deg(L)\) using
\[
0\to L(-p)\to L\to L|_p\to 0
\]
at a point \(p\). Hence the desired inequality holds in rank \(1\).

Now let \(B\) have rank \(r\geq 2\). Because \(B\) is globally generated and the ground field is infinite, \(r-1\) general global sections are everywhere linearly independent on the curve. Thus they define an exact sequence
\[
0\to \mathcal O_X^{r-1}\to B\to L\to 0,
\]
where \(L\) is a globally generated line bundle and \(\deg L=\deg B\). Therefore
\[
h^0(B)\leq (r-1)+h^0(L)\leq (r-1)+(\deg B+1)=\deg B+r.
\]
Combining this with the torsion reduction gives the claim for \(A\).

# lemma lem:centralizer-degree-bound

## statement
Let \(C\) be an algebraically closed field of characteristic \(0\), let \(X/C\) be a smooth proper curve, and let \((H,\theta)\) be a semistable Higgs bundle on \(X\). Let
\[
\mathcal E=\ker\bigl(\operatorname{End}_{\mathcal O_X}(H)\xrightarrow{[\theta,\;]}
\operatorname{End}_{\mathcal O_X}(H)\otimes K_X\bigr)
\]
be the sheaf of endomorphisms commuting with \(\theta\). Then every coherent subsheaf \(F\subset \mathcal E\) satisfies \(\deg F\leq 0\).

## proof
We first recall the external semistability input used here. Sheng and Wang prove the following tensor product theorem:

**Complete cited statement.** Let \(k\) be an algebraically closed field. Let \(X\) be a smooth projective variety over \(k\) and \(L\) an ample line bundle over \(X\). Let \(D\) be a reduced effective normal crossing divisor in \(X\). Let \(\lambda\in k\). Let \((E^i_\bullet,\nabla^i)\), \(i=1,2\), be two \(\mu_L\)-semistable parabolic \(\lambda\)-connections over \((X,D)\). If either \(\operatorname{char} k=0\), or \(\operatorname{char} k=p>0\) and \(\operatorname{rk}(E^1)+\operatorname{rk}(E^2)\leq p+1\), then their tensor product is \(\mu_L\)-semistable.

This is Theorem 1.1 of Sheng-Wang, *Tensor product theorem for parabolic \(\lambda\)-connections*, paper_id `Sheng-Wang-2022-tensor-product-parabolic-lambda-connections`, theorem_id `Theorem 1.1`, arXiv id `2107.06624`. In the present setting \(D=\varnothing\), the parabolic structure is trivial, and \(\lambda=0\); a \(\lambda=0\) connection is exactly an \(\mathcal O_X\)-linear Higgs field. Thus the cited theorem specializes to the statement that the tensor product of two semistable Higgs bundles over a characteristic-zero curve is semistable. The paper also explicitly identifies this characteristic-zero Higgs specialization with Simpson's tensor product theorem.

The dual Higgs bundle \(H^\vee\), with its usual dual Higgs field, is semistable: equivalently, a destabilizing Higgs subsheaf of \(H^\vee\) would dualize to a Higgs quotient of \(H\) of slope smaller than \(\mu(H)\), contradicting semistability of \(H\). By the cited tensor product theorem, the Higgs bundle
\[
\operatorname{End}(H)=H^\vee\otimes H
\]
with Higgs field \(\operatorname{ad}(\theta)=[\theta,\;]\) is semistable. Its degree is \(0\).

The sheaf \(\mathcal E\) is the kernel of \(\operatorname{ad}(\theta)\), hence any coherent subsheaf \(F\subset \mathcal E\) is a Higgs subsheaf of the semistable degree-zero Higgs bundle \((\operatorname{End}(H),\operatorname{ad}\theta)\). Therefore \(\mu(F)\leq 0\), and so \(\deg F\leq 0\).

# theorem

## statement
Definition: Let C be an algebraically closed field of characteristic 0, and let \(X / C\) be a proper smooth variety over C. Let (H, θ) be a Higgs bundle over X, and let E denote the endomorphism sheaf of (H, θ). That is,  
\[
\mathcal {E} = \{f \in \underline {{E n d}} _ {\mathcal {O} _ {X}} (\mathcal {H}): f \mathrm{commuteswith} \theta \}.
\]
Then, \(( { \mathcal { H } } , \theta )\) is called quasi-independent if the homomorphism \(H ^ { 1 } ( X , T _ { X / C } ) \to H ^ { 1 } ( X , { \mathcal { E } } )\) induced by θ vanishes. 

Let \(n \geq 1\) be an integer. Does there exist an integer \(m \geq 2\) such that for any proper smooth curve X over C of genus \(g \ge m\) , every quasi-independent, nilpotent semi-stable Higgs bundle (H, θ) of rank n must have \(\theta = 0 ?\)

## proof
Yes. We show that one may take
\[
m=n^2+1.
\]
Since \(n\geq 1\), this integer is at least \(2\).

Let \(X/C\) be a smooth proper curve of genus \(g\geq n^2+1\), let \(K_X=\Omega^1_{X/C}\), and let \((H,\theta)\) be a quasi-independent nilpotent semistable Higgs bundle of rank \(n\). Suppose, for contradiction, that \(\theta\neq 0\).

On a curve, contraction with vector fields gives a morphism
\[
\varphi_\theta:T_X=K_X^{-1}\longrightarrow \mathcal E.
\]
Locally, if \(\theta=A\,dz\), then \(\varphi_\theta(\partial/\partial z)=A\). This endomorphism commutes with \(\theta\), so the image lies in \(\mathcal E\). Since \(\theta\neq 0\), the morphism \(\varphi_\theta\) is nonzero. The sheaf \(\mathcal E\) is torsion-free as a subsheaf of \(\operatorname{End}(H)\), so a nonzero morphism from the line bundle \(K_X^{-1}\) to \(\mathcal E\) is injective. Let \(Q\) be its cokernel:
\[
0\to K_X^{-1}\xrightarrow{\varphi_\theta}\mathcal E\to Q\to 0.
\]

Quasi-independence says precisely that the induced map
\[
H^1(X,K_X^{-1})\to H^1(X,\mathcal E)
\]
is zero. The associated long exact cohomology sequence therefore shows that the boundary map
\[
H^0(X,Q)\to H^1(X,K_X^{-1})
\]
is surjective. Hence
\[
h^0(X,Q)\geq h^1(X,K_X^{-1}).
\]
By Serre duality and Riemann-Roch,
\[
h^1(X,K_X^{-1})=h^0(X,K_X^2)=3g-3
\]
because \(g\geq 2\). Thus
\[
h^0(X,Q)\geq 3g-3. \tag{1}
\]

Now let \(Q'\subset Q\) be the coherent subsheaf generated by all global sections of \(Q\), i.e. the image of
\[
H^0(X,Q)\otimes\mathcal O_X\to Q.
\]
Then \(Q'\) is globally generated and the inclusion \(Q'\subset Q\) identifies \(H^0(X,Q')\) with \(H^0(X,Q)\). Also
\[
\operatorname{rk}(Q')\leq \operatorname{rk}(Q)\leq \operatorname{rk}(\mathcal E)-1\leq n^2-1.
\]

Let \(F\subset\mathcal E\) be the inverse image of \(Q'\). Then
\[
0\to K_X^{-1}\to F\to Q'\to 0
\]
is exact. By Lemma \(\mathrm{lem:centralizer-degree-bound}\), \(\deg F\leq 0\). Therefore
\[
\deg(Q')=\deg(F)-\deg(K_X^{-1})\leq 0+(2g-2)=2g-2.
\]
Applying Lemma \(\mathrm{lem:globally-generated-bound}\) to the globally generated sheaf \(Q'\), we get
\[
h^0(X,Q)=h^0(X,Q')\leq \deg(Q')+\operatorname{rk}(Q')
\leq (2g-2)+(n^2-1)=2g+n^2-3. \tag{2}
\]

The inequalities (1) and (2) imply
\[
3g-3\leq 2g+n^2-3,
\]
so \(g\leq n^2\). This contradicts \(g\geq n^2+1\). Hence \(\theta=0\).

Thus the required integer exists; \(m=n^2+1\) works.
