---
title: Lie Groups
---
<head>
    <script type="text/javascript"
            src="http://cdn.mathjax.org/mathjax/latest/MathJax.js?config=TeX-AMS-MML_HTMLorMML">
    </script>
</head>


**Задача.** Доказать, что не существует четырех точек на плоскости так, чтобы все попарные расстояния
были нечетными целыми числами.

**Решение.**

$$\newcommand{\vect}[1]{\boldsymbol{#1}}$$

Предположим, что такие точки существуют, и рассмотрим их как четыре вектора в $$R^2$$: $$\vect{a},
\boldsymbol{b},\boldsymbol{c},\boldsymbol{d}$$. Мы можем положить $$\boldsymbol{d}=0$$, и тогда условие
о попарных расстояниях означает, что $$\|\boldsymbol{a}\|, \|\boldsymbol{b}\|, \|\boldsymbol{c}\|, \|\boldsymbol{a}-\boldsymbol{b}\|,
\|\boldsymbol{b}-\boldsymbol{c}\|, \|\boldsymbol{a}-\boldsymbol{c}\|$$ - все нечетные числа.

Рассмотрим следующую матрицу, которая состоит из скалярных произведений векторов $$\boldsymbol{a}, \boldsymbol{b}, \boldsymbol{c}$$:

$$ M = \begin{pmatrix} \langle\vect{a},\vect{a}\rangle & \langle\vect{a},\vect{b}\rangle & \langle\vect{a},\vect{c}\rangle \\
\langle\vect{a},\vect{a}\rangle & \langle\vect{a},\vect{a}\rangle & \langle\vect{a},\vect{a}\rangle \\
\langle\vect{a},\vect{a}\rangle & \langle\vect{a},\vect{a}\rangle  & \langle\vect{a},\vect{a}\rangle \end{pmatrix} $$

Нас интересует детерминант этой матрицы.

С одной стороны, $$3\times 3$$ матрицу $$M$$ можно выразить как произведение матрицы $$3\times 2$$, содержащей координаты этих трех
векторов, и транспонированной к ней матрицы $$2 \times 3$$:

$$ M = \begin{pmatrix} \vect{a}_1 & \vect{a}_2 \\ \vect{b}_1 & \vect{b}_2 \\ \vect{c}_1 & \vect{c}_2 \end{pmatrix}
\begin{pmatrix} \vect{a}_1 & \vect{b}_1 & \vect{c}_1 \\ \vect{a}_2 & \vect{b}_2 & \vect{c}_2 \end{pmatrix} $$

