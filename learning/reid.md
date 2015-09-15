---
title: Undergraduate Commutative Algebra
---
<head>
    <script type="text/javascript"
            src="http://cdn.mathjax.org/mathjax/latest/MathJax.js?config=TeX-AMS-MML_HTMLorMML">
    </script>
</head>

Prove Gauss' Lemma.

Let $$A$$ be a UFD. $$f(x) \in A[x]$$ is called *primitive* if among elements of $A$ only units divide
$$f(x)$$ (or all its coefficients simultaneously, which is the same thing). In other words, if 
$$f(x) = a^nx^n+...+a^0$$, and $$s\in A$$ divides every $$a_i$$, then $$s$$ is a unit.

Let $$f(x), g(x)$$ be two primitive polynomials. Prove that $$f(x)g(x)$$ is primitive.

**Proof.** Let $$f(x) = a^nx^n+...+a^0, g(x) = b^mx^m+...+b^0. Let $$s\in A$$, and suppose
that $$s$$ is not a unit and $$s | fg$$. As $$A$$ is a UFD, we can write $$s = s_1*...*s_k$$ a product
of irreducibles, and any of them is still not a unit and divides $$fg$$. Therefore we can and so assume
that $$s$$ is irreducible. 

Since $$s$$ is not a unit and $$f,g$$ are primitive, $$s$$ cannot divide $$f$$
If we can show that $$s | f$$ or $$s | g$$, then $$s$$ must be a unit because $$f$$ and $$f$$ are primitive,
and that will be a cotradiction. So suppose that $$s \not | f$$, and we'll use that assumption to reach the
conclusion that $$s | g$$.

Now we want to establish that we can assume $$s \not | a_0$$. We know that there are some $$a_i$$
not divisible by $$s$$ because $$f$$ is primitive and $$s$$ is not a unit. If $$a_i$$ is the lowest-order 
coefficient in $$f$$ that does not divide $$s$$, we can discard from $$f$$ all the monomials that divide
$$s$$ because their contribution to $$fg$$ also divides $$s$$: after discarding them it will still be true that
$$s | fg$$. Then the lowest-order monomial in $$f$$ is now $$a_ix^i$$, and we can divide by $$x_i$$
which again does not change disivisibility by $$s$$.

Next, we can assume $$s$$ is irreducible: as $$A$$ is a UFD, we can write . Among $$s_i$$ at least one does not divide $$a_0$$, and it still divides $$fg$$, so we can use
that as the new $$s$$. 



$$\newcommand{\vect}[1]{\boldsymbol{#1}}$$ 
**Задача.** Доказать, что не существует четырех точек на плоскости так, чтобы все попарные расстояния
были нечетными целыми числами.

**Решение.** Предположим, что такие точки существуют, и рассмотрим их как четыре вектора в $$R^2$$: $$\vect{a},
\vect{b},\vect{c},\vect{d}$$. Мы можем положить $$\vect{d}=0$$, и тогда условие
о попарных расстояниях означает, что $$\|\vect{a}\|, \|\vect{b}\|, \|\vect{c}\|, \|\vect{a}-\vect{b}\|,
\|\vect{b}-\vect{c}\|, \|\vect{a}-\vect{c}\|$$ - все нечетные числа.

Рассмотрим следующую матрицу, которая состоит из скалярных произведений векторов $$\vect{a}, \vect{b}, \vect{c}$$:

$$ M = \begin{pmatrix} \langle\vect{a},\vect{a}\rangle & \langle\vect{a},\vect{b}\rangle & \langle\vect{a},\vect{c}\rangle \\
\langle\vect{b},\vect{a}\rangle & \langle\vect{b},\vect{b}\rangle & \langle\vect{b},\vect{c}\rangle \\
\langle\vect{c},\vect{a}\rangle & \langle\vect{c},\vect{b}\rangle  & \langle\vect{c},\vect{c}\rangle \end{pmatrix} $$

$$3\times 3$$ матрицу $$M$$ можно выразить как произведение матрицы $$3\times 2$$, содержащей координаты этих трех
векторов, и транспонированной к ней матрицы $$2 \times 3$$:

$$ M = \begin{pmatrix} \vect{a}_1 & \vect{a}_2 \\ \vect{b}_1 & \vect{b}_2 \\ \vect{c}_1 & \vect{c}_2 \end{pmatrix}
\begin{pmatrix} \vect{a}_1 & \vect{b}_1 & \vect{c}_1 \\ \vect{a}_2 & \vect{b}_2 & \vect{c}_2 \end{pmatrix} $$

Ранг любой из этих двух матриц не может быть больше $$2$$, а следовательно и ранг произведения не больше $$2$$. Значит, матрица $$M$$
вырождена, и $$\det M = 0$$. Следовательно, детерминант матрицы $$2M$$ тоже обязан быть $$0$$:

$$ \det 2M = \begin{vmatrix} 2\langle\vect{a},\vect{a}\rangle & 2\langle\vect{a},\vect{b}\rangle & 2\langle\vect{a},\vect{c}\rangle \\
2\langle\vect{b},\vect{a}\rangle & 2\langle\vect{b},\vect{b}\rangle & 2\langle\vect{b},\vect{c}\rangle \\
2\langle\vect{c},\vect{a}\rangle & 2\langle\vect{c},\vect{b}\rangle & 2\langle\vect{c},\vect{c}\rangle \end{vmatrix} = 0$$

Присмотримся к этой матрице $$2M$$, и выразим ее элементы через нормы векторов:

* На диагонали в ней стоят числа вида $$2\langle\vect{a},\vect{a}\rangle = 2\|\vect{a}\|^2$$.
* Во всех остальных ячейках находятся числа вида $$2\langle\vect{a},\vect{b}\rangle = \|\vect{a}\|^2 + \|\vect{b}\|^2 - \|\vect{a}-\vect{b}\|^2$$ 
(это просто-напросто теорема косинусов).

Все нормы векторов в этих выражениях - нечетные целые числа согласно нашему предположению. А квадрат нечетного числа
всегда равен $$1$$ по модулю $$8$$, как легко убедиться. Значит, по модулю $$8$$ все эти $$\|\vect{a}\|^2, \|\vect{a}-\vect{b}\|^2$$ итд. равны $$1$$. 
Используя выражения для членов матрицы выше, мы видим, что

$$2M \equiv \begin{pmatrix} 2 & 1 & 1 \\ 1 & 2 & 1 \\ 1 & 1 & 2 \end{pmatrix} \mod 8$$

Детерминант этой матрицы легко можно вычислить вручную: он равен $$4$$. Следовательно, $$\det 2M \equiv 4 \mod 8$$, что противоречит
полученному ранее результату $$\det 2M = 0$$, что и требовалось доказать.
