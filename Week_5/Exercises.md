# Exercise

## Question 1
Write a program that prints the multiplication table for 1 to 10 using nested for loops
### Solution
```c++
#include <iostream>
using namespace std;
int main()
{
  for (int i = 1; i <= 10; i++) {
    for (int j = 1; j <= 10; j++) {
      cout << i * j << '\t';
    }
    cout << endl;
  }
  return 0;
}
```

## Question 2
Write a program that asks the user to enter a number and then prints the factorial of
that number using a do-while loop. A factorial of a number is the product of all
positive integers less than or equal to that number.

### Note: This solution uses a do-while loop, you may use a while loop as well

### Solution
```c++
#include <iostream>
using namespace std;
int main() 
{
  int number, factorial = 1;
  cout << "Enter a positive integer: ";
  cin >> number;
  int i = 1;
  do {
    factorial *= i;
    i++;
  } while (i <= number);
  cout << "The factorial of " << number << " is " << factorial << endl;
  return 0;
}
```
