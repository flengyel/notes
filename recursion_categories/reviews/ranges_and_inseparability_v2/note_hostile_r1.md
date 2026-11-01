# Author-side hostile audit of the revised standalone note

Source: *Ranges and inseparability in recursion categories*, version 1, 1 November 2026, 13 pages. The complete TeX source was read, together with the revision diff from \`LOCOct10f\`. Anchors below refer to \`output/local_connectedness_note_v1/Ranges_and_Inseparability_v1.tex\`; result numbers and pages were obtained from its current auxiliary file. This is a mathematical and exposition audit, not independent verification of the cited literature.

## (A) Kill-shots / hard blockers

No confirmed hard blocker. In particular, the revised proofs justify removal of local connectedness from Proposition 4.0.4, Proposition 4.0.5 and Theorem 4.1 under the stated inverse-image binary-join hypothesis. The source retains splitness and weak choice, and uses both in the section construction.

The principal typed checks are these.

| Claim and anchor | Typed data, hypotheses and inference checked | Status |
| --- | --- | --- |
| Proposition 4.0.3, p. 8, lines 641–660 | \(f:X\to Y\); the total test ranges over every object \(W\) and total \(g,h:W\to X\). Splitting \(\overline{fg}=\overline{fh}=me\) produces total \(gm,hm:Z\to X\). The total-test equality can then be postcomposed with \(e:W\to Z\). | The displayed restriction calculation proves the arbitrary-partial-test condition. Splitness is used, rather than silently assumed away. |
| Proposition 4.0.4, pp. 8–9, lines 663–731 | \(p=\nabla_X(\alpha+\beta):X+X\to X\); total \(\theta,\theta':Y\to X+X\); \(\alpha\beta=0_X\). The four domains \(\delta_{ij}=(\theta^*\varepsilon_i)((\theta')^*\varepsilon_j)\) join to \(1_Y\). | On each piece, same summands give equal restrictions of \(\alpha+\beta\); opposite summands give zero by \(\alpha\beta=0_X\). The explicitly parenthesized \(q:((Y+Y)+Y)+Y\to Y\) has range \(1_Y\), so the defining equality property of range finishes the proof. No connected probe or extensivity is used. |
| Proposition 4.0.5, p. 9, lines 733–750 | The previous two propositions make \(p\) a partial monomorphism. Weak choice supplies \(f:X\to X+X\) with \(pf=\overline f=\operatorname{ran}(p)=\alpha\vee\beta\). | R4 gives \(\overline p f=f\). Partial monicity then proves uniqueness for two sections with the same composite \(pf\). |
| Proposition 4.0.6, p. 9, lines 752–764 | For complemented \(\alpha\), the section of \(\nabla_X(\alpha^\perp+\alpha)\) is total and has the asserted equations on \(\alpha,\alpha^\perp\). | The section equations give totality; partial monicity gives the two injection equations. |
| Theorem 4.1, pp. 9–10, lines 773–851 | \(F:\mathbf C\to\mathbf D\); \(\chi:FX+FX\to F(X+X)\); the lift is \(Fd_\gamma=\chi s_\gamma\). The total weak-Turing index \(e:X\to X\) gives \(he=d_\gamma e\), hence \(HE=s_\gamma E\) for \(H=\chi^{-1}Fh\) and \(E=Fe\). | The source and target summand endomorphisms are transported through \(\chi\). A separator forces \(E^*F\gamma\) and \(E^*F\gamma^\perp\) to be equal, then zero; totality of \(E\) and the target join law force \(1_{FX}=0_{FX}\). The nonkernel assumption supplies the contradiction. The proof does not require \(F\) to preserve the near product or reflect totality. |
| Proposition 4.1.1, p. 10, lines 867–894 | The join \(d_\gamma=(i_1\gamma)\vee(i_0\gamma^\perp):X\to X+X\) has restriction at least \(\gamma\vee\gamma^\perp=1_X\). | The upper-bound equations give the two restrictions; totality and range agreement give a source section. Applying \(F\), transporting by \(\chi\), and target uniqueness yield the stated lift. |
| Proposition 4.1.2, pp. 11–12, lines 928–1011 | Morphisms in \(\mathbf C_K\) have \(K\)-c.e. domains and ordinary partial-recursive extensions. Total morphisms are therefore ordinary total recursive functions. | Composition, coproducts, ranges and the parameterized Turing morphism remain in that class. The separator \(A\) is \(K\)-decidable but nonrecursive, so its target conditional has no source preimage. The two restricted injections belong to the source but have no common upper bound. |

The unchanged numbered claims were also checked directly at the level indicated below; this supplies a check of their role in the revised arguments, without substituting for source verification of historical attributions.

| Claim | Direct check |
| --- | --- |
| Proposition 2.0.1 | With \(Y=X\times X\), the given \(t=a^{-1}\tau(q_1\times a):Y\times Y\to Y\) is Turing by parameterization. \(N(e)=\langle q_0,kq_0\rangle\) is total and idempotent; precomposition with \((\Delta_Xq_0)\times1_Y\) verifies its index equation. |
| Proposition 3.0.1 | Domains commute; \(\beta\le\gamma\) and \(\beta\phi=\phi\) give \(\gamma\phi=\phi\). |
| Proposition 3.0.2 | Least receiving domains and the equality property of \(\operatorname{ran}\varphi\) give both inequalities in \(\operatorname{ran}(\varepsilon\varphi)=\varepsilon\operatorname{ran}\varphi\). |
| Proposition 3.0.3 | R1 gives one direction. In the other, \(\overline{\psi\varphi}=0\) implies \(\overline\psi\varphi=0\), and taking ranges gives the conclusion. |
| Proposition 3.0.4 | R4 identifies \(\phi\alpha\phi^*\beta\) with \(\beta\phi\alpha\); taking ranges gives the formula. |
| Propositions 3.0.5–3.0.6 | The displayed restriction calculation proves (a). If \(\alpha\le\phi^*\beta\), the image formula gives \(\phi_*\alpha=\beta\phi_*\alpha\), proving (b). For total \(\phi\), (a) gives the missing implication for adjunction. |
| Theorem 3.1 | The total index of a proposed complement equates its inverse image with the inverse image of the diagonal domain. The common domain has meet zero and join identity, contradicting \(1_X\ne0_X\). |
| Proposition 3.2, equivalence (i)–(iii) | A nontotal domain which is weakly total contradicts (i); the range of a nonzero annihilated morphism supplies the nonzero disjoint domain in (ii). A disjoint quasicomplementary pair has weakly total join; conversely zero is a quasicomplement of a weakly total domain. These yield the equivalence. The manuscript cites the source results rather than displaying this proof. |
| Proposition 4.0.1 | Adjointness, the inverse-image join law, distributivity and the image formula show that a decomposition of \(f_*\alpha\) induces a decomposition of \(\alpha\). One component vanishes. The coproduct alternatives follow from the complementary summand domains. |
| Proposition 4.0.2 | If zero is the only connected domain on \(FX\), local connectedness identifies \(1_{FX}\) with zero, contradicting \(1_X\notin\ker F\). |

No claim of minimal hypotheses is made. Retaining splitness is compatible with the proof; this audit does not propose a stronger theorem by deleting it.

## (B) Major weaknesses

No confirmed major weakness in the revised argument. The central theorem's target, nonzero and lifting assumptions are stated and used. The counterexample does not contradict the theorem: it fails precisely the lifting assumption.

The literature attributions and broad representation claims in Sections 1–3 have not been independently checked against the cited primary sources. They are therefore unverified by this audit, not confirmed flaws.

## (C) Minor issues

### C1. Unspecified quantified morphism types in two definitions

- **Anchors:** p. 5, §3.1, lines 369–377, especially “for all appropriate \(\psi,\psi'\)”; p. 8, §4.3, lines 634–635, “for all morphisms \(\theta,\theta'\)”.
- **Claim as written:** the range equality property and the definition of a partial monomorphism quantify morphisms without declaring their common source or target.
- **Failure mode:** ambiguous; explicit typing omitted.
- **Evidence:** absence_in_text. The equations determine the intended types, but the quantifiers are suppressed precisely where the definitions establish them.
- **Impact and severity:** minor exposition defect; no ill-typed equation or false result established.
- **Repairability:** local.
- **Recommended replacements:** “for every object \(Z\) and all parallel morphisms \(\psi,\psi':Y\to Z\)” in the range definition; “for every object \(W\) and all morphisms \(\theta,\theta':W\to X\)” in the partial-monomorphism definition.

### C2. Domain and codomain of the domain operations are suppressed

- **Anchor:** p. 6, lines 448–450, “define its inverse image and image on domains by”.
- **Claim as written:** \(f^*\beta=\overline{\beta f}\) and \(f_*\alpha=\operatorname{ran}(f\alpha)\), for \(f:X\to Y\).
- **Failure mode:** ambiguous; declared signatures omitted.
- **Evidence:** absence_in_text. The signatures are inferable from composition, but the definition does not state them.
- **Impact and severity:** minor typing exposition.
- **Repairability:** local.
- **Recommended replacement:** “For a morphism \(f:X\to Y\), define
  \[
  f^*:\mathrm{Dom}(Y)\to\mathrm{Dom}(X),\quad
  f_*:\mathrm{Dom}(X)\to\mathrm{Dom}(Y)
  \]
  by \(f^*\beta=\overline{\beta f}\) and \(f_*\alpha=\operatorname{ran}(f\alpha)\).”
  These are functions between the indicated domain posets, not additional morphisms of \(\mathbf C\).

### C3. “Range agreement” is an undeclared name for an already defined property

- **Anchors:** p. 9, line 729, “Range agreement therefore gives”; p. 10, line 807, “range agreement gives”.
- **Claim as written:** these phrases invoke the equality property in the definition of range.
- **Failure mode:** ambiguous terminology.
- **Evidence:** absence_in_text and derivation. No separate property called “range agreement” is defined; both deductions are valid applications of the range definition.
- **Impact and severity:** minor terminology defect, with no mathematical failure.
- **Repairability:** replace the phrase at both occurrences by “the defining equality property of the range”. No new definition is needed.

### C4. The operation on indices is not typed in its statement

- **Anchor:** p. 4, Proposition 2.0.1, lines 334–338, “a mapping \(N\)”.
- **Claim as written:** \(N(e)\) is an idempotent index whenever \(e\) is an index.
- **Failure mode:** missing_definition at the level of the signature.
- **Evidence:** absence_in_text. The proof constructs \(t:Y\times Y\to Y\) and a function on total endomorphisms \(Y\to Y\), but the statement does not name \(Y\) or the domain and codomain of \(N\).
- **Impact and severity:** minor explicit-typing defect. The construction is valid; the statement should distinguish the external function \(N\) from a morphism in \(\mathbf C\).
- **Repairability:** replace the opening with “Every \(P\)-recursion category \(\mathbf C\) has an object \(Y\), an idempotent weak Turing morphism \(t:Y\times Y\to Y\), and a function \(N:\mathbf C_T(Y,Y)\to\mathbf C_T(Y,Y)\) such that ...”, and quantify \(\varphi:Y\to Y\). The proof already defines this \(N\) for all total endomorphisms.

### C5. The theorem counters produce unintended-looking nested numbers

- **Anchor:** source lines 17–32 and rendered propositions 2.0.1, 3.0.1, 4.0.1 and 4.1.1.
- **Claim as written:** this is a presentation issue rather than a mathematical claim.
- **Failure mode:** inconsistent_use of numbering conventions, if shared numbering was intended.
- **Evidence:** structural_argument. The declaration \(\backslash\mathrm{newtheorem}\{prop\}\{Proposition\}[thm]\) resets a separate proposition counter at each theorem, rather than sharing the theorem counter.
- **Impact and severity:** optional minor typographical repair; no mathematical content affected.
- **Repairability:** if unified numbering is intended, use \(\backslash\mathrm{newtheorem}\{prop\}[thm]\{Proposition\}\), and the corresponding form for the other environments. This is a house-formatting choice, not an acceptance blocker.

No empty reassurance paragraph, editorial-process statement, or substantive invented mathematical construction was found in the revised passages. “Restriction domain”, “near product”, “partial monomorphism”, “section” and “weak choice” are explicitly defined before their revised uses. The zero domain is deliberately allowed to be connected; this convention is stated rather than silently imported.

## (D) Cross-section consistency failures

No confirmed cross-section mathematical inconsistency.

- Local connectedness remains in the independent connected-domain statements, but is absent from the revised section and inseparability arguments.
- The source and target coproducts are consistently related through the explicit isomorphism \(\chi_{X,X}\).
- The theorem does not demand a total source lift \(d_\gamma\); the weak Turing property indexes its possibly partial composite \(b^{-1}d_\gamma\). Target totality is supplied by \(s_\gamma\), and totality of \(E=Fe\) follows from the total index \(e\).
- Complemented domains in the counterexample need not have recursive membership. This is compatible with the source having only ordinary recursive total morphisms, and is precisely why the conditional lift can fail.
- The unchanged near-product and range definitions support the computations actually used in the revision.

## (E) Acceptance conditions, non-negotiable

1. **Definition endpoint:** declare the quantified morphism types in C1 and the domain-operation signatures in C2. This is required by the current explicit-typing standard. Failure leaves an exposition defect, not a demonstrated false theorem; no mathematical claim needs to be dropped.
2. **Terminology endpoint:** replace the two undeclared “range agreement” invocations by the defining property they use. No proof reconstruction is needed.
3. **Index-operation endpoint:** type \(t\), \(\varphi\), and the external function \(N\) in Proposition 2.0.1 as in C4. This prevents an avoidable internal/external ambiguity. Failure does not supply a counterexample to the proposition.
4. **Final-source endpoint:** retain the explicit coproduct comparison, nonkernel condition, total-index quantifier, splitness reduction and stated target inverse-image join law. Their deletion would reopen the central proof; the current source meets this endpoint.
5. **Production endpoint:** compile and inspect the exact final source after changes. This audit did not perform that build or visual-layout pass.

C5 is optional and does not belong to the acceptance gate.

## (F) Not checked / uncertainty log

The complete note was read. The revised four-piece, splitness, section, conditional, comparison, disjoint-join and counterexample arguments were checked directly. All 18 numbered claims were traced as listed in A.

The cited primary sources, their page numbers, historical attributions, and quotations were not independently verified. The representation theorem, the assertion about \(S_T\)'s connected domains, and the Rosolini/Montagna comparison therefore have the status of source dependencies, not independently reproduced results of this audit. No novelty claim is certified. No Lean formalization or exhaustive countermodel search was run. No build or rendered-layout inspection was performed by this agent.

Strongest confirmed blocker: **none**; the strongest confirmed correction is the suppressed typing in C1–C2 and C4. Strongest suspected unconfirmed blocker: **none supported by the supplied proof text**. Most important unchecked material: **the external source claims underlying the contextual and historical comparisons**. The revised proof assessment does not depend on unavailable material; a full scholarly acceptance verdict does. Final recommendation: **unknown for full-note acceptance; no mathematical reconstruction is required by this audit, and the local explicit-typing and terminology repairs above should be made.**

