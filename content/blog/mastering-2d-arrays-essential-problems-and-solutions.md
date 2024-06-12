---
layout: blog
title: "Mastering 2D Arrays: Essential Problems and Solutions"
description: This comprehensive guide builds upon your knowledge of 1D arrays
  and dives into the exciting world of 2D arrays. Here, you'll find real-world
  problems and step-by-step solutions to hone your programming skills. From
  printing matrices to complex operations like matrix multiplication and wave
  printing, this post equips you to tackle a wide range of 2D array challenges!
date: 2024-06-12
---
Arrays are fundamental data structures in programming, and understanding them is crucial for any developer. In this post, we will delve into various 2D array problems, ordered by increasing difficulty. If you're new to arrays, consider checking out our previous post on [1D Array Problems](https://virajs.top/blog/mastering-array-problems-from-basics-to-advanced/). Let's get started!

## 1. Printing a 3x3 Matrix:

**Problem Statement:** Write a program to print a 3x3 matrix given in a 2D array.

```cpp
#include <iostream>
using namespace std;
int main()
{
    int a[3][3] = {{1, 2, 3},
                   {4, 5, 6},
                   {7, 8, 9}};
    for (int i = 0; i < 3; i++)
    {
        for (int j = 0; j < 3; j++)
        {
            cout << a[i][j] << " ";
        }
        cout << endl;
    }
    return 0;
}
```

**Output:**

```bash
1 2 3 
4 5 6 
7 8 9
```

## 2. Adding Two 3x3 Matrices:

**Problem Statement:** Write a program to add two 3x3 matrices given in a 2D array.

```cpp
#include <iostream>
using namespace std;
int main()
{
    int a[3][3] = {{1, 2, 3},
                   {4, 5, 6},
                   {7, 8, 9}};
    int b[3][3] = {{1, 2, 3},
                   {4, 5, 6},
                   {7, 8, 9}};
    int c[3][3];
    for (int i = 0; i < 3; i++)
    {
        for (int j = 0; j < 3; j++)
        {
            c[i][j] = a[i][j] + b[i][j];
            cout << c[i][j] << "  ";
        }
        cout << endl;
    }
    return 0;
}
```

**Output:**

```bash
2   4   6  
8   10  12  
14  16  18
```

## 3. Finding Principal and Secondary Diagonals:

**Problem Statement:** Find the principal diagonal elements and secondary diagonal 

```cpp
#include <iostream>
using namespace std;
int main()
{
    int a[3][3] = {{1, 2, 3}, // 0,2 1,1 2,0
                   {4, 5, 6},
                   {7, 8, 9}};
    cout << "Primary Diagonal Matrix: " << endl;
    for (int i = 0; i < 3; i++)
    {
        for (int j = 0; j < 3; j++)
        {
            if (i == j)
            {
                cout << a[i][j] << " ";
            }
        }
    }
    cout << endl
         << "Secondary Diagonal Matrix: " << endl;
    int temp = 2;
    for (int i = 0; i < 3; i++)
    {
        cout << a[i][temp] << " ";
        temp--;
    }
    return 0;
}
```

**Output:**

```bash
Primary Diagonal Matrix: 
1 5 9 
Secondary Diagonal Matrix: 
3 5 7
```

## 4. Searching an Element in a 2D Array:

**Problem Statement:** Write a program to find a given element in an array. If the element is not found, print "Element not found".

```cpp
#include <iostream>
using namespace std;
int main()
{
    int a[3][3] = {{1, 2, 3},
                   {4, 5, 6},
                   {7, 8, 9}};
    int key = 11;
    int temp = 0;
    for (int i = 0; i < 3; i++)
    {
        for (int j = 0; j < 3; j++)
        {
            if (a[i][j] == key)
            {
                cout << "Element is present at : " << endl
                     << "row " << i + 1 << " column " << j + 1 << endl;
                temp++;
            }
        }
    }
    if (temp == 0)
    {
        cout << "Element Not found" << endl;
    }
    return 0;
}
```

**Output:**

```bash
Element Not found
```

## 5. Storing Student Roll No. and Marks:

**Problem Statement:** Write a program to store roll number and marks of 4 students in a matrix.

```cpp
#include <iostream>
using namespace std;
int main()
{
    int a[4][2];
    for (int i = 0; i < 4; i++)
    {
        cout << "Roll no.: ";
        cin >> a[i][0];
        for (int j = 1; j < 2; j++)
        {
            cout << "Marks: ";
            cin >> a[i][j];
        }
    }
    for (int i = 0; i < 4; i++)
    {
        for (int j = 0; j < 2; j++)
        {
            cout << a[i][j] << " ";
        }
        cout << endl;
    }
    return 0;
}
```

**Output:**

```bash
Roll no.: 1
Marks: 100
Roll no.: 2
Marks: 90
Roll no.: 3
Marks: 60
Roll no.: 4
Marks: 80
1 100 
2 90 
3 60 
4 80 
```

## 6. Dynamic Student Marks Storage:

**Problem Statement:** Write a program to ask the user for the number of students and store their marks for three subjects in a matrix.

```cpp
#include <iostream>
using namespace std;

int main()
{
    int students;
    cout << "Enter the no. of Students: ";
    cin >> students;
    int arr[students][4];
    for (int i = 0; i < students; i++)
    {
        cout << "Roll Nol.: ";
        cin >> arr[i][0];
        for (int j = 1; j < 4; j++)
        {
            cout << "Marks: ";
            cin >> arr[i][j];
        }
    }
    for (int i = 0; i < students; i++)
    {
        for (int j = 0; j < 4; j++)
        {
            cout << arr[i][j] << " ";
        }
        cout << endl;
    }
    return 0;
}
```

**Output:**

```bash
Enter the no. of Students: 2
Roll Nol.: 001
Marks: 100
Marks: 98
Marks: 99
Roll Nol.: 002
Marks: 80
Marks: 89
Marks: 96
1 100 98 99 
2 80 89 96
```

## 7. Initializing a 5x5 Matrix with 10s:

**Problem Statement:** Write a program to store 10 at every index in a 5x5 matrix.

```cpp
#include <iostream>
using namespace std;

int main()
{

    int arr[5][5];

    for (int i = 0; i < 5; i++)
    {
        for (int j = 0; j < 5; j++)
        {
            arr[i][j] = 10;
        }
    }

    for (int i = 0; i < 5; i++)
    {
        for (int j = 0; j < 5; j++)
        {
            cout << arr[i][j] << " ";
        }
        cout << endl;
        
    }
    

    return 0;
}
```

**Output:**

```bash
10 10 10 10 10 
10 10 10 10 10 
10 10 10 10 10 
10 10 10 10 10 
10 10 10 10 10 
```

## 8. Finding Maximum and Minimum Elements:

**Problem Statement:** Find the maximum and minimum element and their index in a matrix.

```cpp
#include <iostream>
using namespace std;

int main()
{

    int a[3][3] = {{1, 2, 3},
                   {4, 5, 6},
                   {7, 8, 9}};

    int max = a[0][0];
    int min = a[0][0];

    for (int i = 0; i < 3; i++)
    {
        for (int j = 0; j < 3; j++)
        {
            if (a[i][j] > max)
            {
                max = a[i][j];
            }
            else if (a[i][j] < min)
            {
                min = a[i][j];
            }
        }
    }
    for (int i = 0; i < 3; i++)
    {
        for (int j = 0; j < 3; j++)
        {
            if (a[i][j] == max)
            {
                cout << "Max: " << max << endl;
                cout << "Index: " << i << ", " << j << endl;
            }
            if (a[i][j] == min)
            {
                cout << "Min: " << min << endl
                     << "Index: " << i << ", " << j << endl;
            }
        }
    }
    return 0;
}
```

**Output:**

```bash
Min: 1
Index: 0, 0
Max: 9
Index: 2, 2
```

## 9. Sum of an n*m Matrix:

**Problem Statement:** Write a program to find the sum of an n*m matrix.

```cpp
#include <iostream>
using namespace std;
int main()
{

    const int n = 3;
    const int m = 3;

    int arr[n][m] = {{1, 2, 3}, {4, 5, 6}, {7, 8, 9}};

    int sum = 0;

    for (int i = 0; i < n; i++)
    {
        for (int j = 0; j < m; j++)
        {
            sum += arr[i][j];
        }
    }

    cout << "SUM: " << sum;
    return 0;
}
```

**Output:**

```bash
SUM: 45
```

## 10. Sum of a Submatrix:

**Problem Statement:** Given a matrix, find the sum of the rectangle formed by two coordinates (l1, r1) and (l2, r2).

```cpp
#include <iostream>
using namespace std;
int main()
{

    int arr[5][5] = {{1, 2, 3, 4, 5},
                     {6, 7, 8, 9, 10},
                     {11, 12, 13, 14, 15},
                     {15, 17, 18, 19, 20},
                     {21, 22, 23, 24, 25}};

    // (l1,r1) = 1,1 (l2,r2) = 4,4
    int sum = 0;

    for (int i = 1; i < 5; i++)
    {
        for (int j = 1; j < 5; j++)
        {
            sum += arr[i][j];
        }
    }

    cout << "Sum:  " << sum << endl;

    return 0;
}
```

**Output:**

```bash
Sum:  256
```

## 11. Row with Maximum Sum:

**Problem Statement:** Given a matrix filled with 0s and 1s, find the row with the maximum number of 1s.

```cpp
#include <iostream>
using namespace std;
int main()
{
    int arr[3][3] = {{1, 2, 3}, {4, 5, 6}, {7, 8, 9}};
    int sum = 0;
    int x;
    for (int i = 0; i < 3; i++)
    {
        int rowSum = 0;
        for (int j = 0; j < 3; j++)
        {
            rowSum += arr[i][j];
        }
        if (rowSum > sum)
        {
            sum = rowSum;
            x = i;
        }
    }
    cout << "Max Sum: " << sum << endl
         << "Row: " << x;
    return 0;
}
```

**Output:**

```bash
Max Sum: 24
Row: 2
```

# 12. Row with Maximum 1s:

**Problem Statement:** Given a matrix filled with 0s and 1s, find the row with the maximum number of 1s.

```cpp
#include <iostream>
using namespace std;
int main()
{
    int arr[5][5] = {{1, 1, 0, 0, 0},
                     {1, 0, 0, 0, 1},
                     {1, 1, 1, 1, 1},
                     {1, 0, 0, 1, 0},
                     {0, 0, 0, 0, 0}};
    int maxOne = 0;
    int row;
    for (int i = 0; i < 5; i++)
    {
        int rowOne = 0;
        for (int j = 0; j < 5; j++)
        {
            if (arr[i][j] == 1)
            {
                rowOne++;
            }
        }
        if (rowOne > maxOne)
        {
            maxOne = rowOne;
            row = i;
        }
    }
    cout << "Row " << row << " is filled with max 1's" << endl;
    return 0;
}
```

**Output:**

```bash
Row 2 is filled with max 1's
```

# 13. Matrix Transpose (Printing):

**Problem Statement:** Print the transpose of a given matrix.

```cpp
#include <iostream>
using namespace std;
int main()
{
    int arr[3][3] = {{1, 2, 3}, {4, 5, 6}, {7, 8, 9}};

    for (int i = 0; i < 3; i++)
    {
        for (int j = 0; j < 3; j++)
        {
            cout << arr[i][j] << " ";
        }
        cout << endl;
    }
    cout << "Transpose of Given Matrix:" << endl;
    for (int i = 0; i < 3; i++)
    {
        for (int j = 0; j < 3; j++)
        {
            cout << arr[j][i] << " ";
        }
        cout << endl;
    }
    return 0;
}
```

**Output:**

```bash
1 2 3 
4 5 6 
7 8 9 
Transpose of Given Matrix:
1 4 7 
2 5 8 
3 6 9 
```

# 14. Matrix Transpose (Storing in Another Matrix):

**Problem Statement:** Store the transpose of a given matrix in another matrix.

```cpp
#include <iostream>
using namespace std;

int main()
{
    int arr[3][3] = {{1, 2, 3}, {4, 5, 6}, {7, 8, 9}};
    int transpose[3][3];

    for (int i = 0; i < 3; i++)
    {
        for (int j = 0; j < 3; j++)
        {
            cout << arr[i][j] << " ";
        }
        cout << endl;
    }
    for (int i = 0; i < 3; i++)
    {
        for (int j = 0; j < 3; j++)
        {
            transpose[i][j] = arr[j][i];
        }
    }
    cout << "Transpose of Given Matrix:" << endl;

    for (int i = 0; i < 3; i++)
    {
        for (int j = 0; j < 3; j++)
        {
            cout << transpose[i][j] << " ";
        }
        cout << endl;
    }
    return 0;
}
```

**Output:**

```bash
1 2 3 
4 5 6 
7 8 9 
Transpose of Given Matrix:
1 4 7 
2 5 8 
3 6 9 
```

# 15. In-place Matrix Transpose (Without Extra Matrix):

**Problem Statement:** Convert a square matrix into its transpose without using an extra matrix.

```cpp
#include <iostream>
using namespace std;

int main()
{

    int arr[3][3] = {{1, 2, 3}, {4, 5, 6}, {7, 8, 9}};

    for (int i = 0; i < 3; i++)
    {
        for (int j = 0; j < 3; j++)
        {
            cout << arr[i][j] << " ";
        }
        cout << endl;
    }

    int temp;

    int flag = 0;

    for (int i = 0; i < 3; i++)
    {
        for (int j = flag; j < 3; j++)
        {
            int temp = arr[j][i];
            arr[j][i] = arr[i][j];
            arr[i][j] = temp;
        }
        flag++;
    }

    cout << "Transpose: " << endl;

    for (int i = 0; i < 3; i++)
    {
        for (int j = 0; j < 3; j++)
        {
            cout << arr[i][j] << " ";
        }
        cout << endl;
    }

    return 0;
}
```

**Output:**

```bash
1 2 3 
4 5 6 
7 8 9 
Transpose: 
1 4 7 
2 5 8 
3 6 9 
```

# 16. Rotate Matrix 90 Degrees Clockwise:

**Problem Statement:** Rotate a matrix 90 degrees clockwise.

```cpp
#include <iostream>
using namespace std;

int main()
{

    int n, m;

    cout << "Enter the dimensions of matrix: " << endl
         << "M: ";
    cin >> m;
    cout << "N: ";
    cin >> n;

    int arr[m][n];

    cout << "Enter the elements in the matrix: " << endl;

    for (int i = 0; i < m; i++)
    {
        for (int j = 0; j < n; j++)
        {
            cin >> arr[i][j];
        }
    }

    for (int i = 0; i < m; i++)
    {
        for (int j = 0; j < n; j++)
        {
            cout << arr[i][j] << " ";
        }
        cout << endl;
    }

    cout << "Transpose: " << endl;
    int temp;
    int flag = 0;
    for (int i = 0; i < m; i++)
    {
        for (int j = flag; j < n; j++)
        {
            int temp = arr[j][i];
            arr[j][i] = arr[i][j];
            arr[i][j] = temp;
        }
        flag++;
    }

    for (int i = 0; i < m; i++)
    {
        for (int j = 0; j < n; j++)
        {
            cout << arr[i][j] << " ";
        }
        cout << endl;
    }
    cout << "Rotate 90degree: " << endl;

    for (int i = 0; i < m; i++)
    {
        for (int j = 0; j < n / 2; i++)
        {
            int temp = arr[i][j];
            arr[i][j] = arr[i][n - 1 - j];
            arr[i][n - 1 - j] = temp;
        }
    }

    for (int i = 0; i < m; i++)
    {
        for (int j = 0; j < n; j++)
        {
            cout << arr[i][j] << " ";
        }
        cout << endl;
    }

    return 0;
}
```

**Output:**

```bash
Enter the dimensions of matrix: 
M: 3
N: 3
Enter the elements in the matrix: 
1 2 3 4 5 6 7 8 9
1 2 3 
4 5 6 
7 8 9 
Transpose: 
1 4 7 
2 5 8 
3 6 9 
Rotate 90degree: 
7 4 1 
8 5 2 
9 6 3
```

# 17. Matrix Multiplication:

**Problem Statement:** Perform matrix multiplication of two matrices.

```cpp
#include <iostream>
using namespace std;

int main()
{

    int n, m;

    cout << "Enter the dimensions of matrix1: " << endl
         << "M: ";
    cin >> m;
    cout << "N: ";
    cin >> n;

    int arr1[m][n];

    cout << "Enter the elements in the matrix1: " << endl;

    for (int i = 0; i < m; i++)
    {
        for (int j = 0; j < n; j++)
        {
            cin >> arr1[i][j];
        }
    }

    int p, q;

    cout << "Enter the dimensions of matrix2: " << endl
         << "P: ";
    cin >> p;
    cout << "Q: ";
    cin >> q;

    int arr2[p][q];

    cout << "Enter the elements in the matrix2: " << endl;

    for (int i = 0; i < p; i++)
    {
        for (int j = 0; j < q; j++)
        {
            cin >> arr2[i][j];
        }
    }
    if (n != p)
    {
        cout << "Matrix cannot be multiplied";
    }
    else
    {
        int res[m][q];
        for (int i = 0; i < m; i++)
        {
            for (int j = 0; j < q; j++)
            {
                res[i][j] = 0;
                for (int k = 0; k < n; k++)
                {
                    res[i][j] += arr1[i][k] * arr2[k][j];
                }
            }
        }

        cout << "The resultant matrix is:" << endl;

        for (int i = 0; i < m; i++)
        {
            for (int j = 0; j < n; j++)
            {
                cout << res[i][j] << " ";
            }
            cout << endl;
        }
    }

    return 0;
}
```

**Output:**

```bash
Enter the dimensions of matrix1: 
M: 3
N: 3
Enter the elements in the matrix1: 
1 2 3 4 5 6 7 8 9
Enter the dimensions of matrix2: 
P: 3
Q: 3
Enter the elements in the matrix2: 
1 2 3 4 5 6 7 8 9
The resultant matrix is:
30  36  42 
66  81  96 
102 126 150 
```

# 18. Wave Printing (Reverse S):

**Problem Statement:** Print a matrix in a wave pattern (reverse S).

```cpp
#include <iostream>
using namespace std;
int main()
{

    int arr[3][3] = {{1, 2, 3}, {4, 5, 6}, {7, 8, 9}};

    for (int i = 0; i < 3; i++)
    {
        for (int j = 0; j < 3; j++)
        {
            cout << arr[i][j] << " ";
        }
        cout << endl;
    }

    cout << "Wave printing: " << endl;

    for (int i = 0; i < 3; i++)
    {
        if (i % 2 == 0)
        {
            for (int j = 0; j < 3; j++)
            {
                cout << arr[i][j] << " ";
            }
            cout << endl;
        }
        else
        {
            for (int k = 2; k >= 0; k--)
            {
                cout << arr[i][k] << " ";
            }
            cout << endl;
        }
    }

    return 0;
}
```

**Output:**

```bash
1 2 3 
4 5 6 
7 8 9 
Wave printing: 
1 2 3 
6 5 4 
7 8 9 
```

# 19. Wave Printing (Horizontal Waves):

**Problem Statement:** Print a matrix in a wave pattern (column-wise).

```cpp
#include <iostream>
using namespace std;
int main()
{

    int arr[3][3] = {{1, 2, 3}, {4, 5, 6}, {7, 8, 9}};

    for (int i = 0; i < 3; i++)
    {
        for (int j = 0; j < 3; j++)
        {
            cout << arr[i][j] << " ";
        }
        cout << endl;
    }

    cout << "Wave printing2: " << endl;

    for (int j = 0; j < 3; j++)
    {
        if (j % 2 == 0)
        {
            for (int i = 2; i >= 0; i--)
            {
                cout << arr[i][j] << " ";
            }
            cout << endl;
        }
        else
        {
            for (int k = 0; k < 3; k++)
            {
                cout << arr[k][j] << " ";
            }
            cout << endl;
        }
    }

    return 0;
}
```

**Output:**

```bash
1 2 3 
4 5 6 
7 8 9 
Wave printing2: 
7 4 1 
2 5 8 
9 6 3 
```

By practicing these problems, you'll gain a solid understanding of working with 2D arrays. Don't forget to check out our [1D Array Problems](https://virajs.top/blog/mastering-array-problems-from-basics-to-advanced/) post for more foundational concepts. Happy coding!
