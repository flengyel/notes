# Mathematical Writing review of the revised separate note

The revised note, *Ranges and inseparability in recursion categories*, Version 1, 1 November 2026, needs no further writing repair in the changed arguments reviewed here. The four-piece proof states its intermediate morphisms, explains why the four domain pieces suffice, and invokes the defining equality property of the range at the final step. The inseparability proof keeps the source and target coproducts separate through the canonical comparison isomorphism. Its target join hypothesis is stated with the same scope in the abstract, introduction and mathematical statements.

This review applies the supplied Mathematical Writing skill and the actual Knuth–Larrabee–Roberts text in `tmp/review_sources/klr.txt`. In particular, §1, points 5, 10–15 and 26 supply the checks on self-contained statements, connected exposition, definitions at first use, notation and unnecessary jargon. Explicit categorical typing and the prohibition on process commentary are additional requirements of the skill and the author's instructions, not quotations from KLR.

## Current outline and mathematical functions

1. **Introduction.** States the two diagonal results, identifies the range-functor and lifting hypotheses, describes the counterexample, and supplies the historical motivation and roadmap.
2. **Restriction categories and recursion categories.** Supplies the structures used by the later claims.
   - **Restriction categories:** restriction axioms, domains, totality, restriction order and joins, zeros, splitness, restriction coproducts and codiagonals.
   - **P-categories:** near products, the diagonal, projections, associativity and symmetry data, and their relation to restrictions.
   - **Turing morphisms and P-recursion categories:** universal computation, weak Turing morphisms, total indices and the idempotent-index proposition.
3. **Ranges and the diagonal domain.** Supplies range calculations and proves noncomplementation.
   - **Ranges:** receiving domains, ranges, domain joins and distributivity, image and inverse image, the projection formula, and adjointness statements.
   - **A domain with no complement:** the diagonal noncomplementation theorem, quasicomplements, and the comparison with the earlier dominical statements.
4. **Recursively inseparable domains.** Defines separability and proves the range-functor criterion and its limitation.
   - **Connected domains:** records direct-image and coproduct alternatives for connected domains. These remain independent results; the revised section construction does not invoke them.
   - **Range functors:** defines the functors, the canonical comparison and the kernel; records the consequence of local connectedness.
   - **Sections and weak choice:** defines partial monomorphisms and sections, proves the total-test reduction, proves the four-piece comparison proposition, obtains a unique section using weak choice, and obtains its two restrictions on complementary domains.
   - **The inseparability theorem:** states and proves the lifting criterion; then gives the conditional and disjoint-domain-join sufficient conditions.
   - **Failure of the lifting hypothesis:** constructs the computability-theoretic counterexample, verifies its categorical structures, and exhibits both the missing lift and the failure of a common upper bound for two disjoint-domain morphisms.
5. **Acknowledgements and bibliography.** Preserved contextual and source material.

The principal changed dependency is now: the four-piece comparison proposition and the split-category total-test proposition imply partial monicity; weak choice then gives the unique section; its restrictions and the explicit lift feed the diagonal proof. No connected-domain argument is hidden in this chain.

## Comparison with the governing source and task requirements

| Passage | Assessment | Source principle or editorial rationale | Action |
| --- | --- | --- | --- |
| Abstract and introduction | The target hypothesis says that inverse images along every morphism preserve binary joins. The lifting requirement and its sufficient condition remain visible. | KLR §1.5, 12–13: state the scope and orient the reader before technical detail. | Retain. |
| `PropTotalCopMono` | Introduces the summand domains, four intersections and component morphisms before their use. The disjoint-tag case explicitly becomes zero. The final copairing has a parenthesized source. | KLR §1.10–11, 14–15, plus the explicit-typing requirement. | Retain. |
| `PropCopOut` and `PropDichotomy` | Explain the separate uses of splitness, partial monicity and weak choice. The section equations and the complementary restrictions are retained. | KLR §1.10–11; substantive qualifications must survive any economy. | Retain. |
| `ThmRecIns` | Separates target injections from source injections; defines `H` and `E` with types; writes the identities connecting `χ` with the summand domains; derives the contradiction using totality and the join law. | KLR §1.5, 10–11, 14; explicit categorical typing. | Retain. |
| Lifting sufficient conditions and counterexample opening | The equation is consistently `Fd_γ=χ_{X,X}s_γ`. No implicit identification of the two coproduct objects is required. | KLR §1.14 and the distinction between equality and chosen isomorphism. | Retain. |
| Terminology and commentary in the changed text | No invented technical label, empty adjective, proof-audit narration or editorial instruction was found. | KLR §1.26; independent prohibition on process commentary. | No repair required. |

## Definition order and notation

- Composition is fixed at the beginning of §2: `gf` applies `f` first. Restrictions, domains, totality, the restriction order, joins, zeros and restriction coproducts precede their later use.
- The note uses `→` for a morphism in a restriction category and states totality separately. This convention is consistent; replacing every such arrow with a partial-function symbol would add a different convention without resolving a defect.
- Receiving a morphism and the equality property of a range are defined in §3. The later expressions “range agreement” refer to that displayed implication, not to an additional undeclared construction.
- Connected domains and local connectedness are defined before their two retained propositions. Their omission from the revised section and inseparability hypotheses is reflected in the proofs.
- The canonical isomorphism `χ_{X,Y}:FX+FY→F(X+Y)` is declared before the lifting hypothesis. The source lift has type `d_γ:X→X+X`; the target section has type `s_γ:FX→FX+FX`; their comparison has the correct common codomain after composition with `χ`.
- In the four-piece proof, `e_i`, `f_j` and `δ_ij` are explicitly declared to be domains on `Y`; `Γ`, `Γ′` and `P_0`, `P_1` are explicitly domains on `FX` and `FX+FX`. These declarations specify their endomorphism types. The auxiliary morphisms `x_ij`, `y_ij`, `z_ij` and `q` have displayed types.
- The parentheses in `((Y+Y)+Y)+Y` match the iterated copairing. Its range, rather than its totality, is asserted to be `1_Y`, which is the property required for the final equality.
- The computability counterexample uses underlying sets and functions as the concrete definition of its category. This is a representation of a categorical example, and the note states which categorical structures those data define.

No revised outline or prioritized replacement text is warranted: the current order retains the proof dependencies and the changed passages do not require a local repair. In particular, there is no recommendation to compress the four-piece construction or the comparison calculation.

## Scope

I read the entire revised LaTeX source for context and compared the changed passages with `tmp/move28/note_revision.diff` and the original `LOCOct10f.tex`. The detailed review concerns the changed abstract and introduction, the four-piece and unique-section arguments, the revised diagonal argument, and the comparison equations in the sufficient conditions and counterexample opening. This is a mathematical-writing review, not a certification of every retained theorem, historical attribution, novelty claim or future Lean formalization. I did not compile or render the note, did not reverify the primary literature, and did not edit its source or the archived original.
