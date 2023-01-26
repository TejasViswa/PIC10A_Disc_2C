# Problems

## Question 1
Find out if a given number is even or odd
```
Enter an integer: 23
23 is odd.
```
### Solution
```c++
#include <iostream>
using namespace std;

int main() {
  int n;

  cout << "Enter an integer: ";
  cin >> n;

  if ( n % 2 == 0)
    cout << n << " is even.";
  else
    cout << n << " is odd.";

  return 0;
}
```

## Question 2
Find out the greater among 2 given numbers
```
Enter two numbers: 23 57
57 is greater.
```
### Solution
```c++
#include <iostream>
using namespace std;

int main() {
  int a,b;

  cout << "Enter two numbers: ";
  cin >> a >> b;

  if ( a > b )
    cout << a << " is greater.";
  else
    cout << b << " is greater.";

  return 0;
}
```

## Question 3
Find out the greatest number of 3 given numbers
### Solution
```c++
#include <iostream>
using namespace std;

int main() {
  int a,b,c;

  cout << "Enter 3 numbers: ";
  cin >> a >> b >> c;

   if (a > b)
    {
        if (a > c)
            cout << a << " is the greatest. "<<endl;
        else
            cout << c << " is the greatest. "<<endl;
    }
    else
    {
        // Decided a is not greater than b.
        if (b > c)
            cout << b << " is the greatest. "<<endl;
        else
            cout << c << " is the greatest. "<<endl;
    }
  return 0;
}
```

## Question 4
Find out the middle number of 3 given numbers
### Solution
```c++
#include <iostream>
using namespace std;

int main() {
  int a,b,c;

  cout << "Enter 3 numbers: ";
  cin >> a >> b >> c;

   if (a > b)
    {
        if (b > c)
            cout << b << " is the middle number "<<endl;
        else if (a > c)
            cout << c << " is the middle number "<<endl;
        else
            cout << a << " is the middle number "<<endl;
    }
    else
    {
        // Decided a is not greater than b.
        if (a > c)
            cout << a << " is the middle number "<<endl;
        else if (b > c)
            cout << c << " is the middle number "<<endl;
        else
            cout << b << " is the middle number "<<endl;
    }
  return 0;
}
```
