# lemma lem:agcd_is_apvmd

## statement
Let $D$ be an almost GCD domain. Then $D$ is an almost Prüfer $v$-multiplication domain (APVMD). Equivalently, for every finite set $x_1,\dots,x_n \in D \setminus \{0\}$ there exists an integer $m \ge 1$ such that $(x_1^m,\dots,x_n^m)_t$ is $t$-invertible.

## proof
This is the implication recorded in the following cited result: **an AGCD domain is an APVMD**. Source: Muhammad Zafrullah, *Domains whose ideals meet a universal restriction*, `paper_id`: `2006.04135`, `theorem_id`: `Lemma 4.3(6)`, `arXiv id`: `2006.04135`.

# lemma lem:agcd_is_t_sab

## statement
Let $D$ be an almost GCD domain. Then $D$ is a $t$-SAB domain.

## proof
In the notation of the cited paper, an AGCD domain is exactly a $t$-AB domain, and Lemma 4.3(13) states that **an AGCD ($t$-AB) domain is an SAGCD ($t$-SAB) domain**. Hence every AGCD domain is a $t$-SAB domain. Source: Muhammad Zafrullah, *Domains whose ideals meet a universal restriction*, `paper_id`: `2006.04135`, `theorem_id`: `Lemma 4.3(13)`, `arXiv id`: `2006.04135`.

# theorem thm:t_sab_finite_character_criterion

## statement
Let $D$ be a $t$-SAB domain, and let $\Gamma$ be the set of proper nonzero principal ideals of $D$. Then $D$ is of finite $t$-character if and only if every power of every proper $t$-ideal of finite type is contained in at most finitely many mutually $t$-comaximal members of $\Gamma$.

## proof
This is exactly Corollary 6 of *Domains whose ideals meet a universal restriction* specialized to $\ast=t$. Complete cited statement used here: **Let $D$ be a $\ast$-SAB domain. Then $D$ is of finite $\ast$-character if and only if every power of a proper $\ast$-ideal of finite type is contained in at most a finite number of mutually $\ast$-comaximal members of $\Gamma$**. Source: `paper_id`: `2006.04135`, `theorem_id`: `Corollary 6`, `arXiv id`: `2006.04135`.

# theorem thm:zafrullah_obstruction

## statement
Let $D$ be a domain. Assume that there exists an integral $t$-invertible $t$-ideal $A$ that is contained in infinitely many mutually $t$-comaximal $t$-invertible $t$-ideals of $D$. Then $D$ contains a nonzero $t$-locally principal ideal that is not $t$-invertible.

## proof
This is exactly the content of Proposition 4 in Muhammad Zafrullah, *t-invertibility and Bazzoni-like statements*. The proposition proves more precisely that under the displayed hypothesis one can construct a $t$-ideal $F$ that is $t$-locally principal but is not a $t$-ideal of finite type, hence not $t$-invertible. Source: `paper_id`: `[111]`, `theorem_id`: `Proposition 4`, `arXiv id`: not available.

# theorem thm:decl_35

## statement
An integral domain $D$ is called an \emph{almost GCD} (for short, AGCD) domain if for each pair $x, y \in D \setminus \{0\}$ there is an integer $n = n(x,y)$ (depending on $x$ and $y$) such that $x^n D \cap y^n D$ is principal. The theory of AGCD domains runs along lines similar to that of GCD domains; see [6] for more information and a list of references on the topic. An integral domain $D$ is a domain of \emph{finite $t$-character} if every nonzero non-unit of $D$ belongs to at most a finite number of maximal $t$-ideals of $D$. AGCD domains of finite $t$-character were characterized in [34]. An ideal $A$ of $D$ is \emph{$t$-locally principal} if $AD_P$ is principal for every maximal $t$-ideal $P$ of $D$. In [111] it was shown that if $D$ is a P$v$MD then $D$ is of finite $t$-character if and only if every nonzero $t$-locally principal ideal of $D$ is $t$-invertible. A GCD domain is a P$v$MD because the $v$-closure of every nonzero finitely generated ideal in a GCD domain is principal. We can therefore conclude that a GCD domain is of finite $t$-character if and only if every nonzero $t$-locally principal ideal $A$ of $D$ is $t$-invertible.

[6] D. D. Anderson and M. Zafrullah, Almost Bézout domains, J. Algebra 142 (1991), 285-309.

[34] T. Dumitrescu, Y. Lequain, J. Mott and M. Zafrullah, Almost GCD domains of finite t-character, J. Algebra 245 (2001), 161-181.

[111] M. Zafrullah, t-invertibility and Bazzoni-like statements, J. Pure Appl. Algebra 214 (2010), 654-657.

Let $D$ be an almost GCD domain such that every nonzero $t$-locally principal ideal is $t$-invertible. Is $D$ of finite $t$-character?

## proof
We prove that the answer is **yes**.

Assume toward a contradiction that $D$ is **not** of finite $t$-character.

By Lemma `lem:agcd_is_t_sab`, the AGCD hypothesis implies that $D$ is a $t$-SAB domain. Therefore Theorem `thm:t_sab_finite_character_criterion` applies. Since $D$ does not have finite $t$-character, that theorem yields:

there exists a proper $t$-ideal $I$ of finite type and a positive integer $m$ such that $I^m$ is contained in infinitely many mutually $t$-comaximal proper nonzero principal ideals
\[
\gamma_\lambda \qquad (\lambda \in \Lambda),
\]
where $\Lambda$ is infinite.

Choose a finitely generated ideal $J=(a_1,\dots,a_n)$ with $I=J_t$. Then for every $\lambda \in \Lambda$ we have
\[
a_1^m,\dots,a_n^m \in I^m \subseteq \gamma_\lambda.
\]

Next, by Lemma `lem:agcd_is_apvmd`, the AGCD hypothesis also implies that $D$ is an APVMD. Apply the APVMD property to the finite set $a_1^m,\dots,a_n^m$. We obtain an integer $r \ge 1$ such that
\[
A:= (a_1^{mr},\dots,a_n^{mr})_t
\]
is a $t$-invertible $t$-ideal.

For each $\lambda \in \Lambda$, because $\gamma_\lambda$ is principal we have $\gamma_\lambda^r$ again principal, hence a $t$-ideal, and
\[
a_1^{mr},\dots,a_n^{mr} \in \gamma_\lambda^r.
\]
Therefore
\[
A=(a_1^{mr},\dots,a_n^{mr})_t \subseteq \gamma_\lambda^r
\]
for every $\lambda \in \Lambda$.

Also the ideals $\gamma_\lambda^r$ remain mutually $t$-comaximal: indeed, if some maximal $t$-ideal contained both $\gamma_\lambda^r$ and $\gamma_\mu^r$, then it would contain both $\gamma_\lambda$ and $\gamma_\mu$, contradicting the mutual $t$-comaximality of the $\gamma_\lambda$.

Thus we have produced an integral $t$-invertible $t$-ideal $A$ contained in infinitely many mutually $t$-comaximal $t$-invertible $t$-ideals $\gamma_\lambda^r$.

Now apply Theorem `thm:zafrullah_obstruction`. It follows that $D$ contains a nonzero $t$-locally principal ideal that is not $t$-invertible.

But this contradicts the hypothesis of the problem, which says that every nonzero $t$-locally principal ideal of $D$ is $t$-invertible.

Hence our assumption was false. Therefore $D$ is of finite $t$-character.
