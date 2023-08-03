# ASSIGNMENT 7 (for Lecture 7)
1. Prove or disprove the statement “All birds can fly.”
	1. Contradiction: $\forall B: Fly(B) \to \exists B: \neg Fly(B)$
	2. As there are non-flying birds (kiwi, ostrich), then the first statement that all birds can fly is not right - we had proven the inverse statement
2. Prove or disprove the claim $(∀x, y ∈ R)[(x − y)^2 > 0]$
	1. We have to construct two claims: either $(x-y)^2>0$ or $\exists x,y[(x-y)^{2} \leq 0]$
	2. Let $x-y=z$, then our claim is $z \in \mathbb{R}[z^2>0]$
	3. However, if $z=0$, then $z^{2}=0$, disproving our first statement
3. Prove that between any two unequal rationals, there is a third rational
	1. Let first rational be $a=o/q$, second $b=p/q$, and $o \neq p$
	2. If we can't find $w \in \mathbb{Q}[o < w < p]$ or vice versa, we can multiply everything by $x$, and find another number
	3. E.g. $\frac{10o}{10q} < \frac{10o+1}{10q} < \frac{10p}{10q}$
4. Explain why proving φ ⇒ ψ and ψ ⇒ φ establishes the truth of φ ⇔ ψ.
	1. Logical equivalence is always producing the same truth value
	2. So