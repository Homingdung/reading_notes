[TOC]

# 混沌简史

> 参考刘华杰的《百年非线性动力学混沌思想简史》

+ 1898年法国数学家阿达马（J.-S Hadamard） 发表论文“负曲率曲面上的测地流”。他证明了负曲率曲面上的测地流存在“对初始条件的敏感依赖性”。



+ 1906年法国科学史家，科学哲学家迪昂认为初始条件中出现的微笑不确定性将导致很大的不确定性。



+ 彭加勒的贡献：（1）定性动力学 （2）遍历理论，概率思想，回复性理论 （3）周期轨道的存在性，近周期轨处流的结构的详细分析 （4）分岔理论

+ 1921年美国哈佛大学数学集莫尔斯（H. M. Morse） 发文证明存在“不连续型的回复性测地流”。
+ 1913年伯克霍夫（G. D. Birkhoff），证明彭加勒几何定理

+ 1927年范德坡与范德马克发现著名的“分频现象”。
+ KAM定理
+ 同宿轨道与斯美尔马蹄
+ 杜芬方程与上田吸引子
+ 洛伦兹的确定性非周期流

# Overview

Types of Dynamical systems:

+ Differential Equations *describing the evolution of systems in continuous time*
+ Iterated Maps (Difference Equation) *arising in problems where time is discrete*

An Important Idea:

The differential equation can be interpreted as a vector field on the phase space.

1. Euler's method:

​     $x_{n+1}=x_{n}+f(x_n)\Delta t$

2. Refinements: 

   $\hat x=x_n+f(x_n)\Delta t$

   $x_{n+1}=x_n+\frac{1}{2}(f(x_n)+f(\hat x_{n+1}))\Delta t$

3. Runge-Kutta method:

   $k_1=f(x_n)\Delta t$

   $k_2=f(x_n+\frac{1}{2}k_1)\Delta t$

   $k_3=f(x_n+\frac{1}{2}k_2)\Delta t$

   $k_4=f(x_n+k_3)\Delta t$

   $x_{n+1}=x_{n}+\frac{1}{6}(k_1+2k_2+2k_3+k_4)$



# Bifurcations

> Fixed points can be created or destroyed, or their stability can change. These qualitative changes in the dynamics are called bifurcations, and the parameter values at which they occur are called bifurcation points.

**Bifurcation theory** is the [mathematical](https://en.wikipedia.org/wiki/Mathematics) study of changes in the qualitative or [topological](https://en.wikipedia.org/wiki/Topological) structure of a given [family](https://en.wikipedia.org/wiki/Family_of_curves), such as the [integral curves](https://en.wikipedia.org/wiki/Integral_curve) of a family of [vector fields](https://en.wikipedia.org/wiki/Vector_field), and the solutions of a family of [differential equations](https://en.wikipedia.org/wiki/Differential_equation).



$\dot x=\mu x-x^2,\dot y = -y$ , transcritical

$\dot x=\mu x-x^3,\dot y=-y$, supercritical pitchfork

$\dot x=\mu x+x^3,\dot y=-y$,subcritical pitchfork





# Index Theory

> The index of a closed curve C is an integer that measures the **winding** of the vector field on C. The index also provides information about any fixed points that might happen to lie inside the curve.

To compute the index, we do not need to know the vector field everywhere; we only need to know it along C.



# Limit Cycle

Van der Pol equation:

$\ddot x +\mu(x^2-1)\dot x +x=0$

Lienard System:

> This equation is a generalization of the van der Pol oscillator

$\ddot x +f(x)\dot x+g(x)=0$

Lienard Theorem:

Suppose that f(x) and g(x) satisfy the following conditions:

1. f(x) and g(x) are continuously differnetiable for all x;
2. g(-x)=-g(x) for all x (i.e., g(x) is an odd function);
3. g(x) >0 for x>0;
4. f(-x)=f(x) for all x (i.e., f(x) is an even function)
5. The odd function $F(x)=\int_0^x f(u)du$ has exactly one positive zero at x=a, is negative for 0<x<a, is positive and nondecreasing for x>a, and $F(x)\to\infin$ as $x\to \infin$.

Then the system has a unique, stable limit cycle surrounding the origin in the phase plane.





Based on the Lienard's Theorem, we could prove that the van der Pol equation has a unique, stable limit cycle

Weakly Nonlinear Oscillators:

$\ddot x+x+\epsilon h(x,\dot x)=0$

$0 \leq \epsilon \lt\lt 1$ and $h(x,\dot x)$ is an arbitrary smooth function.

Two fundamental examples:

1. van der Pol equation: $\ddot x+x+\epsilon(x^2-1)\dot x=0$
2. Duffing equation: $\ddot x+x+\epsilon x^3=0$

Regular Perturbation Theory

> In [mathematics](https://en.wikipedia.org/wiki/Mathematics) and [physics](https://en.wikipedia.org/wiki/Physics), **perturbation theory** comprises mathematical methods for finding an [approximate solution](https://en.wikipedia.org/wiki/Approximation_theory) to a problem, by starting from the exact [solution](https://en.wikipedia.org/wiki/Solution_(equation)) of a related, simpler problem.



For system $\ddot x+x+\epsilon h(x,\dot x)=0$ , we seek solutions in the form of a power series in $\epsilon$, so if $x(t,\epsilon)$ is a solution, we expand it as:

$x(t,\epsilon)=x_0(t)+\epsilon x_1(t)+\epsilon^2 x_2(t)+...$

Which means that $\epsilon$ was treated as a perturbation of our equation.

  Consider the weakly damped linear oscillator:

$\ddot x+2\epsilon \dot x+x=0$

$x(0)=0,\dot x(0)=1$



$[\ddot x_0+x_0]+\epsilon [\ddot x+2\dot x_0+x_1]+O(\epsilon^2)=0$



$O(1):\ddot x_0+x_0=0$

$O(\epsilon):\ddot x +2\dot x_0 + x_1=0$

Finally, the solution is 

$x(t,\epsilon)=sint-\epsilon tsint+O(\epsilon^2)$, by perturbation theory.







