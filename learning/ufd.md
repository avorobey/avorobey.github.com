---
title: UFD
---
<head>
    <script type="text/javascript"
            src="http://cdn.mathjax.org/mathjax/latest/MathJax.js?config=TeX-AMS-MML_HTMLorMML">
    </script>
</head>

This is a direct proof, without using Gauss's Lemma, of the theorem that a polynomial ring over a UFD
is a UFD. The usual proof uses a lot of machinery: it goes over to the field of fractions of the
original domain, then uses the result that *its* polynomial ring is a PID, therefore Euclidean,
therefore a UFD, and then jumps back from unique factorisations in $$F[x]$$ to unique factorisations
in $$R[x]$$ using Gauss' Lemma. I don't like it very much. It doesn't seem to illuminate what's really
going on in $$R[x]$$, and it feels a little like trickery. I thought there might be a reasonable direct
proof just based on the UFD properties. I found a nice writeup in Pete Clark's Commutative Algebra notes,
where he adopts a direct proof by Zermelo of the Fundamental Theorem of Arithmetic that avoids Euclid's Lemma.
I thought another, similar direct proof of the FTA by ... might look even nicer when translated to UFDs.
This is an attempt to write it up.

**Theorem**. Let $$R$$ be a UFD (unique factorisation domain). Then so is $$R[x]$$.

**Proof**. We need to establish existence and uniqueness of factorisations into irreducibles in $$R[x]$$.

**Existence**. Let $$f(x) = a_nx^n + a_{n-1}x^{n-1} + ... + a_0$$, and if $$f$$ is not irreducible, we expand
it: $$f = gh$$ with $$g,h$$ both non-units; then if either or both of $$g,h$$ are not
irreducible, we expand them and so on. If we can't expand any more and stop, we have a factorisation into irreducibles.
Will we always stop?

* At every point we'll have some elements in the product that are in $$R$$ ("the $$R$$ part"),
and some that are non-constant polynomials in $$R[x]$$ ("the non-constant part").

* The size of the non-constant part is limited, because every non-constant element is eating into
the degree of $$f$$. So there we will stop.

* The product of just the $$R$$ part must always divide all of $$f$$ and in particular $$a_0$$.
Since $$R$$ is a UFD, all the elements of "the $$R$$ part" in an expanded product have unique factorisations,
and all these together may only use up the irreducibles (up to associates) that are in the factorisation of $$a_0$$,
no more. In particular there will not be more non-unit elements of $$R$$ in the expanded product than the number
of irreducibles in $$a_0$$. So the size of the $$R$$ part is limited, and we will stop there, too.

The process will finish with a factorisation, as required.

**Uniqueness**. Let $$f(x) \in R[x]$$, and suppose that $$h(x)$$ is an irreducible divisor of $$f(x)$$. Call
$$h(x)$$ *essential for $$f(x)$$* if in any factorisation $$f(x) = f_1*f_2*...*f_k$$ one of the factors $$f_i$$ must be an
associate of $$h$$. Of course, if there's indeed uniqueness of factorisation, then every irreducible divisor is essential,
but we're yet to prove this.

Suppose for a moment that we proved that every non-constant $$f(x)$$ has an essential divisor. This then suffices to prove
uniqueness of factorisation, by induction on the degree of $$f$$. How? Given any two factorisations of $$f(x)$$, if $$h(x)$$
is an essential divisor, it must be present in both. Discarding it in both and adjusting up to a unit, we get two shorter factorisations of $$f' = f/h$$. Now if $$h$$ is non-constant, then $$f'$$ is of a lower degree and we can apply the inductive hypothesis
(the basis, when $$f$$ is constant, works because $$R$$ is a UFD). But even if $$h \in R$$, we can continue the process and
discard now the essential divisor $$h'$$ of $$f'$$. By the argument made above in the existence proof, there's a limit to how many constant irreducible divisors of $$f$$ we can accumulate, so eventually the next essential divisor will be non-constant and will lower the degree.

It remains to prove that every non-constant $$f(x)$$ indeed has an essential divisor. We will argue that any irreducible divisor *of the smallest degree possible* is essential. There are two different cases to take care of: if the smallest degree is $$0$$, then $$f$$ has constant irreducible divisors. If it's $$>0$$, then the only irreducible divisors are non-constant polynomials.

In the first case, let $$a\in R$$ be irreducible, $$a | f(x)$$, and $$f = f_1*...*f_k$$ a factorisation. 
Let the leading coefficient of $$f_i$$ be $$b_i$$ (if $$f_i \in R$$, then $$b_i=f_i$$), so that the leading coefficient of
 $$f$$ is $$\prod{b_i}$$. $$R$$ is a UFD, so $$a$$ being irreducible means it's prime. Since $$a | f$$, $$a | \prod{b_i}$$,
and since it's prime, $$a | b_i$$ for some $$i$$. If $$f_i \in R$$, then $$a | f_i$$, and being irreducible $$f_i$$ must
be an associate of $$a$$ and we're done.
But maybe $$f_i$$ is a non-constant polynomial $$b_ix^k + f'_i$$ where $$f'_i$$ is of degree $$<k$$.
Since $$f_i$$ is irreducible and $$a | b_i$$, $$a$$ cannot divide $$f'_i$$.
Now if we replace $$f_i$$ by $$f'_i$$ in the factorisation, that is the same thing as to subtract from $$f$$
the polynomial $$f_1*f_2*...*f_{i-1}*b_ix^k*f_{i+1}*...*f_k$$, which is divisible by $$a$$ because $$b_i$$ is.
The result is a new polynomial $$f'$$, still a multiple of $$a$$, with a factorisation in which $$f_i$$ is replaced by $$f'_i$$
and therefore $$f'$$ has a smaller degree than $$f$$. By the inductive hypothesis, $$f'$$ has uniquess of factorisation, so $$a$$ must be present as an associate in the factorisation. The new factor $$f'_i$$ cannot be that associate because $$a$$ does not divide it, so it must be one of the original factors.

Now we deal with the second case, where $$f$$ does not have constant irreducible factors. Let $$b(x) = b_nx^n+...+b_0$$ be
 an irreducible divisor of $$f$$ of the smallest degree possible, and $$f(x) = f_1*...f_k$$ a factorisation.
 We can assume $$k>1$$. To show that $$b(x)$$ has an associate among $$f_i$$, it is enough to show
 $$b(x) | f_i(x)*c$$ for some $$c\in R$$, because $$f_i(x)*c$$ is of lower degree than $$f(x)$$, so it has uniqueness,
 and $$b(x)$$ cannot find an associate inside $$c$$, so its associate must be $$f_i(x)$$.

Now consider some particular $$f_i$$, and let it have degree $$m$$ and a leading monomial $$cx^m$$.
If we multiply $$f_i$$ by $$b_n$$, the leading coefficient of $$b$$, that will allow us to sort of "divide" the result
by $$b$$ ("sort of" because we only match the highest monomial) and get "remainder" of lesser degree:
$$b_n*f_i(x) = c*b(x)*x^{m-n} + r_i$$. Here $$b_n*f_i$$ and $$c*b*x^{m-n}$$ have the same leading monomial:
$$b_n*c*x^m$$, so what remains, $$r_i$$, is of degree $$<m$$, possibly 0. Now if it happens that $$b(x)$$ divides
that remainder, $$b(x) | r_i$$ (and this includes the case $$r_i=0$$), then $$b(x)$$ divides $$b_n*f_i(x)$$,
and by the argument in the previous paragraph that is enough to conclude that $$f_i$$ and $$b(x)$$ are associates. If we're lucky, this will happen for some $$f_i$$. 

So now suppose we're not so lucky and in all these equations we have "remainders" $$r_i$$ not divisible by $$b(x)$$. If we multiply these equations over all the $$f_i$$, then on the right side of the product all the summands will be multiples of $$b(x)$$ except possibly $$\prod{r_i}$$, and on the left side the $$f_i$$ will combine together to form the original $$f$$:

$$\prod{b_n*f_(x)} = b_n^k*\prod{f_i(x)} = b_n^k*f(x) = b(x)*A(x) + \prod{r_i}$$

Since $$b(x)$$ divides $$f$$, we must have also $$b(x) \| \prod{r_i}$$. In the product of $$r_i$$ every factor is of degree strictly less than that of $$f_i$$, so the result is of degree less than $$f$$, and the inductive hypothesis applies. We can expand this product into a factorisation, and $$b(x)$$ will have an associate somewhere in it, meaning $$b(x)$$ must divide one of the $$r_i$$, which contradicts the assumption we made above.


**Alternative uniqueness**. Let $$f(x) \in R[x]$$ be non-constant. We proved that $$f$$ has factorisations, and every factorisation must include a non-constant irreducible polynomial.
Therefore we can safely define $$h(x)$$ to be a non-constant irreducible divisor of $$f(x)$$ of smallest possible degree. We aim to show that any factorisation of $$f$$ must include an associate of $$h$$. If we're able to show this, then given two factorisations of $$f$$, we can discard $$h$$ from both (adjusting up to a unit); since $$h$$ is non-constant, this will lower the degree and the inductive hypothesis finishes the proof (note that the basis of the induction is a constant $$f \in R$$, which works because $$R$$ is a UFD).

