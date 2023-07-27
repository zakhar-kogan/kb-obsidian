# ASSIGNMENT 5 (for Lecture 5)
1. Express the following as existence assertions. (Feel free to use a mix of symbols and words)![](https://i.imgur.com/W8Rpc8C.png)
	1. $\exists\ [x \in \mathbb N]\ \Rightarrow \ x^3=27$
	2. $\exists\ [x \in \mathbb N]\ \Rightarrow \ n>1,000,000$
	3. $\exists\ [x \in \mathbb N]\ \Rightarrow \ ((n>1) \land (n \lnot prime))$
2. Express the following as ‘for all’ assertions (using symbols and words)![](https://i.imgur.com/9WCKjtx.png)
	1. $\forall \ [n\in \mathbb N] \ \Rightarrow \ x^3 \neq 28$ -> $\lnot (\forall x \in \mathbb N)[x^3=28]$
	2. $\forall \ [n\in \mathbb N] \ \Rightarrow \ 0 < n$ 
	3. $\forall \ ([n\in \mathbb N] \land [n>1] \ \Rightarrow \ n=prime$
3. Express the following in symbolic form, using quantifiers for people
	1. (a) Everybody loves somebody: $\forall\ loves\ \exists$ -> $(\forall x)(\exists y)L(x,y)$
	2. (b) Everyone is tall or short. $(\forall x) [Tall(x) \lor Short(x)]$ 
	3. (c) Everyone is tall or everyone is short. $(\forall x)(Tall(x)) \lor (\forall x)(Short(x))$
	4. (d) Nobody is at home. $\lnot(\forall\ |\ at\ home)$
	5. (e) If John comes, all the women will leave. $John\ comes \Rightarrow\ \forall \in women\ \lnot comes$ -> $Comes(John) \Rightarrow (\forall x)[Woman(x) \Rightarrow Leaves(x)]$
	6. (f) If a man comes, all the women will leave. $(\exists x) [Man(x) \land Comes(x)] \Rightarrow (\forall x)[Woman(x) \Rightarrow Leaves(x)]$
4. Express the following using quantifiers that refer (only) to the sets $R$ (real numbers) and $N$ (natural numbers):
	1. (a) The equation $x^2 + a = 0$ has a real root for any real number a: $(\forall a)(\exists\ root(x^2+a=0) \land root \in \mathbb R)$
	2. (b) The equation $x^2 + a = 0$ has a real root for any negative real number a: $(\forall a \land a<0)(\exists root(x^2+a=0) \land root \in \mathbb R)$
	3. (c) Every real number is rational: $(\forall x \in \mathbb R)(x \in \mathbb N)$
	4. (d) There is an irrational number: $\exists x: x \neg \in \mathbb R$ 
	5. (e) There is no largest irrational number. (This one looks quite complicated.) $(\forall x):(\exists y \in \mathbb N)\land(x < y)$
5. Let C be the set of all cars, let D(x) mean that x is domestic, and let M(x) mean that x is badly made. Express the following in symbolic form using these symbols:
	1. (a) All domestic cars are badly made: $(\exists x\in C \land \forall x\ D(x))M(x)$
	2. (b) All foreign cars are badly made. 
	3. (c) All badly made cars are domestic. 
	4. (d) There is a domestic car that is not badly made. 
	5. (e) There is a foreign car that is badly made