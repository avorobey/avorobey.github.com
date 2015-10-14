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
