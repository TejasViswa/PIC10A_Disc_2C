# Problems

## Question 1:
Write a program to emulate a simple calculator using switch statements.
```
Enter an operator (+, -, *, /): +
Enter two numbers: 
2.3
4.5
2.3 + 4.5 = 6.8
```
```
Enter an operator (+, -, *, /): -
Enter two numbers: 
2.3
4.5
2.3 - 4.5 = -2.2
```
### Solution
```c++
// Program to build a simple calculator using switch Statement
#include <iostream>
using namespace std;

int main() {
    char oper;
    float num1, num2;
    cout << "Enter an operator (+, -, *, /): ";
    cin >> oper;
    cout << "Enter two numbers: " << endl;
    cin >> num1 >> num2;

    switch (oper) {
        case '+':
            cout << num1 << " + " << num2 << " = " << num1 + num2;
            break;
        case '-':
            cout << num1 << " - " << num2 << " = " << num1 - num2;
            break;
        case '*':
            cout << num1 << " * " << num2 << " = " << num1 * num2;
            break;
        case '/':
            cout << num1 << " / " << num2 << " = " << num1 / num2;
            break;
        default:
            // operator is doesn't match any case constant (+, -, *, /)
            cout << "Error! The operator is not correct";
            break;
    }

    return 0;
}
```
## Question 2:
Write a program to enter a sequence of non-negative integers and find their sum and print if the sum is a multiple of 3, 5 or both. The sequence of inputs gets terminated when the user enters -1.
```
Input(Enter -1 to quit): 1 2 1 8 8 9 -1
Output: 29 is neither a multiple of 3 nor 5
```
```
Input(Enter -1 to quit): 7 8 -1 
Output: 15 is multiple of both 3 and 5
```
```
Input(Enter -1 to quit): 2 1 3 -1 
Output: 6 is multiple of 3
```
### Solution
You can use a while loop to keep checking if -1 was entered
```c++
#include <iostream>
using namespace std;
int main()
{
    int x = 0, sum = 0;
    cout<<"Input(Enter -1 to quit): ";
    while(x!=-1)
    {
        sum+=x;
        cin>>x;
    }
    cout<<"\nOutput: "<<sum;
    
    if( sum % 3 == 0 && sum % 5 == 0 )
    {
        cout<<" is a multiple of both 3 and 5"
    }
    else if( sum % 3 == 0 )
    {
        cout<<" is a multiple of 3"
    }
    else if( sum % 5 == 0 )
    {
        cout<<" is a multiple of 5"
    }
    else
    {
        cout<<" is neither a multiple of 3 nor 5"
    }
    return 0;
}
```

## Question 3:
Print the following pattern:
```
* * *
$ $ $
* * *
$ $ $
* * *
$ $ $
```
### Solution
To print the above pattern, a simple for loop with n=6 is sufficient:
```c++
#include <iostream>
using namespace std;
int main()
{
    int n = 6;
    for(int i = 1; i <= n; i++)
    {
        if(i%2==1)
        {
            cout<<"* * *"<<endl;
        }
        else
        {
            cout<<"$ $ $"<<endl;
        }
    }
  
  return 0;
}
```
