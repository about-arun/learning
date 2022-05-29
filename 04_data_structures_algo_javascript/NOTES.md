# BIG O

Big O notation is a way to formalize fuzzy counting

It allows us to talk formally about how the runtime of an algorithm grows as the input grows.

We only care about the big trend not the details.

> _We say that an algorithm is **$O(f(n))$** if the number of simple operations the computer has to do is eventually less than a constant times **$f(n)$**, as **$n$** increases._
>
> - $f(n)$ could be linear $(f(n)=n)$
>   - $O(n)$ since as $n$ increases, the runtime increases in the order of $n$.

> - $f(n)$ could be quadratic $(f(n)=n^2)$
>   - $O(n^2)$ in case of nested loops for example.

> - $f(n)$ could be constant $(f(n) = 1)$
>   - $O(1)$ since as $n$ increases it has no effect on its runtime

> - $f(n)$ could be something else entirely different!
