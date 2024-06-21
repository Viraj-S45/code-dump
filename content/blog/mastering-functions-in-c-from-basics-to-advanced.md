---
external: false
layout: blog
title: "Mastering Functions in C++: From Basics to Advanced"
description: Elevate your C++ skills with this comprehensive guide to functions!
  We'll explore various function tasks, starting with basic printing and
  progressing to advanced matrix operations.
date: 2024-06-21
---
Welcome back to our series on mastering C++ programming! In our previous posts, we explored array problems and 2D arrays. Today, we will delve into an essential aspect of C++: functions. Functions help in structuring code, making it reusable and manageable. Whether you're a beginner or advancing towards complex problems, understanding functions is crucial. Let's dive in!

## 1. Print Numbers in a Range

**Problem:** Write a function that prints all numbers from a given start to an end, inclusive.

```cpp
#include <iostream>
using namespace std;
void printNum(int a, int b)
{
    for (int i = a; i <= b; i++)
    {
        cout << i << " ";
    }
    return;
}
int main()
{
    printNum(2, 4);
    return 0;
}
```

**Output:**

```bash
2 3 4 
```


## 2. Print Elements of an Array

**Problem:** Write a function that prints all elements of a given array, separated by spaces.

```cpp
#include <iostream>
using namespace std;
void printArr(int arr[], int sizeArr){
    for (int i = 0; i < sizeArr; i++)
    {
        cout << arr[i] << " ";
    }
    return;
}
int main(){
int array [] = {1,2,3,4,5};
printArr(array, 5);
    return 0;
}
```

**Output:**

```bash
1 2 3 4 5 
```


## 3. Sum of Natural Numbers

**Problem:** Write a function that returns the sum of all natural numbers up to a given number 
N.

```cpp
#include <iostream>
using namespace std;
int sumNatural(int n)
{
    int sum = 0;
    for (int i = 1; i <= n; i++)
    {
        sum += i;
    }
    return sum;
}
int main()
{
    int sum = sumNatural(10);
    cout << "SUM: " << sum << endl;
    return 0;
}
```

**Output:**

```bash
SUM: 55
```


## 4. Sum of Digits in a Number

**Problem:** Write a function that returns the sum of all digits in a given number.

```cpp
#include <iostream>
using namespace std;
int sumOfDigits(int num)
{
    int sum = 0;
    int lastdig;
    while (num > 0)
    {
        lastdig = num % 10;
        sum += lastdig;
        num /= 10;
    }
    return sum;
}
int main()
{
    int sum = sumOfDigits(15);
    cout << sum << endl;
    return 0;
}
```

**Output:**

```bash
6
```


## 5. Count Even and Odd Numbers in an Array

**Problem:** Write a function that counts and prints the number of even and odd numbers in a given array.

```cpp
#include <iostream>
using namespace std;
void countEvenOdd(int arr[], int arrSize)
{
    int evenCount = 0;
    int oddCount = 0;
    
    for (int i = 0; i < arrSize; i++)
    {
        if (arr[i] % 2 == 0)
        {
            evenCount++;
        }
        else
            oddCount++;
    }
    cout << "Odd: " << oddCount << " Even: " << evenCount << endl;
}
int main()
{
    int arr[] = {1, 2, 3, 4, 5, 6, 7, 8, 9, 10};
    countEvenOdd(arr, size(arr));

    return 0;
}
```

**Output:**

```bash
Odd: 5 Even: 5
```


## 6. Maximum and Minimum in an Array

**Problem:** Write a function that prints the maximum and minimum numbers in a given array.

```cpp
#include <iostream>
using namespace std;
void maxMinNum(int arr[], int arrSize)
{
    int max = arr[0];
    int min = arr[0];
    for (int i = 0; i < arrSize; i++)
    {
        if (arr[i] > max)
        {
            max = arr[i];
        }
        else if (arr[i] < min)
        {
            min = arr[i];
        }
    }
    cout << "Max: " << max << endl
         << "Min: " << min << endl;
}
int main()
{
    int arr[] = {1, 2, 3, 4, 5, 6, 7, 8, 9};
    maxMinNum(arr, size(arr));
    return 0;
}
```

**Output:**

```bash
Max: 9
Min: 1
```


## 7. Check Prime Number

**Problem:** Write a function that checks whether a given number is prime. If the number is prime, return 0; otherwise, return 1.

```cpp
#include <iostream>
using namespace std;
int isPrime(int n)
{
    int flag = 0;
    if (n == 1)
    {
      return 0;
    }
    
    else if (n == 2)
    {
        return 1;
    }
    for (int i = 2; i < n; i++)
    {

        if (n % i == 0)
        {
            flag++;
        }
    }
    if (flag == 0)
    {
        return 0;
    }
    else
        return 1;
}
int main()
{
    cout << isPrime(8) << endl;
    return 0;
}
```

**Output:**

```bash
1
```


## 8. Total Prime Numbers in an Array

**Problem:** Write a function that prints the total number of prime numbers in a given array.

```cpp
#include <iostream>
using namespace std;
int isPrime(int n)
{
    int flag = 0;
    if (n == 1)
    {
        return 1;
    }

    else if (n == 2)
    {
        return 0;
    }
    for (int i = 2; i < n; i++)
    {

        if (n % i == 0)
        {
            flag++;
        }
    }
    if (flag == 0)
    {
        return 0;
    }
    else
        return 1;
}
void countPrime(int arr[], int arrSize)
{
    int count = 0;
    for (int i = 0; i < arrSize; i++)
    {
        if (isPrime(arr[i]) == 0)
        {
            count++;
        }
    }
    cout << "Total Number of Prime numbers: " << count << endl;
}
int main()
{
    int arr[] = {1, 2, 3, 4, 5, 6, 7, 8, 9, 10};
    countPrime(arr, size(arr));
    return 0;
}
```

**Output:**

```bash
Total Number of Prime numbers: 4
```


## 9. Factorial of a Number

**Problem:** Write a function that returns the factorial of a given number.

```cpp
#include <iostream>
using namespace std;
int factorial(int n)
{
    int factorial = 1;
    for (int i = 1; i <= n; i++)
    {
        factorial *= i;
    }
    return factorial;
}
int main()
{
    cout << factorial(5)<<endl;
    return 0;
}
```

**Output:**

```bash
120
```


## 10. Merge Two Arrays

**Problem:** Write a function that merges two given arrays into a single  array.

```cpp
#include <iostream>
using namespace std;
void mergeArr(int arr1[], int arrSize1, int arr2[], int arrSize2)
{
    int size = arrSize1 + arrSize2;
    int merge[size];
    for (int i = 0; i < arrSize1; i++)
    {
        merge[i] = arr1[i];
    }
    int flag = 0;
    for (int i = arrSize1; i < size; i++)
    {
        merge[i] = arr2[flag];
        flag++;
    }
    for (int i = 0; i < size; i++)
    {
        cout << merge[i] << " ";
    }
    cout << endl;
}
int main()
{
    int arr1[] = {1, 2, 3, 4, 5};
    int arr2[] = {6, 7, 8, 9, 10};
    mergeArr(arr1, size(arr1), arr2, size(arr2));
    return 0;
}
```

**Output:**

```bash
1 2 3 4 5 6 7 8 9 10 
```


## 11. Find Duplicates in an Array

**Problem:** Write a function that finds and prints duplicate elements in a given array.

```cpp
#include <iostream>
using namespace std;
void findDups(int arr[], int arrSize)
{
    cout << "Duplicates: ";
    for (int i = 0; i < arrSize; i++)
    {
        for (int j = i + 1; j < arrSize; j++)
        {
            if (arr[i] == arr[j])
            {
                cout << arr[i] << " ";
                break;
            }
        }
    }
}
int main()
{
    int arr[] = {1, 2, 3, 4, 5, 4, 5, 6, 7, 8, 8, 9};
    findDups(arr, size(arr));
}
```

**Output:**

```bash
Duplicates: 4 5 8 
```


## 12. Matrix Multiplication

**Problem:** Write a function that multiplies two given matrices and returns the resultant matrix.

```cpp
#include <iostream>
using namespace std;
void matrixMultiplication(int arr1[3][3], int arr2[3][3])
{
    int arr3[3][3];
    for (int i = 0; i < 3; i++)
    {
        for (int j = 0; j < 3; j++)
        {
            arr3[i][j] = 0;
            for (int k = 0; k < 3; k++)
            {
                arr3[i][j] += arr1[i][k] * arr2[k][j];
            }
        }
    }
    cout << "The resultant matrix is : " << endl;
    for (int i = 0; i < 3; i++)
    {
        for (int j = 0; j < 3; j++)
        {
            cout << arr3[i][j] << " ";
        }
        cout << endl;
    }
}
int main(){
    int arr1[3][3] = {{1,2,3},{4,5,6},{7,8,9}};
    int arr2[3][3] = {{1,2,3},{4,5,6},{7,8,9}};
    matrixMultiplication(arr1,arr2);
    return 0;
}
```

**Output:**

```bash
The resultant matrix is : 
30 36 42 
66 81 96 
102 126 150 
```


Mastering functions in C++ is a significant step towards becoming proficient in programming. By solving these problems, you'll gain a deeper understanding of how functions can simplify complex tasks and enhance code reusability. Don't forget to check out our previous posts on [array problems](#) and [2D arrays](#) for more practice.
