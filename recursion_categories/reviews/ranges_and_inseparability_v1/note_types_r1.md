# Type and dependency check of the ranges-and-inseparability note

Source: `output/local_connectedness_note_v1/Ranges_and_Inseparability_v1.tex`, compared with `tmp/move28/LOCOct10f.tex`.

**Disposition:** the new four-domain argument, its application to sections, and the new inseparability proof are mathematically and categorically typed. One minor explicit-quantifier repair is recommended in their existing dependency `PropPartialMono`; no mathematical obstruction was found in the changed proofs.

## Scope and retained statements

Both sources contain 18 theorem/proposition statements: 2 theorems and 16 propositions. The old unlabelled total-test proposition now has the label `PropTotalCopMono`. Its conclusion is retained with the local-connectedness assumption removed. The corresponding assumptions in `PropCopOut` and `ThmRecIns` are weakened in the same way. `PropDisjointJoins` now uses the explicit canonical coproduct comparison. The other 14 statements are unchanged after removing labels and normalizing whitespace.

The mathematical statements and proofs of the preliminary and range-calculus sections are retained. The source is not byte-identical in all of §§1–3: the introduction is adapted to the strengthened criterion, and the preliminary exposition changes “cotuple” to “copairing” and “universal partial function of classical recursion theory” to “universal partial recursive function”. These are not changes to their claims.

This check covers the changed proofs and their relevant typing interfaces. It does not re-prove the entire older manuscript, verify its external literature claims, or constitute a whole-document writing review.

## One minor explicit-typing repair

**Anchor:** `PropPartialMono`, hypothesis “for all morphisms $g,h\in\mathbf C_T$”.

The compositions make the intended types recoverable, but the hypothesis can state them directly:

> Suppose that, for every object $W$ and all total morphisms $g,h:W\to X$, the equality $fg=fh$ implies $\overline f g=\overline f h$.

The existing proof already uses exactly these types. This changes no mathematical hypothesis or conclusion.

## `PropTotalCopMono`

The ambient category is a restriction category with ranges, zeros and binary restriction coproducts. Every inverse-image map on domains is assumed to preserve binary joins.

- $p=\nabla_X(\alpha+\beta):X+X\to X$ is a morphism, not asserted total; its restriction is $\alpha+\beta$.
- The partial projections $\rho_i:X+X\to X$ are not assumed total. Their composites $\varepsilon_i=i_i\rho_i$ are the two summand domains.
- For total $\theta,\theta':Y\to X+X$, the domains $e_i=\theta^*\varepsilon_i$, $f_j=(\theta')^*\varepsilon_j$ and $\delta_{ij}=e_i f_j$ all belong to $\mathrm{Dom}(Y)$.
- Totality and inverse-image join preservation give $e_0\vee e_1=f_0\vee f_1=1_Y$.
- The required distributivity is already established in the range-calculus section, following `PropDomRan`. Therefore the sentence “Distributivity gives” has an earlier proved basis; it does not import extensivity or another hypothesis. It yields $\bigvee_{i,j}\delta_{ij}=1_Y$.

For each pair $i,j$, the morphisms

\[
x_{ij}=\rho_i\theta\delta_{ij},\qquad
y_{ij}=\rho_j\theta'\delta_{ij}:Y\to X
\]

are correctly typed and may be partial. The restriction identity gives the stated factorizations through $i_i$ and $i_j$. Because $pi_0=\alpha$ and $pi_1=\beta$, precomposing $p\theta=p\theta'$ with $\delta_{ij}$ gives

\[
z_{ij}=a_i x_{ij}=a_j y_{ij}:Y\to X.
\]

When $i=j$, the two desired composites are the same $i_i z_{ij}$. When $i\ne j$, idempotence gives $z_{ij}=a_i z_{ij}$, and hence

\[
z_{ij}=a_i a_j y_{ij}=0_{Y,X}.
\]

Both composites into $X+X$ are then zero. No injection cancellation or point argument is required.

The four-fold copairing has the displayed source $((Y+Y)+Y)+Y$ and target $Y$. Its range is the join of the four component domains, hence $1_Y$. Its being a morphism does not assert that it is total. Range agreement consequently gives the required equality of the two morphisms $Y\to X+X$.

Local connectedness, splitness and weak choice are not used in this total-test proposition. Its new assumptions and conclusion are supported by the proof.

## `PropPartialMono` and `PropCopOut`

The splitting in `PropPartialMono` has types $e:W\to Z$, $m:Z\to W$, $em=1_Z$ and $me=\overline{fg}=\overline{fh}$, with $m$ total. Thus $fgm$ and $fhm$ are total. Since their restrictions are bounded above by those of $gm$ and $hm$, the latter are total as well. The total-test hypothesis then applies, and composing its equality on the right with $e$ gives the displayed equality on the original source $W$.

In `PropCopOut`, splitness is retained and permits this reduction. The new `PropTotalCopMono` supplies the required total-test property of $p$. Weak choice then supplies a section. The identities $p f=\overline f=\mathrm{ran}(p)$ and $\overline p f=f$ are valid under the note's definition of a section. Partial monicity proves uniqueness, and $\mathrm{ran}(p)=\alpha\vee\beta$ follows from the receiving property on the two coproduct components.

No local-connectedness argument or unproved preservation of a near product is used here.

## `ThmRecIns`: source and target types

The source is the $P$-recursion category $\mathbf C$; the target is the split restriction category $\mathbf D$. The theorem does not require $F:\mathbf C\to\mathbf D$ to preserve near products.

The source summand domains are

\[
c_0=1_X+0_X,\quad c_1=0_X+1_X
\quad\text{on }X+X.
\]

The target summand domains $P_0,P_1$ are on $FX+FX$. The canonical comparison has type

\[
\chi_{X,X}:FX+FX\xrightarrow{\cong}F(X+X).
\]

Thus $F(c_i)$ and $P_i$ are not identified as endomorphisms of the same object. The displayed equations

\[
\chi_{X,X}P_i=F(c_i)\chi_{X,X}
\]

are well typed and follow by precomposition with each target injection. Functorial preservation of coproducts and zeros suffices.

For a proposed source separator $\gamma$, the domains $\Gamma=F\gamma$ and $\Gamma'=F\gamma^\perp$ are complementary on $FX$. The chosen section $s=s_\gamma:FX\to FX+FX$ exists by `PropCopOut` in $\mathbf D$ and is total by `PropDichotomy`. Its branch equations are correctly typed using the target injections $j_0,j_1$.

The range-agreement argument proving

\[
P_0s=j_0\Gamma',\qquad P_1s=j_1\Gamma
\]

uses the copairing $[\Gamma,\Gamma']:FX+FX\to FX$ with range $1_{FX}$. Taking restrictions gives $s^*P_0=\Gamma'$ and $s^*P_1=\Gamma$.

There is no asserted natural transformation $\gamma\mapsto s_\gamma$, and none is required. The theorem uses the individual unique section for each complemented domain, with the explicit coproduct comparison in its lift equation.

The lift $d_\gamma:X\to X+X$ need not be total in the source. Its composite $u=b^{-1}d_\gamma:X\to X$ is nevertheless eligible for the weak-Turing index property, which applies to every source morphism. The chosen index $e:X\to X$ is total. Consequently $E=Fe$ is total, without any assumption that $F$ reflects totality.

The source identity $he=d_\gamma e$ gives

\[
H E=sE,\qquad H=\chi_{X,X}^{-1}Fh:FX\to FX+FX.
\]

This uses composition preservation only. The source near-product equation was established before applying $F$; no product comparison for $F$ is needed.

Using the canonical squares and the fact that an isomorphism is total gives

\[
F\alpha=\overline{F(c_0)Fh}
=\overline{\chi_{X,X}P_0H}=\overline{P_0H}=H^*P_0,
\]

and similarly $F\beta=H^*P_1$. Contravariant composition of inverse images therefore gives the two displayed equalities

\[
E^*F\alpha=E^*\Gamma',\qquad E^*F\beta=E^*\Gamma.
\]

Monotonicity applied to $F\alpha\le\Gamma$ and $F\beta\le\Gamma'$ makes $E^*\Gamma$ and $E^*\Gamma'$ equal. Their meet is $E^*(\Gamma\Gamma')=E^*0_{FX}=0_{FX}$, so both are zero. Since $E$ is total, its inverse-image join law gives $1_{FX}=0_{FX}$, contradicting $F1_X\ne0_{FX}$. The proof is complete under the stated assumptions.

## Final scope conclusion

The new proofs establish the criterion without local connectedness. All old claims remain present; the pertinent statements are either preserved or stated with their local-connectedness hypothesis removed and their canonical coproduct comparison made explicit. No other mathematical dependency was found missing in the changed section. The small quantifier repair above is the only requested change from this scoped type check.
