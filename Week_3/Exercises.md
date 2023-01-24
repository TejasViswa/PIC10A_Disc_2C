# Exercises

## Question 1
Accept a value (in celsius) from the user and convert it into Farenheit using the formula:
```math
  (x \times \frac{9}{5}) + 32 = y
```
where $x$ is the value in Celsius and $y$ is in Farenheit

### Solution
```c++
#include <iostream>

using namespace std;

int main()
{
    double x;
    cout<<"Please enter a value in C: ";
    cin>>x;
    double y = (x*9/5)+32;
    cout<<"The value in Farenheit is: "<<y<<" deg F";
    return 0;
}
```

## Question 2
Accept a 3-digit number from the user and check if it is a palindrome.

A palindrome is number which remains the same even when reversed.

ie:
- 121 when reversed is still 121 and is hence a palindrome
- 555 when reversed is still 555 and is hence a palindrome
- 123 when reversed is 123 and is hence not a palindrome

### Solution
```c++
#include <iostream>

using namespace std;

int main()
{
    int x;
    cout<<"Please enter a number: ";
    cin>>x;
    int a = x%10; // This extracts the first digit from the right
    int b = (x/10)%10; // This extracts the middle digit
    int c = x/100; // This extracts the last digit from the right
    if(a==c)  // This checks if first digit is the same as last digit
    {
        cout<<"The number is a palindrome"<<endl;
    }
    else
    {
        cout<<"The number is not a palindrome"<<endl;
    }
    return 0;
}
```
