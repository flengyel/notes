# Scoped source audit: Ranges and inseparability in recursion categories, version 1

Audited source: `output/local_connectedness_note_v1/Ranges_and_Inseparability_v1.tex`, against `tmp/move28/LOCOct10f.tex`. This is an author-side mathematical audit of the changed arguments and their affected uses. The full updated source was read for context. The review does not certify every unchanged assertion or the historical and bibliographic claims.

## (A) Kill-shots / hard blockers

No confirmed hard blocker in the changed mathematics. In particular, removing local connectedness from the hypotheses of `PropTotalCopMono`, `PropCopOut`, and `ThmRecIns` is supported by the replacement proofs. These proofs do not invoke connected domains or their join-density.

| Claim and source anchor | Typed interface and law checked | Evidence and status |
| --- | --- | --- |
| `PropTotalCopMono`, beginning “Let $\mathbf C$ be a restriction category with ranges” | $p=\nabla_X(\alpha+\beta):X+X\to X$; $\theta,\theta':Y\to X+X$ are total; $p\theta=p\theta'$ implies $(\alpha+\beta)\theta=(\alpha+\beta)\theta'$. | **Derivation.** The four domains $\delta_{ij}=(\theta^*\varepsilon_i)((\theta')^*\varepsilon_j)$ cover $Y$, by the stated inverse-image join law and domain-lattice distributivity. On each domain the two morphisms either have the same injection or both vanish because $\alpha\beta=0_X$. The explicitly parenthesized copairing $q:((Y+Y)+Y)+Y\to Y$ has range $1_Y$, so range agreement proves the conclusion. Pass. |
| `PropCopOut`, beginning “Let $\mathbf C$ be a split restriction category with ranges” | A section $f:X\to X+X$ of $p:X+X\to X$ satisfies $pf=\overline f=\operatorname{ran}(p)=\alpha\vee\beta$. | **Derivation.** `PropTotalCopMono` establishes the total-test premise of `PropPartialMono`; splitness extends it to arbitrary partial test morphisms. Weak choice supplies the section. R4 gives $\overline p f=f$, so partial monicity proves uniqueness. The range is precisely the previously defined join. Pass. |
| `PropDichotomy` | For complemented $\alpha\in\mathrm{Dom}(X)$, the unique section of $\nabla_X(\alpha^\perp+\alpha)$ is total and obeys $f\alpha=i_1\alpha$ and $f\alpha^\perp=i_0\alpha^\perp$. | **Derivation.** Totality follows from $\alpha\vee\alpha^\perp=1_X$ and the section equation. Partial monicity supplies both component equations. Pass. |
| `ThmRecIns`, lifting hypothesis and proof | $F:\mathbf C\to\mathbf D$ is a range functor; $\chi_{X,X}:FX+FX\to F(X+X)$; $d_\gamma:X\to X+X$ satisfies $Fd_\gamma=\chi_{X,X}s_\gamma$. | **Derivation.** For $h=bt\Delta_X$, the total weak-Turing index $e:X\to X$ gives $he=d_\gamma e$. Thus $H=\chi_{X,X}^{-1}Fh:FX\to FX+FX$ and total $E=Fe:FX\to FX$ satisfy $HE=s_\gamma E$. The summand-domain equations yield $E^*F\alpha=E^*F\gamma^\perp$ and $E^*F\beta=E^*F\gamma$. A separator forces the complementary inverse images to be equal and zero; the target join law and totality of $E$ contradict $1_X\notin\ker F$. No preservation of the near product by $F$, no reflection of totality, and no totality of $d_\gamma$ are used. Pass. |

The new proof uses the stated ranges, restriction zeros, restriction coproducts, inverse-image join law, splitness, weak choice, weak-Turing indexing, and nonzero hypothesis at the indicated steps. No additional extensivity or element-separation hypothesis was found.

## (B) Major weaknesses

No confirmed major weakness in the changed arguments or their affected uses.

The sufficient condition following `ThmRecIns` and `PropDisjointJoins` has the correct comparison isomorphism throughout. Given a total source conditional $d_\gamma:X\to X+X$, the source equation $p_\gamma d_\gamma=1_X$ follows by agreement on $\gamma$ and $\gamma^\perp$. Preservation of totality by $F$ and transport through $\chi_{X,X}$ make $\chi_{X,X}^{-1}Fd_\gamma$ a target section; its equality with $s_\gamma$ follows from the established uniqueness. The assertion does not confuse a right inverse alone with a section of a partial morphism.

The counterexample in `sec:counterexample` remains compatible with the strengthened theorem. The source permits partial maps with oracle-c.e. domains but ordinary partial-recursive extensions. Its complementary domains can separate the specified pair without supplying a total ordinary computable conditional. The target section selecting the nonrecursive set $A$ therefore has no source preimage. The comparison isomorphism is included in the revised lifting equation, and the faithful range-functor claim has its own construction. This checks the affected claim; it is not a new completeness audit of every original model construction.

## (C) Minor issues

No correction required by this source audit of the changed scope. The new arrows, summand maps, domain endomorphisms, four-way copairing, and coproduct comparison are explicitly typed. The symbol $\to$ follows the note's convention for morphisms in a category of partial maps; totality is asserted separately where needed.

## (D) Cross-section consistency failures

No confirmed consistency failure in the changed scope.

- The abstract and introduction now say that inverse images along every morphism preserve binary domain joins; this matches the revised target hypotheses.
- `PropKernel` and the connected-domain alternative remain independent statements. The revised section-construction and inseparability proofs do not use them, and do not silently retain local connectedness.
- The splitness and weak-choice assumptions remain in the section construction and are used there.
- $F(X+X)$ is related to $FX+FX$ by the declared $\chi_{X,X}$ throughout the revised theorem, sufficient condition, and counterexample. The types of $Fd_\gamma$, $s_\gamma$, and $H$ are consistent.
- The original and updated sources each contain 18 numbered theorem/proposition/lemma/corollary environments. The acknowledgments-and-bibliography suffix and the bibliography suffix are byte-for-byte identical between the sources. This verifies preservation of those source portions, not independent validity of their citations.

## (E) Acceptance conditions, non-negotiable

1. **Final-source endpoint:** preserve the explicit $\chi_{X,X}$ in the lifting hypothesis, target proof, sufficient condition, and counterexample, together with the stated target hypotheses and the nonzero condition. The audited revised source meets this endpoint. Dropping these conditions or changing the lift to an ill-typed equality would reopen the audit and block the present inference.
2. **Document endpoint:** compile and inspect the final version after all agents' edits, checking undefined references, displayed formulas, and metadata. This audit does not supply that production check. Any resulting error affecting a theorem statement or proof must be repaired before distribution; a production error alone is not a mathematical rejection.

No mathematical reconstruction is required by this review of the changed scope.

## (F) Not checked / uncertainty log

- No independent verification of the cited literature, historical priority, or original bibliographic metadata was performed. No novelty conclusion is made.
- The unchanged propositions, including the complement/quasicomplement equivalence, were read in context but were not all independently reproved. No confirmed fatal defect in them was established here.
- No Lean formalization, machine proof, or new countermodel search was performed. The review checked the stated restriction-category and range equations directly.
- The original TeX and PDF archival identity and repository publication were outside this mathematical audit. Compilation and rendered-layout inspection are assigned to the parent workflow.

Strongest confirmed blocker: **none in the changed scope**. Strongest suspected but unconfirmed blocker: **none supported by the reviewed text**. Most important thing not checked: **independent verification of the unchanged results and literature on which the complete note relies**. Dependence on unavailable material: **the scoped mathematical conclusion uses the supplied source and does not depend on missing material; a whole-note scholarly verdict would require source verification**. Final recommendation: **unknown for a whole-note acceptance decision; the revised proofs and their affected interfaces pass this scoped source audit without a required mathematical correction**.
