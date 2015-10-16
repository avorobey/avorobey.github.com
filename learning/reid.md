---
title: Undergraduate Commutative Algebra
---
<head>
    <script type="text/javascript"
            src="http://cdn.mathjax.org/mathjax/latest/MathJax.js?config=TeX-AMS-MML_HTMLorMML">
    </script>
</head>

1.1. In $$Z$$, consider $$(5) \cup (6)$$. Any ideal that includes both $$5$$ and $$6$$ must
include $$1$$, so it's all of $$Z$$.

1.2. In $$Z$$, let $$I,J = (3) = 3Z$$. Then $$IJ$$ is $$(9)$$, but $$I \cap J$$ is $$(3)$$. More generally,
in $$Z$$ let $$I = (a), J = (b)$$, then if $$a,b$$ are not co-prime, $$IJ \ne I\cap J$$.

1.3. Given $$f \in k[X,Y]$$, all mixed monomials in $$f$$ can be dropped mod $$(XY)$$, so $$f+(XY)$$ has
a representative with only the constant part and monomials in $$X$$ and $$Y$$, which can be written as
$$a + f(X)X + g(Y)Y$$. Now suppose there's another representative $$a' + f'(X)X + g'(Y)Y$$, then 
$$a-a' + (f-f')X + (g-g')Y \in (XY)$$, meaning $$X | (a-a') + (g-g')Y$$ which forces $$a=a', g=g'$$, and similarly $$f=f'$$.

Products are straightforward: $$(a + f(X)X + g(Y)Y)(a'+f'(X)X+g'(Y)Y) = aa' + (a'f+af'+ff'X)X + (a'g + ag' + gg'Y)Y$$.

$$A$$ has two minimal  prime ideals $$(X)$$ and $$(Y)$$. For example, $$(X)$$ is prime, because $$A/(X)$$ is isomorphic to $$k[Y]$$
(using the representation above) and therefore a domain. $$(X)$$ is minimal, because if $$I \subset (X)$$ is a prime ideal, consider
any element of $$I$$, and represent it as $$X^k*f(X,Y)$$, where $$f$$ is not in $$(X)$$. By primality of $$I$$, $$X^k$$ and then $$X$$
are in $$I$$.

Suppose some other $$I$$ is a minimal prime ideal in $$A$$, and let $$a+f(X)X+g(Y)Y$$ be a nonzero element of $$I$$. We assume that
$$X$$ is not in $$I$$ - otherwise by its minimality $$I=(X)$$. Similarly $$Y \notin I$$. Multiply the element by $$XY$$, then all that's left
is $$aXY$$, and by primality $$a \in I$$, so we must have $$a=0$$, and the element is really $$f(X)X+g(Y)Y$$. Now multiply by $$X$$
to get rid of the $$Y$$-part, and using the primality of $$I$$ keep removing factors of $$X$$ from the $$X$$-part. Since we can't end up
with any nonzero constant part (by the above argument that $$a=0$$), we must finish with plain $$X \in I$$, achieving the contradiction.

a) $$IJ = I\cap J$$. Take $$I=J=(X)$$.

b) $$(I+J)(I\cap J) = IJ$$. Take $$I=(X)$$, $$J=(X+1)$$. Then $$I+J = A$$, I\cap J = 0, IJ=(X(X+1))$$.

c) $$I\cap (J+K) = (I \cap J) + (I \cap K)$$. Take $$I=(X), J=(X+1), K=(X+2)$$. The left-hand side is $$I$$, the right-hand-side is $$0$$.

1.4. The usual notion of coprime in $$Z$$ or $$k[X]$$ is: $$a,b$$ are co-prime if $$g.c.d.(a,b)=1$. But since both $$Z$$ and $$k[X]$$ are
Euclidean domains, the GCD of two elements is expressible as their linear combination, and therefore $$a,b$$ are co-prime iff $$(a)+(b)=(1)$$.

Given $$I+J=A$$, we have $I\cap J$$ = (I\cap J)(I+J) \subseteq (I\cap J)I + (I\cap J)J \subseteq JI + IJ = IJ$$. The other direction is trivial.
Now suppose $$a+IJ \in A/IJ$$. We define the image of $$a$$ in $$(A/I)\times (A/J)$$ as $$(a+I,a+J)$$. We need to prove:

- this is well-defined: if $$a+IJ = a'+IJ$$, then $$a-a'\in IJ$$. Since $$IJ = I\cap J$$ by the above, we have $$a-a' \in I$$ and $$a+I=a'+I$$,
likewise with $$J$$.
- this is a homomorphism of rings: trivial.
- this is 1-1: if $$a+IJ \ne 0$$, then $$a \notin IJ$$, and so certainly $$a \notin I$$ and $$a+I \ne 0$$, same with $$J$$.
- this is onto: given $$b,c \in A$$, we need to find $$a\in A$$ such that $$a-b \in I, a-c\in J$$. Since $$I+J=A$$, we have $$i,j \in I,J$$
such that $$-i+j=b-c$$. Then $$b+i=c+j$$, and we can take $$a=b+i=c+j$$.

Suppose $$I+J=A$$ and we want to prove $$I^n+J^n  = A$$. It suffices to prove $$I^n+J=A$$ because then we can pretend $$I^n$$ is the
new $$I$$ and carry out the same argument for $$J$$. Since $$I+J=A$$, we have $$a+b=1$$ for $$a \in I, b \in J$$. It's enough to show that
$$a^n + b' = 1$$ for some $$b'\in J$$. But the difference between $$a$$ and $$a^n$$ is $$a(a^{n-1}-1)$$ and is divisible by $$1-a = b \in J$$,
so the entire difference is in $$J$$. Therefore if we replace $$a$$ by $$a^n$$, we need only adjust $$b$$ by something in $$J$$ to keep the same
sum $$1$$.

1.5. 