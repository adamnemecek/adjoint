# open questions
* how is this related to probability
* how is this related to winding numbers and browers theorem
* learn more reinforcement learning
* how is this related to
* self-adjoint inner product
* how is fourier nilpotent
* jacobian
* backpropagation
* vanishing trace
* evaluating derivatives
* lie grou pprobability
* operator probability
* differentiable dynamic programming
* type inference
* 




# Zero to infinity
* f: Y -> Y, means that f: Y' -> 0 any update rule you might has the

* this relies on metricity to measure the 0 and


*

* ok how is this relevant to adjoint and norm?
* nilpotent is the update rule or the rules of the game

Lawvere's fixed point theorem can be used for this.

A neural network fundamentally does this, you are trying to find matrices minimize the error function.

You have an update rule that converges on zero (like )

How is this related to say?

## rieman tensor
This came out of researching tensor.
Ricci calculus, definite positive (has inner product), double differentiable, defines orthogonality.

## nonconvex optimization 
Since f is differentiable and convex, a necessary and sufficient condition for a point x⋆ to be optimal is
∇f(x⋆) = 0 (from convex optimization chapter 9)

## dynamic programming
You are updating until you can't improve, thereby makeing the update rule 0.
The adjoint is the other options that you are considering for the particular field.

##
`pow(a, b) = exp(log(a) * b)`

## physicss
physics is just a

## programming
One can think of a program as a tangent space.
The state at any time `t` is the some value `x_t`.

`f(t) = state of computer at time t`
`f'(t) = update rule`

## exponent
The magical property of the exponent is that it wraps around

```
exp(0) = 1
exp(tau * im) = 1
```


See Jordan Curve definition `theta(0) = theta(1)` and no intersection.

## if statement

I guess you can think of an if statement as an adjoint of the state, it lists the possibilities.

## distributional hypothesis

## sign analysis

## knot invariants

## winding numbers
Winding numbers connection brouwers fixed point theorem.

## what if the commuter is the mse?
*

## traced monoidal

## qr decomposition
* upper triangular matrix
    * what if the upper triangular matrix is the if statements
Upper triangular matrix is [back substitution](https://en.wikipedia.org/wiki/Triangular_matrix#Forward_substitution).

You can think of it as the update rule or gradient. Machine learning fundamentally performs a qr decomposition where we are trying to minimize the update .

You can think

## commutativity and nilpotence
* qr decomposition
* if things commute the commuter is 0
* how are

## factorization
I guess you are trying to find

## physics

- bell book
-

## spectra

## linked list

One can think of a nil as a nilpotent ideal where `next(next(list)) = nil`. If the list eventually reaches nil.


```
function hasCycle(head) {
    let fast = head
    let slow = head
    while (fast && fast.next) {
        fast = fast.next.next
        slow = slow.next
        if (fast == slow) return true
    }
    return false
}
```

This is the principle that the cycle detection works on.
<!-- The lenght of the list is then  -->
check the wikipedia, they talk about period and such.

Maybe Fourier is like this, but in this scenario, we are trying to find a cycle,
maybe with the

## nullstellensatz
Read the wikipedia page, talks about vanishing.

## group character
* u1()

## c* algbera

## self-adjoint
Many important linear operators which occur in analysis, such as differential operators, are unbounded. There is also a spectral theorem for self-adjoint operators that applies in these cases. To give an example, every constant-coefficient differential operator is unitarily equivalent to a multiplication operator. Indeed, the unitary operator that implements this equivalence is the Fourier transform; the multiplication operator is a type of Fourier multiplier.

In general, spectral theorem for self-adjoint operators may take several equivalent forms.[10] Notably, all of the formulations given in the previous section for bounded self-adjoint operators—the projection-valued measure version, the multiplication-operator version, and the direct-integral version—continue to hold for unbounded self-adjoint operators, with small technical modifications to deal with domain issues.

[wikipedia](https://en.wikipedia.org/wiki/Spectral_theorem#General_self-adjoint_operators)

## fourier
* the derivative

## lawvere's fixed point theorem


## autodiff
How is autodiff related?
In implementations of autodiff, you don't have the nilpotence but you do have a number that .

You are trying to minimize the gradient (make it as close to zero as possible).

The theoretical perfect neural network in the backward pass updates the grad and tries to make it nilpotent with respect to.


You don't know the log (how many times you have to update and by how much) but you are trying to
minimize the grad.

## probability
How is this related to probability.
Central limit theorem as a fixed point of

## linear logic

As per the Bell, the  calculus doesn't have just like linear logic.

- C* connection.

## pde
You are trying to find an update rule which is 0.

## traced monoidal categories
* https://en.wikipedia.org/wiki/Traced_monoidal_category
