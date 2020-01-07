# Adjointness, norm, and you...

This document is very much a work-in-progress braindump, so please judge it accordingly.

## Adjoint

Adjointness expresses a condition that is essentially universal in mathematics, category theory, probability, logic, optimization, machine learning.

What is adjointness? Depends on the context.

[This page](http://www.reproducibility.org/RSF/book/bei/conj/paper_html/index.html) is illuminating.

I like this definition: "adjoint operator ... back-projects information from data to the underlying model."

Essentially, it carries information about possible states at a point in time so that we can go back and forth. This allows you do optimizations that are otherwise not possible.

## Inverse
Adjointness is only a part of the story. One often sees equations of the following form `inv(x) = adjoint(x)/norm(x)`. Once you have `adjoint` and `norm`, you magically get `inverse`.

## Norm
Norm essentially allows you do a 1-on-1 comparisons. Yes, database normalization falls in this category.

## Category theory
Adjoint functors are the foundation of "category theory". Adjoint functors capture [solutions to optimization problems](https://en.wikipedia.org/wiki/Adjoint_functors#Solutions_to_optimization_problems).

> The slogan is "Adjoint functors arise everywhere".

> — Saunders Mac Lane, Categories for the Working Mathematician


## Monads
Monads can be expressed in terms of [adjoint functors](http://www.stephendiehl.com/posts/adjunctions.html).


## Linear logic

Linear logic is a logic of resources, i.e. where you have to use facts to derive new facts. E.g. if you have a fact, `I have $1` and a rule `$1 -> ice cream`, you have to spend the dollar to get an ice cream.
It can also be seen as a ["the interpretation of classical logic by replacing Boolean algebras by C*-algebras"](https://en.wikipedia.org/wiki/Linear_logic).


## C*-algebras

[C*-algebras](https://en.wikipedia.org/wiki/C*-algebra) are 

## Entity component system
This might be a stretch but I see some of these ideas present even in the context of [entity component systems](https://en.wikipedia.org/wiki/Entity_component_system).
In ECS, instead of using [arrays of structures, you use structure of arrays](https://en.wikipedia.org/wiki/AoS_and_SoA) which to me sounds like an adjoint. In ECS, your data is normed so that it allows for `1-on-1` comparisons.

## Chu spaces
[Chu spaces](https://en.wikipedia.org/wiki/Chu_space) are essentially matrices with certain limitation [(no duplicate rows or columns)](http://math.chapman.edu/~jipsen/sysmics/slides/Pratt4thSYSMICS2018.pdf). They can be used to model [linear logic](http://chu.stanford.edu/live/#7).

## Constructive mathematics

Constructive mathematics is mathematics without the law of excluded middle. To prove something, you need to show it's existence. These is a connection between [constructive mathematics and linear logic](https://arxiv.org/abs/1805.07518).

## Automatic differentiation

Adjointness shows up in the context of [automatic differentiation](https://medium.com/@marksaroufim/automatic-differentiation-step-by-step-24240f97a6e6).
The algebraic foundation of automatic differentiation relies on dual numbers, i.e. numbers of the form `a + b * epsilon`. `Epsilon` is a constant such that `epsilon^2=0 but epsilon != 0`. This is similar to imaginary unit except it squares to 0 instead of -1. 

The problem with differentiation as it's taught in school is that the expression length grows exponentially which makes it prohibitively slow for computation. 

This [blog post](https://blog.demofox.org/2014/12/30/dual-numbers-automatic-differentiation/) is pretty decent.

## Probability

Vladimir Vovk has developed theory of probability that can be easily recast in terms of linear logic.




