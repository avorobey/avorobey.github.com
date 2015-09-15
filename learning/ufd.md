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

**Uniqueness**. Any factorisation of $$f(x) \in R[x]$$ can be separated into two parts: "the $$R$$ part" of
irreducible elements in $$R$$, and "the non-constant part" of non-constant irreducible polynomials. Each of
the parts can be trivial (of length 0). 

We show first that we can assume the $$R$$ part to be trivial. Let $$f = f_1*f_2*...*f_k$$ be any factorisation
of $$f$$ with a non-trivial $$R part$$, so that we can assume $$f_1=a \in R$$ and $$a$$ is irreducible. Let
$$f = g_1*g_2*...*g_s$$ be any other factorisation. We want to show that some $$g_i$$ is in $$R$$ and is
an associate of $$a$$. Suppose we've done that. Then we can discard $$f_1=a$$ and $$g_i$$ from the two factorisations,
and continue to do the same to the rest of the $$R$$ part of $$f_1*f_2*...*f_k$$ until it's trivial. At the same time,
the factorisation $$g_1*g_2*...g_s$$ must also run out of its $$R$$ part, otherwise we could do the same argument
with an irreducible $$R$$-element there and expect to find an associate in the first factorisation. We see then
that the lengths of the $$R$$ parts must be equal in any two factorisations, and the $$R$$ parts themselves match up
associate to associate; therefore it only remains to prove uniqueness for the non-constant parts  of the factorisations.

We now prove that an irreducible $$a\in R$$ that divides $$f$$ must find an associate in a factorisation $$f = g_1*g_2*...*g_s$$.
We prove this as a separate claim by induction on the degree of $$f$$. Let the leading coefficient of
$$g_i$$ be $$b_i$$ (if $$g_i \in R$$, then $$b_i=g_i$$), so that the leading coefficient of
 $$f$$ is \product{b_i}. $$R$$ is a UFD, so $$a$$ being irreducible means it's prime. Since $$a | f$$, $$a | \prod{b_i}$$,
and since it's prime, $$a | b_i$$ for some $$i$$. If $$g_i \in R$$, then $$a | g_i$$, and being irreducible $$g_i$$ must
be an associate of $$a$$ and we're done. But maybe $$g_i$$ is a non-constant polynomial $$b_ix^k + g'_i$$ where $$g'_i$$ is of degree $$<k$$. Since $$g_i$$ is irreducible and $$a | b_i$$, $$a$$ cannot divide $$g'_i$$. Now if we replace $$g_i$$ by $$g'_i$$ in the factorisation, that is the same thing as to subtract from $$f$$ the polynomial $$g_1*g_2*...*g_{i-1}*b_ix^k*{g_i+1}*...*g_s$$, which divides $$a$$ because $$b_i$$ does. We're left with a factorisation of some $$f'$$ of smaller degree, in which by the induction hypothesis $$a$$ finds an associate; this associate cannot be the new factor $$g'_i$$ because $$a$$ does not divide it, so it must be one of the original factors.


: $$g_i = c_kx^k + ... + c_0$$, and we know that its leading coefficient $$c_k$$ divides $$a$$: $$c_k = a*h$$ for some $$h\in R$$. Consider $$f - 


We show that factorisation is unique by a double induction: first by the degree of $$f(x)$$,
and then within the same degree by the minimal size of the "$$R$$ part" in any factorisation of $$f$$.  
So, given $$f(x)$$ which has a factorisation with a nontrivial $$R$$ part, we will reduce it to one with
a smaller $$R$$ part; and given $$f(x)$$ 







We first establish that it's enough to deal with primitive polynomials.

A polynomial in $$R[x]$$ is called *primitive* if the only members of $$R$$ that divide it
(that is, divide its every coefficient) are the units. An irreducible polynomial must be primitive, but
the converse is not necessarily true. Any non-constant polynomial $$f(x)i = a_nx^n + a_{n-1}x^{n-1} + ... + a_0$$
 can be written as a product
$$f(x) = cf'(x)$$, where $$c \in R$$ (possibly a unit) and $$f'$$ is primitive: we just keep extracting
more non-unit divisors out of $$f$$ until it becomes primitive; the process must end for the same reason
as in the existence proof above. This $$c$$, called the *content* of $$f$$, is unique up to a unit. To see
that, consider its factorisation into irreducibles: these irreducibles must all come from a factorisation
of $$a_0$$ (for example; could use any other coefficient) and they must be exactly the irreducibles of $$a_0$$
that are shared with all the other coefficients, and no more. A difference choice of a subset of irreducibles of
$$a_0$$ will either give a product that does not divide all of $$f$$, or leave behind an $$f'$$ that is not primitive.

Now suppose there are two different factorisations of $$f$$. Each of them has its "$$R$$ part" and its "non-constant part". 

