---
title: Lie Groups
---
<head>
    <script type="text/javascript"
            src="http://cdn.mathjax.org/mathjax/latest/MathJax.js?config=TeX-AMS-MML_HTMLorMML">
    </script>
</head>


Chapter 1

Motivation and matrix Lie groups

Lie groups are groups with elements that are able to vary continuously. That is, besides forming the product
of two elements or an inverse of an element, as expected in any group, you also have some way of moving continuously
from one element to another, and this continuous variation is compatible with the group structure. What does "compatible with the group structure mean"? Say you have an element A and an element B, and you form their product AB. Now you start slowly moving from A by some continuous path, and at the same time slowly moving from B somewhere else. Then, as A and B 




A Lie group is a differential manifold that is also a group, such that group multiplication and
inverse are infinitely differentiable functions. Such a manifold is often called a smooth manifold,
and infinitely differentiable functions are also known as smooth functions.

A straightforward example is \\( R^n \\) as an abelian group under addition. This is an \\( n- \\) dimensional
smooth manifold and addition with its inverse are obviously infinitely differentiable. 

For an example with a more interesting group operation, consider a circle of radius \\( 1 \\) around the origin on the
complex plane, which we think of topologically as \\( R^2 \\). Multiplication is well-defined for points 
on this circle as product of complex numbers of absolute value \\( 1 \\) . Under this operation, the
 circle forms a group.  
We can write out the operation in terms of pairs of real coordinates, and it is clearly infinitely differentiable.
  The inverse of \\( (a,b) \\) is \\( (a,-b) \\), and that is also obviously smooth. The circle is a \\( 1- \\) 
dimensional smooth submanifold of \\( R^2 \\).

This example is typical in many ways of interesting Lie groups. The smooth manifold - here a circle - lies inside a larger ambient Euclidean space (indeed any smooth manifold can be embedded in a Euclidean space). This space comes with a rich algebraic structure, but the Lie group and its operation are not too "nice" with respect to that structure. We see that the circle is not at all a linear subspace of \\( R^2 \\), for example; it is not closed under vector addition or scalar multiplication, and the group operation is not some sort of obvious and simple component-wise multiplication. If we forget the motivation that comes from complex numbers, and just view the product on the circle as defined by the formula \\( (a,b)(c,d) = (ad-bc, ac+bd) \\) on points in \\( R^2 \\), we see that it's a smooth function of some sort, but it doesn't seem immediately natural or obvious for \\( R^2 \\) as a Euclidean space. Viewed topologically as sitting inside a Euclidean space, a Lie group is a "curvy", non-linear object, and its group product is typically a very "curvy", non-linear function. 



Here is an example MathJax inline rendering \\( 1/x^{2} \\), and here is a block rendering: 
\\[ \frac{1}{n^{2}} \\]
