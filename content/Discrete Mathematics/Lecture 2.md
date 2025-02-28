# Divisibility
An integer $a$ divides an integer $b$ if and only if there exists an integer $s$ such that $as=b$. Written as $a \mid b$ (a divides b).
In logical notation, this is written as $a,b \in \mathbb{Z}, a \mid b$ if $\exists s \in \mathbb{Z}$ such that $as=b$.
For example, $7 \mid 42$ because $\exists 6 \in \mathbb{Z}$.
Conversely, $10 \nmid 42$ because $\nexists s \in \mathbb{Z}$ such that $10s=42$.
# Direct Proofs
Demonstrating a one statement's truth implies another statement's truth. For example, for $p \to q$ and $q \to r$ and $r \to s$ and $s \to t$, it logically follows that $p \to t$.
## A Simple Direct Proof
An integer $a$ is even if and only if $2 \mid a$. A non-even integer is said to be odd.
We can prove directly that $2 \mid n$ implies $2 \mid n^2$, that is a square of an even number is also even.

Let $n^2 = (2s)^2 = 2(2s^2)$. This gives us that $\exists (2s^2) \in \mathbb{Z}$ such that $2(2s^2)=n^2$ and hence $2 \mid n^2$. The same reasoning can be provided that $(2 \mid n) \to (2 \mid n^3)$ or that $(3 \mid n) \to (3 \mid n^2)$.
## Example of a Direct Proof not working
"Show that $n$ is an integer, such that $n^2$ is even, then $n$ is also even", ie we want to prove $\forall n \in \mathbb{Z}, (2 \mid n^2) \to (2 \mid n)$.
A similar argument tells us that $(2 \mid n^2)$ so $\exists s \in \mathbb{Z}$ such that $2s = n^2$. Although this shows that $n = \sqrt{2}\sqrt{s}$, this doesn't lead to a statement in the form of $n=2t$ for some integer $t$.
# Contrapositives
Where: if every time $p$ is true, $q$ is also true, then every time $q$ is false, $p$ must also be false.
For example, the statement "I have no brothers and sisters" implies "I have no brothers". The contrapositive of this is that "I have a brother" implies "I have a brother or sister".
Contrapositives do not change the truth of an original statement. If true, the contrapositive is true and if false, the contrapositive is false.
## Proof by Contrapositive
Relies on negating both statements and reversing the direction of implication.
When seeking to prove that if we have an integer $n$ such that $n^2$ is even, then $n$ must also be even. Here, we also then seek to prove that if $n$ is not even, $n^2$ is certainly not even.
Let $n \in \mathbb{Z}$ be an odd number. This tells us that $\exists s \in \mathbb{Z}$ such that $(2s+1)=n$.
We have $n^2 = (2s+1)^2 = 4s^2 + 4s + 1 = 2(2s^2 + 2s) + 1$, so n^2 is therefore 1 larger than an even number so is odd.
We have shown that $\neg (2 \mid n) \to \neg (2 \mid n^2)$ and hence that $(2 \mid n^2) \to (2 \mid n)$. If $n^2$ is even and $n$ is an integer, $n$ is even.
# Proof by Contradiction
This proofs makes an assumption which is the negation of what we wish to prove, and then constructing a logical argument that leads to a statement which is clearly false.
Formally, this consists of starting with a statement $p$ (assumed to be true) and showing that $p \to \neg p$. Since no statement can be true and not true, the initial assumption of $p$ being true must be incorrect.
# Example Proofs
## Prime Numbers
A prime number is an integer greater than 1 which is divisible only by 1 and itself. That is, $n \in \mathbb{Z}$ is prime if and only if $(s \nmid n) \forall s \in \mathbb{Z}^+ \ {1,n}$.
Rather than proving that $(n \text{ is prime}) \land (n > 2) \to (2 \nmid n)$ , we can instead show that $(2\mid n) \to \neg((n \text{ is prime}) \land (n>2))$.
This is trivial to prove, since if 2 divides $n$, $\exists s \in \mathbb{Z}$ such that $2s = n$. If this is the case, then $n$ is not prime since it has 2 and $s$ as divisors.
When writing out all primes, we observe that they appear to be less and less frequent. The question is if there are a finite or infinite number of prime numbers. We can show that there are infinitely many by first assuming that there are not infinitely many, leading to a contradiction.
If we assume that there are a finite number of primes, there is a list of distinct primes $p_1,p_2,...,p_n$ (any number not in this list is not prime). Consider the number $N = (p_1,p_2,...,p_n) + 1$. It is easy to see that N is not divisible by any of the primes, but is not itself a prime.
This is a contradiction, since N should've been in the original list, hence our initial assumption that there are a finite number of primes must be false.
## Irrational Numbers
To prove that $\sqrt2$ is irrational, we can prove by contradiction. Assume that $\sqrt2$ is rational, and that its simplest form is $\sqrt2=\frac{a}{b}$ for the integers $a$ and $b$.
This means that $a^2=2b^2$, which tells us that $a^2$ is even, which implies that $a$ is even.
If $a$ is even, $\forall c \in \mathbb{Z}$ such that $a=2c$. This gives $a^2 = (2c)^2 = 2b^2$, hence $2c^2=b^2$.
$\sqrt2=\frac{b}{c}$, which contradicts the original assumption that $\sqrt2=\frac{a}{b}$ is the simplest form.
## Rational Numbers
We can directly prove that between any two distinct rational numbers, there exists another rational number.
Let our two distinct rational numbers be $a$ and $b$, such that $a < b$. These can be expressed in their simplest forms $a=\frac{p}{q},b=\frac{r}{s}$.
The value $\frac{a+b}{2} = \frac{p}{2q} + \frac{r}{2s} = \frac{ps+qr}{2qs}$ is midway between $a$ and $b$ and is also rational (since $p,q,r,s$ are integers).