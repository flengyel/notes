# Independent check: sections without local connectedness

**Conclusion.** The local-connectedness assumption can be removed from the current proposition `prop:local-switch`. The other hypotheses used below are the existing ones: a split restriction category with ranges satisfying range agreement, restriction zeros, binary restriction coproducts, weak choice, and preservation of binary joins of restriction idempotents by inverse image along every partial morphism. No coproduct-extensivity assumption, element argument, connected probe, or additional choice principle is used.

This checks the proposed strengthening of the section proposition. It is not a review of the whole paper or of the older `LOCOct10f` manuscript.

## Statement checked

Let `A` have the preceding structure. For disjoint restriction idempotents `a,b:X ⇀ X`, put

\[
p=\nabla_X(a+b):X+X\rightharpoonup X.
\]

Then `p` is a partial monomorphism and has a unique section `s:X ⇀ X+X`. Moreover

\[
ps=\bar s=a\vee b,\qquad sa=i_0a,\qquad sb=i_1b,
\]

and

\[
s^*(1_X+0_X)=a,\qquad s^*(0_X+1_X)=b.
\]

For complementary `c,c'`, take `a=c'` and `b=c` to obtain a total section of `∇_X(c'+c)` with the required reversed tags.

## Coproduct identities

Let

\[
i_0,i_1:X\longrightarrow X+X,
\quad r_0=[1_X,0_X],\quad r_1=[0_X,1_X]:X+X\rightharpoonup X,
\]

and write

\[
\varepsilon_0=i_0r_0=1_X+0_X,
\qquad \varepsilon_1=i_1r_1=0_X+1_X.
\]

The restriction axioms and coproduct universal property give

\[
\bar r_i=\varepsilon_i,\quad
r_i i_i=1_X,\quad r_i i_{1-i}=0_X,\quad
\varepsilon_0\varepsilon_1=0_{X+X},\quad
\varepsilon_0\vee\varepsilon_1=1_{X+X}.
\]

For example, the equality `bar r_i=ε_i` follows by precomposing with the two total injections and using `bar r_i i_j=i_j overline(r_i i_j)`. An idempotent receiving both `ε_0` and `ε_1` fixes both injections, hence is the identity; this proves their join is the identity.

Since `∇_X` is total,

\[
\bar p=a+b.
\]

Disjointness `ab=0_X` gives the typed morphism identities

\[
ap=[a,0_X]:X+X\rightharpoonup X,
\qquad bp=[0_X,b]:X+X\rightharpoonup X.
\]

Consequently, for `t:Y ⇀ X+X`:

\[
\begin{array}{lll}
\varepsilon_0t=t&\Longrightarrow&\bar p t=i_0ap t,\quad bp t=0_{Y,X},\\
\varepsilon_1t=t&\Longrightarrow&\bar p t=i_1bp t,\quad ap t=0_{Y,X}.
\end{array}
\]

These identities follow by substituting `t=ε_i t` and evaluating the coproduct components. No cancellation of an injection is needed.

## Partial monicity for total test morphisms

Let `θ,θ':Y→X+X` be total, with `pθ=pθ'`. Define restriction idempotents on `Y` by

\[
e_i=\theta^*\varepsilon_i,
\qquad f_j=(\theta')^*\varepsilon_j,
\qquad \delta_{ij}=e_i f_j
\quad (i,j\in\{0,1\}).
\]

Totality and inverse-image preservation give

\[
e_0\vee e_1=f_0\vee f_1=1_Y.
\]

Inverse image along the partial morphism `e_i:Y ⇀ Y` gives

\[
e_i=e_i^*(f_0\vee f_1)
=e_i^*f_0\vee e_i^*f_1
=e_if_0\vee e_if_1.
\]

Thus the four `δ_ij` have join `1_Y`. This is the exact step that uses join preservation along a restriction idempotent, rather than only along a total morphism.

The restriction identity

\[
\varepsilon_i\theta=\theta\overline{\varepsilon_i\theta}=\theta e_i
\]

and its analogue for `θ'` imply

\[
\varepsilon_i\theta\delta_{ij}=\theta\delta_{ij},
\qquad
\varepsilon_j\theta'\delta_{ij}=\theta'\delta_{ij}.
\]

If `i=j=0`, the coproduct identities above and `pθ=pθ'` give

\[
\bar p\theta\delta_{00}
=i_0ap\theta\delta_{00}
=i_0ap\theta'\delta_{00}
=\bar p\theta'\delta_{00}.
\]

For `i=j=1`, the same calculation uses `i_1bp`.

For `i=0,j=1`, the two sides are zero:

\[
\bar p\theta\delta_{01}
=i_0ap\theta\delta_{01}
=i_0ap\theta'\delta_{01}=0_{Y,X+X},
\]

because `θ'δ_01` is in the second summand, while

\[
\bar p\theta'\delta_{01}
=i_1bp\theta'\delta_{01}
=i_1bp\theta\delta_{01}=0_{Y,X+X},
\]

because `θδ_01` is in the first summand. The case `i=1,j=0` is symmetric, with the two explicit summand roles exchanged.

Form the iterated binary copairing

\[
h=[\delta_{00},\delta_{01},\delta_{10},\delta_{11}]:
((Y+Y)+Y)+Y\rightharpoonup Y.
\]

A restriction idempotent receives `h` exactly when it receives all four components, so

\[
\operatorname{ran}(h)=\bigvee_{i,j}\delta_{ij}=1_Y.
\]

The four equalities imply `(bar p θ)h=(bar p θ')h`. Range agreement therefore gives

\[
\bar p\theta=(\bar p\theta)\operatorname{ran}(h)
=(\bar p\theta')\operatorname{ran}(h)=\bar p\theta'.
\]

This replaces the current appeal to jointly epimorphic connected restriction idempotents.

## Arbitrary partial test morphisms

Let `u,v:W ⇀ X+X` satisfy `pu=pv`. Split the common restriction idempotent

\[
r=\overline{pu}=\overline{pv}=me,
\qquad m:Z\to W,\quad e:W\rightharpoonup Z,
\qquad em=1_Z.
\]

The morphisms `pum` and `pvm` are total. Indeed `r m=m`, and the restriction identity together with cancellation by the split monomorphism `m` gives their restriction idempotent `1_Z`. Since `overline(pum) ≤ overline(um)` and `overline(pvm) ≤ overline(vm)`, the morphisms `um` and `vm` are total too. They have equal composites with `p`; the preceding argument gives

\[
\bar p um=\bar p vm.
\]

Precomposing with `e` yields

\[
\bar p u r=\bar p v r.
\]

The restriction axiom gives `bar p u=u overline(pu)=u r`, hence `bar p u r=bar p u`; the same holds for `v`. Therefore

\[
\bar p u=\bar p v.
\]

This proves partial monicity. Splitness is used precisely in this reduction.

## Existence, uniqueness and identities of the section

Weak choice supplies `s:X ⇀ X+X` with

\[
ps=\bar s,\qquad psp=p.
\]

Thus `bar s` receives `p`. If a restriction idempotent `t:X ⇀ X` receives `p`, then

\[
t\bar s=tps=ps=\bar s.
\]

It follows that `bar s=ran(p)`. A restriction idempotent receives `p` exactly when it receives both `p i_0=a` and `p i_1=b`; hence `ran(p)=a∨b`.

The restriction axiom gives `bar p s=s overline(ps)=s`. If `s'` is another section, it has the same restriction `ran(p)`, so `ps=ps'`; partial monicity gives `s=s'`.

Now `p(sa)=a=p(i_0a)`. Partial monicity, `bar p s=s`, and `(a+b)i_0a=i_0a` give `sa=i_0a`. Likewise `sb=i_1b`.

The morphisms `ε_0s` and `i_0a`, both of type `X ⇀ X+X`, agree after `a` and `b`; they therefore agree after `[a,b]:X+X ⇀ X`. Range agreement gives equality after `a∨b=bar s`. Each morphism is already supported there, so `ε_0s=i_0a`. Taking restrictions gives `s*ε_0=a`. The same calculation gives `s*ε_1=b`.

## Hypotheses and consequence for the criterion

- Range agreement, not local connectedness, combines the four idempotent pieces.
- Preservation of binary joins along all partial morphisms is used to distribute `e_i` over `f_0∨f_1`. A weaker hypothesis restricted to total morphisms is not what this proof verifies.
- Binary restriction coproducts and zeros give the partial projections and summand identities; no extensive total category is presumed.
- Splitness reduces arbitrary partial tests to total ones.
- Weak choice supplies the section after partial monicity has been proved.

The source-inseparability criterion can consequently retain its stated lifting condition and all other hypotheses while dropping local connectedness of the target. The existing proof from the two section inverse-image equations and the lifted-separator corollary then applies unchanged.

**Disposition:** the proposed strengthening is proved under the current hypotheses. Publishing only a local-connectedness version would retain an unnecessary assumption. This check does not show that splitness, weak choice or full inverse-image join preservation can be removed.
