# Mathematical-writing review of the revised note

The note needs local repairs to explicit typing, one compressed parameter construction, and theorem numbering. Its section proposition and inseparability proof explain their central categorical steps; shortening those proofs would remove useful mathematics. No change of outline is recommended.

Reviewed: *Ranges and inseparability in recursion categories*, version 1, 1 November 2026, complete source `output/local_connectedness_note_v1/Ranges_and_Inseparability_v1.tex`, lines 1–1065. PDF pages below are physical pages of the 13-page note. This is an editorial review, not a correctness or novelty certification. No source edits were made.

## Actual outline and dependencies

| Existing section | Mathematical function and results | Dependencies |
|---|---|---|
| Abstract | States noncomplementation, comparison theorem, sufficient lift condition, and counterexample. | Results of §§3–4. |
| 1. Introduction | Explains the two domain problems and the role of a range functor; compares syntactic categories and locally connected examples; gives roadmap. | Cited Di Paola–Heller, Rosolini, Montagna, Di Paola–Montagna, Heller, Lengyel. |
| 2.1 Restriction categories | Defines restriction, domains, order, zeros, splitness, and coproducts. | Restriction axioms. |
| 2.2 P-categories | Defines near product and its coherences, induced restriction, prodominical and dominical categories, isotypicality. | §2.1; cited representation results. |
| 2.3 Turing morphisms and P-recursion categories | Defines parameterization and weak Turing indices, proves diagonal index identity, constructs idempotent indices. | Near product, total maps, isotypicality. |
| 3.1 Ranges | Defines range by receiving and equality properties; proves range restriction, join calculus, image/inverse-image identity and adjunction. | §2.1, ranges, coproducts. |
| 3.2 A domain with no complement | Proves diagonal noncomplementation; relates complements and quasicomplements; discusses the scope of a representation claim. | Weak Turing index identity; inverse-image lattice operations; cited comparison claims. |
| 4.1 Connected domains | Defines connectedness/local connectedness; proves direct-image connectedness and coproduct alternatives. | Distributive domains, adjunction, inverse-image binary joins. |
| 4.2 Range functors | Defines preserved data, coproduct comparison and kernel; proves existence of a nonzero connected target domain under local connectedness. | §4.1. |
| 4.3 Sections and weak choice | Defines section/partial monomorphism/weak choice; reduces partial tests to total tests under splitness; proves the four-piece coproduct test, uniqueness of sections, and conditional equations. | Splitness, weak choice, ranges, global inverse-image binary joins. |
| 4.4 The inseparability theorem | States and proves lifted-target conditional comparison; gives two sufficient lift conditions and disjoint-morphism-join proposition. | Weak Turing identity; range functor; §4.3. Local connectedness is not used here. |
| 4.5 Failure of the lifting hypothesis | Constructs the category C_K, verifies its structure and Turing morphism, exhibits a separable diagonal pair and a target section without lift, and proves failure of disjoint morphism upper bounds. | Program parameterization and oracle enumeration; categorical definitions of §§2–4. |
| Acknowledgments and references | Attribution and literature dependencies. | Existing author-supplied acknowledgments. |

## Comparison with Mathematical Writing

Consulted the supplied `tmp/review_sources/klr.pdf` / `klr.txt`: §1, printed pp. 1–6 (PDF pp. 3–8), and §§4–5, printed pp. 9–13 (PDF pp. 11–15). Verified §1 point 5 on self-contained theorem statements; points 10–11 on connected explanations and defining variables; point 13 on prose readable while formulas are skimmed; points 14–15 on consistent notation; point 17 on sentences readable from left to right; and point 26 on unnecessary jargon. §§4–5 explicitly qualify definition placement and support useful proof signposts. The review therefore does not delete transitions merely because they are transitions. The exact-counter, explicit-hom-type, and user-preferred vocabulary recommendations below are editorial judgments, not claimed rules of Knuth–Larrabee–Roberts.

| Anchor | Actual difficulty | Basis | Recommended action |
|---|---|---|---|
| Preamble, lines 17–34; visible e.g. PDF p. 8, Propositions 4.0.3–4.0.4 | `\newtheorem{prop}{Proposition}[thm]` creates a separate proposition counter reset by the theorem counter. The result is numbering such as 3.0.6, 3.1.1, 4.0.4 and 4.1.1 in a note otherwise numbered by section. These look like subsection references but do not match the subsections. | Independent typographic/navigation judgment; §1 point 14 supports consistency. | Share the theorem counter: `\newtheorem{prop}[thm]{Proposition}` and likewise for other theorem-like environments. Keep labels. |
| Proposition `IdempotentTheorem`, PDF p. 4, lines 334–338 | The statement names `t`, `N`, `e`, and `\varphi` without declaring the object on which they act or the class on which N is an assignment. The proof supplies the missing types later. | §1 points 5 and 11; explicit-typing convention. | State an object Y, `t:Y\times Y\to Y`, and N as an assignment on total endomorphisms of Y. See replacement below. |
| Same proof, lines 344–348 | “duplicate the resulting parameter map” omits the map and the identity proving it has the required parameterization. This is the one substantive construction compressed into a verbal instruction. | §1 points 10–11; independent requirement to expose a proof-bearing construction. | Name the total parameter map c and give `\Delta_Xc:V\to Y` and the equation below. |
| Range definition, PDF p. 5, lines 369–377 | “for all appropriate ψ,ψ′” leaves the common source, target, and quantification over the target unstated in the defining equality property. | §1 point 11; explicit-typing convention. | Quantify over every object Z and all `\psi,\psi':Y\to Z`. |
| Image/inverse-image definition, PDF pp. 5–6, lines 448–450 | The formulas determine the types, but the two ordered maps that are subsequently called adjoint are never given typed signatures. | Independent explicit-typing convention, compatible with §1 point 11. | Give `f^*:\mathrm{Dom}(Y)\to\mathrm{Dom}(X)` and `f_*:\mathrm{Dom}(X)\to\mathrm{Dom}(Y)` in the definition. |
| Partial monomorphism definition, PDF p. 8, lines 634–635 | “for all morphisms θ,θ′” omits the common source and common target. | §1 point 11; explicit-typing convention. | Quantify over every object Z and all `\theta,\theta':Z\to X`. |
| Four-piece proof, PDF p. 9, lines 726–730; inseparability proof, lines 805–808 | “Range agreement” is not introduced as a term. Its meaning can be recovered, but it abbreviates the defining equality property exactly where that property proves an inference. | §1 points 11 and 26; independent vocabulary judgment. | Refer to the defining equality property of the stated range. Keep the copairing and its range computation. |
| Lines 433, 467–468 | The first sentence announces an immediately adjacent proposition without identifying the implication; the second repeats the entire conclusion of the next proposition. | Skill's independent economy requirement; not a demand to eliminate all signposts. | Delete line 433. Delete lines 467–468 and attach the existing citation to the proposition statement. Keep line 476, which explains why the following proposition proves adjointness. |
| Proposition `PropImageFact`, line 458 | “Let ... and let ... , then” joins a declaration to a conclusion with a comma. | §1 point 17. | End the declaration with a period, then write “Then ...”. |
| Connected-domain introduction, line 551 | “a surrogate ... for points” is motivational but does not say which property of points is used. The next sentences already define the property. | §1 point 26; independent terminology judgment. | Use the attribution alone: “Connected domains were introduced in ... and used in ... .” Do not add a new name for them. |

## Definition order and terminology

Confirmed, adequately introduced in reading order: restriction/totality/order/zeros/splitness before their proofs; coproduct injections and copairing before conditional constructions; near product and pairing before Turing morphisms; weak Turing index before the diagonal equation; range before domain joins; image/inverse image before adjunction; complement and quasicomplement before their comparison; connectedness before local connectedness; range functor and its coproduct comparison before the main theorem; section and weak choice before the existence proof; lifting hypothesis inside the theorem; recursive separability before the conclusion; graph equality and recursive object codings before the counterexample verification.

The note does not use “genuine,” “actual,” “structural,” “obvious,” “clearly,” or “standard” to evade justification. “Classical” occurs only in Odifreddi's book title and should remain. “Receives” and “t-index” have explicit mathematical definitions and uses; their specialized meanings are not defects merely because they are local terminology. “Section” is explicitly defined in the partial-map sense; no silent replacement by the total-category meaning is warranted. “Preimage under F” is disambiguated by the typed hom-map and explicit equality in the lifting hypothesis.

The category of the object X is fixed in the principal statements. The remaining open type placeholders are those identified above; the main conditional and four-piece proof already name the types of their constructed morphisms.

## Paragraph-purpose pass

The complete prose was read, including comments, abstract, acknowledgments, and bibliography. The blocks have these functions: lines 59–70 summarize results; 77–131 introduce the problem, compare sources, and give roadmap; 136–358 define the categorical data and prove parameter constructions; 362–493 define ranges and prove their calculus; 497–539 state/prove noncomplementation and compare a cited representation claim; 543–626 define inseparability/connectedness/range functors and prove their consequences; 628–764 define sections and prove the conditional construction; 767–894 position, state, prove and supply sufficient hypotheses for inseparability; 897–1011 construct and verify the counterexample; 1014–1064 give attribution and references. Within these blocks only the adjacent announcements/repetition at lines 433 and 467–468 lack an additional mathematical function. The explicit hypothesis distinctions, domain equations, and counterexample limitations should remain.

## Exact consequential replacements

### 1. State the index assignment with its types

Replace the statement at lines 334–338 by:

```latex
Every $P$-recursion category $\mathbf C$ contains an object $Y$ and an
idempotent weak Turing morphism $t:Y\times Y\to Y$. For this choice of
$t$, there is an assignment $e\mapsto N(e)$ on total endomorphisms of
$Y$ such that $N(e):Y\to Y$ is an idempotent $t$-index of
$\varphi:Y\to Y$ whenever $e$ is a $t$-index of $\varphi$.
```

This keeps N an external assignment, as in the existing statement; it does not assert that N is a morphism of C.

### 2. Give the duplicated parameter map

Replace the last part of lines 344–348, after “given”, with:

```latex
$f:V\times Y\to Y$, choose a total morphism $c:V\to X$ such that
\[
 \tau(c\times1_X)=af(1_V\times a^{-1}).
\]
Then $g=\Delta_Xc:V\to Y$ is total, $q_1g=c$, and
\[
 t(g\times1_Y)=a^{-1}\tau(c\times a)=f.
\]
```

The unchanged beginning of the sentence introduces `t=a^{-1}\tau(q_1\times a)`; the replacement exposes the parameter morphism and its universal-property equation.

### 3. Type the range equality property

Replace lines 372–377 by:

```latex
Suppose that $\varepsilon$ receives $\phi$ and that, for every object
$Z$ and all morphisms $\psi,\psi':Y\to Z$, the equality
$\psi\phi=\psi'\phi$ implies
$\psi\varepsilon=\psi'\varepsilon$. Then $\varepsilon$ is the least
domain in $\mathrm{Dom}(Y)$ receiving $\phi$. We call $\varepsilon$
the range of $\phi$ and write $\mathrm{ran}\phi=\varepsilon$.
```

### 4. Type the lattice maps and partial-monomorphism test

For lines 448–450:

```latex
For a morphism $f:X\to Y$, define its inverse image
$f^*:\mathrm{Dom}(Y)\to\mathrm{Dom}(X)$ and image
$f_*:\mathrm{Dom}(X)\to\mathrm{Dom}(Y)$ by
$f^*\beta=\rst{\beta f}$ and $f_*\alpha=\mathrm{ran}(f\alpha)$.
```

For the definition at lines 634–635:

```latex
A morphism $\phi:X\to Y$ is a \textit{partial monomorphism} if, for
every object $Z$ and all morphisms $\theta,\theta':Z\to X$, the
equality $\phi\theta=\phi\theta'$ implies
$\rst\phi\,\theta=\rst\phi\,\theta'$.
```

### 5. Refer to the range property by its mathematical content

At lines 729–730:

```latex
The defining equality property of $\mathrm{ran}(q)=1_Y$ therefore gives
$(\alpha+\beta)\theta=(\alpha+\beta)\theta'$.
```

At lines 805–808 retain the agreement after both complementary domains and the equation `\mathrm{ran}[\Gamma,\Gamma']=1_{FX}`, then replace “range agreement gives” by “the defining equality property of this range gives”.

## Scope and retained uncertainty

Read all 1065 source lines and extracted text of the 13-page PDF; visually inspected PDF p. 8, including the four-piece proof's opening and the anomalous proposition numbering. I did not compile a changed source, because this task assigned review without edits. I did not independently reverify cited representation, equivalence, and literature-priority claims against their primary mathematical sources; no source claim is labeled false or novel on that basis. The hostile reviewer is checking mathematical validity independently. No further literature additions or section reorganization are justified by this prose review.
