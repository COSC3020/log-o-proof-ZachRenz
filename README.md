[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-24ddc0f5d75046c5622901739e7c5dd533143b0c8e959d652212380cedb1ea36.svg)](https://classroom.github.com/a/fbkbKZ5N)
# Asymptotic Equivalences

In the lectures, we said that logarithms with different bases don't affect the
asymptotic complexity of an algorithm. Prove that $O(\log_{2} n)$ is the same as
$O(\log_{5} n)$. Use the mathematical definition of $O$ -- do a formal proof,
not just the intuition.

I have started with the formal definition of $O$ below. Add your answer to this
markdown file. [This
page](https://docs.github.com/en/get-started/writing-on-github/working-with-advanced-formatting/writing-mathematical-expressions)
might help with the notation for mathematical expressions.

$T(n) \in O(f(n)) \iff \exists c, n_0: T(n) \leq c \cdot f(n) \forall n \geq n_0$

# Proof

$Let$  $f(n) = \log_{5}n$

$T(n) \in O(\log_{5}n) \iff \exists c, n_0: T(n) \leq c \cdot \log_{5}n \forall n \geq n_0$

$\text{Using the property}$ $\log_{a}b = \log_{c}b / \log_{c}a$

$\log_{5}n = \log_{2}n / \log_{2}5$ $\text{Where}$ $\log_{2}5$ $\text{is some constant}$

$\text{Let's insert it into Big O of log base 5 by Multipying by}$ $1 / \log_{2}n$ $\text{and writing our constants under one C for the second part}$

$T(n) \in O(\log_{5}n) \iff \exists c, n_0: T(n) \leq c \cdot 1/ \log_{2}n \forall n \geq n_0$ ($1/ \log_{2}n$ is equivalent to $\log_{2}n / \log_{2}5$ and $\log_{2}n$ will dominate the function in asymptotic complexity)

$\text{Which is equivalent to if}$ $f(n) = \log_{2}n$

$T(n) \in O(\log_{2}n) \iff \exists c, n_0: T(n) \leq c \cdot \log_{2}n \forall n \geq n_0$

$\therefore \forall O(\log_{a}n) \text{where a is any constant } \exists O(\log_{b}n) \text{where b is some constant, that is equal to the previous log, because we can use the change of base properity, }$
$\text{and rewrite it to be identical to the first log.}$ 


