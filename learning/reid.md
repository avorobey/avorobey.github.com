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

$$A$$ has two minimal  prime ideals $$(X)$$ and $$(Y)$$. To show $$(X)$$ is prime, assume the product above is in $$(X)$$, which means
that $$aa' = a'g+ag'+gg'Y = 0$$. Assume the first factor is not in $$(X)$$, which means $$a \ne 0$$ or $$g \ne 0$$ (or both), and
in either case we want to deduce $$a' = g' = 0$$, so that the other factor is in $$(X)$$. 

First case: $$a \ne 0$$, then $$a' = 0$$ and
$$ag' + gg'Y = g'(a+gY) = 0$$. Since $$a \ne 0$$, the polynomial $$a+gY$$ is definitely nonzero, so $$g'=0$$ as required.

Second case: $$g \ne 0$$, and we can assume $$a=0$$ because otherwise it's the previous case; then $$g(a'+g'Y)=0$$, and so
$$a'+g'Y = 0$$, from which $$a'=0, g'=0$$ follow immediately.

$$(Y)$$ is prime for the same reason. 