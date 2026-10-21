# Recursion categories

## Catalogue and coalgebraic representations

*A catalogue and classification problems over sets of integers*

Version 3, 21 October 2026.

- [Read the note (PDF)](Recursion_Categories_and_Coalgebraic_Representations_v3.pdf).
- [LaTeX source](Recursion_Categories_and_Coalgebraic_Representations_v3.tex).

The note catalogues numerical, syntactic, operator, and other recursion
categories; develops comparisons of coalgebraic representations; and studies
representations using observations of sets of integers. Section 5.5 relates
pointed Moore coalgebras to strictly causal operators on streams, proves
countable and computable realization results, and connects equality of these
operators with behavioral equivalence.

## Application and substitution for external higher types

Version 1, 21 October 2026.

- [Read the note (PDF)](Application_and_Substitution_v1.pdf).
- [LaTeX source](Application_and_Substitution_v1.tex).

Partial function types on numerical partial equivalence relations, computation
names, and strict and lazy substitution. The note gives explicit application
and abstraction operations and proves the substitution law for the lazy
finite-type semantics.

## Coalgebraic higher types and determinacy

Version 1, 21 October 2026.

- [Read the note (PDF)](Coalgebraic_Higher_Types_and_Determinacy_v1.pdf).
- [LaTeX source](Coalgebraic_Higher_Types_and_Determinacy_v1.tex).

Coalgebraic realizations of the preceding higher-type operations, comparisons
with restriction splitting and regular exact completion, and a range
obstruction at the partial numerical function type. The note studies dependent
choice, Boolean separation, determinacy, continuous representative lifts, and
their realization by stream transducers.

## Building the notes

To build the PDF with a TeX installation containing the packages listed in the
source, run `pdflatex` twice from this directory. For example:

```sh
pdflatex -interaction=nonstopmode -halt-on-error Recursion_Categories_and_Coalgebraic_Representations_v3.tex
pdflatex -interaction=nonstopmode -halt-on-error Recursion_Categories_and_Coalgebraic_Representations_v3.tex
```

Use the corresponding source filename to build either companion note.
Each bibliography is included in its source; no separate bibliography tool is
needed. The repository's [CC BY 4.0 license](../LICENSE) applies to these notes.
