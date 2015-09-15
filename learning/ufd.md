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
$$h(x)$$ *essential* if in any factorisation $$f(x) = f_1*f_2*...*f_k$$ one of the factors $$f_i$$ must be an
associate of $$h$$. The idea is that if we can show that $$f$$ has an essential divisor, then we can discard it from any two
factorisations of $$f$$ and pass to a simpler $$f$$, enabling us to use induction.

First, we prove that any irreducible divisor of $$f$$ in $$R$$ is essential. That is, let $$a\in R$$ be irreducible, $$a | f(x)$$. Then $$a$$ finds an associate in any factorisation $$f = f_1*...*f_k$$. We prove this by induction on the degree of $$f$$.
Let the leading coefficient of $$f_i$$ be $$b_i$$ (if $$f_i \in R$$, then $$b_i=f_i$$), so that the leading coefficient of
 $$f$$ is \prod{b_i}. $$R$$ is a UFD, so $$a$$ being irreducible means it's prime. Since $$a | f$$, $$a | \prod{b_i}$$,
and since it's prime, $$a | b_i$$ for some $$i$$. If $$f_i \in R$$, then $$a | f_i$$, and being irreducible $$f_i$$ must
be an associate of $$a$$ and we're done. But maybe $$f_i$$ is a non-constant polynomial $$b_ix^k + f'_i$$ where $$f'_i$$ is of degree $$<k$$. Since $$f_i$$ is irreducible and $$a | b_i$$, $$a$$ cannot divide $$f'_i$$. Now if we replace $$f_i$$ by $$f'_i$$ in the factorisation, that is the same thing as to subtract from $$f$$ the polynomial $$f_1*f_2*...*f_{i-1}*b_ix^k*f_{i+1}*...*f_k$$, which divides $$a$$ because $$b_i$$ does. We're left with a factorisation of some $$f'$$ of smaller degree, in which by the induction hypothesis $$a$$ finds an associate; this associate cannot be the new factor $$f'_i$$ because $$a$$ does not divide it, so it must be one of the original factors.

Now any factorisation of $$f(x) \in R[x]$$ can be separated into two parts: "the $$R$$ part" of
irreducible elements in $$R$$, and "the non-constant part" of non-constant irreducible polynomials. Each of
the parts can be trivial (of length 0). By what we just proved, if we have two factorisations of $$f$$ with 
a nontrivial $$R$$ part in at least one of them, we can take one by one irreducible divisors from the $$R$$ part
and match them with associates in the other factorisation, then discard them both (adjusting what remains up to a unit).
After a number of steps both factorisations must simultaneously end up with trivial $$R$$ parts, and no other factorisation
of this new $$f$$ may have a non-trivial $$R$$ part. Therefore if we show uniqueness only for such polynomials that factor
only into non-constant divisors, that will suffice to finish the proof.

So now let $$f$$ be such a polynomial, and let $$b(x) = b_nx^n+...+b_0$$ be an irreducible divisor of $$f$$ of the smallest degree possible, which means that $$b(x)$$ is still non-constant. Let $$f(x) = f_1*...f_k$$ be any factorisation.
If we find that $$b(x) | f_i$$ for some $$i$$, we're done. Actually, even if we show $$b(x) | c*f_i(x)$$ for some $$c\in R$$, that is also enough, because, given $$b(x)*c'(x) = f_i(x)*c$$, we can factor $$c'(x)$$ and use the argument above to discard the "$$R$$ parts" of both sides; after that the right side will be just $$f_i(x)$$ and the left will still have $$b(x)$$, so $$b(x) | f(x)$$ will be true, and being both irreducible they must be associates.

Now consider some particular $$f_i$$, and let it have degree $$m$$ and a leading monomial $$cx^m$$. If we multiply $$f_i$$ by $$b_n$$, the leading coefficient of $$b$$, that will allow us to sort of "divide" the result by $$b$$ ("sort of" because we only match the highest monomial) and get "remainder" of lesser degree: $$b_n*f_i(x) = c*b(x)*x^{m-n} + r_i$$. Here $$b_n*f_i$$ and $$c*b*x^{m-n}$$ have the same leading monomial: $$b_n*c*x^m$$, so what remains, $$r_i$$, is of degree $$<m$$, possibly 0. Now if it happens that $$b(x)$$ divides that remainder, $$b(x)|r_i$$ (and this includes the case $$r_i=0$$), then $$b(x)$$ divides $$b_n*f_i(x)$$, and by the argument in the previous paragraph that is enough to conclude that $$f_i$$ and $$b(x)$$ are associates. If we're lucky, this will happen for some $$f_i$$. 

So now suppose we're not so lucky and in all these equations we have "remainders" $$r_i$$ not divisible by $$b(x)$$. If we multiply these equations over all the $$f_i$$, then on the right side of the product all the summands will be multiples of $$b(x)$$ except possibly $$\prod{r_i}$$, and on the left side the $$f_i$$ will combine together to form the original $$f$$:

$$\prod{b_n*f_(x)} = b_n^k*\prod{f_i(x)} = b_n^k*f(x) = b(x)*A(x) + \prod{r_i}$$

Since $$b(x)$$ divides $$f$$, we must have also $$b(x) || \prod{r_i}$$, that is $$b(x)*c'(x) = \prod(r_i)$$ for some $$c'(x) \in R[x]$$. In the product of $$r_i$$ every factor is of degree strictly less than that of $$f_i$$, so the result is of degree less than $$f$$. We can now expand this product into a factorisation, and get rid of all the $$R$$ parts on both sides via the same argument as before, which will still leave $$b(x)$$ as in irreducible divisor. The inductive hypothesis now shows that $$b(x)$$ finds an associate somewhere in this factorisation, which means it divides one of the $$r_i$$, which contradicts the assumption we made above.


