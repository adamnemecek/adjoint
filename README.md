# Adjointness, norm, and you...
<!-- 
* diagonalization & markov property https://www.math.wustl.edu/~freiwald/309markov.pdf
* what is the meaning of orthogonality (in the context of c*?)
* qr decomposition = upper triangular * diagonal
* upper trianglular = modulo

[duality of state and observations](https://citeseerx.ist.psu.edu/viewdoc/download?doi=10.1.1.123.7075&rep=rep1&type=pdf)
[Parallel algorithms for finding common fixed points of paracontractions](https://www.researchgate.net/publication/233110331_Parallel_algorithms_for_finding_common_fixed_points_of_paracontractions)

"fixed point" "reinforcement learning"

"fixed point" "dynamic programming"
* http://www.mit.edu/~dimitrib/Semicontractive_Lecture3.pdf

* https://people.eecs.berkeley.edu/~pabbeel/cs287-fa09/lecture-notes/lecture5-2pp.pdf

https://bartoszmilewski.com/2019/11/06/fixed-points-and-diagonal-arguments/

* given a map, you can decompose it to a nilpotent and a invertible part https://web.evanchen.cc/notes/Harvard-55a.pdf (page 30)

product of unions = sum of products (third kolmogorov axiom) really means that you have a norm?
* 1/2 or 1/sqrt(2) are really just pythagorean theorem
-->

This document is very much a work-in-progress braindump, so please judge it accordingly.

## Adjoint

Adjointness expresses a condition that is essentially universal in mathematics, category theory, probability, logic, optimization, machine learning. It captures this difference between global and local. Adjointness operates locally, norm operates globally.

What is adjointness? Depends on the context.

[This page](http://www.reproducibility.org/RSF/book/bei/conj/paper_html/index.html) is illuminating.

I like this definition: 
> "adjoint operator ... back-projects information from data to the underlying model."

Essentially, it carries information about possible states at a point in time so that we can go back and forth. This allows you do optimizations that are otherwise not possible.

One can also see it as the _adversarial relationship_ between two things. This relationship is so common that once you see it, you can't unsee it.

_Adjointness expresses a condition that allows for inference, causality, and optimization_. If the adjoint condition is met, information from one dimension can be used to make predictions about another dimension.

Nilpotence is another way of viewing adjointness. 

## Inverse
Adjointness is only a part of the story. One often sees equations of the following form `inverse(x) = adjoint(x)/norm(x)`. Once you have `adjoint` and `norm`, you magically get `inverse`.

## Norm
Norm essentially allows you do a 1-on-1 comparisons. Yes, database normalization falls in this category. Another way of looking at this is that by dividing by norm, you get some in some sense _canonical form_ of the object in question. What is a canonical form? Computation. 

> Systems of formal logic, such as type theory, try to transform expressions into a canonical form which then serves as the end result of the given computation or deduction.

from [ncatlab](https://ncatlab.org/nlab/show/canonical+form).

## Identity
> Every diagonal argument -- Cantor's theorem, Russell's paradox, Gödel's incompleteness theorem, the halting problem, the Y combinator, Curry's paradox, etc. -- uses the same basic trick. This trick is expressed explicitly by Lawvere's fixed point theorem: https://ncatlab.org/nlab/show/Lawvere%27s+fixed+point+theorem

[source](https://twitter.com/shachaf/status/1183934586775957504)

As stated above `inverse(x) = adjoint(x)/norm(x)`. We add an additional constraint, the unitarity `identity(x) = x/inv(x)`.

## Linear algebra
The inner and outer product can be expressed succinctly in terms of adjoints.
```julia
inner(a) = a'*a
outer(a) = a*a'
```

## Fourier transform

You get the inverse of a Fourier transform by taking the adjoint of the sum (in this case, you do conjugate the exponents) and divide it by a norm `1/length(signal)`. Notice how adjoint operates locally (on the single exponents) and the norms operates globally (it knows how many elements are in the signal.


## Category theory
Adjoint functors are the foundation of "category theory". Adjoint functors capture [solutions to optimization problems](https://en.wikipedia.org/wiki/Adjoint_functors#Solutions_to_optimization_problems).

> The slogan is "Adjoint functors arise everywhere".

> — Saunders Mac Lane, Categories for the Working Mathematician


## Monads
Monads can be expressed in terms of [adjoint functors](http://www.stephendiehl.com/posts/adjunctions.html).

## Linear logic

Linear logic is a logic of resources, i.e. you have to use facts to derive new facts. E.g. if you have a fact, `I have $1` and a rule `$1 -> ice cream`, you have to spend the dollar to get an ice cream.
It can also be seen as a ["the interpretation of classical logic by replacing Boolean algebras by C*-algebras"](https://en.wikipedia.org/wiki/Linear_logic). Linear logic can therefore be as a logic with `adjoint` and `norm`. See how linear logic maps to Chu spaces for further detail. Linear logic has been futher expanded into [adjoint logic](https://www.cs.cmu.edu/~fp/papers/adjoint18b.pdf).
The Rust borrow checker is based on a subset of linear logic. This is what allows Rust to reason about resource ownership statically.

## Entity component system
This might be a stretch but I see some of these ideas present even in the context of [entity component systems](https://en.wikipedia.org/wiki/Entity_component_system). ECS is used heavily in games but it has applications beyond that.
In ECS, instead of using [arrays of structures, you use structure of arrays](https://en.wikipedia.org/wiki/AoS_and_SoA) which to me sounds like an adjoint. In ECS, your data is normalized so that it allows for `1-on-1` comparisons.

## Chu spaces
[Chu spaces](https://en.wikipedia.org/wiki/Chu_space) are essentially matrices with certain limitation [(no duplicate rows or columns)](http://math.chapman.edu/~jipsen/sysmics/slides/Pratt4thSYSMICS2018.pdf). They can be used to model [linear logic](http://chu.stanford.edu/live/#7).

I think of Chu spaces as objects with the good properties of tensors (covariance, contravariance) without being a pain-in-the-ass to work with.

Check out this [blog post](https://boxbase.org/entries/2019/jul/15/chu-construction/).

## Constructive mathematics
Constructive mathematics is mathematics without the law of excluded middle. To prove something, you need to show it's existence. These is a connection between [constructive mathematics and linear logic](https://arxiv.org/abs/1805.07518).

## Automatic differentiation

Adjointness shows up in the context of [automatic differentiation](https://medium.com/@marksaroufim/automatic-differentiation-step-by-step-24240f97a6e6).
The algebraic foundation of automatic differentiation relies on dual numbers, i.e. numbers of the form `a + b * epsilon`. `Epsilon` is a constant such that `epsilon^2=0 but epsilon != 0`. This is similar to imaginary unit except it squares to 0 instead of -1.

The problem with differentiation as it's taught in school is that the expression length of the derivative grows exponentially which makes it prohibitively slow for computation.

This [blog post](https://blog.demofox.org/2014/12/30/dual-numbers-automatic-differentiation/) is pretty decent.

## Probability

Vladimir Vovk has developed theory of probability that can be easily recast in terms of linear logic.

Roughtly, translated [Kolmogorov's 3 axioms](https://en.wikipedia.org/wiki/Probability_axioms) can be read as follows:
1.) norm
2.) unitarity
3.) adjointness (notice how we turn the inside product into the outside sum) 
 

## Potential applications
I've been thinking about a new representation of polynomials. Instead of using zeros, one would use a sequence of dual numbers that capture the minima and maxima of the polynomial. Theoretically, one could then evaluate polynomials by some smooth interpolation between two neighbouring points. Dual numbers allow you to capture the curvature at point naturally so it would make sense that this should be possible.

## Related concepts (these will be explained layer)
* Young tableau
* Non-commutative logic
* Message passing + adjoint logic
* [backpropagation (and others)](https://twitter.com/breandan/status/1324566706908483586)
* spectral theorem






