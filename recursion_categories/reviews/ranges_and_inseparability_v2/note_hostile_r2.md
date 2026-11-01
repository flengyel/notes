# Scoped recheck of the note repairs

Source: *Ranges and inseparability in recursion categories*, version 2, against \`tmp/review29/note_repairs.diff\`. Only the changed passages and the equations needed to check their interfaces were rechecked.

## (A) Kill-shots / hard blockers

None confirmed. The repairs preserve the theorem statements' hypotheses and conclusions.

## (B) Major weaknesses

None confirmed in the repair scope.

The typed operation
\[
N:\mathbf C_T(Y,Y)\longrightarrow\mathbf C_T(Y,Y)
\]
is supported by the proof for every total endomorphism \(e:Y\to Y\). Both \(k=q_1e\Delta_X:X\to X\) and \(N(e)=\langle q_0,kq_0\rangle:Y\to Y\) are total. The index-preservation argument is asserted only when \(e\) indexes the specified \(\varphi:Y\to Y\).

The expanded Turing-morphism argument is composable. The parameterization equation has source \(V\times X\) and target \(X\). With \(g=\Delta_Xc:V\to Y\), \(q_1g=c\), and
\[
t(g\times1_Y)=a^{-1}\tau(c\times a):V\times Y\to Y.
\]
Precomposing the parameterization equation with \(1_V\times a\) proves the asserted equality to \(f\). No additional hypothesis is used.

## (C) Minor issues

One introduced grammatical defect was identified and corrected during this recheck.

- **Anchor:** \`PropCopOut\`, source lines 743–744.
- **Claim as written:** “For every object \(X\) and all \(\alpha,\beta\in\mathrm{Dom}(X)\) with \(\alpha\beta=0_X\), then \(p=\cdots\) has a unique section”.
- **Failure mode:** ambiguous grammatical construction; no mathematical failure.
- **Evidence:** absence_in_text / direct reading. “For every ... with ...” does not take the following “then”.
- **Impact:** local minor prose defect only.
- **Repair:** the exact current source now reads “For every object \(X\) and all ... with ..., the morphism \(p=\cdots\) has a unique section”. This removes “then” and preserves the quantifiers, all hypotheses and the conclusion. **Closed.**

All first-round typing and terminology findings are closed. No further optional polish is proposed.

## (D) Cross-section consistency failures

None confirmed in the repair scope.

The quantified morphisms in the range and partial-monomorphism definitions now have the required common types. The functions \(f^*\) and \(f_*\) have the correct source and target domain posets. Replacing “range agreement” by the defining equality property of the relevant range preserves both deductions. Sharing the theorem counter changes printed numbers while labels remain intact.

The two removed transition sentences contribute no hypothesis or inference. The adjunction citation is retained in the proposition. Replacing the metaphor about points leaves the mathematical connected-domain definition and its literature dependencies in place.

## (E) Acceptance conditions, non-negotiable

1. The extraneous “then” in \`PropCopOut\` has been removed in the exact current source. The sole local repair finding is closed; no theorem needs to be dropped or weakened.
2. Compile the final source so the shared theorem counter and all label references resolve. Compilation and rendered-layout checks are outside this agent's recheck.

## (F) Not checked / uncertainty log

This recheck covers only \`tmp/review29/note_repairs.diff\` and the repaired argument's composability. The unchanged remainder of the note and external references were not re-audited.

Strongest confirmed blocker: **none**. The identified local grammar correction is **closed**. Strongest suspected unconfirmed blocker: **none supported by the repair text**. Most important unchecked item: **the final compile and rendered references after theorem-counter changes**. The scoped conclusion does not depend on unavailable mathematical material. Final recommendation: **unknown for a whole-note acceptance decision; all scoped mathematical, typing, terminology and grammar findings are closed, with production checks assigned to the parent workflow**.

