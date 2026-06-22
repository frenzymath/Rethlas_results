# lemma lem:lifting_rank_two_criterion

## statement
Let \(A\in \mathbb C^{N\times M}\), and write its rows as \(a_1^*,\ldots,a_N^*\), where \(a_j\in\mathbb C^M\). Define the real-linear map on Hermitian matrices
\[
    \mathcal L_A(Q)=(a_1^*Qa_1,\ldots,a_N^*Qa_N)\in\mathbb R^N .
\]
Then the phase retrieval map \(x\in \mathbb C^M/\mathbb T\mapsto |Ax|\) is injective if and only if \(\ker \mathcal L_A\) contains no nonzero Hermitian matrix of rank at most \(2\).

## proof
The modulus data and the squared modulus data determine each other, so we may use \((|a_j^*x|^2)_j\). For \(x,y\in\mathbb C^M\),
\[
    |a_j^*x|^2-|a_j^*y|^2
    = a_j^*(xx^*-yy^*)a_j .
\]
Thus, if \(x\) and \(y\) have the same measurements, then
\[
    Q=xx^*-yy^*
\]
lies in \(\ker \mathcal L_A\). If \(x\) and \(y\) are not equivalent modulo \(\mathbb T\), then \(Q\ne0\), and clearly \(\operatorname{rank}Q\le2\).

Conversely, suppose \(0\ne Q\in\ker\mathcal L_A\) is Hermitian and \(\operatorname{rank}Q\le2\). We split according to the inertia of \(Q\).

If \(Q\) has both a positive and a negative eigenvalue, then, since its rank is at most \(2\), the spectral theorem gives
\[
    Q=xx^*-yy^*
\]
for nonzero vectors \(x,y\). Since \(\mathcal L_A(Q)=0\), the squared modulus measurements of \(x\) and \(y\) agree. The vectors \(x\) and \(y\) are not equivalent modulo \(\mathbb T\), because otherwise \(xx^*-yy^*\) would be a scalar multiple of \(xx^*\), not an indefinite rank-two matrix.

It remains to handle the semidefinite cases. Suppose first that \(Q\ge0\). Since \(Q\ne0\), choose a nonzero vector \(x\in\operatorname{range}(Q)\). For each \(j\),
\[
    0=a_j^*Qa_j.
\]
Because \(Q\ge0\), this implies \(Q^{1/2}a_j=0\), hence \(a_j\) is orthogonal to \(\operatorname{range}(Q)\). Therefore \(a_j^*x=0\) for every \(j\), so \(Ax=A\,0=0\). The nonzero vector \(x\) is not equivalent to \(0\) modulo \(\mathbb T\), so the phase retrieval map is not injective. If \(Q\le0\), the same argument applies to \(-Q\ge0\). Thus any nonzero rank-at-most-two Hermitian element of \(\ker\mathcal L_A\) produces noninjectivity. This proves the equivalence.

# lemma lem:transverse_bad_frame

## statement
For every integer \(M\ge2\), with \(N=4M-5\), there is a matrix \(A_0\in\mathbb C^{N\times M}\) and an open neighborhood \(U\) of \(A_0\) in \(\mathbb C^{N\times M}\) such that every \(A\in U\) is not injective for phase retrieval.

## proof
Let
\[
    Q_0=\operatorname{diag}(1,-1,0,\ldots,0).
\]
We construct \(A_0\) row by row. Let \(e_1,\ldots,e_{M-2}\) denote the standard basis of \(\mathbb C^{M-2}\), and let \(0\) denote the zero vector in \(\mathbb C^{M-2}\). The rows, written as column measurement vectors, are
\[
    (1,1,0),\qquad (1,-1,0),\qquad (1,i,0),
\]
and, for each \(\ell=1,\ldots,M-2\), the four vectors
\[
    (1,1,e_\ell),\qquad (1,1,ie_\ell),\qquad
    (1,-1,e_\ell),\qquad (1,-1,ie_\ell).
\]
There are \(3+4(M-2)=4M-5=N\) rows. Every one of these vectors \(a\) satisfies
\[
    a^*Q_0a=|a_1|^2-|a_2|^2=0.
\]
Thus \(Q_0\in\ker\mathcal L_{A_0}\), so \(A_0\) itself is not injective. We now prove that this obstruction persists under small perturbations of \(A_0\).

Consider the following exact local parametrization of Hermitian matrices of rank at most \(2\) near \(Q_0\). Put
\[
    D(s,b)=
    \begin{pmatrix}
        1+s/2 & b\\
        \overline b & -1+s/2
    \end{pmatrix},
    \qquad
    C(z,t)=
    \begin{pmatrix}
        z_1 & t_1\\
        \vdots & \vdots\\
        z_{M-2} & t_{M-2}
    \end{pmatrix},
\]
where \(s\in\mathbb R\) and \(b,z_\ell,t_\ell\in\mathbb C\). For \((s,b,z,t)\) sufficiently small, \(D(s,b)\) is invertible, and
\[
    Q(s,b,z,t)=
    \begin{pmatrix}
        D(s,b) & C(z,t)^*\\
        C(z,t) & C(z,t)D(s,b)^{-1}C(z,t)^*
    \end{pmatrix}
\]
is Hermitian of rank at most \(2\). Also \(Q(0,0,0,0)=Q_0\).

For a row vector \(a\), define
\[
    F_a(s,b,z,t)=a^*Q(s,b,z,t)a .
\]
At the origin, the differential is computed from the linear part
\[
    H(s,b,z,t)=
    \begin{pmatrix}
        s/2 & b & \overline z^{\,T}\\
        \overline b & s/2 & \overline t^{\,T}\\
        z & t & 0
    \end{pmatrix},
\]
because the lower-right block \(C D^{-1}C^*\) has no linear term. Hence, for \(a=(u,v,w)\) with \(|u|=|v|=1\),
\[
    dF_a(0)(s,b,z,t)
    =
    s+2\operatorname{Re}(\overline u\,b\,v)
      +2\operatorname{Re}\!\left(\overline u\,\overline z^{\,T}w
      +\overline v\,\overline t^{\,T}w\right).
\]
For the first three rows this gives
\[
    s+2\operatorname{Re}b,\qquad
    s-2\operatorname{Re}b,\qquad
    s-2\operatorname{Im}b.
\]
Thus these three differentials determine \(s\), \(\operatorname{Re}b\), and \(\operatorname{Im}b\).

Fix \(\ell\). Once \(s=b=0\), the four rows involving \(e_\ell\) give
\[
    2\operatorname{Re}(z_\ell+t_\ell),\qquad
    2\operatorname{Im}(z_\ell+t_\ell),\qquad
    2\operatorname{Re}(z_\ell-t_\ell),\qquad
    2\operatorname{Im}(z_\ell-t_\ell).
\]
These determine \(z_\ell\) and \(t_\ell\). Therefore the total differential
\[
    (s,b,z,t)\longmapsto \bigl(dF_{a_j}(0)(s,b,z,t)\bigr)_{j=1}^N
\]
is an isomorphism from the real vector space
\[
    \mathbb R\times\mathbb C\times\mathbb C^{M-2}\times\mathbb C^{M-2}
\]
onto \(\mathbb R^N\). Both spaces have real dimension
\[
    1+2+2(M-2)+2(M-2)=4M-5=N.
\]

Now let \(A\) vary near \(A_0\), and define
\[
    \Phi(A,s,b,z,t)
    =
    \bigl(a_j(A)^*Q(s,b,z,t)a_j(A)\bigr)_{j=1}^N,
\]
where \(a_j(A)\) denotes the \(j\)-th measurement vector of \(A\). We have
\[
    \Phi(A_0,0,0,0,0)=0,
\]
and the derivative of \(\Phi\) with respect to \((s,b,z,t)\) at that point is the isomorphism just proved. By the real implicit function theorem, for all \(A\) in some open neighborhood \(U\) of \(A_0\), there are small parameters \((s(A),b(A),z(A),t(A))\) such that
\[
    \Phi(A,s(A),b(A),z(A),t(A))=0.
\]
The corresponding \(Q(A)=Q(s(A),b(A),z(A),t(A))\) is nonzero, Hermitian, and has rank at most \(2\). Hence \(Q(A)\in\ker\mathcal L_A\). By Lemma \(\mathrm{lem:lifting\_rank\_two\_criterion}\), every \(A\in U\) is not injective for phase retrieval.

# theorem

## statement
Let $N,M$ be two integers. Given a complex matrix $A \in \mathbb C^{N\times M}$, the phase retrieval problem aims to recover a vector $x \in \mathbb C^{M}$ from $|Ax|$, where $|\cdot|$ is the entrywise modulus. Let $\mathbb T$ be the unit circle in $\mathbb C$, we can only hope to recover $x$ module $\mathbb T$. More precisely, let $\mathbb C^M/\mathbb T$ be $\mathbb C^M$ module $\mathbb T$ (meaning that $x=(x_1,\ldots,x_M) \in \mathbb C^M$ and $y=(y_1,\ldots,y_M) \in \mathbb C^M$ are equivalent if and only if there exists $|z|=1$ such that $x=zy$), we say $A$ is injective for phase retrieval if the map
\begin{align*}
    x \in \mathbb C^M/\mathbb T \to |Ax|
\end{align*}
is injective.

    Let $N=4M-5$ and let $A \in \mathbb C^{N\times M}$ be a matrix with entries i.i.d.\ drawn from the standard complex Gaussian distribution (a complex standard Gaussian has the law of $a+ib$ where $a,b \sim \mathcal N(0,\frac{1}{2})$ are independent). Let $p_M$ be the probability that the mapping
    \begin{align*}
        x \in \mathbb C^M/\mathbb T \to |Ax|
    \end{align*}
    is injective. Prove or disprove that $p_M<1$ for all $M$.

## proof
The random matrix model in the statement is defined only when \(N=4M-5\) is a nonnegative integer. Thus the meaningful range of the question is \(M\ge2\); for \(M=1\), \(N=-1\), so the matrix space \(\mathbb C^{N\times M}\) and the probability \(p_M\) are not defined. We prove the asserted inequality throughout this meaningful range.

By Lemma \(\mathrm{lem:transverse\_bad\_frame}\), there is a nonempty open set
\[
    U\subset \mathbb C^{N\times M}
\]
such that every \(A\in U\) is not injective for phase retrieval. The standard complex Gaussian distribution on \(\mathbb C^{N\times M}\) has a strictly positive density with respect to Lebesgue measure. Therefore every nonempty open set has positive probability, and
\[
    \mathbb P(A\in U)>0.
\]
Consequently
\[
    p_M
    =
    \mathbb P(A\text{ is injective for phase retrieval})
    \le 1-\mathbb P(A\in U)
    <1.
\]
Thus the proposed inequality \(p_M<1\) holds for all meaningful integers \(M\ge2\). For \(M=1\), the formula \(N=4M-5\) gives \(N=-1\), so the stated random matrix model is not defined.
