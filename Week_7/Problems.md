# Problems

## Question 1
Write a progam to merge two arrays
```c++
#include <iostream>
using namespace std;

int main()
{
    int arr1[] = {1,2,3,4,5};
    int N1 = 5;
    int arr2[] = {7,7,7,7,7,7};
    int N2 = 6;

    int arr3[N1+N2];
    int N, i = 0, j = 0;
    if(N1 > N2)
    {
        N = N1;
    }
    else
    {
        N = N2;
    }
    
    while(i<N)
    {
        arr3[j] = arr1[i];
        j++;
        arr3[j] = arr2[i];
        j++;
        i++;
        
    }
    
    while(i<N1)
    {
        arr3[j] = arr1[i];
        i++;
        j++;
    }
    
    while(i<N2)
    {
        arr3[j] = arr2[i];
        i++;
        j++;
    }
    
    for(int k = 0; k < (N1+N2); k++)
    {
        cout << arr3[k] << " ";
    }
    
    return 0;
}
```
