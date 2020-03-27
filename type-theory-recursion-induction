> Recursion and induction are very much the same thing! This becomes obvious if you use a programming language with dependent types, such as Agda, but it can be demonstrated to some extent without them too.

> Remember, that due to the Curry-Howard correspondence, types are propositions and programs are proofs. When you are writing a function of type Nat -> Nat (I will use Haskell notation), you are trying to prove that, given a natural number, your program will terminate and produce another natural number. Now we may have a definition like this:
```
f 0 = 1
f (1 + n) = n * f n
```

> which is both a recursive definition of f and an inductive proof of its termination at the same time!

> You can read it as a proof in a following way:

> Let's prove that f x terminates for any x.

> Base case: we have f 0 constant by definition so it terminates.
> Inductive case: if we assume f n termiates, f (1 + n) terminates too (because all the functions it calls terminate).
> Note that as recursion is not limited to a function decrementing its counter, induction is not limited to natural numbers either. There is also structural induction, corresponding to structural recursion, both of which are very popular in mathematics/programming. These are to be used when trying to prove things/define functions on more complex data structures (lists/trees/etc.).

> Now, to address your concern about the "direction" of the recursion/induction. It is helpful to consider "direction of demand" and "direction of supply" here, which are opposite.

> When you define recursive function, the demand (method calls) flows from larger values to base case. On the other hand, the supply (the return values) flow from the base case to the larger values of parameter. "definedness" is another way way of thinking about supply. It starts at the base case and propagates to infinity via the recursive case.

> Now, when you are doing inductive proofs, theorems are your supply while goals are your demand. You can make a theorem T 0 out of the base case and then improve to however large T n you like using inductive case: your supply flows from 0 to infinity. Now if you have a goal G n, you can make a smaller goals G (n-k) out of it using the inductive step until you reach zero. This way your demand goes from n to 0.

> As you can see, the direction of supply is "to infinity" in both cases and the direction of demand is "to zero" in both cases.

> You can also reverse the apparent order in the descriptions of induction and recursion without changing their meaning:

> Induction is when to prove that P n holds you need to first reduce your goal to P 0 by repeatedly applying the inductive case and then prove the resulting goal using the base case.

> Similarly, recursion is when you first define a base case and then define the further values in terms of the previous ones. See, the directions are easily swapped!
Source: https://stackoverflow.com/questions/10959874/what-is-the-relationship-between-recursion-and-proof-by-induction
