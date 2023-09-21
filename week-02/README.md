# Week 02. Python Basics II.

### Presentations

- [Class 1 Presentation](presentation_1_4x3.pdf);
- [Class 2 Presentation](presentation_2_4x3.pdf).

### Good to Read

- Class 1:
 - [Collections](https://fadeevlecturer.github.io/python_lectures/notebooks/python/collections.html);
 - [Sequences](https://fadeevlecturer.github.io/python_lectures/notebooks/python/sequences.html);
 - [List Internals](https://habr.com/ru/articles/273045/)
 - [Tuple vs List](https://www.geeksforgeeks.org/python-difference-between-list-and-tuple/);
 - [Dict](https://medium.com/@artturi-jalli/python-dictionary-a-complete-guide-538292873053);
 - [Dict Internals](https://habr.com/ru/articles/432996/);
 - [Iterators](https://habr.com/ru/articles/488112/);
 - [Garbage Collector I](https://habr.com/ru/articles/417215/);
 - [Garbage Collector II](https://fadeevlecturer.github.io/python_lectures/notebooks/python/garbage_collector.html);
 - [Type hints](https://habr.com/ru/companies/lamoda/articles/432656/).
- Class 2:
 - [Functional programming](https://habr.com/ru/articles/555378/);
 - [Modules & Packages](https://habr.com/ru/articles/718828/);
 - [Requirements](https://semakin.dev/2020/04/requirements_txt/?ysclid=lmsfzwiheg711857653);
 - [Files & I/O I](https://eldoyle.github.io/PythonIntro/08-ReadingandWritingTextFiles/);
 - [Files & I/O II](https://habr.com/ru/companies/selectel/articles/547290/);
 - [Files & I/O III](https://fadeevlecturer.github.io/python_lectures/notebooks/python/filesystem.html);
 - [Files & I/O IV](https://fadeevlecturer.github.io/python_lectures/notebooks/python/files.html).

### Coding Homework

## 2.1 Maximum sum of consecutive array elements (maxk).
Given an integer array whose size does not exceed 10000 and a number **k**, which is less than or equal to the length of the array. 
Write a *maxk* program that determines which consecutive elements of an array have the maximum sum.
The program must read the size of the array, its elements, and the number **k** from the standard input stream, and then print the maximum sum **k** of consecutive array elements to the standard output stream.
The program is prohibited from accessing the same array element more than twice, as well as declaring any auxiliary arrays.

## 2.2 Greatest prime divisor (primediv).
Write a program *primediv* that calculates the greatest prime divisor of a number **x**. 
The number **x** is entered from the standard input stream, and it is known that $-2^{31} <= x < 2^{31}$.
The program must use the sieve of Eratosthenes to construct an array of prime numbers.

## 2.3 Saddle point in a matrix (saddlepoint).

**Definition.** An element of a two-dimensional array is called a **saddle element** if it is both the largest in its row and the smallest in its column.

An integer two-dimensional array is given, the size of which does not exceed $10 \times 10$. It is known that all elements of the array are different. Write a program saddlepoint.c that determines the saddle point in this map.

The program must read from the standard input the number of rows and columns of a two-dimensional array and its elements. The program should output to the standard stream the coordinates of the found saddle point or the word “none” if the saddle point does not exist.

The program is prohibited from accessing the same array element twice.

## 2.4 Array Reversal Function (revarray).

TODO
