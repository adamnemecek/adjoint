# Adjointness, norm, and you...
<!-- 
# all computable functions are continous 
 * https://cs.stackexchange.com/questions/80978/why-are-computable-functions-continuous
 * https://wikimpri.dptinfo.ens-cachan.fr/lib/exe/fetch.php?media=cours:upload:cours-2021-mpri-partie-i-goodmpri.pdf
* [Sometimes all functions are continuous](http://math.andrej.com/2006/03/27/sometimes-all-functions-are-continuous/#:~:text=A%20function%20is%20computably%20continuous,of%20are%20needed%20to%20determine%20.)


* diagonalization & markov property https://www.math.wustl.edu/~freiwald/309markov.pdf
* what is the meaning of orthogonality (in the context of c*?)
* qr decomposition = upper triangular * diagonal
* upper trianglular = modulo
* fixed point self-referentiality https://link.springer.com/article/10.1007/BF01405490
* bisimulation https://en.wikipedia.org/wiki/Bisimulation#Fixpoint_definition
 * Bisimilarity can also be defined in order theoretical fashion, in terms of fixpoint theory, more precisely as the greatest fixed point of a certain function defined below.
* https://eprints.illc.uva.nl/id/eprint/969/1/MoL-2015-28.text.pdf
* [Coalgebras, Chu Spaces, and Representations of Physical Systems](https://arxiv.org/abs/0910.3959)
* [Big Toy Models: Representing Physical Systems As Chu Spaces](https://arxiv.org/abs/0910.2393)

# non-commutative linear logic
* [On noncommutative extensions of linear logic](https://arxiv.org/pdf/1703.10092.pdf)

# reciprocal lattice 
 * https://en.wikipedia.org/wiki/Reciprocal_lattice
 * In physics, the reciprocal lattice represents the Fourier transform of another lattice 

# operator algebra
 * https://www.google.com/books/edition/Advances_in_Linear_Logic/ROEf2h5FvD4C?hl=en&gbpv=1&dq=%22operator+algebra%22+logic&pg=PA38&printsec=frontcover mentions operator algebras
* Optimal Implementation of Functional Programming Languages: https://github.com/asperti/BOHM1.1
* [OPERATOR ALGEBRAS AND THE OPERATIONAL SEMANTICS OF PROBABILISTIC LANGUAGES](https://cyberleninka.org/article/n/1010639)
* [Semantics for a Quantum Programming Language by Operator Algebras](https://arxiv.org/pdf/1412.8545.pdf)
* [Prolegomena to an Operator Theory of Computation](https://www.mdpi.com/2078-2489/11/7/349/htm)

* PROBABILITY, MARXISM, AND QUANTUM ENSEMBLES https://history.ubc.ca/wp-content/uploads/sites/23/2019/06/probability2012.pdf

* https://en.wikipedia.org/wiki/Spectral_theorem
* https://math.stackexchange.com/questions/1815161/relationship-between-fourier-coefficients-eigenvalues-and-the-spectrum-of-a-ri
*  prime number decomposition of the fourier transform https://arxiv.org/pdf/1410.2054v1.pdf
* https://math.stackexchange.com/questions/25126/is-it-possible-to-link-the-eigenvalues-of-a-matrix-to-the-fourier-transform-of-t

* https://en.wikipedia.org/wiki/Circulant_matrix
 * In numerical analysis, circulant matrices are important because they are diagonalized by a discrete Fourier transform, and hence linear equations that contain them may be quickly solved using a fast Fourier transform.[1] They can be interpreted analytically as the integral kernel of a convolution operator on the cyclic group {\displaystyle C_{n}}C_{n} and hence frequently appear in formal descriptions of spatially invariant linear operations.

fourier number multiplication 
* https://math.stackexchange.com/questions/27444/integer-multiplication-using-fft

* [A Generic Logic for Proving Linearizability](https://artkhyzha.github.io/papers/fm16-extended.pdf)

* [The Fourier Transform As Diagonalization](https://www.science20.com/jon_lederman/fourier_transform_diagonalization)

[duality of state and observations](https://citeseerx.ist.psu.edu/viewdoc/download?doi=10.1.1.123.7075&rep=rep1&type=pdf)
[Parallel algorithms for finding common fixed points of paracontractions](https://www.researchgate.net/publication/233110331_Parallel_algorithms_for_finding_common_fixed_points_of_paracontractions)

* proof net & string diagram 
 * [Proof Diagrams for Multiplicative Linear Logic](https://arxiv.org/pdf/1606.09016.pdf)
 * 

# fixed point
* Fixed points are everywhere
* paxos is a fixed point algorithm
 * [Generalized Consensus and Paxos](https://www.semanticscholar.org/paper/Generalized-Consensus-and-Paxos-Lamport/fc3fbb4c76448e8968f8a19f076d133b2e7a2849)
* trace theory
 * [trace theory http://www.cas.mcmaster.ca/~cas724/2007/paper2.pdf

"fixed point" "reinforcement learning"

"fixed point" "dynamic programming"
* http://www.mit.edu/~dimitrib/Semicontractive_Lecture3.pdf

* https://people.eecs.berkeley.edu/~pabbeel/cs287-fa09/lecture-notes/lecture5-2pp.pdf

https://bartoszmilewski.com/2019/11/06/fixed-points-and-diagonal-arguments/

* given a map, you can decompose it to a nilpotent and a invertible part https://web.evanchen.cc/notes/Harvard-55a.pdf (page 30)

product of unions = sum of products (third kolmogorov axiom) really means that you have a norm?
* 1/2 or 1/sqrt(2) are really just pythagorean theorem

* contraction mapping + dynamic programming https://www.math.wustl.edu/~freiwald/309markov.pdf

## fixed point
* http://nlab-pages.s3.us-east-2.amazonaws.com/nlab/show/Lawvere's+fixed+point+theorem
* In ‘Diagonal arguments and Cartesian closed categories’ (Lawvere 69) we demystified the incompleteness theorem of Gödel and the truth-definition theory of Tarski by showing that both are consequences of some very simple algebra in the Cartesian-closed setting. 
* http://emis.matem.unam.mx/journals/TAC/reprints/articles/15/tr15.pdf
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

## Quantum mechanics
In the Linear logic section, we mention the idea of having to use axioms to derive new axioms. This is the core idea behind the [no-cloning theorem](https://en.wikipedia.org/wiki/No-cloning_theorem) as well. Futhermore the connections between C* (which has closure under adjoint and norm) and quantum mechanics are well documented (https://www.math.uchicago.edu/~may/VIGRE/VIGRE2009/REUPapers/Gleason.pdf).

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



<!--
# spectra + fixed points + eigenvalues
* https://math.stackexchange.com/questions/25126/is-it-possible-to-link-the-eigenvalues-of-a-matrix-to-the-fourier-transform-of-t
* https://en.wikipedia.org/wiki/Parseval%27s_theorem for unitary
* https://towardsdatascience.com/deriving-convolution-from-first-principles-4ff124888028
-->


