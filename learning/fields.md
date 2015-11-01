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

## Introduction to the course

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

## Pseudo Algebraically Closed Fields

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
common fixed field $$Q(\underline{\sigma}) = \{x \in \tilde{Q}: x =\sigma_1(x)=\dots = \sigma_n(x)\}$$ is a PAC (a theorem by Jarden).

## Hilbertian Fields

Next we discuss "Hilbertian", which is an arithmetical property of the field, as opposed to PAC which is a geometric property.

Definition. $$K$$ is called Hilbertian if for every $$f(x,y) \in K[X,Y]$$ that is irreducible in $$K(X)[Y]$$ (in other words, it's irreducible
and has positive content in $$Y$$), there's an infinite number of $$a\in K$$ such that $$f(a,Y)$$ is irreducible in $$K[Y]$$.

There's an equivalent geometric definition but it's not very helpful: for every $$\phi:C\to P_K^1$$ over $$K$$ that is dominant (its image includes
an open dense set) and $$C$$ is irreducible, there's an infinite number of $$a \in P_K^1$$ such that $$\phi^{-1}(a)$$ is $$K$$-irreducible.

Example. An algebraically closed field is not Hilbertian. In some sense "Hilbertian" is almost opposed to "algebraically closed".

Example. $$R$$ is not Hilbertian, for example consider $$Y^3-X$$ or any other polynomial of degree 3.

Example. $$Q_p$$ (the $$p$$-adics) is not Hilbertian.

Hilber's Irreducibility Theorem: $$Q$$ is Hilbertian (and so is any number field = a finite extension of $$Q$$).

Example of an application of Hilbert's Irreducibility theorem. Does the ring $$Q[x]$$ satisfy the Dirichlet theorem for arithmetical series,
that is, is it true that for every $$a,b \in Q[x]$$ co-prime there's $$c \in Q[x]$$ such that $$a(x)+cb(x)$$ is irreducible?

Answer: yes. Assuming $$a,b$$ are co-prime, $$a(x)+Yb(x)$$ is irreducible, and so by Hilbert's Irreducibility Theorem there's an infinite number
of $$c\in Q$$ (a fortiori $$\in Q[x]$$) so that $$a(x)+cb(x)$$ is irreducible.

(Note: here we started from $$a+Yb$$ being irreducible in $$Q(X)[Y]$$, and applying Gauss's Lemma twice, moved to irreducibility in $$Q[X,Y]$$
and then in $$Q(Y)[X]$$ which is what we need to apply the theorem).

Another positive example: A function field, say $$K_0(t)$$ over a  base field $$K_0$$, is Hilbertian. This breaks down to two cases:

If $$K_0$$ is finite, the proof is analogous to Hilbert's Irreducibility Theorem.

If $$K_0$$ is infinite, this is a consequence of a theorem by Bertini: if there's a variety and an irreducible hyperplane intersecting it, then
for almost any hyperplane we choose (apart from a finite number of exceptions) the intersection is irreducible.

Example. $$Q^{\text{cycl}}$$, which is $$Q(e^{\frac{2\pi i}{r}}: r=1,2,\dots)$$, is Hilbertian (result by Kuyk).

**Exercise**: $$Q^{\text{sol}}$$ is the composition in $$C$$ of all the finite extensions $$N/Q$$ with a solvable Galois group. Prove that $$Q^{\text{sol}}$$
is not Hilbertian. This can be proved directly or using what the Galois theorem says about a solvable extension.

Another positive example. Theorem by Weissover(?): If $$K$$ is Hilbertian, $$N/K$$ a Galois extension (finite or infinite), then every proper extension of $$N$$
is Hilbertian. (Note: even though $$N$$ itself might well not be!). So for example any finite extension of $$Q^{\text{sol}}$$ above is Hilbertian. The field
$$Q^{\text{tot,R}}(\sqrt{-1})$$ mentioned above in the PAC section is a finite extension of $$Q^{\text{tot,R}}$$, and so is Hilbertian.

## $$\omega$$-free Groups

Now we discuss "$$\omega$$-free", and although this is a group-theoretic property, we give a field theory definition. We'll say $$\text{Gal}(K)$$ is $$\omega$$-free
if given any two finite groups $$G,H$$ and an epimorphism $$\phi:G \to H$$ and a finite Galois extension $$L/K$$ with $$\text{Gal}(L/K)\cong H$$, there exists a Galois
extension $$N/K$$ with $$\text{Gal}(N/K) \cong G$$ and the restriction map from $$\text{Gal}(N/K)$$ to $$\text{Gal}(L/K)$$ corresponds to $$\phi$$ under these
isomorphisms.

The case $$H=1$$ shows that the inverse Galois problem is solvable under a Hilbertian PAC field. Unfortunately, $$Q$$ is not PAC.

We noted earlier that $$Q^{tot,R}(\sqrt{-1})$$ is noth PAC and Hilbertian, so we can conclude that $$\text{Gal}(Q^{tot,R}(\sqrt{-1}))$$ is $$\omega$$-free, that is
free in the category of profinite groups (? not sure I wrote that down right).

Open problem: What can be said about $$\text{Gal}(Q)$$? We don't even know what its continuous finite quotient groups are.

Open problem: Is $$Q^{\text{sol}}$$ PAC?

## Infinite Galois Theory

### Goal: Extend Galois theory to infinite extensions.

Let $$L/K$$ be an algebraic extension. We'll say that $$L/K$$ is separable if $$L = \bigcup_{i \in I}{L_i}$$ and each $$L_i$$ is separable.
Similarly, $$L/K$$ is normal/Galois if it's a union of finite normal/Galois extensions. Clearly, $$L/K$$ is Galois iff it's separable and normal.

Definition. $$\text{Gal}(L/K) = \{ \sigma \in L: \text{\sigma is an automorphism of }L \text{ constant on }K \} = \text{Aut}_k(L)$$

Example 1. $$K^{\text{sep}} = \{ x \in \tilde{K}: x\text{'s irreducible polynomial is separable} \}$$

$$K^{\text{sep}}$$ is Galois. That it's separable is clear, and it's normal because if an element is separable, so are all its conjugates.

Definition. $$\text{Gal}(K) = \text{Gal}(K^{\text{sep}}/K) = Aut_K(\tilde{K}).

**Exercise**: Explain the last equality above - why can we move from $$K^{\text{sep}}$$ to $$\tilde{K}$$?

Example. The maximal abelian extension of $$K$$: $$K^{\text{ab}} = \bigcup_{L/K}L$$ over all finite Galois extensions with abelian Galois groups.
$$K^{\text{ab}}/K$$ is Galois.

**Exercise**. $$\text{Gal}(K^{\text{ab}})$$ is abelian, and $$K^{\text{ab}}$$ is maximal under this property, i.e. any other extension
(even an infinite one) with an abelian Galois group is in $$K^{\text{ab}}$$.


**Exercise**. $$L = Q(\sqrt{p} \| p \text{ is prime})$$. Prove that $$\text{Gal}(L/Q) = (Z/2Z)^{\aleph_0}$$.

### Fundamental Theorem of Galois Theory

### Example of why it fails in infintie exntesions

Second example

### Krull topology

**Exercise**. Prove that the above defines a basis for a topology.

### Proving the Fundamental Theorem of Galois Theory




## Exercises

**Exercise**: $$Q^{\text{sol}}$$ is the composition in $$C$$ of all the finite extensions $$N/Q$$ with a solvable Galois group. Prove that $$Q^{\text{sol}}$$
is not Hilbertian. 

The polynomial $$Y^2-X$$ is irreducible in $$Q^\text{sol}(X)[Y]$$. But for any value $$X=a$$, $$Y^2-a$$ cannot be irreducible, because $$Q^\text{sol}$$
contains all radical extensions of $$Q$$ and is itself closed under radical extensions, so it contains a square root of $$a$$.

**Exercise**: Explain the last equality above - why can we move from $$K^{\text{sep}}$$ to $$\tilde{K}$$?

$$\tilde(K)/K^\text{sep}$$ is a purely inseparable extension. Suppose it's nontrivial and then $$K$$ has nonzero characteristic $$p$$. It's known that if
$$f(X) \in K[X]$$ is a polynomial that is inseparable in an extension $$E/K$$, then $$f(X) = g(X^p)$$ for another polynomial $$g(X)\in K[X]$$. If $$g$$ itself
is inseparable, this can be iterated until we get to $$f(X) = h(X^{p^n})$$ and $$h(X) \in K[X]$$ is separable. In our case $$E/K$$ is $$\tilde{K}/K^\text{sep}$$,
and we conclude that if $$a$$ is an inseparable element of this extension, then $$a^{p^n}$$ is a zero of a separable polynomial with coefficients in $$K^\text{sep}$$,
meaning that $$a^{p^n}$$ itself is in $$K^\text{sep}$$.

So the extension  $$\tilde{K}/K^\text{sep}$$ is obtained by adjoining to $$K^\text{sep}$$ all possible $$p^n$$-th roots. Then every automorphism of $$\tilde{K}$$
that fixes $$K^\text{sep}$$ must permute the roots of polynomials in $$K^\text{sep}[X]$$. But each element  $$a \in \tilde{K}$$ is a root of some such polynomial $$X^{p^n}-a^{p^n}$$,
and since this polynomial splits as $$(X-a)^p$$ (here we use the characteristic of $$K$$), it only has one root, and every automorphism that fixes $$K^\text{sep}$$ must fix $$a$$.
It follows that if an automorphism of $$\tilde(K)$$ fixes $$K^\text{sep}$$, it is an identity, or in other words, the restriction map from $$\text{Aut}_K(\tilde{K})
to $$\text{Aut}_K(K^\text{sep}) = \text{Gal}(K^{\text{sep}}/K)$$ is an isomorphism.


**Exercise**. $$\text{Gal}(K^{\text{ab}})$$ is abelian, and $$K^{\text{ab}}$$ is maximal under this property, i.e. any other extension
(even an infinite one) with an abelian Galois group is in $$K^{\text{ab}}$$.


**Exercise**. $$L = Q(\sqrt{p} \| p \text{ is prime})$$. Prove that $$\text{Gal}(L/Q) = (Z/2Z)^{\aleph_0}$$.

**Exercise**. Prove that the above defines a basis for a topology.















