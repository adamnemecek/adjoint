# Adjointness, norm, and you...

This document is very much a work-in-progress braindump, so please judge it accordingly.

## Adjoint

Adjointness expresses a condition that is essentially universal in mathematics, category theory, probability, logic, optimization, machine learning.

What is adjointness? Depends on the context.

[This page](http://www.reproducibility.org/RSF/book/bei/conj/paper_html/index.html) is illuminating.

I like this definition: "adjoint operator ... back-projects information from data to the underlying model."

Essentially, it carries information about possible states at a point in time so that we can go back and forth.

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


## Chu spaces
[Chu spaces](https://en.wikipedia.org/wiki/Chu_space) are essentially matrices with certain limitation [(no duplicate rows or columns)](http://math.chapman.edu/~jipsen/sysmics/slides/Pratt4thSYSMICS2018.pdf). They can be used to model [linear logic](http://chu.stanford.edu/live/#7).

## Constructive mathematics

Constructive mathematics is mathematics without the law of excluded middle. To prove something, you need to show it. These is a connection between [constructive mathematics and linear logic](https://arxiv.org/abs/1805.07518).

## Concurrency



## Probability

Check out [Kolmogorov's three axioms of probability](https://en.wikipedia.org/wiki/Probability_axioms#Axioms) on Wikipedia. Translated, these mean:
1. 
2. you have a norm
3. you have an adjoint




