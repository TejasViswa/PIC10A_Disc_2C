# Exercises

## Prof's Question
Count the number of vowels in a given string
```c++
# include <iostream>
# include <string>

using namespace std;

// determine whether a character is a vowel
bool is_vowel(char character) {
    bool status_vowel;
    status_vowel = character == 'a' || character == 'A';
    status_vowel = status_vowel || character == 'e' || character == 'E';
    status_vowel = status_vowel || character == 'i' || character == 'I';
    status_vowel = status_vowel || character == 'o' || character == 'O';
    status_vowel = status_vowel || character == 'u' || character == 'U';

    return status_vowel;
}

// count number of vowels
int count_vowels(string str) {
    int length = str.length();
    int count = 0;
    for (int i = 0; i < length; i++) {
        if (is_vowel(str[i])) {
            count++;
        }
    }
    return count;
}


// main function
int main() {
    // input string
    cout << "Please input your string: " << endl;
    string str;
    getline(cin, str);

    cout << "Number of vowels in the string is " << count_vowels(str) << "." << endl;

    return 0;

}

```
Alternative Solution for the `is_vowel` function:
```c++
bool is_vowel(char character) {
    switch(character)
    {
        case 'a': case 'A':
        case 'e': case 'E':
        case 'i': case 'I':
        case 'o': case 'O':
        case 'u': case 'U': 
            return true;
        default:
            return false;
    }
}
```

## Question 1
Write a program to print a square with a function of given size and character
```
Enter the size of square: 5
Enter the character to create the square with: @

@ @ @ @ @
@       @
@       @
@       @
@ @ @ @ @

```
```
Enter the size of square: 3
Enter the character to create the square with: &

& & &
&   &
& & &

```
### Solution
```c++
#include <iostream>
using namespace std;

void drawSquare(int size, char c)
{
    for(int i=1; i<=size; i++)
    {
        for(int j=1; j<=size; j++)
        {
            if(i==1 || i==size)
                cout<<c<<' ';
            else if(j==1 || j==size)
                cout<<c<<' ';
            else
                cout<<"  ";
        }
        cout<<endl;
    }
}

int main() {
    int size;
    char c;
    cout << "Enter the size of square: ";
    cin>>size;
    cout << "Enter the character to create the square with: ";
    cin>>c;
    
    drawSquare(size,c);

    return 0;
}
```

## Question 2
An Armstrong number of three digits is an integer such that the sum of the cubes of its digits is equal to the number itself. For example, 371 is an Armstrong number since 3^3 + 7^3 + 1^3 = 371. Other examples: 0,1,153,370,371,407,etc
Write a program to check if a given number is an armstrong number.
```
Please enter an integer: 371
371 is an armstrong number
```
### Solution
```c++
#include <iostream>
using namespace std;

bool isArmstrong(int num)
{
    int originalNum = num, rem = 0, result = 0;
    
    while (originalNum != 0) {
        // rem contains the last digit
        rem = originalNum % 10;
        
        result += rem * rem * rem;
        
        // removing last digit from the orignal number
        originalNum /= 10;
    }
    
    return (result==num);
}

int main() {
    int num;
    cout << "Enter a three-digit integer: ";
    cin >> num;

    if (isArmstrong(num))
        cout << num << " is an Armstrong number.";
    else
        cout << num << " is not an Armstrong number.";

    return 0;
}
```
An extension of the above problem is to print all 3-digit armstrong numbers.
### Solution
```c++
#include <iostream>
using namespace std;

bool isArmstrong(int num)
{
    int originalNum = num, rem = 0, result = 0;
    
    while (originalNum != 0) {
        // rem contains the last digit
        rem = originalNum % 10;
        
        result += rem * rem * rem;
        
        // removing last digit from the orignal number
        originalNum /= 10;
    }
    
    return (result==num);
}

int main() {
    cout << "The 3 digit armstrong numbers are:"<<endl;
    
    for(int i=0; i<=999; i++)
    {
        if (isArmstrong(i))
            cout << i <<endl;
    }

    return 0;
}
```
