# Exercises

## Question 1
Write a program that reads in an 4 digit integer and breaks it into a sequence of individual digits. For example, the input 1638 is displayed as
```
Please enter the input sequence: 1638
1 6 3 8
```
### Hint:
Any number mod (using the modulo '%' operator to get the remainder) with 10 can help you extract the digit in unit's place (eg: 15 % 10 gives 5, 227 % 10 gives 7). Any number that is integer divided by 10 is rounded to the nearest multiple of 10 (eg: 157 / 10 gives 15, 14 / 10 gives 1). Do you notice a pattern here with how you can extract digits at the unit's place with modulo and push the digits towards the unit's place using the integer division?

## Question 2
Write a program to swap two variables (both with and without a temporary variable). For example, let a = 5 and b = 10:
```
Before swapping.
a = 5, b = 10

After swapping.
a = 10, b = 5
```
### Hint:
Using another temporary variable we can store the value of one of variables temporarily while it is being copied onto. ie: When a is assigned to b, the value of b is lost and assigning b to a now would mean that a is essentially unchanged (a holds the same value). A temporary variable can help resolve this issue.
If using a temporary variable is not allowed then a bit of math can help. You can add the two variables and subtract one with the other to swap the values. Alternatively, you can use multiplication and division in the same way.

## Question 3
Write a program that reads two times in military format (0900, 1730) and prints the number of hours and minutes between the two times. Here is a sample run. Assume that the second time is always greater than the first.
```
Please enter the first time: 0900
Please enter the second time: 1730
8 hours 30 minutes
```
### Hint:

