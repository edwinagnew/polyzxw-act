

Review 1

| feedback | scope | status | comments |
| --- | --- | --- | --- |
| The equations of Fig 1 are claimed to make the language complete, as they come from ref [22] which proved the result. This result however is proven for qudits (with arbitrary d), so the axioms had to be specialized to d=2. Several axioms are missing, which I assume is because they become unnecessary in the qubit case, but I think that already requires at least some discussion. However, I have no idea how (HD) from [22] is specialized in the (HD) from the present paper. |  | | |
|  Section 6.1 is not very enlightening, it's a simple application of Lemma 4.5 | | |(E) disagree - its important example of applicability - do we need to rephrase that? | 
|  Not enough emphasis is put on the commutative vs non-commutative ring of multilinear polynomials. Non-commutativity (which is necessary for thm 6.1 to hold) is only mentioned in the intro and conclusion, but not in the main body. The multilinear polynomial ring used throughout the paper also has fixed variable ordering (i.e. we can't have x1x2 and x2x1 in the polynomial for thm 6.1 to hold, and in that case it's not because x2x1 = x1x2, but really because x2x1 is not allowed). Maybe this can be fixed by quotienting the ring with x_ix_j whenever i>=j? | | | (E) I agree with the first bit (controlled matrices arent commutative, controlled states are and we should emphasise this better), but not sure about the second - the ordering is just a convention so why would it need a quotient? |
| lemmas B.1 and B.2 are only argued semantically. But if we are not interested in how things are derived using the equational theory, then we may as well prove a lot of the lemmas by simple semantic equivalence|
| The proof of normal form (thm 5.1) is a bit quick, especially in the argument of termination. In particular, (3) may actually increase the depth (e.g if another W generator is connected to the central Z-spider). | | | (E) this is true - if theres another W in (3), they would end up being connected by a cup, which effectively pushes one down a level. So i guess (5) would have to follow it? 
| In thm 5.2: In equation D.14, the induction hypothesis is used for n+1, which is what we want to prove...| | | (E) I think the RHS should be $\phi_n$ not $\phi_{n+1}$? |
|p 2. The n-ary W generator is technically not defined (eq 2.5)| | fixed |
| Fig1: (TA) is also used to prove Lemma B.10 (eq B.18), which is used in the proof of completeness for arithmetic diagrams. It is also very possible that the proofs of B.1 and B.2 (if they exist) need (TA).| | | (E) not true - lemma B10 uses BZW which is a separate axiom. TBD for proofs of B1 and B2 but i doubt it. 
|Prop 1 could be better phrased as: we define \tilde{M1M2} as [diagram], and its interpretation is indeed [...]|
| Prop 1 essentially explains how to build larger controlled maps, but it feels like we are missing the base cases (e.g. controls of Paulis). | 
| Prop 2 seems to be a definition| |
| It feels like the choice of the "branching node" defines a new multiplication ⊠, which is also valid as long as it is a monoid. There might hence be more motivation on the choice of the W generator. (It only gets clearer when we reach the last section)|  | | (E) just needs a brief comment that coW copies controlled states?  
| Section 3: propositions are semantically obvious, so their value is if they can be proven syntactically. All are proven syntactically, except for Prop 5, which is broken down to equivalence of basis elements (which is essentially semantic).| | | (E) feel like we could prove this syntatically, but would require some ZH rules?
| Lemma A.1. should be rephrased as a definition first, and then a lemma/prop that it has the appropriate semantics. |
| Lemmas 4.1 and 4.2 are proven semantically in the appendices, although the axioms should be enough to prove them syntactically (I assume the authors forgot to remove the appendix proofs)| 
| Lemma 4.2 is really just the axiom CMcom, I'm not sure why it's there at all| | fixed | (E) this section needs a closer look - we didnt properly rewrite it after adding new rules
| Lemma 4.3 however uses lemma B.1. which is never proven syntactically. I doubt it can be properly be proven using the axioms from Fig1 (same for Lemma B.2) | 
| Lemma 4.4: it would be clearer with a picture, since the \circ operator does not tell you that it's supposed to be applied on the control wire (also the \circ operation on diagram was not defined)| | done
| p 9: "This fragment of the ZXW-calculus defines a subcategory" -> define it properly: what are its objects and morphisms? Naively, it does not seem to be a subcategory of ZXW diagrams, since for instance id:2->2 does not seem to be an arithmetic diagram (but I imagine 2 is an object) |

Reviewer 2

| feedback | scope | status | comments |
| --- | --- | --- | --- |
| * p5. In section 3, the authors show how control can be embedded as a higher-order map. It would be interesting to know how this relates to the recently introduced notion of controlled PROPs. |
| * p6. The color of the wires of the diagrams containing a Ctrl box seems inconsistent throughout the section. | | done
| * p10. Proposition 6 and Theorem 5.2 are missing a period at the end of their statements. | | done