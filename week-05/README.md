# Week 05. Asymptotic Complexity.

### Presentations

- [Class 1 & 2 Presentation](week5.pdf).

### Good to Read

- [Asymptotic Complexity](https://www.youtube.com/watch?v=cXCuXNwzdfY&t=303s&ab_channel=AlekOS);
- [Python Docs](https://docs.python.org/3/index.html);
- [Binary Search (for int)](https://neerc.ifmo.ru/wiki/index.php?title=%D0%A6%D0%B5%D0%BB%D0%BE%D1%87%D0%B8%D1%81%D0%BB%D0%B5%D0%BD%D0%BD%D1%8B%D0%B9_%D0%B4%D0%B2%D0%BE%D0%B8%D1%87%D0%BD%D1%8B%D0%B9_%D0%BF%D0%BE%D0%B8%D1%81%D0%BA);
- [Heap](https://habr.com/ru/articles/263765/).
- [Bubble Sort](https://habr.com/ru/articles/204600/)
- [Insertion Sort](https://habr.com/ru/articles/181271/)

### Coding Homework

## 5.1. Binary search.
Let a sorted array of **n** elements be given, where 0 < **n** <= 10^, target value **k** and type of sorting: -1 - descending, 1 - ascending;
Write a function that find for the value of **k** in an array and returns the index of the first occurrence of value, if the value of **k** is not found, return -1.

## 5.2. Shortest superstring (superstr).
Let a set of **n** strings be given, where 0 < **n** <= 10. 
It is known that none of these strings is a substring of another string. 
Write a program function that calculates the length of the shortest string containing all these strings as substrings.
The program must read the number **n** and then **n** strings from the standard input stream. 
The length of the shortest line containing all lines read should be printed to standard output.

## 5.3. Sums forming powers of two (power2).
Let a sequence of **n** non-repeating integers be given, where 0 < **n** <= 24, and each integer is in the range from $10^{-6}$ to $10^{-6}$.
Write a program function that calculates how many non-empty combinations of numbers from a sequence exist such that the sum of the numbers in the combination is equal to the power of the number **n**.
The program must read from the standard input the number **n**, and then **n** the numbers that form the sequence. The program should print the number of combinations to standard output.

## 5.4. Bidirectional bubble sort function (bubblesort). [click](https://en.wikipedia.org/wiki/Cocktail_shaker_sort)
In classical bubble sort, the sequence being sorted is always passed in one direction.
Modify the bubble sort algorithm so that it alternates passes through the sequence from left to right and from right to left.
Write a bubblesort function that performs a bidirectional bubble sort of an arbitrary sequence. The function must be declared as
```Python
def bubblesort(
  nel: int,
  compare: Callable[[int, int], int],
  swap: Callable[[int, int], None],
) -> None:
  pass
```
where,
  - nel is number of elements in the sequence;
  - compare is a comparison function that returns -1 if the first argument is less than the second, 0 if the elements are equal, 1 otherwise;
  - swap — pointer to the function for exchanging i-th and j-th elements of the sequence.
