---
title: Fields Arithmetic
---
<head>
    <script type="text/javascript"
            src="http://cdn.mathjax.org/mathjax/latest/MathJax.js?config=TeX-AMS-MML_HTMLorMML">
    </script>
    <style>
      p {
        width: 960px;
      }  
    </style>
</head>

Oct 26, 2015

Introduction to the course

This course deals with the relationships between the arithmetic properties of fields
and the group-theoretic properties of their Galois groups. Given a field $$K$$, we can look
at the Galois group of some extension, $$\text{Gal}(N/K)$$, or even the absolute Galois group (to
be defined later) $$G(K)$$. What can be said about the connections between them?

A trivial example. $$\text{Gal}(K)=1$$ means there are no symmetries of roots of irreducible polynomials
$$\iff$$ $$K$$ is separably closed, meaning $$K$$ has no nontrivial separable extensions.

(Note: this isn't the same thing as $$K$$ being algebraically closed. An example to illustrate this:
$$F_p(t) \to F_p(t)^{sep} \to \widetilde{F_p(t)}$$. Here $$F_p(t)^{sep}$$ is the separable closure
of $$F_p(t)$$, and it is not equal to the algebraic closure $$\widetilde{F_p(t)}$$. To see this, consider
the element $$t^{1/p} \in \widetilde{F_p(t)}$$; its minimal polynomial is $$x^p-t$$ which factors as
$$(x-t^{1/p})^p$$, because $$x \to x^p$$ is a homomorphism, and so doesn't have distinct roots).

Less trivial example. If $$\text{Gal}(K)$$ is finite and nontrivial, what does that say about $$K$$? For
example, $$\text{Gal}(R)=Z/2Z$$, because the only automorphisms of $$C$$ that fix $$R$$ are $$1$$
and complex conjugation. 

Theorem (Artin-Schreier). $$A_1 < |\text{Gal}(K)| < \infty \iff$$

1. $$\text{char}K = 0$$.
2. There's an order on $$K$$ and $$K$$ is closed under that order (meaning every positive element has a square root).
3. $$\tilde{K} = K(\sqrt{-1})$$.
4. $$\text{Gal}(K) = Z/2Z$$.

So "philosophically" $$K$$ looks like $$R$$, although it can be rather different, for example the algebraic real numbers
(which is a countable field). We won't prove this theorem in this course.

The main theorem of the course, which we will strive to prove, is:

Theorem. Let $$K$$ be pseudo algebraically closed (PAC). Then $$K$$ is Hilbertian $$\iff \text{Gal}(K)$$ is $$\omega$$-free.
We proceed to give an introduction to "PAC", "Hilbertian" and "$$\omega$$-free".


