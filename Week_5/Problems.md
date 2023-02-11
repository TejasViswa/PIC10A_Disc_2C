# Problems

## Question 1
Write a program that prints all even numbers between 1 and 100 but stops after it has
printed the number 20. The program should use the "break" statement to stop after
printing 20. The program should also skip printing the number 4.
### Solution
```c++
#include <iostream>
using namespace std;
int main() {
  int i = 2;
  while (i <= 100) {
    if (i == 4) {
      i += 2;
      continue;
    }
    if (i > 20) {
      break;
    }
    cout << i << endl;
    i += 2;
  }
  return 0;
}
```

## Question 2
Check if a given number is prime or not
### Solution
```c++
#include <iostream>
using namespace std;

int main() {

  int i, n;
  bool is_prime = true;

  cout << "Enter a positive integer: ";
  cin >> n;

  // 0 and 1 are not prime numbers
  if (n == 0 || n == 1) {
    is_prime = false;
  }

  // loop to check if n is prime
  for (i = 2; i <= n/2; ++i) {
    if (n % i == 0) {
      is_prime = false;
      break;
    }
  }

  if (is_prime)
    cout << n << " is a prime number";
  else
    cout << n << " is not a prime number";

  return 0;
}

```

