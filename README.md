# Program-to-find-Smallest-Element-of-the-array-using-Recursion-in-CPP

Smallest Element of  the array using Recursion in C++
 

Here, in this page we will discuss the program to find smallest element of the array using recursion in C++. We are given with an array and we need to print the smallest element. We will discuss the approach using recursion and iteratively both to find the smallest element.

Example :

Input : arr[6]= {10, 7, 78, 67, 89, 12}
Output :  Smallest Element is : 7
Smallest Element of the array using Recursion in C++
Method 1 (Using Recursion):
In this method we will discuss the recursive solution to find the smallest element of an array. We will do the following steps to achieve the smallest element.

Create a recursive function say smallest_element(int n, int arr).
Base Condition : If(n==1) return arr[0].
Else, return min(arr[n-1], smallest_element(n-1, arr).
 
Time and Space Complexity :
Time Complexity : O(n), where n is the size of the array.
Space Complexity : O(1)
Smallest Element in C++
Related Pages
Finding Number of times x digit occurs in a given input
 
Finding number of integers which has exactly x divisors
 
Largest element in an array

Power of a Number

Prime Number

Code in C++
Run
#include<bits/stdc++.h>
using namespace std;

//Recursive Function
int smallest_element(int n, int arr[]){

   if(n==1) return arr[0];

   return min(arr[n-1], smallest_element(n-1, arr));
}

//Driver Code
int main(){

   int arr[] = {10, 45, 78, 34, 67};

   int n = sizeof(arr)/sizeof(arr[0]);

   cout<<"Smallest Element is "<<smallest_element(n, arr);
}
Output

Smallest Element is 10
Method 2 (Using Iteration):
In this method we will discuss the iterative solution to find the smallest element of an array. We will do the following steps to achieve the smallest element.

Create a variable say min_element and initialize it with INT_MAX.
Run a loop from 0 to n and set min_element = min(arr[i], min_element).
After Complete iteration print min_element.
Time and Space Complexity :
Time Complexity : O(n)
Space Complexity : O(1)
Code in C++
Run
#include<bits/stdc++.h>
using namespace std;

int smallest_element(int n, int arr[]){

   int min_element = INT_MAX;

   for(int i=0; i<n; i++)
     min_element = min(arr[i], min_element);

   return min_element;
}

int main(){

   int arr[] = {10, 45, 78, 34, 67};

   int n = sizeof(arr)/sizeof(arr[0]);
 
   cout<<"Smallest Element is "<<smallest_element(n, arr);
}
Output

Smallest Element is 10
