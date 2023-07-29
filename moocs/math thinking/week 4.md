1. Show that $¬[∃xA(x)]$ is equivalent to $∀x[¬A(x)]$.
	1. First is "For no x is A(x) true", second is "There exists x for which A(x) is not true". The second one is a negation of "For each x A(x) is true", the first one is a negation of it, also.
2. Prove False: *There is an even prime bigger than 2*
	1. A prime should not be divisible by anything but 1 and itself. An even prime is divisible by 2, so it cannot exist
3. 
	1. (a) All students like pizza. (All people): $(\forall x \in S) \left[ P(x) \right]$
	2. (b) One of my friends does not have a car. (All people): $\exists x (F(x) \rightarrow \neg C(x)$
	3. (c) Some elephants do not like muffins. (All animals): $\exists x(E(x) \to \neg M(x))$
	4. (d) Every triangle is isosceles. (All geometric figures) $\forall x (T(x) \to I(x))$
	5. (e) Some of the students in the class are not here today. (All people): $\exists x (S(x) \to \neg C(x))$
	6. (f) Everyone loves somebody. (All people): $\forall x \exists y (L(x, y))$
	7. (g) Nobody loves everybody. (All people): $\neg \exists x \forall y (L(x, y))$
	8. (h) If a man comes, all the women will leave. (All people): $\exists m \forall w (C(m) \to L(w))$
	9. (i) All people are tall or short. (All people): $\forall p (T(p) \lor S(p))$
	10. (j) All people are tall or all people are short. (All people): $\forall p (S(p)) \lor \forall p (T(p))$
	11. (k) Not all precious stones are beautiful. (All stones): $\exists s (\neg B(s))$
	12. (l) Nobody loves me. (All people): $\neg \exists x (L(x, me))$
	13. (m) At least one American snake is poisonous. (All snakes): $\exists s \in A (P(s))$ -> $\exists s (A(s) \land P(s))$
	14. (n) At least one American snake is poisonous. (All animals): $\exists x (S(x) \land A(x) \land P(x))$
4. asdasd
5. Which of the following are true? The domain for each is given in parentheses
	1. (a) ∃x(2x + 3 = 5x + 1) (Natural numbers): $F$
	2. (b) ∃x(x^2 = 2) (Rational numbers): $T$
	3. (c) ∀x∃y(y = x^2 ) (Real numbers): $T$
	4. (d) ∀x∃y(y = x^2 ) (Natural numbers): $F$
	5. (e) ∀x∃y∀z(xy = xz) (Real numbers): $T$
	6. (f) ∀x∃y∀z(xy = xz) (Prime numbers): $F$
	7. (g) ∀x[x < 0 ⇒ ∃y(y^2 = x)] (Real numbers): $F$
	8. (h) ∀x[x < 0 ⇒ ∃y(y^2 = x)] (Positive real numbers): $F$
6. Negate the following statements and put each answer into positive form: 
	1. (a) (∀x ∈ N )(∃y ∈ N )(x + y = 1): $(\exists x \in \mathbb{N})(\forall y \in \mathbb{N}(x+y \neq 1))$
	2. (b) (∀x>0)(∃y <0)(x + y = 0) (where x, y are real number variables): $all$
	3. (c) ∃x(∀ > 0)(− < x < ) (where x,  are real number variables) 
	4. (d) (∀x ∈ N )(∀y ∈ N )(∃z ∈ N )(x + y = z 2)
7. Give a negation (in positive form) of the famous “Abraham Lincoln sentence” which we met in the previous assignment: “You may fool all the people some of the time, you can even fool some of the people all of the time, but you cannot fool all of the people all the time.”
	1. $(a)$
8. ![](https://i.imgur.com/UtDLcSC.png)
   Write down a formal definition for f being discontinuous at a. Your definition should be in positive form.
	1. $(\exists \epsilon > 0)(\exists \delta > 0)(\forall x) \left[ |x-a|>\delta \implies |f(x)-f(a)| > \epsilon \right]$
