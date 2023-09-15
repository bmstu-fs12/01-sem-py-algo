# Week 01. Python Basics I.

### Presentations

- [Class 1 Presentation](presentation_1_4x3.pdf);
- [Class 2 Presentation](presentation_2_4x3.pdf).

### Good to Read

- Class 1:
  - [Python](https://www.python.org/);
  - [Python Docs](https://docs.python.org/3/index.html);
  - [Git Book](https://git-scm.com/book/en/v2);
  - [Linkedin Habr I](https://habr.com/ru/articles/653691/);
  - [Linkedin Habr II](https://habr.com/ru/articles/674236/).

- Class 2:
  - [Process Memory Organization](https://habr.com/ru/companies/smart_soft/articles/185226/);
  - [Difference between Compiler and Interpreter](https://www.interviewbit.com/blog/difference-between-compiler-and-interpreter/);
  - [Introduction to Compilers, Interpreters and JIT](https://habr.com/ru/companies/vk/articles/304748/);
  - [CPython Mechanism](https://habr.com/ru/companies/yandex/articles/511972/);
  - [Data Types in Python](https://skillbox.ru/media/code/tipy-dannykh-v-python-dlya-nachinayushchikh-kakie-byvayut-i-kak-s-nimi-rabotat/?ysclid=lmdndlmi48434433889).

### Coding Homework

## 1.1 Polynomial (polynom)
Write a program that calculates the value of a polynomial: $$P_n (x) = a_n x^n + a_{n- 1} x^{n -1} + \ldots + a_1 x + a_0$$
and its derivative at a given point $x_0$. The coefficients of the polynomial and the value of $x_0$ are integers ranging from $-2^{63}$ to $2^{63} - 1$.
The program must read from the standard input the degree of the polynomial **n**, the value of $x_0$ and the coefficients of the polynomial $a_n, ..., a_0$.
You need to print the values of $P_n (x_0), P_n'(x_0)$ to standard output.
To calculate the value of a polynomial, you need to use Horner's scheme:
$$P_n (x) = (...((a_n x + a_{n-1}) x + a_{n-2})x + \ldots + a_1)x +a_0.$$

To calculate the value of the derivative of a polynomial, it is necessary to modify Horner's scheme in an obvious way.

## 1.2 Product of numbers modulo (mulmod)
Compose a program that evaluates the expression $\left(a\cdot b\right)\textrm{ mod }m$, that is, the remainder of dividing the product of the numbers $a$ and $b$ by $m$.
The program must read the numbers $a$, $b$ and $m$ from the standard input stream, and output the result to the standard output stream.

Program multiplication to modulo division calculations using a Horner's scheme. Let's represent the number in the binary number system:
$$b=\overline{b_{63}b_{62}\ldots b_{1}b_{0}}.$$
Here $b_{63},:b_{62},:\ldots:,:b_{1},:b_{0}$ are the binary digits that form the number, that is
$$b=b_{63}\cdot2^{63}+b_{62}\cdot2^{62}+\ldots+b_{1}\cdot2+b_{0}.$$
Then
$$\left(a\cdot b\right)\textrm{ mod }m=\left[a\cdot b_{63}\cdot2^{63}+a\cdot b_{62}\cdot2^{62}+\ldots+a\cdot b_{1}\cdot2+a\cdot b_{0}\right]\textrm{ mod }m.$$
Transforming this expression according to Horner’s scheme, we obtain
$$\left(a\cdot b\right)\textrm{ mod }m=\left[\left(\ldots\left(a\cdot b_{63}\cdot2+a\cdot b_{62}\right)\cdot2+\ldots+a\cdot b_{1}\right)\cdot2+a\cdot b_{0}\right]\textrm{ mod }m.$$
Considering that for any $x$, $y$ and $m$ the identities are valid
$$\left(x+y\right)\textrm{ mod }m\equiv\left(\left(x\textrm{ mod }m\right)+\left(y\textrm{ mod }m\right)\right)\textrm{ mod }m,$$
When calculating the right side of our formula, we have the right to do the following: if there is a possibility that the sum of two terms will exceed $2^{64}$, we need to add the remainders from dividing these terms by $m$; similarly for the work. This technique guarantees that an overflow will never occur during the calculation.

## 1.3 Fibonacci number system (fibsys)
Fibonacci numbers are a sequence of natural numbers $f_i$, in which

```math
\begin{cases}f_{0}=f_{1}=1,\\f_{i}=f_{i-2}+f_{i-1}, & \forall i>1.\end{cases}
```
According to Zeckendorff's theorem, any positive integer can be uniquely represented as a sum of different Fibonacci numbers that does not include two consecutive Fibonacci numbers.
To factor a positive integer $x$ into a Zeckendorff sum, you need to do the following as long as $x > 0$:
- find the maximum Fibonacci number $f < x$;
- add $f$ to the Zeckendorff sum;
- subtract $f$ from $x$.

Recall that in a positional number system, the weight of each digit depends on its position in the number notation. Accordingly, the basis of a positional number system is a sequence of numbers that define the weight of each digit. For example, for the decimal system the base is the sequence 1, 10, 100, 1000, 10000, 100000, etc.

**The Fibonacci number system** is a positional number system with two digits - 0 and 1, the basis of which is the Fibonacci numbers, starting with $f_i$: 1, 2, 3, 5, 8, 13, 21, 34, etc.
In order to guarantee the uniqueness of a number in the Fibonacci number system, the number must not contain two consecutive ones (Zeckendorff's theorem).

Write a program *fibsys* that converts the integer $0\leq x<2^{63}$ to the Fibonacci number system. The program must read the number $x$ from the standard input stream and output to the standard output stream a sequence of zeros and ones that forms the Fibonacci notation of the number $x$.

## 1.4 Intersection of sets (intersect)
Let $\mathbb{N}_{32}$ be the set of natural numbers from 0 to 31. Given two sets $A \subseteq \mathbb{N}\_{32}$ and $B\subseteq\mathbb{N}\_{32}$. Write a program intersect.c that calculates the intersection of the sets $A$ and $B$. The program must output to standard output the elements of set $A\cap B$, sorted in ascending order. It is prohibited to use arrays to store sets: each set must be represented by a 32-bit integer such that if its $i$-th bit is 1, then the number $i$ belongs to the set.

## 1.5 Factorial's zeros
Write a function, named `factorial`, that calculates the value of given number's factorial: $n! = 1 \cdot 2 \cdot 3 \cdot ... \cdot (n - 1) \cdot n$. Write a function, named `factorial_zeros`, that calculates how many zeros are in the end of `factorial(n)` without its direct calculation.

## 1.6 Josephus Flavius task
In 67 AD during the Jewish-Roman War, Josephus Flavius and forty rebels were trapped in a cave. Preferring being suicided to captivity, they decided to stand in a circle and kill every third of the survivors. Josephus wanted to stay alive and realized where he had to stand in the circle to stay alive in the series of executions. So he lived to tell the tale.

Let's assume that there are $N$ rebels, numerated from $0$ to $N-1$, and they start to kill themselves starting from $0$ and then killing each $K$'th of them. Write a program, which helps Josephus to survive depending on given $N$ and $K$.
