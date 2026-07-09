

## Reviewer 1

**Comment**:

- The paper seems specifically aimed at readers who are already knowledgeable in
quantum graphical calculi

**Reponse**: ???

**Comment**:
- The frontier between syntax and semantics is blurred throughout the paper, leaving us
wondering for each diagram equation if it is graphically proven or merely semantic.

**Reponse**: We have restructured the paper significantly to make the syntax/semantic distinction clearer. This includes defining controlled states/matrices axiomatically and including these axioms in Fig 1. We also take care to justify the (semantic) use of proof-by-plugging where necessary throughout the appendices.

**Comment**::
- The equations of Fig 1 are claimed to make the language complete, as they come from
ref [22] which proved the result. This result however is proven for qudits (with arbitrary
d), so the axioms had to be specialized to d=2. Several axioms are missing, which I
assume is because they become unnecessary in the qubit case, but I think that already
requires at least some discussion. However, I have no idea how (HD) from [22] is
specialized in the (HD) from the present paper.

**Reponse**: We have added Appendix C which explains how the qudit axioms are specialised to the qubit case. This includes a detailed derivation of (HD).

**Comment**:

- Section 6.1 is not very enlightening, it's a simple application of Lemma 4.5

**Response**: We have added further explanation to this section (now 7.1) to illustrate the significance of this example.

**Comment**:

- Not enough emphasis is put on the commutative vs non-commutative ring of multilinear
polynomials. Non-commutativity (which is necessary for thm 6.1 to hold) is only
mentioned in the intro and conclusion, but not in the main body.

**Reponse**: This is now made clearer throughout the paper, in particular in section 5.

**Comment**:

- The multilinear polynomial ring used throughout the paper also has fixed variable
ordering (i.e. we can't have x1x2 and x2x1 in the polynomial for thm 6.1 to hold, and in
that case it's not because x2x1 = x1x2, but really because x2x1 is not allowed). Maybe
this can be fixed by quotienting the ring with x_ix_j whenever i>=j?

**Response**: ???

**Comment**: 
- Some proofs are unsatisfactory. E.g. lemmas B.1 and B.2 are only argued semantically.
But if we are not interested in how things are derived using the equational theory, then we
may as well prove a lot of the lemmas by simple semantic equivalence. 

**Response**: This is addressed in our response to the second comment.

**Comment**: 

The proof of normal form (thm 5.1) is a bit quick, especially in the argument of termination. In
particular, (3) may actually increase the depth (e.g if another W generator is connected to
the central Z-spider). In thm 5.2: In equation D.14, the induction hypothesis is used for
n+1, which is what we want to prove...

**Response**: Thank you for catching this edge case - we have now addressed it explicitly.

**Comment**: 
The standard interpretation is given for the generators of the language, but not for
compositions

**Reponse**: ???? (i added a sentence but maybe needs a diagram)

**Comment**:
p 2. The n-ary W generator is technically not defined (eq 2.5)

**Response**: This is now defined in eq 2.5

**Comment**: 
Fig1: (TA) is also used to prove Lemma B.10 (eq B.18), which is used in the proof of
completeness for arithmetic diagrams. It is also very possible that the proofs of B.1 and
B.2 (if they exist) need (TA).

**Response**: (TA) is now included in the axioms required for completeness.


**Comment**:
Prop 1 could be better phrased as: we define \tilde{M1M2} as [diagram], and its interpretation is indeed [...]

**Response**: We have implemented this suggestion directly - definition 3.3 and proposition 1.

**Comment**:
Prop 1 essentially explains how to build larger controlled maps, but it feels like we are
missing the base cases (e.g. controls of Paulis).

**Response**: Any state/square matrix can be turned into a controlled map, so there are technically infinitely many base cases. We have provided the example of CNOT. (is this too passive????)

**Comment**: 

Prop 2 seems to be a definition.

**Response**: This is now definition 3.4.

**Comment**:
It feels like the choice of the "branching node" defines a new multiplication ⊠, which is
also valid as long as it is a monoid. There might hence be more motivation on the choice
of the W generator. (It only gets clearer when we reach the last section)

**Response**: This is now addressed in remark 3. (is that enough????)

**Comment**:

Section 3: propositions are semantically obvious, so their value is if they can be proven
syntactically. All are proven syntactically, except for Prop 5, which is broken down to
equivalence of basis elements (which is essentially semantic).

**Response**: As with the second comment, we have made this clearer by introducing axioms for controlled maps.

**Comment**:

Lemma A.1. should be rephrased as a definition first, and then a lemma/prop that it has
the appropriate semantics.

**Response**: This is now definition A.1 and lemmas A.1,A.2.

**Comment**:
Lemmas 4.1 and 4.2 are proven semantically in the appendices, although the axioms
should be enough to prove them syntactically (I assume the authors forgot to remove the
appendix proofs)


Lemma 4.2 is really just the axiom CMcom, I'm not sure why it's there at all
Lemma 4.3 however uses lemma B.1. which is never proven syntactically. I doubt it can
be properly be proven using the axioms from Fig1 (same for Lemma B.2)

**Response**: these comments have all been addressed by introducing axioms for controlled maps. The semantics of these axioms are verified in appendix D.1 and the remaining properties are proven in D.2

**Comment**:
Lemma 4.4: it would be clearer with a picture, since the \circ operator does not tell you
that it's supposed to be applied on the control wire (also the \circ operation on diagram
was not defined)

**Response**: This has been replaced with a diagram, and references to the \circ operator have been removed (except for matrix multiplication)

**Comment**:
p 9: "This fragment of the ZXW-calculus defines a subcategory" -> define it properly:
what are its objects and morphisms? Naively, it does not seem to be a subcategory of
ZXW diagrams, since for instance id:2->2 does not seem to be an arithmetic diagram (but
I imagine 2 is an object)

**Response**: ?????

## Reviewer 2

**Comment**
* p5. In section 3, the authors show how control can be embedded as a higher-order map.
It would be interesting to know how this relates to the recently introduced notion of
controlled PROPs.

**Response**: We now compare to controlled PROPs in the conclusion.

**Comment**:
* p6. The color of the wires of the diagrams containing a Ctrl box seems inconsistent
throughout the section.

**Response**: this has been reformatted.

**Comment**:
* p10. Proposition 6 and Theorem 5.2 are missing a period at the end of their statements.

**Response**: fixed.