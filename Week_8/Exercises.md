# Exercise

## Question 1
Create a function to print the sum of diagonals of a square array
### Solution
```c++
// A simple C++ program to find sum of diagonals
#include <iostream>
using namespace std;

void printDiagonalSums(int mat[][], int n)
{
	int principal = 0, secondary = 0;
	for (int i = 0; i < n; i++) {
		for (int j = 0; j < n; j++) {

			// Condition for principal diagonal
			if (i == j)
				principal += mat[i][j];

			// Condition for secondary diagonal
			if ((i + j) == (n - 1))
				secondary += mat[i][j];
		}
	}

	cout << "Principal Diagonal:" << principal << endl;
	cout << "Secondary Diagonal:" << secondary << endl;
}

// Driver code
int main()
{
  	int N = 4;
	int a[N][N] = { { 1, 2, 3, 4 }, { 5, 6, 7, 8 },
					{ 1, 2, 3, 4 }, { 5, 6, 7, 8 } };
	printDiagonalSums(a, N);
	return 0;
}

```
A more efficient solution:
```c++
// An efficient C++ program to find sum of diagonals
#include <iostream>
using namespace std;

const int MAX = 100;

void printDiagonalSums(int mat[][], int n)
{
	int principal = 0, secondary = 0;
	for (int i = 0; i < n; i++) {
		principal += mat[i][i];
		secondary += mat[i][n - i - 1];	
	}

	cout << "Principal Diagonal:" << principal << endl;
	cout << "Secondary Diagonal:" << secondary << endl;
}

// Driver code
int main()
{
  	int N = 4;
	int a[N][N] = { { 1, 2, 3, 4 }, { 5, 6, 7, 8 },
					{ 1, 2, 3, 4 }, { 5, 6, 7, 8 } };
	printDiagonalSums(a, N);
	return 0;
}

```
