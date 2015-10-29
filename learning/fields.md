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

Theorem (Artin-Schreier). $$\text{Gal}(K)$$ is finite and nontrivial $$\iff$$

1. $$\text{char}K = 0$$.
2. There's an order on $$K$$ and $$K$$ is closed under that order (meaning every positive element has a square root).
3. $$\tilde{K} = K(\sqrt{-1})$$.
4. $$\text{Gal}(K) = Z/2Z$$.

So "philosophically" $$K$$ looks like $$R$$, although it can be rather different, for example the algebraic real numbers
(which is a countable field). We won't prove this theorem in this course.

The main theorem of the course, which we will strive to prove, is:

Theorem. Let $$K$$ be pseudo algebraically closed (PAC). Then $$K$$ is Hilbertian $$\iff \text{Gal}(K)$$ is $$\omega$$-free.
We proceed to give an introduction to "PAC", "Hilbertian" and "$$\omega$$-free".

Definition. $$K$$ is called pseudo algebraically closed (PAC) if every curve $$C$$ over $$K$$ that is totally irreducible
(meaning irreducible over the algebraic closure) has a point in the field, that is, $$C(K) \ne \emptyset$$.

Equivalently: every polynomial $$f \in K[X,Y]$$ that is totally irreducible (irreducible in $$\tilde{K}[X,Y]$$) has an
infinity of pairs $$(a,b)\in K^2$$ such that $$f(a,b)=0$$.

(Note: the difference between "one point" in the first definition and "the infinity of pairs" in the second is due to the fact
that we can delete a finite number of points from a curve and it still remains a curve).

$$R$$ is not a PAC: the polynomial $$y^2+x^2+1$$ is irreducible over the closure. It follows that any $$K\subset R$$ is also not
PAC, including $$Q$$.

$$C$$ is a trivial example of a PAC field, as is any other algebraically closed field, due to the Nullenstensatz.

It's not easy to show nontrivial examples and prove they're PAC. Two examples without proofs:

Example 1. An algebraic element $$x$$ over $$Q$$ is called totally real if for any embedding $$Q(x)\to C$$ the image of $$x$$ is in $$R$$.
Equivalently, the minimal irreducible polynomial of $$x$$ has only real roots. $$\sqrt{2}$$ is totally real, while $$\sqrt[3]{2}$$ is not.
The field $$Q^{\text{tot,R}}(\sqrt{-1})$$ is PAC (a theorem by Monet and Pop).

Example 2. $$\text{Gal}(Q)$$ is a topological group (we won't discuss the topology now), and it's compact. Therefore there's a Haar measure
on it which is a probability measure. Theorem: with probability 1, if we choose $$\sigma_1, \dots, \sigma_n \in \text{Gal}(Q)$$, then their
common fixed field $$Q(\underline{\sigma}} = \{x \in \tilde{Q}: x =\sigma_1(x)=\dots = \sigma_n(x)\}$$ is a PAC (a theorem by Jarden).

Next we discuss "Hilbertian", which is an arithmetical property of the field, as opposed to PAC which is a geometric property.

Definition. $$K$$ is called Hilbertian if for every $$f(x,y) \in K[X,Y]$$ that is irreducible in $$K(X)[Y]$$ (in other words, it's irreducible
and has positive content in $$Y$$), there's an infinite number of $$a\in K$$ such that $$f(a,Y)$$ is irreducible in $$K[Y]$$.

There's an equivalent geometric definition but it's not very helpful: for every $$\phi:C\to P_K^1$$ over $$K$$ that is dominant (its image includes
an open dense set) and $$C$$ is irreducible, there's an infinite number of $$a \in P_K^1$$ such that $$\phi^{-1}(a)$$ is $$K$$-irreducible.

Example. An algebraically closed field is not Hilbertian. In some sense "Hilbertian" is almost opposed to "algebraically closed".

Example. $$R$$ is not Hilbertian, for example consider $$Y^3-X$$ or any other polynomial of degree 3.
Example. $$Q_p$$ (the $$p$$-adics) is not Hilbertian.

























