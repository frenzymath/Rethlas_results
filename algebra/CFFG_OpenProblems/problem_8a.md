# lemma lem:complete_domain_choice

## statement
Let
\[
T=\mathbb{C}[[x,y,z]]/(x^2-yz),
\]
and let \(M=(x,y,z)T\). Then:

1. \(T\) is a complete \(2\)-dimensional Cohen-Macaulay local domain.
2. \(|T|=|T/M|=|\mathbb{C}|\).
3. The height-one prime ideal
\[
Q=(x,y)T
\]
is not principal.

## proof
The ring \(\mathbb{C}[[x,y,z]]\) is a complete regular local domain of dimension \(3\). The quotient
\[
T=\mathbb{C}[[x,y,z]]/(x^2-yz)
\]
is isomorphic to the subring \(\mathbb{C}[[u^2,uv,v^2]]\subseteq \mathbb{C}[[u,v]]\) via
\[
x\mapsto uv,\qquad y\mapsto u^2,\qquad z\mapsto v^2.
\]
Hence \(T\) is a domain. Since \(x^2-yz\) is a nonzerodivisor in the regular local ring \(\mathbb{C}[[x,y,z]]\), the quotient \(T\) is a hypersurface and therefore Cohen-Macaulay of dimension \(2\).

Also \(T/M\cong \mathbb{C}\), and a formal power series ring in finitely many variables over the uncountable field \(\mathbb{C}\) has the same cardinality as \(\mathbb{C}\), so \(|T|=|T/M|=|\mathbb{C}|\).

Finally,
\[
T/Q \cong \mathbb{C}[[z]],
\]
so \(Q\) is prime and has height \(1\). To see that \(Q\) is not principal, note that \(MQ\subseteq M^2\), while \(x,y\notin M^2\) because the defining relation is quadratic. Hence the images of \(x\) and \(y\) in \(Q/MQ\) are nonzero and linearly independent over \(T/M\cong\mathbb{C}\). Thus \(\mu(Q)=\dim_{\mathbb{C}}(Q/MQ)\ge 2\), so \(Q\) is not principal.


# lemma lem:jensen_special_case

## statement
There exists a \(2\)-dimensional local UFD \(A\) such that \(\widehat{A}\cong T\) and the generic formal fiber of \(A\) is local with maximal ideal \((0)\).

## proof
We apply the following external result.

Complete cited statement:

Corollary 2.4 of Jensen, *Completions of UFDs with Semi-Local Formal Fibers* (paper_id: `10.1080/00927870500346321`, theorem_id: `Corollary 2.4`, arXiv id: none) states:

“Let \((T,M)\) be a complete local ring and \(|T/M|=|T|\). Let \(P\in \operatorname{Spec}T\). Then there exists a local UFD \(A\) such that \(\widehat A=T\) and the generic formal fiber of \(A\) is local with maximal ideal \(P\) iff \(T\) is a field or DVR and \(P=(0)\), or \(T\) has depth at least two and:

1. \(P\) is nonmaximal and contains all associated prime ideals of \(T\);
2. \(P\cap\) the prime subring of \(T\) is \((0)\);
3. if \(J\in \operatorname{Spec}T\) with \(\operatorname{ht}(J)>\operatorname{depth}(T_J)=1\), then \(J\subseteq P\).”

We apply this with the ring \(T\) from Lemma \ref{lem:complete_domain_choice} and with \(P=(0)\). The hypotheses hold:

1. \(T\) is complete and \(|T|=|T/M|\) by Lemma \ref{lem:complete_domain_choice}.
2. \(T\) has depth \(2\) by Lemma \ref{lem:complete_domain_choice}.
3. Since \(T\) is a domain, its only associated prime is \((0)\), so \(P=(0)\) contains all associated primes.
4. \(P=(0)\) is nonmaximal and meets the prime subring trivially.
5. Because \(T\) is Cohen-Macaulay, there is no prime \(J\) with \(\operatorname{ht}(J)>\operatorname{depth}(T_J)=1\).

Therefore Jensen’s corollary yields a local UFD \(A\) with \(\widehat A\cong T\) whose generic formal fiber is local with maximal ideal \((0)\).


# lemma lem:a_is_weak_and_has_bad_quotient

## statement
For the ring \(A\) of Lemma \ref{lem:jensen_special_case}, the following hold:

1. \(A\) is weakly quasi-complete.
2. There exists a prime element \(a\in A\) such that \(A/aA\) is a one-dimensional Noetherian local domain that is not weakly quasi-complete.

## proof
Because the generic formal fiber of \(A\) is local with maximal ideal \((0)\), the only prime ideal of \(\widehat A\cong T\) contracting to \((0)\) is \((0)\) itself. Hence every nonzero prime ideal of \(\widehat A\) has nonzero contraction to \(A\).

Now invoke the following external result.

Complete cited statement:

Proposition 1 of Farley, *Quasi-completeness and localizations of polynomial domains: A conjecture from “Open Problems in Commutative Ring Theory”* (paper_id: `BKMS.b140895`, theorem_id: `Proposition 1`, arXiv id: none) states:

“A Noetherian local integral domain \(R\) is weakly quasi-complete if and only if \(P\cap R\neq\{0\}\) for each non-zero prime ideal \(P\) of \(\widehat R\), the completion of \(R\).”

Since \(A\) is a Noetherian local integral domain and every nonzero prime of \(\widehat A\) meets \(A\) nontrivially, Proposition 1 shows that \(A\) is weakly quasi-complete.

Next consider the height-one prime \(Q=(x,y)T\) from Lemma \ref{lem:complete_domain_choice}. Since \(Q\neq (0)\), the triviality of the generic formal fiber implies
\[
q:=Q\cap A \neq (0).
\]
Because \(\widehat A\) is faithfully flat over \(A\), we have
\[
1 \le \operatorname{ht}(q)\le \operatorname{ht}(Q)=1,
\]
so \(\operatorname{ht}(q)=1\). As \(A\) is a UFD, \(q=aA\) for some prime element \(a\in A\).

We claim that \(aT\) is not prime. Indeed, \(aT\subseteq Q\). If \(aT\) were prime, then \(\operatorname{ht}(aT)=1\), so the inclusion \(aT\subseteq Q\) of height-one prime ideals would force \(aT=Q\), contradicting the fact that \(Q\) is not principal.

Therefore \(T/aT\) is not a domain. Since completion commutes with quotient for Noetherian local rings,
\[
\widehat{A/aA}\cong \widehat A/a\widehat A \cong T/aT,
\]
so \(\widehat{A/aA}\) is not a domain. Because \(a\) is prime in the domain \(A\), the quotient \(A/aA\) is a one-dimensional Noetherian local domain. Hence \(A/aA\) is not analytically irreducible.

Now use the criterion quoted in the problem statement itself:

Complete cited statement:

Anderson, *Quasi-complete semilocal rings and modules* (paper_id: `Anderson-2014-Chapter`, theorem_id: `Corollary 2.2`, arXiv id: none): “A one-dimensional Noetherian local domain is (weakly) quasi-complete if and only if it is analytically irreducible.”

Since \(A/aA\) is a one-dimensional Noetherian local domain that is not analytically irreducible, it follows that \(A/aA\) is not weakly quasi-complete.


# theorem thm:main

## statement
Let (R,M) be a Noetherian local ring. R is said to be quasi-complete if for any decreasing sequence {A_n}_{n=1}^∞ of ideals of R and each natural number k, there exists a natural number s_k with A_{s_k} ⊆ (⋂_{n=1}^∞ A_n) + M^k. If this condition holds for any decreasing sequence {A_n}_{n=1}^∞ of ideals of R with ⋂_{n=1}^∞ A_n = 0, then R is called weakly quasi-complete (in which case we actually have A_{s_k} ⊆ M^k). If R is complete, then R is quasi-complete, which implies that R is weakly quasi-complete. Also, R is quasi-complete if and only if each homomorphic image of R is weakly quasi-complete. The implication "R complete implies R is quasi-complete" was first proved by Chevalley [24, Lemma 7]; see also [4, Theorem 1.3]. Note that a DVR is quasi-complete but need not be complete. More generally, a one-dimensional Noetherian local domain is (weakly) quasi-complete if and only if it is analytically irreducible [4, Corollary 2.2]. References: [24] C. Chevalley, On the theory of local rings, Ann. Math. 44 (1943), 690–708. [4] D. D. Anderson, Quasi-complete semilocal rings and modules, Commutative Algebra: Recent Advances in Commutative Rings, Integer-Valued Polynomials, and Polynomial Functions, Springer Verlag, New York, 2014. Prove that there exists a weakly quasi-complete ring that is not quasi-complete.

## proof
Let \(A\) be the local UFD constructed in Lemma \ref{lem:jensen_special_case}. By Lemma \ref{lem:a_is_weak_and_has_bad_quotient}, \(A\) is weakly quasi-complete.

The same lemma also gives a prime element \(a\in A\) such that the homomorphic image \(A/aA\) is not weakly quasi-complete.

Finally, the problem statement itself records the equivalence:

Complete cited statement:

“A Noetherian local ring \(R\) is quasi-complete if and only if each homomorphic image of \(R\) is weakly quasi-complete.”

Applying this to \(A\), the quotient \(A/aA\) shows that \(A\) is not quasi-complete.

Thus \(A\) is a weakly quasi-complete Noetherian local ring that is not quasi-complete. This proves the required existence statement.
