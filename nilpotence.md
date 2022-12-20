# open questions
* how is this related to probability
* how is this related to winding numbers and browers theorem
* learn more reinforcement learning
* how is this related to


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

## dynamic programming
You are updating until you can't improve, thereby makeing the update rule 0.
The adjoint is the other options that you are considering.


## physics
physics is just a

## programming
Onen can think of a program as a tangent space, the state at any point is the value

`f(t) = state of computer at time t`
`f'(t) = update rule`

## exponent
The magical property of the exponent is that it wraps around
```
exp(0) = 1
exp(tau * im) = 1
```

See Jordan Curve definition `theta(0) = theta(1)`.

## distributional hypothesis


## sign analysis
    * winding numbers brouwers fixed point theorem

## winding numbers


## what if the commuter is the mse?
*

## qr decomposition
* upper triangular matrix
    * what if the upper triangular matrix is the if statements

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

As per the Bell, the inifitesimal calculus doesn't have just like linear logic.

## pde

