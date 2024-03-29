# Adjointness, norm, fixed point and you...
* [Join the `Adjoint` discord server](https://discord.gg/mr9TAhpyBW)
<!--
* what's the deal with vanishing traces?

* riesz representation theorem
    * see the wikipedia on anti-linearity it sure looks like a fourier?


* windwing number is very similar
   * [Brouwers Fixed Point Theorem Proof using Winding Numbers](https://math.stackexchange.com/questions/3674669/brouwers-fixed-point-theorem-proof-using-winding-numbers)

* de rahm twisted cohomology
  * [Twisted de Rham cohomology, homological definition of the integral and "Physics over a ring"]https://arxiv.org/abs/0809.0086
  * Definition. Physics is a part of mathematics devoted to the calculation of integrals of the form g(x)e^f(x)dx. Different branches of physics are distinguished by the range of the variable x and by the names used for f(x), g(x) and for the integral. For example, in classical statistical physics x runs over a symplectic manifold, f(x) is called the Hamiltonian function and the integral has the meaning of a partition function or of a correlation function. In a d-dimensional quantum field theory x runs over the space of functions on a d-dimensional manifold (the space of fields) and f(x) is interpreted as an action functional.
  * note how this is a lot like fourier
  * its an inner product (sum of a * b) where b is the circle

* api is a fixed point
  * the returned value

* characters groups
  * https://en.wikipedia.org/wiki/Character_group
  * We can express explicit elements in the character group as follows: recall that elements in `U(1)` can be expressed as `exp(tau * i * x)`
  * thereby we can express fourier (as below) `fou(k, n, N) = u1(-k * n / N)`

* dijkstras semantics
  * ralph levien: https://news.ycombinator.com/item?id=32919426

* miniagda
  * https://twitter.com/Lavoisierbug/status/1573897118942519297
  * https://www.cse.chalmers.se/~abela/miniagda/#:~:text=bounded%20lambda%2Dabstraction,when%20i%20%3D%200

* reversible computation
  * curerntly computation is a semi-group, it should be a group

* fourier-group connection

  * check out dft wiki
    * check out the clockface (https://en.wikipedia.org/w/index.php?title=Discrete_Fourier_transform&oldid=1102326617)
    * `fou(k, n, N) = exp(-im * tau * (k * n) / N)`
    * fou projects a linear thing to a clock face
    * entropy connection (below)

* quantum entropy
  * is fourier and entropy related
    one is `\sigma(x * exp(...))` other one is `sigma(x * log(x))`
  * kl divergence gets rid of the minus sign
    * fourier projects

* lll lattice algorithm
  * boaz barak lecture notes
  * lattice reduction

* https://twitter.com/Lavoisierbug/status/1573897118942519297
  * simple dependently typed langauge

* "linear logic" "factorization systems"
   * orthomodular lattice (see vaughan pratt paper on quantum mechanics)
   * martin hyland
   * chu spaces factorizations
* p == np
   * i guess you fourier the program and the data and then do piecewise (?)
   * check out

* dual polynomials
    * i wonder if the trick is that if we represent polynomials in terms of extrema, we have more information about the polynomials since the extrema are projective zeros
  * when you keep projecting minima, you will eventually get a zero
      * what is multiplication by (0 + eps) and (1 + eps)

  * central limit theorem

* read
* think that the problem

* from https://ncatlab.org/nlab/show/well-pointed+topos#general
* To maintain this logical result in constructive mathematics (that is, without excluded middle in the metalogic), one must add the following requirements:
    * the terminal object is indecomposable, and
    * the terminal object is projective.


* google topos "fixed point"
    * Martin-Löf′s partial type theory, i.e., type theory with a fixed point operator, is extended with universes and given a domain-theoretic interpretation using
    * the beauty about "partial types with a fixed point" is that you can infer the complete lattice (since you have a fixed point)

* the reason why you dont want exluded middle is because that's the thing you are calculating in some sense, you don't want it to be
    * excluded middle == orthogonality
    * it's not that the property itself is


* what is orthogonality in the context of linear logic and programs

* look into coherent spaces
    * this is an interpretation of logic as dual banach spaces
* i guess a topos is a point in a space that has a fixed point
    *

* how does fourier of programs work?
    * bisimulation

* what is the orthogonality in fourier,
should this be the program

*
* a linked list is nilpotent since if you keep `next^n(l)`


* commutatity = orthogonality (note how orthogonal matrices commute, it's order invariant)
* distributativity = adjoints
* associativity = norm/delooping (see ncatlab on associativy)

* contravariant lattice

* branch and bound
  * this is essentially adjoint and norm
  *

* https://qchu.wordpress.com/2012/11/06/string-diagrams-duality-and-trace/

* i have been working under the assumption that i need to find periodicity of the whole program, what if i need to find periodicity of each of the possible execution traces? i imagine that these will have something in common that can be factored outs
  * check out the clausen formula
  *
* discrete fourier transform
  *
* bisimulation
* lattice fourier found
* reciprocal lattice
  * bravais lattice (there is only 14 of them)
  * i wonder if the solution is that there will be a super lattice that if you shine light on it will light up only certain points on the lattice (thereby selecting the particular lattice) and then you can shine more light on it and read off the diffraction pattern
* reciprocal lattice vectors
  * see
* crystals are defined by their pattern
* i wonder if the trick is that you calculate the spectrum of the program (since it has a group structure) and then also calculate the
* in the travelling salesman problem
* noga alon
  * spectral graph
  * he talks about how
* [Simulation and Bisimulations for Probabilistic Systems, and their Logical Contents](https://www.youtube.com/watch?v=j31R8r3YuzY)


* "computational algebraic geometry technique for determining nonlinear normal modes of structural systems"
* [adjoint functors and monads](https://ahilado.wordpress.com/2017/06/20/adjoint-functors-and-monads/)

## orthogonality
  * it means mutually exclusive
    * "In taxonomy, an orthogonal classification is one in which no item is a member of more than one group, that is, the classifications are mutually exclusive."
  * what is orthogonality in the context of programming?
  * what is duality in the context of programming
  * i guess if you have an if statement,
```swift
  if a {
    b
  } else {
    c
  }
```
statements b and c are orthogonal to each other (can't happen at once)
but statements a, b are dual to each other and so are a, c dual to each other
* orthogonality also means rotated by one unit (think how in fourier)
* think about transition matrices and orthogonality
  * A term rewriting system is said to be orthogonal if it is left-linear and is non-ambiguous. Orthogonal term rewriting systems are confluent.
  * In combinatorics, two n×n Latin squares are said to be orthogonal if their superimposition yields all possible n2 combinations of entries.[15]
*

* [Program Synthesis with Equivalence Reduction](https://par.nsf.gov/servlets/purl/10100598)
  * "How can we exploit operator semantics to efficiently explore large spaces of candidate programs?"
* "fixed point" cotangent
  * https://legacy-www.math.harvard.edu/history/bott/bottbio/node18.html
* iconic math books
* https://twitter.com/SebastjanVoros/status/1499453039056465932
  * calculus of self-reference
  * https://gist.github.com/adamnemecek/4d88cde664f0e93548a65f36990c165e
* [From parametricity to conservation laws, via Noether's theorem](https://dl.acm.org/doi/10.1145/2535838.2535867)
  * programming using lagrangians
  * Invariance is of pargamount importance in programming languages and in physics. In programming languages,

* is the point of fixed points that they are points in a space that are commutative?
  https://twitter.com/johncarlosbaez/status/1562102229724585990
  * https://en.wikipedia.org/wiki/Braided_monoidal_category
  * i guess one can think of this as a OS schedulers, when a lock is unlocked
    * the threads t1, t2 can either be scheduled as t2, or t1 since it's commutative
  * which matrices are commutative?

* is the euler's formula really about relationship between `split-complex numbers`, `dual numbers` and `complex numbers`

* pca genetics https://medium.com/swlh/a-gentle-introduction-into-the-application-of-principal-component-analysis-pca-in-genomics-269026453295
* cotangent space = causality?
* [The Fourier transform is a neural network](https://sidsite.com/posts/fourier-nets/)

* [triangular matrix](https://en.wikipedia.org/wiki/Triangular_matrix#Forward_substitution)
  * A matrix equation in the form {\displaystyle L\mathbf {x} =\mathbf {b} }{\displaystyle L\mathbf {x} =\mathbf {b} } or {\displaystyle U\mathbf {x} =\mathbf {b} }{\displaystyle U\mathbf {x} =\mathbf {b} } is very easy to solve by an iterative process called forward substitution for lower triangular matrices and analogously back substitution for upper triangular matrices. The process is so called because for lower triangular matrices, one first computes {\displaystyle x_{1}}x_{1}, then substitutes that forward into the next equation to solve for {\displaystyle x_{2}}x_{2}, and repeats through to {\displaystyle x_{n}}x_{n}. In an upper triangular matrix, one works backwards, first computing {\displaystyle x_{n}}x_{n}, then substituting that back into the previous equation to solve for {\displaystyle x_{n-1}}x_{n-1}, and repeating through {\displaystyle x_{1}}x_{1}.
* are dual numbers and orthogonality are kind of the same
orthogonal means
  * `M * transpose(M) = I`
  * `M *


* range is a manifold
  * the center of the a range is the fixed point eigenvalue since it's scale invariant
  * actually maybe not

* coevent
  * [Quantum measures and the coevent interpretation](~grab25)
* https://arxiv.org/pdf/math/0206103.pdf
* cotangent causality (grab35.png)
* why is a specturm important? it allows you to figure out the inverse easily in the case of circulant matrices, the

* https://research.utwente.nl/en/publications/functional-programming-with-bananas-lenses-envelopes-and-barbed-w
* [how is a graph like a manifold](https://arxiv.org/pdf/math/0206103.pdf)
* http://web.archive.org/web/20160316230842/http://comonad.com/reader/2009/recursion-schemes/
* cohomology computation
* tangent bundle is the adjoint of sorts
* turning a line into a circle/group with an exponent
* `exp(x) = cos(x) + i*sin(x)`
* `exp(x, ortho) = cos(x) + ortho * sin(x)`

* https://en.wikipedia.org/wiki/Traced_monoidal_category
  * (As shown later [12], the dynamical part of the Geometry of Interaction system was implemented using precisely the same tools required to model reversible (space-bounded) Turing machines).
* "traced monoidal categories" "geometry of interaction"
* "geometry of interaction" tangent
* mathematical structure of stable physical systems
* Proof-nets and the Hilbert space
* "abstract interpretation" "linear logic"
* cotangent = pullbacks
* functional programming in sublinear space

* https://plato.stanford.edu/entries/logic-linear/#hyland00ic

* extensional vs intensional = value vs reference
* moral proofs
* linear (affine) logic is decidable and therefore rice's theorem does not apply
  * from plato.stanford.edu

* is there a better fourier that lets you calculate matrix inverse using said fourier?
  * for a circulant matrix, one can use the fft of a row to calculate the inverse
  * is there a transform that
  * the inverse of a diagonal matrix
  * inv(x::Circulant) = fft(row)
* https://terrytao.wordpress.com/tag/pontryagin-duality/
  * note how at the end there's |x|^2
  *
  ```julia
  function inv(x::Matrix)

  end
  ```

* what is the relationship between nipotence and orthogonality
  * are dual numbers self orthogonal?

* fourier relies on nilpotence
  * https://en.wikipedia.org/wiki/Pontryagin_duality#Fourier_transform_and_Fourier_inversion_formula_for_L1-functions
  * https://en.wikipedia.org/wiki/Riemann%E2%80%93Lebesgue_lemma
  * "Note the Fourier transform depends on the choice of Haar measure. It is not too difficult to show that the Fourier transform of an {\displaystyle L^{1}}L^{1} function on {\displaystyle G}G is a bounded continuous function on {\displaystyle {\widehat {G}}}\widehat{G} which vanishes at infinity."

* is the

* nilpotence == projectivity https://arxiv.org/pdf/1406.3455.pdf

## fourier analysis is a special case of representation theory
* https://mathoverflow.net/questions/37021/is-fourier-analysis-a-special-case-of-representation-theory-or-an-analogue
* http://www.math.uchicago.edu/~may/VIGRE/VIGRE2009/REUPapers/Patel.pdf

* can we get an inverse matrix using a fourier?
  * yes for circulant matrices

* https://en.wikipedia.org/wiki/Circulant_matrix
* "In numerical analysis, circulant matrices are important because they are diagonalized by a discrete Fourier transform, and hence linear equations that contain them may be quickly solved using a fast Fourier transform.[1] They can be interpreted analytically as the integral kernel of a convolution operator on the cyclic group {\displaystyle C_{n}}C_{n} and hence frequently appear in formal descriptions of spatially invariant linear operations."

# category theory
* the nice thing about category theory is that theoretically unlike with normal functions, when you have say `F=m*a` with imperative programming, you have to write three functions
to figure out each of the variables, with category theory you can ideally just write a single category and the rest will be done automatically
*

# computation as manifold
* you can think or a program as
* ike and mike talk about this



# reversible computation
* https://en.wikipedia.org/wiki/Cotangent_space

  * given a state at time T, the adjoint is the tangent space, the set of possible spaces that we can reach when we combine if with an event (event space duality) (redo)
  * cotangent space is the space of the spaces coming into the current state (undo)
  * "The tangent space and the cotangent space at a point are both real vector spaces of the same dimension and therefore isomorphic to each other via many possible isomorphisms. The introduction of a Riemannian metric or a symplectic form gives rise to a natural isomorphism between the tangent space and the cotangent space at a point, associating to any tangent covector a canonical tangent vector."

* fixed point
# perception
* mind imposes a linear structure on periodic phenomena (find the paper that says this)
* joy of visual perception
*

* godel escher bach talks about braiding
* he is right about

* In those days, by a “mathematicus,” or “Sternseher,” was understood a man that earned his living by making astrological predictions.
* bifuraction + "fixed point"

* [predictive coding + autodiff](https://arxiv.org/abs/2106.13082)

* subspace is a subgroup
  * one can think of inference as rebuilding a space from it's subspaces
* [Dimensionality Reduction with Subspace Structure Preservation](https://arxiv.org/abs/1412.2404)
* [A Subspace-based Approach for Dimensionality Reduction and Important Variable Selection](https://arxiv.org/abs/2106.01584)
* cobordism hypothesis
  * Yes. The physical motivation is that topological field theories, as examples of quantum field theories, should be fully local, meaning that one should be able to calculate any information about a (fully extended) TQFT 𝑍 on a manifold 𝑀 by cutting 𝑀 into pieces, formulating 𝑍 on these pieces, and gluing. The takeaway in physics is that in any class of systems thought to be described by topological field theories, one should be able to determine the TQFT for a particular system from how the system behaves on a neighborhood of a point.
  * https://mathoverflow.net/questions/309093/physical-consequences-of-cobordism-hypothesis
* linearizability
  * this is the same as trace theory, trace theory has the
  * https://en.wikipedia.org/wiki/Linearizability
    * check the list of
  * spectrum == history
  *

* [A Prehistory of n-Categorical Physics](https://math.ucr.edu/home/baez/history.pdf)
  * But in our universe, is also possible for physical systems to undergo a special sort of process where they ‘switch places’:
  * this switching places: check out whitney embedding

* [Generalizing Topology via Chu Spaces](https://arxiv.org/abs/1101.2999)

* cobordism + thom spectra
* https://en.wikipedia.org/wiki/Whitney_embedding_theorem
  * the curve has intersections (i.e.)
* "whitney embedding theorem" "fixed point"
  * https://valentermz.github.io/documents/slides/fixed_point_theorems-handout.pdf
* [taken's embedding theorem]()
* [Discovering State Variables Hidden in Experimental Data](https://arxiv.org/abs/2112.10755)
* https://www.dpmms.cam.ac.uk/~wz302/randDoc/tangent.pdf

* "dual numbers" cotangent

* robotics learning physics
  * https://news.ycombinator.com/item?id=32329783

* Epicycles worked very well and were highly accurate, because, as Fourier analysis later showed, any smooth curve can be approximated to arbitrary accuracy with a sufficient number of epicycles.
  * https://en.wikipedia.org/wiki/Deferent_and_epicycle
* scale invariance is a big thing in quantum mechanics
  * can you make neural networks scale invariant?
* find "noga alon" p == np paper, p==np
  * this maybe? https://www.cs.tau.ac.il/~nogaa/PDFS/spectalg.pdf
* bisimuation + coinduction

* groupoid + closed monoidal category

* [Induction, Coinduction, and Fixed Points:
Intuitions and Tutorial](https://arxiv.org/pdf/1903.05127.pdf)
  * talks about fixed points in other papers
* covariant, cotangent
* cocycle, coboundary https://ncatlab.org/nlab/show/coboundary
* "closed monoidal category" cotangent
* Discrete-Time Machines in Closed Monoidal Categories.
* "Kalman has published several works on realization, controlability, and observability"
(see [14] and [15])

  * https://ncatlab.org/nlab/show/coboundary
* spectral theorem book
* https://graphicallinearalgebra.net/
 * colored graph nodes are orthogonal
* why hypergraphs https://news.ycombinator.com/item?id=32283022
 * talks about unifying things
* is the kalman fiter just a low pass filter https://news.ycombinator.com/item?id=32271351
* [A Unifying Review of Linear Gaussian Models", by Sam Roweis and Zoubin Ghahramani.](https://news.ycombinator.com/item?id=32271693)
* adjoint method
* coinductive calculus
  * https://news.ycombinator.com/item?id=32191372
* realizability on ncatlab
 * andrej bauers phd thesis talksa bout fixed point newton method
  http://math.andrej.com/wp-content/uploads/2006/04/thesis.pdf
  * One possible way to find a computational interpretation for univalence in homotopy type theory is to interpret it in using realizability. Stekelburg provides a univalent universe of modest Kan complexes.
  * samson abramsky talks about this too
  * kantian synthetic vs analytical
* https://hal.inria.fr/hal-02548315/document

* [fourier mind](https://en.wikipedia.org/wiki/Holonomic_brain_theory#:~:text=Holonomic%20brain%20theory%2C%20also%20known,in%20or%20between%20brain%20cells.)
  *[ ](https://www.google.com/books/edition/Biological_and_Quantum_Computing_for_Hum/W-3wzjxqUDIC?hl=en&gbpv=0)

* [The phrasal lexicon](https://aclanthology.org/T75-2013.pdf)

* [Fixed point index](https://en.wikipedia.org/wiki/Fixed-point_index)
* [Nonlinear Dynamics and Chaos](https://www.amazon.com/Nonlinear-Dynamics-Student-Solutions-Manual/dp/0813349109/ref=pd_lpo_1?pd_rd_i=0813349109&psc=1)
 * bifucation (stepanov too)
 *
* [A structural approach to reversible computation](https://arxiv.org/abs/1111.7154#:~:text=Samson%20Abramsky,progresses%20towards%20its%20physical%20limits.)
* [Towards a Theory of Programming Languages](https://group-mmm.org/~eberhart/research/report_m2.pdf)
* [Adjoint Reactive GUI Programming](https://arxiv.org/pdf/2010.12338.pdf)
* [Jordan curve theorem](https://en.wikipedia.org/wiki/Jordan_curve_theorem#Discrete_version)
  * The Jordan curve theorem can be proved from the Brouwer fixed point theorem (in 2 dimensions),[1] and the Brouwer fixed point theorem can be proved from the Hex theorem: "every game of Hex has at least one winner", from which we obtain a logical implication: Hex theorem implies Brouwer fixed point theorem, which implies Jordan curve theorem.[2]
* [Concurrent Separation Logic Meets Template Games](https://arxiv.org/pdf/2005.04453)
* [Bipolar theorem for quantum cones](https://link.springer.com/article/10.1007/s10688-012-0029-x)
 * In this note duality properties of quantum cones are investigated. We propose a bipolar theorem for quantum cones, which provides a new proof of the operator bipolar theorem proved by Effros and Webster. In particular, a representation theorem for a quantum cone is proved.
* [Pseudospectral optimal control](https://en.wikipedia.org/wiki/Pseudospectral_optimal_control)
  * Moreover, their structure can be highly exploited to make them more computationally efficient, as ad-hoc scaling[21] and Jacobian computation methods, involving dual number theory[22] have been developed.
* [Geometry of Interaction and the Dynamics of Proof Reduction: a tutorial](https://cgi.luddy.indiana.edu/~ehaghver/Tutorial.pdf)

* [Geometry of Interaction and linear combinatory algebras](https://www.researchgate.net/publication/220173613_Geometry_of_Interaction_and_Linear_Combinatory_Algebras)
  We illustrate the construction on six standard examples, representing both “particle-style” as well as “wave-style”Geometry of Interaction

* https://www.sciencedirect.com/topics/mathematics/embedding-theorem

* [Geometrical semantics for linear logic (multiplicative fragment)](https://core.ac.uk/download/pdf/81144945.pdf)

* https://core.ac.uk/download/pdf/81144945.pdf

* dao of functional programming

* geometry of syntax and semantics for directed file transformations
* von neumann patent for differential analyzer



* differential geometry of interaction
* [The Geometry of Interaction of Differential Interaction Nets](https://arxiv.org/pdf/0804.1435.pdf)

* https://twitter.com/deontologistics/status/1518329618813657088
* [Factor graph](https://en.wikipedia.org/wiki/Factor_graph)
 * is a tree? fixed point?
 * https://en.wikipedia.org/wiki/Invariant_theory reynolds operator idempotent

* https://en.wikipedia.org/wiki/Multiplexer
* invariant theory + probability: https://www.maths.ox.ac.uk/node/35937

* when i was studying probability, math, physics, cs I was always more interested in the things they had in common rather than the pecularities. I was trying to figure out what was the invariant of all these sciences. It should therefore come as no surprise that the invariant is in fact the idea of invariants.

* https://github.com/adamnemecek/ChuCalculator/
* http://chu.stanford.edu/source/
* full inverse is inv(x) = a' / (a' * a)

#
* [SOME GEOMETRIC PERSPECTIVES IN CONCURRENCY THEORY]()
* https://en.wikipedia.org/wiki/Ultrafinitism

# chu spaces + spectrum / fixed point
* https://link.springer.com/article/10.3103/S1055134409030055

# p*q*inv(p)
* https://en.wikipedia.org/wiki/Conjugacy_class
* https://en.wikipedia.org/wiki/Adjoint_representation
* https://en.wikipedia.org/wiki/Spectral_theorem

# [A Novel Spectral Coding in a Large Graph Database](https://openproceedings.org/2008/conf/edbt/ZouCYL08.pdf)

# can you speed up type inference by using fourier?
* [Cubical Type Theory](https://www.cse.chalmers.se/~coquand/face.pdf)

* [Asymptotic spectra: Theory, applications and extensions](https://staff.fnwi.uva.nl/j.zuiddam/papers/convexity.pdf)
# "type theory" factorization + spectrum


# determinant is  the volume of the parallepiped (matrix inverse)

# jordan
* https://en.wikipedia.org/wiki/Jordan_normal_form

[Least and Greatest Fixed Points in Linear Logic](https://arxiv.org/abs/0910.3383.pdf)

## lagrangian & noether theorem
* they are invariantsjor

## filters
* useful for defining continuity
 * https://en.wikipedia.org/wiki/Filters_in_topology#Filters_and_prefilters
 * dual ideal
 * https://en.wikipedia.org/wiki/Invariant_measure
 * https://en.wikipedia.org/wiki/Invariant_(mathematics)


## paxos lattice
## paxos linearizable
* [Linearizable Replicated State Machines with Lattice Agreement](https://arxiv.org/abs/1810.05871)




## path "fixed point"
* [Solving Fixed-Point Problems with Inequality and Equality Constraints via a Non-Interior Point Homotopy Path-Following Method](https://www.hindawi.com/journals/mpe/2017/3456834/)8
 * " In this paper, we provide a constructive proof of the general Brouwer fixed-point theorem and then obtain the existence of a smooth path which connects a given point to the fixed point."

* [A walk over the shortest path: Dijkstra’s Algorithm viewed as fixed-point computation](https://www.cs.utexas.edu/users/misra/psp.dir/WalkShortestPath.pdf)

* [On Paths Generated by Fixed Point Algorithms](https://www.jstor.org/stable/3689213)

## spectral logic
* From proof-nets to bordisms: the geometric meaning of multiplicative connectives
* http://pi.math.cornell.edu/m/People/PhD/2005Aug/slavnov
* what's up with the cones?
 * coherence (technically — a conic subset of the tangent bundle)
* https://news.ycombinator.com/item?id=31228934 mentions cones, what's up with that? are they just adjoints? normed cone

* [Towards a semantics for higher-order quantum computation](https://www.mscs.dal.ca/~selinger/papers/cones.pdf)

* google spectral logic
* i found a reversible logic synthesis book thing that has some czech people mention using quantum logic for generalization of probability
 * Quantum logics as underlying structures of generalized probability theory
* [Linear logic in normed cones: probabilistic coherence spaces and beyond](https://arxiv.org/abs/1803.06005)

## what is linearity
* when you lookup the standard definition of linearity you get this
* Additivity: f(x + y) = f(x) + f(y).
 * this is adjoint
* Homogeneity of degree 1: f(αx) = α f(x) for all α.
 * this is norm

## constructivism
* [Constructivist Perspective on Physics](https://citeseerx.ist.psu.edu/viewdoc/download?doi=10.1.1.395.56&rep=rep1&type=pdf)

##links to sort out
* [space of interaction](https://arxiv.org/pdf/2104.13795.pdf)

## linear logic + operator algebras
* google search for "linear logic" fourier
* girard "Moreover, if we remember that coding is based on the development by means of Fourier series (which involves the Hilbert space) everything that was done can be formulated in terms of operator algebras." (from advances in linear logic the first paper page 38)

* [Fixed points in programming: datatypes and protocols](https://math.usask.ca/fvk/Cockett%20talk%20Saskatoon-2014.pdf)
* [What is a good process semantics?](https://pages.cpsc.ucalgary.ca/~robin/talks/estonia.pdf)

## chu spaces + fixed points
* [Chu Spaces, Concept Lattices, and Domains](http://www.entcs.org/files/mfps19/83018.pdf)
* [APPROXIMABLE CONCEPTS, CHU SPACES,
AND INFORMATION SYSTEMS](https://citeseerx.ist.psu.edu/viewdoc/download?doi=10.1.1.387.6096&rep=rep1&type=pdf)
* [](https://citeseerx.ist.psu.edu/viewdoc/download?doi=10.1.1.387.6096&rep=rep1&type=pdf)
* [A mosaic of Chu spaces and Channel Theory I: Category-theoretic concepts and tools](https://chrisfieldsresearch.com/mosaic1-pre.pdfce)
* operad is a norm

## query: spectral methods probability
* [Spectral methods for a generalized probability theory](https://www.ams.org/journals/tran/1965-119-03/S0002-9947-1965-0183657-6/S0002-9947-1965-0183657-6.pdf)

* [On modeling and complete solutions to general fixpoint problems in multi-scale systems with applications](https://fixedpointtheoryandapplications.springeropen.com/articles/10.1186/s13663-018-0648-x)
# abstract interpretation and programsyntehsis are adjoints
*

* lists are nilpotent (you reach nil eventually)

# all computable functions are continous
 * https://cs.stackexchange.com/questions/80978/why-are-computable-functions-continuous
 * https://wikimpri.dptinfo.ens-cachan.fr/lib/exe/fetch.php?media=cours:upload:cours-2021-mpri-partie-i-goodmpri.pdf
* [Sometimes all functions are continuous](http://math.andrej.com/2006/03/27/sometimes-all-functions-are-continuous/#:~:text=A%20function%20is%20computably%20continuous,of%20are%20needed%20to%20determine%20.)

* a dfa and an nfa can both be represented as a binary transition matrix meaning one can calculate their fourier

* boundary value
 * https://matjohn.ku.edu/Notes/Math951Notes_Ch4.pdf
 * https://advancesindifferenceequations.springeropen.com/articles/10.1186/1687-1847-2014-14
 * [A fixed point iterative method for the solution of two-point boundary value problems for a second order differential equations](https://www.sciencedirect.com/science/article/pii/S1110016817302958value )

* google: foruier "travelling salesman"
 * [Optical processor for solving the traveling salesman problem (TSP)](https://citeseerx.ist.psu.edu/viewdoc/download?doi=10.1.1.211.150&rep=rep1&type=pdf)
* A game semantics for proof search: Preliminary results

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
* equivalence of boundedness and continuity https://en.wikipedia.org/wiki/Bounded_operator
 * note that all computable functions are continous

## spectral theory
 * [The Fourier transform on the real line is in one sense the spectral theory of differentiation qua differential operator.](https://en.wikipedia.org/wiki/Spectral_theory)
* ["Hilbert himself was surprised by the unexpected application of this theory, noting that "I developed my theory of infinitely many variables from purely mathematical interests, and even called it 'spectral analysis' without any presentiment that it would later find application to the actual spectrum of physics."](https://en.wikipedia.org/wiki/Spectral_theory)
* https://en.wikipedia.org/wiki/Riesz_projector

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

## fixed point
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

* https://en.wikipedia.org/wiki/Fixed_point_(mathematics)
 *

* given a map, you can decompose it to a nilpotent and a invertible part https://web.evanchen.cc/notes/Harvard-55a.pdf (page 30)

product of unions = sum of products (third kolmogorov axiom) really means that you have a norm?
* 1/2 or 1/sqrt(2) are really just pythagorean theorem

* contraction mapping + dynamic programming https://www.math.wustl.edu/~freiwald/309markov.pdf

## fixed point
* http://nlab-pages.s3.us-east-2.amazonaws.com/nlab/show/Lawvere's+fixed+point+theorem
* In ‘Diagonal arguments and Cartesian closed categories’ (Lawvere 69) we demystified the incompleteness theorem of Gödel and the truth-definition theory of Tarski by showing that both are consequences of some very simple algebra in the Cartesian-closed setting.
* http://emis.matem.unam.mx/journals/TAC/reprints/articles/15/tr15.pdf

* "geometry of interaction" "fixed point"
 * [Towards a Typed Geometry of Interaction](https://cgi.luddy.indiana.edu/~ehaghver/HS-CSL05-LNCS.pdf)
 * [Geometry of Interaction and the Dynamics of Proof Reduction: a tutorial](https://cgi.luddy.indiana.edu/~ehaghver/Tutorial.pdf)

* [Flow Analysis in the Geometry of Interaction](https://link.springer.com/content/pdf/10.1007/3-540-61055-3_37.pdf)
* [Girard's !() as a reversible fixed-point operator](https://arxiv.org/abs/1309.0361)
* [Feedback for linearly distributive categories: traces and fixpoints](https://www.math.mcgill.ca/rags/linear/trace.pdf)
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


