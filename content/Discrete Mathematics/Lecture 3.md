# Sets
A set is a well-defined collection of distinct **elements**. Sets are denoted with `{ }`, for example the set of positive integers less than 5 would be written as $\{1,2,3,4\}$. Sets can also be denoted by listing criteria met by all elements, for example the same set can be written as $\{x:x\in \mathbb{Z}^+\land (x<5)\}$.

Sets $\{1,2,3,4\}$, $\{1,3,2,4\}$, and $\{1,2,3,4,3,2,1\}$ are the same since they contain the same elements. It doesn't matter how many times an element is repeated.

Elements do not have to be numerical (ie. the set of Australian states is $\{\text{New South Wales}, \text{Queensland}, \text{Victoria}, \text{South Australia}, \text{Western Australia}, \text{Tasmania}\}$).

The number of distinct elements in a set is the **cardinality** of that set, denoted by $|\ |$. For example, if $A = \{1,2,1,3,2,3,4\}$, ${|A|=4}$.

We say that $x$ is an element of $A$ like: $x \in A$. We say that two sets $A$ and $B$ are equal, $A=B$, if $(x\in A)\leftrightarrow (x\in B)$ for all $x$.
# Unions, Intersections, Compliments
The intersection of sets $A$ and $B$ (both) is defined as $A\cap B=\{x:(x\in A)\land (x\in B)\}$.
The union of sets $A$ and $B$ (either or) is defined as $A\cup B=\{x:(x\in A)\lor(x\in B)\}$.
The compliment of the set $A$ (not in $A$) is defined as $A^c=\overline{\rm A}=\{x:(x\notin A)\}$.
# Empty Sets, Set Differences, Subsets
A set with no elements is denoted as the "empty set" $\varnothing=\{\}$.
The set difference of sets $A$ and $B$, the set of elements in $A$ but not $B$, is denoted as $A\setminus B=\{x:(x\in A) \land(x\notin B)\}$. For example if $A=\{c,d,7,11\}$ and $B=\{c,10,11\}$, then $A\setminus B=\{d,7\}$ and $B\setminus A=\{10\}$.

$A$ being a subset of $B$ (all elements of $A$ are in $B$) is denoted as $A\subseteq B$ if $(x\in A)\to (x\in B)$. This also means that $A\cap B^c=\varnothing$.
If $A\subseteq B$ and $B\subseteq A$, then $A=B$.

$A$ is a **strict** subset of $B$ ($A\subset B$) if $A\subseteq B$ and $A \neq B$ (there are other elements in $B$ that are not in $A$).
# Logic and Set Theory: De Morgan's Laws
De Morgan's laws gives us $\neg(p\land q)\leftrightarrow(\neg p\land\neg q)$ and $\neg(p\lor q)\leftrightarrow(\neg p\land\neg q)$. Both laws have close analogies in set theory.
$x \notin (A\cap B)^c\leftrightarrow x\in(A^c\cup B^c)$ and $x\in(A\cup B)^c\leftrightarrow x\in(A^c\cap B^c)$ resemble the above laws.
## Proving $x \notin (A\cap B)^c\leftrightarrow x\in(A^c\cup B^c)$
- $x\in(A\cup B)^c$, $\therefore x\notin(A\cup B)$ (picking any element belonging to the left side)
- $x\notin (A\cap B)\implies x\notin A,x\notin B$
- $x \in A^c$ or $x\in B^c$, hence $x \in (A^c \cup B^c)$. This gives $(A\cap B)^c \subseteq (A^c\cup B^c)$.

- $x\in(A^c\cup B^c) \implies x\in A^c, x\in B^c$
- $x \notin A$ or $x \notin B \implies x \notin (A\cap B)$.
- $x\notin(A\cap B), \therefore x\in(A\cap B)^c$.
- $(A^c\cup B^c)\subseteq (A \cap B)^c$, hence $(A^c\cup B^c)=(A\cap B)^c$.